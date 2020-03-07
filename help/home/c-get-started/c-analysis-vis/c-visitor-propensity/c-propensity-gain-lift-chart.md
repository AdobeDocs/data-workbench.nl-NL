---
description: De grafieken van de Lift en van de Aanwinst bieden visualisaties voor het evalueren van de potentiële prestaties van een gescoord model aan om prestaties over bepaalde gedeelten van het publiek te evalueren.
solution: Analytics
title: Hoogte- en hijskaarten
topic: Data workbench
uuid: 4f08277e-deea-48d3-ab15-214c43ad6664
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Hoogte- en hijskaarten{#propensity-gain-and-lift-charts}

De grafieken van de Lift en van de Aanwinst bieden visualisaties voor het evalueren van de potentiële prestaties van een gescoord model aan om prestaties over bepaalde gedeelten van het publiek te evalueren.

De grafieken van de aanwinst en van de lift zijn visualisaties die worden gebouwd om de potentiële prestaties van het genoteerde model te evalueren. Deze grafieken evalueren de prestaties over elk deel van de bevolking.

**Om een grafiek van de Lift of van de Aanwinst te openen**

1. Selecteer [!DNL Add Visualization > Predictive Analytics > Scoring] .
1. Over **[!UICONTROL Model Complete]** een opgeslagen score heen.

![](assets/propensity_lift_gain_1.png)

**Over Lift- en winstkaarten**

De grafieken van de Lift en van de Aanwinst zijn nuttige visuele hulpmiddelen om de waarde van een vooruitlopende model te meten. Beide grafieken bestaan uit een liftkromme (groen) en een basislijn (roze). Voor de Grafiek **van de** Aanwinst, vertegenwoordigt de afstand tussen de hefboomkromme en de basislijn hoeveel u prestaties in reacties (of de &quot; aanwinst&quot;) kunt verbeteren van het gebruiken van de vooruitlopende wijze. De winst wordt bereikt door voorrang te geven aan en het richten van de vooruitzichten (klanten/bezoekers) die het waarschijnlijkst zijn om te zetten, eerder dan marketing aan klanten/bezoekers willekeurig. Op deze manier, kunt u de verwachte waarde kwantificeren van het gebruiken van het vooruitlopende model om te kiezen welke vooruitzichten om te contacteren.

Net als in de Grafiek van de Aanwinst, toont de **Lift Grafiek** hoeveel waarschijnlijker u positieve reacties zult ontvangen dan als u toevallig met vooruitzichten contacteerde. U wilt de afstand tussen de hefboomkromme en de basislijn zo groot mogelijk zijn, die grotere verwachte winst vertegenwoordigen van het gebruiken van het vooruitlopende model om klanten te contacteren. Wiskundig worden de aanwinst- en hefgrafieken als volgt gedefinieerd:

* **Winst** = (Verwachte Reactie die het Predictieve Model aan de Vooruitzichten van het Contact gebruikt) / (Verwachte Reactie van willekeurig Contacterende Vooruitzichten)
* **Lift** = (Verwachte respons onder een specifieke groepsgrootte van vooruitzichten die wordt geïdentificeerd met behulp van het voorspellende model) / (Verwachte respons onder dezelfde Willekeurige groepsgrootte van vooruitzichten)

**Voorbeeld van liften- en winstkaarten**

Bijvoorbeeld, overweeg het voorbeeld van een detailhandelaar die een e-mail re-marketing campagne wil lanceren om yoga broek te verkopen. Historisch gezien verwacht de analist een gemiddeld responspercentage van 20%, gebaseerd op eerdere e-mailmarketingcampagnes die vergelijkbaar zijn met deze. Terwijl de analist bijna 5 miljoen klanten in zijn e-mailgegevensbestand heeft, willen de zaken slechts aan die klanten op de markt brengen die aan e-mail en aankoop het meest waarschijnlijk zullen antwoorden. Op deze manier maximaliseert het bedrijf het rendement van de campagne en zorgt het er tegelijkertijd voor dat het niet onnodig e-mails naar niet-geïnteresseerde klanten verzendt. Gezien een verwacht responspercentage van 20 procent, verwachten de marktspeler en de analist dat ongeveer 1 miljoen klanten waarschijnlijk zullen reageren en aankopen. In plaats van willekeurig te veronderstellen welke van die klanten onder de 20 percenten reacties zullen zijn, wil de analist slim zijn over het voorspellen van welke van de één miljoen vooruitzichten (onder de gegevensbestand van 5 miljoen klanten) het meest waarschijnlijk zullen antwoorden.

Gebruikend het Scorende vermogen van het Publiek van Adobe, definieert de analist succes als vooruitzicht klikt op een e-mail en koopt yoga broek (de afhankelijke variabele). Na het selecteren van de onafhankelijke variabelen (op basis van ervaring en kennis die is opgedaan bij het analyseren van de correlaties met gegevens en het bundelen van het publiek onder andere analyses), wordt elk vooruitzicht beoordeeld op hun waarschijnlijkheid om positief te reageren op de campagne voor het opnieuw op de markt brengen van e-mail (klikken op de e-mail en yoga-broek kopen). De analist opent de resulterende Gain- en Lift-diagrammen op basis van het voorspellende model.

De y-as toont het percentage van de cumulatieve verwachte positieve reacties. In ons voorbeeld verwachten we een totaal van 1 miljoen positieve reacties. Een waarde van 20% op de y-as komt overeen met 20% van de 1 miljoen verwachte positieve reacties, of 200.000 positieve reacties. De x-as toont het percentage potentiële klanten contacteerde. In ons voorbeeld, vertegenwoordigt de x-as een fractie van de 5 miljoen klanten in het e-mailgegevensbestand. De basislijn (Roze) is het totale responspercentage - als u contact opneemt met X% van de vooruitzichten, ontvangt u X% van de totale positieve respons. Gebruikend het voorspellende model, toont de (groene) hefboomkromme het percentage positieve die reacties (y-as) worden verkregen door een bepaald percentage vooruitzichten (x-as) te contacteren.

In de Lift-kaart wordt de verwachte lift weergegeven als gevolg van het gebruik van het voorspellende model om de hoogste 1 miljoen vooruitzichten te bepalen die het waarschijnlijkst zijn om een yoga-broek aan te schaffen nadat u op de e-mail hebt geklikt. Voor het contacteren van 20 percent van willekeurig geselecteerde vooruitzichten gebruikend geen vooruitlopende model, zou u moeten verwachten om 20 percent van responders te krijgen. Nochtans, gebruikend het voorspellende model om de hoogste 20 percent van vooruitzichten te identificeren die het waarschijnlijkst te antwoorden, verwacht u om 50% van de responders te krijgen. De y-waarde van de hefboomkromme bij 20 percenten is 50/20 = 2.5. De liftgrafiek toont hoeveel waarschijnlijker u respondenten zult ontvangen dan als u een willekeurige steekproef van vooruitzichten contacteert. Bijvoorbeeld, door slechts 20 percenten van vooruitzichten te contacteren die op het vooruitlopende model worden gebaseerd zult u 2.5 keer zo veel respondenten bereiken vergeleken bij het gebruiken van geen voorspellend model.
