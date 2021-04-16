---
description: Instructies voor het verwijderen van Insight Server, Transform of Repeater.
title: De software verwijderen
uuid: 79cf0db6-0f99-40fa-a7b0-38dd8d7246bd
exl-id: 3ba5e5e3-c1a2-4ecb-9f88-a3fe923837e7
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 0%

---

# De software verwijderen{#uninstalling-your-software}

Instructies voor het verwijderen van Insight Server, Transform of Repeater.

## Adobe van Insight Server verwijderen{#section-7d7befe672854df79bb6c28ec02f6670}

1. Deregistreer de [!DNL Insight Server] dienst van Vensters.

   1. Open een opdrachtprompt en navigeer naar de submap bin in de map waarin u [!DNL Insight Server] hebt geïnstalleerd.

      Voorbeeld: [!DNL C:\Adobe\Server\bin]

   1. Bij de bevelherinnering, voer het volgende bevel uit om het als dienst onder Microsoft Windows tegen te houden en te verwijderen:

      ```
      InsightServer64.exe /unregserver
      ```

1. Verwijder de installatiemap [!DNL Insight Server].

## Transformatie {#section-5e6a604dadb5477ba4dc9f93c9be0897} verwijderen

1. Gebruik de volgende stappen om het [!DNL profile.cfg] dossier voor elk profiel bij te werken waarmee u [!DNL Transform] gebruikte.

   1. Open [!DNL Profile Manager].
   1. Klik met de rechtermuisknop op het vinkje naast [!DNL profile.cfg] en klik **[!UICONTROL Make Local]**. Er wordt een vinkje voor dit bestand weergegeven in de kolom [!DNL User].

   1. Klik met de rechtermuisknop op het nieuwe vinkje en klik op **[!UICONTROL Open]** > **[!UICONTROL in Insight]**. Het venster [!DNL profile.cfg] verschijnt.

   1. Verwijder in het venster [!DNL profile.cfg] de profielvermelding [!DNL Transform] uit de vector Directories.

   1. Klik met de rechtermuisknop **[!UICONTROL (modified)]** boven in het venster en klik **[!UICONTROL Save]**.

   1. Klik in [!DNL Profile Manager] met de rechtermuisknop op het vinkje voor [!DNL profile.cfg] in de kolom [!DNL User] en klik vervolgens op **[!UICONTROL Save to]** > *&lt;**[!UICONTROL profile name]**>*.

1. Verwijder de map [!DNL Transform] uit de map [!DNL Profiles] in de installatiemap [!DNL Insight Server].

## Repeater {#section-2f94141d956749d88f549dbea26e5272} verwijderen

1. Deregistreer de [!DNL Repeater] dienst van Vensters.

   1. Open een opdrachtprompt en navigeer naar de submap bin in de map waarin u [!DNL Repeater] hebt geïnstalleerd.

      Voorbeeld: [!DNL D:\Adobe\Repeater\bin]

   1. Bij de bevelherinnering, voer het volgende bevel uit om het als dienst onder Microsoft Windows tegen te houden en te verwijderen:

      ```
      InsightServer64.exe /unregserver
      ```

1. Verwijder de installatiemap [!DNL Repeater].
