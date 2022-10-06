---
description: Instructies voor het verwijderen van Insight Server, Transform of Repeater.
title: De software verwijderen
uuid: 79cf0db6-0f99-40fa-a7b0-38dd8d7246bd
exl-id: 3ba5e5e3-c1a2-4ecb-9f88-a3fe923837e7
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 0%

---

# De software verwijderen{#uninstalling-your-software}

{{eol}}

Instructies voor het verwijderen van Insight Server, Transform of Repeater.

## Adobe van Insight Server verwijderen {#section-7d7befe672854df79bb6c28ec02f6670}

1. Registratie van de [!DNL Insight Server] Windows-service.

   1. Open een opdrachtprompt en navigeer naar de submap bin in de map waarin u hebt geïnstalleerd [!DNL Insight Server].

      Voorbeeld: [!DNL C:\Adobe\Server\bin]

   1. Bij de bevelherinnering, voer het volgende bevel uit om het als dienst onder Microsoft Windows tegen te houden en te verwijderen:

      ```
      InsightServer64.exe /unregserver
      ```

1. Verwijder de [!DNL Insight Server] installatiemap.

## Transformatie verwijderen {#section-5e6a604dadb5477ba4dc9f93c9be0897}

1. Gebruik de volgende stappen om de [!DNL profile.cfg] bestand voor elk profiel dat u gebruikt [!DNL Transform].

   1. Open de [!DNL Profile Manager].
   1. Klik met de rechtermuisknop op het vinkje naast [!DNL profile.cfg] en klik op **[!UICONTROL Make Local]**. Er wordt een vinkje voor dit bestand weergegeven in het dialoogvenster [!DNL User] kolom.

   1. Klik met de rechtermuisknop op het nieuwe vinkje en klik op **[!UICONTROL Open]** > **[!UICONTROL in Insight]**. De [!DNL profile.cfg] wordt weergegeven.

   1. In de [!DNL profile.cfg] venster, de [!DNL Transform] profielvermelding uit de map Directories.

   1. Klikken met rechtermuisknop **[!UICONTROL (modified)]** boven aan het venster en klik op **[!UICONTROL Save]**.

   1. In de [!DNL Profile Manager], klikt u met de rechtermuisknop op het vinkje voor [!DNL profile.cfg] in de [!DNL User] kolom, klik vervolgens op **[!UICONTROL Save to]** > *&lt;**[!UICONTROL profile name]**>*.

1. Verwijder de [!DNL Transform] uit de [!DNL Profiles] in uw [!DNL Insight Server] installatiemap.

## Repeater verwijderen {#section-2f94141d956749d88f549dbea26e5272}

1. Registratie van de [!DNL Repeater] Windows-service.

   1. Open een opdrachtprompt en navigeer naar de submap bin in de map waarin u hebt geïnstalleerd [!DNL Repeater].

      Voorbeeld: [!DNL D:\Adobe\Repeater\bin]

   1. Bij de bevelherinnering, voer het volgende bevel uit om het als dienst onder Microsoft Windows tegen te houden en te verwijderen:

      ```
      InsightServer64.exe /unregserver
      ```

1. Verwijder de [!DNL Repeater] installatiemap.
