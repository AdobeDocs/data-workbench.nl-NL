---
description: Instructies voor het verwijderen van Insight Server, Transform of Repeater.
solution: Analytics
title: De software verwijderen
uuid: 79cf0db6-0f99-40fa-a7b0-38dd8d7246bd
translation-type: tm+mt
source-git-commit: 34cdcfc83ae6bb620706db37228e200cff43ab2c
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 0%

---


# De software verwijderen{#uninstalling-your-software}

Instructies voor het verwijderen van Insight Server, Transform of Repeater.

## Adobe van Insight Server verwijderen {#section-7d7befe672854df79bb6c28ec02f6670}

1. Registreer de [!DNL Insight Server] Windows-service niet.

   1. Open een opdrachtprompt en navigeer naar de submap bin in de map waarin u hebt geïnstalleerd [!DNL Insight Server].

      Voorbeeld: [!DNL C:\Adobe\Server\bin]

   1. Bij de bevelherinnering, voer het volgende bevel uit om het als dienst onder Microsoft Windows tegen te houden en te verwijderen:

      ```
      InsightServer64.exe /unregserver
      ```

1. Verwijder de [!DNL Insight Server] installatiemap.

## Transformatie verwijderen {#section-5e6a604dadb5477ba4dc9f93c9be0897}

1. Voer de volgende stappen uit om het [!DNL profile.cfg] bestand bij te werken voor elk profiel waarmee u werkt [!DNL Transform].

   1. Open de [!DNL Profile Manager].
   1. Klik met de rechtermuisknop op het vinkje naast [!DNL profile.cfg] en klik op **[!UICONTROL Make Local]**. In de [!DNL User] kolom wordt een vinkje voor dit bestand weergegeven.

   1. Klik met de rechtermuisknop op het nieuwe vinkje en klik op **[!UICONTROL Open]** > **[!UICONTROL in Insight]**. Het [!DNL profile.cfg] venster verschijnt.

   1. Verwijder in het [!DNL profile.cfg] venster het [!DNL Transform] profielitem uit de vector Directories.

   1. Klik met de rechtermuisknop **[!UICONTROL (modified)]** boven in het venster en klik op **[!UICONTROL Save]**.

   1. Klik in het [!DNL Profile Manager]vak met de rechtermuisknop op het vinkje voor [!DNL profile.cfg] in de [!DNL User] kolom en klik vervolgens op **[!UICONTROL Save to]** > *&lt;**[!UICONTROL profile name]**>*.

1. Verwijder de [!DNL Transform] map uit de [!DNL Profiles] map in de [!DNL Insight Server] installatiemap.

## Repeater verwijderen {#section-2f94141d956749d88f549dbea26e5272}

1. Registreer de [!DNL Repeater] Windows-service niet.

   1. Open een opdrachtprompt en navigeer naar de submap bin in de map waarin u hebt geïnstalleerd [!DNL Repeater].

      Voorbeeld: [!DNL D:\Adobe\Repeater\bin]

   1. Bij de bevelherinnering, voer het volgende bevel uit om het als dienst onder Microsoft Windows tegen te houden en te verwijderen:

      ```
      InsightServer64.exe /unregserver
      ```

1. Verwijder de [!DNL Repeater] installatiemap.

