# Simulator
Im Rahmen der Entwicklung des Testwerkzeugs [GlobalTester](https://globaltester.secunet.com/de/) existiert bereits ein Simulator für elektronische Reisepässe (ePassport) bzw. den neuen elektronischen Personalausweis (nPA). Dieser Simulator wird bereits als kommerzielle Version für Konformitätstests gemäß der BSI TR-03105 erfolgreich eingesetzt. Die kommerzielle Version nutzt dabei ebenfalls nur kommerziell verfügbare Hardware, die die Kommunikation zwischen dem Kartenleser und dem Software-Simulator übernimmt. Die Hardware (Comprion CLT one) handelt dabei die Parameter für die Kommunikation aus und stellt dem Simulator die APDU zur Verfügung. Der Simulator wiederum berechnet die Antworten und sendet diese über die Hardware zurück an den Kartenleser. Die Abbildung zeigt diese Art der Kommunikation in Anlehnung an das ISO/OSI-Schichtenmodell.

![Simulator_ISO_Layer](https://persosim.github.io/Simulator_ISO_Layer.png)

Da für ein Open Source Projekt wie PersoSim die Hardware aufgrund der hohen Kosten nur schwer zur Verfügung steht, stellen wir hier eine Alternative bereit. Statt physikalischer Hardware nutzen wir hier einen virtuellen Kartenleser, der sich wie ein ganz normaler Kartenleser in bestehende Anwendungen integrieren lässt und der die Kommunikation mit dem Simulator übernimmt. In obiger Abbildung ist diese Art der Kommunikation ebenfalls abgebildet.

Die folgende Grafik ordnet den Simulator aus dem Projekt PersoSim in den Kontext des deutschen Personalausweis und der eID-Clients sowie der eID-Server ein.

![PersoSim_Grafik_DE](https://persosim.github.io/PersoSim_Grafik_DE.jpg)
