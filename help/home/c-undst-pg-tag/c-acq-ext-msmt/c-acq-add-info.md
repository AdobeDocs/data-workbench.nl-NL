---
description: De het koordvariabelen van de vraag kunnen aan een verzoek worden toegevoegd JavaScript om extra metingen te verzamelen wanneer een verzoek wordt ingediend.
solution: Analytics
title: Aanvullende informatie verkrijgen
topic: Data workbench
uuid: 0a8075e9-4986-42c4-b505-3985b433cf8e
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Aanvullende informatie verkrijgen{#acquiring-additional-information}

De het koordvariabelen van de vraag kunnen aan een verzoek worden toegevoegd JavaScript om extra metingen te verzamelen wanneer een verzoek wordt ingediend.

Deze variabelen kunnen manueel of door manuscript in de pagina zelf worden toegevoegd.

De extra informatie die van een pagina kan worden verkregen kan aan het ingebedde voorwerp via manuscript worden toegevoegd gebruikend de volgende code als voorbeeld:

```
<!-- BEGIN REFERENCE PAGE TAG--> 
<script language="javascript"> 
var vlc = "0" //Capture Link Click  1=TRUE, 0=FALSE 
var v = {}; 
v["_pn"] = "Application Form"; 
v["_1"] = “99.99”; 
v["_2"] = "visa"; 
</script> 
 
<script language="javascript" src=”http://www.myserver.com/path/to/zig.js" type="text/javascript"></script> 
<noscript> 
 
<img src="/path/to/zag.gif?Log=1&v_jd=1" border="0" width="1" height="1"/> 
</noscript> 
<!-- END REFERENCE PAGE TAG-->
```

In dit voorbeeld, kunnen de manuscriptvariabelen voor v_1 en v_2 uit een andere functie binnen uw Web-pagina worden afgeleid. De variabelen zijn als voorbeelden opgenomen. Naast de basislijnmetingen die met elk verzoek worden verworven, zouden de volgende uitgebreide metingen met het verzoek van URL hierboven worden verworven:

| Verzamelde gegevens | Toelichting | Voorbeeld |
|---|---|---|
| v_pn= | Waarde verbonden aan de v_pn variabele van het vraagkoord | v_pn=Application Form |
| v_1= | Waarde verbonden aan de v_1 variabele van het vraagkoord | v_1=99,99 |
| v_2= | Waarde verbonden aan de v_2 variabele van het vraagkoord | v_2=visum |

