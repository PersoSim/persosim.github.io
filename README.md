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
* Alternativ zum virtuellen Kartenleser können Sie auch die **RemoteIFD-Schnittstelle** von PersoSim nutzen. Diese können Sie auch lokal einsetzen um mit PersoSim zu kommunizieren.
* **Simulator**: Starten Sie den Simulator (Eclipse RCP) für die jeweilige Plattform (Win, macOS, Linux) im entpackten Verzeichnis. Wir unterstützen mittlerweile nur noch die Versionen mit 64 Bit.
  * Windows: [de.persosim.rcp.product-0.18.3-20220209-win32.win32.x86_64.zip](https://persosim.github.io/software/de.persosim.rcp.product-0.18.3-20220209-win32.win32.x86_64.zip)
  * macOS: [de.persosim.rcp.product-0.18.3-20220209-macosx.cocoa.x86_64.zip](https://persosim.github.io/software/de.persosim.rcp.product-0.18.3-20220209-macosx.cocoa.x86_64.zip)
  * Linux: [de.persosim.rcp.product-0.18.3-20220209-linux.gtk.x86_64.zip](https://persosim.github.io/software/de.persosim.rcp.product-0.18.3-20220209-linux.gtk.x86_64.zip)     
* (optional) **Profil Editor**: Starten Sie den Editor (Eclipse RCP) für die jeweilige Plattform (Win, macOS, Linux) im entpackten Verzeichnis.
  * Windows: [de.persosim.editor.rcp.product-0.18.3-20220209-win32.win32.x86_64.zip](https://persosim.github.io/software/de.persosim.editor.rcp.product-0.18.3-20220209-win32.win32.x86_64.zip) 
  * macOS: [de.persosim.editor.rcp.product-0.18.3-20220209-macosx.cocoa.x86_64.zip](https://persosim.github.io/software/de.persosim.editor.rcp.product-0.18.3-20220209-macosx.cocoa.x86_64.zip)
  * Linux: [de.persosim.editor.rcp.product-0.18.3-20220209-linux.gtk.x86_64.zip](https://persosim.github.io/software/de.persosim.editor.rcp.product-0.18.3-20220209-linux.gtk.x86_64.zip)
* (optional) **Android-Version**: Das APK für Android finden Sie hier: [PersoSim_0_17_2.apk](https://persosim.github.io/software/PersoSim_0_17_2.apk)

Weitere Versionen von PersoSim finden Sie unter [Releases](https://github.com/PersoSim/PersoSim/releases) auf der github-Seite.


## Handbücher
Im [Anwenderhandbuch](https://persosim.github.io/manuals/Anwenderdokumentation_v1.4.pdf) beschreiben wir die Grundlagen zum Einsatz von PersoSim, angefangen von der Installation bis zum Einsatz.

Die Vorgehensweise zum Ändern von Trust Points beschreiben wir im Dokument [TA_Trust_Points_v1.3.pdf](https://persosim.github.io/manuals/TA_Trust_Points_v1.3.pdf).

## Profile
In PersoSim nutzen wir nicht nur typische Profile, wie sie im physischen Personalausweis verwendet werden, sondern auch Unionsbürgerkarten und Smart-eID. Informationen zu den Profilen der jeweiligen Varianten stellen wir in den folgenden Dokumenten bereit:
* Klassischer Personalausweis: [PersoSim_Personalisierungsdaten_nPA.pdf](https://persosim.github.io/manuals/PersoSim_Personalisierungsdaten_nPA.pdf)
* Unionsbürgerkarte: [PersoSim_Personalisierungsdaten_eID_UB.pdf](https://persosim.github.io/manuals/PersoSim_Personalisierungsdaten_eID_UB.pdf)
* Smart-eID: [Smart-eID-PersoSim_Personalisierungsdaten-2021.pdf](https://persosim.github.io/manuals/Smart-eID-PersoSim_Personalisierungsdaten-2021.pdf)


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




