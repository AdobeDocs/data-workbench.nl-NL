---
description: Identificeer minimumeisen en aanbevelingen voor Data Workbench (vroeger [!DNL Insight]) servercomponenten alvorens uw systeem te plannen en uit te voeren.
title: Serversysteemvereisten
uuid: c4487c76-03b9-4755-893b-555d451b1e69
exl-id: 6dd78331-8370-400e-b580-9b9bad13e62c
source-git-commit: 232117a8cacaecf8e5d7fcaccc5290d6297947e5
workflow-type: tm+mt
source-wordcount: '1683'
ht-degree: 0%

---

# Serversysteemvereisten{#server-system-requirements}

Identificeer minimumvereisten en aanbevelingen voor de servercomponenten van de Data Workbench alvorens uw systeem te plannen en uit te voeren.

## DPU-vereisten{#dpu-requirements}

De eenheid van de Gegevensverwerking van de server (DPU) is de belangrijkste component van de gegevensverwerking van Data Workbench. Het luistert naar netwerkverbindingen van Data Workbench, leest ruwe brongegevens van de Eenheid van de Server van het Dossier (FSU) en gebruikt aanzienlijke computer en opslagmiddelen.

### Gelicentieerde capaciteit {#section-71850e13783443798b3df9eb22cc63dc}

Raadpleeg de beschrijving van de services in de *Adobe [!DNL Data Workbench (Insight)] Serviceovereenkomst* voor informatie over licentiecapaciteit.

>[!NOTE]
>
>Voor *MS System Center Endpoint Protection* in Windows 2012 Servers moeten deze uitvoerbare bestanden worden toegevoegd aan de ***Uitgesloten processen:*** >
>* [!DNL InsightServer64.exe]
>* [!DNL ReportServer.exe]
>* [!DNL ExportIntegration.exe]

>


### DPU-systeem Recommendations en vereisten {#section-ae30555959bf4a309c76d0fd597b5162}

Adobe verstrekt aanbevelingen betreffende een ontwerp van de Data Workbench dat aan uw bedrijfsbehoeften voldoet. De volgende richtlijnen zijn echter handig wanneer u het besturingssysteem (OS) en de hardware selecteert, omdat door de geoptimaliseerde aard van de DPU-software specifieke vereisten op het besturingssysteem/hardwareplatform worden geplaatst.

Als één enkele dataset door de capaciteit of de snelheid van één enkele DPU wordt beperkt, kunt u hen groeperen. Bijvoorbeeld, veronderstel u drie vergunning gegeven exemplaren van de software DPU hebt die samen worden gebruikt om een grotere dataset sneller in werking te stellen. Aangezien de gegevens gelijkmatig over de machines worden verdeeld, wordt de in licentie gegeven capaciteit van de dataset met drie vermenigvuldigd. Bovendien wordt de verwerkingssnelheid per rij drie keer sneller dan één enkele DPU.

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
   <td colname="col3"> De nieuwste generatie 4-core+ processors van Intel of AMD worden aanbevolen. 8 cores voor optimale prestaties; voor een afweging tussen snelheid en kosten worden vier cores aanbevolen. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>RAM </p> </td> 
   <td colname="col2"> <p>8 GB </p> </td> 
   <td colname="col3"> <p>12 GB </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Opslag van werkgegevens </p> </td> 
   <td colname="col2"> <p>1 TB+ aan totale logische tijdelijke opslag. </p> <p>Toegang tot het schijfsubsysteem met lage latentie </p> </td> 
   <td colname="col3"> <p>Voor tijdelijke opslag beveelt Adobe aan: </p> 
    <ul id="ul_F3D033B90CF94F44A2A773B3F6852283"> 
     <li id="li_B902CF7CC6A44F02838B285ADC725A75">(4 tot 8) * (750 GB of hoger) SATA harde schijven (3,5-inch spindle.) </li> 
     <li id="li_A378F4E1443F4BB2B54DC7E8372EE572">(6 tot 10) * (300 GB of hoger) SATA harde schijven (2,5-inch spindle.) </li> 
    </ul> <p>Deze moeten in een JBOD-array worden geconfigureerd. Als de bruto-schijfcapaciteit groter is dan 2 TB, kan ook een array van RAID1-volumes met twee schijven worden gebruikt. Configureer bijvoorbeeld zes schijven als een RAID 1-paar van 3*(2*750 GB). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Systeemgegevensopslag </p> </td> 
   <td colname="col2"> <p>Bovendien vereist Adobe opslag met hoge beschikbaarheid van een bescheiden grootte (20 GB) voor het besturingssysteem, DPU-software en andere systeemsoftware. </p> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Clusterhardware </p> </td> 
   <td colname="col2"> <p>Zie aanbevelingen. </p> </td> 
   <td colname="col3"> <p>Gebruik een homogene set servers. In een cluster DPU, vermindert de langzaamste server de prestaties van de volledige dataset. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Netwerkprestaties groeperen </td> 
   <td colname="col2"> Een geschakeld-gigabitEthernet verbinding of groter. </td> 
   <td colname="col3"> </td> 
  </tr> 
 </tbody> 
</table>

### Alternatieve schijfsubsystemen {#section-6f984eabe8074759aa9deaf17e3a68b7}

Houd bij het overwegen van alternatieve schijfsubsystemen voor tijdelijke opslag rekening met de volgende factoren en richtlijnen:

* DPU is ongebruikelijk veeleisend van een krachtig schijfsysteem, zodat de vestiging van een ontoereikend schijfsubsysteem prestatiesknelpunten kan veroorzaken.
* De software DPU voert zijn eigen prestaties-georiënteerde gegevensstriping over een reeks schijven JBOD uit. Gebruik RAID niet om de snelheid te verhogen.
* Adobe adviseert dat DPU 400+ MB/s gezamenlijke aanhoudende bandbreedte aan de schijven heeft.
* De gemiddelde leesgrootte is zeer hoog (2 MB+). Daarom werken SAS-schijven (15.000 of 10.000 rpm) vaak iets beter (of slechter) dan SATA-schijven tegen een aanzienlijke prijs en een hoge capaciteit.
* Gebruik geen SAN-architectuur. De ervaring leert dat de kosten om een SAN op de vereiste niveaus te laten presteren doorgaans extreem zijn.
* Het lokale schijfsubsysteem wordt gebruikt als werkruimte. Er gaan geen gegevens verloren als gevolg van een HDD-fout. Vermijd dus kostbare, langzamere systemen met hoge beschikbaarheid.

### Snelheidsoverwegingen {#section-01330be232894e08a526d8d82b7c4eb2}

Adobe kan geen garantie of representatie bieden met betrekking tot de snelheid waarmee gegevens door een geconfigureerde Data Workbench worden verwerkt, omdat een verscheidenheid aan factoren van invloed is op de gegevensverwerkingssnelheid, waaronder maar niet beperkt tot het volgende:

* Aantal gegevensrijen
* Aantal afmetingen (kolommen) van gegevens
* Aantal en complexiteit van aangepaste verwerkingsstappen
* Gebruik van clustering
* Hardwaresnelheid

## Eisen voor bestandsservereenheden{#file-server-unit-requirements}

De FSU (File Serving Unit) van de server is de belangrijkste component voor gegevensopslag en -beheer van Data Workbench. FSU handelt als dossierserver voor ruwe brongegevens aan DPU, en, waar aangewezen, coördineert het groeperen van DPUs. Elke FSU heeft een licentie om brongegevens te leveren tot maximaal vijf (5) DPU&#39;s.

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
   <td colname="col2"> <p>Deze vereisten zijn dezelfde als die van de DPU. Voor de FSU beveelt Adobe echter aan de minimumeisen te gebruiken in plaats van de aanbevelingen te volgen. </p> </td> 
   <td colname="col3"> </td>
  </tr> 
  <tr> 
   <td colname="col1"> <p>Schijfsysteem </p> <p>De FSU vereist hoogst-beschikbare, overtollige opslag voor grote volumes van gegevens. Adobe zal met u samenwerken om uw nauwkeurige vereisten te bepalen. </p> </td> 
   <td colname="col1"> <p>Adobe beveelt aan: </p> 
    <ul id="ul_FFEEE5052FFD4876BA9A6476DD096539"> 
     <li id="li_F98750D509D640C68885D53FC691ED43">(12 of meer) * (750 GB of meer) SATA harde schijven in een RAID 5/6-configuratie. </li> 
     <li id="li_3F84F63F9541476987015C27FDE8251B">Krachtige SAN-verbinding met 100 MB/s+ aanhoudende bandbreedte. </li> 
    </ul> <p>Aangezien FSU de ruwe brongegevens houdt, zou om het even welk verlies onherstelbaar zijn, en Adobe adviseert om deze gegevens op regelmatige basis te steunen. </p> </td> 
   <td colname="col2"> </td>
  </tr> 
  <tr> 
   <td colname="col1"> <p>Netwerkprestaties </p> </td> 
   <td colname="col2"> <p>Adobe vereist geschakeld-gigabitEthernet verbindingen tussen FSUs en DPUs die samenwerken. </p> </td> 
   <td colname="col3"> </td>
  </tr> 
 </tbody> 
</table>

## Sensorvereisten{#sensor-requirements}

De Sensor van de Data Workbench verzamelt gebeurtenisgegevens van Web, toepassing, en servers van de gegevensinzameling die aan om het even welke server moeten worden overgebracht. [!DNL Sensor’s] De instrumentatie verzekert constant nauwkeurige meting van gebeurtenissen die in uw kanaal van Internet voorkomen. [!DNL Sensor] ondersteunt veel combinaties van webserversoftware en -besturingssysteem.

### Sensor System Recommendations {#section-0a981c3a47b644c1a1a56974ba033b9c}

In de volgende tabel worden de systeemaanbevelingen voor [!DNL Sensor] beschreven:

<table id="table_A132E06D6B8146C1B199B82464EA0898"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Functies </th> 
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
   <td colname="col2"> <p>32 MB RAM moet beschikbaar zijn voor <span class="wintitle"> Sensor </span> op de HTTP-server of andere servercomputer die de host is. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Netwerkprestaties </p> </td> 
   <td colname="col2"> <p>1 Mbps of meer netwerkverbinding met een herhalingsserver of <span class="keyword"> gegevenswerkbankserver </span>. <span class="wintitle"> De sensor verbruikt  </span> typisch veel minder bandbreedte dan één (1) Mbps. Uw Adobe consultants zullen u helpen de daadwerkelijke hoeveelheid bandbreedte te schatten die op routinebasis wordt vereist. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Netwerkpoorten en Firewalls </p> </td> 
   <td colname="col2"> <p> <span class="wintitle"> De sensor  </span> verbindt met de server van de  <span class="keyword"> gegevenswerkbank  </span> gebruikend HTTPS (typisch haven 443, hoewel dit configureerbaar is) of HTTP (typisch haven 80, hoewel dit configureerbaar is). </p> <p>De juiste poort op een firewall tussen een <span class="wintitle">-sensor </span> en de doelserver <span class="keyword"> voor gegevenswerkbank </span> of herhalingsserver mag alleen worden geopend tussen de respectieve <span class="wintitle">-sensor </span>-hostcomputer en de <span class="keyword">-gegevenswerkbench-server </span> of herhalingsserver voordat de <span class="wintitle">-sensor wordt gestart </span> installatieproces. <span class="wintitle"> Sensor  </span> maakt een uni-directionele HTTPS- of HTTP-verbinding met een  <span class="keyword"> gegevensworkbench-server  </span> of -repeaterserver. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Netwerkbeheersystemen </p> </td> 
   <td colname="col2"> <p>De bestaande systemen van het netwerkbeheer zouden de gezondheid van de onderliggende computerhardware (bijvoorbeeld, schijfruimte, netwerkdienst) en netwerkconnectiviteit evenals het Logboek van de Gebeurtenis van Vensters of de syslog van UNIX moeten controleren. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Tijdsynchronisatie van server </p> </td> 
   <td colname="col2"> <p>Zorg ervoor dat de systeemtijd van de computer voortdurend wordt gesynchroniseerd op elke computer waarop een <span class="wintitle">-sensor </span> wordt gehost. De de servertoepassingen en computers van het Web die door <span class="wintitle"> Sensor </span> worden gecontroleerd moeten gesynchroniseerde systeemtijden hebben voor de gebeurtenisgegevens die van hen worden verzameld nauwkeurig zijn. Raadpleeg de documentatie bij het besturingssysteem van uw besturingssysteem voor stappen om systeemtijden doorlopend te synchroniseren met NTP of een andere dergelijke tijdsynchronisatiefaciliteit. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>DNS-naamgebruik </p> </td> 
   <td colname="col2"> <p>Adobe raadt aan dat <span class="wintitle"> Sensors </span> een DNS-naam (in plaats van een IP-adres) gebruiken om het netwerkadres op te lossen van een <span class="keyword">-gegevenswerkbankserver </span> of een herhalingsserver. Wanneer een <span class="wintitle">-sensor </span> een DNS-naam gebruikt, moet het DNS- of lokale hostbestand van de hostwebserver worden geconfigureerd om de naam van de <span class="keyword">-gegevenswerkbankserver </span> of herhalingsserver op te lossen. </p> </td> 
  </tr> 
 </tbody> 
</table>

### Ondersteuningsserversoftware {#section-d6071706539f49d9a861d87b98e6f382}

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

Voor andere server- en besturingssysteemcombinaties raadpleegt u Adobe over de beschikbaarheid. Niet alle functies van [!DNL Sensor] zijn beschikbaar bij alle combinaties van web/toepassingsserver en besturingssysteem. Voor meer informatie over bepaalde [!DNL Sensor] versies, gelieve te contacteren de Steun van Adobe.

## Vereisten rapportserver{#report-server-requirements}

De server van het het werkbankrapport van gegevens is de component die de output van geplande rapportering toestaat. De uitvoerrapporten kunnen de vorm hebben van .PNG-afbeeldingen of .XLS-spreadsheets die in een bestandssysteem zijn geplaatst, of als e-mailberichten. Zijn hardwarevereisten zijn identiek aan [Data Workbench Cliënt](https://experienceleague.adobe.com/docs/data-workbench/using/install/c-data-workbench-client-install.html).

De volgende vereisten gelden voor [!DNL report server]:

* Toegang tot het bestandssysteem voor de uitvoer van gegevens (delen van netwerk of lokaal station).
* Toegang tot de geconfigureerde SMTP-server.
* Microsoft Excel 2003 of hoger geïnstalleerd op [!DNL report]-server. Zie [Overwegingen voor server-zijAutomatisering van Bureau](http://support.microsoft.com/kb/257757) voor extra informatie.

## Netwerkbeheer{#network-management}

Adobe raadt aan dat bestaande netwerkbeheersystemen de hardware en het netwerk controleren waarop het Data Workbench-platform steunt.

Bovendien adviseert Adobe controle van de de gebeurtenislogboeken van Vensters van FSUs en DPUs, die worden geschreven aan wanneer een fout voorkomt.

>[!NOTE]
>
>Elk netwerkopslagsysteem dat logboekbestanden host, moet ten minste 10 MB aan blijvende bandbreedte per DPU bieden.

## Beschikbaarheid van gegevens{#data-availability}

Het is een normale en vereiste praktijk voor serverDPU om gegevens in nieuwe of vernieuwde dataset te verwerken en opnieuw te verwerken.

Dit kan voorkomen wegens configuratieveranderingen, gegevensbronveranderingen, hardwareveranderingen, ongepaste configuratie, hardwaremislukking, softwaremislukking, machtsmislukking, etc. Wanneer dergelijke verwerking of herverwerking plaatsvindt, moeten alle dataset en systeemgegevens onmiddellijk beschikbaar zijn voor de DPU- en FSU-componenten. Wanneer deze eis niet wordt nageleefd, kan dit leiden tot aanzienlijke en onnodige vertraging van het systeem.

## DPU- en FSU-netwerkproblemen{#dpu-and-fsu-network-issues}

Overwegingen in mening te houden wanneer het werken met netwerken DPU en FSU.

* Voor netwerkdistributie van logbestanden moet elk netwerkopslagsysteem dat logboekbestanden host, ten minste 10 MB aan continue bandbreedte per DPU bieden.
* DPU, FSU, en de Data Workbench communiceren bidirectioneel via HTTP of HTTPS op haven 80 of 443 (door gebrek; de havens kunnen alternatief worden gevormd).
* Data Workbench [!DNL Sensor(s)] moet in staat zijn (eenrichtingsverkeer) verbinding te maken met de servers.
* Om DPU toe te staan om waakzame berichten via SMTP te verzenden, moet het de gevormde server kunnen contacteren SMTP.
* Adobe adviseert dat FSUs en DPUs netwerknamen zoals FSU01.CLIENT.COM worden gegeven om herconfiguratie te vermijden als het geval van een IP-adres verandert.
