---
description: De sensor laat u toe om de gegevens van het Webverzoek (gebeurtenis of logboekgegevens) evenals uitgebreide metingsgegevens te verwerven.
solution: Analytics
title: Wat voor soort gegevens kan ik verkrijgen?
topic: Data workbench
uuid: 5ac864b8-4017-4d80-b491-7a5976225eb2
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Wat voor soort gegevens kan ik verkrijgen?{#what-kind-of-data-can-i-acquire}

De sensor laat u toe om de gegevens van het Webverzoek (gebeurtenis of logboekgegevens) evenals uitgebreide metingsgegevens te verwerven.

De uitgebreide metingsgegevens zijn niet beschikbaar aan uw Webservers als deel van hun normale verrichting.

De volgende onderwerpen worden beschreven:

## Webaanvraaggegevens {#section-a28217e8a8c047eb9b1c0ca1f67c832f}

[!DNL Sensor] maakt het mogelijk om gegevens van het Webverzoek (gebeurtenis of logboekgegevens) automatisch te verkrijgen en te vervoeren naar een centrale plaats voor opslag en verwerking voor analyse. Tenzij u specifiek verkiest om bepaalde soorten verzoeken uit te filtreren en geen gegevens over die verzoektypes te verzamelen, vangt [!DNL Sensor] gegevens over alle GET verzoeken die van de Webservers worden gemaakt waarop het geïnstalleerd is.

[!DNL Sensor] automatiseert dit proces van gegevensverwerving voor alle GET verzoeken die op uw servers worden gedaan en heeft significante bedrijfs en technische voordelen over alternatieve methodes om de gegevens van het websiteverzoek te verwerven. Deze voordelen omvatten het volgende:

* De verzoeken die voor analyse en rapportering onnodig zijn kunnen worden gefilterd uit alvorens u kosten voor hun aankoop, vervoer, opslag, en verwerking oploopt.
* De beheerders van de plaats moeten niet logboekdossiers in partij, of manueel of via manuscript roteren.
* [!DNL Sensor] voegt logboekdossiers bij een centrale plaats samen om gemakkelijke toegang voor verwerking toe te staan.
* [!DNL Sensor] organiseert en slaat logboekdossiers in een gemeenschappelijk gegeven-bewarend formaat op, verwijderend de behoefte om hen voor te verwerken alvorens zij voor analyse en rapporteringsdoeleinden kunnen worden gebruikt.
* De instanties van bepaalde inhoudstypes kunnen in de logboekdossiers worden omvat alhoewel de meeste verzoeken om een bepaald inhoudstype automatisch uit worden gefiltreerd.
* [!DNL Sensor] comprimeert de ingangen van het logboekdossier, die beduidend minder opslagruimte vereisen, die kosten drukken en de gegevens toelaten om voor analyse voor langere periodes beschikbaar worden gehouden.
* [!DNL Sensor’s] de fouten verdraagzame eigenschappen staan systeem en netwerkfouten toe terwijl nog het verzekeren van de levering van de logboekgegevens aan een centrale bewaarplaats.
* [!DNL Sensor] maakt de uitvoering van gecontroleerde experimenten met webinhoud, -processen en -marketingcampagnes mogelijk.
* [!DNL Sensor] tijdstempels logingangen in eenheden van 100ns, die nieuwe types van analytische functionaliteit toestaan.
* [!DNL Sensor] stelt eigenaars van sites in staat om gegevens (metingen) toe te voegen aan de logboekitems na de eerste implementatie, zodat ze deze kunnen analyseren en rapporteren.

Voor meer informatie over het verwerven van uitgebreide meetgegevens, zie het [Verkrijgen van de Metingen](../../home/c-undst-pg-tag/c-acq-bsln-msmts/c-acq-bsln-msmts.md#concept-ed9b4b21693a4bafac75d60708b9b6fe)van de Basislijn.

## Uitgebreide meetgegevens {#section-b7f0285de49e432b9db8fda85fa735ba}

[!DNL Sensor] ondersteunt ook het gebruik van paginatags (of ingesloten objectverzoeken) om meetgegevens te verzamelen die niet beschikbaar zijn voor uw webservers als onderdeel van hun normale werking. De markeringen van de pagina worden algemeen gebruikt om te meten:

* Het bekijken van een logische pagina in een dynamische website.
* Het bekijken van inhoud of advertenties op een derde gecontroleerde website.
* Het bekijken van inhoud die van een browser geheim voorgeheugen of CDN wordt gediend.
* Gedetailleerde informatie over de browser van een bezoeker, inclusief metingen zoals laadtijd van pagina&#39;s, schermresolutie, welke formuliervelden de bezoeker heeft ingevuld, enzovoort.
* Andere gegevens die niet anders door browsers naar uw Webservers worden verzonden.

[!DNL Sensor] verzamelt om het even welke informatie die in om het even welk GET verzoek wordt geplaatst dat aan een Webserver wordt ingediend die loopt [!DNL Sensor]. Dergelijke verzoeken kunnen van om het even welke soort ingebedde objecten verzoeken komen, hetzij om eenvoudig te meten dat het verzoek op een bepaald tijdstip door een bepaalde browser werd gedaan of om andere meetgegevens in de stroom van de gegevensverzameling over te brengen zodat het voor analyse en rapporteringsdoeleinden kan worden verwerkt.

[!DNL Sensor] verstrekt het beste van zowel cliënt-kant als server-zijgegevensaanwinst werelden-het verwerft uw server-zijgegevens van het Weblogboek en verzamelt cliënt-kant, derdeplaats, of geheim voorgeheugen-opwindende metingen die door ingebedde objecten verzoeken worden genomen. Met andere woorden, [!DNL Sensor] verwerft zowel de verzoekgegevens die normaal aan uw Webservers (server-zijmetingen) worden bekend als om het even welke extra metingsgegevens die u door het gebruik van paginabags (cliënt-zijmetingen) verzamelt die hun gegevens naar om het even welke Webservers verzenden die lopen [!DNL Sensor]. Dergelijke Webservers kunnen aan het verzamelen van cliënt-zijmetingen worden gewijd maar zijn niet vereist om te zijn.

Voor meer informatie over het verwerven van uitgebreide meetgegevens, zie het [Verkrijgen van Uitgebreide Metingen](../../home/c-undst-pg-tag/c-acq-ext-msmt/c-acq-ext-msmt.md#concept-d171a6d2bde843cdb65bcfe69c6a4944).
