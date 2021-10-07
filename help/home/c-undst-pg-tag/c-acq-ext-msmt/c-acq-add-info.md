---
description: Tekenreeksvariabelen van de query kunnen aan een JavaScript-aanvraag worden toegevoegd om aanvullende metingen te verzamelen wanneer een aanvraag wordt gedaan.
title: Aanvullende informatie ophalen
uuid: 0a8075e9-4986-42c4-b505-3985b433cf8e
exl-id: ad4f5e08-b7b7-4de3-b0c2-71440facb2d1
source-git-commit: 79981e92dd1c2e552f958716626a632ead940973
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 0%

---

# Aanvullende informatie ophalen{#acquiring-additional-information}

Tekenreeksvariabelen van de query kunnen aan een JavaScript-aanvraag worden toegevoegd om aanvullende metingen te verzamelen wanneer een aanvraag wordt gedaan.

Deze variabelen kunnen handmatig of met een script op de pagina zelf worden toegevoegd.

Aanvullende informatie die van een pagina kan worden opgehaald, kan via een script aan het ingesloten object worden toegevoegd met de volgende code als voorbeeld:

```
<!-- BEGIN REFERENCE PAGE TAG-->
<script language="javascript">
var vlc = "0" //Capture Link Click  1=TRUE, 0=FALSE
var v = {};
v["_pn"] = "Application Form";
v["_1"] = “99.99”;
v["_2"] = "visa";
</script>

<script language="javascript" src=”https://www.myserver.com/path/to/zig.js" type="text/javascript"></script>
<noscript>

<img src="/path/to/zag.gif?Log=1&v_jd=1" border="0" width="1" height="1"/>
</noscript>
<!-- END REFERENCE PAGE TAG-->
```

In dit voorbeeld kunnen de scriptvariabelen voor v_1 en v_2 worden afgeleid van een andere functie binnen uw webpagina. De variabelen zijn als voorbeelden ingevoegd. Naast de basislijnmetingen die bij elk verzoek zijn verkregen, zouden de volgende uitgebreide metingen worden verkregen met het verzoek van de bovenstaande URL:

| Gegevens verzameld | Toelichting | Voorbeeld |
|---|---|---|
| v_pn= | Waarde gekoppeld aan de variabele v_pn-queryreeks | v_pn=Toepassingsformulier |
| v_1= | Waarde gekoppeld aan de variabele v_1-queryreeks | v_1=99.99 |
| v_2= | Waarde gekoppeld aan de variabele v_2-queryreeks | v_2=visa |
