# Business Impact Analyse (BIA)

> **Dokumentenkontrolle**  
> Eigentümer: BCM-Leitung  
> Genehmigt von: CEO  
> Version: 2.0  
> Gültig ab: 2026-02-15  
> Nächste Überprüfung: 2027-02-15  
> Klassifizierung: Vertraulich

## 1. Zweck und Scope

Die Business Impact Analyse identifiziert die kritischen Geschäftsprozesse der Nordwind Logistics GmbH, quantifiziert die Auswirkung von Unterbrechungen im Zeitverlauf und definiert die Wiederherstellungsziele (RTO und RPO), die Grundlage für Continuity- und Disaster-Recovery-Pläne sind.

**Scope:** Alle Geschäftsprozesse der Nordwind Logistics GmbH, inklusive Hauptsitz in Hamburg und Niederlassung in Rotterdam.

## 2. Methodik

Die BIA folgt den Vorgaben von ISO 22301 und ISO/IEC 27031. Sie wurde zwischen dem 2026-01-20 und dem 2026-02-10 in strukturierten Workshops mit den Prozess­verantwortlichen erhoben. Pro Prozess wurden bewertet:

- **Finanzielle Auswirkung** über vier Zeitfenster: 4 Stunden, 1 Tag, 3 Tage, 1 Woche.
- **Regulatorische Auswirkung** (Bußgelder, Meldepflichten, Vertragsverletzungen).
- **Reputations-Auswirkung** (Kundenvertrauen, mediale Aufmerksamkeit).
- **Operative Auswirkung** (Unfähigkeit, Kunden zu bedienen, Sicherheitsrisiken).

Jede Auswirkung wurde auf einer Skala von 1–5 bewertet. Die Werte bei 1 Woche dienten zur Ableitung der **Maximum Tolerable Period of Disruption (MTPD)** und zur Festlegung von **Recovery Time Objective (RTO)** und **Recovery Point Objective (RPO)** unterhalb der MTPD mit Sicherheits­puffer.

## 3. Kritische Prozesse

| ID | Prozess | Verantwortlich | MTPD | RTO | RPO | Priorität |
|---|---|---|---|---|---|---|
| P-01 | Sendungserfassung und -verfolgung (Kundenportal) | Operationsleitung | 8 h | 4 h | 1 h | Kritisch |
| P-02 | Disposition und Tourenplanung | Operationsleitung | 12 h | 6 h | 1 h | Kritisch |
| P-03 | Kundenrechnungsstellung | CFO | 5 Tage | 3 Tage | 24 h | Hoch |
| P-04 | Kundenservice | Vertriebsleitung | 1 Tag | 8 h | 8 h | Hoch |
| P-05 | Lohnabrechnung | HR-Leitung | 15 Tage | 7 Tage | 24 h | Mittel |
| P-06 | HR-Administration (ohne Lohnabrechnung) | HR-Leitung | 10 Tage | 5 Tage | 24 h | Mittel |
| P-07 | Einkauf und Lieferantenmanagement | Einkauf | 10 Tage | 5 Tage | 24 h | Mittel |
| P-08 | Recht und Vertragsmanagement | Legal | 30 Tage | 10 Tage | 7 Tage | Niedrig |
| P-09 | Marketing | Marketingleitung | 30 Tage | 15 Tage | 7 Tage | Niedrig |

## 4. Detailbewertung (Auszug — Top-3-Prozesse)

### P-01 — Sendungserfassung und -verfolgung

**Beschreibung:** Kunden buchen Sendungen über das Online-Portal (AST-002) und verfolgen sie in Echtzeit. Der Prozess speist direkt Disposition und Kundenrechnungsstellung.

**Abhängigkeiten:**

- IT: AST-002 (Logistikportal SaaS), AST-001 (Kundendatenbank), AST-003 (M365), AST-010 (Firewall), Internetanbindung an Hamburg und Rotterdam.
- Personen: 4 Disponenten, 2 Kundenservice-Mitarbeitende, 1 IT-Rufbereitschaft.
- Lieferanten: Vendor X Logistics (SUP-004), AWS (SUP-001).
- Einrichtungen: Hamburg HQ (AST-016) — mit Rotterdam als Ausweichstandort.

**Auswirkung im Zeitverlauf:**

| Zeit | Finanziell | Regulatorisch | Reputation | Operativ | Gesamt (1–5) |
|---|---|---|---|---|---|
| 4 h | 15.000 EUR Umsatzverlust | Gering — SLA überwacht | Mittel — Kundenbeschwerden | Hoch — Lieferverzögerungen | 4 |
| 1 Tag | 80.000 EUR + SLA-Gutschriften | Mittel — SLA-Verletzung | Hoch — Social Media | Hoch — verpasste Lieferfenster | 5 |
| 3 Tage | 300.000 EUR + Kundenabwanderungsrisiko | Hoch — Vertragsverletzung | Sehr hoch — Presseberichterstattung wahrscheinlich | Sehr hoch — Logistik-Zusammenbruch | 5 |
| 1 Woche | 900.000 EUR + massive Abwanderung | Sehr hoch | Kritisch | Kritisch | 5 |

**MTPD:** 8 Stunden. **RTO:** 4 Stunden. **RPO:** 1 Stunde. **Priorität:** Kritisch.

**Minimum Business Continuity Objective (MBCO):** Manuelle Sendungserfassung per Telefon + Spreadsheet-Aufnahme bei 30 % Kapazität innerhalb von 2 Stunden nach erklärter Unterbrechung.

### P-02 — Disposition und Tourenplanung

**Beschreibung:** Zuweisung von Sendungen an Fahrer und Routenoptimierung. Hängt von P-01 als Input ab.

**Abhängigkeiten:** AST-002, AST-007 (ERP), Routenplanungssystem (Teil des Logistikportals), Disponenten, Fahrer, Fahrzeuge.

**Auswirkung im Zeitverlauf:** Finanzielle Auswirkung wächst rasch — bei 1 Woche 1,2 Mio. EUR Verlust plus Vertragsstrafen. Regulatorisch: mittel (verpasste EU-Lieferpflichten für regulierte Güter). Operativ: kritisch nach 12 h.

**MTPD:** 12 Stunden. **RTO:** 6 Stunden. **RPO:** 1 Stunde. **Priorität:** Kritisch.

**MBCO:** Manuelle Disposition über ausgedruckte Tourenblätter aus dem letzten Backup, 50 % Normalkapazität innerhalb von 4 Stunden.

### P-03 — Kundenrechnungsstellung

**Beschreibung:** Monatliche Rechnungserstellung und Ad-hoc-Rechnungen für Premium-Kunden. Hängt von Sendungsdaten (aus P-01) und ERP (AST-007) ab.

**Abhängigkeiten:** AST-007 (ERP), AST-001 (Kunden-DB), Finanzmitarbeitende, E-Mail für Rechnungsversand.

**Auswirkung im Zeitverlauf:** Finanzielle Auswirkung bei 1 Woche verzögert — 250.000 EUR verzögerter Umsatz, aber kein dauerhafter Verlust. Regulatorisch: niedrig. Reputation: mittel für Premium-Kunden. Operativ: niedrig.

**MTPD:** 5 Tage. **RTO:** 3 Tage. **RPO:** 24 Stunden. **Priorität:** Hoch.

**MBCO:** Manuelle Rechnungserstellung für die Top-20-Kunden innerhalb 1 Tag auf Basis exportierter Daten.

*(Prozesse P-04 bis P-09 folgen derselben Struktur und sind im BIA-Workbook abgelegt.)*

## 5. Ressourcenbedarf bei Unterbrechung

Um auf MBCO-Niveau während einer Unterbrechung zu arbeiten, werden mindestens folgende Ressourcen benötigt:

| Ressource | Normal | Minimum | Quelle |
|---|---|---|---|
| Disponenten | 4 | 2 | Quergeschultes Personal aus Kundenservice |
| Kundenservice-Mitarbeitende | 2 | 1 | Vertriebsleitung deckt zweite Position |
| IT-Rufbereitschaft | 1 | 1 | Rufbereitschaftsplan |
| Logistikportal (oder manuelles Fallback) | Portal | Telefon + Spreadsheet | Vorbereitetes Fallback-Kit |
| ERP | Verfügbar | Lese-Exports | Tägliche Exporte auf sicherem Share |
| Arbeitsplätze | 6 | 3 | Hot Desks + Laptops |
| Konnektivität | Glasfaser + Mobilfunk-Backup | Mobilfunk-Backup | Vorkonfigurierter 4G-Router |
| Einrichtungen | Hamburg HQ | Niederlassung Rotterdam | Niederlassung übernimmt HQ-Prozesse |

## 6. Identifizierte Single Points of Failure

Die BIA deckte drei Single Points of Failure auf, die nicht vollständig gemindert sind:

1. **Vendor X Logistics (SUP-004):** Einziger SaaS-Anbieter für das Logistikportal. Minderung in Bearbeitung — Qualifizierung eines zweiten Anbieters (als RTP-008 verfolgt).
2. **Dispositionswissen konzentriert auf 4 Personen:** Querschulungsplan für 2026-Q2 ins HR-Programm aufgenommen.
3. **ERP auf On-Prem-Server:** HA vorhanden, aber ein RZ-Totalausfall erfordert 8 Stunden Failover zum DR-Standort. Akzeptiert angesichts der MTPD für Rechnungsstellung.

## 7. Verknüpfungen zu Continuity-Plänen

- P-01 und P-02 → Continuity Plan CP-01 (Logistikbetrieb).
- P-03 → Continuity Plan CP-02 (Finanzen).
- P-05 und P-06 → Continuity Plan CP-03 (HR).
- DR für alle IT-Assets → Disaster Recovery Plan DRP-01.

## 8. Überprüfung und nächste Schritte

- Die BIA wird jährlich und nach jeder größeren organisatorischen, technischen oder lieferantenseitigen Änderung überprüft.
- Validierung der Annahmen durch Tabletop-Übungen (nächste: 2026-05-20).
- Quartalsweiser Abgleich der RTO/RPO mit dem Disaster-Recovery-Register.

---

*Genehmigt von Katharina Meier (CEO) am 2026-02-15.*
