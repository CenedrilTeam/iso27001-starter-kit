# Business Impact Analysis (BIA)

> **Document control**  
> Owner: Business Continuity Lead  
> Approved by: CEO  
> Version: 2.0  
> Effective date: 2026-02-15  
> Next review: 2027-02-15  
> Classification: Confidential

## 1. Purpose and scope

This Business Impact Analysis identifies the critical business processes of Nordwind Logistics GmbH, quantifies the impact of disruptions over time, and defines the recovery objectives (RTO and RPO) that drive the continuity plans and disaster recovery plans.

**Scope:** all business processes of Nordwind Logistics GmbH, including the HQ in Hamburg and the branch in Rotterdam.

## 2. Methodology

The BIA follows ISO 22301 and ISO/IEC 27031 guidance. It was conducted through structured workshops with process owners between 2026-01-20 and 2026-02-10. For each process, the team assessed:

- **Financial impact** across four time buckets: 4 hours, 1 day, 3 days, 1 week.
- **Regulatory impact** (fines, reporting obligations, breach of contract).
- **Reputational impact** (customer confidence, media attention).
- **Operational impact** (inability to serve customers, safety risks).

Each impact was rated on a 1–5 scale. Scores at 1 week were used to derive **Maximum Tolerable Period of Disruption (MTPD)** and to set **Recovery Time Objectives (RTO)** and **Recovery Point Objectives (RPO)** below the MTPD with a safety margin.

## 3. Critical processes

| ID | Process | Owner | MTPD | RTO | RPO | Priority |
|---|---|---|---|---|---|---|
| P-01 | Shipment booking and tracking (customer portal) | Head of Ops | 8h | 4h | 1h | Critical |
| P-02 | Dispatch and route planning | Head of Ops | 12h | 6h | 1h | Critical |
| P-03 | Customer invoicing | CFO | 5 days | 3 days | 24h | High |
| P-04 | Customer support | Head of Sales | 1 day | 8h | 8h | High |
| P-05 | Payroll | HR Lead | 15 days | 7 days | 24h | Medium |
| P-06 | HR administration (excluding payroll) | HR Lead | 10 days | 5 days | 24h | Medium |
| P-07 | Procurement and supplier management | Procurement | 10 days | 5 days | 24h | Medium |
| P-08 | Legal and contract management | Legal | 30 days | 10 days | 7 days | Low |
| P-09 | Marketing | Marketing Lead | 30 days | 15 days | 7 days | Low |

## 4. Detailed assessment (extract — top 3 processes)

### P-01 — Shipment booking and tracking

**Description:** Customers book shipments through the online portal (AST-002) and track them in real time. The process feeds directly into dispatch and customer invoicing.

**Dependencies:**

- IT: AST-002 (logistics portal SaaS), AST-001 (customer database), AST-003 (M365), AST-010 (firewall), internet connectivity at Hamburg and Rotterdam.
- People: 4 dispatchers, 2 customer service agents, 1 IT on-call.
- Suppliers: Vendor X Logistics (SUP-004), AWS (SUP-001).
- Facilities: Hamburg HQ (AST-016) — with Rotterdam as secondary site.

**Impact over time:**

| Time | Financial | Regulatory | Reputational | Operational | Total (1–5) |
|---|---|---|---|---|---|
| 4h | EUR 15,000 lost revenue | Low — SLA monitored | Medium — customer complaints | High — delivery delays | 4 |
| 1 day | EUR 80,000 lost revenue + SLA credits | Medium — SLA breach | High — social media | High — missed delivery windows | 5 |
| 3 days | EUR 300,000 + customer churn risk | High — contract breach | Very high — press coverage likely | Very high — logistics collapse | 5 |
| 1 week | EUR 900,000 + major churn | Very high | Critical | Critical | 5 |

**MTPD:** 8 hours. **RTO:** 4 hours. **RPO:** 1 hour. **Priority:** Critical.

**Minimum Business Continuity Objective (MBCO):** Manual shipment booking via phone + spreadsheet intake at 30% capacity within 2 hours of declared disruption.

### P-02 — Dispatch and route planning

**Description:** Assigning shipments to drivers and optimising routes. Depends on P-01 for inputs.

**Dependencies:** AST-002, AST-007 (ERP), route planning system (part of logistics portal), dispatchers, drivers, vehicles.

**Impact over time:** Financial impact grows rapidly — at 1 week, EUR 1.2M lost plus penalty clauses. Regulatory impact: moderate (missed EU delivery obligations for regulated goods). Operational impact: critical after 12h.

**MTPD:** 12 hours. **RTO:** 6 hours. **RPO:** 1 hour. **Priority:** Critical.

**MBCO:** Manual dispatch via printed route sheets from the last known backup, supporting 50% of normal capacity within 4 hours.

### P-03 — Customer invoicing

**Description:** Monthly invoice generation plus ad-hoc invoicing for premium customers. Depends on shipment records (from P-01) and ERP (AST-007).

**Dependencies:** AST-007 (ERP), AST-001 (customer DB), finance staff, email for delivery of invoices.

**Impact over time:** Financial impact at 1 week is delayed — EUR 250,000 in postponed revenue but no permanent loss. Regulatory: low. Reputational: medium for premium customers. Operational: low.

**MTPD:** 5 days. **RTO:** 3 days. **RPO:** 24 hours. **Priority:** High.

**MBCO:** Manual invoice creation for top 20 customers within 1 day using exported data.

*(Processes P-04 to P-09 follow the same structure and are stored in the BIA workbook.)*

## 5. Resource requirements at disruption

To operate at MBCO level during a disruption, the following minimum resources are required:

| Resource | Normal | Minimum | Source |
|---|---|---|---|
| Dispatchers | 4 | 2 | Cross-trained staff from customer support |
| Customer service agents | 2 | 1 | Head of Sales covers second |
| IT on-call | 1 | 1 | On-call rota |
| Logistics portal (or manual fallback) | Portal | Phone + spreadsheet | Prepared fallback kit |
| ERP | Available | Read-only exports | Daily exports in secure share |
| Workstations | 6 | 3 | Hot desks + laptops |
| Connectivity | Fibre + mobile backup | Mobile backup | Pre-provisioned 4G router |
| Facilities | Hamburg HQ | Rotterdam branch | Branch supports HQ processes |

## 6. Single points of failure identified

The BIA revealed three single points of failure that are not fully mitigated:

1. **Vendor X Logistics (SUP-004):** Sole SaaS provider for the logistics portal. Mitigation in progress — second provider qualification (tracked as RTP-008).
2. **Dispatch expertise concentrated in 4 people:** Cross-training plan added to the HR programme for 2026-Q2.
3. **ERP on-prem server:** HA in place, but a DC-level disaster would require 8 hours to fail over to the DR site. Accepted given MTPD of invoicing.

## 7. Links to continuity plans

- P-01 and P-02 → Continuity Plan CP-01 (Logistics operations).
- P-03 → Continuity Plan CP-02 (Finance).
- P-05 and P-06 → Continuity Plan CP-03 (HR).
- DR for all IT assets → Disaster Recovery Plan DRP-01.

## 8. Review and next steps

- Review the BIA annually and after any major organisational, technological, or supplier change.
- Validate the assumptions through tabletop exercises (next: 2026-05-20).
- Confirm RTO/RPO against the disaster recovery register quarterly.

---

*Approved by Katharina Meier (CEO) on 2026-02-15.*
