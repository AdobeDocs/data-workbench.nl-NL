---
description: Websites die zijn gemaakt met behulp van Flash vereisen speciale aandacht voor het vastleggen van bezoekersacties die worden uitgevoerd in de rich media-inhoud.
title: Bezoekersactiviteit bijhouden binnen inhoud van Flash-rijke media
uuid: fe2e75eb-0897-4f63-b582-b4f1fdce02a1
exl-id: f51c7034-a7fd-4575-80e1-18fc6513ca2b
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '713'
ht-degree: 2%

---

# Bezoekersactiviteit bijhouden binnen inhoud van Flash-rijke media{#tracking-visitor-activity-within-flash-rich-media-content}

{{eol}}

Websites die zijn gemaakt met behulp van Flash vereisen speciale aandacht voor het vastleggen van bezoekersacties die worden uitgevoerd in de rich media-inhoud.

Gebruiken [!DNL Flash] ActionScript, kunt u eenvoudige wijzigingen aanbrengen in uw bestaande [!DNL Flash] films waarmee u alle interactie van de bezoeker met de film kunt bijhouden, zoals knopklikken of muisbewegingen.

Om de activiteiten van de bezoeker binnen uw [!DNL Flash] film, volgt u de onderstaande stappen:

1. Voeg de volgende ActionScript code aan uw film toe. Deze code vertegenwoordigt een functie die door gebeurtenissen binnen [!DNL Flash] film die u wilt bijhouden.

   ```
   // FLASH TAG CODE BEGIN
   var FLASHTAGURI = "[PATH_TO_WEB_SERVER]/flashtag.txt";
   function tag(PAGENAME,VARIABLES) {
   loadVariablesNum(FLASHTAGURI+”?”+"PAGENAME="+PAGENAME+"&"+VARIABLES,0);
   }
   // FLASH TAG CODE END
   ```

1. Een leeg bestand maken met de naam [!DNL flashtag.txt] en plaats het bestand op uw webservers.
1. Vervang \[[!DNL PATH_TO_WEB_SERVER]\] plaatsaanduiding met het volledig gekwalificeerde of relatieve pad naar de locatie van het [!DNL flashtag.txt] bestand. Bijvoorbeeld:

   ```
   var FLASHTAGURI = https://www.mysite.com/flashtag/flashtag.txt”;
   ```

1. Voeg de volgende ActionScript-code toe aan alle gebeurtenissen die moeten worden bijgehouden. Deze code vertegenwoordigt een functieaanroep die wordt gebruikt om gegevens over de gebeurtenis vast te leggen:

   ```
   on(release) {tag("[PUT_PAGE_NAME_HERE]","[PUT_ADDITIONAL_VAR_HERE]");}
   ```

   In dit voorbeeld wordt het gebruik van de gebeurtenis on(release) getoond. nochtans, kan de markering () functie door om het even welke gebeurtenis worden van verwijzingen voorzien die u kunt willen volgen, zoals on (pers), on (rollover), on (rollout), of on (keypress) gebeurtenis.

   De \[[!DNL PUT_PAGE_NAME_HERE]De tijdelijke aanduiding \] moet worden vervangen door een tekenreeks die de naam vertegenwoordigt van de pagina of gebeurtenis die u bijhoudt. De \[[!DNL PUT_PAGE_NAME_HERE]\]variabele kan handmatig of via een verwijzing naar een variabele worden gewijzigd om een unieke naam aan te duiden voor de pagina of gebeurtenis in het dialoogvenster [!DNL Flash] toepassing. De waarde die de \[[!DNL PUT_PAGE_NAME_HERE]\] placeholder kan uit een eenvoudige naam bestaan of kan worden gestructureerd om een hiërarchische structuur te vertegenwoordigen gelijkend op volledige URI. Bijvoorbeeld:

   ```
   on(release) {tag(“/about_us/index.swf","[PUT_ADDITIONAL_VAR_HERE]");}
   ```

   Adobe raadt u aan om vóór de implementatie van code een schriftelijke specificatie voor paginanamen en gebeurtenisnamen samen te stellen om de afstemming van bedrijfsvereisten en ontwikkelingstaken te vergemakkelijken en het potentieel voor extra ontwikkelingscycli te beperken.

1. Indien gewenst kunnen extra variabelen worden verzameld en gekoppeld aan pagina&#39;s of gebeurtenissen in het dialoogvenster [!DNL Flash] film. Hiervoor vervangt u de \[[!DNL PUT_ADDITIONAL_VAR_HERE]\] tijdelijke aanduiding met een set naam=waarde-paren gescheiden door een en-teken (&amp;). Bijvoorbeeld:

   ```
   on(release) {tag(“/about_us/index.swf"," var1=value1&var2=value2");}
   ```

   De variabelen kunnen handmatig of via een verwijzing naar een variabele worden gewijzigd om extra kenmerken aan te duiden die moeten worden verzameld en gekoppeld aan de pagina of gebeurtenis. Als er geen toepasselijke aanvullende variabelen zijn om te verzamelen, verwijdert u \[[!DNL PUT_ADDITIONAL_VAR_HERE]\].

   Uw instelling voor het bijhouden van bezoekers binnen [!DNL Flash] rich media content is nu voltooid. Wanneer de gebeurtenis wordt aangeroepen, wordt de tag [!DNL (PAGENAME,VARIABLES)] wordt aangeroepen, waardoor een HTTP-aanvraag wordt gedaan voor het volgende bestand. Deze functie wordt aangeroepen naast andere functies die kunnen worden geactiveerd zoals gedefinieerd in uw [!DNL Flash] film:

   ```
   https://www.mysite.com/flashtag/flashtag.txt?PAGENAME=/about_us/index.swf&var1=value1&var2=value2
   ```

De HTTP-aanvraag die het resultaat is van de [!DNL Flash] De functie ActionScript van de markering leidt ertoe dat de volgende informatie met betrekking tot elke gebeurtenis binnen wordt verzameld [!DNL Flash] film. De laatste rij in de tabel (W3C-naam cs-uri-query) vertegenwoordigt de informatie die wordt verzameld voor de extra variabelen die in de functieaanroep zijn opgegeven.

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
   <td colname="col3"> Id gelezen uit een cookie die door de gebruiker in de browser is geplaatst <span class="wintitle"> Sensor </span> inzake het eerste verzoek van de bezoeker </td>
   <td colname="col4"> v1st=3C94007B4E01F9C2 </td>
  </tr>
  <tr>
   <td colname="col1"> <p>Datum </p> <p>Tijd </p> </td>
   <td colname="col2"> Tijdstempel </td>
   <td colname="col3"> Tijdstip waarop het verzoek door de server werd verwerkt (bij precisie 100 ns; nauwkeurigheid is afhankelijk van serveromgeving en NTP) </td>
   <td colname="col4"> 2002-11-21 17:21:45,123 </td>
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
