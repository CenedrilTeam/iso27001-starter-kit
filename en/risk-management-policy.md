# Risk Management Policy

> **Document control**  
> Owner: [POLICY_OWNER_ROLE, e.g. Information Security Officer]  
> Approved by: [APPROVER_NAME_AND_ROLE]  
> Version: [VERSION]  
> Effective date: [EFFECTIVE_DATE]  
> Next review: [NEXT_REVIEW_DATE]

## 1. Legal/Regulatory Basis

ISO/IEC 27001:2022 — Information Security Management Systems (Clauses 6.1, 6.2, 8.2, 8.3).

ISO/IEC 27005:2022 — Information Security Risk Management.

BSI IT-Grundschutz:

- BSI-Standard 200-3 (Risk Analysis based on IT-Grundschutz)
- ISMS.1 (Security Management)

Additional jurisdiction-specific laws and regulations that apply to [YOUR_ORGANISATION_NAME] are listed in the Legal Register and are incorporated by reference. Typical examples include data protection laws (e.g. GDPR), sector-specific regulations (e.g. NIS2, DORA, HIPAA) and contractual security requirements from key customers.

## 2. Purpose & Scope

This Risk Management Policy defines the methodology for identifying, analysing, evaluating and treating information security risks at **[YOUR_ORGANISATION_NAME]**. It establishes a systematic, repeatable process that ensures risks are managed consistently and in alignment with the organisation's risk appetite and strategic objectives.

The policy applies to all information assets, business processes, IT systems and third-party services within the scope of the ISMS. It is used by risk owners, the Information Security Officer, management and all personnel involved in risk assessment and treatment activities.

The risk management process follows ISO/IEC 27005:2022 and is structured in four phases: risk identification, risk analysis, risk evaluation and risk treatment. This policy documents the complete methodology so that an auditor or stakeholder can understand how the organisation conducts risk management.

## 3. Risk Context & Risk Sources

### 3.1 Establishing the Context

Before conducting a risk assessment, the context is established by considering the external and internal factors identified in the ISMS scope (Information Security Policy, Clause 4.1), the requirements of interested parties (Information Security Policy, Clause 4.2) and the scope boundaries of the ISMS (Information Security Policy, Clause 4.3). The risk assessment scope covers all assets, processes and services within the ISMS boundary.

### 3.2 Risk Source Catalogue

Risks are identified through a catalogue of risk sources that covers the full spectrum of potential origins. Risk sources are grouped into the following categories:

- **Human Intentional:** State-related actors, organised crime, terrorist groups, ideological activists, specialised hacking outfits, amateur hackers, insiders/avengers, and pathological attackers. Each source is characterised by its typical motivation (espionage, financial gain, disruption, influence).
- **Human Unintentional:** Employees and partners who cause security events through lack of awareness, negligence or insufficient resources.
- **Non-Hacking Intentional:** Petty criminals (theft, arson), market competitors and data brokers acting through non-technical means.
- **Environmental:** Natural disasters, extreme weather events and other environmental conditions that affect information processing facilities.
- **Technical:** Hardware malfunctions and software defects that lead to security-relevant failures.

The risk source catalogue is maintained as static reference data and is updated when new source categories emerge or existing categories no longer reflect the current threat landscape.

## 4. Risk Identification (ISO 27001 Clause 6.1.2)

Risk identification follows a structured, asset-based approach that links organisational assets to threats and vulnerabilities to produce risk scenarios. The identification process proceeds through the following steps:

### 4.1 Identification of Assets

Primary information assets (data, records, intellectual property) and supporting assets (IT systems, applications, network infrastructure, personnel, physical facilities) are identified from the ISMS asset inventory. Each primary asset is assigned confidentiality, integrity and availability (CIA) requirements based on the information classification scheme.

### 4.2 Identification of Threats

For each supporting asset, applicable threats are identified from the threat catalogue. Threats describe adverse actions or events that exploit vulnerabilities. Each threat is linked to one or more risk sources and characterised by the affected CIA dimension(s). The threat catalogue covers categories including cyber-attacks, physical intrusion, social engineering, environmental events and technical failures.

### 4.3 Identification of Vulnerabilities

Vulnerabilities — weaknesses in assets or controls that can be exploited by threats — are identified for each supporting asset. Sources include vulnerability assessments, penetration tests, audit findings, vendor advisories and incident investigations. Vulnerabilities are categorised by the asset type they affect.

### 4.4 Risk Scenario Construction

Risk scenarios are constructed by combining a primary asset, supporting asset(s), a vulnerability, a threat and the associated risk source into a coherent narrative. Each scenario describes a plausible path from threat exploitation to business impact. Scenarios capture which CIA dimensions are affected (confidentiality, integrity, availability) and identify the risk owner — the person accountable for managing the risk.

## 5. Risk Analysis

### 5.1 Impact Assessment

The potential impact of each risk scenario is assessed across the following business-relevant dimensions: **Financial**, **Reputational**, **Legal & Regulatory**, **Operational** and **Safety & Personnel**. Each dimension is rated on a 5-level scale from **Very Low** (level 1) to **Very High** (level 5).

The overall impact score for a scenario is determined using the **highest single value** method across all assessed dimensions. This ensures that a severe impact in any one dimension is not masked by lower ratings in others. Organisations may alternatively use a weighted average where specific dimensions (e.g. Safety) should dominate the final score.

### 5.2 Likelihood Assessment

The likelihood of each risk scenario occurring is assessed on a 5-level scale from **Very Unlikely** (level 1) to **Almost Certain** (level 5). Likelihood assessment considers historical incident data, threat intelligence, vulnerability scan results, the effectiveness of existing controls and expert judgement.

### 5.3 Risk Score Calculation

The risk score for each scenario is calculated as:

**Risk Score = Impact × Likelihood**

This produces a risk score range from 1 to 25. The risk score is plotted on a 5×5 risk matrix that visualises the distribution of all assessed scenarios.

## 6. Risk Evaluation

Each assessed risk is compared against the defined risk acceptance thresholds to determine whether treatment is required. The following risk levels are defined:

- **Very Low (1–4):** Accepted without further action. Monitored as part of normal operations.
- **Low (5–8):** Accepted with documented justification. Monitored during scheduled reviews.
- **Medium (9–12):** Treatment recommended. Reviewed by the Information Security Officer.
- **High (13–16):** Treatment required. Escalated to top management if not treated within the defined timeline.
- **Very High (17–25):** Immediate treatment required. Reported to top management without delay.

Risks are prioritised by their risk score in descending order. Risks that exceed the acceptance threshold require immediate treatment. Risks within the acceptance threshold are documented and monitored. The risk evaluation results are recorded in the risk register.

## 7. Risk Treatment (ISO 27001 Clause 6.1.3)

For each risk that requires treatment, one of the following treatment options is selected:

### 7.1 Treatment Options

- **Risk Avoidance:** The activity or condition that gives rise to the risk is eliminated entirely. The risk source is removed by discontinuing the process, decommissioning the asset or withdrawing from the business activity. Avoided risks have a residual risk score of zero.
- **Risk Modification (Controls):** One or more security controls from the ISO 27001 Annex A control set are applied to reduce the impact, the likelihood, or both. Controls are selected based on their effectiveness against the specific threat-vulnerability combination. Multiple controls can be linked to a single risk scenario. The residual risk after control implementation is re-assessed.
- **Risk Sharing (Transfer):** The risk is shared with an external party through insurance, outsourcing, contractual allocation or other arrangements. The organisation retains accountability for the risk but transfers the financial or operational consequences. Sharing arrangements are documented with the receiving party, the scope of transfer and any residual risk retained.
- **Risk Retention (Acceptance):** The risk is accepted without further treatment. Retention is appropriate when the risk score falls within the acceptance threshold, when the cost of treatment exceeds the potential impact, or when management makes an informed decision to accept the risk. Each retained risk requires documented justification and formal acceptance by the risk owner.

### 7.2 Statement of Applicability

The Statement of Applicability (SoA) documents all controls from ISO 27001 Annex A, their applicability status and justification. For each applicable control, the SoA records whether the control is implemented, partially implemented or planned. Controls that are not applicable include a justification for exclusion. The SoA is maintained as a living document and updated whenever controls are added, removed or modified.

### 7.3 Residual Risk

After treatment measures are applied, the residual risk for each scenario is re-assessed using the same impact and likelihood scales. The residual risk score is compared against the acceptance thresholds. Residual risks that still exceed the acceptance threshold are escalated to management for decision. All residual risks are formally accepted by their risk owners and documented in the risk treatment plan.

## 8. Risk Treatment Plan

The risk treatment plan (RTP) is the central document that tracks the implementation of risk treatment decisions. For each treated risk scenario, the RTP records:

- The original risk score and risk level.
- The selected treatment option and the specific controls or measures to be implemented.
- The responsible person (risk owner) and the implementation timeline.
- The target residual risk score after treatment.
- The actual residual risk score after implementation, verified through re-assessment.
- The status of each treatment action (planned, in progress, implemented, verified).

The RTP is reviewed at each management review to track progress, identify overdue actions and adjust priorities based on changing risk levels. Treatment effectiveness is measured by comparing the total risk exposure before and after treatment.

## 9. Risk Communication

Risk information is communicated to stakeholders to support informed decision-making:

- **Top Management:** Receives aggregated risk reports including the risk matrix, risk level distribution, treatment progress and residual risk status through the management review process.
- **Risk Owners:** Are informed of the risks assigned to them, the required treatment actions, deadlines and the current residual risk status.
- **Information Security Officer:** Maintains the risk register, coordinates risk assessments and facilitates risk treatment planning.
- **Interested Parties:** The Stakeholder Register identifies which interested parties require risk-related communication, including customers, regulators and business partners, and defines the scope, frequency and channel of communication.

## 10. Monitoring & Review

Risk assessments are performed at planned intervals and on an event-driven basis. The following triggers initiate a risk re-assessment:

- **Scheduled review:** At least annually as part of the ISMS management review cycle.
- **Significant change:** Organisational restructuring, new business processes, technology changes, relocation or expansion of the IT infrastructure.
- **Incident or near miss:** Information security incidents, data breaches or near-miss events that reveal previously unidentified risks or invalidate existing risk assessments.
- **Threat landscape change:** New threat intelligence, emerging attack vectors, changes in the regulatory environment or published vulnerability disclosures affecting systems in scope.
- **Audit findings:** Internal or external audit results that identify control deficiencies or new risk areas.
- **Supplier or third-party change:** Changes to supplier risk profiles, contractual arrangements or third-party service levels.

The effectiveness of risk treatment measures is monitored through control testing, vulnerability assessments, penetration tests and incident trend analysis. Monitoring results feed into the next risk assessment cycle.

## 11. Continual Improvement

The risk management process is subject to continual improvement. Lessons learned from risk assessments, treatment effectiveness reviews, incidents and audit findings are used to refine the methodology, update the risk source and threat catalogues, improve the accuracy of impact and likelihood assessments, and enhance the integration of risk management into business processes.

Improvement actions are documented in the corrective and preventive action (CAPA) register and tracked through the ISMS corrective action process. Changes to the risk management methodology are approved by management and communicated to all personnel involved in risk management activities.

## 12. Roles & Responsibilities

- **Top Management:** Approves this policy and the risk acceptance criteria. Accepts residual risks that exceed the acceptance threshold through informed decision. Reviews risk status in the management review.
- **Information Security Officer (ISO):** Maintains the risk management process, facilitates risk assessments, coordinates risk treatment planning and reports risk status to management.
- **Risk Owners:** Are accountable for the risks assigned to them. Approve treatment plans for their risks, monitor treatment implementation and accept residual risks within their authority.
- **Asset Owners:** Provide input on asset value, CIA requirements and vulnerability information for their assigned assets. Support impact assessment by describing the business consequences of asset compromise.
- **Department Heads:** Participate in risk identification and analysis for their areas of responsibility. Ensure that treatment actions assigned to their departments are implemented on schedule.
- **All Employees:** Report potential risks, vulnerabilities and incidents through established channels. Participate in risk-related training and awareness activities.

## 13. Review & Maintenance

This policy is reviewed:

- At least annually, as part of the ISMS management review cycle.
- When the risk assessment methodology requires adjustment based on lessons learned.
- When significant changes to the organisational context, threat landscape or regulatory environment affect risk management practices.
- When audit findings or incident investigations identify deficiencies in the risk management process. 
