---
description: Callouts zijn vensters die u aan een werkruimte toevoegt om aandacht aan een bepaald afmetingselement te brengen door een nieuwe visualisatie met een virtuele selectie van dat element te creëren.
solution: Analytics
title: Het toevoegen van callouts aan een werkruimte
topic: Data workbench
uuid: fb3dd74d-da20-40cb-bc96-e56d25003e48
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Het toevoegen van callouts aan een werkruimte{#adding-callouts-to-a-workspace}

Callouts zijn vensters die u aan een werkruimte toevoegt om aandacht aan een bepaald afmetingselement te brengen door een nieuwe visualisatie met een virtuele selectie van dat element te creëren.

De Werkbank van gegevens wordt geleverd met een standaardreeks callout types. Omdat uw implementatie volledig kan worden aangepast, kunnen de beschikbare callout types die in uw implementatie verschijnen van verschillen wat in deze gids gedocumenteerd is.

Door gebrek, verstrekt de Werkbank van Gegevens de volgende callouts:

* [Annotatie](../../../home/c-get-started/c-vis/c-call-wkspc.md#section-7b6742160b3f4aed872a09c8c023f90d)
* [Blanco-lijngrafiek](../../../home/c-get-started/c-vis/c-call-wkspc.md#section-5dcc0504bdb64ed4976f880e2f7b277f)
* [Blanco-kattenplot](../../../home/c-get-started/c-vis/c-call-wkspc.md#section-5dcc0504bdb64ed4976f880e2f7b277f)
* [Blanco tabel](../../../home/c-get-started/c-vis/c-call-wkspc.md#section-5dcc0504bdb64ed4976f880e2f7b277f)
* [Vertrouwen Legenda](../../../home/c-get-started/c-vis/c-call-wkspc.md#section-386d1293ddc24a0c9cccb332e20db791)
* [Metrische Legenda](../../../home/c-get-started/c-vis/c-call-wkspc.md#section-daa6d372c22246d9827880a9d6e804d8)

>[!NOTE]
>
>De callouts functioneren niet als selecties (namelijk beïnvloeden zij andere visualisaties binnen de werkruimte) tenzij u een selectie binnen de callout maakt.

U kunt callout definities toevoegen of uitgeven door de callout dossiers te vormen die in de de installatiemap van de *profielnaam*\Context\Callout folder of the [!DNL Server] worden opgeslagen. Zie het [Vormen Callouts](../../../home/c-get-started/c-intf-anlys-ftrs/c-config-callouts.md#concept-f6e91e172f5e4c009245c9c549beb76a).

## Om een annotatiecallout aan een visualisatie toe te voegen {#section-7b6742160b3f4aed872a09c8c023f90d}

1. Klik het element met de rechtermuisknop aan waarvoor u een callout wilt tot stand brengen, dan klik **[!UICONTROL Add Callout]** > **[!UICONTROL Annotation]** > **[!UICONTROL Image]** of **[!UICONTROL Add Callout]** > **[!UICONTROL Annotation]** > **[!UICONTROL Text]**. Een leeg venster toont met een zichtbare verbinding aan dat element.

   ![](assets/client-call.png)

   Om callouts aan de visualisaties van de Grafiek toe te voegen, moet u bij de bodem van de visualisatie (de basisas) met de rechtermuisknop aanklikken om een menu te openen.

   ![](assets/visualization_callout_linegraph.png)

1. Afhankelijk van uw selectie, voltooi de aangewezen stap:

   * Voor een tekstannotatie, typ of kleef de gewenste tekst in de callout, dan formatteer de tekst zoals aangewezen. Zie [Werken met tekstannotaties](../../../home/c-get-started/c-analysis-vis/c-annots/c-text-annots.md#concept-55b4aa3e0c58470b8e3c9d452e12a777).
   * Voor een beeldannotatie, kleef het gewenste beeld in de callout door het beeld te kopiëren, dan met de rechtermuisknop te klikken binnen de callout. Klik op **[!UICONTROL Paste image]**. Zie [Werken met afbeeldingsannotaties](../../../home/c-get-started/c-analysis-vis/c-annots/c-image-annots.md#concept-02081ed7d91c4fdcb8fc863f2a51c962).

## Om een lege lijst, een lijngrafiek, of een spatterplot toe te voegen callout aan een visualisatie {#section-5dcc0504bdb64ed4976f880e2f7b277f}

1. Klik het element met de rechtermuisknop aan waarvoor u een callout wilt tot stand brengen en **[!UICONTROL Add Callout]** > *&lt;**[!UICONTROL callout type]**>* klikken.

   Het volgende voorbeeld toont een Lege callout van de Lijst.

   ![](assets/vis_callout_blank_bar_graph.png)

1. Als u een dimensie wilt selecteren, klikt u met de rechtermuisknop **[!UICONTROL None]** en klikt u **[!UICONTROL Change Dimension]** > *&lt;**[!UICONTROL dimension name]**>*.

   >[!NOTE]
   >
   >Als u de afmeting binnen een visualisatie verandert die een callout heeft, verandert de callout van wordt verbonden met het element van de originele afmeting aan het worden verbonden met de volledige visualisatie.

## Om een vertrouwenslegende callout aan een visualisatie toe te voegen {#section-386d1293ddc24a0c9cccb332e20db791}

1. Klik het element met de rechtermuisknop aan waarvoor u de callout wilt tot stand brengen en **[!UICONTROL Add Callout]** > klikken **[!UICONTROL Confidence Legend]**.

   ![](assets/vis_callout_confidenceLegend.png)

1. Indien gewenst, verander het [!DNL Metric or Formula] gebied.

Voor de regels van de uitdrukkingssyntaxis, zie de Syntaxis van de Taal van de [Vraag](../../../home/c-get-started/c-qry-lang-syntx/c-qry-lang-syntx.md#concept-15d1d3f5164a47d49468c5acb7299d9f). Zie [vertrouwenwekkende](../../../home/c-get-started/c-analysis-vis/c-legends/c-conf-leg.md#concept-73db81c2c218427786c04068aa778efd)resultaten.

## Om een metrische legende callout aan een visualisatie toe te voegen {#section-daa6d372c22246d9827880a9d6e804d8}

1. Klik het element met de rechtermuisknop aan waarvoor u de callout wilt tot stand brengen en **[!UICONTROL Add Callout]** > klikken **[!UICONTROL Metric Legend]**.

   ![](assets/vis_callout_metricLegend.png)

1. Indien gewenst, voeg metriek aan toe of verwijder metriek uit de metrische legende.

Zie [Metrische Legends](../../../home/c-get-started/c-analysis-vis/c-legends/c-metric-leg.md#concept-e7195bc8f7844ae295bda3a88b028d5b).
