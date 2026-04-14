# Management Review Minutes — 2026-Q1

> **Document control**  
> Owner: Information Security Officer  
> Approved by: CEO  
> Version: 1.0  
> Effective date: 2026-03-30  
> Classification: Internal

## Meeting details

- **Organisation:** Nordwind Logistics GmbH
- **Scope reviewed:** ISMS as per Statement of Applicability v3.0
- **Date:** 2026-03-30, 09:00–12:30
- **Location:** HQ Hamburg, room Nordsee + Teams
- **Chair:** Katharina Meier (CEO)
- **Minutes:** Anna Weber (ISO)

## Attendees

| Name | Role | Present |
|---|---|---|
| Katharina Meier | CEO | Yes |
| Thomas Weissenberg | CFO | Yes |
| Anna Weber | Information Security Officer | Yes |
| Markus Schulz | IT Operations Lead | Yes |
| Julia Hoffmann | Data Protection Officer | Yes |
| Thomas Krüger | HR Lead | Yes |
| Elena Fischer | Finance Lead | Yes |
| Sebastian Brand | Head of Engineering | Yes |
| Lisa Hartmann | Head of Sales | Apologies — input submitted in writing |

## Agenda (ISO/IEC 27001:2022 clause 9.3.2)

1. Status of actions from previous management review
2. Changes in external and internal issues
3. Feedback on ISMS performance (nonconformities, monitoring, audit results, control effectiveness, fulfilment of objectives)
4. Feedback from interested parties
5. Results of risk assessment and risk treatment plan status
6. Opportunities for continual improvement
7. Decisions and actions

---

## 1. Status of previous actions

From management review 2025-Q4 (2025-12-15), four actions were tracked. Three are closed, one is in progress.

| Action | Owner | Due | Status |
|---|---|---|---|
| Formalise vulnerability SLA by severity | IT Ops Lead | 2026-02-28 | Closed — published in IT Operations Policy v1.5 |
| Deploy FIDO2 to admin accounts | ISO | 2026-06-30 | In progress — phase 1 complete (CHG-2026-002) |
| Update leaver checklist to enforce 2h access revocation | HR Lead | 2026-03-31 | Closed — new checklist in use since 2026-03-01 |
| Roll out M365 backup via Veeam for M365 | IT Ops Lead | 2026-02-28 | Closed — operational since 2026-02-10 |

## 2. Changes in external and internal issues

**External:**

- NIS2 transposition act in force since 2026-01-01. Nordwind Logistics is classified as an "important entity" in the transport sector. Registration with BSI completed on 2026-01-18.
- Customer segment "cross-border e-commerce" grew by 22% in the last two quarters, increasing volume of personal data processed.
- Threat landscape: BSI Lagebericht 2025 confirms ransomware remains the top operational risk for mid-size logistics.

**Internal:**

- New office in Rotterdam opened on 2026-02-15 (9 staff). In scope of the ISMS from day one.
- Reorganisation in Finance: new Finance Lead since 2026-02-01.
- M365 tenant consolidation project started; will change parts of the access control architecture in Q3.

## 3. ISMS performance

### 3.1 Nonconformities and corrective actions

Five CAPAs open in the quarter, two closed, three in progress. No overdue major nonconformities. Reference: CAPA register.

### 3.2 Monitoring and measurement results (KPIs)

| KPI | Target | Actual Q1 | Trend |
|---|---|---|---|
| Phishing simulation click rate | <5% | 4.2% | ↓ from 5.8% |
| MFA coverage (user accounts) | 100% | 100% | stable |
| MFA coverage (admin accounts, phishing-resistant) | 100% | 48% | ↑ (FIDO2 rollout in progress) |
| Critical patches within SLA (14 days) | 100% | 92% | ↓ from 96% — see CAPA-2026-004 |
| Backup restore test success rate | 100% | 100% | stable |
| Mean time to detect (MTTD) | <2h | 1h 35min | ↑ (improvement) |
| Mean time to respond (MTTR, high severity) | <24h | 17.3h | ↑ (improvement) |
| Security awareness training completion | >95% | 96% | stable |

### 3.3 Audit results

- **Internal audit 2026-Q1** completed on 2026-02-10 (scope: access control + HR security). Three findings, all in CAPA.
- **External surveillance audit** scheduled for 2026-05-18 (KPMG).

### 3.4 Control effectiveness

- Technical controls: effective overall. DLP partial implementation (endpoint part outstanding, tracked as RTP-006).
- Organisational controls: effective. Policy conformance check in February showed 97% acknowledgement rate.
- Physical controls: one incident (see 3.6) — controls worked as designed.

### 3.5 Fulfilment of security objectives (from 2026 plan)

| Objective | Status |
|---|---|
| Reduce phishing click rate below 5% | Achieved (4.2%) |
| Reach 100% phishing-resistant MFA for admins by 2026-06-30 | On track |
| Complete FIDO2 rollout for all staff by 2026-09-30 | On track |
| Close all high-severity vulns within SLA for 2 consecutive quarters | Not achieved this quarter |
| Pass external surveillance audit with no major findings | Pending (May) |

### 3.6 Incidents

Ten recorded security incidents (INC-2026-001 to INC-2026-010). One was a reportable GDPR breach (INC-2026-006, accidental email disclosure — 45 records, no sensitive categories). Notification to BfDI was sent within 32 hours. Data subjects were informed on the same day. Post-incident review completed; CAPA-2026-005 tracks the corrective actions.

No NIS2 early-warning notifications were required this quarter.

## 4. Feedback from interested parties

- **Customers:** One complaint about unencrypted contract attachment — root cause of CAPA-2026-005. Otherwise no complaints. Customer satisfaction survey (Q1) returned 4.3/5 for "security and trust".
- **Employees:** Awareness survey (Q1) returned 4.1/5. Feedback requested clearer guidance on AI tool use — to be addressed in AUP v2.2.
- **Works council:** Accepted the FIDO2 rollout plan. Requested additional clarity on screen monitoring rules during remote work — to be added to Remote Working Policy.
- **Regulators (BfDI):** Acknowledged the breach notification without follow-up.
- **Suppliers:** No incidents reported by critical suppliers.

## 5. Risk assessment and treatment

Risk register reviewed. Five main risks:

- **R-001 Ransomware** — treatment progressing, residual score unchanged until FIDO2 and segmentation complete.
- **R-002 Phishing** — residual score lowered from 12 to 9 after phishing simulation improvements.
- **R-003 Insider data exfiltration** — DLP work ongoing.
- **R-004 Supplier outage** — accepted with monitoring; second provider qualification in Q2/Q3.
- **R-005 Misconfiguration** — S3 account-wide block implemented (RTP-011 closed). IaC scan in progress.

Risk appetite remains: low for confidentiality and integrity breaches affecting customer data, medium for availability impacts under 4 hours.

No new top-level risks identified this quarter.

## 6. Opportunities for improvement

- Introduce AI acceptable-use addendum to the AUP.
- Automate vulnerability SLA reporting via SIEM dashboard.
- Extend supplier security questionnaire with NIS2 alignment section.
- Pilot a red team exercise with external provider in Q4.

## 7. Decisions and actions

| # | Decision / Action | Owner | Due | Type |
|---|---|---|---|---|
| MR-2026-Q1-01 | Approve ISMS Statement of Applicability v3.0 | CEO | 2026-03-30 | Decision |
| MR-2026-Q1-02 | Approve risk treatment plan update (RTP v4) | CEO | 2026-03-30 | Decision |
| MR-2026-Q1-03 | Allocate budget EUR 15,000 for FIDO2 staff rollout | CEO | 2026-03-30 | Decision |
| MR-2026-Q1-04 | Draft AUP addendum on AI tool use | ISO | 2026-05-31 | Action |
| MR-2026-Q1-05 | Build vulnerability SLA dashboard in SIEM | IT Ops Lead | 2026-06-30 | Action |
| MR-2026-Q1-06 | Qualify second logistics SaaS provider | Procurement | 2026-12-31 | Action |
| MR-2026-Q1-07 | Plan red team exercise for Q4 (scope + vendor shortlist) | ISO | 2026-08-31 | Action |
| MR-2026-Q1-08 | Prepare external surveillance audit (KPMG, 2026-05-18) | ISO | 2026-05-11 | Action |

**Conclusion:** The ISMS is suitable, adequate and effective. Continuing direction: reinforce identity controls (FIDO2), improve vulnerability handling, and prepare for NIS2 audit readiness.

**Next management review:** 2026-06-29.

---

*Minutes approved by Katharina Meier (CEO) on 2026-04-02.*
