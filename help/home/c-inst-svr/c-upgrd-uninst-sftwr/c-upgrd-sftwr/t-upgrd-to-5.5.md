---
description: Servercomponenten voor Data Workbench 6.1 bijwerken vanaf 5.4-installatie.
title: DWB Server upgrade 5.4 naar 5.5
uuid: 9cf9f493-f098-4c6d-a8b5-786833496557
exl-id: dd8c2a89-6a40-4ebf-a964-eb4851ab94a5
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '192'
ht-degree: 0%

---

# Upgrade van DWB-server: 5,4 t/m 5,5{#dwb-server-upgrade-to}

{{eol}}

Servercomponenten voor Data Workbench 6.1 bijwerken vanaf 5.4-installatie.

Daarom is de modernisering [!DNL Insight] 5,4 tot [!DNL Insight] 5.5 is relatief eenvoudig.

U kunt ook rechtstreeks upgraden vanaf [!DNL Insight] 5.3 t/m [!DNL Insight] 5.5. de onderstaande stappen te volgen. Zorg ervoor dat u alle upgradetaken uitvoert die in het dialoogvenster [Bijwerken van Insight 5.4 naar 5.5](../../../../home/c-inst-svr/c-upgrd-uninst-sftwr/c-upgrd-sftwr/t-upgrd-to-5.5.md#task-b581e47952e941158d52db3e68f076b9) en de [Bijwerken van Insight 5.4 naar 5.5](../../../../home/c-inst-svr/c-upgrd-uninst-sftwr/c-upgrd-sftwr/t-upgrd-to-5.5.md#task-b581e47952e941158d52db3e68f076b9) sectie.

1. Stop de [!DNL Insight Server] services op alle servers in de cluster, met uitzondering van de [!DNL Insight Master Server].

   1. Nieuw kopiëren [!DNL ReportServer.exe] en [!DNL Insight.exe] bestanden naar de map Software\Insight.

   1. Na de [!DNL Insight] de client is bijgewerkt, kopieert u de [!DNL InsightServer.exe] en [!DNL InsightServer64.exe] in de map \Bin.

   1. Wacht op de [!DNL Insight Master Server] om te beginnen, dan verifieer de versie die via [!DNL Connections] visualisatie.

1. Op de cluster [!DNL Master Server] in de [!DNL Insight] client:

   1. Een lokale kopie maken van het bestaande [!DNL Base] profiel en hernoemen (bijvoorbeeld BaseBackup).
   1. Nieuw kopiëren [!DNL Base] naar de map Profielen.
   1. Herhaal deze twee stappen voor de map Transform.

1. Kopieer de map Scripts van het serverpakket naar de map [!DNL Master Server] in de installatiemap van de Server.
1. Kopieer de [!DNL Terrain Images.cfg.off] in de map Components van het bestand [!DNL Master Server].
   **De clientsoftware upgraden vanaf [!DNL Insight] 5,4 t/m 5,5**

In de [!DNL Insight.cfg] , zorgt u ervoor dat de instelling Software bijwerken is ingesteld op TRUE.
