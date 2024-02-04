You can find an english description of PersoSim [here](https://persosim.github.io/readme_eng.html).
# Der Open Source Simulator für den elektronischen Personalausweis
Willkommen auf dem Internet-Portal der Open Source Community zu PersoSim, dem Simulator für den neuen elektronischen Personalausweis (nPA oder ePA). PersoSim dient dazu, die Softwareentwicklung für die Nutzung des neuen Personalausweises voranzutreiben. Dazu möchte das Projekt Entwickler, Unternehmen und Behörden in dieser Community zusammenbringen. PersoSim ist ein Mosaikstein im Testkonzept des BSI für die eID-Infrastruktur. Die [Testinfrastruktur](https://www.bsi.bund.de/DE/Themen/Oeffentliche-Verwaltung/Elektronische-Identitaeten/Online-Ausweisfunktion/Testinfrastruktur/eID-Anwendung/eID-Anwendung_node.html) beschreibt die einzelnen Komponenten innerhalb der eID-Infrastruktur wie bspw. [PersoSim](https://www.bsi.bund.de/DE/Themen/Oeffentliche-Verwaltung/Elektronische-Identitaeten/Online-Ausweisfunktion/Testinfrastruktur/PersoSim/PersoSim_node.html) und informiert über die Testmöglichkeiten sowie die dazugehörigen Testwerkzeuge. Interessierte Anwender und Entwickler sind natürlich herzlichst eingeladen, sich an der PersoSim-Community auf unterschiedliche Weise einzubringen. Die github Repositories mit dem Quellcode und weiteren Informationen für Entwickler liegen hier: [https://github.com/PersoSim](https://github.com/PersoSim).

# Aktuelles
## Weiterentwicklung von PersoSim gestartet
> Aktuell sammeln wir neue Anforderungen für die Weiterentwicklung von PersoSim. Dazu sprechen wir mit unterschiedlichen Stakeholdern, sammeln neue Anforderungen, bewerten diese und sortieren sie ein um sie dann zu implementieren. Es wird also zukünftig wieder neue Releases geben. Neuigkeiten werden wir auch über unseren neuen Mastodon-Account bereitstellen: <a rel="me" href="https://mastodon.social/@persosim">mastodon.social/@persosim</a>

## PersoSim 0.18.3 veröffentlicht
> Der Simulator für den deutschen Personalausweis steht nun in Version 0.18.3 zur Verfügung. Die Änderungen erstrecken sich auf die Smart-eID, so dass der Simulator nun neue Profile für die Smart-eID beinhaltet, die  zusätzlich mit dem Editor bearbeitet werden können.

## PersoSim jetzt auch auf der BSI-Website
> Das BSI hat auf seiner Website nun eine eigene [Seite](https://www.bsi.bund.de/PersoSim) für PersoSim angelegt. Dort gibt es alle Informationen zum Simulator und den dazugehörigen Tools in kompakter Form. Als Teil der eID-Infrastruktur ist PersoSim ein wichtiger Mosaikstein, um die Interoperabilität der Komponenten im deutschen eID-System sicherzustellen. Die Testinfrastruktur setzt sich zu diesem Zweck aus den einzelnen Komponenten der eID-Infrastruktur zusammen, um den Herstellern der einzelnen Komponenten Testmöglichkeiten sowie Testwerkzeuge an die Hand zu geben. Für darüberhinausgehende Tests – wie bspw. die Integration des Simulators in die bestehende Continuous Integration – stehen die Entwickler und Berater der secunet gerne zur Verfügung.

Ältere News befinden sich im [Archiv](https://persosim.github.io/news_archive.html).

# Downloads und Installation
Dieses Kapitel enthält die Dateien, die für den Betrieb des Simulators nötig sind, sowie eine kurze Anleitung zur Installation. Wir unterstützen neben Windows auch Linux und macOS für die stationäre Variante von PersoSim. Für ältere Smartphones mit NFC liegt ein Android-APK bereit.

## Systemvoraussetzungen
Java muss mindestens in Version 1.8 oder neuer installiert sein. Wir empfehlen entweder das Installationspaket von [Adoptium](https://adoptium.net/de/), das alle notwendigen Einstellungen automatisch vornimmt, oder das [OpenJDK](https://jdk.java.net/) bei dem die Einstellungen manuell durchgeführt werden können.

## Vorgehensweise zur Installation
Bitte nutzen Sie die folgenden Schritte zum Installieren und Starten des Simulators:
* Installation des Treibers für den **virtuellen Kartenleser**: Wählen Sie bitte je nach System Treiber für Linux bzw. macOS oder Windows und folgen Sie bitte den Installationsanweisungen. Der Windows-Treiber enthält die notwendigen Dateien sowohl für Windows 7, 8 und 10 jeweils als Architektur mit 32 Bit oder 64 Bit.
  * Den Treiber für Linux und macOS müssen Sie derzeit selbst kompilieren; die Sourcen finden Sie hier: [PersoSim_Driver_PCSCLite_20180209.tgz](https://persosim.github.io/software/PersoSim_Driver_PCSCLite_20180209.tgz).
  * Das Installationspaket für Windows finden Sie hier: [PersoSim_Driver_win_20180209.zip](https://persosim.github.io/software/PersoSim_Driver_win_20180209.zip)
* **Simulator**: Starten Sie den Simulator (Eclipse RCP) für die jeweilige Plattform ([Windows](https://persosim.github.io/software/de.persosim.rcp.product-0.18.3-20220209-win32.win32.x86_64.zip), [macOS](https://persosim.github.io/software/de.persosim.rcp.product-0.18.3-20220209-macosx.cocoa.x86_64.zip), [Linux](https://persosim.github.io/software/de.persosim.rcp.product-0.18.3-20220209-linux.gtk.x86_64.zip)) im entpackten Verzeichnis. Wir unterstützen mittlerweile nur noch die Versionen mit 64 Bit.
* (optional) **Profil Editor**: Starten Sie den Editor (Eclipse RCP) für die jeweilige Plattform ([Windows](https://persosim.github.io/software/de.persosim.editor.rcp.product-0.18.3-20220209-win32.win32.x86_64.zip), [macOS](https://persosim.github.io/software/de.persosim.editor.rcp.product-0.18.3-20220209-macosx.cocoa.x86_64.zip), [Linux](https://persosim.github.io/software/de.persosim.editor.rcp.product-0.18.3-20220209-linux.gtk.x86_64.zip)) im entpackten Verzeichnis.
* (optional) **Android-Version**: Das APK für Android finden Sie hier: [PersoSim_0_17_2.apk](https://persosim.github.io/software/PersoSim_0_17_2.apk)

## Handbücher
Im [Anwenderhandbuch](https://persosim.github.io/manuals/Anwenderdokumentation_v1.4.pdf) beschreiben wir die Grundlagen zum Einsatz von PersoSim, angefangen von der Installation bis zum Einsatz.

Die Vorgehensweise zum Ändern von Trust Points beschreiben wir im Dokument [TA_Trust_Points_v1.3.pdf](https://persosim.github.io/manuals/TA_Trust_Points_v1.3.pdf).

## Profile
In PersoSim nutzen wir nicht nur typische Profile, wie sie im physischen Personalausweis verwendet werden, sondern auch Unionsbürgerkarten und Smart-eID. Informationen zu den Profilen der jeweiligen Varianten stellen wir in den folgenden Dokumenten bereit:
* Klassischer Personalausweis: [PersoSim_Personalisierungsdaten_nPA.pdf](https://persosim.github.io/manuals/PersoSim_Personalisierungsdaten_nPA.pdf)
* Unionsbürgerkarte: [PersoSim_Personalisierungsdaten_eID_UB.pdf](https://persosim.github.io/manuals/PersoSim_Personalisierungsdaten_eID_UB.pdf)
* Smart-eID: [Smart-eID-PersoSim_Personalisierungsdaten-2021.pdf](https://persosim.github.io/manuals/Smart-eID-PersoSim_Personalisierungsdaten-2021.pdf)

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

# Simulator
Im Rahmen der Entwicklung des Testwerkzeugs [GlobalTester](https://globaltester.secunet.com/de/) existiert bereits ein Simulator für elektronische Reisepässe (ePassport) bzw. den neuen elektronischen Personalausweis (nPA). Dieser Simulator wird bereits als kommerzielle Version für Konformitätstests gemäß der BSI TR-03105 erfolgreich eingesetzt. Die kommerzielle Version nutzt dabei ebenfalls nur kommerziell verfügbare Hardware, die die Kommunikation zwischen dem Kartenleser und dem Software-Simulator übernimmt. Die Hardware (Comprion CLT one) handelt dabei die Parameter für die Kommunikation aus und stellt dem Simulator die APDU zur Verfügung. Der Simulator wiederum berechnet die Antworten und sendet diese über die Hardware zurück an den Kartenleser. Die Abbildung zeigt diese Art der Kommunikation in Anlehnung an das ISO/OSI-Schichtenmodell.

![Simulator_ISO_Layer](https://persosim.github.io/Simulator_ISO_Layer.png)

Da für ein Open Source Projekt wie PersoSim die Hardware aufgrund der hohen Kosten nur schwer zur Verfügung steht, stellen wir hier eine Alternative bereit. Statt physikalischer Hardware nutzen wir hier einen virtuellen Kartenleser, der sich wie ein ganz normaler Kartenleser in bestehende Anwendungen integrieren lässt und der die Kommunikation mit dem Simulator übernimmt. In obiger Abbildung ist diese Art der Kommunikation ebenfalls abgebildet.

Die folgende Grafik ordnet den Simulator aus dem Projekt PersoSim in den Kontext des deutschen Personalausweis und der eID-Clients sowie der eID-Server ein.

![PersoSim_Grafik_DE](https://persosim.github.io/PersoSim_Grafik_DE.jpg)

# Frequently Asked Questions (FAQ)
## Community
### Wie kann ich mich als Entwickler an der PersoSim-Community beteiligen? 
Entwickler sind selbstverständlich dazu eingeladen die Open-Source-Software PersoSim weiterzuentwickeln bzw. in eigene Anwendungen zu integrieren.

### Wo findet man den Quellcode zum Simulator PersoSim? 
Wir unterscheiden zwischen der Anwender-Community hier auf dieser Website und der Entwickler-Community. Den Source Code zum Projekt PersoSim stellen wir deshalb auf github bereit. Das Repository findet man hier: [github.com/PersoSim](https://github.com/persosim). Dort gibt es auch technische Informationen, die den Einstieg in den Source Code des Simulators erleichtern soll. 

### Gibt es Trainings im Kontext PersoSim?
Als secunet bieten wir Ihnen über den Support hier in der Community auch Trainings zum Thema PersoSim an. Wir bieten Ihnen ebenfalls Unterstützung bei der Integration von PersoSim in Ihren Entwicklungs- bzw. Testprozess an (Continuous Integration). Kontaktieren Sie uns dazu bitte über info@secunet.com. 

### Gibt es Veröffentlichungen zum Thema PersoSim? 
Wir haben PersoSim auf unterschiedlichen Veranstaltungen wie dem BSI IT-Sicherheitskongress oder der Security Document World präsentiert. Darüber hinaus gibt es Veröffentlichungen zum Thema, z.B. in der Zeitschrift Datenschutz und Datensicherheit (DuD). Soweit verfügbar finden Sie die Präsentationen und Artikel im Kapitel [Publikationen](https://persosim.github.io/#publikationen).

## Einsatz des Simulators
### Welche Betriebssysteme werden unterstützt? 
Wir haben Treiber für den virtuellen Kartenleser auf den Betriebssystemen Windows, Linux und macOS bereitgestellt. Der Simulator läuft ebenfalls auf diesen Betriebssystemen. Zusätzlich haben wir eine App für Android implementiert, die ebenfalls einen Personalausweis simuliert und die NFC-Schnittstelle nutzt. 

### Wie lautet die PIN und die CAN für die verwendeten Profile? 
Die Profile nutzen alle als PIN die ‚123456‘ und als CAN die ‚500540‘. Als PUK ist die ‚9876543210‘ personalisiert. 

### Wird für den Simulator spezielle Hardware benötigt? 
Nein, es handelt sich um eine reine Softwarelösung für die keine weitere Hardware benötigt wird. Der Simulator beinhaltet einen virtuellen Kartenleser für die Betriebssysteme Windows, Linux und macOS, der als Verbindung zwischen Applikation und Simulator dient.

### Welche Zertifikate werden für die mitgelieferten Profile verwendet und wo findet man diese? 
Im entpackten PersoSim-Verzeichnis finden Sie im Verzeichnis \plugins\de.persosim.simulator_XXX\personalization\gtCertificates die zugrundeliegenden AT-, IS und ST-Zertifikate. Die Profile selbst werden mit einem Zertifikat der Beta-PKI durch das BSI signiert. 

### Wie kann man eigene Profile erstellen? 
Damit Sie nicht in den XML-Dateien editieren müssen, um eigene Profile zu erstellen, haben wir einen Editor implementiert. Dieser hilft Ihnen eigene Profile zu erstellen, die Sie dann im Simulator verwenden können. Der Editor steht im Kapitel [Vorgehensweise zur Installation](https://persosim.github.io/#vorgehensweise-zur-installation) bereit. 

### Wie kann man die Selbstauskunft in der AusweisApp2 mit PersoSim verwenden? 
Die AusweisApp2 kommuniziert von Haus aus mit einem für den Echtbetrieb ausgelegten eID-Server, der die Echtheit des simulierten Ausweises berechtigterweise anzweifelt. Um die simulierten Personalausweise auszulesen gibt es zwei Möglichkeiten:
* In der Datei ‚config.json‘ im Verzeichnis der AusweisApp2 können Sie den eID-Server umstellen. Unter "selfAuthentication" stellen Sie bitte auf den folgenden eID-Testserver um: "https://test.governikus-eid.de/AusweisAuskunft/WebServiceRequesterServlet?mode=json".
* In der Oberfläche der AusweisApp2 klicken Sie bitte zehnmal auf die Versionsnummer. Damit aktivieren Sie in den Entwicklermodus. Im Entwicklermodus können Sie dann unter Einstellungen im Bereich Entwicklermodus den Testmodus für die Selbstauskunft aktivieren.

### Warum lässt sich der Treiber unter Windows 10 nicht mehr installieren? 
Microsoft hat die Restriktionen für Treibersignaturen unter Windows 10 verschärft. Seit Version 1809 ist es nicht mehr möglich unsignierte Treiber zu installieren, stattdessen führt die Installation zum Fehlercode „0x80070643“. Ein Workaround besteht darin, Windows 10 im erweiterten Modus zu starten, in welchem man die Treibersignaturprüfung einmalig deaktivieren kann. Ein Anleitung um in diesem Modus zu starten findet sich z. B. [hier](https://www.tobias-hartmann.net/2018/05/windows-10-erzwingen-der-treibersignatur-deaktivieren/). Für die späteren Starts ist dieser Vorgang nicht mehr nötig, PersoSim funktioniert dennoch.  

Wichtig ist dabei, dass man ggf. zunächst die Reste der vorherigen Installationsversuche (=Virtuelle Kartenleser ohne Treiber) aus dem Geräte-Manager entfernt. Ansonsten sind anschließend mehrere virtuelle Leser installiert und PersoSim kommuniziert nicht korrekt mit dem Leser.

Aufgrund des Status als Testtool für Entwickler, nicht als Produkt für Endanwender, ist eine Signatur des Kartenlesertreibers bis auf Weiteres nicht geplant.

### Wie kann man das Pseudonym für ein Profil ändern? 
Ab Version 0.15 kann man im Editor das Pseudonym für ein Profil ändern. Dazu werden im Profil der öffentliche und der geheime Schlüssel für Restricted Identification (RI) gespeichert. Sie können unter RI nun neue Schlüsselpaare automatisch generieren lassen.

# Publikationen
Die folgenden Publikationen wurden bisher im Kontext von PersoSim veröffentlicht:
* [PersoSim simuliert den elektronischen Personalausweis – und mehr (secuview, 2017)](https://persosim.github.io/docs/sec_PersoSim_secuview_2_2017_offprint_DE.pdf)
* [PersoSim - Ein Simulator für den elektronischen Personalausweis (BSI Forum, 2015)](https://persosim.github.io/docs/BSI-Forum_2015-PersoSim_Artikel.pdf)
* [Vortrag auf der Security Document World (2015)](https://persosim.github.io/docs/SDW_2015_PersoSim_Folien.pdf)
* [Vortrag auf dem IT-Sicherheitskongress des BSI (2015)](https://persosim.github.io/docs/Sicherheitskongress_2015_PersoSim_Folien.pdf)
* [Konferenzbeitrag IT-Sicherheitskongress des BSI (2015)](https://persosim.github.io/docs/Sicherheitskongress_2015_PersoSim_Artikel.pdf)
* [PersoSim – Simulator of the German ID card (The Vault, S. 24-27, 2014)](https://persosim.github.io/docs/The_Vault_14_2014.pdf)
* [PersoSim - Der Open Source Simulator für den elektronischen Personalausweis (Datenschutz und Datensicherheit, 2014)](https://persosim.github.io/docs/DuD_2014_PersoSim_Artikel.pdf)

# Sponsor und Zertifizierung
Das Projekt PersoSim wird finanziert durch das Bundesamt für Sicherheit in der Informationstechnik. PersoSim ist wie andere physische Personalausweise auch nach TR-03105 Teil 3.3 zertifiziert und entspricht somit den Vorgaben des BSI für hoheitliche Dokumente.

![BSI Logo](https://persosim.github.io/bsi_logo.png)  ![BSI-K-TR-0198-2015](https://persosim.github.io/BSI-K-TR-0198-2015_halfsize.jpg)




