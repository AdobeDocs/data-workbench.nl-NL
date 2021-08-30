---
description: De staafgrafiek in Data Workbench bevat nu een regressievergelijking voor meerdere meetwaarden in meerdere grafieken.
title: Regressieanalyse grafiek
uuid: 8512890e-f42b-4dce-826a-2b4bf2a215f4
exl-id: bfc76c4a-edd5-41fe-b875-c199ea3beab5
source-git-commit: 232117a8cacaecf8e5d7fcaccc5290d6297947e5
workflow-type: tm+mt
source-wordcount: '272'
ht-degree: 0%

---

# Regressieanalyse grafiek{#regression-analysis-graph}

De staafgrafiek in Data Workbench bevat nu een regressievergelijking voor meerdere meetwaarden in meerdere grafieken.

[Met staafgrafieken ](https://experienceleague.adobe.com/docs/data-workbench/using/client/analysis-visualizations/graphs/c-graphs.html) in Data Workbench kunt u metriek in een grafiek verkleinen tot metriek in een andere grafiek. Als u meerdere grafieken hebt, kunt u een metrische waarde (als de onafhankelijke variabele) vergelijken met een grafiek die andere metrische gegevens evalueert (als afhankelijke variabelen). Dit laat u de sterkte van het verband tussen één afhankelijke variabele (metrisch gevestigd eerst) en een reeks andere veranderende metriek (regressies met gevestigde afhankelijke metrisch) bepalen.

Met de regressieanalyse op basis van een grafiekvisualisatie kunnen analisten &#39;wat-als&#39;-scenario&#39;s uitvoeren. Welke gevolgen zal deze verhoging bijvoorbeeld hebben voor de inkomsten als de bezoeken tot dit niveau stijgen?

**Regressieanalyse instellen**

1. Selecteer grafiek als afhankelijke metrisch voor een regressievergelijking.

   Klik met de rechtermuisknop op de grafiek en selecteer **Instellen als standaard-metrisch voor regressie**.

   ![](assets/c_graph_regression_1.png)

1. Andere metrische grafieken instellen als onafhankelijke variabelen.

   Klik metrisch met de rechtermuisknop aan en selecteer **[!UICONTROL Regress with `<base metric name>`]** voor andere metriek.

   ![](assets/c_graph_regression.png)

1. U kunt regressie weergeven door met de rechtermuisknop op de grafiek te klikken om de balk omhoog en omlaag te verplaatsen.

   Als u met de rechtermuisknop op de grafiek voor een bepaalde waarde klikt, kunt u de regressieverhoudingen voor elke metrische waarde zien die voor naar boven of naar onder waarden wordt gebaseerd.

   ![](assets/c_graph_regression_2.png)

   Als mijn paginaweergaven bijvoorbeeld dalen naar 86.041, hebben de andere meetgegevens de volgende waarden: Bezoeken op 12.183 en Bezoekers op 12.028.

   ![](assets/c_graph_regression_3.png)

   Als de Bezoekers door Bezoek waarden tot 26.141 stijgen, dan zullen de andere metriek Bezoekingen bij 26.560 zijn en de Mening van de Pagina zal bij 189.091 zijn.
