---
description: Lijst van dossiers die met de Server van het Inzicht en de aanwezige dossiers worden geïnstalleerd nadat het is geregistreerd, en looppas voor het eerst.
solution: Insight
title: Insight Server Directory Structure
uuid: 8339b275-f118-4d5d-937e-4df9f8a56b50
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Insight Server Directory Structure{#insight-server-directory-structure}

Lijst van dossiers die met de Server van het Inzicht en de aanwezige dossiers worden geïnstalleerd nadat het is geregistreerd, en looppas voor het eerst.

## Bestanden die zijn opgenomen in het Installatiepakket {#section-daec17dab3e34c3c9e1ef65842cb91f1}

De volgende folders zijn inbegrepen in het [!DNL Insight Server] installatiepakket:

<table id="table_CE713A3D671C453A87986E4CD4620EF3"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Directoraat </th> 
   <th colname="col2" class="entry"> Beschrijving van de inhoud van de directory </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Toegangsbeheer </td> 
   <td colname="col2"> <span class="keyword"> Het de configuratiedossier van de Server van het </span> inzicht dat een lijst van de Groepen van de Toegang specificeert. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Adressen </td> 
   <td colname="col2"> Adres(sen) gebruikt voor communicatie met <span class="keyword"> Insight Server </span>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Controle </td> 
   <td colname="col2"> Dagelijkse toegangslogboeken die details betreffende alle pogingen bevatten om verbindingen aan de Server van het <span class="keyword"> Inzicht te verbinden </span>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> vuilnisbak </td> 
   <td colname="col2"> <span class="keyword"> De uitvoerbare </span> programmadossiers van de Server van het inzicht. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Certificaten </td> 
   <td colname="col2"> SSL digitale certificaten. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Onderdelen </td> 
   <td colname="col2"> <span class="keyword"> De dossiers van de de </span> componentenconfiguratie van de Server van het inzicht. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Onderdelen voor verwerkingsservers </td> 
   <td colname="col2"> <span class="keyword"> De dossiers van de de </span> componentenconfiguratie van de Server van het inzicht voor de verwerking van de Servers van het <span class="keyword"> Inzicht </span> binnen een cluster van de Server van het <span class="keyword"> Inzicht </span> . </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Gebeurtenissen </td> 
   <td colname="col2"> Dagelijkse gebeurtenislogboeken die gedetailleerde berichten van de gebeurtenisstatus, met inbegrip van foutenmeldingen bevatten. De gebeurtenissen die door de Server van het <span class="keyword"> Inzicht worden gevangen en worden geregistreerd </span> worden ook getoond in de Kijker van de Gebeurtenis van Vensters. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Logboeken </td> 
   <td colname="col2"> <p>Logbestanden van de <span class="wintitle"> sensor </span>(en). </p> <p>"Logboeken"is de standaardregistrerenfolder, maar een afwisselende folder kan in het <span class="filepath"> communications.cfg- </span> dossier zijn gespecificeerd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Zoekopdrachten </td> 
   <td colname="col2"> De dossiers van de raadpleging, zoals robot en de lijsten van de onderzoeksmotor. <span class="keyword"> De Server van het zicht </span> moet alle raadplegingsdossiers in geheugen laden. De totale grootte van alle raadplegingsdossiers die in de dossiers van de componentenconfiguratie van verwijzingen worden voorzien, plus overheadkosten (bijvoorbeeld, 12 bytes per rij voor <span class="filepath"> FlatFileLookup </span> - dossiers), moet niet het beschikbare fysieke of virtuele geheugen overschrijden dat beschikbaar is nadat alle andere softwaretoepassingen worden geladen. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Profielen </td> 
   <td colname="col2"> <p>Bestanden die betrekking hebben op elk profiel (configuratie, werkruimte en visualisatiebestanden). De profielen worden bevolkt door gegevens van een dataset. De gegevensbestanden omvatten gebeurtenisgegevens ("loggegevens"); dergelijke gegevens kunnen door geïnstalleerde <span class="wintitle"> sensoren worden gevangen </span>, door de bakens van het Web of paginabags worden overgebracht, of door gegevenspakhuizen worden ingevoerd. <span class="keyword"> De </span> gebruikers van het inzicht met toegang tot een bepaald profiel kunnen de reeks verwerkte gegevens voor dat profiel evenals de Werkruimten en de visualisaties gebruiken die binnen dat profiel worden bepaald. </p> <p>De werkruimten zijn het werkgebieden voor systeembeleid of analyse. Een werkruimte kan veelvoudige interfaces bevatten die verschillende details over systeemprestaties tonen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Software </td> 
   <td colname="col2"> <span class="keyword"> Software-updates </span> van het inzicht. De de softwareupdates van het rapport worden ook hier opgeslagen. </td> 
  </tr> 
 </tbody> 
</table>

## directory&#39;s en bestanden die na opstarten zijn gemaakt {#section-ef7408e8fae64454b326ec07453d4628}

De onderstaande directory&#39;s worden gemaakt nadat ze zijn geregistreerd en voor het eerst worden uitgevoerd: [!DNL Insight Server]

<table id="table_89CC9F3E568044C8A0072BF0A6EDCCEF"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Directoraat </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Staat </td> 
   <td colname="col2"> De informatie van de verwerking die door de Server van het <span class="keyword"> Inzicht wordt geproduceerd </span>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Temp. </td> 
   <td colname="col2"> <p>Plaats van de tijdelijke dossiers die door de Server van het <span class="keyword"> Inzicht </span> tijdens opwerking en verrichting worden gebruikt. Er is gewoonlijk één dossier (genoemd <span class="filepath"> temp.db </span> door gebrek) per fysieke aandrijving. </p> <p> <span class="keyword"> De Server van het zicht </span> moet worden gevormd om aan deze folder te schrijven. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Spoor </td> 
   <td colname="col2"> Logboek en gebeurtenisgegevens over de Server van het <span class="keyword"> Inzicht </span>. Nuttig voor het oplossen van problemen. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Gebruikers </td> 
   <td colname="col2"> Genoemde ( <span class="keyword"> Inzicht </span>) gebruikers met toegang tot de profielen op de Server. Een folder voor elke erkende genoemde gebruiker wordt gecreeerd binnen de folderGebruikers \ wanneer de gebruiker tot de Server van het <span class="keyword"> Inzicht </span> via <span class="keyword"> Inzicht eerst toegang heeft </span>. De folder voor elke genoemde gebruiker bevat folders die aan alle profielen beantwoorden die de gebruiker op die Server van het <span class="keyword"> Inzicht </span> evenals hun lokale adresdossiers heeft betreden. </td> 
  </tr> 
 </tbody> 
</table>

