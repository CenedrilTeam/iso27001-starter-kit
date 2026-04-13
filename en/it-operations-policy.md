# IT Operations Security Policy

> **Document control**  
> Owner: [POLICY_OWNER_ROLE, e.g. Information Security Officer]  
> Approved by: [APPROVER_NAME_AND_ROLE]  
> Version: [VERSION]  
> Effective date: [EFFECTIVE_DATE]  
> Next review: [NEXT_REVIEW_DATE]

## 1. Legal/Regulatory Basis

ISO/IEC 27001:2022 / ISO/IEC 27002:2022, Annex A — Technological Controls:

- A 8.8 — Management of Technical Vulnerabilities
- A 8.13 — Information Backup
- A 8.14 — Redundancy of Information Processing Facilities
- A 8.15 — Logging
- A 8.16 — Monitoring Activities
- A 8.17 — Clock Synchronisation
- A 8.20 — Network Security
- A 8.21 — Security of Network Services
- A 8.22 — Segregation of Networks
- A 8.23 — Web Filtering

BSI IT-Grundschutz:

- OPS.1.1.3 (Patch and Change Management)
- DER.1.A12 (Evaluation of Information from External Sources)
- CON.3 (Backup Concept)
- OPS.1.1.5 (Logging)
- DER.1 (Detecting Security-Relevant Events)
- OPS.1.2.6 (NTP Time Synchronisation)
- NET.1.1 (Network Architecture and Design)
- NET.1.2 (Network Management)
- NET.3.1 (Routers and Switches)
- NET.1.1.A4 (Network Segmentation into Security Zones)
- NET.3.2 (Firewall)

Additional jurisdiction-specific laws — in particular NIS2, sector-specific IT operations requirements, telecommunications law and data retention law — are listed in the Legal Register and incorporated by reference.

## 2. Purpose & Scope

This policy establishes the operational security rules for IT systems, networks and services at **[YOUR_ORGANISATION_NAME]**. It covers vulnerability management, backup, redundancy, logging, monitoring, time synchronisation, network security, network service security, network segregation and web filtering.

The policy applies to all personnel responsible for operating, administering or using IT infrastructure, including employees, contractors and third-party service providers with access to the organisation's information processing facilities.

## 3. Technical Vulnerability Management (A 8.8)

An accurate asset inventory (see asset management) is the prerequisite for effective vulnerability management. Information about technical vulnerabilities is obtained in a timely manner, the exposure is evaluated and appropriate measures are taken to address associated risks. Software that is no longer supported by the vendor is retired or replaced; continued use requires a documented risk acceptance with compensating controls.

### 3.1 Roles, Resources & Tooling

- **Roles & Responsibilities:** Defined roles cover vulnerability monitoring, risk assessment, patch coordination and remediation tracking. The IT security team coordinates the vulnerability management process and reports findings to the Information Security Officer.
- **Information Resources:** For each asset type in the software inventory, dedicated information sources for vulnerability detection are identified (vendor advisories, CERT feeds, CVE databases, NVD). The sources are reviewed quarterly and updated when new asset types are introduced.
- **Supplier Obligations:** Contracts with software and hardware suppliers include clauses requiring timely vulnerability reporting, security patch provision and coordinated disclosure handling.
- **Vulnerability Scanning:** Automated vulnerability scanning tools run against all externally reachable and critical internal systems on a defined schedule (at minimum monthly). Scan results are verified, and patch effectiveness is confirmed through follow-up scans.
- **Penetration Testing:** Planned, documented penetration tests or vulnerability assessments are conducted at least annually by authorised and qualified personnel. Scope, methodology and rules of engagement are agreed in advance, and findings are tracked to resolution.
- **Third-Party Libraries & Source Code:** Third-party libraries, open-source components and custom source code are tracked for known vulnerabilities through software composition analysis tools. This is linked to the secure development lifecycle (see secure coding practices).

### 3.2 Vulnerability Disclosure & Reporting

- **Own Products & Services:** Vulnerabilities in the organisation's own products and services, including those introduced through external components, are detected through continuous monitoring, automated scanning and user reports.
- **Internal & External Reports:** Vulnerability reports are accepted from both internal personnel and external researchers. Every report is acknowledged, triaged within 48 hours and tracked to resolution.
- **Public Point of Contact:** A publicly accessible point of contact (e.g. security@domain, a dedicated web form) is maintained for responsible vulnerability disclosure by external parties.
- **Reporting Procedures:** Defined procedures govern vulnerability submission, including online forms, structured templates and integration with threat intelligence forums. Reports are classified by severity upon receipt.

### 3.3 Analysis & Verification

- **Report Analysis:** Each vulnerability report is analysed and verified to determine its validity, affected systems and the response and remediation needed. Duplicate reports are consolidated.
- **Risk Assessment:** For each confirmed vulnerability, the associated risks are identified using CVSS scores and the organisation's asset criticality. Appropriate actions are determined: patching, applying a workaround, risk acceptance with documented justification, or isolating the affected system.
- **Audit Log:** An audit log is maintained for all vulnerability management steps — from initial report through analysis, decision, remediation and verification. The log is retained according to the organisation's log retention schedule.

### 3.4 Remediation & Patching

- **Timely Action:** Remediation actions are taken within defined timelines based on severity: critical vulnerabilities within 72 hours, high within 7 days, medium within 30 days, low within 90 days.
- **Change Management:** All patches and updates follow the established change management controls (see the *Configuration & Change Management Policy*) including impact assessment and approval.
- **Legitimate Sources:** Updates and patches are obtained exclusively from legitimate, verified sources (vendor websites, authorised repositories). Checksums and digital signatures are verified before installation.
- **Pre-Installation Testing:** Updates are tested and evaluated in a non-production environment before installation on production systems. Test results are documented.
- **Prioritisation:** High-risk and business-critical systems are patched first. Prioritisation considers asset criticality, exploitation likelihood and exposure level.
- **Remediation Plan:** An effective, permanent remediation plan is developed for each confirmed vulnerability, specifying actions, responsible parties, timelines and verification criteria.
- **Effectiveness Confirmation:** After remediation, the effectiveness of the applied fix is confirmed through re-scanning, re-testing or manual verification.
- **Patch Authenticity:** The authenticity and integrity of patches are verified via checksums, digital signatures or secure hashes before deployment.
- **Workarounds (No Update Available):** When no vendor update is available, vendor-recommended workarounds are applied and documented as interim measures.
- **Service Disablement:** When no update or workaround exists, affected services or features are disabled to reduce the attack surface.
- **Tightened Access Controls:** When no patch is available, access controls around the vulnerable system are tightened and additional firewall rules are applied to restrict exposure.
- **Intrusion Detection Shielding:** Unpatched systems are placed behind intrusion detection/prevention systems (IDS/IPS) to detect and block exploitation attempts.
- **Increased Monitoring:** Monitoring of unpatched systems is increased to detect exploitation attempts, including enhanced log review and alerting.
- **Awareness Raising:** When a vulnerability affects systems that cannot be immediately patched, relevant personnel are informed about the vulnerability, its risks and applicable precautions.
- **Vendor Update Facilities:** For commercial software, vendor-provided update mechanisms (automatic update services, managed update channels) are used where available and configured for timely delivery.
- **Delayed Update Assessment:** If adequate testing of an update is not possible within the required timeline, the update may be delayed. The associated risk of delayed patching is evaluated, documented and accepted by the risk owner before deferral.

## 4. Information Backup (A 8.13)

A comprehensive backup concept is documented for each critical system, covering backup scope, schedule, storage, retention and restoration procedures. The 3-2-1 rule applies: at least three copies of data, on two different media types, with one copy stored offsite. Backup design accounts for ransomware scenarios by maintaining offline or immutable backup copies.

### 4.1 Backup Design & Protection

- **Backup Facilities:** Adequate backup facilities are provided for all essential information, software and system images to enable full recovery after a loss event.
- **Backup Records:** Accurate, complete records of all backups are maintained, including backup scope, schedule, media used, storage location and documented restoration procedures per system.
- **Backup Schedule:** The backup schedule reflects recovery point objectives defined in the business continuity plan, the security requirements and the information classification of the data. Critical systems are backed up at least daily; less critical data according to its classification level.
- **Offsite Storage:** Backup copies are stored at a remote location sufficiently distant from the main site to avoid both being affected by the same disaster. The offsite location meets the same physical and environmental security requirements as the primary site.
- **Physical & Environmental Protection:** Backup media are protected against unauthorised access, theft, environmental damage (temperature, humidity, electromagnetic interference) and deterioration through appropriate physical and environmental controls.
- **Regular Testing:** Backup media are tested regularly to ensure data integrity and readability. Restoration is tested on a dedicated test system — never on production — to verify that the full recovery process functions correctly.
- **Backup Encryption:** Backups are encrypted based on the risk assessment and the classification of the backed-up data. Encryption keys for backups are stored separately from the backup media and managed according to the key management policy.
- **Data Loss Detection:** Procedures detect inadvertent data loss or corruption before the backup executes, ensuring that corrupted data is not backed up over valid copies.
- **Backup Monitoring:** Backup execution is monitored automatically. Failures are logged, alerted and addressed within defined timelines. Backup logs are reviewed weekly.
- **Cloud Backup:** Where cloud-based backup services are used, the cloud provider's capabilities are assessed against the organisation's backup requirements including data sovereignty, encryption, retention, restoration speed and contractual SLAs.

### 4.2 Backup Testing & Validation

- **Incident Response Alignment:** Backup measures are tested regularly against the objectives of the incident response and business continuity plans to confirm that backed-up data, software and system images are sufficient for full recovery.
- **Restoration Time Testing:** Restoration procedures are tested against the recovery time requirements defined in the business continuity plan. Test results are documented and any shortfalls in restoration speed trigger corrective action.

## 5. Redundancy of Information Processing Facilities (A 8.14)

Availability requirements for business services and information systems are identified, and the architecture is designed with sufficient redundancy to meet them. Redundancy design considers the relationship with ICT readiness for business continuity and accounts for the integrity risks that data replication to duplicated components can introduce.

### 5.1 Redundancy Design

- **Multiple ISP / Critical Facility Suppliers:** Contracts are maintained with at least two independent internet service providers or critical facility suppliers to eliminate single-provider dependency.
- **Redundant Networks:** Redundant network paths are implemented so that the failure of a single network link does not disrupt critical services.
- **Geographically Separate Data Centres:** Two geographically separated data centres with mirrored systems are operated for critical services, ensuring continuity if one site becomes unavailable.
- **Redundant Power Supplies:** Physically redundant power supplies and independent power sources (UPS, generators, dual utility feeds) are installed for critical information processing facilities.
- **Parallel Software Instances:** Multiple parallel software instances with automatic load balancing are deployed for critical applications, distributing workload and providing failover capacity.
- **Duplicated Components:** Critical hardware components — CPUs, disks, memory, firewalls, routers, switches — are duplicated to eliminate single points of failure.

### 5.2 Failover Testing

- **Failover Verification:** Failover from primary to redundant components is tested at planned intervals to confirm that automatic switchover works as intended, that no data is lost during transition and that performance meets defined thresholds.

## 6. Logging (A 8.15)

Logs are produced, stored, protected and analysed to record events relevant to information security and privacy. Log data is forwarded to a central log server. Retention periods are defined per regulation and data type. Logs do not contain passwords or personally identifiable information unless explicitly required and protected. All systems use synchronised time sources (see clock synchronisation) to enable cross-system log correlation.

### 6.1 Event Data to Log

- **User IDs:** Every logged event records the user ID of the account or entity that initiated or was associated with the action.
- **System Activities:** System-level activities — service starts/stops, scheduled tasks, batch job executions and system errors — are logged with sufficient detail for troubleshooting and security analysis.
- **Dates & Times:** Each log entry includes the date and time of the event, recorded from the synchronised system clock in UTC or a defined local timezone with UTC offset.
- **Device Identity & Location:** The identity of the device (hostname, asset ID) and, where applicable, its physical or logical location are recorded in each log entry.
- **Network Addresses & Protocols:** Source and destination IP addresses, port numbers and the network protocol used are logged for all network-related events.
- **Access Attempts:** All access attempts — successful and failed — to systems, applications and data are logged, including the authentication method used.
- **Resource Access:** Access to critical resources (databases, file shares, APIs, administrative interfaces) is logged with the accessed resource identified.
- **Configuration Changes:** All changes to system, application and security configurations are logged, including the previous and new values where feasible.
- **Privilege Use:** The use of privileged accounts and elevated permissions is logged, including the specific privilege exercised and the target system or resource.
- **Utility & Tool Use:** The use of system utilities, diagnostic tools and administrative utilities is logged with the command or operation executed.
- **File Access & Deletion:** Access to, modification of and deletion of files — particularly those containing classified or sensitive information — are logged.
- **Access Control Alarms:** Events triggered by access control mechanisms (account lockouts, repeated authentication failures, unauthorised access attempts) are logged and generate alerts.
- **Security System Activation & Deactivation:** The activation, deactivation or modification of security systems (firewalls, IDS/IPS, anti-malware, DLP) is logged.
- **Identity Management Changes:** Changes to user accounts, group memberships, roles and permissions in identity management systems are logged.
- **Application Transactions:** User-initiated transactions in business-critical applications are logged at a level of detail appropriate to the application's classification.

### 6.2 Log Protection & Integrity

- **Message Type Alteration Detection:** Controls detect alterations to logged message types, including changes to the log format, event categorisation or severity classification.
- **Log File Tampering Detection:** Edits, deletions or unauthorised modifications to log files are detected through integrity monitoring. Users — including those with privileged access — are not permitted to delete or deactivate logs of their own activities.
- **Capacity & Overwrite Protection:** Log storage capacity is monitored. The system detects and alerts on failures to record events or the overwriting of log data due to storage exhaustion. Log rotation policies ensure that logs are archived before being overwritten.
- **Cryptographic Hashing:** Cryptographic hashes are applied to log files at defined intervals to enable detection of any post-creation modification.
- **Append-Only Storage:** Log files are stored in append-only or read-only formats. Write-once media or immutable storage is used where the risk assessment warrants it.
- **Public Transparency Files:** Where applicable, public transparency mechanisms (e.g. certificate transparency logs, blockchain-anchored timestamps) are used to provide independently verifiable proof that log entries have not been altered.

### 6.3 Log Analysis

- **Expert Analysis Skills:** Personnel performing log analysis possess the required expertise in event interpretation, attack pattern recognition and forensic analysis techniques. Training is provided at onboarding and refreshed annually.
- **Event Attribute Analysis:** Log analysis considers event attributes (source, target, action, outcome, timing) to identify patterns indicative of security incidents.
- **Rule-Based Exceptions (SIEM):** A security information and event management (SIEM) system applies rule-based correlation and exception detection across log sources to identify events that deviate from expected patterns.
- **Behavioural Baselines (UEBA):** User and entity behaviour analytics establish behavioural baselines and detect deviations that indicate compromised accounts, insider threats or policy violations.
- **Trend & Pattern Analysis:** Long-term trend and pattern analysis is performed on aggregated log data to identify emerging threats, recurring incidents or gradual changes in attack vectors.
- **Threat Intelligence Integration:** Log analysis incorporates threat intelligence feeds (indicators of compromise, known malicious IPs, attack signatures) to enrich event context and accelerate detection.

### 6.4 Log Review Activities

- **Protected Resource Access Review:** Access attempts to protected resources (DNS servers, web proxies, file shares) are reviewed regularly to identify unauthorised access patterns or data exfiltration attempts.
- **DNS Log Analysis:** DNS query logs are analysed to detect communication with known botnet command-and-control servers, domain generation algorithms or DNS tunnelling activity.
- **Service Provider Usage Reports:** Usage reports from external service providers (cloud, SaaS, managed services) are reviewed to identify anomalous consumption patterns or unauthorised use.
- **Physical Monitoring Correlation:** Logs from physical monitoring systems (access control, CCTV, environmental sensors) are correlated with IT event logs to detect coordinated physical-digital attack scenarios.
- **Cross-System Log Correlation:** Logs from different systems, applications and security tools are correlated to provide a unified view of events and detect multi-stage attacks that span multiple systems.

### 6.5 Logging Tools

- **Audit & Interrogation Tools:** Dedicated tools for querying, searching and interrogating log data are deployed. These tools support structured queries, full-text search and filtering by event attributes.
- **Automated Monitoring & Consolidated Reports:** Automated monitoring tools generate consolidated reports on log events, summarising key metrics, anomaly counts and security indicators for management review.
- **SIEM Platform:** A SIEM platform is deployed for centralised log storage, correlation, normalisation and alert generation. The SIEM ingests logs from all critical systems and applies detection rules aligned with the organisation's threat landscape.
- **Tamper Detection via Transparency:** Where public transparency files or blockchain-anchored mechanisms are available, they are integrated into the logging infrastructure to provide independent tamper detection for high-integrity log streams.

Audit logs required for regulatory compliance or evidence collection are archived according to the defined retention periods. When logs are shared with vendors for debugging, they are de-identified to remove sensitive data and personally identifiable information before transfer.

## 7. Monitoring Activities (A 8.16)

Networks, systems and applications are monitored continuously to detect anomalous behaviour and potential security incidents. The monitoring scope and depth are determined by business and information security requirements and take applicable legal obligations into account. A formal detection concept defines the monitoring strategy, responsibilities and escalation paths. Security events detected through monitoring and logging are escalated to the Security Operations incident management process for triage, classification and response.

### 7.1 Monitoring Scope

- **Network Traffic:** Inbound, outbound and internal network traffic is monitored for anomalies, unauthorised connections and indicators of compromise.
- **System, Server & Application Access:** Access to servers, operating systems and business applications is monitored, with particular attention to privileged access and after-hours activity.
- **Critical Configuration Files:** Changes to critical configuration files (OS, security tools, network devices, applications) are monitored in real time and generate alerts on unauthorised modifications.
- **Security Tool Logs:** Output from security tools — antivirus, IDS/IPS, firewalls, data loss prevention, web application firewalls — is monitored and correlated centrally.
- **Event Logs:** System and application event logs are continuously ingested into the monitoring platform and evaluated against detection rules.
- **Code Execution Authorisation:** Execution of software and scripts is monitored. Unauthorised or unsigned code execution attempts are detected and blocked where technically feasible.
- **Resource Usage:** CPU, memory, disk and bandwidth utilisation are monitored to detect resource exhaustion, denial-of-service conditions and cryptomining activity.

### 7.2 Baseline Establishment

- **Utilisation Baselines:** Normal and peak resource utilisation baselines are established for all monitored systems. Deviations from these baselines are flagged for investigation.
- **User Access Baselines:** Typical access patterns per user — including usual access times, source locations and frequency — are profiled to enable detection of anomalous behaviour.

### 7.3 Anomaly Detection

- **Unplanned Process Termination:** Unexpected termination of critical processes or services triggers an immediate alert and automated restart attempt where configured.
- **Malware-Typical Activity:** Network traffic to known malicious IP addresses, domains or URLs and behaviour patterns typical of malware (beaconing, lateral movement, data staging) are detected and alerted.
- **Known Attack Signatures:** The monitoring system applies up-to-date attack signatures from threat intelligence feeds to detect known exploits and attack patterns.
- **Unusual System Behaviour:** System behaviour that deviates from established baselines — unexpected processes, abnormal memory usage, unusual network connections — triggers investigation.
- **Bottlenecks & Overloads:** System bottlenecks, resource overloads and capacity threshold breaches are detected and escalated to prevent service degradation or denial-of-service conditions.
- **Unauthorised Access:** Attempts to access systems, applications or data without valid authorisation are detected, logged and alerted in real time.
- **Unauthorised Scanning:** Network scanning and port probing activity originating from internal or external sources is detected and generates alerts for investigation.
- **Protected Resource Access:** Access attempts to particularly protected resources (administrative interfaces, sensitive data stores, security infrastructure) are monitored with heightened sensitivity.
- **User & System Behaviour vs. Baseline:** Deviations from established user and system behaviour baselines — unusual login times, atypical data access volumes, abnormal transaction patterns — are flagged for analysis.

### 7.4 Alert Generation & Response

- **Threshold-Based Alerts:** Alerts are generated based on predefined thresholds and detection rules. Threshold values are reviewed quarterly and adjusted based on operational experience.
- **False Positive Tuning:** Detection rules and thresholds are tuned continuously to minimise false positives while maintaining detection accuracy. Tuning decisions are documented.
- **Trained Response Personnel:** Trained personnel are available to respond to monitoring alerts within defined response times. Escalation paths are documented and practised through exercises.
- **Redundant Alert Systems:** Redundant alert notification systems (e.g. email, SMS, dedicated alerting platforms) ensure that critical alerts reach response personnel even if one notification channel fails.

### 7.5 Monitoring Techniques

- **Threat Intelligence:** Monitoring systems incorporate threat intelligence feeds to identify indicators of compromise and known threat actor techniques, tactics and procedures.
- **Machine Learning & AI:** Machine learning and AI-based detection capabilities are used where appropriate to identify anomalies and zero-day threats that signature-based detection cannot cover.
- **Blocklists & Allowlists:** Network and application monitoring enforces blocklists (known malicious IPs, domains, hashes) and allowlists to restrict communication to authorised destinations.
- **Security Assessments:** Findings from penetration tests, vulnerability assessments and security audits are fed back into the monitoring system to improve detection rules and coverage.
- **Performance Monitoring Anomaly Detection:** Performance monitoring data is analysed for security-relevant anomalies — such as CPU spikes indicative of cryptomining or bandwidth surges indicating data exfiltration.
- **Log & Monitoring Combination:** Log data and real-time monitoring are combined to provide comprehensive situational awareness, enabling detection of slow-moving threats that individual data sources miss.
- **Botnet Communication Detection:** Network monitoring specifically targets botnet command-and-control communication patterns, including DNS-based C2, HTTP beaconing and encrypted tunnel detection.

## 8. Clock Synchronisation (A 8.17)

Accurate and consistent time across all systems is essential for log correlation, forensic investigations and evidence admissibility. The following rules govern clock synchronisation.

- **Reference Clock:** A reference clock source derived from radio time signals (DCF77, MSF) or GPS is used as the authoritative time source for all logging and time-stamping operations.
- **NTP / PTP Synchronisation:** All systems — servers, network devices, endpoints and applications — synchronise their clocks via NTP (Network Time Protocol) or PTP (Precision Time Protocol) to the defined reference clock. Time drift tolerance does not exceed one second for standard systems and one millisecond for systems requiring high-precision timestamps.
- **Clock Difference Monitoring:** Clock differences between systems, including cloud services and on-premises infrastructure, are monitored and recorded. Alerts are generated when synchronisation drift exceeds the defined tolerance.

## 9. Network Security (A 8.20)

The network architecture is designed, documented and maintained in security zones (management, server, client, DMZ, guest, IoT) following the principle of least privilege. Network documentation is kept current and reflects the actual topology. Firewall rules follow a deny-by-default approach, and network monitoring is integrated into the security concept.

### 9.1 Network Design & Governance

- **Information Type & Classification:** The type, sensitivity and classification of information that each network or network segment supports is identified and documented. Network controls are applied proportionally to the classification level.
- **Responsibilities & Procedures:** Responsibilities for network security management and procedures for operating network infrastructure are defined, documented and assigned to qualified personnel.
- **Network Documentation & Diagrams:** Current, accurate network documentation is maintained, including topology diagrams, IP address plans, device inventories and connection points. Documentation is updated after every change.
- **Separation of Operational Responsibility:** Where feasible, operational responsibility for networks is separated from the operation of the computer systems that use those networks, to maintain independent oversight.
- **Public, Third-Party & Wireless Controls:** Special controls are applied to safeguard information passing over public networks, connections from third-party networks and wireless networks. These controls include encryption, authentication, access restrictions and monitoring.
- **Logging & Monitoring:** Network activities are logged and monitored to detect security events. Network monitoring is integrated into the organisation's overall security monitoring concept.
- **Network Management Coordination:** Network management activities are coordinated across the organisation to optimise service levels, ensure consistent security policy enforcement and avoid conflicting configurations.

### 9.2 Network Access & Authentication

- **System Authentication:** Systems on the network are authenticated before being granted network access. 802.1X port-based authentication or equivalent mechanisms are used for wired and wireless connections.
- **Connection Restriction & Filtering:** Network connections are restricted and filtered by firewalls configured with deny-by-default rules. Only explicitly authorised traffic is permitted, and rules are reviewed at least semi-annually.
- **Device Connection Control:** Unauthorised devices are detected and restricted from connecting to the network through network access control (NAC) mechanisms. Only registered and compliant devices are permitted.

### 9.3 Network Hardening & Protection

- **Network Device Hardening:** Network devices (routers, switches, firewalls, access points) are hardened by disabling unnecessary services, changing default credentials, applying current firmware and enabling secure management protocols (SSH, SNMPv3).
- **Segregated Administration Channels:** Network administration traffic is segregated from production traffic through dedicated management VLANs or out-of-band management networks.
- **Critical Subnet Isolation:** The ability exists to temporarily isolate critical network subnets under active attack, containing the threat while maintaining essential services on unaffected segments.
- **Vulnerable Protocol Disablement:** Known vulnerable network protocols and services are disabled or replaced with secure alternatives. Where a vulnerable protocol is operationally necessary, compensating controls (network segmentation, encryption, monitoring) are applied.
- **Virtualised Network Security:** Security controls equivalent to those applied to physical networks are applied to virtualised networks, including micro-segmentation, virtual firewalls and traffic inspection within virtualised environments.

## 10. Security of Network Services (A 8.21)

Security measures for network services — including managed firewalls, intrusion detection, VPN services and private network connections — are identified, implemented and monitored. The ability of network service providers to manage agreed services securely is assessed and audited regularly.

### 10.1 Service Access Governance

- **Accessible Networks & Services:** The networks and network services that personnel are authorised to access are explicitly defined. Access beyond the defined scope requires prior approval.
- **Authentication per Service:** Each network service requires appropriate authentication — the strength of authentication is proportional to the sensitivity of the service and the data it processes.
- **Authorisation Procedures:** Formal authorisation procedures govern which users and systems are permitted to access each network service. Access is granted on a need-to-use basis and reviewed periodically.
- **Management & Technical Controls:** Management procedures and technical controls are implemented to protect access to network services. Controls include access logging, session management and anomaly detection.
- **Access Means:** The means used to access network services (VPN, wireless, direct connection) are defined per service. Remote access to internal services is conducted exclusively through approved VPN connections.
- **Time & Location Attributes:** Access to sensitive network services is restricted by time-of-day and source-location attributes where the risk assessment warrants it.
- **Usage Monitoring:** The use of network services is monitored to detect unauthorised access, excessive consumption and anomalous patterns. Monitoring results feed into the security monitoring process.

### 10.2 Technical Service Security

- **Authentication & Encryption Technology:** Network services use current authentication and encryption technologies (TLS 1.2+, IPsec, WPA3, 802.1X) appropriate to the service classification.
- **Technical Connection Parameters:** Technical parameters for secure connection to network services — including cipher suites, certificate requirements, protocol versions and session timeout values — are defined and enforced.
- **Caching Parameters:** Caching parameters for network services (proxy caches, content delivery, session caches) are configured to prevent unauthorised data retention and ensure that sensitive information is not cached beyond operational need.
- **Access Restriction Procedures:** Procedures restrict access to network services and applications based on user identity, device compliance status and connection context. Network-level access control lists complement application-level authorisation.

## 11. Segregation of Networks (A 8.22)

Large networks are divided into separate network domains and separated from the public network. Segregation is based on the security requirements of each domain, information classification and trust level of connected systems.

### 11.1 Wired Domain Segregation

- **Perimeter Definition:** The network perimeter for each domain (management, server, client, DMZ, guest, IoT/OT) is defined, documented and enforced through physical or logical separation.
- **Gateway-Controlled Access:** Access between network domains is controlled through gateways (firewalls, proxy servers, filtering routers) that enforce traffic policies based on defined rules. Direct inter-domain communication bypassing the gateway is blocked.
- **Security-Based Segregation:** The segregation criteria are based on the security requirements, classification level and trust level of the systems and information in each domain. Higher-security domains have stricter ingress and egress controls.

### 11.2 Wireless Network Segregation

- **Radio Coverage Adjustment:** Wireless network radio coverage is adjusted to minimise signal leakage beyond the organisation's physical perimeter, reducing the risk of unauthorised interception or connection.
- **Wireless as External:** All wireless network traffic is treated as external (untrusted) until the device has authenticated through a security gateway using 802.1X or equivalent enterprise authentication.
- **Guest Network Segregation:** Wireless guest networks are fully segregated from the internal personnel network. Guest traffic is routed directly to the internet without access to internal resources.

## 12. Web Filtering (A 8.23)

Access to external websites is managed to reduce exposure to malicious content and to prevent access to unauthorised online resources. Web filtering rules are enforced at the network perimeter and, where applicable, on endpoints.

### 12.1 Blocked Categories

- **Upload Sites:** Access to external file upload and file sharing sites is blocked unless a documented business justification has been approved. Approved exceptions are reviewed semi-annually.
- **Known Malicious Sites:** Websites identified as hosting malware, phishing content or exploit kits are blocked through regularly updated URL categorisation databases and threat intelligence feeds.
- **Command-and-Control Servers:** Communication with known or suspected command-and-control (C2) servers is blocked at the network perimeter. C2 indicators are updated from threat intelligence feeds.
- **Threat Intelligence Sites:** Sites identified as malicious through threat intelligence sharing (ISACs, CERT advisories, commercial feeds) are added to the blocklist within 24 hours of notification.
- **Illegal Content:** Access to websites sharing illegal content (as defined by applicable law) is blocked.

### 12.2 Usage Governance

- **Online Resource Usage Rules:** Rules for the safe and appropriate use of online resources are defined in the acceptable use policy. These rules specify which categories of websites are permitted for business use and which are restricted or blocked.
- **Personnel Training:** Personnel are trained on the secure use of online resources, including recognising phishing sites, avoiding drive-by downloads and reporting suspicious URLs. Training is delivered at onboarding and refreshed annually.

## 13. Roles & Responsibilities

- **Top Management:** Approves this policy, allocates resources for IT operations security infrastructure and ensures alignment with business objectives and legal requirements.
- **Information Security Officer (ISO):** Maintains this policy, defines monitoring and logging requirements, reviews vulnerability management effectiveness, oversees network security architecture and coordinates incident escalation from monitoring and detection systems.
- **IT Operations / System Administrators:** Implement and operate the controls defined in this policy. Manage patching, backup execution, log collection, monitoring tools, network devices and redundancy infrastructure. Respond to alerts and execute remediation procedures.
- **Network Administrators:** Design, implement and maintain the network architecture, firewall rules, network segmentation and access controls in accordance with this policy. Keep network documentation current.
- **System & Application Owners:** Ensure that their systems comply with backup schedules, logging requirements and vulnerability remediation timelines. Report deviations to IT operations.
- **All Personnel:** Use IT resources in accordance with the acceptable use policy. Report suspected vulnerabilities, security incidents and anomalous system behaviour to the IT helpdesk or Information Security Officer.

## 14. Review & Maintenance

This policy is reviewed:

- At least annually, as part of the ISMS management review cycle.
- After significant security incidents affecting IT operations (e.g. successful exploitation of a vulnerability, backup failure during recovery, network breach).
- When the threat landscape changes significantly (e.g. new classes of vulnerabilities, emerging attack techniques, changes in threat intelligence).
- Following significant changes to the IT infrastructure, network architecture, service providers or business processes.
- When new legal, regulatory or contractual requirements affecting IT operations security are identified.

Operations documentation is updated following changes managed through the Security Operations change management process to ensure that procedures, runbooks and system descriptions reflect the current state of the IT environment.
