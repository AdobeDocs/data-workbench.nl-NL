---
description: Met 'Propensity scoring' kunt u klanten definiëren op basis van de mogelijkheid van een succesvolle conversie of voltooiing van een bepaalde gebeurtenis. Het staat u toe om het potentiële effect van inspanningen te maximaliseren alvorens een proces uit te voeren of een campagne te leiden.
solution: Analytics
title: Propensiteitsscore
topic: Data workbench
uuid: 4f7163f5-6fe4-4f87-9e27-71ec8b4717af
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Propensiteitsscore{#propensity-scoring}

Met &#39;Propensity scoring&#39; kunt u klanten definiëren op basis van de mogelijkheid van een succesvolle conversie of voltooiing van een bepaalde gebeurtenis. Het staat u toe om het potentiële effect van inspanningen te maximaliseren alvorens een proces uit te voeren of een campagne te leiden.

## De waarde van het Scoren van de dichtheid {#section-c51ece66effc42de9b754f0f46027c1b}

Met &#39;Propensity-scoring&#39; kunt u gegevensdetectie uitvoeren om verborgen gedragingen of patronen te identificeren die op uw gegevens voorkomen. Specifiek, helpt het rangschikken van de dichtheid u clusters van gelijkaardige klanten identificeren gebruikend meer geconcentreerde en objectieve middelen eerder dan eenvoudige segmentatie of het filtreren. Bovendien kunt u met &#39;propensity scoring&#39; voorspellende mogelijkheden instellen om het gedrag van de hoogwaardige klant van uw bedrijf te identificeren.

Zodra je het publiek met een hoge waarde hebt geïdentificeerd, kun je het beste bereiken. Bijvoorbeeld, als u Zaken aan Bedrijf bent, kunt u verkoopvraaglood hebben die u toestaan om de lood dan te scoren en hun waarschijnlijkheid te identificeren om offline om te zetten. Omdat elke leiding de kosten verhoogt, is het creëren van een prikkel om toekomstige klanten met de hoogste waarschijnlijkheid te identificeren van het omzetten van een verkoop de meest efficiënte en minst dure manier om uw middelen te concentreren.

Het rangschikken van de dichtheid verstrekt de capaciteit om die factoren te identificeren die het meest voorspelbaar van een bepaalde score zijn of de waarschijnlijkheid van een gebeurtenis te verhogen die plaatsvindt, maar het kan ook worden toegepast om specifieke vragen te beantwoorden: Zal de klant converteren? Zal de klant reageren op een e-mail? Zal de klant terugkopen? Met &#39;Propensity scoring&#39; kunt u deze vragen beantwoorden en bezoekers identificeren met een neiging tot actie die vervolgens kan worden ingesteld en gescand.

Bovendien kunt u filters gebruiken om een ondergroep van bezoekers te bepalen die moeten worden gescoord gebruikend de facultatieve **[!UICONTROL Training Filter]** eigenschap. Als geen filter wordt toegepast, dan worden alle bezoekers gericht voor het noteren.

## Kenmerken van de Propensity Scoring Visualization {#section-28413bc7d33b42c59cecb427c1c5a3fa}

Om de Propensity Scoring Visualization te openen, klik **[!UICONTROL Add]** > **[!UICONTROL Visualization]** > **[!UICONTROL Predictive Analytics]** > **[!UICONTROL Scoring]** > **[!UICONTROL Propensity Score]**.

![](assets/propensity_visualization_GO.png)

De Propensity Scoring Visualization bevat deze functies die toegankelijk zijn op de werkbalk:

| Werkbalkfunctie | Beschrijving |
|---|---|
| Ga weg | Klik om het het noteren proces na vestigingsparameters in werking te stellen. |
| Terugzetten | Ontruim alle montages in de visualisatie. |
| Belasting | Laadt eerder gecreeerde ScoreDim die u toestaat om het het noteren model te veranderen en/of te herbouwen. |
| Opslaan | Sparen de dichtheid die visualisatie als een dossier van de Duim visualiseren dat moet worden betreden en worden geopend zoals nodig. |
| Verzenden | Dien het scoren taak voor server-zijverwerking voor. |
| Opties | Plaats de Filter van de Opleiding om de ondergroep van bezoekers te beperken. De standaardfilter is **[!UICONTROL Train on Everyone]**, maar u kunt het veranderen door werkruimteselecties te maken of een filter te bouwen gebruikend **[!UICONTROL Filter Editor]**. |
| Doel instellen | Stel de afhankelijke variabele in. |
| Metrisch | Voeg Metriek als Onafhankelijke Variabelen toe. |
| Elementen | De elementen van de Dimensie van de belemmering gebruikend de `<Ctrl>` + `<Alt>` sleutels van de lijsten van de Dimensie. |

**Zie ook**:

* De [aanwinst- en liftenkaarten](../../../../home/c-get-started/c-analysis-vis/c-visitor-propensity/c-propensity-gain-lift-chart.md#concept-0d049f6baf534f7fb97f271843ba6c4a). Deze meningen kunnen van een volledig het noteren model of van worden geopend [!DNL Add Visualization> Predictive Analytics > Scoring.]
* De [ModelKijker](../../../../home/c-get-started/c-analysis-vis/c-visitor-propensity/c-propensity-model-viewer.md#concept-d4fdf4b335c04b0ea07e70ab9a7ce9dd). Deze meningen kunnen van een volledig het noteren model of van worden geopend [!DNL Add Visualization> Predictive Analytics > Scoring.]
* De [complexe eigenschap van de Beschrijving](../../../../home/c-get-started/c-analysis-vis/c-visitor-propensity/c-propensity-complex-filter.md#concept-f9c55e54837f4b5995a00bc950ce5dff) van de Filter.

## Het gebruiken van de Propensity Scoring Visualization {#section-63ced03fa2eb44f2b8a98d61a6c88122}

* **Bepaal één of meerdere filters om de bezoekerspopulatie voor het noteren** te bepalen. Met deze optie **[!UICONTROL Training Filter]** kunt u bezoekers op basis van geselecteerde criteria benaderen. Als geen opleidingsfilter wordt toegepast, dan worden alle bezoekers gericht voor het noteren. Als het Opleidingsfilter is ingesteld, is het scoringsresultaat zinvol voor de gedefinieerde bezoekerspopulatie, hoewel elke bezoeker nog een score krijgt.
* **Identificeer de positieve bezoekers**. Om de afhankelijke variabele te bepalen om een doelfilter te specificeren die de positieve bezoekers identificeert die het gewenste resultaat aanpassen. Dit kan zo eenvoudig zijn zoals Opbrengst > $10, of een veel complexere filter.
* **De filter van het Doel mag niet het zelfde zijn als de filter** van de Opleiding. Logischerwijs, zou de Filter van het Doel een toevoeging aan de Filter van de Opleiding moeten zijn, resulterend in een positieve ondergroep van de bezoekerspopulatie die moet worden genoteerd.
* **Selecteer variabelen van belang (onafhankelijke variabelen) als input aan het het Scoren algoritme** van de Volheid. Dit kunnen Metriek of individuele elementen van een Dimensie zijn. Propensity Scoring begint net als in [Visitor Clustering](../../../../home/c-get-started/c-analysis-vis/c-visitor-cluster/c-visitor-cluster.md#concept-1c2406ef7b284a56a02daa38eaa2e73d). Het systeem begint vangend een bepaalde hoeveelheid steekproeven die de definitie van de eerder vastgestelde opleidingsfilter (als om het even welk) aanpassen. Momenteel wordt de steekproefgrootte vastgesteld op 10% van de scorende populatie (gedefinieerd door een trainingsfilter), met een minimum van 20.000 en een maximum van 100.000, en is gebonden aan de scorende bevolkingsgrootte.

* Een dimensie van de Score heeft elementen die zich van 0% tot 100% uitstrekken die de waarschijnlijkheid bepalen van de bezoekers die de variabele van het Doel aanpassen.

