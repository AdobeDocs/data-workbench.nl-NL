---
description: De parameter ExpFile wijst naar de locatie van het configuratiebestand van het experiment, dat uw experiment definieert.
solution: Analytics
title: De parameter ExpFile wijzigen
uuid: bf146f46-f541-4969-8d90-af1a0c969344
exl-id: 9c527ef9-aeda-4d83-8b98-a7dccbd55fe8
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '220'
ht-degree: 0%

---

# De parameter ExpFile wijzigen{#modifying-the-expfile-parameter}

{{eol}}

De parameter ExpFile wijst naar de locatie van het configuratiebestand van het experiment, dat uw experiment definieert.

Als u deze parameter instelt, kunt u experimenten uitvoeren. Voor stappen om het dossier van de experimentconfiguratie tot stand te brengen, zie [Het vormen en het Opstellen van de Experimenteer](../../../home/c-undst-ctrld-exp/t-crt-ctrld-exp/c-cnfg-dply-exp.md#concept-50f1de0242904698937bb72b3ea1b429).

Hieronder ziet u een voorbeeld van de parameter ExpFile:

```
ExpFile /home/experiment.txt
```

Dit tabblad gescheiden tekstbestand ( [!DNL .txt]) kan overal in [!DNL Sensor] en kan elke gewenste naam hebben.

Zorg ervoor u de plaats van de experimentenfolder en de naam van het configuratiedossier registreert dat u specificeert omdat u uw dossier van de experimentconfiguratie (dat later in deze gids moet worden beschreven) gebruikend deze naam en in deze folder moet opslaan.

>[!NOTE]
>
>Als u deze parameter niet op dezelfde manier instelt op elke computer in uw webcluster waarop een [!DNL Sensor] is geïnstalleerd, werkt gecontroleerde experimenten niet.

Deze ingang kan preconfigured zijn en in blijven [!DNL Sensor] configuratiebestand doorlopend te configureren zonder nadelige gevolgen. Als de opgegeven naam van het configuratiebestand voor het experiment niet wordt gevonden door [!DNL Sensor] of leeg is (dat wil zeggen dat het bestaat, maar geen inhoud heeft), [!DNL Sensor] voert het experiment niet uit, registreert een foutengebeurtenis op de server van HTTP, en blijft normaal in alle andere opzichten werken.
