# Richtlinie zur Geschäftskontinuität

> **Dokumentenkontrolle**  
> Eigentümer: [RICHTLINIEN_EIGENTÜMER_ROLLE, z. B. Informationssicherheitsbeauftragte/r]  
> Genehmigt von: [GENEHMIGER_NAME_UND_ROLLE]  
> Version: [VERSION]  
> Gültig ab: [GÜLTIGKEITSDATUM]  
> Nächste Überprüfung: [NÄCHSTES_ÜBERPRÜFUNGSDATUM]

## 1. Rechtliche/Regulatorische Grundlage

ISO/IEC 27001:2022 / ISO/IEC 27002:2022, Anhang A:

- A 5.29 — Informationssicherheit während einer Störung
- A 5.30 — IKT-Bereitschaft für die Geschäftskontinuität

BSI IT-Grundschutz:

- DER.4 (Notfallmanagement / Business Continuity Management)
- DER.2.1 (Behandlung von Sicherheitsvorfällen)
- CON.3 (Datensicherungskonzept)

BSI-Standard 200-4 (Business Continuity Management).

Weitere jurisdiktionsspezifische Gesetze und Vorschriften — insbesondere NIS2, DORA und branchenspezifische Resilienzanforderungen — sind im Rechtsregister aufgeführt und werden durch Verweis einbezogen.

## 2. Zweck & Geltungsbereich

Diese Richtlinie legt den Rahmen für das Business Continuity Management von **[IHR_ORGANISATIONSNAME]** fest. Sie definiert, wie die Informationssicherheit während Störungen aufrechterhalten wird, wie IKT-Dienste auf die Geschäftskontinuität vorbereitet werden und wie die Organisation ihre Fähigkeit zur Wiederherstellung nach widrigen Ereignissen plant, testet und verbessert.

Die Richtlinie umfasst die Geschäftsauswirkungsanalyse, die Festlegung von Wiederherstellungszielen, die IKT-Kontinuitätsplanung, das Testen und Üben sowie die Aufrechterhaltung von Informationssicherheitsmaßnahmen über alle Phasen der Störung und Wiederherstellung hinweg. Sie gilt für alle Geschäftsprozesse, IKT-Dienste und Informationswerte innerhalb des Geltungsbereichs des ISMS. Alle Beschäftigten, Auftragnehmer und Drittanbieter, die an Kontinuitätsplanung, -reaktion oder -wiederherstellung beteiligt sind, unterliegen dieser Richtlinie.

Das Notfallmanagement priorisiert kritische Geschäftsprozesse. Eskalationsverfahren für Vorfälle definieren klare Schwellen für den Übergang von der Vorfallreaktion zur Notfall- und Krisenaktivierung.

## 3. Informationssicherheit während einer Störung (A 5.29)

Die Informationssicherheit wird während Störungen auf einem angemessenen Niveau aufrechterhalten. Sicherheitsmaßnahmen bleiben während der Vorfallreaktion, des Failover- und des Wiederherstellungsbetriebs aktiv. Wo primäre Maßnahmen nicht verfügbar sind, treten vorab genehmigte kompensierende Maßnahmen sofort in Kraft. Die Wiederherstellung aus verschiedenen Ausfallszenarien — einschließlich technischer Ausfälle, Lieferkettenstörungen, Naturkatastrophen und Cyberangriffe — wird im Voraus als Teil des Notfallmanagements geplant.

- **Sicherheitsmaßnahmen in Kontinuitätsplänen:** Jeder Kontinuitätsplan dokumentiert die relevanten Informationssicherheitsmaßnahmen im Normalbetrieb und definiert, welche kompensierenden Maßnahmen während einer Störung gelten. Failover-Umgebungen erhalten dieselben Zugriffskontrollniveaus, Netzwerksegmentierung und Überwachungsfähigkeiten wie Produktionssysteme. Die Backup-Verschlüsselung wird vor der Wiederherstellung verifiziert, um Datenintegrität und -vertraulichkeit sicherzustellen.
- **Sicherheitsverfahren im Störungsmodus:** Für kritische Sicherheitsmaßnahmen definieren Kontinuitätspläne Störungsmodus-Verfahren, die beschreiben, wie der Schutz aufrechterhalten wird, wenn Primärsysteme nicht verfügbar sind. Mitarbeitende mit Wiederherstellungsverantwortung erhalten jährliche Schulungen zu diesen Verfahren und nehmen an Übungen teil, die ihre Fähigkeit zur Bedienung der Maßnahmen unter eingeschränkten Bedingungen validieren.
- **Kompensierende Maßnahmen:** Für Sicherheitsmaßnahmen, die während einer Störung nicht funktionieren können, dokumentieren Kontinuitätspläne kompensierende Maßnahmen, die einen gleichwertigen Schutz bieten. Jeder Eintrag kompensierender Maßnahmen spezifiziert die ersetzte Primärmaßnahme, den Aktivierungsauslöser und die verantwortliche Person. Kompensierende Maßnahmen werden während Kontinuitätsübungen getestet und nach jeder realen Aktivierung überprüft.

## 4. IKT-Bereitschaft für die Geschäftskontinuität (A 5.30)

Die IKT-Bereitschaft für die Geschäftskontinuität stellt sicher, dass die zur Unterstützung kritischer Geschäftsprozesse erforderlichen IKT-Dienste innerhalb definierter Zeitrahmen wiederhergestellt werden können. Das IKT-Kontinuitätsprogramm deckt den gesamten Lebenszyklus ab: Geschäftsauswirkungsanalyse, Festlegung von Wiederherstellungszielen, Planung, Umsetzung, Testen, Pflege und fortlaufende Verbesserung. Das Datensicherungskonzept deckt sowohl die Erstellung als auch die Wiederherstellung von Backups ab, regelmäßige Wiederherstellungstests sowie die sichere Backup-Lagerung an geografisch getrennten Standorten. Detaillierte Backup-Dokumentation — einschließlich Umfang, Methode, Zeitplan, Aufbewahrung, Speicherorten und Ergebnissen von Wiederherstellungstests — wird als Teil des Notfallwiederherstellungsplans jedes Systems geführt.

### 4.1 Geschäftsauswirkungsanalyse & Wiederherstellungsziele

- **Mindestanforderungen an Leistung & Kapazität:** Jeder IKT-Kontinuitätsplan spezifiziert Mindestanforderungen an Leistung und Kapazität während einer Störung, einschließlich akzeptabler Bandbreite, Speicherkapazität, Rechenleistung und gleichzeitiger Benutzerschwellenwerte. Diese Spezifikationen werden aus der Geschäftsauswirkungsanalyse (BIA) abgeleitet und durch die Prozesseigentümer der abhängigen Geschäftsaktivitäten validiert. Dienstleistungsniveaus im reduzierten Modus werden formal dokumentiert und allen Stakeholdern kommuniziert.
- **Wiederanlaufziele (RTO):** Für jeden priorisierten IKT-Dienst wird ein Wiederanlaufziel (Recovery Time Objective, RTO) definiert. Wiederherstellungsverfahren spezifizieren die genaue Abfolge der Wiederherstellungsschritte, Systemabhängigkeiten und Verifizierungsprüfpunkte. RTOs werden durch regelmäßiges Testen validiert. Jedes Testergebnis, das das definierte RTO überschreitet, löst eine Korrekturmaßnahme und eine Planrevision aus. RTO-Werte werden jährlich und nach wesentlichen Änderungen der IKT-Landschaft überprüft.
- **Wiederherstellungspunkte (RPO):** Für jede priorisierte Informationsressource wird ein Wiederherstellungspunkt (Recovery Point Objective, RPO) definiert. Backup-Strategien und -Frequenzen sind darauf ausgerichtet, die RPO-Anforderungen zu erfüllen oder zu übertreffen. Die Backup-Wiederherstellung wird regelmäßig getestet, um die RPO-Erreichung zu verifizieren. Wo RPO-Anforderungen nahezu keinen Datenverlust zulassen, werden synchrone Replikation oder kontinuierliche Datenschutzmechanismen implementiert. RPO-Werte bestimmen den Backup-Zeitplan, der im Notfallwiederherstellungsplan jedes Systems dokumentiert ist.

### 4.2 Organisationsstruktur

- **IKT-Kontinuitätsorganisation:** Eine IKT-Kontinuitätsorganisation wird mit definierten Rollen eingerichtet: IKT-Kontinuitätsmanager, Wiederherstellungsteam-Leitungen und technische Wiederherstellungsspezialisten. Für jede Rolle ist eine benannte Vertretung vorgesehen, um die Verfügbarkeit bei Abwesenheiten sicherzustellen. Kompetenzanforderungen sind dokumentiert und werden durch Schulungsnachweise verifiziert. Der IKT-Kontinuitätsmanager berichtet der Geschäftsleitung und koordiniert sich mit der/dem Informationssicherheitsbeauftragten in allen sicherheitsbezogenen Kontinuitätsangelegenheiten. Eskalationswege von der Vorfallreaktion zum Notfall- und Krisenmanagement sind definiert und dokumentiert.

### 4.3 IKT-Kontinuitätsplanung

- **Dokumentierte IKT-Kontinuitätspläne:** Für jeden kritischen IKT-Dienst werden umfassende IKT-Kontinuitätspläne dokumentiert. Jeder Plan enthält Aktivierungskriterien, schrittweise Wiederherstellungsanweisungen, Kontaktlisten mit primären und sekundären Kontakten, Ressourcenanforderungen (Personal, Hardware, Software, Netzwerk, Räumlichkeiten) und erwartete Zeitpläne. Pläne verweisen auf die anwendbaren Sicherheitsmaßnahmen aus dem Abschnitt Informationssicherheit während einer Störung. Kommunikationsverfahren legen fest, wie interne und externe Stakeholder in jeder Phase der Störung informiert werden.
- **Managementgenehmigung:** IKT-Kontinuitätspläne werden formal von der Geschäftsleitung genehmigt, bevor die Aktivierungsbereitschaft erklärt wird. Die Genehmigung umfasst die Überprüfung von Management Summaries, Kostenauswirkungen, Restrisikobewertungen und Ressourcenzusagen. Eine erneute Genehmigung wird jährlich sowie nach wesentlichen Änderungen der IKT-Umgebung, der Organisationsstruktur oder der Bedrohungslandschaft eingeholt. Genehmigungsnachweise werden als dokumentierte Informationen im ISMS aufbewahrt.

### 4.4 Tests & Übungen

- **Regelmäßiges Testen & Üben:** IKT-Kontinuitätspläne werden in definierten Intervallen getestet: Tabletop-Übungen mindestens vierteljährlich, technische Wiederherstellungstests mindestens halbjährlich und vollständige Simulationsübungen mindestens jährlich. Testergebnisse, identifizierte Lücken und Korrekturmaßnahmen werden in Testberichten dokumentiert. Jeder Test verifiziert, dass RTOs und RPOs unter realistischen Bedingungen erreichbar sind. Die Backup-Wiederherstellung wird regelmäßig getestet, um zu bestätigen, dass gesicherte Daten innerhalb der RPO-Ziele wiederhergestellt werden können. Gewonnene Erkenntnisse fließen in Planrevisionen ein, und ungelöste Feststellungen werden über den ISMS-Korrekturmaßnahmenprozess nachverfolgt.

### 4.5 Kontinuitätsmanagement

- **Ursachenunabhängige Reaktion:** IKT-Kontinuitätspläne adressieren Störungen unabhängig von der Ursache, einschließlich technischer Ausfälle, Naturkatastrophen, Cyberangriffe, menschlichen Fehlern und Lieferkettenversagens. Reaktionsverfahren sind wo möglich ursachenunabhängig gestaltet, mit ursachenspezifischen Ergänzungen für gezielte Szenarien wie Ransomware, Rechenzentrumsausfall oder Ausfall kritischer Lieferanten. Die Wiederherstellungsplanung deckt vielfältige Ausfallszenarien ab.
- **Unterstützung priorisierter Aktivitäten:** Die in der BIA identifizierten priorisierten Geschäftsaktivitäten werden ihren erforderlichen IKT-Diensten zugeordnet, einschließlich aller Abhängigkeiten von Infrastruktur, Anwendungen, Daten und externen Dienstleistern. Lückenanalysen verifizieren, dass Kontinuitätspläne die Verfügbarkeit dieser Dienste innerhalb der definierten RTOs sicherstellen. Wo Lücken identifiziert werden, werden Behebungsmaßnahmen zugewiesen, nachverfolgt und verifiziert, bevor Pläne als einsatzbereit erklärt werden.
- **Proaktive Reaktion & Frühwarnung:** Kontinuitätspläne definieren Aktivierungskriterien, die eine frühzeitige Reaktion ermöglichen, bevor eine vollständige Störung eintritt. Pläne werden bei der Erkennung von Vorfällen aktiviert, die zu einer Dienstunterbrechung eskalieren könnten, einschließlich Überschreitungen von Kapazitätsschwellen, Replikationsverzögerungswarnungen, Meldungen über Verschlechterung von Lieferantendiensten und Eskalationen von Sicherheitsvorfällen.

## 5. Rollen & Verantwortlichkeiten

- **Geschäftsleitung:** Genehmigt diese Richtlinie, stellt Ressourcen für das Business Continuity Management bereit und stellt sicher, dass Kontinuitätsziele mit der Gesamtgeschäftsstrategie abgestimmt sind.
- **Informationssicherheitsbeauftragte/r (ISB):** Stellt sicher, dass Informationssicherheitsmaßnahmen in alle Kontinuitätspläne integriert sind und dass kompensierende Maßnahmen einen angemessenen Schutz während Störungen bieten.
- **IKT-Kontinuitätsmanager:** Koordiniert das IKT-Kontinuitätsprogramm, pflegt Kontinuitätspläne, plant Tests und Übungen und berichtet der Geschäftsleitung über die Programmwirksamkeit.
- **Wiederherstellungsteam-Leitungen:** Steuern die Ausführung von Wiederherstellungsverfahren für die ihnen zugewiesenen IKT-Dienste, koordinieren sich mit technischen Wiederherstellungsspezialisten und berichten dem IKT-Kontinuitätsmanager über den Fortschritt.
- **Technische Wiederherstellungsspezialisten:** Führen schrittweise Wiederherstellungsverfahren aus, verifizieren die Systemintegrität nach der Wiederherstellung und bestätigen, dass Sicherheitsmaßnahmen wiederhergestellt sind.
- **Prozesseigentümer:** Definieren geschäftliche Anforderungen an RTOs, RPOs und Mindest-Service-Level über den BIA-Prozess. Validieren, dass Kontinuitätspläne ihre operativen Bedürfnisse erfüllen.
- **Alle Beschäftigten & Auftragnehmer:** Nehmen an Kontinuitätsübungen teil, befolgen Verfahren im Störungsmodus und melden Vorfälle, die eine Aktivierung von Kontinuitätsplänen auslösen können.

## 6. Überprüfung & Pflege

Diese Richtlinie wird überprüft:

- Mindestens jährlich im Rahmen des ISMS-Managementbewertungszyklus.
- Nach wesentlichen Geschäftskontinuitätsvorfällen, einschließlich tatsächlicher Aktivierungen von Kontinuitätsplänen.
- Wenn sich die Ergebnisse der Geschäftsauswirkungsanalyse wesentlich ändern, einschließlich Änderungen an der Priorisierung kritischer Prozesse oder an Wiederherstellungszielen.
- Nach wesentlichen Änderungen der IKT-Infrastruktur, der Organisationsstruktur oder der Lieferantenlandschaft.
- Nach Kontinuitätsübungen, die wesentliche Lücken oder Verbesserungsmöglichkeiten aufzeigen.
- Wenn neue rechtliche, regulatorische oder vertragliche Anforderungen an die Geschäftskontinuität identifiziert werden.
