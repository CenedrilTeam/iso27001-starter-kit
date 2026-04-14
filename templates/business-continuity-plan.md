# Business Continuity Plan — CP-01 Logistics Operations

> **Document control**  
> Owner: Business Continuity Lead  
> Approved by: CEO  
> Version: 1.3  
> Effective date: 2026-02-20  
> Next review: 2027-02-20  
> Classification: Confidential — BCM team

## 1. Purpose and scope

This continuity plan covers processes P-01 (Shipment booking and tracking) and P-02 (Dispatch and route planning), identified in the BIA as critical with an MTPD of 8 and 12 hours respectively.

The plan applies to disruptions that affect Hamburg HQ, the Rotterdam branch, or critical suppliers (primarily Vendor X Logistics, AWS, M365). It does not cover personnel emergencies, which are handled by the HR continuity plan.

## 2. Activation

### 2.1 Trigger conditions

Activation is triggered by any of the following:

- The logistics portal (AST-002) is unreachable for more than 30 minutes during business hours.
- Hamburg HQ is inaccessible for more than 1 hour during business hours.
- A confirmed major incident (severity High or above) affects a critical system with RTO ≤ 4 hours.
- Declaration by the Crisis Management Team (CMT).

### 2.2 Decision authority

The BCM Lead, the ISO, or the IT Operations Lead may declare activation. The CEO is informed immediately and has override authority.

### 2.3 Notification

On activation, the following notifications are issued within 15 minutes:

- CMT members via the crisis phone tree.
- All affected staff via SMS and email.
- Customers via the portal status page.
- Key suppliers that are relied on during recovery.

## 3. Roles and responsibilities

| Role | Name | Responsibility During Activation |
|---|---|---|
| CMT Chair | Katharina Meier (CEO) | Overall decision-making, external communications |
| Deputy | Thomas Weissenberg (CFO) | Financial decisions, deputising for CEO |
| BCM Lead | Markus Schulz | Coordinate recovery, maintain situation log |
| ISO | Anna Weber | Security implications, incident response interface |
| IT Ops Lead | Markus Schulz (deputised) | Technical recovery of IT systems |
| Ops Lead | Tobias Wagner | Business process continuity |
| Comms Lead | Sarah Lindner | Internal and external communications |
| DPO | Julia Hoffmann | GDPR impact assessment if applicable |

## 4. Recovery strategy

### 4.1 Scenario A — Logistics portal outage (Vendor X Logistics)

**Objective:** Maintain 30% shipment booking capacity within 2 hours, full capacity within 4 hours.

**Steps:**

1. **T+0 to T+15 min:** BCM Lead confirms outage with vendor. IT Ops Lead opens P1 ticket with vendor. CMT notified.
2. **T+15 to T+30 min:** Activate fallback procedure LOG-FB-01 (manual intake via phone + shared spreadsheet). Dispatch team switches to the printed route sheet from the last export.
3. **T+30 to T+60 min:** Customer service team announces fallback on portal status page and prepared email template. Top-20 customers are called individually by account managers.
4. **T+1h to T+2h:** Additional staff cross-deployed from customer support to dispatch to reach 30% capacity.
5. **T+2h to T+4h:** Continue manual operation. Monitor vendor updates every 30 minutes. Prepare for portal recovery.
6. **On recovery:** Reconcile manually captured bookings into the portal. Issue recovery confirmation to customers.

### 4.2 Scenario B — Hamburg HQ inaccessible

**Objective:** Relocate critical operations to Rotterdam within 4 hours.

**Steps:**

1. **T+0 to T+15 min:** CMT activates relocation. Rotterdam branch is notified.
2. **T+15 min to T+1h:** Core staff (dispatchers, IT on-call, BCM Lead) relocate to Rotterdam or work from home with pre-provisioned laptops.
3. **T+1h to T+4h:** Rotterdam office provides 6 hot desks + conference room for CMT. VPN + VoIP redirected to Rotterdam.
4. **T+4h onwards:** Monitor HQ status. Plan return.

### 4.3 Scenario C — M365 tenant outage

**Objective:** Maintain internal and external communication via alternative channels.

**Steps:**

1. **T+0 to T+15 min:** Confirm outage with Microsoft Service Health. Notify CMT.
2. **T+15 min:** Switch internal communication to Signal (pre-provisioned crisis group) and personal phone numbers.
3. **T+30 min:** Customer communications via portal status page and vendor-hosted backup email (`crisis@nordwind-logistics.net`).
4. **T+1h onwards:** Critical documents accessible via offline copy of the crisis binder and daily export of key M365 data.

### 4.4 Scenario D — Ransomware or major cyber incident

Managed jointly with the Incident Response Plan (PROC-001). BCM activation focuses on business continuity while incident response focuses on containment and eradication.

## 5. Resources available at activation

- **Crisis room:** Hamburg HQ, room Nordsee. Backup: Rotterdam, room Haven.
- **Crisis binder:** Printed copies at HQ, Rotterdam, at the BCM Lead's home.
- **Fallback kit:** 6 preconfigured laptops, 2 × 4G routers, 2 × satellite phones stored in the HR safe.
- **Crisis communication templates:** See Crisis Communication Template document.
- **Offline contact lists:** Employees, suppliers, customers (top 50), authorities.
- **Alternative email:** `crisis@nordwind-logistics.net` hosted at a separate provider.

## 6. Dependencies

| Dependency | Provider | Failover |
|---|---|---|
| Logistics portal | Vendor X Logistics | Manual fallback (LOG-FB-01) |
| Email and collaboration | Microsoft M365 | Signal + backup email |
| Cloud infrastructure | AWS eu-central-1 | Cross-region read replica |
| Connectivity | Primary fibre ISP | 4G mobile backup router |
| Power | Grid | UPS (30 min) + generator (24h) |
| Dispatch expertise | 4 dispatchers | Cross-trained customer service staff |

## 7. Recovery procedures

The plan references the following runbooks:

- RB-DB-001 — Customer database restore
- RB-SAAS-002 — Logistics portal failover and recovery
- RB-AD-001 — Domain controller failover
- RB-ERP-001 — ERP failover
- LOG-FB-01 — Manual logistics fallback procedure

## 8. Testing and review

- **Tabletop exercise:** Twice per year (last: 2025-11-10, next: 2026-05-20).
- **Partial simulation:** Annually (last: 2025-09-15 — portal failover).
- **Full walk-through:** Annually.
- **Plan review:** Annually or after any significant change in people, processes, technology, or suppliers.

## 9. Return to normal

Once the triggering incident is resolved, the BCM Lead assesses readiness for return:

- Systems operational and verified.
- Data integrity validated.
- Security posture restored (confirmed by the ISO).
- Staff briefed on return procedures.

The CEO formally declares return to normal operations. Lessons learned are captured in a post-incident review within 10 working days and fed into the CAPA register.

---

*Approved by Katharina Meier (CEO) on 2026-02-20.*
