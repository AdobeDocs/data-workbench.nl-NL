---
description: Vastleggen van activiteit over derdewebsiteverbindingen om de analyse van het Doel van het Uitgang toe te laten.
title: Afsluiten bij externe koppelingen bijhouden
uuid: 523f5b4c-4600-4d44-82e7-4a8b2db2d266
exl-id: fd7434e9-cd66-408e-baa9-6a0df4039786
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '193'
ht-degree: 0%

---

# Afsluiten bijhouden naar externe koppelingen{#tracking-exits-to-external-links}

Vastleggen van activiteit over derdewebsiteverbindingen om de analyse van het Doel van het Uitgang toe te laten.

Webpagina&#39;s kunnen koppelingen naar websites van derden bevatten, en activiteiten in die koppelingen kunnen worden vastgelegd om Exit Target-analyse mogelijk te maken, met name wanneer de externe site verantwoordelijk is voor het betalen van verwijzingskosten wanneer dergelijke verwijzingen worden ontvangen. Omdat de klikgebeurtenis aan de logboekdossiers van het derdesysteem door gebrek wordt geschreven, moeten de veranderingen aan de verbinding voor de klikgebeurtenis worden aangebracht om plaatselijk worden gevangen. De koppeling naar een andere fabrikant op uw website moet als volgt worden gewijzigd:

```
<A HREF=”http://www.myserver.com/PageExit.htm?v_eurl=http://www.othersite.com”>
```

Het bestand [!DNL PageExit.htm] waarnaar wordt verwezen, moet worden gemaakt en gestructureerd met het volgende script:

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

Door het verzoek om het [!DNL PageExit.htm] dossier te doen, wordt de v_eurl waarde verzameld voor analysedoeleinden. Wanneer [!DNL PageExit.htm] is geladen, wordt deze bovendien direct doorgestuurd naar de opgegeven doellocatie v_eurl.

| Gegevens verzameld | Toelichting | Voorbeeld |
|---|---|---|
| v_eurl | Waarde gekoppeld aan de variabele v_eurl-queryreeks. Deze waarde vertegenwoordigt de doel-URL van de koppeling in de HTML-pagina. | v_eurl=www.othersite.com |
