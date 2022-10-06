---
description: De referentiepagina-tag bestaat uit een script voor de uitvoering van een paginalabel dat zich op een webserver bevindt. Wanneer deze tag wordt aangeroepen, resulteert dit in de verzameling van alle client-side gegevens voor de pagina die door de sitebezoeker is aangevraagd.
title: Het script voor de uitvoering van de referentiepagina-tag bewerken
uuid: 0db00b89-e420-423d-9b88-8b724baa828f
exl-id: bc922b59-716e-4e92-84b5-59a52620df03
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '231'
ht-degree: 1%

---

# Het script voor de uitvoering van de referentiepagina-tag bewerken{#editing-the-reference-page-tag-execution-script}

{{eol}}

De referentiepagina-tag bestaat uit een script voor de uitvoering van een paginalabel dat zich op een webserver bevindt. Wanneer deze tag wordt aangeroepen, resulteert dit in de verzameling van alle client-side gegevens voor de pagina die door de sitebezoeker is aangevraagd.

U kunt de [!DNL Reference Page Tag Execution Script] om extra informatie te verzamelen die tijdens vereisten kan worden geïdentificeerd het verzamelen van vergaderingen met het Adobe Consulting Services team. De [!DNL Reference Page Tag Execution Script] is relatief klein om grote downloadtoevoegingen aan uw webpagina&#39;s te voorkomen.

Het volgende [!DNL Reference Page Tag Execution Script] code wordt aan u verstrekt in een dossier genoemd [!DNL zig.js]:

```
//REFERENCE PAGE TAG 
// CONSTANTS 
var ct = "<img src="; 
var cd = "[PATH_TO_WEB_SERVER]"; //this should contain the domain of 
                               //the web site that will host the 
                                //page tag 
 
var cu = "[PATH_TO_WEB_PAGE_TAG_CODE]/zag.gif?Log=1";  
                                 //this should contain the full path to 
                                 //the zag.gif file (excluding domain) 
                                 //and include the query string of log=1 
var ce = ">"; 
var c = {}; 
c["sw"] = screen.width; 
c["sh"] = screen.height; 
c["cd"] = screen.colorDepth; 
var co = ""; 
 
for ( cKey in c ) { 
co = co+"&"+cKey+"="+escape(c[cKey]); 
} 
document.write(ct,cd,cu,co,ce); 
 
var d = {}; 
d["dt"] = document.title; 
d["dr"] = document.referrer; 
d["cb"] = new Date().getTime(); 
var vo = ""; 
 
if (typeof v != "undefined") { 
for ( vKey in v ) { 
vo = vo+"&"+vKey+"="+escape(v[vKey]); 
} 
} 
for ( dKey in d ) { 
vo = vo+"&"+dKey+"="+escape(d[dKey]); 
} 
document.write(ct,cd,cu,vo,ce); 
//END REFERENCE PAGE TAG 
```

Om het verzamelen van gegevens te vergemakkelijken door gebruik te maken van de [!DNL Reference Page Tag]Voer de volgende stappen uit:

1. Een afbeeldingsbestand van 1 pixel bij 1 pixel maken of plaatsen met de naam [!DNL zag.gif] in een map op uw webserver.
1. Wijzig de cd-variabele om te verwijzen naar het juiste domein van uw website of Adobe beheerde servicedomein waarvan de [!DNL zag.gif] Er wordt naar het bestand verwezen. De verwijzing naar het bestand wordt gemaakt door het uitvoeren van de opdracht [!DNL zig.js] bestandsfuncties. Bijvoorbeeld:

   ```
   //www.mysite.com
   ```

1. Wijzig de cu-variabele om te verwijzen naar het juiste pad naar de locatie van het [!DNL zag.gif] bestand. Bijvoorbeeld

   ```
   /scripts
   ```

1. Zorg ervoor dat de juiste cachebeheerkoppen zijn ingesteld voor de [!DNL zag.gif] en [!DNL zig.js] bestanden.
