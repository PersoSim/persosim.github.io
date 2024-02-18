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


