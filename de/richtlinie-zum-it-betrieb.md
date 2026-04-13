# Richtlinie zum IT-Betrieb

> **Dokumentenkontrolle**  
> Eigentümer: [RICHTLINIEN_EIGENTÜMER_ROLLE, z. B. Informationssicherheitsbeauftragte/r]  
> Genehmigt von: [GENEHMIGER_NAME_UND_ROLLE]  
> Version: [VERSION]  
> Gültig ab: [GÜLTIGKEITSDATUM]  
> Nächste Überprüfung: [NÄCHSTES_ÜBERPRÜFUNGSDATUM]

## 1. Rechtliche/Regulatorische Grundlage

ISO/IEC 27001:2022 / ISO/IEC 27002:2022, Anhang A — Technologische Maßnahmen:

- A 8.8 — Handhabung technischer Schwachstellen
- A 8.13 — Datensicherung
- A 8.14 — Redundanz von Informationsverarbeitungseinrichtungen
- A 8.15 — Protokollierung
- A 8.16 — Überwachungsaktivitäten
- A 8.17 — Uhrensynchronisation
- A 8.20 — Netzwerksicherheit
- A 8.21 — Sicherheit von Netzwerkdiensten
- A 8.22 — Trennung von Netzwerken
- A 8.23 — Webfilterung

BSI IT-Grundschutz:

- OPS.1.1.3 (Patch- und Änderungsmanagement)
- DER.1.A12 (Auswertung von Informationen aus externen Quellen)
- CON.3 (Datensicherungskonzept)
- OPS.1.1.5 (Protokollierung)
- DER.1 (Detektion sicherheitsrelevanter Ereignisse)
- OPS.1.2.6 (NTP-Zeitsynchronisation)
- NET.1.1 (Netzarchitektur und -design)
- NET.1.2 (Netzmanagement)
- NET.3.1 (Router und Switches)
- NET.1.1.A4 (Netzsegmentierung in Sicherheitszonen)
- NET.3.2 (Firewall)

Weitere jurisdiktionsspezifische Gesetze — insbesondere NIS2, sektorspezifische Anforderungen an den IT-Betrieb, Telekommunikationsrecht und Aufbewahrungsrecht — sind im Rechtsregister aufgeführt und werden durch Verweis einbezogen.

## 2. Zweck & Geltungsbereich

Diese Richtlinie legt die betrieblichen Sicherheitsregeln für IT-Systeme, Netzwerke und Dienste bei **[IHR_ORGANISATIONSNAME]** fest. Sie deckt Schwachstellenmanagement, Datensicherung, Redundanz, Protokollierung, Überwachung, Zeitsynchronisation, Netzwerksicherheit, Netzwerkdienstsicherheit, Netztrennung und Webfilterung ab.

Die Richtlinie gilt für alle Personen, die für den Betrieb, die Administration oder die Nutzung der IT-Infrastruktur verantwortlich sind, einschließlich Beschäftigter, Auftragnehmer und Drittanbieter mit Zugriff auf die Informationsverarbeitungseinrichtungen der Organisation.

## 3. Handhabung technischer Schwachstellen (A 8.8)

Ein genaues Asset-Verzeichnis (siehe Asset Management) ist Voraussetzung für ein wirksames Schwachstellenmanagement. Informationen über technische Schwachstellen werden zeitnah eingeholt, die Exposition wird bewertet und angemessene Maßnahmen zur Behandlung der damit verbundenen Risiken werden ergriffen. Software, die vom Hersteller nicht mehr unterstützt wird, wird außer Betrieb genommen oder ersetzt; fortgesetzte Nutzung erfordert eine dokumentierte Risikoakzeptanz mit kompensierenden Maßnahmen.

### 3.1 Rollen, Ressourcen & Werkzeuge

- **Rollen & Verantwortlichkeiten:** Definierte Rollen decken Schwachstellenüberwachung, Risikobewertung, Patch-Koordination und Umsetzungsverfolgung ab. Das IT-Sicherheitsteam koordiniert den Schwachstellenmanagement-Prozess und meldet Feststellungen an die/den Informationssicherheitsbeauftragte/n.
- **Informationsquellen:** Für jeden Asset-Typ im Softwareverzeichnis werden dedizierte Informationsquellen zur Schwachstellenerkennung identifiziert (Herstelleradvisories, CERT-Feeds, CVE-Datenbanken, NVD). Die Quellen werden vierteljährlich überprüft und bei Einführung neuer Asset-Typen aktualisiert.
- **Lieferantenpflichten:** Verträge mit Software- und Hardwarelieferanten enthalten Klauseln, die zeitnahe Schwachstellenmeldungen, die Bereitstellung von Sicherheitspatches und koordinierte Offenlegung fordern.
- **Schwachstellenscans:** Automatisierte Schwachstellenscanner laufen nach einem definierten Zeitplan (mindestens monatlich) gegen alle extern erreichbaren und kritischen internen Systeme. Scanergebnisse werden verifiziert, und die Wirksamkeit von Patches wird durch Folge-Scans bestätigt.
- **Penetrationstests:** Geplante, dokumentierte Penetrationstests oder Schwachstellenbewertungen werden mindestens jährlich von autorisierten und qualifizierten Personen durchgeführt. Umfang, Methodik und Regeln für den Einsatz werden vorab vereinbart, und Feststellungen werden bis zur Behebung nachverfolgt.
- **Drittanbieter-Bibliotheken & Quellcode:** Drittanbieter-Bibliotheken, Open-Source-Komponenten und eigener Quellcode werden mit Software Composition Analysis auf bekannte Schwachstellen überwacht. Dies ist an den sicheren Entwicklungslebenszyklus gebunden (siehe sichere Programmierpraxis).

### 3.2 Offenlegung & Meldung von Schwachstellen

- **Eigene Produkte & Dienste:** Schwachstellen in den eigenen Produkten und Diensten der Organisation, einschließlich solcher, die durch externe Komponenten eingeführt werden, werden durch kontinuierliche Überwachung, automatisierte Scans und Nutzermeldungen erkannt.
- **Interne & externe Meldungen:** Schwachstellenmeldungen werden sowohl von internen Personen als auch von externen Forschern angenommen. Jede Meldung wird bestätigt, innerhalb von 48 Stunden triagiert und bis zur Behebung nachverfolgt.
- **Öffentliche Kontaktstelle:** Eine öffentlich zugängliche Kontaktstelle (z. B. security@domain, ein dediziertes Webformular) wird für die verantwortliche Offenlegung von Schwachstellen durch externe Parteien unterhalten.
- **Meldeverfahren:** Definierte Verfahren regeln die Schwachstelleneinreichung, einschließlich Onlineformularen, strukturierten Vorlagen und Integration mit Threat-Intelligence-Foren. Meldungen werden beim Eingang nach Schweregrad klassifiziert.

### 3.3 Analyse & Verifizierung

- **Meldungsanalyse:** Jede Schwachstellenmeldung wird analysiert und verifiziert, um ihre Gültigkeit, die betroffenen Systeme und die erforderliche Reaktion und Behebung zu ermitteln. Duplikatmeldungen werden konsolidiert.
- **Risikobewertung:** Für jede bestätigte Schwachstelle werden die zugehörigen Risiken anhand von CVSS-Werten und der Asset-Kritikalität der Organisation identifiziert. Angemessene Maßnahmen werden festgelegt: Patch, Workaround, Risikoakzeptanz mit dokumentierter Begründung oder Isolation des betroffenen Systems.
- **Audit-Protokoll:** Ein Audit-Protokoll wird für alle Schritte des Schwachstellenmanagements geführt — von der ersten Meldung über Analyse, Entscheidung, Behebung bis zur Verifizierung. Das Protokoll wird gemäß dem Log-Aufbewahrungsplan der Organisation aufbewahrt.

### 3.4 Behebung & Patching

- **Zeitnahe Maßnahmen:** Behebungsmaßnahmen werden nach Schweregrad innerhalb definierter Fristen umgesetzt: kritische Schwachstellen innerhalb von 72 Stunden, hohe innerhalb von 7 Tagen, mittlere innerhalb von 30 Tagen, niedrige innerhalb von 90 Tagen.
- **Änderungsmanagement:** Alle Patches und Updates folgen den etablierten Änderungsmanagement-Kontrollen (siehe *Richtlinie zu Konfigurations- und Änderungsmanagement*), einschließlich Folgenabschätzung und Genehmigung.
- **Legitime Quellen:** Updates und Patches werden ausschließlich aus legitimen, verifizierten Quellen bezogen (Herstellerwebsites, autorisierte Repositorien). Prüfsummen und digitale Signaturen werden vor der Installation verifiziert.
- **Tests vor Installation:** Updates werden in einer Nicht-Produktionsumgebung vor der Installation auf Produktionssystemen getestet und bewertet. Testergebnisse werden dokumentiert.
- **Priorisierung:** Systeme mit hohem Risiko und geschäftskritische Systeme werden zuerst gepatcht. Die Priorisierung berücksichtigt Asset-Kritikalität, Ausnutzungswahrscheinlichkeit und Expositionsgrad.
- **Behebungsplan:** Ein wirksamer, dauerhafter Behebungsplan wird für jede bestätigte Schwachstelle entwickelt und legt Maßnahmen, Verantwortliche, Zeitpläne und Verifizierungskriterien fest.
- **Wirksamkeitsbestätigung:** Nach der Behebung wird die Wirksamkeit der angewendeten Korrektur durch Re-Scan, Re-Test oder manuelle Verifikation bestätigt.
- **Patch-Authentizität:** Die Authentizität und Integrität von Patches wird vor der Bereitstellung über Prüfsummen, digitale Signaturen oder sichere Hashes verifiziert.
- **Workarounds (kein Update verfügbar):** Wenn kein Herstellerupdate verfügbar ist, werden vom Hersteller empfohlene Workarounds angewendet und als Übergangsmaßnahmen dokumentiert.
- **Dienstabschaltung:** Wenn kein Update oder Workaround existiert, werden betroffene Dienste oder Funktionen deaktiviert, um die Angriffsfläche zu reduzieren.
- **Verschärfte Zugriffskontrollen:** Wenn kein Patch verfügbar ist, werden Zugriffskontrollen um das verwundbare System verschärft und zusätzliche Firewall-Regeln angewendet, um die Exposition einzuschränken.
- **Abschirmung durch Intrusion Detection:** Nicht gepatchte Systeme werden hinter Intrusion-Detection-/Prevention-Systeme (IDS/IPS) gestellt, um Ausnutzungsversuche zu erkennen und zu blockieren.
- **Erhöhte Überwachung:** Die Überwachung nicht gepatchter Systeme wird verstärkt, um Ausnutzungsversuche zu erkennen, einschließlich intensivierter Log-Prüfung und Alarmierung.
- **Sensibilisierung:** Wenn eine Schwachstelle Systeme betrifft, die nicht sofort gepatcht werden können, werden relevante Personen über die Schwachstelle, ihre Risiken und die geltenden Vorsichtsmaßnahmen informiert.
- **Hersteller-Update-Mechanismen:** Für kommerzielle Software werden vom Hersteller bereitgestellte Update-Mechanismen (automatische Update-Dienste, verwaltete Update-Kanäle) genutzt, wo verfügbar, und für die zeitnahe Auslieferung konfiguriert.
- **Bewertung verzögerter Updates:** Ist ein angemessener Test eines Updates innerhalb der erforderlichen Frist nicht möglich, kann das Update verzögert werden. Das zugehörige Risiko des verzögerten Patchens wird bewertet, dokumentiert und vom Risikoeigentümer vor dem Aufschub akzeptiert.

## 4. Datensicherung (A 8.13)

Ein umfassendes Datensicherungskonzept wird für jedes kritische System dokumentiert und deckt Sicherungsumfang, -plan, -speicherung, -aufbewahrung und -wiederherstellungsverfahren ab. Es gilt die 3-2-1-Regel: mindestens drei Datenkopien, auf zwei verschiedenen Medientypen, mit einer Kopie an einem externen Standort. Das Sicherungsdesign berücksichtigt Ransomware-Szenarien, indem Offline- oder unveränderliche Sicherungskopien geführt werden.

### 4.1 Sicherungsdesign & -schutz

- **Sicherungseinrichtungen:** Angemessene Sicherungseinrichtungen werden für alle wesentlichen Informationen, Software und Systemabbilder bereitgestellt, um eine vollständige Wiederherstellung nach einem Datenverlust zu ermöglichen.
- **Sicherungsaufzeichnungen:** Genaue, vollständige Aufzeichnungen aller Sicherungen werden geführt, einschließlich Sicherungsumfang, -plan, verwendeter Medien, Speicherort und dokumentierter Wiederherstellungsverfahren pro System.
- **Sicherungsplan:** Der Sicherungsplan spiegelt die im Business-Continuity-Plan definierten Recovery Point Objectives, die Sicherheitsanforderungen und die Informationsklassifizierung der Daten wider. Kritische Systeme werden mindestens täglich gesichert; weniger kritische Daten gemäß ihrer Klassifizierungsstufe.
- **Auslagerung:** Sicherungskopien werden an einem entfernten Standort gespeichert, der hinreichend weit vom Hauptstandort entfernt ist, um zu verhindern, dass beide von derselben Katastrophe betroffen sind. Der ausgelagerte Standort erfüllt dieselben physischen und umweltbezogenen Sicherheitsanforderungen wie der Primärstandort.
- **Physischer & umweltbezogener Schutz:** Sicherungsmedien werden durch angemessene physische und umweltbezogene Maßnahmen gegen unbefugten Zugriff, Diebstahl, Umweltschäden (Temperatur, Feuchtigkeit, elektromagnetische Interferenz) und Verschleiß geschützt.
- **Regelmäßige Tests:** Sicherungsmedien werden regelmäßig getestet, um die Datenintegrität und Lesbarkeit sicherzustellen. Die Wiederherstellung wird auf einem dedizierten Testsystem getestet — niemals auf der Produktion — um zu verifizieren, dass der gesamte Wiederherstellungsprozess korrekt funktioniert.
- **Sicherungsverschlüsselung:** Sicherungen werden auf Grundlage der Risikobewertung und der Klassifizierung der gesicherten Daten verschlüsselt. Verschlüsselungsschlüssel für Sicherungen werden getrennt von den Sicherungsmedien gespeichert und gemäß der Schlüsselverwaltungsrichtlinie verwaltet.
- **Erkennung von Datenverlust:** Verfahren erkennen unbeabsichtigten Datenverlust oder -korruption, bevor die Sicherung ausgeführt wird, um sicherzustellen, dass beschädigte Daten nicht über gültige Kopien gesichert werden.
- **Sicherungsüberwachung:** Die Sicherungsausführung wird automatisch überwacht. Fehler werden protokolliert, alarmiert und innerhalb definierter Fristen behandelt. Sicherungsprotokolle werden wöchentlich überprüft.
- **Cloud-Sicherung:** Wenn cloudbasierte Sicherungsdienste genutzt werden, werden die Fähigkeiten des Cloud-Anbieters anhand der Sicherungsanforderungen der Organisation bewertet, einschließlich Datensouveränität, Verschlüsselung, Aufbewahrung, Wiederherstellungsgeschwindigkeit und vertraglicher SLAs.

### 4.2 Sicherungstests & Validierung

- **Abstimmung auf Incident Response:** Sicherungsmaßnahmen werden regelmäßig gegen die Ziele der Incident-Response- und Business-Continuity-Pläne getestet, um zu bestätigen, dass gesicherte Daten, Software und Systemabbilder für eine vollständige Wiederherstellung ausreichen.
- **Wiederherstellungszeittests:** Wiederherstellungsverfahren werden gegen die im Business-Continuity-Plan definierten Wiederherstellungszeitanforderungen getestet. Testergebnisse werden dokumentiert, und etwaige Defizite bei der Wiederherstellungsgeschwindigkeit lösen Korrekturmaßnahmen aus.

## 5. Redundanz von Informationsverarbeitungseinrichtungen (A 8.14)

Verfügbarkeitsanforderungen für Geschäftsservices und Informationssysteme werden identifiziert, und die Architektur wird mit ausreichender Redundanz gestaltet, um sie zu erfüllen. Das Redundanzdesign berücksichtigt den Zusammenhang mit der IKT-Bereitschaft für Business Continuity und trägt den Integritätsrisiken Rechnung, die durch Datenreplikation auf duplizierte Komponenten entstehen können.

### 5.1 Redundanzdesign

- **Mehrere ISPs / Lieferanten kritischer Einrichtungen:** Es werden Verträge mit mindestens zwei unabhängigen Internetdienstanbietern oder Lieferanten kritischer Einrichtungen geführt, um die Abhängigkeit von einem einzigen Anbieter zu eliminieren.
- **Redundante Netze:** Redundante Netzwege sind so implementiert, dass der Ausfall einer einzelnen Netzwerkverbindung kritische Dienste nicht unterbricht.
- **Geografisch getrennte Rechenzentren:** Zwei geografisch getrennte Rechenzentren mit gespiegelten Systemen werden für kritische Dienste betrieben und sichern die Kontinuität, falls ein Standort nicht verfügbar ist.
- **Redundante Stromversorgungen:** Physisch redundante Stromversorgungen und unabhängige Energiequellen (USV, Generatoren, doppelte Versorgungsanschlüsse) werden für kritische Informationsverarbeitungseinrichtungen installiert.
- **Parallele Softwareinstanzen:** Mehrere parallele Softwareinstanzen mit automatischem Load Balancing werden für kritische Anwendungen bereitgestellt und verteilen die Last sowie Failover-Kapazität.
- **Doppelte Komponenten:** Kritische Hardwarekomponenten — CPUs, Festplatten, Speicher, Firewalls, Router, Switches — werden dupliziert, um Single Points of Failure zu eliminieren.

### 5.2 Failover-Tests

- **Failover-Verifizierung:** Das Failover von primären auf redundante Komponenten wird in geplanten Intervallen getestet, um zu bestätigen, dass die automatische Umschaltung wie beabsichtigt funktioniert, während des Übergangs keine Daten verloren gehen und die Leistung die definierten Schwellenwerte erfüllt.

## 6. Protokollierung (A 8.15)

Protokolle werden erstellt, gespeichert, geschützt und analysiert, um Ereignisse aufzuzeichnen, die für Informationssicherheit und Datenschutz relevant sind. Protokolldaten werden an einen zentralen Log-Server weitergeleitet. Aufbewahrungsfristen werden je nach Vorschrift und Datentyp festgelegt. Protokolle enthalten keine Passwörter oder personenbezogenen Daten, sofern dies nicht ausdrücklich erforderlich und geschützt ist. Alle Systeme nutzen synchronisierte Zeitquellen (siehe Uhrensynchronisation), um eine systemübergreifende Log-Korrelation zu ermöglichen.

### 6.1 Zu protokollierende Ereignisdaten

- **Benutzer-IDs:** Jedes protokollierte Ereignis erfasst die Benutzer-ID des Kontos oder der Entität, die die Aktion initiiert oder mit ihr verbunden war.
- **Systemaktivitäten:** Aktivitäten auf Systemebene — Dienststarts/-stopps, geplante Aufgaben, Batch-Job-Ausführungen und Systemfehler — werden mit ausreichend Detail für Fehlersuche und Sicherheitsanalyse protokolliert.
- **Datum & Uhrzeit:** Jeder Logeintrag enthält Datum und Uhrzeit des Ereignisses, erfasst von der synchronisierten Systemuhr in UTC oder einer definierten Lokalzeit mit UTC-Offset.
- **Geräteidentität & Standort:** Die Identität des Geräts (Hostname, Asset-ID) und gegebenenfalls sein physischer oder logischer Standort werden in jedem Logeintrag erfasst.
- **Netzwerkadressen & Protokolle:** Quell- und Ziel-IP-Adressen, Portnummern und das verwendete Netzwerkprotokoll werden für alle netzwerkbezogenen Ereignisse protokolliert.
- **Zugriffsversuche:** Alle Zugriffsversuche — erfolgreiche und fehlgeschlagene — auf Systeme, Anwendungen und Daten werden protokolliert, einschließlich der verwendeten Authentifizierungsmethode.
- **Ressourcenzugriff:** Zugriffe auf kritische Ressourcen (Datenbanken, Dateifreigaben, APIs, Administrationsschnittstellen) werden protokolliert, wobei die zugegriffene Ressource identifiziert wird.
- **Konfigurationsänderungen:** Alle Änderungen an System-, Anwendungs- und Sicherheitskonfigurationen werden protokolliert, einschließlich der vorherigen und neuen Werte, soweit möglich.
- **Nutzung von Privilegien:** Die Nutzung privilegierter Konten und erhöhter Rechte wird protokolliert, einschließlich der konkret ausgeübten Privilegien und des Zielsystems oder der Zielressource.
- **Verwendung von Utilities & Tools:** Die Nutzung von Systemutilities, Diagnosetools und Administrationswerkzeugen wird mit dem ausgeführten Befehl oder Vorgang protokolliert.
- **Dateizugriff & -löschung:** Zugriff, Änderung und Löschung von Dateien — insbesondere solche mit klassifizierten oder sensiblen Informationen — werden protokolliert.
- **Zugriffskontrollalarme:** Ereignisse, die durch Zugriffskontrollmechanismen ausgelöst werden (Kontosperrungen, wiederholte Authentifizierungsfehler, unbefugte Zugriffsversuche), werden protokolliert und erzeugen Alarme.
- **Aktivierung & Deaktivierung von Sicherheitssystemen:** Die Aktivierung, Deaktivierung oder Änderung von Sicherheitssystemen (Firewalls, IDS/IPS, Anti-Malware, DLP) wird protokolliert.
- **Änderungen im Identitätsmanagement:** Änderungen an Benutzerkonten, Gruppenzugehörigkeiten, Rollen und Berechtigungen in Identitätsmanagementsystemen werden protokolliert.
- **Anwendungstransaktionen:** Von Nutzern initiierte Transaktionen in geschäftskritischen Anwendungen werden auf einem Detaillierungsgrad protokolliert, der der Klassifizierung der Anwendung angemessen ist.

### 6.2 Log-Schutz & -Integrität

- **Erkennung von Nachrichtentyp-Änderungen:** Kontrollen erkennen Änderungen an protokollierten Nachrichtentypen, einschließlich Änderungen am Log-Format, der Ereigniskategorisierung oder der Schweregrad-Klassifizierung.
- **Erkennung von Log-Datei-Manipulation:** Bearbeitungen, Löschungen oder unbefugte Änderungen an Protokolldateien werden durch Integritätsüberwachung erkannt. Nutzer — einschließlich solcher mit privilegiertem Zugriff — dürfen Protokolle ihrer eigenen Aktivitäten nicht löschen oder deaktivieren.
- **Kapazitäts- & Überschreibungsschutz:** Die Log-Speicherkapazität wird überwacht. Das System erkennt und alarmiert bei Ausfällen der Ereignisaufzeichnung oder beim Überschreiben von Protokolldaten aufgrund von Speichererschöpfung. Log-Rotationsrichtlinien stellen sicher, dass Protokolle archiviert werden, bevor sie überschrieben werden.
- **Kryptographisches Hashing:** Kryptographische Hashes werden in definierten Intervallen auf Protokolldateien angewendet, um die Erkennung nachträglicher Änderungen zu ermöglichen.
- **Append-Only-Speicherung:** Protokolldateien werden in Append-Only- oder Read-Only-Formaten gespeichert. Write-Once-Medien oder unveränderlicher Speicher werden verwendet, wo die Risikobewertung dies rechtfertigt.
- **Öffentliche Transparenzdateien:** Wo anwendbar, werden öffentliche Transparenzmechanismen (z. B. Certificate-Transparency-Logs, Blockchain-verankerte Zeitstempel) eingesetzt, um unabhängig überprüfbaren Nachweis zu liefern, dass Logeinträge nicht verändert wurden.

### 6.3 Log-Analyse

- **Fachkenntnisse zur Analyse:** Personen, die Log-Analysen durchführen, verfügen über die erforderlichen Kenntnisse in Ereignisinterpretation, Angriffsmustererkennung und forensischen Analysetechniken. Schulungen werden beim Onboarding und jährlich aufgefrischt.
- **Analyse von Ereignisattributen:** Log-Analysen berücksichtigen Ereignisattribute (Quelle, Ziel, Aktion, Ergebnis, Zeit), um Muster zu erkennen, die auf Sicherheitsvorfälle hindeuten.
- **Regelbasierte Ausnahmen (SIEM):** Ein Security-Information-and-Event-Management-System (SIEM) wendet regelbasierte Korrelation und Ausnahmenerkennung über Logquellen hinweg an, um Ereignisse zu identifizieren, die von erwarteten Mustern abweichen.
- **Verhaltens-Baselines (UEBA):** User and Entity Behaviour Analytics etablieren Verhaltens-Baselines und erkennen Abweichungen, die auf kompromittierte Konten, Insider-Bedrohungen oder Richtlinienverstöße hindeuten.
- **Trend- & Musteranalyse:** Langfristige Trend- und Musteranalysen werden auf aggregierten Logdaten durchgeführt, um aufkommende Bedrohungen, wiederkehrende Vorfälle oder schleichende Veränderungen von Angriffsvektoren zu identifizieren.
- **Integration von Threat Intelligence:** Die Log-Analyse bezieht Threat-Intelligence-Feeds ein (Indicators of Compromise, bekannte bösartige IPs, Angriffssignaturen), um den Ereigniskontext anzureichern und die Erkennung zu beschleunigen.

### 6.4 Log-Prüfaktivitäten

- **Prüfung von Zugriffen auf geschützte Ressourcen:** Zugriffsversuche auf geschützte Ressourcen (DNS-Server, Webproxys, Dateifreigaben) werden regelmäßig überprüft, um unbefugte Zugriffsmuster oder Datenexfiltrationsversuche zu identifizieren.
- **DNS-Log-Analyse:** DNS-Query-Logs werden analysiert, um Kommunikation mit bekannten Botnet-Command-and-Control-Servern, Domain-Generation-Algorithmen oder DNS-Tunneling-Aktivitäten zu erkennen.
- **Nutzungsberichte von Dienstleistern:** Nutzungsberichte externer Dienstleister (Cloud, SaaS, Managed Services) werden überprüft, um anomale Nutzungsmuster oder unbefugte Nutzung zu identifizieren.
- **Korrelation physischer Überwachung:** Protokolle physischer Überwachungssysteme (Zutrittskontrolle, CCTV, Umweltsensoren) werden mit IT-Ereignisprotokollen korreliert, um koordinierte physisch-digitale Angriffsszenarien zu erkennen.
- **Systemübergreifende Log-Korrelation:** Protokolle aus verschiedenen Systemen, Anwendungen und Sicherheitswerkzeugen werden korreliert, um eine einheitliche Sicht auf Ereignisse zu liefern und mehrstufige Angriffe zu erkennen, die sich über mehrere Systeme erstrecken.

### 6.5 Protokollierungswerkzeuge

- **Audit- & Abfragewerkzeuge:** Dedizierte Werkzeuge zum Abfragen, Suchen und Untersuchen von Logdaten werden eingesetzt. Diese Werkzeuge unterstützen strukturierte Abfragen, Volltextsuche und Filterung nach Ereignisattributen.
- **Automatisierte Überwachung & konsolidierte Berichte:** Automatisierte Überwachungswerkzeuge erstellen konsolidierte Berichte über Logereignisse und fassen wichtige Kennzahlen, Anomaliezahlen und Sicherheitsindikatoren für die Managementüberprüfung zusammen.
- **SIEM-Plattform:** Eine SIEM-Plattform wird für zentrale Logspeicherung, Korrelation, Normalisierung und Alarmgenerierung eingesetzt. Das SIEM nimmt Logs von allen kritischen Systemen auf und wendet Detektionsregeln an, die auf die Bedrohungslage der Organisation abgestimmt sind.
- **Manipulationserkennung über Transparenz:** Wo öffentliche Transparenzdateien oder Blockchain-verankerte Mechanismen verfügbar sind, werden sie in die Protokollierungsinfrastruktur integriert, um unabhängige Manipulationserkennung für hochintegre Log-Streams zu bieten.

Audit-Logs, die für regulatorische Compliance oder Beweissicherung erforderlich sind, werden gemäß den definierten Aufbewahrungsfristen archiviert. Wenn Logs zur Fehlerdiagnose an Anbieter weitergegeben werden, werden sie vor der Übertragung de-identifiziert, um sensible Daten und personenbezogene Informationen zu entfernen.

## 7. Überwachungsaktivitäten (A 8.16)

Netzwerke, Systeme und Anwendungen werden kontinuierlich überwacht, um anomales Verhalten und potenzielle Sicherheitsvorfälle zu erkennen. Umfang und Tiefe der Überwachung werden durch Geschäfts- und Informationssicherheitsanforderungen bestimmt und berücksichtigen geltende rechtliche Verpflichtungen. Ein formales Detektionskonzept definiert die Überwachungsstrategie, Verantwortlichkeiten und Eskalationspfade. Durch Überwachung und Protokollierung erkannte Sicherheitsereignisse werden an den Incident-Management-Prozess der Security Operations zur Triage, Klassifizierung und Reaktion eskaliert.

### 7.1 Überwachungsumfang

- **Netzwerkverkehr:** Eingehender, ausgehender und interner Netzwerkverkehr wird auf Anomalien, unbefugte Verbindungen und Indicators of Compromise überwacht.
- **Zugriff auf Systeme, Server & Anwendungen:** Zugriffe auf Server, Betriebssysteme und Geschäftsanwendungen werden überwacht, mit besonderem Augenmerk auf privilegierte Zugriffe und Aktivitäten außerhalb der Geschäftszeiten.
- **Kritische Konfigurationsdateien:** Änderungen an kritischen Konfigurationsdateien (Betriebssystem, Sicherheitswerkzeuge, Netzwerkgeräte, Anwendungen) werden in Echtzeit überwacht und erzeugen Alarme bei unbefugten Änderungen.
- **Logs von Sicherheitswerkzeugen:** Die Ausgaben von Sicherheitswerkzeugen — Antivirus, IDS/IPS, Firewalls, Data Loss Prevention, Web Application Firewalls — werden überwacht und zentral korreliert.
- **Ereignisprotokolle:** System- und Anwendungsereignisprotokolle werden kontinuierlich in die Überwachungsplattform aufgenommen und gegen Detektionsregeln ausgewertet.
- **Autorisierung der Code-Ausführung:** Die Ausführung von Software und Skripten wird überwacht. Unbefugte oder nicht signierte Code-Ausführungsversuche werden erkannt und, wo technisch machbar, blockiert.
- **Ressourcennutzung:** CPU-, Speicher-, Festplatten- und Bandbreitennutzung werden überwacht, um Ressourcenerschöpfung, Denial-of-Service-Bedingungen und Cryptomining-Aktivitäten zu erkennen.

### 7.2 Baseline-Erstellung

- **Auslastungs-Baselines:** Normale und Spitzenauslastungs-Baselines werden für alle überwachten Systeme etabliert. Abweichungen von diesen Baselines werden zur Untersuchung markiert.
- **Baselines für Nutzerzugriffe:** Typische Zugriffsmuster pro Nutzer — einschließlich üblicher Zugriffszeiten, Quellorte und -häufigkeit — werden profiliert, um die Erkennung anomalen Verhaltens zu ermöglichen.

### 7.3 Anomalieerkennung

- **Ungeplante Prozessbeendigung:** Unerwartete Beendigung kritischer Prozesse oder Dienste löst einen sofortigen Alarm und, sofern konfiguriert, einen automatisierten Neustartversuch aus.
- **Malware-typische Aktivitäten:** Netzwerkverkehr zu bekannten bösartigen IP-Adressen, Domains oder URLs sowie Verhaltensmuster, die typisch für Malware sind (Beaconing, laterale Bewegung, Daten-Staging), werden erkannt und alarmiert.
- **Bekannte Angriffssignaturen:** Das Überwachungssystem wendet aktuelle Angriffssignaturen aus Threat-Intelligence-Feeds an, um bekannte Exploits und Angriffsmuster zu erkennen.
- **Ungewöhnliches Systemverhalten:** Systemverhalten, das von etablierten Baselines abweicht — unerwartete Prozesse, abnormale Speichernutzung, ungewöhnliche Netzwerkverbindungen — löst Untersuchungen aus.
- **Engpässe & Überlastungen:** Systemengpässe, Ressourcenüberlastungen und Überschreitungen von Kapazitätsschwellen werden erkannt und eskaliert, um Dienstverschlechterung oder Denial-of-Service-Bedingungen zu verhindern.
- **Unbefugter Zugriff:** Versuche, ohne gültige Berechtigung auf Systeme, Anwendungen oder Daten zuzugreifen, werden in Echtzeit erkannt, protokolliert und alarmiert.
- **Unbefugtes Scannen:** Netzwerk- und Port-Scan-Aktivitäten aus internen oder externen Quellen werden erkannt und erzeugen Alarme zur Untersuchung.
- **Zugriff auf besonders geschützte Ressourcen:** Zugriffsversuche auf besonders geschützte Ressourcen (Administrationsschnittstellen, sensible Datenspeicher, Sicherheitsinfrastruktur) werden mit erhöhter Empfindlichkeit überwacht.
- **Nutzer- & Systemverhalten vs. Baseline:** Abweichungen von etablierten Verhaltens-Baselines für Nutzer und Systeme — ungewöhnliche Login-Zeiten, atypische Datenzugriffsvolumina, abnormale Transaktionsmuster — werden zur Analyse markiert.

### 7.4 Alarmgenerierung & Reaktion

- **Schwellenwertbasierte Alarme:** Alarme werden auf Basis vordefinierter Schwellenwerte und Detektionsregeln erzeugt. Schwellenwerte werden vierteljährlich überprüft und auf Basis operativer Erfahrungen angepasst.
- **Tuning von False Positives:** Detektionsregeln und Schwellenwerte werden kontinuierlich getunt, um False Positives zu minimieren und gleichzeitig die Erkennungsgenauigkeit zu erhalten. Tuning-Entscheidungen werden dokumentiert.
- **Geschultes Reaktionspersonal:** Geschultes Personal steht zur Verfügung, um innerhalb definierter Reaktionszeiten auf Überwachungsalarme zu reagieren. Eskalationspfade sind dokumentiert und werden in Übungen trainiert.
- **Redundante Alarmsysteme:** Redundante Alarmbenachrichtigungssysteme (z. B. E-Mail, SMS, dedizierte Alarmplattformen) stellen sicher, dass kritische Alarme das Reaktionspersonal auch dann erreichen, wenn ein Benachrichtigungskanal ausfällt.

### 7.5 Überwachungstechniken

- **Threat Intelligence:** Überwachungssysteme beziehen Threat-Intelligence-Feeds ein, um Indicators of Compromise und bekannte Taktiken, Techniken und Verfahren von Bedrohungsakteuren zu identifizieren.
- **Machine Learning & KI:** Machine-Learning- und KI-basierte Detektionsfähigkeiten werden, wo angemessen, eingesetzt, um Anomalien und Zero-Day-Bedrohungen zu identifizieren, die signaturbasierte Erkennung nicht abdecken kann.
- **Block- & Allow-Listen:** Netzwerk- und Anwendungsüberwachung setzen Blocklisten (bekannte bösartige IPs, Domains, Hashes) und Allow-Listen durch, um Kommunikation auf autorisierte Ziele zu beschränken.
- **Sicherheitsbewertungen:** Erkenntnisse aus Penetrationstests, Schwachstellenbewertungen und Sicherheitsaudits werden in das Überwachungssystem zurückgespielt, um Detektionsregeln und Abdeckung zu verbessern.
- **Anomalieerkennung durch Performance-Monitoring:** Performance-Monitoring-Daten werden auf sicherheitsrelevante Anomalien analysiert — etwa CPU-Spitzen, die auf Cryptomining hinweisen, oder Bandbreitenanstiege, die auf Datenexfiltration hindeuten.
- **Kombination von Logs & Überwachung:** Logdaten und Echtzeit-Überwachung werden kombiniert, um umfassendes Lagebewusstsein zu bieten und die Erkennung langsamer Bedrohungen zu ermöglichen, die einzelne Datenquellen verpassen.
- **Erkennung von Botnet-Kommunikation:** Die Netzwerküberwachung zielt gezielt auf Kommunikationsmuster von Botnet-Command-and-Control ab, einschließlich DNS-basiertem C2, HTTP-Beaconing und Erkennung verschlüsselter Tunnel.

## 8. Uhrensynchronisation (A 8.17)

Genaue und konsistente Zeit über alle Systeme hinweg ist wesentlich für Log-Korrelation, forensische Untersuchungen und die Beweiskraft. Die folgenden Regeln regeln die Uhrensynchronisation.

- **Referenzuhr:** Eine Referenzuhrquelle, die aus Funkzeitsignalen (DCF77, MSF) oder GPS abgeleitet wird, wird als maßgebliche Zeitquelle für alle Protokollierungs- und Zeitstempel-Operationen verwendet.
- **NTP- / PTP-Synchronisation:** Alle Systeme — Server, Netzwerkgeräte, Endgeräte und Anwendungen — synchronisieren ihre Uhren über NTP (Network Time Protocol) oder PTP (Precision Time Protocol) mit der definierten Referenzuhr. Die Zeitdrifttoleranz überschreitet eine Sekunde für Standardsysteme und eine Millisekunde für Systeme, die hochpräzise Zeitstempel benötigen, nicht.
- **Überwachung von Uhrenabweichungen:** Uhrenabweichungen zwischen Systemen, einschließlich Cloud-Diensten und On-Premises-Infrastruktur, werden überwacht und aufgezeichnet. Alarme werden generiert, wenn die Synchronisationsdrift die definierte Toleranz überschreitet.

## 9. Netzwerksicherheit (A 8.20)

Die Netzwerkarchitektur wird nach dem Prinzip des geringsten Privilegs in Sicherheitszonen (Management, Server, Client, DMZ, Gast, IoT) gestaltet, dokumentiert und gepflegt. Die Netzwerkdokumentation wird aktuell gehalten und spiegelt die tatsächliche Topologie wider. Firewall-Regeln folgen einem Deny-by-default-Ansatz, und die Netzwerküberwachung ist in das Sicherheitskonzept integriert.

### 9.1 Netzwerkdesign & Governance

- **Informationstyp & Klassifizierung:** Art, Sensibilität und Klassifizierung der Informationen, die jedes Netzwerk oder Netzwerksegment unterstützt, werden identifiziert und dokumentiert. Netzwerkmaßnahmen werden proportional zur Klassifizierungsstufe angewendet.
- **Verantwortlichkeiten & Verfahren:** Verantwortlichkeiten für das Netzwerksicherheitsmanagement und Verfahren für den Betrieb der Netzwerkinfrastruktur sind definiert, dokumentiert und qualifizierten Personen zugewiesen.
- **Netzwerkdokumentation & -diagramme:** Aktuelle, genaue Netzwerkdokumentation wird geführt, einschließlich Topologiediagrammen, IP-Adressplänen, Geräteinventaren und Verbindungspunkten. Die Dokumentation wird nach jeder Änderung aktualisiert.
- **Trennung operativer Verantwortlichkeit:** Wo machbar, wird die operative Verantwortung für Netzwerke von der Verantwortung für die Computersysteme, die diese Netzwerke nutzen, getrennt, um unabhängige Aufsicht zu gewährleisten.
- **Maßnahmen für öffentliche, Dritt- & drahtlose Netze:** Spezielle Maßnahmen werden angewendet, um Informationen zu schützen, die über öffentliche Netze, Verbindungen aus Drittnetzen und drahtlose Netze übertragen werden. Diese Maßnahmen umfassen Verschlüsselung, Authentifizierung, Zugriffsbeschränkungen und Überwachung.
- **Protokollierung & Überwachung:** Netzwerkaktivitäten werden protokolliert und überwacht, um Sicherheitsereignisse zu erkennen. Die Netzwerküberwachung ist in das übergreifende Sicherheitsüberwachungskonzept der Organisation integriert.
- **Koordination des Netzwerkmanagements:** Netzwerkmanagement-Aktivitäten werden organisationsweit koordiniert, um Service-Level zu optimieren, eine konsistente Durchsetzung von Sicherheitsrichtlinien sicherzustellen und widersprüchliche Konfigurationen zu vermeiden.

### 9.2 Netzwerkzugriff & Authentifizierung

- **Systemauthentifizierung:** Systeme im Netzwerk werden authentifiziert, bevor ihnen Netzwerkzugriff gewährt wird. Für kabelgebundene und drahtlose Verbindungen werden 802.1X-portbasierte Authentifizierung oder gleichwertige Mechanismen verwendet.
- **Verbindungsbeschränkung & -filterung:** Netzwerkverbindungen werden durch Firewalls mit Deny-by-default-Regeln beschränkt und gefiltert. Nur ausdrücklich autorisierter Verkehr ist erlaubt, und die Regeln werden mindestens halbjährlich überprüft.
- **Kontrolle von Geräteverbindungen:** Unbefugte Geräte werden erkannt und durch Network-Access-Control-Mechanismen (NAC) daran gehindert, sich mit dem Netzwerk zu verbinden. Nur registrierte und konforme Geräte sind zugelassen.

### 9.3 Netzwerkhärtung & -schutz

- **Härtung von Netzwerkgeräten:** Netzwerkgeräte (Router, Switches, Firewalls, Access Points) werden gehärtet, indem unnötige Dienste deaktiviert, Standardzugangsdaten geändert, aktuelle Firmware angewendet und sichere Managementprotokolle (SSH, SNMPv3) aktiviert werden.
- **Getrennte Administrationskanäle:** Netzwerkadministrationsverkehr wird durch dedizierte Management-VLANs oder Out-of-Band-Managementnetze vom Produktionsverkehr getrennt.
- **Isolation kritischer Subnetze:** Die Fähigkeit besteht, kritische Netzwerk-Subnetze während eines aktiven Angriffs vorübergehend zu isolieren, um die Bedrohung einzudämmen und gleichzeitig wesentliche Dienste auf nicht betroffenen Segmenten aufrechtzuerhalten.
- **Deaktivierung verwundbarer Protokolle:** Bekannte verwundbare Netzwerkprotokolle und Dienste werden deaktiviert oder durch sichere Alternativen ersetzt. Wenn ein verwundbares Protokoll betrieblich notwendig ist, werden kompensierende Maßnahmen (Netzsegmentierung, Verschlüsselung, Überwachung) angewendet.
- **Sicherheit virtualisierter Netze:** Auf virtualisierte Netze werden Sicherheitsmaßnahmen angewendet, die denen für physische Netze entsprechen, einschließlich Mikrosegmentierung, virtueller Firewalls und Verkehrsinspektion innerhalb virtualisierter Umgebungen.

## 10. Sicherheit von Netzwerkdiensten (A 8.21)

Sicherheitsmaßnahmen für Netzwerkdienste — einschließlich Managed Firewalls, Intrusion Detection, VPN-Dienste und private Netzwerkverbindungen — werden identifiziert, umgesetzt und überwacht. Die Fähigkeit von Netzwerkdienstleistern, vereinbarte Dienste sicher zu verwalten, wird regelmäßig bewertet und auditiert.

### 10.1 Governance des Dienstzugriffs

- **Zugängliche Netze & Dienste:** Die Netze und Netzwerkdienste, auf die Personen zugreifen dürfen, sind ausdrücklich definiert. Zugriffe über den definierten Umfang hinaus erfordern eine vorherige Genehmigung.
- **Authentifizierung pro Dienst:** Jeder Netzwerkdienst erfordert eine angemessene Authentifizierung — die Stärke der Authentifizierung ist proportional zur Sensibilität des Dienstes und der verarbeiteten Daten.
- **Autorisierungsverfahren:** Formale Autorisierungsverfahren regeln, welchen Nutzern und Systemen der Zugriff auf jeden Netzwerkdienst gestattet ist. Zugriffe werden auf Need-to-use-Basis gewährt und periodisch überprüft.
- **Managementverfahren & technische Maßnahmen:** Managementverfahren und technische Maßnahmen werden implementiert, um den Zugriff auf Netzwerkdienste zu schützen. Die Maßnahmen umfassen Zugriffsprotokollierung, Sitzungsmanagement und Anomalieerkennung.
- **Zugriffsmittel:** Die Mittel, die für den Zugriff auf Netzwerkdienste verwendet werden (VPN, drahtlos, direkte Verbindung), sind pro Dienst definiert. Der Fernzugriff auf interne Dienste erfolgt ausschließlich über genehmigte VPN-Verbindungen.
- **Zeit- & Ortsattribute:** Der Zugriff auf sensible Netzwerkdienste wird durch Tageszeit- und Herkunftsortattribute beschränkt, wo die Risikobewertung dies rechtfertigt.
- **Nutzungsüberwachung:** Die Nutzung von Netzwerkdiensten wird überwacht, um unbefugte Zugriffe, übermäßigen Verbrauch und anomale Muster zu erkennen. Überwachungsergebnisse fließen in den Sicherheitsüberwachungsprozess ein.

### 10.2 Technische Dienstsicherheit

- **Authentifizierungs- & Verschlüsselungstechnologie:** Netzwerkdienste verwenden aktuelle Authentifizierungs- und Verschlüsselungstechnologien (TLS 1.2+, IPsec, WPA3, 802.1X), die der Dienstklassifizierung angemessen sind.
- **Technische Verbindungsparameter:** Technische Parameter für eine sichere Verbindung zu Netzwerkdiensten — einschließlich Cipher Suites, Zertifikatsanforderungen, Protokollversionen und Sitzungs-Timeout-Werte — sind definiert und werden durchgesetzt.
- **Cache-Parameter:** Cache-Parameter für Netzwerkdienste (Proxy-Caches, Content Delivery, Sitzungs-Caches) werden so konfiguriert, dass unbefugte Datenhaltung verhindert wird und sensible Informationen nicht über den operativen Bedarf hinaus zwischengespeichert werden.
- **Verfahren zur Zugriffsbeschränkung:** Verfahren beschränken den Zugriff auf Netzwerkdienste und Anwendungen basierend auf Nutzeridentität, Geräte-Compliance-Status und Verbindungskontext. Access Control Lists auf Netzwerkebene ergänzen die Autorisierung auf Anwendungsebene.

## 11. Trennung von Netzwerken (A 8.22)

Große Netze werden in getrennte Netzwerkdomänen unterteilt und vom öffentlichen Netz getrennt. Die Trennung basiert auf den Sicherheitsanforderungen jeder Domäne, der Informationsklassifizierung und dem Vertrauensniveau verbundener Systeme.

### 11.1 Trennung kabelgebundener Domänen

- **Perimeterdefinition:** Der Netzwerkperimeter für jede Domäne (Management, Server, Client, DMZ, Gast, IoT/OT) ist definiert, dokumentiert und wird durch physische oder logische Trennung durchgesetzt.
- **Gateway-kontrollierter Zugriff:** Der Zugriff zwischen Netzwerkdomänen wird durch Gateways (Firewalls, Proxy-Server, filternde Router) kontrolliert, die Verkehrsrichtlinien auf Basis definierter Regeln durchsetzen. Direkte domänenübergreifende Kommunikation unter Umgehung des Gateways ist blockiert.
- **Sicherheitsbasierte Trennung:** Die Trennungskriterien basieren auf den Sicherheitsanforderungen, der Klassifizierungsstufe und dem Vertrauensniveau der Systeme und Informationen in jeder Domäne. Domänen mit höherer Sicherheit haben strengere Ein- und Ausgangskontrollen.

### 11.2 Trennung drahtloser Netze

- **Anpassung der Funkabdeckung:** Die Funkabdeckung drahtloser Netze wird so angepasst, dass Signalaustritt über den physischen Perimeter der Organisation hinaus minimiert wird, wodurch das Risiko unbefugten Abfangens oder Verbindens reduziert wird.
- **Drahtlos als extern:** Der gesamte drahtlose Netzwerkverkehr wird als extern (nicht vertrauenswürdig) behandelt, bis das Gerät sich über ein Sicherheitsgateway mit 802.1X oder gleichwertiger Enterprise-Authentifizierung authentifiziert hat.
- **Trennung des Gastnetzes:** Drahtlose Gastnetze sind vollständig vom internen Personalnetz getrennt. Gastverkehr wird ohne Zugriff auf interne Ressourcen direkt ins Internet geleitet.

## 12. Webfilterung (A 8.23)

Der Zugriff auf externe Websites wird gesteuert, um die Exposition gegenüber bösartigen Inhalten zu reduzieren und den Zugriff auf unbefugte Online-Ressourcen zu verhindern. Webfilter-Regeln werden am Netzwerkperimeter und, wo anwendbar, auf Endgeräten durchgesetzt.

### 12.1 Gesperrte Kategorien

- **Upload-Sites:** Der Zugriff auf externe Datei-Upload- und Dateifreigabe-Sites ist gesperrt, sofern keine dokumentierte geschäftliche Begründung genehmigt wurde. Genehmigte Ausnahmen werden halbjährlich überprüft.
- **Bekannte bösartige Sites:** Websites, die als Hosts für Malware, Phishing-Inhalte oder Exploit-Kits identifiziert wurden, werden durch regelmäßig aktualisierte URL-Kategorisierungsdatenbanken und Threat-Intelligence-Feeds gesperrt.
- **Command-and-Control-Server:** Kommunikation mit bekannten oder vermuteten Command-and-Control-Servern (C2) wird am Netzwerkperimeter blockiert. C2-Indikatoren werden aus Threat-Intelligence-Feeds aktualisiert.
- **Threat-Intelligence-Sites:** Durch Threat-Intelligence-Sharing (ISACs, CERT-Advisories, kommerzielle Feeds) als bösartig identifizierte Sites werden innerhalb von 24 Stunden nach Benachrichtigung zur Blockliste hinzugefügt.
- **Illegale Inhalte:** Der Zugriff auf Websites, die illegale Inhalte (gemäß geltendem Recht) teilen, wird blockiert.

### 12.2 Nutzungssteuerung

- **Regeln zur Nutzung von Online-Ressourcen:** Regeln für die sichere und angemessene Nutzung von Online-Ressourcen sind in der Richtlinie zur akzeptablen Nutzung definiert. Diese Regeln legen fest, welche Website-Kategorien für geschäftliche Zwecke zulässig sind und welche eingeschränkt oder gesperrt sind.
- **Personalschulung:** Beschäftigte werden in der sicheren Nutzung von Online-Ressourcen geschult, einschließlich des Erkennens von Phishing-Sites, des Vermeidens von Drive-by-Downloads und des Meldens verdächtiger URLs. Schulungen werden beim Onboarding durchgeführt und jährlich aufgefrischt.

## 13. Rollen & Verantwortlichkeiten

- **Geschäftsleitung:** Genehmigt diese Richtlinie, stellt Ressourcen für die IT-Betriebssicherheitsinfrastruktur bereit und stellt die Abstimmung mit Geschäftszielen und rechtlichen Anforderungen sicher.
- **Informationssicherheitsbeauftragte/r (ISB):** Pflegt diese Richtlinie, definiert Überwachungs- und Protokollierungsanforderungen, überprüft die Wirksamkeit des Schwachstellenmanagements, beaufsichtigt die Netzwerksicherheitsarchitektur und koordiniert die Vorfalleskalation aus Überwachungs- und Detektionssystemen.
- **IT-Betrieb / Systemadministratoren:** Setzen die in dieser Richtlinie definierten Maßnahmen um und betreiben sie. Verwalten Patching, Sicherungsausführung, Log-Sammlung, Überwachungswerkzeuge, Netzwerkgeräte und Redundanzinfrastruktur. Reagieren auf Alarme und führen Behebungsverfahren aus.
- **Netzwerkadministratoren:** Entwerfen, implementieren und pflegen die Netzwerkarchitektur, Firewall-Regeln, Netzsegmentierung und Zugriffskontrollen gemäß dieser Richtlinie. Halten die Netzwerkdokumentation aktuell.
- **System- & Anwendungseigentümer:** Stellen sicher, dass ihre Systeme den Sicherungsplänen, Protokollierungsanforderungen und Fristen für die Schwachstellenbehebung entsprechen. Melden Abweichungen an den IT-Betrieb.
- **Alle Beschäftigten:** Nutzen IT-Ressourcen in Übereinstimmung mit der Richtlinie zur akzeptablen Nutzung. Melden vermutete Schwachstellen, Sicherheitsvorfälle und anomales Systemverhalten an den IT-Helpdesk oder die/den Informationssicherheitsbeauftragte/n.

## 14. Überprüfung & Pflege

Diese Richtlinie wird überprüft:

- Mindestens jährlich im Rahmen des ISMS-Managementbewertungszyklus.
- Nach wesentlichen Sicherheitsvorfällen, die den IT-Betrieb betreffen (z. B. erfolgreiche Ausnutzung einer Schwachstelle, Sicherungsausfall bei der Wiederherstellung, Netzwerkdurchbruch).
- Wenn sich die Bedrohungslage wesentlich ändert (z. B. neue Klassen von Schwachstellen, aufkommende Angriffstechniken, Änderungen in Threat Intelligence).
- Nach wesentlichen Änderungen der IT-Infrastruktur, der Netzwerkarchitektur, der Dienstleister oder Geschäftsprozesse.
- Wenn neue rechtliche, regulatorische oder vertragliche Anforderungen an die IT-Betriebssicherheit identifiziert werden.

Betriebsdokumentation wird nach Änderungen, die über den Change-Management-Prozess der Security Operations gesteuert werden, aktualisiert, um sicherzustellen, dass Verfahren, Runbooks und Systembeschreibungen den aktuellen Zustand der IT-Umgebung widerspiegeln.
