You can find an **english** description of PersoSim [here](https://persosim.github.io/readme_eng.html).

**Inhaltsverzeichnis**

[Der Open Source Simulator für den elektronischen Personalausweis](https://persosim.github.io#der-open-source-simulator-f%C3%BCr-den-elektronischen-personalausweis)

[Aktuelles](https://persosim.github.io#aktuelles)

[Downloads und Installation](https://persosim.github.io#downloads-und-installation)

[Technik](https://persosim.github.io/technology.html)

[Simulator](https://persosim.github.io/simulator.html)

[Frequently Asked Questions (FAQ)](https://persosim.github.io/faq.html)

[Publikationen](https://persosim.github.io#publikationen)

[Sponsor und Zertifizierung](https://persosim.github.io#sponsor-und-zertifizierung)

https://www.bsi.bund.de/DE/Themen/Oeffentliche-Verwaltung/Elektronische-Identitaeten/Online-Ausweisfunktion/Testinfrastruktur/testinfrastruktur_node.html

# Der Open Source Simulator für den elektronischen Personalausweis
Willkommen auf dem Internet-Portal der Open Source Community zu PersoSim, dem Simulator für den neuen elektronischen Personalausweis (nPA oder ePA). PersoSim dient dazu, die Softwareentwicklung für die Nutzung des neuen Personalausweises voranzutreiben. Dazu möchte das Projekt Entwickler, Unternehmen und Behörden in dieser Community zusammenbringen. PersoSim ist ein Mosaikstein im Testkonzept des BSI für die eID-Infrastruktur. Die [Testinfrastruktur](https://www.bsi.bund.de/DE/Themen/Oeffentliche-Verwaltung/Elektronische-Identitaeten/Online-Ausweisfunktion/Testinfrastruktur/testinfrastruktur_node.html) beschreibt die einzelnen Komponenten innerhalb der eID-Infrastruktur wie bspw. [PersoSim](https://www.bsi.bund.de/DE/Themen/Oeffentliche-Verwaltung/Elektronische-Identitaeten/Online-Ausweisfunktion/Testinfrastruktur/PersoSim/PersoSim_node.html) und informiert über die Testmöglichkeiten sowie die dazugehörigen Testwerkzeuge. Interessierte Anwender und Entwickler sind natürlich herzlichst eingeladen, sich an der PersoSim-Community auf unterschiedliche Weise einzubringen. Die github Repositories mit dem Quellcode und weiteren Informationen für Entwickler liegen hier: [https://github.com/PersoSim](https://github.com/PersoSim).

Bei Fragen zu PersoSim ist unsere FAQ hilfreich, die wir ständig erweitern. Sollte sich die Frage dort nicht klären lassen, sind wir über unsere Support-Adresse erreichbar: support (at) persosim (punkt) de und versuchen alle Fragen bzgl. PersoSim zu lösen. Gerne nehmen wir darüber auch Ideen zur Verbesserung oder Erweiterungswünsche auf. 

# Aktuelles

## PersoSim Version 1.1 veröffentlicht
> Zum Ende des Jahres haben wir nun die Version 1.1 von PersoSim veröffentlicht. In diese Releasem gibt es zwei Änderungen:
> * Der Editor ermöglicht es nun dem Anwender die RI-Schlüssel selbst zu ändern oder neu generieren zu lassen. Darüber hinaus werden jetzt beim ersten Start von PersoSim die RI-Schlüssel für jedes Profil neu ausgewürfelt. Dies dient dazu, um Konflikte bei der Anmeldung auf Websites zu vermeiden.  
> * Im Editor lassen sich nun Profile im JSON-Format exportieren, so dass die Profile zukünftig im Emulator der AusweisApp verwendet werden können. Informationen zum JSON-Format gibt es hier: [File system](https://www.ausweisapp.bund.de/sdk/simulator.html#filesystem).

## PersoSim für macOS veröffentlicht
> Wir freuen uns, dass wir nun auch endlich wieder eine Version für macOS zur Verfügung stellen können. In diesem Zusammenhang haben wir das Pairing für RemoteIFD bzw. SaK einheitlich für alle drei Plattformen auf Zertifikats-Fingerprints umgestellt. Zusätzlich haben wir die Sourcen für den virtuellen Kartenleser an das aktuelle macOS angepasst. Die Links zum Download der Version 1.0.1 finden sich weiter unten in Kapitel [Downloads und Installation](https://persosim.github.io#downloads-und-installation) oder hier [Release 1.0.1](https://github.com/PersoSim/PersoSim/releases/tag/1.0.1)

## PersoSim Version 1.0.0 veröffentlicht
> Wir freuen uns, dass wir nun Version 1.0.0 des PersoSim-Simulators und des -Editors veröffentlichen können. Zum Download stehen Version für Windows und Linux zur Verfügung. Die macOS-Version folgt demnächst. Die maßgeblichen Änderungen haben wir im Unterbau vorgenommen, so dass wir neue Änderungen zukünftig einfacher implementieren können. Dabei geht es um die folgenden Änderungen:
> * PersoSim und der dazugehörige Editor basieren nun auf Java 17 bzw. 21 sowie auf Eclipse 2024/3
> * Der Editor signiert nun die Personalisierungsdaten mit ECDSA-256, ECDSA-384 oder ECDSA-512
> * Die Profile (nPA und UB) wurden aktualisiert und neu signiert
> * Im Logging des Simulators werden nun auf Systeminformationen protokolliert  

Ältere News befinden sich im [Archiv](https://persosim.github.io/news_archive.html).

# Downloads und Installation
Dieses Kapitel enthält die Dateien, die für den Betrieb des Simulators nötig sind, sowie eine kurze Anleitung zur Installation. Wir unterstützen neben Windows auch Linux und macOS für die stationäre Variante von PersoSim. Für ältere Smartphones mit NFC liegt ein Android-APK bereit.

## Systemvoraussetzungen
Java muss mindestens in Version 17 oder neuer installiert sein. Wir empfehlen entweder das Installationspaket von [Adoptium](https://adoptium.net/de/), das alle notwendigen Einstellungen automatisch vornimmt, oder das [OpenJDK](https://jdk.java.net/) bei dem die Einstellungen manuell durchgeführt werden können.

## Vorgehensweise zur Installation
Bitte nutzen Sie die folgenden Schritte zum Installieren und Starten des Simulators:
* Installation des Treibers für den **virtuellen Kartenleser**: Wählen Sie bitte je nach System Treiber für Linux bzw. macOS oder Windows und folgen Sie bitte den Installationsanweisungen. Der Windows-Treiber enthält die notwendigen Dateien sowohl für Windows 7, 8 und 10 jeweils als Architektur mit 32 Bit oder 64 Bit.
  * Den Treiber für Linux und macOS müssen Sie derzeit selbst kompilieren; die Sourcen finden Sie hier: [PersoSim_Driver_PCSCLite_20240917.tgz](https://persosim.github.io/software/PersoSim_Driver_PCSCLite_20240917.tgz).
  * Das Installationspaket für Windows finden Sie hier: [PersoSim_Driver_win_20180209.zip](https://persosim.github.io/software/PersoSim_Driver_win_20180209.zip)
* Alternativ zum virtuellen Kartenleser können Sie auch die **RemoteIFD-Schnittstelle** von PersoSim nutzen. Diese können Sie auch lokal einsetzen um mit PersoSim zu kommunizieren.
* **Simulator**: Starten Sie den Simulator (Eclipse RCP) für die jeweilige Plattform (Win, macOS, Linux) im entpackten Verzeichnis. Wir unterstützen mittlerweile nur noch die Versionen mit 64 Bit.
  * Windows: [PersoSim 1.1.0](https://github.com/PersoSim/PersoSim/releases/download/1.1.0/de.persosim.rcp.product-1.1.0-20241212-win32.win32.x86_64.zip)
  * macOS: [PersoSim 1.1.0](https://github.com/PersoSim/PersoSim/releases/download/1.1.0/de.persosim.rcp.product-1.1.0-20241212-macosx.cocoa.aarch64.tar.gz)
  * Linux: [PersoSim 1.1.0](https://github.com/PersoSim/PersoSim/releases/download/1.1.0/de.persosim.rcp.product-1.1.0-20241212-linux.gtk.x86_64.tar.gz)     
* (optional) **Profil Editor**: Starten Sie den Editor (Eclipse RCP) für die jeweilige Plattform (Win, macOS, Linux) im entpackten Verzeichnis.
  * Windows: [PersoSim Editor 1.1.0](https://github.com/PersoSim/PersoSim/releases/download/1.1.0/de.persosim.editor.rcp.product-1.1.0-20241212-win32.win32.x86_64.zip) 
  * macOS: [PersoSim Editor 1.1.0](https://github.com/PersoSim/PersoSim/releases/download/1.1.0/de.persosim.editor.rcp.product-1.1.0-20241212-macosx.cocoa.aarch64.tar.gz)
  * Linux: [PersoSim Editor 1.1.0](https://github.com/PersoSim/PersoSim/releases/download/1.1.0/de.persosim.editor.rcp.product-1.1.0-20241212-linux.gtk.x86_64.tar.gz)
* (optional) **Android-Version**: Das APK für Android finden Sie hier: [PersoSim_0_17_2.apk](https://persosim.github.io/software/PersoSim_0_17_2.apk)

Weitere Versionen von PersoSim finden Sie unter [Releases](https://github.com/PersoSim/PersoSim/releases) auf der github-Seite.

*Hinweis zu macOS: Nach dem Download einer Datei unter macOS in das Standard-Verzeichnis "Downloads" setzt macOS für diese Datei ein Quarantäne-Flag. Sobald dieses Flag gesetzt wird, kommt beim Start von PersoSim die Fehlermeldung, dass die Datei defekt sei und in den Mülleimer verschoben werden sollte. Man kann dieses Problem umgehen, indem man die PersoSim-Datei über einen anderen Weg als den Browser herunterlädt, z.B. über wget. Oder man entfernt nach dem Download das Quarantäne-Flag mit folgendem Kommando: sudo xattr -r -d com.apple.quarantine /path/to/de.persosim.rcp.product-1.0.1-20240912-macosx.cocoa.x86_64.tar.gz*

## Handbücher
Im [Anwenderhandbuch](https://persosim.github.io/manuals/Anwenderdokumentation_v1.4.pdf) beschreiben wir die Grundlagen zum Einsatz von PersoSim, angefangen von der Installation bis zum Einsatz.

Die Vorgehensweise zum Ändern von Trust Points beschreiben wir im Dokument [TA_Trust_Points_v1.3.pdf](https://persosim.github.io/manuals/TA_Trust_Points_v1.3.pdf).

## Profile
In PersoSim nutzen wir nicht nur typische Profile, wie sie im physischen Personalausweis verwendet werden, sondern auch Unionsbürgerkarten und Smart-eID. Informationen zu den Profilen der jeweiligen Varianten stellen wir in den folgenden Dokumenten bereit:
* Klassischer Personalausweis: [PersoSim Personalisierungsdaten nPA 2024](https://persosim.github.io/manuals/nPA-PersoSim_Personalisierungsdaten_V3-2024.pdf)
* Unionsbürgerkarte: [PersoSim Personalisierungsdaten eID UB 2024](https://persosim.github.io/manuals/eID-UB-PersoSim_Personalisierungsdaten_V2-2024.pdf)
* Smart-eID: [PersoSim Personalisierungsdaten Smart-eID 2021](https://persosim.github.io/manuals/Smart-eID-PersoSim_Personalisierungsdaten-2021.pdf)


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




