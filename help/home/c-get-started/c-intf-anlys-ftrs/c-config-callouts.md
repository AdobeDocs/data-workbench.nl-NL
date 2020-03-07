---
description: De callouts brengen aandacht aan een bepaald afmetingselement door een nieuwe visualisatie met een virtuele selectie van een bepaald afmetingselement in een visualisatie te creëren.
solution: Analytics
title: Vorm een callout
topic: Data workbench
uuid: 779764bd-86c3-49cf-aabc-edb39caf0490
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Vorm een callout{#configure-a-callout}

De callouts brengen aandacht aan een bepaald afmetingselement door een nieuwe visualisatie met een virtuele selectie van een bepaald afmetingselement in een visualisatie te creëren.

U kunt callouts toevoegen of uitgeven door de callout dossiers te vormen die in een Profielen \*profielnaam*\Context\Callout folder of the [!DNL Server] installatieomslag worden opgeslagen. Callouts die aandacht aan bepaald metrisch in een aantekenvelvisualisatie brengen worden genoemd metrische callouts. De metrische callout dossiers worden opgeslagen in de Profielen \*profielnaam*\Context\Metric Callout folder.

Voor instructies om een callout of metrische callout aan een visualisatie toe te voegen, zie het [Toevoegen van Callouts aan een Werkruimte](../../../home/c-get-started/c-vis/c-call-wkspc.md#concept-212b09e763044d938987b4a9c658adc0).

**Om een nieuw type van callout te creëren**

1. In om het even welke werkruimte, creeer een visualisatie die de gegevens bevat die u in het nieuwe callout type wilt verschijnen. Bijvoorbeeld, als u uw callout een lijst wilt zijn, creeert u een lijstvisualisatie die de gewenste metrische en afmeting toont.
1. Klik de hoogste grens van het callout venster met de rechtermuisknop aan en klik **[!UICONTROL Save]**.
1. Klik in het [!DNL Save] venster op ![](assets/btn_folder_up.png), dubbelklik **[!UICONTROL Context]** en dubbelklik op **[!UICONTROL Callout]**. Typ in het [!DNL File Name] veld een naam voor het bestand en klik op **[!UICONTROL Save]**. Het callout dossier wordt bewaard aan de het werkprofielnaam \*\Context\Callout folder van de Gebruiker.

   >[!NOTE]
   >
   >Wanneer het noemen van uw callout, kies een beschrijvende naam die op het visualisatietype en metrisch en afmeting wijst die het toont. Bijvoorbeeld, als u een callout van een lijstvisualisatie wilt tot stand brengen die de zittingen metrisch over de dimensie van de Dag tonen, kon u de callout &quot;Zittingen door de Lijst van de Dag noemen.&quot;

1. (Facultatief) om deze verandering aan alle gebruikers van het werkprofiel beschikbaar te stellen:

   1. In [!DNL Profile Manager], klik **[!UICONTROL Context]**, dan klik **[!UICONTROL Callout]**. Deze omslag bevat alle visualisatiedossiers ( [!DNL .vw]) die de bestaande callout types bepalen.

   1. Klik met de rechtermuisknop op het vinkje naast de bestandsnaam van de nieuwe callout in de [!DNL User] kolom en klik op **[!UICONTROL Save to]** > *&lt;**[!UICONTROL working profile name]**>*.

**Om een callout in een metrische callout te veranderen**

1. In [!DNL Profile Manager], klik **[!UICONTROL Context]**, dan klik **[!UICONTROL Callout]**. Deze omslag bevat alle visualisatiedossiers ( [!DNL .vw]) die de bestaande callout types bepalen.

1. Klik het vinkje naast het dossier met de rechtermuisknop aan - noem van het type van callout dat u wilt veranderen en klikken **[!UICONTROL Make Local]**. Nadat het dossier aan de lokale computer is gedownload, verschijnt een vinkje in de [!DNL User] kolom.

1. Klik het vinkje naast het dossier met de rechtermuisknop aan - noem in de [!DNL User] kolom en klik **[!UICONTROL Open]** > **[!UICONTROL In Notepad]**.

1. Bepaal de plaats van de [!DNL metric_y = ref:] ingang in het callout dossier en vervang de bestaande waarde met het woord Metrisch. De benadrukte tekst in het volgende dossierfragment toont waar u dit woord opneemt.

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

1. Klik op **[!UICONTROL File]** > **[!UICONTROL Save As]**. In het **[!UICONTROL Save As]** venster, klik eens, dan tweemaal klikken **[!UICONTROL Metric Callout]**. Typ in het [!DNL File Name] veld een naam voor het bestand en klik op **[!UICONTROL Save]**. Het metrische callout dossier wordt bewaard aan de Gebruiker \*het werk profielnaam*\Context\Metric Callout folder.

1. (Facultatief) om deze metrische callout ter beschikking te stellen van alle gebruikers van het het werk profiel, in het [!DNL Profile Manager], klik het vinkje naast het dossier - noem in de [!DNL User] kolom met de rechtermuisknop aan en klik **[!UICONTROL Save to]** > *&lt;**[!UICONTROL working profile name]**>*.

