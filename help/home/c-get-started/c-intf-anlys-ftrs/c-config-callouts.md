---
description: Bijroepen brengen aandacht aan een bepaald afmeting element door een nieuwe visualisatie met een virtuele selectie van een bepaald afmeting element in een visualisatie te creëren.
title: Een bijschrift configureren
uuid: 779764bd-86c3-49cf-aabc-edb39caf0490
exl-id: 509163b2-0bd1-47b4-8612-aac460a501cc
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '492'
ht-degree: 0%

---

# Een bijschrift configureren{#configure-a-callout}

{{eol}}

Bijroepen brengen aandacht aan een bepaald afmeting element door een nieuwe visualisatie met een virtuele selectie van een bepaald afmeting element in een visualisatie te creëren.

U kunt callouts toevoegen of uitgeven door de callout dossiers te vormen die in een Profiles \*profiel naam* \ van de Context \ omslag Bijschrift van Profiles worden opgeslagen [!DNL Server] installatiemap. Bijschriften die aandacht aan bepaalde metrisch in een aantekenvelvisualisatie brengen worden genoemd metrische callouts. Metrische bijschriftbestanden worden opgeslagen in de map Profielen\*profielnaam*\Context\Metric Bijschrift.

Voor instructies om een callout of metrische callout aan een visualisatie toe te voegen, zie [Bijschriften toevoegen aan een werkruimte](../../../home/c-get-started/c-vis/c-call-wkspc.md#concept-212b09e763044d938987b4a9c658adc0).

**Een nieuw type bijschrift maken**

1. In om het even welke werkruimte, creeer een visualisatie die de gegevens bevat die u in het nieuwe bijschrifttype wilt verschijnen. Als u bijvoorbeeld wilt dat de callout een tabel is, maakt u een tabelvisualisatie met de gewenste metrische en afmeting.
1. Klik met de rechtermuisknop op de bovenrand van het bijschriftvenster en klik op **[!UICONTROL Save]**.
1. In de [!DNL Save] venster, klikt u op ![](assets/btn_folder_up.png), dubbelklikken **[!UICONTROL Context]** en dubbelklik vervolgens **[!UICONTROL Callout]**. In de [!DNL File Name] veld, typt u een naam voor het bestand en klikt u op **[!UICONTROL Save]**. Het bijschriftbestand wordt opgeslagen in de map User\*working profile name*\Context\Bijschrift.

   >[!NOTE]
   >
   >Wanneer het noemen van uw callout, kies een beschrijvende naam die op het visualisatietype en metrisch en afmeting wijst die het toont. Bijvoorbeeld, als u een callout van een lijstvisualisatie wilt tot stand brengen die metrische zittingen over de dimensie van de Dag toont, kon u de callout &quot;Zittingen door Lijst van de Dag noemen.&quot;

1. (Optioneel) Deze wijziging beschikbaar stellen voor alle gebruikers van het werkprofiel:

   1. In de [!DNL Profile Manager], klikt u op **[!UICONTROL Context]** en klik vervolgens op **[!UICONTROL Callout]**. Deze map bevat alle visualisatiebestanden ( [!DNL .vw]) die de bestaande bijschrifttypen definiëren.

   1. Klik met de rechtermuisknop op het vinkje naast de bestandsnaam van het nieuwe bijschrift in het dialoogvenster [!DNL User] kolom en klik op **[!UICONTROL Save to]** > *&lt;**[!UICONTROL working profile name]**>*.

**Een callout wijzigen in een metrische callout**

1. In de [!DNL Profile Manager], klikt u op **[!UICONTROL Context]** en klik vervolgens op **[!UICONTROL Callout]**. Deze map bevat alle visualisatiebestanden ( [!DNL .vw]) die de bestaande bijschrifttypen definiëren.

1. Klik met de rechtermuisknop op het vinkje naast de bestandsnaam van het type bijschrift dat u wilt wijzigen en klik op **[!UICONTROL Make Local]**. Nadat het bestand naar de lokale computer is gedownload, wordt in het dialoogvenster [!DNL User] kolom.

1. Klik met de rechtermuisknop op het vinkje naast de bestandsnaam in het dialoogvenster [!DNL User] kolom en klik op **[!UICONTROL Open]** > **[!UICONTROL In Notepad]**.

1. Zoek de [!DNL metric_y = ref:] in het bijschriftbestand en vervangt u de bestaande waarde door het woord Metrisch. De gemarkeerde tekst in het volgende bestandsfragment laat zien waar u dit woord invoegt.

   ```
   window = simpleBorderWindow: 
     client = graph: 
       bars = bool: true
       dim_x = ref: wdata/model/dim/dimension name
       lines = bool: false
       metrics = vector: 1 items
         0 = gr_metric: 
           metric_y = ref: Metric
           yaxis = axisLegend: 
             max_value = double: maximum y-value
             min_value = double: minimum y-value
             zoom_max = double: maximum y-zoom
             zoom_min = double: minimum y-zoom
   . . . 
   ```

1. Klik op **[!UICONTROL File]** > **[!UICONTROL Save As]**. In de **[!UICONTROL Save As]** venster, klikt u eenmaal en dubbelklikt u vervolgens **[!UICONTROL Metric Callout]**. In de [!DNL File Name] veld, typt u een naam voor het bestand en klikt u op **[!UICONTROL Save]**. Het metrische bijschriftbestand wordt opgeslagen in de map voor metrische bijschriften in de map Gebruiker\*werkprofielnaam*\Context\Metric.

1. (Optioneel) U kunt deze metrische bijschrift als volgt beschikbaar maken voor alle gebruikers van het werkprofiel: [!DNL Profile Manager]klikt u met de rechtermuisknop op het vinkje naast de bestandsnaam in het dialoogvenster [!DNL User] kolom en klik op **[!UICONTROL Save to]** > *&lt;**[!UICONTROL working profile name]**>*.
