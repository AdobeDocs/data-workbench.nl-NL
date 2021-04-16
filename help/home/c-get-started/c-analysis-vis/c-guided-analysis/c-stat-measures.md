---
description: Om de statistieken te helpen, voorziet Data Workbench in drie statistische maatregelen in de geleide analyse visualisatie.
title: Statistische maatregelen
uuid: a8782cd2-d657-4c04-9c5d-8e0af2a3b76e
exl-id: 166ff98b-d531-4b31-897e-0c7fedbd2f4d
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '467'
ht-degree: 0%

---

# Statistische maatregelen{#statistical-measures}

Om de statistieken te helpen, voorziet Data Workbench in drie statistische maatregelen in de geleide analyse visualisatie.

>[!NOTE]
>
>Hoewel wiskunde u kan helpen oordelen over de correlaties in uw gegevens, moet de context rond de gegevens ook in overweging worden genomen.

* **Chi Sq** pis een test van statistisch belang die het uiterlijk van het vinkje in de visualisatie bepaalt. Wiskundig gezien is het waarschijnlijk dat we de nulhypothese kunnen verwerpen, die stelt dat de verschillen tussen de twee groepen kunnen worden verklaard door willekeurige variaties. Praktisch gezien, als de Chi Sq p-waarde minder dan bijna 100% is, kunnen wij de correlatie ongeacht zijn gemeten sterkte (zoals beschreven in de volgende U statistic en V statistische secties) negeren.
* **U** statistisch is een maat voor de sterkte van de statistische correlatie. Wiskundig komt het uit een tak van wiskunde, genaamd informatietheorie, en houdt nauw verband met het concept van wederzijdse informatie tussen de distributies van de twee groepen. Het kan ook worden beschouwd als de samendrukbaarheid van een groep bij een optimaal coderingsschema voor de andere groep. Deze maatregel functioneert in de praktijk zeer goed in het algemene geval van een dimensie met veel elementen die weinig bezoekers bevatten. De maatregel varieert van 0 (zwak) tot 1 (sterk).
* **V** statistisch is ook een maat voor de sterkte van de statistische correlatie. Wiskundig gezien houdt het verband met de bekende V-statistiek van Cramer, die alleen verschilt door een normaliseringsstap die bedoeld is om de symmetrie van de maatregel met betrekking tot de omkering van de selectie te verbeteren. In de praktijk werkt deze maatregel redelijk goed met vele soorten dimensies en houdt hij verband met een veelgebruikte statistische maatstaf. De maatregel varieert van 0 (zwak) tot 1 (sterk).

>[!NOTE]
>
>De U- en V-statistieken zijn zodanig gekozen dat ze elkaar aanvullen. Elke statistiek is afgestemd om de typen correlaties te detecteren waarop de andere niet zo sterk reageert.

Met deze visualisatie als richtlijn kunt u andere visualisaties toevoegen aan uw werkruimte voor meer inzicht in uw gegevens op basis van de selectie.

Het volgende [!DNL Site] voorbeeld bevat een staafgrafiek die zittingen voor dagen in Januari, Februari, Maart, en April toont. Merk op dat één dag in Januari wordt geselecteerd.

![](assets/vis_GuidedAnalysis_withVis.png)

De geleide analyse visualisatie in de laag-linkerhoek van de werkruimte wijst erop dat de dimensie van het Aantal van de Zitting nuttige informatie over de geselecteerde dag verstrekt.

Door de grafiek van de bar van het Aantal van de Zitting in de laag-juiste hoek van de werkruimte te onderzoeken, kunt u zien dat de gegevens voor Zitting Nummer 2 veel lager zijn dan het benchmark. We kunnen dus concluderen dat, als percentage, op de geselecteerde dag minder tweede sessies hebben plaatsgevonden dan normaal. Als u een staafgrafiek wilt weergeven voor een van de dimensies die worden vermeld in de visualisatie van de geleide analyse, selecteert u gewoon de dimensie door met de muis op de dimensie te klikken.
