# Remote Working & BYOD Policy

> **Document control**  
> Owner: [POLICY_OWNER_ROLE, e.g. Information Security Officer]  
> Approved by: [APPROVER_NAME_AND_ROLE]  
> Version: [VERSION]  
> Effective date: [EFFECTIVE_DATE]  
> Next review: [NEXT_REVIEW_DATE]

## 1. Legal/Regulatory Basis

ISO/IEC 27001:2022 / ISO/IEC 27002:2022, Annex A — People Controls:

- A 6.7 — Remote Working

BSI IT-Grundschutz:

- OPS.1.2.4 (Teleworking — Rules, Security Concept, Communication)
- INF.8 (Working from Home — Physical Security, Access Control)
- INF.9 (Mobile Workplace — Selection, Rules, Visual Privacy)
- NET.3.3 (VPN — Planning, Configuration, Access Management)

Additional jurisdiction-specific laws — in particular labour law, data protection law (GDPR), occupational health and safety regulations and works council co-determination rules — are listed in the Legal Register and incorporated by reference.

## 2. Purpose & Scope

This policy establishes the information security requirements for remote working at **[YOUR_ORGANISATION_NAME]**. It covers all forms of work performed outside the organisation's premises, including home offices, mobile workplaces, co-working spaces and any other location where personnel access organisational information via ICT equipment.

This policy applies to:

- All employees who work remotely (full-time, part-time, occasional)
- External personnel (contractors, consultants, temporary staff) performing work outside organisational premises
- All devices used for remote access, including organisation-owned and, where explicitly permitted, privately-owned devices (BYOD)

The objective is to ensure that information processed, stored and transmitted during remote work receives the same level of protection as information handled within the organisation's premises, while enabling flexible working arrangements.

## 3. Security Conditions & Risk Considerations (A 6.7)

[YOUR_ORGANISATION_NAME] permits remote working activities under the conditions and restrictions set out in this policy. Before personnel begin remote work, the applicable security requirements are communicated and acknowledged. The following conditions apply to all remote working arrangements:

### 3.1 Physical Security of Remote Locations

- **Location Security Assessment:** Before commencing remote work at a new location, personnel complete a self-assessment checklist that evaluates the physical security of the site. The assessment covers building access controls, room lockability, the risk of unauthorised entry and any jurisdictional differences that affect applicable security and privacy law. Locations that do not meet the minimum criteria are not approved for processing sensitive information.
- **Approved Workplace Types:** Remote work takes place in home offices with a dedicated workspace, or in pre-approved co-working spaces that meet minimum infrastructure and privacy requirements. Public transport, open cafes and other locations where visual or auditory privacy cannot be maintained are not used for processing confidential or restricted information.
- **Physical Environment Rules:** Remote workplaces are equipped with a lockable cabinet or container for storing confidential documents and removable media. A clean desk practice applies at all remote locations. Confidential documents are transported between sites in sealed, non-transparent containers. Printing of confidential documents at the remote workplace is avoided where possible; where necessary, printouts are secured immediately and disposed of using a cross-cut shredder or returned to the organisation for secure destruction. Security incidents are reported immediately through the established reporting channels (see incident reporting policy).

### 3.2 Communication Security & Network Access

- **Encrypted Remote Access:** All remote access to the organisation's network is secured via a cryptographically protected VPN connection. The VPN configuration takes into account the sensitivity of the systems being accessed and the classification of information transmitted over the connection. Split tunnelling is disabled on VPN clients to prevent data leakage through unprotected channels.
- **Home & Public Network Rules:** Public Wi-Fi networks are only used in conjunction with the organisation's VPN. Home networks are configured to meet minimum security standards: WPA3 encryption (or WPA2 as a minimum), changed default router password, current router firmware, and a separate guest network where household IoT devices connect. Personnel verify these settings before commencing remote work and re-verify annually or after router replacement.
- **Authentication & Access Control:** Remote access to the organisation's network requires multi-factor authentication (MFA). Single-factor authentication (password only) is not permitted for remote network access. Access privileges granted for remote sessions follow the principle of least privilege and are limited to the systems and data required for the assigned tasks.

### 3.3 Remote Access Technologies

- **Virtual Desktop & Remote Access:** Where privately owned equipment is used for remote work (BYOD), access is provided exclusively through a virtual desktop infrastructure (VDI) or comparable remote access solution. This ensures that organisational data is processed and stored on organisation-controlled systems, not on the private device itself. Direct storage of organisational information on privately owned devices is prohibited unless explicitly approved and encrypted.
- **Secure Deployment & Initialisation:** Remote work devices are provisioned and initialised through a centralised, automated process. Operating system images, security configurations and required software are deployed using the organisation's endpoint management system. Manual setup of remote work devices by end users is not permitted. Changes to security configurations require IT authorisation.

### 3.4 Protection Against Unauthorised Access

- **Protection at Home:** At home offices, screens are positioned so that household members and visitors cannot view their content. When leaving the workstation — even briefly — the screen is locked. Confidential phone calls and video conferences are conducted in a closed room. Children and other household members do not have access to work devices, and work devices are stored in a locked space when not in use.
- **Protection in Public:** When working in public or semi-public locations, a privacy screen filter is used on all devices. Confidential or restricted information is not displayed or discussed in environments where third parties can observe or overhear. Devices are never left unattended; when personnel leave their seat (e.g. in a train or airport lounge), all devices and documents are taken along or secured.

### 3.5 Endpoint Security Measures

- **Firewall & Malware Protection:** Every device used for remote work has an active, centrally managed host firewall and up-to-date anti-malware software. The firewall is configured to block all inbound connections that are not explicitly required. Anti-malware definitions are updated automatically at least daily. Real-time scanning is enabled and cannot be disabled by the user.

## 4. Implementation Measures for Remote Working

The following measures are implemented by [YOUR_ORGANISATION_NAME] to support secure remote working arrangements:

### 4.1 Equipment & Workspace Provisioning

- **Equipment Provisioning:** The organisation provides all equipment required for remote work, including laptops, monitors, docking stations, keyboards and lockable storage furniture. The use of privately owned devices for processing organisational information is not permitted unless explicitly authorised through the BYOD approval process. All organisation-issued equipment is asset-tagged, inventoried and subject to the organisation's asset management procedures.
- **Physical Workspace Security:** The home office workspace is located in a separate room or a clearly delineated area that can be secured against unauthorised access. Windows and doors are closed and locked when the workspace is unoccupied. Smoke detectors and adequate power supply (surge protection) are available. Personnel working from locations with elevated burglary risk take additional protective measures (e.g. security locks, alarm systems) as recommended by the organisation.

### 4.2 Permitted Work & Access Authorisation

- **Permitted Work & Information Classification:** The line manager and the Information Security Officer jointly determine which tasks are permitted for remote execution, which information classification levels are handled remotely and which internal systems and services the remote worker is authorised to access. Information classified as STRICTLY CONFIDENTIAL is not processed remotely unless an explicit risk assessment has been completed and approved. These authorisations are documented and reviewed annually.
- **Family & Visitor Access Rules:** Household members and visitors do not use organisation-owned equipment under any circumstances. Work equipment is stored in a locked room or locked cabinet when not actively in use. Video calls and screen-sharing sessions are conducted in a location where household members and visitors cannot view the screen or overhear the conversation.

### 4.3 Remote Working Training

- **Remote Working Training:** All personnel who work remotely and all IT support staff who assist remote workers complete a dedicated remote working security training before commencing remote work. The training covers secure handling of equipment and information outside the office, VPN usage, clean desk practices, incident reporting, physical security of the remote workplace and the proper handling of confidential calls and video conferences. Refresher training takes place annually and whenever this policy is updated.

### 4.4 Mobile Device Management & Security

- **Device Security Controls:** All remote access devices are enrolled in the organisation's Mobile Device Management (MDM) or endpoint management platform. The following security controls are enforced centrally: automatic screen lock after a maximum of 5 minutes of inactivity, strong passcode or biometric unlock, full-disk encryption, device location tracking (enabled with personnel consent in accordance with data protection law) and remote wipe capability. Lost or stolen devices are reported immediately, and a remote wipe is initiated without delay.

### 4.5 Support, Maintenance & Insurance

- **Hardware & Software Support:** The IT department provides remote support for all organisation-issued equipment via remote desktop tools and a dedicated helpdesk. For hardware defects that cannot be resolved remotely, a replacement device is shipped or the employee brings the device to the office. Designated IT contact persons and support hours are communicated to all remote workers. Remote maintenance and troubleshooting sessions are logged.
- **Insurance Coverage:** The organisation maintains appropriate insurance coverage for equipment used at remote workplaces, including coverage for theft, damage and transport. Personnel are informed about the scope of coverage and their obligation to report damage or loss promptly.

### 4.6 Backup & Business Continuity

- **Backup & Business Continuity:** Data created or modified during remote work is stored on organisation-managed systems (network drives, cloud storage) rather than on local devices. Where local storage is unavoidable, automatic synchronisation to the central backup infrastructure is configured. Remote workers verify regularly that their data synchronisation is functioning correctly. Business continuity plans account for scenarios in which remote workers lose connectivity or equipment, and alternative work procedures are documented.

### 4.7 Audit & Security Monitoring

- **Audit & Security Monitoring:** Remote access sessions are logged centrally, including user identity, connection time, duration and accessed resources. Logs are reviewed regularly for anomalies (e.g. access from unusual locations, connections outside working hours, failed authentication attempts). The organisation reserves the right to audit remote workplaces for compliance with this policy, with appropriate advance notice and in accordance with data protection law. Findings from audits feed into the continuous improvement of this policy.

### 4.8 Termination of Remote Working Arrangements

- **Termination of Remote Working:** When a remote working arrangement ends — whether due to role change, end of employment or organisational decision — all remote access rights are revoked immediately. All organisation-owned equipment (laptops, monitors, docking stations, storage furniture, access tokens) is returned within five business days. A documented handover checklist is completed. VPN credentials and certificates specific to the remote arrangement are deactivated on the same day the arrangement ends.

## 5. Roles & Responsibilities

- **Top Management:** Approves this policy, provides resources for secure remote working infrastructure and sets the strategic direction for remote work.
- **Information Security Officer (ISO):** Defines security requirements for remote working, conducts risk assessments for remote work scenarios, monitors compliance and updates this policy.
- **IT Department:** Provisions and manages remote work equipment, operates VPN and MDM infrastructure, provides helpdesk support and implements technical controls.
- **Human Resources (HR):** Incorporates remote working conditions into employment contracts, coordinates remote working agreements and manages the onboarding/offboarding of remote workers.
- **Line Managers:** Approve remote work arrangements for their team, determine permitted tasks and information classifications and verify that team members comply with this policy.
- **All Remote Workers:** Comply with this policy, complete required training, secure their remote workplace and report security incidents immediately.

## 6. Review & Maintenance

This policy is reviewed:

- At least annually as part of the ISMS management review cycle.
- After significant changes to the remote working infrastructure or technology landscape.
- After security incidents related to remote working.
- When changes in applicable law (labour law, data protection, occupational health) affect remote working conditions.
