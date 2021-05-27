---
description: Als onderdeel van de verzamelde gegevens voor basislijnmeting verzamelt Sensor de domeincookies die van de computer van de bezoeker worden verzonden wanneer deze een aanvraag van uw webserver indient.
title: Metingsgegevens ophalen via cookies
uuid: 34cd6baf-6317-4774-8165-58208698b53c
exl-id: 37c7b5f6-33bf-4373-963a-e08a826e05df
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '587'
ht-degree: 0%

---

# Metingsgegevens ophalen via cookies{#acquiring-measurement-data-through-cookies}

Als onderdeel van de verzamelde gegevens voor basislijnmeting verzamelt Sensor de domeincookies die van de computer van de bezoeker worden verzonden wanneer deze een aanvraag van uw webserver indient.

Dit omvat zowel permanente cookies als sessiecookies die uw website instelt wanneer een bezoeker communiceert met uw systeem.

In de meeste gevallen stellen websites permanente cookies in om bezoekers te identificeren of gebruikersinvoer vast te leggen voor gebruik tijdens volgende bezoekerssessies. Alle informatie die in permanente cookies wordt geschreven en opgeslagen, kan samen met alle andere meetgegevens in de gegevenswerkbankserver worden vastgelegd en gebruikt.

Een voorbeeld van zo&#39;n aanhoudend cookie kan een klant-id bevatten in de vorm van een numerieke sleutel die aanwezig is in een domeinspecifieke cookie die op de computer van de bezoeker staat. Naast het identificeren van de gebruiker als retourbezoeker, zou de permanente cookie ook kunnen worden gebruikt om de bezoeker nader te identificeren als een terugkerende klant of om de bezoeker te koppelen aan informatie in een klantendatabase zodat demografische informatie van de offline klant kan worden weergegeven binnen [!DNL Site] en kan worden gebruikt voor interactieve analyse.

Sessiecookies kunnen een goed mechanisme zijn om gebruikersinvoer te verzamelen via formuliervelden of andere dynamische interactieve elementen op uw website. Als een website formulieren implementeert om gebruikerspecifieke invoergegevens vast te leggen, blijft de informatie alleen in het sessiecookie aanwezig zolang de sessie actief is. Wanneer een gebruiker uw website verlaat of een sessie vervolgens beëindigt, wordt de informatie niet meer opgeslagen op de computer van de gebruiker. De ingevoerde informatie wordt echter vastgelegd door [!DNL Sensor] en beschikbaar gesteld als meetgegevens binnen [!DNL Site].

Hieronder ziet u een voorbeeld van het gebruik van een sessiecookie om één formuliervariabele vast te leggen die een bezoeker heeft ingevoerd.

```
<html> 
<head> 
<title>Cookie Collection </title> 
 
<script language="JavaScript"> 
function AppendFormValues() 
{ 
 
var item = document.testform.elements[i]; 
var formitem = “v_”+i; 
var formvalue = item.value; 
cookie += formitem + "=" + formvalue + "&"; 
document.cookie = cookie; 
 
testform.submit(); 
 
} 
</script> 
</head> 
<body> 
<form name="testform" method="post" action="nextpage.asp"> 
<input type="text" size=15 name="name"><br />enter name 
<br><br> 
 
<a href="javascript:AppendFormValues();">Click Here To </a><br /><br /> 
<br /><br /><br /> 
 
</body> 
</html> 
```

In dit voorbeeld wordt een functie aangeroepen om een sessiecookie op de computer van de bezoeker in te stellen met de naam van het veld en de waarde die in het formulierveld is ingevoerd. Terwijl het formulier wordt verzonden en de volgende webpagina wordt opgevraagd, wordt de set sessiecookies doorgegeven aan de webserver en verzameld door [!DNL Sensor]. De volgende gegevens zijn daarom beschikbaar binnen de server van de gegevenswerkbank voor gebruik in gegevensanalyse:

| Gegevens verzameld | Toelichting | Voorbeeld |
|---|---|---|
| v_1 | Waarde die is gekoppeld aan het cookie v_1. Deze waarde vertegenwoordigt de NAAM die is ingevoerd in het formulierveld dat heeft geleid tot het instellen van het sessiecookie. | v_1=John Smith |

Sessiecookies kunnen ook worden gebruikt om formuliervelden of een groot aantal ingesloten JavaScript-variabelen die zich in een HTML-pagina bevinden, herhaaldelijk vast te leggen. In het volgende voorbeeld wordt JavaScript gebruikt om alle formuliervelden in een HTML-bestand recursief vast te leggen en een sessiecookie in te stellen met de juiste naam=waarde paren.

```
<script language="JavaScript"> 
 
function AppendFormValues() 
{ 
 
var cookie="formcookie="; 
for (i=0; i<document.testform.length; i++){ 
if (document.testform.elements[i].type =="radio") {            
if (document.testform.elements[i].checked){ 
var item = document.testform.elements[i]; 
var formitem = “v_”+i; 
var formvalue = item.value; 
cookie += formitem + "=" + formvalue + "&"; 
} 
} 
else if (document.testform.elements[i].type =="select") { 
var item = document.testform.elements[i]; 
var formitem = “v_”+i; 
var optionindex = eval(document.testform.elements[i].selectedIndex); 
var formvalue = document.testform.elements[i].options[optionindex].value;             
cookie += formitem + "=" + formvalue + "&"; 
} 
else{ 
var item = document.testform.elements[i]; 
var formitem = “v_”+i; 
var formvalue = item.value; 
cookie += formitem + "=" + formvalue + "&"; 
} 
} 
document.cookie = cookie; 
document.testform.submit(); 
} 
 
</script>
```

In dit voorbeeld wordt op de computer van de bezoeker een sessiecookie ingesteld met de naam en waarde van elk formulierveld in het formulier. Dit zijn invoervelden, selectievakjes, keuzerondjes, selectiekaders en tekstgebieden. Zoals u in dit voorbeeld zult merken, is het, omdat het aantal formuliervelden onbekend is, noodzakelijk om alle formuliernamen en veldwaarden als één tekenreeks vast te leggen, gescheiden door een en-teken. Deze stap moet worden genomen vanwege een beperking van het aantal cookies dat een gebruiker op een bepaald tijdstip op zijn of haar computer kan hebben. In Microsoft Internet Explorer kunnen slechts twintig (20) sessiecookies aanwezig zijn voordat de oudste wordt neergezet.
