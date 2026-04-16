# Information Transfer Policy

> **Document control**  
> Owner: [POLICY_OWNER_ROLE, e.g. Information Security Officer]  
> Approved by: [APPROVER_NAME_AND_ROLE]  
> Version: [VERSION]  
> Effective date: [EFFECTIVE_DATE]  
> Next review: [NEXT_REVIEW_DATE]

## 1. Legal/Regulatory Basis

ISO/IEC 27001:2022 / ISO/IEC 27002:2022, Annex A — Organisational Controls:

- A 5.14 — Information Transfer

BSI IT-Grundschutz:

- CON.9 (Information Exchange)
- CON.1 (Crypto Concept)
- CON.7.A9 (Secure Handling of Mobile Storage Media)
- APP.5.3 (General E-Mail Clients and Servers)
- SYS.4.5 (Removable Media)
- SYS.4.1.A5 (Usage Policies for Printers, Copiers and All-in-One Devices)

Additional jurisdiction-specific laws — in particular data protection law (GDPR), electronic signature law (eIDAS) and sector-specific transfer obligations (NIS2, financial and healthcare regulations) — are listed in the Legal Register and incorporated by reference.

## 2. Purpose & Scope

This policy defines the rules, procedures and agreements for the secure transfer of information at **[YOUR_ORGANISATION_NAME]**. It covers all forms of information transfer — electronic, physical storage media and verbal — both within the organisation and with external parties.

This policy applies to:

- All employees (permanent, temporary, part-time)
- External personnel (contractors, consultants, temporary staff) who transfer information on behalf of the organisation
- Third parties with whom information is exchanged under formal agreements
- All information regardless of format: electronic data, physical documents and storage media, verbal communications

The protection measures applied to information in transit reflect the classification level of the information involved as defined in the *Information Classification & Labelling Policy*. Before any transfer, the sender verifies that the recipient is authorised to receive the information and that an appropriate transfer channel is used.

## 3. General Transfer Requirements (A 5.14)

The following requirements apply to all types of information transfer — electronic, physical and verbal. They form the baseline that is supplemented by the channel-specific rules in subsequent sections.

### 3.1 Protection of Information in Transit

Information in transit is protected against interception, unauthorised access, copying, modification, misrouting, destruction and denial of service. The level of protection is commensurate with the classification level of the information:

- **Encryption:** Information classified CONFIDENTIAL or above is encrypted during transfer using cryptographic techniques that meet current standards (AES-256 for symmetric encryption, RSA-2048 / ECDSA P-256 or higher for asymmetric encryption, TLS 1.2 as minimum for transport encryption — TLS 1.3 preferred). Key lengths follow BSI TR-02102 recommendations and are reviewed annually.
- **Access control:** Transfer channels enforce access controls commensurate with the classification level. INTERNAL information uses membership-based channels (shared drives, intranet). CONFIDENTIAL information uses individually authorised, encrypted channels. STRICTLY CONFIDENTIAL information uses end-to-end encrypted channels with named-recipient access only.
- **Integrity verification:** Transfers of CONFIDENTIAL or higher information include integrity verification mechanisms (checksums, digital signatures or hash values) so that recipients can confirm the information has not been altered in transit.
- **Anti-misrouting:** Automated transfer systems include validation checks (recipient address verification, domain whitelisting) to prevent information from being sent to incorrect destinations.

Before transferring information externally, the sender verifies that the recipient is authorised to receive information at the given classification level and that the transfer method provides adequate protection. Residual information and metadata (tracked changes, embedded comments, hidden data, EXIF data) are removed from documents and files before transfer to prevent unintended disclosure.

### 3.2 Traceability & Chain of Custody

A chain of custody is maintained for information classified CONFIDENTIAL or above during transfer:

- **Transfer logging:** Each transfer event is logged with sender identity, recipient identity, timestamp, content reference (document name or identifier — not the content itself), transfer method used and protection measures applied.
- **Digital signatures:** Transfers of critical business information (contracts, legal documents, regulatory filings) use digital signatures to provide non-repudiation — the sender cannot deny having sent the information, and the recipient can verify its origin and integrity.
- **Acknowledgement of receipt:** For STRICTLY CONFIDENTIAL transfers, the recipient confirms receipt through a documented acknowledgement (digitally signed response, signed delivery note or equivalent).

Transfer logs are retained in accordance with the retention schedule and are available for audit and incident investigation purposes.

### 3.3 Transfer Contact Directory

A contact directory for information transfer is maintained, identifying the responsible persons for each transfer type:

- **Information owners / asset owners:** Authorise transfers of their information, approve recipient lists and define classification-specific handling requirements.
- **Risk owners:** Assess and accept residual risks associated with specific transfer channels or third-party agreements.
- **Information Security Officer:** Advises on transfer security controls, reviews transfer agreements and is the escalation point for transfer-related security concerns.
- **Information custodians:** Operate and maintain transfer infrastructure (email gateways, file transfer services, courier processes) and ensure technical controls are functioning.

The contact directory is accessible to all personnel on the intranet and is updated whenever roles change. In case of uncertainty about a transfer, personnel contact the information owner or the Information Security Officer before proceeding.

### 3.4 Incident Responsibilities & Liabilities

Responsibilities for information security incidents during transfer are clearly assigned:

- **Sender responsibility:** The sender is responsible for selecting an appropriate transfer method, applying the correct protection measures and verifying the recipient's authorisation. If information is lost, intercepted or corrupted during transfer, the sender reports the incident immediately through the incident management process.
- **Recipient responsibility:** The recipient confirms receipt of expected transfers, reports missing or tampered deliveries and handles received information in accordance with its classification level.
- **Third-party transfers:** Transfer agreements with external parties include liability clauses specifying responsibilities in the event of data loss, unauthorised access or breach of confidentiality. These clauses are reviewed by the legal department before signing.

### 3.5 Labelling of Transferred Information

Information retains its classification label throughout the transfer process so that every handler and recipient immediately understands the protection requirements:

- **Electronic transfers:** Email subject lines include the classification level tag (e.g. [CONFIDENTIAL]). File names or metadata carry the classification. Classification banners are applied to document headers and footers.
- **Physical transfers:** Outer packaging displays the classification level. For STRICTLY CONFIDENTIAL material, double enveloping is used — the inner envelope carries the classification marking, the outer envelope shows only addressing information with no indication of the sensitivity of the contents.
- **Verbal transfers:** The speaker states the classification level at the beginning of the conversation (see Section 6 on Verbal Transfer).

The labelling system is defined in the *Information Classification & Labelling Policy*. Personnel verify that labels are correctly applied before initiating any transfer.

### 3.6 Transfer Service Reliability & Availability

Transfer services used by the organisation meet the following reliability and availability requirements:

- **Internal services:** Email, file sharing and collaboration platforms are operated with defined service levels (availability targets, maximum downtime windows, capacity thresholds). IT monitors these services and reports deviations.
- **External / third-party services:** Service level agreements (SLAs) with external transfer service providers specify availability guarantees, incident response times and data protection obligations. SLA performance is reviewed at least annually.
- **Failover:** For business-critical transfer channels, alternative transfer methods are documented and tested so that information can still be exchanged if the primary channel is unavailable.
- **Compatibility:** Before establishing a new transfer channel — internally or with a third party — IT verifies that the sending and receiving systems are technically compatible and that security controls function correctly end-to-end.

### 3.7 Acceptable Use of Transfer Facilities

The use of information transfer facilities at [YOUR_ORGANISATION_NAME] is governed by the *Acceptable Use Policy*. In summary:

- Transfer facilities (email, file sharing, messaging, removable media, fax) are provided for business purposes. Limited personal use is permitted provided it does not compromise security.
- Only transfer methods approved by IT are used for organisational information. Unapproved file-sharing services, personal email accounts and unvetted cloud platforms are not used to transfer organisational data.
- Personnel do not circumvent technical transfer controls (DLP rules, email encryption, web filtering) or use anonymising tools to bypass monitoring.

### 3.8 Retention & Disposal of Transfer Records

Business records created or transmitted through transfer channels are subject to the organisation's retention schedule:

- **Email messages:** Retained in the email archiving system for the period specified in the retention schedule. Automatic deletion is applied after expiry unless a legal hold is in effect.
- **Chat and instant messaging logs:** Retained for the defined period. Personnel are aware that business decisions communicated via chat are subject to the same retention rules as email.
- **File transfer logs:** Transfer metadata (sender, recipient, timestamp, file name) is retained for audit trail purposes in accordance with the logging policy.
- **Disposal:** When transfer records reach the end of their retention period, they are securely disposed of using methods appropriate to the classification level of the information.

### 3.9 Legal, Regulatory & Contractual Requirements

Information transfers comply with all applicable legal, statutory, regulatory and contractual obligations:

- **Data protection:** Personal data is transferred in compliance with the GDPR and applicable national data protection laws. Cross-border transfers outside the EEA use approved transfer mechanisms (adequacy decisions, standard contractual clauses, binding corporate rules).
- **Electronic signatures:** Where legal or regulatory requirements demand authenticated documents (contracts, regulatory filings, audit reports), qualified electronic signatures conforming to eIDAS Regulation (EU) 910/2014 or equivalent national law can be used.
- **Sector-specific regulations:** Transfers subject to sector-specific rules (e.g. financial regulations, healthcare data requirements, critical infrastructure obligations under NIS2) comply with the additional controls specified in those regulations. The legal and regulatory register maintained by the organisation documents which regulations apply.
- **Contractual obligations:** Transfers to or from contractual partners follow the security requirements stipulated in the relevant contract or service agreement. Non-disclosure agreements (NDAs) are in place before exchanging CONFIDENTIAL or higher information with external parties.

## 4. Electronic Transfer

Electronic transfer includes email, file sharing platforms, collaboration tools, instant messaging, cloud storage and any other digital communication channel. The following rules supplement the general transfer requirements above.

### 4.1 Malware Protection

All electronic information transfers pass through malware detection controls:

- **Email gateway:** Inbound and outbound email is scanned for malware at the email gateway. Attachments containing executable code, macro-enabled documents or file types on the organisation's blocked list are quarantined and the sender/recipient is notified.
- **File transfer services:** Files uploaded to or downloaded from organisational file-sharing and collaboration platforms are scanned by the platform's integrated anti-malware engine before they become available to recipients.
- **Removable media:** Data written to or read from removable media (USB drives, external hard drives, optical discs) is scanned for malware before processing (see also Section 5 on Physical Storage Media).
- **Encrypted transfers:** Where end-to-end encryption prevents gateway-level scanning, endpoint protection on the receiving device performs the malware scan upon decryption. Recipients do not open encrypted attachments on devices without active, up-to-date endpoint protection.

Malware protection controls are aligned with the organisation's *Endpoint Security & Malware Protection Policy*.

### 4.2 Secure Attachment & File Handling

Sensitive electronic information transmitted as attachments is protected commensurate with its classification level:

- **INTERNAL:** Standard transport encryption (TLS) between email servers is sufficient. No additional attachment encryption is required for internal transfers within the organisation's network.
- **CONFIDENTIAL:** Attachments sent externally are encrypted (password-protected archive with AES-256, or S/MIME / PGP encrypted email). The decryption key is transmitted via a separate channel (e.g. phone call, SMS, separate email).
- **STRICTLY CONFIDENTIAL:** End-to-end encryption is mandatory. Attachments are only sent via approved secure file transfer services with named-recipient access, audit logging and automatic expiration. Email is not used for STRICTLY CONFIDENTIAL attachments unless end-to-end encryption (S/MIME or PGP) is in place for both sender and recipient.
- **Large files:** Files exceeding the email size limit are transferred via the organisation's approved secure file transfer service — not via personal cloud storage, consumer file-sharing platforms or unencrypted FTP.

### 4.3 Prevention of Misdirected Communications

Controls are in place to prevent information from being sent to incorrect recipients:

- **Address verification:** Email auto-complete is configured to flag external recipients with a visual warning. Personnel verify the recipient address before sending, especially when the message contains classified information or is addressed to distribution lists.
- **External recipient notification:** Emails to external recipients automatically include a banner or disclaimer identifying the message as external-bound, prompting the sender to confirm that external sharing is intended.
- **DLP rules:** Data loss prevention (DLP) rules flag emails and file transfers that contain classification markers (CONFIDENTIAL, STRICTLY CONFIDENTIAL) and are directed to external or unauthorised recipients. Flagged transfers are held for sender confirmation or routed to the Information Security Officer for review.
- **Recall and deletion:** If a misdirected transfer is detected, the sender immediately notifies IT and the Information Security Officer. IT initiates recall (for email) or access revocation (for file-sharing links) and the incident is reported through the incident management process.

### 4.4 Approval of External Transfer Services

External public services used for information transfer require prior approval:

- **Approval process:** Before any external service (instant messaging, social networking, file sharing, cloud storage) is used to transfer organisational information, a formal request is submitted to IT. IT conducts a security and data protection assessment in coordination with the Information Security Officer and the Data Protection Officer.
- **Approved service register:** A register of approved and prohibited external transfer services is maintained by IT and published on the intranet. Only services listed as approved are used for business purposes.
- **Periodic review:** The approved service register is reviewed at least semi-annually. Services that no longer meet security or data protection requirements are removed and users are notified of approved alternatives.
- **Prohibited services:** Consumer-grade file-sharing (e.g. personal Dropbox, Google Drive with private accounts), unvetted messaging platforms and social media direct messages are not used to transfer information classified INTERNAL or above.

### 4.5 Authentication on Public Networks

When information is transferred via publicly accessible networks, stronger authentication and encryption controls apply:

- **VPN requirement:** Access to internal transfer services (email, file shares, collaboration platforms) from public or untrusted networks is routed through the organisation's VPN. Direct access without VPN from public networks is technically blocked.
- **Multi-factor authentication (MFA):** All transfer services accessible over the internet require MFA. Single-factor password authentication is not accepted for internet-facing transfer services.
- **Certificate-based authentication:** Automated system-to-system transfers over public networks use certificate-based mutual TLS authentication. API keys or tokens are not transmitted in URLs or query strings.
- **Public Wi-Fi:** When using public Wi-Fi (hotels, airports, conference venues), all organisational traffic — including information transfers — passes through the VPN. No organisational data is transferred over public Wi-Fi without VPN protection.

### 4.6 Electronic Communication Restrictions

The following technical restrictions are enforced on electronic communication facilities to prevent data leakage:

- **Auto-forwarding:** Automatic forwarding of organisational email to external email addresses is technically disabled. Manual forwarding of classified information to personal or external email accounts is prohibited.
- **Auto-reply content:** Out-of-office replies to external recipients do not include sensitive information such as internal project names, customer names or details about the employee's location or travel plans.
- **Attachment size limits:** Maximum attachment sizes are configured on the email gateway. Files exceeding the limit are redirected to the approved secure file transfer service.
- **Print jobs:** Classified documents sent to network printers use secure print (badge-release or PIN). Print data stored on printer internal storage is encrypted where the device supports it, and is automatically deleted after printing.

### 4.7 SMS & Instant Messaging

Short message services (SMS) and instant messaging carry inherent risks for information security:

- SMS messages and standard instant messages (WhatsApp personal, Telegram, consumer Signal groups) are not used to transmit information classified CONFIDENTIAL or above. These services may store messages on servers outside the organisation's control, display content on lock screens visible to bystanders and lack enterprise audit logging.
- For time-critical communications that require mobile reach, the organisation's approved enterprise messaging platform (with end-to-end encryption and enterprise key management) is used instead.
- If a brief, non-classified notification is sent via SMS or consumer messaging (e.g. "please check your email"), it contains no classified content, no customer names and no project details.

### 4.8 Fax & Legacy Communication

Fax machines and fax-over-IP services present specific security risks:

- **Built-in message stores:** Fax machines may retain copies of sent and received documents in internal memory, which can be accessed by unauthorised persons. After transmitting classified documents, the fax memory is cleared.
- **Misdial risk:** Accidental or deliberate misprogramming of fax numbers can result in classified information being sent to incorrect recipients. Personnel verify the fax number with the recipient by phone before sending CONFIDENTIAL information.
- **Preferred alternatives:** Where possible, encrypted electronic transfer methods are used instead of fax. If fax is the only available channel (e.g. for certain government or legal communications), a secure fax-over-IP solution with encryption and access logging is preferred over traditional analogue fax.

## 5. Physical Storage Media Transfer

Physical transfer includes the dispatch, transport and receipt of documents, USB drives, external hard drives, backup tapes, optical discs and other tangible media containing information. All physical media containing classified information are encrypted before dispatch (AES-256 full-disk or container encryption); the decryption key is transmitted via a separate channel.

### 5.1 Dispatch & Receipt Responsibilities

Clear responsibilities are assigned for each stage of physical information transfer:

- **Authorisation:** The information owner authorises the dispatch of physical media containing CONFIDENTIAL or higher information. For INTERNAL information, the sending department head approves dispatch.
- **Dispatch notification:** The sender notifies the recipient in advance (via a separate channel such as email or phone) that a physical transfer is en route, including the expected delivery date and a reference number.
- **Receipt confirmation:** The recipient confirms receipt to the sender within one business day using the reference number. If confirmation is not received within the expected timeframe, the sender escalates to the Information Security Officer.

### 5.2 Addressing & Transportation

Physical transfers are addressed and transported securely:

- **Addressing:** The recipient's full name, department and organisational address are clearly printed on the outer packaging. For classified material, the outer packaging carries no indication of the sensitivity of the contents — only the routing information.
- **Tracking:** Transfers of CONFIDENTIAL or higher media use tracked delivery services with shipment tracking numbers. The tracking number is recorded in the transfer log.
- **Delivery failures:** If a delivery fails, is returned or is reported as lost, the sender and the Information Security Officer are notified immediately. The incident is assessed for potential data exposure and handled through the incident management process.

### 5.3 Packaging & Environmental Protection

Packaging protects the contents against physical damage and environmental factors during transit:

- **Paper documents:** CONFIDENTIAL and above documents are placed in opaque, sealed envelopes. For STRICTLY CONFIDENTIAL material, double enveloping is used.
- **Storage media:** USB drives, hard drives, tapes and optical discs are packaged in padded, anti-static containers that protect against impact, heat, moisture and electromagnetic fields in accordance with the manufacturer's storage and transport specifications.
- **Minimum standard:** All physical transfers use opaque packaging at minimum. Transparent bags, open trays or unsealed envelopes are not used for classified material.

### 5.4 Courier & Transport Service Management

- **Authorised courier list:** A management-approved list of authorised and reliable courier services is maintained. Couriers are evaluated based on security capabilities, track record, insurance coverage and relevant certifications. The list is reviewed annually and after any courier-related security incident.
- **Classification-based service tiers:** The approved courier list differentiates by classification level. Standard postal or parcel services are acceptable for INTERNAL material. CONFIDENTIAL and STRICTLY CONFIDENTIAL material is transported only by courier services that offer tracked, signed-for and insured delivery with defined chain-of-custody procedures.
- **Courier identification standards:** Courier personnel identify themselves upon pickup and delivery with a valid photo ID and company credentials. For STRICTLY CONFIDENTIAL transfers, a pre-shared reference number is additionally required for verification.
- **Verification procedures:** Personnel at pickup and delivery points verify the courier's identity by checking photo ID against the pre-registered name, confirming the courier company affiliation and validating the shipment reference number. The courier's identity details are recorded in the dispatch/receipt log.

### 5.5 Tamper Protection

Tamper-evident or tamper-resistant controls are applied based on the classification level of the information being transported:

- **INTERNAL:** Standard sealed envelopes or packages are sufficient.
- **CONFIDENTIAL:** Tamper-evident seals (security tape, serialised tamper-evident bags) are applied. The seal number is recorded in the transfer log and communicated to the recipient via a separate channel.
- **STRICTLY CONFIDENTIAL:** Tamper-resistant containers (locked bags, security cases) are used in addition to tamper-evident seals. The container and seal are inspected by the recipient upon arrival; any signs of tampering are immediately reported to the Information Security Officer.

### 5.6 Physical Transfer Logging

A standardised log is maintained for all physical information transfers, capturing:

- Content description (what is being transferred — document title, media type, number of items)
- Classification level of the transferred information
- Protection measures applied (encryption, tamper-evident seals with serial numbers, packaging type)
- List of authorised recipients
- Handover time to the courier or transit custodian
- Receipt confirmation time at the destination
- Identity of persons involved at each stage (sender, courier, recipient)

The physical transfer log template is available on the intranet. Completed logs are retained in accordance with the retention schedule.

## 6. Verbal Transfer

Verbal transfer includes face-to-face conversations, telephone calls, video conferences and voice messages. While verbal communication leaves fewer traces than electronic or physical transfer, it is equally subject to interception and eavesdropping risks.

### 6.1 Conversation Security

- **Location awareness:** Confidential verbal conversations are not conducted in public places (restaurants, trains, airport lounges, open co-working spaces) or over insecure communication channels (unencrypted phone lines, consumer video conferencing without end-to-end encryption). If a sensitive discussion is necessary while travelling, it takes place in a private setting (closed hotel room, booked meeting room) using the organisation's approved encrypted communication tools.
- **Participant screening:** Before discussing information classified CONFIDENTIAL or above, the meeting organiser verifies that all participants (in person and remote) are authorised to receive information at that classification level. Uninvited or unverified participants are asked to leave before classified information is discussed.
- **Room controls:** Sensitive conversations take place in rooms with appropriate physical controls — closed doors, adequate sound insulation, no visibility of screens or whiteboards from outside. For STRICTLY CONFIDENTIAL discussions, designated secure meeting rooms with verified soundproofing are used. Mobile phones of non-essential attendees are left outside or placed in a signal-blocking container where the sensitivity warrants it.

### 6.2 Voicemail & Answering Machines

Messages containing classified information are not left on voicemail systems or answering machines. These systems can be:

- Replayed by unauthorised persons who share access to the mailbox
- Stored on shared or communal systems with insufficient access controls
- Accidentally recorded on the wrong mailbox due to misdialling

If the intended recipient is unavailable, the caller leaves a non-sensitive callback request (name, phone number, "please call back regarding project X") without disclosing classified content. The substantive discussion takes place when direct voice contact is established.

### 6.3 Classification Disclaimer

Sensitive conversations begin with a brief classification disclaimer so that all participants understand the handling requirements:

- The speaker announces the classification level of the information about to be discussed (e.g. "The following information is classified CONFIDENTIAL and is shared on a need-to-know basis").
- If the conversation covers topics at different classification levels, the speaker announces the transition when moving to a higher level.
- At the end of the conversation, the speaker reminds participants of any handling restrictions (e.g. "Please do not discuss these details outside this group").

## 7. Third-Party Transfer Agreements

Where [YOUR_ORGANISATION_NAME] regularly exchanges information with external parties (customers, suppliers, partners, regulators), formal transfer agreements are established and maintained:

- **Agreement scope:** The agreement specifies the types of information exchanged, the classification levels involved, the permitted transfer channels, the protection measures required and the responsibilities of each party.
- **Recipient authentication:** The agreement defines how recipients authenticate themselves before receiving classified information (e.g. pre-shared reference numbers, digital certificates, designated contact persons).
- **Confidentiality clauses:** For CONFIDENTIAL or higher information, a non-disclosure agreement (NDA) or equivalent confidentiality clause is signed before the first transfer. The NDA specifies how the receiving party stores, protects and eventually returns or destroys the information.
- **Incident reporting:** The agreement includes a mutual obligation to report security incidents affecting transferred information within an agreed timeframe.
- **Review:** Transfer agreements are reviewed annually and updated when the scope of information exchange changes, when security requirements change or after a security incident involving the third party.

## 8. Roles & Responsibilities

- **Top Management:** Approves this policy and third-party transfer agreements that involve STRICTLY CONFIDENTIAL information. Ensures adequate resources for secure transfer infrastructure.
- **Information Security Officer (ISO):** Maintains this policy, defines transfer security controls, reviews transfer agreements, investigates transfer-related incidents and maintains the transfer contact directory.
- **IT Department:** Operates and monitors transfer infrastructure (email gateways, file transfer services, DLP systems, VPN). Maintains the approved service register. Implements technical controls (auto-forwarding blocks, malware scanning, encryption enforcement). Evaluates new transfer services for security and compatibility.
- **Data Protection Officer (DPO):** Reviews transfer arrangements involving personal data for GDPR compliance. Advises on cross-border transfer mechanisms and data processing agreements with transfer service providers.
- **Information Owners / Asset Owners:** Authorise transfers of their information, maintain authorised recipient lists, define classification-specific handling requirements and approve third-party transfer agreements for their information assets.
- **Facility Management / Mail Room:** Operates physical transfer processes (dispatch, receipt, courier coordination). Verifies courier identification. Maintains the physical transfer log.
- **All Personnel:** Follow this policy when transferring information by any means. Verify recipient authorisation and transfer channel appropriateness. Report misdirected, lost or tampered transfers immediately.

## 9. Review & Maintenance

This policy is reviewed:

- At least annually as part of the ISMS management review cycle.
- When new transfer technologies or services are introduced (e.g. new collaboration platform, new file-sharing service, new courier provider).
- After significant security incidents involving information transfer (data leakage, misdirected communication, courier loss).
- When changes to applicable law affect transfer requirements (e.g. new cross-border data transfer rules, updated electronic signature regulations, sector-specific transfer obligations).
- When the organisation's classification scheme or labelling procedures are materially updated.
