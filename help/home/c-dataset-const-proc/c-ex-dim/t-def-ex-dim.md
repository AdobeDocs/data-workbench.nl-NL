---
description: Stappen om uitgebreide afmetingen te bepalen.
solution: Analytics
title: Uitgebreide afmetingen definiëren
topic: Data workbench
uuid: 25946998-54ca-4595-a2f9-9c593917643a
translation-type: tm+mt
source-git-commit: 27600561841db3705f4eee6ff0aeb8890444bbc9

---


# Uitgebreide afmetingen definiëren{#defining-extended-dimensions}

Stappen om uitgebreide afmetingen te bepalen.

1. Terwijl het werken in uw datasetprofiel, open [!DNL Profile Manager] en klik **[!UICONTROL Dataset]** om zijn inhoud te tonen.
1. Open het [!DNL Transformation.cfg] dossier of het [!DNL Transformation Dataset Include] dossier waarin u de uitgebreide afmeting wilt bepalen.

   * (Geadviseerd) om een dataset te openen omvat dossier, zie de [Dataset Dossiers](../../../home/c-dataset-const-proc/c-dataset-inc-files/c-abt-dataset-inc-files.md)omvat.

      >[!NOTE]
      >
      >Adobe adviseert bepalend uitgebreide afmetingen in één of meerdere nieuwe [!DNL Transformation Dataset Include] dossiers. Voor meer informatie, zie het [Creëren van Nieuwe Dataset Dossiers](../../../home/c-dataset-const-proc/c-dataset-inc-files/c-work-dataset-inc-files/t-create-new-dataset-inc-files.md#task-b29f30605c374a6ca747ac843337b06e)omvatten.

   * Om het [!DNL Transformation.cfg] dossier te openen, zie het [Uitgeven van het Dossier](../../../home/c-dataset-const-proc/c-trans-config-file/t-edit-trans-config-file.md#task-cfef4142c1bf4437a669d1fdc75cabbc)van de Configuratie van de Transformatie.

1. Klik met de rechtermuisknop **[!UICONTROL Transformations]** en klik **[!UICONTROL Add new]** > *&lt;**[!UICONTROL Extended dimension type]**>*.
1. Voer de juiste informatie in voor uw uitgebreide dimensie. Voor beschrijvingen van de transformatietypen en informatie over hun parameters, zie de volgende secties:

   * [Afmetingen telbaar](../../../home/c-dataset-const-proc/c-ex-dim/c-types-ex-dim/c-count-dim.md#concept-f28b633419494e7bbc510012dbfcc6f8)
   * [Eenvoudige afmetingen](../../../home/c-dataset-const-proc/c-ex-dim/c-types-ex-dim/c-simple-dim.md#concept-c1d804dac4094489afe61560d2908181)
   * [Vele-aan-Vele Afmetingen](../../../home/c-dataset-const-proc/c-ex-dim/c-types-ex-dim/c-many-dim.md#concept-5ed3cca8b2194d4f96134f6238040998)
   * [Numerieke afmetingen](../../../home/c-dataset-const-proc/c-ex-dim/c-types-ex-dim/c-num-dim.md#concept-8513b9afaff447c8b334410b565b91ed)
   * [Denormale Afmetingen](../../../home/c-dataset-const-proc/c-ex-dim/c-types-ex-dim/c-denormal-dim.md#concept-54a2600b8ee748b7acff405daccf3489)
   * [Afmetingen tijd](../../../home/c-dataset-const-proc/c-ex-dim/c-types-ex-dim/c-time-dim.md#concept-1e4eeb8d33964bb2a8d5768d6439df67)

      Voor om het even welke uitgebreide afmeting die u bepaalt, kunt u één of meerdere commentaarlijnen aan de parameter van Commentaren toevoegen om de afmeting verder te beschrijven of nota&#39;s over zijn gebruik toe te voegen. Om een commentaar toe te voegen, klik het **[!UICONTROL Comments]** etiket met de rechtermuisknop aan en klik **[!UICONTROL Add new]** > **[!UICONTROL Comment Line]**.

1. Nadat u uw uitgebreide dimensie(en) in het configuratiebestand hebt gedefinieerd, slaat u het bestand lokaal op en slaat u het op in uw datasetprofiel op de gegevenswerkbankserver.
