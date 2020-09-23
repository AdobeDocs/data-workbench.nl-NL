---
description: Door gebrek, schrijft de Server van het Inzicht zijn dataset (temp.db) aan de zelfde aandrijving zoals de het programmadossiers van de Server van het Inzicht.
solution: Analytics
title: Het vormen van de Plaats van de Dataset (temp.db)
uuid: a6884cad-70ed-4bc6-853c-700d301fb178
translation-type: tm+mt
source-git-commit: 34cdcfc83ae6bb620706db37228e200cff43ab2c
workflow-type: tm+mt
source-wordcount: '251'
ht-degree: 0%

---


# Het vormen van de Plaats van de Dataset (temp.db){#configuring-the-location-of-the-dataset-temp-db}

Door gebrek, schrijft de Server van het Inzicht zijn dataset (temp.db) aan de zelfde aandrijving zoals de het programmadossiers van de Server van het Inzicht.

Bijvoorbeeld, als u [!DNL Insight Server] op aandrijving C installeert, schrijft het de dataset aan aandrijving C.

Als u de dataset op een verschillende aandrijving wilt handhaven, of als de hoeveelheid gegevens u verwacht te verzamelen het gebruik van veelvoudige aandrijving vereist, moet u het [!DNL Insight Server] dossier bijwerken om te specificeren waar u het [!DNL Disk Files.cfg] dossier [!DNL Insight Server] [!DNL temp.db] wilt schrijven.

**De locatie van temp.db configureren**

1. Navigeer naar de [!DNL Components] map in de map waarin u hebt geïnstalleerd [!DNL Insight Server].

   Voorbeeld: [!DNL C:\Adobe\Server\Components]

1. Open het [!DNL Disk Files.cfg] bestand in een teksteditor, zoals Kladblok.

   Standaard bevat dit bestand één item in de schijfbestandsstructuur, zoals hieronder wordt weergegeven.

   ```
   component = DiskSpaceManagerComponent:
     Disk Files = vector: 1 items
      0 = string: Temp\\temp.db
     Detect Disk Corruption = bool: true
   ```

1. Wijzig de definitie Schijfbestanden om de locatie van [!DNL temp.db]de bestanden te wijzigen. In het volgende voorbeeld ziet u hoe u de configuratie kunt bewerken om het [!DNL temp.db] bestand over de stations C, D en E te verspreiden:

   ```
   component = DiskSpaceManagerComponent:
     Disk Files = vector: 3 items
       0 = string: C:\\Temp\\temp.db
       1 = string: D:\\Temp\\temp.db
       2 = string: E:\\Temp\\temp.db
     Detect Disk Corruption = bool: true
   ```

   >[!NOTE]
   >
   >Let op het gebruik van de dubbele backslashes in de bovenstaande bestandsnamen. In [!DNL Insight Server] configuratiebestanden is de backslash een escape-teken. Deze wordt gebruikt om speciale controlereeksen (bijvoorbeeld \t voor een tabteken) in tekst uit te drukken. Als u een backslash wilt weergeven, moet u de backslash tweemaal typen (bijvoorbeeld \\) om de functie escape te overschrijven. Dit is alleen van toepassing wanneer u configuratiebestanden bewerkt in een teksteditor, zoals Kladblok.

