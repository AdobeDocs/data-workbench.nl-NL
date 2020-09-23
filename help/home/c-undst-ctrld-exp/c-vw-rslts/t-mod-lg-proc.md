---
description: U moet het x-experimentveld toevoegen aan het bestand Log Processing.cfg, dat wordt gebruikt om een uitgebreide dimensie te maken.
solution: Analytics,Analytics
title: Logverwerking wijzigen.cfg
topic: Data workbench
uuid: 9105b09b-e3d5-4922-a205-b459553a4bec
translation-type: tm+mt
source-git-commit: 34cdcfc83ae6bb620706db37228e200cff43ab2c
workflow-type: tm+mt
source-wordcount: '186'
ht-degree: 0%

---


# Logverwerking wijzigen.cfg{#modifying-log-processing-cfg}

U moet het x-experimentveld toevoegen aan het bestand Log Processing.cfg, dat wordt gebruikt om een uitgebreide dimensie te maken.

Zie Transformation.cfg [wijzigen](../../../home/c-undst-ctrld-exp/c-vw-rslts/t-mod-trfmtn.md#task-d61b02853a82492c9a76e3c5fe8a3fb6).

**Logverwerking wijzigen.cfg**

1. Open de werkruimte in [!DNL Insight]de werkruimte door met de rechtermuisknop te klikken in een werkruimte en te klikken [!DNL Profile Manager] > **[!UICONTROL Admin]** , of door de werkruimte Profielbeheer te openen op het **[!UICONTROL Profile Manager]**[!DNL Admin] tabblad.
1. Klik in de [!DNL Profile Manager]werkbalk **[!UICONTROL Dataset]** om de inhoud weer te geven.
1. Klik met de rechtermuisknop op het vinkje naast [!DNL Log Processing.cfg] en klik op **[!UICONTROL Make Local]**. In de [!DNL User] kolom wordt een vinkje voor dit bestand weergegeven.
1. Klik met de rechtermuisknop op het nieuwe vinkje en klik op **[!UICONTROL Open]** > **[!UICONTROL in Insight]**. Het [!DNL Log Processing.cfg] venster verschijnt.
1. Klik **[!UICONTROL Fields]** om de inhoud weer te geven.
1. Klik met de rechtermuisknop op het laatste veld in de huidige lijst en klik op **[!UICONTROL Add new]** > **[!UICONTROL Field]**.
1. Typ x-experiment in het nieuwe veld, zoals in het volgende voorbeeld wordt getoond:

   ![Stapinfo](assets/logprocessing.png)

1. Klik met de rechtermuisknop **[!UICONTROL (modified)]** boven in het venster en klik op **[!UICONTROL Save]**.
1. Klik in de [!DNL Profile Manager]sectie met de rechtermuisknop op het vinkje voor [!DNL Log Processing.cfg] in de [!DNL User] kolom en klik vervolgens op **[!UICONTROL Save to]** > *&lt;**[!UICONTROL profile name]**>* om de lokaal aangebrachte wijzigingen in het werkprofiel op te slaan.

   >[!NOTE]
   >
   >De dataset begint onmiddellijk opwerkingsproces.

   Voor meer informatie over de Verwerking van het Logboek en de Gebieden zie de Gids *van de Configuratie van de* Dataset.

