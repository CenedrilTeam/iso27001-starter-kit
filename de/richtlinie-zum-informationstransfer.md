# Richtlinie zum Informationstransfer

> **Dokumentenkontrolle**  
> Eigentümer: [RICHTLINIEN_EIGENTÜMER_ROLLE, z. B. Informationssicherheitsbeauftragte/r]  
> Genehmigt von: [GENEHMIGER_NAME_UND_ROLLE]  
> Version: [VERSION]  
> Gültig ab: [GÜLTIGKEITSDATUM]  
> Nächste Überprüfung: [NÄCHSTES_ÜBERPRÜFUNGSDATUM]

## 1. Rechtliche/Regulatorische Grundlage

ISO/IEC 27001:2022 / ISO/IEC 27002:2022, Anhang A — Organisatorische Maßnahmen:

- A 5.14 — Informationsübertragung

BSI IT-Grundschutz:

- CON.9 (Informationsaustausch)
- CON.1 (Kryptokonzept)
- CON.7.A9 (Sicherer Umgang mit mobilen Datenträgern)
- APP.5.3 (Allgemeine E-Mail-Clients und -Server)
- SYS.4.5 (Wechseldatenträger)
- SYS.4.1.A5 (Nutzungsrichtlinien für Drucker, Kopierer und Multifunktionsgeräte)

Weitere jurisdiktionsspezifische Gesetze — insbesondere Datenschutzrecht (DSGVO), Recht der elektronischen Signatur (eIDAS) und sektorspezifische Übertragungspflichten (NIS2, Finanz- und Gesundheitsvorschriften) — sind im Rechtsregister aufgeführt und werden durch Verweis einbezogen.

## 2. Zweck & Geltungsbereich

Diese Richtlinie legt die Regeln, Verfahren und Vereinbarungen für den sicheren Transfer von Informationen bei **[IHR_ORGANISATIONSNAME]** fest. Sie deckt alle Formen des Informationstransfers ab — elektronisch, physische Datenträger und mündlich — sowohl innerhalb der Organisation als auch mit externen Parteien.

Diese Richtlinie gilt für:

- Alle Beschäftigten (unbefristet, befristet, Teilzeit)
- Externes Personal (Auftragnehmer, Berater, Leiharbeitskräfte), das im Auftrag der Organisation Informationen überträgt
- Dritte, mit denen Informationen im Rahmen formaler Vereinbarungen ausgetauscht werden
- Alle Informationen unabhängig vom Format: elektronische Daten, physische Dokumente und Datenträger, mündliche Kommunikation

Die Schutzmaßnahmen für Informationen während der Übertragung spiegeln die Klassifizierungsstufe der beteiligten Informationen gemäß der *Richtlinie zur Informationsklassifizierung und Kennzeichnung* wider. Vor jedem Transfer verifiziert der Absender, dass der Empfänger berechtigt ist, die Informationen zu erhalten, und dass ein geeigneter Übertragungskanal verwendet wird.

## 3. Allgemeine Übertragungsanforderungen (A 5.14)

Die folgenden Anforderungen gelten für alle Arten des Informationstransfers — elektronisch, physisch und mündlich. Sie bilden die Grundlage, die durch die kanalspezifischen Regeln in den nachfolgenden Abschnitten ergänzt wird.

### 3.1 Schutz von Informationen während der Übertragung

Informationen während der Übertragung werden gegen Abfangen, unbefugten Zugriff, Kopieren, Modifikation, Fehlleitung, Zerstörung und Denial of Service geschützt. Das Schutzniveau ist der Klassifizierungsstufe der Informationen angemessen:

- **Verschlüsselung:** Als VERTRAULICH oder höher klassifizierte Informationen werden während der Übertragung mit kryptographischen Verfahren verschlüsselt, die aktuellen Standards entsprechen (AES-256 für symmetrische Verschlüsselung, RSA-2048 / ECDSA P-256 oder höher für asymmetrische Verschlüsselung, TLS 1.2 als Minimum für Transportverschlüsselung — TLS 1.3 bevorzugt). Die Schlüssellängen folgen den Empfehlungen der BSI TR-02102 und werden jährlich überprüft.
- **Zugriffskontrolle:** Übertragungskanäle erzwingen Zugriffskontrollen, die der Klassifizierungsstufe angemessen sind. INTERN-Informationen nutzen mitgliedschaftsbasierte Kanäle (geteilte Laufwerke, Intranet). VERTRAULICH-Informationen nutzen individuell autorisierte, verschlüsselte Kanäle. STRENG VERTRAULICH-Informationen nutzen Ende-zu-Ende-verschlüsselte Kanäle mit Zugriff ausschließlich für benannte Empfänger.
- **Integritätsprüfung:** Übertragungen von als VERTRAULICH oder höher klassifizierten Informationen umfassen Integritätsprüfmechanismen (Prüfsummen, digitale Signaturen oder Hash-Werte), damit Empfänger bestätigen können, dass die Informationen während der Übertragung nicht verändert wurden.
- **Fehlleitungsschutz:** Automatisierte Übertragungssysteme enthalten Validierungsprüfungen (Empfängeradressprüfung, Domain-Whitelisting), um zu verhindern, dass Informationen an falsche Ziele gesendet werden.

Vor der externen Übertragung von Informationen verifiziert der Absender, dass der Empfänger berechtigt ist, Informationen der gegebenen Klassifizierungsstufe zu empfangen, und dass die Übertragungsmethode angemessenen Schutz bietet. Resterinformationen und Metadaten (Änderungsverfolgung, eingebettete Kommentare, versteckte Daten, EXIF-Daten) werden vor der Übertragung aus Dokumenten und Dateien entfernt, um unbeabsichtigte Offenlegung zu verhindern.

### 3.2 Nachvollziehbarkeit & Chain of Custody

Für als VERTRAULICH oder höher klassifizierte Informationen wird während der Übertragung eine Chain of Custody aufrechterhalten:

- **Übertragungsprotokollierung:** Jedes Übertragungsereignis wird protokolliert mit Absenderidentität, Empfängeridentität, Zeitstempel, Inhaltsreferenz (Dokumentenname oder Bezeichner — nicht der Inhalt selbst), verwendeter Übertragungsmethode und angewendeten Schutzmaßnahmen.
- **Digitale Signaturen:** Übertragungen kritischer Geschäftsinformationen (Verträge, Rechtsdokumente, aufsichtsrechtliche Meldungen) nutzen digitale Signaturen zur Nichtabstreitbarkeit — der Absender kann den Versand nicht leugnen, und der Empfänger kann Herkunft und Integrität verifizieren.
- **Empfangsbestätigung:** Bei STRENG VERTRAULICH-Übertragungen bestätigt der Empfänger den Empfang durch eine dokumentierte Bestätigung (digital signierte Antwort, unterzeichneter Lieferschein oder Gleichwertiges).

Übertragungsprotokolle werden gemäß dem Aufbewahrungsplan aufbewahrt und stehen für Audit- und Vorfalluntersuchungszwecke zur Verfügung.

### 3.3 Kontaktverzeichnis für Informationstransfer

Ein Kontaktverzeichnis für den Informationstransfer wird geführt, das die verantwortlichen Personen für jeden Übertragungstyp benennt:

- **Informationseigentümer / Asset-Eigentümer:** Autorisieren Übertragungen ihrer Informationen, genehmigen Empfängerlisten und definieren klassifizierungsspezifische Handhabungsanforderungen.
- **Risikoeigentümer:** Bewerten und akzeptieren Restrisiken im Zusammenhang mit bestimmten Übertragungskanälen oder Drittvereinbarungen.
- **Informationssicherheitsbeauftragte/r:** Berät zu Übertragungssicherheitsmaßnahmen, überprüft Transfervereinbarungen und ist Eskalationspunkt für übertragungsbezogene Sicherheitsanliegen.
- **Informationsverwalter:** Betreiben und pflegen die Übertragungsinfrastruktur (E-Mail-Gateways, Datei-Transferdienste, Kurierprozesse) und stellen sicher, dass die technischen Maßnahmen funktionieren.

Das Kontaktverzeichnis ist allen Beschäftigten im Intranet zugänglich und wird bei Rollenwechseln aktualisiert. Bei Unsicherheit über einen Transfer kontaktieren Beschäftigte den Informationseigentümer oder die/den Informationssicherheitsbeauftragte/n vor dem Fortfahren.

### 3.4 Verantwortlichkeiten & Haftung bei Vorfällen

Verantwortlichkeiten für Informationssicherheitsvorfälle während der Übertragung sind klar zugewiesen:

- **Absenderverantwortung:** Der Absender ist verantwortlich für die Auswahl einer geeigneten Übertragungsmethode, die Anwendung der korrekten Schutzmaßnahmen und die Verifizierung der Empfängerberechtigung. Wenn Informationen während der Übertragung verloren, abgefangen oder beschädigt werden, meldet der Absender den Vorfall sofort über den Vorfallmeldeprozess.
- **Empfängerverantwortung:** Der Empfänger bestätigt den Empfang erwarteter Übertragungen, meldet fehlende oder manipulierte Sendungen und behandelt empfangene Informationen gemäß ihrer Klassifizierungsstufe.
- **Dritttransfers:** Transfervereinbarungen mit externen Parteien enthalten Haftungsklauseln, die Verantwortlichkeiten im Fall von Datenverlust, unbefugtem Zugriff oder Vertraulichkeitsverletzung spezifizieren. Diese Klauseln werden vor der Unterzeichnung von der Rechtsabteilung geprüft.

### 3.5 Kennzeichnung übertragener Informationen

Informationen behalten ihre Klassifizierungskennzeichnung während des gesamten Übertragungsprozesses, damit jeder Bearbeiter und Empfänger die Schutzanforderungen unmittelbar versteht:

- **Elektronische Übertragungen:** E-Mail-Betreffzeilen enthalten das Klassifizierungsstufen-Tag (z. B. [VERTRAULICH]). Dateinamen oder Metadaten tragen die Klassifizierung. Klassifizierungsbanner werden in Kopf- und Fußzeilen von Dokumenten angewendet.
- **Physische Übertragungen:** Die äußere Verpackung zeigt die Klassifizierungsstufe. Für STRENG VERTRAULICH-Material wird eine doppelte Kuvertierung verwendet — der innere Umschlag trägt die Klassifizierungskennzeichnung, der äußere Umschlag zeigt nur Adressinformationen ohne Hinweis auf die Sensibilität des Inhalts.
- **Mündliche Übertragungen:** Die sprechende Person nennt die Klassifizierungsstufe zu Beginn des Gesprächs (siehe Abschnitt 6 zum mündlichen Transfer).

Das Kennzeichnungssystem ist in der *Richtlinie zur Informationsklassifizierung und Kennzeichnung* definiert. Beschäftigte verifizieren, dass die Kennzeichnungen vor Einleitung eines Transfers korrekt angewendet wurden.

### 3.6 Zuverlässigkeit & Verfügbarkeit von Übertragungsdiensten

Die von der Organisation genutzten Übertragungsdienste erfüllen die folgenden Zuverlässigkeits- und Verfügbarkeitsanforderungen:

- **Interne Dienste:** E-Mail, Dateifreigaben und Kollaborationsplattformen werden mit definierten Service-Leveln betrieben (Verfügbarkeitsziele, maximale Ausfallzeiten, Kapazitätsschwellen). Die IT überwacht diese Dienste und meldet Abweichungen.
- **Externe / Drittanbieter-Dienste:** Service Level Agreements (SLAs) mit externen Anbietern von Übertragungsdiensten spezifizieren Verfügbarkeitsgarantien, Reaktionszeiten bei Vorfällen und Datenschutzpflichten. Die SLA-Leistung wird mindestens jährlich überprüft.
- **Failover:** Für geschäftskritische Übertragungskanäle werden alternative Übertragungsmethoden dokumentiert und getestet, damit Informationen auch ausgetauscht werden können, wenn der primäre Kanal nicht verfügbar ist.
- **Kompatibilität:** Vor der Einrichtung eines neuen Übertragungskanals — intern oder mit einer dritten Partei — verifiziert die IT, dass die sendenden und empfangenden Systeme technisch kompatibel sind und die Sicherheitsmaßnahmen Ende-zu-Ende korrekt funktionieren.

### 3.7 Akzeptable Nutzung von Übertragungseinrichtungen

Die Nutzung der Informationsübertragungseinrichtungen bei [IHR_ORGANISATIONSNAME] richtet sich nach der *Richtlinie zur akzeptablen Nutzung*. Zusammenfassend:

- Übertragungseinrichtungen (E-Mail, Dateifreigabe, Messaging, Wechseldatenträger, Fax) werden für geschäftliche Zwecke bereitgestellt. Begrenzte private Nutzung ist zulässig, sofern sie die Sicherheit nicht beeinträchtigt.
- Nur von der IT genehmigte Übertragungsmethoden werden für organisatorische Informationen verwendet. Nicht genehmigte Dateifreigabedienste, private E-Mail-Konten und ungeprüfte Cloud-Plattformen werden nicht zur Übertragung organisatorischer Daten verwendet.
- Beschäftigte umgehen keine technischen Übertragungsmaßnahmen (DLP-Regeln, E-Mail-Verschlüsselung, Web-Filter) und nutzen keine Anonymisierungstools zur Umgehung der Überwachung.

### 3.8 Aufbewahrung & Entsorgung von Übertragungsaufzeichnungen

Geschäftsaufzeichnungen, die über Übertragungskanäle erstellt oder übermittelt werden, unterliegen dem Aufbewahrungsplan der Organisation:

- **E-Mail-Nachrichten:** Werden im E-Mail-Archivsystem für den im Aufbewahrungsplan festgelegten Zeitraum aufbewahrt. Automatische Löschung erfolgt nach Ablauf, sofern kein Legal Hold besteht.
- **Chat- und Instant-Messaging-Protokolle:** Werden für den definierten Zeitraum aufbewahrt. Beschäftigte sind sich bewusst, dass per Chat kommunizierte Geschäftsentscheidungen denselben Aufbewahrungsregeln unterliegen wie E-Mail.
- **Datei-Transferprotokolle:** Übertragungsmetadaten (Absender, Empfänger, Zeitstempel, Dateiname) werden zu Audit-Trail-Zwecken gemäß der Protokollierungsrichtlinie aufbewahrt.
- **Entsorgung:** Wenn Übertragungsaufzeichnungen das Ende ihres Aufbewahrungszeitraums erreichen, werden sie mit Methoden sicher entsorgt, die der Klassifizierungsstufe der Informationen angemessen sind.

### 3.9 Rechtliche, regulatorische & vertragliche Anforderungen

Informationstransfers entsprechen allen geltenden rechtlichen, gesetzlichen, regulatorischen und vertraglichen Verpflichtungen:

- **Datenschutz:** Personenbezogene Daten werden in Übereinstimmung mit der DSGVO und den geltenden nationalen Datenschutzgesetzen übertragen. Grenzüberschreitende Transfers außerhalb des EWR nutzen genehmigte Übermittlungsmechanismen (Angemessenheitsbeschlüsse, Standardvertragsklauseln, verbindliche interne Datenschutzvorschriften).
- **Elektronische Signaturen:** Wenn gesetzliche oder regulatorische Anforderungen authentifizierte Dokumente verlangen (Verträge, aufsichtsrechtliche Meldungen, Auditberichte), werden qualifizierte elektronische Signaturen gemäß der eIDAS-Verordnung (EU) 910/2014 oder gleichwertigem nationalen Recht verwendet.
- **Sektorspezifische Vorschriften:** Transfers, die sektorspezifischen Regeln unterliegen (z. B. Finanzregulierung, Anforderungen an Gesundheitsdaten, Pflichten für kritische Infrastrukturen nach NIS2), halten die in diesen Vorschriften festgelegten zusätzlichen Maßnahmen ein. Das von der Organisation geführte Rechts- und Regulierungsregister dokumentiert, welche Vorschriften gelten.
- **Vertragliche Verpflichtungen:** Transfers zu oder von Vertragspartnern folgen den im jeweiligen Vertrag oder Dienstleistungsvertrag festgelegten Sicherheitsanforderungen. Geheimhaltungsvereinbarungen (NDAs) bestehen vor dem Austausch von VERTRAULICH oder höher klassifizierten Informationen mit externen Parteien.

## 4. Elektronischer Transfer

Elektronischer Transfer umfasst E-Mail, Dateifreigabeplattformen, Kollaborationstools, Instant Messaging, Cloud-Speicher und alle anderen digitalen Kommunikationskanäle. Die folgenden Regeln ergänzen die oben genannten allgemeinen Übertragungsanforderungen.

### 4.1 Malware-Schutz

Alle elektronischen Informationstransfers durchlaufen Malware-Erkennungsmaßnahmen:

- **E-Mail-Gateway:** Eingehende und ausgehende E-Mails werden am E-Mail-Gateway auf Malware gescannt. Anhänge mit ausführbarem Code, makroaktivierte Dokumente oder Dateitypen auf der Sperrliste der Organisation werden in Quarantäne gestellt und der Absender/Empfänger wird benachrichtigt.
- **Datei-Transferdienste:** Dateien, die in organisatorische Dateifreigabe- und Kollaborationsplattformen hochgeladen oder daraus heruntergeladen werden, werden von der plattformintegrierten Anti-Malware-Engine gescannt, bevor sie den Empfängern zur Verfügung stehen.
- **Wechseldatenträger:** Daten, die auf Wechseldatenträger (USB-Sticks, externe Festplatten, optische Medien) geschrieben oder von diesen gelesen werden, werden vor der Verarbeitung auf Malware gescannt (siehe auch Abschnitt 5 zu physischen Datenträgern).
- **Verschlüsselte Transfers:** Wo Ende-zu-Ende-Verschlüsselung einen Scan auf Gateway-Ebene verhindert, führt der Endgeräteschutz auf dem empfangenden Gerät den Malware-Scan bei der Entschlüsselung durch. Empfänger öffnen verschlüsselte Anhänge nicht auf Geräten ohne aktiven, aktuellen Endpunktschutz.

Malware-Schutzmaßnahmen sind auf die *Richtlinie zu Endpunktsicherheit und Malware-Schutz* der Organisation abgestimmt.

### 4.2 Sichere Anhang- & Datei-Handhabung

Sensible elektronische Informationen, die als Anhänge übertragen werden, werden ihrer Klassifizierungsstufe entsprechend geschützt:

- **INTERN:** Standardmäßige Transportverschlüsselung (TLS) zwischen E-Mail-Servern ist ausreichend. Für interne Übertragungen innerhalb des Netzes der Organisation ist keine zusätzliche Anhangverschlüsselung erforderlich.
- **VERTRAULICH:** Extern versendete Anhänge werden verschlüsselt (passwortgeschütztes Archiv mit AES-256 oder S/MIME- / PGP-verschlüsselte E-Mail). Der Entschlüsselungsschlüssel wird über einen separaten Kanal übermittelt (z. B. Telefonat, SMS, separate E-Mail).
- **STRENG VERTRAULICH:** Ende-zu-Ende-Verschlüsselung ist verpflichtend. Anhänge werden nur über genehmigte sichere Datei-Transferdienste mit Zugriff durch benannte Empfänger, Audit-Logging und automatischem Verfall versendet. E-Mail wird für STRENG VERTRAULICH-Anhänge nicht verwendet, sofern nicht sowohl Absender als auch Empfänger Ende-zu-Ende-Verschlüsselung (S/MIME oder PGP) einsetzen.
- **Große Dateien:** Dateien, die das E-Mail-Größenlimit überschreiten, werden über den genehmigten sicheren Datei-Transferdienst der Organisation übertragen — nicht über private Cloud-Speicher, Consumer-Dateifreigabeplattformen oder unverschlüsseltes FTP.

### 4.3 Vermeidung fehlgeleiteter Kommunikation

Maßnahmen sind etabliert, um zu verhindern, dass Informationen an falsche Empfänger gesendet werden:

- **Adressverifizierung:** Die E-Mail-Autovervollständigung ist so konfiguriert, dass externe Empfänger mit einer visuellen Warnung gekennzeichnet werden. Beschäftigte verifizieren die Empfängeradresse vor dem Versand, insbesondere wenn die Nachricht klassifizierte Informationen enthält oder an Verteilerlisten gerichtet ist.
- **Benachrichtigung bei externen Empfängern:** E-Mails an externe Empfänger enthalten automatisch einen Banner oder Disclaimer, der die Nachricht als extern gerichtet kennzeichnet und den Absender zur Bestätigung auffordert, dass eine externe Weitergabe beabsichtigt ist.
- **DLP-Regeln:** Data-Loss-Prevention-Regeln (DLP) kennzeichnen E-Mails und Dateitransfers, die Klassifizierungsmarkierungen (VERTRAULICH, STRENG VERTRAULICH) enthalten und an externe oder unbefugte Empfänger gerichtet sind. Gekennzeichnete Transfers werden zur Absenderbestätigung zurückgehalten oder zur Prüfung an die/den Informationssicherheitsbeauftragte/n weitergeleitet.
- **Rückruf und Löschung:** Wird ein fehlgeleiteter Transfer erkannt, benachrichtigt der Absender sofort die IT und die/den Informationssicherheitsbeauftragte/n. Die IT initiiert einen Rückruf (für E-Mail) oder einen Zugriffsentzug (für Dateifreigabelinks), und der Vorfall wird über den Vorfallmeldeprozess gemeldet.

### 4.4 Genehmigung externer Übertragungsdienste

Externe öffentliche Dienste zur Informationsübertragung erfordern eine vorherige Genehmigung:

- **Genehmigungsprozess:** Bevor ein externer Dienst (Instant Messaging, soziale Netzwerke, Dateifreigabe, Cloud-Speicher) zur Übertragung organisatorischer Informationen genutzt wird, wird ein formaler Antrag an die IT gestellt. Die IT führt in Abstimmung mit der/dem Informationssicherheitsbeauftragten und der/dem Datenschutzbeauftragten eine Sicherheits- und Datenschutzbewertung durch.
- **Register genehmigter Dienste:** Ein Register genehmigter und verbotener externer Übertragungsdienste wird von der IT geführt und im Intranet veröffentlicht. Nur als genehmigt gelistete Dienste werden für geschäftliche Zwecke genutzt.
- **Periodische Überprüfung:** Das Register genehmigter Dienste wird mindestens halbjährlich überprüft. Dienste, die die Sicherheits- oder Datenschutzanforderungen nicht mehr erfüllen, werden entfernt, und Nutzer werden über genehmigte Alternativen informiert.
- **Verbotene Dienste:** Consumer-Dateifreigabe (z. B. privates Dropbox, Google Drive mit Privatkonten), ungeprüfte Messaging-Plattformen und Direktnachrichten in sozialen Medien werden nicht zur Übertragung von Informationen genutzt, die als INTERN oder höher klassifiziert sind.

### 4.5 Authentifizierung in öffentlichen Netzen

Wenn Informationen über öffentlich zugängliche Netze übertragen werden, gelten stärkere Authentifizierungs- und Verschlüsselungsmaßnahmen:

- **VPN-Anforderung:** Der Zugriff auf interne Übertragungsdienste (E-Mail, Dateifreigaben, Kollaborationsplattformen) aus öffentlichen oder nicht vertrauenswürdigen Netzen wird über das VPN der Organisation geleitet. Direkter Zugriff ohne VPN aus öffentlichen Netzen ist technisch blockiert.
- **Multi-Faktor-Authentifizierung (MFA):** Alle über das Internet zugänglichen Übertragungsdienste erfordern MFA. Einfache Passwort-Authentifizierung wird für internetzugängliche Übertragungsdienste nicht akzeptiert.
- **Zertifikatsbasierte Authentifizierung:** Automatisierte System-zu-System-Transfers über öffentliche Netze nutzen zertifikatsbasierte gegenseitige TLS-Authentifizierung. API-Schlüssel oder Token werden nicht in URLs oder Query-Strings übertragen.
- **Öffentliches WLAN:** Bei Nutzung von öffentlichem WLAN (Hotels, Flughäfen, Konferenzorte) läuft der gesamte organisatorische Datenverkehr — einschließlich Informationstransfers — durch das VPN. Keine organisatorischen Daten werden ohne VPN-Schutz über öffentliches WLAN übertragen.

### 4.6 Einschränkungen elektronischer Kommunikation

Die folgenden technischen Einschränkungen werden für elektronische Kommunikationseinrichtungen durchgesetzt, um Datenabfluss zu verhindern:

- **Automatische Weiterleitung:** Die automatische Weiterleitung organisatorischer E-Mails an externe E-Mail-Adressen ist technisch deaktiviert. Die manuelle Weiterleitung klassifizierter Informationen an private oder externe E-Mail-Konten ist untersagt.
- **Inhalt automatischer Antworten:** Abwesenheitsantworten an externe Empfänger enthalten keine sensiblen Informationen wie interne Projektnamen, Kundennamen oder Details zum Aufenthaltsort oder Reiseplan des Beschäftigten.
- **Anhangsgrößenlimits:** Maximale Anhangsgrößen werden am E-Mail-Gateway konfiguriert. Dateien, die das Limit überschreiten, werden an den genehmigten sicheren Datei-Transferdienst umgeleitet.
- **Druckaufträge:** Klassifizierte Dokumente, die an Netzwerkdrucker gesendet werden, nutzen Secure Print (Badge-Freigabe oder PIN). Druckdaten auf dem internen Speicher des Druckers werden verschlüsselt, sofern das Gerät dies unterstützt, und werden nach dem Drucken automatisch gelöscht.

### 4.7 SMS & Instant Messaging

Kurznachrichtendienste (SMS) und Instant Messaging bergen inhärente Risiken für die Informationssicherheit:

- SMS-Nachrichten und Standard-Instant-Messages (WhatsApp privat, Telegram, Consumer-Signal-Gruppen) werden nicht zur Übermittlung von Informationen verwendet, die als VERTRAULICH oder höher klassifiziert sind. Diese Dienste können Nachrichten auf Servern außerhalb der Kontrolle der Organisation speichern, Inhalte auf Sperrbildschirmen für Umstehende sichtbar anzeigen und verfügen nicht über unternehmensweites Audit-Logging.
- Für zeitkritische Kommunikation, die mobile Erreichbarkeit erfordert, wird stattdessen die genehmigte Enterprise-Messaging-Plattform der Organisation (mit Ende-zu-Ende-Verschlüsselung und Enterprise-Schlüsselverwaltung) verwendet.
- Wenn eine kurze, nicht klassifizierte Benachrichtigung per SMS oder Consumer-Messaging versendet wird (z. B. „Bitte prüfe deine E-Mail"), enthält sie keinen klassifizierten Inhalt, keine Kundennamen und keine Projektdetails.

### 4.8 Fax & Legacy-Kommunikation

Faxgeräte und Fax-over-IP-Dienste weisen spezifische Sicherheitsrisiken auf:

- **Eingebaute Nachrichtenspeicher:** Faxgeräte können Kopien gesendeter und empfangener Dokumente im internen Speicher behalten, auf die unbefugte Personen zugreifen können. Nach der Übertragung klassifizierter Dokumente wird der Fax-Speicher gelöscht.
- **Fehlwahlrisiko:** Versehentliches oder absichtliches Fehlprogrammieren von Faxnummern kann dazu führen, dass klassifizierte Informationen an falsche Empfänger gesendet werden. Beschäftigte verifizieren die Faxnummer mit dem Empfänger telefonisch, bevor sie VERTRAULICH-Informationen senden.
- **Bevorzugte Alternativen:** Wo möglich, werden verschlüsselte elektronische Übertragungsmethoden anstelle von Fax verwendet. Ist Fax der einzige verfügbare Kanal (z. B. für bestimmte behördliche oder rechtliche Kommunikation), wird eine sichere Fax-over-IP-Lösung mit Verschlüsselung und Zugriffsprotokollierung gegenüber traditionellem analogen Fax bevorzugt.

## 5. Transfer auf physischen Datenträgern

Physischer Transfer umfasst den Versand, Transport und Empfang von Dokumenten, USB-Sticks, externen Festplatten, Backup-Bändern, optischen Medien und anderen materiellen Medien, die Informationen enthalten. Alle physischen Datenträger, die klassifizierte Informationen enthalten, werden vor dem Versand verschlüsselt (AES-256-Vollverschlüsselung oder Container-Verschlüsselung); der Entschlüsselungsschlüssel wird über einen separaten Kanal übermittelt.

### 5.1 Verantwortlichkeiten bei Versand & Empfang

Klare Verantwortlichkeiten sind für jede Phase des physischen Informationstransfers zugewiesen:

- **Autorisierung:** Der Informationseigentümer autorisiert den Versand physischer Datenträger mit VERTRAULICH oder höher klassifizierten Informationen. Für INTERN-Informationen genehmigt der Leiter der versendenden Abteilung den Versand.
- **Versandbenachrichtigung:** Der Absender benachrichtigt den Empfänger vorab (über einen separaten Kanal wie E-Mail oder Telefon), dass ein physischer Transfer unterwegs ist, einschließlich des erwarteten Liefertermins und einer Referenznummer.
- **Empfangsbestätigung:** Der Empfänger bestätigt den Empfang gegenüber dem Absender innerhalb eines Werktages unter Verwendung der Referenznummer. Wird die Bestätigung nicht innerhalb des erwarteten Zeitraums empfangen, eskaliert der Absender an die/den Informationssicherheitsbeauftragte/n.

### 5.2 Adressierung & Transport

Physische Transfers werden sicher adressiert und transportiert:

- **Adressierung:** Der vollständige Name, die Abteilung und die Organisationsadresse des Empfängers sind deutlich auf der äußeren Verpackung aufgedruckt. Für klassifiziertes Material enthält die äußere Verpackung keinen Hinweis auf die Sensibilität des Inhalts — nur die Routing-Informationen.
- **Sendungsverfolgung:** Transfers von VERTRAULICH oder höher klassifizierten Datenträgern nutzen nachverfolgte Lieferdienste mit Sendungsnummern. Die Sendungsnummer wird im Transferprotokoll erfasst.
- **Zustellungsausfälle:** Wenn eine Zustellung fehlschlägt, zurückgesendet oder als verloren gemeldet wird, werden der Absender und die/der Informationssicherheitsbeauftragte umgehend benachrichtigt. Der Vorfall wird auf potenzielle Datenoffenlegung bewertet und über den Vorfallmeldeprozess behandelt.

### 5.3 Verpackung & Umweltschutz

Die Verpackung schützt den Inhalt während des Transports vor physischen Schäden und Umwelteinflüssen:

- **Papierdokumente:** Als VERTRAULICH und höher klassifizierte Dokumente werden in undurchsichtigen, versiegelten Umschlägen versandt. Für STRENG VERTRAULICH-Material wird doppelte Kuvertierung verwendet.
- **Datenträger:** USB-Sticks, Festplatten, Bänder und optische Medien werden in gepolsterten, antistatischen Behältern verpackt, die gemäß den Lager- und Transportspezifikationen des Herstellers vor Stößen, Hitze, Feuchtigkeit und elektromagnetischen Feldern schützen.
- **Mindeststandard:** Alle physischen Transfers nutzen mindestens undurchsichtige Verpackung. Transparente Beutel, offene Ablagen oder unversiegelte Umschläge werden für klassifiziertes Material nicht verwendet.

### 5.4 Kurier- & Transportdienst-Management

- **Liste autorisierter Kuriere:** Eine von der Geschäftsleitung genehmigte Liste autorisierter und zuverlässiger Kurierdienste wird geführt. Kuriere werden anhand von Sicherheitsfähigkeiten, Erfolgsbilanz, Versicherungsschutz und relevanten Zertifizierungen bewertet. Die Liste wird jährlich und nach jedem kurierbezogenen Sicherheitsvorfall überprüft.
- **Klassifizierungsbasierte Dienstkategorien:** Die Liste genehmigter Kuriere differenziert nach Klassifizierungsstufe. Standardmäßige Post- oder Paketdienste sind für INTERN-Material akzeptabel. VERTRAULICH- und STRENG VERTRAULICH-Material wird ausschließlich durch Kurierdienste transportiert, die verfolgte, unterschriftspflichtige und versicherte Zustellung mit definierten Chain-of-Custody-Verfahren anbieten.
- **Standards zur Kurieridentifikation:** Kurierpersonal identifiziert sich bei Abholung und Zustellung mit einem gültigen Lichtbildausweis und Unternehmensausweis. Für STRENG VERTRAULICH-Transfers ist zusätzlich eine vorab ausgetauschte Referenznummer zur Verifizierung erforderlich.
- **Verifizierungsverfahren:** Personen an Abhol- und Zustellpunkten verifizieren die Identität des Kuriers durch Abgleich des Lichtbildausweises mit dem vorregistrierten Namen, Bestätigung der Zugehörigkeit zum Kurierunternehmen und Validierung der Sendungsreferenznummer. Die Identitätsdetails des Kuriers werden im Versand-/Empfangsprotokoll erfasst.

### 5.5 Manipulationsschutz

Manipulationssichtbare oder manipulationssichere Maßnahmen werden abhängig von der Klassifizierungsstufe der transportierten Informationen angewendet:

- **INTERN:** Standardmäßige versiegelte Umschläge oder Pakete sind ausreichend.
- **VERTRAULICH:** Manipulationssichtbare Siegel (Sicherheitsklebeband, serialisierte manipulationssichtbare Beutel) werden angebracht. Die Siegelnummer wird im Transferprotokoll erfasst und dem Empfänger über einen separaten Kanal mitgeteilt.
- **STRENG VERTRAULICH:** Manipulationssichere Behälter (abschließbare Taschen, Sicherheitskoffer) werden zusätzlich zu manipulationssichtbaren Siegeln verwendet. Behälter und Siegel werden vom Empfänger bei Ankunft geprüft; jegliche Anzeichen von Manipulation werden umgehend der/dem Informationssicherheitsbeauftragten gemeldet.

### 5.6 Protokollierung physischer Transfers

Für alle physischen Informationstransfers wird ein standardisiertes Protokoll geführt, das Folgendes erfasst:

- Inhaltsbeschreibung (was übertragen wird — Dokumententitel, Medientyp, Anzahl der Elemente)
- Klassifizierungsstufe der übertragenen Informationen
- Angewendete Schutzmaßnahmen (Verschlüsselung, manipulationssichtbare Siegel mit Seriennummern, Verpackungsart)
- Liste autorisierter Empfänger
- Übergabezeitpunkt an den Kurier oder Transitverwalter
- Zeitpunkt der Empfangsbestätigung am Zielort
- Identität der an jeder Phase beteiligten Personen (Absender, Kurier, Empfänger)

Die Vorlage für das physische Transferprotokoll ist im Intranet verfügbar. Abgeschlossene Protokolle werden gemäß dem Aufbewahrungsplan aufbewahrt.

## 6. Mündlicher Transfer

Mündlicher Transfer umfasst persönliche Gespräche, Telefonate, Videokonferenzen und Sprachnachrichten. Obwohl mündliche Kommunikation weniger Spuren hinterlässt als elektronischer oder physischer Transfer, unterliegt sie gleichermaßen den Risiken des Abfangens und Abhörens.

### 6.1 Gesprächssicherheit

- **Ortsbewusstsein:** Vertrauliche mündliche Gespräche werden nicht an öffentlichen Orten (Restaurants, Zügen, Flughafen-Lounges, offenen Coworking-Spaces) oder über unsichere Kommunikationskanäle (unverschlüsselte Telefonleitungen, Consumer-Videokonferenzen ohne Ende-zu-Ende-Verschlüsselung) geführt. Ist ein sensibles Gespräch während einer Reise notwendig, findet es in einer privaten Umgebung statt (geschlossenes Hotelzimmer, gebuchter Besprechungsraum) unter Nutzung der genehmigten verschlüsselten Kommunikationstools der Organisation.
- **Teilnehmerprüfung:** Vor der Diskussion von als VERTRAULICH oder höher klassifizierten Informationen verifiziert die Besprechungsorganisation, dass alle Teilnehmer (persönlich und remote) berechtigt sind, Informationen dieser Klassifizierungsstufe zu empfangen. Nicht eingeladene oder unverifizierte Teilnehmer werden gebeten, den Raum zu verlassen, bevor klassifizierte Informationen besprochen werden.
- **Raumkontrollen:** Sensible Gespräche finden in Räumen mit angemessenen physischen Maßnahmen statt — geschlossene Türen, ausreichende Schalldämmung, keine Sicht auf Bildschirme oder Whiteboards von außen. Für STRENG VERTRAULICH-Gespräche werden designierte sichere Besprechungsräume mit verifizierter Schalldämmung verwendet. Mobiltelefone nicht essentieller Teilnehmer werden draußen gelassen oder in einen signalblockierenden Behälter gelegt, sofern die Sensibilität dies rechtfertigt.

### 6.2 Voicemail & Anrufbeantworter

Nachrichten mit klassifizierten Informationen werden nicht auf Voicemail-Systemen oder Anrufbeantwortern hinterlassen. Diese Systeme können:

- Von unbefugten Personen, die sich Zugang zur Mailbox teilen, abgespielt werden
- Auf gemeinsam genutzten Systemen mit unzureichenden Zugriffskontrollen gespeichert werden
- Aufgrund von Fehlwahlen versehentlich auf der falschen Mailbox aufgezeichnet werden

Ist der beabsichtigte Empfänger nicht erreichbar, hinterlässt der Anrufer eine nicht sensible Rückrufbitte (Name, Telefonnummer, „Bitte rufen Sie wegen Projekt X zurück"), ohne klassifizierten Inhalt preiszugeben. Die inhaltliche Diskussion findet statt, wenn direkter Sprachkontakt hergestellt ist.

### 6.3 Klassifizierungshinweis

Sensible Gespräche beginnen mit einem kurzen Klassifizierungshinweis, damit alle Teilnehmer die Handhabungsanforderungen verstehen:

- Die sprechende Person kündigt die Klassifizierungsstufe der zu besprechenden Informationen an (z. B. „Die folgenden Informationen sind als VERTRAULICH klassifiziert und werden nach dem Need-to-know-Prinzip geteilt").
- Deckt das Gespräch Themen unterschiedlicher Klassifizierungsstufen ab, kündigt die sprechende Person den Übergang an, wenn zu einer höheren Stufe gewechselt wird.
- Am Ende des Gesprächs erinnert die sprechende Person die Teilnehmer an etwaige Handhabungsbeschränkungen (z. B. „Bitte besprechen Sie diese Details nicht außerhalb dieser Gruppe").

## 7. Transfervereinbarungen mit Dritten

Wo [IHR_ORGANISATIONSNAME] regelmäßig Informationen mit externen Parteien (Kunden, Lieferanten, Partner, Regulierungsbehörden) austauscht, werden formale Transfervereinbarungen etabliert und gepflegt:

- **Geltungsbereich der Vereinbarung:** Die Vereinbarung spezifiziert die Arten der ausgetauschten Informationen, die beteiligten Klassifizierungsstufen, die zulässigen Übertragungskanäle, die erforderlichen Schutzmaßnahmen und die Verantwortlichkeiten jeder Partei.
- **Empfängerauthentifizierung:** Die Vereinbarung definiert, wie sich Empfänger authentifizieren, bevor sie klassifizierte Informationen erhalten (z. B. vorab ausgetauschte Referenznummern, digitale Zertifikate, benannte Ansprechpersonen).
- **Vertraulichkeitsklauseln:** Für VERTRAULICH oder höher klassifizierte Informationen wird vor dem ersten Transfer eine Geheimhaltungsvereinbarung (NDA) oder gleichwertige Vertraulichkeitsklausel unterzeichnet. Die NDA spezifiziert, wie die empfangende Partei die Informationen speichert, schützt und letztlich zurückgibt oder vernichtet.
- **Vorfallmeldung:** Die Vereinbarung enthält eine gegenseitige Verpflichtung, Sicherheitsvorfälle, die übertragene Informationen betreffen, innerhalb eines vereinbarten Zeitraums zu melden.
- **Überprüfung:** Transfervereinbarungen werden jährlich überprüft und aktualisiert, wenn sich der Umfang des Informationsaustauschs ändert, wenn sich Sicherheitsanforderungen ändern oder nach einem Sicherheitsvorfall, an dem die dritte Partei beteiligt ist.

## 8. Rollen & Verantwortlichkeiten

- **Geschäftsleitung:** Genehmigt diese Richtlinie und Transfervereinbarungen mit Dritten, die STRENG VERTRAULICH-Informationen betreffen. Stellt angemessene Ressourcen für die sichere Übertragungsinfrastruktur bereit.
- **Informationssicherheitsbeauftragte/r (ISB):** Pflegt diese Richtlinie, definiert Übertragungssicherheitsmaßnahmen, überprüft Transfervereinbarungen, untersucht übertragungsbezogene Vorfälle und pflegt das Kontaktverzeichnis für den Informationstransfer.
- **IT-Abteilung:** Betreibt und überwacht die Übertragungsinfrastruktur (E-Mail-Gateways, Datei-Transferdienste, DLP-Systeme, VPN). Pflegt das Register genehmigter Dienste. Setzt technische Maßnahmen um (Blockierung automatischer Weiterleitung, Malware-Scan, Durchsetzung von Verschlüsselung). Bewertet neue Übertragungsdienste auf Sicherheit und Kompatibilität.
- **Datenschutzbeauftragte/r (DSB):** Überprüft Übertragungsregelungen mit Bezug zu personenbezogenen Daten auf DSGVO-Konformität. Berät zu grenzüberschreitenden Übermittlungsmechanismen und Auftragsverarbeitungsverträgen mit Anbietern von Übertragungsdiensten.
- **Informationseigentümer / Asset-Eigentümer:** Autorisieren Übertragungen ihrer Informationen, pflegen autorisierte Empfängerlisten, definieren klassifizierungsspezifische Handhabungsanforderungen und genehmigen Transfervereinbarungen mit Dritten für ihre Informationswerte.
- **Gebäudemanagement / Poststelle:** Betreibt physische Übertragungsprozesse (Versand, Empfang, Kurierkoordination). Verifiziert die Kurieridentifikation. Pflegt das physische Transferprotokoll.
- **Alle Beschäftigten:** Halten diese Richtlinie bei jeder Art von Informationstransfer ein. Verifizieren die Berechtigung des Empfängers und die Eignung des Übertragungskanals. Melden fehlgeleitete, verlorene oder manipulierte Transfers unverzüglich.

## 9. Überprüfung & Pflege

Diese Richtlinie wird überprüft:

- Mindestens jährlich im Rahmen des ISMS-Managementbewertungszyklus.
- Wenn neue Übertragungstechnologien oder -dienste eingeführt werden (z. B. neue Kollaborationsplattform, neuer Dateifreigabedienst, neuer Kurierdienstleister).
- Nach wesentlichen Sicherheitsvorfällen im Zusammenhang mit dem Informationstransfer (Datenabfluss, fehlgeleitete Kommunikation, Kurierverlust).
- Wenn Änderungen im geltenden Recht die Übertragungsanforderungen betreffen (z. B. neue Regeln für grenzüberschreitende Datenübermittlungen, aktualisierte Vorschriften zu elektronischen Signaturen, sektorspezifische Übertragungspflichten).
- Wenn das Klassifizierungsschema oder die Kennzeichnungsverfahren der Organisation wesentlich aktualisiert werden.
