# Internal Audit Plan and Report — 2026

> **Document control**  
> Owner: Information Security Officer  
> Approved by: CEO  
> Version: 1.0  
> Effective date: 2026-01-15  
> Classification: Internal

## Part A — Annual Internal Audit Plan 2026

### 1. Purpose and scope

This plan describes how Nordwind Logistics GmbH conducts internal audits of its information security management system in 2026, in accordance with ISO/IEC 27001:2022 clause 9.2. The plan ensures that the ISMS is independently and impartially verified against ISO requirements and against the organisation's own policies, and that the audit programme covers the entire ISMS at least once over the three-year cycle 2024–2026.

**ISMS scope under audit:** all processes, locations and assets within the ISMS scope statement v3.0 (Hamburg HQ + Rotterdam branch).

### 2. Audit principles

- **Independence:** auditors do not audit their own work. Where internal capacity is insufficient, an external auditor is engaged.
- **Impartiality:** findings are based on evidence, not opinion.
- **Risk-based prioritisation:** areas with higher risk or recent change are audited more frequently.
- **Continual improvement:** every audit produces input for the next management review and the CAPA register.

### 3. Three-year coverage matrix

| ISO clause / area | 2024 | 2025 | 2026 |
|---|---|---|---|
| 4 Context of the organisation | x |  | x |
| 5 Leadership |  | x |  |
| 6 Planning + risk management | x | x | x |
| 7 Support (resources awareness documentation) |  | x | x |
| 8 Operation | x | x | x |
| 9 Performance evaluation | x | x | x |
| 10 Improvement | x | x | x |
| Annex A.5 Organisational | partial | partial | full |
| Annex A.6 People | partial | full | partial |
| Annex A.7 Physical | full |  | partial |
| Annex A.8 Technological | partial | partial | full |

### 4. 2026 audit schedule

| Audit ID | Scope | Type | Lead Auditor | Planned Date | Effort | Status |
|---|---|---|---|---|---|---|
| IA-2026-Q1 | Access control + HR security (A.5.15-18 + A.6) | Internal | Anna Weber (ISO) + peer | 2026-02-10 | 3 days | Completed |
| IA-2026-Q2 | Cryptography + data deletion + classification (A.8.10-12 + A.8.24 + A.5.12-13) | Internal | Anna Weber + external peer | 2026-05-12 | 3 days | Planned |
| IA-2026-Q3 | Supplier security + cloud (A.5.19-23) | Internal | Anna Weber | 2026-08-18 | 2 days | Planned |
| IA-2026-Q4 | BCM + incident management (A.5.24-30 + A.8.13-14) | Internal | External auditor (Cobalt Alliance) | 2026-11-09 | 4 days | Planned |
| EA-2026-Surveillance | Full ISMS surveillance audit | External certification | KPMG | 2026-05-18 | 5 days | Planned |

### 5. Methodology

Each internal audit follows the same five-phase approach:

1. **Plan:** confirm scope, criteria, sampling, and notify auditees one week in advance.
2. **Conduct:** opening meeting → document review → interviews → observation → sampling.
3. **Report:** draft findings classified as Major nonconformity, Minor nonconformity, Observation, or Opportunity for improvement.
4. **Closing:** present findings to auditees, agree on facts, hand over to closing meeting.
5. **Follow-up:** findings are entered into the CAPA register and tracked to closure.

### 6. Audit criteria

- ISO/IEC 27001:2022 (full standard).
- ISO/IEC 27002:2022 (control guidance, where useful).
- Internal policies and procedures listed in the document control register.
- Applicable legal and regulatory requirements from the legal register.
- Contractual customer commitments.

### 7. Resources and competence

The internal audit programme requires an estimated 12 person-days for 2026, covered by the ISO and one external co-auditor for independence. The lead internal auditor (Anna Weber) holds a current ISO/IEC 27001 Lead Auditor certification. External auditors are required to hold equivalent qualifications and to provide a recent CV before the engagement.

### 8. Reporting and management review

A consolidated audit summary is prepared by the ISO at the end of each quarter and included in the management review inputs. Major nonconformities are escalated immediately and do not wait for the management review cycle.

---

## Part B — Internal Audit Report IA-2026-Q1

### 1. Audit identification

| Field | Value |
|---|---|
| Audit ID | IA-2026-Q1 |
| Audit type | Internal |
| Scope | Access control (A.5.15–A.5.18) + HR security (A.6.1–A.6.6) |
| Audit criteria | ISO/IEC 27001:2022 + Access Control Policy v2.0 + HR Security Policy v1.5 |
| Lead auditor | Anna Weber (ISO) |
| Co-auditor | Tobias Becker (external — independence) |
| Audit dates | 2026-02-08 to 2026-02-10 |
| Auditees | HR Lead, IT Operations Lead, two department heads, three sampled employees |
| Report date | 2026-02-12 |

### 2. Audit objectives

- Verify that joiner / mover / leaver processes work as documented.
- Verify that access rights are reviewed and adjusted in line with the Access Control Policy.
- Verify that HR security controls (screening, NDAs, awareness) are implemented and evidenced.

### 3. Methodology applied

- Document review: HR Security Policy, Access Control Policy, joiner/leaver checklists, last quarterly access review report, screening procedure.
- Interviews with HR Lead and IT Operations Lead.
- Sampling: 10 joiner records (Q4 2025 + Q1 2026), 5 leaver records, 2 mover records, 2 quarterly access reviews.
- Walk-through of the joiner workflow with one new hire.
- System inspection: Active Directory account creation logs, MDM enrolment, Personio onboarding records.

### 4. Findings summary

| Finding | Classification | Clause | Status |
|---|---|---|---|
| F-01 Three joiner accounts created without approval ticket | Minor nonconformity | A.5.18 | Open — CAPA-2026-001 |
| F-02 Quarterly access review for marketing OU not completed in Q4 2025 | Minor nonconformity | A.5.18 | Open — CAPA-2026-006 |
| F-03 Background screening evidence not stored consistently | Observation | A.6.1 | Open — to be discussed at MR |
| F-04 Strong joiner workflow with clear automation | Strength | — | Closed (positive) |
| F-05 Leaver checklist effective — 2h revocation target met for sampled records | Strength | A.5.11 + A.6.5 | Closed (positive) |

### 5. Detailed findings

#### F-01 — Joiner accounts created without approval ticket

**Classification:** Minor nonconformity
**Clause:** A.5.18 Access rights
**Evidence:** Sample of 10 joiner records included three accounts (created on 2025-11-04, 2025-12-09, 2026-01-22) where the IT Operations team created the AD account before the HR onboarding ticket existed in Personio. The corresponding tickets were created retroactively the following day.
**Risk:** Account creation without prior approval bypasses the access governance gate and could allow over-privileged or premature access.
**Recommendation:** Enforce a hard gate in the joiner workflow that prevents AD account creation without a linked approved Personio ticket. Add a monthly reconciliation of AD accounts created vs. Personio tickets.
**Action:** CAPA-2026-001 (HR Lead, due 2026-05-15).

#### F-02 — Quarterly access review for marketing OU not completed in Q4 2025

**Classification:** Minor nonconformity
**Clause:** A.5.18 Access rights
**Evidence:** The Q4 2025 quarterly access review report covers all OUs except marketing. The marketing OU was scheduled for review on 2025-12-15 but the meeting was cancelled and not rescheduled.
**Risk:** Without a recent access review, dormant or inappropriate marketing OU access rights could persist.
**Recommendation:** Complete the missing review for the marketing OU within 30 days. Add a formal escalation rule: any cancelled access review must be rescheduled within 5 working days.
**Action:** CAPA-2026-006 (IT Operations Lead, due 2026-03-15).

#### F-03 — Background screening evidence not stored consistently

**Classification:** Observation
**Evidence:** For two of five sensitive-role hires sampled, the background check confirmation was filed in the HR Lead's personal mailbox rather than the encrypted HR archive.
**Risk:** Personal mailbox storage is not retention-controlled and creates a risk of loss or unauthorised access.
**Recommendation:** Update the screening procedure to require all evidence to be filed in the encrypted HR archive within 5 working days.
**Action:** Discuss at next management review; lightweight CAPA expected.

### 6. Strengths observed

- The joiner workflow is well documented, automated, and integrated between Personio and Active Directory.
- The leaver process consistently meets the 2-hour access revocation target — all five sampled leaver accounts were disabled within 90 minutes of the leaver date.
- HR Lead and IT Operations Lead demonstrated a strong working relationship, with clear escalation paths for exceptions.

### 7. Closing meeting

A closing meeting was held on 2026-02-10 at 16:00 with the HR Lead, IT Operations Lead, and the audited employees. All findings were presented, facts were confirmed without dispute, and corrective action timelines were agreed.

### 8. Conclusion

The audit objectives were achieved. The scope of the audit (access control + HR security) is largely effective, with two minor nonconformities and one observation. None of the findings affect the validity of the ISMS certification. All findings are tracked in the CAPA register and will be reported at the next management review.

---

*Approved: Anna Weber, Information Security Officer — 2026-02-12.*
