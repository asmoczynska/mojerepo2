```mermaid
sequenceDiagram
    actor User as Użytkownik
    participant FE as Frontend
    participant BE as Backend
    participant WK as Węzeł Krajowy

    rect rgb(245,245,245)
    Note over User,WK: Inicjalizacja logowania

    User->>FE: Kliknięcie „Przejdź"

    FE->>BE: GET /web/api/authentication/init-parameters

    BE-->>FE: 200 OK\nwkUrl, samlRequest

    FE->>WK: POST SAMLRequest

    end

    rect rgb(245,245,245)
    Note over User,WK: Uwierzytelnienie w WK

    WK-->>User: Ekran logowania

    User->>WK: Uwierzytelnienie

    end

    rect rgb(245,245,245)
    Note over User,WK: Powrót do aplikacji

    WK->>BE: POST /web/api/authentication/verify\nSAMLart

    BE->>WK: Weryfikacja artefaktu SAML

    WK-->>BE: Dane użytkownika

    BE->>BE: Utworzenie sesji

    alt Logowanie zakończone sukcesem
        BE-->>User: HTTP 303 Redirect\nSet-Cookie Session-Token
    else Błąd logowania
        BE-->>User: Redirect /error?traceId={traceId}
    end

    end

    rect rgb(245,245,245)
    Note over FE,BE: Pobranie danych użytkownika

    FE->>BE: GET /web/api/authentication/user-info

    BE-->>FE: 200 OK\nDane użytkownika

    FE-->>User: Wyświetlenie danych użytkownika

    end

    rect rgb(245,245,245)
    Note over FE,BE: Korzystanie z aplikacji

    FE->>BE: GET /api/pids

    BE-->>FE: Dane PID

    FE->>BE: POST /web/api/pids/revoke

    BE-->>FE: Wynik operacji

    end

    rect rgb(245,245,245)
    Note over FE,BE: Wylogowanie

    User->>FE: Wyloguj się

    FE->>BE: POST /web/api/authentication/logout

    BE-->>FE: 200 OK

    FE-->>User: Strona startowa

    end
    ```