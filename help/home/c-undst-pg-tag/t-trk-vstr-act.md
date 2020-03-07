---
description: De websites die gebruikend Flits worden ontworpen vereisen speciale aandacht met betrekking tot de vangst van bezoekersacties die binnen de rijke media inhoud worden uitgevoerd.
solution: Analytics
title: Het volgen van de Activiteit van de Bezoeker binnen de Inhoud van de Media van de Flits Rich
topic: Data workbench
uuid: fe2e75eb-0897-4f63-b582-b4f1fdce02a1
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Het volgen van de Activiteit van de Bezoeker binnen de Inhoud van de Media van de Flits Rich{#tracking-visitor-activity-within-flash-rich-media-content}

De websites die gebruikend Flits worden ontworpen vereisen speciale aandacht met betrekking tot de vangst van bezoekersacties die binnen de rijke media inhoud worden uitgevoerd.

Gebruikend [!DNL Flash] ActionScript, kunt u eenvoudige veranderingen in uw bestaande [!DNL Flash] films aanbrengen om het volgen van alle bezoekersinteractie met de film, zoals knoopkliks of muisbewegingen toe te staan.

Volg onderstaande stappen om het volgen van bezoekersactiviteiten in uw [!DNL Flash] film te vergemakkelijken:

1. Voeg de volgende code ActionScript aan uw film toe. Deze code vertegenwoordigt een functie die door gebeurtenissen binnen de [!DNL Flash] film kan worden geroepen die u wilt volgen.

   ```
   // FLASH TAG CODE BEGIN 
   var FLASHTAGURI = "[PATH_TO_WEB_SERVER]/flashtag.txt"; 
   function tag(PAGENAME,VARIABLES) { 
   loadVariablesNum(FLASHTAGURI+”?”+"PAGENAME="+PAGENAME+"&"+VARIABLES,0); 
   } 
   // FLASH TAG CODE END
   ```

1. Creeer een leeg dossier genoemd [!DNL flashtag.txt] en plaats het dossier op uw Webservers.
1. Binnen de functie in Stap 1, vervang [!DNL [PATH_TO_WEB_SERVER]] placeholder met volledig - gekwalificeerde of relatieve weg aan de plaats van het [!DNL flashtag.txt] dossier. Bijvoorbeeld:

   ```
   var FLASHTAGURI = http://www.mysite.com/flashtag/flashtag.txt”;
   ```

1. Voeg de volgende code ActionScript aan alle te volgen gebeurtenissen toe. Deze code vertegenwoordigt een functievraag die wordt gebruikt om gegevens over de gebeurtenis te vangen:

   ```
   on(release) {tag("[PUT_PAGE_NAME_HERE]","[PUT_ADDITIONAL_VAR_HERE]");}
   ```

   Dit voorbeeld illustreert het gebruik van de on(versie) gebeurtenis; nochtans, kan de markering () functie door om het even welke gebeurtenis worden van verwijzingen voorzien die u, zoals een on (pers), op (het omvergooien), op (uitlooptraject), of op (keypress) gebeurtenis kunt willen volgen.

   [!DNL [PUT_PAGE_NAME_HERE]] placeholder zou met een koord moeten worden vervangen dat de naam van de pagina of de gebeurtenis vertegenwoordigt die u volgt. De [!DNL [PUT_PAGE_NAME_HERE]]variabele kan of manueel of door veranderlijke verwijzing worden gewijzigd om een unieke naam voor de pagina of de gebeurtenis binnen de [!DNL Flash] toepassing aan te duiden. De waarde die [!DNL [PUT_PAGE_NAME_HERE]] vervangt placeholder kan uit een eenvoudige naam bestaan of kan worden gestructureerd om een hiërarchische structuur te vertegenwoordigen gelijkend op volledige URI. Bijvoorbeeld:

   ```
   on(release) {tag(“/about_us/index.swf","[PUT_ADDITIONAL_VAR_HERE]");}
   ```

   Adobe adviseert dat, voorafgaand aan codeplaatsing, u een geschreven specificatie voor paginanamen en gebeurtenisnamen compileert om de groepering van bedrijfsvereisten en ontwikkelingstaken te vergemakkelijken en het potentieel voor extra ontwikkelingscycli te verminderen.

1. Indien gewenst, kunnen de extra variabelen worden verzameld en met pagina&#39;s of gebeurtenissen in de [!DNL Flash] film worden geassocieerd. Om dit te doen, vervang [!DNL [PUT_ADDITIONAL_VAR_HERE]] placeholder met een reeks naam=value paren die door een ampersand (&amp;) worden gescheiden. Bijvoorbeeld:

   ```
   on(release) {tag(“/about_us/index.swf"," var1=value1&var2=value2");}
   ```

   De variabelen kunnen of manueel of door veranderlijke verwijzing worden gewijzigd om extra attributen aan te duiden die met de pagina of de gebeurtenis moeten worden verzameld en worden geassocieerd. Als er geen toepasselijke extra te verzamelen variabelen zijn, verwijder [!DNL [PUT_ADDITIONAL_VAR_HERE]].

   Uw opstelling van bezoeker het volgen binnen [!DNL Flash] rijke media inhoud is nu volledig. Wanneer de gebeurtenis wordt aangehaald, zal de markeringsfunctie worden geroepen, resulterend in een HTTP- verzoek dat voor het volgende dossier wordt ingediend. [!DNL (PAGENAME,VARIABLES)] Deze functie zal naast andere functies worden geroepen die kunnen worden teweeggebracht zoals die binnen uw [!DNL Flash] film worden bepaald:

   ```
   http://www.mysite.com/flashtag/flashtag.txt?PAGENAME=/about_us/index.swf&var1=value1&var2=value2
   ```

Het HTTP- verzoek dat uit de functie van ActionScript van de [!DNL Flash] Markering voortvloeit resulteert in de volgende informatie die met betrekking tot elke gebeurtenis binnen de [!DNL Flash] film wordt verzameld. De laatste rij in de lijst (de naam van W3C cs-uri-vraag) vertegenwoordigt de informatie die voor de extra variabelen wordt verzameld die in uw functievraag worden gespecificeerd.

<table id="table_A7ED9D38F36B4405947B2F48EA94D3C4"> 
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
   <td colname="col3"> Herkenningsteken dat van een koekje wordt gelezen dat in browser van de gebruiker door <span class="wintitle"> </span> Sensor op het aanvankelijke verzoek van de Bezoeker wordt geplaatst </td> 
   <td colname="col4"> v1st=3C94007B4E01F9C2 </td> 
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
   <td colname="col4"> Tekst/html </td> 
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
   <td colname="col3"> Het stamgedeelte van URI dat door de cliënt wordt gevraagd </td> 
   <td colname="col4"> /flashtag/flashtag.txt </td> 
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
   <td colname="col4"> www.mysite.com </td> 
  </tr> 
  <tr> 
   <td colname="col1"> cs (referentie) </td> 
   <td colname="col2"> URL verwijzen </td> 
   <td colname="col3"> Inhoud van het de verwijzingsgebied van HTTP dat door de cliënt wordt verzonden </td> 
   <td colname="col4"></td> 
  </tr> 
  <tr> 
   <td colname="col1"> cs (gebruikersagent) </td> 
   <td colname="col2"> Gebruikersagent </td> 
   <td colname="col3"> Apparaat dat wordt gebruikt om een verzoek aan de server van HTTP in te dienen </td> 
   <td colname="col4"> Mozilla/4.0+(compatibel;+MSIE+6.0; +Windows+NT+5.1) </td> 
  </tr> 
  <tr> 
   <td colname="col1"> cs (cookie) </td> 
   <td colname="col2"> Clientcookies van domein </td> 
   <td colname="col3"> Inhoud van alle koekjes van de gebruiker voor de plaats </td> 
   <td colname="col4"> <p>KL_TC1 1038058778312 </p> <p>KL972x1038058778312282052 </p> <p>KL_PVKL972 0 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> cs-uri-query </td> 
   <td colname="col2"> Query-tekenreeks </td> 
   <td colname="col3"> Het gedeelte van het vraagkoord, als om het even welk, van URI gevraagd door de cliënt </td> 
   <td colname="col4"> PAGENAME=/about_us/index.swf&amp;var1=value1&amp;var2=value2 </td> 
  </tr> 
 </tbody> 
</table>

