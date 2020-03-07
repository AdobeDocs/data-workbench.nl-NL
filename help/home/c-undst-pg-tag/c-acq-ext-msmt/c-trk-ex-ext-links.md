---
description: Het vangen van activiteit over derdewebsiteverbindingen om de analyse van het Doel van de Uitgang toe te laten.
solution: Analytics
title: Het volgen gaat aan Externe Verbindingen weg
topic: Data workbench
uuid: 523f5b4c-4600-4d44-82e7-4a8b2db2d266
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Het volgen gaat aan Externe Verbindingen weg{#tracking-exits-to-external-links}

Het vangen van activiteit over derdewebsiteverbindingen om de analyse van het Doel van de Uitgang toe te laten.

De Web-pagina&#39;s kunnen verbindingen aan derdewebsites bevatten, en de activiteit over die verbindingen kan worden gevangen om de analyse van het Doel van de Uitgang toe te laten, vooral in het geval dat de derdeplaats verantwoordelijk is voor het betalen van verwijzingskosten wanneer dergelijke verwijzingen worden ontvangen. Omdat de klikgebeurtenis aan de logboekdossiers van het derdesysteem door gebrek wordt geschreven, moeten de wijzigingen aan de verbinding voor de klikgebeurtenis worden aangebracht die plaatselijk moet worden gevangen. De derdeverbinding aanwezig binnen uw website moet als volgt worden gewijzigd:

```
<A HREF=”http://www.myserver.com/PageExit.htm?v_eurl=http://www.othersite.com”>
```

Het referenced [!DNL PageExit.htm] dossier moet worden gecreeerd en zou moeten worden gestructureerd om het volgende manuscript te bevatten:

```
<html> 
<head> 
 
<script> 
function getExitURLQuery(variable) 
{ 
 
var query = window.location.search.substring(1); 
var vars = query.split("&"); 
for (var i=0; i<vars.length; i++) 
{ 
var pair = vars[i].split("="); 
if (pair[0] == variable) 
{ 
return pair[1]; 
} 
 }  
} 
</script> 
 
<script> 
location.replace(getExitURLQuery("v_eurl")); 
</script>  
 
</head> 
</html>
```

Door het verzoek om het [!DNL PageExit.htm] bestand in te dienen, wordt de v_eurl waarde verzameld voor analysedoeleinden. Bovendien, wanneer [!DNL PageExit.htm] wordt geladen, richt het onmiddellijk aan de gespecificeerde v_eurl doelplaats opnieuw.

| Verzamelde gegevens | Toelichting | Voorbeeld |
|---|---|---|
| v_eurl | Waarde verbonden aan de v_eurl variabele van het vraagkoord. Deze waarde vertegenwoordigt het doel URL van de verbinding aanwezig binnen de HTML- pagina. | v_eurl=www.othersite.com |

