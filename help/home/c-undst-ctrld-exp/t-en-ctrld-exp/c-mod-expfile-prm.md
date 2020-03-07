---
description: De parameter ExpFile richt aan de plaats van het dossier van de experimentele configuratie, dat uw experiment bepaalt.
solution: Insight,Analytics
title: Het wijzigen van de Parameter ExpFile
topic: Data workbench
uuid: bf146f46-f541-4969-8d90-af1a0c969344
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Het wijzigen van de Parameter ExpFile{#modifying-the-expfile-parameter}

De parameter ExpFile richt aan de plaats van het dossier van de experimentele configuratie, dat uw experiment bepaalt.

Het plaatsen van deze parameter laat u toe om experimenten in werking te stellen. Voor stappen om het dossier van de experimentele configuratie tot stand te brengen, zie het [Vormen van en het Opstellen van de Experiment](../../../home/c-undst-ctrld-exp/t-crt-ctrld-exp/c-cnfg-dply-exp.md#concept-50f1de0242904698937bb72b3ea1b429).

Na is een voorbeeld van de parameter ExpFile:

```
ExpFile /home/experiment.txt
```

Dit lusje afgebakende tekstdossier ( [!DNL .txt]) kan overal in de [!DNL Sensor] omslag worden gevestigd en kan om het even welke geschikte naam hebben.

Zorg ervoor u de plaats van de experimentenfolder en de naam van het configuratiedossier registreert dat u specificeert omdat u uw dossier van de experimentele configuratie (dat later in deze gids moet worden beschreven) moet bewaren gebruikend deze naam en in deze folder.

>[!NOTE]
>
>Als u deze parameter niet identiek op elke machine in uw Webcluster plaatst waarop een [!DNL Sensor] geïnstalleerd is, werkt de gecontroleerde experimentatie niet.

Deze ingang kan preconfigured zijn en in het [!DNL Sensor] configuratiedossier op een aan de gang zijnde basis zonder negatief effect blijven. Als het gespecificeerde dossier van de experimentele configuratie niet door wordt gevonden [!DNL Sensor] of het leeg is (namelijk bestaat het maar heeft geen inhoud), voert [!DNL Sensor] niet het experiment uit, registreert een foutengebeurtenis op de server van HTTP, en blijft normaal in alle andere opzichten werken.
