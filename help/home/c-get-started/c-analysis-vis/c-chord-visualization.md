---
description: Met de koordvisualisatie kunt u zowel de verhouding als de correlatie tussen de meetwaarden weergeven, waarbij grotere tekens worden weergegeven als een indicatie voor een sterkere correlatie.
title: Visualisatie kord
uuid: 3f322f58-f8f5-4d91-bdf8-4b5f9d7fb072
exl-id: d712f7b3-de2f-4ca4-a1bf-a2e4d42a084e
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '359'
ht-degree: 0%

---

# Visualisatie kord{#chord-visualization}

{{eol}}

Met de koordvisualisatie kunt u zowel de verhouding als de correlatie tussen de meetwaarden weergeven, waarbij grotere tekens worden weergegeven als een indicatie voor een sterkere correlatie.

Met de koordvisualisatie kunt u correlaties tussen metriek identificeren, zodat u mogelijke correlaties kunt toevoegen en gemakkelijk kunt evalueren. Het verstrekt ook een andere mening in om het even welke eerder gebouwd [Correlatiematrix](https://experienceleague.adobe.com/docs/data-workbench/using/client/analysis-visualizations/correlation-analysis/c-correlation-analysis.html). Met behulp van de koordvisualisatie kunt u geen positieve of negatieve correlatie tussen de meetgegevens identificeren, alleen dat er een correlatie bestaat. In bepaalde gevallen kan het bepalen van een directe of omgekeerde relatie worden geïdentificeerd door tegenmeetgegevens toe te passen.

1. **Open de **[!UICONTROL Chord]**visualisatie**.

   Klik met de rechtermuisknop in de werkruimte [!DNL Visualization > Predictive Analytics > Chord].

1. **Een Dimension selecteren in het menu**.

   Er wordt een lege visualisatie geopend, zodat u een dimensie kunt selecteren. De naam van de dimensie wordt boven aan de lege koordvisualisatie weergegeven.

   >[!NOTE]
   >
   >Als er al een correlatiematrix is geopend in de werkruimte, kunt u deze ook weergeven als een koordvisualisatie.

1. **Metriek kiezen om te correleren**.

   Metrische gegevens slepen vanaf het tabblad **[!UICONTROL Finder]** door te klikken **[!UICONTROL Ctrl-Alt]** om metriek van de lijst aan de grafiek te slepen. Nadat twee of meer metriek worden geselecteerd, zal de grafiek automatisch verfrissen en beginnen tonend correlatiegegevens. Voeg waar nodig metriek toe om gegevenspunten te correleren.

   ![](assets/chord_drag_metric.png)

   De koordvisualisatie toont het aandeel van het geheel dat door het gebied van elk segment wordt vertegenwoordigd. Blijf metriek toevoegen zoals nodig om significante verhoudingen te identificeren en te onderzoeken.

   ![](assets/chord_selected.png)

1. **De koordvisualisatie weergeven**.

   Beweeg over elke metrische waarde in de visualisatie om relaties te zien. In het voorbeeld ziet u een correlatie tussen Eenheden en de meeste andere metriek (behalve voor de **Bezoek duur** metrisch).

   ![](assets/chord_visualization_1.png)

   Wanneer u de muisaanwijzer op de knop **Bezoek duur** Metrisch op de visualisatie van het Koord, kunt u zien er zeer weinig of hoogstens zwakke correlatie tussen alle andere metriek is.

   ![](assets/chord_visualization_2.png)

1. **Instellingen wijzigen.** Klik met de rechtermuisknop op de koordvisualisatie om een menu te openen waarin u de afmetingen kunt wijzigen, de afmetingen kunt weergeven als absolute getallen of als percentages, de geselecteerde metrische waarde of alle metriek kunt verwijderen, kleuren en details kunt bewerken en waarden kunt exporteren naar een correlatiematrix.

   ![](assets/chord_menu.png)
