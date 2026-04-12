# Richtlinie zur Informationsklassifizierung und -kennzeichnung

> **Dokumentenkontrolle**  
> Eigentümer: [RICHTLINIEN_EIGENTÜMER_ROLLE, z. B. Informationssicherheitsbeauftragte/r]  
> Genehmigt von: [GENEHMIGER_NAME_UND_ROLLE]  
> Version: [VERSION]  
> Gültig ab: [GÜLTIGKEITSDATUM]  
> Nächste Überprüfung: [NÄCHSTES_ÜBERPRÜFUNGSDATUM]

## 1. Rechtliche/Regulatorische Grundlage

ISO/IEC 27001:2022 / ISO/IEC 27002:2022, Anhang A — Organisatorische Maßnahmen:

- A 5.12 — Klassifizierung von Informationen
- A 5.13 — Kennzeichnung von Informationen

BSI IT-Grundschutz:

- ISMS.1.A10 (Sicherheitskonzept)
- BSI-Standard 200-2 Kapitel 5.1 (Klassifikation von Geschäftsprozessen und Informationen)
- BSI-Standard 200-2 Kapitel 8.2 (Schutzbedarfsfeststellung)

Weitere jurisdiktionsspezifische Gesetze und Vorschriften — insbesondere Datenschutzrecht (DSGVO), Geschäftsgeheimnisschutz und branchenspezifische Vertraulichkeitsanforderungen — sind im Rechtsregister aufgeführt und werden durch Verweis einbezogen.

## 2. Zweck & Geltungsbereich

Diese Richtlinie legt ein einheitliches Klassifizierungs- und Kennzeichnungsschema für Informationen und andere zugehörige Assets bei **[IHR_ORGANISATIONSNAME]** fest. Sie stellt sicher, dass Informationen ein angemessenes Schutzniveau entsprechend ihrer Bedeutung für die Organisation erhalten, unter Berücksichtigung von Anforderungen an Vertraulichkeit, Integrität und Verfügbarkeit.

Diese Richtlinie gilt für:

- Alle Informationswerte, unabhängig vom Format (digital, Papier, mündlich)
- Alle zugehörigen Assets (Systeme, Speichermedien, Anwendungen), die klassifizierte Informationen verarbeiten, speichern oder übertragen
- Alle Beschäftigten, Auftragnehmer und Dritten, die Informationen der Organisation oder ihr anvertraute Informationen handhaben

Das Klassifizierungsschema bildet die Grundlage für Zugriffskontrollentscheidungen, Handhabungsregeln und Schutzmaßnahmen bei [IHR_ORGANISATIONSNAME].

## 3. Klassifizierung von Informationen (A 5.12)

Die Eigentümer von Informationen (Asset-Eigentümer) sind für deren Klassifizierung verantwortlich. Klassifizierungen und zugehörige Schutzmaßnahmen berücksichtigen geschäftliche Anforderungen an die gemeinsame Nutzung oder Beschränkung von Informationen, den Schutz der Integrität und die Gewährleistung der Verfügbarkeit sowie rechtliche Anforderungen. Assets, die keine Informationen sind, werden in Übereinstimmung mit der Klassifizierung der Informationen klassifiziert, die von ihnen gespeichert, verarbeitet, anderweitig gehandhabt oder geschützt werden.

Informationen können nach einer bestimmten Zeit ihre Sensibilität oder Kritikalität verlieren. Überklassifizierung führt zu unnötigen Kontrollen und zusätzlichem Aufwand; Unterklassifizierung führt zu unzureichendem Schutz. Klassifizierungsstufen werden regelmäßig überprüft und angepasst, wenn sich geschäftliche Anforderungen oder die Bedrohungslandschaft ändern.

### 3.1 Klassifizierungskonventionen & Überprüfung

[IHR_ORGANISATIONSNAME] klassifiziert Informationen entlang von drei Schutzdimensionen: **Vertraulichkeit**, **Integrität** und **Verfügbarkeit**. Jede Dimension verwendet eine definierte Menge von Stufen. Der Asset-Eigentümer weist bei Erstellung des Informationswerts pro Dimension eine Klassifizierungsstufe zu. Die Klassifizierung wird überprüft:

- Mindestens jährlich im Rahmen der Überprüfung des Asset-Inventars.
- Immer dann, wenn sich Inhalt, Kontext oder Nutzung der Informationen wesentlich ändern.
- Wenn die Informationen mit neuen Parteien geteilt oder in neuen Geschäftsprozessen verwendet werden.
- Wenn die Informationen das Ende einer definierten Aufbewahrungsfrist erreichen oder veröffentlicht werden.

### 3.2 Vertraulichkeitsstufen

[IHR_ORGANISATIONSNAME] verwendet die folgenden vier Vertraulichkeitsstufen. Jede Stufe spiegelt die Auswirkungen wider, die eine unbefugte Offenlegung für die Organisation hätte:

#### ÖFFENTLICH

*Informationen für uneingeschränkte Verbreitung. Die Offenlegung verursacht keinen Schaden für die Organisation.*

- **Zugriff:** Keine Zugriffsbeschränkungen. Verfügbar für die allgemeine Öffentlichkeit.
- **Speicherung:** Keine besonderen Speicheranforderungen. Standard-Speicherung der Organisation ist ausreichend.
- **Übertragung:** Keine Beschränkungen der Übertragungsmethode. Kann frei geteilt werden.
- **Entsorgung:** Standardentsorgungsverfahren (Papierrecycling, normale Löschung digitaler Dateien).
- **Kennzeichnung:** Die Kennzeichnung als ÖFFENTLICH ist optional. Nicht gekennzeichnete Informationen gelten nicht automatisch als öffentlich.

#### INTERN

*Informationen nur zur internen Nutzung. Unbefugte Offenlegung könnte geringfügige Unannehmlichkeiten, aber keinen erheblichen Schaden verursachen.*

- **Zugriff:** Zugriff auf Beschäftigte und autorisiertes externes Personal beschränkt. Need-to-know-Prinzip empfohlen, aber nicht zwingend.
- **Speicherung:** Speicherung auf organisatorischen Systemen mit Standard-Zugriffskontrollen. Physische Dokumente in Standard-Büroflächen (keine publikumsnahen Bereiche).
- **Übertragung:** Nutzung von organisatorischer E-Mail oder genehmigten Dateifreigabeplattformen. Verschlüsselung für interne Übertragung empfohlen, aber nicht zwingend.
- **Entsorgung:** Papier: Entsorgung über Bürocontainer oder Behälter für vertrauliche Abfälle. Digital: Standard-Löschung aus organisatorischen Systemen.
- **Kennzeichnung:** Kennzeichnung von Dokumenten, E-Mails und Dateifreigaben als INTERN. Kopfzeilen-/Fußzeilen-Markierungen auf Dokumenten nutzen.

#### VERTRAULICH

*Sensible Geschäftsinformationen. Unbefugte Offenlegung könnte erheblichen Schaden für die Organisation, ihre Partner oder Kunden verursachen.*

- **Zugriff:** Zugriff auf speziell autorisierte Personen strikt nach dem Need-to-know-Prinzip beschränkt. Zugriff wird vom Informationseigentümer genehmigt.
- **Speicherung:** Digital: Speicherung auf zugriffskontrollierten Systemen mit verschlüsseltem Speicher. Physisch: Aufbewahrung in verschlossenen Schränken oder gesicherten Büroflächen.
- **Übertragung:** Verschlüsselte E-Mail oder sicherer Dateitransfer. Keine Nutzung öffentlicher Cloud-Dienste, außer diese sind genehmigt und verschlüsselt. Physischer Transfer per versiegeltem, blickdichtem Umschlag.
- **Entsorgung:** Papier: Kreuzschnittvernichtung (DIN 66399 Sicherheitsstufe P-4 oder höher). Digital: Sichere Löschung mit genehmigten Werkzeugen; verschlüsselte Medien können nach Schlüsselvernichtung entsorgt werden.
- **Kennzeichnung:** Alle Dokumente, Dateien und Behälter werden eindeutig als VERTRAULICH gekennzeichnet. E-Mail-Betreffzeilen enthalten die Klassifizierungskennzeichnung.

#### STRENG VERTRAULICH

*Hochsensible Informationen (z. B. Geschäftsgeheimnisse, besondere Kategorien personenbezogener Daten). Unbefugte Offenlegung könnte schweren oder existenzbedrohenden Schaden verursachen.*

- **Zugriff:** Zugriff strikt auf namentlich benannte Personen mit ausdrücklicher Genehmigung des Informationseigentümers und der Geschäftsleitung beschränkt. Zugriffslisten werden geführt und regelmäßig überprüft.
- **Speicherung:** Digital: Speicherung ausschließlich auf speziell dafür vorgesehenen, verschlüsselten Systemen mit Multi-Faktor-Zugangskontrolle. Physisch: Aufbewahrung in Tresoren oder Hochsicherheitsräumen mit Zugriffsprotokollierung.
- **Übertragung:** Ende-zu-Ende-Verschlüsselung ist zwingend. Nutzung ausschließlich genehmigter sicherer Kanäle. Keine Übertragung per Standard-E-Mail. Physischer Transfer nur durch vertrauenswürdige Kuriere mit Chain-of-Custody-Dokumentation.
- **Entsorgung:** Papier: Kreuzschnittvernichtung (DIN 66399 Sicherheitsstufe P-5 oder höher) mit bezeugter Vernichtung. Digital: Kryptographische Löschung oder physische Vernichtung der Datenträger, dokumentiert und bezeugt.
- **Kennzeichnung:** Alle Dokumente, Dateien und Behälter werden deutlich als STRENG VERTRAULICH gekennzeichnet. Jede Seite trägt die Klassifizierungskennzeichnung. E-Mail-Betreffzeilen enthalten die Klassifizierungskennzeichnung.

### 3.3 Integritätsstufen

[IHR_ORGANISATIONSNAME] verwendet die folgenden Integritätsstufen. Jede Stufe spiegelt die Auswirkungen wider, die eine unbefugte Änderung oder ein Verlust der Korrektheit für die Organisation hätte:

- **Normal:** Kleinere Ungenauigkeiten sind tolerierbar und können ohne nennenswerten Aufwand korrigiert werden.
- **Hoch:** Ungenauigkeiten könnten nennenswerten Schaden verursachen. Die Korrektheit ist überprüfbar.
- **Sehr hoch:** Informationen sind jederzeit korrekt. Jede Veränderung könnte schweren Schaden verursachen.

### 3.4 Verfügbarkeitsstufen

[IHR_ORGANISATIONSNAME] verwendet die folgenden Verfügbarkeitsstufen. Jede Stufe spiegelt die Auswirkungen wider, die ein Verlust der Verfügbarkeit für die Organisation hätte:

- **Normal:** Ausfallzeiten von bis zu mehreren Tagen sind tolerierbar.
- **Hoch:** Die maximal tolerierbare Ausfallzeit beträgt wenige Stunden. Längere Ausfälle verursachen erhebliche geschäftliche Auswirkungen.
- **Sehr hoch:** Informationen sind jederzeit verfügbar. Jeder Ausfall verursacht schweren Schaden.

### 3.5 Abstimmung mit der Zugriffskontrolle

Das Klassifizierungsschema ist mit der Zugriffskontroll-Richtlinie von [IHR_ORGANISATIONSNAME] abgestimmt. Zugriffsrechte werden auf Basis der Klassifizierungsstufe der Informationen vergeben: Je höher die Klassifizierung, desto restriktiver die Zugriffskontrollen. Rollenbasierte Zugriffskontrolle (RBAC) und das Prinzip der minimalen Rechte werden angewendet. Zugriffsentscheidungen beziehen sich auf die vom Asset-Eigentümer zugewiesene Klassifizierungsstufe.

### 3.6 Organisationsweite Konsistenz

Dieses Klassifizierungsschema ist für alle Abteilungen, Geschäftsbereiche und Standorte von [IHR_ORGANISATIONSNAME] verbindlich. Die folgenden Maßnahmen gewährleisten eine einheitliche Anwendung:

- Diese Richtlinie wird allen Beschäftigten während des Onboardings und über regelmäßige Sensibilisierungsschulungen kommuniziert.
- Klassifizierungsverfahren werden in Dokumentenmanagement-, Projektmanagement- und IT-Service-Management-Prozesse integriert.
- Vorlagen für gängige Dokumenttypen enthalten vorformatierte Klassifizierungskennzeichnungen.
- Die/der Informationssicherheitsbeauftragte führt regelmäßige Stichproben zur Überprüfung der korrekten Klassifizierung durch.

### 3.7 Organisationsübergreifende Klassifizierung

Das von [IHR_ORGANISATIONSNAME] verwendete Klassifizierungsschema kann von den Schemata von Partnerorganisationen abweichen, auch wenn die Stufenbezeichnungen ähnlich erscheinen. Wenn Vereinbarungen mit anderen Organisationen den Informationsaustausch umfassen, spezifizieren die Vereinbarungen Verfahren zur Identifizierung der Klassifizierung ausgetauschter Informationen und zur Interpretation der Klassifizierungsstufen der anderen Organisation. Die Entsprechung zwischen verschiedenen Schemata wird durch den Vergleich der zugehörigen Handhabungs- und Schutzmethoden bestimmt.

## 4. Kennzeichnung von Informationen (A 5.13)

Die Kennzeichnungsverfahren decken Informationen und andere zugehörige Assets in allen Formaten ab. Die Kennzeichnung spiegelt das oben etablierte Klassifizierungsschema wider. Kennzeichnungen sind leicht erkennbar und werden einheitlich angewendet, sodass alle Beschäftigten die Klassifizierung jeder Information, auf die sie stoßen, sofort erkennen können.

### 4.1 Kennzeichnungsmethoden

Asset-Eigentümer stellen sicher, dass Informationen je nach Format und Medium nach den folgenden Methoden gekennzeichnet werden:

- **Papierdokumente:** Klassifizierungskennzeichnung in der Kopf- oder Fußzeile jeder Seite. Deckblätter und erste Seiten tragen eine prominente Kennzeichnung. Ordner und Mappen sind auf Rücken und Vorderseite gekennzeichnet.
- **Elektronische Dokumente:** Klassifizierungskennzeichnung in Kopf-/Fußzeile des Dokuments (für Office-Dokumente), im Dateinamen (mit Präfix wie *VERTRAULICH_Bericht_2025.pdf*) und/oder über Dokumenten-Metadaten-Eigenschaften.
- **E-Mail:** Klassifizierungskennzeichnung am Anfang der Betreffzeile (z. B. [VERTRAULICH]). Sensible Anhänge tragen ihre eigene Klassifizierungskennzeichnung.
- **Speichermedien:** Physische Medien (USB-Sticks, externe Festplatten, Sicherungsbänder) werden mit der höchsten Klassifizierungsstufe der enthaltenen Informationen gekennzeichnet.
- **Anwendungen und Datenbanken:** Klassifizierungs-Metadaten werden auf Datenfeld-, Datensatz- oder Container-Ebene angewendet, wo dies technisch machbar ist. Systeme, die keine Klassifizierung pro Datensatz unterstützen, schützen alle enthaltenen Informationen auf der höchsten vorkommenden Klassifizierungsstufe.
- **Mündliche Kommunikation:** Vor mündlicher Besprechung klassifizierter Informationen (in Meetings, Telefonaten, Videokonferenzen) nennt die sprechende Person die Klassifizierungsstufe und stellt sicher, dass nur autorisierte Personen anwesend sind.

### 4.2 Digitale Metadaten

[IHR_ORGANISATIONSNAME] nutzt Metadaten zur Identifikation, Verwaltung und Steuerung von Informationen, insbesondere hinsichtlich der Vertraulichkeit. Metadaten ermöglichen effizientes Suchen und erlauben Systemen, auf Basis von Klassifizierungskennzeichnungen zu interagieren und Entscheidungen zu treffen. Die Kennzeichnungsverfahren beschreiben, wie Metadaten an Informationen angebracht werden, welche Kennzeichnungen zu verwenden sind und wie Daten gehandhabt werden, im Einklang mit dem Informationsmodell und der IKT-Architektur der Organisation. Relevante zusätzliche Metadaten (z. B. welcher Prozess die Information wann erstellt hat) werden von Systemen bei der Verarbeitung hinzugefügt.

### 4.3 Ausnahmen von der Kennzeichnung

[IHR_ORGANISATIONSNAME] definiert die folgenden Fälle, in denen eine Kennzeichnung entfallen oder vereinfacht werden kann:

- **ÖFFENTLICHE Informationen:** Die Kennzeichnung ist für Informationen der niedrigsten Vertraulichkeitsstufe optional, da das Fehlen einer Kennzeichnung keine höhere Klassifizierung impliziert. Allerdings werden nicht gekennzeichnete Informationen nicht ohne Prüfung als öffentlich angenommen.
- **Routinemäßige interne Kommunikation:** Routinemäßige interne E-Mails und Chat-Nachrichten, die keine Informationen oberhalb der Stufe INTERN enthalten, erfordern keine expliziten Klassifizierungskennzeichnungen, es sei denn, sie werden extern weitergeleitet.
- **Automatisierte Datenflüsse:** Wenn Informationsflüsse zwischen Systemen vollständig automatisiert und zugriffskontrolliert sind, kann die einzelne Kennzeichnung durch eine systemweite Klassifizierung ersetzt werden, sofern das System alle enthaltenen Informationen auf der angemessenen Stufe schützt.

Auch wenn die Kennzeichnung entfällt, bleibt der Asset-Eigentümer dafür verantwortlich, dass die Information entsprechend ihrer Klassifizierungsstufe gehandhabt wird.

### 4.4 Umgang mit nicht kennzeichenbaren Informationen

In bestimmten Situationen ist eine Kennzeichnung technisch oder praktisch nicht machbar (z. B. mündliche Informationen, Live-Demonstrationen, Altsysteme ohne Metadaten-Unterstützung). In diesen Fällen:

- Informationen, die nicht gekennzeichnet werden können, werden als **VERTRAULICH** behandelt, bis der Asset-Eigentümer eine Klassifizierung zuweist und kommuniziert.
- Der Asset-Eigentümer dokumentiert die Klassifizierung im Asset-Inventar und stellt sicher, dass alle mit der Information umgehenden Personen mündlich oder schriftlich über die Klassifizierung informiert werden.
- Wenn nicht gekennzeichnete Informationen aus einem System exportiert werden (z. B. durch Ausdruck, Download oder Weiterleitung), bringt die exportierende Person die entsprechende Kennzeichnung am Exportpunkt an.

### 4.5 Sensibilisierung & Schulung

Alle Beschäftigten werden für Kennzeichnungsverfahren sensibilisiert und erhalten die notwendige Schulung, um sicherzustellen, dass Informationen korrekt gekennzeichnet und gehandhabt werden. Beschäftigte werden auch darauf hingewiesen, dass die Kennzeichnung mitunter unbeabsichtigte negative Auswirkungen haben kann, da klassifizierte Assets für böswillige Akteure leichter identifizierbar sein könnten. Dieses Risiko wird durch ergänzende Zugriffskontrollen und das Prinzip der minimalen Rechte gemindert, nicht durch Verschleierung.

Ausgaben aus Systemen, die als sensibel oder kritisch klassifizierte Informationen enthalten, tragen eine angemessene Klassifizierungskennzeichnung.

## 5. Rollen & Verantwortlichkeiten

- **Geschäftsleitung:** Genehmigt diese Richtlinie, stellt angemessene Ressourcen für die Umsetzung bereit und kommuniziert die organisatorische Erwartung an den korrekten Umgang mit Informationen.
- **Informationssicherheitsbeauftragte/r (ISB):** Pflegt diese Richtlinie, definiert und überprüft Klassifizierungsstufen, führt Stichproben zur Einhaltung von Klassifizierung und Kennzeichnung durch und berät Asset-Eigentümer.
- **Asset-Eigentümer (Informationseigentümer):** Klassifizieren die ihnen gehörenden Informationen, weisen Klassifizierungsstufen zu und überprüfen sie, genehmigen Zugriffsanträge auf ihre Informationen und stellen sicher, dass Kennzeichnungs- und Handhabungsregeln befolgt werden.
- **IT-Abteilung:** Implementiert technische Maßnahmen zur Kennzeichnung (Metadaten, DLP, Vorlagen), setzt an Klassifizierungsstufen ausgerichtete Zugriffskontrollen durch und stellt sicher, dass Systeme Klassifizierungs-Metadaten unterstützen können.
- **Alle Beschäftigten:** Wenden Klassifizierungskennzeichnungen korrekt an, handhaben Informationen entsprechend ihrer Klassifizierung, melden vermutete Fehlklassifizierungen und nehmen an Sensibilisierungsschulungen zu Klassifizierung und Kennzeichnung teil.

## 6. Überprüfung & Pflege

Diese Richtlinie wird überprüft:

- Mindestens jährlich im Rahmen des ISMS-Managementbewertungszyklus.
- Wenn sich geschäftliche Anforderungen an Informationsaustausch oder -schutz wesentlich ändern.
- Nach wesentlichen Sicherheitsvorfällen im Zusammenhang mit Fehlklassifizierungen oder Informationsabfluss.
- Bei Änderungen am rechtlichen oder regulatorischen Rahmen, die Klassifizierungsanforderungen betreffen (z. B. neue Datenschutzverordnungen, Änderungen des Geschäftsgeheimnisgesetzes).
- Wenn die Organisation neue Informationsaustauschvereinbarungen mit externen Parteien eingeht, die eine Abstimmung der Klassifizierungsschemata erfordern.
