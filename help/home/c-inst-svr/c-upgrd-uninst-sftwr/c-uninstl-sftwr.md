---
description: Instructies om de Server, de Transformatie, of de Repeater van het Inzicht te desinstalleren.
solution: Insight
title: Uw software verwijderen
uuid: 79cf0db6-0f99-40fa-a7b0-38dd8d7246bd
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Uw software verwijderen{#uninstalling-your-software}

Instructies om de Server, de Transformatie, of de Repeater van het Inzicht te desinstalleren.

## Uninstall Insight Server Adobe {#section-7d7befe672854df79bb6c28ec02f6670}

1. Registreer de [!DNL Insight Server] Windows-service niet.

   1. Open een bevelherinnering en navigeer aan de baksubfolder in de omslag waar u installeerde [!DNL Insight Server].

      Voorbeeld: [!DNL C:\Adobe\Server\bin]

   1. Bij de bevelherinnering, voer het volgende bevel uit om het als dienst onder Microsoft Windows tegen te houden en unregister:

      ```
      InsightServer64.exe /unregserver
      ```

1. Schrap de [!DNL Insight Server] installatiefolder.

## Transformeren verwijderen {#section-5e6a604dadb5477ba4dc9f93c9be0897}

1. Gebruik de volgende stappen om het [!DNL profile.cfg] dossier voor elk profiel bij te werken waarmee u gebruikte [!DNL Transform].

   1. Open de [!DNL Profile Manager].
   1. Klik het vinkje naast met de rechtermuisknop aan [!DNL profile.cfg] en klik **[!UICONTROL Make Local]**. Een vinkje voor dit dossier verschijnt in de [!DNL User] kolom.

   1. Klik het pas gecreëerde vinkje met de rechtermuisknop aan en klik **[!UICONTROL Open]** > **[!UICONTROL in Insight]**. Het [!DNL profile.cfg] venster wordt weergegeven.

   1. In het [!DNL profile.cfg] venster, schrap de [!DNL Transform] profielingang van de vector van Folders.

   1. Klik **[!UICONTROL (modified)]** bij de bovenkant van het venster met de rechtermuisknop aan en klik **[!UICONTROL Save]**.

   1. Klik in de [!DNL Profile Manager], rechtsklik op het vinkje voor [!DNL profile.cfg] in de [!DNL User] kolom en klik vervolgens op **[!UICONTROL Save to]** > *&lt;**[!UICONTROL profile name]**>*.

1. Schrap de [!DNL Transform] omslag van de [!DNL Profiles] omslag in uw [!DNL Insight Server] installatiefolder.

## Repeater verwijderen {#section-2f94141d956749d88f549dbea26e5272}

1. Registreer de [!DNL Repeater] Windows-service niet.

   1. Open een bevelherinnering en navigeer aan de baksubfolder in de omslag waar u installeerde [!DNL Repeater].

      Voorbeeld: [!DNL D:\Adobe\Repeater\bin]

   1. Bij de bevelherinnering, voer het volgende bevel uit om het als dienst onder Microsoft Windows tegen te houden en unregister:

      ```
      InsightServer64.exe /unregserver
      ```

1. Schrap de [!DNL Repeater] installatiefolder.

