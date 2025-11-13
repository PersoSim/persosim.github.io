# Archiv der bisherigen Meldungen
Hier befinden sich ältere Meldungen zum Projekt "PersoSim":

## PersoSim Version 1.1 veröffentlicht
Zum Ende des Jahres haben wir nun die Version 1.1 von PersoSim veröffentlicht. In diese Release gibt es zwei Änderungen:
* Der Editor ermöglicht es nun dem Anwender die RI-Schlüssel selbst zu ändern oder neu generieren zu lassen. Darüber hinaus werden jetzt beim ersten Start von PersoSim die RI-Schlüssel für jedes Profil neu ausgewürfelt. Dies dient dazu, um Konflikte bei der Anmeldung auf Websites zu vermeiden.  
* Im Editor lassen sich nun Profile im JSON-Format exportieren, so dass die Profile zukünftig im Emulator der AusweisApp verwendet werden können. Informationen zum JSON-Format gibt es hier: [File system](https://www.ausweisapp.bund.de/sdk/simulator.html#filesystem).

## PersoSim für macOS veröffentlicht
Wir freuen uns, dass wir nun auch endlich wieder eine Version für macOS zur Verfügung stellen können. In diesem Zusammenhang haben wir das Pairing für RemoteIFD bzw. SaK einheitlich für alle drei Plattformen auf Zertifikats-Fingerprints umgestellt. Zusätzlich haben wir die Sourcen für den virtuellen Kartenleser an das aktuelle macOS angepasst. Die Links zum Download der Version 1.0.1 finden sich weiter unten in Kapitel [Downloads und Installation](https://persosim.github.io#downloads-und-installation) oder hier [Release 1.0.1](https://github.com/PersoSim/PersoSim/releases/tag/1.0.1)

## PersoSim Version 1.0.0 veröffentlicht
Wir freuen uns, dass wir nun Version 1.0.0 des PersoSim-Simulators und des -Editors veröffentlichen können. Zum Download stehen Version für Windows und Linux zur Verfügung. Die macOS-Version folgt demnächst. Die maßgeblichen Änderungen haben wir im Unterbau vorgenommen, so dass wir neue Änderungen zukünftig einfacher implementieren können. Dabei geht es um die folgenden Änderungen:
* PersoSim und der dazugehörige Editor basieren nun auf Java 17 bzw. 21 sowie auf Eclipse 2024/3
* Der Editor signiert nun die Personalisierungsdaten mit ECDSA-256, ECDSA-384 oder ECDSA-512
* Die Profile (nPA und UB) wurden aktualisiert und neu signiert
* Im Logging des Simulators werden nun auf Systeminformationen protokolliert  

## PersoSim-Präsentation im Rahmen der DIF AG eID
Im Rahmen der 19. Sitzung der DIF AG eID beim BSI in Bonn hatten wir die Gelegenheit, PersoSim zu präsentieren. Wir haben dort den aktuellen Stand des Projekts dargestellt und eine Demo zu PersoSim gegeben. Die Demo hat sich dabei von der Installation des Treibers für den virtuellen Kartenleser über die Nutzung des Simulators bis zur Kommunikation zwischen zwei HCE-Smartphones erstreckt. Anschließend konnten wir mit den Teilnehmern über ihre Einsatzzwecke von PersoSim und ihre Erweiterungswünsche sowie Verbesserungsvorschläge diskutieren. Die Folien zum Vortrag finden sich hier: [DIF-AG-eID_PersoSim-Workshop_20240307.pdf](https://persosim.github.io/docs/DIF-AG-eID_PersoSim-Workshop_20240307.pdf).

## Weiterentwicklung von PersoSim gestartet
Aktuell sammeln wir neue Anforderungen für die Weiterentwicklung von PersoSim. Dazu sprechen wir mit unterschiedlichen Stakeholdern, sammeln neue Anforderungen, bewerten diese und sortieren sie ein um sie dann zu implementieren. Es wird also zukünftig wieder neue Releases geben. Neuigkeiten werden wir auch über unseren neuen Mastodon-Account bereitstellen: <a rel="me" href="https://mastodon.social/@persosim">mastodon.social/@persosim</a>

## PersoSim 0.18.3 veröffentlicht
Der Simulator für den deutschen Personalausweis steht nun in Version 0.18.3 zur Verfügung. Die Änderungen erstrecken sich auf die Smart-eID, so dass der Simulator nun neue Profile für die Smart-eID beinhaltet, die  zusätzlich mit dem Editor bearbeitet werden können.

## PersoSim jetzt auch auf der BSI-Website
Das BSI hat auf seiner Website nun eine eigene [Seite](https://www.bsi.bund.de/PersoSim) für PersoSim angelegt. Dort gibt es alle Informationen zum Simulator und den dazugehörigen Tools in kompakter Form. Als Teil der eID-Infrastruktur ist PersoSim ein wichtiger Mosaikstein, um die Interoperabilität der Komponenten im deutschen eID-System sicherzustellen. Die Testinfrastruktur setzt sich zu diesem Zweck aus den einzelnen Komponenten der eID-Infrastruktur zusammen, um den Herstellern der einzelnen Komponenten Testmöglichkeiten sowie Testwerkzeuge an die Hand zu geben. Für darüberhinausgehende Tests – wie bspw. die Integration des Simulators in die bestehende Continuous Integration – stehen die Entwickler und Berater der secunet gerne zur Verfügung.

## PersoSim 0.17.2 veröffentlicht
Der Ausweis-Simulator PersoSim steht nun in Version 0.17.2 mit den folgenden Änderungen bereit:
* Remote IFD - Schnittstelle: Aktualisierung auf v2 gemäß Ergänzung TR-03112-6 und Fehlerbehebungen bei der Verbindung mit der AusweisApp2
* Aktualisierung der Handbücher: Die Handbücher wurden überarbeitet und stehen zudem nun auch in englischer Sprache bereit
* Einstellung von x86: PersoSim steht zukünftig nicht mehr für x86-Systeme bereit
* Kleinere Fehlerbehebungen im Simulator z.B. beim Laden von Profildateien unter Android oder der Kartenkommunikation in bestimmten Situationen

## secuview berichtet über PersoSim
In der Ausgabe 2/2017 der secuview gibt es einen Artikel zu PersoSim. Holger Funke beschreibt dort den Simulator und die Einsatzmöglichkeiten. Der Artikel steht unter ‚Veröffentlichungen‘ zur Verfügung oder direkt über diesen [Link](https://persosim.github.io/docs/sec_PersoSim_secuview_2_2017_offprint_DE.pdf)
