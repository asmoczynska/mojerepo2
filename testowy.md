```mermaid
sequenceDiagram
    title Przepływ uwierzytelniania SAML 2.0 Artifact Binding (WK)

    actor User as Użytkownik
    participant FE as Frontend (FE)
    participant BE as Backend (BE)
    participant WK as Auth Service<br/>(WK / Węzeł Krajowy)
    participant Redis as Redis<br/>(Session Store)

    %% Krok 1 — Inicjalizacja logowania

    User->>FE: Kliknięcie „Przejdź"

    FE->>BE: GET /web/api/authentication/init-parameters

    BE->>BE: Generowanie SAMLRequest

    BE-->>FE: 200 OK<br/>{ wkUrl, samlRequest }

    %% Krok 2 — Przekierowanie na stronę WK

    FE->>FE: Tworzy formularz HTML<br/>POST + SAMLRequest

    FE->>User: Auto-submit formularza

    User->>WK: POST wkUrl<br/>SAMLRequest=<base64>

    User<->>WK: Uwierzytelnienie użytkownika

    %% Krok 3 — Powrót z WK i utworzenie sesji

    WK->>User: Redirect POST<br/>/web/api/authentication/verify

    User->>BE: POST /web/api/authentication/verify<br/>Content-Type: application/x-www-form-urlencoded<br/>SAMLart=AAQAAMh48...

    BE->>WK: Artifact Resolution<br/>(server-to-server)

    WK-->>BE: Dane użytkownika<br/>PESEL, imię, nazwisko

    BE->>BE: Walidacja odpowiedzi SAML

    BE->>Redis: Utworzenie sesji

    Redis-->>BE: sessionId

    BE->>BE: Ustawienie cookie Session-Token

    BE->>BE: Ustawienie daty wygaśnięcia sessionValidTo

    alt Logowanie zakończone sukcesem
        BE-->>User: HTTP 303 Redirect
        Note right of BE: Set-Cookie: Session-Token
    else Błąd logowania
        BE-->>User: Redirect /error?traceId={traceId}
    end

    %% Krok 4 — Pobranie danych użytkownika

    User->>FE: Otwarcie aplikacji

    FE->>BE: GET /web/api/authentication/user-info<br/>Cookie: Session-Token

    BE->>Redis: Odczyt sesji

    Redis-->>BE: Dane sesji użytkownika

    BE-->>FE: 200 OK<br/>{ firstName,<br/>surname,<br/>sessionValidTo }

    FE->>User: Wyświetlenie danych użytkownika

    Note over FE,BE
      Każde kolejne wywołanie API
      automatycznie przesyła
      cookie Session-Token
    end

    %% Krok 5 — Korzystanie z aplikacji

    FE->>BE: GET /api/pids<br/>Cookie: Session-Token

    BE->>Redis: Odczyt sesji

    Redis-->>BE: Sesja aktywna

    BE-->>FE: Dane PID

    FE->>BE: POST /web/api/pids/revoke<br/>Cookie: Session-Token

    BE->>Redis: Odczyt sesji

    Redis-->>BE: Sesja aktywna

    BE-->>FE: Wynik operacji

    %% Krok 6 — Wylogowanie

    User->>FE: Kliknięcie „Wyloguj się"

    FE->>BE: POST /web/api/authentication/logout<br/>Cookie: Session-Token

    BE->>Redis: Usuń sesję

    Redis-->>BE: OK

    BE-->>FE: 200 OK

    FE->>FE: Usuń Session-Token

    FE->>User: Przekierowanie na stronę startową

    Note over BE,Redis
      Po usunięciu rekordu w Redis
      sesja jest nieważna.
      Nie jest wykorzystywana
      blacklista tokenów.
    end
    ```