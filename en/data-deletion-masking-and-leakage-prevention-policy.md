# Data Deletion, Masking & Leakage Prevention Policy

> **Document control**  
> Owner: [POLICY_OWNER_ROLE, e.g. Information Security Officer]  
> Approved by: [APPROVER_NAME_AND_ROLE]  
> Version: [VERSION]  
> Effective date: [EFFECTIVE_DATE]  
> Next review: [NEXT_REVIEW_DATE]

## 1. Legal/Regulatory Basis

ISO/IEC 27001:2022 / ISO/IEC 27002:2022, Annex A — Technological and Organisational Controls:

- A 8.10 — Information Deletion
- A 8.11 — Data Masking
- A 8.12 — Data Leakage Prevention
- A 5.33 — Protection of Records

BSI IT-Grundschutz:

- CON.6.A1 (Rules for the Deletion and Destruction of Information)
- CON.6.A2 (Proper Disposal of Sensitive Equipment)
- CON.6.A3 (Deletion of Storage Media Before and After Use)
- CON.6.A4 (Selection of Suitable Deletion Methods)
- OPS.1.1.6.A11 (Use of Production Data in Test and Development Environments)
- CON.2 (Data Protection — Standard Data Protection Model SDM)
- NET.1.1.A35 (Network-Based Data Loss Prevention)
- SYS.2.1.A24 (Handling of External Interfaces)
- ISMS.1.A13 (Documentation of the Security Process)

Additional jurisdiction-specific laws and regulations — in particular GDPR, national data protection law, PCI DSS and sector-specific retention requirements — are listed in the Legal Register and incorporated by reference.

## 2. Purpose & Scope

This policy establishes rules for the secure deletion of information, the masking and pseudonymisation of sensitive data, the prevention of data leakage and the protection of organisational records at **[YOUR_ORGANISATION_NAME]**. It implements the requirements of ISO/IEC 27002:2022 controls A 8.10, A 8.11, A 8.12 and A 5.33, and reflects the BSI IT-Grundschutz requirements for deletion and destruction, data masking and privacy, and records management.

The policy applies to all personnel, information systems, applications, services and third-party suppliers that store, process or handle information on behalf of the organisation. It covers all forms of information — digital and physical — across the entire information lifecycle from creation through to final deletion or disposal.

Sensitive information is not kept for longer than it is required. Reducing the accumulation of data that is no longer needed limits the risk of unauthorised disclosure, regulatory non-compliance and reputational harm. This policy supports the organisation's data retention policy by defining the controls that apply when retention periods expire, when data subjects exercise deletion rights and when devices are decommissioned.

## 3. Information Deletion (A 8.10)

When deleting information from systems, applications and services, the chosen method is commensurate with the sensitivity of the information and the type of storage medium involved. Third-party agreements include explicit requirements on information deletion — both during the term of the service and upon its termination. Deletion processes are automated in accordance with topic-specific retention policies where technically feasible; logs track or verify that these automated deletion events have occurred.

### 3.1 Deletion Methods & Documentation

- **Deletion Method Selection:** The deletion method applied to a given item of information is chosen in accordance with business requirements and applicable laws and regulations. For unencrypted digital media, a PRNG-based multi-pass overwrite meeting BSI CON.6 level O-3 (or equivalent) is used. For encrypted digital media where the encryption key can be irrecoverably destroyed, cryptographic erasure is the preferred method. For optical media, deletion meets ISO/IEC 21964-2 level O-3. The method selected and its justification are documented for each deletion event.
- **Deletion Evidence:** The results of each deletion event are recorded as evidence. Records include the date of deletion, the information asset or dataset affected, the storage medium type, the deletion method applied, the responsible party and confirmation that the deletion was successfully completed. These records are retained for audit purposes in accordance with the retention schedule.
- **Third-Party Deletion Evidence:** Where external service providers delete information on behalf of the organisation — including cloud service providers, managed service providers and certified disposal contractors — documented evidence of deletion is obtained before or upon termination of the service. Evidence takes the form of a deletion certificate, audit report or equivalent confirmation specifying the method used. External providers are required to meet the same standards as internal deletion procedures; compliance is verified through regular audits.

### 3.2 Secure System-Level Deletion

- **Automated Secure Deletion:** Systems are configured to securely destroy information when it is no longer required — whether triggered by the expiry of a retention period defined in the data retention policy or by a data subject access request invoking the right to erasure. Automated deletion routines are tested at least annually to confirm they execute as intended and leave no recoverable remnants.
- **Deletion of Obsolete Copies:** Obsolete versions, backup copies, working copies and temporary files are deleted wherever they are located — including local workstations, file shares, collaboration platforms, email archives and cloud storage. Personnel are responsible for identifying and removing such copies in their areas of responsibility; IT operations performs periodic sweeps to identify orphaned data.
- **Secure Deletion Software:** Approved, certified secure deletion software is used to permanently delete information from digital storage in a manner that prevents recovery using specialist forensic tools. Only software listed on the organisation's approved deletion tools register is used for this purpose. The software version and configuration settings used are recorded as part of the deletion evidence.
- **Certified Disposal Providers:** Where the organisation uses external providers for secure disposal services, only providers that are certified to recognised standards (e.g. ISO/IEC 21964 / DIN 66399, NAID AAA) are engaged. Provider certifications are verified before appointment and at each annual contract review. Central collection points for media awaiting disposal are physically secured and access-restricted to prevent unauthorised removal.
- **Media-Specific Disposal Methods:** Disposal mechanisms are matched to the type of storage medium being disposed of. Hard disk drives and other magnetic media are degaussed and then physically shredded to at minimum BSI CON.6 level H-3. Solid-state drives and flash memory are subjected to cryptographic erasure followed by physical destruction to level E-3. Paper and print-outs are shredded to at least level P-3 on site or by a certified provider. Integrated storage (e.g. soldered memory in smartphones and IoT devices) is handled through factory reset followed by physical destruction where required by the information classification.
- **Cloud Service Deletion:** Before relying on a cloud service provider's deletion capability, the organisation verifies that the provider's deletion method is acceptable under this policy and applicable law. Where the provider's standard deletion mechanism is insufficient (e.g. does not prevent recovery from backup snapshots), the organisation requests specific deletion procedures or invokes contractual deletion rights. Confirmation of cloud deletion is obtained in writing and retained as evidence.

### 3.3 Device Decommissioning

- **Equipment Returned to Vendors:** When equipment is sent back to vendors — for repair, replacement, upgrade or end-of-lease return — all auxiliary storage (hard disk drives, SSDs, USB memory, SD cards) and internal memory modules are physically removed from the equipment before it leaves the organisation's premises. Where removal is technically impossible without voiding warranties or damaging the device, the storage medium is rendered unreadable through certified destruction or cryptographic erasure before dispatch. A checklist documenting the removal or destruction is completed for each equipment return.
- **Classification-Based Device Deletion:** The deletion method for a device is determined by the highest classification level of information the device has handled. For devices that have processed information classified as internal or above, destruction or a certified factory reset procedure is applied; a simple user-initiated reset without verification is not sufficient. For smartphones and tablets, a factory reset followed by a setup wizard run is the minimum standard. For IoT devices and network equipment, a factory reset combined with a credential change on the management interface is applied; where this is not sufficient for the classification level, physical destruction is used.
- **Physical Destruction:** Where physical destruction of storage media is required — either because secure deletion is technically infeasible or because the information classification demands it — the physical destruction controls defined in the *Physical Security Policy* are applied. Physical destruction renders the storage medium and the information it contains irrecoverable. The destruction event is witnessed, documented and retained as evidence.

## 4. Data Masking & Pseudonymisation (A 8.11)

Where the protection of sensitive data — in particular personally identifiable information (PII) — is a concern, the organisation applies data masking, pseudonymisation or anonymisation techniques to hide the data, disguise the true identity of PII principals or sever the link between sensitive information and the identity to which it relates. Before relying on any technique as a privacy safeguard, its adequacy is verified: effective data anonymisation covers all elements of the sensitive information, since a person can be identified indirectly through the combination of non-directly-identifying data points even after direct identifiers are removed (re-identification risk).

Production data containing PII is not used in test, development or quality assurance environments without first being at least pseudonymised, and preferably anonymised. Where complete anonymisation is technically infeasible, the Data Protection Officer is involved in assessing the residual re-identification risk before testing commences.

### 4.1 Masking Techniques

- **Encryption:** Data fields containing sensitive information are encrypted such that only authorised users holding the decryption key can view the plain-text values. Encryption used for masking purposes follows the algorithm and key management requirements of the *Cryptography Policy*.
- **Nulling or Character Deletion:** Characters within a sensitive field are replaced with null values, spaces or deletion characters so that unauthorised users cannot reconstruct the full value. Partial masking (e.g. showing only the last four digits of a payment card number) is used where the business process requires a fragment of the original value for operational purposes while protecting the remainder.
- **Numeric and Date Variation:** Numeric values and dates in datasets are varied — shifted, scaled or randomised — so that the statistical distribution is preserved for analytical purposes while individual values no longer correspond to real records. The variation algorithm and its parameters are documented and applied consistently across related datasets to maintain referential integrity.
- **Substitution:** Sensitive values are replaced with realistic but fictional substitute values (e.g. replacing real names with names from a synthetic name dictionary, or replacing real addresses with valid but non-existent addresses). Substitution tables and mapping files that would allow re-identification are stored separately from the masked dataset and access-controlled.
- **Hashing:** Sensitive values are replaced with their cryptographic hash. Where consistent pseudonymisation across datasets is required (e.g. to join anonymised tables), a keyed hash (HMAC) with a secret salt is used. The salt and the hash algorithm are documented. One-way hashing without a salt is only used for fields where it is acceptable that the hash cannot be reversed and cross-dataset joins are not required.

### 4.2 Implementation Requirements

- **Minimum Data Principle:** Not all users are granted access to all data. Database queries, API responses and data display masks are designed to return only the minimum fields required for each user's role and task. Role-based access controls are combined with field-level masking so that sensitive fields are omitted or masked for users who have no business need to see them, even when they have access to the record as a whole.
- **Record-Level Obfuscation:** Where certain records within a dataset are not to be visible to specific users — for example because a data subject has exercised a confidentiality right over certain health records — a mechanism is implemented to obfuscate those records. Users who do not have access rights to the obfuscated record are presented with an indicator that a record exists but its content is restricted, rather than being shown the sensitive data or receiving an error that could reveal the content indirectly.
- **Obfuscation of Obfuscation:** Where a PII principal requires that the fact of obfuscation itself is not revealed to other users — for example in healthcare contexts where the existence of certain types of obfuscated data is itself sensitive — the system is configured to present the record as if no obfuscation is applied. Only users with explicitly granted roles can discern whether a record has been subject to this secondary obfuscation layer.
- **Legal and Regulatory Masking Requirements:** Masking is applied wherever required by law or regulation. Payment card data (PAN, CVV, expiry date) is masked during processing and storage in accordance with PCI DSS requirements. Special categories of personal data under GDPR (Article 9) are subject to enhanced masking controls. The organisation's Standard Data Protection Model (SDM) compliance assessment identifies further fields that require masking under applicable data protection law.

### 4.3 Usage Controls & Re-identification Prevention

- **Strength of Masking:** The level of protection provided by the masking, pseudonymisation or anonymisation technique is proportionate to the intended use of the processed data. Data released for external research or publication requires full anonymisation with a documented re-identification risk assessment. Data used for internal testing requires at minimum pseudonymisation. Data used for internal analytics may use pseudonymisation or aggregation. The technique selection and the rationale for its adequacy are documented.
- **Access Controls on Processed Data:** Masked, pseudonymised or anonymised datasets are subject to access controls appropriate to the residual sensitivity of the data. Even after masking, datasets may retain enough information to allow re-identification in combination with other sources; accordingly, access is restricted to personnel with a documented business need and is revoked when that need ceases.
- **Usage Agreements and Restrictions:** Agreements or contractual restrictions governing the permissible uses of masked or pseudonymised data are established before the data is shared internally or externally. Recipients are notified of applicable restrictions (e.g. the data may only be used for the stated analytical purpose and may not be used to take decisions affecting individuals).
- **Prohibition on Re-identification:** Collating masked or pseudonymised data with other available information sources — whether internal datasets, publicly available data or commercially obtained data — for the purpose of re-identifying a PII principal is prohibited. This prohibition is communicated to all users of masked datasets and is included in data access agreements. Violations are treated as a data protection incident and reported in accordance with the incident management process.
- **Tracking of Data Flows:** A record is maintained of all instances where masked, pseudonymised or anonymised data is provided to a recipient or received from a source. The record includes the date, the dataset or fields involved, the technique applied, the recipient or source and the stated purpose. This record supports accountability, enables revocation of access where necessary and facilitates breach notifications if a re-identification risk is later identified.

## 5. Data Leakage Prevention (A 8.12)

The organisation implements organisational and technical measures to reduce the risk of sensitive information being disclosed to unauthorised parties through intentional or accidental data leakage. Data leakage prevention (DLP) inherently involves monitoring personnel communications and online activities; prior to deploying any DLP tool or monitoring capability, legal counsel reviews the implementation for compliance with applicable employment law, data protection law and works council consultation requirements.

### 5.1 Classification & Channel Monitoring

- **Information Classification for DLP:** Information requiring protection against leakage is identified and classified. Categories include personally identifiable information, payment card data, health data, intellectual property (source code, product designs, pricing models), legally privileged communications and merger or acquisition information. The classification scheme defined in the *Information Classification & Labelling Policy* provides the basis for determining which information categories are subject to DLP controls and at what level of protection.
- **Leakage Channel Monitoring:** The following channels are monitored for potential data leakage: outbound email (including attachments), web uploads and cloud storage synchronisation, file transfer services and FTP, mobile devices and endpoint removable storage, printing and screen capture activity and instant messaging and collaboration platforms. Monitoring scope, methods and data retention for monitoring logs are defined in a monitoring policy reviewed and approved by legal counsel before deployment.
- **Leakage Prevention Actions:** Where DLP rules detect a potential leakage event, the system takes one of the following automated actions depending on the severity: log only (for low-risk events, for monitoring and trend analysis), user notification and confirmation (requiring the user to acknowledge a warning before proceeding) or quarantine and block (for high-risk events, holding the outbound item for review by the data owner or Information Security Officer before release or deletion). Quarantine notifications are sent to the relevant data owner within one business day.

### 5.2 DLP Tool Deployment

- **Discovery and Monitoring of Sensitive Data at Rest:** DLP tools are deployed to identify and monitor sensitive information at risk of unauthorised disclosure, including unstructured data residing on user workstations, shared drives and collaboration platforms. Automated discovery scans run at least monthly to detect sensitive data that has been stored outside approved repositories, and findings are reported to data owners for remediation.
- **Detection of Disclosure Events:** DLP tools detect the disclosure of sensitive information across all monitored channels, including uploads to untrusted third-party cloud services, transmission via personal email accounts and copying to unauthorised external storage. Detected events generate alerts that are reviewed and triaged by the Information Security Officer or a delegated DLP analyst within the response times defined in the incident management procedure.
- **Blocking Unauthorised Transmissions:** User actions and network transmissions that would expose sensitive information outside the organisation's control are blocked at the technical level. Specific blocking rules cover: preventing bulk copying of database entries into spreadsheets or external applications; blocking uploads of classified data to consumer cloud services not on the approved services list; restricting the use of removable media interfaces on endpoint devices that have not been authorised for data transfer; and preventing the use of unauthorised screen-capture utilities on devices that process restricted information.

### 5.3 Additional DLP Measures

**Copy-Paste and Upload Restrictions:** Where the risk assessment determines that preventing copy-paste or upload of data to services, devices and storage media outside organisational control is necessary, the organisation deploys DLP technology or configures existing tools to allow users to view and work with data held remotely without being able to extract it to uncontrolled environments. Remote-view-only access configurations are used for the most sensitive datasets where technically feasible.

**Data Owner Approval for Exports:** Where a legitimate business need requires the export of sensitive data beyond standard access controls — for example to share with a business partner or to perform an authorised bulk analysis — the relevant data owner approves the export in writing before it is executed. The approval records the purpose, the recipient, the dataset or fields involved, any masking applied and the applicable data handling obligations. Users who perform approved exports are personally accountable for the proper handling of the exported data.

**Screenshot and Screen Recording Policy:** Taking screenshots, screen recordings or photographs of screens displaying sensitive information is addressed through the organisation's acceptable use policy, terms and conditions of system access and security awareness training. Where technically enforceable, screenshot functionality is disabled on applications that display the most sensitive categories of information. Compliance is monitored through periodic audits and user activity reviews.

**Backup Protection:** Where sensitive information is included in backups, the backup media and backup data are protected using encryption, role-based access controls and physical protection of storage media. Backup encryption keys are managed in accordance with the *Cryptography Policy*. Access to backup restoration functions for sensitive datasets is restricted to authorised personnel and logged.

## 6. Protection of Records (A 5.33)

The organisation protects the authenticity, reliability, integrity and usability of its records throughout their lifecycle as business context and management requirements change over time. Records management covers any set of information — regardless of structure or form — that is created, captured and managed in the course of business, including documents, collections of data and digital or analogue information. Metadata describing the context, content and structure of records is treated as an essential component of any record and is protected with the same controls as the record itself.

### 6.1 Records Management Guidelines

- **Storage, Handling and Disposal Guidelines:** Guidelines covering the storage, handling, chain of custody and disposal of records are established and maintained. These guidelines define approved storage locations and media for each record type, handling procedures that prevent unauthorised access or modification (including physical access controls for paper records and access controls for electronic records), chain-of-custody requirements for records transferred between departments or to external parties and disposal procedures that prevent unauthorised reconstruction of disposed records. The guidelines include explicit measures for the prevention of record manipulation, including tamper-evident storage where appropriate and version-controlled document management for electronic records. Guidelines are aligned with the organisation's topic-specific records management policy and reviewed at least annually.

### 6.2 Retention Schedule

- **Retention Schedule:** A retention schedule is maintained that defines, for each record type, the retention period applicable and the trigger event from which that period is counted (e.g. date of creation, date of contract termination, date of last transaction). Retention periods are set in accordance with applicable national and regional legislation, sector-specific regulations, contractual obligations and community expectations. The retention schedule is reviewed at least annually and updated whenever applicable legal or regulatory requirements change. Records that have passed their retention period and for which no legal hold or override is in effect are disposed of in accordance with the secure deletion procedures in Section 3 of this policy.

**Record Categories:** Records are categorised by type, including accounting and financial records, business transaction records, personnel records, legal and compliance records and information security records. Each category in the retention schedule specifies the applicable retention period, the allowable storage media (physical or electronic), the access classification and the applicable disposal method. National law and regulation take precedence in setting retention periods where they specify minimum or maximum retention durations for a given record type.

**Data Retrieval:** Storage systems are chosen and configured to ensure that required records can be retrieved in an acceptable timeframe and in a usable format, throughout the full retention period. For electronic storage media, procedures are established to ensure continued access — including readability of both storage media and file formats — as technology changes over the retention period. Media integrity is checked at intervals consistent with manufacturer recommendations and media deterioration risk.

**Encrypted Archives and Cryptographic Keys:** Where electronic records are stored in encrypted form or are protected by digital signatures, the associated cryptographic keys and the decryption or signature-verification software are retained for the full duration of the records' retention period. This ensures that records remain readable and verifiable throughout the period they are required to be kept. Key retention follows the procedures defined in the *Cryptography Policy*.

## 7. Roles & Responsibilities

- **Top Management:** Approves this policy and ensures that adequate resources are allocated for deletion tooling, DLP infrastructure, masking capabilities and records management systems. Receives annual reporting on the status of data deletion compliance and DLP incident trends.
- **Information Security Officer (ISO):** Maintains this policy; defines approved deletion methods, DLP rules and masking standards; oversees DLP alert triage; coordinates legal review prior to DLP deployment; and ensures that deletion evidence and DLP incident records are retained in accordance with the retention schedule.
- **Data Protection Officer (DPO):** Reviews DLP deployment plans and monitoring configurations for compliance with GDPR and applicable data protection law; assesses re-identification risk for pseudonymised and anonymised datasets; approves the use of production PII in test environments where full anonymisation is not feasible; and advises on masking adequacy for special-category data.
- **IT Operations:** Configures and operates secure deletion tools, DLP platforms and automated retention-based deletion processes; carries out device decommissioning procedures; maintains the approved deletion tools register and the DLP configuration documentation; and executes physical media disposal in accordance with this policy.
- **Data Owners:** Classify information under their ownership in accordance with the *Information Classification & Labelling Policy*; approve data exports; receive and act on DLP quarantine notifications; maintain the retention schedule entries for their record types; and confirm that deletion evidence is obtained from third parties holding their data.
- **Legal Counsel:** Reviews DLP monitoring configurations for employment law and data protection compliance prior to deployment; advises on deletion obligations arising from data subject requests and regulatory requirements; and maintains up-to-date input to the retention schedule reflecting applicable legal retention periods.
- **All Personnel:** Delete obsolete copies of information from their areas of responsibility; use only approved deletion tools; comply with DLP policies and acceptable use rules; report suspected data leakage events to the Information Security Officer; and complete security awareness training covering data deletion and DLP obligations.

## 8. Review & Maintenance

This policy and the associated retention schedule, approved deletion tools register and DLP rule set are reviewed:

- At least annually, to verify continued alignment with applicable law, regulatory requirements, business processes and the threat landscape.
- When applicable legislation or regulation is amended — in particular GDPR implementing acts, national data protection law, sector-specific retention requirements or export control rules affecting deletion methods.
- Following any data leakage incident, deletion failure or records management audit finding — to identify control gaps and update policy, tools or procedures accordingly.
- When significant changes occur to the organisation's information systems, cloud service portfolio, storage infrastructure or organisational structure that affect the scope or effectiveness of existing controls.
- When third-party deletion providers, DLP tool vendors or cloud service providers are added, changed or removed, to re-verify compliance with this policy's requirements.

All versions of this policy are archived in the document management system in accordance with the records management guidelines in Section 6. The version history, including the date of each review, the reviewer and a summary of changes, is maintained as part of the document record.
