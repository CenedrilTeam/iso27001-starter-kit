# Incident-Response-Runbooks

> **Dokumentenkontrolle**  
> Eigentümer: Informationssicherheitsbeauftragte  
> Genehmigt von: CEO  
> Version: 1.0  
> Gültig ab: 2026-03-01  
> Klassifizierung: Vertraulich — beschränkt auf SecOps, IT-Betrieb, DSB, CMT

## Verwendung dieses Dokuments

Dieses Dokument enthält Runbooks für die häufigsten Informationssicherheitsvorfälle bei Nordwind Logistics GmbH. Jedes Runbook folgt derselben Struktur nach NIST SP 800-61 Rev. 2: **Vorbereitung → Erkennung & Analyse → Eindämmung → Beseitigung → Wiederherstellung → Lessons Learned**.

Runbooks ersetzen kein Urteilsvermögen. Sie sind ein Ausgangspunkt. Der Incident Response Plan (PROC-001) definiert den Gesamtprozess, die Rollen und die Schweregrad-Matrix.

**Schweregrad-Skala:**

- **Niedrig:** isoliert, eingedämmt, keine Geschäftsauswirkung, keine personenbezogenen Daten betroffen.
- **Mittel:** begrenzte Geschäftsauswirkung, keine bestätigte Datenpanne, mit internen Ressourcen handhabbar.
- **Hoch:** wesentliche Geschäftsauswirkung ODER bestätigte personenbezogene Datenpanne ODER mehr als ein kritisches System betroffen.
- **Kritisch:** organisationsweite Auswirkung ODER Ransomware ODER große regulatorische Exposition.

**Häufig referenzierte Rollen:**

- **On-Call Engineer** — Erstreaktion, 24/7 verfügbar
- **ISB** — Informationssicherheitsbeauftragte, verantwortet den Vorfall
- **DSB** — Datenschutzbeauftragte, verantwortet regulatorische Aspekte personenbezogener Datenpannen
- **IT-Betriebsleitung** — verantwortet technische Wiederherstellung
- **CMT** — Krisenmanagement-Team, aktiviert bei Hoch und Kritisch
- **Kommunikationsleitung** — verantwortet externe Kommunikation

---

## Runbook 1 — Ransomware

**Auslöser:** Dateien mit unbekannter Endung umbenannt, Lösegeldnotiz gefunden, EDR-Ransomware-Erkennung, Massendatei-Änderungs-Alarm, mehrere Nutzer melden Unfähigkeit, Dateien zu öffnen.

**Standard-Schweregrad:** Kritisch

### T+0 bis T+15 Minuten — Erkennung und sofortige Eindämmung

1. On-Call Engineer bestätigt, dass kein Fehlalarm vorliegt: EDR-Konsole prüfen, nach Lösegeldnotiz suchen, eine betroffene Datei öffnen.
2. **Betroffenen Host sofort vom Netz trennen.** Netzwerkkabel ziehen oder Netzwerkadapter via EDR deaktivieren. Nicht ausschalten (flüchtige Beweise könnten verloren gehen).
3. ISB über die Krisen-Hotline informieren. Die ISB erklärt den Vorfall mit Schweregrad Kritisch.
4. ISB aktiviert das CMT. War-Room-Kanal eröffnen.
5. Alle Hosts mit denselben Indikatoren über EDR-Threat-Hunting identifizieren. Jeden Treffer isolieren.
6. Kompromittierte/s Benutzerkonto/-konten deaktivieren und Zugangsdaten rotieren.

### T+15 Minuten bis T+1 Stunde — Scope und Eindämmung

1. Lateral-Movement-Pfade identifizieren: Authentifizierungslogs der letzten 7 Tage für das kompromittierte Konto auf anderen Systemen prüfen.
2. Prüfen, ob die Backup-Infrastruktur betroffen ist. Falls ja, Backups bis zur Verifikation als nicht vertrauenswürdig behandeln.
3. Entscheidung treffen, ob betroffene Fileshares offline genommen werden. Standard: ja.
4. Bereitschafts-Rechtsbeistand und DSB informieren. Die DSB beginnt parallel eine Datenschutz-Folgenbewertung.
5. Snapshots aller betroffenen Hosts für forensische Analyse erstellen (vollständiges Festplatten-Image wo möglich).
6. CEO informieren. CEO genehmigt externe Incident-Response-Unterstützung bei Bedarf.

### T+1 bis T+24 Stunden — Beseitigung und Wiederherstellungsentscheidung

1. **Kein Lösegeld zahlen.** Dies ist eine stehende Entscheidung von Nordwind Logistics und im PROC-001 dokumentiert.
2. Ransomware-Familie wenn möglich identifizieren (ID Ransomware, EDR-Anbieter-Advisories prüfen). Entsprechendes Beseitigungsverfahren anwenden.
3. Entscheidung: Betroffene Systeme aus sauberen OS-Images neu aufbauen, dann Daten aus Offline-Backup wiederherstellen.
4. Vor jeder Wiederherstellung verifizieren, dass das Offline-Backup nicht betroffen ist. Erst in eine isolierte Umgebung wiederherstellen und Datei-Integrität validieren.
5. **Behördenmeldungen:**
   - NIS2-Frühwarnung an BSI innerhalb von 24 Stunden nach Kenntnisnahme (Vorlage im Krisenkommunikations-Dokument).
   - DSGVO Art. 33 Meldung an BfDI innerhalb 72 Stunden, falls personenbezogene Daten betroffen sind.
6. Kundenbenachrichtigung: durch Kommunikationsleitung vorbereitet, von CEO genehmigt, gemäß Krisenkommunikations-Template versendet.

### T+24 Stunden und danach — Wiederherstellung

1. Betroffene Systeme aus sauberen Images mit gehärteten Baselines neu aufbauen.
2. Daten aus verifiziertem Offline-Backup wiederherstellen.
3. Alle Zugangsdaten in der kompromittierten Domäne zurücksetzen (oder vollständige AD-krbtgt-Rotation, falls Domain Controller betroffen waren).
4. Monitoring-Sensitivität für 30 Tage nach dem Vorfall erhöhen.
5. Bestätigen, dass Backups weiter funktionieren.

### Lessons Learned

Innerhalb von 10 Arbeitstagen nach Vorfallschluss führt die ISB eine Post-Incident-Review durch. Output: Post-Incident-Report, CAPA-Einträge, aktualisiertes Runbook (falls nötig), Feedback in Bedrohungsregister.

---

## Runbook 2 — Phishing und Zugangsdaten-Kompromittierung

**Auslöser:** Nutzer meldet verdächtige E-Mail und gibt an, Zugangsdaten eingegeben zu haben; Postfach mit Bounces überflutet; MFA-Prompt-Fatigue; EDR-Alarm zu Credential-Stealer-Browser-Erweiterung; SIEM-Alarm zu unmöglicher Reise (impossible travel).

**Standard-Schweregrad:** Mittel (Hoch bei Admin-Konto oder Finanzteam)

### T+0 bis T+15 Minuten — Eindämmung

1. On-Call Engineer deaktiviert sofort das betroffene Benutzerkonto (M365 + AD).
2. Force-Sign-Out für alle Sessions des betroffenen Nutzers erzwingen.
3. Aktive OAuth-Tokens und Refresh-Tokens widerrufen.
4. Zugangsdaten rotieren. Temporäres Passwort ausgeben.
5. Vorfallticket eröffnen und ISB informieren.

### T+15 Minuten bis T+1 Stunde — Untersuchung

1. Authentifizierungslogs für das betroffene Konto der letzten 14 Tage abrufen. Suchen nach:
   - Anmeldungen aus unerwarteten Standorten oder IPs.
   - Erstellten Mail-Weiterleitungsregeln.
   - Postfach-Delegationsänderungen.
   - Erteilten OAuth-Einwilligungen.
   - Gesendete-Ordner mit internen Phishing- oder Betrugsversuchen.
2. Falls Mail-Weiterleitungsregeln erstellt wurden — entfernen und als Beweis erfassen.
3. Prüfen, ob der Nutzer Zugriff auf Finanz- oder HR-Systeme hat und ob in den letzten 24 Stunden sensible Transaktionen stattfanden.
4. Im SIEM nach derselben Phishing-URL oder Indikatoren über alle Nutzer hinweg suchen. URL am Mail- und Web-Gateway blockieren.

### T+1 Stunde bis T+24 Stunden — Eindämmung (organisationsweit)

1. Phishing-Domain und alle beobachteten Indikatoren am Mailfilter, Webfilter, DNS und EDR blockieren.
2. Gezielte Suche über alle Postfächer nach der ursprünglichen Phishing-E-Mail. In Quarantäne stellen oder löschen.
3. Alle Mitarbeitenden über die Phishing-Welle mit konkreten Details informieren (Absender, Betreff, was tun bei Klick).
4. Benutzerkonto erst nach MFA-Neuerfassung und Sicherheits-Briefing wieder aktivieren.

### Wiederherstellung und Nachverfolgung

1. Indikatoren in Bedrohungsregister aufnehmen.
2. Innerhalb von 30 Tagen gezielte Phishing-Simulation gegen das betroffene Team durchführen.
3. Falls das Phishing-Kit bestehende Kontrollen umging, CAPA für Verschärfung der Mailfilterung oder Beschleunigung des FIDO2-Rollouts eröffnen.
4. Falls Finanz- oder Datenbetrug stattgefunden hat (z. B. CEO-Fraud), auf Hoch eskalieren und zusätzlich Runbook 3 anwenden.

---

## Runbook 3 — Personenbezogene Datenpanne

**Auslöser:** E-Mail mit personenbezogenen Daten an falschen Empfänger, verlorenes Gerät mit personenbezogenen Daten, unbefugter Zugriff auf Datenbank mit personenbezogenen Daten, fehlkonfigurierter Cloud-Speicher mit offengelegten personenbezogenen Daten, öffentliche Offenlegung von Kundeninformationen.

**Standard-Schweregrad:** Hoch (immer — nach Bewertung neu beurteilen)

### T+0 bis T+15 Minuten — Erstmaßnahme

1. Wer die Panne entdeckt, informiert die DSB sofort.
2. Die DSB erklärt den Vorfall und eröffnet ein Breach-Record. Die 72-Stunden-Frist nach DSGVO Art. 33 beginnt im Moment der Kenntnisnahme.
3. Sofortmaßnahme zum Stoppen weiterer Offenlegung: E-Mail zurückrufen, System offline nehmen, Zugriff entziehen, Konfiguration ändern.

### T+15 Minuten bis T+1 Stunde — Erstbewertung

1. Die DSB dokumentiert:
   - Art der Panne (Vertraulichkeit, Integrität, Verfügbarkeit).
   - Kategorien der betroffenen Personen.
   - Kategorien der betroffenen personenbezogenen Daten (besondere Kategorien gemäß DSGVO Art. 9?).
   - Ungefähre Anzahl betroffener Personen und Datensätze.
   - Wahrscheinliche Folgen für betroffene Personen.
   - Getroffene oder geplante Maßnahmen.
2. Die DSB informiert ISB, CEO und Kommunikationsleitung.
3. Falls die Panne voraussichtlich zu einem hohen Risiko für betroffene Personen führt, beginnt die DSB den Entwurf einer Art. 34 Benachrichtigung.

### T+1 Stunde bis T+24 Stunden — Untersuchung

1. Ursache feststellen: menschlicher Fehler, technischer Defekt, böswillige Handlung, Lieferantenversagen?
2. Feststellen, ob die Daten tatsächlich von einer unbefugten Partei abgerufen wurden (im Gegensatz zu nur offengelegt).
3. Bestätigen, dass die Eindämmung vollständig ist. Falls nicht, eskalieren.
4. Bei Unsicherheit über Meldepflichten externen Rechtsbeistand konsultieren.

### Innerhalb 72 Stunden — Behördenmeldung

1. Meldung an die zuständige Aufsichtsbehörde (BfDI) über das Online-Portal einreichen. Alle verfügbaren Fakten angeben. Bei unvollständigen Fakten das Bekannte einreichen und später ergänzen.
2. Begründung im Breach-Record dokumentieren.
3. Falls die Panne grenzüberschreitende Verarbeitung betrifft, federführende Aufsichtsbehörde identifizieren und Meldung entsprechend leiten.

### Wenn erforderlich — Benachrichtigung der betroffenen Personen (Art. 34)

1. Benachrichtigung mit dem Krisenkommunikations-Template entwerfen.
2. DSB und CEO genehmigen den Wortlaut.
3. Über den geeignetsten Kanal versenden (E-Mail, Brief oder öffentliche Bekanntmachung, falls individueller Kontakt nicht möglich ist).

### Wiederherstellung und Nachverfolgung

1. Korrekturmaßnahmen umsetzen, um Wiederholung zu verhindern (CAPA).
2. Breach-Register aktualisieren.
3. Im nächsten Management-Review berichten.
4. Falls die Panne durch einen Lieferanten verursacht wurde, Lieferanten-Sicherheitsprüfung auslösen.

---

## Runbook 4 — Distributed Denial of Service (DDoS)

**Auslöser:** Kundenseitiger Dienst nicht erreichbar, Monitoring-Alarme zu Antwortzeit, abnormale Traffic-Spitze, Web Application Firewall meldet volumetrischen Angriff.

**Standard-Schweregrad:** Mittel (Hoch bei Spitzenzeiten oder längerem Ausfall)

### T+0 bis T+15 Minuten — Bestätigen und charakterisieren

1. On-Call Engineer bestätigt, dass es sich um DDoS handelt und nicht um Backend-Versagen: WAF-Dashboard, Traffic-Graphen, Quell-IP-Verteilung prüfen.
2. Angriffstyp identifizieren: volumetrisch (Netzwerk), Protokoll (TCP SYN, UDP) oder Anwendungsschicht (HTTP-Flood).
3. ISB und IT-Betriebsleitung informieren. ISB erklärt den Vorfall.

### T+15 Minuten bis T+1 Stunde — Mitigation

1. **Volumetrisch/Netzwerk:** Upstream-DDoS-Schutz beim ISP oder CDN-Anbieter aktivieren. Rate Limiting und Geoblocking aktivieren, falls der Angriff geografisch konzentriert ist.
2. **Protokoll:** Ressourcenlimits an Edge-Geräten erhöhen, SYN-Cookies aktivieren, Upstream-Anbieter kontaktieren.
3. **Anwendungsschicht:** WAF-Challenge-Modus aktivieren, Rate Limits pro IP erhöhen, bekannte Bot-Signaturen blockieren, bei Cloud-Native-Anwendungen Instanzen skalieren.
4. Mit Anbietern koordinieren. Bei SaaS-Anbietern (z. B. Logistikportal) sofort P1-Ticket eröffnen.
5. Mit Kunden über Statusseite kommunizieren (Krisenkommunikations-Template).

### T+1 Stunde bis T+24 Stunden — Anhaltende Mitigation

1. Mitigationsregeln kontinuierlich überwachen und anpassen.
2. Traffic-Samples für Post-Incident-Analyse erfassen (bereits gefiltert, um Log-Wachstum zu begrenzen).
3. Falls Erpressung vorliegt (RDoS), nicht zahlen. ISB und CEO informieren. Als separaten Vorfall behandeln.

### Wiederherstellung und Nachverfolgung

1. Mitigation graduell zurückfahren, sobald der Angriff abklingt.
2. Post-Incident-Review: War die WAF wirksam, hat das CDN den Angriff abgefangen, war die Kundenkommunikation rechtzeitig?
3. Bedrohungsregister mit Angriffssignaturen aktualisieren.
4. Vertragliche SLAs mit dem Upstream-Anbieter überprüfen.

---

## Runbook 5 — Verlorenes oder gestohlenes Gerät

**Auslöser:** Mitarbeiter meldet verlorenes oder gestohlenes Firmen-Laptop, -Telefon oder Wechselmedium. Gerät kann vertrauliche Daten enthalten und Netzwerkzugang ermöglichen.

**Standard-Schweregrad:** Mittel (Hoch falls Gerät personenbezogene Kundendaten oder unverschlüsselte besondere Kategorien enthielt)

### T+0 bis T+15 Minuten — Eindämmung

1. On-Call Engineer oder IT-Helpdesk bestätigt die Meldung (wann, wo, welches Gerät).
2. Remote Wipe via MDM auslösen (Intune für Windows/iOS, Jamf für macOS).
3. Benutzerkonto temporär deaktivieren und Force-Sign-Out aus allen Sessions erzwingen.
4. Gerätezertifikat aus Active Directory und IdP widerrufen.
5. ISB informieren.

### T+15 Minuten bis T+1 Stunde — Bewertung

1. Feststellen, welche Daten auf dem Gerät waren:
   - War Festplattenverschlüsselung aktiviert und aktiv? (BitLocker- / FileVault-Status aus MDM.)
   - Hatte der Nutzer lokale Kopien von Kundendaten, personenbezogenen Daten oder Verträgen?
   - An welchen Systemen war das Gerät authentifiziert?
2. Falls Festplattenverschlüsselung als aktiv bestätigt war und das Gerät beim Verlust ausgeschaltet war, ist das Risiko deutlich reduziert.
3. Falls das Gerät personenbezogene Daten enthielt und der Verschlüsselungsstatus unsicher ist, als potenzielle personenbezogene Datenpanne behandeln und DSB einbinden (Runbook 3).
4. Erinnerung des Nutzers schriftlich erfassen.

### T+1 Stunde bis T+24 Stunden — Untersuchung und Polizeibericht

1. Der Nutzer erstattet Anzeige bei der Polizei und stellt das Aktenzeichen bereit.
2. Versicherung wird informiert, falls zutreffend.
3. Die ISB dokumentiert den Vorfall und verknüpft ihn mit dem Gerätedatensatz im Asset-Register.
4. Falls das Gerät gezielt gestohlen wurde (verdächtige Umstände), auf Hoch eskalieren und prüfen, ob andere Mitarbeitende desselben Teams gefährdet sind.

### Wiederherstellung und Nachverfolgung

1. Ersatzgerät ausgeben, nachdem der Nutzer zur Gerätesicherheit nachgeschult wurde.
2. Prüfen, ob die Daten auf dem Gerät notwendig oder übermäßig waren — gegebenenfalls minimieren.
3. Prüfen, ob Geräte-Tracking und Remote-Wipe-Abdeckung in der gesamten Flotte bei 100 % liegen.
4. Falls der Verlust eine Prozesslücke offenbart, CAPA eröffnen.

---

## Nach jedem Vorfall — Abschluss und Verbesserung

Unabhängig davon, welches Runbook verwendet wurde, löst jeder geschlossene Vorfall aus:

1. **Post-Incident-Report** innerhalb von 10 Arbeitstagen, geschrieben vom IR-Lead, geprüft durch die ISB.
2. **CAPA-Einträge** für jede Ursache, die Korrekturmaßnahmen erfordert.
3. **Bedrohungsregister-Aktualisierung** falls neue Indikatoren oder TTPs beobachtet wurden.
4. **Runbook-Aktualisierung** falls der Vorfall Lücken in diesem Dokument offenbart hat.
5. **Management-Review-Input** im nächsten Quartalsreview.

---

*Diese Runbooks sind lebende Dokumente. Mindestens jährlich und nach jedem Vorfall überprüfen. Zuletzt überprüft: 2026-03-01.*
