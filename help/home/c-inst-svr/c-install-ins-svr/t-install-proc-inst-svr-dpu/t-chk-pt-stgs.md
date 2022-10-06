---
description: Standaard luistert Insight Server op poort 80 (voor HTTP) en poort 443 (voor HTTPS).
title: De poortinstellingen controleren
uuid: 1adad226-5891-4498-80b6-1bb4d67f5bbb
exl-id: 924860e3-5afa-4c0f-bb7a-d38d5c1355b7
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '114'
ht-degree: 0%

---

# De poortinstellingen controleren{#checking-the-port-settings}

{{eol}}

Standaard luistert Insight Server op poort 80 (voor HTTP) en poort 443 (voor HTTPS).

Als deze poorten al zijn toegewezen door een ander proces op de computer waarop u hebt geïnstalleerd [!DNL Insight Server]de volgende procedure gebruiken om [!DNL Insight Server’s] poorttoewijzingen.

**De poorttoewijzingen wijzigen**

1. Ga naar de [!DNL Components] map in de map waarin u hebt geïnstalleerd [!DNL Insight Server].

   Voorbeeld: [!DNL C:\Adobe\Server\Components]

1. Open de [!DNL Communications.cfg] bestand in een teksteditor, zoals Kladblok.
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

1. Als dit niet de havens zijn die u wilt [!DNL Insight Server] om te gebruiken, verander de haventaken, dan sparen en sluit het dossier.
