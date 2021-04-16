---
description: Met het JavaScript Document Object Model kunt u aanvullende scriptmethoden gebruiken om de aanvraag voor het bestand zig.js aan te vullen.
title: Documentobjecten ophalen
uuid: 7681c337-b147-4937-9d9c-0ff48d9bdd00
exl-id: eae6609c-be86-44cf-a1a1-69ffb43231fa
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 0%

---

# Documentobjecten ophalen{#acquiring-document-objects}

Met het JavaScript Document Object Model kunt u aanvullende scriptmethoden gebruiken om de aanvraag voor het bestand zig.js aan te vullen.

Informatie zoals de waarde van META-tags, ID-waarden van DIV-tags, enzovoort, kan op naam worden genoemd en worden verzameld als variabelen voor gebruik in de analyse. Als u bijvoorbeeld de informatie in het element META van het HTML-document dynamisch wilt vastleggen, kunt u de volgende JavaScript-syntaxis gebruiken:

```
<!-- BEGIN REFERENCE PAGE TAG--> 
<script language="javascript"> 
var m0 = document.getElementsByTagName('META')[0]; //define the first instance of META 
var metacontent = m0.getAttribute('content'); //get the ‘content’ value of META 
var vlc = "0" //Capture Link Click  1=TRUE, 0=FALSE 
var v = {}; 
v["_1"] = metacontent; 
</script> 
 
<script language="javascript" src=”http://www.myserver.com/path/to/zig.js" type="text/javascript"></script> 
 
<noscript> 
<img src="/path/to/zag.gif?Log=1&v_jd=1" border="0" width="1" height="1"/> 
</noscript> 
 
<!-- END REFERENCE PAGE TAG-->
```

| Gegevens verzameld | Toelichting | Voorbeeld |
|---|---|---|
| v_1= | Waarde die is gekoppeld aan de variabele van de METAVALUE-queryreeks. Deze waarde vertegenwoordigt de gegevens binnen het element META van het HTML-document. | v_1=Deze pagina bevat inhoud die te maken heeft met de volgorde waarin u bedankt bent voor de pagina. |

Nadat de gegevens zijn verzameld, kunt u de gegevenswerkbankserver configureren om deze meetgegevens te verwerken voor analyse en rapportage.
