# Acceptable Use Policy

> **Document control**  
> Owner: [POLICY_OWNER_ROLE, e.g. Information Security Officer]  
> Approved by: [APPROVER_NAME_AND_ROLE]  
> Version: [VERSION]  
> Effective date: [EFFECTIVE_DATE]  
> Next review: [NEXT_REVIEW_DATE]

## 1. Legal/Regulatory Basis

ISO/IEC 27001:2022 / ISO/IEC 27002:2022, Annex A — Organisational Controls:

- A 5.10 — Acceptable Use of Information and Other Associated Assets

BSI IT-Grundschutz:

- ISMS.1.A2 (Definition of Security Objectives and Strategy)
- ORP.3.A3 (Instruction of Personnel in the Secure Use of IT)
- CON.9 (Information Exchange)
- CON.7.A2 (Security Awareness for Personnel)

Additional jurisdiction-specific laws and regulations — in particular data protection, telecommunications and employment law — are listed in the Legal Register and are incorporated by reference.

## 2. Purpose & Scope

This policy defines the rules for the acceptable use of information and other associated assets at **[YOUR_ORGANISATION_NAME]**. It establishes clear boundaries between permitted and prohibited behaviour to protect the organisation's information assets, reputation and legal standing.

This policy applies to:

- All employees (permanent, temporary, part-time)
- External personnel (contractors, consultants, temporary staff) with access to organisational assets
- All information assets regardless of format (digital, paper, verbal)
- All associated assets: hardware (laptops, mobile devices, printers), software, cloud services, network infrastructure, storage media and communication systems provided or approved by the organisation

Personnel are required to familiarise themselves with this policy, acknowledge it in writing, and comply with its provisions. Violation of this policy may result in disciplinary action as defined in the *HR Security Policy*.

## 3. Behavioural Expectations & Prohibited Actions

All personnel of [YOUR_ORGANISATION_NAME] are expected to use information and associated assets responsibly, professionally and in a manner consistent with the organisation's security objectives. Assets are provided for business purposes; limited personal use is tolerated provided it does not interfere with work duties, compromise security or violate this policy.

### 3.1 Expected Behaviour Standards

All personnel:

- Lock their workstation (Win+L / Ctrl+Cmd+Q) when leaving the desk, even briefly.
- Follow the clean desk policy: no classified documents left unattended on desks, printers or whiteboards.
- Use strong, unique passwords for each system and never share credentials with anyone, including IT support.
- Report suspected security incidents, phishing emails and policy violations immediately to the Information Security Officer or via the designated reporting channel.
- Verify the identity and authorisation of individuals requesting access to information before sharing it.
- Handle information in accordance with its classification level as defined in the Information Classification Policy.

### 3.2 Explicitly Prohibited Actions

The following actions are strictly prohibited:

- Attempting to bypass, disable or circumvent security controls (firewalls, endpoint protection, DLP systems, access controls).
- Accessing, storing or distributing illegal, offensive, discriminatory or pornographic content using organisational assets.
- Using organisational systems for unauthorised commercial activities, political campaigning or cryptocurrency mining.
- Connecting unauthorised network equipment (routers, switches, wireless access points) to the corporate network.
- Sharing organisational credentials or access tokens with third parties, including family members.
- Forwarding work emails to personal email accounts to circumvent data-loss controls.
- Photographing or screen-capturing classified information without authorisation from the information owner.
- Impersonating other users or using another person's account.

### 3.3 Internet & Email Use

Internet access and email are provided as business tools. The following rules apply:

- **Permitted:** Business-related research, professional development, access to cloud services approved by IT, limited personal browsing during breaks (news, banking, travel) that does not involve prohibited content categories.
- **Prohibited:** Downloading pirated software, media or other copyrighted material; accessing hacking tools or exploit databases for non-authorised purposes; streaming high-bandwidth media during business hours unless required for work; using anonymous proxy services or VPN tunnels to bypass web filtering.
- **Email:** Attachments classified above INTERNAL are encrypted before sending externally. Personnel verify recipient addresses before sending sensitive emails. Auto-forwarding to external addresses is technically blocked. Suspicious emails are reported, not forwarded.

### 3.4 Social Media

Personnel may access social media for professional purposes (LinkedIn, industry forums). The following restrictions apply:

- Do not disclose [YOUR_ORGANISATION_NAME]'s internal projects, customer information, financial data or security architecture on social media platforms.
- Do not post photographs of workplaces, whiteboards, screens or documents that may reveal classified information.
- Clearly distinguish personal opinions from official [YOUR_ORGANISATION_NAME] positions when posting in a professional context.
- Do not accept connection requests from unknown individuals claiming to be colleagues or partners without verification.

### 3.5 AI Tools & Cloud Services

The use of artificial intelligence tools and external cloud services is subject to the following rules:

- **Approved tools only:** Only AI tools and cloud services explicitly approved by IT and listed in the approved software register may be used for business purposes.
- **No classified data in public AI:** Personnel do not enter information classified above PUBLIC into public AI services (e.g. ChatGPT, Gemini, Midjourney) unless the tool has been specifically approved with appropriate data processing agreements in place.
- **Output verification:** AI-generated outputs used in business decisions, customer communications or official documents are reviewed and verified by a qualified person before use.
- **Shadow IT:** Creating accounts on unapproved cloud services (file sharing, project management, communication) to handle organisational data is prohibited. Report unmet needs to IT so that approved alternatives can be evaluated.

### 3.6 Software Installation

The following rules apply to software on organisational devices:

- Software may only be installed from the organisation's approved software catalogue or with explicit written approval from IT.
- Browser extensions are approved by IT before installation; unapproved extensions are blocked via group policy.
- Open-source software may only be used if it has been reviewed and approved through the organisation's software approval process.
- Personnel do not disable automatic updates or endpoint protection software.

### 3.7 Removable Media & Mobile Devices

The use of removable media and mobile devices is subject to the following restrictions:

- **USB drives:** Only organisation-issued, encrypted USB drives are used. Personal USB drives, external hard drives and SD cards are prohibited on organisational systems.
- **Mobile devices:** Company-issued mobile devices are protected with a PIN/biometric lock and device encryption. Lost or stolen devices are reported to IT immediately for remote wipe.
- **Personal devices (BYOD):** Use of personal devices for work purposes is only permitted if enrolled in the organisation's mobile device management (MDM) solution and compliant with the BYOD policy.

### 3.8 Printing & Physical Media

The following rules apply to printed documents and physical information carriers:

- Classified documents are only printed when necessary and collected from the printer promptly. The secure print function (release only after PIN entry at the printer) is used where available.
- Printouts of classified or restricted information are destroyed via cross-cut shredding (DIN 66399, minimum P-3) after use — not disposed of via standard waste bins.
- Classified documents are not left on open desks, in meeting rooms or in publicly accessible areas.

## 4. Monitoring & Transparency

[YOUR_ORGANISATION_NAME] monitors the use of its information assets and associated infrastructure to detect security threats, policy violations and unauthorised access. Monitoring is conducted within the boundaries of applicable law and in a manner that respects the privacy and dignity of personnel.

### 4.1 Scope of Monitoring

The following monitoring activities are performed:

- **Network traffic:** Internet traffic is logged by category (e.g. web filtering logs). Encrypted traffic is inspected at the gateway level where technically implemented and legally permitted.
- **Email:** Inbound and outbound email is scanned for malware, spam and data-loss indicators (e.g. classification labels in attachments sent to external recipients). Email content is not routinely read by administrators.
- **Endpoint protection:** Endpoint detection and response (EDR) tools monitor for malware, unauthorised software and anomalous behaviour on all managed devices.
- **Access logs:** Authentication events, privilege escalations and access to classified information are logged and retained for audit purposes.
- **Physical access:** Entry to secured areas is logged via access control systems (badge readers, biometrics).

### 4.2 What Is Not Monitored

The following are explicitly excluded from monitoring to protect employee privacy:

- Screen recording or keystroke logging of individual users (except during authorised forensic investigations).
- Content of private communications during permitted personal use, unless flagged by automated DLP or malware detection.
- GPS tracking of company vehicles or mobile devices outside of working hours.

### 4.3 Legal Basis & Employee Notification

Monitoring is conducted on the following legal bases:

- Legitimate interest of the employer in protecting its information assets (Art. 6(1)(f) GDPR).
- Compliance with legal obligations (Art. 6(1)(c) GDPR) where applicable sector regulations require logging.
- Works council agreement where a works council exists, covering scope, purpose and retention of monitoring data.

All personnel are informed about the scope and purpose of monitoring:

- During the onboarding process as part of the information security briefing.
- Through this policy, which is published on the organisation's intranet and acknowledged in writing.
- Via the organisation's privacy notice for employees.

### 4.4 Privacy Safeguards

The following safeguards are in place to prevent abuse of monitoring capabilities:

- Monitoring data is accessible only to authorised personnel (Information Security Officer, IT Security team and — where legally required — the works council or data protection officer).
- Individual-level analysis (linking logs to a specific person) requires a documented reason and approval from the Information Security Officer and the Data Protection Officer.
- Monitoring logs are retained for the minimum period required by the retention schedule and then securely deleted.
- Any investigation based on monitoring data follows the organisation's incident response process and respects the principle of proportionality.

## 5. Asset Handling Procedures

The following procedures govern the handling of information and associated assets throughout their lifecycle at [YOUR_ORGANISATION_NAME]. These procedures supplement the organisation's classification scheme and ensure that assets are protected commensurate with their classification level.

### 5.1 Classification-Based Access Restrictions

Access to information and associated assets is restricted based on the classification level assigned under the organisation's classification scheme:

- **PUBLIC:** No access restrictions. Available to all personnel and the general public.
- **INTERNAL:** Access limited to employees and authorised external personnel. Shared drives, intranet sites and collaboration spaces enforce membership-based access.
- **CONFIDENTIAL:** Access restricted to specifically authorised individuals on a need-to-know basis. Access is approved by the information owner and enforced through role-based access control (RBAC).
- **STRICTLY CONFIDENTIAL:** Access limited to named individuals with explicit written authorisation from the information owner and senior management. Access is logged and reviewed quarterly.

When in doubt about a user's authorisation level, personnel deny access and refer the request to the information owner for decision.

### 5.2 Authorised User Management

A register of authorised users is maintained for information and associated assets classified CONFIDENTIAL or above:

- The information owner maintains and periodically reviews the list of individuals authorised to access their assets.
- Access rights are reviewed at least every six months, upon role change and upon termination.
- The register includes the user's name, role, scope of access (read/write/admin), date of authorisation and the authorising owner.
- Temporary access (e.g. for projects or audits) is time-limited and automatically revoked upon expiration.
- IT maintains a corresponding technical access control list (ACL) that reflects the owner's authorisation register.

### 5.3 Protection of Copies

Copies of information — whether temporary or permanent, digital or physical — are protected at the same level as the original:

- Copies inherit the classification level and handling rules of the source information.
- Creating copies of CONFIDENTIAL or STRICTLY CONFIDENTIAL information requires authorisation from the information owner.
- The number of copies is kept to the minimum necessary for the intended purpose.
- Backup copies are subject to the same access controls and encryption requirements as the originals.
- When the purpose for which a copy was made no longer exists, the copy is securely disposed of in accordance with the disposal procedures below.

### 5.4 Storage Requirements

Information and associated assets are stored in accordance with manufacturer specifications and the organisation's protection requirements:

- Electronic storage media (hard drives, SSDs, tapes) are stored within the environmental conditions specified by the manufacturer (temperature, humidity, electromagnetic exposure).
- Classified digital information is stored on encrypted storage in access-controlled environments.
- Physical documents classified CONFIDENTIAL or above are stored in locked cabinets or safes when not in active use.
- Storage locations are documented, including any off-site or cloud storage locations.
- Storage conditions are reviewed periodically as part of asset management to ensure continued compliance with manufacturer and organisational requirements.

### 5.5 Marking of Storage Media

All copies of storage media are clearly marked to indicate their content and classification level:

- Physical storage media (USB drives, external hard drives, backup tapes, optical discs) carry a visible label indicating the highest classification level of the data stored on them.
- Labels include the classification level, a brief description of the content, the owner and the date of creation.
- Where physical labelling is impractical (e.g. micro SD cards), the containing case or envelope is labelled instead.
- Digital media labelling is implemented through file naming conventions, metadata and directory structures as defined in the Labelling of Information policy.
- Unlabelled storage media is treated as containing CONFIDENTIAL information until the content is verified and appropriately marked.

### 5.6 Disposal Authorisation & Methods

Disposal of information and associated assets is authorised and performed using methods appropriate to the classification level:

- **Authorisation:** Disposal of assets classified CONFIDENTIAL or above requires written authorisation from the information owner. Disposal of STRICTLY CONFIDENTIAL assets additionally requires approval from the Information Security Officer.
- **Paper documents:** Cross-cut shredding in accordance with DIN 66399 — security level P-3 for INTERNAL, P-4 for CONFIDENTIAL, P-5 or higher for STRICTLY CONFIDENTIAL.
- **Digital storage:** Secure deletion using approved tools (e.g. multi-pass overwrite, cryptographic erasure). For STRICTLY CONFIDENTIAL data, physical destruction of the storage medium is required.
- **Equipment:** Before disposal, reassignment or return of equipment (laptops, mobile devices, printers), all organisational data is securely wiped. Hard drives in devices that processed STRICTLY CONFIDENTIAL data are physically destroyed.
- **Documentation:** All disposal activities are documented, including the asset identifier, classification level, disposal method used, date and the person who performed the disposal. Destruction certificates are obtained from external disposal service providers.

## 6. Consequences of Policy Violations

Violations of this policy are treated in accordance with [YOUR_ORGANISATION_NAME]'s disciplinary process as defined in the *HR Security Policy*. All personnel are expected to report observed or suspected violations without fear of retaliation.

### 6.1 Escalation Levels

Depending on the severity, intent and recurrence of the violation, the following measures may be applied:

- **Level 1 — Minor / first-time unintentional violation:** Verbal warning, documented discussion with line manager and mandatory refresher training on the relevant topic.
- **Level 2 — Repeated or negligent violation:** Written warning with documented corrective actions; temporary restriction of access rights pending completion of additional training.
- **Level 3 — Serious violation or wilful disregard:** Formal disciplinary hearing; suspension of all access rights pending investigation; involvement of HR and legal counsel.
- **Level 4 — Violation with material damage or criminal conduct:** Termination of employment or contract in accordance with applicable labour law; referral to law enforcement where criminal activity is suspected; pursuit of civil remedies for damages incurred.

The assessment considers the nature and gravity of the breach, whether the action was intentional or accidental, whether the individual had received adequate training and whether this is a first or repeated offence.

## 7. Roles & Responsibilities

- **Top Management:** Approves this policy, ensures adequate resources for implementation and sets the organisational expectation for responsible use of information assets.
- **Information Security Officer (ISO):** Maintains this policy, defines acceptable use rules in coordination with IT and HR, monitors compliance, investigates violations and coordinates monitoring activities within legal boundaries.
- **IT Department:** Implements and operates technical controls (web filtering, DLP, endpoint protection, MDM, secure print), maintains the approved software register and supports the ISO in monitoring and incident response.
- **Data Protection Officer (DPO):** Ensures that monitoring activities comply with data protection legislation, reviews works council agreements related to monitoring and advises on privacy-preserving approaches.
- **Human Resources (HR):** Communicates this policy during onboarding, ensures written acknowledgement, initiates the disciplinary process for violations and maintains training records.
- **Line Managers:** Ensure that their team members are aware of and comply with this policy, escalate observed violations and support the enforcement of corrective actions.
- **Information Owners (Asset Owners):** Maintain authorised user registers for their assets, authorise copies and disposal and define classification-specific access restrictions.
- **All Personnel:** Read, acknowledge and comply with this policy. Report suspected violations, security incidents and unmet tool or service needs through the appropriate channels.

## 8. Review & Maintenance

This policy is reviewed:

- At least annually as part of the ISMS management review cycle.
- When new technologies are introduced that affect acceptable use (e.g. new AI tools, collaboration platforms, BYOD changes).
- After significant security incidents involving misuse of information or assets.
- When changes to applicable law affect monitoring, data protection or employee rights (e.g. new data-protection requirements, amendments to telecommunications or labour legislation).
- When the organisation's classification scheme or asset management processes are materially updated.
