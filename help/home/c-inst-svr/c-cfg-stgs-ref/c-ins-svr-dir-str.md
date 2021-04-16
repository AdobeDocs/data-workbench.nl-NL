---
description: Lijst met bestanden die met Insight Server zijn geïnstalleerd en de bestanden die aanwezig zijn nadat deze zijn geregistreerd en voor het eerst worden uitgevoerd.
title: Insight Server Directory Structure
uuid: 8339b275-f118-4d5d-937e-4df9f8a56b50
exl-id: 568391d0-e0f7-4a5a-ad71-de33c52968a0
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '499'
ht-degree: 0%

---

# Insight Server Directory Structure{#insight-server-directory-structure}

Lijst met bestanden die met Insight Server zijn geïnstalleerd en de bestanden die aanwezig zijn nadat deze zijn geregistreerd en voor het eerst worden uitgevoerd.

## Bestanden die zijn opgenomen in het installatiepakket {#section-daec17dab3e34c3c9e1ef65842cb91f1}

De volgende directory&#39;s zijn opgenomen in het [!DNL Insight Server]-installatiepakket:

<table id="table_CE713A3D671C453A87986E4CD4620EF3"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Map </th> 
   <th colname="col2" class="entry"> Beschrijving van inhoud van directory </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Toegangsbeheer </td> 
   <td colname="col2"> <span class="keyword"> Het  </span> configuratiedossier van de Server van het inzicht dat een lijst van de Groepen van de Toegang specificeert. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Adressen </td> 
   <td colname="col2"> Adres(sen) gebruikt voor communicatie met <span class="keyword"> Insight Server </span>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Audit </td> 
   <td colname="col2"> Dagelijkse toegangslogboeken met details betreffende alle pogingen tot verbindingen met <span class="keyword"> Insight Server </span>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> bin </td> 
   <td colname="col2"> <span class="keyword"> Uitvoerbare  </span> programmabestanden van Insight Server. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Certificaten </td> 
   <td colname="col2"> SSL digitale certificaten. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Onderdelen </td> 
   <td colname="col2"> <span class="keyword"> Insight Server- </span> componentconfiguratiebestanden. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Componenten voor het verwerken van servers </td> 
   <td colname="col2"> <span class="keyword"> De dossiers van de de  </span> componentenconfiguratie van de Server van het inzicht voor de verwerking van de Servers van het  <span class="keyword"> Inzicht  </span> binnen een  <span class="keyword"> cluster van de Server van het  </span> Inzicht. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Gebeurtenissen </td> 
   <td colname="col2"> Dagelijkse logboekbestanden met gedetailleerde gebeurtenisstatusberichten, inclusief foutberichten. Gebeurtenissen die worden vastgelegd en geregistreerd door <span class="keyword"> Insight Server </span> worden ook weergegeven in Windows Event Viewer. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Logboeken </td> 
   <td colname="col2"> <p>Logbestanden geproduceerd door <span class="wintitle"> Sensor </span>(s). </p> <p>Logs is de standaard logboekregistrerende folder, maar een afwisselende folder kan in <span class="filepath"> mededelingen.cfg </span> dossier zijn gespecificeerd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Zoeken </td> 
   <td colname="col2"> Bestanden opzoeken, zoals lijsten met robot en zoekmachines. <span class="keyword"> De Server van het inzicht  </span> moet alle raadplegingsdossiers in geheugen laden. De totale grootte van alle raadplegingsdossiers waarnaar in componentenconfiguratiedossiers, plus overheadkosten worden verwezen (bijvoorbeeld, 12 bytes per rij voor <span class="filepath"> FlatFileLookup </span> dossiers), moet het beschikbare fysieke of virtuele geheugen niet overschrijden dat beschikbaar is nadat alle andere softwaretoepassingen worden geladen. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Profielen </td> 
   <td colname="col2"> <p>Bestanden die zijn gerelateerd aan elk profiel (configuratie-, werkruimte- en visualisatiebestanden). Profielen worden gevuld met gegevens uit een gegevensset. Datasets omvatten gebeurtenisgegevens ("loggegevens"); dergelijke gegevens kunnen worden vastgelegd door geïnstalleerde <span class="wintitle"> sensoren </span>, verzonden door webbeacons of paginatags, of invoer van gegevensopslagplaatsen. <span class="keyword"> De  </span> gebruikers van het inzicht met toegang tot een bepaald profiel kunnen de reeks verwerkte gegevens voor dat profiel evenals de Werkruimten en visualisaties gebruiken die binnen dat profiel worden bepaald. </p> <p>De werkruimten zijn werkgebieden voor systeembeheer of analyse. Een werkruimte kan meerdere interfaces bevatten die verschillende details over de systeemprestaties weergeven. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Software </td> 
   <td colname="col2"> <span class="keyword"> De  </span> softwareupdates van het inzicht. Updates van rapportsoftware worden hier ook opgeslagen. </td> 
  </tr> 
 </tbody> 
</table>

## Mappen en bestanden gemaakt na opstarten {#section-ef7408e8fae64454b326ec07453d4628}

De hieronder vermelde directory&#39;s worden gemaakt nadat [!DNL Insight Server] voor het eerst is geregistreerd en uitgevoerd:

<table id="table_89CC9F3E568044C8A0072BF0A6EDCCEF"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Map </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Staat </td> 
   <td colname="col2"> Verwerkingsinformatie gegenereerd door <span class="keyword"> Insight Server </span>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Temperatuur </td> 
   <td colname="col2"> <p>Locatie van de tijdelijke bestanden die door <span class="keyword"> Insight Server </span> worden gebruikt tijdens opwerking en bewerking. Er is gewoonlijk één bestand (standaard genaamd <span class="filepath"> temp.db </span>) per fysieke schijf. </p> <p> <span class="keyword"> De Server van het inzicht  </span> moet worden gevormd om aan deze folder te schrijven. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Traceren </td> 
   <td colname="col2"> Loggegevens en gebeurtenisgegevens over <span class="keyword"> Insight Server </span>. Nuttig voor probleemoplossing. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Gebruikers </td> 
   <td colname="col2"> Benoemde gebruikers ( <span class="keyword"> Insight </span>) met toegang tot de profielen op de server. Er wordt een directory voor elke geautoriseerde benoemde gebruiker gemaakt in de directory Users\ wanneer de gebruiker <span class="keyword"> Insight Server </span> via <span class="keyword"> Insight </span> voor het eerst benadert. De map voor elke benoemde gebruiker bevat mappen die overeenkomen met alle profielen die de gebruiker heeft geopend op die <span class="keyword"> Insight Server </span> en hun lokale adresbestanden. </td> 
  </tr> 
 </tbody> 
</table>
