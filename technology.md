# Technik
## Technische Details
In diesem Abschnitt möchten wir technische Details veröffentlichen, die im Kontext des elektronischen Personalausweises interessant sind. Genauer gesagt geht es um die Varianten des Personalausweises, eID-Clients für den elektronischen Personalausweis sowie Open Source Projekte im Kontext des Personalausweises. 

## Varianten des Personalausweises
Seit der Einführung des elektronischen Personalausweises im November 2010 wurden immer wieder Modifikationen vorgenommen. So wurde bspw. erst im Q2/2012 die Datengruppe 13 verwendet, die den möglichen Geburtsnamen des Inhabers bzw. der Inhaberin enthält oder im Q1/2013 wurde erstmals die DG10 verwendet (Staatsangehörigkeit). Diese Änderungen werden in Annex D der BSI [TR-03127](https://www.bsi.bund.de/DE/Themen/Unternehmen-und-Organisationen/Standards-und-Zertifizierung/Technische-Richtlinien/TR-nach-Thema-sortiert/tr03127/TR-03127_node.html) vollständig aufgeführt. Zusätzlich stehen diese Änderungen als DefectList gemäß BSI [TR-03129](https://www.bsi.bund.de/DE/Themen/Unternehmen-und-Organisationen/Standards-und-Zertifizierung/Technische-Richtlinien/TR-nach-Thema-sortiert/tr03129/TR-03129_node.html) zur Verfügung. Die DefectList beinhaltet Produktionsfehler und -änderungen, die bei einer großen Menge von ausgegebenen Dokumenten wie dem Personalausweis unvermeidlich sind. Ein Terminal kann ein oder mehrere DefectLists über das Kommando GetDefectList anfordern. Anwendungsentwicklern im eID-Kontext wird auf dieser Basis eine Möglichkeit gegeben, die im Feld verfügbaren Varianten des Personalausweises korrekt zu behandeln und diese Varianten in ihre Software zu integrieren. 

## eID-Clients für den elektronischen Personalausweis
Die folgenden eID-Clients stehen zur Verfügung, um auf unterschiedlichen Plattformen auf den Personalausweis zuzugreifen.

| Merkmal | AusweisApp | Authada-App | Open eID Client |
| :------: | -------- | -------- |-------- |
| **Hersteller** | Bund/Governikus | Authada | ecsec |
| **Website** | [www.ausweisapp.bund.de](https://www.ausweisapp.bund.de/home/) | App Store | [www.openecard.org](https://www.openecard.org/startseite/) |
| **Source Code** |	[github.com/Governikus/AusweisApp2](https://github.com/Governikus/AusweisApp2) | nicht verfügbar | [github.com/ecsec/open-ecard](https://github.com/ecsec/open-ecard) |
| **Unterstützte Plattformen** | Windows, macOS, (Linux), Android, iOS | Android, iOS | Windows, Android, iOS |
| **BSI Zertifizierung** | ja | ja | ja |
| **SDK verfügbar** | ja | ja | nein |

## Open Source Projekte im Kontext des Personalausweises
Im Kontext des Personalausweises gibt es unterschiedliche Projekte. wir möchten an dieser Stelle den Open Source Projekten eine Möglichkeit bieten, sich vorzustellen. Diese Liste wird mit der Zeit erweitert. Sollten Sie Ihr Projekt in dieser Liste vermissen, kontaktieren Sie uns einfach.

* androsmex: Eine Implementierung des PACE-Protokolls für Android-Geräte mit NFC-Schnittstelle. Siehe: [code.google.com/p/androsmex ](https://github.com/tsenger/androsmex)
* eIDClientCore: Eine gemeinsame Initiative der Bundesdruckerei und der Humboldt-Universität Berlin um eine clientseitige eID-Basis-Software zum Bereitstellen der eID-Funktionalität zu entwickeln. Siehe http://sar.informatik.hu-berlin.de/BeID-lab/eIDClientCore/
* openpace: Krypto-Bibliothek mit allen EAC2-Protokollen. Siehe [https://github.com/frankmorgner/openpace](https://github.com/frankmorgner/openpace)


