---
description: Servercomponenten voor Data Workbench 6.1 bijwerken vanaf 5.4-installatie.
title: DWB Server upgrade 5.4 naar 5.5
uuid: 9cf9f493-f098-4c6d-a8b5-786833496557
exl-id: dd8c2a89-6a40-4ebf-a964-eb4851ab94a5
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '192'
ht-degree: 0%

---

# Upgrade van DWB-server: 5.4 t/m 5.5{#dwb-server-upgrade-to}

Servercomponenten voor Data Workbench 6.1 bijwerken vanaf 5.4-installatie.

Daarom is de upgrade van [!DNL Insight] 5.4 naar [!DNL Insight] 5.5 relatief eenvoudig.

U kunt ook rechtstreeks upgraden van [!DNL Insight] 5.3 naar [!DNL Insight] 5.5 met de onderstaande stappen. Zorg ervoor u alle verbeteringstaken uitvoert die in [Van Inzicht 5.4 aan 5.5 worden vermeld ](../../../../home/c-inst-svr/c-upgrd-uninst-sftwr/c-upgrd-sftwr/t-upgrd-to-5.5.md#task-b581e47952e941158d52db3e68f076b9) sectie en [Upgraden van Inzicht 5.4 aan 5.5](../../../../home/c-inst-svr/c-upgrd-uninst-sftwr/c-upgrd-sftwr/t-upgrd-to-5.5.md#task-b581e47952e941158d52db3e68f076b9) sectie.

1. Stop de [!DNL Insight Server] diensten op alle servers in de cluster behalve [!DNL Insight Master Server].

   1. Kopieer de nieuwe [!DNL ReportServer.exe]- en [!DNL Insight.exe]-bestanden naar de map Software\Insight.

   1. Nadat de [!DNL Insight] cliënt heeft bijgewerkt, kopieer [!DNL InsightServer.exe] en [!DNL InsightServer64.exe] dossiers in de omslag \ van de Bak.

   1. Wacht tot [!DNL Insight Master Server] begint, dan verifieer de versie die via [!DNL Connections] visualisatie loopt.

1. Op de [!DNL Master Server] van de cluster in de [!DNL Insight] cliënt:

   1. Maak een lokale kopie van het bestaande [!DNL Base]-profiel en wijzig de naam ervan (bijvoorbeeld BaseBackup).
   1. Kopieer het nieuwe [!DNL Base] profiel naar de omslag van Profielen.
   1. Herhaal deze twee stappen voor de map Transform.

1. Kopieer de map Scripts van het serverpakket naar de map [!DNL Master Server] in de installatiemap van de server.
1. Kopieer het [!DNL Terrain Images.cfg.off] dossier in de omslag van Componenten van [!DNL Master Server].
   **De clientsoftware upgraden van  [!DNL Insight] 5.4 naar 5.5**

Zorg ervoor dat in het [!DNL Insight.cfg]-bestand de instelling Software bijwerken is ingesteld op TRUE.
