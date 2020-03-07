---
description: Servercomponenten voor Data Workbench 6.1 upgraden vanaf installatie 5.4.
solution: Insight
title: DWB-serverupgrade 5.4 naar 5.5
uuid: 9cf9f493-f098-4c6d-a8b5-786833496557
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# DWB-serverupgrade: 5,4 t/m 5,5{#dwb-server-upgrade-to}

Servercomponenten voor Data Workbench 6.1 upgraden vanaf installatie 5.4.

De opwaardering van [!DNL Insight] 5,4 naar [!DNL Insight] 5,5 is derhalve relatief eenvoudig.

U kunt van [!DNL Insight] 5.3 aan [!DNL Insight] 5.5 direct ook bevorderen gebruikend de hieronder stappen. Zorg ervoor u alle verbeteringstaken uitvoert die in de [Bevordering van Inzicht 5.4 tot 5.5](../../../../home/c-inst-svr/c-upgrd-uninst-sftwr/c-upgrd-sftwr/t-upgrd-to-5.5.md#task-b581e47952e941158d52db3e68f076b9) sectie en de [Bevordering van Inzicht 5.4 tot 5.5](../../../../home/c-inst-svr/c-upgrd-uninst-sftwr/c-upgrd-sftwr/t-upgrd-to-5.5.md#task-b581e47952e941158d52db3e68f076b9) sectie worden vermeld.

1. Stop de [!DNL Insight Server] diensten op alle servers in de cluster behalve [!DNL Insight Master Server]de cluster.

   1. Kopieer de nieuwe [!DNL ReportServer.exe] en [!DNL Insight.exe] dossiers aan de omslag van het Inzicht van de Software \.

   1. Nadat de [!DNL Insight] cliënt heeft bijgewerkt, kopieer de [!DNL InsightServer.exe] en [!DNL InsightServer64.exe] dossiers in de omslag van de Bak \.

   1. Wacht tot [!DNL Insight Master Server] te beginnen, dan verifieer de versie die via de [!DNL Connections] visualisatie loopt.

1. Op de cluster [!DNL Master Server] in de [!DNL Insight] cliënt:

   1. Maak een lokaal exemplaar van het bestaande [!DNL Base] profiel en noem het (bijvoorbeeld, BaseBackup) anders.
   1. Kopieer het nieuwe [!DNL Base] profiel naar de map Profielen.
   1. Herhaal deze twee stappen voor de omslag van de Transformatie.

1. Kopieer de omslag van Manuscripten van het serverpakket op [!DNL Master Server] in de de installatiefolder van de Server.
1. Kopieer het [!DNL Terrain Images.cfg.off] dossier in de omslag van Componenten van [!DNL Master Server].
   **Om cliëntsoftware van[!DNL Insight]5.4 tot 5.5 te bevorderen**

In het [!DNL Insight.cfg] dossier, zorg ervoor dat het plaatsen van de Software van de Update aan WAAR wordt geplaatst.
