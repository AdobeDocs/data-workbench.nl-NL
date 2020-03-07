---
description: Als deel van de verzamelde gegevens van de Meting van de Basislijn, verzamelt de Sensor de domeinkoekjes die van de machine van een bezoeker worden verzonden wanneer het indienen van een verzoek van uw Webserver.
solution: Analytics
title: Het verwerven van meetgegevens door koekjes
topic: Data workbench
uuid: 34cd6baf-6317-4774-8165-58208698b53c
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Het verwerven van meetgegevens door koekjes{#acquiring-measurement-data-through-cookies}

Als deel van de verzamelde gegevens van de Meting van de Basislijn, verzamelt de Sensor de domeinkoekjes die van de machine van een bezoeker worden verzonden wanneer het indienen van een verzoek van uw Webserver.

Dit omvat zowel hardnekkige als sessiecookies die uw website plaatst wanneer een bezoeker met uw systeem in wisselwerking staat.

In de meeste gevallen, plaatsen de websites blijvende koekjes om bezoekers te identificeren of gebruikersinput te vangen voor gebruik binnen verdere bezoekerszittingen. Alle informatie die wordt geschreven naar en opgeslagen in permanente cookies kan samen met alle andere meetgegevens in de gegevenswerkbankserver worden vastgelegd en gebruikt.

Een voorbeeld van zo&#39;n blijvend koekje kon een klantenherkenningsteken in de vorm van een numerieke sleutel impliceren aanwezig binnen een domein-specifieke koekje dat op de machine van de bezoeker verblijft. Naast het identificeren van de gebruiker als terugkeerbezoeker, kon het blijvende koekje ook worden gebruikt om de bezoeker als terugkerende klant verder te identificeren of de bezoeker te binden aan informatie in een klantengegevensbestand om off-line klantendemografische informatie toe te staan binnen worden getoond [!DNL Site] en voor interactieve analyse worden gebruikt.

De koekjes van de zitting kunnen een goed mechanisme zijn om gebruikersinput door vormgebieden of andere dynamische interactieve elementen binnen uw website te verzamelen. In het geval van een website die vormen uitvoert om gebruiker-specifieke inputgegevens te vangen, blijft de informatie in het zittingskoekje slechts zolang de zitting actief is. Wanneer een gebruiker uw website verlaat of later een zitting beëindigt, wordt de informatie niet meer opgeslagen op de computer van de gebruiker. De ingevoerde informatie wordt echter vastgelegd door [!DNL Sensor] en beschikbaar gesteld als meetgegevens binnen [!DNL Site].

Na is een voorbeeld van het gebruiken van een zittingskoekje om één enkele vormvariabele te vangen ingegaan door een bezoeker.

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

In dit voorbeeld, wordt een functie geroepen om een zittingskoekje op de machine van de bezoeker met de naam van het gebied en de waarde te plaatsen ingegaan in het vormgebied. Aangezien de vorm wordt voorgelegd, en de verdere Web-pagina wordt gevraagd, wordt de reeks van het zittingskoekje overgegaan tot de Webserver en door verzameld [!DNL Sensor]. De volgende gegevens zijn daarom beschikbaar binnen de server van de gegevenswerkbank voor gebruik in gegevensanalyse:

| Verzamelde gegevens | Toelichting | Voorbeeld |
|---|---|---|
| v_1 | Waarde verbonden aan het v_1 koekje. Deze waarde vertegenwoordigt de NAAM ingegaan in het vormgebied dat in het zittingskoekje resulteerde dat wordt geplaatst. | v_1=John Smith |

De koekjes van de zitting kunnen ook worden gebruikt om vormgebieden of een massa ingebedde variabelen te vangen JavaScript huidig binnen een HTML- pagina. In het volgende voorbeeld, wordt JavaScript gebruikt om het even welk vormgebied recursief te vangen huidig binnen een HTML- dossier en een zittingskoekje met de aangewezen name=value paren te plaatsen.

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

In dit voorbeeld, wordt een zittingskoekje geplaatst op de machine van de bezoeker met de naam en de waarde van elk vormgebied dat binnen de vorm bestaat. Dit omvat inputgebieden, controledozen, radioknopen, uitgezochte dozen, en tekstgebieden. Aangezien u in dit voorbeeld kunt opmerken, omdat het aantal vormgebieden onbekend is, is het noodzakelijk om alle vormnaam en gebiedswaarden als één enkel koord te vangen, dat door een ampersand wordt afgebakend. Deze stap moet worden genomen vanwege een beperking van het aantal cookies dat een gebruiker op een bepaald moment op zijn of haar computer kan hebben. Microsoft Internet Explorer laat slechts twintig (20) zittingskoekjes toe om aanwezig te zijn alvorens het begint dalend oudste.
