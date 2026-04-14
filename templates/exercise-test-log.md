# BCM Exercise & Test Log

> **Document control**  
> Owner: Business Continuity Lead  
> Approved by: Information Security Officer  
> Version: 1.0  
> Effective date: 2026-04-01  
> Classification: Internal

## Purpose

This document records all business continuity and disaster recovery exercises, tests, and drills carried out by Nordwind Logistics GmbH. It serves as the primary evidence that continuity capabilities are validated regularly, as required by ISO/IEC 27001:2022 Annex A 5.29 and A 5.30 and ISO 22301 clause 8.5.

---

## Exercise EX-2025-03 — Portal failover partial simulation

| Field | Value |
|---|---|
| Date | 2025-09-15 |
| Type | Partial simulation (technical failover + business-process continuation) |
| Scope | CP-01 — Logistics portal outage scenario (Scenario A) |
| Duration | 4 hours |
| Participants | BCM Lead, IT Ops Lead, 2 dispatchers, 1 customer service agent, Vendor X contact |
| Observer | ISO |

**Objective:** Validate that manual logistics fallback LOG-FB-01 can reach 30% booking capacity within 2 hours of declared outage.

**Scenario:** Simulated loss of the logistics portal at 09:00. Dispatchers switched to manual intake procedures.

**Results:**

- Fallback activated at T+12 min (target: T+15 min). **Passed.**
- 30% capacity reached at T+1h 45min (target: T+2h). **Passed.**
- Full capacity restored after portal was re-enabled at T+4h 20min. Reconciliation completed at T+5h 10min. **Passed.**

**Findings:**

- **Finding 1 (Medium):** The printed route sheet was 48 hours old instead of the target 24 hours. Root cause: scheduled export script failed silently. **CAPA-2025-011** — Add monitoring to the export script and alert on failure. Closed 2025-10-02.
- **Finding 2 (Low):** Two customer service agents did not know where to find the fallback playbook. Refresher training scheduled.
- **Finding 3 (Low):** The vendor contact number in the crisis binder was outdated. Updated immediately.

**Overall assessment:** The exercise objectives were achieved. Two procedural improvements and one data-quality CAPA.

---

## Exercise EX-2025-04 — Tabletop incident response

| Field | Value |
|---|---|
| Date | 2025-11-10 |
| Type | Tabletop exercise |
| Scope | Ransomware scenario — IRP + CP-01 + crisis communications |
| Duration | 3 hours |
| Participants | CMT (full), IT Ops, SecOps, DPO, Comms Lead |
| Observer | External — Cobalt Alliance Security GmbH |

**Scenario:** Simulated ransomware attack discovered at 02:30 on a Saturday. Encryption detected on file server and two domain controllers. Ransom note demands EUR 900,000 in Bitcoin.

**Key decisions exercised:**

- Activation of incident response + BCM + crisis communications.
- Decision not to pay (formal CMT decision documented).
- Regulatory notification timeline (BSI 24h early warning + BfDI 72h).
- Customer communication strategy and press holding statement.

**Findings:**

- **Finding 1 (High):** No clear owner for the 24h NIS2 early-warning notification outside office hours. **CAPA-2025-012** — Update IRP to designate the on-call engineer as the initial declarer. Closed 2026-01-05.
- **Finding 2 (Medium):** The CMT had no clear legal counsel contact for ransom-pay decisions. Added to the crisis binder.
- **Finding 3 (Medium):** The press holding statement template was outdated. Rewritten and integrated into the crisis communication template.
- **Finding 4 (Low):** Several participants were unfamiliar with the incident severity matrix. Training added to the 2026 plan.

**Overall assessment:** The team handled the scenario with a clear decision structure. Four findings — none blocking, one immediately closed.

---

## Test TR-2026-01 — Customer database restore

| Field | Value |
|---|---|
| Date | 2026-02-15 |
| Type | Technical restore test |
| Scope | DR-001 Customer database (AST-001) |
| Duration | 3 hours |
| Participants | IT Ops Lead, DBA |
| Observer | ISO |

**Objective:** Validate that the customer database can be restored from the offsite backup within the 4-hour RTO with data loss ≤ 15 minutes (RPO).

**Method:** Full restore into an isolated DR environment. Verified row counts, referential integrity, and application connectivity against a masked test frontend.

**Results:**

- Restore completed in **2h 50min** (target: 4h). **Passed.**
- Data loss measured at **12 minutes** (target: 15 min). **Passed.**
- Application connectivity verified with all major queries.

**Findings:** None.

**Overall assessment:** Restore test successful. No changes required. Next test: 2026-05-15.

---

## Test TR-2026-02 — Domain controller failover

| Field | Value |
|---|---|
| Date | 2026-01-20 |
| Type | Technical failover test |
| Scope | DR-003 Domain controllers (AST-005) |
| Duration | 2 hours |
| Participants | IT Ops Lead, system administrator |
| Observer | None |

**Result:** Failover to secondary DC completed in 1h 30min (target: 2h). Authentication verified. Passed.

**Findings:** None.

---

## Drill DR-2026-01 — Evacuation drill (Hamburg HQ)

| Field | Value |
|---|---|
| Date | 2026-03-05 |
| Type | Physical evacuation drill |
| Scope | Full HQ evacuation |
| Duration | 45 min |
| Participants | All HQ staff (56 people) |
| Observer | Fire department + Facilities Lead |

**Result:** Building cleared in 6 min 40s (target: <8 min). All staff accounted for at the muster point. Passed.

**Findings:**

- **Finding 1 (Low):** One emergency exit door was temporarily blocked by delivery boxes. Immediately cleared. Reminder issued to the warehouse team.

---

## Upcoming exercises (2026 plan)

| ID | Type | Scope | Planned Date | Lead |
|---|---|---|---|---|
| EX-2026-01 | Tabletop | Supplier failure (Vendor X Logistics) + CP-01 | 2026-05-20 | BCM Lead |
| TR-2026-03 | Technical restore | DR-001 Customer database | 2026-05-15 | IT Ops Lead |
| TR-2026-04 | Technical failover | DR-002 Logistics portal (with vendor) | 2026-06-10 | IT Ops Lead |
| EX-2026-02 | Full walk-through | CP-01 end-to-end with dispatch team | 2026-09-15 | BCM Lead |
| EX-2026-03 | Tabletop | Data breach (GDPR Art. 33) + crisis comms | 2026-11-10 | DPO + ISO |
| DR-2026-02 | Evacuation | Hamburg HQ | 2026-09-03 | Facilities Lead |

---

*Log reviewed quarterly by the BCM Lead and included in the management review inputs.*
