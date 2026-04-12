# Richtlinie zu Konfigurations- und Änderungsmanagement

> **Dokumentenkontrolle**  
> Eigentümer: [RICHTLINIEN_EIGENTÜMER_ROLLE, z. B. Informationssicherheitsbeauftragte/r]  
> Genehmigt von: [GENEHMIGER_NAME_UND_ROLLE]  
> Version: [VERSION]  
> Gültig ab: [GÜLTIGKEITSDATUM]  
> Nächste Überprüfung: [NÄCHSTES_ÜBERPRÜFUNGSDATUM]

## 1. Rechtliche/Regulatorische Grundlage

ISO/IEC 27001:2022 / ISO/IEC 27002:2022, Anhang A — Technologische Maßnahmen:

- A 8.9 — Konfigurationsmanagement
- A 8.32 — Änderungsmanagement

BSI IT-Grundschutz:

- OPS.1.1.1.A5 (Festlegung gehärteter Standardkonfigurationen)
- OPS.1.1.1.A7 (Sicherstellung eines ordnungsgemäßen IT-Betriebs)
- OPS.1.1.1.A8 (Regelmäßiger Soll-Ist-Vergleich)
- OPS.1.1.2.A11 (Dokumentation von IT-Administrationstätigkeiten)
- OPS.1.1.2.A26 (Konfigurationssicherung)
- APP.6.A4 (Regelungen für die Installation und Konfiguration von Software)
- OPS.1.1.3.A1 (Konzept für das Patch- und Änderungsmanagement)
- OPS.1.1.3.A2 (Festlegung von Verantwortlichkeiten)
- OPS.1.1.3.A5 (Umgang mit Änderungsanforderungen)
- OPS.1.1.3.A6 (Abstimmung von Änderungsanforderungen)
- OPS.1.1.3.A7 (Integration des Änderungsmanagements in die Geschäftsprozesse)
- OPS.1.1.3.A10 (Sicherstellung der Integrität und Authentizität von Softwarepaketen)
- OPS.1.1.3.A11 (Kontinuierliche Dokumentation der Informationsverarbeitung)

Weitere jurisdiktionsspezifische Gesetze und Vorschriften sind im Rechtsregister aufgeführt und werden durch Verweis einbezogen.

## 2. Zweck & Geltungsbereich

Diese Richtlinie legt Regeln für die Verwaltung der Sicherheitskonfigurationen von Hardware, Software, Diensten und Netzwerken sowie für die Steuerung von Änderungen an informationsverarbeitenden Einrichtungen und Informationssystemen bei **[IHR_ORGANISATIONSNAME]** fest. Sie stellt sicher, dass IT-Komponenten während ihres gesamten Lebenszyklus mit den erforderlichen Sicherheitseinstellungen betrieben werden und dass Änderungen kontrolliert, dokumentiert und unter Wahrung der Informationssicherheit umgesetzt werden.

Die Richtlinie gilt für alle IT-Systeme, Anwendungen, Dienste, Netzwerke und Infrastrukturkomponenten, die von oder im Auftrag der Organisation betrieben werden, einschließlich Cloud-gehosteter Umgebungen. Sie umfasst alle Personen und Dritten, die diese Komponenten konfigurieren, administrieren, ändern oder warten.

Konfigurations- und Änderungsmanagement sind komplementäre Disziplinen: Das Konfigurationsmanagement definiert und setzt den sicheren Basiszustand von IT-Komponenten durch, während das Änderungsmanagement sicherstellt, dass jede Abweichung vom oder Aktualisierung dieses Basiszustands geplant, genehmigt, getestet und dokumentiert wird. Gemeinsam adressieren sie eine grundlegende Ursache von Sicherheitsausfällen — unkontrollierte Konfigurationen und nicht verwaltete Änderungen.

## 3. Sichere Konfigurationsverwaltung (A 8.9)

Konfigurationen — einschließlich Sicherheitskonfigurationen — für Hardware, Software, Dienste und Netzwerke werden eingerichtet, dokumentiert, umgesetzt, überwacht und überprüft. IT-Komponenten werden kategorisiert und für jede Kategorie wird eine gehärtete Standardkonfiguration definiert. Diese Templates setzen die Sicherheitsanforderungen der Organisation um und berücksichtigen Herstellerempfehlungen sowie öffentlich verfügbare Sicherheitsleitfäden. Software wird mit minimal erforderlicher Funktionalität und minimal notwendigen Berechtigungen installiert, wobei datensparsame Datenschutzeinstellungen standardmäßig angewendet werden. Alle Konfigurationsdaten werden vor unbefugtem Zugriff geschützt und ihre Integrität bleibt gewahrt.

### 3.1 Gehärtete Standardtemplates

- **Öffentlich verfügbare Leitfäden:** Gehärtete Standardtemplates werden unter Verwendung öffentlich verfügbarer Leitfäden entwickelt, einschließlich Hersteller-Sicherheits-Baselines, Empfehlungen anerkannter Sicherheitsorganisationen (z. B. BSI IT-Grundschutz, CIS Benchmarks, DISA STIGs) und branchenüblicher Best Practices. Die Quellenverweise für jedes Template werden daneben dokumentiert.
- **Bestimmung des Schutzniveaus:** Das erforderliche Sicherheitsniveau für jedes Konfigurationstemplate wird durch den Schutzbedarf der IT-Komponentenkategorie bestimmt — speziell durch die Anforderungen an Vertraulichkeit, Integrität und Verfügbarkeit der verarbeiteten Daten und bereitgestellten Dienste. Höhere Schutzbedarfe führen zu strengeren Konfigurations-Baselines.
- **Ausrichtung an Richtlinien:** Jedes Konfigurationstemplate ist mit der Informationssicherheitsrichtlinie der Organisation, themenspezifischen Richtlinien, geltenden Standards und sonstigen Sicherheitsanforderungen abgestimmt. Templates werden vor der Bereitstellung auf Konsistenz mit der Zugriffskontroll-Richtlinie, dem Datenklassifizierungsschema und geltenden Compliance-Verpflichtungen überprüft.
- **Machbarkeit & Anwendbarkeit:** Bevor ein Konfigurationstemplate finalisiert wird, werden seine Machbarkeit und Anwendbarkeit im spezifischen operativen Kontext der Organisation bewertet. Wo eine Sicherheitsanforderung aus einer Referenz-Baseline nicht ohne Funktionsbeeinträchtigung oder unverhältnismäßige operative Auswirkungen umgesetzt werden kann, wird eine kompensierende Maßnahme dokumentiert und genehmigt.

Jedes Konfigurationstemplate ist versionskontrolliert, eindeutig identifizierbar und an einem sicheren, zugriffskontrollierten Ort gespeichert. Templates werden in einer isolierten Umgebung getestet, bevor sie auf Produktionssysteme ausgerollt werden. Sicherheitsupdates für Software werden angewendet, bevor Komponenten in den Produktivbetrieb gehen.

### 3.2 Identitäts- und Zugriffshärtung

- **Minimierung privilegierter Identitäten:** Die Anzahl der Identitäten mit privilegierten oder administratorischen Zugriffsrechten auf eine IT-Komponente wird minimiert. Gemeinsam genutzte oder generische Administrationskonten werden vermieden; wo technisch unvermeidbar, wird deren Nutzung strikt kontrolliert und jede Aktion ist einer Einzelperson zurechenbar. Die Rollentrennung zwischen administrativen und normalen operativen Funktionen wird durch getrennte Konten durchgesetzt.
- **Deaktivierung unnötiger Identitäten:** Unnötige, ungenutzte oder unsichere vorinstallierte Konten und Identitäten (z. B. Gastkonten, anonyme Zugriffskonten, nicht mehr benötigte Hersteller-Servicekonten) werden als Teil des initialen Härtungsprozesses und fortlaufend deaktiviert oder entfernt. Wenn Personen die Organisation verlassen oder Rollen wechseln, werden die zugehörigen Identitäten umgehend überprüft und deaktiviert.

### 3.3 Dienst- und Funktionsminimierung

- **Deaktivierung unnötiger Funktionen & Dienste:** Nur Dienste, Protokolle, Funktionen und Features, die für den operativen Zweck einer IT-Komponente erforderlich sind, werden aktiviert. Unnötige Funktionen — einschließlich nicht genutzter Netzwerkdienste, Demo- oder Beispielanwendungen, ungenutzter Skript-Engines und überflüssiger Betriebssystemkomponenten — werden deaktiviert oder deinstalliert. Software wird mit dem minimal erforderlichen Funktionsumfang installiert.
- **Einschränkung des Zugriffs auf Dienstprogramme & Host-Parameter:** Der Zugriff auf mächtige Dienstprogramme (z. B. Shell-Interpreter, Registry-Editoren, Diagnosewerkzeuge, Bootloader-Konfigurationsschnittstellen) und Host-Parameter-Einstellungen ist auf autorisierte Administratoren beschränkt. Wo möglich, wird der Zugriff über rollenbasierte Berechtigungen gesteuert, und die Nutzung solcher Programme wird protokolliert.

### 3.4 System-Basiskonfiguration

- **Zeitsynchronisation:** Uhren aller IT-Komponenten werden über NTP oder ein gleichwertiges Protokoll mit einer autoritativen Zeitquelle synchronisiert. Genaue und konsistente Zeitstempel über Systeme hinweg sind erforderlich für Log-Korrelation, Vorfalluntersuchung, Zertifikatsvalidierung und Audit-Nachweise.
- **Hersteller-Standard-Authentisierungsinformationen:** Hersteller-voreingestellte Passwörter, Authentisierungstoken, Zertifikate und andere Standard-Authentisierungsinformationen werden unmittelbar nach der initialen Installation geändert, bevor ein System an das Produktionsnetzwerk angeschlossen wird. Andere wichtige sicherheitsrelevante Standardparameter (z. B. Standard-Community-Strings, Standard-API-Schlüssel, Standard-Verschlüsselungseinstellungen) werden im Rahmen des initialen Konfigurationsprozesses überprüft und aktualisiert.
- **Automatisches Session-Timeout:** Auf allen interaktiven Rechengeräten und -sitzungen werden Timeout-Funktionen konfiguriert, die das Gerät nach einer definierten Inaktivitätsdauer automatisch abmelden oder sperren. Der Inaktivitätsschwellenwert wird entsprechend der Sensibilität des Systems und der über die Sitzung zugänglichen Daten festgelegt.

### 3.5 Lizenzprüfung

- **Lizenz-Compliance:** Konfigurationstemplates und Deployment-Prozesse enthalten einen Prüfschritt, der bestätigt, dass Lizenzanforderungen für alle Softwarekomponenten vor der Installation erfüllt sind. Das Software-Lizenzregister (siehe *Richtlinie zum Schutz geistigen Eigentums*) wird konsultiert, um zu bestätigen, dass die Anzahl der Installationen die lizenzierten Berechtigungen nicht überschreitet und dass Lizenzbedingungen in der Deployment-Konfiguration eingehalten werden.

### 3.6 Überprüfung & Aktualisierung von Templates

- **Periodische Template-Überprüfung & Aktualisierung:** Alle gehärteten Standardkonfigurationstemplates werden regelmäßig überprüft und aktualisiert, wenn neue Bedrohungen oder Schwachstellen identifiziert werden, die die entsprechende Komponentenkategorie betreffen, wenn neue Software- oder Hardwareversionen sicherheitsrelevante Änderungen einführen oder wenn Hersteller-Sicherheitsleitfäden aktualisiert werden. Nach jeder Überprüfung werden aktualisierte Templates versioniert, getestet und erneut auf betroffene Systeme ausgerollt.

## 4. Konfigurationsaufzeichnungen & Überwachung (A 8.9)

Konfigurationsaufzeichnungen für alle IT-Komponenten werden in einer Configuration Management Database (CMDB) oder einem gleichwertigen Inventarsystem geführt. Die CMDB ist die maßgebliche Quelle für den Konfigurationszustand und unterstützt sowohl das operative Management als auch die Sicherheitsüberwachung. Der Zugriff auf Konfigurationsaufzeichnungen ist auf autorisiertes IT-Betriebspersonal beschränkt.

### 4.1 Konfigurationsaufzeichnungen

- **Eigentümer- & Kontaktinformationen:** Jede Konfigurationsaufzeichnung enthält den aktuellen Eigentümer oder die benannte Kontaktstelle für das Asset — die Person, die für die Sicherheitskonfiguration der IT-Komponente verantwortlich ist und Konfigurationsänderungen genehmigt.
- **Datum der letzten Konfigurationsänderung:** Datum und Art der jüngsten Konfigurationsänderung werden für jedes Asset erfasst, damit der IT-Betrieb Komponenten identifizieren kann, die nicht innerhalb der erwarteten Wartungszyklen aktualisiert wurden, und um Konfigurationsänderungen mit Vorfall-Zeitlinien zu korrelieren.
- **Version des Konfigurationstemplates:** Die Version des auf jedes Asset angewendeten gehärteten Standardkonfigurationstemplates wird erfasst. Dies ermöglicht die schnelle Identifizierung von Komponenten, die nicht das aktuelle genehmigte Template verwenden, und erleichtert eine gezielte Behebung nach einem Template-Update.
- **Abhängigkeitsbeziehungen:** Konfigurationsaufzeichnungen erfassen Beziehungen und Abhängigkeiten zwischen Assets — zum Beispiel, welche Server von einer gemeinsamen Datenbankkonfiguration abhängen, welche Anwendungen auf eine bestimmte Middleware-Version angewiesen sind und welche Netzwerkgeräte die Zugriffskontrolle für ein bestimmtes Serversegment durchsetzen. Diese Abhängigkeitszuordnungen werden in Auswirkungsbewertungen für Konfigurationsänderungen verwendet.

### 4.2 Überwachungsumfang

- **Wartungsdienstprogramme:** Wartungswerkzeuge mit Zugriff auf Systemkonfigurationen (z. B. Software-Deployment-Agents, Patch-Management-Clients, Firmware-Update-Utilities) werden in den Konfigurationsüberwachungsumfang aufgenommen. Ihre eigene Konfiguration unterliegt denselben Härtungs- und Überprüfungsanforderungen wie die von ihnen verwalteten Systeme.
- **Remote-Support-Werkzeuge:** Remote-Support- und Remote-Administrationswerkzeuge (z. B. VPN-Gateways, Jump-Server, Remote-Desktop-Dienste, Out-of-Band-Management-Schnittstellen) werden in die Konfigurationsüberwachung einbezogen. Zugriffe über diese Werkzeuge werden protokolliert, und die Konfigurationen der Remote-Support-Infrastruktur werden gemäß denselben gehärteten Templates wie andere Produktionskomponenten gepflegt.
- **Enterprise-Management-Werkzeuge:** Enterprise-IT-Management-Plattformen (z. B. Configuration Management Databases, IT-Service-Management-Systeme, Monitoring-Plattformen, Identitätsmanagementsysteme) werden in die Konfigurationsüberwachung einbezogen. Aufgrund ihres privilegierten Zugriffs auf die verwaltete Infrastruktur unterliegen diese Systeme verschärften Härtungsanforderungen und regelmäßigen Konfigurationsüberprüfungen.
- **Backup- & Restore-Software:** Backup- und Restore-Softwarekonfigurationen werden in den Überwachungsumfang aufgenommen. Konfigurationssicherungen werden sowohl auf Anwendungs- als auch auf Systemebene nach einem regelmäßigen Zeitplan durchgeführt. Eine zusätzliche Konfigurationssicherung wird vor jeder IT-Administrationsaktivität mit potenziell weitreichenden Auswirkungen erstellt. Die Wiederherstellbarkeit von Konfigurationssicherungen wird regelmäßig verifiziert, um zu bestätigen, dass bei Bedarf ein sauberer Konfigurationszustand wiederhergestellt werden kann.

### 4.3 Soll-Ist-Vergleich

Ein regelmäßiger Soll-Ist-Vergleich wird für alle IT-Komponenten im Geltungsbereich durchgeführt — vergleicht die aktuelle Konfiguration jeder Komponente mit ihrem definierten gehärteten Standardtemplate. Dieser Vergleich wird wo technisch machbar mit automatisierten Konfigurations-Compliance-Scan-Werkzeugen durchgeführt, die strukturierte Abweichungsberichte erzeugen. Wo Automatisierung nicht möglich ist, werden manuelle Konfigurationsaudits nach einem definierten Zeitplan durchgeführt. Identifizierte Abweichungen werden auf Sicherheitsauswirkungen bewertet, klassifiziert und innerhalb ihrem Risiko angemessener Fristen behoben. Alle Abweichungen und ihr Behebungsstatus werden in der CMDB nachverfolgt. Automatisierung der Konfigurationsdurchsetzung (Infrastructure-as-Code, Desired-State-Configuration-Management) wird eingesetzt, wo betriebliche Bedingungen es zulassen, um das Zeitfenster zwischen Erkennung und Behebung von Konfigurationsabweichungen zu verkürzen.

## 5. Änderungsmanagement (A 8.32)

Alle Änderungen an informationsverarbeitenden Einrichtungen und Informationssystemen — einschließlich Hardwareersatz, Softwareinstallationen und -aktualisierungen, Konfigurationsänderungen, Netzwerkänderungen und Änderungen an IKT-Diensten — unterliegen einem formalen Änderungsmanagementprozess. Dieser Prozess umfasst Dokumentation, Spezifikation, Test, Qualitätskontrolle und gesteuerte Umsetzung. Unzureichende Änderungskontrolle ist eine anerkannte häufige Ursache von System- und Sicherheitsausfällen; diese Richtlinie stellt sicher, dass jede Änderung vor dem Produktiv-Deployment geplant, genehmigt, getestet und aufgezeichnet wird. Der Änderungsmanagementprozess integriert IKT-Infrastruktur- und Softwareänderungen und gilt für Produktionsumgebungen einschließlich Betriebssysteme, Datenbanken, Middleware und Anwendungssoftware. Softwarepakete werden ausschließlich von vertrauenswürdigen Lieferanten bezogen, und ihre Integrität wird vor der Installation über Prüfsummen oder digitale Signaturen verifiziert. Änderungen werden in einer getrennten Testumgebung getestet, bevor sie in Produktion gehen.

### 5.1 Änderungsplanung & Auswirkungsanalyse

- **Planung & Auswirkungsanalyse:** Jede Änderungsanforderung enthält eine dokumentierte Auswirkungsanalyse, die sicherheitsrelevante Implikationen, operative Abhängigkeiten und potenzielle Auswirkungen auf andere Systeme und Dienste umfasst. Die in den Konfigurationsaufzeichnungen (Abschnitt 4.1) erfassten Abhängigkeitsbeziehungen fließen in diese Analyse ein. Alle betroffenen Systeme, Dienste und Stakeholder-Gruppen werden vor Einholung der Genehmigung identifiziert. Wo eine Änderung Informationssicherheitsmaßnahmen oder IKT-Kontinuitätsvorkehrungen betreffen könnte, wird die/der Informationssicherheitsbeauftragte als Teil der Analyse konsultiert.

### 5.2 Genehmigung

- **Genehmigung von Änderungen:** Jede Änderung erfordert vor der Umsetzung eine ausdrückliche Genehmigung. Genehmigungsebenen sind nach Änderungskategorie und potenzieller Auswirkung definiert: Routine-Änderungen mit geringem Risiko werden durch die verantwortliche IT-Betriebs-Teamleitung genehmigt, wesentliche Änderungen mit breiterer Auswirkung erfordern die Genehmigung durch die/den Informationssicherheitsbeauftragte/n und den relevanten Asset-Eigentümer, und Großänderungen an Kerninfrastruktur oder organisationsübergreifenden Geschäftsprozessen erfordern Genehmigung auf Managementebene. Nicht genehmigte Änderungen werden als Sicherheitsvorfälle behandelt. Bei Großänderungen wird die/der ISB in die Genehmigungsentscheidung einbezogen.

### 5.3 Kommunikation

- **Kommunikation an interessierte Parteien:** Genehmigte Änderungen werden allen relevanten interessierten Parteien vor der Umsetzung kommuniziert. Dies umfasst betroffene Geschäftseinheiten, IT-Betriebsteams, Systemeigentümer und — wo die Änderung extern sichtbare Dienste betrifft — relevante externe Stakeholder. Bei Änderungen mit breiten Auswirkungen wird ein Änderungskalender oder ein geplantes Wartungsfenster im Voraus veröffentlicht. Der Abstimmungsprozess berücksichtigt Informationssicherheitsauswirkungen auf alle Zielgruppen und schließt einen definierten Eskalationspfad für Prioritätsentscheidungen ein.

### 5.4 Test & Abnahme

- **Test & Abnahme:** Alle Änderungen werden vor der Produktionsbereitstellung in einer getrennten Testumgebung getestet, die die Produktionskonfiguration so genau wie praktisch möglich nachbildet. Abnahmekriterien werden als Teil des Änderungsplans definiert und sind vor dem Übergang der Änderung in die Produktion nachweislich erfüllt. Die Abnahme wird formal mit Name der verantwortlichen Person, Datum und Ergebnis protokolliert. Prüfsummen oder digitale Signaturen von Softwarepaketen werden vor der Installation verifiziert.

### 5.5 Umsetzung & Deployment

- **Umsetzungs- & Deployment-Pläne:** Änderungen werden gemäß einem dokumentierten Deployment-Plan umgesetzt, der die Abfolge der Schritte, die verantwortlichen Personen, das Umsetzungsfenster, die betroffenen Konfigurationselemente und die Post-Implementation-Verifikationsschritte spezifiziert. Die Umsetzung erfolgt mit den autorisierten Konfigurationsmanagement-Werkzeugen. Konfigurationsaufzeichnungen in der CMDB werden unmittelbar nach erfolgreichem Deployment aktualisiert, um den neuen Zustand widerzuspiegeln. Alle während der Umsetzung durchgeführten administrativen Tätigkeiten werden dokumentiert, mit Angabe was geändert wurde, wann, wer die Änderung vorgenommen hat und die Grundlage oder Begründung der Änderung.

### 5.6 Notfall- & Rollback-Verfahren

- **Notfall- & Rollback-Verfahren:** Jeder Änderungsplan enthält dokumentierte Fallback- und Rollback-Verfahren, die beschreiben, wie der vorherige Konfigurationszustand wiederhergestellt werden kann, wenn die Änderung fehlschlägt, unerwartete Probleme verursacht oder rückgängig gemacht werden muss. Eine Konfigurationssicherung wird vor jeder Änderung mit potenziell weitreichenden Konsequenzen erstellt. Rollback-Verfahren werden wo machbar in der Testphase getestet. Für Notfalländerungen — erforderlich zur Reaktion auf kritische Sicherheitsvorfälle oder drohende Systemausfälle — ist ein beschleunigtes Genehmigungsverfahren definiert, das die Zurechenbarkeit aufrechterhält und gleichzeitig eine schnelle Reaktion ermöglicht. Notfalländerungen unterliegen denselben Dokumentations- und Nachbetrachtungsanforderungen wie Standardänderungen.

### 5.7 Änderungsaufzeichnungen

- **Änderungsaufzeichnungen:** Für jede Änderung wird ein vollständiges Protokoll geführt, das Folgendes umfasst: die Änderungsanforderung und ihre Auswirkungsanalyse, die Genehmigungsentscheidung mit Datum und genehmigender Person, die versandte Kommunikation, Testergebnisse und Abnahmenachweise, Umsetzungsdetails einschließlich Deployment-Plan, Rollback-Verfahren und aller aufgetretenen Abweichungen sowie das Ergebnis der Nachverifizierung. Änderungsaufzeichnungen werden in einem manipulationsnachweisfähigen System gespeichert und gemäß dem Aufbewahrungsplan der Organisation aufbewahrt. Änderungen werden über alle Phasen, Anwendungen und Systeme hinweg dokumentiert.

### 5.8 Dokumentationsaktualisierungen

- **Betriebsdokumentation & Nutzerverfahren:** Wenn eine Änderung den Betrieb eines Systems oder Dienstes betrifft, werden die relevante Betriebsdokumentation und Nutzerverfahren vor oder unmittelbar nach dem Deployment der Änderung aktualisiert (siehe auch *Richtlinie zur IT-Betriebssicherheit*). Veraltete Dokumentation wird ersetzt und archiviert statt gelöscht, um die Änderungshistorie zu bewahren.
- **IKT-Kontinuitätspläne & Wiederherstellungsverfahren:** Wenn eine Änderung Systeme oder Dienste betrifft, die von IKT-Kontinuitätsplänen oder Vorfallreaktions- und Wiederherstellungsverfahren abgedeckt sind, werden diese Pläne vor Abschluss der Änderung überprüft und aktualisiert, um die geänderte Umgebung widerzuspiegeln. Die Änderungsaufzeichnung erfasst, ob Kontinuitätspläne überprüft wurden und welche Aktualisierungen vorgenommen wurden.

## 6. Rollen & Verantwortlichkeiten

- **Geschäftsleitung:** Genehmigt diese Richtlinie, stellt Ressourcen für Konfigurationsmanagement-Werkzeuge und Änderungsmanagementprozesse bereit und entscheidet über Prioritätseskalationen für Änderungen, die Kerngeschäftsprozesse betreffen.
- **Informationssicherheitsbeauftragte/r (ISB):** Pflegt diese Richtlinie, überprüft und genehmigt gehärtete Standardkonfigurationstemplates auf Sicherheitsangemessenheit, wird bei allen Änderungen mit erheblichen Sicherheitsauswirkungen konsultiert und in die Genehmigungsentscheidung bei Großänderungen einbezogen.
- **IT-Betrieb:** Entwickelt, pflegt und rollt gehärtete Standardkonfigurationstemplates aus; betreibt die CMDB; führt Soll-Ist-Vergleiche und Behebungen durch; setzt genehmigte Änderungen gemäß Deployment-Plänen um; dokumentiert alle administrativen Tätigkeiten; erstellt Konfigurationssicherungen vor Änderungen mit hoher Auswirkung. Verantwortlichkeiten für Patch- und Änderungsmanagement sind für alle Organisationseinheiten definiert.
- **Asset-/Systemeigentümer:** Definieren Schutzbedarf und Betriebsanforderungen ihrer Assets, genehmigen Konfigurationstemplates für ihre Systeme, genehmigen Änderungen innerhalb ihrer delegierten Befugnis und stellen sicher, dass Betriebsdokumentation und Kontinuitätspläne für ihre Systeme nach Änderungen aktuell gehalten werden.
- **Change Advisory Board (oder gleichwertige Funktion):** Überprüft und koordiniert wesentliche Änderungsanträge, berücksichtigt Informationssicherheitsauswirkungen auf alle Zielgruppen und gibt Empfehlungen zur Genehmigung und Terminierung. Moderiert den Eskalationspfad an die Geschäftsleitung für Prioritätsentscheidungen.
- **Alle Beschäftigten:** Halten autorisierte Konfigurationseinstellungen ein und melden beobachtete unbefugte Änderungen oder Abweichungen vom erwarteten Systemverhalten an den IT-Betrieb oder die/den Informationssicherheitsbeauftragte/n.

## 7. Überprüfung & Pflege

Diese Richtlinie und die zugehörigen Konfigurationsmanagementverfahren werden überprüft:

- Mindestens jährlich, um die Ausrichtung an der aktuellen IT-Infrastruktur, der Bedrohungslandschaft und regulatorischen Anforderungen zu verifizieren.
- Wenn wesentliche Änderungen an der IT-Architektur, den Geschäftsprozessen oder dem Risikoprofil der Organisation eintreten.
- Nach einem Sicherheitsvorfall, der auf eine Konfigurationsschwäche oder eine nicht genehmigte Änderung zurückzuführen ist.
- Wenn neue IT-Komponentenkategorien eingeführt werden, die neue gehärtete Standardkonfigurationstemplates erfordern.
- Wenn aktualisierte Hersteller-Sicherheitsleitfäden, BSI-IT-Grundschutz-Anforderungen oder relevante externe Standards (z. B. CIS Benchmarks) veröffentlicht werden, die den Inhalt ausgerollter Templates betreffen.

Die Aktualität der Konfigurationstemplates wird fortlaufend gepflegt: Jedes Template wird überprüft, wenn eine neue Software- oder Hardwareversion sicherheitsrelevante Änderungen einführt, und mindestens jährlich als Teil des Gesamtüberprüfungszyklus der Richtlinie. Die CMDB und die darin enthaltenen Änderungsaufzeichnungen werden durchgehend als lebendige Dokumentation gepflegt.
