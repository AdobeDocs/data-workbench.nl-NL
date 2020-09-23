---
description: Nu het x-experimentveld beschikbaar is, moet u een uitgebreide dimensie maken om het x-experimentveld in uw gegevensset op te nemen, zodat u de resultaten in Inzicht kunt bekijken.
solution: Analytics,Analytics
title: Transformatie wijzigen.cfg
topic: Data workbench
uuid: c17e48db-8fd9-4640-b621-6963bb8223d7
translation-type: tm+mt
source-git-commit: 34cdcfc83ae6bb620706db37228e200cff43ab2c
workflow-type: tm+mt
source-wordcount: '357'
ht-degree: 0%

---


# Transformatie wijzigen.cfg{#modifying-transformation-cfg}

Nu het x-experimentveld beschikbaar is, moet u een uitgebreide dimensie maken om het x-experimentveld in uw gegevensset op te nemen, zodat u de resultaten in Inzicht kunt bekijken.

Hiervoor moet u een nieuwe dimensie aan het [!DNL Transformation.cfg] bestand toevoegen.

Als u meerdere experimenten wilt uitvoeren, moet u ook een nieuwe gesplitste transformatie aan het [!DNL Transformation.cfg] bestand toevoegen. Deze gesplitste transformatie scheidt de verschillende experiment- en groepsnamen zodat de informatie gemakkelijker te interpreteren is. Als u wilt voorkomen dat gegevens opnieuw worden verwerkt als u later aanvullende experimenten moet toevoegen, raadt Adobe u aan de transformatie Splitsen toe te voegen, zelfs als u momenteel niet van plan bent meerdere experimenten uit te voeren.

De volgende procedure omvat het creëren van zowel de nieuwe gesplitste transformatie als de uitgebreide dimensie. Als u de gesplitste transformatie niet wilt toevoegen, slaat u gewoon stap 5-7 over.

**Transformation.cfg wijzigen**

1. Open de werkruimte in [!DNL Insight]de werkruimte door met de rechtermuisknop te klikken in een werkruimte en te klikken [!DNL Profile Manager] > **[!UICONTROL Admin]** , of door de werkruimte Profielbeheer te openen op het **[!UICONTROL Profile Manager]**[!DNL Admin] tabblad.
1. Klik in de [!DNL Profile Manager]werkbalk **[!UICONTROL Dataset]** om de inhoud weer te geven.
1. Klik met de rechtermuisknop op het vinkje naast [!DNL Transformation.cfg] en klik op **[!UICONTROL Make Local]**. In de [!DNL User] kolom wordt een vinkje voor dit bestand weergegeven.
1. Klik met de rechtermuisknop op het nieuwe vinkje en klik op **[!UICONTROL Open]** > **[!UICONTROL in Insight]**. Het [!DNL Transformation.cfg] venster verschijnt.
1. Klik **[!UICONTROL Transformation]** om de inhoud weer te geven.
1. Klik met de rechtermuisknop **[!UICONTROL Transformations]** en klik op **[!UICONTROL Add new]** > **[!UICONTROL Split]**.
1. Voltooi de nieuwe splitsing bij kommatransformatie, zoals in het volgende voorbeeld wordt getoond:

   ![Stapinfo](assets/New_split_transformation.png)

   >[!NOTE]
   >
   >U kunt elke gewenste waarde invoeren in het veld Naam.

1. Klik met de rechtermuisknop **[!UICONTROL Extended Dimensions]** en klik op **[!UICONTROL Add new]** > **[!UICONTROL ManyToMany]**.
1. Vul de nieuwe dimensie in zoals in het volgende voorbeeld:

   ![Stapinfo](assets/New_Dimension_controlled_experiment_groups.png)

   >[!NOTE]
   >
   >* U kunt elke gewenste waarde invoeren in het veld Naam.
   >* Als u de gesplitste transformatie niet hebt opgenomen, moet u &quot;x-experiment&quot; in het [!DNL Input] veld typen.


1. Klik met de rechtermuisknop **[!UICONTROL (modified)]** boven in het venster en klik op **[!UICONTROL Save]**.
1. Klik in het [!DNL Profile Manager]dialoogvenster met de rechtermuisknop op het vinkje voor [!DNL Transformation.cfg] in de [!DNL User] kolom en klik vervolgens op **[!UICONTROL Save to]** > **[!UICONTROL profile name]** om de lokaal aangebrachte wijzigingen in het werkprofiel op te slaan.

   >[!NOTE]
   >
   >De dataset begint onmiddellijk opnieuw te transformeren.

   Voor meer informatie over [!DNL Transformation.cfg] en uitgebreide afmetingen, zie de Gids *van de Configuratie van de* Dataset.
