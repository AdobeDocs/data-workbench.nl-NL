---
description: Identificeer minimumvereisten en aanbevelingen voor de servercomponenten van de Werkbank van Gegevens (vroeger [!DNL Inzicht]) alvorens uw systeem te plannen en uit te voeren.
title: Serversysteemvereisten
uuid: c4487c76-03b9-4755-893b-555d451b1e69
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Serversysteemvereisten{#server-system-requirements}

Identificeer minimumeisen en aanbevelingen voor de servercomponenten van de Werkbank van Gegevens alvorens uw systeem te plannen en uit te voeren.

## DPU-vereisten{#dpu-requirements}

De server Gegevensverwerkingseenheid (DPU) is de belangrijkste component van de gegevensverwerking van de Werkbank van Gegevens. Het let op netwerkverbindingen van de Werkbank van Gegevens, leest ruwe brongegevens van de Eenheid van de Server van het Dossier (FSU) en gebruikt wezenlijke computer en opslagmiddelen.

### Capaciteit onder licentie {#section-71850e13783443798b3df9eb22cc63dc}

Gelieve te verwijzen naar de Beschrijving van de Diensten in de Overeenkomst *van de Dienst van[!DNL Data Workbench (Insight)]Adobe* voor de informatie van de vergunningscapaciteit.

>[!NOTE]
>
>Voor de Bescherming *van het Eindpunt van het Centrum van het Systeem van* MS in Vensters 2012 Servers, moeten deze uitvoerbare voorwerpen aan de ***Uitgesloten Processen worden toegevoegd:*** >
>* [!DNL InsightServer64.exe]
>* [!DNL ReportServer.exe]
>* [!DNL ExportIntegration.exe]
>



### De Aanbevelingen en de Vereisten van het Systeem DPU {#section-ae30555959bf4a309c76d0fd597b5162}

Adobe verstrekt aanbevelingen betreffende een ontwerp van de Werkbank van Gegevens dat aan uw bedrijfsbehoeften voldoet. Nochtans, zijn de volgende richtlijnen nuttig wanneer het selecteren van het werkende systeem (OS) en de hardware, omdat de geoptimaliseerde aard van de software DPU specifieke vereisten op het OS/hardwareplatform plaatst.

Als één enkele dataset door de capaciteit of de snelheid van één enkele DPU wordt beperkt, kunt u hen groeperen. Bijvoorbeeld, veronderstel u drie vergunning gegeven exemplaren van de software hebt DPU die samen wordt gebruikt om een grotere dataset sneller in werking te stellen. Aangezien de gegevens gelijkmatig over de machines worden verdeeld, wordt de gelicentieerde capaciteit van de dataset met drie vermenigvuldigd. Bovendien wordt de verwerkingssnelheid per rij drie keer sneller dan één enkele DPU.

Om de beste prestaties van uw investering te bereiken DPU, adviseert Adobe de volgende krachtige componenten die in de volgende lijst worden beschreven:

<table id="table_DA0A60CFBA7D4EF98B5ED5A3D8D6777B"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> </th> 
   <th colname="col2" class="entry"> Vereist </th> 
   <th colname="col3" class="entry"> Aanbevolen </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Besturingssysteem </p> </td> 
   <td colname="col2"> <p>Microsoft Windows Server 2008 x64 </p> </td> 
   <td colname="col3"> <p>Microsoft Windows Server 2012 x64 </p> <p> Microsoft Windows Server 2016 x64 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>CPU </p> </td> 
   <td colname="col2"> <p>Zie aanbevelingen. </p> </td> 
   <td colname="col3"> De nieuwste generatie 4-core+ processors van Intel of AMD worden aanbevolen. Voor optimale prestaties, 8 kernen; voor een afweging tussen snelheid en kosten worden vier kernen aanbevolen. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>RAM </p> </td> 
   <td colname="col2"> <p>8 GB </p> </td> 
   <td colname="col3"> <p>12 GB </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Opslag van werkgegevens </p> </td> 
   <td colname="col2"> <p>1 TB+ aan totale logische tijdelijke opslag. </p> <p>Lage latentietoegang tot het subsysteem "Schijf" </p> </td> 
   <td colname="col3"> <p>Voor tijdelijke opslag adviseert Adobe één van beiden: </p> 
    <ul id="ul_F3D033B90CF94F44A2A773B3F6852283"> 
     <li id="li_B902CF7CC6A44F02838B285ADC725A75">(4 tot 8) * (750 GB of hoger) SATA HDD's (3,5-inch spindle.) </li> 
     <li id="li_A378F4E1443F4BB2B54DC7E8372EE572">(6 tot 10) * (300 GB of hoger) SATA HDD's (2,5-inch spindle.) </li> 
    </ul> <p>Deze zouden in een serie moeten worden gevormd JBOD. Als de brutoschijfcapaciteit meer dan 2 TB bedraagt, kan ook een array van 2-disk RAID1-volumes worden gebruikt. Configureer bijvoorbeeld zes schijven als een RAID 1-paar van 3*(2*750 GB.) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Systeemgegevensopslag </p> </td> 
   <td colname="col2"> <p>Bovendien, vereist Adobe high-availability opslag van een bescheiden grootte (20 GB) voor OS, de software DPU, en andere systeemsoftware. </p> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Clusterhardware </p> </td> 
   <td colname="col2"> <p>Zie aanbevelingen. </p> </td> 
   <td colname="col3"> <p>Gebruik een homogene set servers. In een cluster DPU, vermindert de langzaamste server de prestaties van de gehele dataset. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Netwerkprestaties groeperen </td> 
   <td colname="col2"> Een geschakeld-gigabit verbinding Ethernet of groter. </td> 
   <td colname="col3"> </td> 
  </tr> 
 </tbody> 
</table>

### Alternatieve schijfsubsystemen {#section-6f984eabe8074759aa9deaf17e3a68b7}

Wanneer het overwegen van alternatieve schijfsubsystemen voor tijdelijke opslag, overweeg de volgende factoren en de richtlijnen:

* DPU eist ongebruikelijk van een krachtig schijfsysteem, zodat kan de vestiging van een ontoereikend schijfsubsysteem prestatiesknelpunten veroorzaken.
* De software DPU doet zijn eigen prestatiegerichte gegevens striping over een reeks schijven JBOD. Gebruik RAID niet om de snelheid te verhogen.
* Adobe adviseert dat DPU 400+ MB/s gezamenlijke duurzame bandbreedte aan de schijven heeft.
* De gemiddelde leesgrootte is zeer hoog (2 MB+). Om deze reden presteren 15K of 10K SAS schijven vaak iets beter (of slechter) dan SATA schijven tegen een aanzienlijke prijs en capaciteitsboete.
* Vermijd het gebruik van een SAN-architectuur. De ervaring leert dat de kosten om een SAN op de vereiste niveaus te laten presteren meestal extreem hoog zijn.
* Het lokale schijfsubsysteem wordt gebruikt als krasruimte-geen gegeven wordt permanent verloren van een mislukking van HDD, zodat denk na vermijdend dure, langzamere, high-availability systemen.

### Snelheidsoverwegingen {#section-01330be232894e08a526d8d82b7c4eb2}

Adobe kan geen garantie of geen vertegenwoordiging betreffende de snelheid verstrekken waarbij het gegeven door een gevormde Werkbank van Gegevens wordt verwerkt, omdat een verscheidenheid van factoren de snelheid van de gegevensverwerking, met inbegrip van maar niet beperkt tot het volgende beïnvloeden:

* Aantal rijen gegevens
* Aantal afmetingen (kolommen) van de gegevens
* Aantal en complexiteit van aangepaste verwerkingsstappen
* Gebruik van clustering
* Snelheid van de hardware

## Eisen voor bestandsservereenheden{#file-server-unit-requirements}

De FSU (File Serving Unit) van de server is de belangrijkste component voor gegevensopslag en -beheer van de Data Workbench. FSU doet dienst als dossierserver voor ruwe brongegevens aan DPU, en coördineert, waar aangewezen, het groeperen van DPUs. Elke FSU heeft een vergunning om brongegevens te verstrekken tot vijf (5) DPU&#39;s.

<table id="table_45CF36583DFE4536BB31F6A1F6CC181E"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> FSU-componenten </th> 
   <th colname="col2" class="entry"> Aanbevelingen </th> 
   <th colname="col3" class="entry"> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Besturingssysteem, CPU, RAM </p> </td> 
   <td colname="col2"> <p>Deze vereisten zijn dezelfde als die van de DPU. Nochtans, voor FSU, adviseert Adobe gebruikend de minimumvereisten eerder dan het volgen van de aanbevelingen. </p> </td> 
   <td colname="col3"> </td>
  </tr> 
  <tr> 
   <td colname="col1"> <p>Schijfsysteem </p> <p>De FSU vereist hoogst beschikbare, overtollige opslag voor grote volumes van gegevens. Adobe zal met u werken om uw nauwkeurige vereisten te bepalen. </p> </td> 
   <td colname="col1"> <p>Adobe adviseert: </p> 
    <ul id="ul_FFEEE5052FFD4876BA9A6476DD096539"> 
     <li id="li_F98750D509D640C68885D53FC691ED43">(12 of meer) * (750 GB of meer) SATA-harde schijven in een RAID 5/6-configuratie. </li> 
     <li id="li_3F84F63F9541476987015C27FDE8251B">Krachtige SAN-verbinding met ondersteuning voor een duurzame bandbreedte van 100 MB/s+. </li> 
    </ul> <p>Aangezien FSU de ruwe brongegevens houdt, zou om het even welk verlies niet terugwinbaar zijn, en Adobe stelt voor regelmatig het steunen van deze gegevens voor. </p> </td> 
   <td colname="col2"> </td>
  </tr> 
  <tr> 
   <td colname="col1"> <p>Netwerkprestaties </p> </td> 
   <td colname="col2"> <p>Adobe vereist de verbindingen van geschakeld-gigabitEthernet tussen FSUs en DPUs die samenwerken. </p> </td> 
   <td colname="col3"> </td>
  </tr> 
 </tbody> 
</table>

## Sensorvereisten{#sensor-requirements}

De Sensor van de Werkbank van gegevens verzamelt gebeurtenisgegevens van Web, toepassing, en de servers van de gegevensinzameling die aan om het even welke server moeten worden overgebracht. [!DNL Sensor’s] de instrumentatie verzekert constant nauwkeurige meting van gebeurtenissen die in uw kanaal van Internet voorkomen. [!DNL Sensor] steunt vele combinaties van de serversoftware van het Web en werkend systeem.

### Aanbevelingen voor sensorsysteem {#section-0a981c3a47b644c1a1a56974ba033b9c}

De volgende lijst beschrijft systeemaanbevelingen voor [!DNL Sensor]:

<table id="table_A132E06D6B8146C1B199B82464EA0898"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Kenmerken </th> 
   <th colname="col2" class="entry"> Aanbevolen </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Schijfopslag </p> </td> 
   <td colname="col2"> <p>Minimaal 512 MB. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>RAM </p> </td> 
   <td colname="col2"> <p>32 MB van RAM moet aan <span class="wintitle"> Sensor </span> op HTTP of andere servercomputer beschikbaar zijn die zijn gastheer is. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Netwerkprestaties </p> </td> 
   <td colname="col2"> <p>1 Mbps of grotere netwerkverbinding aan een repeaterserver of een server van de <span class="keyword"> gegevenswerkbank </span>. <span class="wintitle"> De sensor </span> verbruikt typisch veel minder bandbreedte dan één (1) Mbps. Uw adviseurs van Adobe zullen u helpen de daadwerkelijke hoeveelheid bandbreedte schatten die op een routinebasis zou worden vereist. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Netwerkpoorten en firewalls </p> </td> 
   <td colname="col2"> <p> <span class="wintitle"> De sensor </span> verbindt met de server van de <span class="keyword"> gegevenswerkbank </span> gebruikend HTTPS (typisch haven 443, hoewel dit configureerbaar is) of HTTP (typisch haven 80, hoewel dit configureerbaar is). </p> <p>De aangewezen haven op om het even welke firewall die tussen een <span class="wintitle"> Sensor </span> en de server van de doelgegevenswerkbank <span class="keyword"> of de repeaterserver verblijft zou slechts tussen de respectieve </span> Sensor die <span class="wintitle"> computer en de server van de </span> gegevenswerkbank <span class="keyword"> of de repeaterserver alvorens met het de installatieproces van de </span> Sensor te beginnen <span class="wintitle"> </span> ontvangt moeten worden geopend. <span class="wintitle"> De sensor </span> maakt een uni-directionele verbinding HTTPS of van HTTP aan een server van de <span class="keyword"> gegevenswerkbank </span> of repeaterserver. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Netwerkbeheersystemen </p> </td> 
   <td colname="col2"> <p>De bestaande netwerkbeheersystemen zouden de gezondheid van de onderliggende computerhardware (bijvoorbeeld, schijfruimte, netwerkdienst) en netwerkconnectiviteit evenals het Logboek van de Gebeurtenis van Vensters of de syslog van UNIX moeten controleren. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Servertijdsynchronisatie </p> </td> 
   <td colname="col2"> <p>Zorg ervoor dat de tijd van het computersysteem onophoudelijk over elke computer wordt gesynchroniseerd die gastheren een <span class="wintitle"> Sensor </span>. De de servertoepassingen en computers van het Web die door de <span class="wintitle"> Sensor worden gecontroleerd </span> moeten gesynchroniseerde systeemtijden voor de gebeurtenisgegevens hebben die van hen worden verzameld om nauwkeurig te zijn. Gelieve te verwijzen naar de documentatie van uw werkend systeem voor stappen om systeemtijden op een aan de gang zijnde basis met NTP of andere dergelijke faciliteit van de tijdsynchronisatie te synchroniseren. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>DNS-naamgebruik </p> </td> 
   <td colname="col2"> <p>Adobe adviseert dat de <span class="wintitle"> Sensoren een DNS naam (in plaats van een IP adres) </span> gebruiken om het netwerkadres van een server van de <span class="keyword"> gegevenswerkbank </span> of een repeaterserver op te lossen. Wanneer een <span class="wintitle"> Sensor een DNS naam </span> gebruikt, moet DNS van het server van het gastheerWeb of het lokale gastheerdossier worden gevormd om de naam van de server van de <span class="keyword"> gegevenswerkbank </span> of repeaterserver op te lossen. </p> </td> 
  </tr> 
 </tbody> 
</table>

### Support Server-software {#section-d6071706539f49d9a861d87b98e6f382}

De volgende lijst maakt een lijst van de gemeenschappelijkste combinaties die [!DNL Sensor] steunt:

<table id="table_99EA23BBC1A148B49643F4B5E4341C08"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Webserversoftware </th> 
   <th colname="col2" class="entry"> Besturingssysteem </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Apache Server / IBM HTTP Server 2.2 </p> </td> 
   <td colname="col2"> <p>Microsoft Windows Server 2003 of hoger; RedHat Enterprise Linux 6.x of hoger; Sun Solaris 8.x of hoger; IBM AIX 5.1x of hoger. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Apache Server 2.4 </p> </td> 
   <td colname="col2"> <p>RedHat Enterprise Linux 6.x of hoger </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Microsoft IIS </p> </td> 
   <td colname="col2"> <p>Microsoft Windows Server 2003 of hoger </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Java Application Servers (Tomcat, JBoss, iPlanet, Weblogic) </p> </td> 
   <td colname="col2"> <p>Microsoft Windows Server 2003 of hoger; RedHat Enterprise Linux 6.x of hoger; Sun Solaris 8.x of hoger; IBM AIX 5.1x of hoger. </p> </td> 
  </tr> 
 </tbody> 
</table>

Voor andere server en werkende systeemcombinaties, te raadplegen gelieve Adobe betreffende beschikbaarheid. Niet zijn alle eigenschappen van [!DNL Sensor] beschikbaar met alle combinaties van Web/toepassingsserver en werkend systeem. Voor meer informatie over bepaalde [!DNL Sensor] versies, te contacteren gelieve de Steun van Adobe.

## Vereisten voor rapportserver{#report-server-requirements}

De server van het werkbankrapport van gegevens is de component die de output van geplande rapportering toestaat. De rapporten die output zijn kunnen of in de vorm van .PNG beelden of .XLS spreadsheten zijn die in een dossiersysteem worden geplaatst, of als e-mails zijn. Zijn hardwarevereisten zijn identiek aan de Cliënt van de Werkbank van [Gegevens](https://docs.adobe.com/content/help/en/data-workbench/using/install/c-data-workbench-client-install.html).

De volgende eisen gelden voor [!DNL report server]:

* Toegang tot het dossiersysteem voor output van gegevens (netwerkaandeel, of lokale aandrijving).
* Toegang tot de gevormde server SMTP.
* Microsoft Excel 2003 of hoger geïnstalleerd op de [!DNL report] server. Zie [Overwegingen voor server-zijAutomatisering van Bureau](http://support.microsoft.com/kb/257757) voor extra informatie.

## Netwerkbeheer{#network-management}

Adobe adviseert dat de bestaande systemen van het netwerkbeheer de hardware en het netwerk controleren dat het platform van de Werkbank van Gegevens zich op baseert.

Bovendien adviseert Adobe controle van de de gebeurtenislogboeken van Vensters van FSUs en DPUs, die worden geschreven aan wanneer een fout voorkomt.

>[!NOTE]
>
>Om het even welk netwerk opslagsysteem dat logboekdossiers ontvangt moet minstens 10MB per DPU van duurzame bandbreedte verstrekken.

## Beschikbaarheid van gegevens{#data-availability}

Het is een normale en vereiste praktijk voor een serverDPU om gegevens in nieuwe of verfrisste dataset te verwerken en te herverwerken.

Dit kan wegens configuratieveranderingen, gegevensbronveranderingen, hardwareveranderingen, ongepaste configuratie, hardwaremislukking, softwaremislukking, machtsmislukking, etc. voorkomen. Wanneer een dergelijke verwerking of herverwerking plaatsvindt, moeten alle gegevensreeksen en systeemgegevens onmiddellijk beschikbaar zijn voor de DPU- en FSU-componenten. Wanneer niet aan deze eis wordt voldaan, kan dit leiden tot een aanzienlijke en onnodige vertraging van het systeem.

## De Kwesties van het Netwerk van DPU en van FSU{#dpu-and-fsu-network-issues}

Overwegingen om in mening te houden wanneer het werken met netwerken DPU en FSU.

* Voor de netwerkgebonden distributie van het logboekdossier, moet om het even welk genetwerkt opslagsysteem dat logboekdossiers ontvangt minstens 10MB per DPU van duurzame bandbreedte verstrekken.
* DPU, FSU, en de Werkbank van Gegevens communiceren bidirectioneel via HTTP of HTTPS op haven 80 of 443 (door gebrek; de havens kunnen alternatief worden gevormd).
* De werkbank van gegevens [!DNL Sensor(s)] moet (éénweg) met de servers kunnen verbinden.
* Om DPU toe te staan om waakzame berichten via SMTP te verzenden, moet het de gevormde server kunnen contacteren SMTP.
* Adobe adviseert dat FSUs en DPUs netwerknamen zoals FSU01.CLIENT.COM worden gegeven om aanpassing te vermijden als het geval van een IP-adres verandert.