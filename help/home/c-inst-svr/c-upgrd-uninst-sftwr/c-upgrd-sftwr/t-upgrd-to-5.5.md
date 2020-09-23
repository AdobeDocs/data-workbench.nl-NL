---
description: Servercomponenten voor Data Workbench 6.1 bijwerken vanaf 5.4-installatie.
solution: Analytics
title: DWB Server upgrade 5.4 naar 5.5
uuid: 9cf9f493-f098-4c6d-a8b5-786833496557
translation-type: tm+mt
source-git-commit: 34cdcfc83ae6bb620706db37228e200cff43ab2c
workflow-type: tm+mt
source-wordcount: '192'
ht-degree: 0%

---


# Upgrade van DWB-server: 5,4 t/m 5,5{#dwb-server-upgrade-to}

Servercomponenten voor Data Workbench 6.1 bijwerken vanaf 5.4-installatie.

De opwaardering van [!DNL Insight] 5,4 naar [!DNL Insight] 5,5 is dan ook relatief eenvoudig.

U kunt ook rechtstreeks een upgrade uitvoeren van [!DNL Insight] 5.3 naar [!DNL Insight] 5.5 door de onderstaande stappen uit te voeren. Zorg ervoor u alle verbeteringstaken uitvoert die in [Bevorderen van Inzicht 5.4 tot 5.5](../../../../home/c-inst-svr/c-upgrd-uninst-sftwr/c-upgrd-sftwr/t-upgrd-to-5.5.md#task-b581e47952e941158d52db3e68f076b9) sectie en [Bevorderen van Inzicht 5.4 tot 5.5](../../../../home/c-inst-svr/c-upgrd-uninst-sftwr/c-upgrd-sftwr/t-upgrd-to-5.5.md#task-b581e47952e941158d52db3e68f076b9) sectie worden vermeld.

1. Stop de [!DNL Insight Server] diensten op alle servers in de cluster behalve [!DNL Insight Master Server].

   1. Kopieer de nieuwe [!DNL ReportServer.exe] en [!DNL Insight.exe] bestanden naar de map Software\Insight.

   1. Kopieer de bestanden [!DNL Insight] en de bestanden naar de map \Bin nadat de [!DNL InsightServer.exe] [!DNL InsightServer64.exe] client is bijgewerkt.

   1. Wacht tot het programma [!DNL Insight Master Server] is gestart en controleer vervolgens de versie die via de [!DNL Connections] visualisatie wordt uitgevoerd.

1. Op de cluster [!DNL Master Server] in de [!DNL Insight] client:

   1. Maak een lokale kopie van het bestaande [!DNL Base] profiel en wijzig de naam ervan (bijvoorbeeld BaseBackup).
   1. Kopieer het nieuwe [!DNL Base] profiel naar de map Profielen.
   1. Herhaal deze twee stappen voor de map Transform.

1. Kopieer de map Scripts van het serverpakket naar de [!DNL Master Server] installatiemap van de Server.
1. Kopieer het [!DNL Terrain Images.cfg.off] bestand naar de map Components van het [!DNL Master Server]bestand.
   **De clientsoftware upgraden van[!DNL Insight]5.4 naar 5.5**

Controleer in het [!DNL Insight.cfg] bestand of de instelling Software bijwerken is ingesteld op TRUE.
