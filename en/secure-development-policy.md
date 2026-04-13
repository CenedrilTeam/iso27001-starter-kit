# Secure Software Development Policy

> **Document control**  
> Owner: [POLICY_OWNER_ROLE, e.g. Information Security Officer]  
> Approved by: [APPROVER_NAME_AND_ROLE]  
> Version: [VERSION]  
> Effective date: [EFFECTIVE_DATE]  
> Next review: [NEXT_REVIEW_DATE]

## 1. Legal/Regulatory Basis

ISO/IEC 27001:2022 / ISO/IEC 27002:2022, Annex A — Technological Controls:

- A 8.25 — Secure Development Life Cycle
- A 8.26 — Application Security Requirements
- A 8.27 — Secure System Architecture and Engineering Principles
- A 8.28 — Secure Coding
- A 8.29 — Security Testing in Development and Acceptance
- A 8.30 — Outsourced Development
- A 8.31 — Separation of Development, Test and Production Environments
- A 8.33 — Test Information
- A 8.34 — Protection of Information Systems During Audit Testing

BSI IT-Grundschutz:

- CON.8 (Software Development)
- CON.10 (Development of Web Applications)
- APP.6 (General Software)
- APP.7 (Development of Individual Software)
- OPS.1.1.6 (Software Tests and Approvals)
- OPS.2.3 (Outsourcing for Customers)
- ISMS.1 (Security Management)
- DER.3.1 (Audits and Revisions)
- DER.3.2 (Audits Based on the BSI Guideline for IS Audits)

Additional jurisdiction-specific laws — in particular data protection law (GDPR), export control regulations, sector-specific compliance requirements (e.g. financial services, healthcare) and software liability obligations — are listed in the Legal Register and incorporated by reference.

## 2. Purpose & Scope

This policy establishes the rules for secure software development at **[YOUR_ORGANISATION_NAME]**. It covers the secure development life cycle, application security requirements, secure system architecture and engineering principles, secure coding, security testing, outsourced development, environment separation, test information protection and audit testing safeguards.

The policy applies to all personnel involved in software development, testing, deployment and maintenance, including in-house developers, architects, testers, project managers, operations staff and external development partners.

## 3. Secure Development Life Cycle (A 8.25)

A secure development life cycle governs all software development activities. A suitable development methodology is selected for each project or product — whether classic waterfall, agile or continuous delivery — and covers security requirements throughout every phase from design to deployment and maintenance. The methodology is documented and communicated to all development teams.

### 3.1 Life Cycle Elements

- **Environment Separation:** Development, test and production environments are adequately separated to prevent unauthorised access and unintended changes to production systems. Separate virtual or physical domains are used (see environment separation section of this policy).
- **Security in the Methodology:** Security activities are embedded at every stage of the chosen development methodology. This includes threat modelling during design, secure architecture reviews before implementation, and security sign-off before release.
- **Secure Coding Guidelines:** Language-specific secure coding guidelines are maintained for each programming language in use. These guidelines define approved patterns, prohibited constructs (e.g. hard-coded credentials, insecure defaults) and naming conventions.
- **Security Requirements in Specification & Design:** Security requirements are identified during the specification and design phase of every project, based on the information classification and protection requirements of the data being processed (see project security requirements).
- **Security Checkpoints:** Security checkpoints are integrated at defined milestones in every project. At each checkpoint, the project team verifies that the applicable security requirements are met before proceeding to the next phase.
- **System & Security Testing:** Comprehensive testing is performed throughout the development process, including functional tests, regression tests, automated static code analysis (SAST), dynamic application security testing (DAST) and penetration tests for systems with elevated protection requirements.
- **Secure Repositories:** Source code and configuration artefacts are stored in access-controlled repositories. Repository access follows the principle of least privilege, and all changes are traceable through version history.
- **Version Control Security:** Version control systems enforce change traceability — every commit is attributed to an identified author. Branch protection rules prevent direct pushes to release branches, and a backup concept covers all repositories.
- **Security Knowledge & Training:** Developers receive training in secure development practices before contributing to security-relevant code. Training covers requirements analysis, threat modelling, secure architecture, secure coding techniques and security testing methods.
- **Developer Capability:** Developers are qualified to prevent, find and fix security vulnerabilities. Qualification is verified through training records, code review participation and demonstrated proficiency in using static analysis and vulnerability scanning tools.
- **Licensing & Alternatives:** Software licensing requirements are evaluated during technology selection. Alternatives are considered to ensure cost-effective solutions while avoiding future licensing conflicts or vendor lock-in (see IPR compliance).
- **Outsourced Development Assurance:** Where development is outsourced, the supplier provides documented assurance of compliance with these secure development rules. Contractual clauses, audit rights and evidence of secure practices are required (see outsourced development section of this policy).

Project, function and interface documentation is maintained throughout the life cycle. Security-relevant aspects are documented separately for administrators and users. Architecture diagrams and threat models are kept up to date as the system evolves.

## 4. Application Security Requirements (A 8.26)

Information security requirements are identified, specified and approved as part of the requirements analysis for every application that processes, stores or transmits organisational information. These requirements are derived from the business context, the classification of the information involved, applicable legislation and the organisation's risk appetite.

### 4.1 General Requirements

- **Identity Trust & Authentication:** The required level of trust in user identity is determined for each application. Authentication mechanisms are selected accordingly — from simple password-based login for low-sensitivity functions to multi-factor authentication for privileged or high-classification access (see the *Access Control Policy*).
- **Information Type & Classification:** Each application identifies the types and classification levels of information it processes. Processing, storage and display controls are aligned with the applicable classification level.
- **Access Segregation:** Access to data and functions within the application is segregated based on roles and responsibilities. The level of access granted to each role is documented, and role-based access control (RBAC) enforces the principle of least privilege.
- **Resilience Against Attacks:** Applications are designed to withstand malicious attacks and unintentional disruptions. Input validation is performed server-side, output encoding prevents injection attacks (e.g. SQL injection, cross-site scripting), and buffer overflow protections are applied.
- **Legal & Regulatory Compliance:** Legal, statutory and regulatory requirements applicable in every jurisdiction where a transaction is generated, processed, completed or stored are identified during requirements analysis and addressed in the application design.
- **Privacy Requirements:** Privacy requirements are assessed for all parties whose personal data is processed by the application. Data minimisation, purpose limitation and consent management are addressed in the design.
- **Confidential Information Protection:** Confidential information receives dedicated protection measures — encryption at rest and in transit, access logging and restricted display (e.g. masking in user interfaces).
- **Data Protection in Transit & at Rest:** Data is protected during processing, in transit and at rest using encryption algorithms and key lengths appropriate to the classification level. Sensitive data stored temporarily (e.g. in caches or session storage) is cleared when no longer needed.
- **Communication Encryption:** Communications between all involved parties are encrypted. TLS 1.2 or higher is the minimum standard for web-based communications; internal service-to-service calls use mutual TLS or equivalent mechanisms.
- **Input Controls:** All user and system inputs are validated against expected data types, lengths and ranges. Integrity checks (e.g. checksums, hash verification) are applied to data received from external systems. Server-side validation is performed regardless of any client-side checks.
- **Automated Controls:** Automated controls enforce business rules — approval limits, dual-approval workflows and segregation-of-duty checks are implemented in application logic rather than relying solely on manual processes.
- **Output Controls:** Application outputs are controlled to ensure only authorised recipients receive information. Output authorisation checks verify that the requesting user has the appropriate access rights before data is rendered or exported.
- **Free-Text Field Restrictions:** Free-text input fields are restricted in length and content to prevent uncontrolled storage of confidential or personal data. Where free-text fields are necessary, content scanning or classification tagging is applied.
- **Business Process Requirements:** Requirements derived from business processes — transaction logging, audit trails, monitoring integration and non-repudiation — are captured during requirements analysis and implemented as part of the application architecture.
- **Integration with Security Controls:** Applications integrate with centralised security controls: logging and monitoring systems, data leakage prevention tools and security information and event management (SIEM) platforms. Security-relevant events are logged in a format compatible with the organisation's logging infrastructure.
- **Error Message Handling:** Error messages are designed to provide users with actionable information without disclosing internal system details, stack traces, database structures or other information that could aid an attacker. Detailed error information is logged server-side for debugging.

### 4.2 Transactional Services

- **Mutual Identity Trust:** For transactional services, the required level of mutual identity trust between parties is determined and implemented. Digital certificates, electronic signatures or equivalent mechanisms verify each party's identity before transactions are processed.
- **Information Integrity:** The integrity of information exchanged or processed is verified using cyclic redundancy checks, cryptographic hashes or digital signatures. Any lack of integrity is detected and flagged before the transaction completes.
- **Authorisation for Key Documents:** Authorisation processes define who is permitted to approve, issue or sign key transactional documents. Approval workflows enforce segregation of duties and are documented in the application's authorisation matrix.
- **Confidentiality & Non-Repudiation:** Key documents — including contracts, tenders and formal agreements — are protected for confidentiality, integrity, proof of dispatch and proof of receipt. Digital signatures or sealed audit logs provide non-repudiation evidence.
- **Transaction Confidentiality & Integrity:** Transactions (e.g. orders, delivery addresses, receipt confirmations) are protected through end-to-end encryption and integrity verification throughout their entire processing chain.
- **Transaction Confidentiality Duration:** The period during which a transaction remains confidential is defined based on business and legal requirements. Cryptographic protections are maintained for the full duration of the confidentiality period.
- **Insurance & Contractual Requirements:** Insurance requirements and other contractual obligations relating to transactional services are identified and addressed in the application design and supporting operational procedures.

### 4.3 Electronic Ordering & Payment

- **Order Information Confidentiality & Integrity:** Order information is encrypted in transit and at rest. Integrity checks prevent unauthorised modification of order details between submission and fulfilment.
- **Payment Verification:** Payment information supplied by customers is verified to an appropriate degree — address verification, card validation codes and fraud detection mechanisms are applied proportionally to the transaction value and risk.
- **Transaction Duplication Prevention:** Controls prevent loss or duplication of transaction information. Idempotency mechanisms, unique transaction identifiers and reconciliation processes are implemented.
- **Secure Transaction Storage:** Transaction details are stored on systems within the organisational intranet, not on storage platforms directly accessible from the internet. No transaction data is retained on publicly accessible environments or electronic storage media exposed to the public network.
- **Trusted Authority Integration:** Where a trusted authority (e.g. a certificate authority for digital signatures or certificates) is used, security is integrated throughout the entire end-to-end certificate or signature management process, including issuance, renewal, revocation and validation.

## 5. Secure System Architecture & Engineering Principles (A 8.27)

Secure engineering principles are established, documented and applied to all information system development and engineering activities. These principles are reviewed regularly and updated to reflect emerging threats and evolving best practices. Systems are designed based on a security requirements catalogue, a security profile derived from the information classification and a threat model.

### 5.1 Security Control Analysis

- **Full Range of Controls:** The system architecture addresses the full range of security controls required to protect information and systems against identified threats. Control selection is based on the risk assessment and the asset's classification level.
- **Control Capabilities:** Each security control is evaluated for its capability to prevent, detect or respond to security events. Controls are selected to provide a layered defence that addresses all three capabilities.
- **Business-Process-Specific Controls:** Specific security controls required by particular business processes — such as encryption of sensitive information, integrity checking and digital signing — are identified and incorporated into the architecture.
- **Control Placement:** The architecture specifies where and how each security control is applied, whether integrated into the application, the infrastructure layer or a centralised security service. Placement decisions align with the overall security architecture.
- **Integrated Control Set:** Individual security controls — both manual and automated — are designed to work together as an integrated set. Dependencies between controls are documented, and gaps in the overall control chain are identified and addressed.

### 5.2 Engineering Considerations

- **Security Architecture Integration:** Every system design integrates with the organisation's overarching security architecture. Common security services (identity management, logging, encryption) are reused rather than rebuilt.
- **Technical Security Infrastructure:** The design leverages the existing technical security infrastructure — public key infrastructure (PKI), identity and access management (IAM), data leakage prevention and dynamic access management — rather than introducing parallel mechanisms.
- **Organisational Capability:** Technology choices are evaluated against the organisation's capability to develop, operate and support the chosen solution over its full life cycle. Technologies that exceed available internal expertise are selected only when external support arrangements are in place.
- **Cost, Time & Complexity:** The cost, time and complexity of meeting security requirements are considered during technology selection. Trade-offs are documented and approved by the project sponsor and the Information Security Officer.
- **Current Good Practices:** System designs reflect current good practices from industry standards, vendor guidance and recognised security frameworks. Design teams monitor relevant advisories and adjust patterns as the threat landscape evolves.

### 5.3 Secure Design Principles

- **Architecture Principles:** The following architecture principles apply to all system designs: "security by design", "defence in depth", "security by default", "default deny", "fail securely", "distrust input from external applications", "security in deployment", "assume breach", "least privilege", "usability and manageability" and "least functionality". Each design document identifies which principles are applied and how.
- **Security-Oriented Design Review:** A security-oriented design review is conducted for every system before implementation begins. The review identifies information security and privacy vulnerabilities, ensures that security controls are specified and confirms that all security requirements are addressed.
- **Residual Risk Documentation:** Where a security control does not fully meet the stated requirements (e.g. due to overriding safety or usability requirements), the gap is documented and formally acknowledged by the risk owner. Compensating controls are identified where feasible.
- **System Hardening:** All systems are hardened before deployment. Unnecessary services, ports and features are disabled. Default credentials are changed, and only required software components are installed. Hardening baselines are defined per technology stack.

### 5.4 Zero Trust Principles

- **Assume Breach:** System designs assume that the organisation's information systems are already breached. Security controls are not reliant on network perimeter security alone; internal segmentation, monitoring and detection capabilities are built into every layer.
- **Never Trust, Always Verify:** A "never trust and always verify" approach is applied to all access to information systems. Every request is authenticated and authorised regardless of the requester's network location.
- **End-to-End Encryption:** Requests to information systems are encrypted end-to-end. Encryption is not terminated at intermediate network boundaries unless inspection is explicitly required and documented.
- **External-Origin Assumption:** Every request to an information system is verified as if it originated from an open, external network — even when the request originates internally. No automatic trust is granted based on network location.
- **Least Privilege & Dynamic Access:** Access control follows the principle of least privilege. Dynamic access control techniques authenticate and authorise requests based on contextual information — authentication credentials, user identity, endpoint device posture, data classification and situational risk indicators (see the *Access Control Policy*).
- **Strong Authentication:** All requesters are authenticated and all authorisation requests are validated based on user identity, authentication credentials and endpoint device data. Strong authentication (e.g. multi-factor authentication) is enforced for access to systems processing classified information (see the *Access Control Policy*).

## 6. Secure Coding (A 8.28)

Secure coding principles apply to all software development — both in-house and outsourced. A secure coding policy defines organisation-specific expectations, approved principles and prohibited practices. Development tools are configured to support secure coding, and developers receive ongoing training in secure coding techniques.

### 6.1 Planning & Preparation

- **Expectations & Approved Principles:** Organisation-specific expectations and approved principles for secure coding are documented and communicated to all development teams. These apply equally to in-house developers and outsourced code development.
- **Common & Historical Defects:** A catalogue of common and historical coding practices and defects that lead to security and privacy vulnerabilities is maintained. The catalogue is updated when new vulnerability classes emerge and is used as input for training and code review checklists.
- **Development Tool Configuration:** Development tools — including integrated development environments (IDEs), linters and build pipelines — are configured to enforce secure coding rules automatically. Code that violates defined rules is flagged at the earliest possible stage.
- **Vendor Guidance:** Guidance issued by the providers of development tools and execution environments is followed. Security advisories from tool vendors are reviewed and applied in a timely manner.
- **Updated Development Tools:** Development tools (compilers, build systems, dependency managers, static analysis tools) are kept up to date. Tool updates are applied according to the organisation's patch management process, and outdated tool versions are retired.
- **Developer Qualification:** Developers are qualified in writing secure code before they contribute to production systems. Qualification is evidenced through completed training, certifications or demonstrated experience reviewed by a senior developer.
- **Secure Design & Threat Modelling:** Secure design practices and threat modelling are applied during the planning phase of every development effort. Threat models identify relevant threat actors, attack vectors and required countermeasures.
- **Secure Coding Standards:** Secure coding standards are documented for each technology stack. Where recognised industry standards exist (e.g. OWASP, CERT Secure Coding Standards), these are adopted and supplemented with organisation-specific rules. Compliance with the standards is mandatory for all production code.
- **Controlled Development Environments:** Development is performed in controlled environments with defined access rights, approved toolchains and standardised configurations. Uncontrolled or personal environments are not used for production-targeted code.

### 6.2 During Coding

- **Language-Specific Practices:** Secure coding practices specific to the programming languages and techniques being used are defined and followed. These cover language-specific pitfalls such as memory management in C/C++, injection prevention in web languages and serialisation security in Java/.NET.
- **Secure Programming Techniques:** Secure programming techniques are used throughout development — pair programming for security-critical code, refactoring to eliminate security debt, mandatory peer review for all merge requests, dedicated security iterations and test-driven development for security functions.
- **Structured Programming:** Structured programming techniques are employed to produce clear, maintainable and verifiable code. Complex logic is decomposed into well-defined modules with explicit interfaces.
- **Documentation & Defect Removal:** Code is documented to a level that enables independent review. Programming defects that could allow security or privacy vulnerabilities to be exploited are identified and removed during development, not deferred to post-release.
- **Prohibited Design Patterns:** The following insecure design patterns are prohibited: hard-coded passwords or API keys, unapproved code samples from untrusted sources, unauthenticated web services, disabled certificate validation and use of deprecated cryptographic algorithms. Automated checks in the build pipeline detect and block these patterns.
- **Static Analysis During Development:** Static application security testing (SAST) is integrated into the build pipeline and runs on every code change. SAST findings above the defined severity threshold block the build until they are resolved or formally accepted.
- **Attack Surface & Least Privilege:** Before software is made operational, the attack surface is evaluated and minimised. The principle of least privilege is applied to all runtime permissions — services run with the minimum permissions required for their function.
- **Common Programming Error Analysis:** Before software is made operational, an analysis of the most common programming errors (e.g. OWASP Top 10, CWE Top 25) is conducted and documented. The analysis confirms that all applicable error classes have been mitigated.

### 6.3 Review & Maintenance

- **Secure Packaging & Deployment:** Updates are securely packaged and deployed. Installation, update and patch files are verified using checksums or digital signatures before deployment. Deployment pipelines enforce integrity verification as a mandatory step.
- **Vulnerability Handling:** Reported information security and privacy vulnerabilities are handled through the organisation's vulnerability management process (see IT operations policy). Fixes are developed, tested and released according to severity-based timelines.
- **Error & Attack Logging:** Errors and suspected attacks are logged. Security event logs are forwarded to the centralised logging infrastructure and reviewed regularly. Code adjustments are made as necessary based on log analysis findings.
- **Source Code Protection:** Source code is protected against unauthorised access and tampering. Configuration management tools provide access control and version control. Access rights to repositories are reviewed quarterly.
- **External Library Management:** External libraries are managed through a maintained inventory that tracks library name, version, licence and known vulnerabilities. Libraries are updated with each release cycle, and end-of-life libraries are replaced. Vulnerabilities discovered in third-party components are managed through the Security Operations vulnerability management process, including severity-based remediation timelines.
- **Component Selection & Reuse:** Well-vetted, proven components are selected and reused — particularly for authentication and cryptographic functions. In-house reimplementation of standard security functions is avoided. Components are authorised before inclusion in the codebase.
- **External Component Provenance:** The licence, security history and provenance of every external component are evaluated before adoption. Components with known unresolved vulnerabilities, unfavourable licence terms or unclear maintenance status are rejected.
- **External Software Maintainability:** External software tools and libraries are selected only from proven, reputable sources. Each library's maintainability is assessed — active community, regular release cadence and responsive security patching are required. Libraries that no longer meet these criteria are scheduled for replacement.
- **Long-Term Availability:** Sufficiently long-term availability of development resources and artefacts is ensured. Build scripts, tool versions and dependency snapshots are archived so that any released version can be rebuilt if necessary.
- **Modified External Packages — Built-in Controls:** When an external software package is modified, the risk of compromising its built-in security controls and integrity verification processes is assessed before the modification proceeds.
- **Modified External Packages — Vendor Consent:** Before modifying an external software package, the need to obtain consent from the vendor is evaluated. Licence terms are reviewed to confirm that modifications are permitted.
- **Modified External Packages — Vendor Updates:** Before modifying an external software package, the possibility of obtaining the required changes from the vendor as a standard program update is explored. Vendor-provided solutions are preferred over custom modifications.
- **Modified External Packages — Maintenance Impact:** Before modifying an external software package, the impact on future maintenance is assessed. If the modification makes the organisation responsible for maintaining the software, the total cost of ownership — including security patching — is evaluated and approved.
- **Modified External Packages — Compatibility:** Before modifying an external software package, compatibility with other software in use is verified. Integration tests confirm that the modification does not introduce regressions in dependent systems.

## 7. Security Testing in Development & Acceptance (A 8.29)

Security testing processes are defined and implemented across the development life cycle and for acceptance of new systems, upgrades and new versions. A test framework is established according to the protection requirements of the system under test, based on the requirements catalogue. Testing covers both functional and non-functional requirements, with particular emphasis on security-critical functions.

### 7.1 Testing Scope

- **Security Functions:** Security functions are tested comprehensively — including user authentication, access restriction, session management and the use of cryptography. Tests verify that security functions operate correctly under normal conditions, under load and when subjected to malformed inputs.
- **Secure Coding Verification:** Tests verify adherence to the secure coding standards defined in this policy. Automated static analysis (SAST) results are included in the test evidence, and any residual findings are documented with justification.
- **Secure Configuration Verification:** Tests confirm that system configurations — including operating system settings, firewall rules and security component configurations — match the approved hardening baselines and do not introduce unintended exposures.

### 7.2 Test Plans

- **Schedule & Activities:** Test plans include a detailed schedule of test activities and individual test cases. The schedule is aligned with the development milestones and accounts for dependency chains between test phases.
- **Inputs & Expected Outputs:** Each test case defines its inputs and the expected outputs under a range of conditions — including valid inputs, boundary values, invalid inputs and malicious payloads.
- **Evaluation Criteria:** Clear pass/fail criteria are established for evaluating test results. A documented comparison of expected versus actual outcomes (target/actual comparison) is produced for each test run.
- **Further Actions:** Test plans define the decision process and further actions to be taken when tests fail — re-test after fix, risk acceptance with documented justification, or escalation to the Information Security Officer for critical findings.

### 7.3 Testing Methods

- **Code Review:** Code review activities are performed as a core element of security testing. Reviews specifically target security flaws, including handling of unanticipated inputs and boundary conditions. Both automated (SAST) and manual review methods are applied.
- **Vulnerability Scanning:** Vulnerability scanning is performed to identify insecure configurations, missing patches and known system vulnerabilities. Scans are executed in the test environment before release and repeated after significant configuration changes.
- **Penetration Testing:** Penetration testing is performed to identify insecure code and design flaws. For systems with elevated protection requirements, penetration tests follow a documented concept that defines methods, scope and success criteria. Results are tracked to remediation.

### 7.4 Outsourced & Acquired Components

- **Acquisition Process:** An established acquisition process is followed for all externally sourced software components. The process includes security evaluation as a mandatory step before procurement approval.
- **Supplier Security Requirements:** Contracts with suppliers address the identified security requirements, including secure development practices, vulnerability disclosure obligations and the right to perform security testing on delivered components (see supplier management).
- **Security Criteria Evaluation:** Acquired products and services are evaluated against defined security criteria before they are accepted into the operational environment. Evaluation includes vulnerability scanning, configuration review and verification of the supplier's security documentation.

A formal release declaration is issued after successful completion of all required tests. The release confirms that the software meets functional, security and legal requirements and is approved for deployment to production. Regression tests verify that security mechanisms and settings are not altered by updates.

## 8. Outsourced Development (A 8.30)

Where software development is outsourced, the organisation directs and monitors the development activity to ensure that security requirements are met. Contractual agreements, defined service levels and regular oversight govern the outsourcing relationship. The organisation retains responsibility for the security of the outsourced deliverables.

### 8.1 Outsourcing Requirements

- **Licensing & Intellectual Property:** Licensing agreements clearly define code ownership and intellectual property rights for all outsourced content. Ownership of source code, documentation and all development artefacts is assigned to the organisation unless explicitly agreed otherwise (see IPR compliance).
- **Contractual Secure Development:** Contracts with external developers include binding requirements for secure design, secure coding, code review and security testing practices as defined in this policy (see sections on secure coding and security testing).
- **Threat Model Provision:** The organisation provides the applicable threat model to external developers. The threat model identifies relevant threat actors, attack vectors and required countermeasures that the external development team integrates into their design and implementation.
- **Acceptance Testing:** Acceptance tests are performed on all deliverables to verify quality and accuracy. Test cases cover functional requirements, security requirements and integration with existing systems. Deliverables that fail acceptance testing are returned for remediation.
- **Security & Privacy Capability Evidence:** External developers provide evidence that minimum acceptable levels of security and privacy capabilities are established — through assurance reports, certifications (e.g. ISO 27001, SOC 2) or independent audit results.
- **Malicious Content Testing:** External developers provide evidence that sufficient testing has been applied to guard against the presence of malicious content — both intentional (e.g. backdoors, logic bombs) and unintentional (e.g. vulnerable dependencies). Delivery packages are scanned independently before acceptance.
- **Vulnerability Testing Evidence:** External developers provide evidence that sufficient testing has been applied to guard against the presence of known vulnerabilities. This includes current SAST and dependency scanning reports delivered with each release.
- **Source Code Escrow:** Escrow agreements for the software source code are established where the outsourced software is critical to business operations. Escrow terms cover release conditions (e.g. supplier insolvency or discontinuation of support) and regular escrow verification.
- **Audit Rights:** Contracts include the contractual right to audit development processes and controls. Audits may be conducted by the organisation or by an independent third party and cover adherence to secure development practices, access controls and change management.
- **Development Environment Security:** Security requirements for the external development environment are specified in the contract. These include environment separation, access control, data protection and secure handling of the organisation's code and data (see environment separation section of this policy).
- **Applicable Legislation:** Contracts address applicable legislation, including data protection laws (e.g. GDPR and applicable national data protection law), export control regulations and sector-specific requirements. The supplier confirms compliance with all relevant legal obligations.

## 9. Separation of Development, Test & Production Environments (A 8.31)

Development, testing and production environments are separated and controlled to reduce the risk of unauthorised access to or changes of the production environment. The separation approach is documented, including the architecture of each environment and the procedures applied after testing is complete.

### 9.1 Environment Separation Rules

- **Adequate Separation:** Development and production systems are adequately separated and operate in different domains — using separate virtual or physical environments, separate network segments and independent access controls.
- **Deployment Rules & Authorisation:** Rules and authorisation requirements for deploying software from development to production are defined, documented and enforced. Only formally tested and approved releases are deployed to production.
- **Testing Before Production:** All changes to production systems and applications are tested in a testing or staging environment prior to deployment. Test evidence is recorded and linked to the change record (see configuration and change management policy).
- **No Testing in Production:** Testing is not performed directly in production environments except in circumstances that are defined, approved and documented in advance. Any approved production testing is time-limited and subject to enhanced monitoring.
- **Development Tools in Production:** Compilers, editors, debuggers and other development tools or utility programs are not accessible from production systems unless they are required for a specific, approved operational purpose. Unnecessary tools are removed.
- **Environment Identification Labels:** Appropriate environment identification labels are displayed in application menus, command prompts and system banners. Visual differentiation (e.g. colour-coded headers) reduces the risk of personnel accidentally executing actions in the wrong environment.
- **Sensitive Information in Non-Production:** Sensitive information is not copied into development or testing environments unless equivalent security controls are provided. Where production data is needed, it is anonymised or pseudonymised before transfer (see the test information section of this policy).
- **Separation of Duties:** No single person has the ability to make changes to both development and production environments without prior review and approval by a second authorised person. Deployment pipelines enforce this separation technically.

### 9.2 Environment Protection

- **Tool Patching & Updates:** All development, integration and testing tools — including build systems, integrators, compilers, configuration systems and libraries — are patched and updated according to the organisation's patch management process.
- **Secure Configuration:** Systems and software in all non-production environments are securely configured following the same hardening principles applied to production, adjusted only where necessary for development or testing purposes.
- **Access Control:** Access to development, test and staging environments is controlled and granted on a need-to-access basis. Access rights are reviewed quarterly and revoked promptly when no longer required.
- **Change Monitoring:** Changes to the environment infrastructure and code stored therein are monitored. Unauthorised modifications trigger alerts and are investigated.
- **Secure Monitoring:** Security monitoring is applied to non-production environments to detect unauthorised access, misuse and security events. Monitoring coverage is proportional to the sensitivity of the data and code in the environment.
- **Environment Backups:** Backups of development, test and staging environments are taken according to a defined schedule. Backups cover source code repositories, build configurations, environment configurations and test data sets.

## 10. Test Information (A 8.33)

Test information is appropriately selected, protected and managed. Where operational data is used for testing, additional controls prevent unauthorised disclosure and ensure compliance with data protection requirements. Personal data used for testing is at least pseudonymised, ideally anonymised; the Data Protection Officer is involved in defining the approach.

- **Access Control Parity:** The same access control procedures that apply to operational environments are applied to test environments containing operational data. Only authorised test personnel access the data, and access is granted for the duration of the test only.
- **Separate Authorisation per Copy:** A separate, documented authorisation is obtained each time operational information is copied to a test environment. The authorisation specifies the data set, the purpose, the responsible person and the expected retention period.
- **Audit Trail:** The copying and use of operational information for testing purposes is logged. The audit trail records who authorised the copy, when the data was transferred, the volume of data and when it was deleted from the test environment.
- **Data Protection by Masking:** Sensitive information used for testing is protected by removal or masking (e.g. anonymisation, pseudonymisation, tokenisation) before it is transferred to the test environment (see the *Data Deletion, Masking & DLP Policy*).
- **Post-Test Deletion:** Operational information is securely deleted from the test environment immediately after testing is complete. Deletion is verified and documented to prevent unauthorised subsequent use of the test data (see the *Data Deletion, Masking & DLP Policy*).

## 11. Protection During Audit Testing (A 8.34)

Audit tests and other assurance activities involving assessment of operational systems are planned and agreed to minimise disruption to business processes. Access granted for audit purposes is strictly controlled, time-limited and revoked immediately upon completion.

- **Management-Agreed Access:** Audit requests for access to systems and data are agreed with appropriate management before access is granted. The scope, timing and systems involved are documented in the audit engagement letter.
- **Scope Control:** The scope of technical audit tests is agreed and controlled. Tests are limited to the systems, data and time windows specified in the approved audit plan. Any scope extension requires separate approval.
- **Read-Only Access Principle:** Audit tests are limited to read-only access to software and data. Where read-only access is not available to obtain the necessary information, an experienced administrator with the required access rights executes the test on behalf of the auditor, with the auditor observing and verifying the results.
- **Device Security Requirements:** Before access is granted, the security posture of devices used for accessing the systems (e.g. laptops, tablets) is established and verified — including current antivirus software, up-to-date patches, disk encryption and compliant configuration.
- **Non-Read-Only Access Controls:** Access other than read-only is permitted only for isolated copies of system files. Copies are securely deleted when the audit is completed, unless there is a documented obligation to retain them under audit documentation requirements, in which case they are given appropriate protection.
- **Special Processing Requests:** Requests for special or additional processing — such as running audit tools, scripts or automated scanners — are identified, agreed in advance and authorised by the system owner before execution.
- **Availability Consideration:** Audit tests that can affect system availability are scheduled outside business hours. Where this is not feasible, the potential impact is assessed and communicated to affected stakeholders in advance.
- **Access Logging:** All access for audit and test purposes is monitored and logged. Audit access logs are retained according to the organisation's log retention schedule and are available for review by the Information Security Officer.

## 12. Roles & Responsibilities

- **Top Management:** Approves this policy, allocates resources for secure development and ensures organisational commitment to security throughout the software development life cycle.
- **Information Security Officer (ISO):** Oversees the implementation of this policy, conducts or coordinates security design reviews, monitors compliance and reports on the maturity of secure development practices.
- **Development Managers:** Ensure that development teams follow the secure development life cycle, coding standards and testing requirements defined in this policy. Approve release declarations and manage security training for their teams.
- **Developers & Architects:** Apply secure coding standards, perform threat modelling and design reviews, remediate security findings and maintain documentation. Participate in security training and share knowledge within the team.
- **Quality Assurance & Testing:** Execute security test plans, perform code reviews, run vulnerability scans and document test results. Escalate critical findings to the Information Security Officer.
- **IT Operations:** Maintain the separation of development, test and production environments, enforce deployment authorisation rules and support audit testing with appropriate access controls.
- **Data Protection Officer:** Advises on privacy requirements for application design, approves the approach for anonymising or pseudonymising test data and reviews data protection aspects of outsourced development contracts.
- **Procurement & Vendor Management:** Ensures that outsourced development contracts include the required security clauses, audit rights and intellectual property provisions defined in this policy.

## 13. Review & Maintenance

This policy is reviewed and, where necessary, updated:

- At least annually as part of the ISMS management review cycle.
- After significant changes to the development organisation, toolchain or technology stack.
- After security incidents related to software vulnerabilities or development process failures.
- When changes in the threat landscape, regulatory environment or industry best practices require adjustments to secure development practices.
