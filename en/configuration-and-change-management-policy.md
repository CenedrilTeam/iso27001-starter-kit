# Configuration & Change Management Policy

> **Document control**  
> Owner: [POLICY_OWNER_ROLE, e.g. Information Security Officer]  
> Approved by: [APPROVER_NAME_AND_ROLE]  
> Version: [VERSION]  
> Effective date: [EFFECTIVE_DATE]  
> Next review: [NEXT_REVIEW_DATE]

## 1. Legal/Regulatory Basis

ISO/IEC 27001:2022 / ISO/IEC 27002:2022, Annex A — Technological Controls:

- A 8.9 — Configuration Management
- A 8.32 — Change Management

BSI IT-Grundschutz:

- OPS.1.1.1.A5 (Definition of Hardened Standard Configurations)
- OPS.1.1.1.A7 (Ensuring Proper IT Operations)
- OPS.1.1.1.A8 (Regular Target/Actual Comparison)
- OPS.1.1.2.A11 (Documentation of IT Administration Activities)
- OPS.1.1.2.A26 (Configuration Backup)
- APP.6.A4 (Rules for the Installation and Configuration of Software)
- OPS.1.1.3.A1 (Concept for Patch and Change Management)
- OPS.1.1.3.A2 (Definition of Responsibilities)
- OPS.1.1.3.A5 (Handling of Change Requests)
- OPS.1.1.3.A6 (Coordination of Change Requests)
- OPS.1.1.3.A7 (Integration of Change Management into Business Processes)
- OPS.1.1.3.A10 (Ensuring the Integrity and Authenticity of Software Packages)
- OPS.1.1.3.A11 (Continuous Documentation of Information Processing)

Additional jurisdiction-specific laws and regulations are listed in the Legal Register and incorporated by reference.

## 2. Purpose & Scope

This policy establishes rules for managing the security configurations of hardware, software, services and networks, and for controlling changes to information processing facilities and information systems at **[YOUR_ORGANISATION_NAME]**. It ensures that IT components operate with required security settings throughout their lifecycle and that changes are implemented in a controlled, documented manner that preserves information security.

The policy applies to all IT systems, applications, services, networks and infrastructure components operated by or on behalf of the organisation, including cloud-hosted environments. It covers all personnel and third parties who configure, administer, change or maintain these components.

Configuration management and change management are complementary disciplines: configuration management defines and enforces the secure baseline state of IT components, while change management ensures that any deviation from or update to that baseline is planned, authorised, tested and documented. Together they address a fundamental cause of security failures — uncontrolled configurations and unmanaged changes.

## 3. Secure Configuration Management (A 8.9)

Configurations — including security configurations — for hardware, software, services and networks are established, documented, implemented, monitored and reviewed. IT components are categorised and a hardened standard configuration is defined for each category. These templates implement the security requirements of the organisation and incorporate vendor recommendations and publicly available security guidance. Software is installed with minimum required functionality and minimum necessary permissions, with data-minimising privacy settings applied by default. All configuration data is protected against unauthorised access and its integrity is preserved.

### 3.1 Hardened Standard Templates

- **Publicly Available Guidance:** Hardened standard templates are developed using publicly available guidance, including vendor security baselines, recommendations from recognised security organisations (e.g. BSI IT-Grundschutz, CIS Benchmarks, DISA STIGs) and industry best practices. The source references for each template are documented alongside it.
- **Protection Level Determination:** The required level of security for each configuration template is determined by the protection needs of the IT component category — specifically the confidentiality, integrity and availability requirements of the data processed and services provided. Higher protection needs result in stricter configuration baselines.
- **Policy Alignment:** Every configuration template is aligned with the organisation's information security policy, topic-specific policies, applicable standards and other security requirements. Templates are reviewed for consistency with the access control policy, data classification scheme and applicable compliance obligations before deployment.
- **Feasibility & Applicability:** Before a configuration template is finalised, its feasibility and applicability within the organisation's specific operational context are assessed. Where a security requirement from a reference baseline cannot be applied without breaking functionality or creating disproportionate operational impact, a compensating control is documented and approved.

Each configuration template is version-controlled, uniquely identifiable and stored in a secure, access-controlled location. Templates are tested in an isolated environment before being deployed to production systems. Security updates for software are applied before components enter production use.

### 3.2 Identity & Access Hardening

- **Minimisation of Privileged Identities:** The number of identities with privileged or administrator-level access rights on any IT component is minimised. Shared or generic administrator accounts are avoided; where technically unavoidable, their use is strictly controlled and every action is attributable to an individual person. Role separation between administrative and normal operational functions is enforced through distinct account identities.
- **Disabling Unnecessary Identities:** Unnecessary, unused or insecure built-in accounts and identities (e.g. default guest accounts, anonymous access accounts, vendor service accounts no longer required) are disabled or removed as part of the initial hardening process and on an ongoing basis. When personnel leave the organisation or change roles, their associated identities are reviewed and disabled promptly.

### 3.3 Service & Function Minimisation

- **Disabling Unnecessary Functions & Services:** Only services, protocols, functions and features that are required for the operational purpose of an IT component are enabled. Unnecessary functions — including unused network services, demonstration or sample applications, unused scripting engines and surplus operating system components — are disabled or uninstalled. Software is installed with the minimum required functional scope.
- **Restricting Access to Utility Programs & Host Parameters:** Access to powerful utility programs (e.g. shell interpreters, registry editors, diagnostic tools, bootloader configuration interfaces) and host parameter settings is restricted to authorised administrators. Where possible, access is controlled via role-based permissions and logging is enabled for all use of such utilities.

### 3.4 System Baseline Settings

- **Clock Synchronisation:** Clocks on all IT components are synchronised to an authoritative time source using NTP or an equivalent protocol. Accurate and consistent timestamps across systems are required for log correlation, incident investigation, certificate validation and audit evidence.
- **Vendor Default Authentication Information:** Vendor-supplied default passwords, authentication tokens, certificates and other default authentication information are changed immediately after initial installation, before any system is connected to the production network. Other important default security-related parameters (e.g. default community strings, default API keys, default encryption settings) are reviewed and updated as part of the initial configuration process.
- **Automatic Session Time-Out:** Time-out facilities are configured on all interactive computing devices and sessions to automatically log off or lock the device after a defined period of inactivity. The inactivity threshold is set in accordance with the sensitivity of the system and data accessible through the session.

### 3.5 Licence Verification

- **Licence Compliance:** Configuration templates and deployment processes include a verification step confirming that licence requirements for all software components are met before installation. The software licence register (see the *IPR Compliance Policy*) is consulted to confirm that the number of installations does not exceed licensed entitlements and that licence terms are respected in the deployment configuration.

### 3.6 Template Review & Updates

- **Periodic Template Review & Update:** All hardened standard configuration templates are reviewed periodically and updated when new threats or vulnerabilities affecting the relevant component category are identified, when new software or hardware versions introduce security-relevant changes, or when vendor security guidance is updated. After each review, updated templates are version-incremented, tested and re-deployed to affected systems.

## 4. Configuration Records & Monitoring (A 8.9)

Configuration records for all IT components are maintained in a configuration management database (CMDB) or equivalent inventory system. The CMDB is the authoritative source for configuration state and supports both operational management and security monitoring. Access to configuration records is restricted to authorised IT operations personnel.

### 4.1 Configuration Records

- **Owner & Contact Information:** Each configuration record includes the current owner or designated point of contact for the asset — the person accountable for the IT component's security configuration and responsible for approving configuration changes.
- **Last Configuration Change Date:** The date and nature of the most recent configuration change are recorded for each asset, enabling IT operations to identify components that have not been updated within expected maintenance cycles and to correlate configuration changes with incident timelines.
- **Configuration Template Version:** The version of the hardened standard configuration template currently applied to each asset is recorded. This enables rapid identification of components that are not running the current approved template and facilitates targeted remediation after a template update.
- **Dependency Relations:** Configuration records capture relationships and dependencies between assets — for example, which servers depend on a shared database configuration, which applications rely on a specific middleware version and which network devices enforce access control for a given server segment. These dependency mappings are used in impact assessments for configuration changes.

### 4.2 Configuration Monitoring Scope

- **Maintenance Utilities:** Maintenance tools with access to system configurations (e.g. software deployment agents, patch management clients, firmware update utilities) are included in the configuration monitoring scope. Their own configuration is subject to the same hardening and review requirements as the systems they manage.
- **Remote Support Tools:** Remote support and remote administration tools (e.g. VPN gateways, jump servers, remote desktop services, out-of-band management interfaces) are included in configuration monitoring. Access via these tools is logged and the configurations of the remote support infrastructure are maintained in accordance with the same hardened templates as other production components.
- **Enterprise Management Tools:** Enterprise IT management platforms (e.g. configuration management databases, IT service management systems, monitoring platforms, identity management systems) are included in configuration monitoring. Because of their privileged access to the managed infrastructure, these systems are subject to heightened hardening requirements and regular configuration reviews.
- **Backup & Restore Software:** Backup and restore software configurations are included in the monitoring scope. Configuration backups are performed at both the application level and the system level on a regular schedule. An additional configuration backup is taken before any IT administration activity with potentially wide-reaching impact. The restorability of configuration backups is verified periodically to confirm that a clean configuration state can be recovered when required.

### 4.3 Target-Actual Comparison

A regular target-actual comparison is performed for all IT components in scope — comparing the current configuration of each component against its defined hardened standard template. This comparison is performed using automated configuration compliance scanning tools wherever technically feasible, producing structured reports of deviations. Where automation is not possible, manual configuration audits are conducted on a defined schedule. Identified deviations are assessed for security impact, classified and remediated within timeframes proportionate to their risk. All deviations and their remediation status are tracked in the CMDB. Automation of configuration enforcement (infrastructure-as-code, desired-state configuration management) is used wherever operational conditions permit, to reduce the window between detection and remediation of configuration drift.

## 5. Change Management (A 8.32)

All changes to information processing facilities and information systems — including hardware replacements, software installations and updates, configuration modifications, network changes and changes to ICT services — are subject to a formal change management process. This process encompasses documentation, specification, testing, quality control and managed implementation. Inadequate change control is a recognised common cause of system and security failures; this policy ensures that every change is planned, approved, tested and recorded before production deployment. The change management process integrates ICT infrastructure and software changes and applies to production environments including operating systems, databases, middleware and application software. Software packages are sourced only from trustworthy suppliers and their integrity is verified via checksums or digital signatures before installation. Changes are tested in a segregated test environment before production deployment.

### 5.1 Change Planning & Impact Assessment

- **Planning & Impact Assessment:** Every change request includes a documented impact assessment covering security implications, operational dependencies and potential effects on other systems and services. The dependency relations recorded in configuration records (Section 4.1) inform this assessment. All affected systems, services and stakeholder groups are identified before authorisation is sought. Where a change may affect information security controls or ICT continuity arrangements, the Information Security Officer is consulted as part of the assessment.

### 5.2 Authorisation

- **Authorisation of Changes:** Every change requires explicit authorisation before implementation. Authorisation levels are defined by change category and potential impact: routine low-risk changes are authorised by the responsible IT operations team lead, significant changes with broader impact require approval from the Information Security Officer and the relevant asset owner, and major changes affecting core infrastructure or cross-organisational business processes require management-level approval. Unauthorised changes are treated as security incidents. For major changes, the Information Security Officer is involved in the authorisation decision.

### 5.3 Communication

- **Communication to Interested Parties:** Authorised changes are communicated to all relevant interested parties before implementation. This includes affected business units, IT operations teams, system owners and, where the change affects externally visible services, relevant external stakeholders. For changes with broad impact, a change calendar or scheduled maintenance window is published in advance. The coordination process considers information security effects on all target groups and includes a defined escalation path for priority decisions.

### 5.4 Testing & Acceptance

- **Testing & Acceptance:** All changes are tested before production deployment in a segregated test environment that replicates the production configuration as closely as practicable. Acceptance criteria are defined as part of the change plan and are demonstrably satisfied before the change proceeds to production. Acceptance is formally recorded with the name of the responsible person, date and result. Checksums or digital signatures of software packages are verified before installation.

### 5.5 Implementation & Deployment

- **Implementation & Deployment Plans:** Changes are implemented according to a documented deployment plan that specifies the sequence of steps, the responsible persons, the implementation window, the configuration items affected and the post-implementation verification steps. Implementation is performed using the authorised configuration management tooling. Configuration records in the CMDB are updated to reflect the new state immediately upon successful deployment. All administrative activities performed during implementation are documented, recording what changed, when, who made the change and the basis or reason for the change.

### 5.6 Emergency & Rollback Procedures

- **Emergency & Rollback Procedures:** Every change plan includes documented fallback and rollback procedures that describe how to restore the previous configuration state if the change fails, causes unexpected issues or needs to be reversed. A configuration backup is taken before any change with potentially wide-reaching consequences. Rollback procedures are tested during the test phase where feasible. For emergency changes — required to respond to critical security incidents or imminent system failures — an expedited authorisation procedure is defined that maintains accountability while enabling rapid response. Emergency changes are subject to the same documentation and post-implementation review requirements as standard changes.

### 5.7 Change Records

- **Change Records:** A complete record is maintained for every change, covering: the change request and its impact assessment, the authorisation decision with date and authorising person, the communication sent, test results and acceptance evidence, implementation details including the deployment plan, rollback procedure, and any deviations encountered, and the post-implementation verification outcome. Change records are stored in a tamper-evident system and retained according to the organisation's records retention schedule. Changes are documented across all phases, applications and systems.

### 5.8 Documentation Updates

- **Operating Documentation & User Procedures:** When a change affects the operation of a system or service, the relevant operating documentation and user procedures are updated as necessary before or immediately after the change is deployed (see also the *IT Operations Security Policy*). Outdated documentation is superseded and archived rather than deleted, to preserve the change history.
- **ICT Continuity Plans & Recovery Procedures:** When a change affects systems or services covered by ICT continuity plans or incident response and recovery procedures, those plans are reviewed and updated to reflect the changed environment before the change is closed. The change record captures whether continuity plans were reviewed and any updates made.

## 6. Roles & Responsibilities

- **Top Management:** Approves this policy, provides resources for configuration management tooling and change management processes and decides on priority escalations for changes affecting core business processes.
- **Information Security Officer (ISO):** Maintains this policy, reviews and approves hardened standard configuration templates for security adequacy, is consulted on all changes with significant security impact and is involved in major change authorisation decisions.
- **IT Operations:** Develops, maintains and deploys hardened standard configuration templates; operates the CMDB; performs target-actual comparisons and remediation; implements approved changes in accordance with deployment plans; documents all administrative activities; performs configuration backups before high-impact changes. Responsibilities for patch and change management are defined for all organisational units.
- **Asset Owners / System Owners:** Define the protection needs and operational requirements for their assets, approve configuration templates for their systems, authorise changes to their assets within their delegated authority level and ensure that operating documentation and continuity plans for their systems are kept up to date following changes.
- **Change Advisory Board (or equivalent function):** Reviews and coordinates significant change requests, considers information security effects on all target groups and provides recommendations on authorisation and scheduling. Facilitates the escalation path to management for priority decisions.
- **All Personnel:** Follow authorised configuration settings and report any observed unauthorised changes or deviations from expected system behaviour to IT Operations or the Information Security Officer.

## 7. Review & Maintenance

This policy and the associated configuration management procedures are reviewed:

- At least annually, to verify alignment with current IT infrastructure, threat landscape and regulatory requirements.
- When significant changes to the organisation's IT architecture, business processes or risk profile occur.
- Following a security incident attributable to a configuration weakness or an unauthorised change.
- When new IT component categories are introduced that require new hardened standard configuration templates.
- When updated vendor security guidance, BSI IT-Grundschutz requirements or relevant external standards (e.g. CIS Benchmarks) are published that affect the content of deployed templates.

Configuration template currency is maintained on an ongoing basis: each template is reviewed whenever a new software or hardware version introduces security-relevant changes, and at a minimum annually as part of the overall policy review cycle. The CMDB and the change records it contains are maintained as living documentation throughout the year.
