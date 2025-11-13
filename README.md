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
Willkommen auf dem Internet-Portal der Open Source Community zu PersoSim, dem Simulator für den neuen elektronischen Personalausweis (nPA oder ePA). PersoSim dient dazu, die Softwareentwicklung für die Nutzung des neuen Personalausweises voranzutreiben. Dazu möchte das Projekt Entwickler, Unternehmen und Behörden in dieser Community zusammenbringen. PersoSim ist ein Mosaikstein im Testkonzept des BSI für die eID-Infrastruktur. Die [Testinfrastruktur](https://www.bsi.bund.de/DE/Themen/Oeffentliche-Verwaltung/Elektronische-Identitaeten/Online-Ausweisfunktion/Testinfrastruktur/testinfrastruktur_node.html) beschreibt die einzelnen Komponenten innerhalb der eID-Infrastruktur wie bspw. [PersoSim](https://www.bsi.bund.de/DE/Themen/Oeffentliche-Verwaltung/Elektronische-Identitaeten/Online-Ausweisfunktion/Testinfrastruktur/PersoSim/PersoSim_node.html) und informiert über die Testmöglichkeiten sowie die dazugehörigen Testwerkzeuge. Interessierte Anwender und Entwickler sind natürlich herzlichst eingeladen, sich an der PersoSim-Community auf unterschiedliche Weise einzubringen. Die github Repositories mit dem Quellcode und weiteren Informationen für Entwickler liegen hier: [https://github.com/PersoSim](https://github.com/PersoSim).

Bei Fragen zu PersoSim ist unsere FAQ hilfreich, die wir ständig erweitern. Sollte sich die Frage dort nicht klären lassen, sind wir über unsere Support-Adresse erreichbar: support (at) persosim (punkt) de und versuchen alle Fragen bzgl. PersoSim zu lösen. Gerne nehmen wir darüber auch Ideen zur Verbesserung oder Erweiterungswünsche auf. 

# Aktuelles

## PersoSim Version 1.4 veröffentlicht mit Remote-Schnittstelle und verbessertem Logging
> Die neue Version 1.4 des Personalausweis-Simulators liefert die folgenden Features:
> *	Terminal-Schnittstelle: Zur einfacheren Ansteuerung von PersoSim haben wir nun eine Remote-Schnittstelle integriert über die sich PersoSim fernsteuern lässt. Diese Schnittstelle soll den Einsatz für Continuous Integration (CI) erleichtern. Die unterstützen Kommandos werden im aktualisierten Anwenderhandbuch beschrieben.
> *	Remote-IFD-Schnittstelle: der Kopplungscode kann weiterhin zufällig generiert werden bzw. frei gewählt werden. Allerdings ist der Kopplungscode von nun an beim Start auf ‚1234‘ eingestellt, was die Kopplung im Testkontext vereinfachen soll.
> *	Logging: wir haben das Logging in PersoSim grundlegend überarbeitet, so dass der Anwender nun viele Möglichkeiten hat, das Logging für seine Bedürfnisse anzupassen. Nähere Infos dazu finden sich ebenfalls im aktualisierten Anwenderhandbuch.

> Wer sich wundert, wo die Version 1.3 geblieben ist: wir haben die Versionsnummerierung umgestellt, so dass gerade Versionsnummern (minor) nun immer die aktuellen Releases kenntlich machen. Ungerade Nummern stehen für Zwischenversionen, die wir bei Bedarf für Testzwecke bereitstellen.

> Ausblick: In der nächsten Version werden wir die GUI von PersoSim grundlegend überarbeiten.

## PersoSim Version 1.2 veröffentlicht
> Mit der Version 1.2 des Personalausweis-Simulators stellen wir gleich mehrere neue Funktionen bereit:
> * Android: Neue Anbindung des Android Smart Card Emulators aus dem vsmartcard-Projekt an PersoSim. Der Android Smart Card Emulator kann genutzt werden, um PersoSim mithilfe eines Android-Geräts mit NFC und eines RFID-Kartenlesers anzusprechen.
Zur Verwendung muss derzeit noch ein aktueller Stand der App von https://github.com/frankmorgner/vsmartcard/tree/master/ACardEmulator
genutzt werden. Die Version 3.5, wie sie in F-Droid zur Verfügung steht, hat derzeit noch nicht die korrekte Applet-ID, um direkt von der AusweisApp genutzt werden zu können.
Beide Geräte (PersoSim und Android) müssen sich per Netzwerk erreichen können und die korrekte IP-Adresse und der Port müssen im Android Smart Card Emulator eingetragen werden. PersoSim stellt QR-Codes zur Verfügung, die in den Einstellungen der App gescannt werden können, um die entsprechenden Werte zu setzen.
> * Simulator: Zusätzliche Unterstützung des Protokolls CAv3. Mit dem Protokoll Chip Authentication in Version 3 (CAv3) haben wir die Protokolle in PersoSim vervollständigt. CAv3 ist eine Alternative zu CAv2 und Restricted Identification (RI) und bietet neben der starken expliziten Authentifizierung des Ausweises und der bereitgestellten sektorspezifischen Kennungen gegenüber dem Terminal u.a. auch die Sicherstellung der Pseudonymität des Ausweises ohne die Notwendigkeit, dieselben Schlüssel auf mehreren Chips zu verwenden.
> Hinweis: In Zusammenhang mit der Umsetzung von CAv3 haben wir die Profilstruktur erweitert. Aus diesem Grund benötigt der aktuelle Simulator auch Profile, die mit dem aktuellen Editor erstellt werden. Es ist keine Abwärtskompatibilität gewährleistet. Die mitgelieferten Profile sind davon selbstverständlich nicht betroffen.
> *	Simulator: Unterstützung des COMPARE-Kommandos. Mit diesem Kommando lassen sich Daten auf unterschiedliche Weise vergleichen. Wir haben das Kommandos so implementiert, dass der Mechanismus wie beim Personalausweis die Verifikation der Datengruppen DG3 (Geburtsdatum), DG8 (Ablaufdatum) und DG18 (CommunityID) unterstützt.
> *	Simulator: Unterstützung des ENVELOPE-Kommandos. Dieser Mechanismus kann als eine Alternative für Devices genutzt werden, die kein Extended Length unterstützen. Die einzelnen Kommandos zwischen Simulator und Terminal (und umgekehrt) werden dazu in kleinere Pakete verpackt und übertragen.
> Darüber hinaus haben wir die Profile aktualisiert und neu signiert. Profile für die Smart-eID haben wir im Simulator entfernt, da sie nicht mehr benötigt werden.

> Ausblick: Auch die nächste PersoSim-Version wird wieder neue Features beinhalten. In der zukünftigen Version 1.4 stellen ein überarbeitetes Logging zur Verfügung, eine Schnittstelle zur Fernsteuerung des Simulators und eine Vereinfachung bei der Remote-IFD-Interface.

## Windows-Treiber jetzt signiert
> Wir freuen uns, dass wir nun endlich auch einen signierten Windows-Treiber zur Verfügung stellen können. Das Installationspaket liegt hier: [PersoSim_Win_Driver_x64.zip](https://persosim.github.io/software/PersoSim_Win_Driver_x64.zip). Für die Installation des Windows-Treibers sind weiterhin Admin-Rechte notwendig.
> Bedanken möchten wir uns an dieser Stelle bei der Firma adesso, die den Treiber im Rahmen des Fidelio-Projekts signiert hat.


Ältere News befinden sich im [Archiv](https://persosim.github.io/news_archive.html).

# Downloads und Installation
Dieses Kapitel enthält die Dateien, die für den Betrieb des Simulators nötig sind, sowie eine kurze Anleitung zur Installation. Wir unterstützen neben Windows auch Linux und macOS für die stationäre Variante von PersoSim. Für ältere Smartphones mit NFC liegt ein Android-APK bereit.

## Systemvoraussetzungen
Java muss mindestens in Version 17 oder neuer installiert sein. Wir empfehlen entweder das Installationspaket von [Adoptium](https://adoptium.net/de/), das alle notwendigen Einstellungen automatisch vornimmt, oder das [OpenJDK](https://jdk.java.net/) bei dem die Einstellungen manuell durchgeführt werden können.

## Vorgehensweise zur Installation
Bitte nutzen Sie die folgenden Schritte zum Installieren und Starten des Simulators:
* Installation des Treibers für den **virtuellen Kartenleser**: Wählen Sie bitte je nach System Treiber für Linux bzw. macOS oder Windows und folgen Sie bitte den Installationsanweisungen. Der Windows-Treiber enthält die notwendigen Dateien sowohl für Windows 7, 8 und 10 jeweils als Architektur mit 32 Bit oder 64 Bit.
  * Den Treiber für Linux und macOS müssen Sie derzeit selbst kompilieren; die Sourcen finden Sie hier: [PersoSim_Driver_PCSCLite_20240917.tgz](https://persosim.github.io/software/PersoSim_Driver_PCSCLite_20240917.tgz).
  * Das Installationspaket für Windows finden Sie hier: [PersoSim_Win_Driver_x64.zip](https://persosim.github.io/software/PersoSim_Win_Driver_x64.zip)
* Alternativ zum virtuellen Kartenleser können Sie auch die **RemoteIFD-Schnittstelle** von PersoSim nutzen. Diese können Sie auch lokal einsetzen um mit PersoSim zu kommunizieren.
* **Simulator**: Starten Sie den Simulator (Eclipse RCP) für die jeweilige Plattform (Win, macOS, Linux) im entpackten Verzeichnis. Wir unterstützen mittlerweile nur noch die Versionen mit 64 Bit.
  * Windows: [PersoSim 1.4.0](https://github.com/PersoSim/PersoSim/releases/download/1.4.0/de.persosim.rcp.product-1.4.0-20251112-win32.win32.x86_64.zip)
  * macOS: [PersoSim 1.4.0](https://github.com/PersoSim/PersoSim/releases/download/1.4.0/de.persosim.rcp.product-1.4.0-20251112-macosx.cocoa.aarch64.tar.gz)
  * Linux: [PersoSim 1.4.0](https://github.com/PersoSim/PersoSim/releases/download/1.4.0/de.persosim.rcp.product-1.4.0-20251112-linux.gtk.x86_64.tar.gz)     
* (optional) **Profil Editor**: Starten Sie den Editor (Eclipse RCP) für die jeweilige Plattform (Win, macOS, Linux) im entpackten Verzeichnis.
  * Windows: [PersoSim Editor 1.4.0](https://github.com/PersoSim/PersoSim/releases/download/1.4.0/de.persosim.editor.rcp.product-1.4.0-20251112-win32.win32.x86_64.zip) 
  * macOS: [PersoSim Editor 1.4.0](https://github.com/PersoSim/PersoSim/releases/download/1.4.0/de.persosim.editor.rcp.product-1.4.0-20251112-macosx.cocoa.aarch64.tar.gz)
  * Linux: [PersoSim Editor 1.4.0](https://github.com/PersoSim/PersoSim/releases/download/1.4.0/de.persosim.editor.rcp.product-1.4.0-20251112-linux.gtk.x86_64.tar.gz)
* (optional) **Android-Version**: Das APK für Android finden Sie hier: [PersoSim_0_17_2.apk](https://persosim.github.io/software/PersoSim_0_17_2.apk)

Weitere Versionen von PersoSim finden Sie unter [Releases](https://github.com/PersoSim/PersoSim/releases) auf der github-Seite.

*Hinweis zu macOS: Nach dem Download einer Datei unter macOS in das Standard-Verzeichnis "Downloads" setzt macOS für diese Datei ein Quarantäne-Flag. Sobald dieses Flag gesetzt wird, kommt beim Start von PersoSim die Fehlermeldung, dass die Datei defekt sei und in den Mülleimer verschoben werden sollte. Man kann dieses Problem umgehen, indem man die PersoSim-Datei über einen anderen Weg als den Browser herunterlädt, z.B. über wget. Oder man entfernt nach dem Download das Quarantäne-Flag mit folgendem Kommando: sudo xattr -r -d com.apple.quarantine /path/to/de.persosim.rcp.product-1.0.1-20240912-macosx.cocoa.x86_64.tar.gz*

## Handbücher
Im [Anwenderhandbuch](https://persosim.github.io/manuals/PersoSim_Anwenderdokumentation_v1.5.1.pdf) beschreiben wir die Grundlagen zum Einsatz von PersoSim, angefangen von der Installation bis zum Einsatz. Die Vorgehensweise zum Ändern von Trust Points beschreiben wir mittlerweile ebenfalls im Anwenderhandbuch.

## Profile
In PersoSim nutzen wir nicht nur typische Profile, wie sie im physischen Personalausweis verwendet werden, sondern auch Unionsbürgerkarten und Smart-eID. Informationen zu den Profilen der jeweiligen Varianten stellen wir in den folgenden Dokumenten bereit:
* Klassischer Personalausweis: [PersoSim Personalisierungsdaten nPA 2024](https://persosim.github.io/manuals/nPA-PersoSim_Personalisierungsdaten_V3-2024.pdf)
* Unionsbürgerkarte: [PersoSim Personalisierungsdaten eID UB 2024](https://persosim.github.io/manuals/eID-UB-PersoSim_Personalisierungsdaten_V2-2024.pdf)


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




