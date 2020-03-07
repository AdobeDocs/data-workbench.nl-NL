---
description: Om met de statistieken te helpen, verstrekt de Werkbank van Gegevens drie statistische maatregelen in de geleide analyse visualisatie.
solution: Analytics
title: Statistische maatregelen
topic: Data workbench
uuid: a8782cd2-d657-4c04-9c5d-8e0af2a3b76e
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Statistische maatregelen{#statistical-measures}

Om met de statistieken te helpen, verstrekt de Werkbank van Gegevens drie statistische maatregelen in de geleide analyse visualisatie.

>[!NOTE]
>
>Hoewel wiskunde u kan helpen oordelen te maken over de correlaties in uw gegevens, moet de context rond de gegevens ook in aanmerking worden genomen.

* **Chi Sq p** is een test van statistische significantie die het uiterlijk van het vinkje in de visualisatie controleert. Wiskundig gezien is het waarschijnlijk dat we de nulhypothese kunnen verwerpen, waarin staat dat de waargenomen verschillen tussen de twee groepen kunnen worden verklaard door willekeurige variaties. Praktisch gezien, als de Chi Sq p-waarde minder dan bijna 100% is, kunnen we de correlatie negeren ongeacht de gemeten sterkte (zoals beschreven in de volgende statistische secties van de U en V).
* **De U-statistiek** is een maatstaf voor de sterkte van de statistische correlatie. Wiskundig gezien, komt het uit een tak van wiskunde genoemd informatietheorie en is nauw verbonden met het concept wederzijdse informatie tussen de distributies van de twee groepen. Alternatief, kan het van als samendrukbaarheid van één groep worden gedacht gegeven een optimale coderingsregeling voor de andere groep. Praktisch, presteert deze maatregel zeer goed in het gemeenschappelijke geval van een dimensie met vele elementen die weinig bezoekers bevatten. De maatregel varieert van 0 (zwak) tot 1 (sterk).
* **De V-statistiek** is ook een maatstaf voor de sterkte van de statistische correlatie. Wiskundig gezien houdt het verband met de bekende Cramer’s V-statistiek, die alleen verschilt door een normaliseringsstap die bedoeld is om de symmetrie van de maatregel met betrekking tot de inversie van de selectie te verbeteren. In de praktijk werkt deze maatregel redelijk goed met vele soorten dimensies en houdt hij verband met een algemeen gebruikte statistische maatstaf. De maatregel varieert van 0 (zwak) tot 1 (sterk).

>[!NOTE]
>
>De U en V statistieken werden geselecteerd om elkaar aan te vullen - elk stemde om soorten correlaties te ontdekken waaraan andere niet zo sterk zou kunnen antwoorden.

Gebruikend deze visualisatie als uw gids, kunt u andere visualisaties aan uw werkruimte toevoegen om meer inzicht in uw gegevens te verstrekken die op de selectie worden gebaseerd.

Het volgende [!DNL Site] voorbeeld bevat een bargrafiek die zittingen voor dagen in Januari, Februari, Maart, en April toont. Merk op dat één dag in Januari wordt geselecteerd.

![](assets/vis_GuidedAnalysis_withVis.png)

De geleide analysevisualisatie in de laag-linkerhoek van de werkruimte wijst erop dat de dimensie van het Aantal van de Zitting nuttige informatie over de geselecteerde dag verstrekt.

Door de de bargrafiek van het Aantal van de Zitting in de laag-juiste hoek van de werkruimte te onderzoeken, kunt u zien dat de gegevens voor Zitting Nummer 2 veel lager zijn dan de benchmark. Aldus, kunnen wij concluderen dat, als percentage, minder tweede zittingen op de geselecteerde dag voorkwamen dan gebruikelijk is. Om een bar grafiek voor om het even welke afmetingen te bekijken die in de geleide analysevisualisatie worden vermeld, selecteer eenvoudig de afmeting door de afmeting met uw muis te klikken.
