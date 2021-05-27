---
description: Standaard luistert Insight Server op poort 80 (voor HTTP) en poort 443 (voor HTTPS).
title: De poortinstellingen controleren
uuid: 1adad226-5891-4498-80b6-1bb4d67f5bbb
exl-id: 924860e3-5afa-4c0f-bb7a-d38d5c1355b7
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '114'
ht-degree: 0%

---

# De poortinstellingen controleren{#checking-the-port-settings}

Standaard luistert Insight Server op poort 80 (voor HTTP) en poort 443 (voor HTTPS).

Als deze poorten al zijn toegewezen door een ander proces op de computer waarop u [!DNL Insight Server] hebt geïnstalleerd, gebruikt u de volgende procedure om de poorttoewijzingen [!DNL Insight Server’s] te wijzigen.

**De poorttoewijzingen wijzigen**

1. Navigeer naar de map [!DNL Components] in de map waarin u [!DNL Insight Server] hebt geïnstalleerd.

   Voorbeeld: [!DNL C:\Adobe\Server\Components]

1. Open het [!DNL Communications.cfg] dossier in een tekstredacteur zoals Blocnote.
1. Zoek de Poort en de SSL Poort ingangen, zoals hieronder getoond:

   ```
   component = CommServer: 
     Access Control File = Path: Access Control\\Access Control.cfg
     Access Log Directory = string: P:\\Audit\\
     IP Interface = string: 
     Port = int: 80
     SSL Port = int: 443
     Servers = vector: 17 items
       0 = InitServer: 
         Client Type = string: Sensor
         URI = string: /SensorInit.vsp
     . . .
   ```

1. Als dit niet de havens zijn die u [!DNL Insight Server] wilt gebruiken, verander de haventaken, dan sparen en sluit het dossier.
