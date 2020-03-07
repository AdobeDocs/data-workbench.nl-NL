---
description: Door gebrek, luistert de Server van het Inzicht op havens 80 (voor HTTP) en 443 (voor HTTPS).
solution: Insight
title: De poortinstellingen controleren
uuid: 1adad226-5891-4498-80b6-1bb4d67f5bbb
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# De poortinstellingen controleren{#checking-the-port-settings}

Door gebrek, luistert de Server van het Inzicht op havens 80 (voor HTTP) en 443 (voor HTTPS).

Als deze havens reeds door een ander proces op de machine worden toegewezen waar u hebt geïnstalleerd [!DNL Insight Server], gebruik de volgende procedure om [!DNL Insight Server’s] haventaken te veranderen.

**Om de haventaken te veranderen**

1. Navigeer aan de [!DNL Components] omslag in de folder waar u installeerde [!DNL Insight Server].

   Voorbeeld: [!DNL C:\Adobe\Server\Components]

1. Open het [!DNL Communications.cfg] dossier in een tekstredacteur zoals Blocnote.
1. Bepaal de plaats van de Haven en de SSL ingangen van de Haven, zoals hieronder getoond:

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
