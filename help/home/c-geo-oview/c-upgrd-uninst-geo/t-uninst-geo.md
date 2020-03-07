---
description: Stappen om gegevenswerkbankGeography te desinstalleren.
solution: Analytics
title: Geografie van gegevenswerkbank verwijderen
topic: Data workbench
uuid: 038b2dfb-4db2-42c6-85c3-bc5d776e7736
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Geografie van gegevenswerkbank verwijderen{#uninstalling-data-workbench-geography}

Stappen om gegevenswerkbankGeography te desinstalleren.

>[!NOTE]
>
>Als het profiel waarmee u een gegevenswerkbank gebruikt op een servercluster van de gegevenswerkbank [!DNL Geography] wordt uitgevoerd, desinstalleert u het [!DNL Geography] profiel van de server van de hoofdgegevenswerkbank in het cluster.

1. Gebruik de volgende stappen om het [!DNL profile.cfg] dossier voor elk profiel bij te werken waarmee u gegevenswerkbank gebruikte [!DNL Geography].

   1. Open de [!DNL Profile Manager].
   1. Klik het vinkje naast met de rechtermuisknop aan [!DNL profile.cfg] en klik **[!UICONTROL Make Local]**. Een vinkje voor dit dossier verschijnt in de [!DNL User] kolom.

   1. Klik het pas gecreëerde vinkje met de rechtermuisknop aan en klik **[!UICONTROL Open]** > **[!UICONTROL from the workbench]**. Het [!DNL profile.cfg] venster wordt weergegeven.

   1. In het [!DNL profile.cfg] venster, schrap de [!DNL Geography] profielingang van de [!DNL Directories] vector.

   1. Als u een datadienst hebt gebruikt, schrap de [!DNL IP Geo-intelligence] of [!DNL IP Geo-location] profielingang van de [!DNL Directories] vector.

   1. Klik **[!UICONTROL (modified)]** bij de bovenkant van het venster met de rechtermuisknop aan en klik **[!UICONTROL Save]**.

   1. Klik in de [!DNL Profile Manager], rechtsklik op het vinkje voor [!DNL profile.cfg] in de [!DNL User] kolom en klik vervolgens op **[!UICONTROL Save to]** > *&lt;**[!UICONTROL profile name]**>*.

1. Schrap de omslag van de Geografie van de omslag van Profielen in uw folder van de de serverinstallatie van de gegevenswerkbank.
1. Als u de datadienst hebt gebruikt, schrap IP Geo-intelligence of IP Geo-location omslag van de omslag van Profielen in uw folder van de de serverinstallatie van de gegevenswerkbank.
1. Schrap de omslag van de Geografie van de omslag van Raadplegingen in uw folder van de de serverinstallatie van de gegevenswerkbank.
1. Als u de datadienst hebt gebruikt, schrap IP Geo-intelligentie of IP Geo-Locatieomslag van de omslag van Raadplegingen in uw folder van de de serverinstallatie van de gegevenswerkbank.
1. Als u nieuwe terreinbeelden creeerde, schrap het [!DNL Terrain Images.cfg] dossier van de omslag van Componenten in uw de installatiefolder van de gegevenswerkbank server.
