# Access Control Policy

> **Document control**  
> Owner: [POLICY_OWNER_ROLE, e.g. Information Security Officer]  
> Approved by: [APPROVER_NAME_AND_ROLE]  
> Version: [VERSION]  
> Effective date: [EFFECTIVE_DATE]  
> Next review: [NEXT_REVIEW_DATE]

## 1. Legal/Regulatory Basis

ISO/IEC 27001:2022 / ISO/IEC 27002:2022, Annex A — Organisational & Technological Controls:

- A 5.15 — Access Control
- A 5.16 — Identity Management
- A 5.17 — Authentication Information
- A 5.18 — Access Rights
- A 8.2 — Privileged Access Rights
- A 8.3 — Information Access Restriction
- A 8.4 — Access to Source Code
- A 8.5 — Secure Authentication

BSI IT-Grundschutz:

- ORP.4.A1 (Rules for the Creation and Deletion of Users and User Groups)
- ORP.4.A2 (Creation, Modification and Revocation of Permissions)
- ORP.4.A3 (Documentation of User IDs and Access Profiles)
- ORP.4.A4 (Segregation of Duties)
- ORP.4.A5 (Granting of Physical Access Permissions)
- ORP.4.A6 (Granting of Logical Access Permissions)
- ORP.4.A7 (Granting of Data Access Rights)
- ORP.4.A8 (Rules for Password Use)
- ORP.4.A9 (Identification and Authentication)
- ORP.4.A10 (Protection of User IDs with Extensive Permissions)
- ORP.4.A11 (Password Reset)
- ORP.4.A12 (Development of an Authentication Concept for IT Systems and Applications)
- ORP.4.A13 (Suitable Selection of Authentication Mechanisms)
- ORP.4.A14 (Verification of the Effectiveness of User Separation)
- ORP.4.A15 (Approach and Conceptual Design of Identity and Access Management Processes)
- ORP.4.A16 (Policies for Data Access and Logical Access Control)
- ORP.4.A19 (Instruction of All Employees in the Use of Authentication Procedures and Mechanisms)
- ORP.4.A22 (Rules for Password Quality)
- ORP.4.A23 (Rules for Password-Processing Applications and IT Systems)
- ORP.4.A24 (Four-Eyes Principle for Administrative Activities)
- CON.8.A10 (Source Code Access Control)

Additional jurisdiction-specific laws and regulations — in particular data protection law (GDPR) and sector-specific regulations (NIS2, DORA, etc.) — are listed in the Legal Register and incorporated by reference.

## 2. Purpose & Scope

This policy establishes the framework for identity and access management (IAM) at **[YOUR_ORGANISATION_NAME]**. It implements the requirements of ISO/IEC 27002:2022 controls A 5.15 through A 5.18 (Access Control, Identity Management, Authentication Information, Access Rights) and A 8.2 through A 8.5 (Privileged Access Rights, Information Access Restriction, Access to Source Code, Secure Authentication), together with BSI IT-Grundschutz Baustein ORP.4 (Identity and Access Management).

The policy applies to all logical and physical access to information, information systems, networks, applications and source code. It covers all types of identities including personal user accounts, service accounts, shared identities, privileged accounts and non-human entities.

All employees, contractors, temporary personnel and third parties who access organisational systems or information are subject to this policy. Specific responsibilities for IT operations, system administrators, asset owners and line managers are defined in the Roles & Responsibilities section.

## 3. Access Control Policy Framework (A 5.15)

Owners of information and other associated assets determine the information security, privacy and business requirements related to access control. This policy takes account of these requirements and is communicated to all relevant interested parties. Access control rules are implemented by defining and mapping appropriate access rights and restrictions to the relevant entities — whether human users, machines, devices or services. To simplify management, specific roles are assigned to entity groups. Business requirements and risks are considered when determining which access control system is used, how rules are applied and what granularity is required.

### 3.1 Policy Considerations

- **Entity-to-Asset Access Mapping:** For each information asset and associated system, the required type of access (read, write, execute, delete, administer) is determined per entity role. Access requirements are documented in the access control matrix and reviewed whenever asset ownership or business processes change.
- **Application Security:** Access control requirements for applications are defined as part of the application security specification. Application-level access controls enforce role-based permissions and are integrated with the central identity management system where technically feasible.
- **Physical Access:** Logical access control is coordinated with physical access controls. Physical entry to secure areas is supported by appropriate physical entry controls including access badges, biometric readers or key-based mechanisms. Physical and logical access rights are managed consistently and reviewed together.
- **Need-to-Know & Classification Alignment:** Access rights are aligned with information classification levels and privacy requirements. Access to information is granted based on the need-to-know principle: only entities with a documented business need to access specific information at a given classification level receive the corresponding access rights.
- **Privileged Access Restrictions:** Access rights with elevated privileges are subject to additional restrictions including dedicated approval, time-limited grants, enhanced authentication and separate administrative identities. The detailed rules for privileged access are defined in Section 7 of this policy.
- **Segregation of Duties:** Access rights enforce the segregation of incompatible duties as defined in the organisation's segregation-of-duties matrix. No single person holds access rights that allow both initiating and approving a critical transaction.
- **Legal & Contractual Obligations:** Access restrictions mandated by applicable legislation (including GDPR, applicable national data protection law and sector-specific regulations) and contractual obligations are identified, documented and enforced through appropriate access controls. Access to personal data is limited to authorised data processors with a documented lawful basis.
- **Segregation of Access Control Functions:** The functions of access request, access authorisation and access administration are separated. The person requesting access is not the same person who authorises it, and the person authorising access is not the same person who implements the technical configuration. In smaller organisations where full separation is not feasible, compensating controls such as audit logging and periodic review are applied.
- **Formal Authorisation of Access Requests:** Every access request follows a formal authorisation process. Access is not granted until a documented approval from the information owner or delegated authority is recorded. The authorisation workflow is defined in the identity management process.
- **Access Rights Lifecycle Management:** Access rights are managed through their full lifecycle — from initial provisioning through modification to revocation. The processes for managing access rights are defined in the Access Rights Management section of this policy.
- **Logging & Audit Trail:** All access control events — including access grants, modifications, revocations and access attempts — are logged and retained in accordance with the organisation's logging policy. Logs are protected against tampering and reviewed regularly.

### 3.2 Access Control Rules

- **Classification-Consistent Access Rights:** Access rights are consistent with the information classification level assigned to each asset. Higher classification levels require stricter access controls, smaller access groups and more frequent access reviews.
- **Physical Perimeter Consistency:** Access rights are consistent with the physical perimeter security requirements. Entities operating from locations with lower physical security (e.g. remote or public areas) are subject to additional logical access restrictions such as VPN requirements and multi-factor authentication.
- **Distributed Environment Access:** In distributed environments, all available connection types — including LAN, VPN, wireless, cloud and remote desktop — are considered when defining access rules. Entities are provided with access only to the information, networks and network services they are authorised to use, regardless of the connection path. Network segmentation and firewall rules enforce these restrictions at the infrastructure level.
- **Dynamic Access Control:** Where operationally appropriate, dynamic access control factors — such as device posture, geographic location, time of day, risk score and authentication strength — are incorporated into access decisions. These factors supplement static role-based rules and enable context-aware access enforcement.

### 3.3 Overarching Principles

- **Need-to-Know:** An entity is granted access only to the information required to perform its assigned tasks. Different tasks and roles result in different access profiles. Access beyond what is required for the current role is not granted, regardless of seniority or organisational position.
- **Need-to-Use:** Access to information technology infrastructure — including systems, networks and services — is assigned only where a clear business need is documented and approved. Infrastructure access without a current operational purpose is revoked.
- **Least Privilege:** The default access state is "everything is forbidden unless expressly permitted." Access rights are granted at the minimum level required to perform the authorised function. The weaker rule "everything is permitted unless expressly forbidden" is not applied.

### 3.4 Awareness & Change Management

- **Automatic & Manual Label Changes:** Personnel are informed that changes to information labels — whether initiated automatically by information processing systems or manually by a user — can affect existing access rights. When a classification level changes, access rights are reviewed and adjusted accordingly.
- **System-Initiated & Administrator-Initiated Permission Changes:** Personnel are made aware that their access permissions can change both through automated system processes (e.g. role-based provisioning, time-based expiry) and through manual administrator actions. Users who notice unexpected permission changes report them to IT operations.
- **Periodic Approval Review:** Approval rules for access requests are defined at the time of initial setup and reviewed regularly — at least annually and after significant organisational changes. The review verifies that the approval workflow, delegated authorities and escalation paths remain appropriate.

Access control rules are supported by the documented procedures defined in the subsequent sections of this policy (identity management, authentication information, access rights, privileged access, information access restriction, source code access, secure authentication) and by clearly defined responsibilities. All personnel are instructed in the correct use of authentication procedures and mechanisms before receiving system access.

## 4. Identity Management (A 5.16)

The identity management processes ensure that every identity is uniquely assigned, traceable and managed throughout its lifecycle. Each user account is unambiguously linked to a single person or, in the case of non-human identities, to a documented system or service. Identities are created, modified and removed through a formal process with defined approval steps. Guest accounts and default accounts that are not required are disabled or removed. The IAM processes are defined and managed through five sub-processes: policy management, identity profile management, user account management, authorisation profile management and role management.

### 4.1 Identity Management Processes

- **Personal Identity Uniqueness:** Each identity assigned to a person is linked to exactly one individual. This one-to-one mapping ensures personal accountability for all actions performed under that identity. Each user account is unambiguously traceable to a named person.
- **Shared Identities:** Identities shared among multiple persons are permitted only where a documented business or operational necessity exists and no alternative is feasible. Each shared identity requires dedicated approval by the Information Security Officer, documentation of all persons authorised to use it, and a log of individual usage where technically possible.
- **Non-Human Identities:** Identities assigned to service accounts, automated processes, API clients or other non-human entities are subject to segregated approval — separate from regular user account provisioning — and independent ongoing oversight. Each non-human identity has a designated owner who is responsible for its lifecycle, access scope and credential rotation.
- **Timely Disablement & Removal:** Identities that are no longer required are disabled or removed without undue delay. When a person leaves the organisation, all associated user accounts are disabled on the last working day and deleted after a defined retention period. When a person changes role, accounts associated with the previous role are reviewed and adjusted within five working days. Inactive accounts are automatically flagged after 90 days and disabled after 180 days of inactivity.
- **No Duplicate Identities:** Within a single domain or system, each entity is mapped to a single identity. Duplicate identities for the same entity in the same context are avoided. Where an entity legitimately requires multiple identities across different domains (e.g. a standard account and a separate administrative account), each identity is documented with a clear purpose statement.
- **Event Logging for Identities:** All significant events concerning the creation, modification, disablement, deletion and use of user identities and authentication information are recorded in a tamper-protected audit log. This includes account creation, privilege changes, password resets, account lockouts and account deletions.
- **Identity Information Changes:** Changes to identity-related information — such as name changes, role reassignments or updated contact details — are processed through the identity management system. When identity verification documents (e.g. government-issued ID) were part of the initial identity proofing, re-verification is performed if material identity information changes.

### 4.2 Provisioning Steps

- **Business Requirement Confirmation:** Before any identity is created, the business requirement for its establishment is confirmed by the requesting manager or system owner. The request includes the intended purpose, required access scope and expected duration of use.
- **Identity Verification:** The identity of the entity is verified before a logical identity is allocated. For persons, this verification is performed during the onboarding process through government-issued photo identification or equivalent documentation. For external contractors, the sponsoring internal manager confirms the individual's identity.
- **Identity Establishment:** Once the business requirement is confirmed and identity verification is completed, the identity is established in the central identity management system with a unique identifier, documented owner and defined scope.
- **Configuration & Activation:** The identity is configured with the appropriate authentication services (password, MFA token, certificate) and activated only after all prerequisite steps are completed. Initial authentication credentials are generated according to the authentication information policy defined in Section 5 of this policy.
- **Access Rights Assignment:** Specific access rights are assigned to or revoked from the identity based on the applicable authorisation and entitlement decisions. Access provisioning follows the access rights management process defined in Section 6.

When identities provided or issued by third parties (e.g. federated identities, social media credentials) are used, the organisation verifies that the third-party identity provider delivers the required trust level and that associated risks are known and treated. Third-party identity arrangements are governed by the supplier management process and the authentication information controls defined in Section 5.

## 5. Authentication Information (A 5.17)

Authentication information — including passwords, PINs, certificates, tokens and biometric data — is managed securely throughout its lifecycle. The organisation defines rules for password use that are binding for all personnel. Whether passwords alone are sufficient or whether additional or alternative authentication mechanisms are required is determined per system based on the protection needs and the authentication concept. All personnel are instructed in the correct handling of authentication procedures and mechanisms before receiving access credentials.

### 5.1 Allocation of Authentication Information

- **Temporary Credentials:** Passwords or PINs generated automatically during enrolment are non-guessable, unique to each person and expire after first use. Users are required to set a personal password immediately upon initial login.
- **Identity Verification Before Issuance:** Before new, replacement or temporary authentication information is provided, the identity of the requesting user is verified through a defined procedure. For in-person requests, valid photo identification is checked. For remote requests, a multi-step verification process involving the user's manager or a secondary authenticated channel is used.
- **Secure Transmission:** Authentication information — including temporary credentials — is transmitted to users over an authenticated and protected channel. Unprotected (clear text) electronic mail is not used to transmit passwords or other secret authentication information. Where out-of-band delivery is required, a separate channel (e.g. SMS, sealed envelope or encrypted message) is used.
- **Acknowledgement of Receipt:** Users acknowledge receipt of authentication information, confirming they understand the associated responsibilities and the rules for secure handling defined in this policy.
- **Default Credential Replacement:** Default authentication information pre-configured by vendors or provided during system installation is changed immediately after installation and before the system is connected to the production environment. Pre-defined default user names are replaced where technically supported.
- **Record Keeping:** Significant events concerning the allocation and management of authentication information — including issuance, reset, revocation and compromise notifications — are logged. The confidentiality of these records is protected through access restrictions. An approved password vault tool is used where centralised credential storage is required.

### 5.2 User Responsibilities

- **Confidentiality of Credentials:** Secret authentication information such as passwords is kept confidential at all times. Personal passwords are not shared with anyone — including colleagues, managers and IT support staff. Passwords for shared or non-personal identities are disclosed only to explicitly authorised persons. Passwords are entered only when unobserved and are never stored on programmable function keys, sticky notes or in unprotected files.
- **Immediate Change After Compromise:** When authentication information is compromised or suspected of being compromised, the affected credential is changed immediately. Users report suspected compromises to IT operations without delay. For password-based accounts, the user initiates an immediate password change; for token-based or certificate-based credentials, the user contacts IT operations for revocation and replacement.
- **Strong Password Selection:** When passwords are used as authentication information, strong passwords are selected according to the following rules: passwords are not based on easily guessable personal information (names, telephone numbers, dates of birth); passwords are not based on dictionary words or simple combinations thereof; passwords consist of easy-to-remember passphrases that include alphanumeric and special characters; and passwords meet the minimum length defined in the password management system. The use of an approved password manager is recommended to generate and store complex passwords.
- **No Password Reuse Across Services:** A unique password is used for each distinct service and system. The same password is not used across multiple accounts. An approved password vault tool is made available to personnel to support the management of multiple unique passwords.
- **Employment Terms:** The obligation to follow these authentication information rules is included in the terms and conditions of employment for all personnel and in contracts with external parties.

### 5.3 Password Management System

- **Self-Service Password Management:** Users are able to select and change their own passwords. The password change process includes a confirmation procedure (re-entry of the new password) to prevent input errors.
- **Password Strength Enforcement:** The password management system enforces strong passwords in accordance with best practice: minimum length of at least 12 characters for standard accounts and at least 16 characters for privileged accounts, inclusion of multiple character classes (uppercase, lowercase, digits, special characters), and rejection of passwords that fail complexity checks.
- **First-Login Password Change:** Users are forced to change their password at first login. No access to organisational resources beyond the password change function is possible until the initial password has been replaced with a user-chosen password.
- **Event-Driven Password Changes:** Password changes are enforced when warranted by a specific event: after a security incident involving credential exposure, upon termination or change of employment when the departing user has known passwords for identities that remain active (e.g. shared identities), or when credential compromise is detected or suspected. Routine time-based password rotation is not enforced unless compromise detection mechanisms are unavailable.
- **Password History:** The password management system prevents re-use of previous passwords. A password history of at least the last 10 passwords is maintained and enforced.
- **Compromised Password Detection:** The password management system checks new passwords against lists of commonly-used passwords and known compromised username/password combinations from publicly disclosed breaches. Passwords matching these lists are rejected.
- **Password Display Masking:** Passwords are not displayed on screen when being entered. Input fields mask password characters by default. A temporary reveal function is permitted for accessibility purposes.
- **Protected Storage & Transmission:** Passwords are stored and transmitted only in protected form. Passwords are never stored in plain text in databases, configuration files, scripts or logs. Transmission of passwords over networks uses encrypted channels exclusively.
- **Cryptographic Hashing:** Stored passwords are hashed using approved cryptographic techniques — specifically modern adaptive hashing algorithms (e.g. Argon2, bcrypt, scrypt) with per-password salting. Reversible encryption or deprecated hashing algorithms (e.g. MD5, SHA-1) are not used for password storage.

### 5.4 Single Sign-On & Authentication Tools

- **Single Sign-On & Password Vaults:** The organisation provides single sign-on (SSO) or other authentication management tools (e.g. an approved enterprise password vault) to reduce the number of credentials that users are required to manage. Personnel are made aware that these tools also increase the impact of a credential disclosure — if the SSO credential or vault master password is compromised, all linked accounts are affected. SSO credentials and vault master passwords are therefore protected with multi-factor authentication. A central authentication service is used where feasible to enable consistent identity verification across all organisational systems.

## 6. Access Rights Management (A 5.18)

Access rights — both physical and logical — are managed through a formal provisioning, modification and revocation process. All access rights assignments follow the least-privilege and need-to-know principles. The issuance and withdrawal of physical access tokens (chip cards, keys, badges) is documented. Compromised access tokens are replaced immediately. All authorised user accounts, user groups and rights profiles are documented, and this documentation is regularly reviewed to confirm it reflects the actual state of access rights and remains aligned with current tasks and security requirements.

### 6.1 Provision & Revocation of Access Rights

- **Owner Authorisation:** Access to information and associated assets is granted only after authorisation from the designated owner of the information or asset. Where required by the asset classification, separate management approval is obtained in addition to the owner's authorisation.
- **Business Requirement & Policy Alignment:** Every access rights assignment considers the documented business requirements and the rules established in this access control policy. Access that serves no current business purpose is not granted, even if requested.
- **Segregation of Duties in Access Provisioning:** The roles of access approval and access implementation are separated. The person who approves an access request is not the same person who configures the access in the system. Conflicting roles — where a single person could both initiate and complete a sensitive transaction — are identified and separated through access controls.
- **Timely Revocation:** Access rights are removed when a person no longer needs to access the information or asset. When a person leaves the organisation, all access rights are revoked on or before the last working day. IT operations receives notification of personnel departures from HR in advance to prepare access revocation.
- **Temporary Access:** Where access is needed for a limited period — for temporary personnel, project-based work or time-bound tasks — access rights are provisioned with an explicit expiration date. The system automatically revokes access at the defined expiration time. Extensions require a new approval.
- **Access Level Verification:** Before activating access rights, the level of access granted is verified against this access control policy and against other information security and privacy requirements including the segregation-of-duties matrix. Access rights that exceed what the policy permits are not activated.
- **Activation After Authorisation:** Access rights — including those configured by service providers — are activated only after the authorisation procedure has been successfully completed and documented. No access is granted on a preliminary or provisional basis pending approval.
- **Central Access Record:** A central record is maintained of all access rights granted to each user identifier (logical or physical) to information and associated assets. This record is kept up to date and is accessible to the Information Security Officer, IT operations and internal audit for review purposes.
- **Role Change Adjustments:** When a user changes roles or jobs within the organisation, access rights associated with the previous role are reviewed and either removed or adjusted. The new role's access profile is applied, and any excess rights from the previous role are revoked within five working days of the effective date of the role change.
- **Physical & Logical Access Removal:** When access rights are revoked, both physical and logical access mechanisms are addressed. This includes removal, revocation or replacement of keys, badges, chip cards, authentication tokens, subscriptions and system account access. Physical access media are returned and documented.
- **Change Records:** All changes to users' logical and physical access rights are recorded with a timestamp, the identity of the authorising person, the identity of the implementing administrator and the nature of the change. This change log is retained in accordance with the organisation's retention policy and is available for audit.

### 6.2 Review of Access Rights

- **Review After Organisational Changes:** Users' access rights are reviewed after any organisational change — including job changes, promotions, demotions and termination of employment. The review verifies that current access rights match the user's actual role and responsibilities.
- **Privileged Access Review:** Authorisations for privileged access rights are reviewed at least quarterly and after every organisational change affecting persons with privileged access. The review confirms that each privileged account remains justified, that the account holder's competence and trustworthiness still support the privilege, and that the access scope is still the minimum required.

### 6.3 Considerations Before Change or Termination

- **Initiator & Reason Assessment:** When a change or termination of employment occurs, the circumstances are assessed: whether it is initiated by the user or by management, and the reason for the change. Management-initiated terminations and dismissals require immediate access review, as disgruntled personnel may attempt to corrupt information or sabotage systems.
- **Current Responsibilities:** The user's current responsibilities are assessed to determine which access rights require immediate attention. Users with access to sensitive or business-critical systems receive expedited access revocation.
- **Asset Value Assessment:** The value and sensitivity of the assets currently accessible to the user are evaluated. Access to high-value assets (systems handling classified information, financial data or personal data) is prioritised for immediate revocation or restriction during the transition period.

### 6.4 Role-Based Access Control

- **Role Definition:** User access roles are established based on business requirements. Each role summarises a set of access rights into a standard access profile that reflects typical job functions. Standard rights profiles are defined for each function and job role. Roles are documented, approved by the relevant business unit and reviewed annually.
- **Role-Level Management:** Access requests and access reviews are managed at the level of user access roles rather than at the level of individual access rights. When a user's role changes, the corresponding role-based access profile is applied rather than cloning another user's access rights. Cloning is avoided because it carries an inherent risk of accumulating excessive access rights over time.

### 6.5 Contractual Provisions

- **Contractual Sanctions:** Personnel contracts and service contracts include clauses specifying sanctions for attempted unauthorised access. These clauses are aligned with the disciplinary process and are reviewed by the legal function to ensure enforceability under applicable employment and contract law.

## 7. Privileged Access Rights (A 8.2)

Privileged access rights — those that allow the performance of administrative or system-level activities beyond the scope of standard users — are controlled through a dedicated authorisation process. This includes system administrator roles, database administrator roles, root and domain administrator access, and any access that allows modification of system configurations, security settings or audit logs. Accounts with elevated privileges are protected with multi-factor authentication. Standard rights profiles for administrative roles are maintained and regularly reviewed. For systems with increased protection needs, the four-eyes principle is applied to critical administrative activities.

### 7.1 Identification & Allocation

- **Identification of Privileged Users:** For each system or process — including operating systems, database management systems and applications — the persons who require privileged access rights are explicitly identified and documented. The list of privileged users per system is maintained by IT operations and reviewed at least quarterly.
- **Needs-Based & Event-Based Allocation:** Privileged access rights are allocated strictly as needed and, where possible, on an event-by-event basis in line with this access control policy. Privileged access is granted only to persons with the necessary competence to perform the activities that require it, and only to the minimum extent required by their functional role.
- **Authorisation Process & Record:** A documented authorisation process determines who can approve privileged access rights. Privileged access is not granted until the authorisation process is complete and recorded. A central record of all allocated privileges — including the approver, the scope of privilege and the date of allocation — is maintained and protected against unauthorised modification.
- **Expiry Requirements:** Privileged access rights have defined expiry dates. Standing privileged access is reviewed at least quarterly. Where technically feasible, privileged access is granted as time-limited sessions that automatically expire after the approved maintenance window or task duration.

### 7.2 Awareness & Authentication

- **Privilege Awareness:** Users are made aware of their privileged access rights and when they are operating in privileged access mode. Awareness measures include the use of distinct administrative user identities (separate from standard accounts), visual indicators in the user interface (e.g. colour-coded prompts), and where appropriate, dedicated administrative workstations or jump servers.
- **Enhanced Authentication:** Authentication requirements for privileged access are higher than for standard access. Multi-factor authentication is mandatory for all privileged accounts. Re-authentication or authentication step-up is required before performing work with privileged access rights, particularly when escalating from a standard session to a privileged session. For systems with increased protection needs, multi-factor authentication is applied to all accounts.

### 7.3 Review & Lifecycle

- **Regular Review:** Users with privileged access rights are reviewed regularly — at least quarterly — and after any organisational change. The review verifies that each person's duties, role, responsibilities and competence still qualify them for privileged access. Privileged access that is no longer justified is revoked immediately.
- **Generic Administrative Accounts:** The use of generic administration user IDs (such as "root", "admin" or "sa") is avoided where system configuration allows. Where generic accounts cannot be eliminated (e.g. system-level root accounts), their credentials are managed through a privileged access management (PAM) tool, changed regularly, and access to them is logged with individual accountability.
- **Temporary Privileged Access (Break Glass):** Privileged access is granted as temporary access for the time window necessary to implement approved changes or activities — for example, maintenance activities or critical changes. Permanent privileged access is avoided where just-in-time provisioning is technically feasible. Emergency access ("break glass") procedures are documented, and every use of emergency access is logged and reviewed within 24 hours.

### 7.4 Logging & Separation

- **Audit Logging:** All privileged access to systems is logged for audit purposes. Logs capture the identity of the user, the system accessed, the actions performed, the timestamp and the session duration. Privileged access logs are protected against tampering by the account holders themselves and are reviewed regularly by the Information Security Officer.
- **Individual Privileged Identities:** Identities with privileged access rights are not shared or linked to multiple persons. Each person who requires privileged access is assigned a separate, named administrative identity. Identities can be grouped (e.g. in an administrators group) to simplify management, but each group member retains an individual identity for accountability.
- **Separation of Administrative & Standard Activities:** Identities with privileged access rights are used exclusively for administrative tasks. Day-to-day activities — such as reading email, browsing the web or editing documents — are performed under a separate standard user identity. Users with administrative responsibilities maintain at least two accounts: one for administrative work and one for routine activities.

## 8. Information Access Restriction (A 8.3)

Access to information and other associated assets is restricted in accordance with this access control policy. Access restrictions are enforced at the application, system and network levels. For each system and application, a written access regulation exists that defines which identities and groups have which level of access. The organisation distinguishes between physical access (Zutritt), system access (Zugang) and data access (Zugriff), and manages all three categories through formally defined processes.

### 8.1 Basic Access Restriction

- **No Anonymous Access to Sensitive Information:** Access to sensitive information by unknown user identities or anonymously is not permitted. Public or anonymous access is granted only to storage locations and services that contain no sensitive or classified information. All access to classified information requires authenticated user identification.
- **Configuration Mechanisms:** Systems, applications and services provide configuration mechanisms to control access to information. These include access control lists (ACLs), role-based access controls, attribute-based access controls and file system permissions. Access control configurations are documented and managed as part of the system configuration baseline.
- **Data-Level Access Control:** Which data a particular user can access is controlled based on the user's role, the data's classification level and the user's documented need-to-know. Database views, row-level security and application-level filters are used where granular data access control is required.
- **Identity-to-Permission Mapping:** For each system, which identities or groups of identities have which access — including read, write, delete and execute permissions — is explicitly defined and documented. Permissions are assigned to roles rather than to individual identities wherever possible.
- **Isolation of Sensitive Systems:** Physical or logical access controls are used to isolate sensitive applications, application data and systems from less sensitive environments. Network segmentation, dedicated VLANs, firewalls and application-layer gateways enforce isolation boundaries. Access to isolated environments requires separate authentication and authorisation.

### 8.2 Dynamic Access Management — Use Cases

- **Granular Time-Based & Method-Based Control:** Dynamic access management techniques are applied when the organisation requires granular control over who accesses specific information, during what period and in what way — beyond what static role-based controls provide.
- **External Sharing with Retained Control:** When information is shared with persons or entities outside the organisation, dynamic access management is used to maintain control over who can access the shared content, for how long and with what permissions. Access can be revoked at any time without requiring the recipient to return or delete the information.
- **Real-Time Distribution Management:** For information requiring real-time control over its distribution, dynamic access management enables immediate adjustment of access permissions as circumstances change — for example, restricting access when an investigation is initiated or expanding access when a project team grows.
- **Protection Against Unauthorised Modification & Distribution:** Dynamic access controls protect information against unauthorised changes, copying, printing and redistribution. Document-level rights management enforces these restrictions regardless of the storage location or transmission path.
- **Usage Monitoring:** Dynamic access management enables monitoring of information usage — tracking who accessed specific information, when and what actions were performed — to support security oversight and compliance requirements.
- **Change Recording for Investigation:** All changes to dynamically protected information are recorded to support potential future investigations. The change log captures the identity of the person making the change, the nature of the change and the timestamp.

### 8.3 Dynamic Access Management — Rules

- **Dynamic Access Rules:** Rules for dynamic access management are established based on specific use cases. Access permissions can be conditioned on identity, device posture, location and application context. The classification scheme determines which information categories require protection through dynamic access management techniques. Zero-trust principles are applied where the risk profile justifies them: every access request is verified regardless of the network location or prior authentication state.
- **Operational & Monitoring Infrastructure:** Operational processes, monitoring procedures and reporting capabilities are established to support dynamic access management. The technical infrastructure required for real-time access evaluation, policy enforcement and audit logging is maintained by IT operations and tested regularly.

### 8.4 Dynamic Access Management — Mechanisms

- **Authentication & Credential Requirements:** Access to dynamically protected information requires authentication with appropriate credentials or a digital certificate. Anonymous access to dynamically protected content is not permitted.
- **Time-Bound Access:** Access to specific information can be restricted to defined time frames — for example, granting access only after a certain date or revoking access after a specified expiration date. Time-bound restrictions are enforced automatically by the access management system.
- **Encryption-Based Protection:** Encryption is used to protect information at rest and in transit. Access to the decryption key is itself an access control mechanism that limits who can read the protected content.
- **Print Permissions:** Printing permissions for classified or sensitive information are defined per classification level and per user role. Printing of information at the highest classification level is restricted or disabled by default and requires explicit authorisation.
- **Access Recording:** Who accesses dynamically protected information and how the information is used (view, edit, print, download, forward) is recorded in an audit trail. Access records are retained in accordance with the organisation's retention policy.
- **Misuse Alerts:** Automated alerts are raised when attempts to misuse dynamically protected information are detected — for example, repeated unauthorised access attempts, bulk downloads exceeding normal patterns, or access from unusual locations or devices outside business hours.

Dynamic access management techniques do not replace classical access management (e.g. access control lists) but add additional factors for conditionality, real-time evaluation, just-in-time data reduction and other enhancements that are particularly useful for the most sensitive information. Incident response is supported by dynamic access management, as permissions can be modified or revoked at any time.

## 9. Access to Source Code (A 8.4)

Access to program source code, associated items (designs, specifications, verification plans, validation plans) and development tools (compilers, builders, integration tools, test platforms) is strictly controlled. Source code is stored centrally in a source code management system. Access to source code libraries is controlled to reduce the potential for corruption of computer programs.

### 9.1 Source Code Access Controls

- **Managed Access to Source Code:** Access to program source code and source code libraries is managed according to established procedures. Access rights are reviewed when team membership changes and when projects are completed or decommissioned.
- **Read & Write Access Based on Business Need:** Read and write access to source code is granted based on documented business needs and is managed to address risks of unauthorised alteration or misuse. Write access is limited to developers actively working on the relevant code components. Read access is granted to additional roles (e.g. code reviewers, security testers) where justified.
- **Centralised Repository Access:** Where code components are used by multiple developers within the organisation, access is provided through a centralised code repository with read-only access as the default for consumers. Write access to shared components is restricted to designated maintainers.
- **Third-Party & Open-Source Code:** Access to open-source code and third-party code components used within the organisation is provided through read-only access from a curated internal repository or approved package registry. Direct modification of third-party source code is controlled through a documented forking and patching procedure.
- **Change-Controlled Updates:** Updates to source code and associated items are performed in accordance with change control procedures. Access to source code for the purpose of making changes is granted only after appropriate authorisation is received from the code owner or designated approver.
- **Indirect Repository Access:** Developers do not access the source code repository directly at the file system level. All access is mediated through developer tools (version control clients, IDE integrations, CI/CD pipelines) that control and log activities and authorisations on the source code.
- **Secure Storage:** Program listings and source code archives are held in a secure environment. Read and write access to these storage locations is appropriately managed and assigned based on documented roles. Backup copies of source code repositories are encrypted and stored in accordance with the backup policy.
- **Audit Log:** An audit log of all accesses to and all changes to source code is maintained by the source code management system. The audit log records the identity of the person or process, the files or repositories accessed, the type of action (read, write, merge, delete) and the timestamp. Audit logs are protected against modification and retained according to the organisation's log retention policy.
- **Code Integrity Controls:** When source code is intended to be published or distributed, additional controls provide assurance on the code's integrity. These include digital signatures on commits and releases, cryptographic checksums for distributed packages, and signed tags in the version control system.

## 10. Secure Authentication (A 8.5)

A suitable authentication technique is selected for each system based on the classification of the information to be accessed and the system's protection requirements. An authentication concept is developed for each IT system and application, defining the applicable functional and security requirements. Where strong authentication and identity verification is required, authentication methods alternative to or in addition to passwords — such as digital certificates, smart cards, hardware tokens or biometric means — are used. Authentication information for critical systems is accompanied by additional authentication factors (multi-factor authentication). Authentication mechanisms appropriate to the protection needs are used; after each unsuccessful authentication attempt, further attempts are increasingly delayed (Time Delay), and after exceeding the defined number of failed attempts, the account is locked. User separation is periodically verified: users log off after completing their tasks, and multiple users do not operate under the same identity.

### 10.1 Log-On Procedures & Technologies

- **Pre-Authentication Information Restriction:** Sensitive system or application information is not displayed until the log-on process has been successfully completed. Login screens show only the minimum information necessary for authentication and do not reveal system names, software versions, internal IP addresses or other details that could assist an unauthorised user.
- **Authorised-Users Notice:** A general notice is displayed on all log-on screens warning that the system, application or service is to be accessed only by authorised users. This notice informs users that access is logged and that unauthorised access attempts may result in disciplinary and legal consequences.
- **No Diagnostic Help Messages:** During the log-on procedure, no help messages are provided that could aid an unauthorised user. When an authentication error occurs, the system does not indicate which part of the submitted data (username or password) is incorrect. A generic error message (e.g. "Authentication failed") is displayed instead.
- **Deferred Validation:** Log-on information is validated only after all required input data has been submitted. Partial validation — such as confirming a username exists before requesting the password — is not performed, to prevent user enumeration attacks.
- **Brute Force Protection:** Systems are protected against brute force log-on attempts. Protective measures include progressive delay after failed attempts (Time Delay), CAPTCHA challenges after a defined number of failures, mandatory password reset after a threshold number of failed attempts, and account lockout after a maximum number of consecutive errors. The specific thresholds are defined per system based on its risk profile.
- **Authentication Event Logging:** Both unsuccessful and successful authentication attempts are logged. Log entries include the timestamp, the user identity attempted, the source IP address or device identifier, and the outcome (success or failure). Authentication logs are protected against tampering and retained in accordance with the logging policy.
- **Security Event Alerting:** A security event is raised when a potential breach of log-on controls is detected. Alerts are sent to the user (where the account is not locked) and to IT operations when a defined number of failed authentication attempts is reached for a single account, when authentication anomalies are detected (e.g. concurrent sessions from different locations), or when a successful authentication follows multiple failed attempts.
- **Post-Login Security Summary:** On completion of a successful log-on, the following information is displayed or sent via a separate channel: the date and time of the previous successful log-on, and details of any unsuccessful log-on attempts since the last successful log-on. This enables users to detect unauthorised use of their account.
- **Password Input Masking:** Passwords are not displayed in clear text when being entered. Input fields mask password characters by default. Where a temporary reveal function is provided for accessibility or error-reduction purposes, it is activated only at the user's explicit request and deactivated automatically after a short period.
- **Encrypted Network Transmission:** Passwords and other authentication credentials are not transmitted in clear text over any network. All authentication traffic uses encrypted protocols (e.g. TLS, SSH). Intranet authentication traffic is likewise encrypted to prevent interception by network sniffing.
- **Session Timeout:** Inactive sessions are terminated after a defined period of inactivity. The timeout period is configured based on the system's risk profile: high-risk systems (e.g. those accessible from public or external areas) use shorter timeout periods; standard internal systems use a default timeout. After timeout, re-authentication is required to resume the session.
- **Connection Duration Limits:** For high-risk applications, maximum connection duration times are defined to reduce the window of opportunity for unauthorised access. Connections to critical administrative interfaces are terminated and require re-authentication after a defined maximum session duration, regardless of activity.

Biometric authentication information is invalidated if it is ever compromised. Since biometric authentication can be unavailable depending on conditions of use (e.g. moisture, aging, injury), it is always accompanied by at least one alternative authentication technique. For password reset procedures, a secure process is defined and implemented that verifies the identity of the requesting user before issuing new credentials. Emergency and contingency procedures for the IAM system are in place to ensure continued operation if the identity and access management system becomes unavailable.

## 11. Roles & Responsibilities

- **Top Management:** Approves this policy, ensures adequate resources are provided for identity and access management and sponsors the IAM programme.
- **Information Security Officer (ISO):** Owns this policy, defines access control rules, reviews privileged access authorisations, monitors compliance with access control requirements and approves exceptions. Reviews the authentication concept for each IT system and application.
- **IT Operations:** Implements and administers access controls in systems, applications and infrastructure. Manages the identity management system, password management system and privileged access management tools. Configures authentication mechanisms, maintains access logs and executes access provisioning and revocation requests. Operates the central authentication service.
- **Information & Asset Owners:** Authorise access to the information and assets under their ownership. Define access requirements and classification levels. Participate in periodic access reviews for their assets.
- **Line Managers:** Request access rights for their team members, approve access requests within their authorisation scope, notify IT operations of personnel changes (new starters, role changes, departures) in a timely manner and participate in access reviews for their teams.
- **HR Department:** Notifies IT operations of onboarding, role changes, extended absences and departures to trigger the corresponding identity lifecycle actions. Ensures employment contracts include authentication information obligations and unauthorised access sanction clauses.
- **All Personnel:** Comply with this policy, protect their authentication information, use access rights only for authorised purposes, report suspected access control breaches or credential compromises and participate in authentication-related training and awareness programmes.

## 12. Review & Maintenance

This policy and the associated access control procedures are reviewed:

- At least annually, to verify continued alignment with current ISO/IEC 27002, BSI IT-Grundschutz recommendations and regulatory requirements.
- After any significant access-control-related security incident, to identify control gaps and implement improvements.
- When significant organisational changes occur — including mergers, acquisitions, restructuring or introduction of new business processes — that affect access requirements or the identity lifecycle.
- When new systems, applications or platforms are introduced that require integration with the identity and access management framework.
- When changes to applicable laws, regulations or contractual obligations affect access control requirements (e.g. new data protection regulations, sector-specific access rules).
- Following changes to the IAM system infrastructure, authentication service architecture or privileged access management tools.

Privileged access authorisations are reviewed at least quarterly. The documentation of user accounts, groups and rights profiles is reviewed at least annually and compared against the actual state of access rights in all systems. Results of access reviews are documented and any identified discrepancies are remediated within a defined timeline.
