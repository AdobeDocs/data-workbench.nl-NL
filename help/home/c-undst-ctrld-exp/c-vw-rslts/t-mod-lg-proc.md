---
description: U moet het x-experimentveld toevoegen aan het bestand Log Processing.cfg, dat wordt gebruikt om een uitgebreide dimensie te maken.
solution: Analytics,Analytics
title: Logverwerking wijzigen.cfg
uuid: 9105b09b-e3d5-4922-a205-b459553a4bec
exl-id: 23c7873f-8ffd-422f-896b-d6c7e16aabbd
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '186'
ht-degree: 0%

---

# Logverwerking wijzigen.cfg{#modifying-log-processing-cfg}

U moet het x-experimentveld toevoegen aan het bestand Log Processing.cfg, dat wordt gebruikt om een uitgebreide dimensie te maken.

Zie [Transformation.cfg](../../../home/c-undst-ctrld-exp/c-vw-rslts/t-mod-trfmtn.md#task-d61b02853a82492c9a76e3c5fe8a3fb6) wijzigen.

**Logverwerking wijzigen.cfg**

1. Open [!DNL Insight] door met de rechtermuisknop in een werkruimte te klikken en **[!UICONTROL Admin]** > **[!UICONTROL Profile Manager]** te klikken of door de werkruimte Profielbeheer te openen op het tabblad [!DNL Admin].[!DNL Profile Manager]
1. Klik in [!DNL Profile Manager] op **[!UICONTROL Dataset]** om de inhoud ervan weer te geven.
1. Klik met de rechtermuisknop op het vinkje naast [!DNL Log Processing.cfg] en klik **[!UICONTROL Make Local]**. Er wordt een vinkje voor dit bestand weergegeven in de kolom [!DNL User].
1. Klik met de rechtermuisknop op het nieuwe vinkje en klik op **[!UICONTROL Open]** > **[!UICONTROL in Insight]**. Het venster [!DNL Log Processing.cfg] verschijnt.
1. Klik **[!UICONTROL Fields]** om de inhoud ervan weer te geven.
1. Klik met de rechtermuisknop op het laatste veld in de huidige lijst en klik op **[!UICONTROL Add new]** > **[!UICONTROL Field]**.
1. Typ x-experiment in het nieuwe veld, zoals in het volgende voorbeeld wordt getoond:

   ![Stapinfo](assets/logprocessing.png)

1. Klik met de rechtermuisknop **[!UICONTROL (modified)]** boven in het venster en klik **[!UICONTROL Save]**.
1. Klik in [!DNL Profile Manager] met de rechtermuisknop op het vinkje voor [!DNL Log Processing.cfg] in de kolom [!DNL User] en klik vervolgens op **[!UICONTROL Save to]** > *&lt;**[!UICONTROL profile name]**>* om de lokaal aangebrachte wijzigingen in het werkprofiel op te slaan.

   >[!NOTE]
   >
   >De dataset begint onmiddellijk opwerkingsproces.

   Voor meer informatie over de Verwerking van het Logboek en Gebieden zie *Gids van de Configuratie van de Dataset*.
