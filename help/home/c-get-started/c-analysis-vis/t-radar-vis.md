---
description: De grafieken van de radar verstrekken snelle nadruk op de gebieden die in de meeste behoefte aan aandacht zijn, door een visuele mening van een reeks metriek te verstrekken, en hoe zij betrekking hebben of verschillen.
solution: Analytics
title: Radarvisualisatie
topic: Data workbench
uuid: 39d67743-b6c1-46f1-99fd-7c71dfe07932
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Radarvisualisatie{#radar-visualization}

De grafieken van de radar verstrekken snelle nadruk op de gebieden die in de meeste behoefte aan aandacht zijn, door een visuele mening van een reeks metriek te verstrekken, en hoe zij betrekking hebben of verschillen.

Vaak hebt u meer dan één metrisch nodig om geselecteerde observaties in een werkruimte te begrijpen en te evalueren.

Deze visualisatie is nuttig voor vergelijkingen of benchmarks onder de lijstselecties. Bijvoorbeeld, zou u een werkruimtetabel kunnen toevoegen die van opslag een lijst maakt, dan een radar visualisatie met metriek zoals Opbrengsten, Bezoekers, en de Meningen van de Pagina toevoegen. (Zoals getoond in het scherm in de volgende procedure.) Aangezien u opslagselecties in de lijst maakt, verschuift de de voetafdruk van de radar, identificeert het identificeren van zwakheden of sterke punten in de metriek voor de geselecteerde opslag.

Elke straal van een radargrafiek is metrisch, en een minimum van drie metriek wordt vereist. De metrische gegevens worden uitgezet met betrekking tot één verankerde metrisch. De verankerde metrisch en de Schaal aan de parameter van het Anker voor elke metrisch bepalen het schrapen van de metriek met betrekking tot benchmarks.

**Om een radarvisualisatie te maken**

1. Klik in de Werkruimte met de rechtermuisknop aan, dan klik **[!UICONTROL Visualization]** > **[!UICONTROL Radar]**.

   ![](assets/client-rad.png)

1. Om metriek toe te voegen, klik in de visualisatie met de rechtermuisknop aan en selecteer **[!UICONTROL Add Metric]**.
1. Om metrisch aan de grafiek te verankeren, klik op metrisch met de rechtermuisknop aan en kies de volgende optie:

   **Anker aan deze metrisch:** Gebruikt dit metrisch als benchmark waaraan andere metriek worden getrokken. U kunt metrisch tegelijkertijd verankeren. Elke metrisch op de grafiek wordt gefiltreerd door de actieve werkruimteselectie, of door geen filter. De benchmarkverhouding tussen deze twee waarden wordt uitgezet op de as tussen het middelpunt van de grafiek en de metrische naam op de radar. Nul wordt uitgezet in het midden.

1. Om metrisch met verankerde metrisch te schrapen, klik metrisch met de rechtermuisknop aan en kies de volgende optie:

   **Schaal met anker:** Wanneer toegelaten, wordt de as van deze metrisch geschraapt zodat de benchmarkverhouding voor geselecteerd metrisch anker in de cirkel, met nul op het centrum wordt uitgezet. Wanneer niet geselecteerd, vertegenwoordigt de cirkel een benchmarkverhouding van 1. Typisch, zet u Schaal met Anker voor telbare metriek, zoals Bezoekers of de Meningen van de Pagina aan, en zet het voor verhoudingsmetriek, zoals Omzetting, Gemiddelde Duur van de Zitting, of de Meningen van de Pagina per Zitting uit.

