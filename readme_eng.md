# The Open Source Simulator of the German Electronic Identity Card
Welcome to the Internet portal of the open source community for PersoSim, the simulator of the German electronic identity card (nPA or ePA). PersoSim aims to drive the software development for the new eID card and to increase the use of the eID card functions.

For this purpose, the project seeks to bring together developers, businesses and government authorities in this online community. Interested users and developers are invited to contribute to the PersoSim community in different ways. 

# About the Project
The PersoSim project was commissioned by the [German Federal Office for Information Security (BSI)](https://www.bsi.bund.de/EN/Home/home_node.html) and is conducted by the [secunet Security Networks AG](https://www.secunet.com/). The electronic identity card (nPA) with its integrated chip provides a higher authentication strength than do other authentication procedures, such as username and password, and thus is expected to be used increasingly in both eGovernment and eBusiness applications. 

The open source project "PersoSim" provides a simulator for the smart card functions of the new eID card. The eID simulator allows interested users to verify their applications for the new eID card. It offers a versatile alternative to sample cards, which are not only difficult to get but also limited in their use, i.e. because of involved certificates.

All protocols and security mechanisms for the electronic identity card of the technical guideline BSI TR-03110 are implemented in the simulator and allow a complete simulation of the eID function.

In addition to the eID simulator, virtual Windows- and Linux-based card readers (drivers) are developed in the project. These virtual readers allow application developers to also simulate the functions of the different types of reading devices (basic, standard or comfort reader) for the German identity card based on the technical guideline [BSI TR-03119](https://www.bsi.bund.de/SharedDocs/Downloads/EN/BSI/Publications/TechGuidelines/TR03119/BSI-TR-03119_V1_pdf.pdf?__blob=publicationFile&v=2). Thus the virtual card reader supports the use of a PIN pad as it is the case with standard or comfort readers. The virtual drivers are a substitute for costly external test laboratory equipment. 

In particular, manufacturers of eID clients and eID servers as well as eID service providers, which play a significant role in the use of the new ID card for on-line applications (i.e. in eGovernment), can benefit from the many opportunities offered by PersoSim: 

![PersoSim_Grafik_DE](https://persosim.github.io/PersoSim_Grafik_EN.jpg)

Further, the German BSI will use the eID simulator within their institution for future developments and prototypical implementations of new security protocols. Upgrading existing security protocols and evaluating new and stronger protocols for use with physical chip cards is a very time-consuming and costly process. It requires the involvement of several external parties, including manufacturers of semiconductors, COS, and chip cards as well as application developers. These restrictions do not apply when using a software-based simulator, because the protocol under test can be directly accessed. After changes have been made, the protocol is executable through a simple compilation of source code. 

The PersoSim project not only provides an open-source, software-based eID simulator (nPA) but also aims to build a developer community to further enhance the simulator. 

All PersoSim components can be downloaded in chapter [Downloads](https://persosim.github.io/#vorgehensweise-zur-installation). In addition, the source code for the eID simulator and the virtual drivers are available on the github platform [https://github.com/persosim.](https://github.com/persosim). 

Further information in English can be found by clicking the following link [PersoSim – Simulator of the German ID card (The Vault, S. 24-27, 2014)](https://persosim.github.io/docs/The_Vault_14_2014.pdf) by Tobias Senger (BSI), Holger Funke (secunet), Anke Larkworthy (independent consultant), published in The Vault magazine, June 2014.
