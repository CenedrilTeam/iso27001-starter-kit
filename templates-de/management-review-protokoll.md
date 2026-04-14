# Management-Review-Protokoll — 2026-Q1

> **Dokumentenkontrolle**  
> Eigentümer: Informationssicherheitsbeauftragte  
> Genehmigt von: CEO  
> Version: 1.0  
> Gültig ab: 2026-03-30  
> Klassifizierung: Intern

## Sitzungsdetails

- **Organisation:** Nordwind Logistics GmbH
- **Geprüfter Scope:** ISMS gemäß Statement of Applicability v3.0
- **Datum:** 2026-03-30, 09:00–12:30
- **Ort:** HQ Hamburg, Raum Nordsee + Teams
- **Vorsitz:** Katharina Meier (CEO)
- **Protokoll:** Anna Weber (ISB)

## Teilnehmende

| Name | Rolle | Anwesend |
|---|---|---|
| Katharina Meier | CEO | Ja |
| Thomas Weissenberg | CFO | Ja |
| Anna Weber | Informationssicherheitsbeauftragte | Ja |
| Markus Schulz | IT-Betriebsleitung | Ja |
| Julia Hoffmann | Datenschutzbeauftragte | Ja |
| Thomas Krüger | HR-Leitung | Ja |
| Elena Fischer | Finanzleitung | Ja |
| Sebastian Brand | Head of Engineering | Ja |
| Lisa Hartmann | Vertriebsleitung | Entschuldigt — Input schriftlich eingereicht |

## Tagesordnung (ISO/IEC 27001:2022 Abschnitt 9.3.2)

1. Status der Maßnahmen aus dem letzten Management-Review
2. Änderungen externer und interner Rahmenbedingungen
3. Rückmeldungen zur ISMS-Leistung (Nichtkonformitäten, Überwachung, Auditergebnisse, Kontrollwirksamkeit, Zielerreichung)
4. Rückmeldungen interessierter Parteien
5. Ergebnisse der Risikobeurteilung und Status des Risikobehandlungsplans
6. Möglichkeiten zur kontinuierlichen Verbesserung
7. Entscheidungen und Maßnahmen

---

## 1. Status der vorherigen Maßnahmen

Aus dem Management-Review 2025-Q4 (2025-12-15) wurden vier Maßnahmen verfolgt. Drei sind abgeschlossen, eine in Bearbeitung.

| Maßnahme | Verantwortlich | Fällig | Status |
|---|---|---|---|
| Schwachstellen-SLA nach Schweregrad formalisieren | IT-Betriebsleitung | 2026-02-28 | Abgeschlossen — in IT-Betriebsrichtlinie v1.5 veröffentlicht |
| FIDO2 für Admin-Konten ausrollen | ISB | 2026-06-30 | In Bearbeitung — Phase 1 abgeschlossen (CHG-2026-002) |
| Leaver-Checkliste auf 2-h-Entzug aktualisieren | HR-Leitung | 2026-03-31 | Abgeschlossen — neue Checkliste seit 2026-03-01 im Einsatz |
| M365-Backup via Veeam for M365 ausrollen | IT-Betriebsleitung | 2026-02-28 | Abgeschlossen — operativ seit 2026-02-10 |

## 2. Änderungen externer und interner Rahmenbedingungen

**Extern:**

- NIS2-Umsetzungsgesetz seit 2026-01-01 in Kraft. Nordwind Logistics ist als „wichtige Einrichtung" im Verkehrssektor eingestuft. Registrierung beim BSI am 2026-01-18 abgeschlossen.
- Das Kundensegment „Grenzüberschreitender E-Commerce" ist in den letzten zwei Quartalen um 22 % gewachsen, wodurch das Volumen personenbezogener Daten zunimmt.
- Bedrohungslage: BSI-Lagebericht 2025 bestätigt Ransomware weiterhin als operatives Top-Risiko für mittelständische Logistik.

**Intern:**

- Neues Büro in Rotterdam seit 2026-02-15 (9 Mitarbeitende). Ab dem ersten Tag im ISMS-Scope.
- Reorganisation in der Finanzabteilung: neue Finanzleitung seit 2026-02-01.
- M365-Tenant-Konsolidierungsprojekt gestartet; ändert im Q3 Teile der Zugriffskontroll-Architektur.

## 3. ISMS-Leistung

### 3.1 Nichtkonformitäten und Korrekturmaßnahmen

Fünf CAPAs im Quartal offen, zwei abgeschlossen, drei in Bearbeitung. Keine überfälligen schwerwiegenden Nichtkonformitäten. Referenz: CAPA-Register.

### 3.2 Überwachungs- und Messergebnisse (KPIs)

| KPI | Ziel | Ist Q1 | Trend |
|---|---|---|---|
| Phishing-Simulation Klickrate | <5 % | 4,2 % | ↓ von 5,8 % |
| MFA-Abdeckung (Benutzerkonten) | 100 % | 100 % | stabil |
| MFA-Abdeckung (Admin-Konten, phishing-resistent) | 100 % | 48 % | ↑ (FIDO2-Rollout läuft) |
| Kritische Patches innerhalb SLA (14 Tage) | 100 % | 92 % | ↓ von 96 % — siehe CAPA-2026-004 |
| Erfolgsrate Backup-Restore-Tests | 100 % | 100 % | stabil |
| Mean Time to Detect (MTTD) | <2 h | 1 h 35 min | ↑ (Verbesserung) |
| Mean Time to Respond (MTTR, hoher Schweregrad) | <24 h | 17,3 h | ↑ (Verbesserung) |
| Awareness-Schulung Abschlussquote | >95 % | 96 % | stabil |

### 3.3 Auditergebnisse

- **Internes Audit 2026-Q1** abgeschlossen am 2026-02-10 (Scope: Zugriffskontrolle + HR-Sicherheit). Drei Feststellungen, alle im CAPA-Register.
- **Externes Überwachungsaudit** geplant für 2026-05-18 (KPMG).

### 3.4 Wirksamkeit der Kontrollen

- Technische Kontrollen: insgesamt wirksam. DLP teilweise umgesetzt (Endpoint-Teil offen, als RTP-006 verfolgt).
- Organisatorische Kontrollen: wirksam. Policy-Konformitätscheck im Februar zeigte 97 % Bestätigungsquote.
- Physische Kontrollen: ein Vorfall (siehe 3.6) — Kontrollen funktionierten wie vorgesehen.

### 3.5 Erreichung der Sicherheitsziele (aus Plan 2026)

| Ziel | Status |
|---|---|
| Phishing-Klickrate unter 5 % senken | Erreicht (4,2 %) |
| 100 % phishing-resistente MFA für Admins bis 2026-06-30 | Auf Kurs |
| FIDO2-Rollout für alle Mitarbeitenden bis 2026-09-30 abschließen | Auf Kurs |
| Alle High-Schwachstellen in 2 aufeinanderfolgenden Quartalen innerhalb SLA schließen | In diesem Quartal nicht erreicht |
| Externes Überwachungsaudit ohne schwerwiegende Feststellungen bestehen | Offen (Mai) |

### 3.6 Vorfälle

Zehn erfasste Sicherheitsvorfälle (INC-2026-001 bis INC-2026-010). Einer davon war eine meldepflichtige DSGVO-Verletzung (INC-2026-006, versehentliche E-Mail-Offenlegung — 45 Datensätze, keine besonderen Kategorien). Meldung an BfDI innerhalb von 32 Stunden. Betroffene Personen wurden am selben Tag informiert. Post-Incident-Review abgeschlossen; CAPA-2026-005 verfolgt die Korrekturmaßnahmen.

In diesem Quartal waren keine NIS2-Frühwarnmeldungen erforderlich.

## 4. Rückmeldungen interessierter Parteien

- **Kunden:** Eine Beschwerde über unverschlüsselten Vertragsanhang — Ursache von CAPA-2026-005. Ansonsten keine Beschwerden. Kundenzufriedenheits-Umfrage (Q1) ergab 4,3/5 für „Sicherheit und Vertrauen".
- **Mitarbeitende:** Awareness-Umfrage (Q1) ergab 4,1/5. Es wurde mehr Klarheit zum Einsatz von KI-Tools gewünscht — wird in AUP v2.2 adressiert.
- **Betriebsrat:** FIDO2-Rollout-Plan akzeptiert. Zusätzliche Klarstellung zu Bildschirmüberwachung im Homeoffice gewünscht — wird in Telearbeit-Richtlinie ergänzt.
- **Aufsichtsbehörde (BfDI):** Breach-Meldung ohne weitere Rückfrage zur Kenntnis genommen.
- **Lieferanten:** Keine Vorfälle bei kritischen Lieferanten gemeldet.

## 5. Risikobeurteilung und -behandlung

Risikoregister überprüft. Fünf Haupt­risiken:

- **R-001 Ransomware** — Behandlung in Umsetzung, Restrisiko unverändert bis FIDO2 und Segmentierung abgeschlossen sind.
- **R-002 Phishing** — Restrisiko von 12 auf 9 gesenkt nach Verbesserungen bei Phishing-Simulationen.
- **R-003 Insider-Datenabfluss** — DLP-Arbeiten laufen.
- **R-004 Lieferantenausfall** — mit Monitoring akzeptiert; Qualifizierung eines zweiten Anbieters in Q2/Q3.
- **R-005 Fehlkonfiguration** — S3-Account-weiter Block umgesetzt (RTP-011 geschlossen). IaC-Scan in Bearbeitung.

Der Risikoappetit bleibt: niedrig bei Vertraulichkeits- und Integritätsverletzungen von Kundendaten, mittel bei Verfügbarkeitseinschränkungen unter 4 Stunden.

Keine neuen Top-Risiken in diesem Quartal identifiziert.

## 6. Verbesserungsmöglichkeiten

- Einführung eines AUP-Zusatzes zum Einsatz von KI-Tools.
- Automatisierung der Schwachstellen-SLA-Berichterstattung über SIEM-Dashboard.
- Erweiterung des Lieferanten-Sicherheitsfragebogens um einen NIS2-Ausrichtungsabschnitt.
- Pilot einer Red-Team-Übung mit externem Anbieter in Q4.

## 7. Entscheidungen und Maßnahmen

| # | Entscheidung / Maßnahme | Verantwortlich | Fällig | Art |
|---|---|---|---|---|
| MR-2026-Q1-01 | ISMS Statement of Applicability v3.0 genehmigen | CEO | 2026-03-30 | Entscheidung |
| MR-2026-Q1-02 | Aktualisierung des Risikobehandlungsplans (RTP v4) genehmigen | CEO | 2026-03-30 | Entscheidung |
| MR-2026-Q1-03 | Budget von 15.000 EUR für FIDO2-Rollout für Mitarbeitende freigeben | CEO | 2026-03-30 | Entscheidung |
| MR-2026-Q1-04 | AUP-Zusatz zu KI-Tool-Nutzung entwerfen | ISB | 2026-05-31 | Maßnahme |
| MR-2026-Q1-05 | Schwachstellen-SLA-Dashboard im SIEM aufbauen | IT-Betriebsleitung | 2026-06-30 | Maßnahme |
| MR-2026-Q1-06 | Zweiten Logistik-SaaS-Anbieter qualifizieren | Einkauf | 2026-12-31 | Maßnahme |
| MR-2026-Q1-07 | Red-Team-Übung für Q4 planen (Scope + Anbieter-Shortlist) | ISB | 2026-08-31 | Maßnahme |
| MR-2026-Q1-08 | Externes Überwachungsaudit vorbereiten (KPMG, 2026-05-18) | ISB | 2026-05-11 | Maßnahme |

**Schlussfolgerung:** Das ISMS ist geeignet, angemessen und wirksam. Weiterführende Ausrichtung: Identitätskontrollen stärken (FIDO2), Schwachstellenbehandlung verbessern und NIS2-Audit-Bereitschaft vorbereiten.

**Nächstes Management-Review:** 2026-06-29.

---

*Protokoll genehmigt von Katharina Meier (CEO) am 2026-04-02.*
