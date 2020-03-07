---
description: De grafiek van de Bar in de Werkbank van Gegevens omvat nu een regressievergelijking voor veelvoudige metriek over veelvoudige grafieken.
title: Regressieanalyse grafiek
uuid: 8512890e-f42b-4dce-826a-2b4bf2a215f4
translation-type: tm+mt
source-git-commit: cb3ca4b3b993f5f04f6b6cee25850600ff3d8986

---


# Regressieanalyse grafiek{#regression-analysis-graph}

De grafiek van de Bar in de Werkbank van Gegevens omvat nu een regressievergelijking voor veelvoudige metriek over veelvoudige grafieken.

[De grafieken](https://docs.adobe.com/content/help/en/data-workbench/using/client/analysis-visualizations/graphs/c-graphs.html) van de bar in de Werkbank van Gegevens laten u metriek in één grafiek aan metriek in een andere grafiek verminderen. Als u veelvoudige grafieken hebt, kunt u metrisch (als onafhankelijke variabele) vergelijken met een grafiek die andere metriek (als afhankelijke variabelen) evalueert. Dit laat u de sterkte van het verband tussen één afhankelijke variabele (metrisch gevestigd eerst) en een reeks andere veranderende metriek (regressies met gevestigde afhankelijke metrisch) bepalen.

De regressieanalyse op een grafiekvisualisatie staat analisten toe om &quot;wat-als&quot;scenario&#39;s uit te voeren. Als de bezoeken bijvoorbeeld tot dit niveau stijgen, welke gevolgen zal deze verhoging dan hebben voor de inkomsten?

**Regressieanalyse instellen**

1. Selecteer grafiek als afhankelijke metrisch voor een regressievergelijking.

   Klik op de grafiek met de rechtermuisknop en selecteer **Reeks als basis metrisch voor regressie**.

   ![](assets/c_graph_regression_1.png)

1. Plaats andere metrische grafieken als onafhankelijke variabelen.

   Klik metrisch met de rechtermuisknop aan en selecteer **[!UICONTROL Regress with `<base metric name>`]** voor andere metriek.

   ![](assets/c_graph_regression.png)

1. De regressie van de mening door op de grafiek met de rechtermuisknop te klikken om de bar naar boven en naar onder te bewegen.

   Als u op de grafiek voor een specifieke waarde met de rechtermuisknop klikt, kunt u de regressieverhoudingen voor elke metrisch dan zien die voor naar boven of naar onder waarden wordt gebaseerd.

   ![](assets/c_graph_regression_2.png)

   Bijvoorbeeld, als mijn Meningen van de Pagina aan 86.041 verminderen, dan zullen de andere metriek deze waarden hebben: Bezoek op 12.183 en Bezoek op 12.028 bezoekers.

   ![](assets/c_graph_regression_3.png)

   Als de Bezoekers door de waarden van Bezoeken tot 26.141 stijgen, dan zullen de andere metriek Bezoeken bij 26.560 zijn en de Meningen van de Pagina zullen bij 189.091 zijn.

