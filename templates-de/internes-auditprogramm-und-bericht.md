# Internes Auditprogramm und Auditbericht — 2026

> **Dokumentenkontrolle**  
> Eigentümer: Informationssicherheitsbeauftragte  
> Genehmigt von: CEO  
> Version: 1.0  
> Gültig ab: 2026-01-15  
> Klassifizierung: Intern

## Teil A — Jährliches internes Auditprogramm 2026

### 1. Zweck und Scope

Dieses Programm beschreibt, wie Nordwind Logistics GmbH 2026 interne Audits ihres Informationssicherheits-Managementsystems durchführt, gemäß ISO/IEC 27001:2022 Abschnitt 9.2. Das Programm stellt sicher, dass das ISMS unabhängig und unparteiisch gegen ISO-Anforderungen und gegen die eigenen Richtlinien geprüft wird und dass das gesamte ISMS innerhalb des Drei-Jahres-Zyklus 2024–2026 mindestens einmal vollständig auditiert wird.

**Auditierter ISMS-Scope:** alle Prozesse, Standorte und Werte innerhalb des ISMS-Scope-Statements v3.0 (Hamburg HQ + Niederlassung Rotterdam).

### 2. Auditgrundsätze

- **Unabhängigkeit:** Auditoren auditieren nicht ihre eigene Arbeit. Wo interne Kapazität nicht ausreicht, wird ein externer Auditor beauftragt.
- **Unparteilichkeit:** Feststellungen basieren auf Belegen, nicht auf Meinungen.
- **Risikobasierte Priorisierung:** Bereiche mit höherem Risiko oder kürzlichen Änderungen werden häufiger auditiert.
- **Kontinuierliche Verbesserung:** Jedes Audit liefert Input für das nächste Management-Review und das CAPA-Register.

### 3. Drei-Jahres-Abdeckungsmatrix

| ISO-Klausel / Bereich | 2024 | 2025 | 2026 |
|---|---|---|---|
| 4 Kontext der Organisation | x |  | x |
| 5 Führung |  | x |  |
| 6 Planung + Risikomanagement | x | x | x |
| 7 Unterstützung (Ressourcen Awareness Dokumentation) |  | x | x |
| 8 Betrieb | x | x | x |
| 9 Bewertung der Leistung | x | x | x |
| 10 Verbesserung | x | x | x |
| Annex A.5 Organisatorisch | teilweise | teilweise | vollständig |
| Annex A.6 Personal | teilweise | vollständig | teilweise |
| Annex A.7 Physisch | vollständig |  | teilweise |
| Annex A.8 Technologisch | teilweise | teilweise | vollständig |

### 4. Auditplan 2026

| Audit-ID | Scope | Art | Lead Auditor | Geplantes Datum | Aufwand | Status |
|---|---|---|---|---|---|---|
| IA-2026-Q1 | Zugriffskontrolle + HR-Sicherheit (A.5.15-18 + A.6) | Intern | Anna Weber (ISB) + Peer | 2026-02-10 | 3 Tage | Abgeschlossen |
| IA-2026-Q2 | Kryptographie + Datenlöschung + Klassifizierung (A.8.10-12 + A.8.24 + A.5.12-13) | Intern | Anna Weber + externer Peer | 2026-05-12 | 3 Tage | Geplant |
| IA-2026-Q3 | Lieferantensicherheit + Cloud (A.5.19-23) | Intern | Anna Weber | 2026-08-18 | 2 Tage | Geplant |
| IA-2026-Q4 | BCM + Incident-Management (A.5.24-30 + A.8.13-14) | Intern | Externer Auditor (Cobalt Alliance) | 2026-11-09 | 4 Tage | Geplant |
| EA-2026-Surveillance | Vollständiges ISMS-Überwachungsaudit | Externe Zertifizierung | KPMG | 2026-05-18 | 5 Tage | Geplant |

### 5. Methodik

Jedes interne Audit folgt demselben fünfphasigen Vorgehen:

1. **Planung:** Scope, Kriterien und Stichproben festlegen, Auditierte eine Woche vorab informieren.
2. **Durchführung:** Eröffnungsgespräch → Dokumentenprüfung → Interviews → Beobachtung → Stichprobenprüfung.
3. **Bericht:** Feststellungen klassifiziert als Schwerwiegende Nichtkonformität, Geringfügige Nichtkonformität, Beobachtung oder Verbesserungsvorschlag.
4. **Abschluss:** Feststellungen mit Auditierten besprechen, Sachverhalt einigen, Übergabe in Abschlussgespräch.
5. **Nachverfolgung:** Feststellungen werden im CAPA-Register erfasst und bis zum Abschluss verfolgt.

### 6. Auditkriterien

- ISO/IEC 27001:2022 (vollständige Norm).
- ISO/IEC 27002:2022 (Kontrollleitfaden, soweit hilfreich).
- Interne Richtlinien und Verfahren aus dem Dokumentenlenkungs-Register.
- Anwendbare rechtliche und regulatorische Anforderungen aus dem Rechtsregister.
- Vertragliche Kundenzusagen.

### 7. Ressourcen und Kompetenz

Das interne Auditprogramm benötigt für 2026 geschätzt 12 Personentage, abgedeckt durch die ISB und einen externen Co-Auditor zur Sicherstellung der Unabhängigkeit. Die leitende interne Auditorin (Anna Weber) hält eine aktuelle ISO/IEC 27001 Lead Auditor-Zertifizierung. Externe Auditoren benötigen vergleichbare Qualifikationen und reichen vor dem Engagement einen aktuellen Lebenslauf ein.

### 8. Berichterstattung und Management-Review

Eine konsolidierte Audit-Zusammenfassung wird durch die ISB am Quartalsende erstellt und in die Management-Review-Inputs aufgenommen. Schwerwiegende Nichtkonformitäten werden sofort eskaliert und warten nicht auf den Management-Review-Zyklus.

---

## Teil B — Internes Audit-Bericht IA-2026-Q1

### 1. Audit-Identifikation

| Feld | Wert |
|---|---|
| Audit-ID | IA-2026-Q1 |
| Audit-Art | Intern |
| Scope | Zugriffskontrolle (A.5.15–A.5.18) + HR-Sicherheit (A.6.1–A.6.6) |
| Auditkriterien | ISO/IEC 27001:2022 + Zugriffskontroll-Richtlinie v2.0 + HR-Sicherheits-Richtlinie v1.5 |
| Lead Auditor | Anna Weber (ISB) |
| Co-Auditor | Tobias Becker (extern — Unabhängigkeit) |
| Auditzeitraum | 2026-02-08 bis 2026-02-10 |
| Auditierte | HR-Leitung, IT-Betriebsleitung, zwei Abteilungsleitungen, drei Stichproben-Mitarbeitende |
| Berichtsdatum | 2026-02-12 |

### 2. Auditziele

- Verifizieren, dass Joiner-/Mover-/Leaver-Prozesse wie dokumentiert funktionieren.
- Verifizieren, dass Zugriffsrechte gemäß Zugriffskontroll-Richtlinie überprüft und angepasst werden.
- Verifizieren, dass HR-Sicherheitskontrollen (Screening, NDAs, Awareness) umgesetzt und nachgewiesen sind.

### 3. Angewandte Methodik

- Dokumentenprüfung: HR-Sicherheits-Richtlinie, Zugriffskontroll-Richtlinie, Joiner-/Leaver-Checklisten, letzter quartalsweiser Zugriffsreview-Bericht, Screening-Verfahren.
- Interviews mit HR-Leitung und IT-Betriebsleitung.
- Stichproben: 10 Joiner-Datensätze (Q4 2025 + Q1 2026), 5 Leaver-Datensätze, 2 Mover-Datensätze, 2 quartalsweise Zugriffsreviews.
- Walk-through des Joiner-Workflows mit einer neuen Mitarbeiterin.
- Systemprüfung: Active Directory Account-Erstellungslogs, MDM-Enrolment, Personio-Onboarding-Datensätze.

### 4. Übersicht der Feststellungen

| Feststellung | Klassifizierung | Klausel | Status |
|---|---|---|---|
| F-01 Drei Joiner-Konten ohne Genehmigungsticket erstellt | Geringfügige Nichtkonformität | A.5.18 | Offen — CAPA-2026-001 |
| F-02 Quartalsweiser Zugriffsreview für Marketing-OU in Q4 2025 nicht abgeschlossen | Geringfügige Nichtkonformität | A.5.18 | Offen — CAPA-2026-006 |
| F-03 Background-Screening-Nachweise nicht einheitlich abgelegt | Beobachtung | A.6.1 | Offen — im MR zu besprechen |
| F-04 Starker Joiner-Workflow mit klarer Automatisierung | Stärke | — | Geschlossen (positiv) |
| F-05 Leaver-Checkliste wirksam — 2-h-Entzug bei Stichproben erreicht | Stärke | A.5.11 + A.6.5 | Geschlossen (positiv) |

### 5. Detaillierte Feststellungen

#### F-01 — Joiner-Konten ohne Genehmigungsticket erstellt

**Klassifizierung:** Geringfügige Nichtkonformität
**Klausel:** A.5.18 Zugriffsrechte
**Belege:** In der Stichprobe von 10 Joiner-Datensätzen wurden drei Konten (erstellt am 2025-11-04, 2025-12-09, 2026-01-22) festgestellt, bei denen das IT-Betriebsteam das AD-Konto angelegt hat, bevor das HR-Onboarding-Ticket in Personio existierte. Die zugehörigen Tickets wurden am Folgetag rückwirkend erstellt.
**Risiko:** Konto-Erstellung ohne vorherige Genehmigung umgeht die Access-Governance und kann zu überprivilegiertem oder verfrühtem Zugriff führen.
**Empfehlung:** Hartes Gate im Joiner-Workflow erzwingen, das die AD-Konto-Erstellung ohne verknüpftes genehmigtes Personio-Ticket verhindert. Monatlicher Abgleich von AD-Konten und Personio-Tickets ergänzen.
**Maßnahme:** CAPA-2026-001 (HR-Leitung, fällig 2026-05-15).

#### F-02 — Quartalsweiser Zugriffsreview für Marketing-OU in Q4 2025 nicht abgeschlossen

**Klassifizierung:** Geringfügige Nichtkonformität
**Klausel:** A.5.18 Zugriffsrechte
**Belege:** Der Q4-2025-Zugriffsreview-Bericht deckt alle OUs außer Marketing ab. Der Review für die Marketing-OU war für den 2025-12-15 geplant, das Meeting wurde aber abgesagt und nicht neu terminiert.
**Risiko:** Ohne aktuellen Zugriffsreview könnten ruhende oder unangemessene Zugriffsrechte in der Marketing-OU bestehen bleiben.
**Empfehlung:** Den fehlenden Review für die Marketing-OU innerhalb von 30 Tagen abschließen. Formale Eskalationsregel ergänzen: Jeder abgesagte Zugriffsreview muss innerhalb von 5 Arbeitstagen neu terminiert werden.
**Maßnahme:** CAPA-2026-006 (IT-Betriebsleitung, fällig 2026-03-15).

#### F-03 — Background-Screening-Nachweise nicht einheitlich abgelegt

**Klassifizierung:** Beobachtung
**Belege:** Bei zwei von fünf geprüften Einstellungen für sensible Rollen war die Bestätigung der Hintergrundprüfung im persönlichen Postfach der HR-Leitung statt im verschlüsselten HR-Archiv abgelegt.
**Risiko:** Persönliche Postfachablage unterliegt keiner Aufbewahrungssteuerung und birgt Verlust- und Zugriffsrisiken.
**Empfehlung:** Screening-Verfahren so anpassen, dass alle Nachweise innerhalb von 5 Arbeitstagen im verschlüsselten HR-Archiv abgelegt werden müssen.
**Maßnahme:** Im nächsten Management-Review besprechen; leichtgewichtige CAPA wird erwartet.

### 6. Beobachtete Stärken

- Der Joiner-Workflow ist gut dokumentiert, automatisiert und zwischen Personio und Active Directory integriert.
- Der Leaver-Prozess erreicht durchgängig das 2-Stunden-Ziel für Zugriffsentzug — alle fünf Stichproben-Leaver-Konten wurden innerhalb von 90 Minuten nach dem Austrittsdatum deaktiviert.
- HR-Leitung und IT-Betriebsleitung zeigen eine starke Zusammenarbeit mit klaren Eskalationspfaden für Ausnahmen.

### 7. Abschlussgespräch

Ein Abschlussgespräch fand am 2026-02-10 um 16:00 mit HR-Leitung, IT-Betriebsleitung und den auditierten Mitarbeitenden statt. Alle Feststellungen wurden vorgestellt, der Sachverhalt unstrittig bestätigt und die Zeitpläne für Korrekturmaßnahmen vereinbart.

### 8. Schlussfolgerung

Die Auditziele wurden erreicht. Der Audit-Scope (Zugriffskontrolle + HR-Sicherheit) ist weitgehend wirksam, mit zwei geringfügigen Nichtkonformitäten und einer Beobachtung. Keine der Feststellungen beeinträchtigt die Gültigkeit der ISMS-Zertifizierung. Alle Feststellungen sind im CAPA-Register erfasst und werden im nächsten Management-Review berichtet.

---

*Genehmigt: Anna Weber, Informationssicherheitsbeauftragte — 2026-02-12.*
