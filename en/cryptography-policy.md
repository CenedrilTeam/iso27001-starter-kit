# Cryptography Policy

> **Document control**  
> Owner: [POLICY_OWNER_ROLE, e.g. Information Security Officer]  
> Approved by: [APPROVER_NAME_AND_ROLE]  
> Version: [VERSION]  
> Effective date: [EFFECTIVE_DATE]  
> Next review: [NEXT_REVIEW_DATE]

## 1. Legal/Regulatory Basis

ISO/IEC 27001:2022 / ISO/IEC 27002:2022, Annex A — Technological Controls:

- A 8.24 — Use of Cryptography

BSI IT-Grundschutz:

- CON.1.A1 (Selection of Suitable Cryptographic Procedures)
- CON.1.A2 (Data Backup When Using Cryptographic Procedures)
- CON.1.A4 (Suitable Key Management)
- CON.1.A5 (Secure Deletion and Destruction of Cryptographic Keys)
- CON.1.A9 (Definition of Criteria for the Selection of Hardware or Software with Cryptographic Functions)
- CON.1.A10 (Creation of a Crypto Concept)
- CON.1.A15 (Response to Practical Weakening of a Cryptographic Procedure)
- CON.1.A19 (Creation of a Crypto Inventory)

BSI Technical Guideline TR-02102 (Cryptographic Mechanisms: Recommendations and Key Lengths) is applied as the authoritative source for algorithm selection and key length recommendations.

Additional jurisdiction-specific laws and regulations — in particular data protection law (GDPR), export controls on cryptographic technology and sector-specific confidentiality requirements — are listed in the Legal Register and incorporated by reference.

## 2. Purpose & Scope

This policy establishes rules for the effective use of cryptography and the management of cryptographic keys at **[YOUR_ORGANISATION_NAME]**. It ensures proper and effective use of cryptographic techniques to protect the confidentiality, authenticity and integrity of information in accordance with business, information security and privacy requirements.

The policy applies to all personnel, IT systems, applications and services that generate, process, store or transmit information requiring cryptographic protection. This includes employees, contractors and third parties with access to the organisation's information and communication infrastructure.

Cryptography is applied to achieve the following information security objectives:

- **Confidentiality:** Encryption protects sensitive or critical information, whether stored or transmitted, so that only authorised recipients can read it.
- **Integrity & Authenticity:** Digital signatures and message authentication codes verify that stored or transmitted information has not been altered and originates from the claimed sender. File integrity checking algorithms detect unauthorised modifications. Cryptographic hash procedures (SHA-256 or stronger) are available for forensic evidence preservation.
- **Non-repudiation:** Cryptographic techniques provide evidence of the occurrence or non-occurrence of an event or action, preventing a party from denying involvement.
- **Authentication:** Cryptographic techniques authenticate users and system entities requesting access to or transacting with system users, entities and resources.

## 3. Cryptographic Policy (A 8.24)

The technical use of cryptographic procedures alone is insufficient to guarantee confidentiality, integrity and authenticity. Organisational measures complement the technical controls to form a comprehensive cryptographic concept. The following rules govern the selection, deployment and use of cryptography across the organisation.

### 3.1 General Principles

- **Cryptographic Policy Framework:** This policy constitutes the topic-specific policy on cryptography. It defines the general principles for the protection of information through cryptographic means, maximises the benefits of cryptographic techniques and minimises the risks of inappropriate or incorrect use.

### 3.2 Algorithm Selection & Cipher Strength

- **Classification-Based Strength:** The required level of protection is determined by the classification of the information being protected. The type, strength and quality of the cryptographic algorithm are selected accordingly — higher classification levels require stronger algorithms and longer key lengths.
- **Approved Algorithms & Standards:** Only established algorithms that have been intensively examined by the cryptographic community and for which no security vulnerabilities are known are used. The organisation follows the recommendations of BSI Technical Guideline TR-02102 for the selection of algorithms, cipher modes and minimum key lengths. A list of approved cryptographic algorithms, solutions and usage practices is maintained and reviewed annually.

When selecting cryptographic hardware or software, the following criteria are evaluated: functional scope, interoperability with existing systems, error safety and resilience against misuse, projected lifetime of the cryptographic procedure relative to the key lengths employed, legal and regulatory requirements and data protection implications. Certified cryptographic products are preferred where certification covers the relevant cryptographic aspects.

### 3.3 Mobile Device & Storage Media Encryption

- **Mobile Device & Media Encryption:** Information held on mobile user endpoint devices (laptops, smartphones, tablets) and on removable storage media is encrypted at rest using full-disk or container-based encryption. Information transmitted over networks to or from such devices is protected by transport-layer encryption (TLS 1.2 or higher, IPsec VPN).

### 3.4 Impact on Content Inspection Controls

- **Content Inspection Controls:** Where encrypted traffic bypasses security controls that rely on content inspection (e.g. malware detection gateways, data loss prevention filters, content filtering proxies), compensating measures are implemented. These include endpoint-based anti-malware scanning, TLS inspection at the gateway where legally and technically feasible, and application-layer security controls that operate before encryption is applied.

### 3.5 Legal & Cross-Border Requirements

- **Regulatory & Export Restrictions:** Before deploying cryptographic techniques, applicable regulations and national restrictions are identified — particularly for cross-border data flows. Import and export restrictions on cryptographic hardware and software are assessed for each jurisdiction involved. Where legal requirements conflict (e.g. data protection laws mandate encryption while a destination country restricts its use), a risk assessment is conducted and documented before the transfer proceeds.

### 3.6 External Cryptographic Service Providers

- **Service Level Agreements:** Contracts with external suppliers of cryptographic services (e.g. certificate authorities, managed HSM providers, cloud key management services) include explicit provisions for liability, service reliability, key escrow conditions, incident response times and the right to audit. Service level agreements define recovery time objectives for certificate issuance, revocation and key recovery operations.

## 4. Key Management (A 8.24)

Appropriate key management requires secure processes for generating, storing, archiving, retrieving, distributing, retiring and destroying cryptographic keys. The key management system is based on an agreed set of standards, procedures and secure methods covering the entire key lifecycle. Each cryptographic key serves only one purpose — in particular, separate keys are used for encryption and digital signature operations.

### 4.1 Key Generation

- **Key Generation:** Cryptographic keys are generated using approved key generators in a secure environment. Hardware random number generators or certified cryptographic libraries provide the entropy source. Default or pre-installed keys in cryptographic hardware or software are replaced before operational use. Keys for different cryptographic systems and applications are generated separately to limit the impact of a single key compromise.

### 4.2 Public Key Certificates

- **Certificate Issuance:** Public key certificates are obtained from trusted certificate authorities. Internal certificates are issued through the organisation's own PKI infrastructure or a contracted CA service. Each certificate request is validated against the identity of the requesting entity before issuance.
- **Certificate Authenticity Verification:** Before relying on a public key from a third party, its authenticity is verified through the certificate chain. Certificate revocation status is checked via CRL or OCSP before use. Self-signed certificates are only accepted in explicitly documented exceptions with compensating controls.

### 4.3 Key Distribution & Activation

- **Key Distribution & Activation:** Keys are distributed to intended recipients through secure channels that are separate from the data channel. Symmetric keys are never transmitted in plaintext over the same communication path as the encrypted data. Upon receipt, keys are activated through a documented procedure that confirms the integrity and authenticity of the received key material.

### 4.4 Key Storage & Protection

- **Key Storage & Access:** Cryptographic keys are stored in dedicated key stores (hardware security modules, encrypted key vaults, secure enclaves). Access to keys is restricted to authorised personnel and systems through role-based access control. Long-lived cryptographic keys are additionally stored offline, outside the operational IT systems, in a physically secured location.
- **Integrity Protection:** All keys are protected against unauthorised modification and accidental loss through integrity checks (e.g. checksums, HMAC) applied to key material at rest and during transfer.
- **Confidentiality of Secret & Private Keys:** Secret keys (symmetric) and private keys (asymmetric) are protected against unauthorised use and disclosure. They are stored encrypted, transmitted only through secure channels and accessed only through authenticated, authorised processes. Key material never appears in log files, error messages or debugging output.
- **Physical Security of Key Infrastructure:** Equipment used to generate, store and archive keys (HSMs, key servers, smart card personalisation stations) is housed in physically secured areas with access control, environmental monitoring and tamper-evident protection.

### 4.5 Key Rotation & Lifecycle

- **Key Rotation:** Cryptographic keys are changed at intervals defined by risk assessment and the sensitivity of the protected data. Rotation schedules are documented per key type: TLS certificates annually, signing keys biennially, encryption keys for stored data according to classification level. Automated rotation is used wherever technically feasible.
- **Activation & Deactivation Dates:** Each key has defined activation and deactivation dates. Technical controls enforce these dates so that keys are only usable within their designated validity period. Expiring keys and certificates trigger automated alerts at least 30 days before deactivation to allow timely renewal.

### 4.6 Compromised Key Handling

- **Compromised Key Response:** A documented procedure defines the steps to follow when a key compromise is suspected or confirmed. The compromised key is immediately revoked and all systems relying on it are identified and updated. A new key is generated and distributed. The incident is reported to the Information Security Officer and documented through the incident management process. Where the compromised key protected classified information, a risk assessment determines whether re-encryption of the affected data is required.

### 4.7 Key Revocation & Deactivation

- **Key Revocation & Deactivation:** Keys are revoked when they are compromised, when the key holder leaves the organisation or when the associated system or application is decommissioned. Revoked keys are added to certificate revocation lists or marked as inactive in the key management system within 24 hours. When a user leaves the organisation, their keys are revoked and archived (not destroyed) to allow future decryption of historical data if legally required.

### 4.8 Key Recovery & Backup

- **Key Recovery:** A documented key recovery procedure ensures that encrypted information remains accessible if a key is lost or corrupted. Recovery mechanisms (e.g. key escrow, secret sharing, master key decryption) are tested annually. For long-term stored encrypted data, regular checks confirm that the archived keys and the associated cryptographic software or hardware remain usable.
- **Key Backup & Archival:** Cryptographic keys are backed up in encrypted form and stored separately from the data they protect. Backup copies are held in at least two physically separate, access-controlled locations. Archived keys are retained for the period required by the data retention schedule, along with the associated cryptographic software or algorithm documentation needed to use them.

### 4.9 Key Destruction

- **Key Destruction:** Keys that are no longer needed are securely destroyed using approved methods (cryptographic erasure, physical destruction of key media). The destruction procedure and the methods used are documented. Before destroying a key, a check confirms that no encrypted data requiring future access depends on that key. The destruction event is logged with timestamp, responsible person and method used.

### 4.10 Logging & Auditing

- **Logging & Auditing:** All key management activities are logged — including key generation, distribution, activation, rotation, revocation, recovery and destruction. Logs are stored in a tamper-evident format, retained according to the organisation's log retention schedule and reviewed periodically by the Information Security Officer. Anomalies in key usage patterns (e.g. unusual access frequency, access outside business hours) trigger alerts for investigation.

### 4.11 Legal Access Requests

- **Legal Access Requests:** A procedure governs responses to legal requests for access to cryptographic keys or decrypted data (e.g. court orders requiring encrypted information in unencrypted form as evidence). Such requests are reviewed by legal counsel before any key material or decrypted data is released. All disclosures are documented with the legal basis, scope, approving authority and date.

The overall approach to key management — including the methods for generating, protecting and recovering cryptographic keys — is described in the subsections above. This approach covers the full key lifecycle and addresses the recovery of encrypted information in the case of lost, compromised or damaged keys through documented recovery and backup procedures.

## 5. Cryptographic Inventory

A cryptographic inventory is maintained and updated at least annually. For each group of IT systems using cryptographic functions, the following information is recorded:

- **Purpose:** The use case (e.g. full-disk encryption, TLS for communication, digital signatures, VPN tunnels).
- **Responsible Person:** The system owner or administrator accountable for the cryptographic implementation.
- **Algorithm & Parameters:** The cryptographic algorithm, cipher mode and key length in use.
- **Product:** The cryptographic hardware or software product deployed (including version).
- **Key Lifecycle Status:** Current key validity period, last rotation date and next scheduled rotation.

The inventory is cross-referenced with the organisation's asset inventory and serves as the basis for the annual algorithm review (see Review & Maintenance).

## 6. Roles & Responsibilities

- **Top Management:** Approves this policy, allocates resources for cryptographic infrastructure and ensures alignment with business objectives and legal requirements.
- **Information Security Officer (ISO):** Maintains this policy, defines approved algorithms and key lengths, reviews the cryptographic inventory, assesses the impact of weakened algorithms and coordinates incident response for key compromises.
- **IT Operations / Key Administrators:** Implement the cryptographic controls and key management procedures defined in this policy. Generate, distribute, rotate, back up and destroy keys in accordance with the documented processes. Maintain the cryptographic inventory and ensure timely certificate renewal.
- **System & Application Owners:** Ensure that cryptographic requirements are identified for their systems during design and procurement. Select cryptographic solutions from the approved list and integrate them in accordance with this policy.
- **All Personnel:** Use cryptographic tools as instructed (e.g. encrypt laptops, use VPN for remote access, verify digital signatures). Report suspected key compromises or cryptographic failures immediately to the Information Security Officer.

## 7. Review & Maintenance

This policy and the associated cryptographic inventory are reviewed:

- At least annually, based on the cryptographic inventory, to verify that all deployed algorithms, key lengths and cryptographic products remain secure and no known vulnerabilities exist.
- When the BSI Technical Guideline TR-02102 or equivalent international recommendations are updated with new algorithm or key-length guidance.
- After any cryptographic incident (key compromise, algorithm weakness disclosure, certificate authority breach).
- When new legal or regulatory requirements affecting cryptography are identified (e.g. export control changes, quantum computing readiness mandates).
- Following significant changes to the organisation's IT landscape, business processes or risk profile.

If a deployed algorithm is found to be weakened, the response process defined in this policy ensures that the affected algorithm is either hardened (e.g. increased key length) or replaced by a secure alternative before the weakness can be exploited.
