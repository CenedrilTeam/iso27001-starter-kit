# Security Operations Policy

> **Document control**  
> Owner: [POLICY_OWNER_ROLE, e.g. Information Security Officer]  
> Approved by: [APPROVER_NAME_AND_ROLE]  
> Version: [VERSION]  
> Effective date: [EFFECTIVE_DATE]  
> Next review: [NEXT_REVIEW_DATE]

## 1. Legal/Regulatory Basis

ISO/IEC 27001:2022 / ISO/IEC 27002:2022, Annex A — Organisational & Technological Controls:

- A 5.5 — Contact with Authorities
- A 5.6 — Contact with Special Interest Groups
- A 5.7 — Threat Intelligence
- A 5.24 — Information Security Incident Management Planning and Preparation
- A 5.25 — Assessment and Decision on Information Security Events
- A 5.26 — Response to Information Security Incidents
- A 5.27 — Learning from Information Security Incidents
- A 5.28 — Collection of Evidence
- A 8.8 — Management of Technical Vulnerabilities
- A 8.32 — Change Management

BSI IT-Grundschutz:

- DER.2.1 — Security Incident Handling (A1 Incident Definition, A2 Incident Handling Policy, A3 Responsibilities, A4 Notification, A5 Remediation, A6 Recovery, A7 Procedures, A8 Organisational Structures, A9 Reporting Channels, A10 Containment, A11 Classification, A14 Escalation Strategy, A16 Remediation Documentation, A17 Post-Incident Analysis, A18 Process Improvement, A22 Efficiency Review)
- DER.1 — Detecting Security-Relevant Events (A1 Detection Policy, A3 Reporting Paths, A4 Employee Awareness, A5 Built-in Detection Functions, A6 Continuous Monitoring, A12 Evaluation of External Information)
- DER.2.2 — IT Forensics (A1 Legal Framework, A2 First-Response Guide, A3 Forensic Provider Pre-selection, A5 Evidence Procedures, A8 Volatility Order, A10 Forensic Duplication, A11 Documentation, A12 Secure Storage)
- OPS.1.1.1 — General IT Operations (A9 IT Monitoring, A10 Vulnerability Inventory, A20 Vulnerability Testing, A22 Automated Testing)
- OPS.1.1.3 — Patch and Change Management (A1 Concept, A2 Responsibilities, A3 Autoupdate Configuration, A5 Change Requests, A6 Coordination, A7 Business Process Integration, A10 Integrity Verification, A15 Regular Updates)

Additional jurisdiction-specific laws — in particular NIS2, sector-specific breach notification obligations, data protection law (GDPR Article 33/34 breach notification), criminal procedure law and digital evidence admissibility rules — are listed in the Legal Register and incorporated by reference.

## 2. Purpose & Scope

This policy establishes the security operations framework at **[YOUR_ORGANISATION_NAME]**. It defines the requirements for external communication with authorities and interest groups, the collection and use of threat intelligence, the complete incident management lifecycle from planning through response and lessons learned, the management of technical vulnerabilities and the governance of changes to information systems.

This policy applies to:

- All information systems, applications and IT infrastructure operated by or on behalf of the organisation
- All personnel involved in security operations, incident response, vulnerability management and change management
- External service providers, cloud service providers and contractors with access to organisational systems
- All information security events, incidents and vulnerabilities regardless of origin

The objective is to ensure the organisation can prevent, detect, respond to and recover from information security threats in a structured, timely and effective manner while maintaining operational continuity and legal compliance.

## 3. External Relations & Communication

[YOUR_ORGANISATION_NAME] maintains established relationships with relevant authorities to facilitate timely reporting of information security incidents, to understand upcoming regulatory expectations and to receive early warnings about threats. The organisation specifies when and by whom authorities are to be contacted and how identified information security incidents are reported.

### 3.1 Authority Contact Register

The organisation maintains a current register of authority contacts. The register specifies the contact information, the circumstances under which contact is initiated, the responsible internal contact person and the communication method for each of the following authority types:

- **Law Enforcement:** Contact details for the relevant law enforcement agencies are documented, including the criteria triggering mandatory reporting (e.g. suspected criminal activity, data breaches exceeding legal thresholds). The Information Security Officer coordinates with legal counsel before initiating contact.
- **Regulatory Bodies:** Contacts with sector-specific regulatory bodies are maintained. Reporting timelines and formats prescribed by applicable regulations are documented and rehearsed. Regulatory obligations for breach notification (e.g. within 72 hours under GDPR) are observed.
- **Supervisory Authorities:** Contact information for data protection supervisory authorities and other relevant oversight bodies is current. The organisation monitors supervisory guidance and integrates expectations into its security operations.
- **Utilities:** Contact information for the landlord, water and power suppliers is documented. Procedures for notifying these parties in the event of physical security incidents or environmental emergencies are established.
- **Emergency Services:** Direct contact paths to emergency services are established and tested. All personnel are informed of the procedures for contacting emergency services in the event of a physical or environmental emergency.
- **Fire Department:** Contact information for the local fire department is posted visibly at all premises. Coordination procedures for fire drills and evacuation plans are documented.
- **Telecommunication Providers:** Contact information for telecommunication providers is maintained for the purpose of reporting service disruptions, requesting emergency line routing and coordinating incident response activities that involve network infrastructure.

The authority contact register is reviewed at least annually and updated whenever organisational, regulatory or personnel changes occur. Contact with authorities is also used proactively to understand current and upcoming expectations of these authorities regarding applicable information security regulations.

When a security incident occurs, all affected internal and external parties are notified promptly. Before notifying external parties, the organisation verifies whether the data protection officer, the works council or staff representation and the legal department need to be involved. Mandatory reporting obligations for public authorities and regulated sectors are identified in advance under applicable national supervisory laws and rehearsed periodically. The organisation maintains pre-drafted notification templates for each authority type to accelerate response times.

### 3.2 Engagement with Special Interest Groups

[YOUR_ORGANISATION_NAME] participates in relevant special interest groups, professional associations, security forums and information sharing communities. Membership in such groups serves the following purposes:

- **Best Practice Exchange:** The organisation improves its knowledge about best practices in information security and stays up to date with relevant security information through active participation in professional groups and industry associations.
- **Current Awareness:** Participation in interest groups ensures that the organisation's understanding of the information security environment remains current. Members receive briefings, publications and updates that reflect the latest developments.
- **Early Warnings:** Through memberships and subscriptions, the organisation receives early warnings of alerts, advisories and patches pertaining to attacks and vulnerabilities. This includes advisories from CERTs, ISACs and vendor security bulletins.
- **Specialist Advice:** The organisation gains access to specialist information security advice through its network of interest group contacts. This includes expert consultation on emerging threats, compliance challenges and incident response techniques.
- **Information Sharing:** The organisation shares and exchanges information about new technologies, products, services, threats and vulnerabilities with trusted partners. Information sharing agreements govern the confidentiality and permitted use of exchanged information.
- **Incident Liaison:** Interest group memberships provide suitable liaison points when dealing with information security incidents, enabling coordinated response with peer organisations and sector-specific incident response teams.

The Information Security Officer maintains a register of all memberships and subscriptions, reviews their value annually and ensures that information received is disseminated to relevant personnel within the organisation.

Information received through external channels is evaluated systematically. All personnel recognise messages arriving through these channels as potentially security-relevant and forward them to the appropriate internal point of contact. Information from reliable sources — including BSI advisories, CERT-Bund warnings, sector-specific ISACs and vendor bulletins — is assessed for its relevance to the organisation's own information domain. Where the information is relevant, it is escalated in accordance with the incident management process.

## 4. Threat Intelligence (A 5.7)

[YOUR_ORGANISATION_NAME] uses threat intelligence to prevent, detect and respond to threats. Information about existing or emerging threats is collected and analysed to facilitate informed actions that prevent threats from causing harm to the organisation and to reduce the impact of such threats. The collected threat intelligence is relevant (related to the protection of the organisation), insightful (providing an accurate understanding of the threat landscape), contextual (adding situational awareness based on the time of events, their occurrence and prevalence in similar organisations) and actionable (enabling the organisation to act quickly and effectively).

### 4.1 Intelligence Layers

Threat intelligence is structured into three layers, all of which are considered:

- **Strategic Threat Intelligence:** High-level information about the changing threat landscape is exchanged, including types of attackers, attack motivations, geopolitical developments and emerging categories of attacks relevant to the organisation's sector and geographic presence.
- **Tactical Threat Intelligence:** Information about attacker methodologies, tools and technologies is collected and analysed. This includes tactics, techniques and procedures (TTPs) used by threat actors, enabling the organisation to strengthen its defences against known attack patterns.
- **Operational Threat Intelligence:** Details about specific attacks are gathered, including technical indicators of compromise (IoCs) such as IP addresses, domain names, file hashes and malware signatures. These indicators feed into technical detection and prevention systems.

### 4.2 Intelligence Activities

The threat intelligence process encompasses the following activities:

- **Objective Setting:** The organisation establishes clear objectives for threat intelligence production, aligned with its risk profile, industry sector and the information assets it protects.
- **Source Selection:** Internal and external information sources that are necessary and appropriate for threat intelligence production are identified, vetted and selected. Sources include CERT-Bund CSAF feeds, CERT-EU Cyber Briefs, national CSIRT feeds (NCSC UK, BSI Cyber Security Warnings), industry ISACs, commercial threat feeds, open-source intelligence and internal telemetry data.
- **Collection:** Information is collected from selected internal and external sources on a continuous basis. Automated feeds are supplemented by manual research and human intelligence from security community participation. Advisories are enriched with CISA Known Exploited Vulnerabilities (KEV) data to identify actively exploited threats and EPSS (Exploit Prediction Scoring System) scores to assess exploitation probability within 30 days.
- **Processing:** Collected information is processed to prepare it for analysis. Processing includes translating, formatting, normalising, deduplicating and corroborating information from multiple sources.
- **Analysis:** Processed information is analysed to understand how it relates to and is meaningful to the organisation. Analysis assesses the credibility of the source, the relevance to the organisation's assets and the potential impact of identified threats.
- **Dissemination:** Analysed threat intelligence is communicated and shared to relevant individuals in a format that can be understood and acted upon. Strategic intelligence is provided to management, tactical intelligence to security architects and operational intelligence to the security operations team.

### 4.3 Use of Threat Intelligence

Analysed threat intelligence is used in the following ways:

- **Risk Management Integration:** Processes are implemented to include information gathered from threat intelligence sources into the organisation's information security risk management processes, ensuring that the risk register reflects the current threat landscape. Automated asset-matching compares advisory product names against the organisation's IT asset inventory to identify relevant threats without manual review.
- **Technical Controls:** Threat intelligence serves as additional input to technical preventive and detective controls such as firewalls, intrusion detection systems, SIEM platforms and anti-malware solutions.
- **Security Testing:** Threat intelligence provides input to the information security test processes and techniques, including penetration testing scenarios and red team exercises.

The organisation integrates threat intelligence into operational IT monitoring. All IT components are included in a unified monitoring environment that captures relevant parameters and generates alerts when defined thresholds are exceeded. Monitoring results feed into a vulnerability inventory where known weaknesses of all operated IT components and the treatment status of each weakness are centrally recorded and maintained. The IT operations function regularly obtains information about newly disclosed vulnerabilities affecting deployed platforms, firmware, operating systems, applications and services, analyses this information for the specific operational context and initiates remediation actions accordingly.

## 5. Incident Management Planning & Preparation (A 5.24)

[YOUR_ORGANISATION_NAME] establishes appropriate information security incident management processes. The objectives for incident management are agreed with management, and those responsible for incident management understand the organisation's priorities for handling incidents, including resolution time frames based on potential consequences and severity.

A clear definition distinguishes security incidents from routine operational disruptions. All personnel involved in incident handling know this definition. The entry thresholds for a security incident are aligned with the protection requirements of the affected business processes, IT systems and applications. A dedicated security policy for the detection of security-relevant events is derived from the overarching security policy and specifies how detection is planned, implemented and operated. This detection policy is known to all assigned detection personnel and is reviewed regularly.

### 5.1 Roles & Responsibilities

Roles and responsibilities to carry out incident management procedures are determined and communicated to all relevant internal and external interested parties. The following principles apply:

- **Common Reporting Method:** A common method for reporting information security events is established, including a clearly designated point of contact that is known to all personnel. The reporting channel is accessible around the clock.
- **Incident Management Process:** The incident management process follows a six-stage workflow: Reported, Triage, Investigation, Containment, Remediation and Closure. Each stage has defined inputs, decision criteria and outputs. The process provides the organisation with the capability for managing information security incidents, including administration, documentation, detection, triage, prioritisation, analysis, communication and coordination of interested parties.
- **Incident Response Process:** An incident response process provides the organisation with the capability for assessing, responding to and learning from information security incidents. The response process includes defined escalation paths and decision criteria.
- **Competent Personnel:** Only competent personnel handle the issues related to information security incidents within the organisation. Competency requirements are defined for each incident management role.
- **Procedure Documentation & Training:** Personnel tasked with handling information security incidents are provided with procedure documentation and receive periodic training. Training includes tabletop exercises and simulated incident scenarios.
- **Certification & Development:** A process is established to identify required training, certification and ongoing professional development for incident response personnel. Relevant certifications (e.g. GCIH, GCIA, OSCP) are supported by the organisation.

A dedicated incident response team is formed, whose members are convened depending on the nature of the incident. Suitable members are identified, appointed and briefed on their duties before an incident occurs. The composition of the team is reviewed regularly and updated as required. The interfaces between incident handling, fault and error management (IT service desk) and emergency management are analysed, shared resources are identified and all participating staff members are sensitised to each domain. The security management function has read access to any incident management tooling in use.

### 5.2 Incident Management Procedures

Management ensures that an information security incident management plan is created considering different scenarios. Procedures are developed and implemented for the following activities:

- **Event Evaluation:** Information security events are evaluated according to defined criteria for what constitutes an information security incident. Clear thresholds distinguish security events from operational disruptions, aligned with the protection requirements of affected business processes.
- **Detection & Classification:** Information security events and incidents are monitored, detected, classified, analysed and reported by both human and automatic means. Detection capabilities are integrated with the organisation's logging infrastructure and SIEM systems.
- **Incident Lifecycle Management:** Information security incidents are managed to conclusion, including response and escalation according to the type and category of the incident, possible activation of crisis management and continuity plans, controlled recovery from an incident and communication to internal and external interested parties. When an information security incident also constitutes a personal data breach, a linked breach incident is created and both incidents maintain a bidirectional reference.
- **External Coordination:** Coordination with internal and external interested parties such as authorities, external interest groups and forums, suppliers and clients is defined within the incident management plan.
- **Activity Logging:** All incident management activities are logged. The log captures the timeline of events, decisions taken, actions performed and the personnel involved.
- **Evidence Handling:** Procedures for the handling of evidence are integrated into the incident management process to ensure that forensic requirements are met from the earliest stages of incident detection.
- **Root Cause Analysis:** Root cause analysis (post-mortem) procedures are conducted for all significant incidents. The analysis identifies the technical and organisational factors that contributed to the incident.
- **Lessons Learned:** Lessons learned and any required improvements to incident management procedures or information security controls are identified, documented and tracked to implementation.

### 5.3 Reporting Procedures

The incident reporting procedures include the following elements:

- **Immediate Actions:** Clear instructions define the actions to be taken in the case of an information security event, such as noting all pertinent details immediately (malfunction occurring, messages on screen), immediately reporting to the point of contact and only taking coordinated actions.
- **Incident Forms:** Standardised incident reporting forms are used to support personnel in performing all necessary actions when reporting information security incidents. The forms capture event type, affected systems, timeline, initial assessment and actions taken.
- **Feedback Mechanisms:** Suitable feedback processes ensure that persons reporting information security events are notified, to the extent possible, of outcomes after the issue has been addressed and closed.
- **Incident Reports:** Formal incident reports are created for all confirmed incidents. Reports document the incident timeline, impact, root cause, response actions and recommendations.
- **External Reporting:** All external requirements for reporting incidents to relevant interested parties within defined time frames are met. This includes breach notification requirements to regulators (e.g. within 72 hours under GDPR), sector-specific reporting obligations and contractual notification requirements.

Suitable reporting and alerting paths for security-relevant events are documented, specifying which parties are to be informed and when, how each person can be reached and which communication method is used depending on the urgency. All persons relevant to the alerting chain are informed of their duties. The reporting and alerting paths are tested, rehearsed and updated regularly.

An escalation strategy is formulated and agreed between the fault-management function and the information security management function. The escalation strategy contains clear instructions defining who is to be involved, by which channel, for which type of suspected or confirmed security disturbance and at which point in time. It specifies the measures that follow an escalation and how the organisation reacts. Suitable tools — such as ticket systems capable of handling confidential information and remaining available during incidents or emergencies — are selected for this purpose. The escalation strategy and the matching checklists for the service desk are reviewed and rehearsed regularly, including through tabletop exercises.

Information security incidents can transcend organisational and national boundaries. To respond to such incidents, the organisation coordinates response activities and shares information about incidents with external organisations as appropriate, subject to confidentiality requirements and information sharing agreements.

## 6. Event Assessment & Classification (A 5.25)

- **Categorisation & Prioritisation Scheme:** [YOUR_ORGANISATION_NAME] uses an agreed categorisation and prioritisation scheme for information security incidents that enables the identification of the consequences and priority of each incident. Severity assessment uses a four-level scale (Critical, High, Medium, Low) with defined criteria for each level. The point of contact assesses each information security event using this scheme. The scheme classifies events by severity, type (confidentiality breach, integrity violation, availability disruption, combined), affected assets and business impact.

Personnel responsible for coordinating and responding to information security incidents perform the assessment and make a decision on information security events. Results of the assessment and decision are recorded in detail for the purpose of future reference and verification. The classification process is aligned between security management and the operational incident management (service desk) function to avoid conflicting assessments.

### 6.1 Detection of Security-Relevant Events

The detection of security-relevant events encompasses organisational, personnel and technical measures aimed at identifying threats and attacks at the earliest possible stage. The following principles apply:

- **Continuous Monitoring:** All logging data is monitored on a continuous basis and evaluated for anomalies. Designated staff members are assigned to this task and provided with documented procedural instructions for actively searching for security-relevant events in system logs, application logs and network traffic records. Sufficient personnel resources are allocated to sustain the required monitoring coverage.
- **Built-in Detection Functions:** Detection functions available in deployed IT systems and applications are activated and used. Collected event messages are checked at defined intervals. Where an incident is suspected, the event messages of the affected system and neighbouring systems are cross-checked to determine the scope and spread of the event.
- **Central Logging Infrastructure:** Event messages from IT systems and applications are aggregated centrally and analysed using appropriate tools. The signatures and rule sets of detection systems are kept up to date so that security-relevant events can also be identified retrospectively.
- **Threshold-based Alerting:** Thresholds are defined for security-relevant events. When thresholds are exceeded, automated alerts are triggered. Alerting takes into account the severity of the event and the protection requirements of the affected systems. Thresholds are reviewed and adjusted regularly to minimise false positives and maintain detection quality.
- **Employee Awareness:** All employees are sensitised to recognise and immediately report suspicious observations — such as unusual system behaviour, unexpected login failures or unfamiliar processes — to the incident management point of contact rather than ignoring or dismissing them. Client-side event messages are not ignored but forwarded through the established alerting paths.
- **Additional Detection Systems:** Based on the network plan, network segments requiring additional protection are identified. Transitions between internal and external networks are monitored by appropriate detection mechanisms. Malware detection systems are centrally managed and report security-relevant events automatically to the responsible personnel.
- **Data Protection Compliance:** The analysis of logging data complies with applicable data protection legislation. Employee privacy and works council co-determination rights are respected. Organisational rules define the data protection prerequisites under which log data may be analysed manually.
- **Regular Review:** Detection systems and measures in place are audited at regular intervals to verify they remain current and effective. Results are documented and compared against the target state. Deviations are tracked and remediated.

### 6.2 Classification Criteria

The categorisation scheme considers the following factors:

- The number of affected users and systems
- The classification level of the affected information
- The business impact and financial consequences
- Regulatory and contractual reporting obligations triggered by the event
- The potential for the event to escalate or spread
- Reputational impact to the organisation

## 7. Incident Response (A 5.26)

[YOUR_ORGANISATION_NAME] establishes and communicates procedures for information security incident response to all relevant interested parties. Information security incidents are responded to by a designated team with the required competency. The response includes the following activities:

- **Containment:** If the consequences of the incident can spread, the systems affected by the incident are contained. Containment strategies are pre-defined for common incident types (malware infection, unauthorised access, data exfiltration, denial of service) and are executed immediately upon classification. At the containment stage, responders receive first-response guidance warning against evidence-destroying actions (premature shutdown, log rotation, temporary file deletion). Network isolation is preferred over system shutdown to preserve volatile evidence.
- **Evidence Collection:** Evidence is collected as soon as possible after the occurrence of the incident. Volatile data (running processes, network connections, memory contents) is captured before non-volatile data. Evidence handling follows the procedures defined in the evidence collection section of this policy.
- **Escalation:** Incidents are escalated as required, including the activation of crisis management structures and, where necessary, the invocation of business continuity plans. Escalation criteria are pre-defined based on the severity classification.
- **Activity Logging:** All involved response activities are properly logged for later analysis. The log includes timestamps, actions taken, personnel involved, systems affected and decisions made.
- **Stakeholder Communication:** The existence of the information security incident and any relevant details are communicated to all relevant internal and external interested parties following the need-to-know principle. Communication templates are prepared for different stakeholder groups.
- **External Coordination:** The organisation coordinates with internal and external parties such as authorities, external interest groups and forums, suppliers and clients to improve response effectiveness and help to minimise consequences for other organisations.
- **Formal Closure:** Once the incident has been successfully addressed, it is formally closed and recorded. Closure criteria include confirmation that the vulnerability has been remediated, affected systems have been restored and preventive measures have been implemented.
- **Forensic Analysis:** Information security forensic analysis is conducted as required. The decision to initiate a forensic investigation is taken during incident handling based on the severity, the potential for legal action and the need to understand the full scope of compromise.
- **Post-Incident Analysis:** A post-incident analysis is performed to identify the root cause. The analysis is documented and communicated according to defined procedures. Findings feed into the improvement of security controls and incident management procedures.
- **Vulnerability Identification:** Information security vulnerabilities and weaknesses are identified and managed, including those related to controls which have caused, contributed to or failed to prevent the incident. Identified vulnerabilities are tracked through remediation in the vulnerability management process.

Parallel to the root-cause analysis, a deliberate decision is taken whether the priority is to contain the damage or to investigate the incident further. To make this decision, sufficient information about the scope and impact of the incident is gathered first. For selected incident scenarios, worst-case analyses are prepared in advance so that containment decisions can be taken rapidly under pressure.

The remediation of each incident follows a standardised procedure: the responsible team isolates the problem, identifies the root cause, selects remediation measures and obtains operational approval before implementing them. A current contact list of internal and external security specialists is maintained for expert consultation. Secure communication channels with these contacts are established in advance. The entire remediation is documented in a standardised manner, covering all actions performed, timestamps, log data from affected components and decisions taken. Documentation is quality-assured by the Information Security Officer before the incident is marked as closed.

### 7.1 Recovery Procedures

After an incident, affected components are isolated from the network. All required data that provides insight into the nature and cause of the incident is secured. Operating systems and applications on all affected components are examined for changes. Original data is restored from write-protected media, and all security-relevant configurations and patches are applied. Before components are returned to operation, all access credentials on affected components are changed. Where possible, affected components undergo a penetration test before re-deployment. Users are involved in the application functionality tests during recovery, and after restoration, the components — including network perimeter transitions — are monitored with heightened attention.

## 8. Learning from Incidents (A 5.27)

[YOUR_ORGANISATION_NAME] establishes procedures to quantify and monitor the types, volumes and costs of information security incidents. The information gained from the evaluation of information security incidents is used to drive continuous improvement:

- **Incident Plan Enhancement:** The incident management plan is enhanced based on lessons learned, including the addition of new incident scenarios and the refinement of existing procedures. Scenario playbooks are updated to reflect the latest threat patterns and response techniques.
- **Risk Assessment Updates:** Recurring or serious incidents and their root causes are identified to update the organisation's information security risk assessment and to determine and implement necessary additional controls. The organisation collects, quantifies and monitors information about incident types, volumes and costs to reduce the likelihood or consequences of future similar incidents.
- **User Awareness & Training:** Lessons learned from incidents are incorporated into the user awareness and training programme. Anonymised examples illustrate what can happen, how to respond and how to avoid similar incidents in the future.

### 8.1 Incident Metrics & Reporting

The organisation tracks the following metrics on an ongoing basis:

- Mean time to detect (MTTD) and mean time to respond (MTTR) for incidents
- Number of incidents by category and severity level
- Direct and indirect costs associated with incidents
- Percentage of incidents where root cause analysis was completed
- Number of control improvements implemented as a result of incident reviews

Incident metrics are reported to management as part of the periodic management review. Trend analyses are used to identify systemic weaknesses and to prioritise security investments.

After each incident analysis, the organisation examines whether the processes and workflows for incident handling need to be adjusted or further developed. The closure stage includes a structured post-incident review with two explicit checkpoints: (1) experience reports from all participants are collected and documented, and (2) procedure documentation and service desk checklists are reviewed and updated as needed. The organisation checks whether new developments in incident management methodology and forensic techniques can be incorporated into its documentation and workflows. Management is informed of incident statistics at least annually; where there is an immediate need for action, management is informed without delay.

The incident management system is reviewed periodically — through both announced and unannounced exercises — to verify that it remains current and effective. The exercises are coordinated with top management. Metrics such as the time from initial report to confirmed incident status are evaluated. Tabletop exercises and simulated incidents are conducted to ensure readiness.

## 9. Evidence Collection (A 5.28)

[YOUR_ORGANISATION_NAME] develops and follows internal procedures for dealing with evidence related to information security events for the purposes of disciplinary and legal actions. The requirements of different jurisdictions are considered to maximise the chances of admissibility across the relevant jurisdictions. Evidence is collected in a manner that is admissible in the appropriate national courts of law or other disciplinary forums.

### 9.1 Evidence Integrity Requirements

The organisation demonstrates that:

- **Completeness & Integrity:** Records are complete and have not been tampered with in any way. Digital evidence is uploaded during the investigation phase. Each file is automatically secured with a SHA-256 cryptographic hash computed at the time of upload. The hash is stored alongside the file and displayed to verify integrity. A chain-of-custody log records every access to evidence files (upload, download, verification) with user identity, timestamp and purpose.
- **Forensic Copies:** Copies of electronic evidence are demonstrably identical to the originals. Cryptographic hash values (SHA-256 or higher) are computed at the time of acquisition and verified at each subsequent access to confirm integrity. Evidence is categorised by type (screenshot, log export, network capture, malware sample, communication) with file format restrictions per type. For evidence that cannot be uploaded through the platform (e.g. physical storage media), an external reference entry with description and storage location is recorded.
- **System Integrity:** Any information system from which evidence has been gathered was operating correctly at the time the evidence was recorded. System health checks and logs are preserved alongside the evidence to support this assertion.

### 9.2 Forensic Procedures

The evidence management procedures provide instructions for the identification, collection, acquisition and preservation of evidence in accordance with different types of storage media, devices and the status of devices (powered on or off). The procedures address:

- Live forensics for volatile data (RAM, running processes, network connections) before powering down systems
- Post-mortem forensics for non-volatile data (hard drives, SSDs, removable media) using forensic duplication tools
- Order of volatility: data is captured in descending order of volatility, starting with the most transient sources
- Secure storage of evidence in tamper-evident containers or encrypted storage locations

Where available, certification or other relevant means of qualification of personnel and tools are sought to strengthen the value of the preserved evidence. A qualified forensic service provider is pre-selected and documented in the incident management configuration. During investigation, responders can indicate whether external forensic support is being engaged, with provider contact details displayed directly in the workflow. Where appropriate, framework agreements or call-off contracts are concluded so that forensic investigations can begin without delay.

A first-response guide describes, for each type of deployed IT system, the initial measures to be taken upon detection of a security incident so that as few traces as possible are destroyed. The guide explicitly warns against actions that could inadvertently eliminate evidence — such as prematurely shutting down a compromised system before capturing volatile data, or deleting temporary files before analysis. All responsible personnel are trained on the correct use of forensic tools and on the first-response procedures. Forensic tools are verified for correct function and freedom from manipulation before use.

Forensic data retention is governed by defined retention periods that comply with legal and regulatory requirements. The data protection officer and the works council or staff representation are involved from the outset to ensure that the collection and evaluation of forensic data — which often contains personal data — does not violate privacy regulations or internal agreements. Purpose limitation is observed throughout the investigation.

Digital evidence can transcend organisational or jurisdictional boundaries. In such cases, the organisation ensures that it is entitled to collect the required information as digital evidence. When an information security event is first detected, it is not always obvious whether the event will result in court action. Therefore, the organisation involves legal counsel early in any contemplated legal action and takes advice on the evidence required.

## 10. Technical Vulnerability Management (A 8.8)

[YOUR_ORGANISATION_NAME] maintains an accurate inventory of assets as a prerequisite for effective technical vulnerability management. For software assets, the inventory includes the software vendor, software name, version numbers, current state of deployment (what software is installed on which systems) and the person(s) within the organisation responsible for the software. The technical vulnerability management process is aligned with incident management activities to communicate data on vulnerabilities to the incident response function and provide technical procedures to be carried out in case an incident occurs.

Vulnerability instances follow a five-stage lifecycle: Detected, Assessment, Decision, Resolution and Closed. The resolution phase distinguishes two paths: active remediation (with a linked change request and optional compensating measure) or deferral to risk management (with documentation of compensating measures until a permanent fix is available). A vulnerability inventory is maintained centrally, recording all known weaknesses of operated IT components and their treatment status. Each vulnerability instance is linked to a strategic vulnerability category from the organisation's risk catalogue. This bidirectional enrichment allows risk reviewers to see active operational instances per strategic vulnerability and vulnerability handlers to see associated risk scenarios. The IT operations function initiates and tracks the treatment of each vulnerability and ensures timely resolution. A defined process specifies the maximum time frame for installing an available update that fixes a vulnerability, the conditions under which IT components with open vulnerabilities are taken out of service or replaced, and how components are isolated when neither a patch nor a replacement is available. IT systems and software are updated regularly; patches are evaluated and prioritised promptly after release. Where known exploits exist for a published vulnerability, the assessment considers the concrete exploitation risk.

### 10.1 Identifying Technical Vulnerabilities

The organisation implements the following measures to identify technical vulnerabilities:

- **Roles & Responsibilities:** Roles and responsibilities associated with technical vulnerability management are defined and established, including vulnerability monitoring, vulnerability risk assessment, patching, asset tracking and coordination responsibilities.
- **Information Resources:** For software and other technologies, based on the asset inventory, information resources for identifying relevant technical vulnerabilities are identified and awareness about them is maintained. The list of information resources is updated based on changes in the inventory or when new useful resources are found. Sources include CVE databases, vendor security bulletins, CERT advisories and threat intelligence feeds.
- **Supplier Obligations:** Suppliers of information systems, including their components, are required to ensure vulnerability reporting, handling and disclosure, including the requirements in applicable contracts.
- **Vulnerability Scanning:** Vulnerability scanning tools suitable for the technologies in use are deployed to identify vulnerabilities and to verify whether the patching of vulnerabilities was successful. Scans are performed on a regular schedule and following significant changes. Results from automated vulnerability scanners are imported into the central vulnerability inventory for consolidated tracking and treatment.
- **Penetration Testing:** Planned, documented and repeatable penetration tests or vulnerability assessments are conducted by competent and authorised persons to support the identification of vulnerabilities. Test scenarios are systematically derived from the MITRE ATT&CK framework, with test groups prioritised based on observed threat intelligence (incidents, advisories). Findings are transferred directly into the vulnerability management process. Caution is exercised as such activities can compromise the security of the system.
- **Third-Party Library Tracking:** The usage of third-party libraries and source code is tracked for vulnerabilities. A software composition analysis (SCA) process is established as part of the secure development lifecycle.

### 10.2 Vulnerability Disclosure

The organisation develops procedures and capabilities to:

- **Product Vulnerability Detection:** The existence of vulnerabilities in the organisation's products and services, including any external components used in these, is detected through continuous monitoring and reporting.
- **Report Reception:** Vulnerability reports from internal or external sources are received, acknowledged and processed through a defined workflow.
- **Public Point of Contact:** A public vulnerability disclosure portal is operated, enabling security researchers and other external parties to report vulnerabilities in the organisation's products and services. Submissions are automatically registered in the vulnerability management process. Reporters are informed when their reported vulnerability has been processed and resolved. A responsible disclosure policy is published.
- **Reporting Procedures:** Vulnerability reporting procedures, online reporting forms and appropriate threat intelligence or information sharing forums are established and maintained.

### 10.3 Evaluating Technical Vulnerabilities

To evaluate identified technical vulnerabilities, the organisation:

- **Report Analysis:** Analyses and verifies vulnerability reports to determine what response and remediation activity is needed. Reports are triaged based on the CVSS score, the exploitability, the affected assets and the business context.
- **Risk Identification:** Once a potential technical vulnerability has been identified, the associated risks and the actions to be taken are determined. Actions can involve updating vulnerable systems, applying compensating controls or accepting residual risk with documented justification.
- **Audit Log:** An audit log is kept for all steps undertaken in technical vulnerability management, from initial report through assessment, decision, remediation and verification.

### 10.4 Addressing Technical Vulnerabilities

A software update management process ensures that the most up-to-date approved patches and application updates are installed for all authorised software. If changes are necessary, the original software is retained and the changes are applied to a designated copy. All changes are fully tested and documented. The following measures are implemented:

- **Timely Action:** Appropriate and timely action is taken in response to the identification of potential technical vulnerabilities. A defined timeline governs the reaction to notifications of potentially relevant technical vulnerabilities, with severity-based SLAs: critical: 3 days, high: 7 days, medium: 30 days, low: 90 days.
- **Change Management Alignment:** Depending on how urgently a technical vulnerability needs to be addressed, the remediation action is carried out according to the change management process or by following information security incident response procedures for emergency changes. Change requests created from vulnerabilities or incidents are enriched with associated MITRE ATT&CK techniques and recommended mitigations to inform the remediation approach.
- **Legitimate Sources:** Only updates from legitimate sources are used, whether internal or external to the organisation. Update authenticity is verified through digital signatures or checksums.
- **Pre-Deployment Testing:** Updates are tested and evaluated before installation to ensure they are effective and do not result in intolerable side effects. If an update is available, the risks associated with installing the update are compared with the risks posed by the vulnerability.
- **Priority-Based Remediation:** Systems at high risk are addressed first. Remediation priority considers the criticality of the asset, the severity of the vulnerability and the exposure to exploitation.
- **Remediation Development:** Where vendor patches are not available, the organisation develops remediation measures, typically through compensating controls, configuration changes or custom patches.
- **Remediation Verification:** Testing is conducted to confirm whether the remediation or mitigation is effective. Post-patching vulnerability scans verify that the vulnerability has been eliminated.
- **Authenticity Verification:** Mechanisms are in place to verify the authenticity of remediation packages, including digital signature validation and checksum verification against vendor-published values.

### 10.5 Compensating Measures When No Update Is Available

If no update is available or the update cannot be installed, the following compensating measures are considered:

- **Vendor Workarounds:** Any workaround suggested by the software vendor or other relevant sources is applied.
- **Service Deactivation:** Services or capabilities related to the vulnerability are turned off until a patch becomes available.
- **Access Control Hardening:** Access controls (e.g. firewalls) at network borders are adapted or added to limit exposure of the vulnerable component.
- **Virtual Patching:** Vulnerable systems, devices or applications are shielded from attack through deployment of suitable traffic filters (virtual patching) using web application firewalls or intrusion prevention systems.
- **Increased Monitoring:** Monitoring is increased to detect actual exploitation attempts against the unpatched vulnerability.
- **Awareness Raising:** Awareness of the vulnerability is raised among affected users and administrators until remediation is complete.

### 10.6 Update Automation & Delay Considerations

- **Automatic Updates:** For acquired software where vendors regularly release security updates and provide automatic update facilities, the organisation evaluates whether automatic updating is appropriate. Automatic updates are enabled for standard endpoints; servers and critical systems follow the controlled patch management process.
- **Delayed Updates:** If adequate testing of updates is not possible (e.g. due to cost or lack of resources), the organisation assesses the associated risks based on the experience reported by other users before deciding on deployment timing.

Within the patch management strategy, the handling of built-in auto-update mechanisms of deployed software is defined. The organisation specifies how these mechanisms are secured and configured appropriately. New components are reviewed to determine which update mechanisms they contain. Hardware and software products that are no longer supported by the manufacturer and for which no security patches are available are evaluated for continued secure operation; products that cannot be operated securely are retired.

The technical vulnerability management process is regularly monitored and evaluated to ensure its effectiveness and efficiency. The organisation also considers bug bounty programmes where rewards are offered as an incentive to assist in identifying vulnerabilities. Information is shared with competent industry bodies and other interested parties. IT components are tested for vulnerabilities regularly and on an event-driven basis; the appropriate test coverage, depth and method are defined for each component category. Where critical vulnerabilities or threats exist and no patches are yet available, compensating measures are implemented to protect the affected components.

Where the organisation uses a cloud service supplied by a third-party provider, technical vulnerability management of the cloud service provider's resources is ensured by the provider. The provider's responsibilities for technical vulnerability management are part of the cloud service agreement, including processes for reporting the provider's actions relating to technical vulnerabilities.

## 11. Change Management (A 8.32)

Introduction of new systems and major changes to existing systems at [YOUR_ORGANISATION_NAME] follow agreed rules and a formal process of documentation, specification, testing, quality control and managed implementation. Management responsibilities and procedures are in place to ensure satisfactory control of all changes. Change control procedures are documented and enforced to ensure the confidentiality, integrity and availability of information throughout the entire system development lifecycle.

Wherever practicable, change control procedures for ICT infrastructure and software are integrated into a single change management process. The change control procedures include:

- **Impact Assessment:** The potential impact of changes is planned and assessed considering all dependencies. Impact analysis covers the affected information systems, business processes, connected systems, data flows and security controls. The assessment is documented as part of the change request record.
- **Authorisation:** Changes are authorised by the appropriate authority before implementation. Authorisation levels are defined based on the risk category of the change (standard, normal, emergency). No change is implemented without documented authorisation.
- **Communication:** Changes are communicated to relevant interested parties in advance of implementation. Notification includes the scope of the change, the expected impact, the maintenance window and the rollback plan.
- **Testing & Acceptance:** Changes are tested and acceptance-tested before implementation in the production environment. Testing is conducted in a segregated test environment that mirrors the production configuration. Test results are documented and accepted by the change owner.
- **Implementation & Deployment:** Changes are implemented according to documented deployment plans. The deployment plan includes the sequence of activities, responsible personnel, timing, verification steps and go/no-go criteria.
- **Emergency & Contingency:** Emergency and contingency considerations, including fall-back (rollback) procedures, are documented for every change. Emergency changes follow an expedited path with post-implementation review within 48 hours.
- **Change Records:** Records of all changes are maintained, including the request, impact assessment, authorisation, test results, deployment plan, rollback procedure and post-implementation review.
- **Documentation Updates:** Operating documentation and user procedures are updated as necessary to remain appropriate following changes. The verification phase includes a documentation update check confirming whether operations documentation and user procedures have been updated following the change. Where the change addresses a vulnerability, an optional vulnerability scan result field verifies that the addressed vulnerability has been eliminated.
- **Continuity Plan Updates:** ICT continuity plans and response and recovery procedures are updated as necessary to remain appropriate following changes. This ensures that disaster recovery capabilities reflect the current system configuration.

### 11.1 Change Categories

Changes are classified into the following categories:

- **Standard Changes:** Pre-approved, low-risk, frequently recurring changes that follow a documented procedure (e.g. routine patch deployment on non-critical systems).
- **Normal Changes:** Changes that require individual impact assessment, testing and authorisation through the change management process.
- **Emergency Changes:** Changes required to resolve critical incidents or prevent imminent security threats. Emergency changes are authorised by the Information Security Officer or IT Operations Manager and are subject to post-implementation review within 48 hours.

Inadequate control of changes to information processing facilities and information systems is a common cause of system or security failures. Changes to the production environment, especially when transferring software from development to operational environment, can impact the integrity and availability of applications. Good practice includes the testing of ICT components in an environment segregated from both the production and development environments.

A documented concept for the patch and change management process governs all modifications to IT components, software and configuration data with due consideration of security aspects. All patches and changes are planned, approved and documented. Rollback solutions are available before any change is applied; for major changes, the Information Security Officer is involved. The desired security level and security configurations are preserved throughout and after the change. Responsibilities for patch and change management are defined for all organisational areas and reflected in the authorisation concept.

All change requests (Requests for Change, RfCs) are captured and documented. The responsible personnel verify that information security considerations have been sufficiently addressed. The coordination process considers all affected stakeholder groups and the impact on information security. Affected groups have a documented opportunity to provide input. An expedited path is available for urgent change requests. Changes are integrated into the business processes; the current operational situation of affected processes is considered, and all relevant departments are informed of upcoming changes. An escalation tier exists at management level to decide on priority and scheduling conflicts for hardware or software changes.

The integrity and authenticity of all software packages are verified throughout the change process. Where checksums or digital signatures are available, they are validated before deployment. Software and updates are obtained exclusively from trustworthy sources. All changes are documented across all phases, applications and systems in accordance with defined documentation rules.

## 12. Roles & Responsibilities

- **Top Management:** Approves this policy, provides resources for security operations and is informed of significant incidents and their business impact.
- **Information Security Officer (ISO):** Coordinates all security operations activities, maintains the authority contact register and interest group memberships, oversees the threat intelligence programme, chairs the incident response team and reports security metrics to management.
- **Incident Response Team:** Responds to information security incidents, conducts containment and eradication, performs forensic analysis and executes post-incident reviews. Team members are appointed based on the type of incident.
- **IT Operations / IT Department:** Operates detection and monitoring systems, executes vulnerability scans, applies patches and updates, implements authorised changes and maintains system documentation.
- **Change Advisory Board (CAB):** Reviews and authorises normal and high-risk changes, assesses impact on information security and monitors change implementation quality.
- **Data Protection Officer (DPO):** Is consulted for incidents involving personal data, advises on breach notification obligations and ensures forensic activities comply with data protection regulations.
- **Legal Counsel:** Advises on evidence collection procedures, regulatory reporting obligations, contractual notification requirements and legal implications of incidents.
- **All Personnel:** Report information security events through the established reporting channel, preserve evidence by refraining from unauthorised remediation and participate in awareness training on incident recognition and reporting.

## 13. Review & Maintenance

This policy is reviewed:

- At least annually as part of the ISMS management review cycle.
- After significant information security incidents to incorporate lessons learned.
- When the threat landscape changes substantially (new threat actors, emerging attack vectors, geopolitical developments).
- After significant organisational changes (restructuring, mergers, new IT systems, changes in applicable law or regulation).
- When external audit findings or regulatory guidance require updates.

The Information Security Officer is responsible for initiating and coordinating the review process. Changes to this policy are approved by top management and communicated to all affected personnel.
