---
description: Lijst met bestanden die met Insight Server zijn geïnstalleerd en de bestanden die aanwezig zijn nadat deze zijn geregistreerd en voor het eerst worden uitgevoerd.
title: Insight Server Directory Structure
uuid: 8339b275-f118-4d5d-937e-4df9f8a56b50
exl-id: 568391d0-e0f7-4a5a-ad71-de33c52968a0
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '499'
ht-degree: 1%

---

# Insight Server Directory Structure{#insight-server-directory-structure}

{{eol}}

Lijst met bestanden die met Insight Server zijn geïnstalleerd en de bestanden die aanwezig zijn nadat deze zijn geregistreerd en voor het eerst worden uitgevoerd.

## Bestanden die zijn opgenomen in het installatiepakket {#section-daec17dab3e34c3c9e1ef65842cb91f1}

De volgende mappen worden opgenomen in de [!DNL Insight Server] installatiepakket:

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
   <td colname="col2"> <span class="keyword"> Insight Server </span> configuratiebestand dat een lijst met toegangsgroepen opgeeft. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Adressen </td> 
   <td colname="col2"> Adres(sen) gebruikt voor communicatie met <span class="keyword"> Insight Server </span>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Audit </td> 
   <td colname="col2"> Dagelijkse toegangslogboeken met informatie over alle pogingen tot verbindingen met <span class="keyword"> Insight Server </span>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> bin </td> 
   <td colname="col2"> <span class="keyword"> Insight Server </span> uitvoerbare programmabestanden. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Certificaten </td> 
   <td colname="col2"> SSL digitale certificaten. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Onderdelen </td> 
   <td colname="col2"> <span class="keyword"> Insight Server </span> componentconfiguratiebestanden. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Componenten voor het verwerken van servers </td> 
   <td colname="col2"> <span class="keyword"> Insight Server </span> componentconfiguratiebestanden voor verwerking <span class="keyword"> Inzichtsservers </span> binnen een <span class="keyword"> Insight Server </span> cluster. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Gebeurtenissen </td> 
   <td colname="col2"> Dagelijkse logboekbestanden met gedetailleerde gebeurtenisstatusberichten, inclusief foutberichten. Gebeurtenissen vastgelegd en geregistreerd door <span class="keyword"> Insight Server </span> worden ook weergegeven in Windows Event Viewer. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Logboeken </td> 
   <td colname="col2"> <p>Logbestanden geproduceerd door <span class="wintitle"> Sensor </span>(s). </p> <p>"Logs" is de standaardlogboekmap, maar mogelijk is een alternatieve map opgegeven in de <span class="filepath"> communications.cfg </span> bestand. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Zoeken </td> 
   <td colname="col2"> Bestanden opzoeken, zoals lijsten met robot en zoekmachines. <span class="keyword"> Insight Server </span> moet alle opzoekbestanden in het geheugen laden. De totale grootte van alle raadplegingsdossiers waarnaar in de dossiers van de componentenconfiguratie wordt verwezen, plus overheadkosten (bijvoorbeeld, 12 bytes per rij voor <span class="filepath"> FlatFileLookup </span> bestanden), mag het beschikbare fysieke of virtuele geheugen dat beschikbaar is nadat alle andere softwaretoepassingen zijn geladen, niet overschrijden. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Profielen </td> 
   <td colname="col2"> <p>Bestanden die zijn gerelateerd aan elk profiel (configuratie-, werkruimte- en visualisatiebestanden). Profielen worden gevuld met gegevens uit een gegevensset. Datasets omvatten gebeurtenisgegevens ("loggegevens"); dergelijke gegevens kunnen worden vastgelegd door <span class="wintitle"> Sensoren </span>, verzonden door webbeacons of paginatags, of invoer uit gegevensopslagruimten. <span class="keyword"> Inzicht </span> gebruikers met toegang tot een bepaald profiel kunnen de set verwerkte gegevens voor dat profiel gebruiken, evenals de werkruimten en visualisaties die in dat profiel zijn gedefinieerd. </p> <p>De werkruimten zijn werkgebieden voor systeembeheer of analyse. Een werkruimte kan meerdere interfaces bevatten die verschillende details over de systeemprestaties weergeven. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Software </td> 
   <td colname="col2"> <span class="keyword"> Inzicht </span> software-updates. Updates van rapportsoftware worden hier ook opgeslagen. </td> 
  </tr> 
 </tbody> 
</table>

## Mappen en bestanden gemaakt na opstarten {#section-ef7408e8fae64454b326ec07453d4628}

De hieronder vermelde directory&#39;s worden gemaakt na [!DNL Insight Server] voor het eerst wordt geregistreerd en uitgevoerd:

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
   <td colname="col2"> <p>Locatie van de tijdelijke bestanden die worden gebruikt door <span class="keyword"> Insight Server </span> tijdens de opwerking en het bedrijf. Er is meestal één bestand (benoemd <span class="filepath"> temp.db </span> standaard) per fysieke schijf. </p> <p> <span class="keyword"> Insight Server </span> moet worden gevormd om aan deze folder te schrijven. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Traceren </td> 
   <td colname="col2"> Logboek en gebeurtenisgegevens over <span class="keyword"> Insight Server </span>. Nuttig voor probleemoplossing. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Gebruikers </td> 
   <td colname="col2"> Benoemd ( <span class="keyword"> Inzicht </span>) gebruikers met toegang tot de profielen op de server. Er wordt een map voor elke geautoriseerde benoemde gebruiker gemaakt in de map Users\ wanneer de gebruiker voor het eerst toegang krijgt <span class="keyword"> Insight Server </span> via <span class="keyword"> Inzicht </span>. De map voor elke benoemde gebruiker bevat mappen die overeenkomen met alle profielen die de gebruiker voor die gebruiker heeft geopend <span class="keyword"> Insight Server </span> en hun lokale adresbestanden. </td> 
  </tr> 
 </tbody> 
</table>
