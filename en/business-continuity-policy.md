# Business Continuity Policy

> **Document control**  
> Owner: [POLICY_OWNER_ROLE, e.g. Information Security Officer]  
> Approved by: [APPROVER_NAME_AND_ROLE]  
> Version: [VERSION]  
> Effective date: [EFFECTIVE_DATE]  
> Next review: [NEXT_REVIEW_DATE]

## 1. Legal/Regulatory Basis

ISO/IEC 27001:2022 / ISO/IEC 27002:2022, Annex A:

- A 5.29 — Information Security During Disruption
- A 5.30 — ICT Readiness for Business Continuity

BSI IT-Grundschutz:

- DER.4 (Business Continuity Management)
- DER.2.1 (Security Incident Handling)
- CON.3 (Backup Concept)

BSI-Standard 200-4 (Business Continuity Management).

Additional jurisdiction-specific laws and regulations — in particular NIS2, DORA and sector-specific resilience requirements — are listed in the Legal Register and incorporated by reference.

## 2. Purpose & Scope

This policy establishes the business continuity management framework for **[YOUR_ORGANISATION_NAME]**. It defines how information security is maintained during disruptions, how ICT services are prepared for business continuity, and how the organisation plans, tests and improves its ability to recover from adverse events.

The policy covers business impact analysis, recovery objective setting, ICT continuity planning, testing and exercising, and the maintenance of information security controls throughout all phases of disruption and recovery. It applies to all business processes, ICT services and information assets within the scope of the ISMS. All employees, contractors and third-party service providers involved in business continuity planning, response or recovery activities are bound by this policy.

Emergency management planning prioritises critical business processes. Incident escalation procedures define clear thresholds for transitioning from incident response to emergency and crisis activation.

## 3. Information Security During Disruption (A 5.29)

Information security is maintained at an appropriate level during disruptions. Security controls remain active throughout incident response, failover and recovery operations. Where primary controls become unavailable, pre-approved compensating controls take effect immediately. Recovery from various failure scenarios — including technical failure, supply chain disruption, natural disaster and cyberattack — is planned in advance as part of emergency management.

- **Security Controls in Continuity Plans:** Each continuity plan documents the relevant information security controls in normal operation and defines which compensating controls apply during disruption. Failover environments maintain the same access control levels, network segmentation and monitoring capabilities as production systems. Backup encryption is verified before restoration to ensure data integrity and confidentiality.
- **Disruption-Mode Security Procedures:** For critical security controls, continuity plans define disruption-mode procedures that describe how protection is maintained when primary systems are unavailable. Staff with recovery responsibilities receive annual training on these procedures and participate in exercises that validate their ability to operate controls under degraded conditions.
- **Compensating Controls:** For security controls that cannot function during a disruption, continuity plans document compensating controls that provide equivalent protection. Each compensating control entry specifies the primary control it replaces, the activation trigger and the responsible person. Compensating controls are tested during continuity exercises and reviewed after every real activation.

## 4. ICT Readiness for Business Continuity (A 5.30)

ICT readiness for business continuity ensures that the ICT services required to support critical business processes can be restored within defined timeframes. The ICT continuity programme covers the full lifecycle: business impact analysis, recovery objective setting, planning, implementation, testing, maintenance and continual improvement. The backup concept covers both backup creation and restoration, regular restoration testing, and secure backup storage at geographically separated locations. Detailed backup documentation — including scope, method, schedule, retention, storage locations and restore test results — is maintained as part of each system's disaster recovery plan.

### 4.1 Business Impact Analysis & Recovery Objectives

- **Minimum Performance & Capacity Requirements:** Each ICT continuity plan specifies minimum performance and capacity requirements during disruption, including acceptable bandwidth, storage capacity, processing power and user concurrency thresholds. These specifications are derived from the business impact analysis (BIA) and validated by the process owners of the dependent business activities. Degraded-mode service levels are formally documented and communicated to all stakeholders.
- **Recovery Time Objectives (RTO):** A Recovery Time Objective (RTO) is defined for each prioritised ICT service. Restoration procedures specify the exact sequence of recovery steps, system dependencies and verification checkpoints. RTOs are validated through regular testing. Any test result that exceeds the defined RTO triggers a corrective action and plan revision. RTO values are reviewed annually and after significant changes to the ICT landscape.
- **Recovery Point Objectives (RPO):** A Recovery Point Objective (RPO) is defined for each prioritised information resource. Backup strategies and frequencies are aligned to meet or exceed RPO requirements. Backup restoration is tested regularly to verify RPO achievement. Where RPO requirements demand near-zero data loss, synchronous replication or continuous data protection mechanisms are implemented. RPO values drive the backup schedule documented in the disaster recovery plan for each system.

### 4.2 Organisational Structure

- **ICT Continuity Organisation:** An ICT continuity organisation is established with defined roles: ICT continuity manager, recovery team leads and technical recovery specialists. Each role has a designated backup person to ensure availability during absences. Competency requirements are documented and verified through training records. The ICT continuity manager reports to management and coordinates with the Information Security Officer on all security-related continuity matters. Escalation paths from incident response to emergency and crisis management are defined and documented.

### 4.3 ICT Continuity Planning

- **Documented ICT Continuity Plans:** Comprehensive ICT continuity plans are documented for each critical ICT service. Each plan includes activation criteria, step-by-step recovery instructions, contact lists with primary and backup contacts, resource requirements (personnel, hardware, software, network, facilities) and expected timelines. Plans reference the applicable security controls from the Information Security During Disruption section. Communication procedures define how internal and external stakeholders are informed at each phase of the disruption.
- **Management Approval:** ICT continuity plans are formally approved by management before activation readiness is declared. Approval includes review of executive summaries, cost implications, residual risk assessments and resource commitments. Re-approval is obtained annually and after significant changes to the ICT environment, organisational structure or threat landscape. Approval records are retained as documented information within the ISMS.

### 4.4 Testing & Exercises

- **Regular Testing & Exercises:** ICT continuity plans are tested at defined intervals: tabletop exercises at least quarterly, technical recovery tests at least semi-annually and full simulation exercises at least annually. Test results, identified gaps and corrective actions are documented in test reports. Each test verifies that RTOs and RPOs are achievable under realistic conditions. Backup restoration is tested regularly to confirm that backed-up data can be recovered within RPO targets. Lessons learned feed into plan revisions, and unresolved findings are tracked through the ISMS corrective action process.

### 4.5 Continuity Management

- **Cause-Agnostic Response:** ICT continuity plans address disruptions regardless of cause, including technical failure, natural disaster, cyberattack, human error and supply chain failure. Response procedures are designed to be cause-agnostic where possible, with cause-specific supplements for targeted scenarios such as ransomware, data centre loss or critical vendor failure. Recovery planning covers diverse failure scenarios.
- **Prioritised Activity Support:** Prioritised business activities identified in the BIA are mapped to their required ICT services, including all dependencies on infrastructure, applications, data and external service providers. Gap analyses verify that continuity plans ensure these services are available within defined RTOs. Where gaps are identified, remediation actions are assigned, tracked and verified before plans are declared operational.
- **Proactive Response & Early Warning:** Continuity plans define activation criteria that enable early response before a full disruption occurs. Plans activate upon detection of incidents that could escalate to service disruption, including capacity threshold breaches, replication lag alerts, vendor service degradation notices and security incident escalations.

## 5. Roles & Responsibilities

- **Top Management:** Approves this policy, allocates resources for business continuity management and ensures that continuity objectives are aligned with the overall business strategy.
- **Information Security Officer (ISO):** Ensures that information security controls are integrated into all continuity plans and that compensating controls provide adequate protection during disruptions.
- **ICT Continuity Manager:** Coordinates the ICT continuity programme, maintains continuity plans, schedules tests and exercises, and reports on programme effectiveness to management.
- **Recovery Team Leads:** Manage the execution of recovery procedures for their assigned ICT services, coordinate with technical recovery specialists and report progress to the ICT continuity manager.
- **Technical Recovery Specialists:** Execute step-by-step recovery procedures, verify system integrity after restoration and confirm that security controls are re-established.
- **Process Owners:** Define business requirements for RTOs, RPOs and minimum service levels through the BIA process. Validate that continuity plans meet their operational needs.
- **All Employees & Contractors:** Participate in continuity exercises, follow disruption-mode procedures and report incidents that may trigger continuity plan activation.

## 6. Review & Maintenance

This policy is reviewed:

- At least annually, as part of the ISMS management review cycle.
- After significant business continuity incidents, including actual activations of continuity plans.
- When business impact analysis results change significantly, including changes to critical process prioritisation or recovery objectives.
- Following significant changes to the ICT infrastructure, organisational structure or supplier landscape.
- After continuity exercises that reveal material gaps or improvement opportunities.
- When new legal, regulatory or contractual requirements affecting business continuity are identified.
