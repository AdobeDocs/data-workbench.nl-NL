---
description: Door gebrek, schrijft de Server van het Inzicht zijn dataset (temp.db) aan de zelfde aandrijving zoals de het programmadossiers van de Server van het Inzicht.
title: Het vormen van de Plaats van de Dataset (temp.db)
uuid: a6884cad-70ed-4bc6-853c-700d301fb178
exl-id: 6812883f-ad51-4314-8c80-e95c3fe84664
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '251'
ht-degree: 0%

---

# Het vormen van de Plaats van de Dataset (temp.db){#configuring-the-location-of-the-dataset-temp-db}

{{eol}}

Door gebrek, schrijft de Server van het Inzicht zijn dataset (temp.db) aan de zelfde aandrijving zoals de het programmadossiers van de Server van het Inzicht.

Als u bijvoorbeeld [!DNL Insight Server] op aandrijving C, schrijft het de dataset aan aandrijving C.

Als u [!DNL Insight Server] om de dataset op een verschillende aandrijving te handhaven, of als de hoeveelheid gegevens u verwacht te verzamelen het gebruik van veelvoudige aandrijving vereist, moet u bijwerken [!DNL Disk Files.cfg] bestand om aan te geven waar u wilt [!DNL Insight Server] om de [!DNL temp.db] bestand.

**De locatie van temp.db configureren**

1. Ga naar de [!DNL Components] map in de map waarin u hebt geïnstalleerd [!DNL Insight Server].

   Voorbeeld: [!DNL C:\Adobe\Server\Components]

1. Open de [!DNL Disk Files.cfg] bestand in een teksteditor, zoals Kladblok.

   Standaard bevat dit bestand één item in de schijfbestandsstructuur, zoals hieronder wordt weergegeven.

   ```
   component = DiskSpaceManagerComponent:
     Disk Files = vector: 1 items
      0 = string: Temp\\temp.db
     Detect Disk Corruption = bool: true
   ```

1. De locatie wijzigen van [!DNL temp.db]wijzigt u de definitie Schijfbestanden. In het volgende voorbeeld ziet u hoe u de configuratie kunt bewerken om de [!DNL temp.db] bestand op de stations C, D en E:

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
   >Let op het gebruik van de dubbele backslashes in de bovenstaande bestandsnamen. In [!DNL Insight Server] configuratiebestanden, is de backslash een escape-teken. Deze wordt gebruikt om speciale controlereeksen (bijvoorbeeld \t voor een tabteken) in tekst uit te drukken. Als u een backslash wilt weergeven, moet u de backslash tweemaal typen (bijvoorbeeld \\) om de functie escape te overschrijven. Dit is alleen van toepassing wanneer u configuratiebestanden bewerkt in een teksteditor, zoals Kladblok.
