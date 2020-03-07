---
description: De Web-pagina's zijn vaak gestructureerd gebruikend de programmeertaal van het ASPIS (de Actieve Pagina's van de Server).
solution: Analytics
title: ASP-specifieke informatie
topic: Data workbench
uuid: 552288cb-b775-4121-8869-322f2a26932b
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# ASP-specifieke informatie{#asp-specific-information}

De Web-pagina&#39;s zijn vaak gestructureerd gebruikend de programmeertaal van het ASPIS (de Actieve Pagina&#39;s van de Server).

ASP is een technologie van Microsoft die binnen IIS (de Diensten van de Informatie van Internet) loopt. Wanneer browser om een dossier van het ASPIS verzoekt, gaat IIS het verzoek tot de motor van het ASPIS over. De motor van het ASPIS leest het dossier van het ASPIS, lijn door lijn, en voert de manuscripten in het dossier uit. Tot slot is het dossier van het ASPIS teruggekeerd aan browser als duidelijk HTML. Het ASPIS verstrekt RESPOND of VRAAGT voorwerpen die, naast ander gebruik, de reactie of het verzoek van gebruikersvragen of gegevens toestaan die van de vormen van HTML worden voorgelegd.

In bepaalde gevallen, kunt u niet de waarden willen toevoegen ingegaan in vormen aan URL die binnen de bar van het Adres van browser van een gebruiker wordt getoond of die binnen de code van HTML zelf viewable is. De eenvoudige server-kant JavaScript staat u toe om de namen van het vormgebied en hun respectieve waarden aan het logboekdossier toe te voegen zonder hen beschikbaar te maken binnen browser van de gebruiker of hen in het HTML- dossier in te bedden. Om de daadwerkelijke vormwaarden te vangen ingegaan in bepaalde vormen binnen uw website, moeten een paar lijnen van code worden toegevoegd om de vormwaarden aan het logboekverzoek toe te voegen.

Binnen de verwerkingspagina van een formulier de volgende code opnemen om de ingevoerde formulierwaarden aan de aanvraaggegevens toe te voegen (naast het schrijven van de ingediende formulierwaarden aan een externe database of een andere locatie):

```
var sName= Request.Form("Name"); 
var sCity= Request.Form("City"); 
var sState= Request.Form("State"); 
var sZip= Request.Form("Zip"); 
 
Response.AppendToLog("&v_1=" +  sName); 
Response.AppendToLog("&v_2=" +  sCity); 
Response.AppendToLog("&v_3=" +  sState); 
Response.AppendToLog("&v_4=" +  sZip);
```

Dit proces zou de vormwaarden zoals die aan de verzoekgegevens voor de [!DNL Form Processing] pagina worden bepaald toevoegen. Binnen de logboekgegevens, zouden de toegevoegde waarden als vraagkoorden van de [!DNL Form Processing] pagina beschikbaar zijn zoals hieronder geïllustreerd. Bijvoorbeeld, v_1, v_2, v_3 en v_4 zou nu vraagkoorden zijn die de gegevens bevatten ingegaan in de aangewezen vormgebieden. De syntaxis die in het voorbeeld hierboven wordt beschreven kan voor om het even welke extra vormgebieden en waarden worden gedupliceerd die u wilt vangen.

```
http://www.myserver.com/path/to/formprocessingpage.asp?v_1=John+Smith&v_2=Los+Angeles&v_3=California&v_4=90210
```

Als u wilt dat elk formulierveld en elke waarde worden vastgelegd en beschikbaar zijn voor analyse, kunt u de volgende syntaxis gebruiken:

```
var formvalues = Response.Form; 
Response.AppendToLog(formvalues); 
```

Dit voorbeeld zou alle vormgebieden aanwezig binnen HTML samen met hun respectieve waarden nemen en hen toevoegen als vraagkoorden aan de logboekingang voor de [!DNL Form Processing] pagina. Opgemerkt zij dat dit alle verborgen velden in het formulier omvat.

De logboekgegevens zouden worden verhoogd zoals die in de volgende lijst worden gedetailleerd:

| Verzamelde gegevens | Toelichting | Voorbeeld |
|---|---|---|
| v_1 | Waarde verbonden aan het de vraagkoord van de NAAM | v_1=John Smith |
| v_2 | Waarde verbonden aan het de vraagkoord van de CITY | v_2=Los Angeles |
| v_3 | Waarde verbonden aan het STATE vraagkoord | v_3=Californië |
| v_4 | Waarde verbonden aan het het vraagkoord van het PIT | v_4=90210 |

