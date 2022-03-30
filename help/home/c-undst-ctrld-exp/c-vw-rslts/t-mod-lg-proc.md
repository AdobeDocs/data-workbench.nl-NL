---
description: U moet het x-experimentveld toevoegen aan het bestand Log Processing.cfg, dat wordt gebruikt om een uitgebreide dimensie te maken.
solution: Analytics
title: Logverwerking wijzigen.cfg
uuid: 9105b09b-e3d5-4922-a205-b459553a4bec
exl-id: 23c7873f-8ffd-422f-896b-d6c7e16aabbd
source-git-commit: 31f775478b0f0d968310ed10a43ad46791319ee9
workflow-type: tm+mt
source-wordcount: '186'
ht-degree: 0%

---

# Logverwerking wijzigen.cfg{#modifying-log-processing-cfg}

U moet het x-experimentveld toevoegen aan het bestand Log Processing.cfg, dat wordt gebruikt om een uitgebreide dimensie te maken.

Zie [Transformatie wijzigen.cfg](../../../home/c-undst-ctrld-exp/c-vw-rslts/t-mod-trfmtn.md#task-d61b02853a82492c9a76e3c5fe8a3fb6).

**Logverwerking wijzigen.cfg**

1. In [!DNL Insight], opent u de [!DNL Profile Manager] door met de rechtermuisknop in een werkruimte te klikken en te klikken **[!UICONTROL Admin]** > **[!UICONTROL Profile Manager]** of door de werkruimte Profielbeheer te openen in het dialoogvenster [!DNL Admin] tab.
1. In de [!DNL Profile Manager], klikt u op **[!UICONTROL Dataset]** om de inhoud te tonen.
1. Klik met de rechtermuisknop op het vinkje naast [!DNL Log Processing.cfg] en klik op **[!UICONTROL Make Local]**. Er wordt een vinkje voor dit bestand weergegeven in het dialoogvenster [!DNL User] kolom.
1. Klik met de rechtermuisknop op het nieuwe vinkje en klik op **[!UICONTROL Open]** > **[!UICONTROL in Insight]**. De [!DNL Log Processing.cfg] wordt weergegeven.
1. Klikken **[!UICONTROL Fields]** om de inhoud te tonen.
1. Klik met de rechtermuisknop op het laatste veld in de huidige lijst en klik op **[!UICONTROL Add new]** > **[!UICONTROL Field]**.
1. Typ x-experiment in het nieuwe veld, zoals in het volgende voorbeeld wordt getoond:

   ![Stapinfo](assets/logprocessing.png)

1. Klikken met rechtermuisknop **[!UICONTROL (modified)]** boven aan het venster en klik op **[!UICONTROL Save]**.
1. In de [!DNL Profile Manager], klikt u met de rechtermuisknop op het vinkje voor [!DNL Log Processing.cfg] in de [!DNL User] kolom, klik vervolgens op **[!UICONTROL Save to]** > *&lt;**[!UICONTROL profile name]**>* om de lokaal aangebrachte wijzigingen in het werkprofiel op te slaan.

   >[!NOTE]
   >
   >De dataset begint onmiddellijk opwerkingsproces.

   Voor meer informatie over de verwerking van het Logboek en de Gebieden zie *Configuratie-handleiding voor gegevensset*.
