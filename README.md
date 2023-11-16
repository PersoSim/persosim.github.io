# Der Open Source Simulator für den elektronischen Personalausweis
Willkommen auf dem Internet-Portal der Open Source Community zu PersoSim, dem Simulator für den neuen elektronischen Personalausweis (nPA oder ePA). PersoSim dient dazu, die Softwareentwicklung für die Nutzung des neuen Personalausweises voranzutreiben. Dazu möchte das Projekt Entwickler, Unternehmen und Behörden in dieser Community zusammenbringen. PersoSim ist ein Mosaikstein im Testkonzept des BSI für die eID-Infrastruktur. Die [Testinfrastruktur](https://www.bsi.bund.de/DE/Themen/Oeffentliche-Verwaltung/Elektronische-Identitaeten/Online-Ausweisfunktion/Testinfrastruktur/eID-Anwendung/eID-Anwendung_node.html) beschreibt die einzelnen Komponenten innerhalb der eID-Infrastruktur wie bspw. [PersoSim](https://www.bsi.bund.de/DE/Themen/Oeffentliche-Verwaltung/Elektronische-Identitaeten/Online-Ausweisfunktion/Testinfrastruktur/PersoSim/PersoSim_node.html) und informiert über die Testmöglichkeiten sowie die dazugehörigen Testwerkzeuge. Interessierte Anwender und Entwickler sind natürlich herzlichst eingeladen, sich an der PersoSim-Community auf unterschiedliche Weise einzubringen.

# Aktuelles
## Weiterentwicklung von PersoSim gestartet
Aktuell sammeln wir neue Anforderungen für die Weiterentwicklung von PersoSim. Dazu sprechen wir mit unterschiedlichen Stakeholdern, sammeln neue Anforderungen, bewerten diese und sortieren sie ein um sie dann zu implementieren. Es wird also zukünftig wieder neue Releases geben. Neuigkeiten werden wir auch über unseren neuen Mastodon-Account bereitstellen: <a rel="me" href="https://mastodon.social/@persosim">mastodon.social/@persosim</a>

## PersoSim 0.18.3 veröffentlicht
Der Simulator für den deutschen Personalausweis steht nun in Version 0.18.3 zur Verfügung. Die Änderungen erstrecken sich auf die Smart-eID, so dass der Simulator nun neue Profile für die Smart-eID beinhaltet, die  zusätzlich mit dem Editor bearbeitet werden können.

## PersoSim jetzt auch auf der BSI-Website
Das BSI hat auf seiner Website nun eine eigene [Seite](https://www.bsi.bund.de/PersoSim) für PersoSim angelegt. Dort gibt es alle Informationen zum Simulator und den dazugehörigen Tools in kompakter Form. Als Teil der eID-Infrastruktur ist PersoSim ein wichtiger Mosaikstein, um die Interoperabilität der Komponenten im deutschen eID-System sicherzustellen. Die Testinfrastruktur setzt sich zu diesem Zweck aus den einzelnen Komponenten der eID-Infrastruktur zusammen, um den Herstellern der einzelnen Komponenten Testmöglichkeiten sowie Testwerkzeuge an die Hand zu geben. Für darüber hinausgehende Tests – wie bspw. die Integration des Simulators in die bestehende Continuous Integration – stehen die Entwickler und Berater der secunet gerne zur Verfügung.

# Technik
## Technische Details
In diesem Abschnitt möchten wir technische Details veröffentlichen, die im Kontext des elektronischen Personalausweises interessant sind. Genauer gesagt geht es um die Varianten des Personalausweises, eID-Clients für den elektronischen Personalausweis sowie Open Source Projekte im Kontext des Personalausweises. 

## Varianten des Personalausweises
In diesem Abschnitt werden gemäß BSI TR-03127 Varianten von produzierten Personalausweisen und Aufenthaltstiteln gegenüber den aktuellen Versionen der Spezifikationen aufgeführt. Diese Varianten ergeben sich beispielsweise durch Änderungen und Aktualisierungen in den Spezifikationen. Die Ausweise werden bei diesem Verfahren anhand der Seriennummern der genutzten DocumentSigner identifiziert. Die Informationen, die in der folgenden Tabelle aufgeführt sind, stehen zusätzlich elektronisch als DefectList gemäß BSI TR-03129 zur Verfügung. Die DefectList beinhaltet Produktionsfehler und -änderungen, die bei einer großen Menge von ausgegebenen Dokumenten wie dem Personalausweis unvermeidlich sind. Ein Terminal kann ein oder mehrere DefectLists über das Kommando GetDefectList anfordern. 

| Ausgabezeitraum | DS Serial Number | Abweichung | ObjectIdentifier in DefectList |
| -------- | -------- | -------- | -------- |
| Bis Q3/2011 | SN ≤ 106 | Die Ausweise enthalten in EF.CardAccess und EF.ChipSecurity keine Struktur PrivilegedTerminalInfo. Der für nicht-privilegierte Terminals verfügbare Schlüssel für die Chipauthentisierung ist der Schlüssel, der in der ersten ChipAuthenticationInfo adressiert wird. | id­-EAC2PrivilegedTerminalInfoMissing |
| Bis Q3/2011 |SN ≤ 106 | Die Ausweise enthalten in EF.ChipSecurity kein eIDSecurityInfo. |id­-eIDSecurityInfoMissing |
| Bis Q4/2011 | SN ≤ 109 | Die Ausweise erlauben keine mehrfache Authentisierung während einer Kartenaktivierung, d.h. zur Durchführung einer zweiten Authentisierung muss die Karte durch ein Aus- und Anschalten des Lesefeldes zurückgesetzt werden. | id­-PowerDownReq |
| Bis Q2/2012 | SN ≤ 112 | Die Ausweise enthalten keine bzw. eine leere Datengruppe „Geburtsname“ (DG13). | id­-eIDDGMissing mit Parameter DG13 |
| Bis Q1/2013 | SN ≤ 122 | Die Ausweise enthalten keine Datengruppe „Staatsangehörigkeit“ (DG10). | id­-eIDDGMissing mit Parameter DG10 |

Diese Liste mit Änderungen werden wir bei Bedarf weiter fortsetzen. Anwendungsentwicklern im eID-Kontext wird auf dieser Basis eine Möglichkeit gegeben, die im Feld verfügbaren Varianten des Personalausweises korrekt zu behandeln und diese Varianten in ihre Software zu integrieren. 

## eID-Clients für den elektronischen Personalausweis

| Merkmal | AusweisApp | Authada-App | Open eID Client |
| -------- | -------- | -------- |-------- |
| Hersteller | Bund/Governikus | Authada | ecsec |
| Unterstützte Plattformen | Windows, MacOS, (Linux), Android, iOS | Android, iOS | Windows, Android, iOS |
| BSI Zertifizierung | ja | ja | ja |
| SDK verfügbar | ja | ja | nein |

## Open Source Projekte im Kontext des Personalausweises
Im Kontext des Personalausweises gibt es unterschiedliche Projekte. wir möchten an dieser Stellen den Open Source Projekten eine Möglichkeit bieten, sich vorzustellen. Diese Liste wird mit der Zeit erweitert. Sollten Sie Ihr Projekt in dieser Liste vermissen, kontaktieren Sie uns einfach.

* androsmex: Eine Implementierung des PACE-Protokolls für Android-Geräte mit NFC-Schnittstelle. Siehe: [code.google.com/p/androsmex ](https://github.com/tsenger/androsmex)
* eIDClientCore: Eine gemeinsame Initiative der Bundesdruckerei und der Humboldt-Universität Berlin um eine clientseitige eID-Basis-Software zum Bereitstellen der eID-Funktionalität zu entwickeln. Siehe http://sar.informatik.hu-berlin.de/BeID-lab/eIDClientCore/
* openpace: Krypto-Bibliothek mit allen EAC2-Protokollen. Siehe [https://github.com/frankmorgner/openpace](https://github.com/frankmorgner/openpace)

# Simulator
Im Rahmen der Entwicklung des Testwerkzeugs [GlobalTester](https://globaltester.secunet.com/de/) existiert bereits ein Simulator für elektronische Reisepässe (ePassport) bzw. den neuen elektronischen Personalausweis (nPA). Dieser Simulator wird bereits als kommerzielle Version für Konformitätstests gemäß der BSI TR-03105 erfolgreich eingesetzt. Die kommerzielle Version nutzt dabei ebenfalls nur kommerziell verfügbare Hardware, die die Kommunikation zwischen dem Kartenleser und dem Software-Simulator übernimmt. Die Hardware (Comprion CLT one) handelt dabei die Parameter für die Kommunikation aus und stellt dem Simulator die APDU zur Verfügung. Der Simulator wiederum berechnet die Antworten und sendet diese über die Hardware zurück an den Kartenleser. Die Abbildung zeigt diese Art der Kommunikation in Anlehnung an das ISO/OSI-Schichtenmodell.

![Simulator_ISO_Layer](https://github.com/PersoSim/persosim.github.io/blob/main/Simulator_ISO_Layer.png)

Da für ein Open Source Projekt wie PersoSim die Hardware aufgrund der hohen Kosten nur schwer zur Verfügung steht, stellen wir hier eine Alternative bereit. Statt physikalischer Hardware nutzen wir hier einen virtuellen Kartenleser, der sich wie ein ganz normaler Kartenleser in bestehende Anwendungen integrieren lässt und der die Kommunikation mit der Simulator übernimmt. In obiger Abbildung ist diese Art der Kommunikation ebenfalls abgebildet.

Die folgende Grafik ordnet den Simulator aus dem Projekt PersoSim in den Kontext des deustschen Personalausweis und der eID-Clients sowie der eID-Server ein.

![PersoSim_Grafik_DE](https://github.com/PersoSim/persosim.github.io/blob/main/PersoSim_Grafik_DE.jpg)
 
## Zertifizierung PersoSim nach BSI TR-03105
PersoSim ist wie andere physische Personalausweise auch nach TR-03105 Teil 3.3 zertifiziert und entspricht somit den Vorgaben des BSI.

![BSI-K-TR-0198-2015](https://github.com/PersoSim/persosim.github.io/blob/main/BSI-K-TR-0198-2015.jpg)

