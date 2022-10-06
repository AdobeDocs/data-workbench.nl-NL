---
description: De grafieken van de Optillen en van de Aanwinst bieden visualisaties voor het evalueren van de potentiële prestaties van een genoteerd model om prestaties over bepaalde gedeelten van het publiek te evalueren.
title: Hoogte- en oplichtdiagrammen
uuid: 4f08277e-deea-48d3-ab15-214c43ad6664
exl-id: 5ac08512-ac9c-4e85-a4f9-ea6d819095d8
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '806'
ht-degree: 0%

---

# Hoogte- en oplichtdiagrammen{#propensity-gain-and-lift-charts}

{{eol}}

De grafieken van de Optillen en van de Aanwinst bieden visualisaties voor het evalueren van de potentiële prestaties van een genoteerd model om prestaties over bepaalde gedeelten van het publiek te evalueren.

De grafieken van de aanwinst en van de lift zijn visualisaties die worden gebouwd om de potentiële prestaties van het gegraveerde model te evalueren. Deze grafieken evalueren de prestaties over elk deel van de bevolking.

**Een grafiek voor het optillen of vergroten openen**

1. Selecteren [!DNL Add Visualization > Predictive Analytics > Scoring] .
1. Overslaan **[!UICONTROL Model Complete]** van een opgeslagen score.

![](assets/propensity_lift_gain_1.png)

**Info Houtgrafieken optillen en verbreken**

De grafieken van de Lift en van de Aanwinst zijn nuttige visuele hulpmiddelen om de waarde van een vooruitlopende model te meten. Beide grafieken bestaan uit een liftcurve (groen) en een basislijn (roze). Voor de **Grafiek** De afstand tussen de liftcurve en de basislijn geeft aan hoeveel u de prestaties in de responsen (of de &quot; versterking&quot;) kunt verbeteren in de voorspellende modus. De winst wordt gerealiseerd door voorrang te geven aan en zich te richten op de vooruitzichten (klanten/bezoekers) die het meest waarschijnlijk zullen worden omgezet, eerder dan aan marketing aan klanten/bezoekers willekeurig. Op deze manier, kunt u de verwachte waarde kwantificeren van het gebruiken van het vooruitlopende model om te kiezen welke vooruitzichten om te contacteren.

Net als in de Gain Chart geldt voor de **Grafiek optillen** toont hoeveel waarschijnlijker u positieve reacties zult ontvangen dan als u willekeurig vooruitzichten contacteerde. U wilt dat de afstand tussen de liftcurve en de basislijn zo groot mogelijk is, wat een grotere verwachte winst vertegenwoordigt wanneer u het voorspellende model gebruikt om klanten te contacteren. Wiskundig worden de verbreding- en liftdiagrammen als volgt gedefinieerd:

* **Versterking** = (Verwachte reactie met gebruik van voorspellend model om vooruitzichten te contacteren) / (Verwachte reactie van willekeurig contacterende Vooruitzichten)
* **Optillen** = (Verwacht antwoord onder een specifieke groepsgrootte van vooruitzichten die met behulp van het voorspellende model worden geïdentificeerd) / (Verwacht antwoord onder dezelfde specifieke groepsgrootte van willekeurig geïdentificeerde vooruitzichten)

**Voorbeeld van retoucheerdiagrammen en versterkingsgrafieken**

Neem bijvoorbeeld het voorbeeld van een detailhandelaar die een e-mailmarketingcampagne wil starten om een yoga-broek te verkopen. In het verleden verwacht de analist een gemiddeld responspercentage van 20 procent op basis van eerdere e-mailmarketingcampagnes, vergelijkbaar met deze. Terwijl de analist bijna 5 miljoen klanten in zijn e-mailgegevensbestand heeft, wil de zaken slechts aan die klanten in de handel brengen die het meest waarschijnlijk op e-mail en aankoop zullen antwoorden. Op deze manier maximaliseert het bedrijf het rendement van de campagne en zorgt het ervoor dat het niet onnodig e-mails stuurt naar niet-geïnteresseerde klanten. Gezien een verwacht responspercentage van 20 procent, verwachten de marktleider en analist dat ongeveer 1 miljoen klanten waarschijnlijk zullen reageren en kopen. In plaats van willekeurig te veronderstellen welke van die klanten onder de 20 percenten reacties zullen zijn, wil de analist slim zijn over het voorspellen welke van de één miljoen vooruitzichten (onder het gegevensbestand van 5 miljoen klanten) het meest waarschijnlijk zullen antwoorden.

Gebruikend de functie van Audience Scoring, bepaalt de analist succes aangezien een vooruitzicht op een e-mail klikt en yoga broek (de afhankelijke variabele) koopt. Na het selecteren van de onafhankelijke variabelen (op basis van ervaring en kennis die is opgedaan bij het analyseren van de correlaties met gegevens en clustering van het publiek onder andere analyses), wordt elk vooruitzicht beoordeeld op de waarschijnlijkheid dat de campagne voor het opnieuw in de handel brengen van e-mail positief zal worden gereageerd (door op de e-mail te klikken en een yoga-broek aan te schaffen). De analist opent de resulterende Gain- en Lift-diagrammen op basis van het voorspellende model.

Op de y-as wordt het percentage van de cumulatieve verwachte positieve reacties weergegeven. In ons voorbeeld verwachten we in totaal 1 miljoen positieve antwoorden. Een waarde van 20% op de y-as komt overeen met 20% van de 1 miljoen verwachte positieve reacties, ofwel 200.000 positieve reacties. Op de x-as wordt het percentage van de gecontacteerde potentiële klanten weergegeven. In ons voorbeeld vertegenwoordigt de x-as een fractie van de 5 miljoen klanten in het e-mailgegevensbestand. De basislijn (roze) is de totale responssnelheid - als u contact opneemt met X% van de vooruitzichten, krijgt u X% van de totale positieve respons. Met behulp van het voorspellende model geeft de liftcurve (groen) het percentage positieve reacties weer dat is verkregen (y-as) door contact op te nemen met een bepaald percentage vooruitzichten (x-as).

In de Lift-grafiek wordt de verwachte lift uitgestippeld als gevolg van het gebruik van het voorspellende model om de top 1 miljoen te bepalen van de vooruitzichten die het meest waarschijnlijk zijn om een yoga-broek aan te schaffen na ontvangst en klik op de e-mail. Als u contact wilt opnemen met 20% van de willekeurig geselecteerde vooruitzichten zonder voorspellend model, kunt u verwachten dat u 20% van de responders krijgt. Nochtans, gebruikend het vooruitlopende model om de top 20 percenten van vooruitzichten te identificeren het meest waarschijnlijk om te antwoorden, verwacht u 50% van responders te krijgen. De y-waarde van de liftcurve bij 20 % is 50/20 = 2,5. De lift toont hoeveel waarschijnlijker u reacties zult ontvangen dan als u een willekeurige steekproef van vooruitzichten contacteert. Als u bijvoorbeeld slechts 20 procent van de vooruitzichten op basis van het voorspellende model aanspreekt, bereikt u 2,5 keer zoveel respondenten als wanneer u geen voorspellend model gebruikt.
