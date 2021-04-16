---
description: Radargrafieken geven snel focus op de gebieden die de meeste aandacht behoeven, door een visuele weergave van een set meetgegevens te bieden, en hoe ze zich verhouden of verschillen.
title: Radarvisualisatie
uuid: 39d67743-b6c1-46f1-99fd-7c71dfe07932
exl-id: 5385d903-422b-4936-bbb3-0d5ee4d286de
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '400'
ht-degree: 0%

---

# Radarvisualisatie{#radar-visualization}

Radargrafieken geven snel focus op de gebieden die de meeste aandacht behoeven, door een visuele weergave van een set meetgegevens te bieden, en hoe ze zich verhouden of verschillen.

Vaak hebt u meer dan één metrisch nodig om geselecteerde observaties in een werkruimte te begrijpen en te evalueren.

Deze visualisatie is handig voor vergelijkingen of benchmarks in de tabelselecties. U kunt bijvoorbeeld een werkruimtetabel toevoegen met winkels en vervolgens een radarvisualisatie toevoegen met metriek zoals Opbrengst, Bezoekers en Paginaweergaven. (Zoals in het scherm in de volgende procedure wordt getoond.) Terwijl u opslagselecties maakt in de tabel, verschuift de voetafdruk van het radardiagram en worden zwakke punten of sterke punten in de metriek voor de geselecteerde winkel geïdentificeerd.

Elke radiaal van een radargrafiek is metrisch, en een minimum van drie metriek wordt vereist. De metrische gegevens worden uitgezet ten opzichte van één verankerde metrische waarde. De verankerde metrisch en de Schaal aan de parameter van het Anker voor elke metrisch bepalen de schrapping van de metriek met betrekking tot benchmarks.

**Een radarvisualisatie maken**

1. Klik met de rechtermuisknop in de werkruimte en klik vervolgens op **[!UICONTROL Visualization]** > **[!UICONTROL Radar]**.

   ![](assets/client-rad.png)

1. Als u metriek wilt toevoegen, klikt u met de rechtermuisknop in de visualisatie en selecteert u **[!UICONTROL Add Metric]**.
1. Als u een metrische waarde aan het diagram wilt verankeren, klikt u met de rechtermuisknop op een metrische waarde en kiest u de volgende optie:

   **Anker aan deze metrische waarde:** gebruikt deze metrische waarde als benchmark waaraan andere metriek worden getrokken. U kunt één metrische waarde tegelijk verankeren. Elke metrische waarde in het diagram wordt gefilterd door de actieve werkruimteselectie of door geen filter. De benchmarkverhouding tussen deze twee waarden wordt uitgezet op de as tussen het middelpunt van de grafiek en de metrische naam op de radar. Nul wordt uitgezet in het midden.

1. Als u een metrische waarde wilt schalen met de verankerde metrische waarde, klikt u met de rechtermuisknop op de metrische waarde en kiest u de volgende optie:

   **Schalen met anker:** Wanneer deze optie is ingeschakeld, wordt de as van deze metrische waarde zo geschaald dat de benchmarkverhouding voor de geselecteerde ankermetrische waarde in de cirkel wordt uitgezet, met nul in het midden. Als deze optie niet is geselecteerd, is de cirkel een benchmarkverhouding van 1. Doorgaans schakelt u Schaal met anker in voor aftelbare meetgegevens, zoals bezoekers of Paginaweergaven, en schakelt u Schaal uit voor maateenheden voor de verhouding, zoals Omzetting, Gemiddelde sessieduur of Paginaweergaven per sessie.
