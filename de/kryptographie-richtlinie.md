# Kryptographie-Richtlinie

> **Dokumentenkontrolle**  
> Eigentümer: [RICHTLINIEN_EIGENTÜMER_ROLLE, z. B. Informationssicherheitsbeauftragte/r]  
> Genehmigt von: [GENEHMIGER_NAME_UND_ROLLE]  
> Version: [VERSION]  
> Gültig ab: [GÜLTIGKEITSDATUM]  
> Nächste Überprüfung: [NÄCHSTES_ÜBERPRÜFUNGSDATUM]

## 1. Rechtliche/Regulatorische Grundlage

ISO/IEC 27001:2022 / ISO/IEC 27002:2022, Anhang A — Technologische Maßnahmen:

- A 8.24 — Einsatz von Kryptographie

BSI IT-Grundschutz:

- CON.1.A1 (Auswahl geeigneter kryptographischer Verfahren)
- CON.1.A2 (Datensicherung bei Einsatz kryptographischer Verfahren)
- CON.1.A4 (Geeignetes Schlüsselmanagement)
- CON.1.A5 (Sichere Löschung und Vernichtung von kryptographischen Schlüsseln)
- CON.1.A9 (Festlegung von Kriterien zur Auswahl von Hard- oder Software mit kryptographischen Funktionen)
- CON.1.A10 (Entwicklung eines Kryptokonzepts)
- CON.1.A15 (Reaktion auf praktische Schwächung eines kryptographischen Verfahrens)
- CON.1.A19 (Erstellung eines Kryptokatasters)

Die BSI Technische Richtlinie TR-02102 (Kryptographische Verfahren: Empfehlungen und Schlüssellängen) wird als maßgebliche Quelle für Algorithmenauswahl und Schlüssellängen angewendet.

Weitere jurisdiktionsspezifische Gesetze und Vorschriften — insbesondere Datenschutzrecht (DSGVO), Exportkontrollen für kryptographische Technologien und branchenspezifische Vertraulichkeitsanforderungen — sind im Rechtsregister aufgeführt und werden durch Verweis einbezogen.

## 2. Zweck & Geltungsbereich

Diese Richtlinie legt Regeln für den wirksamen Einsatz von Kryptographie und die Verwaltung kryptographischer Schlüssel bei **[IHR_ORGANISATIONSNAME]** fest. Sie stellt den ordnungsgemäßen und wirksamen Einsatz kryptographischer Verfahren zum Schutz der Vertraulichkeit, Authentizität und Integrität von Informationen in Übereinstimmung mit geschäftlichen, informationssicherheits- und datenschutzrechtlichen Anforderungen sicher.

Die Richtlinie gilt für alle Beschäftigten, IT-Systeme, Anwendungen und Dienste, die Informationen erzeugen, verarbeiten, speichern oder übertragen, die einen kryptographischen Schutz benötigen. Dies umfasst Beschäftigte, Auftragnehmer und Dritte mit Zugriff auf die Informations- und Kommunikationsinfrastruktur der Organisation.

Kryptographie wird eingesetzt, um folgende Informationssicherheitsziele zu erreichen:

- **Vertraulichkeit:** Verschlüsselung schützt sensible oder kritische Informationen, ob gespeichert oder übertragen, sodass nur autorisierte Empfänger sie lesen können.
- **Integrität & Authentizität:** Digitale Signaturen und Message Authentication Codes verifizieren, dass gespeicherte oder übertragene Informationen nicht verändert wurden und vom angegebenen Absender stammen. Dateiintegritätsprüfungs-Algorithmen erkennen unbefugte Änderungen. Kryptographische Hash-Verfahren (SHA-256 oder stärker) stehen zur forensischen Beweismittelsicherung bereit.
- **Nicht-Abstreitbarkeit:** Kryptographische Verfahren liefern Nachweise für das Eintreten oder Nicht-Eintreten eines Ereignisses oder einer Handlung und verhindern, dass eine Partei ihre Beteiligung leugnen kann.
- **Authentisierung:** Kryptographische Verfahren authentisieren Benutzer und Systementitäten, die Zugriff auf Systemnutzer, Entitäten und Ressourcen anfordern oder mit ihnen Transaktionen durchführen.

## 3. Kryptographische Richtlinie (A 8.24)

Der technische Einsatz kryptographischer Verfahren allein reicht nicht aus, um Vertraulichkeit, Integrität und Authentizität zu gewährleisten. Organisatorische Maßnahmen ergänzen die technischen Kontrollen zu einem umfassenden Kryptokonzept. Die folgenden Regeln regeln die Auswahl, Bereitstellung und Nutzung von Kryptographie in der gesamten Organisation.

### 3.1 Allgemeine Grundsätze

- **Rahmen der Kryptographie-Richtlinie:** Diese Richtlinie stellt die themenspezifische Richtlinie zur Kryptographie dar. Sie definiert die allgemeinen Grundsätze für den Schutz von Informationen durch kryptographische Mittel, maximiert den Nutzen kryptographischer Verfahren und minimiert die Risiken unangemessener oder falscher Anwendung.

### 3.2 Auswahl von Algorithmen & Verschlüsselungsstärke

- **Klassifizierungsbasierte Stärke:** Das erforderliche Schutzniveau wird durch die Klassifizierung der zu schützenden Informationen bestimmt. Art, Stärke und Qualität des kryptographischen Algorithmus werden entsprechend gewählt — höhere Klassifizierungsstufen erfordern stärkere Algorithmen und längere Schlüssellängen.
- **Genehmigte Algorithmen & Standards:** Es werden nur etablierte Algorithmen verwendet, die von der Kryptographie-Community intensiv geprüft wurden und für die keine Sicherheitsschwachstellen bekannt sind. Die Organisation folgt den Empfehlungen der BSI Technischen Richtlinie TR-02102 zur Auswahl von Algorithmen, Betriebsarten und Mindestschlüssellängen. Eine Liste genehmigter kryptographischer Algorithmen, Lösungen und Einsatzpraktiken wird geführt und jährlich überprüft.

Bei der Auswahl kryptographischer Hardware oder Software werden folgende Kriterien bewertet: Funktionsumfang, Interoperabilität mit bestehenden Systemen, Fehlerverhalten und Widerstandsfähigkeit gegen Missbrauch, geplante Einsatzdauer des kryptographischen Verfahrens im Verhältnis zu den verwendeten Schlüssellängen, rechtliche und regulatorische Anforderungen sowie datenschutzrechtliche Implikationen. Zertifizierte kryptographische Produkte werden bevorzugt, sofern die Zertifizierung die relevanten kryptographischen Aspekte abdeckt.

### 3.3 Verschlüsselung mobiler Geräte & Speichermedien

- **Verschlüsselung mobiler Geräte & Medien:** Informationen auf mobilen Endgeräten (Laptops, Smartphones, Tablets) und auf Wechselspeichermedien werden im Ruhezustand mittels Vollverschlüsselung oder Container-basierter Verschlüsselung geschützt. Über Netzwerke zu oder von solchen Geräten übertragene Informationen werden durch Transport-Layer-Verschlüsselung (TLS 1.2 oder höher, IPsec-VPN) geschützt.

### 3.4 Auswirkungen auf Inhaltsprüfungs-Kontrollen

- **Inhaltsprüfungs-Kontrollen:** Wo verschlüsselter Datenverkehr Sicherheitsmaßnahmen umgeht, die auf Inhaltsprüfung angewiesen sind (z. B. Malware-Erkennungs-Gateways, Data-Loss-Prevention-Filter, Content-Filter-Proxies), werden kompensierende Maßnahmen umgesetzt. Dazu gehören Endpunkt-basiertes Anti-Malware-Scanning, TLS-Inspektion am Gateway, wo rechtlich und technisch machbar, sowie Sicherheitsmaßnahmen auf Anwendungsebene, die vor der Verschlüsselung greifen.

### 3.5 Rechtliche & grenzüberschreitende Anforderungen

- **Regulatorische & Export-Beschränkungen:** Vor dem Einsatz kryptographischer Verfahren werden anwendbare Vorschriften und nationale Beschränkungen identifiziert — insbesondere bei grenzüberschreitenden Datenflüssen. Import- und Exportbeschränkungen für kryptographische Hard- und Software werden für jede beteiligte Jurisdiktion bewertet. Wo rechtliche Anforderungen in Konflikt stehen (z. B. Datenschutzgesetze verlangen Verschlüsselung, während das Zielland deren Nutzung einschränkt), wird vor dem Transfer eine Risikobewertung durchgeführt und dokumentiert.

### 3.6 Externe kryptographische Dienstleister

- **Service Level Agreements:** Verträge mit externen Anbietern kryptographischer Dienste (z. B. Zertifizierungsstellen, Managed-HSM-Anbieter, Cloud-Key-Management-Dienste) enthalten ausdrückliche Bestimmungen zu Haftung, Dienstzuverlässigkeit, Key-Escrow-Bedingungen, Vorfallreaktionszeiten und Auditrechten. Service Level Agreements definieren Wiederherstellungsziele für Zertifikatsausstellung, -widerruf und Schlüsselwiederherstellungsvorgänge.

## 4. Schlüsselmanagement (A 8.24)

Ein angemessenes Schlüsselmanagement erfordert sichere Prozesse für die Erzeugung, Speicherung, Archivierung, den Abruf, die Verteilung, den Rückzug und die Vernichtung kryptographischer Schlüssel. Das Schlüsselmanagementsystem basiert auf einem abgestimmten Satz von Standards, Verfahren und sicheren Methoden, die den gesamten Schlüssellebenszyklus abdecken. Jeder kryptographische Schlüssel dient nur einem Zweck — insbesondere werden für Verschlüsselung und digitale Signatur getrennte Schlüssel verwendet.

### 4.1 Schlüsselerzeugung

- **Schlüsselerzeugung:** Kryptographische Schlüssel werden mit genehmigten Schlüsselerzeugern in einer sicheren Umgebung erzeugt. Hardware-Zufallszahlengeneratoren oder zertifizierte kryptographische Bibliotheken stellen die Entropie-Quelle bereit. Voreingestellte oder vorinstallierte Schlüssel in kryptographischer Hardware oder Software werden vor dem produktiven Einsatz ersetzt. Schlüssel für verschiedene kryptographische Systeme und Anwendungen werden getrennt erzeugt, um die Auswirkungen einer einzelnen Schlüsselkompromittierung zu begrenzen.

### 4.2 Public-Key-Zertifikate

- **Zertifikatsausstellung:** Public-Key-Zertifikate werden von vertrauenswürdigen Zertifizierungsstellen bezogen. Interne Zertifikate werden über die eigene PKI-Infrastruktur der Organisation oder einen vertraglich gebundenen CA-Dienst ausgestellt. Jeder Zertifikatsantrag wird vor der Ausstellung gegen die Identität der antragstellenden Entität validiert.
- **Authentizitätsprüfung von Zertifikaten:** Bevor man sich auf einen öffentlichen Schlüssel einer dritten Partei verlässt, wird dessen Authentizität über die Zertifikatskette verifiziert. Der Zertifikatswiderrufsstatus wird vor der Nutzung über CRL oder OCSP geprüft. Selbstsignierte Zertifikate werden nur in ausdrücklich dokumentierten Ausnahmen mit kompensierenden Maßnahmen akzeptiert.

### 4.3 Schlüsselverteilung & Aktivierung

- **Schlüsselverteilung & Aktivierung:** Schlüssel werden über sichere Kanäle an die vorgesehenen Empfänger verteilt, die vom Datenkanal getrennt sind. Symmetrische Schlüssel werden niemals im Klartext über denselben Kommunikationsweg wie die verschlüsselten Daten übertragen. Nach Empfang werden Schlüssel über ein dokumentiertes Verfahren aktiviert, das die Integrität und Authentizität des empfangenen Schlüsselmaterials bestätigt.

### 4.4 Schlüsselspeicherung & -schutz

- **Schlüsselspeicherung & Zugriff:** Kryptographische Schlüssel werden in dedizierten Schlüsselspeichern (Hardware Security Modules, verschlüsselte Key Vaults, Secure Enclaves) gespeichert. Der Zugriff auf Schlüssel ist durch rollenbasierte Zugriffskontrolle auf autorisiertes Personal und Systeme beschränkt. Langlebige kryptographische Schlüssel werden zusätzlich offline, außerhalb der operativen IT-Systeme, an einem physisch gesicherten Ort aufbewahrt.
- **Integritätsschutz:** Alle Schlüssel werden durch Integritätsprüfungen (z. B. Prüfsummen, HMAC) vor unbefugter Veränderung und versehentlichem Verlust geschützt, sowohl im Ruhezustand als auch während der Übertragung.
- **Vertraulichkeit geheimer und privater Schlüssel:** Geheime Schlüssel (symmetrisch) und private Schlüssel (asymmetrisch) werden vor unbefugter Nutzung und Offenlegung geschützt. Sie werden verschlüsselt gespeichert, nur über sichere Kanäle übertragen und nur durch authentisierte, autorisierte Prozesse zugänglich gemacht. Schlüsselmaterial erscheint niemals in Protokolldateien, Fehlermeldungen oder Debug-Ausgaben.
- **Physische Sicherheit der Schlüssel-Infrastruktur:** Geräte zur Erzeugung, Speicherung und Archivierung von Schlüsseln (HSMs, Key-Server, Smartcard-Personalisierungsstationen) werden in physisch gesicherten Bereichen mit Zugangskontrolle, Umgebungsüberwachung und manipulationssicherer Ausstattung betrieben.

### 4.5 Schlüsselrotation & Lebenszyklus

- **Schlüsselrotation:** Kryptographische Schlüssel werden in Intervallen gewechselt, die durch Risikobewertung und die Sensibilität der geschützten Daten bestimmt werden. Rotationspläne werden pro Schlüsseltyp dokumentiert: TLS-Zertifikate jährlich, Signaturschlüssel alle zwei Jahre, Verschlüsselungsschlüssel für gespeicherte Daten entsprechend der Klassifizierungsstufe. Automatisierte Rotation wird eingesetzt, wo technisch machbar.
- **Aktivierungs- & Deaktivierungsdaten:** Jeder Schlüssel hat definierte Aktivierungs- und Deaktivierungsdaten. Technische Kontrollen setzen diese Daten durch, sodass Schlüssel nur innerhalb ihres festgelegten Gültigkeitszeitraums nutzbar sind. Ablaufende Schlüssel und Zertifikate lösen automatisierte Warnungen mindestens 30 Tage vor der Deaktivierung aus, um rechtzeitige Erneuerung zu ermöglichen.

### 4.6 Umgang mit kompromittierten Schlüsseln

- **Reaktion auf Schlüsselkompromittierung:** Ein dokumentiertes Verfahren legt die Schritte fest, die bei Verdacht auf oder bestätigter Schlüsselkompromittierung zu befolgen sind. Der kompromittierte Schlüssel wird sofort widerrufen und alle darauf angewiesenen Systeme werden identifiziert und aktualisiert. Ein neuer Schlüssel wird erzeugt und verteilt. Der Vorfall wird an die/den Informationssicherheitsbeauftragte/n gemeldet und über den Vorfallmanagementprozess dokumentiert. Wenn der kompromittierte Schlüssel klassifizierte Informationen geschützt hat, ermittelt eine Risikobewertung, ob eine Neuverschlüsselung der betroffenen Daten erforderlich ist.

### 4.7 Schlüsselwiderruf & Deaktivierung

- **Schlüsselwiderruf & Deaktivierung:** Schlüssel werden widerrufen, wenn sie kompromittiert wurden, wenn der Schlüsselinhaber die Organisation verlässt oder wenn das zugehörige System oder die Anwendung außer Betrieb genommen wird. Widerrufene Schlüssel werden innerhalb von 24 Stunden zu Zertifikatswiderrufslisten hinzugefügt oder im Schlüsselmanagementsystem als inaktiv markiert. Wenn ein Benutzer die Organisation verlässt, werden seine Schlüssel widerrufen und archiviert (nicht vernichtet), um die zukünftige Entschlüsselung historischer Daten zu ermöglichen, sofern gesetzlich erforderlich.

### 4.8 Schlüsselwiederherstellung & Sicherung

- **Schlüsselwiederherstellung:** Ein dokumentiertes Schlüsselwiederherstellungsverfahren stellt sicher, dass verschlüsselte Informationen zugänglich bleiben, wenn ein Schlüssel verloren geht oder beschädigt wird. Wiederherstellungsmechanismen (z. B. Key Escrow, Secret Sharing, Masterkey-Entschlüsselung) werden jährlich getestet. Für langfristig gespeicherte verschlüsselte Daten bestätigen regelmäßige Prüfungen, dass die archivierten Schlüssel und die zugehörige kryptographische Software oder Hardware weiterhin nutzbar sind.
- **Schlüsselsicherung & -archivierung:** Kryptographische Schlüssel werden verschlüsselt gesichert und getrennt von den geschützten Daten gespeichert. Sicherungskopien werden an mindestens zwei physisch getrennten, zugangskontrollierten Standorten aufbewahrt. Archivierte Schlüssel werden für die im Datenaufbewahrungsplan erforderliche Dauer aufbewahrt, zusammen mit der zugehörigen kryptographischen Software oder Algorithmen-Dokumentation, die zu ihrer Nutzung erforderlich ist.

### 4.9 Schlüsselvernichtung

- **Schlüsselvernichtung:** Schlüssel, die nicht mehr benötigt werden, werden mit genehmigten Methoden (kryptographische Löschung, physische Vernichtung der Schlüsselmedien) sicher vernichtet. Das Vernichtungsverfahren und die verwendeten Methoden werden dokumentiert. Vor der Vernichtung eines Schlüssels wird geprüft, dass keine verschlüsselten Daten, die zukünftigen Zugriff erfordern, von diesem Schlüssel abhängen. Das Vernichtungsereignis wird mit Zeitstempel, verantwortlicher Person und verwendeter Methode protokolliert.

### 4.10 Protokollierung & Audit

- **Protokollierung & Audit:** Alle Schlüsselmanagement-Aktivitäten werden protokolliert — einschließlich Schlüsselerzeugung, -verteilung, -aktivierung, -rotation, -widerruf, -wiederherstellung und -vernichtung. Protokolle werden manipulationssicher gespeichert, gemäß dem Protokollaufbewahrungsplan der Organisation aufbewahrt und regelmäßig von der/dem Informationssicherheitsbeauftragten überprüft. Anomalien in Schlüsselnutzungsmustern (z. B. ungewöhnliche Zugriffshäufigkeit, Zugriff außerhalb der Geschäftszeiten) lösen Warnungen zur Untersuchung aus.

### 4.11 Rechtliche Zugriffsanfragen

- **Rechtliche Zugriffsanfragen:** Ein Verfahren regelt die Reaktion auf rechtliche Anfragen zum Zugriff auf kryptographische Schlüssel oder entschlüsselte Daten (z. B. Gerichtsbeschlüsse, die verschlüsselte Informationen unverschlüsselt als Beweismittel fordern). Solche Anfragen werden vor der Herausgabe von Schlüsselmaterial oder entschlüsselten Daten durch die Rechtsabteilung geprüft. Alle Offenlegungen werden mit der Rechtsgrundlage, dem Umfang, der genehmigenden Stelle und dem Datum dokumentiert.

Der Gesamtansatz zum Schlüsselmanagement — einschließlich der Methoden zur Erzeugung, zum Schutz und zur Wiederherstellung kryptographischer Schlüssel — ist in den obigen Unterabschnitten beschrieben. Dieser Ansatz deckt den vollständigen Schlüssellebenszyklus ab und adressiert die Wiederherstellung verschlüsselter Informationen im Falle verlorener, kompromittierter oder beschädigter Schlüssel durch dokumentierte Wiederherstellungs- und Sicherungsverfahren.

## 5. Kryptokataster

Ein Kryptokataster wird geführt und mindestens jährlich aktualisiert. Für jede Gruppe von IT-Systemen, die kryptographische Funktionen nutzen, werden folgende Informationen erfasst:

- **Zweck:** Der Anwendungsfall (z. B. Vollverschlüsselung, TLS für Kommunikation, digitale Signaturen, VPN-Tunnel).
- **Verantwortliche Person:** Der Systemeigentümer oder Administrator, der für die kryptographische Umsetzung verantwortlich ist.
- **Algorithmus & Parameter:** Der verwendete kryptographische Algorithmus, der Betriebsmodus und die Schlüssellänge.
- **Produkt:** Das eingesetzte kryptographische Hardware- oder Softwareprodukt (einschließlich Version).
- **Schlüssellebenszyklus-Status:** Aktueller Schlüsselgültigkeitszeitraum, letztes Rotationsdatum und nächste geplante Rotation.

Das Kataster ist mit dem Asset-Inventar der Organisation querverknüpft und dient als Grundlage für die jährliche Algorithmenüberprüfung (siehe Überprüfung & Pflege).

## 6. Rollen & Verantwortlichkeiten

- **Geschäftsleitung:** Genehmigt diese Richtlinie, stellt Ressourcen für die kryptographische Infrastruktur bereit und stellt die Ausrichtung an Geschäftszielen und rechtlichen Anforderungen sicher.
- **Informationssicherheitsbeauftragte/r (ISB):** Pflegt diese Richtlinie, definiert genehmigte Algorithmen und Schlüssellängen, überprüft das Kryptokataster, bewertet die Auswirkungen geschwächter Algorithmen und koordiniert die Vorfallreaktion bei Schlüsselkompromittierungen.
- **IT-Betrieb / Schlüsseladministratoren:** Setzen die in dieser Richtlinie definierten kryptographischen Maßnahmen und Schlüsselmanagementverfahren um. Erzeugen, verteilen, rotieren, sichern und vernichten Schlüssel gemäß den dokumentierten Prozessen. Pflegen das Kryptokataster und stellen rechtzeitige Zertifikatserneuerung sicher.
- **System- & Anwendungseigentümer:** Stellen sicher, dass kryptographische Anforderungen für ihre Systeme während Design und Beschaffung identifiziert werden. Wählen kryptographische Lösungen aus der genehmigten Liste aus und integrieren sie gemäß dieser Richtlinie.
- **Alle Beschäftigten:** Nutzen kryptographische Werkzeuge wie angewiesen (z. B. Verschlüsselung von Laptops, VPN-Nutzung für Remote-Zugriff, Überprüfung digitaler Signaturen). Melden vermutete Schlüsselkompromittierungen oder kryptographische Fehler unverzüglich an die/den Informationssicherheitsbeauftragte/n.

## 7. Überprüfung & Pflege

Diese Richtlinie und das zugehörige Kryptokataster werden überprüft:

- Mindestens jährlich auf Grundlage des Kryptokatasters, um zu verifizieren, dass alle eingesetzten Algorithmen, Schlüssellängen und kryptographischen Produkte sicher bleiben und keine bekannten Schwachstellen bestehen.
- Wenn die BSI Technische Richtlinie TR-02102 oder gleichwertige internationale Empfehlungen mit neuen Algorithmen- oder Schlüssellängenleitfäden aktualisiert werden.
- Nach jedem kryptographischen Vorfall (Schlüsselkompromittierung, Offenlegung einer Algorithmusschwäche, CA-Einbruch).
- Wenn neue rechtliche oder regulatorische Anforderungen identifiziert werden, die die Kryptographie betreffen (z. B. Änderungen bei Exportkontrollen, Post-Quantum-Readiness).
- Nach wesentlichen Änderungen an der IT-Landschaft, den Geschäftsprozessen oder dem Risikoprofil der Organisation.

Wird ein eingesetzter Algorithmus als geschwächt befunden, stellt der in dieser Richtlinie definierte Reaktionsprozess sicher, dass der betroffene Algorithmus entweder gehärtet (z. B. erhöhte Schlüssellänge) oder durch eine sichere Alternative ersetzt wird, bevor die Schwäche ausgenutzt werden kann.
