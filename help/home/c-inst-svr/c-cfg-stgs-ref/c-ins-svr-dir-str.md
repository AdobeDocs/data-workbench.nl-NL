---
description: Lijst met bestanden die met Insight Server zijn geïnstalleerd en de bestanden die aanwezig zijn nadat deze zijn geregistreerd en voor het eerst worden uitgevoerd.
solution: Analytics
title: Insight Server Directory Structure
uuid: 8339b275-f118-4d5d-937e-4df9f8a56b50
translation-type: tm+mt
source-git-commit: 34cdcfc83ae6bb620706db37228e200cff43ab2c
workflow-type: tm+mt
source-wordcount: '499'
ht-degree: 0%

---


# Insight Server Directory Structure{#insight-server-directory-structure}

Lijst met bestanden die met Insight Server zijn geïnstalleerd en de bestanden die aanwezig zijn nadat deze zijn geregistreerd en voor het eerst worden uitgevoerd.

## Bestanden die zijn opgenomen in het installatiepakket {#section-daec17dab3e34c3c9e1ef65842cb91f1}

De volgende directory&#39;s zijn opgenomen in het [!DNL Insight Server] installatiepakket:

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
   <td colname="col2"> <span class="keyword"> Het de configuratiedossier van de Server van het inzicht dat een lijst van de Groepen van de Toegang specificeert. </span> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Adressen </td> 
   <td colname="col2"> Adres(sen) gebruikt voor communicatie met <span class="keyword"> Insight Server </span>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Audit </td> 
   <td colname="col2"> Dagelijkse toegangslogboeken die details betreffende alle geprobeerd verbindingen aan de Server van het <span class="keyword"> Inzicht bevatten </span>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> bin </td> 
   <td colname="col2"> <span class="keyword"> Uitvoerbare programmabestanden van Insight Server. </span> </td> 
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
   <td colname="col2"> <span class="keyword"> De dossiers van de de </span> componentenconfiguratie van de Server van het inzicht voor de verwerking van de Servers van het <span class="keyword"> Inzicht </span> binnen een <span class="keyword"> de </span> cluster van de Server van het Inzicht. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Gebeurtenissen </td> 
   <td colname="col2"> Dagelijkse logboekbestanden met gedetailleerde gebeurtenisstatusberichten, inclusief foutberichten. Gebeurtenissen die door de Server van het <span class="keyword"> Inzicht worden gevangen en worden geregistreerd </span> worden ook getoond in de Kijker van de Gebeurtenis van Vensters. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Logboeken </td> 
   <td colname="col2"> <p>Logbestanden geproduceerd door <span class="wintitle"> sensor </span>(en). </p> <p>"Logs" is de standaardlogboekmap, maar er kan een alternatieve map zijn opgegeven in het <span class="filepath"> bestand communications.cfg </span> . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Zoeken </td> 
   <td colname="col2"> Bestanden opzoeken, zoals lijsten met robot en zoekmachines. <span class="keyword"> De Server van het inzicht </span> moet alle raadplegingsdossiers in geheugen laden. De totale grootte van alle raadplegingsdossiers waarnaar in componentenconfiguratiedossiers, plus overheadkosten (bijvoorbeeld, 12 bytes per rij voor <span class="filepath"> FlatFileLookup </span> dossiers) wordt verwezen, moet niet het beschikbare fysieke of virtuele geheugen overschrijden dat beschikbaar is nadat alle andere softwaretoepassingen worden geladen. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Profielen </td> 
   <td colname="col2"> <p>Bestanden die zijn gerelateerd aan elk profiel (configuratie-, werkruimte- en visualisatiebestanden). Profielen worden gevuld met gegevens uit een gegevensset. Datasets omvatten gebeurtenisgegevens ("loggegevens"); dergelijke gegevens kunnen worden vastgelegd door geïnstalleerde <span class="wintitle"> sensoren </span>, worden verzonden door webbeacons of paginatags, of worden ingevoerd door gegevensopslagplaatsen. <span class="keyword"> Inzichtgebruikers </span> met toegang tot een bepaald profiel kunnen de set verwerkte gegevens voor dat profiel gebruiken, evenals de werkruimten en visualisaties die in dat profiel zijn gedefinieerd. </p> <p>De werkruimten zijn werkgebieden voor systeembeheer of analyse. Een werkruimte kan meerdere interfaces bevatten die verschillende details over de systeemprestaties weergeven. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Software </td> 
   <td colname="col2"> <span class="keyword"> Software-updates voor </span> het inzicht. Updates van rapportsoftware worden hier ook opgeslagen. </td> 
  </tr> 
 </tbody> 
</table>

## Mappen en bestanden gemaakt na opstarten {#section-ef7408e8fae64454b326ec07453d4628}

De hieronder vermelde directory&#39;s worden gemaakt nadat ze voor het eerst [!DNL Insight Server] zijn geregistreerd en uitgevoerd:

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
   <td colname="col2"> De informatie van de verwerking die door de Server van het <span class="keyword"> Inzicht wordt geproduceerd </span>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Temperatuur </td> 
   <td colname="col2"> <p>Plaats van de tijdelijke dossiers die door de Server van het <span class="keyword"> Inzicht </span> tijdens herverwerking en verrichting worden gebruikt. Meestal is er één bestand (standaard genaamd <span class="filepath"> </span> temp.db) per fysieke schijf. </p> <p> <span class="keyword"> De Server van het inzicht </span> moet worden gevormd om aan deze folder te schrijven. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Traceren </td> 
   <td colname="col2"> Logbestand- en gebeurtenisgegevens over <span class="keyword"> Insight Server </span>. Nuttig voor probleemoplossing. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Gebruikers </td> 
   <td colname="col2"> Benoemde gebruikers ( <span class="keyword"> Insight </span>) die toegang hebben tot de profielen op de server. Een folder voor elke geautoriseerde genoemde gebruiker wordt gecreeerd binnen de folder Gebruikers \ wanneer de gebruiker eerst tot de Server van het <span class="keyword"> Inzicht </span> via <span class="keyword"> Inzicht toegang heeft </span>. De folder voor elke genoemde gebruiker bevat folders die aan alle profielen beantwoorden die de gebruiker op die Server van het <span class="keyword"> Inzicht </span> evenals hun lokale adresdossiers heeft betreden. </td> 
  </tr> 
 </tbody> 
</table>

