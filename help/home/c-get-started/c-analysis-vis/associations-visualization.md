---
description: De visualisatie van de Lijst van de Vereniging laat u metriek met metriek, dimensies, en afmetingselementen associëren gebruikend het algoritme van V van Cramer.
title: Visualisatie van associatietabellen
uuid: 4563c336-3377-4929-8694-8c0d00866825
exl-id: 3fc2c025-d369-45ed-8c9e-eb4a0ac412b7
source-git-commit: 232117a8cacaecf8e5d7fcaccc5290d6297947e5
workflow-type: tm+mt
source-wordcount: '309'
ht-degree: 0%

---

# Visualisatie van associatietabellen{#association-table-visualization}

De visualisatie van de Lijst van de Vereniging laat u metriek met metriek, dimensies, en afmetingselementen associëren gebruikend het algoritme van V van Cramer.

In de tabel Koppeling worden waarden vergeleken met de V-berekening van Cramer in plaats van de correlatiecoëfficiënt van Pearson te gebruiken, zoals gebruikt in de [Correlatiematrix](https://experienceleague.adobe.com/docs/data-workbench/using/client/analysis-visualizations/correlation-analysis/c-correlation-analysis.html) en [Correlatie Chord](https://experienceleague.adobe.com/docs/data-workbench/using/client/analysis-visualizations/c-chord-visualization.html) visualisaties (deze kunnen alleen meetgegevens vergelijken, terwijl de Associatietabel en [Associatiekoord](../../../home/c-get-started/c-analysis-vis/associations-chord.md#concept-51d0bda998474dd5946cc2a9b8393445) metriek kunnen vergelijken).

## Een associatietabel maken {#section-87ed12ccc1af4196a1b6534e621c4cbb}

De Lijst van de Vereniging vergelijkt metriek over een aftelbare of niet aftelbare dimensie. De tabel kan worden gewijzigd om koppelingen binnen de visualisatie te markeren door kleuren te kiezen of om de tabel te renderen als een tekstkaart, een warmteoverzicht of beide.

1. Open een tabel met koppelingen.

   Klik met de rechtermuisknop [!DNL Visualization] > [!DNL Predictive Analytics] > [!DNL Association Table].

   ![](assets/association_table.png)

1. Selecteer een uitgebreide afmeting-een Clickthrough, Hit, Product, Bezoek, of de afmeting van de Bezoeker. Een Lijst van de Vereniging zal met de uitgebreide afmeting openen die in de hoek wordt geïdentificeerd en zijn bijbehorende metrisch die in zowel de rij als kolom wordt geplaatst.

   ![](assets/association_table1.png)

   De lijst van Verenigingen gebruikt Cramer&#39;s V als symmetrische correlatie, resulterend in geselecteerde metriek, dimensies, en elementenwaarden die in zowel de kolommen als de rijen van een Lijst van de Vereniging worden weerspiegeld. Als u bijvoorbeeld de uitgebreide **Product**-afmeting selecteert, wordt de **[!UICONTROL Visits]**-metrische waarde gebruikt als de bijbehorende metrische waarde in zowel de rij als de kolom van de tabel. Dit levert een perfecte maar nutteloze vergelijking op (1,00) omdat de vergeleken waarden identiek zijn.

1. Voeg meer waarden toe aan de tabel Koppeling.

   Klik met de rechtermuisknop in een kolom of rij en selecteer **Metrisch toevoegen** of **Dimension toevoegen**. U kunt metriek en afmetingen van een **paneel van de Vinder** ook slepen. U kunt Dimension-elementen ook slepen en neerzetten van een open tabel naar de tabelvisualisatie.

   ![](assets/association_table2.png)

   >[!NOTE]
   >
   >De tabel Koppeling bevat een limiet van tien rijen en kolommen.
