---
description: Webpagina's zijn vaak gestructureerd met de programmeertaal ASP (Active Server Pages).
title: ASP-specifieke informatie
uuid: 552288cb-b775-4121-8869-322f2a26932b
exl-id: f73235e1-d44a-4056-b1f4-a86879c19483
source-git-commit: 79981e92dd1c2e552f958716626a632ead940973
workflow-type: tm+mt
source-wordcount: '446'
ht-degree: 0%

---

# ASP-specifieke informatie{#asp-specific-information}

Webpagina&#39;s zijn vaak gestructureerd met de programmeertaal ASP (Active Server Pages).

ASP is een technologie van Microsoft die binnen IIS (de Diensten van de Informatie van Internet) loopt. Wanneer browser om een dossier van het ASPIS verzoekt, gaat IIS het verzoek tot de motor van het ASPIS over. De ASP-engine leest het ASP-bestand regel voor regel en voert de scripts in het bestand uit. Ten slotte wordt het ASP-bestand als normale HTML aan de browser geretourneerd. ASP biedt RESPOND- of REQUEST-objecten die, naast andere toepassingen, het antwoord of de aanvraag van gebruikersquery&#39;s of gegevens die vanuit HTML-formulieren worden verzonden mogelijk maken.

In bepaalde gevallen wilt u de waarden die in formulieren zijn ingevoerd, mogelijk niet toevoegen aan de URL die wordt weergegeven in de adresbalk van de browser van de gebruiker of die kan worden weergegeven in de HTML-code zelf. Met eenvoudige JavaScript aan de serverzijde kunt u namen van formuliervelden en hun respectieve waarden aan het logbestand toevoegen zonder deze beschikbaar te maken in de browser van de gebruiker of in te sluiten in het HTML-bestand. Als u de werkelijke formulierwaarden wilt vastleggen die in bepaalde formulieren op uw website zijn ingevoerd, moet u enkele coderegels toevoegen om de formulierwaarden aan de logaanvraag toe te voegen.

Neem op de pagina voor de verwerking van een formulier de volgende code op om de ingevoerde formulierwaarden aan de aanvraaggegevens toe te voegen (en schrijf de ingediende formulierwaarden niet alleen naar een externe database of een andere locatie):

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

Hierbij worden de formulierwaarden zoals gedefinieerd toegevoegd aan de aanvraaggegevens voor de pagina [!DNL Form Processing]. Binnen de logboekgegevens, zouden de toegevoegde waarden als vraagkoorden van de [!DNL Form Processing] pagina zoals hieronder geïllustreerd beschikbaar zijn. v_1, v_2, v_3 en v_4 zijn nu bijvoorbeeld queryreeksen die de gegevens bevatten die in de desbetreffende formuliervelden zijn ingevoerd. De syntaxis die in het bovenstaande voorbeeld wordt beschreven, kan worden gedupliceerd voor extra formuliervelden en waarden die u wilt vastleggen.

```
https://www.myserver.com/path/to/formprocessingpage.asp?v_1=John+Smith&v_2=Los+Angeles&v_3=California&v_4=90210
```

Als u wilt dat elk formulierveld en elke waarde worden vastgelegd en beschikbaar zijn voor analyse, kunt u de volgende syntaxis gebruiken:

```
var formvalues = Response.Form;
Response.AppendToLog(formvalues);
```

In dit voorbeeld worden alle formuliervelden gebruikt die zich in de HTML bevinden, samen met de respectieve waarden, en worden deze als queryreeksen toegevoegd aan de logbestandvermelding voor de pagina [!DNL Form Processing]. Opgemerkt zij dat dit alle verborgen velden in het formulier zou omvatten.

De loggegevens worden aangevuld zoals in de volgende tabel wordt beschreven:

| Gegevens verzameld | Toelichting | Voorbeeld |
|---|---|---|
| v_1 | Waarde die is gekoppeld aan de queryreeks NAME | v_1=John Smith |
| v_2 | Waarde die is gekoppeld aan de CITY-queryreeks | v_2=Los Angeles |
| v_3 | Waarde verbonden aan het de vraagkoord van de STAAT | v_3=California |
| v_4 | Waarde die is gekoppeld aan de ZIP-queryreeks | v_4=90210 |
