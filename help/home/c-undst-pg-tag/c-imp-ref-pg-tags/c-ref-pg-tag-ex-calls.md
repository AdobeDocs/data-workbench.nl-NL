---
description: De oproep tot het uitvoeren van de referentiepagina-tag wordt ingevoegd in webpagina's waarvoor u meetgegevens wilt verzamelen.
title: Aanroepen tot uitvoering van referentiepagina-tag toevoegen
uuid: 8c682649-d1b1-40a6-a2b2-4ff5a92b732f
exl-id: a4f9ab2b-50e8-4e0b-9c87-80dffb697316
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '356'
ht-degree: 0%

---

# Aanroepen tot uitvoering van referentiepagina-tag toevoegen{#adding-reference-page-tag-execution-calls}

De oproep tot het uitvoeren van de referentiepagina-tag wordt ingevoegd in webpagina&#39;s waarvoor u meetgegevens wilt verzamelen.

Het moet worden opgenomen in de hoofdtekst van het HTML-document en kan, indien van toepassing, worden geplaatst in een algemene include-voettekst. [!DNL Reference Page Tag Execution Call] kan door uw team worden gewijzigd om extra informatie te verzamelen die tijdens vereisten het verzamelen van vergaderingen met het team van de Diensten van de Raadpleging van Adobe zou kunnen worden geïdentificeerd.

Voer de volgende stappen uit om het verzamelen van gegevens te vergemakkelijken via de [!DNL Reference Page Tag]:

1. Kopieer de volgende code naar de hoofdtekst van het HTML-document:

   ```
   <!--//BEGIN REFERENCE PAGE TAG--> 
   <script language="javascript"> 
   var vlc = "0" //Capture Link Click  1=TRUE, 0=FALSE 
   var v = {}; 
   </script> 
   
   <!--//MODIFIY PATH TO ZIG.JS--> 
   <script language="javascript" src="/path/to/zig.js" type="text/javascript"></script> 
   <!--//END REFERENCE PAGE TAG--> 
   
   <noscript> 
   <img src="/path/to/zag.gif?Log=1&v_jd=1" border="0" width="1" height="1"/> 
   </noscript> 
   <!-- END REFERENCE PAGE TAG-->
   ```

1. Wijzig de weg aan de plaats van [!DNL zig.js] en [!DNL zag.gif] dossiers. Bijvoorbeeld:

   ```
   //www.mysite.com/scripts/zig.js 
   //www.mysite.com/images/zag.gif 
   ```

Zorg ervoor dat de juiste HTTP Cache-Control headers op uw webserver zijn ingesteld om ervoor te zorgen dat de [!DNL zig.js]en [!DNL zag.gif] bestanden niet in de cache van de browser worden geplaatst. U kunt de HTTP Cache-Control koptekstinformatie instellen met een van twee methoden. De eerste methode is het instellen van een HTTP-header via de webserver. De tweede methode is het instellen van een HTTP-header voor elke specifieke pagina of elk ingesloten object met behulp van een script. Met de scriptmethode moet de webpagina zijn gemaakt met een programmeertaal zoals JSP of ASP. De pagina is dan gescripteerd zodat het de aangewezen kopbalinformatie verzendt. Deze methode kent twee duidelijke nadelen: 1) alle pagina&#39;s moeten worden gecodeerd om de header te verzenden, en 2) de pagina&#39;s mogen geen statische HTML zijn, wat enig effect heeft op de prestaties van de webserver.

De websites die op Microsoft IIS lopen kunnen de aangewezen kopbal van HTTP door de Console van het Beheer van Microsoft toevoegen. Websites die via Netscape iPlanet Web Servers worden aangeboden, kunnen dit bereiken door het [!DNL obj.conf]-bestand in de configuratiemap van de site te bewerken. De Apache Web Server verstrekt webmasters de capaciteit om de kopballen van HTTP aan te passen gebruikend de inbegrepen module mod_headers waar AOLServer klantgericht door het gebruik van modules van TCP wordt. Voordat u HTTP Cache-Control headers implementeert, moet u de documentatie raadplegen die specifiek is voor uw webserverplatform.

Over het algemeen zou de kopbal van HTTP als volgt moeten worden gestructureerd:

```
Cache-Control: no-cache 
Pragma: no-cache 
Expires: -1
```
