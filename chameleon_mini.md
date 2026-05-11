# PersoSim mit Chameleon Mini 
Die Version 1.5.5 von PersoSim entspricht der Version 1.6.0, enthält jedoch zusätzlich eine Schnittstelle für die Verwendung des Chameleon Mini zur Simulation. 
Das Chameleon Mini ist ein frei programmierbares Werkzeug für die Kartensimulation welches durch die Firma Kasper & Oswald GmbH verkauft wird. Weitere Informationen diesbezüglich können auf der Herstellerwebsite unter https://kasper-oswald.de/chameleonmini/ gefunden werden.

Das Chameleon Mini ist für die Simulation von simplen NFC-Anwendungen entwickelt worden. Während der Arbeit mit dem Chameleon Mini hat sich gezeigt, dass die Simulation einer eID fähigen SmartCard nach TR-03110 die ursprünglich in der Entwicklung des Chameleon Minis geplanten Leistungen, im Bereich Timing, Kommunikationsraten und Feldstärken bei weitem übersteigt. Trotzdem ist es gelungen über das Chameleon Mini mit einigen ausgewählten Kartenlesern erfolgreiche eID-Vorgänge zu simulieren.

Für die praktische Anwendung bedeutet dies, dass diese Simulationsmöglichkeit nur mit bestimmten Lesern nutzbar ist. Eine Liste von Lesern, die für diesen Zweck geeignet sind, findet sich unter diesem Text. Diese Liste ist jedoch nicht als abschließend zu verstehen, sondern spiegelt Erfahrungen aus der Entwicklung wider.

Für die Verwendungen des Chameleon Mini muss auf dieses erst die bereitgestellte Firmware geflasht werden. Eine Anleitung dazu findet sich auf https://cdn.statically.io/gh/emsec/ChameleonMini@master/Doc/Doxygen/html/_page__getting_started.html

Da diese Version eine prototypische Version ist, wird sie nicht weiter gepflegt werden. Ein Fehler dieser Version auf MacOS ist bekannt, eine Behebung von diesem ist aber derzeit nicht im Projektplan vorgesehen. Es wurde entschieden, diese Version trotz der erwähnten Einschränkungen zu veröffentlichen, da das Chameleon Mini eine kostengünstige, physische Möglichkeit zur Simulation darstellt, die dank der freien Programmierbarkeit auch in anderen Szenarien genutzt werden kann und sich damit auch als Einstiegsmöglichkeit anbietet. Außerdem war es ein Anliegen, die gewonnenen Erkenntnisse und den produzierten Code der Community für weitere Experimente zur Verfügung zu stellen.

Nach derzeitigem Stand sind mit folgenden Kartenlesern prinzipielle erfolgreiche Simulationen mit Chameleon Mini möglich:
* ReinerSCT cyberjack Basis, Charge 2020-36
* uTrust 3700 F und 4701 F
* gemalto Prox-SU

Die einzelnen Dateien zum Release sind hier veröffentlicht: https://github.com/PersoSim/PersoSim/releases/tag/1.5.5
