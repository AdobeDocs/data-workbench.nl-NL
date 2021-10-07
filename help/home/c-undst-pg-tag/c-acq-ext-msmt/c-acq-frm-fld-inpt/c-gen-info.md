---
description: Waarden die in een formulier op een webpagina worden ingevoerd, kunnen met behulp van JavaScript worden verzameld en toegevoegd aan de queryreeks van de pagina die daarna wordt aangevraagd (bij het verzenden van het formulier).
title: Algemene informatie
uuid: 401816a5-1d95-48e6-bedf-ee2a5dbd2d50
exl-id: 9effc72b-e75f-423c-87ec-6ac25edee8d6
source-git-commit: 79981e92dd1c2e552f958716626a632ead940973
workflow-type: tm+mt
source-wordcount: '175'
ht-degree: 0%

---

# Algemene informatie{#general-information}

Waarden die in een formulier op een webpagina worden ingevoerd, kunnen met behulp van JavaScript worden verzameld en toegevoegd aan de queryreeks van de pagina die daarna wordt aangevraagd (bij het verzenden van het formulier).

Dit wordt in het volgende voorbeeld getoond. Neem dit JavaScript op na alle validatiescripts voor formulieren die worden gebruikt op uw HTML-pagina&#39;s.

```
<html>
<head>
</head>
<script language="JavaScript">

function AppendFormValues()
{

for(var i = 0; i < document.formname.length; i++)
{
var item = document.formname.elements[i];
var formitem = “v_”+i;
var formvalue = item.value;
formvalues += formitem + '=' + formvalue + '&';
}
document.formname.action = document.formname.action + '?' + formvalues;

}
</script>
<body>
<form name="formname" action="thankyou.asp" method="POST" onSubmit="AppendFormValues();">
<input name="NAME" size="50" value=""></input>name<br/>
<input name="CITY" size="50" value=""></input>city<br/>
<input name="STATE" size="50" value=""></input>state<br/>
<input name="ZIP" size="10" value=""></input>zip<br />
<input type="submit" name="submit" value="submit"/>
</body>
</html>
```

In dit voorbeeld worden de waarden die door de browsergebruiker in het formulier zijn ingevoerd, toegevoegd aan de volgende pagina &quot;thankyou.asp&quot; die als volgt in de waarde voor FORM-actie wordt aangegeven:

```
https://www.myserver.com/thankyou.asp?v_1=John Smith&v_2=Los Angeles&v_3=California&v_4=90210
```

De volgende uitgebreide metingen zouden met dit verzoek worden verkregen naast de basismetingen die door [!DNL Sensor] worden verzameld:

| Gegevens verzameld | Toelichting | Voorbeeld |
|---|---|---|
| v_1 | Waarde die is gekoppeld aan het formulierveld NAME | v_1=John Smith |
| v_2 | Waarde die is gekoppeld aan het veld CITY-formulier | v_2=Los Angeles |
| v_3 | Waarde die is gekoppeld aan het STATE-formulierveld | v_3=California |
| v_4 | Waarde die is gekoppeld aan het ZIP-formulierveld | v_4=90210 |
