---
description: De markering van de Pagina van de Verwijzing bestaat uit een Manuscript van de Uitvoering van de Markering van de Pagina dat op een Webserver verblijft, en wanneer geroepen resultaten in de inzameling van alle cliënt-zijgegevens voor de pagina die door de plaatsbezoeker wordt gevraagd.
solution: Analytics
title: Het uitgeven van het Manuscript van de Uitvoering van de Markering van de Verwijzing Pagina
topic: Data workbench
uuid: 0db00b89-e420-423d-9b88-8b724baa828f
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Het uitgeven van het Manuscript van de Uitvoering van de Markering van de Verwijzing Pagina{#editing-the-reference-page-tag-execution-script}

De markering van de Pagina van de Verwijzing bestaat uit een Manuscript van de Uitvoering van de Markering van de Pagina dat op een Webserver verblijft, en wanneer geroepen resultaten in de inzameling van alle cliënt-zijgegevens voor de pagina die door de plaatsbezoeker wordt gevraagd.

U kunt wijzigen [!DNL Reference Page Tag Execution Script] om extra informatie te verzamelen die tijdens vereisten kan worden geïdentificeerd verzamelend vergaderingen met het team van de Diensten van het Raadplegen van Adobe. De [!DNL Reference Page Tag Execution Script] grootte is vrij klein om grote downloadtoevoegingen aan uw Web-pagina&#39;s te vermijden.

De volgende [!DNL Reference Page Tag Execution Script] code wordt verstrekt aan u in een dossier genoemd [!DNL zig.js]:

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

Voer de volgende stappen uit om het verzamelen van gegevens door het gebruik van de [!DNL Reference Page Tag]gegevensbank te vergemakkelijken:

1. Creeer of plaats 1 pixel door 1 pixelbeelddossier genoemd in een folder huidig op uw Webserver. [!DNL zag.gif]
1. Wijzig de cd variabele om het aangewezen domein van uw website of Adobe te verwijzen beheerde de dienstdomein waarvan het [!DNL zag.gif] dossier van verwijzingen wordt voorzien. De verwijzing naar het dossier wordt gecreeerd door de uitvoering van de [!DNL zig.js] dossierfuncties. Bijvoorbeeld:

   ```
   //www.mysite.com
   ```

1. Wijzig de cu variabele om de aangewezen weg aan de plaats van het [!DNL zag.gif] dossier van verwijzingen te voorzien. Bijvoorbeeld

   ```
   /scripts
   ```

1. Verzeker aangewezen geheim voorgeheugen-controle de kopballen voor de [!DNL zag.gif] en [!DNL zig.js] dossiers worden gevestigd.
