---
description: Met een binair filter in de correlatiematrix kunt u de waarden voor een of beide gecorreleerde metriek beperken om de vergelijking beter te kunnen focussen.
title: Binair filter in de matrix Correlatie
uuid: 61c3ca37-cfa2-49dc-87de-4e9a44647eca
exl-id: e693fc72-5697-4c47-a498-e0d4d875c688
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '210'
ht-degree: 0%

---

# Binair filter in de Correlatie Matrix{#binary-filter-in-the-correlation-matrix}

Met een binair filter in de correlatiematrix kunt u de waarden voor een of beide gecorreleerde metriek beperken om de vergelijking beter te kunnen focussen.

Een binair filter instellen op een correlatiematrix:

1. Klik met de rechtermuisknop op een metrische naam in de Matrix Correlatie.
1. Selecteer **Metrische details bewerken**.

   ![](assets/correlation_matrix_binary_filter.png)

   Het venster **[!UICONTROL Edit Correlation Metric Details]** wordt geopend.

   ![](assets/correlation_matrix_metric_details.png)

1. Stel een binair filter in.

   Klik eerst op de instelling **[!UICONTROL Inactive]**. Hiermee wordt geschakeld om het filter in te stellen als **[!UICONTROL Active]** en de velden **Comparison** en **Value** weer te geven.

   Selecteer vervolgens een **[!UICONTROL Comparison]**-operator en stel **[!UICONTROL Value]** ervan in om een filter voor de geselecteerde metrische waarde in te stellen.

>[!IMPORTANT]
>
>Het Binaire Filter voor Data Workbench 6.2 is bijgewerkt met nieuwe eigenschappen, die u vereisen om het even welke correlatiematrix met een binair filter te herbouwen dat in vorige versies wordt gebouwd.

## Dimension-elementen toevoegen {#section-f19f4e0368ca488e92d1e28bcc24417c}

U kunt ook een dimensie-element toevoegen om metrisch te beperken. Aan een metrische waarde kan slechts één element zijn gekoppeld.

![](assets/correlation_matrix_element.png)

Klik met de rechtermuisknop in de werkruimte en selecteer **Tabel**. Open een dimensie met de elementen en sleep naar de **[!UICONTROL Element]**-instelling in het venster Metrische gegevens van correlatie bewerken of zet een metrische waarde neer in de matrix Correlatie.
