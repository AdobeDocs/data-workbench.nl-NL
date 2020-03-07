---
description: Het primaire hulpmiddel dat door systeembeheerders wordt gebruikt is de Manager van Servers.
solution: Analytics
title: Servers Manager
topic: Data workbench
uuid: 96c8f060-ffd4-46b9-b039-b2ac024400b6
translation-type: tm+mt
source-git-commit: 948c6dd04819e939b45745db573a53c8be51ce37

---


# Servers Manager{#servers-manager}

Het primaire hulpmiddel dat door systeembeheerders wordt gebruikt is de Manager van Servers.

Het is de belangrijkste interface voor het bepalen van algemene systeemstatus en voor het uitvoeren van systeemconfiguratie, dossierbeheer, en fout controlefuncties.

De servermanager toont een gekleurde punt (knoop) voor elke server en [!DNL Sensor] installatie van de Werkbank van Gegevens in uw systeem en verstrekt de systeemstatus in één oogopslag voor elke installatie. Het toont ook een knoop voor uw installatie van de Werkbank van Gegevens.

De groene knopen vertegenwoordigen actieve verbindingen, vertegenwoordigen de rode knopen verbindingen die gehandicapt of anders ontoegankelijk zijn, en de grijze knopen vertegenwoordigen verbindingen de waarvan staten onbepaald zijn.

![](assets/vis_SysStat_RedGreenDots.png)

Het klikken van een knoop toont informatie over de verbindende component met de rechtermuisknop aan en verleent toegang tot om het even welke verwante menu&#39;s.

De volgende lijsten beschrijven de verstrekte informatie wanneer u een knoop voor de Werkbank van Gegevens, de server van de Werkbank van Gegevens (met inbegrip van een hoofdserver van de Werkbank van Gegevens in een cluster) met de rechtermuisknop aanklikt, of [!DNL Sensor].

<table id="table_C459CAAB07D34144B5BFFCCC84C2BB37"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Object </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Product </p> </td> 
   <td colname="col2"> <p>De naam, de versie van het product, en bouwstijlaantal. </p> <p>Voorbeeld: Werkbank voor gegevens 5.3 (0000001) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Adres </p> </td> 
   <td colname="col2"> <p>IP adres van de computer van de Werkbank van Gegevens. </p> <p>Voorbeeld: 100,0,0,1 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Configureren </p> </td> 
   <td colname="col2"> <p>Een verbinding aan het de configuratiedossier van uw <span class="keyword"> Werkbank van Gegevens </span> . Klik <span class="uicontrol"> vormen </span> &gt; <span class="uicontrol"> Insight.cfg </span> om het de configuratievenster van de Werkbank van Gegevens te tonen. Om het even welke veranderingen die u aanbrengt en in dit venster bewaart worden weerspiegeld in het <span class="filepath"> Insight.cfg- </span> dossier in uw de installatiefolder van de Werkbank van Gegevens. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Product </p> </td> 
   <td colname="col2"> <p>De naam, de versie van het product, en bouwstijlaantal. </p> <p>Voorbeeld: Data Workbench-server 5.3 (0000001) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>GN </p> </td> 
   <td colname="col2"> <p>De gemeenschappelijke naam van de de servercomputer van de Werkbank van Gegevens. </p> <p>Voorbeeld: <span class="filepath"> myserver1.mycompany.com </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Adres </p> </td> 
   <td colname="col2"> <p>IP adres of volledig - gekwalificeerde domeinnaam van de server zoals die in het dossier van Adressen op de computer en de parameter van de Plaats van het Netwerk in het <span class="filepath"> Insight.cfg- </span> dossier wordt gevormd. </p> <p>Voorbeeld: 100,0,0,1 </p> <p>Voor informatie over het dossier van Adressen, zie de Gids <i>van de Installatie en van het Beleid van de Producten van de</i>Server. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Status </p> </td> 
   <td colname="col2"> <p>Huidige status van de server van de Werkbank van Gegevens. Dit gebied toont O.K. wanneer de server van de Werkbank van Gegevens normaal loopt. Als een fout is voorgekomen en de de serverknoop van de Werkbank van Gegevens rood is, toont het gebied de fout (bijvoorbeeld, "403 Verboden"). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Gedetailleerde status </p> </td> 
   <td colname="col2"> <p>Een verbinding aan de server van de Werkbank van <span class="keyword"> Gegevens </span> Gedetailleerde de <span class="wintitle"> </span> interface van de Status, die voor het oplossen van problemenfouten of andere kwesties met de server van de Werkbank van Gegevens nuttig is. </p> <p>Voor meer informatie, zie <a href="../../../home/c-get-started/c-admin-intrf/c-det-stat-interf.md"> de Gedetailleerde Interface</a>van de Status. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Extern bureaublad </p> </td> 
   <td colname="col2"> <p>Opent een <span class="wintitle"> Externe </span> sessie van de Desktop aan de de servercomputer van de Werkbank van Gegevens. </p> <p>Voor meer informatie, zie <a href="../../../home/c-get-started/c-admin-intrf/t-rmt-dsktp-opt.md#task-dc0bdb4630474a17af67b931bc22d9ef"> de Verre Optie van de Desktop </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Serverbestanden </p> </td> 
   <td colname="col2"> <p>Een verbinding aan de Manager van de Dossiers van de <span class="wintitle"> Server </span>, die de folders en de dossiers in de de serverinstallatiefolder van de Werkbank van Gegevens toont. </p> <p>Voor meer informatie, zie <a href="../../../home/c-get-started/c-admin-intrf/c-svr-files-mgr.md#concept-73a0808487c8424285ae7302f53bc5f4"> de Manager van de Dossiers van de Server </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Servercontrole </p> </td> 
   <td colname="col2"> <p>Een verbinding aan de interface van de Monitor van de <span class="wintitle"> </span> Server, die voor het oplossen van problemen of het volgen van prestatiesparameters nuttig is. </p> <p>Voor meer informatie, zie <a href="../../../home/c-get-started/c-admin-intrf/c-svr-mtr-intfc.md#concept-3bea7441de20409585e63060d5489f45"> de Interface van de Monitor van de Server </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Gerelateerde servers </p> </td> 
   <td colname="col2"> <p>Alleen voor datacWorkbench-serverclusters. </p> <p>Een menu dat van de gemeenschappelijke namen van de computers een lijst maakt die in het van de server van de Werkbank van de hoofdgegevens *.address <span class="filepath"> </span> - dossier worden vermeld. Deze lijst omvat gewoonlijk alle servers van de Werkbank van <span class="keyword"> Gegevens van de verwerking </span> in de cluster. Dit menu verschijnt slechts als de Werkbank van Gegevens een exemplaar van het van de server van de Werkbank van <span class="filepath"> Gegevens *.address </span> dossier heeft. </p> <p>Wanneer u klikt op <span class="uicontrol"> Verwante servers </span>, kunt u op een van de volgende klikken: 
     <ul id="ul_3B28B8579B1945FD80669EDFDFDA84A6"> 
      <li id="li_90094B46CB304C179136BB75FF0D6DBD"> <span class="uicontrol"> De Lijst van de Monitor van de server </span>, die de de interfacelijstdetails van de Monitor van de <span class="wintitle"> </span> Server voor alle verwante servers toont </li> 
      <li id="li_CD6FF5BB52874ABCB536C2DE2376587A">De gemeenschappelijke naam van om het even welke server van de Werkbank van Gegevens, die een contextmenu toont dat u toelaat om het even welke volgend voor die bepaalde server te openen: 
       <ul id="ul_928510D1DE68471583F2EE7547AEB824"> 
        <li id="li_8399338137354A59B9B4D24AF7EEE868"> <span class="uicontrol"> Gedetailleerde status </span>. Zie <a href="../../../home/c-get-started/c-admin-intrf/c-det-stat-interf.md"> de Gedetailleerde interface van de Status </a>. </li> 
        <li id="li_0FE569C56B3F4583BC1F3DF3B4F55765"> <span class="uicontrol"> Externe desktop </span>. Zie <a href="../../../home/c-get-started/c-admin-intrf/t-rmt-dsktp-opt.md#task-dc0bdb4630474a17af67b931bc22d9ef"> de optie Extern bureaublad </a>. </li> 
        <li id="li_2B6F8419CB5945C9B411F6A7C2C859FF"> <span class="uicontrol"> Server Files Manager </span>. Zie <a href="../../../home/c-get-started/c-admin-intrf/c-svr-files-mgr.md#concept-73a0808487c8424285ae7302f53bc5f4"> de Manager van de Dossiers van de Server </a>. </li> 
        <li id="li_F22F974EB4DE4F0F93623AE98C7DCEBC"> <span class="uicontrol"> Servermonitor </span>. Zie <a href="../../../home/c-get-started/c-admin-intrf/c-svr-mtr-intfc.md#concept-3bea7441de20409585e63060d5489f45"> de interface van de Monitor van de Server </a>. </li> 
       </ul> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

<table id="table_5BFA0AFE2D9A4337BF04343879DAD03B"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Object </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Product </p> </td> 
   <td colname="col2"> <p>De naam, de versie van het product, en bouwstijlaantal. </p> <p>Voorbeeld: Sensor 3.76; J3,67 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>ID </p> </td> 
   <td colname="col2"> De <span class="wintitle"> identiteitskaart van de Sensor </span> die in het de <span class="wintitle"> configuratiedossier van de </span> Sensor voor deze installatie wordt gespecificeerd. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>IP </p> </td> 
   <td colname="col2"> <p>IP adres van het Web of de toepassingsserver waarop de <span class="wintitle"> Sensor </span> geïnstalleerd is. </p> <p>Voorbeeld: 100,0,0,1 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>PID </p> </td> 
   <td colname="col2"> <p>ID van het proces die door het werkende systeem wordt toegewezen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>SSL </p> </td> 
   <td colname="col2"> <p>Of de <span class="wintitle"> Sensor </span> en de server van de Werkbank van Gegevens communiceren gebruikend SSL. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Tijd </p> </td> 
   <td colname="col2"> <p>Tijd (HH:MM.:SS) dat de <span class="wintitle"> Sensor </span> het laatst een verbinding met de server van de Werkbank van Gegevens vestigde. </p> </td> 
  </tr> 
 </tbody> 
</table>
