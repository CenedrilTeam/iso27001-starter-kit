# Geschäftskontinuitätsplan — CP-01 Logistikbetrieb

> **Dokumentenkontrolle**  
> Eigentümer: BCM-Leitung  
> Genehmigt von: CEO  
> Version: 1.3  
> Gültig ab: 2026-02-20  
> Nächste Überprüfung: 2027-02-20  
> Klassifizierung: Vertraulich — BCM-Team

## 1. Zweck und Scope

Dieser Continuity-Plan deckt die Prozesse P-01 (Sendungserfassung und -verfolgung) und P-02 (Disposition und Tourenplanung) ab, die in der BIA als kritisch mit einer MTPD von 8 bzw. 12 Stunden eingestuft sind.

Der Plan gilt für Unterbrechungen, die das Hamburger HQ, die Rotterdamer Niederlassung oder kritische Lieferanten (vorwiegend Vendor X Logistics, AWS, M365) betreffen. Personal-Notfälle werden über den HR-Continuity-Plan abgedeckt.

## 2. Aktivierung

### 2.1 Auslöserbedingungen

Die Aktivierung wird durch eine der folgenden Bedingungen ausgelöst:

- Das Logistikportal (AST-002) ist während der Geschäftszeiten länger als 30 Minuten nicht erreichbar.
- Das Hamburger HQ ist während der Geschäftszeiten länger als 1 Stunde nicht zugänglich.
- Ein bestätigter Großvorfall (Schweregrad Hoch oder höher) betrifft ein kritisches System mit RTO ≤ 4 Stunden.
- Erklärung durch das Krisenmanagement-Team (CMT).

### 2.2 Entscheidungsbefugnis

Die BCM-Leitung, die ISB oder die IT-Betriebsleitung dürfen die Aktivierung erklären. Die CEO wird unverzüglich informiert und hat Veto-Recht.

### 2.3 Benachrichtigung

Bei Aktivierung werden innerhalb von 15 Minuten folgende Benachrichtigungen ausgelöst:

- CMT-Mitglieder über die Krisen-Telefonkette.
- Alle betroffenen Mitarbeitenden per SMS und E-Mail.
- Kunden über die Statusseite des Portals.
- Schlüssellieferanten, auf die bei der Wiederherstellung gebaut wird.

## 3. Rollen und Verantwortlichkeiten

| Rolle | Name | Verantwortung während der Aktivierung |
|---|---|---|
| CMT-Vorsitz | Katharina Meier (CEO) | Gesamtentscheidungen, externe Kommunikation |
| Stellvertretung | Thomas Weissenberg (CFO) | Finanzentscheidungen, Vertretung der CEO |
| BCM-Leitung | Markus Schulz | Koordination der Wiederherstellung, Lagebuch |
| ISB | Anna Weber | Sicherheitsauswirkungen, Incident-Response-Schnittstelle |
| IT-Betriebsleitung | Markus Schulz (in Doppelfunktion) | Technische Wiederherstellung der IT-Systeme |
| Operationsleitung | Tobias Wagner | Geschäftsprozess-Kontinuität |
| Kommunikationsleitung | Sarah Lindner | Interne und externe Kommunikation |
| DSB | Julia Hoffmann | DSGVO-Auswirkungen sofern relevant |

## 4. Wiederherstellungsstrategie

### 4.1 Szenario A — Ausfall des Logistikportals (Vendor X Logistics)

**Ziel:** 30 % Sendungserfassungs-Kapazität innerhalb 2 Stunden, volle Kapazität innerhalb 4 Stunden halten.

**Schritte:**

1. **T+0 bis T+15 min:** BCM-Leitung bestätigt Ausfall mit Anbieter. IT-Betriebsleitung eröffnet P1-Ticket beim Anbieter. CMT informiert.
2. **T+15 bis T+30 min:** Fallback-Verfahren LOG-FB-01 aktivieren (manuelle Erfassung per Telefon + gemeinsames Spreadsheet). Dispositionsteam wechselt auf ausgedruckte Tourenblätter aus dem letzten Export.
3. **T+30 bis T+60 min:** Kundenservice kündigt Fallback auf der Portal-Statusseite und mit vorbereiteter E-Mail-Vorlage an. Top-20-Kunden werden einzeln durch Account Manager angerufen.
4. **T+1 h bis T+2 h:** Zusätzliches Personal aus dem Kundenservice in die Disposition verlagert, um 30 % Kapazität zu erreichen.
5. **T+2 h bis T+4 h:** Manueller Betrieb fortführen. Anbieterstatus alle 30 Minuten überwachen. Wiederanlauf vorbereiten.
6. **Bei Wiederherstellung:** Manuell erfasste Buchungen in das Portal zurückspielen. Wiederherstellungs­bestätigung an Kunden senden.

### 4.2 Szenario B — Hamburger HQ nicht zugänglich

**Ziel:** Kritische Operationen innerhalb 4 Stunden nach Rotterdam verlagern.

**Schritte:**

1. **T+0 bis T+15 min:** CMT aktiviert Verlagerung. Niederlassung Rotterdam wird informiert.
2. **T+15 min bis T+1 h:** Kernpersonal (Disponenten, IT-Rufbereitschaft, BCM-Leitung) verlagert sich nach Rotterdam oder arbeitet aus dem Homeoffice mit vorbereiteten Laptops.
3. **T+1 h bis T+4 h:** Rotterdam stellt 6 Hot Desks + Besprechungsraum für das CMT zur Verfügung. VPN + VoIP auf Rotterdam umgeleitet.
4. **Ab T+4 h:** HQ-Status weiter beobachten. Rückkehr planen.

### 4.3 Szenario C — M365-Tenant-Ausfall

**Ziel:** Interne und externe Kommunikation über alternative Kanäle aufrechterhalten.

**Schritte:**

1. **T+0 bis T+15 min:** Ausfall mit Microsoft Service Health bestätigen. CMT informieren.
2. **T+15 min:** Interne Kommunikation auf Signal (vorbereitete Krisengruppe) und private Telefonnummern umstellen.
3. **T+30 min:** Kundenkommunikation über Portal-Statusseite und anbieterseitig gehostete Ausweich-E-Mail (`crisis@nordwind-logistics.net`).
4. **Ab T+1 h:** Kritische Dokumente über Offline-Kopie des Krisenordners und tägliche Exporte wichtiger M365-Daten zugänglich.

### 4.4 Szenario D — Ransomware oder größerer Cybervorfall

Wird gemeinsam mit dem Incident Response Plan (PROC-001) gesteuert. BCM-Aktivierung konzentriert sich auf Geschäftskontinuität, Incident Response auf Eindämmung und Bereinigung.

## 5. Verfügbare Ressourcen bei Aktivierung

- **Krisenraum:** Hamburg HQ, Raum Nordsee. Ausweich: Rotterdam, Raum Haven.
- **Krisenordner:** Gedruckte Exemplare in HQ, Rotterdam und bei der BCM-Leitung zu Hause.
- **Fallback-Kit:** 6 vorkonfigurierte Laptops, 2 × 4G-Router, 2 × Satellitentelefone, im HR-Safe gelagert.
- **Krisenkommunikations-Templates:** siehe Dokument „Krisenkommunikations-Template".
- **Offline-Kontaktlisten:** Mitarbeitende, Lieferanten, Kunden (Top 50), Behörden.
- **Alternative E-Mail:** `crisis@nordwind-logistics.net` bei separatem Anbieter gehostet.

## 6. Abhängigkeiten

| Abhängigkeit | Anbieter | Failover |
|---|---|---|
| Logistikportal | Vendor X Logistics | Manuelles Fallback (LOG-FB-01) |
| E-Mail und Zusammenarbeit | Microsoft M365 | Signal + Ausweich-E-Mail |
| Cloud-Infrastruktur | AWS eu-central-1 | Cross-Region Read Replica |
| Konnektivität | Primärer Glasfaser-ISP | 4G-Mobilfunk-Backup-Router |
| Strom | Netz | USV (30 min) + Generator (24 h) |
| Dispositionswissen | 4 Disponenten | Quergeschultes Kundenservice-Personal |

## 7. Wiederherstellungsverfahren

Der Plan verweist auf folgende Runbooks:

- RB-DB-001 — Wiederherstellung Kundendatenbank
- RB-SAAS-002 — Logistikportal-Failover und -Wiederherstellung
- RB-AD-001 — Domain-Controller-Failover
- RB-ERP-001 — ERP-Failover
- LOG-FB-01 — Manuelles Logistik-Fallback-Verfahren

## 8. Tests und Überprüfung

- **Tabletop-Übung:** Zweimal jährlich (zuletzt: 2025-11-10, nächste: 2026-05-20).
- **Teilsimulation:** Jährlich (zuletzt: 2025-09-15 — Portal-Failover).
- **Vollständiger Durchlauf:** Jährlich.
- **Plan-Review:** Jährlich oder nach jeder wesentlichen Änderung bei Personen, Prozessen, Technik oder Lieferanten.

## 9. Rückkehr zum Normalbetrieb

Sobald der auslösende Vorfall behoben ist, bewertet die BCM-Leitung die Bereitschaft zur Rückkehr:

- Systeme sind betriebsbereit und verifiziert.
- Datenintegrität ist validiert.
- Sicherheitsniveau ist wiederhergestellt (durch die ISB bestätigt).
- Mitarbeitende sind über das Rückkehr­vorgehen informiert.

Die CEO erklärt formal die Rückkehr zum Normalbetrieb. Lessons Learned werden innerhalb von 10 Arbeitstagen in einem Post-Incident-Review erfasst und in das CAPA-Register überführt.

---

*Genehmigt von Katharina Meier (CEO) am 2026-02-20.*
