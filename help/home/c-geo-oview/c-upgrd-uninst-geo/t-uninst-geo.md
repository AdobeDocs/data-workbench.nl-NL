---
description: Stappen om data workbenchGeography te verwijderen.
title: Data Workbench Geography verwijderen
uuid: 038b2dfb-4db2-42c6-85c3-bc5d776e7736
exl-id: e3898423-3b28-4786-834a-1d1ff9deb7c6
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '248'
ht-degree: 0%

---

# Data Workbench Geography{#uninstalling-data-workbench-geography} verwijderen

Stappen om data workbenchGeography te verwijderen.

>[!NOTE]
>
>Als het profiel waarmee u gegevenswerkbank [!DNL Geography] gebruikt, wordt uitgevoerd op een gegevenswerkbankservercluster, verwijdert u het [!DNL Geography]-profiel van de master gegevenswerkbankserver in de cluster.

1. Gebruik de volgende stappen om het [!DNL profile.cfg] dossier voor elk profiel bij te werken waarmee u gegevenswerkbank [!DNL Geography] gebruikte.

   1. Open [!DNL Profile Manager].
   1. Klik met de rechtermuisknop op het vinkje naast [!DNL profile.cfg] en klik **[!UICONTROL Make Local]**. Er wordt een vinkje voor dit bestand weergegeven in de kolom [!DNL User].

   1. Klik met de rechtermuisknop op het nieuwe vinkje en klik op **[!UICONTROL Open]** > **[!UICONTROL from the workbench]**. Het venster [!DNL profile.cfg] verschijnt.

   1. Verwijder in het [!DNL profile.cfg]-venster het [!DNL Geography]-profielitem uit de [!DNL Directories]-vector.

   1. Als u een gegevensservice hebt gebruikt, verwijdert u de [!DNL IP Geo-intelligence]- of [!DNL IP Geo-location]-profielvermelding uit de [!DNL Directories]-vector.

   1. Klik met de rechtermuisknop **[!UICONTROL (modified)]** boven in het venster en klik **[!UICONTROL Save]**.

   1. Klik in [!DNL Profile Manager] met de rechtermuisknop op het vinkje voor [!DNL profile.cfg] in de kolom [!DNL User] en klik vervolgens op **[!UICONTROL Save to]** > *&lt;**[!UICONTROL profile name]**>*.

1. Verwijder de map Geografie uit de map Profielen in de installatiemap van de gegevenswerkbank.
1. Als u een datadienst hebt gebruikt, schrap IP Geo-intelligentie of IP Geo-location omslag van de omslag van Profielen in uw de installatiemap van de gegevenswerkbankserver.
1. Verwijder de map Geography uit de map Lookups in de installatiemap van de gegevenswerkbank.
1. Als u een datadienst hebt gebruikt, schrap IP Geo-intelligentie of IP Geo-location omslag van de omslag van Lookups in uw folder van de de serverinstallatie van de gegevenswerkbank.
1. Als u nieuwe terreinbeelden creeerde, schrap het [!DNL Terrain Images.cfg] dossier van de omslag van Componenten in uw folder van de de serverinstallatie van de gegevenswerkbank.
