---
description: Stappen om uitgebreide afmetingen te definiëren.
title: Uitgebreide Dimension definiëren
uuid: 25946998-54ca-4595-a2f9-9c593917643a
exl-id: e1664548-e2b4-47bb-8bec-155c16873e08
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '191'
ht-degree: 0%

---

# Uitgebreide Dimension definiëren{#defining-extended-dimensions}

{{eol}}

Stappen om uitgebreide afmetingen te definiëren.

1. Tijdens het werken in uw datasetprofiel, open [!DNL Profile Manager] en klik op **[!UICONTROL Dataset]** om de inhoud te tonen.
1. Open de [!DNL Transformation.cfg] of de [!DNL Transformation Dataset Include] bestand waarin u de uitgebreide dimensie wilt definiëren.

   * (Aanbevolen) Als u een dataset wilt openen, raadpleegt u [Gegevensset met bestanden](../../../home/c-dataset-const-proc/c-dataset-inc-files/c-abt-dataset-inc-files.md).

      >[!NOTE]
      >
      >Adobe raadt aan uitgebreide afmetingen in een of meer nieuwe dimensies te definiëren [!DNL Transformation Dataset Include] bestanden. Zie voor meer informatie [Nieuwe gegevensset maken met include-bestanden](../../../home/c-dataset-const-proc/c-dataset-inc-files/c-work-dataset-inc-files/t-create-new-dataset-inc-files.md#task-b29f30605c374a6ca747ac843337b06e).

   * Als u het dialoogvenster [!DNL Transformation.cfg] bestand, zie [Het configuratiebestand voor transformatie bewerken](../../../home/c-dataset-const-proc/c-trans-config-file/t-edit-trans-config-file.md#task-cfef4142c1bf4437a669d1fdc75cabbc).

1. Klikken met rechtermuisknop **[!UICONTROL Transformations]** en klik op **[!UICONTROL Add new]** > *&lt;**[!UICONTROL Extended dimension type]**>*.
1. Voer de juiste gegevens in voor de uitgebreide dimensie. Zie de volgende secties voor beschrijvingen van de transformatietypen en informatie over de parameters ervan:

   * [Vertelbare Dimension](../../../home/c-dataset-const-proc/c-ex-dim/c-types-ex-dim/c-count-dim.md#concept-f28b633419494e7bbc510012dbfcc6f8)
   * [Eenvoudige Dimension](../../../home/c-dataset-const-proc/c-ex-dim/c-types-ex-dim/c-simple-dim.md#concept-c1d804dac4094489afe61560d2908181)
   * [Veel-tot-veel Dimension](../../../home/c-dataset-const-proc/c-ex-dim/c-types-ex-dim/c-many-dim.md#concept-5ed3cca8b2194d4f96134f6238040998)
   * [Numerieke Dimension](../../../home/c-dataset-const-proc/c-ex-dim/c-types-ex-dim/c-num-dim.md#concept-8513b9afaff447c8b334410b565b91ed)
   * [Denormale Dimension](../../../home/c-dataset-const-proc/c-ex-dim/c-types-ex-dim/c-denormal-dim.md#concept-54a2600b8ee748b7acff405daccf3489)
   * [Dimension tijd](../../../home/c-dataset-const-proc/c-ex-dim/c-types-ex-dim/c-time-dim.md#concept-1e4eeb8d33964bb2a8d5768d6439df67)

      Voor om het even welke uitgebreide afmeting die u bepaalt, kunt u één of meerdere commentaarlijnen aan de parameter van Commentaren toevoegen om de afmeting verder te beschrijven of nota&#39;s over zijn gebruik toe te voegen. Als u een opmerking wilt toevoegen, klikt u met de rechtermuisknop op de knop **[!UICONTROL Comments]** label en klik **[!UICONTROL Add new]** > **[!UICONTROL Comment Line]**.

1. Nadat u de uitgebreide dimensie(s) in het configuratiebestand hebt gedefinieerd, slaat u het bestand lokaal op en slaat u het op in het gegevenssetprofiel op de gegevenswerkbankserver.
