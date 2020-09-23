---
description: De parameter ExpFile wijst naar de locatie van het configuratiebestand van het experiment, dat uw experiment definieert.
solution: Analytics,Analytics
title: De parameter ExpFile wijzigen
topic: Data workbench
uuid: bf146f46-f541-4969-8d90-af1a0c969344
translation-type: tm+mt
source-git-commit: 34cdcfc83ae6bb620706db37228e200cff43ab2c
workflow-type: tm+mt
source-wordcount: '220'
ht-degree: 0%

---


# De parameter ExpFile wijzigen{#modifying-the-expfile-parameter}

De parameter ExpFile wijst naar de locatie van het configuratiebestand van het experiment, dat uw experiment definieert.

Als u deze parameter instelt, kunt u experimenten uitvoeren. Voor stappen om het dossier van de experimentele configuratie tot stand te brengen, zie het [Vormen en het Opstellen van de Experiment](../../../home/c-undst-ctrld-exp/t-crt-ctrld-exp/c-cnfg-dply-exp.md#concept-50f1de0242904698937bb72b3ea1b429).

Hieronder ziet u een voorbeeld van de parameter ExpFile:

```
ExpFile /home/experiment.txt
```

Dit door tabs gescheiden tekstbestand ( [!DNL .txt]) kan overal in de [!DNL Sensor] map staan en elke gewenste naam hebben.

Zorg ervoor u de plaats van de experimentenfolder en de naam van het configuratiedossier registreert dat u specificeert omdat u uw dossier van de experimentconfiguratie (dat later in deze gids moet worden beschreven) gebruikend deze naam en in deze folder moet opslaan.

>[!NOTE]
>
>Als u deze parameter niet op dezelfde manier instelt op elke computer in uw webcluster waarop een computer [!DNL Sensor] is geïnstalleerd, werkt gecontroleerde experimenten niet.

Deze ingang kan preconfigured zijn en in het [!DNL Sensor] configuratiedossier onophoudelijk zonder negatief effect blijven. Wanneer de opgegeven naam van het configuratiebestand voor het experiment niet wordt gevonden door [!DNL Sensor] of leeg is (het bestaat, maar heeft geen inhoud), [!DNL Sensor] wordt het experiment niet uitgevoerd, wordt een foutgebeurtenis op de HTTP-server geregistreerd en wordt het normaal in alle andere opzichten uitgevoerd.
