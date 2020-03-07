---
description: Instructies om mededelingen voor de Server of de Repeater van het Inzicht te vormen.
solution: Insight
title: Instellingen voor communicatie-configuratie
uuid: 03297cf0-eb55-4db0-b692-eba24fcf947c
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Instellingen voor communicatie-configuratie{#communications-configuration-settings}

Instructies om mededelingen voor de Server of de Repeater van het Inzicht te vormen.

Voltooi de parameters in het volgende dossier:

[!DNL Product Name installation directory\Components\Communications.cfg]

>[!NOTE]
>
>Alvorens om het even welke parameters te wijzigen die niet in deze lijst worden vermeld, gelieve Adobe te contacteren.

<table id="table_C87F1150E53548F484A8C0CFE91F1079"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Parameter </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Access Control File </td> 
   <td colname="col2"> <p>Plaats van het <span class="filepath"> Access Control.cfg- </span> bestand. De standaardplaats is de <span class="filepath"> omslag van het Toegangsbeheer </span> binnen de de installatiefolder van de Server van het <span class="keyword"> Inzicht </span> of van de <span class="wintitle"> Repeater </span> . </p> <p>Voorbeeld: <filepath></filepath> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Access Log Directory </td> 
   <td colname="col2"> <p>Omslag waaraan u de controlelogboeken wilt in kaart brengen. </p> <p>Voorbeeld: <filepath></filepath> </p> <p> <p>Opmerking:  U kunt controlelogboeken aan een andere lokale aandrijving in kaart brengen (voorbeeld: <span class="filepath"> string: P:\\Audit\\ </span>), maar breng geen controlelogboeken aan een netwerkaandrijving in kaart. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Verboden voor toegangslog </td> 
   <td colname="col2"> Deze parameter kan aan waar of vals worden geplaatst. Het wordt gebruikt om het filtreren van het controlelogboek toe te laten en onbruikbaar te maken. Om ervoor te zorgen dat elk verzoek wordt geregistreerd, plaats de parameter aan Waar. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> IP-interface </td> 
   <td colname="col2"> <p>IP adres aan gebruik wanneer twee netwerkkaarten voor de toegang tot van twee verschillende netwerken beschikbaar zijn. </p> <p>Voorbeeld: I <filepath></filepath><i>&lt; <span class="filepath"> IP-adres </span>&gt;</i> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Poort </td> 
   <td colname="col2"> <p>De niet veilige (HTTP) haven waarop de Server van het <span class="keyword"> Inzicht </span> of de <span class="wintitle"> Repeater </span> luistert. De standaardhaven is 80. Het ingaan van een waarde van 0 maakt niet veilige verbindingen onbruikbaar. </p> <p>Voorbeeld: <filepath></filepath> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> SSL-CIFERS </td> 
   <td colname="col2"> Sommige milieu's vereisen sterkere communicatie veiligheid dan anderen. Als u een specifieke SSL cijferreeks wilt gebruiken, kunt u het met deze parameter specificeren. <p>Voorbeeld: <filepath></filepath> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> SSL-poort </td> 
   <td colname="col2"> <p>Beveilig (via SSL) haven waarop de <span class="keyword"> Server van het Inzicht </span> of de <span class="wintitle"> Repeater </span> luistert. De standaardhaven is 443. Het ingaan van een waarde van 0 maakt veilige verbindingen onbruikbaar. </p> <p>Voorbeeld: <span class="filepath"></span> </p> <filepath></filepath> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <i>n=</i>LoggingServer: </td> 
   <td colname="col2"> Rubriek voor de montages van de Server van het Registreren. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Naam klant </td> 
   <td colname="col2"> <p>De naam van de klant om voor Niet gespecificeerde klanten in administratieve alarm, zoals in het volgende voorbeeld te verschijnen: </p> <p>"Geen gegevens ontvangen van sensor XYZ voor klant "Niet gespecificeerd"in 15." </p> <p>Voorbeeld: <code> 1&nbsp;=&nbsp;LoggingServer:&nbsp; 
      &nbsp;&nbsp;Customer&nbsp;Name&nbsp;=&nbsp;string:&nbsp;CompanyAB </code> </p> <p>Gebruikend het voorbeeld hierboven, zouden de administratieve alarm voor Niet gespecificeerde klanten nu als volgt lezen: </p> <p>"Geen gegevens ontvangen van sensor XYZ voor klant "CompanyAB" in 15." </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <i>n=</i>FileServer: </p> <p> Lokaal pad = tekenreeks: Aanmelden\\\ </p> </td> 
   <td colname="col2"> <p>Omslag waarin u de logboekdossiers wilt opslaan. </p> <p>Voorbeeld: </p> <code> 9&nbsp;=&nbsp;FileServer:&nbsp; 
     &nbsp;&nbsp;Local&nbsp;Path&nbsp;=&nbsp;string:&nbsp;Logs\\ </code> <p>Om tot deze omslag van de Manager van de Dossiers van de <span class="wintitle"> Server toegang te hebben </span>, moet de plaats die in deze parameter wordt gespecificeerd de plaats aanpassen die u in de parameter van de Wegen van het Logboek in het <span class="filepath"> Logboek Processing.cfg- </span> dossier specificeert. Voor meer informatie over het wijzigen van de folder van Logboeken in het <span class="filepath"> Logboek Processing.cfg- </span> dossier, zie het hoofdstuk van het Dossier van de Configuratie van de Logboekverwerking van de Gids van de Configuratie van de <i>Dataset</i>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <i>n=</i>FileServer: </p> <p> Lokaal pad = tekenreeks: Audit\\\\\ </p> </td> 
   <td colname="col2"> <p>Omslag waaraan u de controlelogboeken wilt in kaart brengen. </p> <p>Voorbeeld: </p> <code> 5&nbsp;=&nbsp;FileServer:&nbsp; 
     &nbsp;&nbsp;Local&nbsp;Path&nbsp;=&nbsp;string:&nbsp;Audit\\ </code> <p>Opmerking:  <p>U kunt controlelogboeken aan een andere lokale aandrijving in kaart brengen (voorbeeld: <span class="filepath"> string: P:\\Audit\\ </span>), maar breng geen controlelogboeken aan een netwerkaandrijving in kaart. </p> <p>Om tot deze omslag van de Manager van de Dossiers van de <span class="wintitle"> Server toegang te kunnen hebben </span>, moet de plaats die in deze parameter wordt gespecificeerd de plaats aanpassen die u in de parameter van de Folder van het Logboek van de Toegang in dit dossier. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <i>n=</i>NormalizeServer: </td> 
   <td colname="col2"> <p>Deze parameter is slechts op de Server van het <span class="keyword"> Inzicht van toepassing </span>. </p> <p>Voor meer informatie over het specificeren van de Gecentraliseerde Server van de Normalisatie voor uw <span class="keyword"> cluster van de Server van het Inzicht, zie het hoofdstuk van het Dossier van de Configuratie van de Configuratie van het Logboek van de Gids </span> van de Configuratie van de <i></i>Dataset. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <i>n=</i>ReportStatusServer: </p> <p> URI = string: /ReportStatus.vsp </p> </td> 
   <td colname="col2"> <p>Deze parameter is slechts op de Server van het <span class="keyword"> Inzicht van toepassing </span>. </p> <p>Laat u toe om de <span class="keyword"> status van het Rapport in de Gedetailleerde interface van de Status voor de Server van het </span> Inzicht te bekijken <span class="keyword"> </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

