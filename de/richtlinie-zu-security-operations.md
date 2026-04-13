# Richtlinie zu Security Operations

> **Dokumentenkontrolle**  
> Eigentümer: [RICHTLINIEN_EIGENTÜMER_ROLLE, z. B. Informationssicherheitsbeauftragte/r]  
> Genehmigt von: [GENEHMIGER_NAME_UND_ROLLE]  
> Version: [VERSION]  
> Gültig ab: [GÜLTIGKEITSDATUM]  
> Nächste Überprüfung: [NÄCHSTES_ÜBERPRÜFUNGSDATUM]

## 1. Rechtliche/Regulatorische Grundlage

ISO/IEC 27001:2022 / ISO/IEC 27002:2022, Anhang A — Organisatorische & Technologische Maßnahmen:

- A 5.5 — Kontakt mit Behörden
- A 5.6 — Kontakt mit speziellen Interessensgruppen
- A 5.7 — Threat Intelligence
- A 5.24 — Planung und Vorbereitung des Informationssicherheits-Vorfallmanagements
- A 5.25 — Bewertung und Entscheidung über Informationssicherheitsereignisse
- A 5.26 — Reaktion auf Informationssicherheitsvorfälle
- A 5.27 — Lernen aus Informationssicherheitsvorfällen
- A 5.28 — Sammlung von Beweismitteln
- A 8.8 — Handhabung technischer Schwachstellen
- A 8.32 — Änderungsmanagement

BSI IT-Grundschutz:

- DER.2.1 — Behandlung von Sicherheitsvorfällen (A1 Vorfalldefinition, A2 Richtlinie zur Vorfallbehandlung, A3 Verantwortlichkeiten, A4 Benachrichtigung, A5 Behebung, A6 Wiederherstellung, A7 Verfahren, A8 Organisatorische Strukturen, A9 Meldewege, A10 Eindämmung, A11 Klassifizierung, A14 Eskalationsstrategie, A16 Dokumentation der Behebung, A17 Nachbereitung, A18 Prozessverbesserung, A22 Effizienzüberprüfung)
- DER.1 — Detektion sicherheitsrelevanter Ereignisse (A1 Detektionsrichtlinie, A3 Meldewege, A4 Sensibilisierung der Beschäftigten, A5 Eingebaute Detektionsfunktionen, A6 Kontinuierliche Überwachung, A12 Auswertung externer Informationen)
- DER.2.2 — IT-Forensik (A1 Rechtlicher Rahmen, A2 First-Response-Leitfaden, A3 Vorauswahl forensischer Dienstleister, A5 Beweissicherungsverfahren, A8 Reihenfolge der Volatilität, A10 Forensische Duplizierung, A11 Dokumentation, A12 Sichere Aufbewahrung)
- OPS.1.1.1 — Allgemeiner IT-Betrieb (A9 IT-Monitoring, A10 Schwachstelleninventar, A20 Schwachstellentests, A22 Automatisierte Tests)
- OPS.1.1.3 — Patch- und Änderungsmanagement (A1 Konzept, A2 Verantwortlichkeiten, A3 Autoupdate-Konfiguration, A5 Änderungsanträge, A6 Koordination, A7 Integration in Geschäftsprozesse, A10 Integritätsprüfung, A15 Regelmäßige Updates)

Weitere jurisdiktionsspezifische Gesetze — insbesondere NIS2, sektorspezifische Meldepflichten, Datenschutzrecht (DSGVO Artikel 33/34 Meldepflichten), Strafprozessrecht und Regeln zur Zulässigkeit digitaler Beweise — sind im Rechtsregister aufgeführt und werden durch Verweis einbezogen.

## 2. Zweck & Geltungsbereich

Diese Richtlinie legt den Rahmen für Security Operations bei **[IHR_ORGANISATIONSNAME]** fest. Sie definiert die Anforderungen für die externe Kommunikation mit Behörden und Interessensgruppen, die Sammlung und Nutzung von Threat Intelligence, den vollständigen Vorfallmanagement-Lebenszyklus von der Planung über die Reaktion bis zu Lessons Learned, das Management technischer Schwachstellen und die Governance von Änderungen an Informationssystemen.

Diese Richtlinie gilt für:

- Alle Informationssysteme, Anwendungen und die IT-Infrastruktur, die von oder im Auftrag der Organisation betrieben werden
- Alle Personen, die an Security Operations, Incident Response, Schwachstellenmanagement und Änderungsmanagement beteiligt sind
- Externe Dienstleister, Cloud-Anbieter und Auftragnehmer mit Zugriff auf organisatorische Systeme
- Alle Informationssicherheitsereignisse, -vorfälle und -schwachstellen unabhängig vom Ursprung

Ziel ist es, sicherzustellen, dass die Organisation Informationssicherheitsbedrohungen strukturiert, zeitnah und wirksam verhindern, erkennen, darauf reagieren und sich von ihnen erholen kann, während der operative Betrieb und die Rechtskonformität aufrechterhalten werden.

## 3. Externe Beziehungen & Kommunikation

[IHR_ORGANISATIONSNAME] pflegt etablierte Beziehungen zu relevanten Behörden, um eine zeitnahe Meldung von Informationssicherheitsvorfällen zu ermöglichen, bevorstehende regulatorische Erwartungen zu verstehen und Frühwarnungen zu Bedrohungen zu erhalten. Die Organisation legt fest, wann und von wem Behörden kontaktiert werden und wie identifizierte Informationssicherheitsvorfälle gemeldet werden.

### 3.1 Register der Behördenkontakte

Die Organisation pflegt ein aktuelles Register der Behördenkontakte. Das Register spezifiziert die Kontaktdaten, die Umstände, unter denen Kontakt aufgenommen wird, die verantwortliche interne Ansprechperson und die Kommunikationsmethode für jeden der folgenden Behördentypen:

- **Strafverfolgungsbehörden:** Kontaktdaten der relevanten Strafverfolgungsbehörden sind dokumentiert, einschließlich der Kriterien, die eine Meldepflicht auslösen (z. B. Verdacht auf Straftaten, Datenschutzverletzungen oberhalb gesetzlicher Schwellenwerte). Die/der Informationssicherheitsbeauftragte stimmt sich vor der Kontaktaufnahme mit der Rechtsberatung ab.
- **Regulierungsbehörden:** Kontakte zu sektorspezifischen Regulierungsbehörden werden gepflegt. Meldefristen und -formate, die durch geltende Vorschriften vorgeschrieben sind, sind dokumentiert und werden geübt. Regulatorische Meldepflichten bei Datenschutzverletzungen (z. B. innerhalb von 72 Stunden nach DSGVO) werden eingehalten.
- **Aufsichtsbehörden:** Kontaktdaten für Datenschutz-Aufsichtsbehörden und andere relevante Aufsichtsgremien sind aktuell. Die Organisation verfolgt behördliche Leitlinien und integriert deren Erwartungen in ihre Security Operations.
- **Versorgungsunternehmen:** Kontaktdaten für Vermieter, Wasser- und Stromversorger sind dokumentiert. Verfahren zur Benachrichtigung dieser Parteien bei physischen Sicherheitsvorfällen oder Umweltnotfällen sind etabliert.
- **Rettungsdienste:** Direkte Kommunikationswege zu Rettungsdiensten sind etabliert und getestet. Alle Personen sind über die Verfahren zur Kontaktaufnahme mit Rettungsdiensten im Falle eines physischen oder umweltbezogenen Notfalls informiert.
- **Feuerwehr:** Kontaktdaten der örtlichen Feuerwehr sind an allen Standorten sichtbar ausgehängt. Koordinationsverfahren für Feuerübungen und Evakuierungspläne sind dokumentiert.
- **Telekommunikationsanbieter:** Kontaktdaten für Telekommunikationsanbieter werden zur Meldung von Dienststörungen, zur Anforderung von Notrufleitungen und zur Koordination von Incident-Response-Aktivitäten im Zusammenhang mit der Netzwerkinfrastruktur gepflegt.

Das Register der Behördenkontakte wird mindestens jährlich überprüft und bei organisatorischen, regulatorischen oder personellen Änderungen aktualisiert. Der Kontakt zu Behörden wird auch proaktiv genutzt, um aktuelle und bevorstehende Erwartungen dieser Behörden in Bezug auf geltende Informationssicherheitsvorschriften zu verstehen.

Wenn ein Sicherheitsvorfall eintritt, werden alle betroffenen internen und externen Parteien umgehend benachrichtigt. Vor der Benachrichtigung externer Parteien prüft die Organisation, ob die/der Datenschutzbeauftragte, der Betriebsrat bzw. die Personalvertretung und die Rechtsabteilung einzubeziehen sind. Verpflichtende Meldepflichten an Behörden und regulierte Sektoren werden im Voraus unter dem geltenden nationalen Aufsichtsrecht identifiziert und regelmäßig geübt. Die Organisation pflegt vorformulierte Benachrichtigungsvorlagen für jeden Behördentyp, um die Reaktionszeiten zu verkürzen.

### 3.2 Einbindung in spezielle Interessensgruppen

[IHR_ORGANISATIONSNAME] nimmt an relevanten speziellen Interessensgruppen, Berufsverbänden, Sicherheitsforen und Informationsaustauschgemeinschaften teil. Die Mitgliedschaft in solchen Gruppen dient folgenden Zwecken:

- **Austausch bewährter Praktiken:** Die Organisation verbessert ihr Wissen über Best Practices der Informationssicherheit und bleibt durch die aktive Teilnahme an Fachgruppen und Branchenverbänden über relevante Sicherheitsinformationen auf dem aktuellen Stand.
- **Aktuelles Lagebewusstsein:** Die Teilnahme an Interessensgruppen stellt sicher, dass das Verständnis der Organisation für das Informationssicherheitsumfeld aktuell bleibt. Mitglieder erhalten Briefings, Publikationen und Aktualisierungen, die die neuesten Entwicklungen widerspiegeln.
- **Frühwarnungen:** Durch Mitgliedschaften und Abonnements erhält die Organisation Frühwarnungen zu Meldungen, Advisories und Patches im Zusammenhang mit Angriffen und Schwachstellen. Dies umfasst Advisories von CERTs, ISACs und Sicherheitsbulletins der Hersteller.
- **Fachberatung:** Die Organisation erhält über ihr Netzwerk an Interessensgruppenkontakten Zugang zu fachlicher Beratung zur Informationssicherheit. Dazu gehört die Expertenberatung zu aufkommenden Bedrohungen, Compliance-Herausforderungen und Techniken der Incident Response.
- **Informationsaustausch:** Die Organisation teilt und tauscht Informationen über neue Technologien, Produkte, Dienste, Bedrohungen und Schwachstellen mit vertrauenswürdigen Partnern. Vereinbarungen zum Informationsaustausch regeln die Vertraulichkeit und zulässige Nutzung ausgetauschter Informationen.
- **Vorfallbezogene Zusammenarbeit:** Mitgliedschaften in Interessensgruppen bieten geeignete Anknüpfungspunkte bei der Bearbeitung von Informationssicherheitsvorfällen und ermöglichen eine koordinierte Reaktion mit Partnerorganisationen und sektorspezifischen Incident-Response-Teams.

Die/der Informationssicherheitsbeauftragte führt ein Register aller Mitgliedschaften und Abonnements, bewertet deren Nutzen jährlich und stellt sicher, dass empfangene Informationen an relevante Personen innerhalb der Organisation verteilt werden.

Über externe Kanäle empfangene Informationen werden systematisch bewertet. Alle Personen erkennen Nachrichten über diese Kanäle als potenziell sicherheitsrelevant und leiten sie an die zuständige interne Anlaufstelle weiter. Informationen aus zuverlässigen Quellen — einschließlich BSI-Advisories, CERT-Bund-Warnungen, sektorspezifischer ISACs und Herstellerbulletins — werden auf ihre Relevanz für den eigenen Informationsbereich der Organisation bewertet. Wo die Informationen relevant sind, werden sie gemäß dem Vorfallmanagement-Prozess eskaliert.

## 4. Threat Intelligence (A 5.7)

[IHR_ORGANISATIONSNAME] nutzt Threat Intelligence, um Bedrohungen zu verhindern, zu erkennen und auf sie zu reagieren. Informationen über bestehende oder aufkommende Bedrohungen werden gesammelt und analysiert, um informierte Maßnahmen zu ermöglichen, die verhindern, dass Bedrohungen der Organisation schaden, und die Auswirkungen solcher Bedrohungen zu reduzieren. Die gesammelte Threat Intelligence ist relevant (bezogen auf den Schutz der Organisation), aufschlussreich (bietet ein genaues Verständnis der Bedrohungslage), kontextbezogen (ergänzt Situationsbewusstsein auf Basis des Zeitpunkts, des Auftretens und der Verbreitung von Ereignissen in vergleichbaren Organisationen) und handlungsfähig (ermöglicht der Organisation ein schnelles und wirksames Handeln).

### 4.1 Intelligence-Ebenen

Threat Intelligence ist in drei Ebenen strukturiert, die alle berücksichtigt werden:

- **Strategische Threat Intelligence:** Informationen auf hoher Ebene über die sich verändernde Bedrohungslage werden ausgetauscht, einschließlich Angreifertypen, Motivationen, geopolitischer Entwicklungen und aufkommender Angriffskategorien, die für den Sektor und die geografische Präsenz der Organisation relevant sind.
- **Taktische Threat Intelligence:** Informationen über Angreifermethoden, -werkzeuge und -technologien werden gesammelt und analysiert. Dies umfasst Taktiken, Techniken und Verfahren (TTPs), die von Bedrohungsakteuren verwendet werden, und ermöglicht es der Organisation, ihre Abwehr gegen bekannte Angriffsmuster zu stärken.
- **Operative Threat Intelligence:** Details zu spezifischen Angriffen werden gesammelt, einschließlich technischer Indicators of Compromise (IoCs) wie IP-Adressen, Domainnamen, Datei-Hashes und Malware-Signaturen. Diese Indikatoren fließen in technische Detektions- und Präventionssysteme ein.

### 4.2 Intelligence-Aktivitäten

Der Threat-Intelligence-Prozess umfasst die folgenden Aktivitäten:

- **Zielsetzung:** Die Organisation legt klare Ziele für die Threat-Intelligence-Produktion fest, abgestimmt auf ihr Risikoprofil, den Branchensektor und die von ihr geschützten Informationswerte.
- **Quellenauswahl:** Interne und externe Informationsquellen, die für die Threat-Intelligence-Produktion notwendig und geeignet sind, werden identifiziert, geprüft und ausgewählt. Quellen umfassen CERT-Bund-CSAF-Feeds, CERT-EU Cyber Briefs, nationale CSIRT-Feeds (NCSC UK, BSI-Cyber-Sicherheits-Warnungen), Branchen-ISACs, kommerzielle Threat-Feeds, Open-Source-Intelligence und interne Telemetriedaten.
- **Sammlung:** Informationen werden kontinuierlich aus ausgewählten internen und externen Quellen gesammelt. Automatisierte Feeds werden durch manuelle Recherche und Human Intelligence aus der Teilnahme an der Sicherheitscommunity ergänzt. Advisories werden mit CISA-Known-Exploited-Vulnerabilities-Daten (KEV) angereichert, um aktiv ausgenutzte Bedrohungen zu identifizieren, und mit EPSS-Werten (Exploit Prediction Scoring System), um die Ausnutzungswahrscheinlichkeit innerhalb von 30 Tagen zu bewerten.
- **Verarbeitung:** Gesammelte Informationen werden zur Vorbereitung der Analyse verarbeitet. Die Verarbeitung umfasst Übersetzen, Formatieren, Normalisieren, Deduplizieren und Abgleichen von Informationen aus mehreren Quellen.
- **Analyse:** Verarbeitete Informationen werden analysiert, um zu verstehen, wie sie sich auf die Organisation beziehen und welche Bedeutung sie für sie haben. Die Analyse bewertet die Glaubwürdigkeit der Quelle, die Relevanz für die Werte der Organisation und die potenziellen Auswirkungen identifizierter Bedrohungen.
- **Verbreitung:** Analysierte Threat Intelligence wird an relevante Personen in einem Format kommuniziert und geteilt, das verstanden und umgesetzt werden kann. Strategische Intelligence wird dem Management bereitgestellt, taktische Intelligence den Sicherheitsarchitekten und operative Intelligence dem Security-Operations-Team.

### 4.3 Nutzung von Threat Intelligence

Analysierte Threat Intelligence wird auf folgende Weise genutzt:

- **Integration in das Risikomanagement:** Prozesse werden umgesetzt, um aus Threat-Intelligence-Quellen gewonnene Informationen in die Informationssicherheits-Risikomanagement-Prozesse der Organisation aufzunehmen, sodass das Risikoregister die aktuelle Bedrohungslage widerspiegelt. Automatisiertes Asset-Matching vergleicht Produktnamen aus Advisories mit dem IT-Asset-Verzeichnis der Organisation, um relevante Bedrohungen ohne manuelle Überprüfung zu identifizieren.
- **Technische Maßnahmen:** Threat Intelligence dient als zusätzliche Eingabe für technische präventive und detektive Maßnahmen wie Firewalls, Intrusion-Detection-Systeme, SIEM-Plattformen und Anti-Malware-Lösungen.
- **Sicherheitstests:** Threat Intelligence liefert Input für Informationssicherheits-Testprozesse und -techniken, einschließlich Penetrationstestszenarien und Red-Team-Übungen.

Die Organisation integriert Threat Intelligence in die operative IT-Überwachung. Alle IT-Komponenten sind in eine einheitliche Überwachungsumgebung eingebunden, die relevante Parameter erfasst und Alarme auslöst, wenn definierte Schwellenwerte überschritten werden. Überwachungsergebnisse fließen in ein Schwachstelleninventar ein, in dem bekannte Schwachstellen aller betriebenen IT-Komponenten und der Bearbeitungsstatus jeder Schwachstelle zentral erfasst und gepflegt werden. Die IT-Betriebsfunktion bezieht regelmäßig Informationen über neu bekannt gewordene Schwachstellen, die eingesetzte Plattformen, Firmware, Betriebssysteme, Anwendungen und Dienste betreffen, analysiert diese Informationen für den spezifischen Betriebskontext und leitet entsprechende Behebungsmaßnahmen ein.

## 5. Planung & Vorbereitung des Vorfallmanagements (A 5.24)

[IHR_ORGANISATIONSNAME] etabliert angemessene Informationssicherheits-Vorfallmanagement-Prozesse. Die Ziele für das Vorfallmanagement werden mit dem Management vereinbart, und die für das Vorfallmanagement Verantwortlichen verstehen die Prioritäten der Organisation für die Behandlung von Vorfällen, einschließlich Bearbeitungsfristen auf Basis der potenziellen Folgen und Schweregrade.

Eine klare Definition unterscheidet Sicherheitsvorfälle von routinemäßigen Betriebsstörungen. Alle an der Vorfallbehandlung beteiligten Personen kennen diese Definition. Die Eintrittsschwellen für einen Sicherheitsvorfall sind auf den Schutzbedarf der betroffenen Geschäftsprozesse, IT-Systeme und Anwendungen abgestimmt. Eine dedizierte Sicherheitsrichtlinie zur Detektion sicherheitsrelevanter Ereignisse wird aus der übergreifenden Sicherheitsrichtlinie abgeleitet und legt fest, wie die Detektion geplant, umgesetzt und betrieben wird. Diese Detektionsrichtlinie ist allen zugewiesenen Detektionsbeschäftigten bekannt und wird regelmäßig überprüft.

### 5.1 Rollen & Verantwortlichkeiten

Rollen und Verantwortlichkeiten zur Durchführung der Vorfallmanagement-Verfahren werden festgelegt und an alle relevanten internen und externen interessierten Parteien kommuniziert. Es gelten folgende Grundsätze:

- **Einheitliche Meldemethode:** Eine einheitliche Methode zur Meldung von Informationssicherheitsereignissen wird etabliert, einschließlich einer klar benannten Ansprechstelle, die allen Personen bekannt ist. Der Meldeweg ist rund um die Uhr erreichbar.
- **Vorfallmanagement-Prozess:** Der Vorfallmanagement-Prozess folgt einem sechsstufigen Workflow: Gemeldet, Triage, Untersuchung, Eindämmung, Behebung und Abschluss. Jede Phase hat definierte Eingaben, Entscheidungskriterien und Ausgaben. Der Prozess gibt der Organisation die Fähigkeit, Informationssicherheitsvorfälle zu verwalten, einschließlich Administration, Dokumentation, Detektion, Triage, Priorisierung, Analyse, Kommunikation und Koordination interessierter Parteien.
- **Incident-Response-Prozess:** Ein Incident-Response-Prozess gibt der Organisation die Fähigkeit, Informationssicherheitsvorfälle zu bewerten, auf sie zu reagieren und aus ihnen zu lernen. Der Reaktionsprozess umfasst definierte Eskalationspfade und Entscheidungskriterien.
- **Kompetentes Personal:** Nur kompetentes Personal behandelt Themen im Zusammenhang mit Informationssicherheitsvorfällen innerhalb der Organisation. Kompetenzanforderungen sind für jede Vorfallmanagement-Rolle definiert.
- **Verfahrensdokumentation & Schulung:** Personen, die mit der Behandlung von Informationssicherheitsvorfällen beauftragt sind, erhalten Verfahrensdokumentation und regelmäßige Schulungen. Die Schulungen umfassen Tabletop-Übungen und simulierte Vorfallszenarien.
- **Zertifizierung & Entwicklung:** Ein Prozess zur Identifikation erforderlicher Schulungen, Zertifizierungen und fortlaufender beruflicher Weiterbildung für Incident-Response-Personal ist etabliert. Relevante Zertifizierungen (z. B. GCIH, GCIA, OSCP) werden von der Organisation unterstützt.

Ein dediziertes Incident-Response-Team wird gebildet, dessen Mitglieder je nach Art des Vorfalls einberufen werden. Geeignete Mitglieder werden vor Eintritt eines Vorfalls identifiziert, benannt und über ihre Pflichten eingewiesen. Die Zusammensetzung des Teams wird regelmäßig überprüft und bei Bedarf aktualisiert. Die Schnittstellen zwischen Vorfallbehandlung, Fehler- und Störungsmanagement (IT-Service-Desk) und Notfallmanagement werden analysiert, gemeinsam genutzte Ressourcen werden identifiziert und alle beteiligten Beschäftigten werden für die jeweiligen Domänen sensibilisiert. Die Sicherheitsmanagementfunktion hat Lesezugriff auf die eingesetzten Vorfallmanagement-Werkzeuge.

### 5.2 Verfahren des Vorfallmanagements

Die Geschäftsleitung stellt sicher, dass ein Informationssicherheits-Vorfallmanagement-Plan erstellt wird, der verschiedene Szenarien berücksichtigt. Verfahren werden für die folgenden Aktivitäten entwickelt und umgesetzt:

- **Ereignisbewertung:** Informationssicherheitsereignisse werden nach definierten Kriterien bewertet, die einen Informationssicherheitsvorfall ausmachen. Klare Schwellenwerte unterscheiden Sicherheitsereignisse von Betriebsstörungen, abgestimmt auf den Schutzbedarf der betroffenen Geschäftsprozesse.
- **Detektion & Klassifizierung:** Informationssicherheitsereignisse und -vorfälle werden durch menschliche und automatische Mittel überwacht, erkannt, klassifiziert, analysiert und gemeldet. Detektionsfähigkeiten sind in die Protokollierungsinfrastruktur und SIEM-Systeme der Organisation integriert.
- **Lebenszyklusmanagement von Vorfällen:** Informationssicherheitsvorfälle werden bis zum Abschluss verwaltet, einschließlich Reaktion und Eskalation je nach Art und Kategorie des Vorfalls, möglicher Aktivierung von Krisenmanagement- und Kontinuitätsplänen, kontrollierter Wiederherstellung nach einem Vorfall und Kommunikation mit internen und externen interessierten Parteien. Wenn ein Informationssicherheitsvorfall auch eine Verletzung personenbezogener Daten darstellt, wird ein verknüpfter Breach-Vorfall angelegt, und beide Vorfälle behalten eine bidirektionale Referenz.
- **Externe Koordination:** Die Koordination mit internen und externen interessierten Parteien wie Behörden, externen Interessensgruppen und Foren, Lieferanten und Kunden ist im Vorfallmanagement-Plan festgelegt.
- **Aktivitätsprotokollierung:** Alle Vorfallmanagement-Aktivitäten werden protokolliert. Das Protokoll erfasst den Zeitverlauf der Ereignisse, getroffene Entscheidungen, durchgeführte Maßnahmen und beteiligtes Personal.
- **Umgang mit Beweismitteln:** Verfahren zum Umgang mit Beweismitteln sind in den Vorfallmanagement-Prozess integriert, um sicherzustellen, dass forensische Anforderungen von den frühesten Phasen der Vorfallerkennung an erfüllt werden.
- **Ursachenanalyse:** Ursachenanalyseverfahren (Post-Mortem) werden für alle signifikanten Vorfälle durchgeführt. Die Analyse identifiziert die technischen und organisatorischen Faktoren, die zum Vorfall beigetragen haben.
- **Lessons Learned:** Lessons Learned und erforderliche Verbesserungen der Vorfallmanagement-Verfahren oder Informationssicherheitsmaßnahmen werden identifiziert, dokumentiert und bis zur Umsetzung nachverfolgt.

### 5.3 Meldeverfahren

Die Vorfallmeldeverfahren umfassen die folgenden Elemente:

- **Sofortmaßnahmen:** Klare Anweisungen legen die bei einem Informationssicherheitsereignis zu ergreifenden Maßnahmen fest, etwa die sofortige Erfassung aller relevanten Details (auftretende Störung, Bildschirmmeldungen), die umgehende Meldung an die Ansprechstelle und nur die Durchführung koordinierter Maßnahmen.
- **Vorfallformulare:** Standardisierte Formulare zur Vorfallmeldung unterstützen die Beschäftigten dabei, alle notwendigen Maßnahmen beim Melden von Informationssicherheitsvorfällen durchzuführen. Die Formulare erfassen Ereignistyp, betroffene Systeme, Zeitverlauf, erste Bewertung und ergriffene Maßnahmen.
- **Feedback-Mechanismen:** Geeignete Feedback-Prozesse stellen sicher, dass Personen, die Informationssicherheitsereignisse melden, soweit möglich über die Ergebnisse nach Abschluss der Bearbeitung informiert werden.
- **Vorfallberichte:** Formale Vorfallberichte werden für alle bestätigten Vorfälle erstellt. Berichte dokumentieren den Vorfallzeitverlauf, die Auswirkungen, die Ursache, Reaktionsmaßnahmen und Empfehlungen.
- **Externe Meldung:** Alle externen Anforderungen zur Meldung von Vorfällen an relevante interessierte Parteien innerhalb definierter Fristen werden erfüllt. Dazu gehören Meldepflichten bei Datenschutzverletzungen an Aufsichtsbehörden (z. B. innerhalb von 72 Stunden nach DSGVO), sektorspezifische Meldepflichten und vertragliche Benachrichtigungsanforderungen.

Geeignete Melde- und Alarmwege für sicherheitsrelevante Ereignisse sind dokumentiert und legen fest, welche Parteien wann zu informieren sind, wie jede Person erreicht werden kann und welche Kommunikationsmethode je nach Dringlichkeit verwendet wird. Alle für die Alarmierungskette relevanten Personen sind über ihre Pflichten informiert. Melde- und Alarmwege werden regelmäßig getestet, geübt und aktualisiert.

Eine Eskalationsstrategie wird zwischen der Fehlermanagement-Funktion und der Informationssicherheitsmanagement-Funktion formuliert und abgestimmt. Die Eskalationsstrategie enthält klare Anweisungen, die festlegen, wer über welchen Kanal bei welcher Art von vermuteter oder bestätigter Sicherheitsstörung zu welchem Zeitpunkt einzubeziehen ist. Sie spezifiziert die Maßnahmen, die einer Eskalation folgen, und wie die Organisation reagiert. Geeignete Werkzeuge — etwa Ticketsysteme, die in der Lage sind, vertrauliche Informationen zu verarbeiten und während Vorfällen oder Notfällen verfügbar zu bleiben — werden für diesen Zweck ausgewählt. Die Eskalationsstrategie und die zugehörigen Checklisten für den Service-Desk werden regelmäßig überprüft und geübt, auch durch Tabletop-Übungen.

Informationssicherheitsvorfälle können Organisations- und Landesgrenzen überschreiten. Um auf solche Vorfälle zu reagieren, koordiniert die Organisation Reaktionsaktivitäten und teilt Informationen über Vorfälle mit externen Organisationen, wie angemessen und unter Beachtung der Vertraulichkeitsanforderungen und Vereinbarungen zum Informationsaustausch.

## 6. Ereignisbewertung & Klassifizierung (A 5.25)

- **Kategorisierungs- & Priorisierungsschema:** [IHR_ORGANISATIONSNAME] verwendet ein vereinbartes Kategorisierungs- und Priorisierungsschema für Informationssicherheitsvorfälle, das die Identifikation der Folgen und der Priorität jedes Vorfalls ermöglicht. Die Schweregradbewertung verwendet eine vierstufige Skala (Kritisch, Hoch, Mittel, Niedrig) mit definierten Kriterien für jede Stufe. Die Ansprechstelle bewertet jedes Informationssicherheitsereignis nach diesem Schema. Das Schema klassifiziert Ereignisse nach Schweregrad, Typ (Vertraulichkeitsverletzung, Integritätsverletzung, Verfügbarkeitsstörung, kombiniert), betroffenen Assets und Geschäftsauswirkungen.

Personen, die für die Koordination und Reaktion auf Informationssicherheitsvorfälle verantwortlich sind, führen die Bewertung durch und treffen Entscheidungen über Informationssicherheitsereignisse. Die Ergebnisse der Bewertung und Entscheidung werden detailliert zum Zweck der späteren Referenz und Verifizierung erfasst. Der Klassifizierungsprozess ist zwischen dem Sicherheitsmanagement und der operativen Vorfallmanagement-Funktion (Service-Desk) abgestimmt, um widersprüchliche Bewertungen zu vermeiden.

### 6.1 Detektion sicherheitsrelevanter Ereignisse

Die Detektion sicherheitsrelevanter Ereignisse umfasst organisatorische, personelle und technische Maßnahmen mit dem Ziel, Bedrohungen und Angriffe so früh wie möglich zu identifizieren. Es gelten die folgenden Grundsätze:

- **Kontinuierliche Überwachung:** Alle Protokolldaten werden kontinuierlich überwacht und auf Anomalien ausgewertet. Benannte Beschäftigte werden dieser Aufgabe zugewiesen und erhalten dokumentierte Verfahrensanweisungen zur aktiven Suche nach sicherheitsrelevanten Ereignissen in System-, Anwendungs- und Netzwerkverkehrsprotokollen. Es werden ausreichende personelle Ressourcen zur Aufrechterhaltung der erforderlichen Überwachungsabdeckung bereitgestellt.
- **Eingebaute Detektionsfunktionen:** Detektionsfunktionen, die in eingesetzten IT-Systemen und Anwendungen verfügbar sind, werden aktiviert und genutzt. Gesammelte Ereignismeldungen werden in definierten Intervallen überprüft. Bei Verdacht auf einen Vorfall werden die Ereignismeldungen des betroffenen Systems und benachbarter Systeme abgeglichen, um den Umfang und die Ausbreitung des Ereignisses zu bestimmen.
- **Zentrale Protokollierungsinfrastruktur:** Ereignismeldungen von IT-Systemen und Anwendungen werden zentral aggregiert und mit geeigneten Werkzeugen analysiert. Die Signaturen und Regelwerke von Detektionssystemen werden aktuell gehalten, sodass sicherheitsrelevante Ereignisse auch rückwirkend identifiziert werden können.
- **Schwellwertbasierte Alarmierung:** Für sicherheitsrelevante Ereignisse werden Schwellenwerte definiert. Bei Überschreiten der Schwellenwerte werden automatisierte Alarme ausgelöst. Die Alarmierung berücksichtigt die Schwere des Ereignisses und den Schutzbedarf der betroffenen Systeme. Die Schwellenwerte werden regelmäßig überprüft und angepasst, um False Positives zu minimieren und die Detektionsqualität zu erhalten.
- **Sensibilisierung der Beschäftigten:** Alle Beschäftigten werden sensibilisiert, verdächtige Beobachtungen — etwa ungewöhnliches Systemverhalten, unerwartete Anmeldefehler oder unbekannte Prozesse — umgehend an die Ansprechstelle des Vorfallmanagements zu melden, statt sie zu ignorieren oder abzutun. Clientseitige Ereignismeldungen werden nicht ignoriert, sondern über die etablierten Alarmwege weitergeleitet.
- **Zusätzliche Detektionssysteme:** Basierend auf dem Netzplan werden Netzwerksegmente identifiziert, die zusätzlichen Schutz erfordern. Übergänge zwischen internen und externen Netzen werden durch geeignete Detektionsmechanismen überwacht. Malware-Detektionssysteme werden zentral verwaltet und melden sicherheitsrelevante Ereignisse automatisch an die zuständigen Personen.
- **Datenschutzkonformität:** Die Analyse von Protokolldaten entspricht der geltenden Datenschutzgesetzgebung. Die Privatsphäre der Beschäftigten und die Mitbestimmungsrechte des Betriebsrats werden respektiert. Organisatorische Regeln definieren die datenschutzrechtlichen Voraussetzungen, unter denen Protokolldaten manuell analysiert werden dürfen.
- **Regelmäßige Überprüfung:** Detektionssysteme und -maßnahmen werden in regelmäßigen Abständen auditiert, um zu verifizieren, dass sie aktuell und wirksam bleiben. Die Ergebnisse werden dokumentiert und mit dem Soll-Zustand verglichen. Abweichungen werden nachverfolgt und behoben.

### 6.2 Klassifizierungskriterien

Das Kategorisierungsschema berücksichtigt die folgenden Faktoren:

- Die Anzahl der betroffenen Nutzer und Systeme
- Die Klassifizierungsstufe der betroffenen Informationen
- Die geschäftlichen Auswirkungen und finanziellen Folgen
- Regulatorische und vertragliche Meldepflichten, die durch das Ereignis ausgelöst werden
- Das Potenzial, dass sich das Ereignis ausweitet oder ausbreitet
- Reputationsschäden für die Organisation

## 7. Reaktion auf Vorfälle (A 5.26)

[IHR_ORGANISATIONSNAME] etabliert und kommuniziert Verfahren zur Reaktion auf Informationssicherheitsvorfälle an alle relevanten interessierten Parteien. Auf Informationssicherheitsvorfälle wird von einem benannten Team mit der erforderlichen Kompetenz reagiert. Die Reaktion umfasst die folgenden Aktivitäten:

- **Eindämmung:** Können sich die Folgen des Vorfalls ausbreiten, werden die vom Vorfall betroffenen Systeme eingedämmt. Eindämmungsstrategien sind für gängige Vorfalltypen (Malware-Infektion, unbefugter Zugriff, Datenexfiltration, Denial of Service) vordefiniert und werden unmittelbar nach der Klassifizierung ausgeführt. In der Eindämmungsphase erhalten Responder First-Response-Hinweise, die vor beweismittelzerstörenden Maßnahmen warnen (vorzeitiges Herunterfahren, Log-Rotation, Löschen temporärer Dateien). Netzwerkisolation wird dem Systemshutdown vorgezogen, um flüchtige Beweise zu erhalten.
- **Beweissicherung:** Beweise werden so bald wie möglich nach dem Eintreten des Vorfalls gesichert. Flüchtige Daten (laufende Prozesse, Netzwerkverbindungen, Speicherinhalte) werden vor nicht-flüchtigen Daten erfasst. Der Umgang mit Beweismitteln folgt den im Abschnitt zur Beweissicherung dieser Richtlinie festgelegten Verfahren.
- **Eskalation:** Vorfälle werden nach Bedarf eskaliert, einschließlich der Aktivierung von Krisenmanagementstrukturen und erforderlichenfalls der Auslösung von Business-Continuity-Plänen. Eskalationskriterien sind auf Basis der Schweregradklassifizierung vordefiniert.
- **Aktivitätsprotokollierung:** Alle beteiligten Reaktionsaktivitäten werden zur späteren Analyse ordnungsgemäß protokolliert. Das Protokoll enthält Zeitstempel, ergriffene Maßnahmen, beteiligte Personen, betroffene Systeme und getroffene Entscheidungen.
- **Stakeholder-Kommunikation:** Das Bestehen des Informationssicherheitsvorfalls und alle relevanten Details werden nach dem Need-to-know-Prinzip an alle relevanten internen und externen interessierten Parteien kommuniziert. Kommunikationsvorlagen werden für verschiedene Stakeholder-Gruppen vorbereitet.
- **Externe Koordination:** Die Organisation koordiniert mit internen und externen Parteien wie Behörden, externen Interessensgruppen und Foren, Lieferanten und Kunden, um die Reaktionswirksamkeit zu verbessern und Folgen für andere Organisationen zu minimieren.
- **Formaler Abschluss:** Sobald der Vorfall erfolgreich bearbeitet wurde, wird er formal abgeschlossen und erfasst. Abschlusskriterien umfassen die Bestätigung, dass die Schwachstelle behoben, betroffene Systeme wiederhergestellt und präventive Maßnahmen umgesetzt wurden.
- **Forensische Analyse:** Bei Bedarf wird eine Informationssicherheits-Forensik durchgeführt. Die Entscheidung, eine forensische Untersuchung einzuleiten, wird während der Vorfallbehandlung auf Basis des Schweregrads, des Potenzials für rechtliche Schritte und der Notwendigkeit getroffen, den vollen Umfang der Kompromittierung zu verstehen.
- **Nachbereitung:** Eine Nachbereitung wird durchgeführt, um die Ursache zu identifizieren. Die Analyse wird gemäß definierter Verfahren dokumentiert und kommuniziert. Die Feststellungen fließen in die Verbesserung der Sicherheitsmaßnahmen und Vorfallmanagement-Verfahren ein.
- **Schwachstellenidentifikation:** Informationssicherheitsschwachstellen und -schwächen werden identifiziert und verwaltet, einschließlich solcher, die im Zusammenhang mit Maßnahmen stehen, die den Vorfall verursacht, zu ihm beigetragen oder seine Verhinderung versäumt haben. Identifizierte Schwachstellen werden im Schwachstellenmanagement-Prozess bis zur Behebung nachverfolgt.

Parallel zur Ursachenanalyse wird bewusst entschieden, ob die Priorität auf der Eindämmung des Schadens oder der weiteren Untersuchung des Vorfalls liegt. Für diese Entscheidung werden zunächst ausreichende Informationen über Umfang und Auswirkungen des Vorfalls gesammelt. Für ausgewählte Vorfallszenarien werden im Voraus Worst-Case-Analysen vorbereitet, sodass Eindämmungsentscheidungen unter Druck schnell getroffen werden können.

Die Behebung jedes Vorfalls folgt einem standardisierten Verfahren: Das zuständige Team isoliert das Problem, identifiziert die Ursache, wählt Behebungsmaßnahmen aus und holt vor der Umsetzung die operative Zustimmung ein. Eine aktuelle Kontaktliste interner und externer Sicherheitsfachleute wird zur Expertenberatung gepflegt. Sichere Kommunikationskanäle zu diesen Kontakten werden im Voraus eingerichtet. Die gesamte Behebung wird in standardisierter Weise dokumentiert und erfasst alle durchgeführten Maßnahmen, Zeitstempel, Protokolldaten betroffener Komponenten und getroffene Entscheidungen. Die Dokumentation wird von der/dem Informationssicherheitsbeauftragten qualitätsgesichert, bevor der Vorfall als geschlossen markiert wird.

### 7.1 Wiederherstellungsverfahren

Nach einem Vorfall werden betroffene Komponenten vom Netz isoliert. Alle erforderlichen Daten, die Einblick in die Art und Ursache des Vorfalls geben, werden gesichert. Betriebssysteme und Anwendungen auf allen betroffenen Komponenten werden auf Veränderungen untersucht. Originaldaten werden von schreibgeschützten Medien wiederhergestellt, und alle sicherheitsrelevanten Konfigurationen und Patches werden angewendet. Bevor Komponenten wieder in Betrieb genommen werden, werden alle Zugangsdaten auf betroffenen Komponenten geändert. Wo möglich, durchlaufen betroffene Komponenten vor der Wiederinbetriebnahme einen Penetrationstest. Nutzer werden in die Anwendungs-Funktionalitätstests während der Wiederherstellung einbezogen, und nach der Wiederherstellung werden die Komponenten — einschließlich Netzübergänge — mit erhöhter Aufmerksamkeit überwacht.

## 8. Lernen aus Vorfällen (A 5.27)

[IHR_ORGANISATIONSNAME] etabliert Verfahren zur Quantifizierung und Überwachung von Typen, Volumen und Kosten von Informationssicherheitsvorfällen. Die aus der Auswertung von Informationssicherheitsvorfällen gewonnenen Informationen werden zur kontinuierlichen Verbesserung genutzt:

- **Verbesserung des Vorfallplans:** Der Vorfallmanagement-Plan wird auf Basis der Lessons Learned verbessert, einschließlich der Aufnahme neuer Vorfallszenarien und der Verfeinerung bestehender Verfahren. Szenario-Playbooks werden aktualisiert, um die neuesten Bedrohungsmuster und Reaktionstechniken widerzuspiegeln.
- **Aktualisierungen der Risikobewertung:** Wiederkehrende oder schwerwiegende Vorfälle und ihre Ursachen werden identifiziert, um die Informationssicherheits-Risikobewertung der Organisation zu aktualisieren und erforderliche zusätzliche Maßnahmen festzulegen und umzusetzen. Die Organisation sammelt, quantifiziert und überwacht Informationen über Vorfallstypen, -volumen und -kosten, um die Wahrscheinlichkeit oder die Folgen künftiger ähnlicher Vorfälle zu reduzieren.
- **Nutzerbewusstsein & Schulung:** Lessons Learned aus Vorfällen werden in das Programm zur Nutzersensibilisierung und -schulung aufgenommen. Anonymisierte Beispiele veranschaulichen, was passieren kann, wie zu reagieren ist und wie ähnliche Vorfälle in Zukunft vermieden werden können.

### 8.1 Vorfallmetriken & Berichterstattung

Die Organisation verfolgt laufend die folgenden Metriken:

- Mittlere Detektionszeit (MTTD) und mittlere Reaktionszeit (MTTR) für Vorfälle
- Anzahl der Vorfälle nach Kategorie und Schweregrad
- Direkte und indirekte Kosten im Zusammenhang mit Vorfällen
- Anteil der Vorfälle, bei denen eine Ursachenanalyse abgeschlossen wurde
- Anzahl der infolge von Vorfallanalysen umgesetzten Maßnahmenverbesserungen

Vorfallmetriken werden der Geschäftsleitung im Rahmen der periodischen Managementbewertung berichtet. Trendanalysen werden genutzt, um systemische Schwächen zu identifizieren und Sicherheitsinvestitionen zu priorisieren.

Nach jeder Vorfallanalyse prüft die Organisation, ob die Prozesse und Workflows für die Vorfallbehandlung angepasst oder weiterentwickelt werden müssen. Die Abschlussphase umfasst eine strukturierte Nachbereitung mit zwei expliziten Checkpoints: (1) Erfahrungsberichte aller Beteiligten werden gesammelt und dokumentiert, und (2) die Verfahrensdokumentation und die Service-Desk-Checklisten werden überprüft und bei Bedarf aktualisiert. Die Organisation prüft, ob neue Entwicklungen in der Vorfallmanagement-Methodik und forensischen Techniken in ihre Dokumentation und Workflows aufgenommen werden können. Die Geschäftsleitung wird mindestens jährlich über Vorfallstatistiken informiert; bei unmittelbarem Handlungsbedarf wird die Geschäftsleitung ohne Verzögerung informiert.

Das Vorfallmanagement-System wird regelmäßig überprüft — durch angekündigte und unangekündigte Übungen — um zu verifizieren, dass es aktuell und wirksam bleibt. Die Übungen werden mit der Geschäftsleitung abgestimmt. Metriken wie die Zeit vom initialen Bericht bis zum bestätigten Vorfallstatus werden ausgewertet. Tabletop-Übungen und simulierte Vorfälle werden durchgeführt, um die Einsatzbereitschaft sicherzustellen.

## 9. Beweissicherung (A 5.28)

[IHR_ORGANISATIONSNAME] entwickelt und befolgt interne Verfahren zum Umgang mit Beweismitteln im Zusammenhang mit Informationssicherheitsereignissen für disziplinarische und rechtliche Maßnahmen. Die Anforderungen verschiedener Jurisdiktionen werden berücksichtigt, um die Chancen auf Zulässigkeit in den relevanten Jurisdiktionen zu maximieren. Beweise werden auf eine Weise gesammelt, die vor den zuständigen nationalen Gerichten oder anderen Disziplinarforen zulässig ist.

### 9.1 Anforderungen an die Beweisintegrität

Die Organisation weist nach, dass:

- **Vollständigkeit & Integrität:** Aufzeichnungen vollständig sind und in keiner Weise manipuliert wurden. Digitale Beweise werden während der Untersuchungsphase hochgeladen. Jede Datei wird automatisch mit einem zum Zeitpunkt des Hochladens berechneten kryptographischen SHA-256-Hash gesichert. Der Hash wird neben der Datei gespeichert und zur Integritätsprüfung angezeigt. Ein Chain-of-Custody-Protokoll erfasst jeden Zugriff auf Beweismitteldateien (Upload, Download, Verifizierung) mit Nutzeridentität, Zeitstempel und Zweck.
- **Forensische Kopien:** Kopien elektronischer Beweise nachweislich identisch mit den Originalen sind. Kryptographische Hash-Werte (SHA-256 oder höher) werden zum Zeitpunkt der Erfassung berechnet und bei jedem späteren Zugriff verifiziert, um die Integrität zu bestätigen. Beweise werden nach Typ kategorisiert (Screenshot, Log-Export, Netzwerk-Capture, Malware-Sample, Kommunikation) mit typenspezifischen Dateiformat-Einschränkungen. Für Beweise, die nicht über die Plattform hochgeladen werden können (z. B. physische Speichermedien), wird ein externer Referenzeintrag mit Beschreibung und Aufbewahrungsort erfasst.
- **Systemintegrität:** Jedes Informationssystem, aus dem Beweise gesammelt wurden, zum Zeitpunkt der Beweisaufnahme korrekt funktioniert hat. System-Health-Checks und -Protokolle werden neben den Beweisen aufbewahrt, um diese Aussage zu stützen.

### 9.2 Forensische Verfahren

Die Beweismittelverfahren bieten Anweisungen zur Identifikation, Sammlung, Erfassung und Aufbewahrung von Beweisen unter Berücksichtigung verschiedener Typen von Speichermedien, Geräten und des Gerätezustands (eingeschaltet oder ausgeschaltet). Die Verfahren adressieren:

- Live-Forensik für flüchtige Daten (RAM, laufende Prozesse, Netzwerkverbindungen) vor dem Herunterfahren von Systemen
- Post-Mortem-Forensik für nicht-flüchtige Daten (Festplatten, SSDs, Wechseldatenträger) unter Verwendung forensischer Duplizierungswerkzeuge
- Reihenfolge der Volatilität: Daten werden in absteigender Reihenfolge der Volatilität erfasst, beginnend mit den flüchtigsten Quellen
- Sichere Aufbewahrung von Beweisen in manipulationssicheren Behältern oder verschlüsselten Speicherorten

Sofern verfügbar, werden Zertifizierungen oder andere relevante Qualifikationsnachweise von Personal und Werkzeugen angestrebt, um den Wert der gesicherten Beweise zu erhöhen. Ein qualifizierter forensischer Dienstleister wird vorausgewählt und in der Vorfallmanagement-Konfiguration dokumentiert. Während der Untersuchung können Responder angeben, ob externe forensische Unterstützung in Anspruch genommen wird, wobei die Kontaktdaten des Anbieters direkt im Workflow angezeigt werden. Wo angemessen, werden Rahmenverträge oder Abrufvereinbarungen geschlossen, damit forensische Untersuchungen ohne Verzögerung beginnen können.

Ein First-Response-Leitfaden beschreibt für jeden Typ eingesetzter IT-Systeme die bei der Erkennung eines Sicherheitsvorfalls zu ergreifenden Erstmaßnahmen, damit möglichst wenige Spuren vernichtet werden. Der Leitfaden warnt ausdrücklich vor Maßnahmen, die versehentlich Beweise vernichten könnten — etwa das vorzeitige Herunterfahren eines kompromittierten Systems vor der Erfassung flüchtiger Daten oder das Löschen temporärer Dateien vor der Analyse. Alle verantwortlichen Personen werden im korrekten Umgang mit forensischen Werkzeugen und in den First-Response-Verfahren geschult. Forensische Werkzeuge werden vor dem Einsatz auf korrekte Funktion und Manipulationsfreiheit überprüft.

Die Aufbewahrung forensischer Daten wird durch definierte Aufbewahrungsfristen geregelt, die rechtlichen und regulatorischen Anforderungen entsprechen. Die/der Datenschutzbeauftragte und der Betriebsrat bzw. die Personalvertretung werden von Beginn an einbezogen, um sicherzustellen, dass die Sammlung und Auswertung forensischer Daten — die häufig personenbezogene Daten enthalten — keine Datenschutzvorschriften oder internen Vereinbarungen verletzt. Die Zweckbindung wird während der gesamten Untersuchung eingehalten.

Digitale Beweise können Organisations- oder Jurisdiktionsgrenzen überschreiten. In solchen Fällen stellt die Organisation sicher, dass sie berechtigt ist, die erforderlichen Informationen als digitale Beweise zu sammeln. Wenn ein Informationssicherheitsereignis erstmals erkannt wird, ist nicht immer offensichtlich, ob das Ereignis zu einem Gerichtsverfahren führt. Daher bezieht die Organisation bei jeder erwogenen rechtlichen Maßnahme frühzeitig die Rechtsberatung ein und lässt sich hinsichtlich der erforderlichen Beweise beraten.

## 10. Handhabung technischer Schwachstellen (A 8.8)

[IHR_ORGANISATIONSNAME] pflegt ein genaues Asset-Verzeichnis als Voraussetzung für ein wirksames technisches Schwachstellenmanagement. Für Software-Assets umfasst das Verzeichnis den Softwarehersteller, den Softwarenamen, die Versionsnummern, den aktuellen Bereitstellungsstand (welche Software auf welchen Systemen installiert ist) und die für die Software verantwortlichen Personen innerhalb der Organisation. Der technische Schwachstellenmanagement-Prozess ist auf die Vorfallmanagement-Aktivitäten abgestimmt, um Daten über Schwachstellen an die Incident-Response-Funktion zu kommunizieren und technische Verfahren für den Fall eines Vorfalls bereitzustellen.

Schwachstelleninstanzen durchlaufen einen fünfstufigen Lebenszyklus: Erkannt, Bewertung, Entscheidung, Behebung und Geschlossen. Die Behebungsphase unterscheidet zwei Pfade: aktive Behebung (mit einem verknüpften Änderungsantrag und optionaler kompensierender Maßnahme) oder Verschiebung in das Risikomanagement (mit Dokumentation kompensierender Maßnahmen bis eine dauerhafte Behebung verfügbar ist). Ein zentrales Schwachstelleninventar wird geführt und erfasst alle bekannten Schwachstellen der betriebenen IT-Komponenten und deren Bearbeitungsstatus. Jede Schwachstelleninstanz ist mit einer strategischen Schwachstellenkategorie aus dem Risikokatalog der Organisation verknüpft. Diese bidirektionale Anreicherung ermöglicht es Risikoprüfern, aktive operative Instanzen pro strategischer Schwachstelle zu sehen, und Schwachstellenbearbeitern, zugehörige Risikoszenarien zu sehen. Die IT-Betriebsfunktion initiiert und verfolgt die Behandlung jeder Schwachstelle und stellt eine zeitnahe Behebung sicher. Ein definierter Prozess legt die maximale Frist für die Installation eines verfügbaren Updates, das eine Schwachstelle behebt, fest, die Bedingungen, unter denen IT-Komponenten mit offenen Schwachstellen außer Betrieb genommen oder ersetzt werden, und wie Komponenten isoliert werden, wenn weder Patch noch Ersatz verfügbar sind. IT-Systeme und Software werden regelmäßig aktualisiert; Patches werden nach Veröffentlichung umgehend bewertet und priorisiert. Sind für eine veröffentlichte Schwachstelle bekannte Exploits vorhanden, berücksichtigt die Bewertung das konkrete Ausnutzungsrisiko.

### 10.1 Identifikation technischer Schwachstellen

Die Organisation setzt die folgenden Maßnahmen zur Identifikation technischer Schwachstellen um:

- **Rollen & Verantwortlichkeiten:** Rollen und Verantwortlichkeiten im Zusammenhang mit dem technischen Schwachstellenmanagement sind definiert und etabliert, einschließlich Schwachstellenüberwachung, Risikobewertung, Patching, Asset-Tracking und Koordinationsverantwortlichkeiten.
- **Informationsquellen:** Für Software und andere Technologien werden auf Basis des Asset-Verzeichnisses Informationsquellen zur Identifikation relevanter technischer Schwachstellen identifiziert, und das Bewusstsein dafür wird aufrechterhalten. Die Liste der Informationsquellen wird auf Basis von Änderungen im Verzeichnis oder wenn neue nützliche Quellen gefunden werden aktualisiert. Quellen umfassen CVE-Datenbanken, Hersteller-Sicherheitsbulletins, CERT-Advisories und Threat-Intelligence-Feeds.
- **Lieferantenpflichten:** Lieferanten von Informationssystemen, einschließlich ihrer Komponenten, werden verpflichtet, die Meldung, Behandlung und Offenlegung von Schwachstellen sicherzustellen, einschließlich der Anforderungen in geltenden Verträgen.
- **Schwachstellenscans:** Für die eingesetzten Technologien geeignete Schwachstellen-Scan-Werkzeuge werden bereitgestellt, um Schwachstellen zu identifizieren und zu verifizieren, ob das Patching von Schwachstellen erfolgreich war. Scans werden nach einem regelmäßigen Zeitplan und nach wesentlichen Änderungen durchgeführt. Ergebnisse automatisierter Schwachstellenscanner werden zur konsolidierten Verfolgung und Behandlung in das zentrale Schwachstelleninventar importiert.
- **Penetrationstests:** Geplante, dokumentierte und wiederholbare Penetrationstests oder Schwachstellenbewertungen werden von kompetenten und autorisierten Personen durchgeführt, um die Identifikation von Schwachstellen zu unterstützen. Testszenarien werden systematisch aus dem MITRE-ATT&CK-Framework abgeleitet, wobei Testgruppen auf Basis beobachteter Threat Intelligence (Vorfälle, Advisories) priorisiert werden. Feststellungen werden direkt in den Schwachstellenmanagement-Prozess überführt. Vorsicht ist geboten, da solche Aktivitäten die Sicherheit des Systems beeinträchtigen können.
- **Tracking von Drittanbieter-Bibliotheken:** Die Nutzung von Drittanbieter-Bibliotheken und Quellcode wird auf Schwachstellen nachverfolgt. Ein Software-Composition-Analysis-Prozess (SCA) ist als Teil des sicheren Entwicklungslebenszyklus etabliert.

### 10.2 Offenlegung von Schwachstellen

Die Organisation entwickelt Verfahren und Fähigkeiten, um:

- **Erkennung von Produktschwachstellen:** Das Vorhandensein von Schwachstellen in Produkten und Diensten der Organisation, einschließlich in diesen verwendeter externer Komponenten, wird durch kontinuierliche Überwachung und Meldung erkannt.
- **Entgegennahme von Meldungen:** Schwachstellenmeldungen aus internen oder externen Quellen werden entgegengenommen, bestätigt und über einen definierten Workflow bearbeitet.
- **Öffentliche Kontaktstelle:** Ein öffentliches Portal zur Schwachstellenmeldung wird betrieben und ermöglicht es Sicherheitsforschern und anderen externen Parteien, Schwachstellen in Produkten und Diensten der Organisation zu melden. Einreichungen werden automatisch im Schwachstellenmanagement-Prozess registriert. Melder werden informiert, wenn ihre gemeldete Schwachstelle bearbeitet und behoben wurde. Eine Richtlinie zur verantwortungsvollen Offenlegung wird veröffentlicht.
- **Meldeverfahren:** Verfahren zur Schwachstellenmeldung, Online-Meldeformulare und geeignete Threat-Intelligence- oder Informationsaustauschforen werden etabliert und gepflegt.

### 10.3 Bewertung technischer Schwachstellen

Zur Bewertung identifizierter technischer Schwachstellen:

- **Meldungsanalyse:** Die Organisation analysiert und verifiziert Schwachstellenmeldungen, um zu bestimmen, welche Reaktions- und Behebungsaktivitäten erforderlich sind. Meldungen werden auf Basis des CVSS-Scores, der Ausnutzbarkeit, der betroffenen Assets und des Geschäftskontexts triagiert.
- **Risikoidentifikation:** Sobald eine potenzielle technische Schwachstelle identifiziert wurde, werden die zugehörigen Risiken und die zu ergreifenden Maßnahmen festgelegt. Maßnahmen können das Aktualisieren verwundbarer Systeme, die Anwendung kompensierender Maßnahmen oder die Akzeptanz von Restrisiken mit dokumentierter Begründung umfassen.
- **Audit-Protokoll:** Ein Audit-Protokoll wird für alle Schritte des technischen Schwachstellenmanagements geführt, von der Erstmeldung über Bewertung, Entscheidung, Behebung bis zur Verifizierung.

### 10.4 Behandlung technischer Schwachstellen

Ein Software-Update-Management-Prozess stellt sicher, dass die aktuellsten genehmigten Patches und Anwendungsupdates für alle autorisierten Softwareprodukte installiert werden. Sind Änderungen erforderlich, wird die Originalsoftware beibehalten und die Änderungen werden auf eine dedizierte Kopie angewendet. Alle Änderungen werden vollständig getestet und dokumentiert. Die folgenden Maßnahmen werden umgesetzt:

- **Zeitnahe Maßnahmen:** Angemessene und zeitnahe Maßnahmen werden als Reaktion auf die Identifikation potenzieller technischer Schwachstellen ergriffen. Eine definierte Zeitleiste regelt die Reaktion auf Meldungen potenziell relevanter technischer Schwachstellen mit schweregradbasierten SLAs: kritisch: 3 Tage, hoch: 7 Tage, mittel: 30 Tage, niedrig: 90 Tage.
- **Abstimmung mit dem Änderungsmanagement:** Abhängig davon, wie dringend eine technische Schwachstelle behandelt werden muss, erfolgt die Behebung gemäß dem Änderungsmanagement-Prozess oder nach den Incident-Response-Verfahren für Notfalländerungen. Aus Schwachstellen oder Vorfällen erstellte Änderungsanträge werden mit zugehörigen MITRE-ATT&CK-Techniken und empfohlenen Mitigationen angereichert, um den Behebungsansatz zu informieren.
- **Legitime Quellen:** Es werden nur Updates aus legitimen Quellen verwendet, ob intern oder extern. Die Update-Authentizität wird durch digitale Signaturen oder Prüfsummen verifiziert.
- **Pre-Deployment-Tests:** Updates werden vor der Installation getestet und bewertet, um sicherzustellen, dass sie wirksam sind und keine inakzeptablen Nebenwirkungen verursachen. Ist ein Update verfügbar, werden die mit der Installation des Updates verbundenen Risiken mit den durch die Schwachstelle verursachten Risiken verglichen.
- **Priorisierte Behebung:** Systeme mit hohem Risiko werden zuerst behandelt. Die Behebungspriorität berücksichtigt die Kritikalität des Assets, den Schweregrad der Schwachstelle und die Exposition gegenüber Ausnutzung.
- **Entwicklung von Behebungen:** Wo Herstellerpatches nicht verfügbar sind, entwickelt die Organisation Behebungsmaßnahmen, typischerweise durch kompensierende Maßnahmen, Konfigurationsänderungen oder individuelle Patches.
- **Verifizierung der Behebung:** Es werden Tests durchgeführt, um zu bestätigen, ob die Behebung oder Mitigation wirksam ist. Post-Patch-Schwachstellenscans verifizieren, dass die Schwachstelle beseitigt wurde.
- **Authentizitätsprüfung:** Mechanismen sind vorhanden, um die Authentizität von Behebungspaketen zu verifizieren, einschließlich Validierung digitaler Signaturen und Prüfsummenvergleich mit vom Hersteller veröffentlichten Werten.

### 10.5 Kompensierende Maßnahmen bei fehlendem Update

Ist kein Update verfügbar oder kann das Update nicht installiert werden, werden die folgenden kompensierenden Maßnahmen in Betracht gezogen:

- **Herstellerworkarounds:** Jeder vom Softwarehersteller oder aus anderen relevanten Quellen vorgeschlagene Workaround wird angewendet.
- **Deaktivierung von Diensten:** Mit der Schwachstelle verbundene Dienste oder Funktionen werden deaktiviert, bis ein Patch verfügbar ist.
- **Verschärfung der Zugriffskontrolle:** Zugriffskontrollen (z. B. Firewalls) an Netzwerkgrenzen werden angepasst oder ergänzt, um die Exposition der verwundbaren Komponente zu begrenzen.
- **Virtual Patching:** Verwundbare Systeme, Geräte oder Anwendungen werden durch geeignete Verkehrsfilter (Virtual Patching) mithilfe von Web Application Firewalls oder Intrusion-Prevention-Systemen vor Angriffen geschützt.
- **Erhöhte Überwachung:** Die Überwachung wird verstärkt, um tatsächliche Ausnutzungsversuche gegen die nicht gepatchte Schwachstelle zu erkennen.
- **Sensibilisierung:** Das Bewusstsein für die Schwachstelle wird bei betroffenen Nutzern und Administratoren bis zum Abschluss der Behebung geschärft.

### 10.6 Automatisierung & Verzögerungen von Updates

- **Automatische Updates:** Für beschaffte Software, bei der Hersteller regelmäßig Sicherheitsupdates veröffentlichen und automatische Update-Funktionen bieten, bewertet die Organisation, ob automatisches Aktualisieren angemessen ist. Automatische Updates sind für Standard-Endgeräte aktiviert; Server und kritische Systeme folgen dem kontrollierten Patch-Management-Prozess.
- **Verzögerte Updates:** Ist ein angemessener Test von Updates nicht möglich (z. B. aufgrund von Kosten oder fehlenden Ressourcen), bewertet die Organisation die zugehörigen Risiken auf Basis der von anderen Nutzern berichteten Erfahrungen, bevor über den Bereitstellungszeitpunkt entschieden wird.

Innerhalb der Patch-Management-Strategie wird der Umgang mit eingebauten Auto-Update-Mechanismen der eingesetzten Software definiert. Die Organisation legt fest, wie diese Mechanismen gesichert und angemessen konfiguriert werden. Neue Komponenten werden überprüft, um festzustellen, welche Update-Mechanismen sie enthalten. Hardware- und Softwareprodukte, die vom Hersteller nicht mehr unterstützt werden und für die keine Sicherheitspatches verfügbar sind, werden auf ihren sicheren Weiterbetrieb bewertet; Produkte, die nicht sicher betrieben werden können, werden außer Betrieb genommen.

Der technische Schwachstellenmanagement-Prozess wird regelmäßig überwacht und bewertet, um seine Wirksamkeit und Effizienz sicherzustellen. Die Organisation berücksichtigt auch Bug-Bounty-Programme, bei denen Belohnungen als Anreiz zur Unterstützung bei der Identifikation von Schwachstellen angeboten werden. Informationen werden mit kompetenten Branchengremien und anderen interessierten Parteien geteilt. IT-Komponenten werden regelmäßig und ereignisgetrieben auf Schwachstellen getestet; Testumfang, -tiefe und -methode werden für jede Komponentenkategorie definiert. Wo kritische Schwachstellen oder Bedrohungen bestehen und noch keine Patches verfügbar sind, werden kompensierende Maßnahmen zum Schutz der betroffenen Komponenten umgesetzt.

Wo die Organisation einen Cloud-Dienst eines Drittanbieters nutzt, stellt der Anbieter das technische Schwachstellenmanagement der Ressourcen des Cloud-Dienstanbieters sicher. Die Verantwortlichkeiten des Anbieters für das technische Schwachstellenmanagement sind Teil der Cloud-Dienstvereinbarung, einschließlich der Prozesse zur Meldung der Maßnahmen des Anbieters im Zusammenhang mit technischen Schwachstellen.

## 11. Änderungsmanagement (A 8.32)

Die Einführung neuer Systeme und wesentliche Änderungen an bestehenden Systemen bei [IHR_ORGANISATIONSNAME] folgen vereinbarten Regeln und einem formalen Prozess der Dokumentation, Spezifikation, Prüfung, Qualitätskontrolle und gesteuerten Umsetzung. Managementverantwortlichkeiten und -verfahren sind etabliert, um eine zufriedenstellende Kontrolle aller Änderungen sicherzustellen. Änderungskontrollverfahren sind dokumentiert und werden durchgesetzt, um die Vertraulichkeit, Integrität und Verfügbarkeit von Informationen über den gesamten Systementwicklungslebenszyklus hinweg sicherzustellen.

Wo praktikabel, werden Änderungskontrollverfahren für IKT-Infrastruktur und Software in einen einzigen Änderungsmanagement-Prozess integriert. Die Änderungskontrollverfahren umfassen:

- **Folgenabschätzung:** Die potenziellen Auswirkungen von Änderungen werden unter Berücksichtigung aller Abhängigkeiten geplant und bewertet. Die Folgenabschätzung deckt die betroffenen Informationssysteme, Geschäftsprozesse, verbundenen Systeme, Datenflüsse und Sicherheitsmaßnahmen ab. Die Bewertung wird als Teil des Änderungsantragsdatensatzes dokumentiert.
- **Autorisierung:** Änderungen werden vor der Umsetzung von der zuständigen Stelle autorisiert. Autorisierungsstufen werden auf Basis der Risikokategorie der Änderung (Standard, Normal, Notfall) definiert. Keine Änderung wird ohne dokumentierte Autorisierung umgesetzt.
- **Kommunikation:** Änderungen werden vor der Umsetzung an relevante interessierte Parteien kommuniziert. Die Benachrichtigung umfasst den Umfang der Änderung, die erwarteten Auswirkungen, das Wartungsfenster und den Rollback-Plan.
- **Tests & Abnahme:** Änderungen werden vor der Umsetzung in der Produktionsumgebung getestet und abgenommen. Tests werden in einer getrennten Testumgebung durchgeführt, die die Produktionskonfiguration widerspiegelt. Testergebnisse werden dokumentiert und vom Änderungseigentümer akzeptiert.
- **Umsetzung & Bereitstellung:** Änderungen werden gemäß dokumentierten Bereitstellungsplänen umgesetzt. Der Bereitstellungsplan umfasst die Abfolge der Aktivitäten, die verantwortlichen Personen, den Zeitpunkt, die Verifizierungsschritte und Go-/No-Go-Kriterien.
- **Notfall & Contingency:** Notfall- und Contingency-Überlegungen, einschließlich Fallback-Verfahren (Rollback), werden für jede Änderung dokumentiert. Notfalländerungen folgen einem beschleunigten Pfad mit einer Nachbesprechung innerhalb von 48 Stunden nach der Umsetzung.
- **Änderungsdatensätze:** Aufzeichnungen aller Änderungen werden geführt, einschließlich Antrag, Folgenabschätzung, Autorisierung, Testergebnisse, Bereitstellungsplan, Rollback-Verfahren und Nachbesprechung.
- **Aktualisierung der Dokumentation:** Betriebs- und Nutzerdokumentation wird nach Bedarf aktualisiert, um nach Änderungen angemessen zu bleiben. Die Verifizierungsphase umfasst eine Prüfung der Dokumentationsaktualisierung, die bestätigt, ob Betriebsdokumentation und Nutzerverfahren nach der Änderung aktualisiert wurden. Wenn die Änderung eine Schwachstelle behebt, verifiziert ein optionales Ergebnisfeld eines Schwachstellenscans, dass die behobene Schwachstelle beseitigt wurde.
- **Aktualisierung der Kontinuitätspläne:** IKT-Kontinuitätspläne und Reaktions- und Wiederherstellungsverfahren werden nach Bedarf aktualisiert, um nach Änderungen angemessen zu bleiben. Dies stellt sicher, dass Disaster-Recovery-Fähigkeiten die aktuelle Systemkonfiguration widerspiegeln.

### 11.1 Änderungskategorien

Änderungen werden in die folgenden Kategorien eingeteilt:

- **Standardänderungen:** Vorab genehmigte, risikoarme, häufig wiederkehrende Änderungen, die einem dokumentierten Verfahren folgen (z. B. routinemäßige Patch-Bereitstellung auf nicht-kritischen Systemen).
- **Normale Änderungen:** Änderungen, die eine individuelle Folgenabschätzung, Tests und Autorisierung über den Änderungsmanagement-Prozess erfordern.
- **Notfalländerungen:** Änderungen, die zur Behebung kritischer Vorfälle oder zur Abwehr unmittelbarer Sicherheitsbedrohungen erforderlich sind. Notfalländerungen werden von der/dem Informationssicherheitsbeauftragten oder dem IT-Betriebsleiter autorisiert und unterliegen einer Nachbesprechung innerhalb von 48 Stunden nach der Umsetzung.

Eine unzureichende Kontrolle von Änderungen an Informationsverarbeitungseinrichtungen und Informationssystemen ist eine häufige Ursache für System- oder Sicherheitsausfälle. Änderungen an der Produktionsumgebung, insbesondere beim Transfer von Software aus der Entwicklung in die Betriebsumgebung, können die Integrität und Verfügbarkeit von Anwendungen beeinträchtigen. Gute Praxis umfasst das Testen von IKT-Komponenten in einer Umgebung, die sowohl von der Produktions- als auch von der Entwicklungsumgebung getrennt ist.

Ein dokumentiertes Konzept für den Patch- und Änderungsmanagement-Prozess regelt alle Modifikationen an IT-Komponenten, Software und Konfigurationsdaten unter gebührender Berücksichtigung sicherheitsrelevanter Aspekte. Alle Patches und Änderungen werden geplant, genehmigt und dokumentiert. Rollback-Lösungen stehen vor jeder Anwendung einer Änderung zur Verfügung; bei wesentlichen Änderungen wird die/der Informationssicherheitsbeauftragte einbezogen. Das gewünschte Sicherheitsniveau und die Sicherheitskonfigurationen werden während und nach der Änderung erhalten. Verantwortlichkeiten für Patch- und Änderungsmanagement sind für alle Organisationsbereiche definiert und spiegeln sich im Berechtigungskonzept wider.

Alle Änderungsanträge (Requests for Change, RfCs) werden erfasst und dokumentiert. Die verantwortlichen Personen verifizieren, dass Informationssicherheitsaspekte ausreichend berücksichtigt wurden. Der Koordinationsprozess berücksichtigt alle betroffenen Stakeholder-Gruppen und die Auswirkungen auf die Informationssicherheit. Betroffene Gruppen haben eine dokumentierte Möglichkeit, sich einzubringen. Ein beschleunigter Pfad steht für dringende Änderungsanträge zur Verfügung. Änderungen werden in die Geschäftsprozesse integriert; die aktuelle operative Situation der betroffenen Prozesse wird berücksichtigt, und alle relevanten Abteilungen werden über bevorstehende Änderungen informiert. Eine Eskalationsstufe besteht auf Managementebene, um über Prioritäts- und Terminkonflikte bei Hardware- oder Softwareänderungen zu entscheiden.

Die Integrität und Authentizität aller Softwarepakete wird während des gesamten Änderungsprozesses verifiziert. Wo Prüfsummen oder digitale Signaturen verfügbar sind, werden sie vor der Bereitstellung validiert. Software und Updates werden ausschließlich aus vertrauenswürdigen Quellen bezogen. Alle Änderungen werden über alle Phasen, Anwendungen und Systeme hinweg gemäß definierten Dokumentationsregeln dokumentiert.

## 12. Rollen & Verantwortlichkeiten

- **Geschäftsleitung:** Genehmigt diese Richtlinie, stellt Ressourcen für Security Operations bereit und wird über wesentliche Vorfälle und deren Geschäftsauswirkungen informiert.
- **Informationssicherheitsbeauftragte/r (ISB):** Koordiniert alle Security-Operations-Aktivitäten, pflegt das Register der Behördenkontakte und Interessensgruppen-Mitgliedschaften, beaufsichtigt das Threat-Intelligence-Programm, leitet das Incident-Response-Team und berichtet Sicherheitsmetriken an die Geschäftsleitung.
- **Incident-Response-Team:** Reagiert auf Informationssicherheitsvorfälle, führt Eindämmung und Beseitigung durch, führt forensische Analysen durch und setzt Nachbesprechungen um. Teammitglieder werden je nach Art des Vorfalls benannt.
- **IT-Betrieb / IT-Abteilung:** Betreibt Detektions- und Überwachungssysteme, führt Schwachstellenscans durch, wendet Patches und Updates an, setzt autorisierte Änderungen um und pflegt die Systemdokumentation.
- **Change Advisory Board (CAB):** Prüft und autorisiert normale und risikoreiche Änderungen, bewertet die Auswirkungen auf die Informationssicherheit und überwacht die Qualität der Änderungsumsetzung.
- **Datenschutzbeauftragte/r (DSB):** Wird bei Vorfällen mit Bezug zu personenbezogenen Daten konsultiert, berät zu Meldepflichten bei Datenschutzverletzungen und stellt sicher, dass forensische Aktivitäten den Datenschutzvorschriften entsprechen.
- **Rechtsberatung:** Berät zu Beweismittelverfahren, regulatorischen Meldepflichten, vertraglichen Benachrichtigungsanforderungen und rechtlichen Implikationen von Vorfällen.
- **Alle Beschäftigten:** Melden Informationssicherheitsereignisse über den etablierten Meldeweg, sichern Beweise, indem sie von unbefugter Behebung absehen, und nehmen an Sensibilisierungsschulungen zur Vorfallerkennung und -meldung teil.

## 13. Überprüfung & Pflege

Diese Richtlinie wird überprüft:

- Mindestens jährlich im Rahmen des ISMS-Managementbewertungszyklus.
- Nach wesentlichen Informationssicherheitsvorfällen, um Lessons Learned aufzunehmen.
- Wenn sich die Bedrohungslage wesentlich ändert (neue Bedrohungsakteure, aufkommende Angriffsvektoren, geopolitische Entwicklungen).
- Nach wesentlichen organisatorischen Änderungen (Umstrukturierung, Fusionen, neue IT-Systeme, Änderungen im geltenden Recht oder in Vorschriften).
- Wenn externe Auditfeststellungen oder behördliche Leitlinien Aktualisierungen erfordern.

Die/der Informationssicherheitsbeauftragte ist für die Einleitung und Koordination des Überprüfungsprozesses verantwortlich. Änderungen an dieser Richtlinie werden von der Geschäftsleitung genehmigt und an alle betroffenen Personen kommuniziert.
