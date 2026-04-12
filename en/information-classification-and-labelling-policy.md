# Information Classification & Labelling Policy

> **Document control**  
> Owner: [POLICY_OWNER_ROLE, e.g. Information Security Officer]  
> Approved by: [APPROVER_NAME_AND_ROLE]  
> Version: [VERSION]  
> Effective date: [EFFECTIVE_DATE]  
> Next review: [NEXT_REVIEW_DATE]

## 1. Legal/Regulatory Basis

ISO/IEC 27001:2022 / ISO/IEC 27002:2022, Annex A — Organisational Controls:

- A 5.12 — Classification of Information
- A 5.13 — Labelling of Information

BSI IT-Grundschutz:

- ISMS.1.A10 (Security Concept)
- BSI-Standard 200-2 Chapter 5.1 (Classification of Business Processes and Information)
- BSI-Standard 200-2 Chapter 8.2 (Protection Needs Assessment)

Additional jurisdiction-specific laws and regulations — in particular data protection law (GDPR), trade secret protection and sector-specific confidentiality requirements — are listed in the Legal Register and incorporated by reference.

## 2. Purpose & Scope

This policy establishes a consistent classification and labelling scheme for information and other associated assets at **[YOUR_ORGANISATION_NAME]**. It ensures that information receives an appropriate level of protection in accordance with its importance to the organisation, considering requirements for confidentiality, integrity and availability.

This policy applies to:

- All information assets, regardless of format (digital, paper, verbal)
- All associated assets (systems, storage media, applications) that process, store or transmit classified information
- All employees, contractors and third parties who handle information belonging to or entrusted to the organisation

The classification scheme provides the basis for access control decisions, handling rules and protective measures across [YOUR_ORGANISATION_NAME].

## 3. Classification of Information (A 5.12)

The owners of information (asset owners) are accountable for their classification. Classifications and associated protective controls take account of business needs for sharing or restricting information, for protecting integrity and assuring availability, as well as legal requirements. Assets other than information are classified in compliance with the classification of information that is stored in, processed by, or otherwise handled or protected by the asset.

Information can cease to be sensitive or critical after a certain period of time. Over-classification leads to unnecessary controls and additional expense; under-classification leads to insufficient protection. Classification levels are reviewed periodically and adjusted when business requirements or the threat landscape change.

### 3.1 Classification Conventions & Review

[YOUR_ORGANISATION_NAME] classifies information along three protection dimensions: **confidentiality**, **integrity** and **availability**. Each dimension uses a defined set of levels. The asset owner assigns a classification level per dimension upon creation of the information asset. The classification is reviewed:

- At least annually as part of the asset inventory review.
- Whenever the content, context or use of the information changes materially.
- When the information is shared with new parties or used in new business processes.
- When the information reaches the end of a defined retention period or is made public.

### 3.2 Confidentiality Levels

[YOUR_ORGANISATION_NAME] uses the following four confidentiality levels. Each level reflects the impact that unauthorised disclosure would have on the organisation:

#### PUBLIC

*Information intended for unrestricted distribution. Disclosure causes no harm to the organisation.*

- **Access:** No access restrictions. Available to the general public.
- **Storage:** No special storage requirements. Standard organisational storage is sufficient.
- **Transmission:** No restrictions on transmission method. May be shared freely.
- **Disposal:** Standard disposal procedures (recycling for paper, normal deletion for digital files).
- **Labelling:** Labelling as PUBLIC is optional. Unlabelled information is not automatically considered public.

#### INTERNAL

*Information for internal use only. Unauthorised disclosure could cause minor inconvenience but no significant damage.*

- **Access:** Access restricted to employees and authorised external personnel. Need-to-know principle recommended but not mandatory.
- **Storage:** Store on organisational systems with standard access controls. Physical documents in standard office areas (no public-facing locations).
- **Transmission:** Use organisational email or approved file-sharing platforms. Encryption recommended but not mandatory for internal transmission.
- **Disposal:** Paper: dispose via office shredder or confidential waste bin. Digital: standard deletion from organisational systems.
- **Labelling:** Label documents, emails and file shares as INTERNAL. Use header/footer markings on documents.

#### CONFIDENTIAL

*Sensitive business information. Unauthorised disclosure could cause significant damage to the organisation, its partners or its customers.*

- **Access:** Access restricted to specifically authorised individuals on a strict need-to-know basis. Access is approved by the information owner.
- **Storage:** Digital: store on access-controlled systems with encrypted storage. Physical: store in locked cabinets or secured office areas.
- **Transmission:** Use encrypted email or secure file transfer. Do not use public cloud services unless approved and encrypted. Physical transfer via sealed, opaque envelope.
- **Disposal:** Paper: cross-cut shredding (DIN 66399 security level P-4 or higher). Digital: secure deletion using approved tools; encrypted media may be disposed of after key destruction.
- **Labelling:** All documents, files and containers are clearly labelled as CONFIDENTIAL. Email subject lines include the classification label.

#### STRICTLY CONFIDENTIAL

*Highly sensitive information (e.g. trade secrets, special categories of personal data). Unauthorised disclosure could cause severe or existential damage.*

- **Access:** Access strictly limited to named individuals with explicit authorisation from the information owner and senior management. Access lists are maintained and reviewed regularly.
- **Storage:** Digital: store only on specifically designated, encrypted systems with multi-factor access control. Physical: store in safes or high-security rooms with access logging.
- **Transmission:** End-to-end encryption mandatory. Use only approved secure channels. No transmission via standard email. Physical transfer only by trusted courier with chain-of-custody documentation.
- **Disposal:** Paper: cross-cut shredding (DIN 66399 security level P-5 or higher) with witnessed destruction. Digital: cryptographic erasure or physical destruction of media, documented and witnessed.
- **Labelling:** All documents, files and containers are prominently labelled as STRICTLY CONFIDENTIAL. Every page carries the classification label. Email subject lines include the classification label.

### 3.3 Integrity Levels

[YOUR_ORGANISATION_NAME] uses the following integrity levels. Each level reflects the impact that unauthorised modification or loss of correctness would have on the organisation:

- **Normal:** Minor inaccuracies are tolerable and can be corrected without significant effort.
- **High:** Inaccuracies could cause notable damage. Correctness is verifiable.
- **Very High:** Information is correct at all times. Any alteration could cause severe harm.

### 3.4 Availability Levels

[YOUR_ORGANISATION_NAME] uses the following availability levels. Each level reflects the impact that a loss of availability would have on the organisation:

- **Normal:** Downtime of up to several days is tolerable.
- **High:** Maximum tolerable downtime is a few hours. Longer outages cause significant business impact.
- **Very High:** Information is available at all times. Any outage causes severe damage.

### 3.5 Alignment with Access Control

The classification scheme is aligned with [YOUR_ORGANISATION_NAME]'s access control policy. Access rights are granted based on the classification level of the information: the higher the classification, the more restrictive the access controls. Role-based access control (RBAC) and the principle of least privilege are applied. Access decisions reference the classification level assigned by the asset owner.

### 3.6 Organisational Consistency

This classification scheme is mandatory across all departments, business units and locations of [YOUR_ORGANISATION_NAME]. The following measures ensure consistent application:

- This policy is communicated to all personnel during onboarding and via periodic awareness training.
- Classification procedures are integrated into document management, project management and IT service management processes.
- Templates for common document types include pre-formatted classification labels.
- The Information Security Officer conducts periodic spot checks to verify correct classification.

### 3.7 Cross-Organisational Classification

The classification scheme used by [YOUR_ORGANISATION_NAME] may differ from schemes used by partner organisations, even when level names appear similar. When agreements with other organisations include information sharing, the agreements specify procedures to identify the classification of exchanged information and to interpret the classification levels of the other organisation. Correspondence between different schemes is determined by comparing the associated handling and protection methods.

## 4. Labelling of Information (A 5.13)

Labelling procedures cover information and other associated assets in all formats. The labelling reflects the classification scheme established above. Labels are easily recognisable and applied consistently so that all personnel can immediately determine the classification of any information they encounter.

### 4.1 Labelling Methods

Asset owners ensure that information is labelled according to the following methods, depending on the format and medium:

- **Paper documents:** Classification label in the header or footer of every page. Cover pages and first pages carry a prominent label. Folders and binders are labelled on the spine and front cover.
- **Electronic documents:** Classification label in the document header/footer (for office documents), in the file name (using a prefix such as *CONFIDENTIAL_Report_2025.pdf*) and/or via document metadata properties.
- **Email:** Classification label at the beginning of the subject line (e.g. [CONFIDENTIAL]). Sensitive attachments carry their own classification labels.
- **Storage media:** Physical media (USB drives, external hard drives, backup tapes) are labelled with the highest classification level of the information they contain.
- **Applications and databases:** Classification metadata is applied at the data field, record or container level where technically feasible. Systems that do not support per-record classification protect all contained information at the highest classification level present.
- **Verbal communication:** Before discussing classified information verbally (in meetings, phone calls, video conferences), the speaker states the classification level and ensures that only authorised individuals are present.

### 4.2 Digital Metadata

[YOUR_ORGANISATION_NAME] uses metadata to identify, manage and control information, especially with regard to confidentiality. Metadata enables efficient searching and allows systems to interact and make decisions based on classification labels. The labelling procedures describe how to attach metadata to information, what labels to use and how data is handled, in line with the organisation's information model and ICT architecture. Relevant additional metadata (e.g. which process created the information and when) is added by systems when they process information.

### 4.3 Exceptions from Labelling

[YOUR_ORGANISATION_NAME] defines the following cases where labelling may be omitted or simplified:

- **PUBLIC information:** Labelling is optional for information at the lowest confidentiality level, as the absence of a label does not imply a higher classification. However, unlabelled information is not assumed to be public without verification.
- **Internal communications of routine nature:** Routine internal emails and chat messages that do not contain information above the INTERNAL level do not require explicit classification labels, unless they are forwarded externally.
- **Automated data flows:** Where information flows between systems are fully automated and access-controlled, per-item labelling may be replaced by system-level classification, provided the system protects all contained information at the appropriate level.

Even when labelling is omitted, the asset owner remains responsible for ensuring that the information is handled in accordance with its classification level.

### 4.4 Handling Unlabellable Information

In certain situations, labelling is technically or practically not feasible (e.g. verbal information, live demonstrations, legacy systems without metadata support). In these cases:

- Information that cannot be labelled is treated as **CONFIDENTIAL** until the asset owner assigns and communicates a classification.
- The asset owner documents the classification in the asset inventory and ensures that all individuals handling the information are informed of its classification verbally or in writing.
- When unlabelled information is exported from a system (e.g. via printout, download or forwarding), the exporting person applies the appropriate label at the point of export.

### 4.5 Awareness & Training

All personnel are made aware of labelling procedures and receive the necessary training to ensure information is correctly labelled and handled. Personnel are also informed that labelling can sometimes have unintended negative effects, as classified assets may become easier to identify by malicious actors. This risk is mitigated through complementary access controls and the principle of least privilege rather than through obscurity.

Output from systems containing information classified as sensitive or critical carries an appropriate classification label.

## 5. Roles & Responsibilities

- **Top Management:** Approves this policy, ensures adequate resources for implementation and sets the organisational expectation for proper information handling.
- **Information Security Officer (ISO):** Maintains this policy, defines and reviews classification levels, conducts spot checks on classification and labelling compliance and provides guidance to asset owners.
- **Asset Owners (Information Owners):** Classify the information they own, assign and review classification levels, approve access requests for their information and ensure that labelling and handling rules are followed.
- **IT Department:** Implements technical controls for labelling (metadata, DLP, templates), enforces access controls aligned with classification levels and ensures systems can support classification metadata.
- **All Personnel:** Apply classification labels correctly, handle information in accordance with its classification, report suspected misclassification and participate in awareness training on classification and labelling.

## 6. Review & Maintenance

This policy is reviewed:

- At least annually as part of the ISMS management review cycle.
- When business requirements for information sharing or protection change materially.
- After significant security incidents involving misclassification or information leakage.
- When changes to the legal or regulatory framework affect classification requirements (e.g. new data protection regulations, trade secret law amendments).
- When the organisation enters into new information-sharing agreements with external parties that require alignment of classification schemes.
