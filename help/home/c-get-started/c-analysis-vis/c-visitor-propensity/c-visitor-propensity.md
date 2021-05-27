---
description: Met scoring in volheid kunt u klanten definiëren op basis van de mogelijkheid dat een bepaalde gebeurtenis succesvol is omgezet of voltooid. Zo kunt u het potentiële effect van uw inspanningen maximaliseren voordat u een proces uitvoert of een campagne leidt.
title: Score volheid
uuid: 4f7163f5-6fe4-4f87-9e27-71ec8b4717af
exl-id: 832a1e6c-8eeb-4dcc-97e8-9570e1a6eb4f
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '747'
ht-degree: 0%

---

# Score van volheid{#propensity-scoring}

Met scoring in volheid kunt u klanten definiëren op basis van de mogelijkheid dat een bepaalde gebeurtenis succesvol is omgezet of voltooid. Zo kunt u het potentiële effect van uw inspanningen maximaliseren voordat u een proces uitvoert of een campagne leidt.

## De waarde van het Score van de Volheid {#section-c51ece66effc42de9b754f0f46027c1b}

Met de optie Propensiteitsscoring kunt u gegevensdetectie uitvoeren om verborgen gedragingen of patronen die in de gegevens voorkomen, te identificeren. Specifiek, helpt het bezit van de dichtheid die u clusters van gelijkaardige klanten identificeert gebruikend meer geconcentreerde en objectieve middelen eerder dan eenvoudige segmentatie of het filtreren. Bovendien laat het bezit u opstelling het voorspelbare mogelijkheden scoren om gedrag voor de hoge-waardeklant van uw bedrijf te identificeren.

Zodra u het hoogwaardigheidspubliek hebt geïdentificeerd, kunt u hen dan voor het grootste effect aanhalen. Bijvoorbeeld, als u Zaken aan Bedrijf bent, kunt u verkoopvraaglood hebben die u toestaan om dan de lood te scoren en hun waarschijnlijkheid te identificeren om offline om te zetten. Omdat elke lead de kosten verhoogt, is het creëren van een prikkel om toekomstige klanten met de hoogste waarschijnlijkheid te identificeren van het omzetten van een verkoop de meest efficiënte en goedkoopste manier om uw middelen te concentreren.

Met de functie voor volheidsscoring kunt u de factoren identificeren die het meest voorspellend zijn voor een bepaalde score of de kans vergroten dat een gebeurtenis plaatsvindt, maar u kunt deze ook toepassen op het beantwoorden van specifieke vragen: Zal de klant converteren? Zal de klant op een e-mail antwoorden? Zal de klant terugkopen? Met scoring in volheid kunt u deze vragen beantwoorden en bezoekers identificeren met een neiging tot actie die vervolgens kan worden ingesteld en gescoord.

Daarnaast kunt u filters gebruiken om een subset bezoekers te definiëren die met de optionele functie **[!UICONTROL Training Filter]** moeten worden gecodeerd. Als er geen filter wordt toegepast, krijgen alle bezoekers de doelversie voor scoring.

## Kenmerken van de Visualisatie van het Score van de Volheid {#section-28413bc7d33b42c59cecb427c1c5a3fa}

Klik **[!UICONTROL Add]** > **[!UICONTROL Visualization]** > **[!UICONTROL Predictive Analytics]** > **[!UICONTROL Scoring]** > **[!UICONTROL Propensity Score]** om de Visualisatie van het Score van de Volheid te openen.

![](assets/propensity_visualization_GO.png)

In de Visualisatie met het scorebord voor volheid zijn de volgende functies beschikbaar vanaf de werkbalk:

| Werkbalkfunctie | Beschrijving |
|---|---|
| Ga | Klik om het scoringsproces uit te voeren nadat u parameters hebt ingesteld. |
| Herstellen | Alle instellingen in de visualisatie wissen. |
| Laden | Laadt eerder gecreeerd ScoreDim die u toestaat om het het schrapen model te veranderen en/of opnieuw op te bouwen. |
| Opslaan | Sla de weergave van de waarheidsscoring op als een grijs bestand dat naar wens moet worden geopend en geopend. |
| Verzenden | Schrijf een scoretaak in voor verwerking op de server. |
| Opties | Stel het trainingsfilter in om de subset met bezoekers te beperken. Het standaardfilter is **[!UICONTROL Train on Everyone]**, maar u kunt het veranderen door werkruimteselecties te maken of een filter te bouwen gebruikend **[!UICONTROL Filter Editor]**. |
| Doel instellen | Stel de afhankelijke variabele in. |
| Metrisch | Metriek toevoegen als onafhankelijke variabelen. |
| Elementen | Sleep Dimension-elementen met de toetsen `<Ctrl>` + `<Alt>` uit Dimension-tabellen. |

**Zie ook**:

* De [Grafieken verbreken en optillen](../../../../home/c-get-started/c-analysis-vis/c-visitor-propensity/c-propensity-gain-lift-chart.md#concept-0d049f6baf534f7fb97f271843ba6c4a). Deze weergaven kunnen worden geopend vanuit een volledig scoremodel of [!DNL Add Visualization> Predictive Analytics > Scoring.]
* De [Modelviewer](../../../../home/c-get-started/c-analysis-vis/c-visitor-propensity/c-propensity-model-viewer.md#concept-d4fdf4b335c04b0ea07e70ab9a7ce9dd). Deze weergaven kunnen worden geopend vanuit een volledig scoremodel of [!DNL Add Visualization> Predictive Analytics > Scoring.]
* De functie [Complexe filterbeschrijving](../../../../home/c-get-started/c-analysis-vis/c-visitor-propensity/c-propensity-complex-filter.md#concept-f9c55e54837f4b5995a00bc950ce5dff).

## Met de &#39;Propensity ScorVisualization&#39; {#section-63ced03fa2eb44f2b8a98d61a6c88122}

* **Definieer een of meer filters om de bezoekerspopulatie voor scoring** te definiëren. Met deze optionele **[!UICONTROL Training Filter]** kunt u bezoekers aanwijzen op basis van geselecteerde criteria. Als er geen trainingsfilter wordt toegepast, krijgen alle bezoekers de doelversie voor scoring. Als het trainingsfilter is ingesteld, heeft het resultaat van de scoring betekenis voor de gedefinieerde bezoekerspopulatie, hoewel elke bezoeker nog steeds een score krijgt.
* **De positieve bezoekers** identificeren. De afhankelijke variabele definiëren om een doelfilter op te geven waarin de positieve bezoekers worden geïdentificeerd die overeenkomen met het gewenste resultaat. Dit kan zo eenvoudig zijn als Opbrengst > $10, of een veel complexere filter.
* **Het doelfilter mag niet hetzelfde zijn als het trainingsfilter**. Logisch, zou het Filter van het Doel een toevoeging aan de Filter van de Opleiding moeten zijn, resulterend in een positieve ondergroep van de bezoekersbevolking die moet worden genegeerd.
* **Selecteer de gewenste variabelen (onafhankelijke variabelen) als invoer voor het algoritme** voor het waarderen van de dichtheid. Dit kunnen metriek of individuele elementen van een Dimension zijn. De scores van de dichtheid zullen beginnen preprocessing enkel zoals in [het Groeperen van de bezoeker](../../../../home/c-get-started/c-analysis-vis/c-visitor-cluster/c-visitor-cluster.md#concept-1c2406ef7b284a56a02daa38eaa2e73d). Het systeem begint met het vastleggen van een bepaalde hoeveelheid samples die overeenkomen met de definitie van het eerder ingestelde trainingsfilter (indien aanwezig). Momenteel is de steekproefgrootte vastgesteld op 10% van de scorepopulatie (gedefinieerd door het trainingsfilter), met een minimum van 20.000 en een maximum van 100.000, en is gebonden aan de grootte van de scorepopulatie.

* Een Dimension van de Score heeft elementen die zich van 0% tot 100% uitstrekken die de waarschijnlijkheid bepalen van de bezoekers die de variabele van het Doel aanpassen.
