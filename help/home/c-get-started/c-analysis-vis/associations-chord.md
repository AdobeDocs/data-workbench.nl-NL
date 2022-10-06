---
description: De visualisatie van het Koord van de Vereniging staat u toe om zowel de verhouding als de vereniging tussen metriek, dimensies, en elementen te tonen, tonend grotere koorden als aanwijzing van een sterkere vereniging.
title: Visualisatie van associatiekoord
uuid: c656ffc8-e45a-44c0-a29b-cdc10dcbd1f2
exl-id: e71394ef-4895-4a3e-912d-d6f56ca8f001
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '428'
ht-degree: 0%

---

# Visualisatie van associatiekoord{#association-chord-visualization}

{{eol}}

De visualisatie van het Koord van de Vereniging staat u toe om zowel de verhouding als de vereniging tussen metriek, dimensies, en elementen te tonen, tonend grotere koorden als aanwijzing van een sterkere vereniging.

In de tabel Koppelingen worden waarden vergeleken met de V-berekening van Cramer in plaats van de correlatiecoëfficiënt van Pearson te gebruiken, zoals gebruikt in de tabel [Correlatiematrix](/help/home/c-get-started/c-analysis-vis/c-correlation-analysis/c-correlation-analysis.md) en [Correlatiekoord](/help/home/c-get-started/c-analysis-vis/associations-visualization.md) visualisaties (deze kunnen metriek slechts vergelijken, terwijl de Lijst van de Vereniging en het Koord metriek, afmetingen, en elementen kunnen vergelijken). Het koord van Verenigingen verstrekt ook een andere mening in eerder gebouwd [Koppelingstabel](../../../home/c-get-started/c-analysis-vis/associations-visualization.md#concept-9d937dda38174875b32095c6eaf22f2f).

**Een associatiekoord maken**

1. Klik in een werkruimte met de rechtermuisknop **Visualisatie > Predictive Analytics > Association Chord**.

   Er wordt een menu geopend waarin u een uitgebreide dimensie in de lijst kunt selecteren.

   ![](assets/association_chord1.png)

   Als deze optie is geselecteerd, wordt de lege Associatietabel geopend met de geselecteerde Dimension die in de titel is geïdentificeerd. ![](assets/association_chord2.png)

1. **Een metrisch element, dimensie of dimensie-element selecteren**.

   Klik met de rechtermuisknop op de koordvisualisatie en selecteer **Metrisch toevoegen** of **Dimension toevoegen**. Selecteer items in het menu om aan het akkoord toe te voegen.

   U kunt ook metriek en afmetingen slepen vanuit de **[!UICONTROL Finder]** door te klikken **[!UICONTROL Ctrl-Alt]** en het slepen van metriek en afmetingen aan het koord. Of sleep dimensie-elementen rechtstreeks van een open tabel naar de koordvisualisatie.

1. **Kies aanvullende metriek, afmetingen en elementen die u wilt koppelen**.

   Nadat twee of meer waarden zijn geselecteerd, wordt het diagram automatisch vernieuwd en wordt het weergeven van koppelingsgegevens gestart. Voeg desgewenst metriek toe aan de gegevenspunten.

   ![](assets/association_chord.png)

   De koordvisualisatie toont het aandeel van het geheel dat door het gebied van elk segment wordt vertegenwoordigd. Ga door met het toevoegen van metriek/dimensies/elementen waar nodig om significante relaties te identificeren en te onderzoeken.

1. **De koordvisualisatie weergeven**.

   Beweeg over elke waarde in de visualisatie om relaties te zien.

1. **Instellingen wijzigen.** Klik met de rechtermuisknop op de koordvisualisatie om een menu te openen waarin u de afmetingen, afmetingen of elementen als absolute getallen of als percentages weergeeft, de geselecteerde metrische of alle metrische waarden verwijdert, kleuren en details bewerkt en waarden exporteert naar een tabel met koppelingen.

**Om een Koord van de Vereniging van een Lijst van de Vereniging te bouwen:**

1. Een **Associatietabel** visualisatie.
1. Klik met de rechtermuisknop en selecteer **Visualisatie kord exporteren**. Een diagram van het Koord van de Vereniging zal met waarden openen die in de Lijst van de Vereniging worden geselecteerd. ![](assets/association_table_to_chord.png)

>[!IMPORTANT]
>
>Het uitvoeren van een Lijst van de Vereniging van een Diagram van het Koord van de Vereniging die minstens één metrisch bevat zal in gedupliceerde elementen in de rijen/kolommen van de Lijst van de Vereniging resulteren. Om dubbele elementen te vermijden, creeer een nieuwe Lijst van de Vereniging en voeg de gewenste elementen eerder dan het uitvoeren van de elementen van een Diagram van het Koord van de Vereniging toe.
