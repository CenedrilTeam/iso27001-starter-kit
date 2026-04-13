# Richtlinie zur sicheren Softwareentwicklung

> **Dokumentenkontrolle**  
> Eigentümer: [RICHTLINIEN_EIGENTÜMER_ROLLE, z. B. Informationssicherheitsbeauftragte/r]  
> Genehmigt von: [GENEHMIGER_NAME_UND_ROLLE]  
> Version: [VERSION]  
> Gültig ab: [GÜLTIGKEITSDATUM]  
> Nächste Überprüfung: [NÄCHSTES_ÜBERPRÜFUNGSDATUM]

## 1. Rechtliche/Regulatorische Grundlage

ISO/IEC 27001:2022 / ISO/IEC 27002:2022, Anhang A — Technologische Maßnahmen:

- A 8.25 — Sicherer Entwicklungslebenszyklus
- A 8.26 — Anforderungen an die Anwendungssicherheit
- A 8.27 — Grundsätze sicherer Systemarchitektur und -entwicklung
- A 8.28 — Sichere Programmierung
- A 8.29 — Sicherheitstests in Entwicklung und Abnahme
- A 8.30 — Ausgelagerte Entwicklung
- A 8.31 — Trennung von Entwicklungs-, Test- und Produktionsumgebungen
- A 8.33 — Testinformationen
- A 8.34 — Schutz von Informationssystemen bei Audittests

BSI IT-Grundschutz:

- CON.8 (Softwareentwicklung)
- CON.10 (Entwicklung von Webanwendungen)
- APP.6 (Allgemeine Software)
- APP.7 (Entwicklung von Individualsoftware)
- OPS.1.1.6 (Softwaretests und -freigaben)
- OPS.2.3 (Outsourcing für Kunden)
- ISMS.1 (Sicherheitsmanagement)
- DER.3.1 (Audits und Revisionen)
- DER.3.2 (Audits auf Basis des Leitfadens IS-Revision)

Weitere jurisdiktionsspezifische Gesetze — insbesondere Datenschutzrecht (DSGVO), Exportkontrolle, sektorspezifische Compliance-Anforderungen (z. B. Finanzdienstleistungen, Gesundheitswesen) und Softwarehaftungspflichten — sind im Rechtsregister aufgeführt und werden durch Verweis einbezogen.

## 2. Zweck & Geltungsbereich

Diese Richtlinie legt die Regeln für die sichere Softwareentwicklung bei **[IHR_ORGANISATIONSNAME]** fest. Sie deckt den sicheren Entwicklungslebenszyklus, Anforderungen an die Anwendungssicherheit, Grundsätze sicherer Systemarchitektur und -entwicklung, sichere Programmierung, Sicherheitstests, ausgelagerte Entwicklung, Umgebungstrennung, Schutz von Testinformationen und Schutzmaßnahmen bei Audittests ab.

Die Richtlinie gilt für alle an Softwareentwicklung, -tests, -bereitstellung und -wartung beteiligten Personen, einschließlich interner Entwickler, Architekten, Tester, Projektmanager, Betriebspersonal und externer Entwicklungspartner.

## 3. Sicherer Entwicklungslebenszyklus (A 8.25)

Ein sicherer Entwicklungslebenszyklus steuert alle Softwareentwicklungsaktivitäten. Für jedes Projekt oder Produkt wird eine geeignete Entwicklungsmethodik gewählt — ob klassisches Wasserfall-, agiles oder Continuous-Delivery-Modell — und deckt Sicherheitsanforderungen in jeder Phase von der Konzeption bis zur Bereitstellung und Wartung ab. Die Methodik ist dokumentiert und wird an alle Entwicklungsteams kommuniziert.

### 3.1 Lebenszyklus-Elemente

- **Umgebungstrennung:** Entwicklungs-, Test- und Produktionsumgebungen werden angemessen getrennt, um unbefugten Zugriff und unbeabsichtigte Änderungen an Produktionssystemen zu verhindern. Es werden getrennte virtuelle oder physische Domänen verwendet (siehe Abschnitt zur Umgebungstrennung dieser Richtlinie).
- **Sicherheit in der Methodik:** Sicherheitsaktivitäten sind in jede Phase der gewählten Entwicklungsmethodik eingebettet. Dazu gehören Threat Modelling während des Designs, sichere Architekturüberprüfungen vor der Implementierung und Sicherheitsfreigabe vor dem Release.
- **Leitlinien zur sicheren Programmierung:** Sprachspezifische Leitlinien zur sicheren Programmierung werden für jede verwendete Programmiersprache gepflegt. Diese Leitlinien definieren genehmigte Muster, verbotene Konstrukte (z. B. hartkodierte Anmeldeinformationen, unsichere Standardeinstellungen) und Namenskonventionen.
- **Sicherheitsanforderungen in Spezifikation & Design:** Sicherheitsanforderungen werden in der Spezifikations- und Designphase jedes Projekts identifiziert, basierend auf der Informationsklassifizierung und den Schutzanforderungen der verarbeiteten Daten (siehe Projektsicherheitsanforderungen).
- **Sicherheits-Checkpoints:** Sicherheits-Checkpoints sind an definierten Meilensteinen jedes Projekts integriert. An jedem Checkpoint verifiziert das Projektteam, dass die geltenden Sicherheitsanforderungen erfüllt sind, bevor die nächste Phase beginnt.
- **System- & Sicherheitstests:** Umfassende Tests werden während des gesamten Entwicklungsprozesses durchgeführt, einschließlich Funktionstests, Regressionstests, automatisierter statischer Codeanalyse (SAST), dynamischer Anwendungssicherheitstests (DAST) und Penetrationstests für Systeme mit erhöhten Schutzanforderungen.
- **Sichere Repositories:** Quellcode und Konfigurationsartefakte werden in zugangskontrollierten Repositories gespeichert. Der Zugriff folgt dem Prinzip des geringsten Privilegs, und alle Änderungen sind über den Versionsverlauf nachvollziehbar.
- **Versionskontroll-Sicherheit:** Versionskontrollsysteme erzwingen die Nachverfolgbarkeit von Änderungen — jeder Commit ist einem identifizierten Autor zugeordnet. Branch-Protection-Regeln verhindern direkte Pushes auf Release-Branches, und ein Sicherungskonzept deckt alle Repositories ab.
- **Sicherheitswissen & Schulung:** Entwickler erhalten Schulungen in sicheren Entwicklungspraktiken, bevor sie zu sicherheitsrelevantem Code beitragen. Schulungen umfassen Anforderungsanalyse, Threat Modelling, sichere Architektur, sichere Programmiertechniken und Sicherheitstestmethoden.
- **Entwicklerkompetenz:** Entwickler sind qualifiziert, Sicherheitsschwachstellen zu verhindern, zu finden und zu beheben. Die Qualifikation wird durch Schulungsnachweise, Teilnahme an Code-Reviews und nachgewiesene Kompetenz im Umgang mit statischen Analyse- und Schwachstellenscanner-Werkzeugen verifiziert.
- **Lizenzierung & Alternativen:** Softwarelizenzanforderungen werden bei der Technologieauswahl bewertet. Alternativen werden geprüft, um kosteneffiziente Lösungen sicherzustellen und zukünftige Lizenzkonflikte oder Vendor-Lock-in zu vermeiden (siehe IPR-Compliance).
- **Gewährleistung bei ausgelagerter Entwicklung:** Wo Entwicklung ausgelagert wird, liefert der Lieferant eine dokumentierte Zusicherung der Einhaltung dieser Regeln zur sicheren Entwicklung. Vertragsklauseln, Auditrechte und Nachweise sicherer Praktiken sind erforderlich (siehe Abschnitt zur ausgelagerten Entwicklung dieser Richtlinie).

Projekt-, Funktions- und Schnittstellendokumentation wird über den gesamten Lebenszyklus hinweg gepflegt. Sicherheitsrelevante Aspekte werden getrennt für Administratoren und Nutzer dokumentiert. Architekturdiagramme und Threat-Modelle werden aktuell gehalten, während sich das System weiterentwickelt.

## 4. Anforderungen an die Anwendungssicherheit (A 8.26)

Informationssicherheitsanforderungen werden als Teil der Anforderungsanalyse für jede Anwendung, die organisatorische Informationen verarbeitet, speichert oder überträgt, identifiziert, spezifiziert und genehmigt. Diese Anforderungen leiten sich aus dem Geschäftskontext, der Klassifizierung der betroffenen Informationen, geltender Gesetzgebung und dem Risikoappetit der Organisation ab.

### 4.1 Allgemeine Anforderungen

- **Identitätsvertrauen & Authentifizierung:** Der erforderliche Grad des Vertrauens in die Nutzeridentität wird für jede Anwendung festgelegt. Authentifizierungsmechanismen werden entsprechend gewählt — von einfacher passwortbasierter Anmeldung für wenig sensible Funktionen bis hin zur Multi-Faktor-Authentifizierung für privilegierten oder hochklassifizierten Zugriff (siehe *Zugriffskontroll-Richtlinie*).
- **Informationstyp & Klassifizierung:** Jede Anwendung identifiziert die Typen und Klassifizierungsstufen der von ihr verarbeiteten Informationen. Verarbeitungs-, Speicher- und Anzeigemaßnahmen sind auf die geltende Klassifizierungsstufe abgestimmt.
- **Trennung von Zugriffen:** Der Zugriff auf Daten und Funktionen innerhalb der Anwendung wird nach Rollen und Verantwortlichkeiten getrennt. Der für jede Rolle gewährte Zugriffsumfang wird dokumentiert, und rollenbasierte Zugriffskontrolle (RBAC) setzt das Prinzip des geringsten Privilegs durch.
- **Widerstandsfähigkeit gegen Angriffe:** Anwendungen werden so gestaltet, dass sie böswilligen Angriffen und unbeabsichtigten Störungen standhalten. Eingabevalidierung erfolgt serverseitig, Ausgabekodierung verhindert Injection-Angriffe (z. B. SQL-Injection, Cross-Site-Scripting), und Pufferüberlaufschutz wird angewendet.
- **Rechtliche & regulatorische Compliance:** Rechtliche, gesetzliche und regulatorische Anforderungen, die in jeder Jurisdiktion gelten, in der eine Transaktion erzeugt, verarbeitet, abgeschlossen oder gespeichert wird, werden bei der Anforderungsanalyse identifiziert und im Anwendungsdesign berücksichtigt.
- **Datenschutzanforderungen:** Datenschutzanforderungen werden für alle Parteien bewertet, deren personenbezogene Daten von der Anwendung verarbeitet werden. Datenminimierung, Zweckbindung und Einwilligungsmanagement werden im Design behandelt.
- **Schutz vertraulicher Informationen:** Vertrauliche Informationen erhalten dedizierte Schutzmaßnahmen — Verschlüsselung im Ruhezustand und während der Übertragung, Zugriffsprotokollierung und eingeschränkte Anzeige (z. B. Maskierung in Benutzeroberflächen).
- **Datenschutz in Ruhe & Transit:** Daten werden während der Verarbeitung, bei der Übertragung und im Ruhezustand mit Verschlüsselungsalgorithmen und Schlüssellängen geschützt, die der Klassifizierungsstufe angemessen sind. Temporär gespeicherte sensible Daten (z. B. in Caches oder Session-Storage) werden gelöscht, wenn sie nicht mehr benötigt werden.
- **Kommunikationsverschlüsselung:** Kommunikation zwischen allen beteiligten Parteien ist verschlüsselt. TLS 1.2 oder höher ist der Mindeststandard für webbasierte Kommunikation; interne Service-zu-Service-Aufrufe verwenden gegenseitiges TLS oder gleichwertige Mechanismen.
- **Eingabekontrollen:** Alle Nutzer- und Systemeingaben werden gegen erwartete Datentypen, Längen und Wertebereiche validiert. Integritätsprüfungen (z. B. Prüfsummen, Hash-Verifizierung) werden auf von externen Systemen empfangene Daten angewendet. Die serverseitige Validierung erfolgt unabhängig von clientseitigen Prüfungen.
- **Automatisierte Kontrollen:** Automatisierte Kontrollen setzen Geschäftsregeln durch — Genehmigungsgrenzen, Doppelgenehmigungs-Workflows und Prüfungen der Funktionstrennung werden in der Anwendungslogik implementiert, statt sich allein auf manuelle Prozesse zu verlassen.
- **Ausgabekontrollen:** Anwendungsausgaben werden kontrolliert, um sicherzustellen, dass nur autorisierte Empfänger Informationen erhalten. Ausgabeautorisierungsprüfungen verifizieren, dass der anfragende Nutzer die entsprechenden Zugriffsrechte hat, bevor Daten gerendert oder exportiert werden.
- **Einschränkungen für Freitextfelder:** Freitext-Eingabefelder werden in Länge und Inhalt eingeschränkt, um unkontrollierte Speicherung vertraulicher oder personenbezogener Daten zu verhindern. Wo Freitextfelder notwendig sind, werden Inhaltsprüfung oder Klassifizierungskennzeichnung angewendet.
- **Geschäftsprozessanforderungen:** Anforderungen aus Geschäftsprozessen — Transaktionsprotokollierung, Audit-Trails, Überwachungsintegration und Nichtabstreitbarkeit — werden bei der Anforderungsanalyse erfasst und als Teil der Anwendungsarchitektur umgesetzt.
- **Integration mit Sicherheitsmaßnahmen:** Anwendungen integrieren sich in zentrale Sicherheitsmaßnahmen: Protokollierungs- und Überwachungssysteme, Data-Loss-Prevention-Werkzeuge und Security-Information-and-Event-Management-Plattformen (SIEM). Sicherheitsrelevante Ereignisse werden in einem mit der Protokollierungsinfrastruktur der Organisation kompatiblen Format protokolliert.
- **Handhabung von Fehlermeldungen:** Fehlermeldungen werden so gestaltet, dass sie den Nutzern handlungsrelevante Informationen bieten, ohne interne Systemdetails, Stack Traces, Datenbankstrukturen oder andere Informationen preiszugeben, die einem Angreifer helfen könnten. Detaillierte Fehlerinformationen werden serverseitig zum Debugging protokolliert.

### 4.2 Transaktionsdienste

- **Gegenseitiges Identitätsvertrauen:** Für Transaktionsdienste wird der erforderliche Grad des gegenseitigen Identitätsvertrauens zwischen den Parteien festgelegt und implementiert. Digitale Zertifikate, elektronische Signaturen oder gleichwertige Mechanismen verifizieren die Identität jeder Partei, bevor Transaktionen verarbeitet werden.
- **Informationsintegrität:** Die Integrität ausgetauschter oder verarbeiteter Informationen wird mittels zyklischer Redundanzprüfungen, kryptographischer Hashes oder digitaler Signaturen überprüft. Ein Integritätsverlust wird vor Abschluss der Transaktion erkannt und gemeldet.
- **Autorisierung für Schlüsseldokumente:** Autorisierungsprozesse legen fest, wer Schlüsseldokumente einer Transaktion genehmigen, ausstellen oder signieren darf. Genehmigungsworkflows setzen die Funktionstrennung durch und sind in der Autorisierungsmatrix der Anwendung dokumentiert.
- **Vertraulichkeit & Nichtabstreitbarkeit:** Schlüsseldokumente — einschließlich Verträge, Ausschreibungen und formeller Vereinbarungen — werden auf Vertraulichkeit, Integrität, Versandnachweis und Empfangsnachweis geschützt. Digitale Signaturen oder versiegelte Audit-Logs liefern Nichtabstreitbarkeitsnachweise.
- **Transaktionsvertraulichkeit & -integrität:** Transaktionen (z. B. Bestellungen, Lieferadressen, Empfangsbestätigungen) werden durch Ende-zu-Ende-Verschlüsselung und Integritätsprüfung während der gesamten Verarbeitungskette geschützt.
- **Dauer der Transaktionsvertraulichkeit:** Der Zeitraum, während dessen eine Transaktion vertraulich bleibt, wird auf Basis der geschäftlichen und rechtlichen Anforderungen festgelegt. Kryptographische Schutzmaßnahmen werden über den gesamten Vertraulichkeitszeitraum aufrechterhalten.
- **Versicherungs- & Vertragsanforderungen:** Versicherungs- und andere Vertragsanforderungen im Zusammenhang mit Transaktionsdiensten werden identifiziert und im Anwendungsdesign sowie in unterstützenden operativen Verfahren berücksichtigt.

### 4.3 Elektronische Bestellung & Zahlung

- **Vertraulichkeit & Integrität von Bestellinformationen:** Bestellinformationen werden im Transit und im Ruhezustand verschlüsselt. Integritätsprüfungen verhindern unbefugte Änderungen an Bestelldetails zwischen Einreichung und Erfüllung.
- **Zahlungsverifizierung:** Von Kunden bereitgestellte Zahlungsinformationen werden in angemessenem Umfang verifiziert — Adressverifizierung, Kartenvalidierungscodes und Betrugserkennungsmechanismen werden proportional zu Transaktionswert und Risiko angewendet.
- **Verhinderung von Transaktionsduplikaten:** Maßnahmen verhindern den Verlust oder die Duplizierung von Transaktionsinformationen. Idempotenzmechanismen, eindeutige Transaktions-IDs und Abstimmungsprozesse werden implementiert.
- **Sichere Transaktionsspeicherung:** Transaktionsdetails werden auf Systemen innerhalb des Organisationsintranets gespeichert, nicht auf Speicherplattformen, die direkt aus dem Internet zugänglich sind. Keine Transaktionsdaten werden auf öffentlich zugänglichen Umgebungen oder elektronischen Speichermedien aufbewahrt, die dem öffentlichen Netz ausgesetzt sind.
- **Integration einer vertrauenswürdigen Instanz:** Wo eine vertrauenswürdige Instanz (z. B. eine Zertifizierungsstelle für digitale Signaturen oder Zertifikate) genutzt wird, ist die Sicherheit über den gesamten End-to-End-Prozess des Zertifikats- oder Signaturmanagements integriert, einschließlich Ausstellung, Erneuerung, Widerruf und Validierung.

## 5. Grundsätze sicherer Systemarchitektur & -entwicklung (A 8.27)

Grundsätze sicherer Entwicklung werden etabliert, dokumentiert und auf alle Aktivitäten der Informationssystementwicklung und -gestaltung angewendet. Diese Grundsätze werden regelmäßig überprüft und aktualisiert, um aufkommende Bedrohungen und sich entwickelnde Best Practices zu berücksichtigen. Systeme werden auf Basis eines Sicherheitsanforderungskatalogs, eines aus der Informationsklassifizierung abgeleiteten Sicherheitsprofils und eines Threat-Modells gestaltet.

### 5.1 Analyse der Sicherheitsmaßnahmen

- **Volle Bandbreite an Maßnahmen:** Die Systemarchitektur adressiert die volle Bandbreite der Sicherheitsmaßnahmen, die zum Schutz von Informationen und Systemen gegen identifizierte Bedrohungen erforderlich sind. Die Maßnahmenauswahl basiert auf der Risikobewertung und der Klassifizierungsstufe des Assets.
- **Kontrollfähigkeiten:** Jede Sicherheitsmaßnahme wird auf ihre Fähigkeit bewertet, Sicherheitsereignisse zu verhindern, zu erkennen oder auf sie zu reagieren. Maßnahmen werden so ausgewählt, dass sie eine mehrschichtige Verteidigung bieten, die alle drei Fähigkeiten abdeckt.
- **Geschäftsprozessspezifische Maßnahmen:** Spezifische Sicherheitsmaßnahmen, die von bestimmten Geschäftsprozessen benötigt werden — wie die Verschlüsselung sensibler Informationen, Integritätsprüfung und digitale Signatur — werden identifiziert und in die Architektur aufgenommen.
- **Platzierung der Maßnahmen:** Die Architektur spezifiziert, wo und wie jede Sicherheitsmaßnahme angewendet wird, ob sie in die Anwendung, in die Infrastrukturschicht oder in einen zentralen Sicherheitsdienst integriert ist. Platzierungsentscheidungen stehen im Einklang mit der gesamten Sicherheitsarchitektur.
- **Integriertes Maßnahmenset:** Einzelne Sicherheitsmaßnahmen — sowohl manuelle als auch automatisierte — werden so gestaltet, dass sie als integriertes Set zusammenarbeiten. Abhängigkeiten zwischen Maßnahmen werden dokumentiert, und Lücken in der gesamten Kontrollkette werden identifiziert und behoben.

### 5.2 Engineering-Erwägungen

- **Integration in die Sicherheitsarchitektur:** Jedes Systemdesign integriert sich in die übergreifende Sicherheitsarchitektur der Organisation. Gemeinsame Sicherheitsdienste (Identitätsmanagement, Protokollierung, Verschlüsselung) werden wiederverwendet statt neu gebaut.
- **Technische Sicherheitsinfrastruktur:** Das Design nutzt die bestehende technische Sicherheitsinfrastruktur — Public Key Infrastructure (PKI), Identity and Access Management (IAM), Data Leakage Prevention und dynamisches Zugriffsmanagement — statt parallele Mechanismen einzuführen.
- **Organisatorische Fähigkeit:** Technologieentscheidungen werden an der Fähigkeit der Organisation gemessen, die gewählte Lösung über ihren gesamten Lebenszyklus zu entwickeln, zu betreiben und zu unterstützen. Technologien, die die verfügbare interne Expertise übersteigen, werden nur dann gewählt, wenn externe Unterstützungsvereinbarungen bestehen.
- **Kosten, Zeit & Komplexität:** Kosten, Zeit und Komplexität der Erfüllung von Sicherheitsanforderungen werden bei der Technologieauswahl berücksichtigt. Kompromisse werden dokumentiert und vom Projektsponsor und der/dem Informationssicherheitsbeauftragten genehmigt.
- **Aktuelle Best Practices:** Systemdesigns spiegeln aktuelle Best Practices aus Industriestandards, Herstellerleitlinien und anerkannten Sicherheits-Frameworks wider. Design-Teams beobachten relevante Advisories und passen Muster an, während sich die Bedrohungslage entwickelt.

### 5.3 Sichere Designprinzipien

- **Architekturprinzipien:** Die folgenden Architekturprinzipien gelten für alle Systemdesigns: „Security by Design", „Defence in Depth", „Security by Default", „Default Deny", „Fail Securely", „Distrust Input from External Applications", „Security in Deployment", „Assume Breach", „Least Privilege", „Usability and Manageability" und „Least Functionality". Jedes Designdokument identifiziert, welche Prinzipien angewendet werden und wie.
- **Sicherheitsorientierte Designüberprüfung:** Eine sicherheitsorientierte Designüberprüfung wird für jedes System vor Beginn der Implementierung durchgeführt. Die Überprüfung identifiziert Informationssicherheits- und Datenschutzschwachstellen, stellt sicher, dass Sicherheitsmaßnahmen spezifiziert sind, und bestätigt, dass alle Sicherheitsanforderungen adressiert werden.
- **Dokumentation von Restrisiken:** Wo eine Sicherheitsmaßnahme die genannten Anforderungen nicht vollständig erfüllt (z. B. aufgrund übergeordneter Sicherheits- oder Benutzbarkeitsanforderungen), wird die Lücke dokumentiert und vom Risikoeigentümer formal anerkannt. Kompensierende Maßnahmen werden, wo machbar, identifiziert.
- **System-Härtung:** Alle Systeme werden vor der Bereitstellung gehärtet. Unnötige Dienste, Ports und Funktionen werden deaktiviert. Standardzugangsdaten werden geändert, und nur die benötigten Softwarekomponenten werden installiert. Härtungs-Baselines werden pro Technologie-Stack definiert.

### 5.4 Zero-Trust-Prinzipien

- **Assume Breach:** Systemdesigns gehen davon aus, dass die Informationssysteme der Organisation bereits kompromittiert sind. Sicherheitsmaßnahmen verlassen sich nicht allein auf die Netzwerkperimetersicherheit; interne Segmentierung, Überwachung und Detektionsfähigkeiten sind in jede Schicht eingebaut.
- **Never Trust, Always Verify:** Ein „Never Trust and Always Verify"-Ansatz wird auf jeden Zugriff auf Informationssysteme angewendet. Jede Anfrage wird authentifiziert und autorisiert, unabhängig vom Netzwerkstandort des Anfragenden.
- **Ende-zu-Ende-Verschlüsselung:** Anfragen an Informationssysteme werden Ende-zu-Ende verschlüsselt. Die Verschlüsselung wird nicht an Zwischen-Netzwerkgrenzen beendet, es sei denn, eine Inspektion ist ausdrücklich erforderlich und dokumentiert.
- **Externer-Ursprung-Annahme:** Jede Anfrage an ein Informationssystem wird so verifiziert, als ob sie aus einem offenen, externen Netz stammen würde — auch wenn die Anfrage intern erzeugt wird. Kein automatisches Vertrauen wird auf Basis des Netzwerkstandorts gewährt.
- **Least Privilege & dynamischer Zugriff:** Die Zugriffskontrolle folgt dem Prinzip des geringsten Privilegs. Dynamische Zugriffskontrollen authentifizieren und autorisieren Anfragen auf Basis kontextbezogener Informationen — Authentifizierungs-Anmeldedaten, Nutzeridentität, Zustand des Endgeräts, Datenklassifizierung und situative Risikoindikatoren (siehe *Zugriffskontroll-Richtlinie*).
- **Starke Authentifizierung:** Alle Anfragenden werden authentifiziert, und alle Autorisierungsanfragen werden auf Basis von Nutzeridentität, Authentifizierungs-Anmeldedaten und Endgerätedaten validiert. Starke Authentifizierung (z. B. Multi-Faktor-Authentifizierung) wird für den Zugriff auf Systeme durchgesetzt, die klassifizierte Informationen verarbeiten (siehe *Zugriffskontroll-Richtlinie*).

## 6. Sichere Programmierung (A 8.28)

Grundsätze der sicheren Programmierung gelten für jede Softwareentwicklung — sowohl intern als auch ausgelagert. Eine Richtlinie zur sicheren Programmierung definiert organisationsspezifische Erwartungen, genehmigte Prinzipien und verbotene Praktiken. Entwicklungswerkzeuge werden so konfiguriert, dass sie die sichere Programmierung unterstützen, und Entwickler erhalten fortlaufende Schulungen in sicheren Programmiertechniken.

### 6.1 Planung & Vorbereitung

- **Erwartungen & genehmigte Prinzipien:** Organisationsspezifische Erwartungen und genehmigte Prinzipien für die sichere Programmierung werden dokumentiert und an alle Entwicklungsteams kommuniziert. Diese gelten gleichermaßen für interne Entwickler und ausgelagerte Codeentwicklung.
- **Häufige & historische Fehler:** Ein Katalog häufiger und historischer Programmierpraktiken und Fehler, die zu Sicherheits- und Datenschutzschwachstellen führen, wird gepflegt. Der Katalog wird aktualisiert, wenn neue Schwachstellenklassen auftauchen, und dient als Eingabe für Schulungen und Checklisten für Code-Reviews.
- **Konfiguration von Entwicklungswerkzeugen:** Entwicklungswerkzeuge — einschließlich integrierter Entwicklungsumgebungen (IDEs), Linter und Build-Pipelines — werden so konfiguriert, dass sichere Programmierregeln automatisch durchgesetzt werden. Code, der definierte Regeln verletzt, wird in der frühestmöglichen Phase markiert.
- **Herstellerleitlinien:** Leitlinien der Anbieter von Entwicklungswerkzeugen und Ausführungsumgebungen werden befolgt. Sicherheits-Advisories von Werkzeuganbietern werden geprüft und zeitnah angewendet.
- **Aktuelle Entwicklungswerkzeuge:** Entwicklungswerkzeuge (Compiler, Build-Systeme, Abhängigkeitsverwalter, statische Analysewerkzeuge) werden aktuell gehalten. Werkzeug-Updates werden gemäß dem Patch-Management-Prozess der Organisation angewendet, und veraltete Werkzeugversionen werden außer Betrieb genommen.
- **Entwicklerqualifikation:** Entwickler sind qualifiziert, sicheren Code zu schreiben, bevor sie zu Produktionssystemen beitragen. Die Qualifikation wird durch abgeschlossene Schulungen, Zertifizierungen oder nachgewiesene Erfahrung, die von einem Senior Developer überprüft wurde, nachgewiesen.
- **Sicheres Design & Threat Modelling:** Sichere Designpraktiken und Threat Modelling werden in der Planungsphase jedes Entwicklungsvorhabens angewendet. Threat-Modelle identifizieren relevante Bedrohungsakteure, Angriffsvektoren und erforderliche Gegenmaßnahmen.
- **Standards für sichere Programmierung:** Standards für sichere Programmierung werden für jeden Technologie-Stack dokumentiert. Wo anerkannte Industriestandards existieren (z. B. OWASP, CERT Secure Coding Standards), werden diese übernommen und durch organisationsspezifische Regeln ergänzt. Die Einhaltung der Standards ist für jeden Produktionscode verpflichtend.
- **Kontrollierte Entwicklungsumgebungen:** Entwicklung erfolgt in kontrollierten Umgebungen mit definierten Zugriffsrechten, genehmigten Toolchains und standardisierten Konfigurationen. Unkontrollierte oder persönliche Umgebungen werden nicht für produktionsgerichteten Code verwendet.

### 6.2 Während der Programmierung

- **Sprachspezifische Praktiken:** Sichere Programmierpraktiken, die für die verwendeten Programmiersprachen und Techniken spezifisch sind, werden definiert und befolgt. Diese decken sprachspezifische Fallstricke ab wie Speicherverwaltung in C/C++, Injection-Vermeidung in Websprachen und Serialisierungssicherheit in Java/.NET.
- **Sichere Programmiertechniken:** Sichere Programmiertechniken werden während der gesamten Entwicklung angewendet — Pair Programming für sicherheitskritischen Code, Refactoring zur Beseitigung von Sicherheitsschulden, verpflichtendes Peer-Review für alle Merge-Requests, dedizierte Sicherheits-Iterationen und testgetriebene Entwicklung für Sicherheitsfunktionen.
- **Strukturierte Programmierung:** Strukturierte Programmiertechniken werden eingesetzt, um klaren, wartbaren und überprüfbaren Code zu produzieren. Komplexe Logik wird in klar definierte Module mit expliziten Schnittstellen zerlegt.
- **Dokumentation & Fehlerbehebung:** Code wird in einem Umfang dokumentiert, der eine unabhängige Überprüfung ermöglicht. Programmierfehler, die die Ausnutzung von Sicherheits- oder Datenschutzschwachstellen ermöglichen könnten, werden während der Entwicklung identifiziert und beseitigt, nicht nach dem Release verschoben.
- **Verbotene Designmuster:** Die folgenden unsicheren Designmuster sind verboten: hartkodierte Passwörter oder API-Schlüssel, nicht genehmigte Code-Beispiele aus nicht vertrauenswürdigen Quellen, nicht authentifizierte Webdienste, deaktivierte Zertifikatsvalidierung und die Verwendung veralteter kryptographischer Algorithmen. Automatisierte Prüfungen in der Build-Pipeline erkennen und blockieren diese Muster.
- **Statische Analyse während der Entwicklung:** Static Application Security Testing (SAST) ist in die Build-Pipeline integriert und läuft bei jeder Code-Änderung. SAST-Befunde oberhalb des definierten Schweregradschwellenwerts blockieren den Build, bis sie behoben oder formal akzeptiert sind.
- **Angriffsfläche & Least Privilege:** Bevor Software in Betrieb genommen wird, wird die Angriffsfläche bewertet und minimiert. Das Prinzip des geringsten Privilegs wird auf alle Laufzeitrechte angewendet — Dienste laufen mit den minimalen Berechtigungen, die für ihre Funktion erforderlich sind.
- **Analyse häufiger Programmierfehler:** Bevor Software in Betrieb genommen wird, wird eine Analyse der häufigsten Programmierfehler (z. B. OWASP Top 10, CWE Top 25) durchgeführt und dokumentiert. Die Analyse bestätigt, dass alle anwendbaren Fehlerklassen abgemildert wurden.

### 6.3 Überprüfung & Pflege

- **Sichere Paketierung & Bereitstellung:** Updates werden sicher paketiert und bereitgestellt. Installations-, Update- und Patch-Dateien werden vor der Bereitstellung mit Prüfsummen oder digitalen Signaturen verifiziert. Bereitstellungs-Pipelines erzwingen die Integritätsprüfung als obligatorischen Schritt.
- **Umgang mit Schwachstellen:** Gemeldete Informationssicherheits- und Datenschutzschwachstellen werden über den Schwachstellenmanagement-Prozess der Organisation behandelt (siehe Richtlinie zum IT-Betrieb). Korrekturen werden entwickelt, getestet und nach schweregradbasierten Zeitplänen veröffentlicht.
- **Fehler- & Angriffs-Protokollierung:** Fehler und vermutete Angriffe werden protokolliert. Sicherheitsereignisprotokolle werden an die zentrale Protokollierungsinfrastruktur weitergeleitet und regelmäßig überprüft. Code-Anpassungen werden bei Bedarf auf Basis der Log-Analyse-Befunde vorgenommen.
- **Schutz des Quellcodes:** Der Quellcode ist vor unbefugtem Zugriff und Manipulation geschützt. Konfigurationsmanagement-Werkzeuge bieten Zugriffskontrolle und Versionskontrolle. Zugriffsrechte auf Repositories werden vierteljährlich überprüft.
- **Verwaltung externer Bibliotheken:** Externe Bibliotheken werden über ein gepflegtes Inventar verwaltet, das Bibliotheksname, Version, Lizenz und bekannte Schwachstellen erfasst. Bibliotheken werden mit jedem Release-Zyklus aktualisiert, und End-of-Life-Bibliotheken werden ersetzt. Schwachstellen, die in Drittanbieter-Komponenten entdeckt werden, werden über den Schwachstellenmanagement-Prozess der Security Operations verwaltet, einschließlich schweregradbasierter Behebungsfristen.
- **Komponentenauswahl & -wiederverwendung:** Gut geprüfte, bewährte Komponenten werden ausgewählt und wiederverwendet — insbesondere für Authentifizierungs- und kryptographische Funktionen. Die interne Neuimplementierung standardmäßiger Sicherheitsfunktionen wird vermieden. Komponenten werden vor der Aufnahme in die Codebasis genehmigt.
- **Herkunft externer Komponenten:** Lizenz, Sicherheitshistorie und Herkunft jeder externen Komponente werden vor der Übernahme bewertet. Komponenten mit bekannten ungelösten Schwachstellen, ungünstigen Lizenzbedingungen oder unklarem Wartungsstatus werden abgelehnt.
- **Wartbarkeit externer Software:** Externe Softwarewerkzeuge und Bibliotheken werden nur aus bewährten, seriösen Quellen ausgewählt. Die Wartbarkeit jeder Bibliothek wird bewertet — eine aktive Community, regelmäßige Release-Kadenz und reaktive Sicherheitspatches sind erforderlich. Bibliotheken, die diese Kriterien nicht mehr erfüllen, werden zum Austausch vorgesehen.
- **Langfristige Verfügbarkeit:** Die hinreichend langfristige Verfügbarkeit von Entwicklungsressourcen und -artefakten wird sichergestellt. Build-Skripte, Werkzeugversionen und Abhängigkeits-Snapshots werden archiviert, sodass jede veröffentlichte Version bei Bedarf neu gebaut werden kann.
- **Modifizierte externe Pakete — Eingebaute Kontrollen:** Wenn ein externes Softwarepaket modifiziert wird, wird das Risiko bewertet, dessen eingebaute Sicherheitsmaßnahmen und Integritätsprüfprozesse zu kompromittieren, bevor die Modifikation durchgeführt wird.
- **Modifizierte externe Pakete — Herstellerzustimmung:** Vor der Modifikation eines externen Softwarepakets wird die Notwendigkeit bewertet, die Zustimmung des Herstellers einzuholen. Lizenzbedingungen werden geprüft, um zu bestätigen, dass Modifikationen zulässig sind.
- **Modifizierte externe Pakete — Hersteller-Updates:** Vor der Modifikation eines externen Softwarepakets wird die Möglichkeit erkundet, die erforderlichen Änderungen vom Hersteller als Standard-Programm-Update zu erhalten. Vom Hersteller bereitgestellte Lösungen werden gegenüber individuellen Modifikationen bevorzugt.
- **Modifizierte externe Pakete — Wartungsauswirkung:** Vor der Modifikation eines externen Softwarepakets werden die Auswirkungen auf die zukünftige Wartung bewertet. Wenn die Modifikation die Organisation für die Wartung der Software verantwortlich macht, werden die Total Cost of Ownership — einschließlich Sicherheits-Patches — bewertet und genehmigt.
- **Modifizierte externe Pakete — Kompatibilität:** Vor der Modifikation eines externen Softwarepakets wird die Kompatibilität mit anderer im Einsatz befindlicher Software verifiziert. Integrationstests bestätigen, dass die Modifikation keine Regressionen in abhängigen Systemen einführt.

## 7. Sicherheitstests in Entwicklung & Abnahme (A 8.29)

Sicherheitstestprozesse werden über den gesamten Entwicklungslebenszyklus hinweg und für die Abnahme neuer Systeme, Upgrades und neuer Versionen definiert und umgesetzt. Ein Test-Framework wird gemäß den Schutzanforderungen des zu testenden Systems auf Basis des Anforderungskatalogs etabliert. Tests decken sowohl funktionale als auch nicht-funktionale Anforderungen ab, mit besonderem Schwerpunkt auf sicherheitskritischen Funktionen.

### 7.1 Testumfang

- **Sicherheitsfunktionen:** Sicherheitsfunktionen werden umfassend getestet — einschließlich Benutzerauthentifizierung, Zugriffsbeschränkung, Sitzungsmanagement und Nutzung von Kryptographie. Tests verifizieren, dass Sicherheitsfunktionen unter normalen Bedingungen, unter Last und bei missgebildeten Eingaben korrekt funktionieren.
- **Verifizierung sicherer Programmierung:** Tests verifizieren die Einhaltung der in dieser Richtlinie definierten Standards für sichere Programmierung. Ergebnisse automatisierter statischer Analyse (SAST) werden in die Testnachweise aufgenommen, und alle verbleibenden Befunde werden mit Begründung dokumentiert.
- **Verifizierung sicherer Konfiguration:** Tests bestätigen, dass Systemkonfigurationen — einschließlich Betriebssystemeinstellungen, Firewall-Regeln und Konfigurationen von Sicherheitskomponenten — den genehmigten Härtungs-Baselines entsprechen und keine unbeabsichtigten Expositionen einführen.

### 7.2 Testpläne

- **Zeitplan & Aktivitäten:** Testpläne enthalten einen detaillierten Zeitplan der Testaktivitäten und einzelner Testfälle. Der Zeitplan stimmt mit den Entwicklungsmeilensteinen überein und berücksichtigt Abhängigkeitsketten zwischen Testphasen.
- **Eingaben & erwartete Ergebnisse:** Jeder Testfall definiert seine Eingaben und die erwarteten Ergebnisse unter einer Reihe von Bedingungen — einschließlich gültiger Eingaben, Grenzwerten, ungültiger Eingaben und schädlicher Payloads.
- **Bewertungskriterien:** Klare Bestanden/Nicht-Bestanden-Kriterien werden für die Bewertung der Testergebnisse festgelegt. Ein dokumentierter Soll-Ist-Vergleich wird für jeden Testlauf erstellt.
- **Weitere Maßnahmen:** Testpläne definieren den Entscheidungsprozess und weitere Maßnahmen, die bei Testfehlschlägen zu ergreifen sind — erneuter Test nach Behebung, Risikoakzeptanz mit dokumentierter Begründung oder Eskalation an die/den Informationssicherheitsbeauftragte/n bei kritischen Befunden.

### 7.3 Testmethoden

- **Code-Review:** Code-Review-Aktivitäten werden als Kernelement der Sicherheitstests durchgeführt. Reviews zielen gezielt auf Sicherheitsmängel ab, einschließlich der Handhabung unerwarteter Eingaben und Grenzbedingungen. Sowohl automatisierte (SAST) als auch manuelle Review-Methoden werden angewendet.
- **Schwachstellenscans:** Schwachstellenscans werden durchgeführt, um unsichere Konfigurationen, fehlende Patches und bekannte Systemschwachstellen zu identifizieren. Scans werden in der Testumgebung vor dem Release ausgeführt und nach wesentlichen Konfigurationsänderungen wiederholt.
- **Penetrationstests:** Penetrationstests werden durchgeführt, um unsicheren Code und Designfehler zu identifizieren. Für Systeme mit erhöhten Schutzanforderungen folgen Penetrationstests einem dokumentierten Konzept, das Methoden, Umfang und Erfolgskriterien definiert. Ergebnisse werden bis zur Behebung nachverfolgt.

### 7.4 Ausgelagerte & beschaffte Komponenten

- **Beschaffungsprozess:** Ein etablierter Beschaffungsprozess wird für alle extern bezogenen Softwarekomponenten befolgt. Der Prozess umfasst die Sicherheitsbewertung als obligatorischen Schritt vor der Beschaffungsgenehmigung.
- **Sicherheitsanforderungen an Lieferanten:** Verträge mit Lieferanten adressieren die identifizierten Sicherheitsanforderungen, einschließlich sicherer Entwicklungspraktiken, Pflichten zur Schwachstellenoffenlegung und des Rechts, Sicherheitstests an gelieferten Komponenten durchzuführen (siehe Lieferantenmanagement).
- **Bewertung nach Sicherheitskriterien:** Beschaffte Produkte und Dienste werden vor ihrer Aufnahme in die operative Umgebung gegen definierte Sicherheitskriterien bewertet. Die Bewertung umfasst Schwachstellenscans, Konfigurationsüberprüfungen und die Verifizierung der Sicherheitsdokumentation des Lieferanten.

Eine formale Release-Erklärung wird nach erfolgreichem Abschluss aller erforderlichen Tests ausgestellt. Das Release bestätigt, dass die Software funktionale, sicherheits- und rechtliche Anforderungen erfüllt und für die Bereitstellung in der Produktion genehmigt ist. Regressionstests verifizieren, dass Sicherheitsmechanismen und -einstellungen durch Updates nicht verändert werden.

## 8. Ausgelagerte Entwicklung (A 8.30)

Wo Softwareentwicklung ausgelagert wird, leitet und überwacht die Organisation die Entwicklungsaktivität, um sicherzustellen, dass Sicherheitsanforderungen erfüllt werden. Vertragliche Vereinbarungen, definierte Service-Level und regelmäßige Aufsicht regeln die Outsourcing-Beziehung. Die Organisation behält die Verantwortung für die Sicherheit der ausgelagerten Ergebnisse.

### 8.1 Outsourcing-Anforderungen

- **Lizenzierung & geistiges Eigentum:** Lizenzvereinbarungen definieren Code-Eigentum und geistige Eigentumsrechte für alle ausgelagerten Inhalte klar. Das Eigentum an Quellcode, Dokumentation und allen Entwicklungsartefakten wird der Organisation zugewiesen, sofern nicht ausdrücklich etwas anderes vereinbart ist (siehe IPR-Compliance).
- **Vertraglich gesicherte sichere Entwicklung:** Verträge mit externen Entwicklern enthalten verbindliche Anforderungen an sicheres Design, sichere Programmierung, Code-Review und Sicherheitstestpraktiken gemäß dieser Richtlinie (siehe Abschnitte zu sicherer Programmierung und Sicherheitstests).
- **Bereitstellung des Threat-Modells:** Die Organisation stellt externen Entwicklern das geltende Threat-Modell zur Verfügung. Das Threat-Modell identifiziert relevante Bedrohungsakteure, Angriffsvektoren und erforderliche Gegenmaßnahmen, die das externe Entwicklungsteam in sein Design und seine Implementierung integriert.
- **Abnahmetests:** Abnahmetests werden an allen Ergebnissen durchgeführt, um Qualität und Korrektheit zu verifizieren. Testfälle decken funktionale Anforderungen, Sicherheitsanforderungen und die Integration mit bestehenden Systemen ab. Ergebnisse, die Abnahmetests nicht bestehen, werden zur Nachbesserung zurückgegeben.
- **Nachweis von Sicherheits- & Datenschutzfähigkeiten:** Externe Entwickler liefern Nachweise, dass Mindestniveaus an Sicherheits- und Datenschutzfähigkeiten etabliert sind — durch Assurance-Berichte, Zertifizierungen (z. B. ISO 27001, SOC 2) oder unabhängige Audit-Ergebnisse.
- **Tests auf schädliche Inhalte:** Externe Entwickler liefern Nachweise, dass ausreichende Tests durchgeführt wurden, um das Vorhandensein schädlicher Inhalte abzuwehren — sowohl beabsichtigte (z. B. Hintertüren, Logikbomben) als auch unbeabsichtigte (z. B. verwundbare Abhängigkeiten). Lieferpakete werden vor der Abnahme unabhängig gescannt.
- **Nachweis von Schwachstellentests:** Externe Entwickler liefern Nachweise, dass ausreichende Tests durchgeführt wurden, um das Vorhandensein bekannter Schwachstellen abzuwehren. Dies umfasst aktuelle SAST- und Abhängigkeitsscan-Berichte, die bei jedem Release geliefert werden.
- **Source-Code-Escrow:** Escrow-Vereinbarungen für den Software-Quellcode werden etabliert, wenn die ausgelagerte Software geschäftskritisch ist. Die Escrow-Bedingungen umfassen Freigabebedingungen (z. B. Insolvenz des Lieferanten oder Einstellung des Supports) und regelmäßige Escrow-Verifizierung.
- **Auditrechte:** Verträge enthalten das vertragliche Recht, Entwicklungsprozesse und -maßnahmen zu auditieren. Audits können von der Organisation oder einem unabhängigen Dritten durchgeführt werden und decken die Einhaltung sicherer Entwicklungspraktiken, Zugriffskontrollen und Änderungsmanagement ab.
- **Sicherheit der Entwicklungsumgebung:** Sicherheitsanforderungen an die externe Entwicklungsumgebung werden im Vertrag spezifiziert. Dazu gehören Umgebungstrennung, Zugriffskontrolle, Datenschutz und sichere Handhabung des Codes und der Daten der Organisation (siehe Abschnitt zur Umgebungstrennung dieser Richtlinie).
- **Geltende Gesetzgebung:** Verträge adressieren geltende Gesetzgebung, einschließlich Datenschutzgesetze (z. B. DSGVO und geltendes nationales Datenschutzrecht), Exportkontrollvorschriften und sektorspezifische Anforderungen. Der Lieferant bestätigt die Einhaltung aller relevanten rechtlichen Verpflichtungen.

## 9. Trennung von Entwicklungs-, Test- & Produktionsumgebungen (A 8.31)

Entwicklungs-, Test- und Produktionsumgebungen werden getrennt und kontrolliert, um das Risiko unbefugten Zugriffs auf oder unbeabsichtigter Änderungen der Produktionsumgebung zu reduzieren. Der Trennungsansatz wird dokumentiert, einschließlich der Architektur jeder Umgebung und der Verfahren, die nach Abschluss der Tests angewendet werden.

### 9.1 Regeln zur Umgebungstrennung

- **Angemessene Trennung:** Entwicklungs- und Produktionssysteme werden angemessen getrennt und in verschiedenen Domänen betrieben — mit getrennten virtuellen oder physischen Umgebungen, getrennten Netzwerksegmenten und unabhängigen Zugriffskontrollen.
- **Bereitstellungsregeln & Autorisierung:** Regeln und Autorisierungsanforderungen für die Bereitstellung von Software von der Entwicklung in die Produktion werden definiert, dokumentiert und durchgesetzt. Nur formell getestete und genehmigte Releases werden in die Produktion bereitgestellt.
- **Tests vor Produktion:** Alle Änderungen an Produktionssystemen und -anwendungen werden vor der Bereitstellung in einer Test- oder Staging-Umgebung getestet. Testnachweise werden erfasst und mit dem Änderungsdatensatz verknüpft (siehe Richtlinie zu Konfigurations- und Änderungsmanagement).
- **Keine Tests in der Produktion:** Tests werden nicht direkt in Produktionsumgebungen durchgeführt, außer unter Bedingungen, die im Voraus definiert, genehmigt und dokumentiert sind. Jede genehmigte Produktionstestung ist zeitlich begrenzt und unterliegt verstärkter Überwachung.
- **Entwicklungswerkzeuge in der Produktion:** Compiler, Editoren, Debugger und andere Entwicklungswerkzeuge oder Dienstprogramme sind von Produktionssystemen nicht zugänglich, es sei denn, sie werden für einen bestimmten, genehmigten operativen Zweck benötigt. Unnötige Werkzeuge werden entfernt.
- **Umgebungs-Identifikationskennzeichnungen:** Angemessene Umgebungs-Identifikationskennzeichnungen werden in Anwendungsmenüs, Befehlszeilenaufforderungen und System-Bannern angezeigt. Visuelle Differenzierung (z. B. farbcodierte Header) reduziert das Risiko, dass Personen versehentlich Aktionen in der falschen Umgebung ausführen.
- **Sensible Informationen in Nicht-Produktion:** Sensible Informationen werden nicht in Entwicklungs- oder Testumgebungen kopiert, es sei denn, gleichwertige Sicherheitsmaßnahmen sind vorhanden. Wo Produktionsdaten benötigt werden, werden sie vor der Übertragung anonymisiert oder pseudonymisiert (siehe Abschnitt zu Testinformationen dieser Richtlinie).
- **Funktionstrennung:** Keine einzelne Person hat die Fähigkeit, Änderungen sowohl in Entwicklungs- als auch in Produktionsumgebungen ohne vorherige Prüfung und Genehmigung durch eine zweite autorisierte Person vorzunehmen. Bereitstellungs-Pipelines setzen diese Trennung technisch durch.

### 9.2 Umgebungsschutz

- **Werkzeug-Patching & Updates:** Alle Entwicklungs-, Integrations- und Testwerkzeuge — einschließlich Build-Systeme, Integratoren, Compiler, Konfigurationssysteme und Bibliotheken — werden gemäß dem Patch-Management-Prozess der Organisation gepatcht und aktualisiert.
- **Sichere Konfiguration:** Systeme und Software in allen Nicht-Produktionsumgebungen werden sicher konfiguriert, wobei dieselben Härtungsprinzipien wie in der Produktion angewendet werden, nur wo nötig für Entwicklungs- oder Testzwecke angepasst.
- **Zugriffskontrolle:** Der Zugriff auf Entwicklungs-, Test- und Staging-Umgebungen wird kontrolliert und auf Need-to-access-Basis gewährt. Zugriffsrechte werden vierteljährlich überprüft und umgehend entfernt, wenn sie nicht mehr benötigt werden.
- **Änderungsüberwachung:** Änderungen an der Umgebungsinfrastruktur und dem darin gespeicherten Code werden überwacht. Unbefugte Änderungen lösen Alarme aus und werden untersucht.
- **Sichere Überwachung:** Sicherheitsüberwachung wird auf Nicht-Produktionsumgebungen angewendet, um unbefugten Zugriff, Missbrauch und Sicherheitsereignisse zu erkennen. Die Überwachungsabdeckung ist proportional zur Sensibilität der Daten und des Codes in der Umgebung.
- **Umgebungs-Sicherungen:** Sicherungen von Entwicklungs-, Test- und Staging-Umgebungen werden nach einem definierten Zeitplan erstellt. Sicherungen decken Quellcode-Repositories, Build-Konfigurationen, Umgebungskonfigurationen und Testdatensätze ab.

## 10. Testinformationen (A 8.33)

Testinformationen werden angemessen ausgewählt, geschützt und verwaltet. Wenn operative Daten für Tests verwendet werden, verhindern zusätzliche Maßnahmen unbefugte Offenlegung und gewährleisten die Einhaltung von Datenschutzanforderungen. Personenbezogene Daten, die für Tests verwendet werden, werden mindestens pseudonymisiert, idealerweise anonymisiert; die/der Datenschutzbeauftragte wird in die Festlegung des Ansatzes einbezogen.

- **Parität der Zugriffskontrolle:** Dieselben Zugriffskontrollverfahren, die für operative Umgebungen gelten, werden auf Testumgebungen angewendet, die operative Daten enthalten. Nur autorisiertes Testpersonal greift auf die Daten zu, und der Zugriff wird nur für die Dauer des Tests gewährt.
- **Separate Autorisierung pro Kopie:** Jedes Mal, wenn operative Informationen in eine Testumgebung kopiert werden, wird eine separate, dokumentierte Autorisierung eingeholt. Die Autorisierung spezifiziert den Datensatz, den Zweck, die verantwortliche Person und den erwarteten Aufbewahrungszeitraum.
- **Audit-Trail:** Das Kopieren und die Verwendung operativer Informationen zu Testzwecken wird protokolliert. Der Audit-Trail erfasst, wer die Kopie autorisiert hat, wann die Daten übertragen wurden, das Datenvolumen und wann sie aus der Testumgebung gelöscht wurden.
- **Datenschutz durch Maskierung:** Sensible Informationen, die für Tests verwendet werden, werden durch Entfernung oder Maskierung (z. B. Anonymisierung, Pseudonymisierung, Tokenisierung) geschützt, bevor sie in die Testumgebung übertragen werden (siehe *Richtlinie zu Datenlöschung, Maskierung und DLP*).
- **Löschung nach Test:** Operative Informationen werden nach Abschluss der Tests unverzüglich sicher aus der Testumgebung gelöscht. Die Löschung wird verifiziert und dokumentiert, um eine unbefugte spätere Nutzung der Testdaten zu verhindern (siehe *Richtlinie zu Datenlöschung, Maskierung und DLP*).

## 11. Schutz bei Audittests (A 8.34)

Audittests und andere Assurance-Aktivitäten, die die Bewertung operativer Systeme umfassen, werden geplant und vereinbart, um Störungen von Geschäftsprozessen zu minimieren. Der zu Auditzwecken gewährte Zugang wird streng kontrolliert, zeitlich begrenzt und nach Abschluss umgehend widerrufen.

- **Vom Management vereinbarter Zugriff:** Auditanfragen für den Zugriff auf Systeme und Daten werden vor Gewährung des Zugriffs mit dem zuständigen Management vereinbart. Umfang, Zeitpunkt und beteiligte Systeme werden im Auditauftragsschreiben dokumentiert.
- **Umfangskontrolle:** Der Umfang technischer Audittests wird vereinbart und kontrolliert. Tests sind auf die Systeme, Daten und Zeitfenster beschränkt, die im genehmigten Auditplan spezifiziert sind. Jede Umfangserweiterung erfordert eine separate Genehmigung.
- **Nur-Lese-Zugriffsprinzip:** Audittests sind auf den Nur-Lese-Zugriff auf Software und Daten beschränkt. Wo Nur-Lese-Zugriff nicht verfügbar ist, um die erforderlichen Informationen zu erhalten, führt ein erfahrener Administrator mit den erforderlichen Zugriffsrechten den Test im Auftrag des Auditors aus, wobei der Auditor die Ergebnisse beobachtet und verifiziert.
- **Geräte-Sicherheitsanforderungen:** Vor Gewährung des Zugriffs wird die Sicherheitslage der für den Zugriff auf die Systeme verwendeten Geräte (z. B. Laptops, Tablets) festgestellt und verifiziert — einschließlich aktueller Antivirensoftware, aktueller Patches, Festplattenverschlüsselung und konformer Konfiguration.
- **Nicht-Nur-Lese-Zugriffskontrollen:** Nicht-Nur-Lese-Zugriff ist nur für isolierte Kopien von Systemdateien zulässig. Kopien werden nach Abschluss des Audits sicher gelöscht, es sei denn, es besteht eine dokumentierte Verpflichtung zu ihrer Aufbewahrung im Rahmen der Auditdokumentationsanforderungen; in diesem Fall erhalten sie angemessenen Schutz.
- **Anfragen zu besonderer Verarbeitung:** Anfragen zu besonderer oder zusätzlicher Verarbeitung — wie der Ausführung von Auditwerkzeugen, Skripten oder automatisierten Scannern — werden identifiziert, im Voraus vereinbart und vom Systemeigentümer vor der Ausführung autorisiert.
- **Berücksichtigung der Verfügbarkeit:** Audittests, die die Systemverfügbarkeit beeinträchtigen können, werden außerhalb der Geschäftszeiten geplant. Wo dies nicht möglich ist, werden die potenziellen Auswirkungen bewertet und betroffenen Beteiligten vorab kommuniziert.
- **Zugriffsprotokollierung:** Jeder Zugriff zu Audit- und Testzwecken wird überwacht und protokolliert. Audit-Zugriffsprotokolle werden gemäß dem Log-Aufbewahrungsplan der Organisation aufbewahrt und stehen der/dem Informationssicherheitsbeauftragten zur Überprüfung zur Verfügung.

## 12. Rollen & Verantwortlichkeiten

- **Geschäftsleitung:** Genehmigt diese Richtlinie, stellt Ressourcen für sichere Entwicklung bereit und stellt die organisatorische Verpflichtung zur Sicherheit über den gesamten Softwareentwicklungslebenszyklus sicher.
- **Informationssicherheitsbeauftragte/r (ISB):** Überwacht die Umsetzung dieser Richtlinie, führt oder koordiniert Sicherheits-Designüberprüfungen durch, überwacht die Einhaltung und berichtet über die Reife der sicheren Entwicklungspraktiken.
- **Entwicklungsleitung:** Stellt sicher, dass Entwicklungsteams den sicheren Entwicklungslebenszyklus, die Programmierstandards und Testanforderungen dieser Richtlinie befolgen. Genehmigt Release-Erklärungen und verwaltet Sicherheitsschulungen für ihre Teams.
- **Entwickler & Architekten:** Wenden Standards für sichere Programmierung an, führen Threat Modelling und Designüberprüfungen durch, beheben Sicherheitsbefunde und pflegen die Dokumentation. Nehmen an Sicherheitsschulungen teil und teilen Wissen im Team.
- **Qualitätssicherung & Tests:** Führen Sicherheitstestpläne aus, führen Code-Reviews durch, führen Schwachstellenscans durch und dokumentieren Testergebnisse. Eskalieren kritische Befunde an die/den Informationssicherheitsbeauftragte/n.
- **IT-Betrieb:** Pflegt die Trennung von Entwicklungs-, Test- und Produktionsumgebungen, setzt Bereitstellungsautorisierungsregeln durch und unterstützt Audittests mit angemessenen Zugriffskontrollen.
- **Datenschutzbeauftragte/r:** Berät zu Datenschutzanforderungen für das Anwendungsdesign, genehmigt den Ansatz zur Anonymisierung oder Pseudonymisierung von Testdaten und überprüft Datenschutzaspekte ausgelagerter Entwicklungsverträge.
- **Beschaffung & Lieferantenmanagement:** Stellt sicher, dass ausgelagerte Entwicklungsverträge die in dieser Richtlinie definierten erforderlichen Sicherheitsklauseln, Auditrechte und Bestimmungen zum geistigen Eigentum enthalten.

## 13. Überprüfung & Pflege

Diese Richtlinie wird überprüft und bei Bedarf aktualisiert:

- Mindestens jährlich im Rahmen des ISMS-Managementbewertungszyklus.
- Nach wesentlichen Änderungen an der Entwicklungsorganisation, der Toolchain oder dem Technologie-Stack.
- Nach Sicherheitsvorfällen im Zusammenhang mit Software-Schwachstellen oder Entwicklungsprozess-Fehlern.
- Wenn Änderungen in der Bedrohungslage, im regulatorischen Umfeld oder in den Best Practices der Branche Anpassungen an den sicheren Entwicklungspraktiken erfordern.
