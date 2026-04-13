# Richtlinie zu Telearbeit & BYOD

> **Dokumentenkontrolle**  
> Eigentümer: [RICHTLINIEN_EIGENTÜMER_ROLLE, z. B. Informationssicherheitsbeauftragte/r]  
> Genehmigt von: [GENEHMIGER_NAME_UND_ROLLE]  
> Version: [VERSION]  
> Gültig ab: [GÜLTIGKEITSDATUM]  
> Nächste Überprüfung: [NÄCHSTES_ÜBERPRÜFUNGSDATUM]

## 1. Rechtliche/Regulatorische Grundlage

ISO/IEC 27001:2022 / ISO/IEC 27002:2022, Anhang A — Personenbezogene Maßnahmen:

- A 6.7 — Telearbeit

BSI IT-Grundschutz:

- OPS.1.2.4 (Telearbeit — Regelungen, Sicherheitskonzept, Kommunikation)
- INF.8 (Häuslicher Arbeitsplatz — Physische Sicherheit, Zutrittskontrolle)
- INF.9 (Mobiler Arbeitsplatz — Auswahl, Regeln, Sichtschutz)
- NET.3.3 (VPN — Planung, Konfiguration, Zugriffsmanagement)

Weitere jurisdiktionsspezifische Gesetze — insbesondere Arbeitsrecht, Datenschutzrecht (DSGVO), Arbeitsschutzvorschriften und Betriebsverfassungsgesetz — sind im Rechtsregister aufgeführt und werden durch Verweis einbezogen.

## 2. Zweck & Geltungsbereich

Diese Richtlinie legt die Informationssicherheitsanforderungen für Telearbeit bei **[IHR_ORGANISATIONSNAME]** fest. Sie deckt alle Formen der Arbeit außerhalb der Räumlichkeiten der Organisation ab, einschließlich Homeoffice, mobiler Arbeitsplätze, Coworking-Spaces und aller anderen Orte, an denen Personen über IKT-Geräte auf organisatorische Informationen zugreifen.

Diese Richtlinie gilt für:

- Alle Beschäftigten, die remote arbeiten (Vollzeit, Teilzeit, gelegentlich)
- Externes Personal (Auftragnehmer, Berater, Leiharbeitskräfte), das außerhalb der Räumlichkeiten der Organisation arbeitet
- Alle Geräte, die für den Remote-Zugriff verwendet werden, einschließlich organisationseigener und, wo ausdrücklich zulässig, privater Geräte (BYOD)

Ziel ist es, sicherzustellen, dass Informationen, die während der Telearbeit verarbeitet, gespeichert und übertragen werden, denselben Schutz erhalten wie Informationen, die innerhalb der Räumlichkeiten der Organisation bearbeitet werden, bei gleichzeitiger Ermöglichung flexibler Arbeitsformen.

## 3. Sicherheitsbedingungen & Risikoerwägungen (A 6.7)

[IHR_ORGANISATIONSNAME] gestattet Telearbeit unter den in dieser Richtlinie festgelegten Bedingungen und Einschränkungen. Bevor Personen mit der Telearbeit beginnen, werden die geltenden Sicherheitsanforderungen kommuniziert und bestätigt. Die folgenden Bedingungen gelten für alle Telearbeitsarrangements:

### 3.1 Physische Sicherheit der Remote-Standorte

- **Bewertung der Standortsicherheit:** Bevor Telearbeit an einem neuen Standort beginnt, führen Personen eine Selbstbewertungscheckliste durch, die die physische Sicherheit des Standorts bewertet. Die Bewertung umfasst Gebäudezugangskontrollen, Abschließbarkeit von Räumen, das Risiko unbefugten Zutritts sowie jurisdiktionsbezogene Unterschiede, die geltendes Sicherheits- und Datenschutzrecht betreffen. Standorte, die die Mindestkriterien nicht erfüllen, werden nicht für die Verarbeitung sensibler Informationen zugelassen.
- **Zulässige Arbeitsplatztypen:** Telearbeit findet in Homeoffices mit einem dedizierten Arbeitsbereich oder in vorab genehmigten Coworking-Spaces statt, die die Mindestanforderungen an Infrastruktur und Privatsphäre erfüllen. Öffentliche Verkehrsmittel, offene Cafés und andere Orte, an denen visuelle oder akustische Privatsphäre nicht gewährleistet werden kann, werden nicht zur Verarbeitung vertraulicher oder eingeschränkter Informationen genutzt.
- **Regeln für das physische Umfeld:** Remote-Arbeitsplätze sind mit einem abschließbaren Schrank oder Behälter für die Aufbewahrung vertraulicher Dokumente und Wechseldatenträger ausgestattet. An allen Remote-Standorten gilt eine Clean-Desk-Praxis. Vertrauliche Dokumente werden in versiegelten, nicht durchsichtigen Behältern zwischen Standorten transportiert. Das Drucken vertraulicher Dokumente am Remote-Arbeitsplatz wird nach Möglichkeit vermieden; wo notwendig, werden Ausdrucke sofort gesichert und mit einem Kreuzschnittschredder vernichtet oder zur sicheren Vernichtung an die Organisation zurückgegeben. Sicherheitsvorfälle werden unverzüglich über die etablierten Meldewege gemeldet (siehe Richtlinie zur Vorfallmeldung).

### 3.2 Kommunikationssicherheit & Netzwerkzugriff

- **Verschlüsselter Remote-Zugriff:** Jeder Remote-Zugriff auf das Netzwerk der Organisation erfolgt über eine kryptographisch geschützte VPN-Verbindung. Die VPN-Konfiguration berücksichtigt die Sensibilität der zugegriffenen Systeme und die Klassifizierung der über die Verbindung übertragenen Informationen. Split Tunneling ist auf VPN-Clients deaktiviert, um Datenabfluss über ungeschützte Kanäle zu verhindern.
- **Regeln für Heim- & öffentliche Netzwerke:** Öffentliche WLAN-Netze werden nur in Verbindung mit dem VPN der Organisation genutzt. Heimnetzwerke werden so konfiguriert, dass sie Mindestsicherheitsstandards erfüllen: WPA3-Verschlüsselung (oder mindestens WPA2), geändertes Router-Standardpasswort, aktuelle Router-Firmware und ein separates Gastnetzwerk, in dem IoT-Geräte des Haushalts verbunden sind. Die Personen verifizieren diese Einstellungen vor Beginn der Telearbeit und erneut jährlich oder nach einem Router-Tausch.
- **Authentifizierung & Zugriffskontrolle:** Der Remote-Zugriff auf das Netzwerk der Organisation erfordert Multi-Faktor-Authentifizierung (MFA). Einfache Passwort-Authentifizierung ist für den Remote-Netzwerkzugriff nicht zulässig. Die für Remote-Sitzungen gewährten Zugriffsrechte folgen dem Prinzip des geringsten Privilegs und sind auf die für die zugewiesenen Aufgaben erforderlichen Systeme und Daten beschränkt.

### 3.3 Remote-Zugriffstechnologien

- **Virtueller Desktop & Remote-Zugriff:** Wenn private Geräte für Telearbeit genutzt werden (BYOD), erfolgt der Zugriff ausschließlich über eine Virtual Desktop Infrastructure (VDI) oder eine vergleichbare Remote-Zugriffslösung. Dies stellt sicher, dass organisatorische Daten auf von der Organisation kontrollierten Systemen verarbeitet und gespeichert werden, nicht auf dem privaten Gerät selbst. Die direkte Speicherung organisatorischer Informationen auf privaten Geräten ist untersagt, sofern sie nicht ausdrücklich genehmigt und verschlüsselt ist.
- **Sichere Bereitstellung & Initialisierung:** Remote-Arbeitsgeräte werden durch einen zentralisierten, automatisierten Prozess bereitgestellt und initialisiert. Betriebssystem-Images, Sicherheitskonfigurationen und erforderliche Software werden über das Endgeräte-Management-System der Organisation bereitgestellt. Die manuelle Einrichtung von Remote-Arbeitsgeräten durch Endnutzer ist nicht zulässig. Änderungen an Sicherheitskonfigurationen erfordern die Autorisierung durch die IT.

### 3.4 Schutz vor unbefugtem Zugriff

- **Schutz im Homeoffice:** Im Homeoffice werden Bildschirme so positioniert, dass Haushaltsmitglieder und Besucher den Inhalt nicht einsehen können. Beim Verlassen des Arbeitsplatzes — auch kurzzeitig — wird der Bildschirm gesperrt. Vertrauliche Telefonate und Videokonferenzen werden in einem geschlossenen Raum durchgeführt. Kinder und andere Haushaltsmitglieder haben keinen Zugang zu Arbeitsgeräten, und Arbeitsgeräte werden bei Nichtgebrauch in einem verschlossenen Raum aufbewahrt.
- **Schutz in der Öffentlichkeit:** Beim Arbeiten an öffentlichen oder halböffentlichen Orten wird auf allen Geräten ein Sichtschutzfilter verwendet. Vertrauliche oder eingeschränkte Informationen werden nicht in Umgebungen angezeigt oder besprochen, in denen Dritte beobachten oder mithören können. Geräte werden niemals unbeaufsichtigt gelassen; wenn Personen ihren Sitzplatz verlassen (z. B. im Zug oder in einer Flughafen-Lounge), werden alle Geräte und Dokumente mitgenommen oder gesichert.

### 3.5 Endpunktsicherheitsmaßnahmen

- **Firewall & Malware-Schutz:** Jedes für Telearbeit verwendete Gerät verfügt über eine aktive, zentral verwaltete Host-Firewall und aktuelle Anti-Malware-Software. Die Firewall ist so konfiguriert, dass sie alle eingehenden Verbindungen blockiert, die nicht ausdrücklich erforderlich sind. Anti-Malware-Definitionen werden mindestens täglich automatisch aktualisiert. Echtzeit-Scanning ist aktiviert und kann vom Nutzer nicht deaktiviert werden.

## 4. Umsetzungsmaßnahmen für Telearbeit

Die folgenden Maßnahmen werden von [IHR_ORGANISATIONSNAME] umgesetzt, um sichere Telearbeitsarrangements zu unterstützen:

### 4.1 Ausstattung & Arbeitsplatzbereitstellung

- **Ausstattungsbereitstellung:** Die Organisation stellt alle für Telearbeit erforderlichen Ausstattungen bereit, einschließlich Laptops, Monitoren, Dockingstationen, Tastaturen und abschließbaren Aufbewahrungsmöbeln. Die Nutzung privater Geräte zur Verarbeitung organisatorischer Informationen ist nicht zulässig, sofern sie nicht ausdrücklich über den BYOD-Genehmigungsprozess genehmigt wurde. Alle von der Organisation ausgegebenen Geräte sind mit Asset-Tags versehen, inventarisiert und unterliegen den Asset-Management-Verfahren der Organisation.
- **Sicherheit des physischen Arbeitsplatzes:** Der Homeoffice-Arbeitsplatz befindet sich in einem separaten Raum oder einem klar abgegrenzten Bereich, der gegen unbefugten Zutritt gesichert werden kann. Fenster und Türen werden bei Nichtbelegung des Arbeitsplatzes geschlossen und abgeschlossen. Rauchmelder und angemessene Stromversorgung (Überspannungsschutz) sind vorhanden. Personen, die von Standorten mit erhöhtem Einbruchrisiko arbeiten, treffen zusätzliche Schutzmaßnahmen (z. B. Sicherheitsschlösser, Alarmanlagen) gemäß Empfehlung der Organisation.

### 4.2 Zulässige Arbeit & Zugriffsautorisierung

- **Zulässige Arbeit & Informationsklassifizierung:** Die Führungskraft und die/der Informationssicherheitsbeauftragte legen gemeinsam fest, welche Aufgaben für die Remote-Ausführung zulässig sind, welche Informationsklassifizierungsstufen remote bearbeitet werden und auf welche internen Systeme und Dienste der Remote-Arbeitende zugreifen darf. Als STRENG VERTRAULICH klassifizierte Informationen werden nicht remote verarbeitet, sofern nicht eine explizite Risikobewertung abgeschlossen und genehmigt wurde. Diese Genehmigungen werden dokumentiert und jährlich überprüft.
- **Regeln für Familien- & Besucherzugang:** Haushaltsmitglieder und Besucher verwenden unter keinen Umständen organisationseigene Geräte. Arbeitsgeräte werden in einem verschlossenen Raum oder abschließbaren Schrank aufbewahrt, wenn sie nicht aktiv genutzt werden. Videoanrufe und Bildschirmfreigabesitzungen werden an einem Ort durchgeführt, an dem Haushaltsmitglieder und Besucher den Bildschirm nicht einsehen oder das Gespräch mithören können.

### 4.3 Schulung zur Telearbeit

- **Schulung zur Telearbeit:** Alle Personen, die remote arbeiten, und alle IT-Support-Mitarbeiter, die Remote-Arbeitende unterstützen, absolvieren vor Beginn der Telearbeit eine dedizierte Telearbeits-Sicherheitsschulung. Die Schulung umfasst den sicheren Umgang mit Geräten und Informationen außerhalb des Büros, VPN-Nutzung, Clean-Desk-Praktiken, Vorfallmeldung, physische Sicherheit des Remote-Arbeitsplatzes und die korrekte Handhabung vertraulicher Telefonate und Videokonferenzen. Auffrischungsschulungen finden jährlich und bei jeder Aktualisierung dieser Richtlinie statt.

### 4.4 Mobile Device Management & Sicherheit

- **Gerätesicherheitsmaßnahmen:** Alle Remote-Zugriffsgeräte werden in die Mobile-Device-Management-Plattform (MDM) oder Endgeräte-Management-Plattform der Organisation eingebunden. Die folgenden Sicherheitsmaßnahmen werden zentral durchgesetzt: automatische Bildschirmsperre nach maximal 5 Minuten Inaktivität, starker Passcode oder biometrische Entsperrung, Vollverschlüsselung der Festplatte, Geräte-Standortverfolgung (mit Zustimmung der Beschäftigten gemäß Datenschutzrecht aktiviert) und Remote-Wipe-Fähigkeit. Verlorene oder gestohlene Geräte werden umgehend gemeldet, und ein Remote-Wipe wird unverzüglich ausgelöst.

### 4.5 Support, Wartung & Versicherung

- **Hardware- & Software-Support:** Die IT-Abteilung bietet Remote-Support für alle von der Organisation ausgegebenen Geräte über Remote-Desktop-Tools und einen dedizierten Helpdesk. Bei Hardwaredefekten, die nicht remote behoben werden können, wird ein Ersatzgerät geliefert oder der Beschäftigte bringt das Gerät ins Büro. Designierte IT-Ansprechpersonen und Supportzeiten werden allen Remote-Arbeitenden kommuniziert. Remote-Wartungs- und Fehlerbehebungssitzungen werden protokolliert.
- **Versicherungsschutz:** Die Organisation unterhält einen angemessenen Versicherungsschutz für an Remote-Arbeitsplätzen verwendete Ausstattung, einschließlich Deckung für Diebstahl, Beschädigung und Transport. Die Beschäftigten werden über den Deckungsumfang und ihre Pflicht zur unverzüglichen Meldung von Schäden oder Verlusten informiert.

### 4.6 Datensicherung & Business Continuity

- **Datensicherung & Business Continuity:** Während der Telearbeit erstellte oder geänderte Daten werden auf von der Organisation verwalteten Systemen (Netzwerklaufwerke, Cloud-Speicher) gespeichert und nicht auf lokalen Geräten. Wo lokale Speicherung unvermeidbar ist, wird eine automatische Synchronisation mit der zentralen Sicherungsinfrastruktur konfiguriert. Remote-Arbeitende überprüfen regelmäßig, ob ihre Datensynchronisation ordnungsgemäß funktioniert. Business-Continuity-Pläne berücksichtigen Szenarien, in denen Remote-Arbeitende die Verbindung oder Geräte verlieren, und alternative Arbeitsverfahren werden dokumentiert.

### 4.7 Audit & Sicherheitsüberwachung

- **Audit & Sicherheitsüberwachung:** Remote-Zugriffssitzungen werden zentral protokolliert, einschließlich Nutzeridentität, Verbindungszeitpunkt, Dauer und zugegriffener Ressourcen. Protokolle werden regelmäßig auf Anomalien überprüft (z. B. Zugriffe von ungewöhnlichen Orten, Verbindungen außerhalb der Arbeitszeiten, fehlgeschlagene Authentifizierungsversuche). Die Organisation behält sich das Recht vor, Remote-Arbeitsplätze mit angemessener Vorankündigung und in Übereinstimmung mit dem Datenschutzrecht auf Einhaltung dieser Richtlinie zu auditieren. Feststellungen aus Audits fließen in die kontinuierliche Verbesserung dieser Richtlinie ein.

### 4.8 Beendigung von Telearbeitsarrangements

- **Beendigung der Telearbeit:** Wenn ein Telearbeitsarrangement endet — sei es durch Rollenwechsel, Ende des Beschäftigungsverhältnisses oder organisatorische Entscheidung — werden alle Remote-Zugriffsrechte unverzüglich widerrufen. Alle organisationseigenen Geräte (Laptops, Monitore, Dockingstationen, Aufbewahrungsmöbel, Zugangstokens) werden innerhalb von fünf Werktagen zurückgegeben. Eine dokumentierte Übergabecheckliste wird ausgefüllt. VPN-Zugangsdaten und Zertifikate, die für das Remote-Arrangement spezifisch sind, werden am selben Tag deaktiviert, an dem das Arrangement endet.

## 5. Rollen & Verantwortlichkeiten

- **Geschäftsleitung:** Genehmigt diese Richtlinie, stellt Ressourcen für eine sichere Telearbeitsinfrastruktur bereit und gibt die strategische Ausrichtung für Telearbeit vor.
- **Informationssicherheitsbeauftragte/r (ISB):** Definiert Sicherheitsanforderungen für Telearbeit, führt Risikobewertungen für Telearbeitsszenarien durch, überwacht die Einhaltung und aktualisiert diese Richtlinie.
- **IT-Abteilung:** Stellt Telearbeitsausstattung bereit und verwaltet sie, betreibt VPN- und MDM-Infrastruktur, bietet Helpdesk-Support und setzt technische Maßnahmen um.
- **Personalabteilung (HR):** Integriert Telearbeitsbedingungen in Arbeitsverträge, koordiniert Telearbeitsvereinbarungen und verwaltet das Onboarding/Offboarding von Remote-Arbeitenden.
- **Führungskräfte:** Genehmigen Telearbeitsarrangements für ihr Team, bestimmen zulässige Aufgaben und Informationsklassifizierungen und verifizieren, dass Teammitglieder diese Richtlinie einhalten.
- **Alle Remote-Arbeitenden:** Halten diese Richtlinie ein, absolvieren erforderliche Schulungen, sichern ihren Remote-Arbeitsplatz und melden Sicherheitsvorfälle unverzüglich.

## 6. Überprüfung & Pflege

Diese Richtlinie wird überprüft:

- Mindestens jährlich im Rahmen des ISMS-Managementbewertungszyklus.
- Nach wesentlichen Änderungen an der Telearbeitsinfrastruktur oder Technologielandschaft.
- Nach Sicherheitsvorfällen im Zusammenhang mit Telearbeit.
- Wenn Änderungen im geltenden Recht (Arbeitsrecht, Datenschutz, Arbeitsschutz) die Bedingungen für Telearbeit beeinflussen.
