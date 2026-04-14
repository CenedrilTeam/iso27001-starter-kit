# BCM Übungs- und Testprotokoll

> **Dokumentenkontrolle**  
> Eigentümer: BCM-Leitung  
> Genehmigt von: Informationssicherheitsbeauftragte  
> Version: 1.0  
> Gültig ab: 2026-04-01  
> Klassifizierung: Intern

## Zweck

Dieses Dokument protokolliert alle Übungen, Tests und Drills zur Geschäftskontinuität und Wiederherstellung bei Nordwind Logistics GmbH. Es dient als zentraler Nachweis, dass Continuity-Fähigkeiten regelmäßig validiert werden, wie von ISO/IEC 27001:2022 Annex A 5.29 und A 5.30 sowie ISO 22301 Abschnitt 8.5 gefordert.

---

## Übung EX-2025-03 — Portal-Failover Teilsimulation

| Feld | Wert |
|---|---|
| Datum | 2025-09-15 |
| Art | Teilsimulation (technischer Failover + Geschäftsprozess-Fortführung) |
| Scope | CP-01 — Szenario A Logistikportal-Ausfall |
| Dauer | 4 Stunden |
| Teilnehmende | BCM-Leitung, IT-Betriebsleitung, 2 Disponenten, 1 Kundenservice-Mitarbeiter, Kontakt bei Vendor X |
| Beobachter | ISB |

**Ziel:** Validieren, dass das manuelle Logistik-Fallback LOG-FB-01 innerhalb von 2 Stunden nach erklärter Unterbrechung 30 % Erfassungs­kapazität erreicht.

**Szenario:** Simulierter Ausfall des Logistikportals um 09:00. Disponenten wechseln zu manueller Erfassung.

**Ergebnisse:**

- Fallback aktiviert bei T+12 min (Ziel: T+15 min). **Bestanden.**
- 30 % Kapazität erreicht bei T+1 h 45 min (Ziel: T+2 h). **Bestanden.**
- Volle Kapazität wiederhergestellt, nachdem das Portal um T+4 h 20 min wieder aktiviert wurde. Abgleich abgeschlossen bei T+5 h 10 min. **Bestanden.**

**Feststellungen:**

- **Feststellung 1 (Mittel):** Das ausgedruckte Tourenblatt war 48 statt der vorgesehenen 24 Stunden alt. Ursache: geplantes Export-Skript ist unbemerkt fehlgeschlagen. **CAPA-2025-011** — Monitoring für das Export-Skript einrichten und bei Fehler alarmieren. Abgeschlossen am 2025-10-02.
- **Feststellung 2 (Niedrig):** Zwei Kundenservice-Mitarbeitende wussten nicht, wo das Fallback-Playbook zu finden ist. Auffrischungs­schulung geplant.
- **Feststellung 3 (Niedrig):** Die Anbieter-Kontaktnummer im Krisenordner war veraltet. Sofort aktualisiert.

**Gesamtbewertung:** Die Übungsziele wurden erreicht. Zwei prozessuale Verbesserungen und eine datenqualitätsbezogene CAPA.

---

## Übung EX-2025-04 — Tabletop Incident Response

| Feld | Wert |
|---|---|
| Datum | 2025-11-10 |
| Art | Tabletop-Übung |
| Scope | Ransomware-Szenario — IRP + CP-01 + Krisenkommunikation |
| Dauer | 3 Stunden |
| Teilnehmende | CMT (vollständig), IT-Betrieb, SecOps, DSB, Kommunikationsleitung |
| Beobachter | Extern — Cobalt Alliance Security GmbH |

**Szenario:** Simulierter Ransomware-Angriff entdeckt um 02:30 an einem Samstag. Verschlüsselung auf Fileserver und zwei Domain Controllern festgestellt. Lösegeldforderung 900.000 EUR in Bitcoin.

**Geübte Kernentscheidungen:**

- Aktivierung von Incident Response + BCM + Krisenkommunikation.
- Entscheidung, nicht zu zahlen (formale CMT-Entscheidung dokumentiert).
- Zeitlinie für Behördenmeldung (BSI 24 h Frühwarnung + BfDI 72 h).
- Kundenkommunikationsstrategie und Holding Statement für die Presse.

**Feststellungen:**

- **Feststellung 1 (Hoch):** Kein klarer Verantwortlicher für die 24-h-NIS2-Frühwarnung außerhalb der Geschäftszeiten. **CAPA-2025-012** — IRP aktualisieren, sodass der On-Call-Engineer als Erstmeldender benannt ist. Abgeschlossen am 2026-01-05.
- **Feststellung 2 (Mittel):** Das CMT hatte keinen klaren Rechtsberater-Kontakt für Lösegeld-Entscheidungen. Ergänzt im Krisenordner.
- **Feststellung 3 (Mittel):** Das Holding Statement für die Presse war veraltet. Neu geschrieben und in das Krisenkommunikations-Template integriert.
- **Feststellung 4 (Niedrig):** Mehrere Teilnehmende waren mit der Schweregrad-Matrix nicht vertraut. Schulung in den Plan 2026 aufgenommen.

**Gesamtbewertung:** Das Team hat das Szenario mit klarer Entscheidungsstruktur bewältigt. Vier Feststellungen — keine blockierend, eine sofort abgeschlossen.

---

## Test TR-2026-01 — Restore Kundendatenbank

| Feld | Wert |
|---|---|
| Datum | 2026-02-15 |
| Art | Technischer Restore-Test |
| Scope | DR-001 Kundendatenbank (AST-001) |
| Dauer | 3 Stunden |
| Teilnehmende | IT-Betriebsleitung, DBA |
| Beobachter | ISB |

**Ziel:** Validieren, dass die Kundendatenbank aus dem Offsite-Backup innerhalb der 4-h-RTO mit Datenverlust ≤ 15 Minuten (RPO) wiederhergestellt werden kann.

**Methode:** Vollständiger Restore in eine isolierte DR-Umgebung. Verifizierung von Row Counts, referenzieller Integrität und Anwendungs­konnektivität gegen ein maskiertes Test-Frontend.

**Ergebnisse:**

- Restore abgeschlossen in **2 h 50 min** (Ziel: 4 h). **Bestanden.**
- Datenverlust gemessen bei **12 Minuten** (Ziel: 15 min). **Bestanden.**
- Anwendungs­konnektivität mit allen wichtigen Queries verifiziert.

**Feststellungen:** Keine.

**Gesamtbewertung:** Restore-Test erfolgreich. Keine Änderungen erforderlich. Nächster Test: 2026-05-15.

---

## Test TR-2026-02 — Domain-Controller-Failover

| Feld | Wert |
|---|---|
| Datum | 2026-01-20 |
| Art | Technischer Failover-Test |
| Scope | DR-003 Domain Controller (AST-005) |
| Dauer | 2 Stunden |
| Teilnehmende | IT-Betriebsleitung, Systemadministrator |
| Beobachter | Keiner |

**Ergebnis:** Failover zum sekundären DC abgeschlossen in 1 h 30 min (Ziel: 2 h). Authentifizierung verifiziert. Bestanden.

**Feststellungen:** Keine.

---

## Drill DR-2026-01 — Evakuierungsübung (Hamburg HQ)

| Feld | Wert |
|---|---|
| Datum | 2026-03-05 |
| Art | Physische Evakuierungsübung |
| Scope | Vollständige HQ-Evakuierung |
| Dauer | 45 min |
| Teilnehmende | Alle HQ-Mitarbeitenden (56 Personen) |
| Beobachter | Feuerwehr + Facility-Leitung |

**Ergebnis:** Gebäude geräumt in 6 min 40 s (Ziel: <8 min). Alle Mitarbeitenden am Sammelpunkt gezählt. Bestanden.

**Feststellungen:**

- **Feststellung 1 (Niedrig):** Eine Notausgangstür war kurzzeitig durch Lieferboxen blockiert. Sofort freigemacht. Erinnerung an das Lager­team ausgesprochen.

---

## Geplante Übungen (Plan 2026)

| ID | Art | Scope | Geplantes Datum | Leitung |
|---|---|---|---|---|
| EX-2026-01 | Tabletop | Lieferantenausfall (Vendor X Logistics) + CP-01 | 2026-05-20 | BCM-Leitung |
| TR-2026-03 | Technischer Restore | DR-001 Kundendatenbank | 2026-05-15 | IT-Betriebsleitung |
| TR-2026-04 | Technischer Failover | DR-002 Logistikportal (mit Anbieter) | 2026-06-10 | IT-Betriebsleitung |
| EX-2026-02 | Vollständiger Durchlauf | CP-01 Ende-zu-Ende mit Dispositionsteam | 2026-09-15 | BCM-Leitung |
| EX-2026-03 | Tabletop | Datenschutzverletzung (DSGVO Art. 33) + Krisenkommunikation | 2026-11-10 | DSB + ISB |
| DR-2026-02 | Evakuierung | Hamburg HQ | 2026-09-03 | Facility-Leitung |

---

*Protokoll wird quartalsweise durch die BCM-Leitung geprüft und als Input in das Management-Review eingebracht.*
