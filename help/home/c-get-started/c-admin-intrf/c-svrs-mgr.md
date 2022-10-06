---
description: Het belangrijkste hulpmiddel dat door systeembeheerders wordt gebruikt is de Manager van Servers.
title: Serverbeheer
uuid: 96c8f060-ffd4-46b9-b039-b2ac024400b6
exl-id: e8b22d9f-3f1b-4a97-942a-85786bd3c547
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '648'
ht-degree: 1%

---

# Serverbeheer{#servers-manager}

{{eol}}

Het belangrijkste hulpmiddel dat door systeembeheerders wordt gebruikt is de Manager van Servers.

Het is de belangrijkste interface voor het bepalen van algemene systeemstatus en voor het uitvoeren van systeemconfiguratie, dossierbeheer, en fout controlefuncties.

De Manager van Servers toont een gekleurd punt (knoop) voor elke server van de Data Workbench en [!DNL Sensor] in uw systeem en biedt in één oogopslag de systeemstatus voor elke installatie. Het toont ook een knoop voor uw Data Workbench installatie.

Groene knooppunten vertegenwoordigen actieve verbindingen, rode knooppunten vertegenwoordigen verbindingen die zijn uitgeschakeld of anderszins niet toegankelijk, en grijze knooppunten vertegenwoordigen verbindingen waarvan de toestand onbepaald is.

![](assets/vis_SysStat_RedGreenDots.png)

Als u met de rechtermuisknop op een knooppunt klikt, wordt informatie over de verbindingscomponent weergegeven en hebt u toegang tot verwante menu&#39;s.

In de volgende tabellen wordt de informatie beschreven die wordt verschaft wanneer u met de rechtermuisknop op een knooppunt voor Data Workbench, Data Workbench-server (inclusief een master Data Workbench-server in een cluster) klikt, of [!DNL Sensor].

<table id="table_C459CAAB07D34144B5BFFCCC84C2BB37"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Item </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Product </p> </td> 
   <td colname="col2"> <p>Productnaam, versie en buildnummer. </p> <p>Voorbeeld: Data Workbench 5.3 (00000001) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Adres </p> </td> 
   <td colname="col2"> <p>IP adres van de computer van de Data Workbench. </p> <p>Voorbeeld: 100.0.0.1 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Configureren </p> </td> 
   <td colname="col2"> <p>Een koppeling naar uw <span class="keyword"> Data Workbench </span> configuratiebestand. Klikken <span class="uicontrol"> Configureren </span> &gt; <span class="uicontrol"> Insight.cfg </span> om het de configuratievenster van de Data Workbench te tonen. Alle wijzigingen die u aanbrengt en opslaat in dit venster, worden weerspiegeld in het dialoogvenster <span class="filepath"> Insight.cfg </span> in de installatiemap van de Data Workbench. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Product </p> </td> 
   <td colname="col2"> <p>Productnaam, versie en buildnummer. </p> <p>Voorbeeld: Data Workbench server 5.3 (00000001) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>GN </p> </td> 
   <td colname="col2"> <p>De algemene naam van de servercomputer van de Data Workbench. </p> <p>Voorbeeld: <span class="filepath"> mijnserver1.mijnbedrijf.nl </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Adres </p> </td> 
   <td colname="col2"> <p>IP adres of volledig - gekwalificeerde domeinnaam van de server zoals die in het dossier van Adressen op de computer en de parameter van de Plaats van het Netwerk in wordt gevormd <span class="filepath"> Insight.cfg </span> bestand. </p> <p>Voorbeeld: 100.0.0.1 </p> <p>Voor informatie over het dossier van Adressen, zie <i>Handleiding voor installatie en beheer van serverproducten</i>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Status </p> </td> 
   <td colname="col2"> <p>Huidige status van de server van de Data Workbench. Dit gebied toont O.K. wanneer de server van de Data Workbench normaal loopt. Als er een fout is opgetreden en het serverknooppunt van de Data Workbench rood is, wordt de fout in het veld weergegeven (bijvoorbeeld "403 Verboden"). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Gedetailleerde status </p> </td> 
   <td colname="col2"> <p>Een koppeling naar de <span class="keyword"> Data Workbench-server </span> <span class="wintitle"> Gedetailleerde status </span> interface, die voor het oplossen van problemenfouten of andere kwesties met de server van de Data Workbench nuttig is. </p> <p>Zie voor meer informatie <a href="../../../home/c-get-started/c-admin-intrf/c-det-stat-interf.md"> De gedetailleerde statusinterface</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Extern bureaublad </p> </td> 
   <td colname="col2"> <p>Hiermee opent u een <span class="wintitle"> Extern bureaublad </span> sessie naar de servercomputer van de Data Workbench. </p> <p>Zie voor meer informatie <a href="../../../home/c-get-started/c-admin-intrf/t-rmt-dsktp-opt.md#task-dc0bdb4630474a17af67b931bc22d9ef"> De optie Extern bureaublad </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Serverbestanden </p> </td> 
   <td colname="col2"> <p>Een koppeling naar de <span class="wintitle"> Serverbestandsbeheer </span>, die de mappen en bestanden in de installatiemap van de Data Workbench-server weergeeft. </p> <p>Zie voor meer informatie <a href="../../../home/c-get-started/c-admin-intrf/c-svr-files-mgr.md#concept-73a0808487c8424285ae7302f53bc5f4"> Serverbestandsbeheer </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Servercontrole </p> </td> 
   <td colname="col2"> <p>Een koppeling naar de <span class="wintitle"> Servercontrole </span> interface, die voor het oplossen van problemen of het volgen van prestatiesparameters nuttig is. </p> <p>Zie voor meer informatie <a href="../../../home/c-get-started/c-admin-intrf/c-svr-mtr-intfc.md#concept-3bea7441de20409585e63060d5489f45"> De interface van de Monitor van de Server </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Gerelateerde servers </p> </td> 
   <td colname="col2"> <p>Alleen voor Data Workbench-serverclusters. </p> <p>Een menu dat een lijst maakt van de algemene namen van de computers die in het master <span class="filepath"> *.address van de server van de Data Workbench </span> bestand. Deze lijst omvat gewoonlijk alle verwerking <span class="keyword"> Data Workbench-servers </span> in de cluster. Dit menu wordt alleen weergegeven als de Data Workbench een kopie van het master <span class="filepath"> *.address van de server van de Data Workbench </span> bestand. </p> <p>Wanneer u op <span class="uicontrol"> Gerelateerde servers </span>kunt u op een van de volgende opties klikken: 
     <ul id="ul_3B28B8579B1945FD80669EDFDFDA84A6"> 
      <li id="li_90094B46CB304C179136BB75FF0D6DBD"> <span class="uicontrol"> Lijst met servermonitoren </span>, die de <span class="wintitle"> Servercontrole </span> interface lijstdetails voor alle verwante servers </li> 
      <li id="li_CD6FF5BB52874ABCB536C2DE2376587A">De gemeenschappelijke naam van om het even welke server van de Data Workbench, die een contextmenu toont dat u toelaat om het even welke volgend voor die bepaalde server te openen: 
       <ul id="ul_928510D1DE68471583F2EE7547AEB824"> 
        <li id="li_8399338137354A59B9B4D24AF7EEE868"> <span class="uicontrol"> Gedetailleerde status </span>. Zie <a href="../../../home/c-get-started/c-admin-intrf/c-det-stat-interf.md"> De gedetailleerde statusinterface </a>. </li> 
        <li id="li_0FE569C56B3F4583BC1F3DF3B4F55765"> <span class="uicontrol"> Extern bureaublad </span>. Zie <a href="../../../home/c-get-started/c-admin-intrf/t-rmt-dsktp-opt.md#task-dc0bdb4630474a17af67b931bc22d9ef"> De optie Extern bureaublad </a>. </li> 
        <li id="li_2B6F8419CB5945C9B411F6A7C2C859FF"> <span class="uicontrol"> Serverbestandsbeheer </span>. Zie <a href="../../../home/c-get-started/c-admin-intrf/c-svr-files-mgr.md#concept-73a0808487c8424285ae7302f53bc5f4"> Serverbestandsbeheer </a>. </li> 
        <li id="li_F22F974EB4DE4F0F93623AE98C7DCEBC"> <span class="uicontrol"> Servercontrole </span>. Zie <a href="../../../home/c-get-started/c-admin-intrf/c-svr-mtr-intfc.md#concept-3bea7441de20409585e63060d5489f45"> De interface van de Monitor van de Server </a>. </li> 
       </ul> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

<table id="table_5BFA0AFE2D9A4337BF04343879DAD03B"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Item </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Product </p> </td> 
   <td colname="col2"> <p>Productnaam, versie en buildnummer. </p> <p>Voorbeeld: Sensor 3.76; J3,67 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>ID </p> </td> 
   <td colname="col2"> De <span class="wintitle"> Sensor </span> ID opgegeven in het dialoogvenster <span class="wintitle"> Sensor </span> configuratiebestand voor deze installatie. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>IP </p> </td> 
   <td colname="col2"> <p>IP-adres van de web- of toepassingsserver waarop <span class="wintitle"> Sensor </span> is geïnstalleerd. </p> <p>Voorbeeld: 100.0.0.1 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>PID </p> </td> 
   <td colname="col2"> <p>Proces-id toegewezen door het besturingssysteem. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>SSL </p> </td> 
   <td colname="col2"> <p>Of <span class="wintitle"> Sensor </span> en de server van de Data Workbench communiceert gebruikend SSL. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Tijd </p> </td> 
   <td colname="col2"> <p>Tijd (HH:MM:SS) dat de <span class="wintitle"> Sensor </span> voor het laatst een verbinding met de Data Workbench-server tot stand gebracht. </p> </td> 
  </tr> 
 </tbody> 
</table>
