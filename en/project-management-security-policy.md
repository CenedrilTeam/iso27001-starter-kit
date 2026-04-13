# Information Security in Project Management

> **Document control**  
> Owner: [POLICY_OWNER_ROLE, e.g. Information Security Officer]  
> Approved by: [APPROVER_NAME_AND_ROLE]  
> Version: [VERSION]  
> Effective date: [EFFECTIVE_DATE]  
> Next review: [NEXT_REVIEW_DATE]

## 1. Legal/Regulatory Basis

ISO/IEC 27001:2022 / ISO/IEC 27002:2022, Annex A — Organisational Controls:

- A 5.8 — Information Security in Project Management

BSI IT-Grundschutz:

- ISMS.1.A9 (Integration of Information Security into Organisation-Wide Processes and Procedures)

Additional jurisdiction-specific laws — in particular data protection law (GDPR), sector-specific project compliance requirements, export control and cross-border data transfer restrictions — are listed in the Legal Register and incorporated by reference.

## 2. Purpose & Scope

This policy establishes how information security is integrated into project management at **[YOUR_ORGANISATION_NAME]**. It ensures that information security risks related to projects and their deliverables are effectively identified, assessed and treated throughout the project life cycle, in accordance with ISO/IEC 27002:2022, A 5.8.

The policy applies to all projects regardless of complexity, size, duration, discipline or application area — including projects for core business processes, ICT, facility management, product development and other supporting processes. It covers all personnel involved in project work, including employees, contractors, consultants and external suppliers acting in project roles.

Information security is not treated as a separate activity bolted on at the end of a project. It is part of the standard project management methodology from initiation through to closure, covering both new projects and ongoing activities.

## 3. Information Security in the Project Lifecycle (A 5.8)

Information security is integrated into project management to ensure that security risks are addressed as part of every project. The project management methodology in use requires that information security considerations are embedded from the earliest stages and maintained throughout the entire project life cycle — not only in ICT projects but in all project types. Project development approaches, whether waterfall or agile, support information security in a structured way adapted to the assessed severity of the risks. Early consideration at the planning and design stages leads to more effective and cost-efficient security outcomes.

### 3.1 Risk Assessment & Treatment in Projects

- **Integrated Risk Assessment:** Information security risks are assessed and treated at an early stage and periodically throughout the project life cycle as an integrated part of overall project risk management. The project risk register includes information security risks alongside other project risks. Risk assessment is conducted at project initiation and repeated at defined milestones — as a minimum at the planning, execution and pre-closure stages.
- **Execution-Phase Communication Security:** Information security risks associated with the execution of a project — including the security of internal and external communication channels, data sharing between project participants, and access to project environments — are identified and treated throughout the project life cycle. Secure communication channels are defined for the project. Rules for sharing project information with internal teams, external partners and customers are established at project initiation and enforced throughout execution.

### 3.2 Early Integration of Security Requirements

- **Security Requirements at Initiation:** Information security requirements are addressed in the early stages of every project — before significant design decisions are made or external commitments entered into. This includes application security requirements, requirements for complying with intellectual property rights, data protection requirements, and requirements derived from other applicable IS controls. A security requirements checklist is completed as part of the project charter. The project does not proceed to the planning phase without documented security requirements sign-off by the Information Security Officer or a designated security reviewer.

### 3.3 Review & Effectiveness Testing

- **Progress Review & Effectiveness Testing:** Progress on information security risk treatment is reviewed at predefined project milestones. The effectiveness of security measures is evaluated and, where feasible, tested — for example through security reviews, penetration testing or code reviews — before a project output goes live or is formally accepted. Findings are tracked to closure and reported to the project sponsor. Results are documented in the project file.

## 4. Information Security Requirements Determination (A 5.8)

Information security requirements for products or services delivered by a project are determined using multiple methods: deriving compliance requirements from this policy, topic-specific policies and regulations; and from activities such as threat modelling, incident reviews, use of vulnerability thresholds and contingency planning. This ensures that the architecture and design of information systems are protected against known threats based on the operational environment. The following points are considered when determining requirements for all types of projects:

### 4.1 Information Classification & Protection Needs

- **Information Inventory & Business Impact:** At project initiation, the information that will be generated, processed, stored or transmitted by the project is identified. Each information type is classified in accordance with the *Information Classification & Labelling Policy* and the potential negative business impact of inadequate security is assessed — covering scenarios such as unauthorised disclosure, incorrect modification or unavailability. The classification and impact assessment drive the selection of security controls for the project.
- **Confidentiality, Integrity & Availability Requirements:** The required protection levels for each identified information type and associated asset are determined in terms of confidentiality (C), integrity (I) and availability (A). A standardised protection needs assessment matrix maps the classification level and CIA requirements to specific security controls. These requirements are documented in the project requirements specification before the design phase begins.

### 4.2 Authentication & Access Control

- **Authentication Requirements:** The level of identity assurance required for each category of entity interacting with the project output — users, systems and services — is determined. Authentication requirements are derived from this assurance level: low-assurance interactions use password-based authentication, medium-assurance interactions require multi-factor authentication, and high-assurance interactions require certificate-based or hardware token authentication. These requirements are documented in the project requirements specification and are consistent with the access control policy.
- **Access Provisioning & Authorisation:** Access provisioning and authorisation processes are defined for all user types involved with the project and its outputs: customers and business end-users, privileged and technical users, project team members, operations staff taking over after project completion, and external suppliers. For each user type, the provisioning workflow, approval authority, access review cycle and deprovisioning trigger are specified. Access to project environments follows the principle of least privilege and is removed when no longer required.

### 4.3 User Duties & Responsibilities

- **User Security Briefing:** All individuals joining a project — employees, contractors and external parties — are informed of their information security duties and responsibilities relevant to the project before being granted access to project resources. This includes acceptable use of project systems and data, incident reporting procedures, data handling rules based on classification, and the consequences of policy violations. Briefings are documented and acknowledgement is recorded.

### 4.4 Business Process Requirements

- **Transaction Logging, Monitoring & Non-Repudiation:** Requirements derived from the business processes supported by the project are identified and incorporated into the project requirements. This includes transaction logging requirements (what events are logged, log retention periods), monitoring requirements (real-time or periodic), and non-repudiation requirements (where proof of the occurrence or non-occurrence of an action is preserved). Monitoring integration points with the organisation's central logging and SIEM infrastructure are specified at the design stage.
- **Integration with IS Control Infrastructure:** Requirements mandated by other information security controls are identified and incorporated into the project. This includes interface requirements for logging and monitoring systems, data loss prevention (DLP) systems, identity and access management systems, vulnerability management feeds, and incident management tools. The project architecture is designed to support these integration points and is validated against them during the review stages.

### 4.5 Legal & Regulatory Compliance

- **Compliance with Legal & Regulatory Environment:** Applicable legal, statutory, regulatory and contractual requirements relevant to the project are identified at initiation and documented as security requirements. This includes data protection legislation (including GDPR where applicable), sector-specific regulations, contractual security obligations and any export control or cross-border data transfer restrictions. Legal counsel is involved in validating the compliance requirements. The compliance mapping is maintained in the project documentation and reviewed when the regulatory environment changes.

### 4.6 Third-Party Assurance

- **Third-Party Security Assurance:** When a project involves third parties (suppliers, subcontractors, consultants, cloud service providers), the required level of assurance that those third parties meet the organisation's information security policy and topic-specific policies is determined. This assurance level drives the inclusion of specific security clauses in agreements and contracts, including the right to audit, requirements for security certifications, incident notification obligations and provisions for the return or secure destruction of information at contract end. Compliance with contractual security requirements is verified during the project and at handover.

## 5. Project Governance & Roles

The appropriateness of information security considerations and activities is followed up at predefined stages by suitable persons or governance bodies. Responsibilities and authorities for information security relevant to each project are defined and allocated to specified roles at project initiation.

Information security is integrated into all business processes and project tasks. This applies not only to new projects but also to ongoing activities. The Information Security Officer is involved in all security-relevant decisions throughout the project life cycle and coordinates with other risk management functions within the organisation.

- **Security Gate Reviews:** Predefined project stages — at a minimum: project initiation, end of design/planning, end of build/development, and pre-go-live — include a security gate where the Information Security Officer or a designated reviewer assesses whether security requirements have been met before the project advances to the next stage.
- **Project Security Role Assignment:** At project initiation, a project security lead is designated. For larger projects this is a dedicated role; for smaller projects it is assigned to the project manager or a named team member. The project security lead coordinates with the Information Security Officer, ensures the security requirements checklist is completed, tracks security findings and represents security interests in project governance meetings.
- **Escalation Path:** Security issues that cannot be resolved within the project team are escalated to the Information Security Officer and, where necessary, to top management. Unresolved security findings blocking a go-live decision are documented and the decision to proceed with or without remediation is taken at an appropriate governance level, with residual risks formally accepted.

## 6. Roles & Responsibilities

- **Top Management:** Approves this policy, ensures adequate resources are allocated for security activities in projects, and takes final decisions on residual risks escalated from project governance.
- **Information Security Officer (ISO):** Maintains this policy and the project security requirements framework. Participates in security gate reviews and advises project teams on security requirements, threat modelling and control selection. Coordinates with other risk management functions and is involved in all security-relevant project decisions. Tracks the security aspects of the project portfolio.
- **Project Sponsors / Project Owners:** Ensure that projects under their sponsorship are conducted in accordance with this policy. Accept residual information security risks at the governance level and ensure adequate budget for security activities within the project.
- **Project Managers:** Integrate security activities into the project plan and schedule. Complete the security requirements checklist at project initiation. Designate the project security lead. Escalate unresolved security issues and ensure security findings are tracked to closure.
- **Project Security Lead:** Coordinates information security activities within the project. Facilitates threat modelling and protection needs assessments. Reviews security requirements with the Information Security Officer. Ensures access provisioning and user briefings are completed before access is granted.
- **IT & System Architecture:** Implements security requirements in the technical design and ensures that interfaces to logging, monitoring, DLP and IAM infrastructure are built into the solution. Participates in security testing before go-live.
- **All Project Participants:** Follow the security briefing received at project onboarding, handle project information in accordance with its classification, use only approved communication channels and report security incidents to the project security lead or the Information Security Officer.

## 7. Review & Maintenance

This policy and the associated project security requirements framework are reviewed:

- At least annually, to verify that the requirements and processes remain aligned with the current threat landscape, organisational risk profile and applicable legal and regulatory requirements.
- After any significant security incident arising from a project environment, to identify lessons learned and update the requirements framework accordingly.
- When significant changes occur to the project management methodology, the organisation's IT landscape, or the applicable legal and regulatory environment.
- When updates to ISO/IEC 27002, ISO 21500, ISO 21502 or the BSI IT-Grundschutz Kompendium introduce new guidance relevant to information security in project management.

The Information Security Officer coordinates the review and ensures that any changes are communicated to project managers and integrated into the project management methodology.
