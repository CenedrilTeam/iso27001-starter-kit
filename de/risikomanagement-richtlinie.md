# Risikomanagement-Richtlinie

> **Dokumentenkontrolle**  
> Eigentümer: [RICHTLINIEN_EIGENTÜMER_ROLLE, z. B. Informationssicherheitsbeauftragte/r]  
> Genehmigt von: [GENEHMIGER_NAME_UND_ROLLE]  
> Version: [VERSION]  
> Gültig ab: [GÜLTIGKEITSDATUM]  
> Nächste Überprüfung: [NÄCHSTES_ÜBERPRÜFUNGSDATUM]

## 1. Rechtliche/Regulatorische Grundlage

ISO/IEC 27001:2022 — Informationssicherheitsmanagementsysteme (Kapitel 6.1, 6.2, 8.2, 8.3).

ISO/IEC 27005:2022 — Informationssicherheits-Risikomanagement.

BSI IT-Grundschutz:

- BSI-Standard 200-3 (Risikoanalyse auf der Basis von IT-Grundschutz)
- ISMS.1 (Sicherheitsmanagement)

Weitere jurisdiktionsspezifische Gesetze und Vorschriften, die für [IHR_ORGANISATIONSNAME] gelten, sind im Rechtsregister aufgeführt und werden durch Verweis einbezogen. Typische Beispiele sind Datenschutzgesetze (z. B. DSGVO), branchenspezifische Regulierungen (z. B. NIS2, DORA, KRITIS) sowie vertragliche Sicherheitsanforderungen wichtiger Kunden.

## 2. Zweck & Geltungsbereich

Diese Risikomanagement-Richtlinie definiert die Methodik zur Identifikation, Analyse, Bewertung und Behandlung von Informationssicherheitsrisiken bei **[IHR_ORGANISATIONSNAME]**. Sie etabliert einen systematischen, wiederholbaren Prozess, der sicherstellt, dass Risiken konsistent und im Einklang mit der Risikobereitschaft und den strategischen Zielen der Organisation gemanagt werden.

Die Richtlinie gilt für alle Informationswerte, Geschäftsprozesse, IT-Systeme und Drittanbieter-Dienste innerhalb des Geltungsbereichs des ISMS. Sie wird von Risikoeigentümern, dem/der Informationssicherheitsbeauftragten, der Geschäftsleitung und allen an Risikobeurteilungs- und -behandlungsaktivitäten beteiligten Personen genutzt.

Der Risikomanagementprozess folgt ISO/IEC 27005:2022 und ist in vier Phasen strukturiert: Risikoidentifikation, Risikoanalyse, Risikobewertung und Risikobehandlung. Diese Richtlinie dokumentiert die vollständige Methodik, sodass ein Auditor oder Stakeholder nachvollziehen kann, wie die Organisation Risikomanagement betreibt.

## 3. Risikokontext & Risikoquellen

### 3.1 Festlegung des Kontexts

Vor der Durchführung einer Risikobeurteilung wird der Kontext festgelegt, indem die in der ISMS-Geltungsbereichsanalyse identifizierten externen und internen Faktoren (Informationssicherheits-Richtlinie, Kapitel 4.1), die Anforderungen interessierter Parteien (Informationssicherheits-Richtlinie, Kapitel 4.2) und die Grenzen des ISMS-Geltungsbereichs (Informationssicherheits-Richtlinie, Kapitel 4.3) berücksichtigt werden. Der Geltungsbereich der Risikobeurteilung umfasst alle Assets, Prozesse und Dienste innerhalb der ISMS-Grenze.

### 3.2 Risikoquellen-Katalog

Risiken werden über einen Katalog von Risikoquellen identifiziert, der das gesamte Spektrum potenzieller Ursprünge abdeckt. Risikoquellen sind in folgende Kategorien gruppiert:

- **Menschlich vorsätzlich:** Staatliche Akteure, organisierte Kriminalität, terroristische Gruppen, ideologische Aktivisten, spezialisierte Hacking-Gruppen, Amateur-Hacker, Insider/Rächer und pathologische Angreifer. Jede Quelle ist durch ihre typische Motivation gekennzeichnet (Spionage, finanzieller Gewinn, Störung, Einflussnahme).
- **Menschlich unbeabsichtigt:** Beschäftigte und Partner, die Sicherheitsereignisse durch mangelndes Bewusstsein, Fahrlässigkeit oder unzureichende Ressourcen verursachen.
- **Nicht-technisch vorsätzlich:** Kleinkriminelle (Diebstahl, Brandstiftung), Wettbewerber und Datenhändler, die mit nicht-technischen Mitteln agieren.
- **Umweltbedingt:** Naturkatastrophen, extreme Wetterereignisse und andere Umgebungsbedingungen, die informationsverarbeitende Einrichtungen beeinträchtigen.
- **Technisch:** Hardware-Fehlfunktionen und Software-Defekte, die zu sicherheitsrelevanten Ausfällen führen.

Der Risikoquellen-Katalog wird als statische Referenzdaten gepflegt und aktualisiert, wenn neue Quellenkategorien auftreten oder bestehende Kategorien die aktuelle Bedrohungslandschaft nicht mehr widerspiegeln.

## 4. Risikoidentifikation (ISO 27001 Kapitel 6.1.2)

Die Risikoidentifikation folgt einem strukturierten, asset-basierten Ansatz, der organisatorische Assets mit Bedrohungen und Schwachstellen verknüpft, um Risikoszenarien zu erstellen. Der Identifikationsprozess verläuft in folgenden Schritten:

### 4.1 Identifikation von Assets

Primäre Informationswerte (Daten, Aufzeichnungen, geistiges Eigentum) und unterstützende Assets (IT-Systeme, Anwendungen, Netzwerkinfrastruktur, Personal, physische Einrichtungen) werden aus dem ISMS-Asset-Inventar identifiziert. Jedem primären Asset werden Anforderungen an Vertraulichkeit, Integrität und Verfügbarkeit (CIA) auf Grundlage des Informationsklassifizierungsschemas zugewiesen.

### 4.2 Identifikation von Bedrohungen

Für jedes unterstützende Asset werden anwendbare Bedrohungen aus dem Bedrohungskatalog identifiziert. Bedrohungen beschreiben nachteilige Handlungen oder Ereignisse, die Schwachstellen ausnutzen. Jede Bedrohung ist mit einer oder mehreren Risikoquellen verknüpft und durch die betroffene(n) CIA-Dimension(en) gekennzeichnet. Der Bedrohungskatalog deckt Kategorien wie Cyber-Angriffe, physisches Eindringen, Social Engineering, Umweltereignisse und technische Ausfälle ab.

### 4.3 Identifikation von Schwachstellen

Schwachstellen — Schwächen in Assets oder Maßnahmen, die von Bedrohungen ausgenutzt werden können — werden für jedes unterstützende Asset identifiziert. Quellen umfassen Schwachstellenbewertungen, Penetrationstests, Auditfeststellungen, Herstellerhinweise und Vorfalluntersuchungen. Schwachstellen werden nach dem Asset-Typ kategorisiert, den sie betreffen.

### 4.4 Konstruktion von Risikoszenarien

Risikoszenarien werden durch die Kombination eines primären Assets, unterstützender Assets, einer Schwachstelle, einer Bedrohung und der zugehörigen Risikoquelle zu einer zusammenhängenden Erzählung konstruiert. Jedes Szenario beschreibt einen plausiblen Pfad von der Ausnutzung einer Bedrohung bis zur geschäftlichen Auswirkung. Szenarien erfassen, welche CIA-Dimensionen betroffen sind (Vertraulichkeit, Integrität, Verfügbarkeit) und identifizieren den Risikoeigentümer — die Person, die für das Management des Risikos verantwortlich ist.

## 5. Risikoanalyse

### 5.1 Auswirkungsbewertung

Die potenzielle Auswirkung jedes Risikoszenarios wird über die folgenden geschäftsrelevanten Dimensionen bewertet: **Finanziell**, **Reputation**, **Rechtlich & Regulatorisch**, **Operativ** und **Sicherheit & Personal**. Jede Dimension wird auf einer 5-stufigen Skala von **Sehr niedrig** (Stufe 1) bis **Sehr hoch** (Stufe 5) bewertet.

Der Gesamtauswirkungswert für ein Szenario wird nach der Methode des **höchsten Einzelwerts** über alle bewerteten Dimensionen bestimmt. Dies stellt sicher, dass eine schwerwiegende Auswirkung in einer einzelnen Dimension nicht durch niedrigere Bewertungen in anderen Dimensionen verdeckt wird. Organisationen können alternativ einen gewichteten Durchschnitt verwenden, wenn bestimmte Dimensionen (z. B. Sicherheit) das Endergebnis dominieren sollen.

### 5.2 Wahrscheinlichkeitsbewertung

Die Eintrittswahrscheinlichkeit jedes Risikoszenarios wird auf einer 5-stufigen Skala von **Sehr unwahrscheinlich** (Stufe 1) bis **Fast sicher** (Stufe 5) bewertet. Die Wahrscheinlichkeitsbewertung berücksichtigt historische Vorfallsdaten, Bedrohungsinformationen, Ergebnisse von Schwachstellenscans, die Wirksamkeit bestehender Maßnahmen und Expertenwissen.

### 5.3 Berechnung des Risikowerts

Der Risikowert für jedes Szenario wird wie folgt berechnet:

**Risikowert = Auswirkung × Wahrscheinlichkeit**

Dies ergibt einen Risikowertbereich von 1 bis 25. Der Risikowert wird in einer 5×5-Risikomatrix dargestellt, die die Verteilung aller bewerteten Szenarien visualisiert.

## 6. Risikobewertung

Jedes beurteilte Risiko wird mit den definierten Risikoakzeptanzschwellwerten verglichen, um festzustellen, ob eine Behandlung erforderlich ist. Folgende Risikostufen sind definiert:

- **Sehr niedrig (1–4):** Wird ohne weitere Maßnahmen akzeptiert. Überwachung im Rahmen des Normalbetriebs.
- **Niedrig (5–8):** Wird mit dokumentierter Begründung akzeptiert. Überwachung während geplanter Überprüfungen.
- **Mittel (9–12):** Behandlung empfohlen. Überprüfung durch die/den Informationssicherheitsbeauftragte/n.
- **Hoch (13–16):** Behandlung erforderlich. Eskalation an die Geschäftsleitung, falls nicht innerhalb der definierten Frist behandelt.
- **Sehr hoch (17–25):** Sofortige Behandlung erforderlich. Unverzügliche Meldung an die Geschäftsleitung.

Risiken werden in absteigender Reihenfolge ihres Risikowerts priorisiert. Risiken, die den Akzeptanzschwellwert überschreiten, erfordern eine sofortige Behandlung. Risiken innerhalb des Akzeptanzschwellwerts werden dokumentiert und überwacht. Die Ergebnisse der Risikobewertung werden im Risikoregister erfasst.

## 7. Risikobehandlung (ISO 27001 Kapitel 6.1.3)

Für jedes behandlungsbedürftige Risiko wird eine der folgenden Behandlungsoptionen ausgewählt:

### 7.1 Behandlungsoptionen

- **Risikovermeidung:** Die Aktivität oder Bedingung, die das Risiko verursacht, wird vollständig eliminiert. Die Risikoquelle wird durch Einstellung des Prozesses, Außerbetriebnahme des Assets oder Rückzug aus der Geschäftstätigkeit entfernt. Vermiedene Risiken haben einen Restrisikowert von null.
- **Risikomodifikation (Maßnahmen):** Eine oder mehrere Sicherheitsmaßnahmen aus dem ISO-27001-Anhang-A-Maßnahmenkatalog werden angewandt, um die Auswirkung, die Wahrscheinlichkeit oder beides zu reduzieren. Maßnahmen werden basierend auf ihrer Wirksamkeit gegen die spezifische Bedrohungs-Schwachstellen-Kombination ausgewählt. Mehrere Maßnahmen können einem einzelnen Risikoszenario zugeordnet werden. Das Restrisiko nach Umsetzung der Maßnahmen wird erneut bewertet.
- **Risikoteilung (Transfer):** Das Risiko wird durch Versicherung, Auslagerung, vertragliche Zuordnung oder andere Vereinbarungen mit einer externen Partei geteilt. Die Organisation behält die Verantwortlichkeit für das Risiko, überträgt jedoch die finanziellen oder operativen Konsequenzen. Teilungsvereinbarungen werden mit der empfangenden Partei, dem Umfang der Übertragung und dem verbleibenden Restrisiko dokumentiert.
- **Risikobeibehaltung (Akzeptanz):** Das Risiko wird ohne weitere Behandlung akzeptiert. Die Beibehaltung ist angemessen, wenn der Risikowert innerhalb des Akzeptanzschwellwerts liegt, wenn die Behandlungskosten die potenzielle Auswirkung übersteigen oder wenn die Geschäftsleitung eine informierte Entscheidung zur Akzeptanz des Risikos trifft. Jedes beibehaltene Risiko erfordert eine dokumentierte Begründung und formale Akzeptanz durch den Risikoeigentümer.

### 7.2 Erklärung zur Anwendbarkeit

Die Erklärung zur Anwendbarkeit (SoA) dokumentiert alle Maßnahmen aus ISO 27001 Anhang A, ihren Anwendbarkeitsstatus und die Begründung. Für jede anwendbare Maßnahme verzeichnet die SoA, ob die Maßnahme umgesetzt, teilweise umgesetzt oder geplant ist. Nicht anwendbare Maßnahmen enthalten eine Begründung für den Ausschluss. Die SoA wird als lebendes Dokument geführt und aktualisiert, wann immer Maßnahmen hinzugefügt, entfernt oder geändert werden.

### 7.3 Restrisiko

Nach Anwendung der Behandlungsmaßnahmen wird das Restrisiko für jedes Szenario anhand derselben Auswirkungs- und Wahrscheinlichkeitsskalen erneut bewertet. Der Restrisikowert wird mit den Akzeptanzschwellwerten verglichen. Restrisiken, die den Akzeptanzschwellwert weiterhin überschreiten, werden zur Entscheidung an die Geschäftsleitung eskaliert. Alle Restrisiken werden formal von ihren Risikoeigentümern akzeptiert und im Risikobehandlungsplan dokumentiert.

## 8. Risikobehandlungsplan

Der Risikobehandlungsplan (RTP) ist das zentrale Dokument, das die Umsetzung der Risikobehandlungsentscheidungen nachverfolgt. Für jedes behandelte Risikoszenario verzeichnet der RTP:

- Den ursprünglichen Risikowert und die Risikostufe.
- Die gewählte Behandlungsoption und die konkreten umzusetzenden Maßnahmen.
- Die verantwortliche Person (Risikoeigentümer) und den Umsetzungszeitplan.
- Den angestrebten Restrisikowert nach der Behandlung.
- Den tatsächlichen Restrisikowert nach der Umsetzung, verifiziert durch Neubewertung.
- Den Status jeder Behandlungsmaßnahme (geplant, in Bearbeitung, umgesetzt, verifiziert).

Der RTP wird bei jeder Managementbewertung überprüft, um den Fortschritt nachzuverfolgen, überfällige Maßnahmen zu identifizieren und Prioritäten basierend auf veränderten Risikostufen anzupassen. Die Behandlungswirksamkeit wird durch den Vergleich der Gesamtrisikoexposition vor und nach der Behandlung gemessen.

## 9. Risikokommunikation

Risikoinformationen werden an Stakeholder kommuniziert, um fundierte Entscheidungsfindung zu unterstützen:

- **Geschäftsleitung:** Erhält aggregierte Risikoberichte einschließlich der Risikomatrix, Risikostufenverteilung, Behandlungsfortschritt und Restrisikostatus im Rahmen der Managementbewertung.
- **Risikoeigentümer:** Werden über die ihnen zugewiesenen Risiken, die erforderlichen Behandlungsmaßnahmen, Fristen und den aktuellen Restrisikostatus informiert.
- **Informationssicherheitsbeauftragte/r:** Pflegt das Risikoregister, koordiniert Risikobeurteilungen und moderiert die Risikobehandlungsplanung.
- **Interessierte Parteien:** Das Interessengruppen-Register identifiziert, welche interessierten Parteien risikobezogene Kommunikation erfordern, einschließlich Kunden, Regulierungsbehörden und Geschäftspartner, und definiert Umfang, Häufigkeit und Kanal der Kommunikation.

## 10. Überwachung & Überprüfung

Risikobeurteilungen werden in geplanten Abständen und anlassbezogen durchgeführt. Folgende Auslöser initiieren eine Risiko-Neubewertung:

- **Planmäßige Überprüfung:** Mindestens jährlich im Rahmen des ISMS-Managementbewertungszyklus.
- **Wesentliche Änderung:** Organisatorische Umstrukturierung, neue Geschäftsprozesse, Technologieänderungen, Standortverlagerung oder Erweiterung der IT-Infrastruktur.
- **Vorfall oder Beinahe-Vorfall:** Informationssicherheitsvorfälle, Datenschutzverletzungen oder Beinahe-Vorfälle, die bisher nicht identifizierte Risiken aufdecken oder bestehende Risikobeurteilungen ungültig machen.
- **Änderung der Bedrohungslandschaft:** Neue Bedrohungsinformationen, aufkommende Angriffsvektoren, Änderungen im regulatorischen Umfeld oder veröffentlichte Schwachstellenmeldungen, die Systeme im Geltungsbereich betreffen.
- **Auditfeststellungen:** Ergebnisse interner oder externer Audits, die Maßnahmendefizite oder neue Risikobereiche identifizieren.
- **Lieferanten- oder Drittanbieteränderung:** Änderungen an Lieferantenrisikoprofilen, vertraglichen Vereinbarungen oder Serviceniveaus von Drittanbietern.

Die Wirksamkeit von Risikobehandlungsmaßnahmen wird durch Maßnahmentests, Schwachstellenbewertungen, Penetrationstests und Vorfallstrendanalysen überwacht. Überwachungsergebnisse fließen in den nächsten Risikobeurteilungszyklus ein.

## 11. Fortlaufende Verbesserung

Der Risikomanagementprozess unterliegt der fortlaufenden Verbesserung. Erkenntnisse aus Risikobeurteilungen, Überprüfungen der Behandlungswirksamkeit, Vorfällen und Auditfeststellungen werden genutzt, um die Methodik zu verfeinern, die Risikoquellen- und Bedrohungskataloge zu aktualisieren, die Genauigkeit der Auswirkungs- und Wahrscheinlichkeitsbewertungen zu verbessern und die Integration des Risikomanagements in Geschäftsprozesse zu stärken.

Verbesserungsmaßnahmen werden im Register für Korrektur- und Vorbeugungsmaßnahmen (CAPA) dokumentiert und über den ISMS-Korrekturmaßnahmenprozess nachverfolgt. Änderungen an der Risikomanagement-Methodik werden von der Geschäftsleitung genehmigt und allen am Risikomanagement beteiligten Personen kommuniziert.

## 12. Rollen & Verantwortlichkeiten

- **Geschäftsleitung:** Genehmigt diese Richtlinie und die Risikoakzeptanzkriterien. Akzeptiert Restrisiken, die den Akzeptanzschwellwert überschreiten, durch informierte Entscheidung. Überprüft den Risikostatus in der Managementbewertung.
- **Informationssicherheitsbeauftragte/r (ISB):** Pflegt den Risikomanagementprozess, moderiert Risikobeurteilungen, koordiniert die Risikobehandlungsplanung und berichtet der Geschäftsleitung über den Risikostatus.
- **Risikoeigentümer:** Sind für die ihnen zugewiesenen Risiken verantwortlich. Genehmigen Behandlungspläne für ihre Risiken, überwachen die Behandlungsumsetzung und akzeptieren Restrisiken innerhalb ihrer Befugnis.
- **Asset-Eigentümer:** Liefern Informationen zu Asset-Wert, CIA-Anforderungen und Schwachstelleninformationen für ihre zugewiesenen Assets. Unterstützen die Auswirkungsbewertung durch Beschreibung der geschäftlichen Konsequenzen einer Asset-Kompromittierung.
- **Abteilungsleiter:** Beteiligen sich an der Risikoidentifikation und -analyse für ihre Verantwortungsbereiche. Stellen sicher, dass ihren Abteilungen zugewiesene Behandlungsmaßnahmen fristgerecht umgesetzt werden.
- **Alle Beschäftigten:** Melden potenzielle Risiken, Schwachstellen und Vorfälle über die eingerichteten Kanäle. Nehmen an risikobezogenen Schulungs- und Sensibilisierungsmaßnahmen teil.

## 13. Überprüfung & Pflege

Diese Richtlinie wird überprüft:

- Mindestens jährlich im Rahmen des ISMS-Managementbewertungszyklus.
- Wenn die Risikobeurteilungsmethodik aufgrund gewonnener Erkenntnisse angepasst werden muss.
- Wenn wesentliche Änderungen am organisatorischen Kontext, der Bedrohungslandschaft oder dem regulatorischen Umfeld die Risikomanagementpraktiken betreffen.
- Wenn Auditfeststellungen oder Vorfalluntersuchungen Mängel im Risikomanagementprozess identifizieren. 
