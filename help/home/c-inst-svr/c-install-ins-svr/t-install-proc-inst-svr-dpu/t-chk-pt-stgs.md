---
description: Standaard luistert Insight Server op poort 80 (voor HTTP) en poort 443 (voor HTTPS).
solution: Analytics
title: De poortinstellingen controleren
uuid: 1adad226-5891-4498-80b6-1bb4d67f5bbb
translation-type: tm+mt
source-git-commit: 34cdcfc83ae6bb620706db37228e200cff43ab2c
workflow-type: tm+mt
source-wordcount: '114'
ht-degree: 0%

---


# De poortinstellingen controleren{#checking-the-port-settings}

Standaard luistert Insight Server op poort 80 (voor HTTP) en poort 443 (voor HTTPS).

Als deze havens reeds door een ander proces op de machine worden toegewezen waar u hebt geïnstalleerd [!DNL Insight Server], gebruik de volgende procedure om [!DNL Insight Server’s] haventaken te veranderen.

**De poorttoewijzingen wijzigen**

1. Navigeer naar de [!DNL Components] map in de map waarin u hebt geïnstalleerd [!DNL Insight Server].

   Voorbeeld: [!DNL C:\Adobe\Server\Components]

1. Open het [!DNL Communications.cfg] bestand in een teksteditor, zoals Kladblok.
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

1. Als dit niet de havens zijn die u wilt gebruiken, verander de haventaken, dan sparen en sluit het dossier. [!DNL Insight Server]
