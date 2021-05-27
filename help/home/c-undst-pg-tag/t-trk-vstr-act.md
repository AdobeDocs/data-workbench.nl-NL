---
description: Websites die zijn gemaakt met behulp van Flash vereisen speciale aandacht voor het vastleggen van bezoekersacties die worden uitgevoerd in de rich media-inhoud.
title: Bezoekersactiviteit bijhouden binnen inhoud van Flash-rijke media
uuid: fe2e75eb-0897-4f63-b582-b4f1fdce02a1
exl-id: f51c7034-a7fd-4575-80e1-18fc6513ca2b
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '713'
ht-degree: 2%

---

# Bezoekersactiviteit bijhouden binnen Flash-rijke media-inhoud{#tracking-visitor-activity-within-flash-rich-media-content}

Websites die zijn gemaakt met behulp van Flash vereisen speciale aandacht voor het vastleggen van bezoekersacties die worden uitgevoerd in de rich media-inhoud.

Met [!DNL Flash] ActionScript kunt u eenvoudige wijzigingen aanbrengen in uw bestaande [!DNL Flash]-films om alle bezoekersinteracties met de film te kunnen bijhouden, zoals knopklikken of muisbewegingen.

Volg onderstaande stappen om het volgen van bezoekersactiviteiten in uw [!DNL Flash] film te vergemakkelijken:

1. Voeg de volgende ActionScript code aan uw film toe. Deze code vertegenwoordigt een functie die door gebeurtenissen binnen de [!DNL Flash] film kan worden geroepen die u wilt volgen.

   ```
   // FLASH TAG CODE BEGIN 
   var FLASHTAGURI = "[PATH_TO_WEB_SERVER]/flashtag.txt"; 
   function tag(PAGENAME,VARIABLES) { 
   loadVariablesNum(FLASHTAGURI+”?”+"PAGENAME="+PAGENAME+"&"+VARIABLES,0); 
   } 
   // FLASH TAG CODE END
   ```

1. Maak een leeg bestand met de naam [!DNL flashtag.txt] en plaats het bestand op uw webservers.
1. Vervang binnen de functie in Stap 1 de tijdelijke aanduiding \[[!DNL PATH_TO_WEB_SERVER]\] door het volledig gekwalificeerde of relatieve pad naar de locatie van het [!DNL flashtag.txt]-bestand. Bijvoorbeeld:

   ```
   var FLASHTAGURI = http://www.mysite.com/flashtag/flashtag.txt”;
   ```

1. Voeg de volgende ActionScript-code toe aan alle gebeurtenissen die moeten worden bijgehouden. Deze code vertegenwoordigt een functieaanroep die wordt gebruikt om gegevens over de gebeurtenis vast te leggen:

   ```
   on(release) {tag("[PUT_PAGE_NAME_HERE]","[PUT_ADDITIONAL_VAR_HERE]");}
   ```

   In dit voorbeeld wordt het gebruik van de gebeurtenis on(release) getoond. nochtans, kan de markering () functie door om het even welke gebeurtenis worden van verwijzingen voorzien die u kunt willen volgen, zoals on (pers), on (rollover), on (rollout), of on (keypress) gebeurtenis.

   De tijdelijke aanduiding \[[!DNL PUT_PAGE_NAME_HERE]\] moet worden vervangen door een tekenreeks die de naam vertegenwoordigt van de pagina of gebeurtenis die u bijhoudt. De variabele \[[!DNL PUT_PAGE_NAME_HERE]\]kan of manueel of door veranderlijke verwijzing worden gewijzigd om een unieke naam voor de pagina of de gebeurtenis binnen &lt;a1 aan te duiden/> toepassing. [!DNL Flash] De waarde die de tijdelijke aanduiding \[[!DNL PUT_PAGE_NAME_HERE]\] vervangt, kan bestaan uit een eenvoudige naam of kan zodanig zijn gestructureerd dat deze een hiërarchische structuur vertegenwoordigt die lijkt op een volledige URI. Bijvoorbeeld:

   ```
   on(release) {tag(“/about_us/index.swf","[PUT_ADDITIONAL_VAR_HERE]");}
   ```

   Adobe raadt u aan om vóór de implementatie van code een schriftelijke specificatie voor paginanamen en gebeurtenisnamen samen te stellen om de afstemming van bedrijfsvereisten en ontwikkelingstaken te vergemakkelijken en het potentieel voor extra ontwikkelingscycli te beperken.

1. Indien gewenst kunnen extra variabelen worden verzameld en gekoppeld aan pagina&#39;s of gebeurtenissen in de [!DNL Flash]-film. Hiervoor vervangt u de tijdelijke aanduiding \[[!DNL PUT_ADDITIONAL_VAR_HERE]\] door een set naam=waarde-paren, gescheiden door een en-teken (&amp;). Bijvoorbeeld:

   ```
   on(release) {tag(“/about_us/index.swf"," var1=value1&var2=value2");}
   ```

   De variabelen kunnen handmatig of via een verwijzing naar een variabele worden gewijzigd om extra kenmerken aan te duiden die moeten worden verzameld en gekoppeld aan de pagina of gebeurtenis. Als er geen toepasselijke aanvullende variabelen zijn om te verzamelen, verwijdert u \[[!DNL PUT_ADDITIONAL_VAR_HERE]\].

   Uw instelling voor het bijhouden van bezoekers binnen [!DNL Flash] rich media-inhoud is nu voltooid. Wanneer de gebeurtenis wordt aangeroepen, wordt de functie tag [!DNL (PAGENAME,VARIABLES)] aangeroepen, wat resulteert in een HTTP-aanvraag voor het volgende bestand. Deze functie zal naast andere functies worden geroepen die zoals bepaald binnen uw [!DNL Flash] film kunnen teweegbrengen:

   ```
   http://www.mysite.com/flashtag/flashtag.txt?PAGENAME=/about_us/index.swf&var1=value1&var2=value2
   ```

De HTTP-aanvraag die voortvloeit uit de functie [!DNL Flash] Tag ActionScript, leidt ertoe dat de volgende informatie wordt verzameld met betrekking tot elke gebeurtenis binnen de film [!DNL Flash]. De laatste rij in de tabel (W3C-naam cs-uri-query) vertegenwoordigt de informatie die wordt verzameld voor de extra variabelen die in de functieaanroep zijn opgegeven.

<table id="table_A7ED9D38F36B4405947B2F48EA94D3C4"> 
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
   <td colname="col3"> Identifier gelezen van een cookie die door <span class="wintitle"> Sensor </span> op eerste verzoek van bezoeker in de browser van de gebruiker is geplaatst. </td> 
   <td colname="col4"> v1st=3C94007B4E01F9C2 </td> 
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
   <td colname="col4"> Tekst/html </td> 
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
   <td colname="col3"> Het stamgedeelte van de URI die door de client wordt aangevraagd </td> 
   <td colname="col4"> /flashtag/flashtag.txt </td> 
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
   <td colname="col4"> www.mysite.com </td> 
  </tr> 
  <tr> 
   <td colname="col1"> cs(referentie) </td> 
   <td colname="col2"> URL verwijzen </td> 
   <td colname="col3"> Inhoud van het veld HTTP-referentie die door de client is verzonden </td> 
   <td colname="col4"></td> 
  </tr> 
  <tr> 
   <td colname="col1"> cs (user-agent) </td> 
   <td colname="col2"> User Agent </td> 
   <td colname="col3"> Apparaat dat wordt gebruikt om een aanvraag bij de HTTP-server in te dienen </td> 
   <td colname="col4"> Mozilla/4.0+(compatibel;+MSIE+6.0; +Windows+NT+5.1) </td> 
  </tr> 
  <tr> 
   <td colname="col1"> cs(cookie) </td> 
   <td colname="col2"> Clientcookies van domein </td> 
   <td colname="col3"> Inhoud van alle cookies van de gebruiker voor de site </td> 
   <td colname="col4"> <p>KL_TC1 1038058778312 </p> <p>KL972x1038058778312282052 </p> <p>KL_PVKL972 0 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> cs-uri-query </td> 
   <td colname="col2"> Tekenreeks query </td> 
   <td colname="col3"> Het gedeelte van de querytekenreeks, indien aanwezig, van de URI die door de client wordt aangevraagd </td> 
   <td colname="col4"> PAGENAME=/about_us/index.swf&amp;var1=value1&amp;var2=value2 </td> 
  </tr> 
 </tbody> 
</table>
