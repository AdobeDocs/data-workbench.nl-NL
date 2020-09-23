---
description: Instructies om mededelingen voor de Server of Repeater van het Inzicht te vormen.
solution: Analytics
title: Configuratie-instellingen voor communicatie
uuid: 03297cf0-eb55-4db0-b692-eba24fcf947c
translation-type: tm+mt
source-git-commit: 34cdcfc83ae6bb620706db37228e200cff43ab2c
workflow-type: tm+mt
source-wordcount: '508'
ht-degree: 0%

---


# Configuratie-instellingen voor communicatie{#communications-configuration-settings}

Instructies om mededelingen voor de Server of Repeater van het Inzicht te vormen.

Voltooi de parameters in het volgende bestand:

[!DNL Product Name installation directory\Components\Communications.cfg]

>[!NOTE]
>
>Neem contact op met Adobe voordat u parameters wijzigt die niet in deze tabel worden vermeld.

<table id="table_C87F1150E53548F484A8C0CFE91F1079"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Parameter </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Toegangscontrolebestand </td> 
   <td colname="col2"> <p>Locatie van het <span class="filepath"> </span> bestand Access Control.cfg. De standaardplaats is de <span class="filepath"> omslag van het Toegangsbeheer binnen de </span> de installatiemap van de Server <span class="keyword"> of van de </span> Repeater van het Inzicht <span class="wintitle"> </span> . </p> <p>Voorbeeld: <code>Access Control File = Path: Access Control\\Access Control.cfg</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Access Log Directory </td> 
   <td colname="col2"> <p>Map waaraan u de controlelogboeken wilt toewijzen. </p> <p>Voorbeeld: <code>Access Log Directory = string: Audit\\</code> </p> <p> <p>Opmerking:  U kunt controlelogboeken toewijzen aan een ander lokaal station (voorbeeld: <span class="filepath"> tekenreeks: P:\\Audit\\ </span>), maar wijs geen controlelogboeken aan een netwerkaandrijving toe. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Toegangslogbestand is volledig </td> 
   <td colname="col2"> Deze parameter kan worden ingesteld op true of false. Het wordt gebruikt om het filtreren van het controlelogboek toe te laten en onbruikbaar te maken. Om ervoor te zorgen dat elk verzoek wordt geregistreerd, plaats de parameter aan Waar. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> IP-interface </td> 
   <td colname="col2"> <p>IP adres aan gebruik wanneer twee netwerkkaarten voor de toegang tot van twee verschillende netwerken beschikbaar zijn. </p> <p>Voorbeeld: <code>IP Interface = string: &lt; IP Address &gt;</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Poort </td> 
   <td colname="col2"> <p>Niet-veilige (HTTP) haven waarop de Server van het <span class="keyword"> Inzicht </span> of <span class="wintitle"> Repeater </span> luistert. De standaardpoort is 80. Als u de waarde 0 invoert, worden niet-beveiligde verbindingen uitgeschakeld. </p> <p>Voorbeeld: <code>Port = int: 80</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> SSL-CIFERS </td> 
   <td colname="col2"> Sommige omgevingen vereisen een sterkere communicatiebeveiliging dan andere. Als u een specifieke SSL cipher reeks wilt gebruiken, kunt u het met deze parameter specificeren. <p>Voorbeeld: <code>SSL Ciphers = string: AES256-SHA256</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> SSL-poort </td> 
   <td colname="col2"> <p>Veilige (via SSL) poort waarop de <span class="keyword"> Insight Server </span> of <span class="wintitle"> Repeater </span> luistert. De standaardpoort is 443. Als u de waarde 0 invoert, worden beveiligde verbindingen uitgeschakeld. </p> <p>Voorbeeld: <span class="filepath"></span> </p> <code>SSL Port = int: 443</code> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <i>n=</i>LoggingServer: </td> 
   <td colname="col2"> Rubriek voor instellingen van Logging Server. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Naam klant </td> 
   <td colname="col2"> <p>Naam van klant die wordt weergegeven voor niet-opgegeven klanten in administratieve waarschuwingen, zoals in het volgende voorbeeld: </p> <p>"Geen gegevens ontvangen van sensor XYZ voor klant "Niet gespecificeerd"in 15." </p> <p>Voorbeeld: <code> 1&nbsp;=&nbsp;LoggingServer:&nbsp; 
      &nbsp;&nbsp;Customer&nbsp;Name&nbsp;=&nbsp;string:&nbsp;CompanyAB </code> </p> <p>In het bovenstaande voorbeeld zouden administratieve waarschuwingen voor niet-opgegeven klanten nu als volgt luiden: </p> <p>"Geen gegevens ontvangen van sensor XYZ voor klant "CompanyAB" in 15." </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <i>n=</i>FileServer: </p> <p> Lokaal pad = tekenreeks: Logbestanden\\ </p> </td> 
   <td colname="col2"> <p>Map waarin u de logbestanden wilt opslaan. </p> <p>Voorbeeld: </p> <code> 9&nbsp;=&nbsp;FileServer:&nbsp; 
     &nbsp;&nbsp;Local&nbsp;Path&nbsp;=&nbsp;string:&nbsp;Logs\\ </code> <p>Als u deze map wilt kunnen openen vanuit het <span class="wintitle"> Server Files Manager </span>, moet de locatie die in deze parameter is opgegeven, overeenkomen met de locatie die u opgeeft in de parameter Log Paths in het <span class="filepath"> Log Processing.cfg- </span> bestand. Voor meer informatie over het wijzigen van de folder van Logboeken in het <span class="filepath"> Logboek Processing.cfg- </span> dossier, zie het hoofdstuk van het Dossier van de Configuratie van de Verwerking van het Logboek van de Gids <i>van de Configuratie van de</i>Dataset. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <i>n=</i>FileServer: </p> <p> Lokaal pad = tekenreeks: Audit\\ </p> </td> 
   <td colname="col2"> <p>Map waaraan u de controlelogboeken wilt toewijzen. </p> <p>Voorbeeld: </p> <code> 5&nbsp;=&nbsp;FileServer:&nbsp; 
     &nbsp;&nbsp;Local&nbsp;Path&nbsp;=&nbsp;string:&nbsp;Audit\\ </code> <p>Opmerking:  <p>U kunt controlelogboeken toewijzen aan een ander lokaal station (voorbeeld: <span class="filepath"> tekenreeks: P:\\Audit\\ </span>), maar wijs geen controlelogboeken aan een netwerkaandrijving toe. </p> <p>Als u toegang tot deze map wilt krijgen vanuit de <span class="wintitle"> Server Files Manager </span>, moet de locatie die in deze parameter is opgegeven, overeenkomen met de locatie die u in de parameter Directory van het Access Log in dit bestand hebt opgegeven. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <i>n=</i>NormalizeServer: </td> 
   <td colname="col2"> <p>Deze parameter is slechts op de Server van het <span class="keyword"> Inzicht van toepassing </span>. </p> <p>Voor meer informatie over het specificeren van de Gecentraliseerde Server van de Normalisatie voor uw <span class="keyword"> cluster van de Server van het Inzicht, zie het hoofdstuk van het Dossier van de Configuratie van de Logverwerking van de </span> Gids <i></i>van de Configuratie van de Dataset. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <i>n=</i>ReportStatusServer: </p> <p> URI = tekenreeks: /ReportStatus.vsp </p> </td> 
   <td colname="col2"> <p>Deze parameter is slechts op de Server van het <span class="keyword"> Inzicht van toepassing </span>. </p> <p>Laat u toe om de <span class="keyword"> status van het Rapport in de Gedetailleerde interface van de Status voor de Server van het </span> Inzicht te bekijken <span class="keyword"> </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>
