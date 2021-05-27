---
description: Bijschriften zijn vensters die u toevoegt aan een werkruimte om de aandacht op een bepaald afmetingselement te vestigen door een nieuwe visualisatie met een virtuele selectie van dat element te creëren.
title: Callouts toevoegen aan een werkruimte
uuid: fb3dd74d-da20-40cb-bc96-e56d25003e48
exl-id: fcdb9231-d44a-4287-b799-6a66f7f79432
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '440'
ht-degree: 0%

---

# Bijschriften toevoegen aan een werkruimte{#adding-callouts-to-a-workspace}

Bijschriften zijn vensters die u toevoegt aan een werkruimte om de aandacht op een bepaald afmetingselement te vestigen door een nieuwe visualisatie met een virtuele selectie van dat element te creëren.

De Data Workbench wordt geleverd met een standaardreeks callout types. Omdat uw implementatie volledig kan worden aangepast, kunnen de beschikbare callout types die in uw implementatie verschijnen van verschillen van wat in deze gids wordt gedocumenteerd.

Standaard biedt Data Workbench de volgende callouts:

* [Aantekening](../../../home/c-get-started/c-vis/c-call-wkspc.md#section-7b6742160b3f4aed872a09c8c023f90d)
* [Lege lijngrafiek](../../../home/c-get-started/c-vis/c-call-wkspc.md#section-5dcc0504bdb64ed4976f880e2f7b277f)
* [Leeg spreidingspad](../../../home/c-get-started/c-vis/c-call-wkspc.md#section-5dcc0504bdb64ed4976f880e2f7b277f)
* [Lege tabel](../../../home/c-get-started/c-vis/c-call-wkspc.md#section-5dcc0504bdb64ed4976f880e2f7b277f)
* [Vertrouwen Legenda](../../../home/c-get-started/c-vis/c-call-wkspc.md#section-386d1293ddc24a0c9cccb332e20db791)
* [Metrische legenda](../../../home/c-get-started/c-vis/c-call-wkspc.md#section-daa6d372c22246d9827880a9d6e804d8)

>[!NOTE]
>
>Bijschriften functioneren niet als selecties (dat wil zeggen, ze hebben geen invloed op andere visualisaties in de werkruimte), tenzij u een selectie maakt in de bijschrift.

U kunt callout definities toevoegen of uitgeven door de callout dossiers te vormen die in *profielnaam*\Context\Callout folder of the [!DNL Server] installatiemap worden opgeslagen. Zie [Het vormen Callouts](../../../home/c-get-started/c-intf-anlys-ftrs/c-config-callouts.md#concept-f6e91e172f5e4c009245c9c549beb76a).

## Een annotatiebijschrift toevoegen aan een visualisatie {#section-7b6742160b3f4aed872a09c8c023f90d}

1. Klik met de rechtermuisknop op het element waarvoor u een bijschrift wilt maken en klik vervolgens op **[!UICONTROL Add Callout]** > **[!UICONTROL Annotation]** > **[!UICONTROL Image]** of **[!UICONTROL Add Callout]** > **[!UICONTROL Annotation]** > **[!UICONTROL Text]**. Er wordt een leeg venster weergegeven met een zichtbare verbinding met dat element.

   ![](assets/client-call.png)

   Als u callouts wilt toevoegen aan grafiekvisualisaties, moet u met de rechtermuisknop klikken onder aan de visualisatie (de basisas) om een menu te openen.

   ![](assets/visualization_callout_linegraph.png)

1. Voer afhankelijk van uw selectie de juiste stap uit:

   * Voor een tekstannotatie typt of plakt u de gewenste tekst in het bijschrift en maakt u de tekst op. Zie [Werken met tekstannotaties](../../../home/c-get-started/c-analysis-vis/c-annots/c-text-annots.md#concept-55b4aa3e0c58470b8e3c9d452e12a777).
   * Voor een afbeeldingsannotatie plakt u de gewenste afbeelding in het bijschrift door de afbeelding te kopiëren en vervolgens met de rechtermuisknop in het bijschrift te klikken. Klik op **[!UICONTROL Paste image]**. Zie [Werken met afbeeldingsannotaties](../../../home/c-get-started/c-analysis-vis/c-annots/c-image-annots.md#concept-02081ed7d91c4fdcb8fc863f2a51c962).

## Een lege tabel, lijngrafiek of spreidingsperceel toevoegen als bijschrift voor een visualisatie {#section-5dcc0504bdb64ed4976f880e2f7b277f}

1. Klik met de rechtermuisknop op het element waarvoor u een bijschrift wilt maken en klik op **[!UICONTROL Add Callout]** > *&lt;**[!UICONTROL callout type]**>*.

   In het volgende voorbeeld ziet u een lege bijschrift bij Tabel.

   ![](assets/vis_callout_blank_bar_graph.png)

1. Als u een dimensie wilt selecteren, klikt u met de rechtermuisknop **[!UICONTROL None]** en klikt u **[!UICONTROL Change Dimension]** > *&lt;**[!UICONTROL dimension name]**>*.

   >[!NOTE]
   >
   >Als u de dimensie binnen een visualisatie verandert die een callout heeft, verandert de callout van wordt verbonden met het element van de originele afmeting aan het worden verbonden met de volledige visualisatie.

## Een betrouwbaarheidsverklaring toevoegen aan een visualisatie {#section-386d1293ddc24a0c9cccb332e20db791}

1. Klik met de rechtermuisknop op het element waarvoor u de callout wilt maken en klik op **[!UICONTROL Add Callout]** > **[!UICONTROL Confidence Legend]**.

   ![](assets/vis_callout_confidenceLegend.png)

1. Wijzig desgewenst het veld [!DNL Metric or Formula].

Voor de regels van de uitdrukkingssyntaxis, zie [Syntaxis van de Taal van de Vraag](../../../home/c-get-started/c-qry-lang-syntx/c-qry-lang-syntx.md#concept-15d1d3f5164a47d49468c5acb7299d9f). Zie [Vertrouwelijkheidshulpmiddelen](../../../home/c-get-started/c-analysis-vis/c-legends/c-conf-leg.md#concept-73db81c2c218427786c04068aa778efd).

## Een metrische legenda-callout toevoegen aan een visualisatie {#section-daa6d372c22246d9827880a9d6e804d8}

1. Klik met de rechtermuisknop op het element waarvoor u de callout wilt maken en klik op **[!UICONTROL Add Callout]** > **[!UICONTROL Metric Legend]**.

   ![](assets/vis_callout_metricLegend.png)

1. Voeg desgewenst metriek toe aan de metrische legenda of verwijder metriek.

Zie [Metrische legenda](../../../home/c-get-started/c-analysis-vis/c-legends/c-metric-leg.md#concept-e7195bc8f7844ae295bda3a88b028d5b).
