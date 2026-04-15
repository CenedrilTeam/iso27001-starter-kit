# Incident Response Runbooks

> **Document control**  
> Owner: Information Security Officer  
> Approved by: CEO  
> Version: 1.0  
> Effective date: 2026-03-01  
> Classification: Confidential — restricted to SecOps, IT Operations, DPO, CMT

## How to use this document

This document contains a set of runbooks for the most common information security incidents at Nordwind Logistics GmbH. Each runbook follows the same structure based on NIST SP 800-61 Rev. 2: **Preparation → Detection & Analysis → Containment → Eradication → Recovery → Lessons Learned**.

Runbooks are not a substitute for judgement. They are a starting point. The Incident Response Plan (PROC-001) defines the overall process, roles and severity matrix.

**Severity scale:**

- **Low:** isolated, contained, no business impact, no personal data involved.
- **Medium:** limited business impact, no confirmed data breach, manageable with internal resources.
- **High:** material business impact OR confirmed personal data breach OR more than one critical system affected.
- **Critical:** organisation-wide impact OR ransomware OR major regulatory exposure.

**Common roles referenced:**

- **On-Call Engineer** — first responder, available 24/7
- **ISO** — Information Security Officer, owns the incident
- **DPO** — Data Protection Officer, owns regulatory aspects of personal data breaches
- **IT Ops Lead** — owns technical recovery
- **CMT** — Crisis Management Team, activated for High and Critical
- **Communications Lead** — owns external messaging

---

## Runbook 1 — Ransomware

**Triggers:** Files renamed with unknown extension, ransom note found, EDR ransomware detection, mass file modification alert, multiple users reporting inability to open files.

**Default severity:** Critical

### T+0 to T+15 minutes — Detection and immediate containment

1. On-Call Engineer confirms the alert is not a false positive: check EDR console, look for ransom note file, attempt to open one affected file.
2. **Disconnect the affected host immediately.** Pull the network cable or disable the network adapter via EDR. Do not power off (volatile evidence may be lost).
3. Notify the ISO via the crisis hotline. The ISO declares the incident at severity Critical.
4. ISO activates the CMT. Open a war room channel.
5. Identify all hosts with the same indicators using EDR threat hunting. Isolate every match.
6. Disable the compromised user account(s) and rotate their credentials.

### T+15 minutes to T+1 hour — Scope and containment

1. Identify lateral movement paths: check authentication logs for the past 7 days for the compromised account on other systems.
2. Identify whether the backup infrastructure has been touched. If yes, treat backups as untrusted until verified.
3. Decide whether to take the affected file shares offline. Default: yes.
4. Notify the on-call legal counsel and DPO. The DPO begins a parallel personal data impact assessment.
5. Snapshot all affected hosts for forensic analysis (full disk image where feasible).
6. Notify CEO. CEO authorises external incident response support if needed.

### T+1 to T+24 hours — Eradication and recovery decision

1. **Do not pay the ransom.** This is a standing decision of Nordwind Logistics and is documented in PROC-001.
2. Identify the ransomware family if possible (check ID Ransomware, EDR vendor advisories). Apply the corresponding eradication procedure.
3. Decision: rebuild affected systems from clean OS images, then restore data from offline backup.
4. Verify the offline backup is unaffected before any restore. Restore to an isolated environment first and validate file integrity.
5. **Regulatory notifications:**
   - NIS2 early warning to BSI within 24 hours of incident awareness (template in crisis communication document).
   - GDPR Art. 33 notification to BfDI within 72 hours if personal data is affected.
6. Customer notification: prepared by Communications Lead, approved by CEO, dispatched per the crisis communication template.

### T+24 hours and beyond — Recovery

1. Rebuild affected systems from clean images using hardened baselines.
2. Restore data from verified offline backup.
3. Reset all credentials in the compromised domain (or full AD krbtgt rotation if domain controllers were affected).
4. Increase monitoring sensitivity for 30 days post-incident.
5. Validate that backups continue to work.

### Lessons learned

Within 10 working days of incident closure, the ISO holds a post-incident review. Output: post-incident report, CAPA entries, updated runbook (if needed), feedback to threat register.

---

## Runbook 2 — Phishing and credential compromise

**Triggers:** User reports a suspicious email and indicates they entered credentials, mailbox flooded with bounces, MFA prompt fatigue, EDR alert on a credential-stealing browser extension, SIEM alert on impossible travel.

**Default severity:** Medium (High if admin account or finance team)

### T+0 to T+15 minutes — Containment

1. On-Call Engineer immediately disables the affected user account (M365 + AD).
2. Force sign-out on all sessions for the affected user.
3. Revoke active OAuth tokens and refresh tokens.
4. Rotate the user's credentials. Issue a temporary password.
5. Open an incident ticket and notify the ISO.

### T+15 minutes to T+1 hour — Investigation

1. Pull authentication logs for the affected account for the past 14 days. Look for:
   - Logins from unexpected locations or IPs.
   - Mail forwarding rules created.
   - Mailbox delegation changes.
   - OAuth consents granted.
   - Sent items showing internal phishing or fraud attempts.
2. If mail forwarding rules were created — remove them and capture them as evidence.
3. Check whether the user has access to financial or HR systems and whether any sensitive transactions occurred in the past 24 hours.
4. Search the SIEM for the same phishing URL or indicators across all users. Block the URL at the mail and web gateway.

### T+1 hour to T+24 hours — Containment (organisation-wide)

1. Block the phishing domain and all observed indicators at the mail filter, web filter, DNS, and EDR.
2. Run a targeted search across all mailboxes for the original phishing email. Quarantine or delete.
3. Notify all employees about the phishing wave with concrete details (sender, subject, what to do if they clicked).
4. Re-enable the user account only after MFA re-enrollment and a security briefing.

### Recovery and follow-up

1. Add the indicators to the threat register.
2. Run a targeted phishing simulation against the affected team within 30 days.
3. If the phishing kit bypassed existing controls, raise a CAPA to harden mail filtering or accelerate FIDO2 rollout.
4. If a financial or data fraud occurred (e.g. CEO fraud), escalate to High and follow Runbook 3 in addition.

---

## Runbook 3 — Personal data breach

**Triggers:** Email sent to wrong recipient with personal data, lost device with personal data, unauthorised access to a database with personal data, misconfigured cloud storage with personal data exposed, public exposure of customer information.

**Default severity:** High (always — re-evaluate after assessment)

### T+0 to T+15 minutes — Initial action

1. Whoever discovers the breach notifies the DPO immediately.
2. The DPO declares the incident and opens a breach record. The 72-hour clock for GDPR Art. 33 starts at the moment of awareness.
3. Take immediate action to stop further exposure: recall the email, take the system offline, revoke access, change the configuration.

### T+15 minutes to T+1 hour — Initial assessment

1. The DPO documents:
   - Nature of the breach (confidentiality, integrity, availability).
   - Categories of data subjects affected.
   - Categories of personal data affected (any special categories under GDPR Art. 9?).
   - Approximate number of affected individuals and records.
   - Likely consequences for data subjects.
   - Measures taken or proposed.
2. The DPO notifies the ISO, CEO, and Communications Lead.
3. If the breach is likely to result in a high risk to data subjects, the DPO begins drafting an Art. 34 notification.

### T+1 hour to T+24 hours — Investigation

1. Determine root cause: human error, technical fault, malicious act, supplier failure?
2. Determine whether the data has actually been accessed by an unauthorised party (vs. merely exposed).
3. Confirm whether containment is complete. If not, escalate.
4. Consult external legal counsel if uncertain about notification obligations.

### Within 72 hours — Regulatory notification

1. Submit notification to the competent supervisory authority (BfDI) via the online portal. Include all available facts. If facts are incomplete, submit what is known and supplement later.
2. Document the rationale in the breach record.
3. If the breach involves cross-border processing, identify the lead supervisory authority and route the notification accordingly.

### When required — Notification to data subjects (Art. 34)

1. Draft notification using the crisis communication template.
2. DPO and CEO approve the wording.
3. Dispatch via the most appropriate channel (email, letter, or public notice if individual contact is not feasible).

### Recovery and follow-up

1. Implement corrective measures to prevent recurrence (CAPA).
2. Update the breach register.
3. Brief the next management review.
4. If the breach was caused by a supplier, trigger a supplier security review.

---

## Runbook 4 — Distributed Denial of Service (DDoS)

**Triggers:** Customer-facing service unreachable, monitoring alerts on response time, abnormal traffic spike, web application firewall flagging volumetric attack.

**Default severity:** Medium (High if peak business hours or extended outage)

### T+0 to T+15 minutes — Confirm and characterise

1. On-Call Engineer confirms the issue is a DDoS, not a backend failure: check WAF dashboard, traffic graphs, source IP distribution.
2. Identify attack type: volumetric (network), protocol (TCP SYN, UDP), or application-layer (HTTP flood).
3. Notify the ISO and IT Ops Lead. ISO declares the incident.

### T+15 minutes to T+1 hour — Mitigation

1. **Volumetric/network:** activate upstream DDoS protection at the ISP or CDN provider. Enable rate limiting and geo-blocking if the attack is geographically concentrated.
2. **Protocol:** increase resource limits on edge devices, enable SYN cookies, contact upstream provider.
3. **Application-layer:** enable WAF challenge mode, increase rate limits per IP, block known bot signatures, scale out application instances if cloud-native.
4. Coordinate with vendors. For SaaS providers (e.g. logistics portal), open a P1 ticket immediately.
5. Communicate with customers via the status page (crisis communication template).

### T+1 hour to T+24 hours — Sustained mitigation

1. Continuously monitor and adjust mitigation rules.
2. Capture traffic samples for post-incident analysis (already filtered to avoid log bloat).
3. If extortion is involved (RDoS), do not pay. Notify ISO and CEO. Treat as a separate incident.

### Recovery and follow-up

1. Wind down mitigation gradually as attack subsides.
2. Post-incident review: was the WAF effective, did the CDN absorb the attack, were customer communications timely?
3. Update the threat register with attack signatures.
4. Review contractual SLAs with the upstream provider.

---

## Runbook 5 — Lost or stolen device

**Triggers:** Employee reports a lost or stolen company laptop, phone, or removable media. Device may contain confidential data and provide network access.

**Default severity:** Medium (High if device contained personal data of customers or unencrypted special categories)

### T+0 to T+15 minutes — Containment

1. On-Call Engineer or IT Helpdesk confirms the report (when, where, what device).
2. Trigger remote wipe via MDM (Intune for Windows/iOS, Jamf for macOS).
3. Disable the user's account temporarily and force sign-out from all sessions.
4. Revoke the device's certificate from Active Directory and the IdP.
5. Notify the ISO.

### T+15 minutes to T+1 hour — Assessment

1. Determine what data was on the device:
   - Was full disk encryption enabled and active? (BitLocker / FileVault status from MDM.)
   - Did the user have local copies of customer data, personal data, or contracts?
   - What systems was the device authenticated to?
2. If full disk encryption was confirmed active and the device was powered off when lost, the risk is significantly reduced.
3. If the device contained personal data and encryption status is uncertain, treat as a potential personal data breach and engage the DPO (Runbook 3).
4. Capture the user's recollection in writing.

### T+1 hour to T+24 hours — Investigation and police report

1. The user files a police report and provides the case number.
2. Insurance is notified if applicable.
3. The ISO documents the incident and links it to the device record in the asset register.
4. If the device was stolen in a targeted manner (suspicious circumstances), escalate to High and consider whether other employees of the same team are at risk.

### Recovery and follow-up

1. Issue replacement device after the user has been re-trained on device security.
2. Review whether the data on the device was necessary or excessive — minimise where appropriate.
3. Review whether device-tracking and remote-wipe coverage is at 100% across the fleet.
4. If the loss reveals a process gap, raise a CAPA.

---

## After every incident — Closure and improvement

Regardless of which runbook was used, every closed incident triggers:

1. **Post-incident report** within 10 working days, written by the IR lead, reviewed by the ISO.
2. **CAPA entries** for each root cause that requires corrective action.
3. **Threat register update** if new indicators or TTPs were observed.
4. **Runbook update** if the incident revealed gaps in this document.
5. **Management review input** at the next quarterly review.

---

*These runbooks are living documents. Review at least annually and after every incident. Last reviewed: 2026-03-01.*
