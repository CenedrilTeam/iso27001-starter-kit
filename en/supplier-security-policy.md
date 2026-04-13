# Supplier Security Policy

> **Document control**  
> Owner: [POLICY_OWNER_ROLE, e.g. Information Security Officer]  
> Approved by: [APPROVER_NAME_AND_ROLE]  
> Version: [VERSION]  
> Effective date: [EFFECTIVE_DATE]  
> Next review: [NEXT_REVIEW_DATE]

## 1. Legal/Regulatory Basis

ISO/IEC 27001:2022 / ISO/IEC 27002:2022, Annex A — Supplier Relationships:

- A 5.19 — Information Security in Supplier Relationships
- A 5.20 — Addressing Information Security Within Supplier Agreements
- A 5.21 — Managing Information Security in the ICT Supply Chain
- A 5.22 — Monitoring, Review and Change Management of Supplier Services
- A 5.23 — Information Security for Use of Cloud Services

ISO/IEC 27036-3 — Information Security for Supplier Relationships.

BSI IT-Grundschutz:

- OPS.2.3 (Outsourcing for Customers)
- OPS.2.2 (Cloud Usage)
- OPS.3.2 (Outsourcing for Service Providers)

Additional jurisdiction-specific laws — in particular NIS2 supply chain obligations, the EU Cyber Resilience Act (for products with digital elements), data protection law (GDPR and cross-border transfer rules), sector-specific outsourcing regulations (e.g. financial services) and contract law — are listed in the Legal Register and incorporated by reference.

## 2. Purpose & Scope

This policy establishes the framework for managing information security risks arising from supplier relationships at **[YOUR_ORGANISATION_NAME]**. It covers the entire supplier lifecycle from initial assessment and selection, through contractual engagement and ongoing monitoring, to orderly termination or transition.

The policy applies to all categories of external suppliers, including ICT service providers, cloud service providers, software and hardware vendors, outsourcing partners, consultants and any other third party that accesses, processes, stores, transmits or provides infrastructure components affecting the confidentiality, integrity or availability of organisational information. All employees, contractors and personnel involved in supplier selection, management or oversight are bound by this policy.

## 3. Supplier Relationships & Classification (A 5.19)

Processes and procedures are implemented to manage security risks associated with supplier products and services. A risk-oriented approach governs the entire outsourcing lifecycle: strategy definition, suitability assessment of potential providers, contractual arrangement, operational management and orderly termination. The responsibility for information security remains with the organisation at all times, regardless of which activities are outsourced.

### 3.1 Supplier Types & Risk Assessment

- **Supplier Type Registry:** A supplier registry classifies all suppliers into defined categories: ICT service providers, cloud service providers, software and hardware vendors, logistics partners, utilities, financial service providers and ICT infrastructure component suppliers. Each entry records the supplier type, the information assets and systems the supplier can affect, the criticality rating and the responsible internal contact.
- **Information & Infrastructure Scope:** For each supplier relationship, the specific information assets, ICT services and physical infrastructure that the supplier accesses, monitors, controls or uses are documented. Access is limited to the minimum scope required for service delivery.
- **ICT Component Impact Assessment:** ICT infrastructure components and services provided by suppliers are classified by their potential impact on confidentiality, integrity and availability. Components that process or transmit sensitive data receive a higher criticality rating and are subject to stricter security requirements.
- **Personnel & Physical Security Expectations:** Minimum personnel security and physical security levels are defined for each supplier category. Suppliers handling sensitive information meet standards equivalent to the internal requirements, including background verification of key personnel where legally permissible and appropriate physical access controls at their facilities.

### 3.2 Evaluation & Selection

- **Evaluation & Selection Process:** Suppliers are evaluated and selected based on the sensitivity of the information, products and services involved. The evaluation process includes market analysis, customer references, document review, certifications (ISO 27001, SOC 2, C5 or equivalent) and, for high-criticality suppliers, on-site security assessments. Evaluation results are documented in the supplier registry with a formal suitability determination.
- **Product & Service Security Assessment:** Before onboarding, the information security and privacy controls of supplier products and services are evaluated. The assessment verifies the accuracy and completeness of the supplier's implemented controls, with particular attention to controls that protect the integrity of information processing. Results are recorded and reviewed before contract execution.

### 3.3 Risk Management & Compliance

- **Supplier Risk Assessment:** Information security risks associated with each supplier relationship are assessed and managed, including risks from potentially malicious supplier personnel, malfunctioning or vulnerable products (including embedded software components and sub-components) and inadequate security practices. Supplier risk assessments are updated at least annually and after significant changes to the supplier relationship or threat landscape.
- **Compliance Monitoring:** Compliance with established information security requirements is monitored for each supplier type and access category. Monitoring methods include third-party audits, independent attestation reports (SOC 2, ISO 27001 certificates), product validation and periodic self-assessment questionnaires. Monitoring frequency is proportional to the criticality of the supplier relationship.
- **Non-Compliance Remediation:** When supplier non-compliance is detected through monitoring, audit or any other means, a defined escalation process is triggered. The supplier receives a formal non-compliance notice with specific remediation requirements and a deadline. Unresolved non-compliance is escalated to management for risk acceptance, contract renegotiation or termination decision.

### 3.4 Incident Handling & Continuity

- **Incident Handling:** Responsibilities for information security incident handling are defined for both the organisation and each supplier. Supplier agreements specify notification timeframes, collaboration procedures during remediation and post-incident reporting obligations. Suppliers report security incidents affecting organisational data within 24 hours of detection.
- **Resilience & Contingency:** Supplier resilience is assessed as part of the onboarding process. Where necessary, recovery and contingency measures are agreed to ensure the continued availability of supplier information processing. For critical suppliers, alternative suppliers or in-house fallback capabilities are identified in advance to avoid disruption if the supplier becomes unable to deliver.

### 3.5 Awareness & Transitions

- **Staff Awareness & Training:** Personnel who interact with supplier staff receive training on the applicable rules of engagement, topic-specific policies, processes and expected behaviour. Training content is tailored to the supplier type and the level of access granted. Training is provided before the first interaction and refreshed annually.
- **Information Transfer & Transitions:** When information, assets or responsibilities are transferred to or from a supplier, the transfer is managed through a documented transition plan. Information security and privacy are maintained throughout the entire transfer period, including interim controls during handover phases.

### 3.6 Secure Termination

- **Access De-Provisioning:** All access rights granted to the supplier are revoked within one business day of relationship termination. The de-provisioning covers logical access (accounts, VPN, API keys) and physical access (badges, keys, tokens). Completion is verified through an access audit.
- **Information Handling at Termination:** At termination, all organisational information held by the supplier is returned in an agreed format or securely destroyed. The supplier provides written confirmation of destruction with a description of the method used.
- **Intellectual Property Ownership:** Ownership of intellectual property developed during the engagement is determined in the supplier agreement. At termination, all IP deliverables, source code and documentation are transferred to the organisation or disposed of as specified in the agreement.
- **Information Portability:** Agreements include provisions for information portability in case of supplier change or insourcing. Data formats, export procedures and timelines are specified to enable a seamless transition to an alternative supplier or internal operation.
- **Records Management:** Retention periods and handling procedures for records generated during the supplier relationship are defined. At termination, records are transferred to the organisation or retained by the supplier for the agreed period in accordance with legal and regulatory requirements.
- **Return of Assets:** All organisational assets (hardware, tokens, documentation, media) held by the supplier are returned within the period specified in the agreement. A return checklist verifies completeness.
- **Secure Disposal:** Information and associated assets that are not returned are securely disposed of using methods that comply with the information classification level. The supplier provides a disposal certificate for each item.
- **Ongoing Confidentiality:** Confidentiality obligations survive the termination of the supplier relationship. Non-disclosure agreements remain in effect for the period specified in the contract, typically a minimum of three years after termination.

### 3.7 Limited-Influence Suppliers

- **Guidance-Based Selection:** Where the organisation cannot place direct security requirements on a supplier (e.g. utility providers, large platform vendors), supplier selection decisions consider the security guidance established in this policy. Available security information, public audit reports and known vulnerabilities of the supplier are evaluated before engagement.
- **Compensating Controls:** For suppliers where direct requirements cannot be imposed, compensating controls are implemented based on a risk assessment. These controls mitigate the residual risk from the supplier's security posture and are documented in the risk register.

## 4. Contractual Security Requirements (A 5.20)

Supplier agreements are documented to ensure both parties have a clear understanding of their obligations regarding information security. A standardised contract template is used for all supplier agreements, incorporating baseline security clauses that are adapted based on the risk profile and criticality of the specific supplier relationship. Contracts are reviewed by information security, legal and procurement representatives before signing.

### 4.1 Information & Classification

- **Information Description & Access Methods:** Each agreement describes the specific information to be provided or accessed and the methods of provision or access. Data flows are documented, including interfaces, protocols and transfer mechanisms.
- **Information Classification:** Agreements require the supplier to handle information according to the organisation's classification scheme. Classified information is labelled before transfer and handled in accordance with the classification level throughout its lifecycle.
- **Classification Mapping:** Where the supplier operates its own classification scheme, a formal mapping between the two schemes is established and documented in the agreement to ensure consistent handling of information.

### 4.2 Legal & Compliance

- **Legal & Regulatory Requirements:** Agreements specify applicable legal, statutory, regulatory and contractual requirements, including data protection obligations, handling of personally identifiable information (PII), intellectual property rights and copyright provisions. The agreement describes how compliance is ensured and verified.
- **Acceptable Use Rules:** Rules for acceptable and unacceptable use of the organisation's information and associated assets are defined in the agreement. The supplier acknowledges these rules and ensures their personnel are informed.

### 4.3 Security Control Obligations

- **Control Obligations:** Each agreement specifies the security controls that both parties implement, including access control, performance review, monitoring, reporting and auditing. The supplier's obligation to comply with the organisation's information security requirements is explicitly stated and contractually binding.
- **ICT Infrastructure Security:** Minimum information security requirements are defined for the supplier's ICT infrastructure for each type of information and access category. These requirements serve as the baseline for individual agreements and are scaled based on business needs and risk criteria. For external cryptographic service providers (certificate authorities, HSM providers, cloud KMS), specific SLA provisions address key availability, escrow arrangements and incident response times.
- **Personnel Authorisation:** Procedures for authorising and removing authorisation for supplier personnel to use organisational information and assets are defined. An explicit list of authorised supplier personnel is maintained and reviewed quarterly. Changes to the authorised personnel list require prior notification.
- **Personnel Screening:** Where legally permissible, agreements require background screening of supplier personnel who access sensitive information. The agreement defines screening responsibilities, verification procedures and notification requirements when screening has not been completed or results raise concerns.
- **Physical Security Controls:** Physical security controls at supplier facilities are commensurate with the classification level of the information processed. Requirements cover access control, environmental protection, visitor management and media handling.
- **Information Transfer Protection:** Controls for protecting information during physical and logical transfer are specified, including encryption standards, secure transport methods and chain-of-custody documentation.

### 4.4 Audit, Incident & Training

- **Incident Management Clauses:** Agreements define incident management requirements, including mandatory notification within 24 hours of detection, collaboration procedures during incident remediation, evidence preservation obligations and post-incident reporting.
- **Training & Awareness Requirements:** Agreements require the supplier to ensure their personnel complete training on the organisation's specific procedures and information security requirements, including incident response procedures and authorisation processes.
- **Third-Party Attestations:** Agreements require the supplier to provide evidence and assurance through recognised third-party attestation mechanisms (ISO 27001 certification, SOC 2 Type II reports, C5 attestation) covering relevant information security requirements. Independent reports on control effectiveness are provided at least annually.
- **Right to Audit:** The organisation retains the right to audit the supplier's processes and controls related to the agreement, either directly or through an independent auditor. Audit scope, frequency and notification requirements are specified in the agreement.
- **Periodic Effectiveness Reports:** The supplier is obligated to deliver periodic reports on control effectiveness. Relevant issues identified in reports are addressed within agreed timelines, with remediation plans tracked to completion.

### 4.5 Sub-Contracting & Remediation

- **Sub-Contracting Provisions:** Agreements include provisions governing sub-contracting. Sub-suppliers are bound by the same security obligations as the primary supplier. The supplier maintains a current list of sub-suppliers and notifies the organisation before any change. Prior approval is required before engaging new sub-suppliers for services involving organisational data.
- **Indemnities & Remediation:** Agreements define indemnities and remediation measures for failure to meet security requirements. Penalty clauses are proportional to the criticality of the service and the severity of the breach. Remediation timelines are specified for different severity categories.
- **Defect Resolution & Conflict Resolution:** A structured defect resolution process with defined severity levels and response times is established. Conflict resolution procedures include escalation paths, mediation provisions and, as a last resort, arbitration clauses.
- **Security Contact Points:** The agreement identifies relevant contacts, including a designated contact person for information security issues on both the supplier and organisation side. Contact details are kept current and reviewed quarterly.

### 4.6 Continuity & Recovery

- **Backup Provisions:** Agreements require the supplier to provide backup aligned with the organisation's requirements in terms of frequency, type and storage location. Backup procedures are documented and restoration is tested regularly.
- **Disaster Recovery Site:** For critical services, agreements require an alternate facility (disaster recovery site) that is not subject to the same threats as the primary facility. Fallback controls are defined for the event that primary controls fail.
- **Change Management:** Agreements include a change management process that ensures advance notification to the organisation of any changes affecting the service. The organisation retains the right to reject changes that negatively impact information security.

### 4.7 Termination Clauses

- **Termination Clauses:** Agreements contain termination clauses covering records management, return of assets, secure disposal of information and associated assets and ongoing confidentiality obligations. Exit timelines and transition support obligations are specified.
- **Secure Data Destruction:** The agreement defines a method for the supplier to securely destroy organisational information as soon as it is no longer required. Destruction is certified and the method complies with the classification level of the data.
- **Handover Support:** At contract end, the supplier provides transition support to another supplier or to the organisation itself. A transition plan with milestones, deliverables and acceptance criteria is agreed before termination takes effect.

### 4.8 Agreement Register & Review

- **Agreement Register:** A central register of all agreements with external parties (contracts, memoranda of understanding, information-sharing agreements, NDAs) is maintained. The register tracks where organisational information is shared or processed and is reviewed at least semi-annually.
- **Regular Agreement Review:** Agreements with external parties are reviewed, validated and updated at least annually to ensure they remain required, fit for purpose and include current information security clauses. Outdated or unnecessary agreements are terminated.

## 5. ICT Supply Chain Management (A 5.21)

ICT products and services are acquired only from reputable sources with documented quality control and security practices. The organisation works with its suppliers to understand the ICT supply chain structure and identifies matters that significantly affect the products and services being provided. Security requirements are propagated throughout the supply chain by requiring suppliers to cascade equivalent obligations to their sub-suppliers. The ICT supply chain encompasses cloud services, IoT devices, hosting services and all embedded hardware and software components. Where the EU Cyber Resilience Act (CRA) applies, suppliers of products with digital elements provide conformity documentation, maintain vulnerability handling processes and supply security updates for the defined support period.

### 5.1 Acquisition & Supply Chain Propagation

- **Acquisition Security Requirements:** Information security requirements are defined for every ICT product or service acquisition. Requirements are proportional to the criticality of the product or service and cover confidentiality, integrity and availability aspects. Procurement templates include a mandatory information security requirements section.
- **Service Supplier Propagation:** ICT service suppliers are contractually required to propagate the organisation's security requirements throughout the supply chain when they sub-contract parts of the service. Compliance of sub-contractors is verified through the primary supplier's attestation or audit programme.
- **Product Supplier Propagation:** ICT product suppliers propagate appropriate security practices throughout the supply chain for products that include components purchased from other suppliers, including sub-contracted software developers and hardware component providers. Evidence of propagation is requested during the evaluation process.

### 5.2 Transparency & Component Documentation

- **Software Bill of Materials (SBOM):** ICT product suppliers provide information describing the software components used in their products, including an SBOM where available. The SBOM is reviewed for known vulnerabilities and maintained as part of the product security documentation. For products falling under the EU Cyber Resilience Act, an SBOM is a mandatory deliverable.
- **Security Function Documentation:** ICT product suppliers provide documentation describing the implemented security functions of their products and the configuration required for secure operation. This documentation is reviewed during onboarding and referenced in operational security procedures.
- **Supply Chain Information Sharing:** Rules for sharing information about the supply chain, potential issues and compromises are established between the organisation and its suppliers. Communication channels and escalation procedures for supply chain incidents are defined.

### 5.3 Validation & Integrity

- **Compliance Validation:** A monitoring process validates that delivered ICT products and services comply with stated security requirements. Validation methods include penetration testing, independent security assessments and verification of third-party attestations for the supplier's information security operations.
- **Critical Component Tracking:** A process identifies and documents product or service components that are critical for maintaining functionality. These components receive increased scrutiny and follow-up, particularly when built outside the organisation or when the supplier outsources component development to other parties.
- **Supply Chain Traceability:** Assurance is obtained that critical components and their origin can be traced throughout the supply chain. Traceability records are maintained for all components classified as high-criticality.
- **Functional Integrity:** Delivered ICT products are verified to function as expected without unexpected or unwanted features. Verification methods include security testing, code review for custom-developed components and comparison against documented specifications.
- **Tamper Prevention & Detection:** Processes ensure that components from suppliers are genuine and unaltered from their specification. Measures include anti-tamper labels, cryptographic hash verification, digital signature validation and monitoring for out-of-specification performance. Tamper prevention is addressed across multiple stages of the system development lifecycle.
- **Security Certification:** For critical ICT products, assurance is obtained that products achieve required security levels through formal certification or evaluation schemes such as the Common Criteria Recognition Arrangement, BSI certification or equivalent frameworks.

### 5.4 Component Lifecycle Management

- **Component Lifecycle Management:** Specific processes manage the lifecycle and availability of ICT components and associated security risks. This includes planning for components that may become unavailable because a supplier ceases operations or discontinues a product due to technology changes. Alternative suppliers are identified in advance and the process for transferring software and competence to an alternative supplier is documented.

## 6. Monitoring, Review & Change Management (A 5.22)

Supplier services are continuously monitored and periodically reviewed to ensure that information security terms and conditions are met, incidents and problems are managed properly and changes in supplier services or business status do not affect service delivery. A designated supplier relationship manager coordinates monitoring activities and reports to management. Sufficient technical skills and resources are available to verify compliance with agreement requirements. The outsourcing register consolidates all active relationships with status, performance metrics and risk ratings.

### 6.1 Change Categories Under Review

- **Service Enhancements:** Enhancements to the supplier's current services are assessed for security impact before implementation. The supplier provides advance notification and documentation of all planned enhancements.
- **New Applications & Systems:** Development of new applications and systems by the supplier is subject to the organisation's change review process. Security requirements are communicated before development begins.
- **Policy & Procedure Changes:** Modifications or updates of the supplier's security policies and procedures are reviewed for potential impact on the organisation's security posture. Material changes require prior approval.
- **Security Control Changes:** New or changed controls introduced to resolve incidents or improve information security are evaluated to ensure alignment with the organisation's security requirements.
- **Network Changes:** Changes and enhancements to the supplier's networks, including those affecting connectivity to the organisation, are subject to advance notification and security review.
- **New Technologies:** Adoption of new technologies by the supplier is assessed for potential security implications, including changes to the risk profile and compatibility with the organisation's infrastructure.
- **Product Version Changes:** Adoption of new products or newer versions and releases by the supplier is reviewed for security impact, including potential introduction of new vulnerabilities or changes to security configurations.
- **Development Tool Changes:** New development tools and environments used by the supplier are evaluated for security compliance, particularly where they process or store organisational data.
- **Facility Relocation:** Changes to the physical location of supplier service facilities are assessed for compliance with data residency requirements, physical security standards and jurisdictional obligations.
- **Sub-Supplier Changes:** Changes to the supplier's sub-suppliers are subject to advance notification. The organisation reviews the security posture of new sub-suppliers before approval.
- **Further Sub-Contracting:** Sub-contracting of services to additional suppliers requires prior written approval. The organisation assesses the security impact and ensures the new sub-contractor meets equivalent security requirements.

### 6.2 Ongoing Monitoring & Review

- **Service Level Monitoring:** Service performance levels are monitored against the agreed metrics. Deviations trigger a documented exception process with root-cause analysis and corrective action planning.
- **Service Reports & Progress Meetings:** Service reports produced by the supplier are reviewed. Regular progress meetings are conducted as required by the agreement, with documented minutes and action items.
- **Supplier Audits:** Audits of suppliers and sub-suppliers are conducted periodically, complemented by review of independent auditor reports where available. Findings are tracked through the corrective action process until closure.
- **Incident Information Sharing:** Information about information security incidents is exchanged between the organisation and the supplier as required by the agreement. Incident trends are reviewed in regular service meetings.
- **Audit Trail Review:** Supplier audit trails and records of security events, operational problems, failures and service disruptions are reviewed. Root-cause analyses are requested for significant events.
- **Incident Response:** Identified information security events or incidents related to supplier services are responded to and managed through the organisation's incident management process, with supplier coordination as defined in the agreement.
- **Vulnerability Management:** Information security vulnerabilities in supplier products and services are identified, assessed and managed. Critical vulnerabilities are escalated through the organisation's vulnerability management process with defined remediation timelines.
- **Sub-Supplier Security Review:** The information security aspects of the supplier's relationships with its own suppliers are reviewed. The organisation verifies that sub-supplier security standards are equivalent to those required of the primary supplier.
- **Service Continuity Assurance:** The supplier maintains sufficient service capability together with workable plans to ensure agreed service continuity levels following major failures or disasters. Business continuity plans and disaster recovery capabilities are reviewed annually.
- **Compliance Ownership:** Suppliers assign named individuals responsible for reviewing compliance with and enforcing the requirements of the agreement. Contact details are kept current and communicated to the organisation.
- **Security Level Evaluation:** The adequacy of the supplier's information security level is evaluated regularly through a combination of self-assessments, third-party attestations and direct audits. Results are recorded in the supplier registry and inform the annual supplier risk reassessment.

## 7. Cloud Services (A 5.23)

The use of cloud services involves shared responsibility for information security between the cloud service provider and the organisation. The responsibilities of both parties are clearly defined and documented. Before adopting a cloud service, a security analysis is conducted that assesses the service model (IaaS, PaaS, SaaS), the deployment model (public, private, hybrid) and the applicable legal jurisdiction. Cloud service agreements are reviewed to ensure they address the organisation's confidentiality, integrity, availability and information handling requirements with appropriate service level objectives and quality targets.

### 7.1 Cloud Service Governance

- **Information Security Requirements:** All relevant information security requirements associated with each cloud service are documented, including data classification constraints, regulatory obligations and technical security controls. Requirements are defined before service procurement and incorporated into the evaluation criteria.
- **Selection Criteria & Usage Scope:** Cloud service selection criteria cover security certifications (ISO 27001, SOC 2, C5), data residency options, encryption capabilities, access control features, API security and incident response maturity. The scope of permitted usage for each cloud service is defined and communicated to users.
- **Cloud Roles & Responsibilities:** Roles and responsibilities for the use and management of each cloud service are documented. The assignment covers service administration, security configuration, access management, monitoring, incident handling and cost management.
- **Shared Responsibility Model:** For each cloud service, a shared responsibility matrix documents which information security controls are managed by the cloud service provider and which are managed by the organisation. The matrix is reviewed at each contract renewal and after significant service changes.
- **Provider Security Capabilities:** The organisation identifies and utilises the information security capabilities provided by each cloud service provider, including encryption, identity management, logging, monitoring and threat detection features. Configuration is aligned with the organisation's security requirements.
- **Assurance Mechanisms:** Assurance on cloud provider security controls is obtained through recognised certification frameworks (C5, ISO 27001, SOC 2 Type II), compliance dashboards provided by the cloud service provider and, where necessary, independent third-party assessments.
- **Multi-Cloud Management:** When multiple cloud services from different providers are used, a consistent approach manages controls, interfaces and changes across all services. Integration points are documented and security configurations are harmonised to prevent gaps between provider environments.
- **Cloud Incident Procedures:** Procedures for handling information security incidents that occur in connection with cloud services are documented. The procedures define communication channels with the provider, evidence preservation steps, forensic support arrangements and notification obligations.
- **Ongoing Cloud Risk Management:** The organisation monitors, reviews and evaluates the ongoing use of cloud services to manage information security risks. Reviews include security posture assessments, service performance analysis and compliance status verification at least annually.
- **Exit Strategy:** Each cloud service has a documented exit strategy that covers data export procedures, format specifications, timeline requirements, deletion confirmation and transition to an alternative provider or in-house infrastructure. Exit strategies are tested periodically to validate feasibility. Concentration risk is assessed to avoid critical dependency on a single provider.

### 7.2 Cloud Service Provider Obligations

- **Architecture Standards:** Cloud service providers deliver solutions based on industry-accepted standards for architecture and infrastructure. Compliance with recognised frameworks is verified through certification or independent assessment.
- **Access Controls:** Access controls of the cloud service are configured to meet the organisation's requirements, including multi-factor authentication, role-based access control, least-privilege assignment and session management. Administrative access is restricted and logged.
- **Malware Protection:** The cloud service provider implements malware monitoring and protection solutions appropriate to the service model. For IaaS, the organisation deploys its own endpoint protection on provisioned resources.
- **Data Residency:** The organisation's sensitive information is processed and stored only at approved locations within defined geographic regions or legal jurisdictions. Data residency requirements are specified in the agreement and verified through technical controls or provider attestation.
- **Dedicated Incident Support:** The cloud service provider delivers dedicated support in the event of an information security incident in the cloud environment. Support includes a named security contact, defined response times and collaboration procedures for forensic investigation.
- **Sub-Contracting Governance:** The organisation's security requirements are maintained when cloud services are further sub-contracted to external suppliers. The agreement specifies whether sub-contracting is permitted and, if so, under what conditions. Where required, sub-contracting is prohibited.
- **Digital Evidence Support:** The cloud service provider supports the organisation in gathering digital evidence, taking into account laws and regulations for digital evidence across applicable jurisdictions. Evidence preservation procedures and access mechanisms are defined in the agreement.
- **Exit Support & Service Continuity:** The cloud service provider delivers appropriate support and maintains service availability for an adequate transition period when the organisation decides to exit the service. Minimum transition periods are specified in the agreement.
- **Backup & Recovery:** The cloud service provider delivers the required backup of data and configuration information and securely manages backups. Backup scope, frequency and retention are aligned with the organisation's requirements. Restoration capability is tested at least annually.
- **Data & Configuration Return:** The cloud service provider returns information such as configuration files, source code and data owned by the organisation upon request during the service provision or at termination. Return formats and procedures are specified in the agreement.

### 7.3 Change Notification Requirements

- **Infrastructure Changes:** The cloud service provider notifies the organisation in advance of changes to the technical infrastructure that affect the cloud service offering, including relocation, reconfiguration or changes in hardware or software. The notification period and approval mechanism are defined in the agreement.
- **Jurisdictional Changes:** Processing or storing information in a new geographic or legal jurisdiction requires advance notification and explicit approval from the organisation. The security and compliance implications of the jurisdictional change are assessed before approval.
- **Sub-Contractor Changes:** The cloud service provider notifies the organisation before using new or changing existing sub-contractors for the delivery of cloud services. The organisation reviews the security posture of the new party before granting approval.

The organisation maintains close contact with its cloud service providers. These contacts enable mutual exchange of information about information security for the use of cloud services, including mechanisms for both parties to monitor service characteristics and report failures to meet agreed service objectives.

## 8. Roles & Responsibilities

- **Top Management:** Approves this policy, the outsourcing strategy and risk acceptance decisions for supplier relationships. Allocates resources for supplier security management.
- **Information Security Officer (ISO):** Defines information security requirements for supplier agreements, conducts or coordinates supplier security assessments, reviews audit results and advises on supplier-related risk treatment decisions.
- **Supplier Relationship Manager:** Maintains the supplier and outsourcing register, coordinates ongoing monitoring activities, manages the agreement lifecycle and produces regular supplier status reports for management.
- **Procurement:** Ensures the standardised contract template with security clauses is used for all supplier agreements. Involves information security and legal representatives in contract negotiations.
- **IT Operations:** Implements and manages technical controls for supplier access, monitors supplier-related security events and coordinates with suppliers on incident response and vulnerability remediation.
- **Legal & Compliance:** Reviews contractual clauses for legal sufficiency, advises on data protection and regulatory obligations and supports dispute resolution processes.
- **Process Owners:** Define business requirements for outsourced services, participate in supplier evaluations and approve service level targets for their respective processes.
- **All Employees:** Follow the rules of engagement for supplier interactions and report suspected security incidents involving supplier personnel or services.

## 9. Review & Maintenance

This policy is reviewed:

- At least annually, as part of the ISMS management review cycle.
- After significant information security incidents involving suppliers.
- When the supplier landscape changes materially, including onboarding of critical new suppliers or termination of key relationships.
- Following changes to legal, regulatory or contractual requirements affecting supplier management.
- After audit findings that reveal material gaps in supplier security management.
- When threat intelligence indicates elevated risks in the supply chain.
