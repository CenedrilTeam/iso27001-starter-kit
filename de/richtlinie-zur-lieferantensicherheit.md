# Richtlinie zur Lieferantensicherheit

> **Dokumentenkontrolle**  
> Eigentümer: [RICHTLINIEN_EIGENTÜMER_ROLLE, z. B. Informationssicherheitsbeauftragte/r]  
> Genehmigt von: [GENEHMIGER_NAME_UND_ROLLE]  
> Version: [VERSION]  
> Gültig ab: [GÜLTIGKEITSDATUM]  
> Nächste Überprüfung: [NÄCHSTES_ÜBERPRÜFUNGSDATUM]

## 1. Rechtliche/Regulatorische Grundlage

ISO/IEC 27001:2022 / ISO/IEC 27002:2022, Anhang A — Lieferantenbeziehungen:

- A 5.19 — Informationssicherheit in Lieferantenbeziehungen
- A 5.20 — Adressierung von Informationssicherheit in Lieferantenvereinbarungen
- A 5.21 — Management der Informationssicherheit in der IKT-Lieferkette
- A 5.22 — Überwachung, Überprüfung und Änderungsmanagement von Lieferantendiensten
- A 5.23 — Informationssicherheit bei der Nutzung von Cloud-Diensten

ISO/IEC 27036-3 — Informationssicherheit für Lieferantenbeziehungen.

BSI IT-Grundschutz:

- OPS.2.3 (Outsourcing aus Kundensicht)
- OPS.2.2 (Cloud-Nutzung)
- OPS.3.2 (Outsourcing aus Dienstleistersicht)

Weitere jurisdiktionsspezifische Gesetze — insbesondere NIS2-Lieferkettenpflichten, der EU Cyber Resilience Act (für Produkte mit digitalen Elementen), Datenschutzrecht (DSGVO und Regeln zur grenzüberschreitenden Datenübermittlung), sektorspezifische Outsourcing-Vorschriften (z. B. Finanzdienstleistungen) und Vertragsrecht — sind im Rechtsregister aufgeführt und werden durch Verweis einbezogen.

## 2. Zweck & Geltungsbereich

Diese Richtlinie legt den Rahmen für das Management von Informationssicherheitsrisiken aus Lieferantenbeziehungen bei **[IHR_ORGANISATIONSNAME]** fest. Sie deckt den gesamten Lieferantenlebenszyklus von der initialen Bewertung und Auswahl über die vertragliche Bindung und laufende Überwachung bis zur geordneten Beendigung oder Überleitung ab.

Die Richtlinie gilt für alle Kategorien externer Lieferanten, einschließlich IKT-Dienstleister, Cloud-Dienstleister, Software- und Hardwarelieferanten, Outsourcing-Partner, Berater und alle anderen Dritten, die auf organisatorische Informationen zugreifen, diese verarbeiten, speichern, übertragen oder Infrastrukturkomponenten bereitstellen, die die Vertraulichkeit, Integrität oder Verfügbarkeit organisatorischer Informationen beeinflussen. Alle Beschäftigten, Auftragnehmer und Personen, die an Lieferantenauswahl, -management oder -aufsicht beteiligt sind, sind an diese Richtlinie gebunden.

## 3. Lieferantenbeziehungen & Klassifizierung (A 5.19)

Prozesse und Verfahren sind etabliert, um Sicherheitsrisiken im Zusammenhang mit Lieferantenprodukten und -diensten zu verwalten. Ein risikoorientierter Ansatz regelt den gesamten Outsourcing-Lebenszyklus: Strategiedefinition, Eignungsprüfung potenzieller Anbieter, vertragliche Gestaltung, operatives Management und geordnete Beendigung. Die Verantwortung für Informationssicherheit verbleibt jederzeit bei der Organisation, unabhängig davon, welche Aktivitäten ausgelagert werden.

### 3.1 Lieferantentypen & Risikobewertung

- **Register der Lieferantentypen:** Ein Lieferantenregister klassifiziert alle Lieferanten in definierte Kategorien: IKT-Dienstleister, Cloud-Dienstleister, Software- und Hardwarelieferanten, Logistikpartner, Versorgungsunternehmen, Finanzdienstleister und Lieferanten von IKT-Infrastrukturkomponenten. Jeder Eintrag erfasst den Lieferantentyp, die Informationswerte und Systeme, die der Lieferant beeinflussen kann, die Kritikalitätseinstufung und die zuständige interne Ansprechperson.
- **Informations- & Infrastrukturumfang:** Für jede Lieferantenbeziehung werden die spezifischen Informationswerte, IKT-Dienste und die physische Infrastruktur dokumentiert, auf die der Lieferant zugreift, die er überwacht, steuert oder nutzt. Der Zugriff ist auf den für die Leistungserbringung erforderlichen Mindestumfang beschränkt.
- **Bewertung der Auswirkung von IKT-Komponenten:** Von Lieferanten bereitgestellte IKT-Infrastrukturkomponenten und -dienste werden nach ihrer potenziellen Auswirkung auf Vertraulichkeit, Integrität und Verfügbarkeit klassifiziert. Komponenten, die sensible Daten verarbeiten oder übertragen, erhalten eine höhere Kritikalitätseinstufung und unterliegen strengeren Sicherheitsanforderungen.
- **Erwartungen an Personal- & physische Sicherheit:** Für jede Lieferantenkategorie werden Mindestanforderungen an Personal- und physische Sicherheit definiert. Lieferanten, die sensible Informationen handhaben, erfüllen Standards, die den internen Anforderungen gleichwertig sind, einschließlich Hintergrundüberprüfungen von Schlüsselpersonal, soweit rechtlich zulässig, und angemessener physischer Zugangskontrollen an ihren Standorten.

### 3.2 Bewertung & Auswahl

- **Bewertungs- & Auswahlprozess:** Lieferanten werden auf Basis der Sensibilität der beteiligten Informationen, Produkte und Dienste bewertet und ausgewählt. Der Bewertungsprozess umfasst Marktanalyse, Kundenreferenzen, Dokumentenprüfung, Zertifizierungen (ISO 27001, SOC 2, C5 oder gleichwertig) und, bei hochkritischen Lieferanten, Sicherheitsbewertungen vor Ort. Bewertungsergebnisse werden im Lieferantenregister mit einer formalen Eignungsfeststellung dokumentiert.
- **Sicherheitsbewertung von Produkten & Diensten:** Vor dem Onboarding werden die Informationssicherheits- und Datenschutzmaßnahmen von Lieferantenprodukten und -diensten bewertet. Die Bewertung verifiziert die Richtigkeit und Vollständigkeit der vom Lieferanten umgesetzten Maßnahmen, mit besonderem Augenmerk auf Maßnahmen zum Schutz der Integrität der Informationsverarbeitung. Ergebnisse werden erfasst und vor Vertragsabschluss geprüft.

### 3.3 Risikomanagement & Compliance

- **Lieferantenrisikobewertung:** Informationssicherheitsrisiken, die mit jeder Lieferantenbeziehung verbunden sind, werden bewertet und verwaltet, einschließlich Risiken durch potenziell böswilliges Lieferantenpersonal, fehlerhafte oder verwundbare Produkte (einschließlich eingebetteter Softwarekomponenten und Unterkomponenten) und unzureichender Sicherheitspraktiken. Lieferantenrisikobewertungen werden mindestens jährlich und nach wesentlichen Änderungen der Lieferantenbeziehung oder Bedrohungslage aktualisiert.
- **Compliance-Überwachung:** Die Einhaltung etablierter Informationssicherheitsanforderungen wird für jeden Lieferantentyp und jede Zugriffskategorie überwacht. Überwachungsmethoden umfassen Drittaudits, unabhängige Attestierungsberichte (SOC 2, ISO-27001-Zertifikate), Produktvalidierung und periodische Selbstbewertungsfragebögen. Die Überwachungshäufigkeit ist proportional zur Kritikalität der Lieferantenbeziehung.
- **Behebung von Nichtkonformitäten:** Wenn Nichtkonformität eines Lieferanten durch Überwachung, Audit oder auf andere Weise festgestellt wird, wird ein definierter Eskalationsprozess ausgelöst. Der Lieferant erhält eine formale Nichtkonformitätsmitteilung mit spezifischen Behebungsanforderungen und einer Frist. Nicht behobene Nichtkonformitäten werden zur Entscheidung über Risikoakzeptanz, Vertragsverhandlung oder Kündigung an die Geschäftsleitung eskaliert.

### 3.4 Vorfallbehandlung & Kontinuität

- **Vorfallbehandlung:** Verantwortlichkeiten für die Behandlung von Informationssicherheitsvorfällen sind sowohl für die Organisation als auch für jeden Lieferanten definiert. Lieferantenvereinbarungen spezifizieren Meldefristen, Zusammenarbeitsverfahren während der Behebung und Nachmeldepflichten. Lieferanten melden Sicherheitsvorfälle, die organisatorische Daten betreffen, innerhalb von 24 Stunden nach Entdeckung.
- **Resilienz & Contingency:** Die Lieferantenresilienz wird als Teil des Onboarding-Prozesses bewertet. Wo erforderlich, werden Wiederherstellungs- und Contingency-Maßnahmen vereinbart, um die fortwährende Verfügbarkeit der Lieferanten-Informationsverarbeitung sicherzustellen. Für kritische Lieferanten werden alternative Lieferanten oder interne Ausweichkapazitäten im Voraus identifiziert, um Unterbrechungen zu vermeiden, wenn der Lieferant nicht mehr liefern kann.

### 3.5 Sensibilisierung & Übergänge

- **Sensibilisierung & Schulung des Personals:** Personen, die mit Lieferantenpersonal interagieren, erhalten Schulungen zu den geltenden Spielregeln, themenspezifischen Richtlinien, Prozessen und erwarteten Verhaltensweisen. Schulungsinhalte sind auf den Lieferantentyp und die Zugriffsebene zugeschnitten. Schulungen werden vor der ersten Interaktion durchgeführt und jährlich aufgefrischt.
- **Informationsübertragung & Übergänge:** Wenn Informationen, Werte oder Verantwortlichkeiten zu oder von einem Lieferanten übertragen werden, wird die Übertragung über einen dokumentierten Übergangsplan gesteuert. Informationssicherheit und Datenschutz werden während des gesamten Übertragungszeitraums aufrechterhalten, einschließlich Zwischenmaßnahmen in Übergangsphasen.

### 3.6 Sichere Beendigung

- **Entzug von Zugriffsrechten:** Alle dem Lieferanten gewährten Zugriffsrechte werden innerhalb eines Werktages nach Beendigung der Beziehung widerrufen. Der Entzug umfasst logische Zugriffe (Konten, VPN, API-Schlüssel) und physischen Zugang (Ausweise, Schlüssel, Tokens). Der Abschluss wird durch ein Zugriffsaudit verifiziert.
- **Informationsbehandlung bei Beendigung:** Bei Beendigung werden alle vom Lieferanten gehaltenen organisatorischen Informationen in einem vereinbarten Format zurückgegeben oder sicher vernichtet. Der Lieferant stellt eine schriftliche Vernichtungsbestätigung mit einer Beschreibung der verwendeten Methode bereit.
- **Eigentum an geistigem Eigentum:** Das Eigentum an geistigem Eigentum, das während der Beauftragung entwickelt wurde, wird in der Lieferantenvereinbarung bestimmt. Bei Beendigung werden alle IP-Lieferungen, Quellcode und Dokumentation gemäß den Vereinbarungen an die Organisation übertragen oder entsorgt.
- **Informationsportabilität:** Vereinbarungen enthalten Bestimmungen zur Informationsportabilität im Falle eines Lieferantenwechsels oder einer Insourcing-Entscheidung. Datenformate, Exportverfahren und Fristen werden festgelegt, um einen nahtlosen Übergang zu einem alternativen Lieferanten oder in den internen Betrieb zu ermöglichen.
- **Aufbewahrung von Aufzeichnungen:** Aufbewahrungsfristen und Handhabungsverfahren für während der Lieferantenbeziehung erzeugte Aufzeichnungen sind definiert. Bei Beendigung werden Aufzeichnungen an die Organisation übergeben oder gemäß den vereinbarten Zeiträumen und rechtlichen/regulatorischen Anforderungen vom Lieferanten aufbewahrt.
- **Rückgabe von Werten:** Alle organisatorischen Werte (Hardware, Tokens, Dokumentation, Medien), die der Lieferant hält, werden innerhalb des in der Vereinbarung festgelegten Zeitraums zurückgegeben. Eine Rückgabecheckliste verifiziert die Vollständigkeit.
- **Sichere Entsorgung:** Informationen und zugehörige Werte, die nicht zurückgegeben werden, werden mit Methoden sicher entsorgt, die der Klassifizierungsstufe der Informationen entsprechen. Der Lieferant stellt für jeden Posten ein Entsorgungszertifikat bereit.
- **Fortbestehende Vertraulichkeit:** Vertraulichkeitspflichten überdauern die Beendigung der Lieferantenbeziehung. Geheimhaltungsvereinbarungen bleiben für den im Vertrag festgelegten Zeitraum in Kraft, typischerweise mindestens drei Jahre nach Beendigung.

### 3.7 Lieferanten mit begrenztem Einfluss

- **Auf Leitlinien basierende Auswahl:** Wo die Organisation einem Lieferanten keine direkten Sicherheitsanforderungen auferlegen kann (z. B. Versorgungsunternehmen, große Plattformanbieter), berücksichtigen Lieferantenauswahlentscheidungen die in dieser Richtlinie etablierten Sicherheitsleitlinien. Verfügbare Sicherheitsinformationen, öffentliche Auditberichte und bekannte Schwachstellen des Lieferanten werden vor der Beauftragung bewertet.
- **Kompensierende Maßnahmen:** Für Lieferanten, bei denen keine direkten Anforderungen gestellt werden können, werden auf Grundlage einer Risikobewertung kompensierende Maßnahmen umgesetzt. Diese Maßnahmen mildern das Restrisiko aus der Sicherheitslage des Lieferanten und werden im Risikoregister dokumentiert.

## 4. Vertragliche Sicherheitsanforderungen (A 5.20)

Lieferantenvereinbarungen werden dokumentiert, um sicherzustellen, dass beide Parteien ein klares Verständnis ihrer Pflichten in Bezug auf Informationssicherheit haben. Für alle Lieferantenvereinbarungen wird eine standardisierte Vertragsvorlage verwendet, die Basissicherheitsklauseln enthält, die auf Basis des Risikoprofils und der Kritikalität der spezifischen Lieferantenbeziehung angepasst werden. Verträge werden vor der Unterzeichnung von Vertretern der Informationssicherheit, der Rechtsabteilung und der Beschaffung geprüft.

### 4.1 Information & Klassifizierung

- **Beschreibung der Information & Zugriffsmethoden:** Jede Vereinbarung beschreibt die spezifischen bereitzustellenden oder zugegriffenen Informationen und die Methoden der Bereitstellung oder des Zugriffs. Datenflüsse werden dokumentiert, einschließlich Schnittstellen, Protokolle und Übertragungsmechanismen.
- **Informationsklassifizierung:** Vereinbarungen verpflichten den Lieferanten, Informationen gemäß dem Klassifizierungsschema der Organisation zu behandeln. Klassifizierte Informationen werden vor der Übertragung gekennzeichnet und während ihres gesamten Lebenszyklus entsprechend der Klassifizierungsstufe gehandhabt.
- **Klassifizierungs-Mapping:** Wenn der Lieferant ein eigenes Klassifizierungsschema verwendet, wird ein formales Mapping zwischen den beiden Schemata erstellt und in der Vereinbarung dokumentiert, um eine einheitliche Handhabung der Informationen zu gewährleisten.

### 4.2 Recht & Compliance

- **Rechtliche & regulatorische Anforderungen:** Vereinbarungen spezifizieren geltende rechtliche, gesetzliche, regulatorische und vertragliche Anforderungen, einschließlich Datenschutzpflichten, Umgang mit personenbezogenen Daten (PII), Rechten des geistigen Eigentums und Urheberrechtsbestimmungen. Die Vereinbarung beschreibt, wie die Einhaltung sichergestellt und verifiziert wird.
- **Regeln zur akzeptablen Nutzung:** Regeln zur akzeptablen und nicht akzeptablen Nutzung der Informationen und zugehörigen Werte der Organisation sind in der Vereinbarung definiert. Der Lieferant erkennt diese Regeln an und stellt sicher, dass sein Personal informiert ist.

### 4.3 Sicherheitsmaßnahmenpflichten

- **Kontrollpflichten:** Jede Vereinbarung spezifiziert die Sicherheitsmaßnahmen, die beide Parteien umsetzen, einschließlich Zugriffskontrolle, Leistungsüberprüfung, Überwachung, Berichterstattung und Auditierung. Die Verpflichtung des Lieferanten, den Informationssicherheitsanforderungen der Organisation zu entsprechen, ist ausdrücklich und vertraglich bindend festgelegt.
- **Sicherheit der IKT-Infrastruktur:** Mindestanforderungen an die Informationssicherheit der IKT-Infrastruktur des Lieferanten werden für jeden Informations- und Zugriffskategorie-Typ definiert. Diese Anforderungen dienen als Grundlage für individuelle Vereinbarungen und werden auf Basis von Geschäftsbedarf und Risikokriterien skaliert. Für externe kryptographische Dienstleister (Zertifizierungsstellen, HSM-Anbieter, Cloud-KMS) adressieren spezifische SLA-Bestimmungen Schlüsselverfügbarkeit, Escrow-Vereinbarungen und Reaktionszeiten bei Vorfällen.
- **Personalautorisierung:** Verfahren zur Autorisierung und zum Widerruf der Autorisierung von Lieferantenpersonal für die Nutzung organisatorischer Informationen und Werte sind definiert. Eine explizite Liste autorisierter Lieferantenmitarbeiter wird geführt und vierteljährlich überprüft. Änderungen an der Liste der autorisierten Mitarbeiter erfordern eine vorherige Benachrichtigung.
- **Personalüberprüfung:** Soweit rechtlich zulässig, verpflichten Vereinbarungen zur Hintergrundüberprüfung von Lieferantenpersonal, das auf sensible Informationen zugreift. Die Vereinbarung definiert die Überprüfungsverantwortlichkeiten, Verifizierungsverfahren und Meldepflichten, wenn eine Überprüfung nicht abgeschlossen wurde oder die Ergebnisse Bedenken aufwerfen.
- **Physische Sicherheitsmaßnahmen:** Physische Sicherheitsmaßnahmen an den Lieferantenstandorten sind der Klassifizierungsstufe der verarbeiteten Informationen angemessen. Anforderungen umfassen Zugangskontrolle, Umweltschutz, Besuchermanagement und Handhabung von Medien.
- **Schutz der Informationsübertragung:** Maßnahmen zum Schutz von Informationen bei physischer und logischer Übertragung sind spezifiziert, einschließlich Verschlüsselungsstandards, sicherer Transportmethoden und Chain-of-Custody-Dokumentation.

### 4.4 Audit, Vorfälle & Schulung

- **Klauseln zum Vorfallmanagement:** Vereinbarungen definieren Anforderungen an das Vorfallmanagement, einschließlich verpflichtender Meldung innerhalb von 24 Stunden nach Entdeckung, Zusammenarbeitsverfahren während der Vorfallbehebung, Beweissicherungspflichten und Nachmeldung.
- **Schulungs- & Sensibilisierungsanforderungen:** Vereinbarungen verpflichten den Lieferanten sicherzustellen, dass sein Personal Schulungen zu den spezifischen Verfahren und Informationssicherheitsanforderungen der Organisation absolviert, einschließlich Incident-Response-Verfahren und Autorisierungsprozessen.
- **Drittparteien-Attestierungen:** Vereinbarungen verpflichten den Lieferanten, Nachweise und Gewährleistungen über anerkannte Drittparteien-Attestierungsmechanismen (ISO-27001-Zertifizierung, SOC-2-Typ-II-Berichte, C5-Attestierung) bereitzustellen, die relevante Informationssicherheitsanforderungen abdecken. Unabhängige Berichte über die Wirksamkeit der Maßnahmen werden mindestens jährlich bereitgestellt.
- **Auditrecht:** Die Organisation behält das Recht, die Prozesse und Maßnahmen des Lieferanten im Zusammenhang mit der Vereinbarung entweder direkt oder durch einen unabhängigen Auditor zu auditieren. Auditumfang, -häufigkeit und -ankündigungsanforderungen sind in der Vereinbarung spezifiziert.
- **Periodische Wirksamkeitsberichte:** Der Lieferant ist verpflichtet, periodische Berichte über die Wirksamkeit der Maßnahmen zu liefern. In den Berichten identifizierte relevante Probleme werden innerhalb vereinbarter Fristen behandelt, wobei Behebungspläne bis zum Abschluss nachverfolgt werden.

### 4.5 Unterauftragsvergabe & Behebung

- **Bestimmungen zur Unterauftragsvergabe:** Vereinbarungen enthalten Bestimmungen zur Unterauftragsvergabe. Unterlieferanten sind an dieselben Sicherheitspflichten gebunden wie der Primärlieferant. Der Lieferant führt eine aktuelle Liste der Unterlieferanten und benachrichtigt die Organisation vor jeder Änderung. Vor der Beauftragung neuer Unterlieferanten für Dienste mit organisatorischen Daten ist eine vorherige Genehmigung erforderlich.
- **Schadenersatz & Behebung:** Vereinbarungen definieren Schadenersatz und Behebungsmaßnahmen bei Nichterfüllung der Sicherheitsanforderungen. Strafklauseln sind proportional zur Kritikalität des Dienstes und zur Schwere des Verstoßes. Behebungsfristen sind für verschiedene Schweregradkategorien spezifiziert.
- **Mängelbeseitigung & Konfliktlösung:** Ein strukturierter Mängelbeseitigungsprozess mit definierten Schweregradstufen und Reaktionszeiten ist etabliert. Konfliktlösungsverfahren umfassen Eskalationspfade, Mediationsbestimmungen und, als letzte Option, Schiedsklauseln.
- **Sicherheitsansprechpersonen:** Die Vereinbarung identifiziert relevante Kontakte, einschließlich einer benannten Ansprechperson für Informationssicherheitsfragen sowohl auf der Lieferanten- als auch auf der Organisationsseite. Kontaktdaten werden aktuell gehalten und vierteljährlich überprüft.

### 4.6 Kontinuität & Wiederherstellung

- **Sicherungsbestimmungen:** Vereinbarungen verpflichten den Lieferanten, Sicherungen im Einklang mit den Anforderungen der Organisation hinsichtlich Häufigkeit, Typ und Speicherort bereitzustellen. Sicherungsverfahren sind dokumentiert und die Wiederherstellung wird regelmäßig getestet.
- **Disaster-Recovery-Standort:** Für kritische Dienste verpflichten Vereinbarungen zu einem Ausweichstandort (Disaster-Recovery-Standort), der nicht denselben Bedrohungen unterliegt wie der Primärstandort. Fallback-Maßnahmen sind für den Fall definiert, dass primäre Maßnahmen ausfallen.
- **Änderungsmanagement:** Vereinbarungen enthalten einen Änderungsmanagement-Prozess, der die rechtzeitige Benachrichtigung der Organisation über alle den Dienst betreffenden Änderungen sicherstellt. Die Organisation behält sich das Recht vor, Änderungen abzulehnen, die die Informationssicherheit negativ beeinflussen.

### 4.7 Kündigungsklauseln

- **Kündigungsklauseln:** Vereinbarungen enthalten Kündigungsklauseln, die die Verwaltung von Aufzeichnungen, die Rückgabe von Werten, die sichere Entsorgung von Informationen und zugehörigen Werten sowie fortbestehende Vertraulichkeitspflichten abdecken. Exit-Fristen und Pflichten zur Übergangsunterstützung sind spezifiziert.
- **Sichere Datenvernichtung:** Die Vereinbarung definiert eine Methode, mit der der Lieferant organisatorische Informationen sicher vernichtet, sobald sie nicht mehr benötigt werden. Die Vernichtung wird zertifiziert, und die Methode entspricht der Klassifizierungsstufe der Daten.
- **Übergangsunterstützung:** Am Vertragsende leistet der Lieferant Übergangsunterstützung an einen anderen Lieferanten oder an die Organisation selbst. Ein Übergangsplan mit Meilensteinen, Lieferungen und Abnahmekriterien wird vor Inkrafttreten der Beendigung vereinbart.

### 4.8 Vereinbarungsregister & Überprüfung

- **Vereinbarungsregister:** Ein zentrales Register aller Vereinbarungen mit externen Parteien (Verträge, Absichtserklärungen, Vereinbarungen zum Informationsaustausch, NDAs) wird geführt. Das Register verfolgt, wo organisatorische Informationen geteilt oder verarbeitet werden, und wird mindestens halbjährlich überprüft.
- **Regelmäßige Vereinbarungsüberprüfung:** Vereinbarungen mit externen Parteien werden mindestens jährlich überprüft, validiert und aktualisiert, um sicherzustellen, dass sie weiterhin erforderlich, zweckmäßig und mit aktuellen Informationssicherheitsklauseln versehen sind. Veraltete oder unnötige Vereinbarungen werden beendet.

## 5. Management der IKT-Lieferkette (A 5.21)

IKT-Produkte und -Dienste werden nur aus seriösen Quellen mit dokumentierten Qualitätssicherungs- und Sicherheitspraktiken bezogen. Die Organisation arbeitet mit ihren Lieferanten zusammen, um die Struktur der IKT-Lieferkette zu verstehen, und identifiziert Angelegenheiten, die die bereitgestellten Produkte und Dienste wesentlich beeinflussen. Sicherheitsanforderungen werden über die gesamte Lieferkette hinweg weitergegeben, indem Lieferanten verpflichtet werden, gleichwertige Pflichten an ihre Unterlieferanten weiterzugeben. Die IKT-Lieferkette umfasst Cloud-Dienste, IoT-Geräte, Hosting-Dienste und alle eingebetteten Hardware- und Softwarekomponenten. Wo der EU Cyber Resilience Act (CRA) anwendbar ist, stellen Lieferanten von Produkten mit digitalen Elementen Konformitätsdokumentation bereit, unterhalten Schwachstellen-Handhabungsprozesse und liefern Sicherheitsupdates für den definierten Supportzeitraum.

### 5.1 Beschaffung & Weitergabe in der Lieferkette

- **Sicherheitsanforderungen bei der Beschaffung:** Informationssicherheitsanforderungen werden für jede Beschaffung von IKT-Produkten oder -Diensten definiert. Die Anforderungen sind proportional zur Kritikalität des Produkts oder Dienstes und decken Vertraulichkeits-, Integritäts- und Verfügbarkeitsaspekte ab. Beschaffungsvorlagen enthalten einen verpflichtenden Abschnitt zu Informationssicherheitsanforderungen.
- **Weitergabe durch Dienstlieferanten:** IKT-Dienstleister werden vertraglich verpflichtet, die Sicherheitsanforderungen der Organisation über die Lieferkette hinweg weiterzugeben, wenn sie Teile des Dienstes in Unterauftrag vergeben. Die Compliance der Unterauftragnehmer wird über das Attestierungs- oder Auditprogramm des Primärlieferanten verifiziert.
- **Weitergabe durch Produktlieferanten:** IKT-Produktlieferanten geben angemessene Sicherheitspraktiken über die Lieferkette hinweg weiter für Produkte, die Komponenten von anderen Lieferanten enthalten, einschließlich Unterauftragnehmern für Softwareentwicklung und Lieferanten von Hardwarekomponenten. Nachweise der Weitergabe werden während des Bewertungsprozesses angefordert.

### 5.2 Transparenz & Komponentendokumentation

- **Software Bill of Materials (SBOM):** IKT-Produktlieferanten stellen Informationen bereit, die die in ihren Produkten verwendeten Softwarekomponenten beschreiben, einschließlich eines SBOM, sofern verfügbar. Das SBOM wird auf bekannte Schwachstellen geprüft und als Teil der Produktsicherheitsdokumentation gepflegt. Für Produkte, die unter den EU Cyber Resilience Act fallen, ist ein SBOM eine verpflichtende Lieferung.
- **Dokumentation von Sicherheitsfunktionen:** IKT-Produktlieferanten stellen Dokumentation bereit, die die umgesetzten Sicherheitsfunktionen ihrer Produkte und die für den sicheren Betrieb erforderliche Konfiguration beschreibt. Diese Dokumentation wird beim Onboarding geprüft und in operativen Sicherheitsverfahren referenziert.
- **Informationsaustausch in der Lieferkette:** Regeln für den Austausch von Informationen über die Lieferkette, potenzielle Probleme und Kompromittierungen werden zwischen der Organisation und ihren Lieferanten festgelegt. Kommunikationskanäle und Eskalationsverfahren für Lieferkettenvorfälle sind definiert.

### 5.3 Validierung & Integrität

- **Compliance-Validierung:** Ein Überwachungsprozess validiert, dass gelieferte IKT-Produkte und -Dienste den genannten Sicherheitsanforderungen entsprechen. Validierungsmethoden umfassen Penetrationstests, unabhängige Sicherheitsbewertungen und die Überprüfung von Drittparteien-Attestierungen für den Informationssicherheitsbetrieb des Lieferanten.
- **Nachverfolgung kritischer Komponenten:** Ein Prozess identifiziert und dokumentiert Produkt- oder Dienstkomponenten, die für die Aufrechterhaltung der Funktionsfähigkeit kritisch sind. Diese Komponenten erhalten verstärkte Prüfung und Nachverfolgung, insbesondere wenn sie außerhalb der Organisation entwickelt werden oder wenn der Lieferant die Komponentenentwicklung an andere Parteien auslagert.
- **Rückverfolgbarkeit in der Lieferkette:** Es wird sichergestellt, dass kritische Komponenten und ihre Herkunft über die gesamte Lieferkette hinweg rückverfolgt werden können. Rückverfolgbarkeitsaufzeichnungen werden für alle als hochkritisch klassifizierten Komponenten geführt.
- **Funktionsintegrität:** Gelieferte IKT-Produkte werden daraufhin überprüft, dass sie wie erwartet funktionieren, ohne unerwartete oder unerwünschte Funktionen. Verifizierungsmethoden umfassen Sicherheitstests, Code-Review für individuell entwickelte Komponenten und Vergleich mit der dokumentierten Spezifikation.
- **Manipulationsschutz & -erkennung:** Prozesse stellen sicher, dass Komponenten von Lieferanten echt und unverändert gegenüber ihrer Spezifikation sind. Zu den Maßnahmen gehören Anti-Manipulations-Etiketten, kryptographische Hash-Verifizierung, Validierung digitaler Signaturen und die Überwachung auf außerhalb der Spezifikation liegende Leistung. Der Manipulationsschutz wird über mehrere Phasen des Systementwicklungslebenszyklus hinweg adressiert.
- **Sicherheitszertifizierung:** Für kritische IKT-Produkte wird durch formale Zertifizierungs- oder Bewertungsschemata wie das Common Criteria Recognition Arrangement, BSI-Zertifizierung oder gleichwertige Frameworks sichergestellt, dass Produkte die erforderlichen Sicherheitsniveaus erreichen.

### 5.4 Komponenten-Lebenszyklusmanagement

- **Komponenten-Lebenszyklusmanagement:** Spezifische Prozesse verwalten den Lebenszyklus und die Verfügbarkeit von IKT-Komponenten und die damit verbundenen Sicherheitsrisiken. Dies umfasst die Planung für Komponenten, die möglicherweise nicht mehr verfügbar sind, weil ein Lieferant den Betrieb einstellt oder ein Produkt aufgrund technologischer Veränderungen abkündigt. Alternative Lieferanten werden im Voraus identifiziert, und der Prozess zur Übertragung von Software und Kompetenz an einen alternativen Lieferanten ist dokumentiert.

## 6. Überwachung, Überprüfung & Änderungsmanagement (A 5.22)

Lieferantendienste werden kontinuierlich überwacht und periodisch überprüft, um sicherzustellen, dass Informationssicherheits-Vertragsbedingungen eingehalten werden, Vorfälle und Probleme ordnungsgemäß bearbeitet werden und Änderungen bei Lieferantendiensten oder Geschäftsstatus die Dienstleistung nicht beeinträchtigen. Eine benannte Lieferantenbeziehungs-Managerin bzw. ein benannter Lieferantenbeziehungs-Manager koordiniert die Überwachungsaktivitäten und berichtet an die Geschäftsleitung. Ausreichende technische Fähigkeiten und Ressourcen stehen zur Verifizierung der Einhaltung der Vertragsanforderungen zur Verfügung. Das Outsourcing-Register konsolidiert alle aktiven Beziehungen mit Status, Leistungsmetriken und Risikobewertungen.

### 6.1 Zu prüfende Änderungskategorien

- **Dienstverbesserungen:** Verbesserungen der aktuellen Dienste des Lieferanten werden vor der Umsetzung auf Sicherheitsauswirkungen bewertet. Der Lieferant stellt eine vorherige Benachrichtigung und Dokumentation aller geplanten Verbesserungen bereit.
- **Neue Anwendungen & Systeme:** Die Entwicklung neuer Anwendungen und Systeme durch den Lieferanten unterliegt dem Änderungsprüfprozess der Organisation. Sicherheitsanforderungen werden vor Beginn der Entwicklung kommuniziert.
- **Änderungen an Richtlinien & Verfahren:** Änderungen oder Aktualisierungen der Sicherheitsrichtlinien und -verfahren des Lieferanten werden auf potenzielle Auswirkungen auf die Sicherheitslage der Organisation überprüft. Wesentliche Änderungen erfordern eine vorherige Genehmigung.
- **Änderungen an Sicherheitsmaßnahmen:** Neue oder geänderte Maßnahmen, die zur Behebung von Vorfällen oder zur Verbesserung der Informationssicherheit eingeführt werden, werden auf Übereinstimmung mit den Sicherheitsanforderungen der Organisation bewertet.
- **Netzwerkänderungen:** Änderungen und Erweiterungen der Netzwerke des Lieferanten, einschließlich solcher, die die Konnektivität zur Organisation beeinflussen, unterliegen einer vorherigen Benachrichtigung und Sicherheitsprüfung.
- **Neue Technologien:** Die Einführung neuer Technologien durch den Lieferanten wird auf potenzielle Sicherheitsimplikationen bewertet, einschließlich Änderungen des Risikoprofils und der Kompatibilität mit der Infrastruktur der Organisation.
- **Produktversionsänderungen:** Die Einführung neuer Produkte oder neuerer Versionen und Releases durch den Lieferanten wird auf Sicherheitsauswirkungen geprüft, einschließlich der potenziellen Einführung neuer Schwachstellen oder Änderungen an Sicherheitskonfigurationen.
- **Änderungen an Entwicklungswerkzeugen:** Neue vom Lieferanten verwendete Entwicklungswerkzeuge und -umgebungen werden auf Sicherheits-Compliance bewertet, insbesondere wenn sie organisatorische Daten verarbeiten oder speichern.
- **Standortverlagerung:** Änderungen am physischen Standort der Lieferanten-Dienststätten werden auf Einhaltung der Datenstandort-Anforderungen, physischen Sicherheitsstandards und jurisdiktionellen Pflichten bewertet.
- **Änderungen bei Unterlieferanten:** Änderungen bei den Unterlieferanten des Lieferanten unterliegen einer vorherigen Benachrichtigung. Die Organisation überprüft die Sicherheitslage neuer Unterlieferanten vor der Genehmigung.
- **Weitere Unterauftragsvergabe:** Die Unterauftragsvergabe von Diensten an zusätzliche Lieferanten erfordert eine vorherige schriftliche Genehmigung. Die Organisation bewertet die Sicherheitsauswirkungen und stellt sicher, dass der neue Unterauftragnehmer gleichwertige Sicherheitsanforderungen erfüllt.

### 6.2 Laufende Überwachung & Überprüfung

- **Service-Level-Überwachung:** Die Dienstleistungsniveaus werden gegen die vereinbarten Metriken überwacht. Abweichungen lösen einen dokumentierten Ausnahmeprozess mit Ursachenanalyse und Planung von Korrekturmaßnahmen aus.
- **Serviceberichte & Fortschrittsgespräche:** Vom Lieferanten erstellte Serviceberichte werden geprüft. Regelmäßige Fortschrittsgespräche werden gemäß der Vereinbarung durchgeführt, mit dokumentierten Protokollen und Aktionspunkten.
- **Lieferantenaudits:** Audits von Lieferanten und Unterlieferanten werden periodisch durchgeführt, ergänzt durch die Überprüfung unabhängiger Auditorberichte, sofern verfügbar. Feststellungen werden über den Korrekturmaßnahmenprozess bis zum Abschluss nachverfolgt.
- **Austausch von Vorfallinformationen:** Informationen über Informationssicherheitsvorfälle werden gemäß der Vereinbarung zwischen der Organisation und dem Lieferanten ausgetauscht. Vorfalltrends werden in regelmäßigen Service-Meetings überprüft.
- **Prüfung von Audit-Trails:** Audit-Trails des Lieferanten und Aufzeichnungen über Sicherheitsereignisse, Betriebsprobleme, Ausfälle und Dienstunterbrechungen werden geprüft. Ursachenanalysen werden für signifikante Ereignisse angefordert.
- **Incident Response:** Identifizierte Informationssicherheitsereignisse oder -vorfälle im Zusammenhang mit Lieferantendiensten werden über den Vorfallmanagement-Prozess der Organisation behandelt und verwaltet, mit Lieferantenkoordination wie in der Vereinbarung definiert.
- **Schwachstellenmanagement:** Informationssicherheitsschwachstellen in Produkten und Diensten des Lieferanten werden identifiziert, bewertet und verwaltet. Kritische Schwachstellen werden über den Schwachstellenmanagement-Prozess der Organisation mit definierten Behebungsfristen eskaliert.
- **Sicherheitsüberprüfung von Unterlieferanten:** Die Informationssicherheitsaspekte der Beziehungen des Lieferanten zu seinen eigenen Lieferanten werden geprüft. Die Organisation verifiziert, dass die Sicherheitsstandards der Unterlieferanten denen entsprechen, die vom Primärlieferanten gefordert werden.
- **Zusicherung der Dienstkontinuität:** Der Lieferant unterhält eine ausreichende Dienstleistungsfähigkeit sowie umsetzbare Pläne, um nach wesentlichen Ausfällen oder Katastrophen die vereinbarten Dienstkontinuitätsniveaus zu gewährleisten. Business-Continuity-Pläne und Disaster-Recovery-Fähigkeiten werden jährlich überprüft.
- **Compliance-Verantwortung:** Lieferanten benennen konkrete Personen, die für die Überprüfung der Einhaltung und die Durchsetzung der Anforderungen der Vereinbarung verantwortlich sind. Kontaktdaten werden aktuell gehalten und der Organisation mitgeteilt.
- **Bewertung des Sicherheitsniveaus:** Die Angemessenheit des Informationssicherheitsniveaus des Lieferanten wird regelmäßig durch eine Kombination aus Selbstbewertungen, Drittparteien-Attestierungen und direkten Audits bewertet. Ergebnisse werden im Lieferantenregister erfasst und fließen in die jährliche Neubewertung des Lieferantenrisikos ein.

## 7. Cloud-Dienste (A 5.23)

Die Nutzung von Cloud-Diensten beinhaltet eine geteilte Verantwortung für Informationssicherheit zwischen dem Cloud-Dienstleister und der Organisation. Die Verantwortlichkeiten beider Parteien sind klar definiert und dokumentiert. Vor der Einführung eines Cloud-Dienstes wird eine Sicherheitsanalyse durchgeführt, die das Dienstmodell (IaaS, PaaS, SaaS), das Bereitstellungsmodell (öffentlich, privat, hybrid) und die anwendbare Rechtsordnung bewertet. Cloud-Dienstvereinbarungen werden geprüft, um sicherzustellen, dass sie die Anforderungen der Organisation an Vertraulichkeit, Integrität, Verfügbarkeit und Informationshandhabung mit angemessenen Service-Level-Zielen und Qualitätszielen adressieren.

### 7.1 Governance von Cloud-Diensten

- **Informationssicherheitsanforderungen:** Alle relevanten Informationssicherheitsanforderungen, die mit jedem Cloud-Dienst verbunden sind, werden dokumentiert, einschließlich Datenklassifizierungsbeschränkungen, regulatorischer Pflichten und technischer Sicherheitsmaßnahmen. Anforderungen werden vor der Beschaffung des Dienstes definiert und in die Bewertungskriterien aufgenommen.
- **Auswahlkriterien & Nutzungsumfang:** Auswahlkriterien für Cloud-Dienste decken Sicherheitszertifizierungen (ISO 27001, SOC 2, C5), Datenstandortoptionen, Verschlüsselungsfähigkeiten, Zugriffskontrollfunktionen, API-Sicherheit und Incident-Response-Reife ab. Der zulässige Nutzungsumfang für jeden Cloud-Dienst wird definiert und an die Nutzer kommuniziert.
- **Cloud-Rollen & -Verantwortlichkeiten:** Rollen und Verantwortlichkeiten für die Nutzung und Verwaltung jedes Cloud-Dienstes sind dokumentiert. Die Zuordnung umfasst Dienstadministration, Sicherheitskonfiguration, Zugriffsmanagement, Überwachung, Vorfallbehandlung und Kostenmanagement.
- **Shared-Responsibility-Modell:** Für jeden Cloud-Dienst dokumentiert eine Shared-Responsibility-Matrix, welche Informationssicherheitsmaßnahmen vom Cloud-Dienstleister und welche von der Organisation verwaltet werden. Die Matrix wird bei jeder Vertragsverlängerung und nach wesentlichen Dienstveränderungen überprüft.
- **Sicherheitsfähigkeiten des Anbieters:** Die Organisation identifiziert und nutzt die von jedem Cloud-Dienstleister bereitgestellten Informationssicherheitsfähigkeiten, einschließlich Verschlüsselung, Identitätsmanagement, Protokollierung, Überwachung und Bedrohungserkennung. Die Konfiguration ist auf die Sicherheitsanforderungen der Organisation abgestimmt.
- **Assurance-Mechanismen:** Assurance über die Sicherheitsmaßnahmen des Cloud-Anbieters wird durch anerkannte Zertifizierungs-Frameworks (C5, ISO 27001, SOC 2 Typ II), vom Cloud-Dienstleister bereitgestellte Compliance-Dashboards und, wo erforderlich, unabhängige Drittbewertungen erlangt.
- **Multi-Cloud-Management:** Wenn mehrere Cloud-Dienste von verschiedenen Anbietern genutzt werden, verwaltet ein konsistenter Ansatz Maßnahmen, Schnittstellen und Änderungen über alle Dienste hinweg. Integrationspunkte werden dokumentiert und Sicherheitskonfigurationen werden harmonisiert, um Lücken zwischen Anbieterumgebungen zu vermeiden.
- **Cloud-Vorfallverfahren:** Verfahren zur Behandlung von Informationssicherheitsvorfällen, die im Zusammenhang mit Cloud-Diensten auftreten, sind dokumentiert. Die Verfahren definieren Kommunikationskanäle mit dem Anbieter, Schritte zur Beweissicherung, forensische Unterstützungsarrangements und Meldepflichten.
- **Laufendes Cloud-Risikomanagement:** Die Organisation überwacht, überprüft und bewertet die fortlaufende Nutzung von Cloud-Diensten zur Steuerung von Informationssicherheitsrisiken. Überprüfungen umfassen Bewertungen der Sicherheitslage, Analysen der Dienstleistungen und mindestens jährliche Verifizierung des Compliance-Status.
- **Exit-Strategie:** Jeder Cloud-Dienst verfügt über eine dokumentierte Exit-Strategie, die Datenexportverfahren, Formatspezifikationen, Terminanforderungen, Löschbestätigung und den Übergang zu einem alternativen Anbieter oder zu interner Infrastruktur abdeckt. Exit-Strategien werden periodisch auf Umsetzbarkeit getestet. Das Konzentrationsrisiko wird bewertet, um kritische Abhängigkeit von einem einzelnen Anbieter zu vermeiden.

### 7.2 Pflichten der Cloud-Dienstleister

- **Architekturstandards:** Cloud-Dienstleister liefern Lösungen auf Basis branchenweit akzeptierter Standards für Architektur und Infrastruktur. Die Einhaltung anerkannter Frameworks wird durch Zertifizierung oder unabhängige Bewertung verifiziert.
- **Zugriffskontrollen:** Die Zugriffskontrollen des Cloud-Dienstes werden so konfiguriert, dass sie den Anforderungen der Organisation entsprechen, einschließlich Multi-Faktor-Authentifizierung, rollenbasierter Zugriffskontrolle, Zuweisung des geringsten Privilegs und Sitzungsmanagement. Administrativer Zugriff ist eingeschränkt und wird protokolliert.
- **Malware-Schutz:** Der Cloud-Dienstleister setzt dem Dienstmodell angemessene Malware-Überwachungs- und Schutzlösungen um. Bei IaaS setzt die Organisation ihren eigenen Endpunktschutz auf bereitgestellten Ressourcen ein.
- **Datenstandort:** Sensible Informationen der Organisation werden nur an genehmigten Standorten innerhalb definierter geografischer Regionen oder Rechtsordnungen verarbeitet und gespeichert. Anforderungen an den Datenstandort sind in der Vereinbarung spezifiziert und werden durch technische Maßnahmen oder Anbieterattestierung verifiziert.
- **Dedizierte Vorfallunterstützung:** Der Cloud-Dienstleister leistet im Falle eines Informationssicherheitsvorfalls in der Cloud-Umgebung dedizierte Unterstützung. Die Unterstützung umfasst eine benannte Sicherheitskontaktperson, definierte Reaktionszeiten und Zusammenarbeitsverfahren für forensische Untersuchungen.
- **Governance der Unterauftragsvergabe:** Die Sicherheitsanforderungen der Organisation bleiben erhalten, wenn Cloud-Dienste weiter an externe Lieferanten untervergeben werden. Die Vereinbarung legt fest, ob Unterauftragsvergabe zulässig ist und, wenn ja, unter welchen Bedingungen. Wo erforderlich, ist die Unterauftragsvergabe untersagt.
- **Unterstützung bei digitalen Beweisen:** Der Cloud-Dienstleister unterstützt die Organisation bei der Sammlung digitaler Beweise unter Berücksichtigung der Gesetze und Vorschriften für digitale Beweise in den geltenden Rechtsordnungen. Beweissicherungsverfahren und Zugriffsmechanismen sind in der Vereinbarung definiert.
- **Exit-Unterstützung & Dienstkontinuität:** Der Cloud-Dienstleister leistet angemessene Unterstützung und erhält die Dienstverfügbarkeit für einen angemessenen Übergangszeitraum aufrecht, wenn die Organisation den Dienst beenden möchte. Mindestübergangszeiträume sind in der Vereinbarung spezifiziert.
- **Sicherung & Wiederherstellung:** Der Cloud-Dienstleister liefert die erforderliche Sicherung von Daten und Konfigurationsinformationen und verwaltet Sicherungen sicher. Sicherungsumfang, -häufigkeit und -aufbewahrung sind auf die Anforderungen der Organisation abgestimmt. Die Wiederherstellungsfähigkeit wird mindestens jährlich getestet.
- **Rückgabe von Daten & Konfiguration:** Der Cloud-Dienstleister gibt Informationen wie Konfigurationsdateien, Quellcode und Daten, die der Organisation gehören, auf Anfrage während der Diensterbringung oder bei Beendigung zurück. Rückgabeformate und -verfahren sind in der Vereinbarung spezifiziert.

### 7.3 Anforderungen zur Änderungsmeldung

- **Infrastrukturänderungen:** Der Cloud-Dienstleister benachrichtigt die Organisation im Voraus über Änderungen an der technischen Infrastruktur, die das Cloud-Dienstangebot beeinflussen, einschließlich Verlagerung, Rekonfiguration oder Änderungen an Hardware oder Software. Der Benachrichtigungszeitraum und der Genehmigungsmechanismus sind in der Vereinbarung definiert.
- **Jurisdiktionsänderungen:** Die Verarbeitung oder Speicherung von Informationen in einer neuen geografischen oder rechtlichen Jurisdiktion erfordert eine vorherige Benachrichtigung und ausdrückliche Genehmigung der Organisation. Die Sicherheits- und Compliance-Implikationen der Jurisdiktionsänderung werden vor der Genehmigung bewertet.
- **Änderungen bei Unterauftragnehmern:** Der Cloud-Dienstleister benachrichtigt die Organisation vor der Nutzung neuer oder der Änderung bestehender Unterauftragnehmer für die Erbringung von Cloud-Diensten. Die Organisation prüft die Sicherheitslage der neuen Partei vor der Genehmigung.

Die Organisation pflegt engen Kontakt zu ihren Cloud-Dienstleistern. Diese Kontakte ermöglichen den gegenseitigen Austausch von Informationen über Informationssicherheit bei der Nutzung von Cloud-Diensten, einschließlich Mechanismen, mit denen beide Parteien Dienstmerkmale überwachen und Versäumnisse bei der Erfüllung vereinbarter Dienstziele melden können.

## 8. Rollen & Verantwortlichkeiten

- **Geschäftsleitung:** Genehmigt diese Richtlinie, die Outsourcing-Strategie und Risikoakzeptanzentscheidungen für Lieferantenbeziehungen. Stellt Ressourcen für das Lieferanten-Sicherheitsmanagement bereit.
- **Informationssicherheitsbeauftragte/r (ISB):** Definiert Informationssicherheitsanforderungen für Lieferantenvereinbarungen, führt oder koordiniert Sicherheitsbewertungen von Lieferanten durch, prüft Auditergebnisse und berät zu Risikobehandlungsentscheidungen im Zusammenhang mit Lieferanten.
- **Lieferantenbeziehungs-Manager/in:** Pflegt das Lieferanten- und Outsourcing-Register, koordiniert laufende Überwachungsaktivitäten, verwaltet den Lebenszyklus von Vereinbarungen und erstellt regelmäßige Lieferantenstatusberichte für die Geschäftsleitung.
- **Beschaffung:** Stellt sicher, dass die standardisierte Vertragsvorlage mit Sicherheitsklauseln für alle Lieferantenvereinbarungen verwendet wird. Bezieht Informationssicherheits- und Rechtsvertreter in Vertragsverhandlungen ein.
- **IT-Betrieb:** Setzt technische Maßnahmen für den Lieferantenzugriff um und verwaltet sie, überwacht sicherheitsrelevante Ereignisse im Zusammenhang mit Lieferanten und koordiniert mit Lieferanten bei Incident Response und Schwachstellenbehebung.
- **Recht & Compliance:** Prüft vertragliche Klauseln auf rechtliche Hinlänglichkeit, berät zu Datenschutz- und regulatorischen Pflichten und unterstützt Streitbeilegungsprozesse.
- **Prozesseigentümer:** Definieren geschäftliche Anforderungen an ausgelagerte Dienste, nehmen an Lieferantenbewertungen teil und genehmigen Service-Level-Ziele für ihre jeweiligen Prozesse.
- **Alle Beschäftigten:** Befolgen die Spielregeln für Lieferanteninteraktionen und melden vermutete Sicherheitsvorfälle im Zusammenhang mit Lieferantenpersonal oder -diensten.

## 9. Überprüfung & Pflege

Diese Richtlinie wird überprüft:

- Mindestens jährlich im Rahmen des ISMS-Managementbewertungszyklus.
- Nach wesentlichen Informationssicherheitsvorfällen mit Lieferantenbezug.
- Wenn sich die Lieferantenlandschaft wesentlich ändert, einschließlich Onboarding neuer kritischer Lieferanten oder Beendigung wesentlicher Beziehungen.
- Nach Änderungen rechtlicher, regulatorischer oder vertraglicher Anforderungen, die das Lieferantenmanagement betreffen.
- Nach Auditfeststellungen, die wesentliche Lücken im Lieferanten-Sicherheitsmanagement aufdecken.
- Wenn Threat Intelligence erhöhte Risiken in der Lieferkette signalisiert.
