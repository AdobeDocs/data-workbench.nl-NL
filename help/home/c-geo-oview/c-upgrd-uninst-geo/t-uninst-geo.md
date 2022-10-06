---
description: Stappen om data workbenchGeography te verwijderen.
title: Data Workbench Geography verwijderen
uuid: 038b2dfb-4db2-42c6-85c3-bc5d776e7736
exl-id: e3898423-3b28-4786-834a-1d1ff9deb7c6
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '248'
ht-degree: 0%

---

# Data Workbench Geography verwijderen{#uninstalling-data-workbench-geography}

{{eol}}

Stappen om data workbenchGeography te verwijderen.

>[!NOTE]
>
>Als het profiel waarmee u gegevens gebruikt, werkbank [!DNL Geography] wordt uitgevoerd op een servercluster van een gegevenswerkbank, verwijdert u de [!DNL Geography] van de master server van de gegevenswerkbank in de cluster.

1. Gebruik de volgende stappen om de [!DNL profile.cfg] bestand voor elk profiel waarmee u een werkbank voor gegevens gebruikt [!DNL Geography].

   1. Open de [!DNL Profile Manager].
   1. Klik met de rechtermuisknop op het vinkje naast [!DNL profile.cfg] en klik op **[!UICONTROL Make Local]**. Er wordt een vinkje voor dit bestand weergegeven in het dialoogvenster [!DNL User] kolom.

   1. Klik met de rechtermuisknop op het nieuwe vinkje en klik op **[!UICONTROL Open]** > **[!UICONTROL from the workbench]**. De [!DNL profile.cfg] wordt weergegeven.

   1. In de [!DNL profile.cfg] venster, de [!DNL Geography] profielitem van de [!DNL Directories] vector.

   1. Als u een gegevensservice hebt gebruikt, verwijdert u de [!DNL IP Geo-intelligence] of [!DNL IP Geo-location] profielitem van de [!DNL Directories] vector.

   1. Klikken met rechtermuisknop **[!UICONTROL (modified)]** boven aan het venster en klik op **[!UICONTROL Save]**.

   1. In de [!DNL Profile Manager], klikt u met de rechtermuisknop op het vinkje voor [!DNL profile.cfg] in de [!DNL User] kolom, klik vervolgens op **[!UICONTROL Save to]** > *&lt;**[!UICONTROL profile name]**>*.

1. Verwijder de map Geografie uit de map Profielen in de installatiemap van de gegevenswerkbank.
1. Als u een datadienst hebt gebruikt, schrap IP Geo-intelligentie of IP Geo-location omslag van de omslag van Profielen in uw de installatiemap van de gegevenswerkbankserver.
1. Verwijder de map Geography uit de map Lookups in de installatiemap van de gegevenswerkbank.
1. Als u een datadienst hebt gebruikt, schrap IP Geo-intelligentie of IP Geo-location omslag van de omslag van Lookups in uw folder van de de serverinstallatie van de gegevenswerkbank.
1. Als u nieuwe terreinbeelden creeerde, schrap [!DNL Terrain Images.cfg] in de map Components in de installatiemap van de gegevenswerkbank.
