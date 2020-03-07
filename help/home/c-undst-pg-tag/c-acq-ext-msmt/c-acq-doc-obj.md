---
description: Gebruikend het Model van de Objecten van het Document JavaScript, kunnen de extra scripting methodes worden gebruikt om het verzoek om het dossier te vergroten zig.js.
solution: Analytics
title: Documentobjecten ophalen
topic: Data workbench
uuid: 7681c337-b147-4937-9d9c-0ff48d9bdd00
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Documentobjecten ophalen{#acquiring-document-objects}

Gebruikend het Model van de Objecten van het Document JavaScript, kunnen de extra scripting methodes worden gebruikt om het verzoek om het dossier te vergroten zig.js.

De informatie zoals de waarde van markeringen META, de waarden van identiteitskaart van markeringen DIV, etc., kan door naam worden van verwijzingen voorzien en als variabelen voor gebruik in analyse worden verzameld. Bijvoorbeeld, om de informatie dynamisch te vangen bevat binnen het element META van het HTML- document, kunt u de volgende syntaxis gebruiken JavaScript:

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

| Verzamelde gegevens | Toelichting | Voorbeeld |
|---|---|---|
| v_1= | Waarde verbonden aan de variabele van het METAVALUE vraagkoord. Deze waarde vertegenwoordigt de gegevens binnen het element META van het HTML- document. | v_1=This de pagina dient inhoud met betrekking tot de orde te dienen dank u pagina. |

Nadat het gegeven wordt verzameld, kunt u de server van de gegevenswerkbank vormen om deze metingsgegevens voor analyse en rapportering te verwerken.
