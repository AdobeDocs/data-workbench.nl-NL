---
description: Nadat de HTML van een pagina door een browser wordt gevraagd, verzoekt browser de ingebedde voorwerpen die in HTML van die pagina van een Webserver van verwijzingen worden voorzien om de pagina in te vullen die door browser wordt getoond.
title: Verzoeken om ingesloten objecten verkrijgen (paginatags)
uuid: 7fe561d1-aa5a-4ac9-82ba-aa27c7d208dd
exl-id: 593e49bc-9619-4e85-8ce3-2e9d23d175c9
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '604'
ht-degree: 1%

---

# Aanvragen voor ingesloten objecten ophalen (paginatags){#acquiring-embedded-object-requests-page-tags}

Nadat de HTML van een pagina door een browser wordt gevraagd, verzoekt browser de ingebedde voorwerpen die in HTML van die pagina van een Webserver van verwijzingen worden voorzien om de pagina in te vullen die door browser wordt getoond.

Dergelijke ingesloten objectaanvragen zijn doorgaans aanvragen voor afbeeldingsbestanden of JavaScript-bestanden, hoewel er momenteel honderden of misschien duizenden typen ingesloten objecten op internet worden gebruikt. Veel van deze ingebedde objecten verzoeken zijn over het algemeen niet nuttig in het analyseren van of het melden van de bedrijfsactiviteit van een Website; veel van dergelijke verzoeken zijn derhalve niet wenselijk voor verwerving , tenzij zij een specifiek bedrijfsdoel hebben , zoals het aanbieden van een advertentie of het nemen van een andere meting van de activiteit van de locatie .

Een afbeelding kan bijvoorbeeld een advertentie zijn en u wilt waarschijnlijk weten dat de advertentie onder de indruk is van een bezoeker. Een JavaScript-fragment wordt mogelijk gebruikt om te meten of de specifieke browser een bepaalde eigenschap heeft en dit naar een [!DNL Sensor] doorgeeft voor aankoop. Elke pagina op een site kan 10 of 100 ingesloten objectaanvragen bevatten. Als een site de loginformatie voor elk van deze aanvragen opslaat, wordt de hoeveelheid gegevensopslag die nodig is om de loggegevens beschikbaar te houden voor toekomstige analyse vermenigvuldigd met het aantal ingesloten objectaanvragen voor elke gevraagde pagina. Om deze reden, [!DNL Site] laat u de verzoeken houden die voor analyse belangrijk zijn en anderen verwerpen alvorens u onnodige opslagkosten aangaat.

Door de functie van de opheffing te gebruiken die in de inhoud-type het filtreren mogelijkheden van [!DNL Sensor] (toevoegend &quot;Log=1&quot;aan het vraagkoord van een ingebedde objecten verzoek URL) wordt verstrekt, kan dat bepaalde ingebedde objecten verzoek en de verwante metingsgegevens worden verworven zonder de plaatsleider te vereisen om alle verzoeken van dat type op te slaan (bijvoorbeeld, alle `<image>` verzoeken).

[!DNL Sensor] verzamelt de meetgegevens in de volgende tabel voor elk ingesloten objectverzoek van de webserver, ervan uitgaande dat dit niet  [!DNL Sensor] is geconfigureerd om het uit te filteren of dat het filter is overschreven. De verzamelde informatie heeft betrekking op de bezoeker en de sessie en volgende sessies via de logitems van het x-trackingid- of cs(cookie)-logboek.

<table id="table_11BE08A798E743EC8E76F738F0CE5884"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> W3C-naam </th> 
   <th colname="col2" class="entry"> Gegevens verzameld </th> 
   <th colname="col3" class="entry"> Toelichting </th> 
   <th colname="col4" class="entry"> Voorbeeld </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> x-trackingid </td> 
   <td colname="col2"> Tracking-id (unieke bezoeker) </td> 
   <td colname="col3"> Identifier gelezen van een cookie die door <span class="wintitle"> Sensor </span> op eerste verzoek in de browser van de gebruiker is geplaatst </td> 
   <td colname="col4"> V1st=3C94007B4E01F9C2 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Datum </p> <p>Tijd </p> </td> 
   <td colname="col2"> Tijdstempel </td> 
   <td colname="col3"> Tijdstip waarop het verzoek door de server werd verwerkt (bij precisie 100 ns; nauwkeurigheid is afhankelijk van serveromgeving en NTP) </td> 
   <td colname="col4"> 2002-11-21 17:21:45.123 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> sc (inhoudstype) </td> 
   <td colname="col2"> Inhoudstype </td> 
   <td colname="col3"> Type object dat door server wordt geretourneerd </td> 
   <td colname="col4"> text/html </td> 
  </tr> 
  <tr> 
   <td colname="col1"> sc-status </td> 
   <td colname="col2"> HTTP Response Status Code </td> 
   <td colname="col3"> Numerieke code die is gegenereerd door de server die de status van de reactie van de HTTP-server aangeeft </td> 
   <td colname="col4"> 200 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> cs-uri-stem </td> 
   <td colname="col2"> URI Stem </td> 
   <td colname="col3"> Het "stam"gedeelte van URI die door de cliënt wordt gevraagd </td> 
   <td colname="col4"> pagedir/page.asp </td> 
  </tr> 
  <tr> 
   <td colname="col1"> c-ip </td> 
   <td colname="col2"> Client IP </td> 
   <td colname="col3"> IP-adres van de verzoekende client </td> 
   <td colname="col4"> 127.0.0.1 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> s-dns </td> 
   <td colname="col2"> Domeinnaam server </td> 
   <td colname="col3"> Domeinnaam van de webserver die de aanvraag verwerkt </td> 
   <td colname="col4"> <span class="filepath"> www.domain.com  </span> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> cs(referentie) </td> 
   <td colname="col2"> URL verwijzen </td> 
   <td colname="col3"> Inhoud van het veld HTTP-referentie die door de client is verzonden </td> 
   <td colname="col4"> <span class="filepath"> http://www.referringsite.com  </span> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> cs (user-agent) </td> 
   <td colname="col2"> User Agent </td> 
   <td colname="col3"> Apparaat dat wordt gebruikt om een aanvraag bij de HTTP-server in te dienen </td> 
   <td colname="col4"> <p>Mozilla/4.0+(compatibel;+MSIE+6.0; </p> <p>+Windows+NT+5.1) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> cs(cookie) </td> 
   <td colname="col2"> Clientcookies van domein </td> 
   <td colname="col3"> Inhoud van alle cookies van de gebruiker voor de site </td> 
   <td colname="col4"> <p>KL_TC1 1038058778312 </p> <p>KL972 x1038058778312282052 </p> <p>KL_PVKL972 0 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> cs-uri-query </td> 
   <td colname="col2"> Tekenreeks query </td> 
   <td colname="col3"> Het gedeelte van de querytekenreeks, indien aanwezig, van de URI die door de client wordt aangevraagd </td> 
   <td colname="col4"> PAGENAME=dynamic1&amp;link=3001 </td> 
  </tr> 
 </tbody> 
</table>
