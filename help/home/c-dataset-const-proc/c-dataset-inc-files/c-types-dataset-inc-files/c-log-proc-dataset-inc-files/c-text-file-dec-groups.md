---
description: De verwerking van logboekdossiers als logboekbronnen vereist de definitie van een decoder binnen de Dataset van de Verwerking van het Logboek omvat dossier om gebieden van gegevens uit de logboekingangen te halen.
solution: Analytics
title: Decodergroepen tekstbestand
topic: Data workbench
uuid: 3ff9700b-4f34-4098-8827-6856897bdb28
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Decodergroepen tekstbestand{#text-file-decoder-groups}

De verwerking van logboekdossiers als logboekbronnen vereist de definitie van een decoder binnen de Dataset van de Verwerking van het Logboek omvat dossier om gebieden van gegevens uit de logboekingangen te halen.

Het bepalen van de decodergroepen van het tekstdossier voor de bronnen van het logboekdossier vereist kennis van de structuur en de inhoud van het logboekdossier, de te halen gegevens, en de gebieden waarin dat gegeven wordt opgeslagen. Deze sectie verstrekt basisbeschrijvingen van de parameters die u voor decoders kunt specificeren, maar de manier waarin u om het even welke decoder gebruikt hangt van het logboekdossier af dat uw brongegevens bevat.

Voor informatie over formaatvereisten voor het logboekbronnen van het logboekdossier, zie de Dossiers [van het](../../../../../home/c-dataset-const-proc/c-log-proc-config-file/c-log-sources.md#concept-3d4fb817c057447d90f166b1183b461e)Logboek. Voor hulp bij het bepalen van de decoders van het tekstdossier, contacteer Adobe.

Een decodergroep van het tekstdossier kan omvatten:

* [Regelmatige expressiecoden](../../../../../home/c-dataset-const-proc/c-dataset-inc-files/c-types-dataset-inc-files/c-log-proc-dataset-inc-files/c-text-file-dec-groups.md#section-67aca2c1f008404da7f845a64abec97c)
* [Afzonderlijke decoders](../../../../../home/c-dataset-const-proc/c-dataset-inc-files/c-types-dataset-inc-files/c-log-proc-dataset-inc-files/c-text-file-dec-groups.md#section-7e0a23decdbc4c75ae750a42446997a6)

## Regelmatige expressiecoden {#section-67aca2c1f008404da7f845a64abec97c}

Een regelmatige uitdrukkingsdecoder identificeert complexe koordpatronen binnen de logboekingangen in een logboekdossier en haalt deze patronen als gebieden van gegevens uit. Voor elke decoder, moet het aantal gebieden het aantal het vangen van sub-patronen in de regelmatige uitdrukking gelijk zijn. Het gedeelte van de lijn die het nde vangen sub-patroon aanpast wordt toegewezen aan het nde gebied voor die lijn.

**Om een regelmatige uitdrukkingsdecoder aan een decodergroep van het tekstdossier toe te voegen**

1. Open het [!DNL Log Processing Dataset Include] dossier zoals die in het [Uitgeven van Bestaande Dataset wordt beschreven omvat Dossiers](../../../../../home/c-dataset-const-proc/c-dataset-inc-files/c-work-dataset-inc-files/t-edit-ex-dataset-inc-files.md#task-456c04e38ebc425fb35677a6bb6aa077) en voegt een decodergroep van het tekstdossier toe. Zie de groepen van de [Decoder van de lijstingang](../../../../../home/c-dataset-const-proc/c-dataset-inc-files/c-types-dataset-inc-files/c-log-proc-dataset-inc-files/c-log-proc-dataset-inc-files.md#concept-999475a22519432e98844622ca95b6ab).

1. Klik **[!UICONTROL Decoders]** onder de pas gecreëerde decodergroep met de rechtermuisknop aan, dan klik **[!UICONTROL Add new]** > **[!UICONTROL Regular Expression]**.

1. Geef de volgende informatie op:

   * **Velden:** Lijst van de gebieden in het logboekdossier. Als om het even welke hier bepaalde gebieden tot de transformatiefase van datasetconstructie moeten worden overgegaan, moeten die gebieden in de parameter van Gebieden van één van de [!DNL Log Processing Dataset Include] dossiers voor de dataset worden vermeld. De gebiedsnamen van de douane moeten met &quot;x-&quot;beginnen.

   * **Naam:** Facultatief herkenningsteken voor de decoder.
   * **Regelmatige expressie:** Gebruikt om de gewenste gebieden uit elke lijn in het dossier te halen.

1. Herhaal stappen 4 en 5 voor een andere decoders die u aan de groep wilt toevoegen.
1. Om het [!DNL Log Processing Dataset Include] dossier op te slaan, klik **[!UICONTROL (modified)]** bij de bovenkant van het venster met de rechtermuisknop aan en klik **[!UICONTROL Save]**.

1. Om de plaatselijk aangebrachte veranderingen aan te brengen worden van kracht, in [!DNL Profile Manager], klik het vinkje voor het dossier in de [!DNL User] kolom met de rechtermuisknop aan. Klik **[!UICONTROL Save to]** > *&lt;**[!UICONTROL profile name]**>*, waar de profielnaam de naam van het datasetprofiel of het geërfte profiel is waartot de dataset dossier behoort.

Sla het gewijzigde configuratiebestand niet op in een van de interne profielen die door Adobe worden geleverd, omdat uw wijzigingen worden overschreven wanneer u updates voor deze profielen installeert.

>[!NOTE]
>
>Een bepaald logboekdossier kan veelvoudige regelmatige uitdrukkingsdecoders hebben. De orde waarin u de decoders bepaalt is belangrijk: de eerste decoder om een lijn in het logboekdossier aan te passen is gebruikt om die lijn te decoderen.

Dit voorbeeld illustreert het gebruik van een regelmatige uitdrukkingsdecoder om gebieden van gegevens uit een lusje-afgebakend tekstdossier te halen. U kunt het zelfde resultaat bereiken door een begrensde decoder met een lusjescheiding te bepalen.

![](assets/cfg_LogProcessingInclude_RegExpDecoder.png)

Voor meer informatie over regelmatige uitdrukkingsdecoders, met inbegrip van terminologie en syntaxis, zie [Regelmatige Uitdrukkingen](../../../../../home/c-dataset-const-proc/c-reg-exp.md#concept-070077baa419475094ef0469e92c5b9c).

## Afzonderlijke decoders {#section-7e0a23decdbc4c75ae750a42446997a6}

Een afgebakende decoder decodeert een logboekdossier de waarvan gebieden door één enkel karakter worden afgebakend. Het aantal velden moet overeenkomen met het aantal kolommen in het afgebakende bestand. nochtans, niet moeten alle gebieden worden genoemd. Als een gebied leeg wordt verlaten, wordt de kolom nog vereist in het logboekdossier, maar de decoder negeert het.

**Om een afgebakende decoder aan een decodergroep van het tekstdossier toe te voegen**

1. Open het [!DNL Log Processing Dataset Include] dossier zoals die in het [Uitgeven van Bestaande Dataset wordt beschreven omvat Dossiers](../../../../../home/c-dataset-const-proc/c-dataset-inc-files/c-work-dataset-inc-files/t-edit-ex-dataset-inc-files.md#task-456c04e38ebc425fb35677a6bb6aa077) en voegt een decodergroep van het tekstdossier toe. Zie de groepen van de [Decoder van de lijstingang](../../../../../home/c-dataset-const-proc/c-dataset-inc-files/c-types-dataset-inc-files/c-log-proc-dataset-inc-files/c-log-proc-dataset-inc-files.md#concept-999475a22519432e98844622ca95b6ab).

1. Klik **[!UICONTROL Decoders]** onder de pas gecreëerde decodergroep met de rechtermuisknop aan, dan klik **[!UICONTROL Add new]** > **[!UICONTROL Delimited]**.

1. Geef de volgende informatie op:

   * **Velden:** Lijst van de gebieden in het logboekdossier. Als om het even welke hier bepaalde gebieden tot de transformatiefase van datasetconstructie moeten worden overgegaan, moeten die gebieden in de parameter van Gebieden van één van de [!DNL Log Processing Dataset Include] dossiers voor de dataset worden vermeld. De gebiedsnamen van de douane moeten met &quot;x-&quot;beginnen.

   * **Afbakening:** Karakter dat wordt gebruikt om gebieden in het outputdossier te scheiden.

1. Herhaal stappen 4 en 5 voor een andere decoders die u aan de groep wilt toevoegen.
1. Om het [!DNL Log Processing Dataset Include] dossier op te slaan, klik **[!UICONTROL (modified)]** bij de bovenkant van het venster met de rechtermuisknop aan en klik **[!UICONTROL Save]**.

1. Om de plaatselijk aangebrachte veranderingen van kracht te maken, in [!DNL Profile Manager], klik het vinkje voor het dossier in de [!DNL User] kolom met de rechtermuisknop aan, dan klik **[!UICONTROL Save to]** > *&lt;**[!UICONTROL profile name]**>*, waar de profielnaam de naam van het datasetprofiel of het geërfte profiel is waartot de dataset omvat dossier behoort.

>[!NOTE]
>
>Sla het gewijzigde configuratiebestand niet op in een van de interne profielen die door Adobe worden geleverd, omdat uw wijzigingen worden overschreven wanneer u updates voor deze profielen installeert.

Dit voorbeeld illustreert het gebruik van een afgebakende decoder om gebieden van gegevens uit een komma-afgebakend tekstdossier te halen dat gegevens over films bevat.

![](assets/cfg_LogProcessingInclude_DelimitedDecoder.png)

