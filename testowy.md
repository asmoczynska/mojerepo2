# **D5.1 UC Specification and Analysis Results** 

## Executive summary



## 1 Introduction

Mobile vehicle registration certificates have been evolving rapidly in the past year thanks to both  European and international efforts. The European Union is actively working on the new Directive 2025/0096 (COD) on vehicle registration documents and vehicle registration data, which introduces a major shift in how we see the vehicle documents, making them part of the whole digital identity infrastructure. In addition, ISO has published a new standard ISO/IEC 7367-2:2026 on the mobile vehicle certificate defining the data model for the document, which is an important step towards interoperability. 

All those efforts have created a solid basis for the work package 5 in the LSP APTITUDE implementing the mobile vehicle registration certificate. WP5 is also drawing on the experiences of the previous pilot projects, especially the LSP POTENTIAL where mobile driving licenses were successfully tested. Thanks to the engagement of the WP5 participants and expertise of other work packages, we are pleased to present you the first deliverable of WP5 focusing on the use case specification and analysis.

### 1.1 Purpose of the document

This document summarises all the critical aspects of the mVRC ecosystem. The first part of the report is more business-oriented, whereas the second part focuses on the technical details. It is the result of eight months of discussions and intense technical work of the WP5 participants.

The objective is to present a comprehensive guide for the mobile vehicle registration certificates. The document includes and describes in detail the legal requirements and international standards, which WP5 will rely on in the development phase, mVRC lifecycle and WP5’s approach to them, presentation of the ecosystem together with actors and roles, user-centric summary of all the scenarios WP5 intends to test, and the technical details of the scenarios encompassing necessary protocols, interoperability requirements, and the mVRC rulebook. The report will also highlight core challenges and limitations, which will influence the implementation of the mVRC within the LSP APTITUDE. Last but not least, the report consolidates insights gathered during the stocktaking phase e.g. existing local solutions.

The report establishes a common knowledge base and shared understanding of the mVRC and should serve as a guide for the next stages of WP5 (implementation, testing, and validation). Some parts of this document are currently available on GitHub, for instance the mVRC rulebook, and may be subject to change as the project evolves. All the necessary updates will be made on GitHub. The links will be shared in this report or at the later stages of the project when the document is publicly available. 

### 1.2 Pilot objectives, Aptitude project context

The objective is to design, implement and demonstrate a mobile vehicle registration certificate using the EUDI wallet. The work package 5 intends to showcase that EU citizens can hold a secure and interoperable mVRC credential proving their ownership, holder, or consumer (delegated owner) rights for a specific vehicle.

This initiative facilitates transactions with the use of mVRCs across the EU. At this time, 11 countries in total participate in the work package 5: Austria, Czechia, France, Germany, Greece, Latvia, Lithuania, the Netherlands, Poland, Portugal, and Ukraine.

Our main ambitions are:
-	demonstrate a successful integration of the mVRC into the EUDI wallet framework, including secure issuance, storage, presentation and verification mechanisms;
-	ensure that the mVRC fully complies with the EUDIW Architecture Reference Framework (ARF) and eIDAS requirements and the upcoming Directive 2025/0096 (COD) on vehicle registration documents and vehicle registration data;
-	conduct interoperability tests within 9 scenarios including mVRC issuance and its remote and proximity presentation, delegation of the mVRC from an EUDI wallet user to another EUDI wallet user, delegation of the mVRC from an organisation to its customer, the remote or proximity presentation of the delegated mVRC, combined presentation of the mVRC and mDL. The scenarios are described in Chapter 6 and 8 of this document;
-	provide concrete recommendations regarding the technical feasibility of the use case, regulatory alignment and operational readiness of the mVRC within the EUDI wallet ecosystem.

Where appropriate, WP5 cooperates with other work packages, for example WP2 or WP7, to ensure interoperability and compliance with the existing standards and regulations.

## 2 Report methodology

This deliverable was developed through a structured data collection process and an iterative methodology, organised around four key activities:

-	Stakeholder engagement – all relevant participants involved in WP5 contributed their expertise, knowledge, and feedback throughout the process.
-	Input collection – regulatory, technical, and operational information was gathered from a wide range of relevant sources to ensure a comprehensive evidence base.
-	Analysis and report development – legal, technical, and organisational aspects were assessed and integrated to provide a consolidated overview of the current state of affairs. The resulting findings were synthesised into a coherent, validated, and project-aligned document designed to support subsequent WP5 activities and future project developments. 
-	Quality assurance – feedback was collected from all WP5 participants, as well as other APTITUDE stakeholders, in accordance with the project's established quality assurance procedures.

Throughout these activities, particular attention was given to maintaining alignment with related work packages, ensuring consistency and coherence across project outputs, especially with WP2 and WP7. This methodological approach is intended to ensure that the findings presented in this deliverable accurately reflect both the strategic objectives of the LSP APTITUDE and the capabilities and priorities of WP5.

### 2.1 Stakeholder involvement

Stakeholder participation played a central role in the stocktaking phase. WP5 engaged its members and ISO representatives, bringing together key actors from the mVRC ecosystem. Several forms of engagement were established:

-	**Stakeholder interviews** – conducted with mVRC issuers, wallet providers, private-sector organisations such as leasing companies, other WP5 members, and ISO representatives responsible for the ISO/IEC 7367-2:2026 standard.
-	**mVRC presentations by WP5 members** – participating countries were invited to present their national mVRC implementations to share experiences and provide inspiration.
-	**Written contributions from WP5 participants** – structured inputs were submitted by consortium members via email or questionnaires, including comments on scenario flows, technology aspects, and operational considerations.
-	**Workshops and working sessions** – several dedicated workshops were organised within the WP5 framework to discuss key topics, including use case scenarios, the mVRC rulebook, and delegation flows.

<br>

All WP5 participants contributed according to their expertise and responsibilities. The following stakeholder groups were involved:

-	**mVRC issuers** – provided insights on credential issuance, delegation mechanisms, scenario flows, data used during the testing phase, the mVRC rulebook, and the mVRC data model.
-	**Wallet providers** – shared technical perspectives related to wallet architecture, secure storage, user journeys, interoperability, and device-bound elements.
-	**Leasing companies** – contributed their perspectives on the delegation model.

This multi-stakeholder approach ensured that the analysis provides a realistic, operationally informed, and interoperability-focused perspective on mVRC deployment.

### 2.2 Sources and tools

The stocktaking exercise drew upon a variety of complementary information sources to establish a comprehensive understanding of the mVRC landscape. These sources included:

-	Relevant European regulatory frameworks, notably Directive 2025/0096 (COD) on vehicle registration documents and vehicle registration data, the eIDAS framework, and the related implementing acts (see Chapter 3 – State of Affairs).
-	International standards and technical specifications, with particular emphasis on ISO/IEC 7367-2:2026, ISO/IEC 18013-5:2021, and ISO/IEC 18013-7:2025 etc. (see Chapter 3 – State of Affairs).
-	A survey distributed to WP5 members via Nextcloud between 1 December 2025 and 26 January 2026. The survey gathered information on participants' involvement in the different use case scenarios, their respective roles within the ecosystem, and their level of familiarity with, and needs related to, the European Digital Identity Wallet (EUDIW) framework.
-	National vehicle registration practices, including country-specific information and existing mVRC implementation initiatives.
-	Workshops related to mapping of mVRC elements from the rulebook onto the local vehicle certificates to identify differences in presence and ensure the interoperability of the mVRC profile across different countries.

By combining documentary analysis with direct input from project participants, the stocktaking process captured a broad range of regulatory, technical, and operational perspectives relevant to the development of the mVRC ecosystem. 

## 3 State of affairs
### 3.1 Legal context
The current legal situation in the EU can be characterised as a transitional model, in which existing regulations based on physical registration documents are gradually being supplemented and replaced by those based on mobile solutions. In this context, the mVRC represents a natural step in the evolution of the EU legal system towards full digitisation, interoperability, and integration with the European digital identity infrastructure.

The basis for the uniform format of registration documents in the European Union is **the Council Directive 1999/37/EC**  of 29th of April 1999 on the registration documents for vehicles (together with Directive 2014/46/EU, which amends it), which harmonises the structure and scope of data contained in vehicle registration certificates, specifying both mandatory and optional elements. This regulation ensures the legibility and comprehensibility of documents in a cross-border context and enables their mutual recognition by the member states, which serves as the foundation for the further digitisation of documents, including the mVRC. At the same time, the development of the legal framework in this area is continuing through **the Proposal for a Directive of the European Parliament and of the Council 2025/0096 (COD) (COM(2025) 179 final)**, which is currently undergoing the co-decision procedure and provides for the repeal of Directive 1999/37/EC and the introduction of a modernised approach to vehicle registration and the management of registration data. The proposal is part of the broader EU Roadworthiness Package.

The proposal explicitly defines the concept of the mobile vehicle registration certificate (mVRC) as an electronic attestation of attributes that the member states are required to issue free of charge as part of the European Digital Identity Wallet in accordance with the eIDAS 2.0 regulation. It also specifies the key functionalities of this solution. The digital wallet must enable the user to download and securely store the issued mVRC, view it, and transmit it to authorised entities, including enforcement authorities, in a manner that allows for immediate verification of the vehicle’s roadworthiness. At the same time, the possibility of selective data sharing is provided, meaning that the user retains control over the scope of the information that they present. The system also provides for automatic or user-initiated data updates (e.g., in the event of a change in the vehicle’s status) and the ability to reissue the document within the wallet.

The amendment to the Directive 1999/37/EC aims to adapt the regulations to the digital reality and enhance interoperability among the member states. The proposal introduces a target model in which the mobile vehicle registration certificates will become the primary form of documentation in the member states, while ensuring data consistency between physical and digital versions and compliance with technical standards (including ISO), along with full integration into the European digital identity infrastructure. Moreover, it supports citizen safety by enabling quick and reliable verification of vehicle legality and effective tracking of their status in cross-border traffic.

A key element enabling the transition from traditional, physical vehicle registration documents to fully digital equivalents is undoubtedly **the eIDAS 2.0 Regulation** (EU Regulation 2024/1183 of the European Parliament and of the Council of 11th of April 2024 amending Regulation (EU) No 910/2014 as regards establishing the European Digital Identity Framework), which provides a coherent legal framework for electronic identification, trust services, and the management of digital identity attributes across the European Union. The main objective of eIDAS 2.0 is the introduction of **the European Digital Identity Wallet (EUDI Wallet)**, a digital service provided by a public or private entity authorised by a member state. The EUDI wallet allows users to securely authenticate themselves both online and offline, store and present digital identity attributes (e.g. PID, mDL, or mVRC documents), and perform electronic signing and other identity-related operations. The system ensures full control over the user data in accordance with the minimal disclosure principle. The system also enables pseudonymisation, and all the attestations must be certified and must comply with high security and accessibility standards. As a result, documents such as the mVRC can function as Electronic Attestations of Attributes (EAA) linked to the user’s identity, stored in the EUDI Wallet and shared on-demand with authorised entities. The wallet is recognised across all the EU member states, ensuring interoperability and secure use in both online and offline services. This solution allows mVRC to become an integral part of the European digital document ecosystem, combining functionality, security, and user control in a single tool.

The foundation for the digitisation of vehicle registries and cross-border data exchange is established by **the EU Directive 2015/413** of the European Parliament and of the Council of 11th of March 2015 on facilitating cross-border exchange of information on road-safety-related traffic offences, which sets a framework for sharing data on vehicles and their owners among the member states, effectively ensuring uniform access to the data across the European Union. The implementation of these objectives relies mostly on the EUCARIS, which is a system enabling the exchange of vehicle data, their owners and holders, and even on insurance policies, for the purpose of combating terrorism and cross-border crime. This directive   drives the development of mobile registration documents and supports their use in an international context and sets the direction for the further digitization of vehicle registration systems within the EU.

Another regulation playing a significant role in building a coherent vehicle data ecosystem in the EU is **the EU Regulation 2018/858** of the European Parliament and of the Council of 30th of May 2018 on the approval and market surveillance of motor vehicles and their trailers, and of systems, components and separate technical units intended for such vehicles. Although this act does not directly govern the vehicle registration process, it constitutes one of the pillars enabling the development of digital registration documents, including the mVRC. The regulation establishes a framework for the vehicle type approval, defines a standardised set of the vehicle technical data, and mandates the issuance of a Certificate of Conformity (CoC), which serves as the primary source of information used at the registration stage. As a result, the mVRC can rely on uniform and verified data from the type-approval process, which enhances its interoperability and enables automatic verification in the cross-border environment.

Furthermore, the Commission Implementing Regulation (EU) 2021/133 sets out preliminary requirements regarding the format and structure of the electronic CoC data and designates the EUCARIS system as the channel for the data exchange between manufacturers and national type-approval authorities. It introduces the obligation to use standard Initial Vehicle Information (IVI) messages and basic rules for communication security and IVI data verification. Additionally, the Commission Implementing Regulation (EU) 2024/1061 goes further by introducing more advanced provisions regarding the secure exchange of certificate of conformity in electronic format (eCoC). It specifies the obligation to use a secure connection and a structured XML format when exchanging IVI messages in the EUCARIS system, the validation of electronic signatures, the logging of all messages to ensure their traceability, and the use of a unique vehicle identifier (VIN), as well as regulating data access rules.

All of the regulations, those directly related to vehicle type approval and registration, and those governing the electronic exchange of data, have a key impact on the mVRC’s profile. They have introduced regulatory uniformity, system compatibility and the security of data and citizens across the EU by creating a coherent, reliable, and interoperable ecosystem of digital registration documents.

### 3.2 ISO Standards
In the context of the works on the mVRC profile, international ISO standards are of vital importance as they form the foundation for ensuring the consistency and interoperability of the designed solutions at the EU level. Their significance has already been emphasised at the regulatory level – directives on the mobile vehicle registration certificates highlight the need for these solutions to be based on the ISO standards. Consequently, as part of the LSP APTITUDE project, the mVRC profile is being designed in accordance with the relevant ISO standards to secure its compliance with EU requirements and readiness for operation in the cross-border environment.  The use of ISO standards enables the harmonisation of data structures and processing methods, whilst enhancing the security, reliability and scalability of the solution. As a result, the mVRC can be effectively integrated with the national vehicle registration systems, digital wallets and verification infrastructure, and can be recognised and accepted by various entities across the European Union. These standards therefore constitute a major element in building a trusted and interoperable ecosystem for digital vehicle documents.

- **ISO/IEC 7367-2:2026**

  The key reference point for designing the mVRC profile and its document structure is the ISO 7367-2. Although this standard has not yet been formally finalised, the project work was conducted based on its most recent draft version, made available for the purposes of the project. The developed mVRC model is therefore fully compliant with this standard.
  
  The ISO/IEC 7367-2 standard is part of the ISO 7367 series, which defines the mdoc schema and supplements it with the data structure for the mobile vehicle registration certificate (mVRC). This standard specifies how vehicle data is represented in a digital form so that it can serve as reliable confirmation of the information contained in the national vehicle registries and meet the conditions required for issuing the document.

  According to the standard’s provisions, the mVRC performs two basic functions. First, it serves as a confirmation of the vehicle’s registration data-reflecting information held by the issuing authority, such as the vehicle owner or holder (user), vehicle identifiers and technical and configuration parameters. Second, it serves as a compliance confirmation, indicating that the vehicle meets specific formal requirements, such as payment of applicable taxes, validity of the technical inspection, or possession of mandatory insurance.

  Additionally, the standard provides for the use of the mVRC as a tool to support the enforcement of traffic regulations, particularly in the context of roadside inspections. This enables, among other things, the verification of authorisation to use the vehicle, owner or holder identification, and checking the conditions for the vehicle’s admission to traffic (e.g. access restrictions for specific vehicle categories).

- **ISO/IEC 18013-5:2021**

  Another relevant reference point for the mVRC profile is the ISO 18013-5 standard, which is part of the ISO 18013 series. This series establishes a common foundation for the international use and mutual recognition of mobile documents, while allowing for the application of national privacy regulations and administrative requirements. This standard defines the mobile document (mdoc) model and standardises the interfaces between the user’s wallet, the verification device (reader), and the issuing authority’s infrastructure. This enables various entities, also in cross-border scenarios, to read the document’s data, link it to its holder, and verify its origin and integrity.

  ISO 18013-5 plays an important role in preventing the fragmentation of the digital document ecosystem. Without a common standard, national solutions may remain inconsistent, which would significantly limit their use beyond borders. A standardised approach ensures interoperability between different systems, devices, and jurisdictions.

  In the context of the mVRC, this standard provides proven mechanisms for proximity data presentation and verification, based on strong cryptographic foundations and the principle of selective data disclosure, which enables the secure and controlled sharing of information. As a result, it is one of the main elements in building an interoperable and secure ecosystem for the mobile vehicle documents in Europe and forms the foundation for solutions such as the EUDI Wallet.

- **ISO/IEC 18013-7:2025** and ISO/IEC CD TS 18013-7 (under development)

  ISO 18013-7 supplements ISO 18013-5 with guidelines for presenting a mobile document to a verifier via the Internet, thereby extending its scope of application to include remote (online) scenarios (OID4VP). As this LSP project also involves the use of the mVRC in online scenarios, this standard is significant, and the solutions being developed in this area are based on its principles.

- **ISO/IEC 23220 series**

  Mobile electronic document applications (mDoc apps) are a key component of modern electronic identification systems, enabling users to authenticate, identify themselves, and optionally sign digital documents. They can support multiple digital credentials, coexist with other eID apps on the same device, and operate across multiple devices belonging to the same user, allowing flexible management of credentials and attributes.   
  The ISO/IEC 23220 series provides a technical framework for such applications, covering secure channel establishment, data element naming conventions, API call serialisation, and data transport over different communication protocols. This series ensures interoperability, exchangeability, and security of mDoc apps, while enabling deployment across various mobile and hardware environments.

  The ISO/IEC 23220 series supports both proximity scenarios, using NFC, Bluetooth Low Energy, or Wi-Fi, and remote scenarios over the Internet. This allows mDoc apps to be used in a wide range of daily life contexts, including government services, finance, healthcare, education, corporate, and private applications.

### 3.3 Existing mVRC implementations
The WP5 leaders conducted a questionnaire among eleven WP5 members (10 member states and Ukraine) between 1 December, 2025 and 26 January, 2026. WP5 members were asked about existing mVRC credentials in their countries. Germany, Austria, France, Portugal, Ukraine stated that they had an mVRC credential in production. In addition, the Netherlands, the Czech Republic, Greece, France, and Poland had a similar credential, document, or a related service available. It is worth noting that existing national implementations, though often advanced and used by citizens, do not fully meet the requirements of the eIDAS 2.0 regulation, particularly in terms of interoperability, the verifiable credentials model, and integration with the European Digital Identity Wallet.

Despite this, they constitute a valuable source of knowledge and inspiration. As part of the work on the mVRC profile, WP5 draws on the experiences of these countries, both at the technical level and in terms of user experience. Examples of solutions, such as applications developed in Germany or Austria, were presented during regular meetings of the WP5 working group and serve as an important reference point for further work.

At the same time, there are countries, such as Poland, that do not yet have a fully-fledged mobile vehicle registration certificate, but offer users access to vehicle data through national digital applications. In such cases, the information is retrieved from the national vehicle registries and can be displayed within the national digital wallet, which also represents a step towards the future implementation of the mVRC.

- **Austria**

   Austria, the mobile vehicle registration certificate operates as part of the eAusweise app, which serves as a central tool for storing and presenting digital documents and credentials. The app allows users to present vehicle data and other documents in a digital form directly on their smartphone, in particular by generating temporary QR codes that can be scanned by authorised entities to verify the data. Access to the app is via the ID Austria system, which ensures secure user authentication (including the two-factor authentication).

  This solution is recognised by public authorities as a valid proof within the country. Users can present the digital document during checks in Austria without the need to carry the paper version. The application also offers additional features, such as notifications of impending document expiry dates and the ability to delegate the vehicle registration certificate to other people for a specified period, enabling third parties to use the vehicle legally without the need to hand over the physical document. Its scope is gradually being expanded to include further types of digital certificates.

- **Germany**

  An example of a national implementation of a mobile vehicle registration certificate is the i-Kfz application, developed by the KBA (Kraftfahrt-Bundesamt) and the technical service provider Bundesdruckerei on behalf of the Federal Ministry of Transport (BMV). It is a tool that allows users to store and manage their digital vehicle registration certificate on iOS and Android devices. In Germany, the digital document is recognised as an equivalent to its paper counterpart and can be used, for example, during police checks or technical inspections. The application for natural persons was launched in November 2025. Since March 2026 it is available for legal entities.

  The process of issuing a digital document in the i-Kfz app for natural persons is based on the electronic identity (eID) authentication. Legal persons alternatively may use a token (QR code) generated during vehicle registration. The data displayed in the app is retrieved directly from the KBA register. The users can delegate their vehicle registration certificate to others via QR codes, specifying the duration of their validity, as well as revoke access to delegated documents. The application provides full control over the lifecycle of the vehicle registration certificate, both the primary and delegated versions, and supports a delegation model. Additionally, it offers a feature for automatically updating vehicle inspection dates and providing reminders of their upcoming expiration.

- **Poland**

  Poland does not have an official, legally recognised mobile vehicle registration certificate (mVRC) that could fully replace the traditional registration certificate for the purposes of traffic stops or other official procedures. Instead, the mObywatel application (the Polish digital identity wallet) features the “My vehicles” service, available to users as part of electronic public services, which allows vehicle owners and co-owners to quickly access key information about their vehicles, retrieved directly from the Central Registry of Vehicles and Drivers (CEPiK). The “My vehicles” service allows the users, among other things, to view the technical vehicle data such as make, model, registration number, or VIN, as well as to monitor the expiration dates of mandatory liability insurance (OC) and the validity of the vehicle’s technical inspection, with the option to refresh the data on demand. However, the “My vehicles” section itself does not have a legal standing equivalent to a physical registration certificate and does not replace it in formal situations, such as handling matters at the Department of Motor Vehicles, undergoing a vehicle inspection, taking out an insurance policy, or crossing a national border. Additionally, the mObywatel application sends notifications informing the user of upcoming deadlines for mandatory liability insurance and vehicle technical inspections, helping the vehicle owner ensure that the required documents remain valid.

Although none of the three example applications meet the requirements set forth in the EU’s eIDAS 2.0 regulation, the experience gained from creating those services is an essential step towards the fully compliant mVRC, which WP5 will develop as part of this LSP project.

### 3.4 Current constraints and limitations
During the work on the mVRC profile, several limitations and challenges have been identified that have a significant impact on the design and testing of the solution. Some of these barriers were known from the outset of the project, due to the nature of national systems, legal regulations, or consortium requirements, while others have emerged during the specification phase. Despite these difficulties, the WP5 team is working to overcome the encountered limitations and develop a solution that is usable, universal, and best suited to the needs of the member states and various stakeholders.

The identified challenges are the following:

- **Limited participation of national registries and responsible authorities** – A limited number of national vehicle registries and institutions responsible for implementing the laws related to the mVRC is participating in the project. This complicates, among other things, data mapping, the harmonisation of solutions, and the development of a final version of the mVRC profile.

- **Limited participation of the EU member states** – Despite the efforts to ensure that the mVRC profile addresses the needs of all the member states, only 11 countries are participating in the LSP. This makes it difficult to fully validate the profile across the EU.

- **An unsettled regulatory environment for the mVRC** – The regulatory framework affecting mVRC is still evolving. This includes directives and regulations related to vehicle registration, ISO standards, and implementing acts under eIDAS 2.0 (e.g., those concerning onboarding to a new digital wallet). Consequently, key components of the pilot project, including the EUDI Wallet, remain under development, necessitating a flexible approach to the design of the mVRC profile.

- **Use of simplifications in the mVRC pilot phase** – Simplifications are introduced to enable testing of the interoperable mVRC solution. If certain functionalities or data are unavailable in the production environment (e.g. national registries), they may be simulated or provided through manual input.

- **Time constraints** – The pilot is being carried out according to a strict schedule, which limits the time available to address the additional, more complex scenarios and the ideas for advanced cross-border use cases.

- **The diversity of business needs** – The current pilot group of relying parties is dominated by representatives of companies specialising in long-term vehicle rental, whose requirements for business travel and document management differ from those operating in the short-term rental sector. The mVRC profile must take these differences into account. However, the limited representation of certain segments makes it challenging to capture a comprehensive set of requirements, often necessitating the reconciliation of differing needs and stakeholder expectations.

- **Existing implementations and user expectations** – Some member states have already implemented mVRCs within their national digital wallets, which significantly shapes user experience and expectations. While citizens expect familiar functionalities to support mVRC adoption, the final European profile must comply with EU regulations (eIDAS 2.0) and ensure interoperability with national systems across all the member states. Identifying these limitations during the pilot phase provides valuable insights that support better preparation for future production deployment, helping to minimise risks and improve implementation efficiency. It enables not only the validation of the core assumptions of the mVRC profile, but also the verification of its interoperability under real cross-border conditions. In the long term, this contributes to the development of a solution capable of operating across the European Union in compliance with applicable regulations and user expectations.


## 4 mVRC profile
### 4.1 High-level description
The mVRC is a mobile vehicle registration certificate and represents a digital equivalent of the traditional vehicle registration document. It is designed as an interoperable credential, which can be used across the European Union, stored and presented with the use of the European Digital Identity Wallet (EUDI Wallet) on a mobile device.

The development of the mVRC profile is based on a set of requirements derived from the EU regulations and technical standards described in Section 3 of this document, which define both the data scope and the way it is structured and exchanged. The detailed data model is specified in the dedicated mVRC rulebook, which includes a set of mandatory attributes required for vehicle identification and status verification, as well as optional attributes that may be used depending on national requirements or specific use cases.

The mVRC profile also incorporates standardised data exchange patterns (request/response), issuer-related security structures (such as IssuerSigned and IssuerAuth/MSO), as well as protocols supporting both proximity and remote interaction flows. In addition, the mVRC profile is based on the ISO/IEC 18013-5 mdoc format. These elements form the foundation of interoperability within the EUDI wallet ecosystem. The mVRC profile also specifies the use of document types and namespaces in line with ISO standards, provides more detailed guidance on the use of data elements, and introduces additional namespaces managed at the EU or a member state level.

The design of the mVRC profile includes the diversity of national vehicle registration systems and existing practices based on the input from project participants and an analysis of current solutions. As a result, the mVRC profile represents a balance between the EU-level harmonisation and the flexibility required to accommodate the specific needs of individual member states. At the same time, its key objective is cross-border interoperability, meaning that a document issued in one member state can be verified and accepted in the other.

Ultimately, the mVRC profile establishes a coherent framework for a digital vehicle document, serving as a foundation for the further development of mobility-related and vehicle management services in a digital, cross-border EU environment.

### 4.2 mVRC lifecycle
In accordance with the approach defined in the Architecture and Reference Framework (ARF), the lifecycle of an mVRC (as an Electronic Attestation of Attributes – EAA) within the EUDI Wallet ecosystem begins when a user, using their wallet unit, requests an attestation provider to issue the mVRC attestation to their wallet unit. The mVRC is issued to the user’s wallet unit following successful authentication and the establishment of trust between the wallet unit and the attestation provider.

Once activated in the wallet, the mVRC enters the valid state, during which it can be used. The document is stored in the wallet and can be presented, delegated or deleted. Subsequently, the mVRC may transition to the expired state, automatically losing validity at the end of its defined validity period, or to the revoked state if it is intentionally revoked.

The lifecycle phases described in this specification are realised through protocol interactions and trust mechanisms defined in the RFCs developed within WP2 of the LSP Aptitude, including RFC001. The presentation and verification of mVRC attestations within the EUDI wallet ecosystem are further aligned with ETSI‑based presentation profiling, as described in the RFC002.

- **Issuance**

  At this stage, the attestation is created, cryptographically bound, and digitally signed by the mVRC issuer, ensuring its authenticity and integrity. The mVRC issuer acts as the authoritative source of the attestation, in accordance with the trust framework defined by eIDAS 2.0, its implementing acts, and the Architecture and Reference Framework (ARF). Following the successful issuance, the mVRC is securely transferred to the wallet unit and stored under the sole control of the holder, enabling its subsequent secure presentation and selective disclosure within the EUDI wallet ecosystem. The wallet unit acts exclusively as a secure storage and presentation component and does not assume issuer or validation responsibilities.

  The mVRC issuance process is based on the OpenID for Verifiable Credential Issuance (OpenID4VCI) 1.0 standard. The PID credential is optionally used to verify the user’s identity prior to issuance. Detailed information on the mVRC issuance process is provided in the RFC document for Scenario 1A (Section 8.1 of this specification) together with some optional steps.

- **Storage**

  After the successful issuance and user approval, the mVRC is stored within the user’s wallet unit. The wallet provider attests that the corresponding private key is stored in a Wallet Secure Cryptographic Application / Wallet Secure Cryptographic Device (WSCA/WSCD) or an equivalent certified keystore, consistent with applicable wallet certification requirements, and the wallet unit proves possession of this key during the issuance process. Access to the mVRC is protected by the user authentication mechanisms implemented by the wallet unit. If applicable, any embedded disclosure policies received during issuance are stored locally and enforced during subsequent presentation interactions.

- **Presentation**

  Within the EUDI wallet ecosystem, the presentation of an mVRC can occur only after the credential has been issued to the user’s wallet unit and activated. The user can present single identifiers or groups of identifiers from their mVRC to a relying party instance or another wallet unit, according to the user’s consent and the successful authentication of the recipient.

  Two presentation protocols are used depending on the scenario:

  -	Proximity presentation using ISO/IEC 18013-5:

  This protocol supports secure attestation presentation in close-range scenarios. An initial communication channel is established using QR codes or NFC, followed by data exchange over BLE, NFC, or Wi‑Fi Aware. ISO/IEC 18013-5 ensures confidentiality and authenticity of exchanged data and supports authentication of the relying party. Although originally designed for mobile driving licences, the protocol is generic and applicable to other attestation types including mVRCs.

  -	Remote presentation using OpenID4VP:

  For remote presentation scenarios, the wallet unit uses the OpenID4VP 1.0 protocol. OpenID4VP defines standardised message structures, transaction flows, and security mechanisms that enable the wallet unit to present attestations in response to a request from a relying party, based on explicit user consent. The protocol is built on OAuth 2.0 and leverages its security properties to ensure confidentiality, data authenticity, transaction binding, and protection. OpenID4VP supports both same‑device and cross‑device presentation scenarios within the EUDI wallet ecosystem.

- **Delegation**

  Delegation of an mVRC enables the owner or holder to grant temporary access to the attestation for third parties, such as family members, friends or customers of leasing companies or car rental companies without transferring the vehicle ownership. This delegation can occur only after issuance. The delegated mVRC can be created as a time-bound copy of the primary mVRC, valid for a predefined period. The users to whom an mVRC is delegated can be called consumers as defined in the mVRC rulebook. The consumers are not able to modify or delegate the delegated mVRCs.

  The delegated mVRC is derived from the primary mVRC and reflects its state at the time of issuance. Within the LSP scenarios, continuous synchronisation, update or automatic re‑issuance of the delegated mVRC is considered out of scope. As a result, changes to the primary mVRC (such as updates resulting from administrative changes or technical inspections, or revocation of delegations by the owner, who retains full control over all active delegations) are not automatically propagated to already issued delegated mVRCs.

- **Re-issuance**

  An mVRC can, in principle, be a subject to re‑issuance during its lifecycle to reflect changes in the state of the vehicle or the attestation. The ARF identifies re‑issuance as conceptual mechanism for reflecting updated information, whereby a new attestation is issued to the wallet unit, replacing a previously issued instance. Any mechanisms of live synchronisation or updates of an existing mVRC attestation with national and, especially cross‑border vehicle registers, would introduce significant technical and operational complexity and are therefore not addressed within the scope of the LSP.

  While the ARF mentions the potential use of mechanisms such as OpenID4VC device-bound refresh tokens for the credential refresh, neither the technical realisation nor the operational processes for re‑issuance are normatively specified. Consequently, the implementation of re‑issuance is not included in any of the WP5 scenarios.

- **Expiration**

  The mVRC can include a predefined validity period after which it automatically transitions to an expired state and can no longer be presented for verification. The expiration is time‑based and does not require any action from the issuer. This mechanism is particularly relevant for temporary usage scenarios, such as delegated access in rental or family‑sharing contexts, where the right to present the mVRC is intentionally limited to a defined timeframe. Once expired, the mVRC becomes unusable for a presentation, preventing further use.

- **Deletion**

  A user may choose to delete the mVRC from the wallet unit at any time. The deletion is a local action performed under user control and authentication. It results in the removal of the credential from the wallet unit.

  It remains an open question whether the deletion of an mVRC from the wallet unit should trigger a revocation request to the attestation provider or whether the attestation should continue to be considered valid on the issuer's side until it expires naturally or is revoked through established revocation mechanisms.

  Within the scope of the LSP, no definitive requirements are defined for propagating user‑initiated deletion events to the attestation provider. Consequently, the deletion of an mVRC from the wallet unit does not automatically imply revocation of the attestation at the issuer side. Any potential linkage between deletion and revocation is considered out of scope of the LSP and may be addressed by individual member states or in future iterations of the specification.

- **Revocation**

  The revocation occurs when the attestation provider actively invalidates the mVRC prior to its natural expiration. This may be a result of changes in the vehicle’s administrative or legal status. The revocation process ensures that outdated or invalid credentials cannot be used for verification, thereby maintaining the integrity of the digital vehicle registration across EU systems and preventing potential misuse during the cross-border travel or administrative procedures.

  Within the LSP, no detailed functional or technical requirements are defined regarding the conditions under which national registries initiate revocation events, nor how such events are triggered and transmitted to the attestation providers. These aspects are considered out of scope of the LSP and remain the responsibility of each member state.

  In line with eIDAS 2.0, two technical approaches to revocation are generally supported: Attestation Status Lists (ASL) and Attestation Revocation Lists (ARL). From the perspective of changing the status of an mVRC attestation to revoked as part of its lifecycle, the LSP assumes the use of the status list. Accordingly, the scope of the LSP is limited to the verification of the revocation status based on the status lists published by the attestation provider.

Within the WP5 scope, the lifecycle of the mVRC is intentionally limited to the stages that are essential for demonstrating interoperability, security, and practical usability within the EUDI wallet ecosystem. WP5 focuses on issuance of the mVRC using OpenID4VCI, remote (online) and proximity presentation, and delegation of the mVRC attestation. These stages cover the core usage scenarios of the mVRC within the pilot.

At the same time, re‑issuance, deletion, and revocation are explicitly out of scope, and none of the pilot scenarios include the implementation or validation of these lifecycle stages. Introducing the additional lifecycle stages could result in very complex and expanded flows, and this could pose a risk that not all the scenarios will be tested during the implementation and testing phase.

### 4.3 Rulebook for the mVRC and WP5 assumptions

The activities within WP5 are based on the ongoing refinement of the mVRC rulebook, which serves as the primary reference point for the entire mVRC profile. As part of this work, analyses have been conducted including the review and mapping of elements derived from national vehicle registers across the member states participating in the work package 5. This process included the identification and classification of data elements according to their status (mandatory, optional, or conditional) in a national context, as well as their comparison across different countries.

The rulebook is directly based on ISO 7367-2 and on the EU directives: EU DIR 2025/0096, EU DIR 1999/37. The profile is compliant with the requirements of the European Digital Identity Framework (EUDI wallet). In this context, the mVRC is issued as a mobile attestation (QEAA or Pub-EAA), managed by the EUDI wallet and operating within the broader ecosystem defined by the ARF.

The rulebook follows a structured approach to data harmonisation combining international standards with the EU regulatory requirements. It distinguishes between three primary namespaces: the ISO namespace, which reflects elements defined at the international standard level, the EU namespace, which adds data elements required at the European level, and the domestic namespace relevant for country-specific identifiers. However, WP5 will mainly work with the ISO and EU namespaces for the purpose of the pilot.

The rulebook also defines and clarifies key roles within the mVRC ecosystem. Concepts such as owner, holder, and user are grounded in the existing EU legal definitions. In addition, the concept of a consumer is introduced to refer to the individual who effectively uses the vehicle without necessarily being its legal owner or holder, for example in cases where the vehicle is delegated while formal ownership remains with another natural or legal person.

The rulebook, and consequently the mVRC profile, is expected to evolve over time. Multiple iterations have already been produced as a result of discussions, technical workshops, and input from the participating member states. Further changes are expected, particularly during the implementation and development phases, as new requirements, regulatory changes, and practical deployment experiences emerge.


## 5 Description of ecosystem – actor and roles

The mVRC ecosystem is designed as an interoperable environment that reflects the intended use of the mobile vehicle registration certificates within the European Union. A key requirement in the pilot is a tight integration with the European Digital Identity Wallet (EUDI wallet), which serves as the central element of all the analysed use cases. This means that each use case involves using the wallet as a tool for storing, presenting, and sharing mVRCs in the digital form. Another key requirement is the cross-border nature of the scenarios, meaning they involve at least one EUDI wallet issued in one member state and a relying party from another country. This approach enables a practical validation of interoperability, trust relationships, and compliance with the European legal and technical frameworks.

Depending on the specific scenario, different actors and roles are involved in the mVRC ecosystem. Some of these roles are mandatory for the correct execution of a given scenario, while others are optional or context-dependent. The following sections provide an overview of all those actors describing their responsibilities and contributions. 

- **User / mVRC owner or holder**

  The mVRC owner corresponds to the legal owner of the vehicle. There may be one or more vehicle owners. The owner holds financial control over the vehicle, including the right to sell, transfer, or dispose of the vehicle, and is recorded as the owner of the vehicle in the systems maintained by the authority issuing the mVRC in accordance with the rules of that authority. The mVRC owner is not necessarily the holder of the mobile vehicle registration certificate, but remains the principal subject associated with the attestation.
  
  The mVRC holder is also a natural or legal person. The mVRC holder is granted the right of use and benefit of the vehicle by the owner of the vehicle and is recorded as the user of the vehicle in the systems maintained by the authority issuing the mVRC. The mVRC holder controls a wallet unit used to receive, store, and present different electronic attestation of attributes (EAAs). Within the mVRC ecosystem, the owner or holder can act as a delegator, enabling controlled and time‑limited use of the vehicle and delegated presentation of the mVRC, without transferring the ownership of the vehicle or holder status of the attestation.

  For the purpose of the WP5 scenarios, the term “owner” refers to a person who is both the vehicle owner and the certificate holder, unless stated otherwise. Therefore, the person who requests issuance, presents the primary mVRC, or initiates its delegation acts as both the owner and the holder.

- **mVRC consumer (delegated user)**
  
  The mVRC consumer is a natural or legal person who has been granted the right of use and benefit of the vehicle on the basis of a legal right other than ownership or holder status, such as a rental contract or family sharing arrangement. The consumer is designated through delegation by the vehicle owner or holder and is authorised to use the vehicle and to present the mVRC within a limited scope and for a defined period of time. The consumer does not hold the mVRC as a registered holder, does not control the primary attestation, and cannot further delegate or modify the mVRC. At any given time, only one consumer may be associated with a vehicle within the mVRC ecosystem.

- **EUDI Wallet instance**

  The EUDI wallet instance is a mobile digital wallet application acting on behalf of a natural person as a secure holder of verifiable credentials and a presenter of verifiable presentations. It is compliant with eIDAS 2.0 and the Architecture and Reference Framework (ARF) for the European Digital Identity Wallet. The wallet manages cryptographic keys under user control, enforces explicit user consent, ensures holder binding, and supports selective disclosure using standardised issuance and presentation protocols such as OpenID4VCI and OpenID4VP. In the context of the mVRC, EUDI wallet instances operate in different roles depending on whether they represent the vehicle owner or primary holder or a consumer.

  **EUDI wallet instance – vehicle owner / primary holder**

  The EUDI wallet instance for the vehicle owner or primary holder acts on behalf of the person who owns the vehicle or is recognised as the primary holder of the mVRC. It securely stores the source mVRC issued by the competent authority and enables its presentation in proximity or remote verification scenarios. In delegation scenarios, this wallet presents the source mVRC and proof of identity to support the issuance of a delegated mVRC, while ensuring user consent, selective disclosure, and cryptographic binding of the source credential to the owner or holder.

  **EUDI wallet instance – consumer (delegated user)**

  The EUDI wallet instance for the consumer (delegated user) acts on behalf of a user who has been granted delegated rights to use the vehicle. It serves as the target wallet for the issuance of a delegated mVRC and completes the applicable OpenID4VCI flow. After a successful identity verification, the wallet stores the delegated mVRC, ensures cryptographic holder binding, and enables presentation of the delegated mVRC strictly within the scope and validity defined by the delegation.

  **European Business Wallets (future consideration)**

  The concept of the business wallets refers to digital wallet instances operated on behalf of legal persons, enabling organisations to receive, manage and present verifiable credentials in a manner comparable to natural persons, while supporting organisational identity, roles and authorisations. Within the broader European Digital Identity Framework, the business wallets are expected to play a key role in enabling digital interactions for companies, including representation, delegation of authority, and access to company-related services.

  The business wallets are not included in the scope of the defined scenarios, and no issuance, delegation or presentation flows involving organisational wallet instances are considered. The scenarios described in this document are limited to wallet instances controlled by natural persons, acting as vehicle owners, holders or delegated users.

  Nevertheless, the business wallets are acknowledged as a relevant future extension of the ecosystem. Their integration may introduce additional roles and interaction patterns, particularly in scenarios involving fleet management, corporate vehicle ownership or organisational delegation. The definition and standardisation of such interactions remain outside the scope of this LSP.

- **Attestation issuer**

  The attestation issuer (or attestation provider) is a trusted entity (service) within the EUDI wallet ecosystem responsible for issuing, signing, and managing the lifecycle of electronic attestations of attributes (EAAs) issued to the EUDI wallet instances. The issuer retrieves and validates authoritative source data from competent registries, applies the required assurance and compliance checks, and issues cryptographically protected credentials bound to the wallet holder using keys attested in the Wallet Unit Attestation (WUA). The issuer ensures compliance with the eIDAS 2.0 trust requirements, applicable EU and national legislation, and relevant data and security specifications including ISO/IEC 7367‑2, while adhering to standardised protocols such as OpenID4VCI and HAIP.

  The issuer typically exposes separate logical interfaces fulfilling the roles of an authorisation server, credential issuer, and verifier, which may be implemented within a single application or as independent component. The detailed architecture and interfaces between these components are out the scope of the LSP and the RFC documents. Throughout the credential lifecycle, the issuer remains the authoritative source for the validity and status of the issued attestations.

  **mVRC issuer**
  
  In the context of mVRC, the issuer is responsible for issuing source mVRC attestations representing vehicle registration data retrieved from verified and authentic national vehicle registers. The mVRC issuer validates vehicle‑related attributes, applies the appropriate assurance level, and issues an mVRC cryptographically bound to the wallet holder. It manages the lifecycle of the mVRC, including status information such as validity, suspension, and revocation, and supports standardised issuance and verification protocols to enable interoperable use across jurisdictions.
  
  **Delegated mVRC issuer**
  
  In the context of the delegated mVRC, the issuer issues mVRC attestations to consumers (delegated users) based on verified delegation conditions. This may include verification of the vehicle owner or primary holder, validation of delegation permissions, and verification of the consumer’s identity. The delegated mVRC issuer issues a distinct delegated mVRC attestation, bound to the consumer’s wallet and constrained by the scope, purpose, and validity defined during delegation. The issuer remains responsible for the lifecycle and status management of the delegated mVRC, ensuring that revocation or suspension can be enforced consistently.
  
  **mDL issuer**
  
  The mDL issuer is responsible for issuing a mobile driving licence attestation to the EUDI wallet instances. The mDL issuer validates licence data, applies the required assurance checks, and issues cryptographically protected mDL credentials bound to the wallet holder. As with mVRC and delegated mVRC, the mDL issuer manages the attestation lifecycle, including updates, suspension, revocation, and status verification, to ensure long‑term trust and legal recognition within the EUDI wallet ecosystem.

- **mVRC data provider / National vehicle registry**

  An mVRC data provider, acting as an authentic source, is an authoritative registry (National Vehicle Registry) or backend system that provides verified vehicle data required for the issuance of the mVRC attestations or where applicable, delegated mVRC attestations. As defined in the Architecture and Reference Framework (ARF), the entity supplies accurate, up-to-date, and authoritative vehicle registration data, as specified in the mVRC profile, to the mVRC issuer for the purpose of issuing electronic attestations of attributes (EAAs).

  Depending on national or organisational arrangements, the National Vehicle Registry may operate as a standalone system, be integrated within the mVRC issuer’s infrastructure, or directly fulfil the role of the mVRC issuer itself. In all cases, the registry remains the authoritative source of truth for vehicle registration data used throughout the lifecycle of mVRC and delegated mVRC attestations.

- **mVRC / mDL verifier or proximity reader**

  An mVRC/mDL verifier is a relying party within the EUDI wallet ecosystem that requests and verifies the presentation of an mVRC, a delegated mVRC, an mDL, or a combination of them in order to perform a specific service or function. Verifiers may include public authorities, private service providers, or automated systems that rely on verified vehicle or driving licence data without assuming control over credential issuance or lifecycle management.

  **In remote (online) scenarios**, an mVRC verifier, delegated mVRC verifier, mDL verifier act as a service provider requesting verifiable presentations from the EUDI wallet instances using OpenID4VP presentation protocols. Typical examples include ferry booking and boarding services, tolling and vignette systems, parking and access management platforms, or any other online services that require verification of a vehicle registration, ownership information, delegated usage rights, or driving licence data. In this context, the verifier validates the authenticity, integrity, issuer trust, and current status of the presented attestations in accordance with applicable trust frameworks, assurance profiles, and interoperability specifications.

  **In proximity scenarios**, the verification is performed by an mVRC, mDL or combined proximity reader, which is a relying party device or system used during in‑person interactions. Proximity readers include law enforcement roadside equipment, parking or access control machines, operators of restricted areas (e.g. environmental zones or underground car parks), vehicle technical inspection centres, or ferry boarding operators. These readers rely on standardised proximity presentation mechanisms aligned with ISO/IEC 18013‑5, to request, receive, and verify mVRC or mDL attestations from EUDI wallet instances.
  
  In proximity scenarios, an additional role of an individual user operating the verification device may be present. It is a natural person operating or supervising a proximity verification device, such as a police officer, who initiates or oversees the verification process. This role is optional, as some proximity verification scenarios may involve fully automated readers that do not require active human participation. In all proximity scenarios, verification is limited to validation and policy enforcement and does not grant the reader or its user the ability to issue, modify, or delegate credentials.

- **Trusted list provider**

  A trusted list provider is an authoritative body responsible for maintaining, managing, signing, and publishing trusted lists within the European Digital Identity Wallet ecosystem. The trusted list provider ensures the availability of reliable, verifiable, and up-to-date information on the current and historical status of entities included in such lists, enabling wallets, issuers, verifiers, and other relying parties to establish and assess trust relationships in a consistent, interoperable, and verifiable manner in accordance with eIDAS 2.0 and the Architecture and Reference Framework (ARF). The trusted list provider operates in accordance with ETSI TS 119 612 and any implementing acts adopted under Article 22 of Regulation (EU) No 910/2014 as amended.

- **PID / mDL provider**

  **A PID provider** is a trusted entity responsible for verifying a user’s identity in compliance with LoA high requirements and issuing Person Identification Data (PID) credentials to the user’s wallet unit. The PID provider signs PID credentials and maintains authoritative status information, which can be accessed in a privacy‑preserving manner by wallets and relying parties to validate PID presentations. The trust in the PID provider is established through ecosystem‑specific governance and trusted entity listings, rather than through eIDAS trusted lists. A PID provider may, but does not have to, be the same organisation as a wallet provider. Where a single organisation performs both roles, it is required to comply with the full set of requirements applicable to each role separately. In the delegation scenarios, the PID provider may support identity verification of the vehicle owner or holder where the PID is used as the identity credential.
  
  **An mDL provider** is a trusted entity responsible for issuing mobile driving licence (mDL) credentials to eligible users and maintaining authoritative status information related to issued mDLs. The mDL provider signs mDL credentials and makes the information required to validate mDL presentations available. Where relevant, the mDL provider may support the identity verification of the vehicle owner, holder, or consumer, particularly in delegation or authorisation use cases.

- **Wallet provider**

  A wallet provider is a member state or an organisation mandated or recognised by a member state to make a certified EUDI wallet solution available to users. The wallet provider delivers and manages wallet units, enabling users to store, manage, and present Person Identification Data (PID), electronic attestations of attributes (QEAA, PuB‑EAA, or EAA), and other personal data under the user’s sole control. This includes ensuring that users retain exclusive control over sensitive cryptographic material, such as private keys associated with their wallet unit.
  
  From the perspective of other actors in the EUDI wallet ecosystem, the wallet provider is responsible for all components of the wallet unit, including ensuring access to a Wallet Secure Cryptographic Device (WSCD) with a security level sufficient to support the high level of assurance as required for the PID usage. This responsibility applies even where the WSCD is integrated into the user device and not supplied directly by the wallet provider.
  
  The wallet provider is responsible for provisioning and lifecycle management of wallet instances, for maintaining authoritative status information related to those instances, and for issuing Wallet Unit Attestations (WUA) and Wallet Instance Attestations (WIA) used to establish trust in wallets during credential issuance and presentation processes. The trust in the wallet provider is established through ecosystem governance mechanisms and dedicated trusted entity lists, and all wallet solutions made available to users must be certified.

An ecosystem defined in this way enables a clear and structured understanding of the roles, responsibilities, and trust relationships between the different participants involved in the mVRC scenarios. The structure, with the EUDI wallet at its core, supports the practical tests and cross‑border cases. This enables a realistic evaluation of interoperability, governance arrangements, and compliance with the European legal and technical frameworks in more realistic conditions.


## 6 Scenarios – summary

This section provides a consolidated overview of the key scenarios, describing the end-to-end use cases of the mVRC within the European Digital Identity Wallet ecosystem. The scenarios address issuance, delegation and presentation of the mVRC, including both remote and proximity interactions, as well as combined use cases involving both the mVRC and mobile driving licence (mDL) attestations.

The scenarios are designed to address real world interactions across the European Union, ranging from roadside checks and vehicle inspections to digital services such as parking, ferry bookings and tolling. They reflect the needs of vehicle owners, consumers, public authorities, issuers and service providers, while ensuring compliance with the requirements of eIDAS 2.0 and the Architecture and Reference Framework. To ensure consistency and to clearly structure these different needs, the scenarios have been organised into three groups, each reflecting the main real world usage patterns of mVRC within the European Digital Identity Wallet ecosystem.

The first group covers use cases in which the mVRC is held and used directly by **the vehicle owner, who, for the purposes of the LSP scenarios, is also assumed to be the holder of the certificate**. This group includes the issuance of the mVRC, as well as its presentation for data sharing purposes in both remote and proximity interactions. The second group focuses on the delegation scenarios, addressing situations in which vehicle usage rights are granted to a third party. It includes delegated mVRC issuance in a wallet-to-wallet (w2w) model and an organisation-to-wallet (o2w) model, as well as the remote and proximity presentation of the delegated mVRC by the consumer. The third group addresses scenarios requiring the combined presentation of mVRC and mobile driving licence (mDL) attestations, covering both remote and proximity interactions where verification of the vehicle registration and driving entitlement is needed within a single transaction.

```mermaid
flowchart LR
    A[mVRC Scenarios]
    subgraph SG1[ ]
        direction LR
        G1["GROUP 1<br/>Owner-held mVRC"]

        G1A["1A<br/>Issuance"]
        G1B["1B<br/>Remote data sharing"]
        G1C["1C<br/>Proximity data sharing"]

        G1 --> G1A
        G1 --> G1B
        G1 --> G1C
    end
    A --> G1

    %% ---------- GROUP 2 ----------
    subgraph SG2[ ]
        direction LR
        G2["GROUP 2<br/>Delegated mVRC"]

        G2A["2A<br/>Issuance w2w"]
        G2B["2B<br/>Issuance o2w"]
        G2C["2C<br/>Remote data sharing"]
        G2D["2D<br/>Proximity data sharing"]

        G2 --> G2A
        G2 --> G2B
        G2 --> G2C
        G2 --> G2D
    end
    A --> G2

    %% ---------- GROUP 3 ----------
    subgraph SG3[ ]
        direction LR
        G3["GROUP 3<br/>Combined mVRC & mDL"]

        G3A["3A<br/>Remote data sharing"]
        G3B["3B<br/>Proximity data sharing"]

        G3 --> G3A
        G3 --> G3B
    end
    A --> G3

    %% ---------- CLASSES ----------
    classDef group fill:#F3F4F6,stroke:#6B7280,stroke-width:1px,color:#111827
    classDef issuance  fill:#E8F1FF,stroke:#8CB4F5,stroke-width:1px,color:#1E3A8A
    classDef remote    fill:#DCEAFE,stroke:#6FA3F7,stroke-width:1px,color:#1E3A8A
    classDef proximity fill:#CFE1FD,stroke:#4F8DF0,stroke-width:1px,color:#1E3A8A

    class G1,G2,G3 group
    class G1A,G2A,G2B issuance
    class G1B,G2C,G3A remote
    class G1C,G2D,G3B proximity
```

All the presentation scenarios described in this section are designed to support selective disclosure of attributes, allowing the user to share only the minimum set of the mVRC or delegated mVRC data required for a specific use case. This design is aligned with the data minimisation and user control principles defined in the eIDAS 2.0 and is implemented through OpenID4VP presentation definitions combined with wallet-mediated user consent. This model supports a high level of assurance, strong cryptographic protection, explicit user consent, and cross‑border interoperability within the European Wallet Ecosystem.

To further clarify the scenarios, it is necessary to identify the roles that are required across all scenarios. The table below provides an overview of the key actors participating in the mVRC issuance and presentation workflows. Each role is classified as either required or optional, depending on whether it is essential in a given scenario.

 Role \ Scenario                                  | 1A | 1B | 1C | 2A | 2B | 2C | 2D | 3A | 3B |
|-------------------------------------------------|----|----|----|----|----|----|----|----|----|
| Owner (user/holder)                             | r  | r  | r  | r  | r  | -  | -  | r  | r  |
| Consumer (delegated user)                       | -  | -  | -  | r  | r  | r  | r  | -  | -  |
| EUDI wallet instance (owner)                    | r  | r  | r  | r  | -  | -  | -  | r  | r  |
| EUDI wallet instance (consumer)                 | -  | -  | -  | r  | r  | r  | r  | -  | -  |
| mVRC issuer                                     | r  | o  | o  | r  | r  | o  | o  | o  | o  |
| mDL issuer                                      | -  | -  | -  | -  | -  | -  | -  | o  | o  |
| mVRC remote verifier                            | -  | r  | -  | -  | -  | r  | -  | r  | -  |
| mDL remote verifier                             | -  | -  | -  | -  | -  | -  | -  | r  | -  |
| National vehicle registry (mVRC data provider)  | o  | -  | -  | o  | o  | -  | -  | -  | -  |
| Trusted list provider                           | o  | o  | o  | o  | o  | o  | o  | o  | o  |
| PID provider                                    | o  | -  | -  | o  | o  | -  | -  | -  | -  |
| mDL provider                                    | -  | -  | -  | o  | o  | -  | -  | -  | -  |
| Wallet provider                                 | o  | -  | -  | o  | o  | -  | -  | -  | -  |
| mVRC proximity verifier\reader                  | -  | -  | r  | -  | -  | -  | r  | -  | r  |
| mDL proximity verifier\reader                   | -  | -  | -  | -  | -  | -  | -  | -  | r  |
| mVRC & mDL proximity reader operator            | -  | -  | o  | -  | -  | -  | o  | -  | o  |

r - required / o - optional		

### 6.1 Motivation, business drivers and pain points from RFCs

- **Regulatory and architectural motivation**

  The scenarios aim to support the digital issuance, delegation and presentation of the mVRC, and their combined use with mobile driving licence (mDL) attestations, in full alignment with the Regulation (EU) No 910/2014 as amended by eIDAS 2.0 and the Architecture and Reference Framework (ARF) for the European Digital Identity Wallet (EUDI Wallet).

  All scenarios are based on standardised and interoperable protocols, in particular OpenID for Verifiable Credential Issuance (OpenID4VCI), OpenID for Verifiable Presentations (OpenID4VP), the High Assurance Interoperability Profile (HAIP) and, where applicable, ISO/IEC 18013-5 for proximity interactions, which together provide a common communication layer for secure credential exchange within the European Digital Identity Wallet ecosystem.

  Additionaly, the purpose is to enable the selective disclosure, allowing users to retain control over which mVRC attributes are shared in a given interaction and to avoid unnecessary data exposure, in line with privacy principles defined in the eIDAS 2.0 regulation.

- **Business drivers**

  From the perspective of citizens and residents, there is a growing expectation that vehicle registration documents can be handled in a fully digital, secure and interoperable way, without reliance on their paper versions. Users want to present their mVRC both remotely, when interacting with online services, and locally in proximity situations, using a single, trusted digital wallet. Furthermore, there is a strong need for a legally reliable mechanism to delegate vehicle usage rights to the third parties (such as family members, employees, or rental and leasing customers) in a way that clearly defines the scope and validity period of those rights. This is essential so that the person who actually uses the vehicle can independently benefit from the functionalities enabled by the mVRC, for example by presenting it during roadside checks, paying for parking, or purchasing ferry tickets. All of these capabilities must operate seamlessly across borders, enabling the mVRC and delegated mVRC credentials to be accepted and used throughout the European Union.

  From the perspective of public authorities, issuers, and service providers, the main driver is the need for a common, standardised model for issuing and presenting the mVRC that simplifies integration across the member states. For the public authorities in particular, it is crucial to have timely access to reliable and verifiable data on vehicles registered in other countries, for example in the context of roadside checks, law enforcement activities or administrative procedures. Therefore, official mVRC issuers must remain the trusted and authoritative source of vehicle registration data and delegated usage rights, ensuring legal certainty and consistent governance across jurisdictions. At the same time, verifiers require clear and reliable cryptographic assurances and straightforward processing rules that can be applied consistently in the cross-border scenarios, allowing services to scale across the EU while maintaining a high level of security and trust.

- **Pain points in the current landscape**

  Current issuance models for the mVRC and similar documents are highly fragmented, as they are typically based on national identity verification mechanisms, legacy systems or bespoke technical integrations. Many of these approaches are designed primarily for domestic use and are not aligned with OpenID4VCI, OpenID4VP or the HAIP, which results in limited interoperability beyond national borders.
  
  Another significant challenge is the lack of a standardised and formally defined concept of the delegated vehicle usage rights. In many cases, the delegation is handled implicitly, for example through the physical handover of a paper registration document. Such approach does not provide a portable, wallet-based proof of the delegated rights and cannot be reliably reused or verified across different services or member states. As a result, the use of vehicle  services by consumers is often constrained, as they cannot independently execute required interactions and must rely on the vehicle owner or holder for actions such as roadside checks, parking access, technical inspections. In practical terms, this frequently means that the vehicle owner or holder must remain involved in transactions or administrative actions, even when they are not the ones using the vehicle, which reduces usability, limits automation, and undermines the effectiveness of the document delegation in everyday scenarios.
  
  Existing solutions frequently fail to provide a consistent and sufficiently strong level of security and assurance. Cryptographic holder binding is often missing or insufficiently implemented, explicit user consent during presentation is not consistently enforced, and protection mechanisms against replay and misuse remain limited. As a result, verifiers may not be able to reliably determine whether the presented data is authentic, up-to-date, and legitimately associated with the presenting user.
  
  Finally, the inconsistency of current solutions leads to high integration and operational costs for all ecosystem participants. Wallet providers and verifiers are forced to support multiple non-standard presentation mechanisms and data models, while issuers must maintain different issuance and verification processes depending on the national context. This fragmentation reduces scalability, increases complexity, and ultimately undermines the goal of seamless, cross-border use of digital vehicle credentials within the European Union.

### 6.2 High-level user journeys per scenario

#### **SCENARIO GROUP 1 – mVRC owned by the vehicle owner**

- **Scenario 1A – mVRC issuance**

  This scenario describes the issuance of a mobile Vehicle Registration Certificate (mVRC) to an end user’s EUDI wallet. The purpose of the scenario is to establish a harmonised, high‑assurance issuance process for an official vehicle registration credential that can be securely stored and later presented by the user across the European Digital Identity Wallet ecosystem.

  
  | Field name | Description | Example values |
  |-----------|-------------|---------------|
  | **Scenario summary** | High-level description of the scenario | The issuance of an mVRC to an end user’s EUDI wallet after successful identity verification and validation of vehicle registration data, ensuring holder binding and cross‑border interoperability. |
  | **User story** | User-centric description | As a vehicle owner, John wants to receive a vehicle registration certificate in his EUDI wallet so that he can use it digitally and securely across the EU. |
  | **Actors** | Actors involved in the scenario | 1. Owner of the vehicle (John) (required); <br> 2. EUDI wallet instance (required); <br> 3. mVRC issuer (required); <br> 4. National vehicle registry (optional); <br> 5. Trusted list provider (optional); <br> 6. PID provider (optional); <br> 7. Wallet provider (optional). |
  | **Context & preconditions** | The conditions that must be met before the scenario starts | 1. John is the owner of the vehicle. <br> 2. John has an activated EUDI wallet. <br> 3. The mVRC issuer is recognised as trusted. <br> 4. Vehicle registration data exists in an authoritative registry. <br> 5. A valid identity credential (PID) is available if required. |
  | **User journey (business flow of events)** | High-level business flow | 1. John initiates the mVRC issuance from the wallet. <br> 2. Identity and vehicle ownership are verified. <br> 3. The issuer validates the registration data. <br> 4. The mVRC is issued. <br> 5. The wallet stores the mVRC and confirms success to the user. |

  ```mermaid
  flowchart TB
    John["John (vehicle owner)"]
    Wallet[John's EUDI wallet]
    Issuer[mVRC issuer]

    John -->|Initiates mVRC issuance| Wallet
    Wallet -->|Requests issuance| Issuer

    Issuer -->|Issues mVRC| Wallet
    Wallet -->|Stores mVRC and confirms issuance| John
  ```

- **Scenario 1B – mVRC remote data sharing**

  This scenario describes the remote presentation and verification of the mVRC data by a vehicle owner through the EUDI wallet in an online context. In this scenario, the user, who already holds a valid mVRC in their EUDI wallet, is requested to share selected vehicle registration data with a remote service provider acting as an mVRC verifier.
  
  The scenario focuses on user control, selective disclosure, interoperability and trust ensuring that only the required data is shared, with the user’s explicit consent, in line with the principles defined in eIDAS 2.0.

  
  | Field name | Description | Example values |
  |-----------|-------------|---------------|
  | **Scenario summary** | High-level description of the scenario | The remote sharing of mVRC data from an end user’s EUDI wallet to an mVRC verifier for an online service, enabling selective disclosure, user control and cross‑border interoperability. |
  | **User story** | User-centric description | As the vehicle owner, John wants to present selected vehicle registration data from his EUDI Wwllet to an authorised party during an in‑person interaction so that he can complete vehicle‑related checks without using physical documents. |
  | **Actors** | Actors involved in the scenario | 1. Owner of the vehicle, e.g. John (required); <br> 2. EUDI wallet instance (required); <br> 3. mVRC verifier (required); <br> 4. mVRC issuer (optional); <br> 5. Trusted list provider (optional). |
  | **Context & preconditions** | The conditions that must be met before the scenario starts | 1. John has an activated EUDI wallet. <br> 2. John holds a valid mVRC in his EUDI wallet. <br> 3. The mVRC was issued by a recognised and trusted mVRC issuer. <br> 4. The mVRC verifier is reachable through a remote (online) interaction. <br> 5. Network connectivity is available. |
  | **User journey (business flow of events)** | High-level business flow | 1. John accesses an online service that requires vehicle registration data. <br> 2. The service requests selected mVRC attributes via the EUDI wallet. <br> 3. John reviews the request and provides explicit consent. <br> 4. The wallet presents the requested mVRC data. <br> 5. The mVRC verifier validates the received data and proceeds with the service. |

  ```mermaid
  flowchart TB
    John["John (vehicle owner)"]
    Wallet[John's EUDI wallet]
    Verifier[mVRC verifier]

    John -->|Initiates online service interaction| Wallet
    Wallet -->|Requests consent for data sharing| John
    John -->|Provides explicit consent| Wallet

    Wallet -->|Presents selected mVRC data| Verifier
    Verifier -->|Validates mVRC data| Wallet

    Wallet -->|Confirms successful data sharing| John
  ```

- **Scenario 1C – mVRC proximity data sharing**

  This scenario describes the proximity presentation and verification of the mVRC data by the vehicle owner through the EUDI wallet. In this scenario, the user, who already holds a valid mVRC in his EUDI wallet, is requested to present selected vehicle registration data to a nearby party (a proximity verifier), for example during roadside checks or other vehicle‑related interactions.

  The scenario focuses on user control, selective disclosure and trust in proximity interactions, ensuring that only the required vehicle registration data is presented, with the user’s explicit consent, in line with the principles defined in eIDAS 2.0.

  
  | Field name | Description | Example values |
  |-----------|-------------|---------------|
  | **Scenario summary** | High-level description of the scenario | The proximity‑based presentation and verification of the mVRC data from an end user’s EUDI wallet to a local verifier, enabling selective disclosure and trusted in‑person interactions. |
  | **User story** | User-centric description | As the vehicle owner, John wants to present selected vehicle registration data from his EUDI wallet during an in‑person interaction so that he can complete vehicle checks without using physical documents. |
  | **Actors** | Actors involved in the scenario | 1. Owner of the vehicle, e.g. John (required); <br> 2. EUDI wallet instance (required); <br> 3. mVRC proximity reader (required); <br> 4. mVRC issuer (optional); <br> 5. Trusted list provider (optional); <br> 6. Wallet provider (optional). |
  | **Context & preconditions** | The conditions that must be met before the scenario starts | 1. John has an activated EUDI wallet. <br> 2. John holds a valid mVRC in his EUDI Wallet. <br> 3. The mVRC was issued by a recognised and trusted mVRC issuer. <br> 4. The proximity reader is physically present and authorised to request the mVRC data. <br> 5. A secure proximity communication channel can be established. |
  | **User journey (business flow of events)** | High-level business flow | 1. John is requested to present some vehicle registration data during an in‑person interaction. <br> 2. The EUDI wallet establishes a proximity connection with the reader. <br> 3. John reviews the request and provides explicit consent. <br> 4. The wallet presents the requested mVRC data. <br> 5. The proximity reader validates the received data and completes the on‑site check or procedure. |

  ```mermaid
  flowchart TB
    John["John (vehicle owner)"]
    Wallet[John's EUDI wallet]
    Reader[mVRC verifier]

    John -->|Initiates or responds to proximity request| Wallet
    Wallet -->|Requests consent for proximity data sharing| John
    John -->|Provides explicit consent| Wallet

    Wallet -->|Presents the selected mVRC data<br/>via proximity interaction| Reader
    Reader -->|Reads and validates mVRC data| Wallet

    Wallet -->|Confirms successful data presentation| John
    ```

---
#### **SCENARIO GROUP 2 – Delegated mVRC**

- **Scenario 2A – issuance of the delegated mVRC (wallet-to-wallet)**

  This scenario describes the issuance of a delegated mVRC from one EUDI wallet to another. In this scenario, the user, who is the owner of the vehicle and the holder of the primary mVRC, grants a consumer the right to use and present the mVRC under defined conditions, without transferring the ownership or the primary holder status.

  The scenario focuses on the controlled delegation, user consent and secure transfer of rights, ensuring that the delegation is explicitly authorised, limited in scope, and managed by the vehicle owner. The delegated mVRC allows the consumer to interact with services requiring vehicle registration data in line with the principles defined in eIDAS 2.0.

  | Field name | Description | Example values |
  |-----------|-------------|---------------|
  | **Scenario summary** | High-level description of the scenario | The issuance of the delegated mVRC from the vehicle owner’s EUDI wallet to a consumer’s wallet, enabling controlled and time‑limited use and presentation of vehicle registration data without transferring ownership. |
  | **User story** | User-centric description | As the vehicle owner, John wants to delegate the right to use and present his vehicle registration certificate to Peter so that Peter can operate the vehicle and interact with services based on the delegated rights. |
  | **Actors** | Actors involved in the scenario | 1. Owner of the vehicle, e.g. John (required); <br> 2. Consumer (a delegated user), e.g. Peter (required); <br> 3. EUDI wallet instance of the owner (required); <br> 4. EUDI wallet instance of the consumer (required); <br> 5. mVRC & delegated mVRC issuer (required); <br> 6. National vehicle registry (optional); <br> 7. Trusted list provider (optional); <br> 8. PID provider (optional); <br> 9. mDL provider (optional); <br> 10. Wallet provider (optional). |
  | **Context & preconditions** | The conditions that must be met before the scenario starts | 1. John has an activated EUDI wallet capable of delegation. <br> 2. John holds a valid mVRC in his EUDI Wallet. <br> 3. Peter has an activated EUDI wallet. <br> 4. The mVRC was issued by a recognised and trusted mVRC issuer. |
  | **User journey (business flow of events)** | High-level business flow | 1. John initiates the delegation process from his EUDI wallet. <br> 2. John defines the delegation scope and conditions (e.g. validity period). <br> 3. John confirms and authorises the delegation. <br> 4. John shares the delegation request with Peter. <br> 5. Peter accepts the delegation using his EUDI wallet. <br> 6. Peter receives and stores the delegated mVRC and can use it for subsequent interactions. |

  ```mermaid
  flowchart TB
    John["John (vehicle owner)"]
    WalletOwner["John's EUDI wallet"]
    Issuer[mVRC & delegated mVRC issuer]
    WalletConsumer["Peter's EUDI wallet"]
    Peter["Peter (consumer)"]

    John -->|Initiates delegation| WalletOwner
    WalletOwner -->|Requests delegation| Issuer

    WalletOwner -->|Defines scope and conditions| Issuer
    John -->|Provides consent| WalletOwner

    Issuer -->|Issues delegated mVRC| WalletConsumer
    WalletConsumer -->|Stores delegated mVRC| Peter

    WalletOwner -->|Confirms delegation| John
  ```

- **Scenario 2B – issuance of the delegated mVRC (organisation-to-wallet)**

  This scenario describes the issuance of a delegated mVRC from an organisation acting as the vehicle owner to a consumer’s EUDI wallet. In this scenario, the organisation, which is the registered owner of the vehicle and associated with the primary mVRC, grants the consumer the right to use and present the mVRC under defined conditions, without transferring any ownership rights.

  The scenario focuses on the controlled delegation, user consent and the secure transfer of usage rights, ensuring that the delegation is explicitly authorised, limited in scope, and managed by the organisation as the vehicle owner. The delegated mVRC enables the consumer to interact with services requiring vehicle registration data, in line with the principles defined in eIDAS 2.0.


  | Field name | Description | Example values |
  |-----------|-------------|---------------|
  | **Scenario summary** | High-level description of the scenario | The issuance of a delegated mVRC from an organisation acting as the vehicle owner to a consumer’s EUDI wallet, enabling controlled and time‑limited use and presentation of vehicle registration data without transferring the ownership. |
  | **User story** | User-centric description | An organisation that owns a vehicle wants to delegate the right to use and present the vehicle registration certificate to Peter so that Peter can operate the vehicle and interact with services. |
  | **Actors** | Actors involved in the scenario | 1. Organisation, acting as the vehicle owner (required); <br> 2. Consumer (a delegated user), e.g. Peter (required); <br> 3. Consumer’s EUDI wallet instance (required); <br> 4. mVRC & delegated mVRC issuer (required); <br> 5. National vehicle registry (optional); <br> 6. Trusted list provider (optional); <br> 7. PID provider (optional); <br> 8. mDL provider (optional); <br> 9. Wallet provider (optional). |
  | **Context & preconditions** | The conditions that must be met before the scenario starts | 1. The organisation is the registered owner of the vehicle and is associated with a valid primary mVRC. <br> 2. The organisation has delegation capabilities within its systems. <br> 3. Peter has an active EUDI Wallet. <br> 4. The mVRC issuer is recognised as trusted. |
  | **User journey (business flow of events)** | High-level business flow | 1. The organisation initiates the delegation process and defines the delegation scope and conditions (e.g. validity period). <br> 2. The organisation authorises the delegation for Peter. <br> 3. Peter initiates the issuance process from his EUDI wallet. <br> 4. The EUDI wallet interacts with the issuer to obtain the delegated mVRC based on the authorised delegation. <br> 5. The issuer issues the delegated mVRC to Peter’s EUDI wallet. <br> 6. Peter receives and stores the delegated mVRC and can use it for subsequent interactions. |

  ```mermaid
  flowchart TB
    Org["Organisation (vehicle owner)"]
    Issuer[mVRC & delegated mVRC issuer]
    WalletConsumer["Peter's EUDI wallet"]
    Peter["Peter (consumer)"]

    Org -->|Defines delegation scope and conditions| Issuer
    Org -->|Authorises delegation| Issuer

    Peter -->|Requests delegated mVRC| WalletConsumer
    WalletConsumer -->|Requests delegated credential| Issuer

    Issuer -->|Issues delegated mVRC| WalletConsumer
    WalletConsumer -->|Stores delegated mVRC| Peter
  ```

- **Scenario 2C – remote presentation of the delegated mVRC**

  This scenario describes the remote presentation and verification of the delegated mVRC data by the consumer (delegated user), who has been granted delegated usage rights and holds a valid delegated mVRC in his EUDI wallet. In this scenario, the consumer is requested to share the selected vehicle registration data with a remote service provider acting as a delegated mVRC verifier.

  The scenario focuses on user control, selective disclosure and interoperability, ensuring that only the required data is shared with the consumer’s explicit consent. The delegated mVRC enables the consumer to interact with remote services, in line with the principles defined in eIDAS 2.0.


  | Field name | Description | Example values |
  |-----------|-------------|---------------|
  | **Scenario summary** | High-level description of the scenario | The remote sharing of the delegated mVRC data from a consumer’s EUDI wallet to a service provider, enabling the consumer (delegated user) to present vehicle registration data. |
  | **User story** | User-centric description | As the consumer, Peter wants to remotely share vehicle registration data from his EUDI wallet with an online service so that he can perform actions based on the rights granted by the vehicle owner without using any physical documents. |
  | **Actors** | Actors involved in the scenario | 1. Consumer (delegated user), e.g. Peter (required); <br> 2. Consumer’s EUDI wallet instance (required); <br> 3. mVRC verifier (required); <br> 4. mVRC issuer (optional); <br> 5. Trusted list provider (optional). |
  | **Context & preconditions** | The conditions that must be met before the scenario starts | 1. Peter holds a valid delegated mVRC in his EUDI wallet. <br> 2. The EUDI wallet is active and capable of remote presentation. <br> 3. The delegated mVRC was issued by a recognised and trusted issuer. <br> 4. The service provider acts as an mVRC (delegated) verifier and is reachable through an online interaction. <br> 5. Network connectivity is available. |
  | **User journey (business flow of events)** | High-level business flow | 1. Peter accesses an online service that requires vehicle registration data. <br> 2. The service requests selected attributes of the delegated mVRC via the EUDI wallet. <br> 3. Peter reviews the request and provides explicit consent. <br> 4. The EUDI wallet presents the requested data of the delegated mVRC to the verifier. <br> 5. The verifier validates the received data and proceeds with the service. |

  ```mermaid
  flowchart TB
    Peter["Peter (consumer)"]
    Wallet[EUDI wallet]
    Verifier["mVRC verifier"]

    Peter -->|Accesses online service| Wallet
    Wallet -->|Requests consent for data sharing| Peter
    Peter -->|Provides explicit consent| Wallet

    Wallet -->|Presents delegated mVRC data| Verifier
    Verifier -->|Validates data| Wallet

    Wallet -->|Confirms successful data sharing| Peter
  ```

- **Scenario 2D – proximity presentation of the delegated mVRC**

  This scenario describes the proximity presentation and verification of the delegated mVRC by a consumer (delegated user), who has been granted delegated usage rights and holds a valid delegated mVRC in their EUDI wallet. In this scenario, the consumer is requested to present selected vehicle registration data to a relying party acting as an mVRC proximity verifier, for example during roadside checks or other on‑site interactions.

  The scenario focuses on user control, selective disclosure and trust in proximity interactions, ensuring that only the required data is presented with the consumer’s explicit consent. The delegated mVRC enables the consumer to perform interactions in local contexts, in line with the principles defined in eIDAS 2.0.

  | Field name | Description | Example values |
  |-----------|-------------|---------------|
  | **Scenario summary** | High-level description of the scenario | The proximity data sharing of the delegated mVRC from the consumer’s EUDI wallet to a local verifier, enabling on site validation of vehicle registration data. |
  | **User story** | User-centric description | As the consumer, Peter wants to present vehicle registration data from his EUDI wallet during an in-person interaction so that he can complete vehicle checks or procedures based on rights granted by the vehicle owner without using physical documents. |
  | **Actors** | Actors involved in the scenario | 1. Consumer (delegated user), e.g. Peter (required); <br> 2. Consumer’s EUDI wallet instance (required); <br> 3. mVRC proximity verifier (required); <br> 4. mVRC proximity reader user (optional, e.g. an officer or operator using the reader); <br> 5. mVRC issuer (delegated) (optional). |
  | **Context & preconditions** | The conditions that must be met before the scenario starts | 1. Peter holds a valid delegated mVRC in his EUDI wallet. <br> 2. The EUDI wallet is capable of proximity interactions. <br> 3. The delegated mVRC was issued by a recognised and trusted issuer. <br> 4. The proximity verifier is physically present and authorised to request the mVRC data. <br> 5. A secure proximity communication channel can be established. |
  | **User journey (business flow of events)** | High-level business flow | 1. Peter opens his EUDI wallet and initiates a proximity presentation. <br> 2. The EUDI wallet generates a QR code containing parameters needed to establish a secure connection and presents it. <br> 3. The proximity verifier scans the QR code and establishes a secure channel to the EUDI wallet. <br> 4. The verifier connects to the EUDI wallet and requests specific mVRC data. <br> 5. Peter reviews the request and provides explicit consent. <br> 6. The EUDI wallet presents the selected delegated mVRC data. <br> 7. The verifier validates the received data and completes the on-site check. |

```mermaid
flowchart TB
    Peter["Peter (consumer)"]
    Wallet["Peter's EUDI wallet"]
    Reader[mVRC proximity verifier]

    Peter -->|Initiates proximity presentation| Wallet
    Wallet -->|Displays pairing information| Reader

    Reader -->|Establishes secure connection| Wallet
    Reader -->|Requests mVRC data| Wallet

    Wallet -->|Requests consent| Peter
    Peter -->|Provides explicit consent| Wallet

    Wallet -->|Presents delegated mVRC data| Reader
    Reader -->|Validates received data| Wallet

    Wallet -->|Confirms successful presentation| Peter
```

---
#### **SCENARIO GROUP 3 – mVRC & mDL presentation**

- **Scenario 3A – mVRC & mDL remote data sharing**

  This scenario describes the remote presentation and verification of both a mobile Driving Licence (mDL) and a mobile Vehicle Registration Certificate (mVRC) within a single transaction using the EUDI wallet. In this scenario, the owner of the vehicle, who holds both credentials in the wallet, is requested to provide selected data from both the mDL and the mVRC to a remote service provider acting as a combined verifier. The scenario addresses the limitation of current solutions, where users are required to present two separate physical documents or a combination of physical and digital credentials.
  
  The scenario focuses on user control, selective disclosure and interoperability, ensuring that only the required data from both credentials is shared with the vehicle owner’s explicit consent, in line with the principles defined in eIDAS 2.0.

  | Field name | Description | Example values |
  |-----------|-------------|---------------|
  | **Scenario summary** | High-level description of the scenario | The remote sharing of both mDL and mVRC data from a vehicle owner’s EUDI wallet to a service provider, enabling combined verification of driving licence and vehicle registration data within a single transaction. |
  | **User story** | User-centric description | As a vehicle owner, John wants to share both his driving licence and vehicle registration data from his EUDI wallet in a single interaction so that he can complete vehicle related services without presenting multiple documents separately. |
  | **Actors** | Actors involved in the scenario | 1. Owner, e.g. John (required); <br> 2. EUDI wallet instance (required); <br> 3. mVRC & mDL verifier (required); <br> 4. mVRC issuer (optional); <br> 5. mDL issuer (optional); <br> 6. Trusted list provider (optional). |
  | **Context & preconditions** | The conditions that must be met before the scenario starts | 1. John has an activated EUDI wallet. <br> 2. John holds a valid mDL and mVRC in the EUDI wallet. <br> 3. Both credentials were issued by recognised and trusted issuers. <br> 4. The EUDI wallet supports combined presentation of multiple credentials. <br> 5. The verifier is reachable through an online interaction. <br> 6. Network connectivity is available. |
  | **User journey (business flow of events)** | High-level business flow | 1. John accesses an online service that requires both driving licence and vehicle registration data. <br> 2. The service requests selected attributes from both mDL and mVRC via the EUDI wallet. <br> 3. John reviews the combined request and provides explicit consent. <br> 4. The EUDI wallet presents the requested data from both credentials to the verifier. <br> 5. The verifier validates the received data and proceeds with the service. |

  ```mermaid
  flowchart TB
    John["John (vehicle owner)"]
    Wallet[EUDI wallet]
    Verifier[mVRC & mDL verifier]

    John -->|Accesses online service| Wallet
    Wallet -->|Requests combined data sharing| John
    John -->|Provides explicit consent| Wallet

    Wallet -->|Presents mDL and mVRC data| Verifier
    Verifier -->|Validates received data| Wallet

    Wallet -->|Confirms successful presentation| John
  ```

- **Scenario 3B – mVRC & mDL proximity data sharing**

  This scenario describes the proximity presentation and verification of both a mobile Driving Licence (mDL) and a mobile Vehicle Registration Certificate (mVRC) within a single transaction using the EUDI wallet. In this scenario, the owner of the vehicle, who holds both credentials in the Wallet, is requested to present selected data from both credentials to a nearby party acting as a combined mVRC & mDL proximity verifier, for example during roadside checks or other on‑site interactions. The scenario addresses the limitations of current practices, where the users are required to present multiple physical documents separately.
  
  The scenario focuses on user control, selective disclosure and trust in proximity interactions, ensuring that only the required data from both credentials is presented with the user’s explicit consent, in line with the principles defined in eIDAS 2.0.

  | Field name | Description | Example values |
  |-----------|-------------|---------------|
  | **Scenario summary** | High-level description of the scenario | The proximity sharing of both mDL and mVRC data from a vehicle owner’s EUDI wallet to a local verifier, enabling combined verification of driving licence and vehicle registration data in a single interaction. |
  | **User story** | User-centric description | As the vehicle owner, John wants to present both his driving licence and vehicle registration data from his EUDI wallet during an in-person interaction so that he can complete checks without presenting multiple documents separately. |
  | **Actors** | Actors involved in the scenario | 1. Owner, e.g. John (required); <br> 2. EUDI wallet instance (required); <br> 3. mVRC & mDL proximity verifier (required); <br> 4. mVRC & mDL proximity reader (optional); <br> 5. mVRC issuer (optional); <br> 6. mDL issuer (optional); <br> 7. Trusted list provider (optional). |
  | **Context & preconditions** | The conditions that must be met before the scenario starts | 1. John has an activated EUDI wallet. <br> 2. John holds a valid mDL and mVRC in his EUDI wallet. <br> 3. The EUDI wallet is capable of proximity interactions. <br> 4. Both credentials were issued by recognised and trusted issuers. <br> 5. The verifier is physically present and authorised to request data. <br> 6. A secure proximity communication channel can be established. |
  | **User journey (business flow of events)** | High-level business flow | 1. John opens the EUDI wallet and initiates a proximity presentation. <br> 2. The EUDI wallet generates a QR code containing parameters needed to establish a secure connection and presents it. <br> 3. The proximity verifier scans the QR code and establishes a secure channel to the EUDI wallet. <br> 4. The verifier connects to the EUDI wallet and requests specific mDL and mVRC data. <br> 5. John reviews the request and provides explicit consent. <br> 6. The EUDI wallet presents the selected mVRC and mDL data. <br> 7. The verifier validates the received data and completes the on-site check. |

  ```mermaid
  flowchart TB
    John["John (vehicle owner)"]
    Wallet[EUDI wallet]
    Reader[mVRC & mDL proximity verifier]

    John -->|Initiates proximity interaction| Wallet
    Wallet -->|Displays pairing information| Reader

    Reader -->|Establishes secure connection| Wallet
    Reader -->|Requests combined mDL and mVRC data| Wallet

    Wallet -->|Requests consent| John
    John -->|Provides explicit consent| Wallet

    Wallet -->|Presents mDL and mVRC data| Reader
    Reader -->|Validates received data| Wallet

    Wallet -->|Confirms successful presentation| John
  ```

## 7 High level requirements (per role)

This section defines the high-level requirements for the roles involved across the scenarios described in this document.

The requirements are derived from:

  - the ARF definition of the wallet's functionality and user control,
  - interaction models defined in OpenID4VCI and OpenID4VP,
  - regulatory principles defined in eIDAS 2.0, including explicit user consent and data minimisation,
  - and, where applicable, the delegation model introduced within the LSP scenarios.

The requirements establish a common baseline of capabilities necessary to ensure interoperability, security and compliance with the principles defined in eIDAS 2.0 and the Architecture and Reference Framework (ARF). They are defined independently of specific scenarios and reflect the functional and trust related responsibilities of each role within the European Digital Identity Wallet ecosystem.

- **User – as an owner / holder / consumer**
  
  The user, acting as an owner or holder of credentials (mVRC or mDL), and, where applicable, as a delegated user (consumer), SHALL fulfil the following requirements.
  
  **Core control and interaction capabilities**

  The user SHALL:

  - control the use of the EUDI wallet and all credentials stored within it;
  - be able to receive and securely store the credentials issued to the wallet;
  - be able to initiate interactions, including issuance, presentation and delegation processes;
  - retain control over when and how the credentials are used or presented;
  - be able to access and manage the credentials held in the wallet.

  **Credential issuance**
  
  The user SHALL:

  - be able to accept or reject credential issuance requests;
  - ensure that the issued credentials are stored securely in the EUDI wallet;
  - control whether the credentials are retained or deleted within the wallet.

  **Consent and data disclosure**

  In line with the eIDAS 2.0 and ARF principles, the user SHALL:

  - review data requests prior to any disclosure;
  - provide explicit and informed consent before sharing any credential data;
  - be able to refuse or cancel any data sharing requests;
  - be informed about which data elements are being requested and for what purpose;
  - dispose of a wallet supporting selective disclosure mechanisms to share only the minimum required mVRC data.

  **Presentation of the credentials**

  The user SHALL: 
  - be able to trigger the presentation of the credentials through the EUDI wallet;
  - be able to present selected attributes from one or multiple credentials;
  - use the credentials in a manner consistent with the granted rights and applicable constraints.

  **Delegation model (LSP requirements)**

  The delegation model introduced in the LSP scenarios extends the standard owner / holder model by allowing controlled sharing of usage rights.

  The owner / primary holder SHALL:

  - be able to grant delegated usage rights for the mVRC;
  - define the scope and conditions of the delegation (e.g. validity period);
  - retain control over all the active delegations;
  - be able to revoke the delegated rights at any time;
  - ensure that delegation does not transfer any ownership or primary holder status.

  The consumer SHALL:

  - be able to receive the delegated credentials into the EUDI wallet;
  - use the delegated credentials in accordance with the defined scope and conditions;
  - be able to present the delegated credentials when required;
  - understand that the usage rights are derived from the delegation and may be revoked.

- **EUDI wallet instances**

  The EUDI wallet instances SHALL:

  - securely store the credentials and associated cryptographic material;
  - enforce holder binding between the credential and the user controlling the wallet;
  - support credential issuance flows using OpenID4VCI;
  - support presentation flows based on OpenID4VP;
  - support issuance, storage and presentation of the delegated mVRC;
  - enforce explicit user consent prior to any data disclosure;
  - support the selective disclosure of attributes;
  - enable presentation of an mVRC or the mVRC together with an mDL within a single interaction;
  - support both remote and proximity interaction models;
  - ensure secure communication with issuers and verifiers;
  - support the management of the delegated credentials where applicable.

- **Issuers (mVRC, delegated mVRC, mDL)**

  Issuers SHALL: 

  - verify the identity and eligibility of the subject prior to credential issuance, where applicable; 
  - issue credentials compliant with ARF and relevant standards (OpenID4VCI, mdoc format); 
  - ensure integrity and authenticity of the credentials through cryptographic signing; 
  - bind the credentials to the intended holder where required; 
  - support issuance flows compatible with EUDI wallet interactions; 
  - ensure that the issued credentials can be validated across the member states.

- **Verifiers (remote and proximity)**

  Verifiers SHALL:

  - request only the minimum set of attributes required for a given use case;
  - support request and processing of credential presentations using OpenID4VP;
  - validate the authenticity, integrity and validity of the presented credentials;
  - verify trust anchors and certificate status using appropriate trust infrastructure;
  - support both single‑credential and multi‑credential scenarios (e.g. mVRC and mDL);
  - ensure secure communication with the EUDI wallet;
  - provide transparency to the user regarding requested data.

- **Other optional supporting roles**

  Optional actors such as PID providers, national registries, mDL providers or wallet providers SHALL:

  - support identity verification processes;
  - provide authoritative data used in the credential issuance;
  - enable supporting infrastructure required for wallet operation;
  - contribute to interoperability across implementations and the member states.

## 8 Technical details of the scenarios

The technical approach for the mVRC is defined for the purpose of this LSP and reflects a jointly agreed baseline for the implementation and testing of the scenarios. While tailored to the needs of the pilot phase,  it will allow reuse and extension in future production environments. The approach has been developed collaboratively with the WP5 members. For some scenarios, different implementation options were considered, and a common baseline was agreed through joint discussions in order to ensure interoperability and consistency across participating implementations.

The mVRC ecosystem described in this document builds on a set of requirements derived from the applicable regulatory frameworks, including eIDAS 2.0, as well as established technical standards and specifications. It is designed to be fully aligned with the EUDI wallet framework as an integral part of its ecosystem. The design combines standardised protocols, credential formats and trust mechanisms to ensure that the scenarios can be implemented consistently across different systems and jurisdictions. The technical approach ensures compliance with the EUDI wallet trust and security principles, including user control, data minimisation and selective disclosure. The following represent some of the key technical principles and foundational building blocks:

- **Credential security and data protection**
  -	Cryptographic binding and proof‑of‑possession, ensuring that credentials can only be used by the legitimate holder;
  -	Selective disclosure, enabling sharing of only the required data elements in line with the data minimisation principles;

- **Credential formats and data structures**
  -	ISO/IEC 18013‑5 (mdoc format), providing a standardised structure for credentials;
  -	ISO/IEC 7367-2, providing the data structure for the mobile vehicle registration certificate (mVRC).

- **Issuance and presentation protocols**
  -	OpenID for Verifiable Credential Issuance (OpenID4VCI) 1.0, aligned with the High Assurance Interoperability Profile (HAIP) 1.0, supporting secure and interoperable credential issuance;
  -	OpenID for Verifiable Presentations (OpenID4VP) 1.0, enabling structured, consent‑based presentation of credential data;
  -	OAuth 2.0, providing the underlying authorisation framework for secure interaction flows;

- **Proximity interaction layer**
  -	Proximity interaction mechanisms based on ISO/IEC 18013‑5, enabling secure device to device communication in proximity scenarios;

- **Trust and regulatory framework**
  -	Electronic Signatures and Trust Infrastructures (ETSI TS 119 472 series), defining profiles for Electronic Attestation of Attributes (EAA), including credential structure and issuance processes;
  -	Trust and validation mechanisms aligned with eIDAS trust models, including the use of the EU trusted lists (e.g. ETSI TS 119 612).

Implementation libraries or reusable software components supporting mVRC scenarios should be published in the project GitHub repository and kept available and reasonably up-to-date for the duration of the relevant implementation and interoperability activities.

### 8.1 Scenario 1A – mVRC issuance

#### 8.1.1 Functional requirements

Scenario 1A is based on OpenID4VCI 1.0 aligned with the High Assurance Interoperability Profile (HAIP) 1.0 and leverages standardised trust frameworks and credential formats to ensure interoperable issuance of the mVRC attestations to the EUDI wallet.

**EUDI Wallet Instance**

| Index | Requirement title | Description | Priority | Acceptance criteria |
|------------|------------------|-------------|--------|---------------------|
| FR-W1A-001 | OpenID4VCI Issuance Support with HAIP 1.0  | EUDI wallet SHALL support the OpenID4VCI 1.0 workflow in HAIP 1.0 to obtain mVRC attestations, including credential offers, authorization, token handling, and credential requests. | High | Wallet successfully completes an OpenID4VCI issuance flow and receives an mVRC attestation. |
| FR-W1A-002 | mVRC Data Model and Structure Support | The EUDI Wallet Instance SHALL support processing, storage, and presentation of mVRC credentials using a data model and structure compliant with ISO 7367 and the applicable mVRC rulebook, ensuring consistent interpretation of mVRC data across issuers and verifiers. | High | The wallet correctly processes and presents mVRC credentials conforming to the standardized data model and structure without data loss or misinterpretation. |
| FR-W1A-003 | mVRC Credential Format Support | EUDI wallet SHALL support receiving, processing, and storing mVRC attestations encoded as mso_mdoc. | High | Wallet stores and later retrieves an issued mVRC in mso_mdoc format. |
| FR-W1A-004 | Credential Offer Initialisation | EUDI wallet SHALL support both cross device and same device flows (QR code or deep link) . | High | Issuance succeeds using both redirect-based and wallet-initiated initiation mechanisms. |
| FR-W1A-005 | User Consent for  Issuance | EUDI wallet SHALL display information about offered mVRC to be issued and require explicit user consent before proceeding. | High | User can approve or cancel issuance after reviewing credential information. |
| FR-W1A-006 | PAR Endpoint Support | The wallet SHALL support Pushed Authorization Requests (PAR) when required by the authorization server policy. | High | Wallet initiates authorization using PAR and receives a request URI. |
| FR-W1A-007 | PKCE Support | The wallet SHALL support PKCE for authorization code flows, including code verifier and challenge handling. | High | Token exchange succeeds only with a valid PKCE code verifier. |
| FR-W1A-008 | Client Attestation JWT Support | The wallet shall support client authentication using Client Attestation JWT where required. | High | Authorization server accepts token requests authenticated with Client Attestation JWT. |
| FR-W1A-009 | Owner Identity Verification Support | The wallet SHOULD be able to perform PID-based identity verification when the issuer requires confirmation of the vehicle owner’s identity prior to mVRC issuance. | Medium | Wallet completes issuance when owner identity verification succeeds and fails when it is required but not completed. |
| FR-W1A-010 | OpenID4VP Identity Verification Support | If applicable, EUDI wallet SHALL support OpenID4VP 1.0 to present a PID attestation for identity verification when required prior to mVRC issuance. | Medium | Wallet successfully responds to an OpenID4VP presentation request requiring PID verification. |
| FR-W1A-011 | PID Attestation Format Support | If applicable, EUDI wallet SHALL present PID attestations encoded as mso_mdoc or SD-JWT VC. | Medium | Wallet presents PID attestations in both supported formats when requested. |
| FR-W1A-012 | User Consent for  Verification | If applicable, EUDI wallet SHALL display information about requested PID data prior to mVRC issuance and require explicit user consent before proceeding. | Medium | User can approve or cancel verification proces after reviewing authorization request. |
| FR-W1A-013 | Wallet Unit Attestation (WUA) in Proof | The wallet SHALL include a Wallet Unit Attestation (WUA), as defined in ARF TS 3, in the proof sent to the credential endpoint when required. | High | Issuer validates WUA and issues mVRC only when WUA is present. |
| FR-W1A-014 | Holder Binding and Proof-of-Possession | EUDI wallet SHALL support holder binding and proof-of-possession mechanisms in line with HAIP requirements. | High | Issuance succeeds only when valid proof-of-possession is provided. |
| FR-W1A-015 | Display of mVRC Credential Data | The EUDI Wallet SHALL display the core data contained in a successfully issued mVRC credential to the user after completion of the issuance process. | High | The EUDI Wallet displays the mVRC credential only after successful issuance and validation, with data accurately reflecting the credential payload.<br> If issuance or validation fails, the mVRC credential is not displayed to the user.
| FR-W1A-016 | Secure Storage of mVRC | EUDI wallet SHOULD securely store issued mVRC attestations and associated metadata. | High | Issued mVRC is securely stored and accessible only with user authorization. |
| FR-W1A-017 | Protocol Error Handling | EUDI wallet SHALL handle protocol, validation, and network errors gracefully and inform the user. | Medium | Wallet displays meaningful error messages when issuance fails. |
| FR-W1A-018 | Issuer Access Certificate Validation (ETSI TL) | The wallet SHOULD validate the issuer’s access certificate using an ETSI Trusted List where applicable. | Medium | Wallet accepts issuers with trusted certificates and rejects invalid ones. |
| FR-W1A-019 | Issuer Registration Certificate Validation (ETSI TL) | The wallet SHOULD validate the issuer’s registration certificate using an ETSI Trusted List where required. | Medium | Wallet rejects issuance from issuers with invalid registration status. |
| FR-W1A-020 | Issuer Seal Validation (ETSI TL) | The wallet SHOULD validate the cryptographic seal on the issued mVRC using trusted list material. | Medium | Wallet stores only mVRC attestations signed by trusted issuers. |
| FR-W1A-021 | DPoP Support | The Wallet SHALL support DPoP for token requests and related proof handling when required by the Authorization Server. | High | The wallet successfully completes token requests when DPoP is required. Requests with missing, invalid, or expired DPoP proof are rejected. |
| FR-W1A-022 | ETSI Issuance Profile Support | The EUDI Wallet Instance SHALL support the applicable provisions of the ETSI issuance profile used in the scenario. | High | The wallet successfully completes issuance flows that apply the ETSI issuance profile requirements. Flows fail when required profile elements are missing or invalid. |
| FR-W1A-023 | Interactive Authorization Endpoint Support | The EUDI Wallet Instance MAY support the Interactive Authorization Endpoint as an alternative authorization interaction model for credential issuance. | Medium | The wallet successfully completes issuance using the Interactive Authorization Endpoint when supported by the Issuer. |

**mVRC issuer**

| Index | Requirement title | Description | Priority | Acceptance criteria |
|----------|------------------|-------------|----------|---------------------|
| FR-I1A-001 | Issue mVRC using OpenID4VCI 1.0 with HAIP 1.0 | The Issuer SHALL implement OpenID4VCI 1.0 in HAIP 1.0 to issue mVRC attestations, including support for credential offers, authorization, token-based access, and the credential endpoint. | High | A wallet can complete an OpenID4VCI issuance flow in authorization code flow and the Issuer returns an mVRC credential response successfully. |
| FR-I1A-002 | mVRC Data Model and Structure Compliance | The mVRC Issuer SHALL issue mVRC credentials using a data model and structure compliant with ISO 7367 and the applicable mVRC rulebook, ensuring consistent semantics, field definitions, and encoding across issuers and jurisdictions. | High | Issued mVRC credentials conform to the standardized data model and structure and are successfully processed by compliant EUDI Wallets |
| FR-I1A-003 | Provide Credential Issuer Metadata | The Issuer SHALL expose OpenID4VCI Credential Issuer Metadata (/.well-known/openid-credential-issuer) describing supported credential types, formats, endpoints, and issuance requirements. | High | The wallet retrieves issuer metadata and can determine the required endpoints, supported formats, and supported credential configurations for mVRC. |
| FR-I1A-004 | Provide Credential Offer for issuance initiation | The Issuer SHALL generate and provide a credential offer (object or credential_offer_uri) that can be encoded as a QR code or deep link to initiate issuance. | High | A user can open an issuer page, obtain a QR/deep link, and the wallet can resolve the offer and start issuance. |
| FR-I1A-005 | OAuth/OID4VCI Authorization Server for issuance | The Issuer SHALL provide (or integrate with) an OAuth 2.0 / OpenID4VCI to authorize wallet access to issuance and issue access tokens for the credential endpoint. | High | The wallet obtains an authorization code and exchanges it for an access token that is accepted by the credential endpoint. |
| FR-I1A-006 | Publish Authorization Server metadata | The Authorization Server shall expose authorization server metadata (/.well-known/oauth-authorization-server) including required endpoints and capabilities (token, authorization, PAR if used). | High | The wallet retrieves AS metadata and can locate the authorization and token endpoints (and PAR endpoint if required). |
| FR-I1A-007 | Support for Pushed Auth Request | The Authorization Server shall support Pushed Authorization Requests (PAR). | High | The wallet sends an authorization request to PAR, receives a request_uri, and completes authorization successfully. |
| FR-I1A-008 | Support for PKCE | The Authorization Server shall require and validate PKCE for authorization code flows. | High | Token exchange succeeds with a valid code_verifier and fails with an invalid code_verifier. |
| FR-I1A-009 | Support Client Attestation JWT authentication | The Authorization Server shall support client authentication using Client Attestation JWT. | High | Token requests authenticated with a valid Client Attestation JWT succeed; invalid/expired attestations are rejected. |
| FR-I1A-010 | Vehicle Owner identity verification via OpenID4VP | The Issuer/AS may require confirmation of the vehicle owner’s identity prior to issuing mVRC; when required, the Issuer shall enforce OpenID4VP-based PID verification before completing authorization/issuance. | Medium | If policy requires verification, issuance is blocked until a valid PID presentation is received; if policy does not require it, issuance proceeds without VP. |
| FR-I1A-011 | Verifier interface for PID validation (OpenID4VP 1.0) | When owner identity verification is used, the Issuer SHALL implement a Verifier interface compliant with OpenID4VP 1.0 to request and validate PID presentations (mso_mdoc or SD-JWT VC). | Medium | The verifier accepts a valid PID presentation satisfying the presentation definition and returns a success result; invalid presentations are rejected. |
| FR-I1A-012 | Key Binding during mVRC Issuance| The mVRC Issuer SHALL support a key binding mechanism during the issuance of mVRC credentials, binding the issued credential to a cryptographic key controlled by the EUDI Wallet holder. | High |The Issuer verifies a cryptographic proof of possession of a wallet-controlled private key during mVRC issuance and binds the credential to the corresponding public key.<be>If key binding verification fails, the mVRC credential is not issued. |
| FR-I1A-013 | Vehicle Registry integration  | The Issuer MAY query an Vehicle Registry to retrieve authoritative vehicle/owner attributes used to populate the issued mVRC attestation. | Medium | When enabled, the Issuer retrieves registry data and the issued mVRC reflects those authoritative attributes; if no record is found, issuance fails with an appropriate error. |
| FR-I1A-014 | Nonce endpoint support  | The Issuer SHOULD expose a nonce endpoint to provide a c_nonce (and expiry) for proof freshness, where required by policy. | Medium | The wallet can obtain a c_nonce from the nonce endpoint and issuance succeeds using a fresh proof; stale nonce results in a rejected credential request. |
| FR-I1A-015 | Validate wallet proof-of-possession | The Issuer shall validate proof-of-possession in credential requests to ensure holder binding and prevent replay, aligned with the applicable ecosystem profile. | High | Credential issuance succeeds with a valid proof and fails if the proof is missing, invalid, or replayed. |
| FR-I1A-016 | Validate Wallet Unit Attestation (WUA) in proof (ARF TS 3) | When required by policy, the Issuer shall validate the Wallet Unit Attestation (WUA) embedded in the wallet’s proof as defined in ARF TS 3, and reject requests where WUA is missing. | High | Credential requests with WUA are accepted; requests without WUA (when required) or with invalid WUA are rejected. |
| FR-I1A-017 | PID seal trust verification | The Issuer (Verifier) SHOULD validate keys/certificates/seals using trusted lists where applicable (ETSI TL), either online or via cached material. | Medium | Issuer (Verifier) rejects interactions that do not satisfy trust policy (e.g., untrusted seals) and proceeds for trusted ones. |
| FR-I1A-018 | WUA seal trust verification | The Issuer (Verifier) SHOULD validate keys/certificates/seals using trusted lists where applicable (ETSI TL), either online or via cached material. | Medium | Issuer rejects interactions that do not satisfy trust policy (e.g., untrusted seals) and proceeds for trusted ones. |
| FR-I1A-019 | Notification endpoint support | The Issuer MAY expose a notification endpoint for the wallet to send issuance acknowledgements or status notifications. | Medium | After successful issuance, the wallet can send a notification and the Issuer responds with success without affecting issuance outcome. |
| FR-I1A-020 | PID status list verification | The mVRC issuer (verifier) SHOULD verify the PID instance using the PID status list upon receiving the PID presentation. | Medium | The issuer rejects mVRC issuance process if the PID instance status is not valid. |
| FR-I1A-021 | Error handling and standards-compliant responses | The Issuer shall return standards-compliant error responses for invalid requests, unsupported formats, missing prerequisites (e.g., verification required), and policy violations. | High | Negative tests produce deterministic, protocol-compliant errors that the wallet can surface to the user. |
| FR-I1A-022 | Support secure session management for issuance | The Issuer SHALL manage issuance sessions securely (state/nonce, anti-CSRF, replay protection) across browser redirects and wallet interactions. | High | The authorization completes only for matching state/nonce/session context; mismatches are rejected. |
| FR-I1A-023 | Support mVRC Status List | The mVRC Issuer SHOULD support the use of a status list mechanism for issued mVRC credentials in order to enable revocation and suspension checks throughout the credential lifecycle. The Issuer SHALL publish and maintain a status list endpoint compliant with the applicable VC status list specification and include a reference to the corresponding status entry in each issued mVRC credential. The status list SHALL be kept up to date to accurately reflect the current validity state of issued mVRC credentials. | Medium | * An issued mVRC credential contains a valid reference to a status list entry<br> * The wallet or verifier can retrieve the referenced status list from the Issuer (or a designated status list service) <br> * The status value correctly reflects the credential state (e.g. valid, revoked, suspended)<br> * Updating the status list (e.g. marking a credential as revoked) is reflected in subsequent status checks without re-issuance of the credential. |
| FR-I1A-024 | Support DPoP | The Authorization Server shall support DPoP for token requests. | High | Token requests with a valid DPoP proof succeed; requests with missing or invalid DPoP proof are rejected. |
| FR-I1A-025 | ETSI Issuance Profile Support | The mVRC Issuer SHALL support the applicable provisions of the ETSI issuance profile used in the scenario. | High | The Issuer successfully processes issuance flows that apply the ETSI issuance profile requirements. Requests with missing or invalid required profile elements are rejected. |
| FR-I1A-026 | Interactive Authorization Endpoint Support | The Authorization Server MAY support the Interactive Authorization Endpoint as an alternative authorization interaction model for credential issuance. | Medium | The Issuer successfully completes issuance using the Interactive Authorization Endpoint when supported by the Wallet. |

---

#### 8.1.2 Protocol profile

**OpenID4VCI**

Specification: OpenID for Verifiable Credential Issuance 1.0  
Profile: High Assurance Interoperability Profile (HAIP) 1.0  
Flow: Authoriszation Code Flow


Key characteristics:
- Credential issuance initiated via a credential offer (QR code or deep link);
- Supported credential offer schemes: haip-vci and openid-credential-offer;
- Credential format: mso_mdoc;
- Use of OAuth 2.0 Pushed Authoriszation Requests (PAR - RFC 9126);
- Proof Key for Code Exchange (PKCE - RFC 7636);
- Client authentication using Client Attestation JWT;
- Holder binding using proof-of-possession mechanisms;

Implementation characteristics:
- Authoriszation flow using Authoriszation Code Flow with PKCE;
- Issuance mode: immediate issuance;
- Request URI methods: GET and POST;

<br>

**OpenID4VP**

Key characteristics:
- Request/response based presentation flow using authoriszation requests;
- Support for response mode: direct_post.jwt;
- Credential format: mso_mdoc;
- Selective disclosure of the requested attributes;
- Holder binding using proof-of-possession mechanisms;
- Optional use for identity verification (e.g. PID presentation);

Implementation characteristics:
- Supported request schemes: haip-vp, openid4vp, mdoc-openid4vp;
- Authorization requests are implemented using JSON Web Token (JAR) by reference;
- Response mode: direct_post.jwt;
- Credential format: mso_mdoc;
- Client identifier prefix type: x509_hash (as defined in HAIP 1.0);
- Use of nonce values to ensure replay protection;

---

#### 8.1.3	Trust and security mechanisms

The scenario relies on a combination of cryptographic and trust mechanisms, including:

- Holder binding and proof-of-possession (PoP)
- Client authentication using Client Attestation JWT
- Wallet attestation mechanisms, including Wallet Unit Attestation (WUA) and Wallet Instance Attestation (WIA), as defined in ARF TS 3
- Validation of issuer and wallet trust anchors using ETSI Trusted Lists (e.g. ETSI TS 119 612)
- Alignment with ETSI TS 119 472 issuance profiles

---

#### 8.1.4	Endpoints

The following endpoints are used as part of the issuance flow:

| Standard | Endpoint | Usage in Scenario | Reference |
|----------|----------|------------------|-----------|
| OpenID4VCI 1.0 / HAIP 1.0 / ETSI TS 119 472-3 | Credential Offer Endpoint | Required | [OpenID4VCI 1.0](https://openid.net/specs/openid-4-verifiable-credential-issuance-1_0.html#section-4), [HAIP 1.0](https://openid.net/specs/openid4vc-high-assurance-interoperability-profile-1_0.html#section-4.2), [ETSI TS 119 472-3](https://www.etsi.org/deliver/etsi_ts/119400_119499/11947203/01.01.01_60/ts_11947203v010101p.pdf)  |
| OpenID4VCI 1.0 / HAIP 1.0 / ETSI TS 119 472-3 | Authorization Endpoint | Required | [OpenID4VCI 1.0](https://openid.net/specs/openid-4-verifiable-credential-issuance-1_0.html#name-authorization-endpoint), [HAIP 1.0](https://openid.net/specs/openid4vc-high-assurance-interoperability-profile-1_0.html#section-4.3), [ETSI TS 119 472-3](https://www.etsi.org/deliver/etsi_ts/119400_119499/11947203/01.01.01_60/ts_11947203v010101p.pdf) |
| RFC 9126 / OpenID4VCI 1.0 / HAIP 1.0 / ETSI TS 119 472-3 | Pushed Authorization Request (PAR) | Required | [RFC 9126](https://www.rfc-editor.org/rfc/rfc9126.html), [OpenID4VCI 1.0](https://openid.net/specs/openid-4-verifiable-credential-issuance-1_0.html#section-5.1.4), [ETSI TS 119 472-3](https://www.etsi.org/deliver/etsi_ts/119400_119499/11947203/01.01.01_60/ts_11947203v010101p.pdf) |
| OpenID4VCI 1.0 / HAIP 1.0 / ETSI TS 119 472-3 | Token Endpoint | Required | [OpenID4VCI 1.0](https://openid.net/specs/openid-4-verifiable-credential-issuance-1_0.html#section-6), [HAIP 1.0](https://openid.net/specs/openid4vc-high-assurance-interoperability-profile-1_0.html#section-4.4), [ETSI TS 119 472-3](https://www.etsi.org/deliver/etsi_ts/119400_119499/11947203/01.01.01_60/ts_11947203v010101p.pdf)  |
| OpenID4VCI 1.0 / HAIP 1.0 | Nonce Endpoint | Required | [OpenID4VCI 1.0](https://openid.net/specs/openid-4-verifiable-credential-issuance-1_0.html#section-7) |
| OpenID4VCI 1.0 / HAIP 1.0 / ETSI TS 119 472-3 | Credential Endpoint | Required | [OpenID4VCI 1.0](https://openid.net/specs/openid-4-verifiable-credential-issuance-1_0.html#section-8), [HAIP 1.0](https://openid.net/specs/openid4vc-high-assurance-interoperability-profile-1_0.html#section-4.5), [ETSI TS 119 472-3](https://www.etsi.org/deliver/etsi_ts/119400_119499/11947203/01.01.01_60/ts_11947203v010101p.pdf) |
| OpenID4VCI 1.0 / ETSI TS 119 472-3 | Notification Endpoint | Optional | [OpenID4VCI 1.0](https://openid.net/specs/openid-4-verifiable-credential-issuance-1_0.html#section-11), [ETSI TS 119 472-3](https://www.etsi.org/deliver/etsi_ts/119400_119499/11947203/01.01.01_60/ts_11947203v010101p.pdf) |
| OpenID4VCI 1.0 / HAIP 1.0 / ETSI TS 119 472-3 | Credential Issuer Metadata Endpoint | Required | [OpenID4VCI 1.0](https://openid.net/specs/openid-4-verifiable-credential-issuance-1_0.html#section-12.2), [HAIP 1.0](https://openid.net/specs/openid4vc-high-assurance-interoperability-profile-1_0.html#section-4.1), [ETSI TS 119 472-3](https://www.etsi.org/deliver/etsi_ts/119400_119499/11947203/01.01.01_60/ts_11947203v010101p.pdf) |
| RFC 8414 / OpenID4VCI 1.0 | Authorization Server Metadata Endpoint | Required | [RFC 8414](https://datatracker.ietf.org/doc/html/rfc8414), [Attestation-Based Client Authentication](https://www.ietf.org/archive/id/draft-ietf-oauth-attestation-based-client-auth-08.html#name-authorization-server-metada), [DPOP](https://www.rfc-editor.org/rfc/rfc9449.html#section-5.1), [OpenID4VCI 1.1 draft](https://openid.github.io/OpenID4VCI/openid-4-verifiable-credential-issuance-1_1-wg-draft.html#name-interactive-authorization-e)  |
| Token Status List | Status List Endpoint | Optional | [Token Status List](https://datatracker.ietf.org/doc/draft-ietf-oauth-status-list/) |
| OpenID4VCI 1.1 draft | Interactive Authorization Endpoint (`/iae`) | Optional | [OpenID4VCI 1.1 draft](https://openid.github.io/OpenID4VCI/openid-4-verifiable-credential-issuance-1_1-wg-draft.html#name-interactive-authorization-e) |
| OpenID4VP 1.0 / HAIP 1.0 | Authorization Endpoint | Required | [OpenID4VP 1.0](https://openid.net/specs/openid-4-verifiable-presentations-1_0.html#section-5), [HAIP 1.0](https://openid.net/specs/openid4vc-high-assurance-interoperability-profile-1_0.html#section-5) |
| OpenID4VP 1.0 | Direct POST JWT | Required | [OpenID4VP 1.0](https://openid.net/specs/openid-4-verifiable-presentations-1_0.html#section-8.3.1) |
| Implementation-specific | Init Endpoint | Optional | N/A |
| Implementation-specific | Status Endpoint | Optional | N/A |

---

#### 8.1.5	Technical interaction flow / sequence diagrams

The following sequence diagram reflects the OpenID4VCI issuance process of the scenario 1A and illustrates the technical interaction flow, showing the main steps and exchanges between the EUDI wallet, the mVRC issuer and supporting components.

##### Basic flow

```mermaid
flowchart LR
  subgraph WALLET[Wallet provider]
    W[EUDI Wallet Instance]
  end

  subgraph ISSUER[mVRC Issuer]
    AS[Authorization Server\ OpenID4VCI]
    I[Issuer API\ OpenID4VCI]
  end


  W -->|OpenID4VCI \<br>OAuth| AS
  W -->|OpenID4VCI| I
```

##### Sequence diagram

```mermaid
sequenceDiagram
  autonumber
  actor U as User
  participant W as EUDI Wallet instance
  participant B as mVRC Issuer web app(frontend)
  participant I as mVRC Issuer - Issuer API (OpenID4VCI)
  participant AS as mVRC Issuer - Authorization Server (OpenID4VCI)

  %% =========================
  %% 1) Issuer UI prepares a Credential Offer (QR / deep link)
  %% =========================
 U->>B: Open issuer start page
  B->>I: POST /init (prepare credential offer parameters)
   I->>B: response with QR Code and credetial offer
   B->>U: Display QR + deep link button (credential_offer_uri)
   B->>I: GET /status
   I-->>B: http 201 
  loop
  B->>I: GET /status poll request
  I->>B: http 200 (Status=PENDING)
  end

  %% =========================
  %% 2) EUDIW obtain Credential offer + metadata (OID4VCI)
  %% =========================
alt Obtain credential offer (cross device or same device flow)
  U->>W: Open EUDI mob app and scan QR code
  else
  U->>B: press deeplink button
  B->>W: invoke EUDI Wallet mob app
 end
  W->>I: credential offer request
  I->>W: credential offer

  W->>I: GET /.well-known/openid-credential-issuer
  I->>W: Credential Issuer Metadata

  W->>AS: GET /.well-known/oauth-authorization-server
  AS->>W: AS Metadata
  W->>U: Display mVRC credential offer and metadata (issuer business name, credential name, claim list, logotype, etc)
  U->>W: Accept credential offer

  %% =========================
  %% 3) Authorization (OpenID4VCI) for issuance
  %% =========================
    W->>W: Obtain WIA (client attestation JWT) from Wallet Provider Backend
    W->>W: Create fresh Client attestation JWt POP
    W->>AS: POST /par (client_id, scope, PKCE, client_attestation_jwt (wia) with fresh pop, etc )
    AS->>W: request_uri
  W->>W: Launch webview in app
  W->>AS: GET /authorize (request_uri, client_id)

  AS->>W: 302 redirect to redirect_uri?code=...&state=...
  W->>W: close webView
  W->>AS: POST /token (code, code_verifier, client_attestation_jwt (wia) with fresh pop )
  AS->>W: access_token (+ optional refresh_token)

  %% =========================
  %% 4) Issuance (credential request)
  %% =========================

  W->>I: POST /credential (Authorization: Bearer access_token, proof with key attestation (WUA)

  I->>I: Prepare, sign, encode mso_mdoc object (mVRC)
  I->>W: Credential response (mVRC as signed, encoded mso_mdoc object)

  W->>W: Store mVRC 

  W->>U: Show success screen in wallet
```

---

##### Extended flow (OpenID4VCI 1.0)

```mermaid
flowchart LR
  subgraph  WALLET[Wallet Provider]
  W[EUDI Wallet Instance]
  WPB[WUA status list]
  end
  subgraph ISSUER[mVRC Issuer]
    AS[Authorization Server OpenID4VCI]
    V[Verifier OpenID4VP]
    I[Issuer API OpenID4VCI]
  end
  subgraph PID[PID Provider]
    PIDSL[PID Status List]
  end
 subgraph TRUST[Trusted Lists Provider]
     TLP[PID Provider Trusted List]
     TLW[Wallet Provider Trusted List]
     TLRP[WRPAC Trusted List]
  end
  subgraph REGISTRY[National Vehicle Registry]
    R[mVRC data registry]
  end

  W -->|OpenID4VCI OAuth| AS
  W -->|OpenID4VP| V
  W -->|OpenID4VCI| I
  V -->|Get PID status list| PIDSL
  V -->|Get trusted list| TLP
  I -->|Get mVRC data| R
  I -->|Get trusted list| TLW
  W -->|Get trusted list| TLRP
  WPB ---|Get WUA status list| I
```

##### Sequence diagram

```mermaid
sequenceDiagram
  autonumber
  actor U as User
  participant W as EUDI Wallet instance
box [mVRC Issuer] 
  participant B as mVRC Issuer web app(frontend)
  participant I as mVRC Issuer - Issuer API (OpenID4VCI)
  participant AS as mVRC Issuer - Authorization Server (OpenID4VCI)
  participant V as mVRC Issuer - Verifier (OpenID4VP)
 end
  participant R as Vehicle Registry (optional)
  participant TL as Trusted Lists Provider (optional)
  participant PD as PID Provider (optional)
  participant WP as Wallet Provider (optional)

  %% =========================
  %% 1) Issuer UI prepares a Credential Offer (QR / deep link)
  %% =========================
  U->>B: Open issuer start page
  B->>I: POST /init (prepare credential offer parameters)
   I->>B: response with QR Code and credential offer
   B->>U: Display QR + deep link button (credential_offer_uri)
   B->>I: GET /status
   I-->>B: http 201 
  loop
  B->>I: GET /status poll request
  I->>B: http 200 (Status=PENDING)
  end

  %% =========================
  %% 2) EUDIW obtain Credential offer + metadata (OID4VCI)
  %% =========================
alt Obtain credential offer (cross device or same device flow)
  U->>W: Open EUDI mob app and scan QR code
  else
  U->>B: press deeplink button
  B->>W: invoke EUDI Wallet mob app
 end
  W->>I: credential offer request
  I->>W: credential offer

  W->>I: GET /.well-known/openid-credential-issuer
  I->>W: Credential Issuer Metadata

  opt Trust check (optional)
    W->>TL: WRPAC trusted List
    TL->>W: WRPAC trusted List
    W->>W: mVRC Issuer access certficate validation &cache Trusted list
  end

  W->>AS: GET /.well-known/oauth-authorization-server
  AS->>W: AS Metadata
  W->>U: Display mVRC credential offer and metadata (issuer business name, credential name, claim list, logotype, etc)
  U->>W: Accept credential offer
  %% =========================
  %% 3) Authorization (OpenID4VCI) for issuance
  %% =========================
    W->>W: Obtain WIA (client attestation JWT) from Wallet Provider Backend
    W->>W: Create fresh Client attestation JWt POP
    W->>AS: POST /par (client_id, scope, PKCE, client_attestation_jwt (wia) with fresh pop, etc )
    AS->>W: request_uri
  W->>W: Launch webView in app (Chrome Custom Tabs -AND, ASWebAuthenticationSession -iOS)
  W->>AS: GET /authorize (request_uri, client_id)

  opt OpenID4VP 
    AS->>V: Redirect authentication with OpenID4VP
    V->>V: Create authorization request
    V->>W: 302 redirect (deeplink to EUDI wallet)
    W->>V: JAR authorization request
    V->>W: OpenID4VP authorization request (with dcql query)
    W->>W: parse authorization request
    W->>U: display data sharing screen
    U->>W: Accept PID data scharing and PIN, biometrics authentication
    W->>W: Prepare and sign VP token
    W->>V: OpenID4VP response (VP token with PID presentation: mso_mdoc or SD-JWT VC)
    opt Verifier trust checks (optional)
      V->>TL: PID Provider trusted List
      TL->>V: PID Provider trusted List
      V->>V: PID seal x5c validation
     end
    opt PID status list check (optional)
      V->>PD: Get PID status list
      PD->>V: JWT/CWT with PID status list
      V->>V: PID idx validation
    end
    V->>W: response with redirect_uri
    W->>W: redirect to redirect_uri using webview
    V->>AS: VP verification result + subject reference
  end
  AS->>W: 302 redirect to redirect_uri?code=...&state=...
  W->>W: close webView
  W->>AS: POST /token (code, code_verifier, client_attestation_jwt (wia) with fresh pop )
  AS->>W: access_token (+ optional refresh_token)

  %% =========================
  %% 4) Issuance (credential request)
  %% =========================
  opt Nonce endpoint used (optional)
    W->>I: POST /nonce (request c_nonce)
    I->>W: c_nonce + c_nonce_expires_in
  end

  W->>I: POST /credential (Authorization: Bearer access_token, proof with key attestation (WUA)

  opt Issuer trust checks (optional)
    I->>TL: GET Wallet provider trusted List
    TL->>I: JWT/CWT with Wallet provider trusted List
    I->>I: WUA seal x5c validation
  end
   opt WUA status list check (optional)
      I->>WP: Get WUA status list
      WP->>I: JWT/CWT with WUA status list
      I->>I: WUA idx validation
    opt mVRC data retrieval (optional)
    I->>R: Query vehicle/owner data (using vehicle owner PID data)
    R->>I: mVRC data attributes
  end
opt mVRC status
  I->>I: add a new status index for mVRC instance being issued.
  end
  I->>I: Prepare, sign, encode mso_mdoc object (mVRC)
  I->>W: Credential response (mVRC as signed, encoded mso_mdoc object)
  end
 opt Issuer trust checks (optional)
    W->>W: mVRC seal x5c validation
  end

  W->>W: Store mVRC 

  opt Notification (optional)
    W->>I: POST /notification 
    I->>W: 204 OK
  end

  W->>U: Show success screen in wallet
```

---

##### Extended flow (OpenID4VCI 1.1 with iae)

```mermaid
flowchart LR
  subgraph  WALLET[Wallet Provider]
  W[EUDI Wallet Instance]
  WPB[WUA status list]
  end
  subgraph ISSUER[mVRC Issuer]
    AS[Authorization Server OpenID4VCI]
    I[Issuer API OpenID4VCI]
  end
  subgraph PID[PID Provider]
    PIDSL[PID Status List]
  end
 subgraph TRUST[Trusted Lists Provider]
     TLP[PID Provider Trusted List]
     TLW[Wallet Provider Trusted List]
     TLRP[WRPAC Trusted List]
  end
  subgraph REGISTRY[National Vehicle Registry]
    R[mVRC data registry]
  end

  W -->|OpenID4VCI OAuth| AS
  W -->|OpenID4VCI| I
  AS -->|Get PID status list| PIDSL
  AS -->|Get trusted list| TLP
  I -->|Get mVRC data| R
  I -->|Get trusted list| TLW
  W -->|Get trusted list| TLRP
  WPB ---|Get WUA status list| I
```

##### Sequence diagram
```mermaid
sequenceDiagram
  autonumber
  actor U as User
  participant W as EUDI Wallet instance
box [mVRC Issuer] 
  participant B as mVRC Issuer web app(frontend)
  participant I as mVRC Issuer - Issuer API (OpenID4VCI)
  participant AS as mVRC Issuer - Authorization Server (OpenID4VCI)
 end
  participant R as Vehicle Registry (optional)
  participant TL as Trusted Lists Provider (optional)
  participant PD as PID Provider (optional)
  participant WP as Wallet Provider (optional)

  %% =========================
  %% 1) Issuer UI prepares a Credential Offer (QR / deep link)
  %% =========================
  U->>B: Open issuer start page
  B->>I: POST /init (prepare credential offer parameters)
   I->>B: response with QR Code and credential offer
   B->>U: Display QR + deep link button (credential_offer_uri)
   B->>I: GET /status
   I-->>B: http 201 
  loop
  B->>I: GET /status poll request
  I->>B: http 200 (Status=PENDING)
  end

  %% =========================
  %% 2) EUDIW obtain Credential offer + metadata (OID4VCI)
  %% =========================
alt Obtain credential offer (cross device or same device flow)
  U->>W: Open EUDI mob app and scan QR code
  else
  U->>B: press deeplink button
  B->>W: invoke EUDI Wallet mob app
 end
  W->>I: credential offer request
  I->>W: credential offer

  W->>I: GET /.well-known/openid-credential-issuer
  I->>W: Credential Issuer Metadata

  opt Trust check (optional)
    W->>TL: WRPAC trusted List
    TL->>W: WRPAC trusted List
    W->>W: mVRC Issuer access certficate validation &cache Trusted list
  end

  W->>AS: GET /.well-known/oauth-authorization-server
  AS->>W: AS Metadata
  W->>U: Display mVRC credential offer and metadata (issuer business name, credential name, claim list, logotype, etc)
  U->>W: Accept credential offer
  %% =========================
  %% 3) Authorization and Authentication (OpenID4VCI) for issuance
  %% =========================
    W->>W: Obtain WIA (client attestation JWT) from Wallet Provider Backend
    W->>W: Create fresh Client attestation JWt POP
    W->>AS: POST /iae initial request (client_id, scope, PKCE, client_attestation_jwt (wia) with fresh pop, etc )
    AS->>W: openid4vp authorization request object (with dcql query)
    W->>W: parse authorization request
    W->>U: display data sharing screen
    U->>W: Accept PID data scharing and PIN, biometrics authentication
    W->>W: Prepare and sign VP token
    W->>AS: OpenID4VP response - follow up request (VP token with PID presentation: mso_mdoc or SD-JWT VC)
    opt Verifier trust checks (optional)
      AS->>TL: PID Provider trusted List
      TL->>AS: PID Provider trusted List
      AS->>AS: PID seal x5c validation
     end
    opt PID status list check (optional)
      AS->>PD: Get PID status list
      PD->>AS: JWT/CWT with PID status list
      AS->>AS: PID idx validation
     end
  AS->>W: respnse follow up request (code, status)
  W->>AS: POST /token (code, code_verifier, client_attestation_jwt (wia) with fresh pop )
  AS->>W: access_token (+ optional refresh_token)

  %% =========================
  %% 4) Issuance (credential request)
  %% =========================
  opt Nonce endpoint used (optional)
    W->>I: POST /nonce (request c_nonce)
    I->>W: c_nonce + c_nonce_expires_in
  end

  W->>I: POST /credential (Authorization: Bearer access_token, proof with key attestation (WUA)

  opt Issuer trust checks (optional)
    I->>TL: GET Wallet provider trusted List
    TL->>I: JWT/CWT with Wallet provider trusted List
    I->>I: WUA seal x5c validation
  end
   opt WUA status list check (optional)
      I->>WP: Get WUA status list
      WP->>I: JWT/CWT with WUA status list
      I->>I: WUA idx validation
    opt mVRC data retrieval (optional)
    I->>R: Query vehicle/owner data (using vehicle owner PID data)
    R->>I: mVRC data attributes
  end
opt mVRC status
  I->>I: add a new status index for mVRC instance being issued.
  end
  I->>I: Prepare, sign, encode mso_mdoc object (mVRC)
  I->>W: Credential response (mVRC as signed, encoded mso_mdoc object)
  end
 opt Issuer trust checks (optional)
    W->>W: mVRC seal x5c validation
  end

  W->>W: Store mVRC 

  opt Notification (optional)
    W->>I: POST /notification 
    I->>W: 204 OK
  end

  W->>U: Show success screen in wallet
```

### 8.2 Scenario 1B – mVRC remote data sharing

#### 8.2.1 Functional requirements

Scenario 1B is based on OpenID4VP 1.0, aligned with the High Assurance Interoperability Profile (HAIP) 1.0, and leverages standardised trust frameworks and credential formats to ensure interoperable and secure remote presentation of the mVRC data from the EUDI wallet to a verifier.

**EUDI Wallet Instance**

| Index | Requirement Title | Description | Priority | Acceptance Criteria |
|------:|-------------------|-------------|----------|---------------------|
| FR-W1B-01 | Support OpenID4VP | The wallet SHALL support the OpenID for Verifiable Presentations (OpenID4VP) 1.0 protocol for remote presentation of mVRC data. | High | The wallet can successfully complete an OpenID4VP flow with a compliant Verifier. |
| FR-W1B-02 | HAIP 1.0 Compliance | The wallet SHALL comply with the High Assurance Interoperability Profile (HAIP) 1.0 requirements applicable to presentation flows. | High | Presentation flows meet HAIP-defined security and assurance requirements. |
| FR-W1B-03 | Support mso_mdoc Format | The wallet SHALL support the mso_mdoc credential format for mVRC credentials, in accordance with ISO/IEC 18013-5 and applicable EUDI Wallet profiles. | High | The wallet can successfully receive, store, and present mVRC credentials in mso_mdoc format. |
| FR-W1B-04 | mVRC Data Model Compliance | The wallet SHALL support the standardized mVRC data model and structure as defined by ISO 7367 and the applicable mVRC rulebook. | High | The wallet correctly interprets and processes mVRC data elements according to the standardized model and structure. |
| FR-W1B-05 | User Consent | The wallet SHALL require explicit user consent before disclosing any mVRC data to a Verifier. | High | No mVRC data is shared without an explicit user-approval action. |
| FR-W1B-06 | Key Binding Support | The wallet SHALL support key binding mechanisms to ensure that presented mVRC data is cryptographically bound to the wallet instance. | High | Presentations include a valid proof of possession bound to a wallet-controlled key. |
| FR-W1B-07 | Cross-Device and Same-Device Flow | The wallet SHALL support cross-device flows using QR code scanning and same-device flows using deeplinks to initiate authorization requests. | High | Both QR-based and deeplink-based authorization requests can be successfully initiated. |
| FR-W1B-08 | Authorization Request Initialization | The wallet SHALL be able to initialize the OpenID4VP authorization request based on Verifier-provided parameters. | High | The wallet correctly processes and responds to an OpenID4VP authorization request. |
| FR-W1B-09 | Verifier Registration Certificate Handling | The wallet SHALL support processing and validation of Verifier registration certificates. | Medium | Registration certificates are successfully parsed and validated when present. |
| FR-W1B-10 | Verifier Trust Validation | The wallet SHALL verify the trust of the Verifier using registration and access certificates against trusted lists. | High | Presentations proceed only if the Verifier trust check succeeds. |
| FR-W1B-11 | DCQL Credential Sets Support | The wallet SHALL support DCQL credential sets as defined by the Verifier presentation request. | High | The wallet correctly resolves and processes DCQL credential sets. |
| FR-W1B-12 | DCQL Claim Sets Support | The wallet SHALL support DCQL claim sets to determine which claims are requested for presentation. | High | Requested claim sets are correctly interpreted and processed. |
| FR-W1B-13 | DCQL Value Constraints Support | The wallet SHALL support DCQL value constraints when selecting data for presentation. | Medium | Presented data complies with DCQL-defined value constraints. |
| FR-W1B-14 | Selective Disclosure | The wallet SHALL support selective disclosure mechanisms to share only the minimum required mVRC data. | High | Only user-approved and requested attributes are included in the presentation. |
| FR-W1B-15 | Data Sharing Preview | The wallet SHALL present the user with a clear preview of the data to be shared, including the Verifier identity and the purpose of data sharing. | High | The user can review requested data, Verifier name, and purpose before consent. |
| FR-W1B-16 | Optional Attribute Selection | The wallet SHALL allow the user to select or deselect optional mVRC attributes prior to presentation. | Medium | Optional attributes can be toggled on or off by the user. |
| FR-W1B-17 | VP Token Encryption | The wallet SHALL encrypt the verifiable presentation when using the `direct_post.jwt` response mode. | High | The VP token is transmitted in encrypted form to the Verifier. |
| FR-W1B-18 | Success Screen Presentation | The wallet SHALL display a success screen after a successful mVRC data presentation transaction. | Low | A clear success confirmation is shown to the user after completion. |
| FR-W1B-19 | Post-Presentation Redirect | The wallet SHALL support redirection after a successful mVRC data presentation, when requested by the Verifier. | Low | The wallet correctly performs a redirect following a successful transaction. |
| FR-W1B-20 | Verifier Metadata Resolution | The wallet SHALL resolve and process Verifier metadata as defined by OpenID4VP to determine supported formats, algorithms, and response modes. | High | The wallet successfully retrieves and applies Verifier metadata during the presentation flow. |
| FR-W1B-21 | Nonce Handling and Replay Protection | The wallet SHALL support nonce handling and include nonce values in verifiable presentations to prevent replay attacks. | High | Presentations include a valid nonce and are rejected if nonce validation fails. |
| FR-W1B-22 | Error Handling and User Feedback | The wallet SHALL handle protocol, trust, and validation errors and present a meaningful error state to the user. | Medium | Errors are correctly detected and a user-readable error message is displayed. |
| FR-W1B-23 | User-Initiated Cancellation | The wallet SHALL allow the user to cancel the presentation process at any time before mVRC data disclosure. | Medium | The user can abort the flow and no data is disclosed after cancellation. |
| FR-W1B-24 | Secure Presentation State Handling | The wallet SHALL securely maintain presentation state across redirects or application context switches during the presentation flow. | Medium | The presentation flow can be resumed or safely terminated without data leakage or corruption. |
| FR-W1B-25 | Support for DC API | The wallet MAY support remote presentation flows using a Digital Credentials API (DC API) supported by the user agent or platform. | Medium | If implemented, the wallet can be invoked through a DC API-compatible user agent or platform and can successfully complete a DC API-based presentation flow |
| FR-W1B-26 | DC API protocol | If the wallet supports DC API flows, it SHALL support the org-iso-mdoc presentation protocol value. The wallet MAY additionally support openid4vp-v1-unsigned, openid4vp-v1-signed | Medium | When DC API support is implemented, the wallet can successfully complete a DC API-based presentation flow using org-iso-mdoc. Additional OpenID4VP Annex A protocol values, if implemented, are processed correctly. |

**mVRC Verifier (service provider)**

| Index | Requirement Title | Description | Priority | Acceptance Criteria |
|------:|-------------------|-------------|----------|---------------------|
| FR-V1B-01 | Support OpenID4VP | The Verifier SHALL support the OpenID for Verifiable Presentations (OpenID4VP) 1.0 protocol to request and receive mVRC presentations. | High | The Verifier successfully completes an OpenID4VP flow with a compliant EUDI Wallet. |
| FR-V1B-02 | HAIP 1.0 Compliance | The Verifier SHALL comply with the High Assurance Interoperability Profile (HAIP) 1.0 requirements applicable to presentation flows. | High | Presentation requests and validation processes meet HAIP-defined assurance requirements. |
| FR-V1B-03 | Support mso_mdoc Format | The Verifier SHALL support verification of mVRC presentations using the mso_mdoc credential format, in accordance with ISO/IEC 18013-5 and applicable EUDI Wallet profiles. | High | The Verifier successfully validates mVRC presentations in mso_mdoc format. |
| FR-V1B-04 | mVRC Data Model Compliance | The Verifier SHALL validate presented mVRC data against the standardized mVRC data model and structure as defined by ISO 7367 and the applicable mVRC rulebook. | High | Presented mVRC data is correctly validated against the standardized data model and rejected if non-compliant. |
| FR-V1B-05 | Authorization Endpoint Exposure | The Verifier SHALL expose an Authorization Endpoint to initiate presentation requests in accordance with OpenID4VP. | High | Wallets can initiate presentation flows using the Verifier Authorization Endpoint. |
| FR-V1B-06 | Presentation Query | The Verifier SHALL define and communicate presentation requirements using standardized mechanisms (DCQL). | High | Wallets can correctly interpret requested credential and claim requirements. |
| FR-V1B-07 | DCQL Credential Sets Definition | The Verifier SHALL support DCQL credential sets to specify acceptable mVRC credentials. | Low | Wallets can resolve requested DCQL credential sets. |
| FR-V1B-08 | DCQL Claim Sets Definition | The Verifier SHALL support DCQL claim sets to specify required and optional mVRC claims. | Medium | Wallets can correctly identify required and optional claims. |
| FR-V1B-09 | DCQL Value Constraints | The Verifier SHALL support DCQL value constraints to restrict acceptable values of requested claims. | Medium | Presented mVRC data is validated against DCQL value constraints. |
| FR-V1B-10 | Nonce Generation | The Verifier SHALL generate and provide a nonce to bind the presentation to a specific transaction and prevent replay attacks. | High | Presentations without a valid nonce are rejected. |
| FR-V1B-11 | Direct Post Endpoint Support | The Verifier SHALL support receiving verifiable presentations using the `direct_post.jwt` response mode. | High | The Verifier successfully receives and processes VP tokens via direct_post.jwt mode. |
| FR-V1B-12 | VP Token Decryption | The Verifier SHALL support decryption of encrypted VP tokens when using `direct_post.jwt`. | High | Encrypted VP tokens are successfully decrypted and validated. |
| FR-V1B-13 | Key Binding Validation | The Verifier SHALL validate cryptographic proofs binding the presented mVRC data to the wallet-controlled key. | High | Presentations without valid key binding proofs are rejected. |
| FR-V1B-14 | Selective Disclosure Processing | The Verifier SHALL correctly process selectively disclosed mVRC data and validate it against the signed credential structure. | High | Selectively disclosed attributes are successfully verified. |
| FR-V1B-15 | User Redirect Handling | The Verifier SHALL support redirecting the user back to a web application or frontend after successful presentation. | High | The user is redirected after successful completion of the presentation flow. |
| FR-V1B-16 | Error Handling | The Verifier SHOULD handle protocol, validation, and trust errors and provide appropriate error responses. | Medium | Errors are returned using standardized error responses. |
| FR-V1B-17 | mVRC Seal Validation | The Verifier SHOULD validate the cryptographic seal applied to the mVRC credential against trusted lists to ensure that the credential was issued by a trusted mVRC Issuer. | Medium | The Verifier successfully validates the mVRC seal using trusted list information and rejects credentials with invalid or untrusted seals. |
| FR-V1B-18 | mVRC Status Verification | The Verifier SHOULD verify the current validity status of the mVRC credential using the applicable mVRC status list . | Medium | mVRC credentials with revoked or suspended status are correctly detected and rejected by the Verifier. |
| FR-V1B-19 | Success Screen Presentation | After successful verification of the mVRC presentation, the Verifier SHALL redirect the user and present a success screen displaying the mVRC data that was shared during the verification process. | High | The user is redirected to a success page and can view the mVRC data that was disclosed as part of the verification. |
| FR-V1B-20 | Business Process Continuation | After successful mVRC verification, the Verifier MAY allow the user to continue the intended business process, such as purchasing ferry tickets, buying an electronic toll vignette, or subscribing to a parking service. | Low | The user can proceed with the business process following successful verification. |
| FR-V1B-21 | Pre-Verification Business Flow | The Verifier MAY support initiating and maintaining the business process context prior to mVRC verification, ensuring a seamless transition into the verification flow. | Low | The business process context is preserved when transitioning from the service flow to the mVRC verification flow. |
| FR-V1B-22 | Support for DC API | The Verifier MAY support remote presentation flows using a Digital Credentials API (DC API) supported by the user agent or platform. | Medium | If implemented, the Verifier can successfully complete a DC API-based presentation flow through a DC API-compatible user agent or platform. |
| FR-V1B-23 | DC API protocol | If the Verifier supports DC API flows, it SHALL support the org-iso-mdoc presentation protocol value. The Verifier MAY additionally support openid4vp-v1-unsigned, openid4vp-v1-signed. | Medium | When DC API support is implemented, the Verifier can successfully initiate and process a DC API-based presentation flow using org-iso-mdoc. Additional OpenID4VP Annex A protocol values, if implemented, are processed correctly. |

---

#### 8.2.2 Protocol profile

**OpenID4VP**

Specification: OpenID for Verifiable Presentations 1.0  
Profile: High Assurance Interoperability Profile (HAIP) 1.0  

Key characteristics:
- Request/response based presentation flow using authoriszation requests;
- Support for response mode: direct_post.jwt;
- Credential format: mso_mdoc;
- Selective disclosure of requested attributes;
- Holder binding using proof-of-possession mechanisms;
- Optional use for identity verification (e.g. PID presentation);

Implementation characteristics:
- Supported request schemes: haip-vp, openid4vp, mdoc-openid4vp;
- Authoriszation requests are implemented using JSON Web Token (JAR) by reference;
- Response mode: direct_post.jwt;
- Credential format: mso_mdoc;
- Client identifier prefix type: x509_hash (as defined in HAIP 1.0);
- Use of nonce values to ensure replay protection;
- Support for credential status verification using status lists;

<br>

**Digital Credentials API (DC API) – optional**

Where supported, remote presentation may also be performed using a Digital Credentials API (DC API). The use of DC API is optional and depends onon the  platform support and implementation choices. OpenID4VP remains the primary and interoperable mechanism for remote presentations.

Key characteristics:
- Browser-/platform-mediated DC API request
- Integration with user agent or operating system for credential access
- Support for mdoc-based credential presentation
- Alternative interaction model to OpenID4VP flows

Implementation characteristics:
- Request transport: browser‑ or platform‑mediated DC API request
- Response mode: dc_api.jwt
- Credential format: mso_mdoc
- Supported protocol values: org-iso-mdoc (required), openid4vp-v1-unsigned and openid4vp-v1-signed (optional)

---

#### 8.2.3	Trust and security mechanisms

The scenario relies on a combination of cryptographic and trust mechanisms to ensure secure and reliable presentation and validation of mVRC data, including:

- Holder binding and proof-of-possession (PoP);
- Client authentication using Client Attestation JWT (where applicable);
- Wallet attestation mechanisms, including Wallet Instance Attestation (WIA);
- Use of nonce values to prevent replay attacks;
- Encryption of verifiable presentation tokens where required (e.g. direct_post.jwt);
- Validation of verifier trust using registration and access certificates;
- Validation of trust anchors using ETSI Trusted Lists (e.g. ETSI TS 119 612);
- Validation of credential integrity and authenticity (e.g. mVRC seal validation);
- Verification of the credential status using mVRC status lists;

---

#### 8.2.4	Endpoints

| Standard | Endpoint | Usage in Scenario | Reference |
|----------|----------|------------------|-----------|
| OpenID4VP 1.0 / JAR / HAIP 1.0 | Authorization Endpoint | Required | [OpenID4VP 1.0](https://openid.net/specs/openid-4-verifiable-presentations-1_0.html#section-5), [JAR RFC RFC 9101](https://www.rfc-editor.org/rfc/rfc9101.html#section-5.2) |
| OpenID4VP 1.0 | Direct POST JWT Endpoint | Required | [OpenID4VP 1.0](https://openid.net/specs/openid-4-verifiable-presentations-1_0.html#section-8.3.1) |
| Implementation-specific | Init Endpoint | Optional | N/A |
| Implementation-specific | Status Endpoint | Optional | N/A |

---

#### 8.2.5	Technical interaction flow – sequence diagrams

The following sequence diagrams illustrate the OpenID4VP-based remote presentation flow for scenario 1B and show the technical interaction between the EUDI wallet, the mVRC Verifier and supporting components.

##### Basic flow

```mermaid
flowchart LR
  subgraph WALLET[Wallet Provider]
    W[EUDI Wallet Instance]
  end

  subgraph VERIFIER[Service provider]
    V[mVRC Verifier]
  end

  W -->|OpenID4VP| V
```

##### Sequence diagram
```mermaid
sequenceDiagram
  autonumber
  actor U as User
  participant W as EUDI Wallet instance
  participant B as mVRC Verifier web app(frontend)
  participant V as mVRC Verifier - API (OpenID4VP)


  U->>B: Open Verifier start page
  B->>V: POST /start-session (prepare Auth request)
  V->>B: response with QR Code and deeplink with schema and request_uri
  B->>V: GET Poll verification status (until completed)(with mVRC Data)
  V-->>B: http 201 
  loop
  B->>V: GET /status poll request
  V->>B: http 200 (Status=PENDING)
  end
  B->>U: Display QR + deep link button (schema with JAR request_uri)

alt Obtain Auth request (cross device or same device flow)
  U->>W: Open EUDI mob app
  W->>B: scan QR code
  B->>W: scan QR code
  else
  U->>B: press deeplink button
  B->>W: invoke EUDI Wallet mob app
 end
  W->>V: JAR request
  V->>W: Authorization request with presentation query (DCQL)
  W->>W: parse and validate Authorization request
  W->>U: Display presentation query
  U->>W: Accept data sahring (user consent)
  W->>W: Prepare VP token(with encryption) and POST request
  W->>V: Send VP token in authorization response
  V->>V: Parse and validate VP token
  B->>V: GET /status poll request
  V->>B: http 200 (Status=OK polling ended) with mVRC presentation data
  V->>W: http 200 with redirect_uri
  W->>U: present success screen o mobile app
  U->>W: close success screen
alt (cross device or samedevice)
  W->>B: redirect do Verifier succes screen
  B->>U: present success screen with mVRC requested data
else
  W->>B: send request GET to redirect_uri
  W->>U: redirect and present Dashboard screen
  B->>U: present success screen with mVRC requested data
end
```

---

##### Extended flow
```mermaid
flowchart LR
  subgraph WALLET[Wallet Provider]
    W[EUDI Wallet Instance]
  end
  subgraph VERIFIER[Service provider]
    V[mVRC Verifier]
  end
  subgraph TRUST[Trust List Provider]
    TL[WRPAC Trusted list]
  end
  subgraph ISSUER[mVRC Issuer]
    I[mRVC status list]
  end
  W -->|OpenID4VP| V
  W -->|Get WRPAC trusted list| TL
  V -->|Get WRPAC trusted list| TL
  V -->|Get mVRC status list| I
```

##### Sequence diagram
```mermaid
sequenceDiagram
  autonumber
  actor U as User
  participant W as EUDI Wallet instance
  participant B as mVRC Verifier web app(frontend)
  participant V as mVRC Verifier
  participant I as mVRC Issuer (status list)
  participant TL as Trusted Lists Provider 


  U->>B: Open Verifier start page
  B->>V: POST /init (prepare Auth request)
  V->>B: response with QR Code and deeplink with schema and request_uri
  B->>V: GET Poll verification status (until completed)(with mVRC Data)
  V-->>B: http 201 
  loop
  B->>V: GET /status poll request
  V->>B: http 200 (Status=PENDING)
  end
  B->>U: Display QR + deep link button (schema with JAR request_uri)

alt Obtain Auth request (cross device or same device flow)
  U->>W: Open EUDI mob app
  W->>B: scan QR code
  B->>W: scan QR code
  else
  U->>B: press deeplink button
  B->>W: invoke EUDI Wallet mob app
 end
  W->>V: JAR request
  V->>W: Authorization request with presentation query (DCQL)
  W->>W: parse and validate Authorization request
   opt Trust check (optional)
    W->>TL: WRPAC trusted List
    TL->>W: WRPAC trusted List
    W->>W: mVRC Verifier access and registration certficate validation &cache Trusted list
  end
  W->>U: Display presentation query
  U->>W: Accept data sahring (user consent)
  W->>W: Prepare VP token(with encryption) and POST request
  W->>V: Send VP token in authorization response
  V->>V: Parse and validate VP token
opt Verifier trust checks (optional)
      V->>TL: WRPAC trusted List
      TL->>V: WRPAC trusted List
      V->>V: mVRC seal x5c validation
     end
    opt mVRC status list check (optional)
      V->>I: Get mVRC status list
      I->>V: JWT/CWT with mVRC status list
      V->>V: mVRC idx validation
    end
  B->>V: GET /status poll request
  V->>B: http 200 (Status=OK polling ended) with mVRC presentation data
  V->>W: http 200 with redirect_uri
  W->>U: present success screen o mobile app
  U->>W: close success screen
alt (cross device or samedevice)
  W->>B: redirect do Verifier succes screen
  B->>U: present success screen with mVRC requested data
else
  W->>B: send request GET to redirect_uri
  W->>U: redirect and present Dashboard screen
  B->>U: present success screen with mVRC requested data
end
```

### 8.3 Scenario 1C – mVRC proximity data sharing

#### 8.3.1	Functional requirements

Scenario 1C is based on proximity presentation mechanisms defined in ISO/IEC 18013‑5 and ISO/IEC TS 23220 standards and supports secure and interoperable in‑person presentation of mVRC data from the EUDI wallet to a proximity verifier/reader.

**EUDI Wallet Instance**

| Index | Requirement Title | Description | Priority | Acceptance Criteria |
|------:|-------------------|-------------|----------|---------------------|
| FR-W1C-01 | ISO 18013-5 Compliance| The wallet SHALL support proximity-based presentation of mVRC attestation in accordance with ISO/IEC 18013-5, using Bluetooth Low Energy (BLE) for device engagement and secure data transfer. | High | The wallet can successfully establish a proximity session with a compliant reader device over BLE, complete device engagement, and transmit requested mVRC data in compliance with ISO/IEC 18013-5. |
| FR-W1C-02 | BLE Peripheral Server Mode Support| The wallet SHALL support Bluetooth Low Energy (BLE) Peripheral Server Mode for proximity-based presentation of mVRC in accordance with ISO/IEC 18013-5. | High | The wallet can operate as a BLE peripheral, advertise availability, establish a secure session with a compliant reader acting as central, and successfully transmit requested mVRC data. |
| FR-W1C-03 | BLE Central Client Mode Support| The wallet MAY support Bluetooth Low Energy (BLE) Central Client Mode for proximity-based presentation of mVRC in accordance with ISO/IEC 18013-5. | Low | If implemented, the wallet can operate as a BLE central device, discover and connect to a compliant reader acting as peripheral, establish a secure session, and transmit requested mVRC data in compliance with ISO/IEC 18013-5. |
| FR-W1C-04 | BLE Transport with Optional L2CAP Support | The wallet MAY support Bluetooth Low Energy L2CAP Connection-Oriented Channels (CoC) as a transport mechanism for enhanced interoperability and performance.| Medium |  If L2CAP CoC is implemented, it functions correctly for proximity data exchange. |
| FR-W1C-05 | Session Encryption Enforcement | The wallet SHALL establish an encrypted session in accordance with ISO/IEC 18013-5 before transmitting any mVRC data. | High | No mVRC data is transmitted before a secure session is successfully established. |
| FR-W1C-06 | Support mso_mdoc Format | The wallet SHALL support the mso_mdoc credential format for mVRC, in accordance with ISO/IEC 18013-5 and applicable EUDI wallet profiles. | High | The wallet can successfully receive, store, and present mVRC in mso_mdoc format. |
| FR-W1C-07 | mVRC Data Model Compliance | The wallet SHALL support the standardized mVRC data model and structure as defined by ISO 7367 (mVRC) and the applicable mVRC rulebook. | High | The wallet correctly interprets and processes mVRC data elements according to the standardized model and structure. |
| FR-W1C-08 | User Consent | The wallet SHALL require explicit user consent before disclosing any mVRC data to a Verifier. | High | No mVRC data is shared without an explicit user-approval action. |
| FR-W1C-09 | Key Binding Support | The wallet SHALL support key binding mechanisms to ensure that presented mVRC data is cryptographically bound to the wallet instance. | High | Presentations include a valid proof of possession bound to a wallet-controlled key. |
| FR-W1C-10 | Verifier Registration Certificate Handling | The wallet SHALL support processing and validation of Verifier registration certificates. | Medium | Registration certificates are successfully parsed and validated when present. |
| FR-W1C-11 | Verifier Trust Validation | The wallet SHALL verify the trust of the verifier using registration and access certificates against trusted lists. | High | Presentations proceed only if the Verifier trust check succeeds. |
| FR-W1C-12 | Selective Disclosure | The wallet SHALL support selective disclosure mechanisms to share only the minimum required mVRC data. | High | Only user-approved and requested attributes are included in the presentation. |
| FR-W1C-13 | Data Sharing Preview | The wallet SHALL present the user with a clear preview of the data to be shared, including the verifier identity and the purpose of data sharing. | High | The user can review requested data, verifier name, and purpose before consent. |
| FR-W1C-14 | Optional Attribute Selection | The wallet SHALL allow the user to select or deselect optional mVRC attributes prior to presentation. | Medium | Optional attributes can be toggled on or off by the user. |
| FR-W1C-15 | Success Screen Presentation | The wallet SHALL display a success screen after a successful mVRC data presentation transaction. | High | A clear success confirmation is shown to the user after completion. |
| FR-W1C-16 | Error Handling and User Feedback | The wallet SHALL handle protocol, trust, and validation errors and present a meaningful error state to the user. | Medium | Errors are correctly detected and a user-readable error message is displayed. |
| FR-W1C-17 | User-Initiated Cancellation | The wallet SHALL allow the user to cancel the presentation process at any time before mVRC data disclosure. | Medium | The user can abort the flow and no data is disclosed after cancellation. |
| FR-W1C-18 | Device Engagement via QR and BLE | The wallet SHALL support ISO/IEC 18013-5 device engagement using QR Code initiation and Bluetooth Low Energy (BLE) transport. | High | The wallet can successfully initiate or respond to device engagement using a QR Code and establish a BLE proximity session with a compliant Reader. |
| FR-W1C-19 | Optional NFC Device Engagement Support | The wallet MAY support ISO/IEC 18013-5 device engagement using Near Field Communication (NFC) as an alternative proximity transport mechanism. | Low | If implemented, the wallet can successfully complete device engagement and data exchange over NFC in accordance with ISO/IEC 18013-5. |

**mVRC Proximity Reader**

| Index | Requirement Title | Description | Priority | Acceptance Criteria |
|------:|-------------------|-------------|----------|---------------------|
| FR-R1C-01 | ISO 18013-5 Compliance | The reader SHALL support ISO/IEC 18013-5 proximity sessions for requesting and validating mVRC attestation over Bluetooth Low Energy (BLE). | High | The reader can successfully establish a proximity session with a compliant wallet and complete device engagement in accordance with ISO/IEC 18013-5. |
| FR-R1C-02 | BLE Central Mode Support | The reader SHALL support Bluetooth Low Energy (BLE) Central mode when interacting with a wallet acting as Peripheral. | High | The reader can scan, discover, and connect to a compliant wallet advertising availability. |
| FR-R1C-03 | Optional BLE Peripheral Mode Support | The reader MAY support BLE Peripheral mode for interoperability scenarios. | Low | If implemented, the reader can accept connections from a compliant wallet acting as Central. |
| FR-R1C-04 | Session Encryption Enforcement | The reader SHALL establish and enforce an encrypted session in accordance with ISO/IEC 18013-5 before requesting or receiving any mVRC data. | High | No credential data is accepted before a secure session is successfully established. |
| FR-R1C-05 | mso_mdoc Format Support | The reader SHALL support parsing and validating mso_mdoc credentials in accordance with ISO/IEC 18013-5 and applicable EUDI Wallet profiles. | High | The reader successfully parses and processes received mVRC in mso_mdoc format. |
| FR-R1C-06 | Data Model Compliance | The reader SHALL interpret mVRC  data elements in accordance with ISO 7367 (mVRC) and applicable rulebooks. | High | Received attributes are correctly mapped and validated against standardized data models. |
| FR-R1C-07 | Device Authentication and Binding Validation | The reader SHALL verify device authentication (DeviceMAC) and holder binding for each received attestation. | High | The reader rejects presentations where device authentication or holder binding validation fails. |
| FR-R1C-08 | mVRC Seal Validation | The reader SHOULD validate the cryptographic seal applied to the mVRC credential against trusted lists to ensure that the credential was issued by a trusted mVRC issuer. | Medium | The reader successfully validates the mVRC seal using trusted list information and rejects credentials with invalid or untrusted seals. |
| FR-R1C-09 | mVRC Status Verification | The reader SHOULD verify the current validity status of the mVRC credential using the applicable mVRC status list (e.g. revocation or suspension status). | Medium | mVRC credentials with revoked or suspended status are correctly detected and rejected by the reader. |
| FR-R1C-10 | Reader Authentication | The reader SHALL support reader authentication mechanisms in accordance with ISO/IEC 18013-5 where applicable. | High | The reader presents valid reader authentication data and is successfully authenticated by the wallet when required. |
| FR-R1C-11 | Replay Protection Validation |The reader SHALL ensure protection against replay attacks by validating session freshness and verifying that each mVRC presentation is cryptographically bound to the active ISO/IEC 18013-5 session. | High | Presentations that are not cryptographically bound to the active session or that reuse prior session parameters are rejected.|
| FR-R1C-12 | Error Handling | The reader SHOULD detect protocol, validation, and trust errors and provide an appropriate system response. | Medium | Invalid or non-compliant presentations are rejected and logged. |
| FR-R1C-13 | Session Termination Handling | The reader SHALL properly terminate BLE sessions and securely dispose of session keys after completion. | Medium | Session keys are invalidated after session closure. |
| FR-R1C-14 | Optional L2CAP Support | The reader MAY support BLE L2CAP Connection-Oriented Channels (CoC) as a transport enhancement. | Medium | If implemented, L2CAP CoC sessions function correctly and interoperably. |
| FR-R1C-15 | Success Screen Presentation | After successful verification of the mVRC presentation, the reader SHALL  present a success screen displaying the mVRC data that was shared during the verification process. | High | A clear success confirmation is shown to the user after completion. |
| FR-R1C-16 | Device Engagement via QR and BLE | The reader SHALL support ISO/IEC 18013-5 device engagement using QR Code scanning and Bluetooth Low Energy (BLE) transport. | High | The reader can scan a QR Code, establish a BLE proximity session, and successfully complete device engagement with a compliant wallet. |
| FR-R1C-17 | Optional NFC Device Engagement Support | The reader MAY support ISO/IEC 18013-5 device engagement using Near Field Communication (NFC) as an alternative proximity transport mechanism. | Low | If implemented, the reader can successfully complete device engagement and receive credential data over NFC in accordance with ISO/IEC 18013-5. |
| FR-R1C-18 | Optional Attribute Request Definition | The reader MAY define the scope and mandatory or optional property of requested mVRC attributes within a proximity verification session. | Medium | If implemented, the reader can specify the scope of requested mVRC attributes or predefined mVRC and mDL data sets, including which attributes are mandatory and which are optional, and the wallet processes the request according to that query. |

---

#### 8.3.2	Protocol profile

**ISO/IEC 18013‑5 / Proximity mdoc (BLE)**

Specification: ISO/IEC 18013‑5 and ISO/IEC TS 23220  

Key characteristics:

- Device‑to‑device proximity interaction using Bluetooth Low Energy (BLE);
- Session establishment using device engagement (QR Code required, NFC optional);
- Use of ephemeral key pairs and session key derivation;
- Encrypted communication channel based on a shared session secret;
- Request/response model for data retrieval;
- Credential format: mso_mdoc;
- Selective disclosure of requested mVRC attributes;
- Holder binding ensured through cryptographic mechanisms;
- Device authentication based on ISO/IEC 18013‑5 mechanisms (DeviceMac);

Implementation characteristics:

- Session establishment using QR code or NFC engagement;
- Holder (EUDI wallet) mode:	Peripheral server (required), Client Central (optional);
- Supported BLE profile:	GATT (reqired), L2CAP (optional);
- Secure session establishment based on ephemeral key exchange (ECDH);
- Encrypted transport of DeviceRequest and DeviceResponse structures;
- Signed data payloads using MSO (Mobile Security Object);
- Support for credential status verification using status lists;
- Support for offline or semi‑offline interaction scenarios;

---

#### 8.3.3	Trust and security mechanisms

The scenario relies on a combination of cryptographic and trust mechanisms to ensure secure and reliable proximity presentation and validation of mVRC data, including:

- Holder binding and proof‑of‑possession (PoP);
- Use of ephemeral keys and session-based encryption to secure communication;
- Device authentication using ISO/IEC 18013‑5 mechanisms (e.g. DeviceSignature);
- Validation of credential integrity and authenticity (e.g. MSO signature validation);
- Certificate path validation of the mdoc document signer;
- Validation of trust anchors using ETSI Trusted Lists (e.g. ETSI TS 119 612);
- Verification of credential status using mVRC status lists;

---

#### 8.3.4 Endpoints

Proximity interactions do not rely on traditional network endpoints. Communication is performed directly between the EUDI wallet and the reader device using short range communication technologies.

Where applicable, backend services such as status list servers may be queried by the reader during validation.

---

#### 8.3.5	Technical interaction flow – sequence diagrams

The following sequence diagram illustrates the proximity presentation flow for the scenario 1C and shows the technical interaction between the user's EUDI wallet, the reader device and supporting components.

The diagram presents the main steps involved in the establishment of the session, secure data exchange and validation of mVRC data using ISO/IEC 18013 5 proximity mechanisms.

##### Flow

```mermaid

flowchart LR
  subgraph WALLET[Wallet provider]
    W[EUDI wallet instance]
  end

  subgraph VERIFIER[Service provider]
    V[mVRC proximity reader]
  end

  subgraph TRUST[Trust List Provider]
    TL[Trusted list service]
  end

  subgraph ISSUER[mVRC Issuer]
    I[mVRC status list]
  end

  W -->|ISO/IEC 18013-5 BLE| V
  W -->|Get trusted list| TL
  V -->|Get trusted list| TL
  V -->|Get mVRC status list| I
```

##### Sequence diagram

```mermaid
 sequenceDiagram
    autonumber

    participant ho as Owner (holder)
    participant re as Proximity reader
    participant sl as Status list<br/>server

    %% ===================== Engagement =====================
    re->>re: Generate sessionID
    Note left of re: sessionID is short lived.

    re->>re: Generate ephemeral key pair ReaderKey_pair
    re->>re: Create ReaderEngagement containing ReaderKey_pub

    alt QR Code Engagement (Static/Dynamic)
        re->>ho: Display QR Code
        ho->>ho: Scan QR Code
        ho->>ho: Extract Data
    else NFC Engagement
        ho->>re: Tap (NFC Proximity)
        re->>ho: Transfer Engagement Data via NFC
        ho->>ho: Extract Data
    end
    Note right of ho : Engagement data contains :<br/>• Reader Ephemeral PublicKey(ReaderKey_pub)<br/>• Supported retrieval methods

    ho->>ho: Generate ephemeral key pair DeviceKey_pair
    ho->>ho: Extract ReaderKey_pub
    ho->>ho: Derive session secret session_secret
    ho->>ho: Generate DeviceEngagement containing DeviceKey_pub
    ho-->>re: Send DeviceEngagement
    re->>re: Extract DeviceKey_pub
    re->>re: Derive session secret session_secret

    %% ===================== Data retrieval =====================
    re->>re: Create DeviceRequest containing requested data_req
    re->>re: Encrypt using session_secret
    re->>re: Create SessionData_req containing DeviceRequest_enc

    re-->>ho: Return SessionData_req as response
    ho->>ho: Extract DeviceRequest_enc and decrypt it
    ho->>ho: Extract data_req
    ho->>ho: Create data_res containing requested data
    ho->>ho: Create DeviceResponse containing data_res

    Note right of ho : Signs the requested mdoc data<br/>using the private key matching the MSO

    ho->>ho: Encrypt DeviceResponse using session_secret
    ho->>ho: Encode encrypted DeviceResponse into SessionData_res
    ho->>ho: Create SessionData_res containing DeviceResponse_enc
    ho-->>re: Send SessionData_res

    re->>re: Extract DeviceResponse_enc and decrypt it
    re->>re: Extract data_res
    re->>re: Verify provided data_res

    Note left of re : • Verifies hashes from MSO<br/>• Certificate path validation<br/>• Revocation of doc signer<br/>• Revocation of mDoc

    re->>re: Check validity of MSO
    re->>re: Calculate hash over all hashes
    re->>re: Check signature matches this hash
    re->>re: Check hashes of provided data
    re->>re: Check doc signer is not revoked

    Note left of re : Certificates which are trustworthy are<br/>provided using VICAL files (out of scope).
    
    alt check revocation if data included in mDoc
        re->>re: Extract status list URL and index
        re->>sl: Get status list
        sl-->>re: Return status list
        re->>re: Check bit at index-th position
    end

    %% ===================== Session termination =====================
    re-->>ho: Terminate Session
    ho->>ho: Delete ephemeral keys
    re->>re: Delete ephemeral keys
```

### 8.4 Scenario 2A – Delegated mVRC issuance (w2w)

#### 8.4.1	Functional requirements

Scenario 2A is based on a delegated mVRC issuance model, where a vehicle owner or holder authorises the issuance of a delegated mVRC credential to another user (consumer) using the EUDI wallets.

The scenario combines OpenID4VP 1.0, aligned with the HAIP 1.0, for verification of the vehicle owner, and OpenID4VCI 1.0 for issuance of the delegated mVRC to the consumer (delegated user) wallet.

The delegation flow requires presentation of the source mVRC and an identity credential (e.g. PID or mDL) by the vehicle owner, followed by the issuance of thea delegated mVRC credential containing the defined scope of vehicle privileges, consumer identity data, and validity period.

**Vehicle owner's EUDI Wallet Instance**

| Index | Requirement Title | Description | Priority | Acceptance Criteria |
|------:|-------------------|-------------|----------|---------------------|
| FR-WO2A-01 | Support OpenID4VP | The wallet SHALL support the OpenID for Verifiable Presentations (OpenID4VP) 1.0 protocol for remote presentation of credentials required in the delegation flow. | High | The wallet can successfully complete an OpenID4VP flow with a compliant Verifier. |
| FR-WO2A-02 | HAIP 1.0 Compliance | The wallet SHALL comply with the High Assurance Interoperability Profile (HAIP) 1.0 requirements applicable to presentation flows. | High | Presentation flows meet HAIP-defined security and assurance requirements. |
| FR-WO2A-03 | Support mso_mdoc Format for mVRC | The wallet SHALL support the `mso_mdoc` credential format for source mVRC credentials, in accordance with ISO/IEC 18013-5 and applicable EUDI Wallet profiles. | High | The wallet can successfully receive, store, and present source mVRC credentials in `mso_mdoc` format. |
| FR-WO2A-04 | mVRC Data Model Compliance | The wallet SHALL support the standardized mVRC data model and structure as defined by ISO 7367 and the applicable mVRC rulebook. | High | The wallet correctly interprets and processes mVRC data elements according to the standardized model and structure. |
| FR-WO2A-05 | Support Identity Credential in mso_mdoc Format | The wallet SHALL support presentation of the identity credential required for delegation initiation, such as PID or mDL, in `mso_mdoc` format where applicable. | High | The wallet can successfully present the required identity credential in the expected format when requested by the Verifier. |
| FR-WO2A-06 | Combined Presentation Support | The wallet SHALL support combined presentation of the source mVRC and the required identity credential within the same OpenID4VP transaction when requested by the Verifier. | High | The wallet can successfully complete a presentation flow in which both the source mVRC and the required identity credential are presented in the same transaction. |
| FR-WO2A-07 | User Consent | The wallet SHALL require explicit user consent before disclosing credential data to a Verifier. | High | No credential data is shared without an explicit user-approval action. |
| FR-WO2A-08 | Key Binding Support | The wallet SHALL support key binding mechanisms to ensure that presented credential data is cryptographically bound to the wallet instance. | High | Presentations include a valid proof of possession bound to a wallet-controlled key. |
| FR-WO2A-09 | Cross-Device and Same-Device Flow | The wallet SHALL support cross-device flows using QR code scanning and same-device flows using deeplinks to initiate authorization requests. | High | Both QR-based and deeplink-based authorization requests can be successfully initiated. |
| FR-WO2A-10 | Authorization Request Initialization | The wallet SHALL be able to initialize the OpenID4VP authorization request based on Verifier-provided parameters. | High | The wallet correctly processes and responds to an OpenID4VP authorization request. |
| FR-WO2A-11 | Verifier Registration Certificate Handling | The wallet SHALL support processing and validation of Verifier registration certificates. | Medium | Registration certificates are successfully parsed and validated when present. |
| FR-WO2A-12 | Verifier Trust Validation | The wallet SHALL verify the trust of the Verifier using registration and access certificates against trusted lists. | High | Presentations proceed only if the Verifier trust check succeeds. |
| FR-WO2A-13 | Selective Disclosure | The wallet SHALL support selective disclosure mechanisms to share only the minimum required credential data. | High | Only user-approved and requested attributes are included in the presentation. |
| FR-WO2A-14 | Data Sharing Preview | The wallet SHALL present the user with a clear preview of the data to be shared, including the Verifier identity and the purpose of data sharing. | High | The user can review requested data, Verifier name, and purpose before consent. |
| FR-WO2A-15 | Optional Attribute Selection | The wallet SHALL allow the user to select or deselect optional attributes prior to presentation. | Medium | Optional attributes can be toggled on or off by the user. |
| FR-WO2A-16 | VP Token Encryption | The wallet SHALL encrypt the verifiable presentation when using the `direct_post.jwt` response mode. | High | The VP token is transmitted in encrypted form to the Verifier. |
| FR-WO2A-17 | Success Screen Presentation | The wallet SHALL display a success screen after a successful credential presentation transaction. | Low | A clear success confirmation is shown to the user after completion. |
| FR-WO2A-18 | Post-Presentation Redirect | The wallet SHALL support redirection after a successful credential presentation, when requested by the Verifier. | Low | The wallet correctly performs a redirect following a successful transaction. |
| FR-WO2A-19 | Verifier Metadata Resolution | The wallet SHALL resolve and process Verifier metadata as defined by OpenID4VP to determine supported formats, algorithms, and response modes. | High | The wallet successfully retrieves and applies Verifier metadata during the presentation flow. |
| FR-WO2A-20 | Nonce Handling and Replay Protection | The wallet SHALL support nonce handling and include nonce values in verifiable presentations to prevent replay attacks. | High | Presentations include a valid nonce and are rejected if nonce validation fails. |
| FR-WO2A-21 | Error Handling and User Feedback | The wallet SHALL handle protocol, trust, and validation errors and present a meaningful error state to the user. | Medium | Errors are correctly detected and a user-readable error message is displayed. |
| FR-WO2A-22 | User-Initiated Cancellation | The wallet SHALL allow the user to cancel the presentation process at any time before credential data disclosure. | Medium | The user can abort the flow and no data is disclosed after cancellation. |

**Consumer's EUDI Wallet Instance**

| Index | Requirement Title | Description | Priority | Acceptance Criteria |
|------:|-------------------|-------------|----------|---------------------|
| FR-WD2A-01 | OpenID4VCI Issuance Support with HAIP 1.0 | The EUDI Wallet Instance SHALL support the OpenID4VCI issuance workflow in HAIP 1.0 to obtain delegated mVRC attestations, including credential offers, authorization, token handling, and credential requests. | High | The wallet successfully completes an OpenID4VCI issuance flow and receives a delegated mVRC attestation. |
| FR-WD2A-02 | Delegated mVRC Data Model and Structure Support | The EUDI Wallet Instance SHALL support processing, storage, and presentation of delegated mVRC credentials using a data model and structure compliant with ISO 7367, the applicable mVRC rulebook, and the delegated vehicle privileges model used in the scenario. | High | The wallet correctly processes and presents delegated mVRC credentials conforming to the expected data model and structure without data loss or misinterpretation. |
| FR-WD2A-03 | Delegated mVRC Credential Format Support | The EUDI Wallet Instance SHALL support receiving, processing, and storing delegated mVRC attestations encoded as `mso_mdoc`. | High | The wallet stores and later retrieves an issued delegated mVRC in `mso_mdoc` format. |
| FR-WD2A-04 | Credential Offer Initialization | The EUDI Wallet Instance SHALL support QR code-based initiation of the delegated mVRC issuance flow. | High | Issuance succeeds when the delegated user scans the QR code containing the credential offer or issuance initiation data. |
| FR-WD2A-05 | User Consent for Issuance | The EUDI Wallet Instance SHALL display information about the offered delegated mVRC and require explicit user consent before proceeding. | High | The user can approve or cancel issuance after reviewing credential information. |
| FR-WD2A-06 | PKCE Support | The wallet SHALL support PKCE for authorization code flows, including code verifier and challenge handling. | High | Token exchange succeeds only with a valid PKCE code verifier. |
| FR-WD2A-07 | Client Attestation JWT Support | The wallet SHALL support client authentication using Client Attestation JWT where required. | High | The Authorization Server accepts token requests authenticated with Client Attestation JWT. |
| FR-WD2A-08 | Consumer (Delegated User) Identity Verification Support | The wallet SHALL support the consumer's (delegated user's) identity verification where required prior to delegated mVRC issuance. | High | The wallet completes issuance when the consumer (delegated user) identity verification succeeds and fails when it is required but not completed. |
| FR-WD2A-09 | OpenID4VP Identity Verification via Interactive Authorization Endpoint | The EUDI Wallet Instance SHALL support processing an OpenID4VP presentation request provided in the `openid4vp_request` parameter of an Interactive Authorization Endpoint response in order to perform the consumer (delegated user) identity verification prior to delegated mVRC issuance. | High | The wallet successfully processes the `openid4vp_request`, completes the required presentation, and submits the resulting `openid4vp_response` to the Interactive Authorization Endpoint. |
| FR-WD2A-10 | Identity Credential Format Support | If applicable, the EUDI Wallet Instance SHALL support presentation of the consumer (delegated user) identity credentials encoded as `mso_mdoc`. | Medium | The wallet presents the required identity credential in the expected format when requested. |
| FR-WD2A-11 | User Consent for Verification | If applicable, the EUDI Wallet Instance SHALL display information about requested identity data prior to delegated mVRC issuance and require explicit user consent before proceeding. | Medium | The user can approve or cancel the verification process after reviewing the authorization request. |
| FR-WD2A-12 | Identity Assertion Exchange (IAE) Support | The EUDI Wallet Instance SHALL support Identity Assertion Exchange (IAE) where required by the Issuer during the delegated mVRC issuance flow. | High | The wallet successfully provides the required identity assertion during issuance when requested by the Issuer. |
| FR-WD2A-13 | Wallet Unit Attestation (WUA) in Proof | The wallet SHALL include a Wallet Unit Attestation (WUA), as defined in ARF TS 3, in the proof sent to the credential endpoint when required. | High | The Issuer validates WUA and issues the delegated mVRC only when WUA is present. |
| FR-WD2A-14 | Holder Binding and Proof-of-Possession | The EUDI Wallet Instance SHALL support holder binding and proof-of-possession mechanisms in line with HAIP requirements. | High | Issuance succeeds only when valid proof-of-possession is provided. |
| FR-WD2A-15 | Display of Delegated mVRC Credential Data | The EUDI Wallet Instance SHALL display the core data contained in a successfully issued delegated mVRC credential to the user after completion of the issuance process. | High | The wallet displays the delegated mVRC credential only after successful issuance and validation, with data accurately reflecting the credential payload. If issuance or validation fails, the delegated mVRC credential is not displayed to the consumer (delegated user). |
| FR-WD2A-16 | Secure Storage of Delegated mVRC | The EUDI Wallet Instance SHOULD securely store issued delegated mVRC attestations and associated metadata. | High | The issued delegated mVRC is securely stored and accessible only with user authorization. |
| FR-WD2A-17 | Protocol Error Handling | The EUDI Wallet Instance SHALL handle protocol, validation, and network errors gracefully and inform the consumer (delegated user). | Medium | The wallet displays meaningful error messages when issuance fails. |
| FR-WD2A-18 | Issuer Access Certificate Validation (ETSI TL) | The wallet SHOULD validate the Issuer’s access certificate using an ETSI Trusted List where applicable. | Medium | The wallet accepts issuers with trusted certificates and rejects invalid ones. |
| FR-WD2A-19 | Issuer Registration Certificate Validation (ETSI TL) | The wallet SHOULD validate the Issuer’s registration certificate using an ETSI Trusted List where required. | Medium | The wallet rejects issuance from issuers with invalid registration status. |
| FR-WD2A-20 | Issuer Seal Validation (ETSI TL) | The wallet SHOULD validate the cryptographic seal on the issued delegated mVRC using trusted list material. | Medium | The wallet stores only delegated mVRC attestations signed by trusted issuers. |
| FR-WD2A-21 | DPoP Support | The wallet SHALL support DPoP for token requests and related proof handling when required by the Authorization Server. | High | The wallet successfully completes token requests when DPoP is required. Requests with missing, invalid, or expired DPoP proof are rejected. |
| FR-WD2A-22 | ETSI Issuance Profile Support | The EUDI Wallet Instance SHALL support the applicable provisions of the ETSI issuance profile used in the scenario. | High | The wallet successfully completes issuance flows that apply the ETSI issuance profile requirements. Flows fail when required profile elements are missing or invalid. |
| FR-WD2A-23 | Interactive Authorization Endpoint Support | The EUDI Wallet Instance SHALL support the Interactive Authorization Endpoint as an alternative authorization interaction model for delegated mVRC issuance, where supported by the Issuer. | High | The wallet successfully completes issuance using the Interactive Authorization Endpoint when supported by the Issuer. |

**mVRC / Delegated mVRC Issuer**

| Index | Requirement Title | Description | Priority | Acceptance Criteria |
|------:|-------------------|-------------|----------|---------------------|
| FR-I2A-001 | Delegation Service Support | The Issuer SHALL provide a dedicated service enabling the vehicle owner or holder to initiate delegated mVRC issuance. | High | The vehicle owner or holder can access a service that starts the delegated mVRC issuance workflow. |
| FR-I2A-002 | Delegation Parameter Input | The Issuer SHALL allow the vehicle owner or holder to define the validity period and scope of delegated vehicle privileges. | High | The service accepts delegation scope and validity period input before issuance proceeds. |
| FR-I2A-003 | Support OpenID4VP for Vehicle Owner Verification | The Issuer SHALL support OpenID4VP 1.0 to request and validate presentation of the source mVRC and the required identity credential from the vehicle owner or holder prior to issuing the delegated mVRC. | High | The Issuer successfully completes an OpenID4VP flow in which the vehicle owner or holder presents the required credentials. |
| FR-I2A-004 | Combined Presentation Request Support | The Issuer SHALL support requesting combined presentation of the source mVRC and the required identity credential from the vehicle owner or holder within the same OpenID4VP transaction. | High | The Issuer successfully requests and validates both credentials in the same OpenID4VP transaction. |
| FR-I2A-005 | Vehicle Owner or Holder Identity Credential Support | The Issuer SHALL support requesting, processing, and validating the vehicle owner or holder identity credential, using PID or mDL, as part of delegation initiation. | High | Delegation initiation succeeds only when the required vehicle owner or holder identity credential is successfully validated. |
| FR-I2A-006 | Vehicle Owner or Holder Verification | The Issuer SHALL verify the identity of the vehicle owner or holder and the entitlement to initiate the delegation before the issuance process proceeds. | High | Delegated mVRC issuance proceeds only after successful verification of the vehicle owner or holder and delegation entitlement. |
| FR-I2A-007 | Support OpenID4VCI Issuance | The Issuer SHALL support OpenID4VCI issuance flows for issuance of delegated mVRC credentials to the delegated user wallet. | High | The Issuer successfully completes an OpenID4VCI issuance flow with a compliant delegated user wallet. |
| FR-I2A-008 | Authorization Code Flow Support | The Issuer SHALL support the authorization code flow for delegated mVRC issuance. | High | The Issuer successfully issues a delegated mVRC using the authorization code flow. |
| FR-I2A-009 | Credential Offer Support | The Issuer SHALL provide a credential offer for the delegated mVRC issuance flow and make it available for QR code-based initiation. | High | The delegated user wallet can obtain and process the credential offer and start issuance. |
| FR-I2A-010 | Interactive Authorization Endpoint Support | The Issuer SHALL support the Interactive Authorization Endpoint for delegated mVRC issuance where identity verification of the consumer (delegated user) is required during the authorization process. | High | The wallet of the consumer successfully completes issuance flows requiring one or more interactions through the Interactive Authorization Endpoint. |
| FR-I2A-011 | OpenID4VP Request via Interactive Authorization Endpoint | Where the consumer (delegated user) identity verification is required, the Issuer SHALL return an OpenID4VP authorization request in the `openid4vp_request` parameter of the Interactive Authorization Endpoint response. | High | The consumer (delegated user) wallet receives an Interactive Authorization Endpoint response containing a valid `openid4vp_request` and can continue the flow. |
| FR-I2A-012 | Consumer (Delegated User) Identity Credential Support | The Issuer SHALL support requesting, processing, and validating the consumer (delegated user) identity credential, using PID or mDL, prior to issuance of the delegated mVRC. | High | Delegated mVRC issuance succeeds only when the required consumer (delegated user) identity credential is successfully validated. |
| FR-I2A-013 | Consumer (Delegated User) Verification | The Issuer SHALL verify the identity of the consumer (delegated user) before issuing the delegated mVRC. | High | A delegated mVRC is issued only after successful consumer (delegated user) identity verification. |
| FR-I2A-014 | Support mso_mdoc Format for Delegated mVRC | The Issuer SHALL issue delegated mVRC credentials in `mso_mdoc` format. | High | The delegated mVRC is issued in `mso_mdoc` format and can be processed by a compliant wallet. |
| FR-I2A-015 | Delegated mVRC Data Model Compliance | The Issuer SHALL issue delegated mVRC credentials using a data model and structure compliant with ISO 7367, the applicable mVRC rulebook, and the delegated vehicle privileges model used in the scenario. | High | The issued delegated mVRC conforms to the expected data model and structure. |
| FR-I2A-016 | Delegated mVRC Generation | The Issuer SHALL generate the delegated mVRC containing the delegated privileges, consumer (delegated user) data, and the validity period defined during the delegation process. | High | The issued credential contains the expected delegation scope, consumer (delegated user) data, and validity period. |
| FR-I2A-017 | Credential Signing | The Issuer SHALL sign the delegated mVRC using its applicable signing certificate and trust chain. | High | The delegated mVRC is cryptographically signed and can be validated by relying parties. |
| FR-I2A-018 | Holder Binding Support | The Issuer SHALL issue the delegated mVRC bound to the consumer (delegated user) wallet in accordance with the applicable proof-of-possession and holder binding requirements. | High | The issued delegated mVRC is cryptographically bound to the consumer (delegated user) wallet. |
| FR-I2A-019 | PKCE Validation | The Issuer SHALL support and validate PKCE in authorization code issuance flows. | High | Token exchange succeeds only when a valid PKCE code verifier is presented. |
| FR-I2A-020 | Client Attestation JWT Support | The Issuer SHALL support Client Attestation JWT validation where wallet client authentication is required. | High | The Issuer accepts token requests authenticated with a valid Client Attestation JWT. |
| FR-I2A-021 | Wallet Proof Validation | The Issuer SHALL validate the wallet proof submitted at the credential endpoint, including proof-of-possession and Wallet Unit Attestation where required. | High | The credential is issued only when the submitted proof satisfies the applicable validation requirements. |
| FR-I2A-022 | DPoP Validation | The Issuer SHALL support and validate DPoP for token requests where required by the Authorization Server. | High | Token requests with missing, invalid, or expired DPoP proof are rejected. |
| FR-I2A-023 | Issuer Metadata Publication | The Issuer SHALL publish the metadata required for delegated mVRC issuance, including supported credential configurations, proof types, endpoints, and applicable authorization capabilities. | High | A compliant wallet can retrieve and use Issuer metadata to complete the issuance flow. |
| FR-I2A-024 | Trust Validation of Wallet and Presented Credentials | The Issuer SHOULD validate the trust status of wallets and presented credentials according to the applicable trust framework and trusted list material. | Medium | Untrusted wallets or credentials are detected and rejected according to the applicable trust model. |
| FR-I2A-025 | Registry Maintenance | The Issuer SHALL maintain a registry of issued delegated mVRC credentials. | Medium | Issued delegated mVRC credentials are recorded in the Issuer registry. |
| FR-I2A-026 | Error Handling | The Issuer SHOULD handle protocol, validation, and trust errors and return consistent error responses. | Medium | Errors are returned in a consistent form and logged for diagnostics. |
| FR-I2A-027 | Session Linking Between Owner or Holder and Consumer (Delegated User) | The Issuer SHALL maintain linkage between the verified vehicle owner or holder session and the consumer (delegated user) issuance session. | High | The delegated mVRC is issued only within the verified delegation transaction initiated by the vehicle owner or holder. |
| FR-I2A-028 | Redirect to Consumer (Delegated User) Issuance Step | After successful vehicle owner or holder verification, the Issuer SHALL enable continuation to the consumer (delegated user) issuance step by generating the issuance initiation data intended for scanning by the consumer's wallet. | High | After successful owner or holder verification, the Issuer generates issuance initiation data that can be used by the consumer (delegated user) wallet to start issuance. |

---

#### 8.4.2	Protocol profile

**OpenID4VP (owner verification)**

Specification: OpenID for Verifiable Presentations 1.0  
Profile: High Assurance Interoperability Profile (HAIP) 1.0  

Key characteristics:

- Request/response-based presentation flow using authorisation requests;
- Support for response mode: direct_post.jwt;
- Credential format: mso_mdoc;
- Selective disclosure of requested attributes;
- Holder binding using proof-of-possession mechanisms;
- Optional use for identity verification (e.g. PID presentation);

Implementation characteristics:

- Supported request schemes: haip-vp, openid4vp, mdoc-openid4vp;
- Authorisation requests are implemented using JSON Web Token (JAR) by reference;
- Response mode: direct_post.jwt;
- Credential format: mso_mdoc;
- Client identifier prefix type: x509_hash (as defined in HAIP 1.0);
- Use of nonce values to ensure replay protection;
- Support for credential status verification using status lists;

<br>

**OpenID4VCI (delegated issuance)**

Specification: OpenID for Verifiable Credential Issuance 1.1  
Profile: High Assurance Interoperability Profile (HAIP) 1.0  
Flow: Authorization Code Flow with Interactive Authorisation Endpoint (IAE)  

Key characteristics:

- Credential issuance initiated via credential offer (QR code);
- Supported credential offer schemes: haip-vci and openid-credential-offer;
- Credential format: mso_mdoc;
- Integration of identity verification within the issuance flow;
- Support for interactive authorisation flows using the Interactive Authorisation Endpoint (IAE);
- Holder binding using proof-of-possession mechanisms;

Implementation characteristics:

- Authorisation flow using Authorisation Code Flow with PKCE;
- Support for Interactive Authorisation Endpoint (IAE) and iae_post.jwt response mode;
- Issuance mode: immediate issuance;
- Request URI methods: GET and POST;
- Key binding and proof mechanisms including PoP and wallet attestation;

---

#### 8.4.3	Trust and security mechanisms

The scenario relies on a combination of cryptographic and trust mechanisms to ensure secure delegation, verification and issuance of mVRC data, including:

- Holder binding and proof-of-possession (PoP);
- Wallet attestation mechanisms, including Wallet Unit Attestation (WUA) and Wallet Instance Attestation (WIA), as defined in ARF TS 3;
- Client authentication using Client Attestation JWT;
- Use of nonce values to prevent replay attacks;
- Validation of trust anchors using ETSI Trusted Lists (e.g. ETSI TS 119 612);
- Validation of issuer and wallet certificates (registration and access certificates);
- Validation of credential integrity and authenticity (mVRC seal validation);
- Verification of credential status using mVRC status lists;
- Alignment with ETSI TS 119 472 issuance profiles;
- Secure linkage between vehicle owner verification and consumer's issuance session;

---

#### 8.4.4 Endpoints

| Standard | Endpoint | Usage in Scenario | Reference |
|----------|----------|------------------|-----------|
| OpenID4VCI 1.0 / HAIP 1.0 / ETSI TS 119 472-3 | Credential Offer Endpoint | Required | [OpenID4VCI 1.0](https://openid.net/specs/openid-4-verifiable-credential-issuance-1_0.html#section-4), [HAIP 1.0](https://openid.net/specs/openid4vc-high-assurance-interoperability-profile-1_0.html#section-4.2), [ETSI TS 119 472-3](https://www.etsi.org/deliver/etsi_ts/119400_119499/11947203/01.01.01_60/ts_11947203v010101p.pdf)  |
| OpenID4VCI 1.0 / HAIP 1.0 / ETSI TS 119 472-3 | Authorization Endpoint | Required | [OpenID4VCI 1.0](https://openid.net/specs/openid-4-verifiable-credential-issuance-1_0.html#name-authorization-endpoint), [HAIP 1.0](https://openid.net/specs/openid4vc-high-assurance-interoperability-profile-1_0.html#section-4.3), [ETSI TS 119 472-3](https://www.etsi.org/deliver/etsi_ts/119400_119499/11947203/01.01.01_60/ts_11947203v010101p.pdf) |
| RFC 9126 / OpenID4VCI 1.0 / HAIP 1.0 / ETSI TS 119 472-3 | Pushed Authorization Request (PAR) | Required | [RFC 9126](https://www.rfc-editor.org/rfc/rfc9126.html), [OpenID4VCI 1.0](https://openid.net/specs/openid-4-verifiable-credential-issuance-1_0.html#section-5.1.4), [ETSI TS 119 472-3](https://www.etsi.org/deliver/etsi_ts/119400_119499/11947203/01.01.01_60/ts_11947203v010101p.pdf) |
| OpenID4VCI 1.0 / HAIP 1.0 / ETSI TS 119 472-3 | Token Endpoint | Required | [OpenID4VCI 1.0](https://openid.net/specs/openid-4-verifiable-credential-issuance-1_0.html#section-6), [HAIP 1.0](https://openid.net/specs/openid4vc-high-assurance-interoperability-profile-1_0.html#section-4.4), [ETSI TS 119 472-3](https://www.etsi.org/deliver/etsi_ts/119400_119499/11947203/01.01.01_60/ts_11947203v010101p.pdf)  |
| OpenID4VCI 1.0 / HAIP 1.0 | Nonce Endpoint | Required | [OpenID4VCI 1.0](https://openid.net/specs/openid-4-verifiable-credential-issuance-1_0.html#section-7) |
| OpenID4VCI 1.0 / HAIP 1.0 / ETSI TS 119 472-3 | Credential Endpoint | Required | [OpenID4VCI 1.0](https://openid.net/specs/openid-4-verifiable-credential-issuance-1_0.html#section-8), [HAIP 1.0](https://openid.net/specs/openid4vc-high-assurance-interoperability-profile-1_0.html#section-4.5), [ETSI TS 119 472-3](https://www.etsi.org/deliver/etsi_ts/119400_119499/11947203/01.01.01_60/ts_11947203v010101p.pdf) |
| OpenID4VCI 1.0 / ETSI TS 119 472-3 | Notification Endpoint | Optional | [OpenID4VCI 1.0](https://openid.net/specs/openid-4-verifiable-credential-issuance-1_0.html#section-11), [ETSI TS 119 472-3](https://www.etsi.org/deliver/etsi_ts/119400_119499/11947203/01.01.01_60/ts_11947203v010101p.pdf) |
| OpenID4VCI 1.0 / HAIP 1.0 / ETSI TS 119 472-3 | Credential Issuer Metadata Endpoint | Required | [OpenID4VCI 1.0](https://openid.net/specs/openid-4-verifiable-credential-issuance-1_0.html#section-12.2), [HAIP 1.0](https://openid.net/specs/openid4vc-high-assurance-interoperability-profile-1_0.html#section-4.1), [ETSI TS 119 472-3](https://www.etsi.org/deliver/etsi_ts/119400_119499/11947203/01.01.01_60/ts_11947203v010101p.pdf) |
| RFC 8414 / OpenID4VCI 1.0 | Authorization Server Metadata Endpoint | Required | [RFC 8414](https://datatracker.ietf.org/doc/html/rfc8414), [Attestation-Based Client Authentication](https://www.ietf.org/archive/id/draft-ietf-oauth-attestation-based-client-auth-08.html#name-authorization-server-metada), [DPOP](https://www.rfc-editor.org/rfc/rfc9449.html#section-5.1), [OpenID4VCI 1.1 draft](https://openid.github.io/OpenID4VCI/openid-4-verifiable-credential-issuance-1_1-wg-draft.html#name-interactive-authorization-e)  |
| Token Status List | Status List Endpoint | Optional | [Token Status List](https://datatracker.ietf.org/doc/draft-ietf-oauth-status-list/) |
| OpenID4VCI 1.1 draft | Interactive Authorization Endpoint (`/iae`) | Optional | [OpenID4VCI 1.1 draft](https://openid.github.io/OpenID4VCI/openid-4-verifiable-credential-issuance-1_1-wg-draft.html#name-interactive-authorization-e) |
| OpenID4VP 1.0 / HAIP 1.0 | Authorization Endpoint | Required | [OpenID4VP 1.0](https://openid.net/specs/openid-4-verifiable-presentations-1_0.html#section-5), [HAIP 1.0](https://openid.net/specs/openid4vc-high-assurance-interoperability-profile-1_0.html#section-5) |
| OpenID4VP 1.0 | Direct POST JWT | Required | [OpenID4VP 1.0](https://openid.net/specs/openid-4-verifiable-presentations-1_0.html#section-8.3.1) |
| Implementation-specific | Init Endpoint | Optional | N/A |
| Implementation-specific | Status Endpoint | Optional | N/A |

---

#### 8.4.5	Technical interaction flow – sequence diagrams

The following diagrams illustrate the delegated mVRC issuance flow for the scenario 2A and show the technical interaction between the EUDI wallet of the vehicle owner, the consumer's EUDI wallet, the mVRC issuer and supporting components.

##### Basic flow

```mermaid
flowchart LR
  subgraph WALLET1[Wallet provider_I]
    WO[User EUDI Wallet Instance]
  end

  subgraph ISSUER[mVRC Issuer]
    V[mVRC PID/mDL Verifier OpenID4VP]
    AS[Authorization Server\ OpenID4VCI]
    I[mVRC / Delegated mVRC Issuer\ OpenID4VCI]
  end

  subgraph WALLET2[Wallet provider_II]
    WD[Delegated User EUDI Wallet Instance]
  end
  WO -->|OpenID4VP| V
  WO -->|QR Code scan| WD
  WD -->|OpenID4VCI| I
  WD -->|OpenID4VCI IAE| AS
```

##### Sequence diagram

```mermaid
sequenceDiagram
  autonumber
  actor U as User (Vehicle Owner)
  participant WO as User EUDI Wallet instance
  box mVRC Issuer 
  participant B as mVRC Issuer web app(frontend)
  participant V as mVRC PID/mDL Verifier (OpenID4VP)
  participant I as mVRC Issuer - Issuer API (OpenID4VCI)
  participant AS as mVRC Issuer - Authorization Server (OpenID4VCI)
 end
  participant WD as Delegated User EUDI Wallet instance
  actor UD as Delegated User

rect rgba(100, 170, 120, 0.18)
      Note left of UD: User (Vehicle Owner) Delegation proces (OpenID4VP)
  U->>B: Open issuer start page
  B->>V: POST /start-session (prepare Auth request)
  V->>B: response with QR Code and deeplink with schema and request_uri
  B->>V: GET Poll verification status (until completed)(with mVRC Data)
  V-->>B: http 201 
  loop
  B->>V: GET /status poll request
  V->>B: http 200 (Status=PENDING)
  end
  B->>U: Display QR + deep link button (schema with JAR request_uri)
  U->>B: press deeplink button
  B->>WO: invoke EUDI Wallet mob app
  WO->>V: JAR request
  V->>WO: Authorization request with presentation query (DCQL)
  WO->>WO: parse and validate Authorization request
  WO->>U: Display presentation query
  U->>WO: Accept data sahring (user consent)
  WO->>WO: Prepare VP token(with encryption) and POST request
  WO->>V: Send VP token in authorization response
  V->>V: Parse and validate VP token
  B->>V: GET /status poll request
  V->>B: http 200 (Status=OK polling ended) with mVRC and PID or mDL presentation data
  V->>WO: http 200 with redirect_uri (initialization screen for OpenID4VCI with credential_offer)
  WO->>U: present success screen o mobile app
  U->>WO: close success screen
  WO->>B: redirect to Verifier initialization screen for OpenID4VCI with credential_offer
  B->>I: POST /init (prepare credential offer parameters)
  I->>B: response with QR Code and credential offer
  B->>B: render Qr Code
  B->>U: display QR Code with credential_offer_uri
   B->>I: GET /status
   I-->>B: http 201 
  loop
  B->>I: GET /status poll request
  I->>B: http 200 (Status=PENDING)
  end
  end

rect rgba(200, 140, 90, 0.18)
      Note left of UD: Delegated User Delegation proces (OpenID4VCI)
  UD->>WD: Open and log in and launch QR code scanner
  WD->>B: scan QR code
  WD->>I: credential offer request
  I->>WD: credential offer
  WD->>I: GET /.well-known/openid-credential-issuer
  I->>WD: Credential Issuer Metadata
  WD->>AS: GET /.well-known/oauth-authorization-server
  AS->>WD: AS Metadata
  WD->>UD: Display mVRC credential offer and metadata<br/> (issuer business name, credential name, claim list, logotype, etc)
  UD->>WD: Accept credential offer

    WD->>WD: Obtain WIA (client attestation JWT) from Wallet Provider Backend
    WD->>WD: Create fresh Client attestation JWt POP
    WD->>AS: POST /iae initial request (client_id, scope, PKCE, client_attestation_jwt (wia) with fresh pop, etc )
    AS->>WD: openid4vp authorization request object (with dcql query)
    WD->>WD: parse authorization request
    WD->>UD: display data sharing screen
    UD->>WD: Accept PID data scharing and PIN, biometrics authentication
    WD->>WD: Prepare and sign VP token
    WD->>AS: OpenID4VP response - follow up request (VP token with PID presentation: mso_mdoc or SD-JWT VC)
  AS->>WD: respnse follow up request (code, status)
  WD->>AS: POST /token (code, code_verifier, client_attestation_jwt (wia) with fresh pop )
  AS->>WD: access_token (+ optional refresh_token)

    WD->>I: POST /nonce (request c_nonce)
    I->>WD: c_nonce + c_nonce_expires_in
  WD->>I: POST /credential (Authorization: Bearer access_token, proof with key attestation (WUA)
  I->>I: Prepare, sign, encode mso_mdoc object (delegated mVRC)
  I->>WD: Credential response (mVRC as signed, encoded mso_mdoc object)
  WD->>WD: Store mVRC 
  opt Notification (optional)
    WD->>I: POST /notification 
    I->>WD: 204 OK
  end
  WD->>UD: Show success screen in wallet
  B->>I: GET /status poll request
  I->>B: http 200 (Status=OK polling ended)
  B->>U: present success screen
end
```

---

##### Extended flow

```mermaid
flowchart LR
  subgraph WALLET1[Wallet provider_I]
    WO[User EUDI Wallet Instance]
  end

  subgraph ISSUER[mVRC Issuer]
    V[mVRC PID/mDL Verifier OpenID4VP]
    AS[Authorization Server\ OpenID4VCI]
    I[mVRC / Delegated mVRC Issuer\ OpenID4VCI]
  end

  subgraph WALLET2[Wallet provider_II]
    WD[Delegated User EUDI Wallet Instance]
    WPB[WUA status list]
  end
 subgraph PID[PID Provider/ mDL Provider]
    PIDSL[PID/mDL Status List]
  end
 subgraph TRUST[Trusted Lists Provider]
     TLP[PID Provider/ mDL Provider Trusted List]
     TLW[Wallet Provider Trusted List]
     TLRP[WRPAC Trusted List]
  end
  subgraph REGISTRY[National Vehicle Registry]
    R[mVRC data registry]
  end
  WO -->|OpenID4VP| V
  WO -->|QR Code scan| WD
  WD -->|OpenID4VCI| I
  WD -->|OpenID4VCI IAE| AS
  V -->|Get PID status list| PIDSL
  V -->|Get trusted list| TLP
  I -->|Get mVRC data| R
  I -->|Get trusted list| TLW
  AS -->|Get trusted list| TLW
  WO -->|Get trusted list| TLRP
  WD ---|Get trusted list| TLRP
  WPB ---|Get WUA status list| I
```

##### Sequence diagram

```mermaid
sequenceDiagram
  autonumber
  actor U as User (Vehicle Owner)
  participant WO as User EUDI Wallet instance
  box mVRC Issuer 
  participant B as mVRC Issuer web app(frontend)
  participant V as mVRC PID/mDL Verifier (OpenID4VP)
  participant I as mVRC Issuer - Issuer API (OpenID4VCI)
  participant AS as mVRC Issuer - Authorization Server (OpenID4VCI)
 end
  participant R as Vehicle Registry (optional)
  participant TL as Trusted Lists Provider (optional)
  participant PD as PID Provider/mDL Provider (optional)
  participant WP as Wallet Provider (optional)
  participant WD as Delegated User EUDI Wallet instance
  actor UD as Delegated User

rect rgba(100, 170, 120, 0.18)
      Note left of UD: User (Vehicle Owner) Delegation proces (OpenID4VP)
  U->>B: Open issuer start page
  B->>V: POST /start-session (prepare Auth request)
  V->>B: response with QR Code and deeplink with schema and request_uri
  B->>V: GET Poll verification status (until completed)(with mVRC Data)
  V-->>B: http 201 
  loop
  B->>V: GET /status poll request
  V->>B: http 200 (Status=PENDING)
  end
  B->>U: Display QR + deep link button (schema with JAR request_uri)
  U->>B: press deeplink button
  B->>WO: invoke EUDI Wallet mob app
  WO->>V: JAR request
  V->>WO: Authorization request with presentation query (DCQL)
  WO->>WO: parse and validate Authorization request
     opt Trust check (optional)
    WO->>TL: WRPAC trusted List
    TL->>WO: WRPAC trusted List
    WO->>WO: mVRC Verifier access and registration certficate validation &cache Trusted list
  end
  WO->>U: Display presentation query
  U->>WO: Accept data sahring (user consent)
  WO->>WO: Prepare VP token(with encryption) and POST request
  WO->>V: Send VP token in authorization response
  V->>V: Parse and validate VP token
  opt Verifier trust checks (optional)
      V->>TL: PID Provider/mDL Provider trusted List
      TL->>V: PID Provider/mDL Provider trusted List
      V->>V: PID/mDL seal x5c validation
     end
    opt PID/mDL status list check (optional)
      V->>PD: Get PID/mDL status list
      PD->>V: JWT/CWT with mVRC status list
      V->>V: mVRC idx validation
    end
  B->>V: GET /status poll request
  V->>B: http 200 (Status=OK polling ended) with mVRC and PID or mDL presentation data
  V->>WO: http 200 with redirect_uri (initialization screen for OpenID4VCI with credential_offer)
  WO->>U: present success screen o mobile app
  U->>WO: close success screen
  WO->>B: redirect to Verifier initialization screen for OpenID4VCI with credential_offer
  B->>I: POST /init (prepare credential offer parameters)
  I->>B: response with QR Code and credential offer
  B->>B: render Qr Code
  B->>U: display QR Code with credential_offer_uri
   B->>I: GET /status
   I-->>B: http 201 
  loop
  B->>I: GET /status poll request
  I->>B: http 200 (Status=PENDING)
  end
  end

rect rgba(200, 140, 90, 0.18)
      Note left of UD: Delegated User Delegation proces (OpenID4VCI)
  UD->>WD: Open and log in and launch QR code scanner
  WD->>B: scan QR code
  WD->>I: credential offer request
  I->>WD: credential offer
  WD->>I: GET /.well-known/openid-credential-issuer
  I->>WD: Credential Issuer Metadata
    opt Trust check (optional)
    WD->>TL: WRPAC trusted List
    TL->>WD: WRPAC trusted List
    WD->>WD: mVRC Issuer access certficate validation &cache Trusted list
  end
  WD->>AS: GET /.well-known/oauth-authorization-server
  AS->>WD: AS Metadata
  WD->>UD: Display mVRC credential offer and metadata<br/> (issuer business name, credential name, claim list, logotype, etc)
  UD->>WD: Accept credential offer

    WD->>WD: Obtain WIA (client attestation JWT) from Wallet Provider Backend
    WD->>WD: Create fresh Client attestation JWT POP
    WD->>AS: POST /iae initial request (client_id, scope, PKCE, client_attestation_jwt (wia) with fresh pop, etc )
    AS->>AS: Parse and validate PAR Request
  opt Authorization Server trust checks (optional)
    AS->>TL: GET Wallet provider trusted List
    TL->>AS: JWT/CWT with Wallet provider trusted List
    AS->>AS: WIA seal x5c validation
  end
    AS->>WD: openid4vp authorization request object (with dcql query)
    WD->>WD: parse authorization request
    WD->>UD: display data sharing screen
    UD->>WD: Accept PID data scharing and PIN, biometrics authentication
    WD->>WD: Prepare and sign VP token
    WD->>AS: OpenID4VP response - follow up request (VP token with PID presentation: mso_mdoc or SD-JWT VC)
    AS->>AS: Parse and validate VP token
      opt Verifier trust checks (optional)
      AS->>TL: PID Provider/mDL Provider trusted List
      TL->>AS: PID Provider/mDL Provider trusted List
      AS->>AS: PID seal x5c validation
     end
    opt PID status list check (optional)
      AS->>PD: Get PID/mDL status list
      PD->>AS: JWT/CWT with PID/mDL status list
      AS->>AS: PID/mDL idx validation
    end
  AS->>WD: respnse follow up request (code, status)
  WD->>AS: POST /token (code, code_verifier, client_attestation_jwt (wia) with fresh pop )
  AS->>AS: Parse and validate token request
  AS->>WD: access_token (+ optional refresh_token)

    WD->>I: POST /nonce (request c_nonce)
    I->>WD: c_nonce + c_nonce_expires_in
  WD->>I: POST /credential (Authorization: Bearer access_token, proof with key attestation (WUA)
   opt Issuer trust checks (optional)
    I->>TL: GET Wallet provider trusted List
    TL->>I: JWT/CWT with Wallet provider trusted List
    I->>I: WUA seal x5c validation
  end
   opt WUA status list check (optional)
      I->>WP: Get WUA status list
      WP->>I: JWT/CWT with WUA status list
      I->>I: WUA idx validation
   end
    opt mVRC data retrieval (optional)
    I->>R: Query vehicle/owner data (using vehicle owner PID data)
    R->>I: mVRC data attributes
  end
opt delegated mVRC status
  I->>I: add a new status index for mVRC instance being issued.
  end
  I->>I: Prepare, sign, encode mso_mdoc object (mVRC)
  I->>WD: Credential response (mVRC as signed, encoded mso_mdoc object)
 opt Issuer trust checks (optional)
    WD->>WD: delegated mVRC seal x5c validation
  end
  WD->>WD: Store delegated mVRC 
  opt Notification (optional)
    WD->>I: POST /notification 
    I->>WD: 204 OK
  end
  WD->>UD: Show success screen in wallet
  B->>I: GET /status poll request
  I->>B: http 200 (Status=OK polling ended)
  B->>U: present success screen
end
```

### 8.5 Scenario 2B – Delegated mVRC issuance (o2w)

#### 8.5.1 Functional requirements

Scenario 2B is based on a delegated mVRC issuance model in which an organisation (e.g. a rental or leasing company) authorises a consumer (delegated user) to obtain a delegated mVRC credential. The scenario combines OpenID4VP for identity verification and authorisation validation, and OpenID4VCI for issuance of both the mVRC delegation permission and the delegated mVRC. The mVRC delegation permission is defined in a dedicated rulebook and is used as a short-lived authorisation credential within the issuance flow.

**Consumer (Delegated User) EUDI Wallet Instance**

| Index | Requirement Title | Description | Priority | Acceptance Criteria |
|------:|-------------------|-------------|----------|---------------------|
| FR-WD2B-001 | OpenID4VCI Issuance Support with HAIP 1.0 | The EUDI Wallet Instance SHALL support the OpenID4VCI issuance workflow in HAIP 1.0 to obtain both the mVRC Delegation Permission and the delegated mVRC, including credential offers, authorization, token handling, and credential requests. | High | The wallet successfully completes the applicable OpenID4VCI issuance flows and receives the mVRC Delegation Permission and the delegated mVRC. |
| FR-WD2B-002 | Delegated mVRC Data Model and Structure Support | The EUDI Wallet Instance SHALL support processing, storage, and presentation of delegated mVRC credentials using a data model and structure compliant with ISO 7367, the applicable mVRC rulebook, and the delegated vehicle privileges model used in the scenario. | High | The wallet correctly processes and presents delegated mVRC credentials conforming to the expected data model and structure without data loss or misinterpretation. |
| FR-WD2B-003 | Delegated mVRC Credential Format Support | The EUDI Wallet Instance SHALL support receiving, processing, and storing delegated mVRC attestations encoded as `mso_mdoc`. | High | The wallet stores and later retrieves an issued delegated mVRC in `mso_mdoc` format. |
| FR-WD2B-004 | mVRC Delegation Permission Credential Support | The EUDI Wallet Instance SHALL support receiving, processing, storing, and presenting the mVRC Delegation Permission credential issued by the organisation. | High | The wallet successfully receives, stores, and later presents the mVRC Delegation Permission in the delegated mVRC issuance flow. |
| FR-WD2B-005 | mVRC Delegation Permission Lifetime Handling | The EUDI Wallet Instance SHALL support handling the mVRC Delegation Permission as a short-lived, one-time credential intended for use in the delegated mVRC issuance flow. | High | The wallet correctly recognizes the mVRC Delegation Permission usage constraints and uses it only within its valid lifetime and intended issuance context. |
| FR-WD2B-006 | Credential Offer Initialization | The EUDI Wallet Instance SHALL support credential offer and issuance initiation methods used in the scenario, including same-device continuation for issuance of the mVRC Delegation Permission and initiation of delegated mVRC issuance by the official mVRC Issuer. | High | The wallet successfully starts the applicable issuance flows using the supported initiation methods. |
| FR-WD2B-007 | User Consent for Issuance | The EUDI Wallet Instance SHALL display information about the offered credential and require explicit user consent before proceeding with issuance of the mVRC Delegation Permission or the delegated mVRC. | High | The user can approve or cancel issuance after reviewing credential information. |
| FR-WD2B-008 | PKCE Support | The wallet SHALL support PKCE for authorization code flows, including code verifier and challenge handling, where applicable. | High | Token exchange succeeds only with a valid PKCE code verifier when PKCE is required. |
| FR-WD2B-009 | Authorization Code Flow Support | The EUDI Wallet Instance SHALL support the OpenID4VCI authorization code flow for issuance of the mVRC Delegation Permission and the delegated mVRC where used in the scenario. | High | The wallet successfully completes issuance flows using the authorization code flow. |
| FR-WD2B-010 | Client Attestation JWT Support | The wallet SHALL support client authentication using Client Attestation JWT where required. | High | The Authorization Server accepts token requests authenticated with Client Attestation JWT. |
| FR-WD2B-011 | Consumer (Delegated User) Identity Verification Support | The wallet SHALL support the consumer identity verification where required prior to issuance of the mVRC Delegation Permission and/or the delegated mVRC. | High | The wallet completes issuance when the consumer identity verification succeeds and fails when it is required but not completed. |
| FR-WD2B-012 | OpenID4VP Identity Verification via Interactive Authorization Endpoint | The EUDI Wallet Instance SHALL support processing an OpenID4VP presentation request provided in the `openid4vp_request` parameter of an Interactive Authorization Endpoint response in order to perform the consumer identity verification prior to delegated mVRC issuance. | High | The wallet successfully processes the `openid4vp_request`, completes the required presentation, and submits the resulting `openid4vp_response` to the Interactive Authorization Endpoint. |
| FR-WD2B-013 | Identity Credential Format Support | The EUDI Wallet Instance SHALL support presentation of consumer identity credentials, such as mDL or PID, encoded as `mso_mdoc`, where applicable in the scenario. | High | The wallet presents the required identity credential in the expected format when requested. |
| FR-WD2B-014 | User Consent for Verification | The EUDI Wallet Instance SHALL display information about requested identity data prior to credential issuance and require explicit user consent before proceeding. | Medium | The user can approve or cancel the verification process after reviewing the authorization request. |
| FR-WD2B-015 | Identity Assertion Exchange (IAE) Support | The EUDI Wallet Instance SHALL support Identity Assertion Exchange (IAE) where required during the authorization code flow for delegated mVRC issuance. | High | The wallet successfully provides the required interaction responses during issuance when requested by the Issuer. |
| FR-WD2B-016 | Wallet Unit Attestation (WUA) in Proof | The wallet SHALL include a Wallet Unit Attestation (WUA), as defined in ARF TS 3, in the proof sent to the credential endpoint when required. | High | The Issuer validates WUA and issues the credential only when WUA is present. |
| FR-WD2B-017 | Holder Binding and Proof-of-Possession | The EUDI Wallet Instance SHALL support holder binding and proof-of-possession mechanisms in line with HAIP requirements. | High | Issuance succeeds only when valid proof-of-possession is provided. |
| FR-WD2B-018 | Combined Presentation Support | The EUDI Wallet Instance SHALL support combined presentation of the mVRC Delegation Permission and the required identity credential within the same OpenID4VP transaction when requested by the official mVRC Issuer. | High | The wallet successfully presents both the mVRC Delegation Permission and the required identity credential in the same OpenID4VP transaction. |
| FR-WD2B-019 | Display of mVRC Delegation Permission Data | The EUDI Wallet Instance SHALL display the core data contained in a successfully issued mVRC Delegation Permission to the user after completion of the issuance process. | High | The wallet displays the mVRC Delegation Permission only after successful issuance and validation, with data accurately reflecting the credential payload. |
| FR-WD2B-020 | Display of Delegated mVRC Credential Data | The EUDI Wallet Instance SHALL display the core data contained in a successfully issued delegated mVRC credential to the user after completion of the issuance process. | High | The wallet displays the delegated mVRC credential only after successful issuance and validation, with data accurately reflecting the credential payload. If issuance or validation fails, the delegated mVRC credential is not displayed to the user. |
| FR-WD2B-021 | Secure Storage of Delegated Credentials | The EUDI Wallet Instance SHOULD securely store issued mVRC Delegation Permission credentials, delegated mVRC attestations, and associated metadata. | High | Issued credentials are securely stored and accessible only with user authorization. |
| FR-WD2B-022 | Protocol Error Handling | The EUDI Wallet Instance SHALL handle protocol, validation, and network errors gracefully and inform the user. | Medium | The wallet displays meaningful error messages when issuance fails. |
| FR-WD2B-023 | Issuer Access Certificate Validation (ETSI TL) | The wallet SHOULD validate the Issuer’s access certificate using an ETSI Trusted List where applicable. | Medium | The wallet accepts issuers with trusted certificates and rejects invalid ones. |
| FR-WD2B-024 | Issuer Registration Certificate Validation (ETSI TL) | The wallet SHOULD validate the Issuer’s registration certificate using an ETSI Trusted List where required. | Medium | The wallet rejects issuance from issuers with invalid registration status. |
| FR-WD2B-025 | Issuer Seal Validation (ETSI TL) | The wallet SHOULD validate the cryptographic seal on the issued delegated mVRC using trusted list material and, where applicable, validate the seal on the mVRC Delegation Permission. | Medium | The wallet stores only credentials signed by trusted issuers. |
| FR-WD2B-026 | DPoP Support | The wallet SHALL support DPoP for token requests and related proof handling when required by the Authorization Server. | High | The wallet successfully completes token requests when DPoP is required. Requests with missing, invalid, or expired DPoP proof are rejected. |
| FR-WD2B-027 | ETSI Issuance Profile Support | The EUDI Wallet Instance SHALL support the applicable provisions of the ETSI issuance profile used in the scenario. | High | The wallet successfully completes issuance flows that apply the ETSI issuance profile requirements. Flows fail when required profile elements are missing or invalid. |
| FR-WD2B-028 | Interactive Authorization Endpoint Support | The EUDI Wallet Instance SHALL support the Interactive Authorization Endpoint as an authorization interaction model for delegated mVRC issuance, where supported by the Issuer. | High | The wallet successfully completes issuance using the Interactive Authorization Endpoint when supported by the Issuer. |

**Organisation (Vehicle Owner or Holder)**

| Index | Requirement Title | Description | Priority | Acceptance Criteria |
|------:|-------------------|-------------|----------|---------------------|
| FR-O2B-001 | Delegation Service Support | The organisation SHALL provide a web application or equivalent service enabling the consumer to initiate the delegation permission issuance process after completion of the relevant business formalities. | High | The consumer can access a service that starts the delegation permission issuance process. |
| FR-O2B-002 | Delegation Scope and Validity Management | The organisation SHALL manage the rental period and scope of delegated vehicle privileges in accordance with the business agreement and use them as input to issuance of the mVRC Delegation Permission. | High | The issued mVRC Delegation Permission reflects the rental period and scope of delegated privileges defined in the business agreement. |
| FR-O2B-003 | Support OpenID4VP for User Verification | The organisation SHALL support OpenID4VP 1.0 to request and validate presentation of the consumer’s identity credential prior to issuance of the mVRC Delegation Permission. | High | The organisation successfully completes an OpenID4VP flow in which the consumer presents the required identity credential. |
| FR-O2B-004 | Identity Credential Request Support | The organisation SHALL support requesting the consumer’s identity credential, using PID or mDL, as part of the delegation permission issuance process. | High | The organisation can successfully request PID or mDL presentation from the consumer when required by the scenario. |
| FR-O2B-005 | Identity Credential Processing and Validation | The organisation SHALL support processing and validating the consumer’s identity credential, using PID or mDL, before issuance of the mVRC Delegation Permission. | High | The mVRC Delegation Permission is issued only when the presented identity credential is successfully validated. |
| FR-O2B-006 | Support mso_mdoc Format for Identity Credential | The organisation SHALL support processing identity credentials encoded as `mso_mdoc`, where applicable in the scenario. | High | The organisation successfully processes the required identity credential in the expected format. |
| FR-O2B-007 | User Verification | The organisation SHALL verify the identity of the consumer (delegated user) before issuing the mVRC Delegation Permission. | High | The mVRC Delegation Permission is issued only after successful delegated user identity verification. |
| FR-O2B-008 | Support OpenID4VCI Issuance | The organisation SHALL support OpenID4VCI issuance flows for issuance of the mVRC Delegation Permission to the consumer's wallet. | High | The organisation successfully completes an OpenID4VCI issuance flow with a compliant wallet and issues the mVRC Delegation Permission. |
| FR-O2B-009 | Authorization Code Flow Support | The organisation SHALL support the authorization code flow for issuance of the mVRC Delegation Permission. | High | The organisation successfully issues the mVRC Delegation Permission using the authorization code flow. |
| FR-O2B-010 | Same-Device Flow Continuation Support | The organisation SHALL support continuation from the verification step to the issuance step on the same mobile device. | High | After successful verification, the consumer can continue the issuance flow on the same device without restarting the transaction. |
| FR-O2B-011 | Credential Offer and Issuance Initiation Support | The organisation SHALL support generation of the data required to initiate issuance of the mVRC Delegation Permission in the consumer's wallet. | High | After successful verification, the wallet can start the issuance flow using the initiation data provided by the organisation. |
| FR-O2B-012 | mVRC Delegation Permission Generation | The organisation SHALL generate an mVRC Delegation Permission containing the delegated vehicle privileges and validity period established in the business process. | High | The issued mVRC Delegation Permission contains the expected delegation scope and validity period. |
| FR-O2B-013 | mVRC Delegation Permission Data Model Support | The organisation SHALL generate the mVRC Delegation Permission using the data model and structure defined for the scenario. | High | The issued mVRC Delegation Permission conforms to the expected data model and structure. |
| FR-O2B-014 | Credential Signing | The organisation SHALL sign the mVRC Delegation Permission using its applicable signing certificate and trust chain. | High | The mVRC Delegation Permission is cryptographically signed and can be validated by relying parties. |
| FR-O2B-015 | Holder Binding Support | The organisation SHALL issue the mVRC Delegation Permission bound to the consumer's wallet in accordance with the applicable proof-of-possession and holder binding requirements. | High | The issued mVRC Delegation Permission is cryptographically bound to the consumer's wallet. |
| FR-O2B-016 | Metadata Publication | The organisation SHALL publish the metadata required for issuance of the mVRC Delegation Permission, including supported credential configurations, proof types, endpoints, and applicable authorization capabilities. | High | A compliant wallet can retrieve and use the organisation metadata to complete the issuance flow. |
| FR-O2B-017 | PKCE Validation | The organisation SHALL support and validate PKCE in authorization code issuance flows where applicable. | High | Token exchange succeeds only when a valid PKCE code verifier is presented. |
| FR-O2B-018 | Client Attestation JWT Support | The organisation SHALL support Client Attestation JWT validation where wallet client authentication is required. | High | The organisation accepts token requests authenticated with a valid Client Attestation JWT. |
| FR-O2B-019 | Wallet Proof Validation | The organisation SHALL validate the wallet proof submitted at the credential endpoint, including proof-of-possession and Wallet Unit Attestation where required. | High | The credential is issued only when the submitted proof satisfies the applicable validation requirements. |
| FR-O2B-020 | DPoP Validation | The organisation SHALL support and validate DPoP for token requests where required by the Authorization Server. | High | Token requests with missing, invalid, or expired DPoP proof are rejected. |
| FR-O2B-021 | Trust Validation | The organisation SHOULD validate the trust status of the consumer's wallet and presented credentials according to the applicable trust framework and trusted list material. | Medium | Untrusted wallets or credentials are detected and rejected according to the applicable trust model. |
| FR-O2B-022 | Error Handling | The organisation SHOULD handle protocol, validation, and trust errors and return consistent error responses. | Medium | Errors are returned in a consistent form and logged for diagnostics. |


**mVRC / Delegated mVRC Issuer**

| Index | Requirement Title | Description | Priority | Acceptance Criteria |
|------:|-------------------|-------------|----------|---------------------|
| FR-I2B-001 | Delegated mVRC Issuance Service Support | The Issuer SHALL provide a dedicated service enabling the delegated user to request issuance of a delegated mVRC based on a previously issued mVRC Delegation Permission. | High | The user can access a service that starts the delegated mVRC issuance process. |
| FR-I2B-002 | Support OpenID4VP for Delegated mVRC Issuance | The Issuer SHALL support OpenID4VP 1.0 to request and validate presentation of the mVRC Delegation Permission and the required identity credential prior to delegated mVRC issuance. | High | The Issuer successfully completes an OpenID4VP flow in which the user presents the required credentials. |
| FR-I2B-003 | Combined Presentation Request Support | The Issuer SHALL support requesting combined presentation of the mVRC Delegation Permission and the required identity credential within the same OpenID4VP transaction. | High | The Issuer successfully requests and validates both credentials in the same OpenID4VP transaction. |
| FR-I2B-004 | mVRC Delegation Permission Validation | The Issuer SHALL validate the authenticity, integrity, trust status, and applicability of the presented mVRC Delegation Permission before issuing the delegated mVRC. | High | The delegated mVRC is issued only if the mVRC Delegation Permission is successfully validated. |
| FR-I2B-005 | mVRC Delegation Permission Usage Constraint Validation | The Issuer SHALL validate that the presented mVRC Delegation Permission is used within its valid lifetime and intended one-time issuance context. | High | The delegated mVRC is issued only if the mVRC Delegation Permission is valid, unexpired, and acceptable for the current issuance transaction. |
| FR-I2B-006 | Identity Credential Request Support | The Issuer SHALL support requesting the delegated user identity credential, using PID or mDL, as part of the delegated mVRC issuance process. | High | The Issuer can successfully request PID or mDL presentation from the user when required by the scenario. |
| FR-I2B-007 | Identity Credential Processing and Validation | The Issuer SHALL support processing and validating the consumer's identity credential, using PID or mDL, before issuance of the delegated mVRC. | High | The delegated mVRC is issued only when the presented identity credential is successfully validated. |
| FR-I2B-008 | Support mso_mdoc Format for Identity Credential | The Issuer SHALL support processing identity credentials encoded as `mso_mdoc`, where applicable in the scenario. | High | The Issuer successfully processes the required identity credential in the expected format. |
| FR-I2B-009 | Consumer's Identity Verification | The Issuer SHALL verify the identity of the consumer before issuing the delegated mVRC. | High | A delegated mVRC is issued only after successful consumer's identity verification. |
| FR-I2B-010 | Subject Binding Validation | The Issuer SHALL verify that the consumer receiving the delegated mVRC is the same subject authorized by the mVRC Delegation Permission, where applicable to the credential design. | High | The delegated mVRC is issued only when the presented identity is consistent with the authorization context represented by the mVRC Delegation Permission. |
| FR-I2B-011 | Support OpenID4VCI Issuance | The Issuer SHALL support OpenID4VCI issuance flows for issuance of delegated mVRC credentials to the consumer's wallet. | High | The Issuer successfully completes an OpenID4VCI issuance flow with a compliant wallet and issues the delegated mVRC. |
| FR-I2B-012 | Authorization Code Flow Support | The Issuer SHALL support the authorization code flow for issuance of the delegated mVRC. | High | The Issuer successfully issues the delegated mVRC using the authorization code flow. |
| FR-I2B-013 | Interactive Authorization Endpoint Support | The Issuer SHALL support the Interactive Authorization Endpoint where the consumer's identity verification is required during the authorization code flow. | High | The consumer's wallet successfully completes issuance flows requiring one or more interactions through the Interactive Authorization Endpoint. |
| FR-I2B-014 | OpenID4VP Request via Interactive Authorization Endpoint | Where he consumer's identity verification is required, the Issuer SHALL return an OpenID4VP authorization request in the `openid4vp_request` parameter of the Interactive Authorization Endpoint response. | High | The consumer's wallet receives an Interactive Authorization Endpoint response containing a valid `openid4vp_request` and can continue the flow. |
| FR-I2B-015 | Credential Offer and Issuance Initiation Support | The Issuer SHALL support generation of the data required to initiate issuance of the delegated mVRC in the consumer's wallet. | High | After successful validation of the presented credentials, the wallet can start or continue the issuance flow using the initiation data provided by the Issuer. |
| FR-I2B-016 | Delegated mVRC Generation | The Issuer SHALL generate a delegated mVRC containing vehicle privileges, consumer personal data, and the established validity period. | High | The issued delegated mVRC contains the expected delegation scope, subject data, and validity period. |
| FR-I2B-017 | Delegated mVRC Data Model Compliance | The Issuer SHALL issue delegated mVRC credentials using a data model and structure compliant with ISO 7367, the applicable mVRC rulebook, and the delegated privileges model used in the scenario. | High | The issued delegated mVRC conforms to the expected data model and structure. |
| FR-I2B-018 | Support mso_mdoc Format for Delegated mVRC | The Issuer SHALL issue delegated mVRC credentials in `mso_mdoc` format. | High | The delegated mVRC is issued in `mso_mdoc` format and can be processed by a compliant wallet. |
| FR-I2B-019 | Credential Signing | The Issuer SHALL sign the delegated mVRC using its applicable signing certificate and trust chain. | High | The delegated mVRC is cryptographically signed and can be validated by relying parties. |
| FR-I2B-020 | Holder Binding Support | The Issuer SHALL issue the delegated mVRC bound to the consumer's wallet in accordance with the applicable proof-of-possession and holder binding requirements. | High | The issued delegated mVRC is cryptographically bound to the consumer's wallet. |
| FR-I2B-021 | Metadata Publication | The Issuer SHALL publish the metadata required for delegated mVRC issuance, including supported credential configurations, proof types, endpoints, and applicable authorization capabilities. | High | A compliant wallet can retrieve and use Issuer metadata to complete the issuance flow. |
| FR-I2B-022 | PKCE Validation | The Issuer SHALL support and validate PKCE in authorization code issuance flows where applicable. | High | Token exchange succeeds only when a valid PKCE code verifier is presented. |
| FR-I2B-023 | Client Attestation JWT Support | The Issuer SHALL support Client Attestation JWT validation where wallet client authentication is required. | High | The Issuer accepts token requests authenticated with a valid Client Attestation JWT. |
| FR-I2B-024 | Wallet Proof Validation | The Issuer SHALL validate the wallet proof submitted at the credential endpoint, including proof-of-possession and Wallet Unit Attestation where required. | High | The credential is issued only when the submitted proof satisfies the applicable validation requirements. |
| FR-I2B-025 | DPoP Validation | The Issuer SHALL support and validate DPoP for token requests where required by the Authorization Server. | High | Token requests with missing, invalid, or expired DPoP proof are rejected. |
| FR-I2B-026 | Trust Validation of Wallet and Presented Credentials | The Issuer SHOULD validate the trust status of wallets and presented credentials according to the applicable trust framework and trusted list material. | Medium | Untrusted wallets or credentials are detected and rejected according to the applicable trust model. |
| FR-I2B-027 | Error Handling | The Issuer SHOULD handle protocol, validation, and trust errors and return consistent error responses. | Medium | Errors are returned in a consistent form and logged for diagnostics. |

---

#### 8.5.2	Protocol profile

**OpenID4VCI (permission + delegated mVRC)**

Specification: OpenID for Verifiable Credential Issuance 1.0 / 1.1  
Profile: High Assurance Interoperability Profile (HAIP) 1.0  
Flow: Authorization Code Flow with Interactive Authorization Endpoint (IAE)  

Key characteristics:
- Credential issuance initiated via credential offer or same-device flow;
- Supports issuance of two credentials: the mVRC delegation permission and delegated mVRC;
- Credential format: mso_mdoc;
- Integration of identity verification within the issuance flow;
- Support for interactive authorisation flows using the Interactive Authorisation Endpoint (IAE);
- Holder binding using proof-of-possession mechanisms;

Implementation characteristics:
- Supported credential offer schemes: haip-vci and openid-credential-offer;
- Authorisation flow using Authorisation Code Flow with PKCE;
- Support for IAE and iae_post.jwt response mode;
- Issuance mode: immediate issuance;
- Request URI methods: GET and POST;

<br>

**OpenID4VP**

Specification: OpenID for Verifiable Presentations 1.0  
Profile: High Assurance Interoperability Profile (HAIP) 1.0  

Key characteristics:
- Request/response-based presentation flow using authorisation requests;
- Support for response mode: direct_post.jwt;
- Credential format: mso_mdoc;
- Combined presentation of the mVRC delegation permission and identity credential;
- Selective disclosure of requested attributes;
- Holder binding using proof-of-possession mechanisms;

Implementation characteristics:
- Supported request schemes: haip-vp, openid4vp, mdoc-openid4vp;
- Authorisation requests are implemented using JSON Web Token (JAR) by reference;
- Response mode: direct_post.jwt;
- Client identifier prefix type: x509_hash (as defined in HAIP 1.0);
- Use of nonce values to ensure replay protection;
- Support for credential status verification using status lists;

---

#### 8.5.3	Trust and security mechanisms

The scenario relies on a combination of cryptographic and trust mechanisms to ensure secure issuance and validation of both the mVRC dDelegation pPermission and the delegated mVRC, including:

- Holder binding and proof-of-possession (PoP);
- Wallet attestation mechanisms, including Wallet Unit Attestation (WUA) and Wallet Instance Attestation (WIA), as defined in ARF TS 3;
- Client authentication using Client Attestation JWT;
- Use of nonce values to prevent replay attacks;
- Validation of trust anchors using ETSI Trusted Lists (e.g. ETSI TS 119 612) or equivalent mechanisms;
- Validation of organiszation and issuer certificates and trust status;
- Validation of mVRC dDelegation pPermission authenticity, integrity, and usage constraints (e.g. lifetime and one-time usage);
- Validation of credential integrity and authenticity (signature validation of delegated mVRC);
- Subject binding validation between the delegation permission and the consumer identity;
- Alignment with applicable ETSI issuance profiles;

---

#### 8.5.4	Endpoints

| Standard | Endpoint | Usage in Scenario | Reference |
|----------|----------|------------------|-----------|
| OpenID4VCI 1.0 / HAIP 1.0 / ETSI TS 119 472-3 | Credential Offer Endpoint | Required | [OpenID4VCI 1.0](https://openid.net/specs/openid-4-verifiable-credential-issuance-1_0.html#section-4), [HAIP 1.0](https://openid.net/specs/openid4vc-high-assurance-interoperability-profile-1_0.html#section-4.2), [ETSI TS 119 472-3](https://www.etsi.org/deliver/etsi_ts/119400_119499/11947203/01.01.01_60/ts_11947203v010101p.pdf)  |
| OpenID4VCI 1.0 / HAIP 1.0 / ETSI TS 119 472-3 | Token Endpoint | Required | [OpenID4VCI 1.0](https://openid.net/specs/openid-4-verifiable-credential-issuance-1_0.html#section-6), [HAIP 1.0](https://openid.net/specs/openid4vc-high-assurance-interoperability-profile-1_0.html#section-4.4), [ETSI TS 119 472-3](https://www.etsi.org/deliver/etsi_ts/119400_119499/11947203/01.01.01_60/ts_11947203v010101p.pdf)  |
| OpenID4VCI 1.0 / HAIP 1.0 | Nonce Endpoint | Required | [OpenID4VCI 1.0](https://openid.net/specs/openid-4-verifiable-credential-issuance-1_0.html#section-7) |
| OpenID4VCI 1.0 / HAIP 1.0 / ETSI TS 119 472-3 | Credential Endpoint | Required | [OpenID4VCI 1.0](https://openid.net/specs/openid-4-verifiable-credential-issuance-1_0.html#section-8), [HAIP 1.0](https://openid.net/specs/openid4vc-high-assurance-interoperability-profile-1_0.html#section-4.5), [ETSI TS 119 472-3](https://www.etsi.org/deliver/etsi_ts/119400_119499/11947203/01.01.01_60/ts_11947203v010101p.pdf) |
| OpenID4VCI 1.0 / ETSI TS 119 472-3 | Notification Endpoint | Optional | [OpenID4VCI 1.0](https://openid.net/specs/openid-4-verifiable-credential-issuance-1_0.html#section-11), [ETSI TS 119 472-3](https://www.etsi.org/deliver/etsi_ts/119400_119499/11947203/01.01.01_60/ts_11947203v010101p.pdf) |
| OpenID4VCI 1.0 / HAIP 1.0 / ETSI TS 119 472-3 | Credential Issuer Metadata Endpoint | Required | [OpenID4VCI 1.0](https://openid.net/specs/openid-4-verifiable-credential-issuance-1_0.html#section-12.2), [HAIP 1.0](https://openid.net/specs/openid4vc-high-assurance-interoperability-profile-1_0.html#section-4.1), [ETSI TS 119 472-3](https://www.etsi.org/deliver/etsi_ts/119400_119499/11947203/01.01.01_60/ts_11947203v010101p.pdf) |
| RFC 8414 / OpenID4VCI 1.0 | Authorization Server Metadata Endpoint | Required | [RFC 8414](https://datatracker.ietf.org/doc/html/rfc8414), [Attestation-Based Client Authentication](https://www.ietf.org/archive/id/draft-ietf-oauth-attestation-based-client-auth-08.html#name-authorization-server-metada), [DPOP](https://www.rfc-editor.org/rfc/rfc9449.html#section-5.1), [OpenID4VCI 1.1 draft](https://openid.github.io/OpenID4VCI/openid-4-verifiable-credential-issuance-1_1-wg-draft.html#name-interactive-authorization-e)  |
| Token Status List | Status List Endpoint | Optional | [Token Status List](https://datatracker.ietf.org/doc/draft-ietf-oauth-status-list/) |
| OpenID4VCI 1.1 draft | Interactive Authorization Endpoint (`/iae`) | Optional | [OpenID4VCI 1.1 draft](https://openid.github.io/OpenID4VCI/openid-4-verifiable-credential-issuance-1_1-wg-draft.html#name-interactive-authorization-e) |
| Implementation-specific | Init Endpoint | Optional | N/A |
| Implementation-specific | Status Endpoint | Optional | N/A |

---

#### 8.5.5	Technical interaction flow – sequence diagrams

The following sequence diagrams illustrate the delegated mVRC issuance flow for Scenario 2B and show the technical interaction between the consumer's EUDI wallet, the organisation, and the mVRC issuer.

The diagrams present the two-step process involving issuance of the mVRC delegation permission by the organisation and subsequent issuance of the delegated mVRC by the official mVRC issuer, including identity verification, authorisation validation and credential delivery.

##### Basic flow
```mermaid
flowchart LR
  subgraph WALLET[Wallet provider]
    WD[Delegated User EUDI Wallet Instance]
  end
  subgraph ORG[Organisation - Vehicle Owner]
    AS2[Authorization Server\ OpenID4VCI]
    I2[mVRC / mVRC Delegation Permission Issuer\ OpenID4VCI]
  end
  subgraph ISSUER[mVRC Issuer]
    AS[Authorization Server\ OpenID4VCI]
    I[mVRC / Delegated mVRC Issuer\ OpenID4VCI]
  end

  WD -->|OpenID4VCI| I2
  WD -->|OpenID4VCI IAE| AS2
  WD -->|OpenID4VCI| I
  WD -->|OpenID4VCI IAE| AS

```

##### Sequence diagram
```mermaid
sequenceDiagram
  autonumber
  actor UD as Delegated User
  participant WD as Delegated User EUDI Wallet instance
  box organisation (Vehicle owner) 
  participant B1 as Organisation web app(frontend)
  participant I1 as Organisation - Issuer API (OpenID4VCI)
  participant AS1 as Organisation - Authorization Server (OpenID4VCI)
 end
  box mVRC Issuer 
  participant B as mVRC Issuer web app(frontend)
  participant I as mVRC Issuer - Issuer API (OpenID4VCI)
  participant AS as mVRC Issuer - Authorization Server (OpenID4VCI)
 end


rect rgba(100, 170, 120, 0.18)
      Note left of UD: GET mVRC Delegation permission from Organisation (OpenID4VCI)
  UD->>B1: Open Organisation start page for delegation process
  B1->>I1: POST /init (prepare credential offer parameters)
   I1->>B1: response with QR Code and credetial offer
   B1->>UD: Display QR + deep link button (credential_offer_uri)
   B1->>I1: GET /status
   I1-->>B1: http 201 
  loop
  B1->>I1: GET /status poll request
  I1->>B1: http 200 (Status=PENDING)
  end
alt Obtain credential offer (cross device or same device flow)
  UD->>WD: Open EUDI mob app and scan QR code
  else
  UD->>B1: press deeplink button
  B1->>WD: invoke EUDI Wallet mob app
 end
  WD->>I1: credential offer request
  I1->>WD: credential offer
  WD->>I1: GET /.well-known/openid-credential-issuer
  I1->>WD: Credential Issuer Metadata
  WD->>AS1: GET /.well-known/oauth-authorization-server
  AS1->>WD: AS Metadata
  WD->>UD: Display mVRC credential offer and metadata<br/> (issuer business name, credential name, claim list, logotype, etc)
  UD->>WD: Accept credential offer

    WD->>WD: Obtain WIA (client attestation JWT) from Wallet Provider Backend
    WD->>WD: Create fresh Client attestation JWt POP
    WD->>AS1: POST /iae initial request (client_id, scope, PKCE, client_attestation_jwt (wia) with fresh pop, etc )
    AS1->>WD: openid4vp authorization request object (with dcql query)
    WD->>WD: parse authorization request
    WD->>UD: display data sharing screen
    UD->>WD: Accept PID data scharing and PIN, biometrics authentication
    WD->>WD: Prepare and sign VP token
    WD->>AS1: OpenID4VP response - follow up request (VP token with PID presentation: mso_mdoc or SD-JWT VC)
  AS1->>WD: respnse follow up request (code, status)
  WD->>AS1: POST /token (code, code_verifier, client_attestation_jwt (wia) with fresh pop )
  AS1->>WD: access_token (+ optional refresh_token)

    WD->>I1: POST /nonce (request c_nonce)
    I1->>WD: c_nonce + c_nonce_expires_in
  WD->>I1: POST /credential (Authorization: Bearer access_token, proof with key attestation (WUA)
  I1->>I1: Prepare, sign, encode mso_mdoc object (mVRC delegation permission)
  I1->>WD: Credential response (mVRC delegation permission as signed, encoded mso_mdoc object)
  WD->>WD: Store mVRC delegation permission
  opt Notification (optional)
    WD->>I1: POST /notification 
    I1->>WD: 204 OK
  end
  WD->>UD: Show success screen in wallet
  B1->>I1: GET /status poll request
  I1->>B1: http 200 (Status=OK polling ended)
  B1->>UD: present success screen
end
 

rect rgba(200, 140, 90, 0.18)
      Note left of UD: GET delegated mVRC from mVRC Issuer (OpenID4VCI)
  UD->>B: Open mVRC Issuer start page for delegation process
  B->>I: POST /init (prepare credential offer parameters)
   I->>B: response with QR Code and credetial offer
   B->>UD: Display QR + deep link button (credential_offer_uri)
   B->>I: GET /status
   I-->>B: http 201 
  loop
  B->>I: GET /status poll request
  I->>B: http 200 (Status=PENDING)
  end
alt Obtain credential offer (cross device or same device flow)
  UD->>WD: Open EUDI mob app and scan QR code
  else
  UD->>B: press deeplink button
  B->>WD: invoke EUDI Wallet mob app
 end
  WD->>I: credential offer request
  I->>WD: credential offer
  WD->>I: GET /.well-known/openid-credential-issuer
  I->>WD: Credential Issuer Metadata
  WD->>AS: GET /.well-known/oauth-authorization-server
  AS->>WD: AS Metadata
  WD->>UD: Display mVRC credential offer and metadata<br/> (issuer business name, credential name, claim list, logotype, etc)
  UD->>WD: Accept credential offer

    WD->>WD: Obtain WIA (client attestation JWT) from Wallet Provider Backend
    WD->>WD: Create fresh Client attestation JWt POP
    WD->>AS: POST /iae initial request (client_id, scope, PKCE, client_attestation_jwt (wia) with fresh pop, etc )
    AS->>WD: openid4vp authorization request object (with dcql query)
    WD->>WD: parse authorization request
    WD->>UD: display data sharing screen
    UD->>WD: Accept PID data scharing and PIN, biometrics authentication
    WD->>WD: Prepare and sign VP token
    WD->>AS: OpenID4VP response - follow up request (VP token with PID presentation: mso_mdoc or SD-JWT VC)
  AS->>WD: respnse follow up request (code, status)
  WD->>AS: POST /token (code, code_verifier, client_attestation_jwt (wia) with fresh pop )
  AS->>WD: access_token (+ optional refresh_token)

    WD->>I: POST /nonce (request c_nonce)
    I->>WD: c_nonce + c_nonce_expires_in
  WD->>I: POST /credential (Authorization: Bearer access_token, proof with key attestation (WUA)
  I->>I: Prepare, sign, encode mso_mdoc object (delegated mVRC)
  I->>WD: Credential response (delegated mVRC as signed, encoded mso_mdoc object)
  WD->>WD: Store delegated mVRC 
  opt Notification (optional)
    WD->>I: POST /notification 
    I->>WD: 204 OK
  end
  WD->>WD: Remove mVRC delegation permission
  WD->>UD: Show success screen in wallet
  B->>I: GET /status poll request
  I->>B: http 200 (Status=OK polling ended)
  B->>UD: present success screen
end
```

---

##### Extended flow

```mermaid
flowchart LR
    subgraph WALLET[Wallet provider]
    WD[Delegated User EUDI Wallet Instance]
    WPB[WUA status list]
  end
  subgraph ORG[Organisation - Vehicle Owner]
    AS1[Authorization Server\ OpenID4VCI]
    I1[mVRC / mVRC Delegation Permission Issuer\ OpenID4VCI]
  end
  subgraph ISSUER[mVRC Issuer]
    AS[Authorization Server\ OpenID4VCI]
    I[mVRC / Delegated mVRC Issuer\ OpenID4VCI]
  end
 subgraph PID[PID Provider/ mDL Provider]
    PIDSL[PID/mDL Status List]
  end
 subgraph TRUST[Trusted Lists Provider]
     TLP[PID Provider/ mDL Provider Trusted List]
     TLW[Wallet Provider Trusted List]
     TLRP[WRPAC Trusted List]
  end
  subgraph REGISTRY[National Vehicle Registry]
    R[mVRC data registry]
  end

  WD -->|OpenID4VCI IAE| AS1
  WD -->|OpenID4VCI| I1
  AS1 -->|Get PID status list| PIDSL
  AS1 -->|Get trusted list| TLP
  I1 -->|Get trusted list| TLW
  AS1 -->|Get trusted list| TLW
  WD ---|Get trusted list| TLRP
  WPB ---|Get WUA status list| I1
 
  WD -->|OpenID4VCI| I
  WD -->|OpenID4VCI IAE| AS
  AS -->|Get PID status list| PIDSL
  AS -->|Get trusted list| TLP
  I -->|Get trusted list| TLW
  AS -->|Get trusted list| TLW
  WPB ---|Get WUA status list| I
  I -->|Get mVRC data| R
```
##### Sequence diagram
```mermaid
sequenceDiagram
  autonumber
  actor UD as Delegated User
  participant WD as Delegated User EUDI Wallet instance
  box Organisation (Vehicle owner) 
  participant B1 as Organisation web app(frontend)
  participant I1 as Organisation - Issuer API (OpenID4VCI)
  participant AS1 as Organisation - Authorization Server (OpenID4VCI)
 end
  box mVRC Issuer 
  participant B as mVRC Issuer web app(frontend)
  participant I as mVRC Issuer - Issuer API (OpenID4VCI)
  participant AS as mVRC Issuer - Authorization Server (OpenID4VCI)
 end
 participant R as Vehicle Registry (optional)
  participant TL as Trusted Lists Provider (optional)
  participant PD as PID Provider/mDL Provider (optional)
  participant WP as Wallet Provider (optional)

rect rgba(100, 170, 120, 0.18)
      Note left of UD: GET mVRC Delegation permission from Organisation (OpenID4VCI)
  UD->>B1: Open Organisation start page for delegation process
  B1->>I1: POST /init (prepare credential offer parameters)
   I1->>B1: response with QR Code and credetial offer
   B1->>UD: Display QR + deep link button (credential_offer_uri)
   B1->>I1: GET /status
   I1-->>B1: http 201 
  loop
  B1->>I1: GET /status poll request
  I1->>B1: http 200 (Status=PENDING)
  end
alt Obtain credential offer (cross device or same device flow)
  UD->>WD: Open EUDI mob app and scan QR code
  else
  UD->>B1: press deeplink button
  B1->>WD: invoke EUDI Wallet mob app
 end
  WD->>I1: credential offer request
  I1->>WD: credential offer
  WD->>I1: GET /.well-known/openid-credential-issuer
  I1->>WD: Credential Issuer Metadata
  opt Trust check (optional)
    WD->>TL: WRPAC trusted List
    TL->>WD: WRPAC trusted List
    WD->>WD: mVRC Issuer access certficate validation &cache Trusted list
  end
  WD->>AS1: GET /.well-known/oauth-authorization-server
  AS1->>WD: AS Metadata
  WD->>UD: Display mVRC credential offer and metadata<br/> (issuer business name, credential name, claim list, logotype, etc)
  UD->>WD: Accept credential offer

    WD->>WD: Obtain WIA (client attestation JWT) from Wallet Provider Backend
    WD->>WD: Create fresh Client attestation JWt POP
    WD->>AS1: POST /iae initial request (client_id, scope, PKCE, client_attestation_jwt (wia) with fresh pop, etc )
    AS1->>AS1: Parse and Validate Pushed authorization request
    opt Authorization Server trust checks (optional)
    AS1->>TL: GET Wallet provider trusted List
    TL->>AS1: JWT/CWT with Wallet provider trusted List
    AS1->>AS1: WIA seal x5c validation
  end
    AS1->>WD: openid4vp authorization request object (with dcql query)
    WD->>WD: parse authorization request
    WD->>UD: display data sharing screen
    UD->>WD: Accept PID data scharing and PIN, biometrics authentication
    WD->>WD: Prepare and sign VP token
    WD->>AS1: OpenID4VP response - follow up request (VP token with PID presentation: mso_mdoc or SD-JWT VC)
    AS1->>AS1: Parse and validate VP token
      opt Verifier trust checks (optional)
      AS1->>TL: PID Provider/mDL Provider trusted List
      TL->>AS1: PID Provider/mDL Provider trusted List
      AS1->>AS1: PID seal x5c validation
     end
    opt PID status list check (optional)
      AS1->>PD: Get PID/mDL status list
      PD->>AS1: JWT/CWT with PID/mDL status list
      AS1->>AS1: PID/mDL idx validation
    end
  AS1->>WD: respnse follow up request (code, status)
  WD->>AS1: POST /token (code, code_verifier, client_attestation_jwt (wia) with fresh pop )
  AS1->>AS1: Parse and validate token request
  AS1->>WD: access_token (+ optional refresh_token)
    WD->>I1: POST /nonce (request c_nonce)
    I1->>WD: c_nonce + c_nonce_expires_in
  WD->>I1: POST /credential (Authorization: Bearer access_token, proof with key attestation (WUA)
     opt Issuer trust checks (optional)
    I1->>TL: GET Wallet provider trusted List
    TL->>I1: JWT/CWT with Wallet provider trusted List
    I1->>I: WUA seal x5c validation
  end
   opt WUA status list check (optional)
      I1->>WP: Get WUA status list
      WP->>I1: JWT/CWT with WUA status list
      I1->>I1: WUA idx validation
   end
  I1->>I1: Prepare, sign, encode mso_mdoc object (mVRC delegation permission)
  I1->>WD: Credential response (mVRC delegation permission as signed, encoded mso_mdoc object)
  opt Organisation (mVRC delegation permission) trust checks (optional)
    WD->>WD: delegated mVRC seal x5c validation
  end
  WD->>WD: Store mVRC delegation permission
  opt Notification (optional)
    WD->>I1: POST /notification 
    I1->>WD: 204 OK
  end
  WD->>UD: Show success screen in wallet
  B1->>I1: GET /status poll request
  I1->>B1: http 200 (Status=OK polling ended)
  B1->>UD: present success screen
end
 

rect rgba(200, 140, 90, 0.18)
      Note left of UD: GET delegated mVRC from mVRC Issuer (OpenID4VCI)
  UD->>B: Open mVRC Issuer start page for delegation process
  B->>I: POST /init (prepare credential offer parameters)
   I->>B: response with QR Code and credetial offer
   B->>UD: Display QR + deep link button (credential_offer_uri)
   B->>I: GET /status
   I-->>B: http 201 
  loop
  B->>I: GET /status poll request
  I->>B: http 200 (Status=PENDING)
  end
alt Obtain credential offer (cross device or same device flow)
  UD->>WD: Open EUDI mob app and scan QR code
  else
  UD->>B: press deeplink button
  B->>WD: invoke EUDI Wallet mob app
 end
  WD->>I: credential offer request
  I->>WD: credential offer
  WD->>I: GET /.well-known/openid-credential-issuer
  I->>WD: Credential Issuer Metadata
     opt Trust check (optional)
    WD->>WD: mVRC Issuer access certficate validation 
  end
  WD->>AS: GET /.well-known/oauth-authorization-server
  AS->>WD: AS Metadata
  WD->>UD: Display mVRC credential offer and metadata<br/> (issuer business name, credential name, claim list, logotype, etc)
  UD->>WD: Accept credential offer

    WD->>WD: Obtain WIA (client attestation JWT) from Wallet Provider Backend
    WD->>WD: Create fresh Client attestation JWt POP
    WD->>AS: POST /iae initial request (client_id, scope, PKCE, client_attestation_jwt (wia) with fresh pop, etc )
    AS->>AS: Parse and Validate Pushed authorization request
    opt Authorization Server trust checks (optional)
    AS->>TL: GET Wallet provider trusted List
    TL->>AS: JWT/CWT with Wallet provider trusted List
    AS->>AS: WIA seal x5c validation
  end
    AS->>WD: openid4vp authorization request object (with dcql query)
    WD->>WD: parse authorization request
    WD->>UD: display data sharing screen
    UD->>WD: Accept PID data scharing and PIN, biometrics authentication
    WD->>WD: Prepare and sign VP token
    WD->>AS: OpenID4VP response - follow up request (VP token with PID presentation: mso_mdoc or SD-JWT VC)
 AS1->>AS1: Parse and validate VP token
      opt Verifier trust checks (optional)
      AS->>TL: PID Provider/mDL Provider trusted List
      TL->>AS: PID Provider/mDL Provider trusted List
      AS->>AS: PID seal x5c validation
     end
    opt PID status list check (optional)
      AS->>PD: Get PID/mDL status list
      PD->>AS: JWT/CWT with PID/mDL status list
      AS->>AS: PID/mDL idx validation
    end
  AS->>WD: respnse follow up request (code, status)
  WD->>AS: POST /token (code, code_verifier, client_attestation_jwt (wia) with fresh pop )
  AS->>WD: access_token (+ optional refresh_token)
    WD->>I: POST /nonce (request c_nonce)
    I->>WD: c_nonce + c_nonce_expires_in
  WD->>I: POST /credential (Authorization: Bearer access_token, proof with key attestation (WUA)
      opt Issuer trust checks (optional)
    I->>TL: GET Wallet provider trusted List
    TL->>I: JWT/CWT with Wallet provider trusted List
    I->>I: WUA seal x5c validation
  end
   opt WUA status list check (optional)
      I->>WP: Get WUA status list
      WP->>I: JWT/CWT with WUA status list
      I->>I: WUA idx validation
   end
      opt mVRC data retrieval (optional)
    I->>R: Query vehicle/owner data (using vehicle owner PID data)
    R->>I: mVRC data attributes
  end
opt mVRC status
  I->>I: add a new status index for delegated mVRC instance being issued.
  end
  I->>I: Prepare, sign, encode mso_mdoc object (delegated mVRC)
  I->>WD: Credential response (delegated mVRC as signed, encoded mso_mdoc object)
  opt Issuer trust checks (optional)
    WD->>WD: delegated mVRC seal x5c validation
  end
  WD->>WD: Store delegated mVRC 
  opt Notification (optional)
    WD->>I: POST /notification 
    I->>WD: 204 OK
  end
  WD->>WD: Remove mVRC delegation permission
  WD->>UD: Show success screen in wallet
  B->>I: GET /status poll request
  I->>B: http 200 (Status=OK polling ended)
  B->>UD: present success screen
end
```

### 8.6 Scenario 2C – mVRC delegation / remote data sharing

#### 8.6.1	Functional requirements

Scenario 2C is based on OpenID4VP 1.0, aligned with the HAIP 1.0, and supports secure and interoperable remote presentation of the delegated mVRC credentials from the EUDI wallet to a verifier. The scenario enables the use of delegated mVRC data within remote service interactions, where verification of the delegated vehicle privileges and user identity is required.

**EUDI Wallet Instance**

| Index | Requirement Title | Description | Priority | Acceptance Criteria |
|------:|-------------------|-------------|----------|---------------------|
| FR-W2C-01 | Support OpenID4VP | The wallet SHALL support the OpenID for Verifiable Presentations (OpenID4VP) 1.0 protocol for remote presentation of mVRC (delegated) data. | High | The wallet can successfully complete an OpenID4VP flow with a compliant Verifier. |
| FR-W2C-02 | HAIP 1.0 Compliance | The wallet SHALL comply with the High Assurance Interoperability Profile (HAIP) 1.0 requirements applicable to presentation flows. | High | Presentation flows meet HAIP-defined security and assurance requirements. |
| FR-W2C-03 | Support mso_mdoc Format | The wallet SHALL support the mso_mdoc credential format for mVRC (delegated) credentials, in accordance with ISO/IEC 18013-5 and applicable EUDI Wallet profiles. | High | The wallet can successfully receive, store, and present mVRC credentials in mso_mdoc format. |
| FR-W2C-04 | mVRC (delegated) Data Model Compliance | The wallet SHALL support the standardized mVRC data model and structure as defined by ISO 7367 and the applicable mVRC rulebook. | High | The wallet correctly interprets and processes mVRC (delegated) data elements according to the standardized model and structure. |
| FR-W2C-05 | User Consent | The wallet SHALL require explicit user consent before disclosing any mVRC (delegated) data to a Verifier. | High | No mVRC (delegated) data is shared without an explicit user-approval action. |
| FR-W2C-06 | Key Binding Support | The wallet SHALL support key binding mechanisms to ensure that presented mVRC (delegated) data is cryptographically bound to the wallet instance. | High | Presentations include a valid proof of possession bound to a wallet-controlled key. |
| FR-W2C-07 | Cross-Device and Same-Device Flow | The wallet SHALL support cross-device flows using QR code scanning and same-device flows using deeplinks to initiate authorization requests. | High | Both QR-based and deeplink-based authorization requests can be successfully initiated. |
| FR-W2C-08 | Authorization Request Initialization | The wallet SHALL be able to initialize the OpenID4VP authorization request based on Verifier-provided parameters. | High | The wallet correctly processes and responds to an OpenID4VP authorization request. |
| FR-W2C-09 | Verifier Registration Certificate Handling | The wallet SHALL support processing and validation of Verifier registration certificates. | Medium | Registration certificates are successfully parsed and validated when present. |
| FR-W2C-10 | Verifier Trust Validation | The wallet SHALL verify the trust of the Verifier using registration and access certificates against trusted lists. | High | Presentations proceed only if the Verifier trust check succeeds. |
| FR-W2C-11 | DCQL Credential Sets Support | The wallet SHALL support DCQL credential sets as defined by the Verifier presentation request. | Low | The wallet correctly resolves and processes DCQL credential sets. |
| FR-W2C-12 | DCQL Claim Sets Support | The wallet SHALL support DCQL claim sets to determine which claims are requested for presentation. | Medium | Requested claim sets are correctly interpreted and processed. |
| FR-W2C-13 | DCQL Value Constraints Support | The wallet SHALL support DCQL value constraints when selecting data for presentation. | Medium | Presented data complies with DCQL-defined value constraints. |
| FR-W2C-14 | Selective Disclosure | The wallet SHALL support selective disclosure mechanisms to share only the minimum required mVRC (delegated) data. | High | Only user-approved and requested attributes are included in the presentation. |
| FR-W2C-15 | Data Sharing Preview | The wallet SHALL present the user with a clear preview of the data to be shared, including the Verifier identity and the purpose of data sharing. | High | The user can review requested data, Verifier name, and purpose before consent. |
| FR-W2C-16 | Optional Attribute Selection | The wallet SHALL allow the user to select or deselect optional mVRC (delegated) attributes prior to presentation. | Medium | Optional attributes can be toggled on or off by the user. |
| FR-W2C-17 | VP Token Encryption | The wallet SHALL encrypt the verifiable presentation when using the `direct_post.jwt` response mode. | High | The VP token is transmitted in encrypted form to the Verifier. |
| FR-W2C-18 | Success Screen Presentation | The wallet SHALL display a success screen after a successful mVRC (delegated) data presentation transaction. | Low | A clear success confirmation is shown to the user after completion. |
| FR-W2C-19 | Post-Presentation Redirect | The wallet SHALL support redirection after a successful mVRC (delegated) data presentation, when requested by the Verifier. | Low | The wallet correctly performs a redirect following a successful transaction. |
| FR-W2C-20 | Verifier Metadata Resolution | The wallet SHALL resolve and process Verifier metadata as defined by OpenID4VP to determine supported formats, algorithms, and response modes. | High | The wallet successfully retrieves and applies Verifier metadata during the presentation flow. |
| FR-W2C-21 | Nonce Handling and Replay Protection | The wallet SHALL support nonce handling and include nonce values in verifiable presentations to prevent replay attacks. | High | Presentations include a valid nonce and are rejected if nonce validation fails. |
| FR-W2C-22 | Error Handling and User Feedback | The wallet SHALL handle protocol, trust, and validation errors and present a meaningful error state to the user. | Medium | Errors are correctly detected and a user-readable error message is displayed. |
| FR-W2C-23 | User-Initiated Cancellation | The wallet SHALL allow the user to cancel the presentation process at any time before mVRC (delegated) data disclosure. | Medium | The user can abort the flow and no data is disclosed after cancellation. |
| FR-W2C-24 | Secure Presentation State Handling | The wallet SHALL securely maintain presentation state across redirects or application context switches during the presentation flow. | Medium | The presentation flow can be resumed or safely terminated without data leakage or corruption. |
| FR-W2C-25 | Support mso_mdoc Format | The wallet SHALL support the mso_mdoc credential format for mVRC (delegated) credentials, in accordance with ISO/IEC 18013-5 and applicable EUDI Wallet profiles. | High | The wallet can successfully receive, store, and present mVRC (delegated) credentials in mso_mdoc format. |

**mVRC Verifier (service provider)**

| Index | Requirement Title | Description | Priority | Acceptance Criteria |
|------:|-------------------|-------------|----------|---------------------|
| FR-V2C-01 | Support OpenID4VP | The Verifier SHALL support the OpenID for Verifiable Presentations (OpenID4VP) 1.0 protocol to request and receive mVRC (delegated) presentations. | High | The Verifier successfully completes an OpenID4VP flow with a compliant EUDI Wallet. |
| FR-V2C-02 | HAIP 1.0 Compliance | The Verifier SHALL comply with the High Assurance Interoperability Profile (HAIP) 1.0 requirements applicable to presentation flows. | High | Presentation requests and validation processes meet HAIP-defined assurance requirements. |
| FR-V2C-03 | Support mso_mdoc Format | The Verifier SHALL support verification of mVRC (delegated) presentations using the mso_mdoc credential format, in accordance with ISO/IEC 18013-5 and applicable EUDI Wallet profiles. | High | The Verifier successfully validates mVRC (delegated) presentations in mso_mdoc format. |
| FR-V2C-04 | mVRC (delegated) Data Model Compliance | The Verifier SHALL validate presented mVRC (delegated) data against the standardized mVRC (delegated) data model and structure as defined by ISO 7367 and the applicable mVRC (delegated) rulebook. | High | Presented mVRC (delegated) data is correctly validated against the standardized data model and rejected if non-compliant. |
| FR-V2C-05 | Authorization Endpoint Exposure | The Verifier SHALL expose an Authorization Endpoint to initiate presentation requests in accordance with OpenID4VP. | High | Wallets can initiate presentation flows using the Verifier Authorization Endpoint. |
| FR-V2C-06 | Presentation Query | The Verifier SHALL define and communicate presentation requirements using standardized mechanisms (DCQL). | High | Wallets can correctly interpret requested credential and claim requirements. |
| FR-V2C-07 | DCQL Credential Sets Definition | The Verifier SHALL support DCQL credential sets to specify acceptable mVRC (delegated) credentials. | Low | Wallets can resolve requested DCQL credential sets. |
| FR-V2C-08 | DCQL Claim Sets Definition | The Verifier SHALL support DCQL claim sets to specify required and optional mVRC (delegated) claims. | Medium | Wallets can correctly identify required and optional claims. |
| FR-V2C-09 | DCQL Value Constraints | The Verifier SHALL support DCQL value constraints to restrict acceptable values of requested claims. | Medium | Presented mVRC (delegated) data is validated against DCQL value constraints. |
| FR-V2C-10 | Nonce Generation | The Verifier SHALL generate and provide a nonce to bind the presentation to a specific transaction and prevent replay attacks. | High | Presentations without a valid nonce are rejected. |
| FR-V2C-11 | Direct Post Endpoint Support | The Verifier SHALL support receiving verifiable presentations using the `direct_post.jwt` response mode. | High | The Verifier successfully receives and processes VP tokens via direct_post.jwt mode. |
| FR-V2C-12 | VP Token Decryption | The Verifier SHALL support decryption of encrypted VP tokens when using `direct_post.jwt`. | High | Encrypted VP tokens are successfully decrypted and validated. |
| FR-V2C-13 | Key Binding Validation | The Verifier SHALL validate cryptographic proofs binding the presented mVRC (delegated) data to the wallet-controlled key. | High | Presentations without valid key binding proofs are rejected. |
| FR-V2C-14 | Selective Disclosure Processing | The Verifier SHALL correctly process selectively disclosed mVRC (delegated) data and validate it against the signed credential structure. | High | Selectively disclosed attributes are successfully verified. |
| FR-V2C-15 | User Redirect Handling | The Verifier SHALL support redirecting the user back to a web application or frontend after successful presentation. | High | The user is redirected after successful completion of the presentation flow. |
| FR-V2C-16 | Error Handling | The Verifier SHALL handle protocol, validation, and trust errors and provide appropriate error responses. | High | Errors are returned using standardized error responses and logged for diagnostics. |
| FR-V2C-17 | mVRC (delegated) Seal Validation | The Verifier SHALL validate the cryptographic seal applied to the mVRC (delegated) credential against trusted lists to ensure that the credential was issued by a trusted mVRC (delegated) Issuer. | High | The Verifier successfully validates the mVRC (delegated) seal using trusted list information and rejects credentials with invalid or untrusted seals. |
| FR-V2C-18 | mVRC (delegated) Status Verification | The Verifier SHALL verify the current validity status of the mVRC (delegated) credential using the applicable mVRC (deleagted) status list (e.g. revocation or suspension status). | High | mVRC (delegated) credentials with revoked or suspended status are correctly detected and rejected by the Verifier. |
| FR-V2C-19 | Success Screen Presentation | After successful verification of the mVRC (delegated) presentation, the Verifier SHALL redirect the user and present a success screen displaying the mVRC data that was shared during the verification process. | High | The user is redirected to a success page and can view the mVRC (delegated) data that was disclosed as part of the verification. |
| FR-V2C-20 | Business Process Continuation | After successful mVRC (delegated) verification, the Verifier MAY allow the user to continue the intended business process, such as purchasing ferry tickets, buying an electronic toll vignette, or subscribing to a parking service. | Low | The user can proceed with the business process following successful verification. |
| FR-V2C-21 | Pre-Verification Business Flow | The Verifier MAY support initiating and maintaining the business process context prior to mVRC (delegated) verification, ensuring a seamless transition into the verification flow. | Low | The business process context is preserved when transitioning from the service flow to the mVRC (delegated) verification flow. |

---

#### 8.6.2	Protocol profile

**OpenID4VP**

Specification: OpenID for Verifiable Presentations 1.0  
Profile: High Assurance Interoperability Profile (HAIP) 1.0  

Key characteristics:

- Request/response- based presentation flow using authoriszation requests;
- Support for response mode: direct_post.jwt;
- Credential format: mso_mdoc;
- Support for presentation of the delegated mVRC credentials;
- Support for DCQL presentation requests (credential sets, claim sets and value constraints);
- Selective disclosure of the requested attributes;
- Holder binding using proof-of-possession mechanisms;

Implementation characteristics:

- Supported request schemes: haip-vp, openid4vp, mdoc-openid4vp;
- Authoriszation requests are implemented using JSON Web Token (JAR) by reference;
- Response mode: direct_post.jwt;
- Credential format: mso_mdoc;
- Client identifier prefix type: x509_hash (as defined in HAIP 1.0);
- Use of nonce values to ensure replay protection;
- Support for credential status verification using status lists;

---

#### 8.6.3	Trust and security mechanisms

The scenario relies on a combination of cryptographic and trust mechanisms to ensure secure and reliable presentation and verification of the delegated mVRC data, including:

- Holder binding and proof-of-possession (PoP);
- Client authentication using Client Attestation JWT where applicable;
- Wallet attestation mechanisms, including Wallet Unit Attestation (WUA) and Wallet Instance Attestation (WIA), where used;
- Use of nonce values to prevent replay attacks;
- Encryption of verifiable presentation tokens where required (e.g. direct_post.jwt);
- Validation of verifier trust using registration and access certificates;
- Validation of trust anchors using ETSI Trusted Lists (e.g. ETSI TS 119 612);
- Validation of credential integrity and authenticity, including delegation-related data;
- Validation of issuer signature (mVRC delegated seal);
- Optional verification of credential status using delegated mVRC status lists;

---

#### 8.6.4	Endpoints

**OpenID for Verifiable Presentations (OpenID4VP)**

- Authorisation Endpoint (REQUIRED) - Initiates the presentation flow by requesting a verifiable presentation from the wallet according to a presentation definition.

- POST (REQUIRED) - Receives the verifiable presentation (vp_token) directly from the wallet as the result of the authorisation request.


**Other suggestions for endpoints**

- Init Endpoint (OPTIONAL) - Custom Endpoint for verification initialisation. It is just a proposed solution, it could be something else instead.

- Status Endpoint (OPTIONAL) - Custom endpoint used to retrieve the final status of the credential verification process for UI update purposes. It is just a proposed solution, it could be a websocket endpoint or something else instead.

---

#### 8.5.5	Technical interaction flow – sequence diagrams

The following sequence diagrams illustrate the remote presentation flow for the delegated mVRC in Scenario 2C and show the technical interaction between the EUDI wallet, the mVRC verifier and supporting components.

The diagrams present the main steps involved in requesting, selecting, and securely presenting the delegated mVRC data, including user consent, selective disclosure, and validation of the presented data within a service interaction context.

##### Basic flow
```mermaid
flowchart LR
  subgraph WALLET[Wallet Provider]
    W[EUDI Wallet Instance]
  end

  subgraph VERIFIER[Service provider]
    V[mVRC - delegated Verifier]
  end


  W -->|OpenID4VP| V
```

##### Sequence diagram
```mermaid
sequenceDiagram
  autonumber
  actor U as User
  participant W as EUDI Wallet instance
  participant B as mVRC (delegated) Verifier web app(frontend)
  participant V as mVRC (delegated) Verifier - API (OpenID4VP)


  U->>B: Open Verifier start page
  B->>V: POST /start-session (prepare Auth request)
  V->>B: response with QR Code and deeplink with schema and request_uri
  B->>V: GET Poll verification status (until completed)(with mVRC (delegated) Data)
  V-->>B: http 201 
  loop
  B->>V: poll request
  V->>B: http 200 (Status=PENDING)
  end
  B->>U: Display QR + deep link button (schema with JAR request_uri)

alt Obtain Auth request (cross device or same device flow)
  U->>W: Open EUDI mob app
  W->>B: scan QR code
  B->>W: scan QR code
  else
  U->>B: press deeplink button
  B->>W: invoke EUDI Wallet mob app
 end
  W->>V: JAR request
  V->>W: Authorization request with presentation query (DCQL)
  W->>W: parse and validate Authorization request
  W->>U: Display presentation query
  U->>W: Accept data sahring (user consent)
  W->>W: Prepare VP token(with encryption) and POST request
  W->>V: Send VP token in authorization response
  V->>V: Parse and validate VP token
  B->>V: poll request
  V->>B: http 200 (Status=OK polling ended) with mVRC (delegated) presentation data
  V->>W: http 200 with redirect_uri
  W->>U: present success screen o mobile app
  U->>W: close success screen
alt (cross device or samedevice)
  W->>B: redirect do Verifier succes screen
  B->>U: present success screen with mVRC (delegated) requested data
else
  W->>B: send request GET to redirect_uri
  W->>U: redirect and present Dashboard screen
  B->>U: present success screen with mVRC (delegated) requested data
end
```

---

##### Extended flow
```mermaid
flowchart LR
  subgraph WALLET[Wallet Provider]
    W[EUDI Wallet Instance]
  end
  subgraph VERIFIER[Service provider]
    V[mVRC - delegated Verifier]
  end
  subgraph TRUST[Trust List Provider]
    TL[WRPAC Trusted list]
  end
  subgraph ISSUER[mVRC - delegated Issuer]
    I[mRVC - delegated status list]
  end
  W -->|OpenID4VP| V
  W -->|Get WRPAC trusted list| TL
  V -->|Get WRPAC trusted list| TL
  V -->|Get mVRC - delegated status list| I

```

##### Sequence diagram
```mermaid
sequenceDiagram
  autonumber
  actor U as User
  participant W as EUDI Wallet instance
  participant B as mVRC (delegated) Verifier web app(frontend)
  participant V as mVRC (delegated) Verifier
  participant I as mVRC (delegated) Issuer (status list)
  participant TL as Trusted Lists Provider 


  U->>B: Open Verifier start page
  B->>V: POST /init (prepare Auth request)
  V->>B: response with QR Code and deeplink with schema and request_uri
  B->>V: GET Poll verification status (until completed)(with mVRC (delegated) Data)
  V-->>B: http 201 
  loop
  B->>V: poll request
  V->>B: http 200 (Status=PENDING)
  end
  B->>U: Display QR + deep link button (schema with JAR request_uri)

alt Obtain Auth request (cross device or same device flow)
  U->>W: Open EUDI mob app
  W->>B: scan QR code
  B->>W: scan QR code
  else
  U->>B: press deeplink button
  B->>W: invoke EUDI Wallet mob app
 end
  W->>V: JAR request
  V->>W: Authorization request with presentation query (DCQL)
  W->>W: parse and validate Authorization request
   opt Trust check (optional)
    W->>TL: WRPAC trusted List
    TL->>W: WRPAC trusted List
    W->>W: mVRC (delegated) Verifier access and registration certficate validation &cache Trusted list
  end
  W->>U: Display presentation query
  U->>W: Accept data sharing (user consent)
  W->>W: Prepare VP token(with encryption) and POST request
  W->>V: Send VP token in authorization response
  V->>V: Parse and validate VP token
opt Verifier trust checks (optional)
      V->>TL: WRPAC trusted List
      TL->>V: WRPAC trusted List
      V->>V: mVRC (delegated) seal x5c validation
     end
    opt mVRC (delegated) status list check (optional)
      V->>I: Get mVRC (delegated) status list
      I->>V: JWT/CWT with PID status list
      V->>V: mVRC (delegated) idx validation
    end
  B->>V: poll request
  V->>B: http 200 (Status=OK polling ended) with mVRC (delegated) presentation data
  V->>W: http 200 with redirect_uri
  W->>U: present success screen on mobile app
  U->>W: close success screen
alt (cross device or samedevice)
  W->>B: redirect do Verifier succes screen
  B->>U: present success screen with mVRC (delegated) requested data
else
  W->>B: send request GET to redirect_uri
  W->>U: redirect and present Dashboard screen
  B->>U: present success screen with mVRC (delegated) requested data
end
```

### 8.7 Scenario 2D – mVRC delegation / proximity data sharing

#### 8.7.1	Functional requirements

Scenario 2D is based on ISO/IEC 18013-5 proximity presentation mechanisms and supports proximity presentation of the delegated mVRC data from the EUDI wallet to a proximity verifier enabling selective disclosure and secure offline/online verification via NFC, BLE, or QR codes. The scenario assumes that the delegated mVRC credential has already been issued and is stored in the EUDI wallet.

**EUDI Wallet Instance**

| Index | Requirement Title | Description | Priority | Acceptance Criteria |
|------:|------------------|-------------|----------|---------------------|
| FR-W2D-01 | ISO 18013-5 Compliance | The wallet SHALL support proximity-based presentation of delegated mVRC in accordance with ISO/IEC 18013-5, using BLE for device engagement and secure communication. | High | The wallet successfully establishes a proximity session with a compliant reader and transmits delegated mVRC data. |
| FR-W2D-02 | BLE Peripheral Server Mode Support | The wallet SHALL support Bluetooth Low Energy (BLE) Peripheral Server Mode for proximity-based presentation of delegated mVRC. | High | The wallet operates as a BLE peripheral and supports secure communication with a compliant reader. |
| FR-W2D-03 | BLE Central Client Mode Support | The wallet MAY support BLE Central Client Mode for proximity-based presentation. | Low | If implemented, the wallet can operate as central and establish a session with a compliant reader. |
| FR-W2D-04 | BLE Transport with Optional L2CAP Support | The wallet MAY support BLE L2CAP CoC as an optional transport mechanism. | Medium | If implemented, L2CAP-based communication functions correctly. |
| FR-W2D-05 | Session Encryption Enforcement | The wallet SHALL establish an encrypted session before transmitting delegated mVRC data. | High | No data is transmitted prior to successful secure session establishment. |
| FR-W2D-06 | Support mso_mdoc Format | The wallet SHALL support delegated mVRC credentials in mso_mdoc format. | High | The wallet successfully presents delegated mVRC in mso_mdoc format. |
| FR-W2D-07 | mVRC (delegated) Data Model Compliance | The wallet SHALL support the delegated mVRC data model in accordance with ISO 7367 and the mVRC rulebook. | High | Delegated mVRC data is correctly processed and presented. |
| FR-W2D-08 | User Consent | The wallet SHALL require explicit user consent before disclosing delegated mVRC data. | High | No data is shared without explicit user approval. |
| FR-W2D-09 | Key Binding Support | The wallet SHALL ensure that presented delegated mVRC data is cryptographically bound to the wallet instance. | High | Presented data includes valid binding to a wallet-controlled key. |
| FR-W2D-10 | Device Engagement Support | The wallet SHALL support ISO/IEC 18013-5 device engagement via QR Code and BLE. | High | The wallet successfully initiates or responds to device engagement. |
| FR-W2D-11 | Verifier/Reader Certificate Handling | he wallet SHALL support processing and validation of reader authentication certificates in accordance with ISO/IEC 18013-5. | Medium | Reader certificates are successfully parsed and validated when present. |
| FR-W2D-12 | Verifier/Reader Trust Validation | The wallet SHALL verify the trust of the reader using certificates and trusted lists. | High | resentation proceeds only if the reader trust validation succeeds. |
| FR-W2D-13 | Selective Disclosure | The wallet SHALL support selective disclosure of delegated mVRC data. | High | Only requested and user-approved attributes are shared. |
| FR-W2D-14 | Data Sharing Preview | The wallet SHALL display requested data, verifier identity, and purpose prior to sharing. | High | The user can review data before consent. |
| FR-W2D-15 | Optional Attribute Selection | The wallet SHALL allow selection/deselection of optional attributes. | Medium | Optional attributes can be configured by the user. |
| FR-W2D-16 | Device Authentication Support | The wallet SHALL support device authentication mechanisms as defined in ISO/IEC 18013-5 (e.g. DeviceMAC). | High | The wallet generates a valid DeviceMAC during presentation. |
| FR-W2D-17 | Success Screen Presentation | The wallet SHALL display a success screen after presentation. | Low | A success confirmation is displayed. |
| FR-W2D-18 | Error Handling and User Feedback | The wallet SHALL handle protocol and validation errors. | Medium | Errors are detected and shown to the user. |
| FR-W2D-19 | User-Initiated Cancellation | The wallet SHALL allow cancellation before disclosure. | Medium | The process can be aborted without data sharing. |
| FR-W2D-20 | Optional NFC Device Engagement Support | The wallet MAY support ISO/IEC 18013-5 device engagement using Near Field Communication (NFC) as an alternative proximity transport mechanism. | Low |  If implemented, the wallet can successfully complete device engagement and data exchange over NFC in accordance with ISO/IEC 18013-5. |

**mVRC Proximity Reader**

mVRC Proximity Reader

| Index | Requirement Title | Description | Priority | Acceptance Criteria |
|------:|------------------|-------------|----------|---------------------|
| FR-R2D-01 | ISO 18013-5 Compliance | The Reader SHALL support ISO/IEC 18013-5 proximity sessions for requesting and validating delegated mVRC credentials over Bluetooth Low Energy (BLE). | High | The Reader can successfully establish a proximity session with a compliant wallet and complete device engagement in accordance with ISO/IEC 18013-5. |
| FR-R2D-02 | BLE Central Mode Support | The Reader SHALL support Bluetooth Low Energy (BLE) Central mode when interacting with a wallet acting as Peripheral. | High | The Reader can scan, discover, and connect to a compliant wallet advertising availability. |
| FR-R2D-03 | Optional BLE Peripheral Mode Support | The Reader MAY support BLE Peripheral mode for interoperability scenarios. | Low | If implemented, the Reader can accept connections from a compliant wallet acting as Central. |
| FR-R2D-04 | Session Encryption Enforcement | The Reader SHALL establish and enforce an encrypted session in accordance with ISO/IEC 18013-5 before requesting or receiving any delegated mVRC data. | High | No credential data is accepted before a secure session is successfully established. |
| FR-R2D-05 | mso_mdoc Format Support | The Reader SHALL support parsing and validating mso_mdoc credentials in accordance with ISO/IEC 18013-5 and applicable EUDI Wallet profiles. | High | The Reader successfully parses and processes received delegated mVRC in mso_mdoc format. |
| FR-R2D-06 | Data Model Compliance | The Reader SHALL interpret delegated mVRC data elements in accordance with ISO 7367 and applicable rulebooks. | High | Received attributes are correctly mapped and validated against standardized data models. |
| FR-R2D-07 | Proof-of-Possession Validation | The Reader SHALL verify cryptographic proof-of-possession and holder binding for each received attestation. | High | The Reader rejects presentations where authentication validation fails. |
| FR-R2D-08 | Delegation Validation | The Reader SHALL validate delegation-related data and constraints included in the delegated mVRC. | High | Delegation scope, validity, and constraints are correctly enforced during verification. |
| FR-R2D-09 | mVRC (delegated) Seal Validation | The Reader SHOULD validate the cryptographic seal of the delegated mVRC against trusted lists to ensure issuer trustworthiness. | Medium | Credentials issued by untrusted issuers are rejected. |
| FR-R2D-10 | mVRC (delegated) Status Verification | The Reader SHOULD verify the current validity status of the delegated mVRC credential using status lists where applicable (optional, out of scope of the LSP). | Medium | Revoked or suspended credentials are correctly detected when validation is performed. |
| FR-R2D-11 | Reader Authentication | The Reader SHALL support reader authentication mechanisms in accordance with ISO/IEC 18013-5 where applicable. | High | The Reader presents valid authentication data and is successfully trusted by the wallet. |
| FR-R2D-12 | Replay Protection Validation | The Reader SHALL ensure protection against replay attacks by validating session freshness and cryptographic binding to the active session. | High | Presentations not bound to the active session are rejected. |
| FR-R2D-13 | Error Handling | The Reader SHOULD detect protocol, validation, and trust errors and provide an appropriate system response. | Medium | Invalid or non-compliant presentations are rejected and logged. |
| FR-R2D-14 | Session Termination Handling | The Reader SHALL properly terminate BLE sessions and securely dispose of session keys after completion. | Medium | Session keys are invalidated after session closure. |
| FR-R2D-15 | Optional L2CAP Support | The Reader MAY support BLE L2CAP Connection-Oriented Channels (CoC) as a transport enhancement. | Medium | If implemented, L2CAP CoC sessions function correctly and interoperably. |
| FR-R2D-16 | Success Screen Presentation | After successful verification of the delegated mVRC presentation, the Reader SHALL present a success screen displaying the shared mVRC data. | High | A clear success confirmation is shown to the user after completion. |
| FR-R2D-17 | Device Engagement via QR and BLE | The Reader SHALL support ISO/IEC 18013-5 device engagement using QR Code scanning and Bluetooth Low Energy (BLE) transport. | High | The Reader can scan a QR Code, establish a BLE session, and complete device engagement. |
| FR-R2D-18 | Optional NFC Device Engagement Support | The Reader MAY support ISO/IEC 18013-5 device engagement using Near Field Communication (NFC) as an alternative transport mechanism. | Low | If implemented, the Reader successfully completes NFC-based engagement and data exchange. |
| FR-R2D-19 | Optional Attribute Request Definition | The Reader MAY define the scope and mandatory or optional property of requested mVRC and mDL attributes within a proximity verification session. | Medium | If implemented, the Reader can specify the scope of requested mVRC and mDL attributes or predefined mVRC and mDL data sets, including which attributes are mandatory and which are optional, and the wallet processes the request according to that query. |

---

#### 8.7.2	Protocol profile

**ISO/IEC 18013‑5 / Proximity mdoc**

Specification: ISO/IEC 18013‑5 and ISO/IEC TS 23220  

Key characteristics:
- Device‑to‑device proximity interaction;
- Session establishment using device engagement (e.g. QR code or NFC);
- Use of ephemeral key pairs and session key derivation;
- Encrypted communication channel based on a shared session secret;
- Request/response model for data retrieval;
- Credential format: mso_mdoc;
- Selective disclosure of the requested mVRC (delegated) attributes;
- Holder binding ensured through cryptographic mechanisms and signed mdoc data;
- Support for presentation of the delegated mVRC credentials;

Implementation characteristics:
- Session establishment using QR code or NFC engagement;
- Exchange of reader and device engagement data;
- Use of ephemeral public/private key pairs;
- Session encryption using a derived session secret;
- Transport of requests and responses using DeviceRequest and DeviceResponse structures;
- Signed data payloads using MSO (Mobile Security Object);
- Verification of MSO integrity and signature;
- Support for offline or semi-offline interaction scenarios;

---

#### 8.7.3	Trust and security mechanisms

The scenario relies on a combination of cryptographic and trust mechanisms to ensure secure and reliable proximity presentation and validation of the delegated mVRC data, including:
- Holder binding and proof‑of‑possession (PoP);
- Use of ephemeral keys and session-based encryption to secure communication;
- Validation of credential integrity and authenticity using MSO signatures;
- Certificate path validation of the mdoc document signer;
- Validation of trust anchors using ETSI trusted lists (e.g. ETSI TS 119 612);
- Verification of the delegated credential status using mVRC status;

---

#### 8.7.4	Endpoints

The scenario does not rely on HTTP endpoints. Communication between the EUDI wallet and the proximity reader is performed using ISO/IEC 18013-5 defined proximity communication mechanisms, such as QR code engagement and NFC.

---

#### 8.7.5	Technical interaction flow – sequence diagrams

The following sequence diagram illustrates the proximity presentation flow for Scenario 2D and shows the technical interaction between the consumer's EUDI wallet, the proximity verifier (reader), and the supporting components.

The diagram presents the main steps involved in session establishment, secure data exchange and validation of delegated mVRC data using ISO/IEC 18013‑5 proximity mechanisms, including verification of credential integrity, signature,  and status where applicable.

##### Flow
```mermaid
flowchart LR
  subgraph WALLET[Wallet Provider]
    W[EUDI Wallet Instance]
  end

  subgraph VERIFIER[Service provider]
    V[Delegated mVRC <br /> Proximity Reader]
  end

  W -->|ISO/IEC 18013-5 BLE| V
```

##### Sequence diagram
```mermaid
 sequenceDiagram
    autonumber

    participant ho as Owner (holder)
    participant re as Proximity reader
    participant sl as Status list<br/>server

    %% ===================== Engagement =====================
    re->>re: Generate sessionID
    Note left of re: sessionID is short lived.

    re->>re: Generate ephemeral key pair ReaderKey_pair
    re->>re: Create ReaderEngagement containing ReaderKey_pub

    alt QR Code Engagement (Static/Dynamic)
        re->>ho: Display QR Code
        ho->>ho: Scan QR Code
        ho->>ho: Extract Data
    else NFC Engagement
        ho->>re: Tap (NFC Proximity)
        re->>ho: Transfer Engagement Data via NFC
        ho->>ho: Extract Data
    end
    Note right of ho : Engagement data contains :<br/>• Reader Ephemeral PublicKey(ReaderKey_pub)<br/>• Supported retrieval methods

    ho->>ho: Generate ephemeral key pair DeviceKey_pair
    ho->>ho: Extract ReaderKey_pub
    ho->>ho: Derive session secret session_secret
    ho->>ho: Generate DeviceEngagement containing DeviceKey_pub
    ho-->>re: Send DeviceEngagement
    re->>re: Extract DeviceKey_pub
    re->>re: Derive session secret session_secret

    %% ===================== Data retrieval =====================
    re->>re: Create DeviceRequest containing requested data_req
    re->>re: Encrypt using session_secret
    re->>re: Create SessionData_req containing DeviceRequest_enc

    re-->>ho: Return SessionData_req as response
    ho->>ho: Extract DeviceRequest_enc and decrypt it
    ho->>ho: Extract data_req
    ho->>ho: Create data_res containing requested data
    ho->>ho: Create DeviceResponse containing data_res

    Note right of ho : Signs the requested mdoc data<br/>using the private key matching the MSO

    ho->>ho: Encrypt DeviceResponse using session_secret
    ho->>ho: Encode encrypted DeviceResponse into SessionData_res
    ho->>ho: Create SessionData_res containing DeviceResponse_enc
    ho-->>re: Send SessionData_res

    re->>re: Extract DeviceResponse_enc and decrypt it
    re->>re: Extract data_res
    re->>re: Verify provided data_res

    Note left of re : • Verifies hashes from MSO<br/>• Certificate path validation<br/>• Revocation of doc signer<br/>• Revocation of mDoc

    re->>re: Check validity of MSO
    re->>re: Calculate hash over all hashes
    re->>re: Check signature matches this hash
    re->>re: Check hashes of provided data
    re->>re: Check doc signer is not revoked

    Note left of re : Certificates which are trustworthy are<br/>provided using VICAL files (out of scope).
    
    alt check revocation if data included in mDoc
        re->>re: Extract status list URL and index
        re->>sl: Get status list
        sl-->>re: Return status list
        re->>re: Check bit at index-th position
    end

    %% ===================== Session termination =====================
    re-->>ho: Terminate Session
    ho->>ho: Delete ephemeral keys
    re->>re: Delete ephemeral keys
```

### 8.8 Scenario 3A - mVRC & mDL remote data sharing

#### 8.8.1 Functional requirements

Scenario 3A is based on OpenID4VP 1.0, aligned with the HAIP 1.0, and supports secure and interoperable remote presentation of combined mVRC and mDL credentials from the EUDI wallet to a verifier, within a single transaction.

**EUDI Wallet Instance**

| Index | Requirement Title | Description | Priority | Acceptance Criteria |
|------:|-------------------|-------------|----------|---------------------|
| FR-W3A-01 | Support OpenID4VP | The wallet SHALL support the OpenID for Verifiable Presentations (OpenID4VP) 1.0 protocol for remote presentation of mVRC data. | High | The wallet can successfully complete an OpenID4VP flow with a compliant Verifier. |
| FR-W3A-02 | HAIP 1.0 Compliance | The wallet SHALL comply with the High Assurance Interoperability Profile (HAIP) 1.0 requirements applicable to presentation flows. | High | Presentation flows meet HAIP-defined security and assurance requirements. |
| FR-W3A-03 | Support mso_mdoc Format | The wallet SHALL support the mso_mdoc credential format for mVRC and mDL credentials, in accordance with ISO/IEC 18013-5 and applicable EUDI Wallet profiles. | High | The wallet can successfully receive, store, and present mVRC and mDL credentials in mso_mdoc format. |
| FR-W3A-04 | mVRC and mDL Data Model Compliance | The wallet SHALL support the standardized mVRC and mDL data model and structure as defined by ISO 7367 (mVRC) and ISO 18013-5 (mDL) and the applicable mVRC rulebook. | High | The wallet correctly interprets and processes mVRC and mDL data elements according to the standardized model and structure. |
| FR-W3A-05 | User Consent | The wallet SHALL require explicit user consent before disclosing any mVRC nad mDL data to a Verifier. | High | No mVRC and mDL data is shared without an explicit user-approval action. |
| FR-W3A-06 | Key Binding Support | The wallet SHALL support key binding mechanisms to ensure that presented mVRC and mDL data is cryptographically bound to the wallet instance. | High | Presentations include a valid proof of possession bound to a wallet-controlled key. |
| FR-W3A-07 | Cross-Device and Same-Device Flow | The wallet SHALL support cross-device flows using QR code scanning and same-device flows using deeplinks to initiate authorization requests. | High | Both QR-based and deeplink-based authorization requests can be successfully initiated. |
| FR-W3A-08 | Authorization Request Initialization | The wallet SHALL be able to initialize the OpenID4VP authorization request based on Verifier-provided parameters. | High | The wallet correctly processes and responds to an OpenID4VP authorization request. |
| FR-W3A-09 | Verifier Registration Certificate Handling | The wallet SHALL support processing and validation of Verifier registration certificates. | Medium | Registration certificates are successfully parsed and validated when present. |
| FR-W3A-10 | Verifier Trust Validation | The wallet SHALL verify the trust of the Verifier using registration and access certificates against trusted lists. | High | Presentations proceed only if the Verifier trust check succeeds. |
| FR-W3A-11 | DCQL Credential Sets Support | The wallet SHALL support DCQL credential sets as defined by the Verifier presentation request. | High | The wallet correctly resolves and processes DCQL credential sets. |
| FR-W3A-12 | DCQL Claim Sets Support | The wallet SHALL support DCQL claim sets to determine which claims are requested for presentation. | High | Requested claim sets are correctly interpreted and processed. |
| FR-W3A-13 | DCQL Value Constraints Support | The wallet SHALL support DCQL value constraints when selecting data for presentation. | Medium | Presented data complies with DCQL-defined value constraints. |
| FR-W3A-14 | Selective Disclosure | The wallet SHALL support selective disclosure mechanisms to share only the minimum required mVRC and mDL data. | High | Only user-approved and requested attributes are included in the presentation. |
| FR-W3A-15 | Data Sharing Preview | The wallet SHALL present the user with a clear preview of the data to be shared, including the Verifier identity and the purpose of data sharing. | High | The user can review requested data, Verifier name, and purpose before consent. |
| FR-W3A-16 | Optional Attribute Selection | The wallet SHALL allow the user to select or deselect optional mVRC and mDL attributes prior to presentation. | Medium | Optional attributes can be toggled on or off by the user. |
| FR-W3A-17 | VP Token Encryption | The wallet SHALL encrypt the verifiable presentation when using the `direct_post.jwt` response mode. | High | The VP token is transmitted in encrypted form to the Verifier. |
| FR-W3A-18 | Success Screen Presentation | The wallet SHALL display a success screen after a successful mVRC and mDL data presentation transaction. | Low | A clear success confirmation is shown to the user after completion. |
| FR-W3A-19 | Post-Presentation Redirect | The wallet SHALL support redirection after a successful mVRC and mDL data presentation, when requested by the Verifier. | Low | The wallet correctly performs a redirect following a successful transaction. |
| FR-W3A-20 | Verifier Metadata Resolution | The wallet SHALL resolve and process Verifier metadata as defined by OpenID4VP to determine supported formats, algorithms, and response modes. | High | The wallet successfully retrieves and applies Verifier metadata during the presentation flow. |
| FR-W3A-21 | Nonce Handling and Replay Protection | The wallet SHALL support nonce handling and include nonce values in verifiable presentations to prevent replay attacks. | High | Presentations include a valid nonce and are rejected if nonce validation fails. |
| FR-W3A-22 | Error Handling and User Feedback | The wallet SHALL handle protocol, trust, and validation errors and present a meaningful error state to the user. | Medium | Errors are correctly detected and a user-readable error message is displayed. |
| FR-W3A-23 | User-Initiated Cancellation | The wallet SHALL allow the user to cancel the presentation process at any time before mVRC and mDL data disclosure. | Medium | The user can abort the flow and no data is disclosed after cancellation. |
| FR-W3A-24 | Secure Presentation State Handling | The wallet SHALL securely maintain presentation state across redirects or application context switches during the presentation flow. | Medium | The presentation flow can be resumed or safely terminated without data leakage or corruption. |

**mVRC & mDL Verifier (service provider)**

| Index | Requirement Title | Description | Priority | Acceptance Criteria |
|------:|-------------------|-------------|----------|---------------------|
| FR-V3A-01 | Support OpenID4VP | The Verifier SHALL support the OpenID for Verifiable Presentations (OpenID4VP) 1.0 protocol to request and receive mVRC and mDL presentations. | High | The Verifier successfully completes an OpenID4VP flow with a compliant EUDI Wallet. |
| FR-V3A-02 | HAIP 1.0 Compliance | The Verifier SHALL comply with the High Assurance Interoperability Profile (HAIP) 1.0 requirements applicable to presentation flows. | High | Presentation requests and validation processes meet HAIP-defined assurance requirements. |
| FR-V3A-03 | Support mso_mdoc Format | The Verifier SHALL support verification of mVRC and mDL presentations using the mso_mdoc credential format, in accordance with ISO/IEC 18013-5 and applicable EUDI Wallet profiles. | High | The Verifier successfully validates mVRC and mDL presentations in mso_mdoc format. |
| FR-V3A-04 | mVRC and mDL Data Model Compliance | The Verifier SHALL validate presented mVRC and mDL data against the standardized mVRC data model and structure as defined by ISO 7367 and the applicable mVRC rulebook. | High | Presented mVRC and mDL data is correctly validated against the standardized data model and rejected if non-compliant. |
| FR-V3A-05 | Authorization Endpoint Exposure | The Verifier SHALL expose an Authorization Endpoint to initiate presentation requests in accordance with OpenID4VP. | High | Wallets can initiate presentation flows using the Verifier Authorization Endpoint. |
| FR-V3A-06 | Presentation Query | The Verifier SHALL define and communicate presentation requirements using standardized mechanisms (DCQL). | High | Wallets can correctly interpret requested credential and claim requirements. |
| FR-V3A-07 | DCQL Credential Sets Definition | The Verifier SHALL support DCQL credential sets to specify acceptable mVRC and mDL credentials. | Low | Wallets can resolve requested DCQL credential sets. |
| FR-V3A-08 | DCQL Claim Sets Definition | The Verifier SHALL support DCQL claim sets to specify required and optional mVRC and mDL claims. | Medium | Wallets can correctly identify required and optional claims. |
| FR-V3A-09 | DCQL Value Constraints | The Verifier SHALL support DCQL value constraints to restrict acceptable values of requested claims. | Medium | Presented mVRC and mDL data are validated against DCQL value constraints. |
| FR-V3A-10 | Nonce Generation | The Verifier SHALL generate and provide a nonce to bind the presentation to a specific transaction and prevent replay attacks. | High | Presentations without a valid nonce are rejected. |
| FR-V3A-11 | Direct Post Endpoint Support | The Verifier SHALL support receiving verifiable presentations using the `direct_post.jwt` response mode. | High | The Verifier successfully receives and processes VP tokens via direct_post.jwt mode. |
| FR-V3A-12 | VP Token Decryption | The Verifier SHALL support decryption of encrypted VP tokens when using `direct_post.jwt`. | High | Encrypted VP tokens are successfully decrypted and validated. |
| FR-V3A-13 | Key Binding Validation | The Verifier SHALL validate cryptographic proofs binding the presented mVRC and mDL data to the wallet-controlled key. | High | Presentations without valid key binding proofs are rejected. |
| FR-V3A-14 | Selective Disclosure Processing | The Verifier SHALL correctly process selectively disclosed mVRC and mDL data and validate it against the signed credential structure. | High | Selectively disclosed attributes are successfully verified. |
| FR-V3A-15 | User Redirect Handling | The Verifier SHALL support redirecting the user back to a web application or frontend after successful presentation. | High | The user is redirected after successful completion of the presentation flow. |
| FR-V3A-16 | Error Handling | The Verifier SHALL handle protocol, validation, and trust errors and provide appropriate error responses. | High | Errors are returned using standardized error responses and logged for diagnostics. |
| FR-V3A-17 | mVRC and mDL Seal Validation | The Verifier SHALL validate the cryptographic seal applied to the mVRC and mDL credential against trusted lists to ensure that the credential was issued by a trusted mVRC and mDL Issuer. | High | The Verifier successfully validates the mVRC and mDL seal using trusted list information and rejects credentials with invalid or untrusted seals. |
| FR-V3A-18 | mVRC and mDL Status Verification | The Verifier SHALL verify the current validity status of the mVRC and mDL credential using the applicable mVRC and mDL status list (e.g. revocation or suspension status). | High | mVRC and mDL credentials with revoked or suspended status are correctly detected and rejected by the Verifier. |
| FR-V3A-19 | Success Screen Presentation | After successful verification of the mVRC and mDL presentation, the Verifier SHALL redirect the user and present a success screen displaying the mVRC and mDL data that was shared during the verification process. | High | The user is redirected to a success page and can view the mVRC and mDL data that was disclosed as part of the verification. |
| FR-V3A-20 | Business Process Continuation | After successful mVRC and mDL verification, the Verifier MAY allow the user to continue the intended business process, such as purchasing ferry tickets, buying an electronic toll vignette, or subscribing to a parking service. | Low | The user can proceed with the business process following successful verification. |
| FR-V3A-21 | Pre-Verification Business Flow | The Verifier MAY support initiating and maintaining the business process context prior to mVRC and mDL verification, ensuring a seamless transition into the verification flow. | Low | The business process context is preserved when transitioning from the service flow to the mVRC and mDL verification flow. |

---

#### 8.8.2	Protocol profile

**OpenID4VP**

Specification: OpenID for Verifiable Presentations 1.0
Profile: High Assurance Interoperability Profile (HAIP) 1.0

Key characteristics:

- Request/response based presentation flow using authoriszation requests;
- Support for response mode: direct_post.jwt;
- Credential format: mso_mdoc;
- Selective disclosure of requested attributes;
- Holder binding using proof-of-possession mechanisms;
- Optional use for identity verification (e.g. PID presentation);

Implementation characteristics:

- Supported request schemes: haip-vp, openid4vp, mdoc-openid4vp;
- Authoriszation requests are implemented using JSON Web Token (JAR) by reference;
- Response mode: direct_post.jwt;
- Credential format: mso_mdoc;
- Client identifier prefix type: x509_hash (as defined in HAIP 1.0);
- Use of nonce values to ensure replay protection;
- Support for credential status verification using status lists;

---

#### 8.8.3	Trust and security mechanisms

The scenario relies on a combination of cryptographic and trust mechanisms to ensure secure and reliable remote presentation and verification of mVRC and mDL data, including:

- Holder binding and proof-of-possession (PoP);
- Client authentication using Client Attestation JWT (where applicable);
- Wallet attestation mechanisms, including Wallet Instance Attestation (WIA);
- Use of nonce values to prevent replay attacks;
- Encryption of verifiable presentation tokens where required (e.g. direct_post.jwt);
- Validation of verifier trust using registration and access certificates;
- Validation of trust anchors using ETSI Trusted Lists (e.g. ETSI TS 119 612);
- Validation of credential integrity and authenticity (e.g. mVRC & mDL seal validation);
- Verification of the credential status using mVRC status lists;

---

#### 8.8.4	Endpoints

**OpenID for Verifiable Presentations (OpenID4VP)**

- Authorization Endpoint (REQUIRED) - Initiates the presentation flow by requesting a verifiable presentation from the wallet according to a presentation definition.

- Direct POST (REQUIRED) - Receives the verifiable presentation (vp_token) directly from the wallet as the result of the authorization request.

**Other suggestions for endpoints**

- Init Endpoint (OPTIONAL) - Custom Endpoint for verification initialization - - just a proposed solution, it could be something else instead.
- Status Endpoint (OPTIONAL) - Custom endpoint used to retrieve the final status of the credential verification process for UI update purposes. - just a proposed solution, it could be a websocket endpoint or something else instead.

---

#### 8.8.6	Technical interaction flow – sequence diagrams

##### Basic flow
```mermaid
flowchart LR
  subgraph WALLET[Wallet Provider]
    W[EUDI Wallet Instance]
  end

  subgraph VERIFIER[Service provider]
    V[mVRC & mDL Verifier]
  end


  W -->|OpenID4VP| V
```

##### Sequence diagram
```mermaid
sequenceDiagram
  autonumber
  actor U as User
  participant W as EUDI Wallet instance
  participant B as mVRC & mDL Verifier web app(frontend)
  participant V as mVRC & mDL Verifier - API (OpenID4VP)


  U->>B: Open Verifier start page
  B->>V: POST /start-session (prepare Auth request)
  V->>B: response with QR Code and deeplink with schema and request_uri
  B->>V: GET Poll verification status (until completed)(with mVRC & mDL Data)
  V-->>B: http 201 
  loop
  B->>V: poll request
  V->>B: http 200 (Status=PENDING)
  end
  B->>U: Display QR + deep link button (schema with JAR request_uri)

alt Obtain Auth request (cross device or same device flow)
  U->>W: Open EUDI mob app
  W->>B: scan QR code
  B->>W: scan QR code
  else
  U->>B: press deeplink button
  B->>W: invoke EUDI Wallet mob app
 end
  W->>V: JAR request
  V->>W: Authorization request with presentation query (DCQL)
  W->>W: parse and validate Authorization request
  W->>U: Display presentation query
  U->>W: Accept data sahring (user consent)
  W->>W: Prepare VP token(with encryption) and POST request
  W->>V: Send VP token in authorization response
  V->>V: Parse and validate VP token
  B->>V: poll request
  V->>B: http 200 (Status=OK polling ended) with mVRC and mDL presentation data
  V->>W: http 200 with redirect_uri
  W->>U: present success screen on mobile app
  U->>W: close success screen
alt (cross device or samedevice)
  W->>B: redirect do Verifier succes screen
  B->>U: present success screen with mVRC and mDL requested data
else
  W->>B: send request GET to redirect_uri
  W->>U: redirect and present Dashboard screen
  B->>U: present success screen with mVRC and mDL requested data
end
```

---

##### Extended flow
```mermaid
flowchart LR
  subgraph WALLET[Wallet Provider]
    W[EUDI Wallet Instance]
  end
  subgraph VERIFIER[Service provider]
    V[mVRC & mDL Verifier]
  end
  subgraph TRUST[Trust List Provider]
    TL[WRPAC Trusted list]
  end
  subgraph ISSUER[mVRC Issuer]
    I[mVRC status list]
  end
  subgraph ISSUER2[mDL Issuer]
    I2[mVRC status list]
  end
  W -->|OpenID4VP| V
  W -->|Get WRPAC trusted list| TL
  V -->|Get WRPAC trusted list| TL
  V -->|Get mVRC status list| I
  V -->|Get mDL status list| I2
```

##### Sequence diagram
```mermaid
sequenceDiagram
  autonumber
  actor U as User
  participant W as EUDI Wallet instance
  participant B as mVRC & mDL Verifier web app(frontend)
  participant V as mVRC & mDL Verifier
  participant I as mVRC Issuer (status list)
  participant I2 as mDL Issuer (status list)
  participant TL as Trusted Lists Provider 


  U->>B: Open Verifier start page
  B->>V: POST /init (prepare Auth request)
  V->>B: response with QR Code and deeplink with schema and request_uri
  B->>V: GET Poll verification status (until completed)(with mVRC & mDL Data)
  V-->>B: http 201 
  loop
  B->>V: poll request
  V->>B: http 200 (Status=PENDING)
  end
  B->>U: Display QR + deep link button (schema with JAR request_uri)

alt Obtain Auth request (cross device or same device flow)
  U->>W: Open EUDI mob app
  W->>B: scan QR code
  B->>W: scan QR code
  else
  U->>B: press deeplink button
  B->>W: invoke EUDI Wallet mob app
 end
  W->>V: JAR request
  V->>W: Authorization request with presentation query (DCQL)
  W->>W: parse and validate Authorization request
   opt Trust check (optional)
    W->>TL: WRPAC trusted List
    TL->>W: WRPAC trusted List
    W->>W: mVRC & mDL Verifier access and registration certficate validation &cache Trusted list
  end
  W->>U: Display presentation query
  U->>W: Accept data sharing (user consent)
  W->>W: Prepare VP token(with encryption) and POST request
  W->>V: Send VP token in authorization response
  V->>V: Parse and validate VP token
opt Verifier trust checks (optional)
      V->>TL: WRPAC trusted List
      TL->>V: WRPAC trusted List
      V->>V: mVRC seal x5c validation
      V->>V: mDL seal x5c validation
     end
    opt mVRC status list check (optional)
      V->>I: Get mVRC status list
      I->>V: JWT/CWT with PID status list
      V->>V: mVRC idx validation
    end
    opt mDL status list check (optional)
      V->>I2: Get mDL status list
      I2->>V: JWT/CWT with PID status list
      V->>V: mDL idx validation
    end
  B->>V: poll request
  V->>B: http 200 (Status=OK polling ended) with mVRC & mDL presentation data
  V->>W: http 200 with redirect_uri
  W->>U: present success screen o mobile app
  U->>W: close success screen
alt (cross device or samedevice)
  W->>B: redirect do Verifier succes screen
  B->>U: present success screen with mVRC & mDL requested data
else
  W->>B: send request GET to redirect_uri
  W->>U: redirect and present Dashboard screen
  B->>U: present success screen with mVRC & mDL requested data
end
```

### 8.9 Scenario 3B - mVRC & mDL proximity data sharing

#### 8.9.1	Functional requirements

Scenario 3B is based on ISO/IEC 18013‑5 proximity presentation and supports combined transmission of mVRC and mDL credentials from the EUDI Wallet to a proximity reader.

The scenario enables secure, device-to-device communication using BLE (and optionally NFC) and ensures interoperability through standardized data formats (mso_mdoc), session-based encryption, and trusted validation mechanisms. Both credentials are presented within a single proximity session while being validated independently by the reader.

**EUDI Wallet Instance**

| Index | Requirement Title | Description | Priority | Acceptance Criteria |
|------:|-------------------|-------------|----------|---------------------|
| FR-W3B-01 | ISO 18013-5 Compliance| The wallet SHALL support proximity-based presentation of mVRC and mDL attestations in accordance with ISO/IEC 18013-5, using Bluetooth Low Energy (BLE) for device engagement and secure data transfer. | High | The wallet can successfully establish a proximity session with a compliant reader device over BLE, complete device engagement, and transmit requested mVRC and/or mDL data in compliance with ISO/IEC 18013-5. |
| FR-W3B-02 | BLE Peripheral Server Mode Support| The wallet SHALL support Bluetooth Low Energy (BLE) Peripheral Server Mode for proximity-based presentation of mVRC and mDL attestations in accordance with ISO/IEC 18013-5. | High | The wallet can operate as a BLE peripheral, advertise availability, establish a secure session with a compliant reader acting as central, and successfully transmit requested mVRC and/or mDL data. |
| FR-W3B-03 | BLE Central Client Mode Support| The wallet MAY support Bluetooth Low Energy (BLE) Central Client Mode for proximity-based presentation of mVRC and mDL attestations in accordance with ISO/IEC 18013-5. | Low | If implemented, the wallet can operate as a BLE central device, discover and connect to a compliant reader acting as peripheral, establish a secure session, and transmit requested mVRC and/or mDL data in compliance with ISO/IEC 18013-5. |
| FR-W3B-04 | BLE Transport with Optional L2CAP Support | The wallet MAY support Bluetooth Low Energy L2CAP Connection-Oriented Channels (CoC) as a transport mechanism for enhanced interoperability and performance.| Medium |  If L2CAP CoC is implemented, it functions correctly for proximity data exchange. |
| FR-W3B-05 | Session Encryption Enforcement | The wallet SHALL establish an encrypted session in accordance with ISO/IEC 18013-5 before transmitting any mVRC or mDL data. | High | No mVRC or mDL data is transmitted before a secure session is successfully established. |
| FR-W3B-06 | Support mso_mdoc Format | The wallet SHALL support the mso_mdoc credential format for mVRC and mDL credentials, in accordance with ISO/IEC 18013-5 and applicable EUDI Wallet profiles. | High | The wallet can successfully receive, store, and present mVRC and mDL credentials in mso_mdoc format. |
| FR-W3B-07 | mVRC and mDL Data Model Compliance | The wallet SHALL support the standardized mVRC and mDL data model and structure as defined by ISO 7367 (mVRC) and ISO 18013-5 (mDL) and the applicable mVRC rulebook. | High | The wallet correctly interprets and processes mVRC and mDL data elements according to the standardized model and structure. |
| FR-W3B-08 | User Consent | The wallet SHALL require explicit user consent before disclosing any mVRC nad mDL data to a Verifier. | High | No mVRC and mDL data is shared without an explicit user-approval action. |
| FR-W3B-09 | Combined Presentation Support | The wallet SHALL support the combined presentation of mVRC and mDL attestations within a single ISO/IEC 18013-5 proximity session. | High | When both mVRC and mDL attestations are requested, the wallet transmits both within the same session context, and each attestation can be independently validated by the Verifier as part of one logical verification event.  |
| FR-W3B-10 | Key Binding Support | The wallet SHALL support key binding mechanisms to ensure that presented mVRC and mDL data is cryptographically bound to the wallet instance. | High | Presentations include a valid proof of possession bound to a wallet-controlled key. |
| FR-W3B-11 | Verifier Registration Certificate Handling | The wallet SHALL support processing and validation of Verifier registration certificates. | Medium | Registration certificates are successfully parsed and validated when present. |
| FR-W3B-12 | Verifier Trust Validation | The wallet SHALL verify the trust of the Verifier using registration and access certificates against trusted lists. | High | Presentations proceed only if the Verifier trust check succeeds. |
| FR-W3B-13 | Selective Disclosure | The wallet SHALL support selective disclosure mechanisms to share only the minimum required mVRC and mDL data. | High | Only user-approved and requested attributes are included in the presentation. |
| FR-W3B-14 | Data Sharing Preview | The wallet SHALL present the user with a clear preview of the data to be shared, including the Verifier identity and the purpose of data sharing. | High | The user can review requested data, Verifier name, and purpose before consent. |
| FR-W3B-15 | Optional Attribute Selection | The wallet SHALL allow the user to select or deselect optional mVRC and mDL attributes prior to presentation. | Medium | Optional attributes can be toggled on or off by the user. |
| FR-W3B-16 | Success Screen Presentation | The wallet SHALL display a success screen after a successful mVRC and mDL data presentation transaction. | High | A clear success confirmation is shown to the user after completion. |
| FR-W3B-17 | Error Handling and User Feedback | The wallet SHALL handle protocol, trust, and validation errors and present a meaningful error state to the user. | Medium | Errors are correctly detected and a user-readable error message is displayed. |
| FR-W3B-18 | User-Initiated Cancellation | The wallet SHALL allow the user to cancel the presentation process at any time before mVRC and mDL data disclosure. | Medium | The user can abort the flow and no data is disclosed after cancellation. |
| FR-W3B-20 | Device Engagement via QR and BLE | The wallet SHALL support ISO/IEC 18013-5 device engagement using QR Code initiation and Bluetooth Low Energy (BLE) transport. | High | The wallet can successfully initiate or respond to device engagement using a QR Code and establish a BLE proximity session with a compliant Reader. |
| FR-W3B-21 | Optional NFC Device Engagement Support | The wallet MAY support ISO/IEC 18013-5 device engagement using Near Field Communication (NFC) as an alternative proximity transport mechanism. | Low | If implemented, the wallet can successfully complete device engagement and data exchange over NFC in accordance with ISO/IEC 18013-5. |

**mVRC & mDL proximity Reader**

| Index | Requirement Title | Description | Priority | Acceptance Criteria |
|------:|-------------------|-------------|----------|---------------------|
| FR-R3B-01 | ISO 18013-5 Compliance | The Reader SHALL support ISO/IEC 18013-5 proximity sessions for requesting and validating mVRC and mDL attestations over Bluetooth Low Energy (BLE). | High | The Reader can successfully establish a proximity session with a compliant wallet and complete device engagement in accordance with ISO/IEC 18013-5. |
| FR-R3B-02 | BLE Central Mode Support | The Reader SHALL support Bluetooth Low Energy (BLE) Central mode when interacting with a wallet acting as Peripheral. | High | The Reader can scan, discover, and connect to a compliant wallet advertising availability. |
| FR-R3B-03 | Optional BLE Peripheral Mode Support | The Reader MAY support BLE Peripheral mode for interoperability scenarios. | Low | If implemented, the Reader can accept connections from a compliant wallet acting as Central. |
| FR-R3B-04 | Session Encryption Enforcement | The Reader SHALL establish and enforce an encrypted session in accordance with ISO/IEC 18013-5 before requesting or receiving any mVRC or mDL data. | High | No credential data is accepted before a secure session is successfully established. |
| FR-R3B-05 | mso_mdoc Format Support | The Reader SHALL support parsing and validating mso_mdoc credentials in accordance with ISO/IEC 18013-5 and applicable EUDI Wallet profiles. | High | The Reader successfully parses and processes received mVRC and mDL attestations in mso_mdoc format. |
| FR-R3B-06 | Data Model Compliance | The Reader SHALL interpret mVRC and mDL data elements in accordance with ISO 7367 (mVRC), ISO/IEC 18013-5 (mDL), and applicable rulebooks. | High | Received attributes are correctly mapped and validated against standardized data models. |
| FR-R3B-07 | Combined Presentation Handling | The Reader SHALL support receiving and validating combined presentation of mVRC and mDL attestations within a single ISO/IEC 18013-5 proximity session. | High | When both attestations are received in one session, the Reader validates each independently within one logical verification event. |
| FR-R3B-08 | Proof-of-Possession Validation | The Reader SHALL verify cryptographic proof-of-possession and holder binding for each received attestation. | High | The Reader rejects presentations where proof-of-possession validation fails. |
| FR-R3B-09 | mVRC and mDL Seal Validation | The Reader SHOULD validate the cryptographic seal applied to the mVRC and mDL credential against trusted lists to ensure that the credential was issued by a trusted mVRC and mDL Issuer. | Medium | The Reader successfully validates the mVRC and mDL seal using trusted list information and rejects credentials with invalid or untrusted seals. |
| FR-R3B-10 | mVRC and mDL Status Verification | The Reader SHOULD verify the current validity status of the mVRC and mDL credential using the applicable mVRC and mDL status list (e.g. revocation or suspension status). | Medium | mVRC and mDL credentials with revoked or suspended status are correctly detected and rejected by the Reader. |
| FR-R3B-11 | Reader Authentication | The Reader SHALL support reader authentication mechanisms in accordance with ISO/IEC 18013-5 where applicable. | High | The Reader presents valid reader authentication data and is successfully authenticated by the wallet when required. |
| FR-R3B-12 | Replay Protection Validation |The Reader SHALL ensure protection against replay attacks by validating session freshness and verifying that each mVRC and mDL presentation is cryptographically bound to the active ISO/IEC 18013-5 session. | High | Presentations that are not cryptographically bound to the active session or that reuse prior session parameters are rejected.|
| FR-R3B-13 | Error Handling | The Reader SHOULD detect protocol, validation, and trust errors and provide an appropriate system response. | Medium | Invalid or non-compliant presentations are rejected and logged. |
| FR-R3B-14 | Session Termination Handling | The Reader SHALL properly terminate BLE sessions and securely dispose of session keys after completion. | Medium | Session keys are invalidated after session closure. |
| FR-R3B-15 | Optional L2CAP Support | The Reader MAY support BLE L2CAP Connection-Oriented Channels (CoC) as a transport enhancement. | Medium | If implemented, L2CAP CoC sessions function correctly and interoperably. |
| FR-R3B-16 | Success Screen Presentation | After successful verification of the mVRC and mDL presentation, the Reader SHALL  present a success screen displaying the mVRC and MDL data that was shared during the verification process. | High | A clear success confirmation is shown to the user after completion. |
| FR-R3B-17 | Device Engagement via QR and BLE | The Reader SHALL support ISO/IEC 18013-5 device engagement using QR Code scanning and Bluetooth Low Energy (BLE) transport. | High | The Reader can scan a QR Code, establish a BLE proximity session, and successfully complete device engagement with a compliant wallet. |
| FR-R3B-18 | Optional NFC Device Engagement Support | The Reader MAY support ISO/IEC 18013-5 device engagement using Near Field Communication (NFC) as an alternative proximity transport mechanism. | Low | If implemented, the Reader can successfully complete device engagement and receive credential data over NFC in accordance with ISO/IEC 18013-5. |
| FR-R3B-19 | Optional Attribute Request Definition | The Reader MAY define the scope and mandatory or optional property of requested mVRC and mDL attributes within a proximity verification session. | Medium | If implemented, the Reader can specify the scope of requested mVRC and mDL attributes or predefined mVRC and mDL data sets, including which attributes are mandatory and which are optional, and the wallet processes the request according to that query. |

---

#### 8.9.2	Protocol profile

**ISO/IEC 18013‑5 / Proximity mdoc (BLE)**

Specification: ISO/IEC 18013‑5 and ISO/IEC TS 23220

Key characteristics:

Device‑to‑device proximity interaction using Bluetooth Low Energy (BLE);
Session establishment using device engagement (QR Code required, NFC optional);
Use of ephemeral key pairs and session key derivation;
Encrypted communication channel based on a shared session secret;
Request/response model for data retrieval;
Credential format: mso_mdoc;
Selective disclosure of requested mVRC attributes;
Holder binding ensured through cryptographic mechanisms;
Device authentication based on ISO/IEC 18013‑5 mechanisms (DeviceMac);
Implementation characteristics:

Session establishment using QR code or NFC engagement;
Holder (EUDI Wallet) mode: Peripheral server - required, Client Central - optional;
Supported BLE profile: GATT - reqired, L2CAP - optional;
Secure session establishment based on ephemeral key exchange (ECDH);
Encrypted transport of DeviceRequest and DeviceResponse structures;
Signed data payloads using MSO (Mobile Security Object);
Support for credential status verification using status lists;
Support for offline or semi‑offline interaction scenarios;

---

#### 8.9.3	Trust and security mechanisms

The scenario relies on a combination of cryptographic and trust mechanisms to ensure secure and reliable proximity presentation and validation of combined mVRC & mDL data, including:

- Holder binding and proof‑of‑possession (PoP);
- Use of ephemeral keys and session-based encryption to secure communication;
- Device authentication using ISO/IEC 18013‑5 mechanisms (e.g. DeviceSignature);
- Validation of credential integrity and authenticity (e.g. MSO signature validation);
- Certificate path validation of the mdoc document signer;
- Validation of trust anchors using ETSI Trusted Lists (e.g. ETSI TS 119 612);
- Verification of credential status using mVRC status lists;

---

#### 8.9.4	Endpoints

Proximity interactions do not rely on traditional network endpoints. Communication is performed directly between the EUDI wallet and the reader device using short range communication technologies.

Where applicable, backend services such as status list servers may be queried by the reader during validation.

---

#### 8.9.5	Technical interaction flow – sequence diagrams

The following sequence diagram illustrates the proximity presentation flow for the scenario 3B and shows the technical interaction between the user's EUDI wallet, the reader device and supporting components.

The diagram presents the main steps involved in the establishment of the session, secure data exchange and validation of mVRC data using ISO/IEC 18013 5 proximity mechanisms.

##### Basic flow
```mermaid
flowchart LR
  subgraph WALLET[Wallet Provider]
    W[EUDI Wallet Instance]
  end

  subgraph VERIFIER[Service provider]
    V[mVRC & mDL <br /> Proximity Reader]
  end

  W -->|ISO/IEC 18013-5 BLE| V
```

##### Sequence diagram

```mermaid
sequenceDiagram
    autonumber

    Actor U as EUDI Wallet User
    participant Holder as EUDI Wallet (Peripheral, GATT Server)
    participant Reader as Proximity Reader (Central, GATT Client)
    Actor RU as Proximity Reader User

    rect rgba(230, 230, 230, 0.18)
      Note left of Holder: Initialization
      RU->>Reader: Launch Proximity Reader
 opt
      Reader->>RU: Display Screen wit query presentation definition (list of attributes)
      RU->>Reader: Select and Accept presentation query
 end
      Reader->>Reader: Generate Device request
      Reader->>Reader: Turn on QR Code scanner
      U->>Holder: Open EUDI mob app and start proximity verification proces
      Holder->>Holder: Prepare EDeviceKey + BLE ConnectionMethod
      Holder->>Holder: Render QR Code
    end

    rect rgba(230, 230, 230, 0.18)
      Note left of Holder: Device Engagement (QR Code)
      Reader->>Holder: Scan QR Code
      Holder->>Reader: DeviceEngagement (CBOR): EDeviceKeyBytes + BLE params
      Reader->>Reader: Build SessionTranscript base
      Reader->>Reader: Scan for BLE peripheral advertising mdoc service
      Reader->>Holder: BLE Connect (Central->Peripheral)
      Holder->>Reader: BLE Connect (Peripheral->Central)
      Reader->>Holder: (Opt) Read Ident = SHA-256(EDeviceKeyBytes)
      Reader->>Holder: Enable Notify on State and Server2Client
    end

    rect rgba(230, 230, 230, 0.18)
      Note left of Holder: Start + Session establishment
      Reader->>Holder: Write State=Start (0x01)
      Holder-->>Reader: Notify State=Start (0x01)
      Reader->>Reader: Generate EReaderKey and derive session keys (ECDH)
    loop
      Reader->>Holder: Client2Server: SessionEstablishment (fragmented)
      Holder-->>Reader: Server2Client: SessionEstablishmentAck/status (fragmented)
    end
    end

    rect rgba(230, 230, 230, 0.18)
      Note left of Holder: Data retrieval (encrypted)
        Reader->>Reader: Build + encrypt DeviceRequest (COSE_Encrypt0)
     loop One or more request rounds
        Reader->>Holder: Client2Server: Encrypted DeviceRequest (fragmented)
      end
        Holder->>Holder: Decrypt and parse Device Request
        Holder->>U: Dispaly Device Request with query
        U->>Holder: Accept data sharing
        Holder->>Holder: build + encrypt DeviceResponse
      loop One or more request rounds
        Holder-->>Reader: Server2Client: Encrypted DeviceResponse (fragmented)
      end
        Reader->>Reader: Decrypt + verify response
      end
    rect rgba(230, 230, 230, 0.18)
      Note left of Holder: Termination
      Reader->>Holder: Write State=End (0x02)
      Holder-->>Reader: Notify State=End (0x02)
      Reader->>Holder: Disconnect
      Holder->>Holder: Delete EDeviceKey
      Reader->>Reader: Delete EReaderKey
    end
      rect rgba(230, 230, 230, 0.18)
      Note left of Holder: Finalization
      Holder->>U: Present success screen 
      Reader->>RU: Present success screen with requested mVRC and mDL data
      U->>Holder: Close success screen
      RU->>Reader: Close success screen
    end     
```

---

##### Extended flow
```mermaid
flowchart LR
  subgraph WALLET[Wallet Provider]
    W[EUDI Wallet Instance]
  end
  subgraph VERIFIER[Service provider]
    V[mVRC & mDL Proximity Reader]
  end
  subgraph TRUST[Trust List Provider]
    TL[WRPAC Trusted list]
  end
  subgraph ISSUER[mVRC Issuer]
    I[mVRC status list]
  end
  subgraph ISSUER2[mDL Issuer]
    I2[mVRC status list]
  end
  W -->|ISO/IEC 18013-5 BLE| V
  W -->|Get WRPAC trusted list| TL
  V -->|Get WRPAC trusted list| TL
  V -->|Get mVRC status list| I
  V -->|Get mDL status list| I2
```

##### Sequence diagram

```mermaid
sequenceDiagram
    autonumber

    Actor U as EUDI Wallet User
    participant Holder as EUDI Wallet (Peripheral, GATT Server)
    participant TL as Trusted Lists Provider
    participant I as mVRC Issuer (status list)
    participant I2 as mDL Issuer (status list) 
    participant Reader as Proximity Reader (Central, GATT Client)
    Actor RU as Proximity Reader User

    rect rgba(230, 230, 230, 0.18)
      Note left of Holder: Initialization
      RU->>Reader: Launch Proximity Reader
 opt
      Reader->>RU: Display Screen with query presentation definition (list of attributes)
      RU->>Reader: Select and Accept presentation query
 end
      Reader->>Reader: Generate Device request
      Reader->>Reader: Turn on QR Code scanner
      U->>Holder: Open EUDI mob app and start proximity verification process
      Holder->>Holder: Prepare EDeviceKey + BLE ConnectionMethod
      Holder->>Holder: Render QR Code
    end

    rect rgba(230, 230, 230, 0.18)
      Note left of Holder: Device Engagement (QR Code)
      Reader->>Holder: Scan QR Code
      Holder->>Reader: DeviceEngagement (CBOR): EDeviceKeyBytes + BLE params
      Reader->>Reader: Build SessionTranscript base
      Reader->>Reader: Scan for BLE peripheral advertising mdoc service
      Reader->>Holder: BLE Connect (Central->Peripheral)
      Holder->>Reader: BLE Connect (Peripheral->Central)
      Reader->>Holder: (Opt) Read Ident = SHA-256(EDeviceKeyBytes)
      Reader->>Holder: Enable Notify on State and Server2Client
    end

    rect rgba(230, 230, 230, 0.18)
      Note left of Holder: Start + Session establishment
      Reader->>Holder: Write State=Start (0x01)
      Holder-->>Reader: Notify State=Start (0x01)
      Reader->>Reader: Generate EReaderKey and derive session keys (ECDH)
    loop
      Reader->>Holder: Client2Server: SessionEstablishment (fragmented)
      Holder-->>Reader: Server2Client: SessionEstablishmentAck/status (fragmented)
    end
    end

    rect rgba(230, 230, 230, 0.18)
      Note left of Holder: Data retrieval (encrypted)
        Reader->>Reader: Build + encrypt DeviceRequest (COSE_Encrypt0)
     loop One or more request rounds
        Reader->>Holder: Client2Server: Encrypted DeviceRequest (fragmented)
      end
        Holder->>Holder: Decrypt and parse Device Request
        opt Trust check (optional)
    Holder->>TL: WRPAC trusted List
    TL->>Holder: WRPAC trusted List
    Holder->>Holder: mVRC & mDL Verifier access and registration certficate validation &cache Trusted list
  end
        Holder->>U: Display Device Request with query
        U->>Holder: Accept data sharing
        Holder->>Holder: build + encrypt DeviceResponse
      loop One or more request rounds
        Holder-->>Reader: Server2Client: Encrypted DeviceResponse (fragmented)
      end
        Reader->>Reader: Decrypt + verify response
opt Reader trust checks (optional)
      Reader->>TL: WRPAC trusted List
      TL->>Reader: WRPAC trusted List
      Reader->>Reader: mVRC seal x5c validation
      Reader->>Reader: mDL seal x5c validation
     end
    opt mVRC status list check (optional)
      Reader->>I: Get mVRC status list
      I->>Reader: JWT/CWT with PID status list
      Reader->>Reader: mVRC idx validation
    end
    opt mDL status list check (optional)
      Reader->>I2: Get mDL status list
      I2->>Reader: JWT/CWT with PID status list
      Reader->>Reader: mDL idx validation
    end
      end
    rect rgba(230, 230, 230, 0.18)
      Note left of Holder: Termination
      Reader->>Holder: Write State=End (0x02)
      Holder-->>Reader: Notify State=End (0x02)
      Reader->>Holder: Disconnect
      Holder->>Holder: Delete EDeviceKey
      Reader->>Reader: Delete EReaderKey
    end
      rect rgba(230, 230, 230, 0.18)
      Note left of Holder: Finalization
      Holder->>U: Present success screen 
      Reader->>RU: Present success screen with requested mVRC i mDL data
      U->>Holder: Close success screen
      RU->>Reader: Close success screen
    end     
```

### 9 Implementation assumptions for the scenarios

The following implementation assumptions apply to all scenarios, wher applicable, and define common operational conditions for interoperability testing within the LSP. These assumptions complement the functional requirements and ensure consistency across remote and proximity presentation flows.

#### Wallet provider

The wallet is assumed to already contain valid credentials (e.g. mVRC, delegated mVRC, and where applicable mDL) prior to the initiation of presentation flows, except for dedicated negative or false‑positive test scenarios;

The wallet provider is expected to ensure availability of test user data, including at least a minimal agreed set of test users where required for issuance scenarios, and to maintain consistency of the test dataset throughout the agreed interoperability testing cycle;

Where WUA status validation is part of the test scenario, the wallet provider should ensure that the relevant WUA status list is available to the mVRC issuer during interoperability testing and that the wallet instances used in the agreed test set can be validated against that status information.

The wallet is expected to support both remote and proximity presentation mechanisms, including:
- OpenID4VP remote presentation flows (QR code and same-device/deeplink initiation),
- ISO/IEC 18013‑5 proximity interactions (QR code and optionally NFC),
depending on the scenario;

The wallet SHALL support combined presentation of multiple credentials where required (e.g. mVRC and mDL) and ensure correct construction of presentations according to the requested scope;

The wallet is expected to correctly process presentation requests, including DCQL-based queries, and construct valid verifiable presentations aligned with the requested credential sets and attribute constraints;

The wallet SHALL enforce explicit user consent prior to any data disclosure and provide clear data sharing preview, including requested attributes and verifier context;

The wallet is expected to support selective disclosure of credential data, including user-controlled selection of optional attributes where applicable;

The wallet SHALL support cryptographic mechanisms required for secure presentation, including:
- proof-of-possession and key binding (remote flows),
- session security and DeviceMAC (proximity flows),
- encryption of verifiable presentations (e.g. direct_post.jwt);

The wallet is expected to support replay protection mechanisms (e.g. nonce handling, session binding);

The wallet SHALL support secure handling of session or presentation lifecycle, including:
- maintenance of presentation state across redirects or context changes (remote flows),
- generation and secure disposal of ephemeral keys (proximity flows);

The wallet is expected to ensure a consistent and user-friendly experience across all flows, including clear indication of presented credentials and their origin;

Supporting libraries or reusable software components may be provided within the LSP environment. Where such artefacts are provided, they should be made available through the project repository and maintained for the duration of implementation and testing activities;

Where Digital Credentials API (DC API) is implemented, Chrome is assumed to be the primary browser for initial implementation and interoperability testing. Support for additional browsers or user agents may be introduced at later stages;

The wallet is not required to support all possible combinations of credentials and attributes but SHALL support the combinations defined for the agreed interoperability testing scenarios;

#### mVRC issuer / delegated mVRC issuer

For the purpose of interoperability testing, the mVRC issuer may use fictional or pre-configured data sources, either as a standalone setup or in combination with integration to a vehicle registry;

The mVRC issuer is expected to maintain a predefined set of test users and associate each user with a predefined vehicle dataset, unless otherwise agreed for specific test cases;

Where PID-based identity verification is implemented, the dataset associated with each test user SHALL be validated against attributes provided in the PID (e.g. given name and family name);

Where PID-based identity verification is not implemented, the mapping between wallet test users and corresponding vehicle datasets SHALL be agreed in advance between the wallet provider and the mVRC issuer;

Where scenarios involve delegation, the issuer is expected to:
- support definition and enforcement of delegation scope and validity;
- maintain linkage between the original credential holder and the delegated credential;
- validate delegation permissions (including authenticity, integrity, and constraints);
- ensure subject binding between the delegated credential and the recipient;

The issuer SHALL support issuance flows in accordance with OpenID4VCI where applicable, including Authorisation Code Flow with Issuer Attestation (IAE) and integration with OpenID4VP where required for identity or permission verification;

The issuer is expected to generate and sign issued credentials (including delegated mVRC) using X.509 certificates, with a trust chain anchored to an agreed trust anchor;

The issuer is expected to maintain a registry or internal record of issued credentials (including delegated credentials), sufficient to support issuance tracking and optional lifecycle management;

If the scope includes testing the lifecycle of attestations, the mVRC issuer is expected to provide a mechanism that allows the status of an issued mVRC to be changed in order to simulate its invalidity;

The issuer is expected to provide a mechanism enabling the issuance initiation interface (e.g. QR code or deep link) to reflect the progress of the issuance session (e.g. via polling, WebSocket, or an equivalent approach);

The issuer infrastructure is not required to be permanently publicly accessible, but it SHALL be network-accessible to participating wallet implementations during agreed interoperability testing windows;

Any connectivity constraints (e.g. firewalls, IP allowlisting, VPN requirements, proxy configurations, or TLS filtering) SHALL be identified and resolved in advance of interoperability testing;

Supporting libraries or reusable software components may be provided within the LSP environment. Where such artefacts are provided, they should be made available through the project repository and maintained for the duration of the implementation and testing activities;

#### mVRC remote verifier / mVRC & mDL remote verifier

The verifier is responsible for defining the scope of data requested for presentation. Where verifier registration certificates are supported by both transaction parties, the requested scope is expected to correspond to the scope declared in the certificate, except for dedicated negative or false-positive test cases;

The verifier is expected to define presentation requests using standardised mechanisms (e.g. DCQL), including credential sets, claim sets, and value constraints, where applicable;

The verifier shall support OpenID4VP presentation flows and processing of verifiable presentations, including:
- handling of QR code-based and same-device (deeplink) initiation;
- decryption and validation of verifiable presentation tokens (e.g. direct_post.jwt);
- support for combined presentation of multiple credentials (e.g. mVRC and mDL) where required;

The verifier is expected to provide a mechanism enabling the verification initiation page to reflect the progress of the presentation session after QR code or deep link generation. Polling, WebSocket, or an equivalent mechanism may be used;

In combined presentation scenarios (group 3) the verifier shall ensure that multiple credentials presented within a single transaction are processed in a consistent manner, while allowing independent validation of each credential where required;

The verifier infrastructure is not required to be permanently publicly accessible, but it SHALL be reachable by participating wallet implementations during agreed interoperability testing windows;

Any connectivity constraints (e.g. firewalls, IP allowlisting, VPN requirements, proxy configurations, or TLS-related filtering) SHALL be identified and resolved in advance of interoperability testing;

Where credential trust validation is performed, the verifier is expected to validate:
- verifier registration and/or access certificates (where applicable);
- trust anchors (e.g. ETSI Trusted Lists);
- credential integrity and authenticity (e.g. mVRC and mDL seals);

The distribution model for verifier registration certificates and access certificates is not yet defined. It is assumed that the approach will be agreed among participating parties prior to interoperability testing, and that the certificates will most likely be provisioned through WP2;

Supporting libraries or reusable software components may be provided within the LSP environment (e.g. via WP2). Where such artefacts are provided, they should be made available through the project repository and maintained for the duration of implementation and testing activities;

Where Digital Credentials API (DC API) is implemented, Chrome is assumed to be the primary browser for initial implementation and interoperability testing. Support for additional browsers or user agents may be introduced at later stages;

#### mVRC proximity reader / mVRC & mDL proximity reader

The reader device is assumed to support proximity interactions in accordance with ISO/IEC 18013‑5;

The reader SHALL support device engagement mechanisms, including QR code-based initiation and MAY support NFC as an alternative transport mechanism;

The reader is expected to generate, present, or process engagement data (e.g. QR code or NFC exchange) required to establish a proximity session with the wallet;

The reader SHALL be capable of establishing a secure communication session using ephemeral key exchange (e.g. ECDH), deriving a shared session secret, and maintaining an encrypted communication channel;

The reader is expected to support session lifecycle management, including secure establishment, maintenance, and termination of proximity sessions;

The reader SHALL support processing of ISO/IEC 18013‑5 data structures (e.g. DeviceRequest and DeviceResponse) and extraction of credential data;

Where applicable, the reader SHALL support validation of delegated mVRC credentials;

The reader SHALL support cryptographic mechanisms for device authentication and session binding (e.g. DeviceMAC) to ensure that presented data is bound to the active session;

The reader is expected to support selective disclosure processing and correctly interpret requested and returned data elements;

Where applicable, the reader MAY access trusted list services (e.g. ETSI Trusted Lists) to validate trust anchors and issuer certificates;

Where applicable, the reader MAY access credential status list services (e.g. revocation or suspension status);

The reader is expected to handle both single-credential and multi-credential scenarios (e.g. combined mVRC and mDL presentation), ensuring consistent processing and independent validation of each credential;

The reader infrastructure (where applicable, e.g. for logging or integration) does not need to be permanently publicly accessible but SHALL be operationally available for interoperability testing scenarios;

Supporting libraries, or reusable software components may be provided within the LSP environment (e.g. via WP2). Where such artefacts are provided, they should be made available through the project repository and maintained for the duration of implementation and testing activities;

## 10 Scope, Challenges and Concluding Remarks


The WP5 APTITUDE for mVRC is conducted in a diverse and evolving ecosystem, bringing together multiple Member states, wallet providers, issuers and service providers operating at different levels of technical maturity and practical experience. This diversity, while fundamental to the value of the pilot, naturally introduces a number of challenges. Participating countries and organisations are at different stages of development of their digital services, identity ecosystems and wallet solutions, which impacts both integration readiness and the level of alignment in implementation approaches.
In addition, the pilot operates within a structured interoperability framework that relies on defined standards and data formats. While this is necessary to ensure consistency across participants, it also introduces certain constraints. For example, the use of the mso_mdoc format as the primary representation for credentials differs from other approaches such as SD-JWT-based credentials, which may offer greater flexibility in certain contexts. As a result, participants must align not only on protocols, but also on specific data models and encoding approaches, which can lead to differences in interpretation and implementation.
At the same time, operating in a cross-border environment requires alignment of trust models, certificate handling mechanisms and interoperability assumptions across jurisdictions. These aspects become particularly visible when solutions developed in different Member states interact with each other. Finally, the breadth of tested scenarios – including remote and proximity presentation, as well as delegation – adds further complexity, as these capabilities need to be validated across multiple technical setups and business contexts.
Despite these challenges, the LSP provides a uniquely valuable opportunity to prepare the mVRC ecosystem for future production deployment. By operating in a controlled and secure environment, the pilot allows stakeholders to test a wide range of scenarios, identify interoperability issues at an early stage and gain practical experience without impacting real users or production systems. The use of synthetic or pre-configured datasets ensures a high level of data protection while still enabling simulation of complex and non-standard situations that would be difficult to test using real data.
The key strength of the pilot lies in its cross-border dimension. Testing scenarios in which wallets, issuers and verifiers originate from different Member states provides practical insight into how standards are interpreted and applied in real implementations. This helps identify gaps, inconsistencies and dependencies early, giving stakeholders more time to adapt and align their solutions. The pilot also demonstrates the flexibility of the mVRC concept across a wide range of business-agnostic use cases, including vehicle rental, leasing, family delegation, corporate fleet usage, access to restricted urban zones, tolling, parking or transport-related services. In many of these contexts, the combined presentation of multiple credentials – in particular mVRC and mDL within a single transaction – is expected to reflect real-life requirements.
Within this framework, the scope of the WP5 is intentionally focused on validating the core functional capabilities of the mVRC ecosystem in a cross-border context. In particular, the pilot concentrates on issuance, presentation – both remote and proximity – and delegation of credentials, which together form the foundation of all defined scenarios and represent the most relevant interactions from both a technical and business perspective.
The revocation, on the other hand, is addressed only to the extent necessary to support verification of credential status during presentation, primarily through the use of status list mechanisms. This allows participants to validate how credential validity is interpreted at the point of use, without introducing additional complexity related to the lifecycle management. The mechanisms by which issuers update, publish or maintain status information remain outside the scope of the pilot and are left to national implementations and organisational practices.
At the same time, reissuance, live updates or modification of existing credentials, is explicitly excluded from the pilot scope. This reflects a deliberate sequencing approach, where the focus is placed on establishing stable and interoperable foundations before introducing additional complexity and more advanced lifecycle capabilities.
The pilot is not intended to replicate full production environments, but rather to provide a structured and pragmatic testing framework that allows participants to validate assumptions, identify integration gaps and better understand dependencies between components. It supports gradual alignment across stakeholders while preserving flexibility for national implementations and differing levels of system maturity.
In conclusion, the Large Scale Pilot represents a critical step towards the future deployment of mVRC in the European Union. By enabling structured validation of key capabilities in a cross-border setting, it contributes to the broader objectives of digital transformation, interoperability and simplification of services for citizens and businesses. The pilot builds on existing European regulations, standards and best practices, supporting the ongoing effort to digitalise services and improve user experience across Member states. Its outcomes will provide valuable input for future implementations and help ensure that mVRC can be deployed in a robust, interoperable and scalable way across the EU.

### 10.1 Within our scope
### 10.2 Beyond our scope

# Annex 1 Rulebook
# Annex 2 Roles in the scenarios

### SCENARIO 1A – mVRC issuance

| Country | Wallet provider | mVRC issuer (EAA provider) |
|---------|-------------------------------|--------------------------------------------------|
| **AT** |  |  |
| **CZ** | Aricoma / DIA |  |
| **DE** |  |  |
| **FR** | France Identité (France Titres - ANTS)  | France Identité (France Titres - ANTS)  |
| **GR** |  |  |
| **LT** |  | Regitra | 
| **LV** |  | CSDD (Road Traffic Safety Directorate) |
| **NL** | Ministry of the Interior and Kingdom Relations(BZK) | RDW (The Netherlands Vehicle Authority) |
| **PL** | COI | COI |
| **PT** | ARTE (Agência para a Reforma Tecnológica do Estado, I.P.) | Instituto dos Registos e do Notariado |
| **UA** | SE Diia | SE Diia |


### SCENARIO 1B – mVRC remote data sharing

| Country | Wallet provider | Relying Party (remote verifier) |
|---------|-------------------------------|--------------------------------------------------|
| **AT** |  |  |
| **CZ** | Aricoma / DIA | |
| **DE** |  |  |
| **FR** | IN Groupe / France Identité (France Titres - ANTS)  | IN Groupe / Thales / iDAKTO |
| **GR** | <span style="color:red">GRNET</span> | <span style="color:red">UAegean / CFF</span> |
| **LT** |  |  | 
| **LV** |  |  |
| **NL** | Ministry of the Interior and Kingdom Relations | City of Amsterdam  |
| **PL** | COI | COI |
| **PT** | ARTE (Agência para a Reforma Tecnológica do Estado, I.P.) | Instituto dos Registos e do Notariado |
| **UA** | SE Diia | SE Diia |

_! RDW (The Netherlands Vehicle Authority) / CSDD (Road Traffic Safety Directorate) - please confirm your roles._


### SCENARIO 1C – mVRC proximity data sharing

| Country | Wallet provider | Relying Party (proximity verifier) |
|---------|-------------------------------|--------------------------------------------------|
| **AT** | youniqx Identity AG |  |
| **CZ** | Aricoma / DIA | |
| **DE** | BDR / BMV (Federal Ministry of Transport) |  |
| **FR** | IN Groupe / France Identité (France Titres - ANTS) | IN Groupe / France Identité (France Titres - ANTS) / iDAKTO |
| **GR** | <span style="color:red">GRNET</span> | <span style="color:red">UAegean / CFF</span> |
| **LT** |  |  | 
| **LV** |  |  |
| **NL** | Ministry of the Interior and Kingdom Relations | City of Amsterdam |
| **PL** | COI | COI |
| **PT** | ARTE (Agência para a Reforma Tecnológica do Estado, I.P.) | 	Instituto dos Registos e do Notariado |
| **UA** | SE Diia |  |

_! RDW (The Netherlands Vehicle Authority) / CSDD (Road Traffic Safety Directorate)- please confirm your roles._


### SCENARIO 2A – delegated mVRC issuance (w2w)

| Country | Wallet provider | mVRC issuer (EAA provider) |
|---------|-------------------------------|--------------------------------------------------|
| **AT** | youniqx Identity AG |  |
| **CZ** |  |  |
| **DE** |  |  |
| **FR** |  |  |
| **GR** |  |  |
| **LT** |  |  |
| **LV** |  | CSDD (Road Traffic Safety Directorate) |
| **NL** |  | RDW (The Netherlands Vehicle Authority) |
| **PL** | COI | COI |
| **PT** | ARTE (Agência para a Reforma Tecnológica do Estado, I.P.) | Instituto dos Registos e do Notariado |
| **UA** | SE Diia | SE Diia |

_!Two wallets will be required, reflecting two distinct roles; one wallet holds an mVRC attestation and another one from a different member state receives the delegated mVRC._

### SCENARIO 2B – delegated mVRC issuance (o2w)

| Country | Wallet provider | mVRC issuer (EAA provider) | proxy mVRC issuer (organisation) - delegation permission |
|---------|-------------------------------|--------------------------------------------------|--------------------------------------------------|
| **AT** |  |  |  |
| **CZ** |  |  |  |
| **DE** |  |  |  |
| **FR** | IN Groupe |  | Renault (Orange Business / Thales) |
| **GR** |  |  |  |
| **LT** |  |  |  |
| **LV** |  | CSDD (Road Traffic Safety Directorate) |  |
| **NL** |  |  |  |
| **PL** | COI | COI | PKO Leasing |
| **PT** | ARTE (Agência para a Reforma Tecnológica do Estado, I.P.) | Instituto dos Registos e do Notariado |  |
| **UA** |  |  |  |


### SCENARIO 2C – mVRC delegation / remote data sharing

| Country | Wallet provider | Relying Party (remote verifier) |
|---------|-------------------------------|--------------------------------------------------|
| **AT** |  |  |
| **CZ** |  |  |
| **DE** |  |  |
| **FR** | IN Groupe |  |
| **GR** | <span style="color:red">GRNET</span> | UAegean |
| **LT** |  |  | 
| **LV** |  |  |
| **NL** |  |  |
| **PL** | COI | COI |
| **PT** | ARTE (Agência para a Reforma Tecnológica do Estado, I.P.) | Instituto dos Registos e do Notariado |
| **UA** | SE Diia |  |


### SCENARIO 2D – mVRC delegation / proximity data sharing

| Country | Wallet provider | Relying Party (proximity verifier) |
|---------|-------------------------------|--------------------------------------------------|
| **AT** | youniqx Identity AG |  |
| **CZ** |  |  |
| **DE** | BDR / BMV (Federal Ministry of Transport)</span> |  |
| **FR** | IN Groupe | IN Groupe / Thales |
| **GR** | <span style="color:red">GRNET</span> | UAegean |
| **LT** |  |  | 
| **LV** |  |  |
| **NL** |  |  |
| **PL** | COI | COI |
| **PT** | ARTE (Agência para a Reforma Tecnológica do Estado, I.P.) | Instituto dos Registos e do Notariado |
| **UA** |  |  |


### SCENARIO 3A – mVRC & mDL remote data sharing

| Country | Wallet provider | Relying Party (remote verifier) |
|---------|-------------------------------|--------------------------------------------------|
| **AT** |  |  |
| **CZ** |  |  |
| **DE** |  |  |
| **FR** |  |  |
| **GR** |  |  |
| **LT** |  |  | 
| **LV** |  |  |
| **NL** |  |  |
| **PL** | COI | COI |
| **PT** |  |  |
| **UA** |  |  |


### SCENARIO 3B – mVRC & mDL proximity data sharing

| Country | Wallet provider | Relying Party (proximity verifier) |
|---------|-------------------------------|--------------------------------------------------|
| **AT** |  |  |
| **CZ** |  |  |
| **DE** |  |  |
| **FR** |  |  |
| **GR** |  |  |
| **LT** |  |  | 
| **LV** |  |  |
| **NL** |  |  |
| **PL** | COI | COI |
| **PT** |  |  |
| **UA** |  |  |

# Annex 3 Delegation scenarios concepts

### Scenario 2A – Delegated mVRC issuance (w2w)

**Concept 1 – Centralised delegation (owner-initiated)**

The vehicle owner initiates the delegation process through the mVRC issuer’s web application, where the scope of the delegated vehicle privileges and the validity period are defined. In order to prove their entitlement, the vehicle owner presents their source mVRC and an identity credential (e.g. mDL or PID) using an OpenID4VP flow.

Following successful verification, the issuer generates issuance initiation data, which is shared with the consumer (delegated user) in the form of a QR code. This QR code (without a deep link) is displayed on the vehicle owner’s device and scanned by the consumer using their EUDI wallet. After scanning the QR code, the consumer’s wallet initiates an OpenID4VCI authorised code flow with support for the Interactive Authorisation Endpoint (IAE). As part of this process, the delegated user may be required to present their own identity credential.

The mVRC issuer then generates and signs the delegated mVRC using its X.509 certificate, with the trust chain anchored to the designated trust anchor. The delegated mVRC includes the defined vehicle privileges, the consumer’s personal data, and the established validity period. Finally, the delegated mVRC is securely delivered to and stored in the consumer’s wallet.
 
**Concept 2 – Decentralised delegation (wallet‑issued permission)**

The delegation process introduces an additional step in which the vehicle owner’s wallet generates a dedicated authorisation credential (mVRC Delegation Permission) that is transferred directly to the delegated user using proximity communication.

The vehicle owner selects the vehicle within the wallet and defines the scope of delegated vehicle privileges and the validity period. As part of the delegation initiation, the consumer (delegated user) is verified locally through the presentation of their identity credential (e.g. mDL or PID) using a proximity interaction (e.g. BLE).

Following the successful local verification, the vehicle owner’s wallet generates and issues the mVRC Delegation Permission. This credential contains the defined scope of the delegated privileges, the validity period, and the relevant consumer - data. It is cryptographically signed using the key associated with the vehicle owner’s wallet and transferred to the delegated user via proximity communication.

The delegated user initiates the delegated mVRC issuance process through the official mVRC issuer’s web service, thereby starting an OpenID4VCI authorisation with support for the Interactive Authorisation Endpoint (IAE). As part of this process, the consumer presents their identity credential together with the received mVRC Delegation Permission. The mVRC issuer validates the presented attestations, verifies data consistency, and trust (including signature validation), and issues the delegated mVRC with the established personal data, validity period, and delegated privileges. Finally, the delegated mVRC is delivered to and securely stored in the delegated user’s wallet.
 
---
Based on the feedback from the consortium members and analysis of implementation complexity and operational feasibility, **concept 1** was selected for this scenario. It provides a simpler and more realistic architecture, ensures centralised control over the issuance process and aligns more closely with existing issuance models and trust frameworks.

### Scenario 2B – Delegated mVRC issuance (o2w)

**Concept 1 – Organisation-issued delegated mVRC**

The delegation process is fully managed by the organisation, which issues and signs the final delegated mVRC credential after verifying the identity of the consumer.

After completing all business formalities (e.g. rental agreement), the consumer accesses the organisation’s web application to initiate the delegated mVRC issuance process. The rental period and the scope of delegated vehicle privileges are already defined as part of the business process. A QR code is generated to initiate the VP process. The user presents their driving license (VP) to the organisation. After successful VP verification, the user is redirected to initiate the issuance using the pre-authorised code flow, continuing the process on the same mobile device (same-device flow). The organisation then generates and signs the delegated mVRC using its X.509 certificate, with the trust chain anchored to the designated trust anchor. The credential includes the defined vehicle privileges, the consumer’s personal data, and the established validity period derived from the business agreement.

Finally, the delegated mVRC is delivered to and securely stored in the consumer’s wallet.
 
**Concept 2 – Centralised issuance based on the delegation permission**

The delegation process is split into two steps, introducing an intermediate authorisation credential (mVRC delegation permission) issued by the organisation and a final delegated mVRC issued by the official mVRC issuer.

After completing the business formalities (e.g. rental agreement), the consumer accesses the organisation’s web application to initiate the delegation process. The rental period and the scope of the delegated vehicle privileges are already defined based on the business agreement. A QR code is generated to initiate the VP process. The consumer presents their driving licence (VO) to the organisation for identity verification. Following successful verification, the consumer is redirected to initiate the issuance process using the pre-authorised code flow, continuing their mobile device (same-device flow).

The organisation generates and signs the mVRC delegation permission using its X.509 certificate with the trust chain anchored to the designated trust anchor and the consumer receives the mVRC delegation permission in their wallet.

The consumer’s wallet initiates the delegated mVRC issuance process via the official and dedicated mVRC issuer service (through the issuer’s web application). This triggers a flow where the consumer presents the mVRC delegation permission as proof of authorisation together with their mDL as proof of identity. Following the successful verification, the user is redirected to the OpenID4VCI pre-authorised code flow to complete the delegated mVRC issuance process. The mVRC issuer generates and signs the delegated mVRC using its X.509 certificate, with the trust chain anchored to the designated trust anchor. The issued credential contains the delegated vehicle privileges, the consumer’s personal data, and the established validity period.

Finally, the delegated mVRC is delivered and securely stored in the consumer’s wallet.
 
---
Based on feedback from the consortium, **concept 2** was selected for this scenario. It aligns more closely with existing regulatory and operational models, ensures centralised control of credential issuance, and reduces the requirements placed on organisations, which may not be authorised to issue regulated vehicle credentials directly.


