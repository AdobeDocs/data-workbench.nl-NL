---
description: Nadat HTML van een pagina door browser wordt gevraagd, verzoekt browser om de ingebedde voorwerpen die in HTML van die pagina van verwijzingen worden voorzien van een Webserver om de pagina in te vullen die door browser wordt getoond.
solution: Analytics
title: Het verwerven van Ingebedde Voorwerp Verzoeken (de Markeringen van de Pagina)
topic: Data workbench
uuid: 7fe561d1-aa5a-4ac9-82ba-aa27c7d208dd
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Het verwerven van Ingebedde Voorwerp Verzoeken (de Markeringen van de Pagina){#acquiring-embedded-object-requests-page-tags}

Nadat HTML van een pagina door browser wordt gevraagd, verzoekt browser om de ingebedde voorwerpen die in HTML van die pagina van verwijzingen worden voorzien van een Webserver om de pagina in te vullen die door browser wordt getoond.

Dergelijke ingebedde objecten verzoeken zijn het meest meestal verzoeken om beelddossiers of dossiers JavaScript, hoewel er honderden of misschien duizenden types van ingebedde voorwerpen vandaag die op Internet worden gebruikt zijn. Veel van deze ingebedde objecten verzoeken zijn over het algemeen niet nuttig bij het analyseren van of het melden van over de bedrijfsactiviteit van een plaats van Internet; veel van dergelijke verzoeken zijn derhalve niet wenselijk voor verwerving , tenzij zij een specifiek zakelijk doel hebben , zoals het aanbieden van een advertentie of het verrichten van een andere meting van de activiteit ter plaatse .

Bijvoorbeeld, kan een beeld een reclame zijn, en u kunt willen weten dat de reclame op een bezoeker onder de indruk was. Een fragment JavaScript kan in gebruik zijn om een meting te nemen dat bepaalde browser een bepaald kenmerk heeft en het terug naar een [!DNL Sensor] aanwinst overgaat. Elke pagina op een plaats kan 10 of 100 ingebedde objecten verzoeken in het hebben. Als een plaats de logboekinformatie voor elk van deze verzoeken opslaat, wordt de hoeveelheid gegevensopslag nodig om de logboekgegevens beschikbaar te houden voor toekomstige analyse vermenigvuldigd met het aantal ingebedde objecten verzoeken voor elke gevraagde pagina. Om deze reden, [!DNL Site] laat u de verzoeken houden die voor analyse belangrijk zijn en anderen verwerpen alvorens u onnodige opslagkosten veroorzaakt.

Door de opheffingseigenschap te gebruiken die in de inhoud-type het filtreren mogelijkheden van [!DNL Sensor] (toevoegend &quot;Log=1&quot;aan het vraagkoord van een ingebed objecten verzoek URL) wordt verstrekt, kan dat bepaalde ingebedde objecten verzoek en de verwante metingsgegevens worden verworven zonder de plaatsmanager te vereisen om alle verzoeken van dat type op te slaan (bijvoorbeeld, allen <image> verzoeken).

[!DNL Sensor] verzamelt de meetgegevens in de volgende lijst voor elk ingebed objecten verzoek dat van de Webserver wordt gemaakt, veronderstellend dat niet [!DNL Sensor] wordt gevormd om het uit te filtreren of dat de filter is met voeten getreden. De verzamelde informatie is verwant met de bezoeker en de zitting en de verdere zittingen door de x-trackingid of cs (koekje) logboekingang.

<table id="table_11BE08A798E743EC8E76F738F0CE5884"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> W3C-naam </th> 
   <th colname="col2" class="entry"> Verzamelde gegevens </th> 
   <th colname="col3" class="entry"> Toelichting </th> 
   <th colname="col4" class="entry"> Voorbeeld </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> x-trackingid </td> 
   <td colname="col2"> Tracking Identifier (unieke bezoeker) </td> 
   <td colname="col3"> Herkenningsteken dat van een koekje wordt gelezen dat in browser van de gebruiker door <span class="wintitle"> Sensor </span> op aanvankelijke verzoek wordt geplaatst </td> 
   <td colname="col4"> V1st=3C94007B4E01F9C2 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Datum </p> <p>Tijd </p> </td> 
   <td colname="col2"> Tijdstempel </td> 
   <td colname="col3"> Tijdstip waarop het verzoek door server (bij precisie 100ns werd verwerkt; nauwkeurigheid hangt van servermilieu en NTP af) </td> 
   <td colname="col4"> 2002-11-21 17:21:45.123 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> SC (inhoudstype) </td> 
   <td colname="col2"> Content type </td> 
   <td colname="col3"> Type voorwerp dat van server is teruggekeerd </td> 
   <td colname="col4"> tekst/html </td> 
  </tr> 
  <tr> 
   <td colname="col1"> SC-status </td> 
   <td colname="col2"> HTTP-responsstatuscode </td> 
   <td colname="col3"> Numerieke code die door de server wordt geproduceerd die nota neemt van het statuut van de reactie van de server van HTTP </td> 
   <td colname="col4"> 200 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> cs-uri-stengel </td> 
   <td colname="col2"> URI Stem </td> 
   <td colname="col3"> Het "stamgedeelte"gedeelte van URI die door de cliënt wordt gevraagd </td> 
   <td colname="col4"> pagedir/page.asp </td> 
  </tr> 
  <tr> 
   <td colname="col1"> c-ip </td> 
   <td colname="col2"> IP client </td> 
   <td colname="col3"> IP-adres van de verzoekende client </td> 
   <td colname="col4"> 127.0.0.1 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> s-dns </td> 
   <td colname="col2"> Serverdomeinnaam </td> 
   <td colname="col3"> De naam van het domein van de Webserver die het verzoek verwerkt </td> 
   <td colname="col4"> <span class="filepath"> www.domain.com </span> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> cs (referentie) </td> 
   <td colname="col2"> URL verwijzen </td> 
   <td colname="col3"> Inhoud van het de verwijzingsgebied van HTTP dat door de cliënt wordt verzonden </td> 
   <td colname="col4"> <span class="filepath"> http://www.referringsite.com </span> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> cs (gebruikersagent) </td> 
   <td colname="col2"> Gebruikersagent </td> 
   <td colname="col3"> Apparaat dat wordt gebruikt om een verzoek aan de server van HTTP in te dienen </td> 
   <td colname="col4"> <p>Mozilla/4.0+(compatibel;+MSIE+6.0; </p> <p>+Windows+NT+5.1) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> cs (cookie) </td> 
   <td colname="col2"> Clientcookies van domein </td> 
   <td colname="col3"> Inhoud van alle koekjes van de gebruiker voor de plaats </td> 
   <td colname="col4"> <p>KL_TC1 1038058778312 </p> <p>KL972 x1038058778312282052 </p> <p>KL_PVKL972 0 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> cs-uri-query </td> 
   <td colname="col2"> Query-tekenreeks </td> 
   <td colname="col3"> Het gedeelte van het vraagkoord, als om het even welk, van URI gevraagd door de cliënt </td> 
   <td colname="col4"> PAGENAME=dynamic1&amp;link=3001 </td> 
  </tr> 
 </tbody> 
</table>

