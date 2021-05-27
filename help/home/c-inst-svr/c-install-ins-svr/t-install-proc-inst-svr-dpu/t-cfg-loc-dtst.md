---
description: Door gebrek, schrijft de Server van het Inzicht zijn dataset (temp.db) aan de zelfde aandrijving zoals de het programmadossiers van de Server van het Inzicht.
title: Het vormen van de Plaats van de Dataset (temp.db)
uuid: a6884cad-70ed-4bc6-853c-700d301fb178
exl-id: 6812883f-ad51-4314-8c80-e95c3fe84664
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '251'
ht-degree: 0%

---

# De locatie van de gegevensset configureren (temp.db){#configuring-the-location-of-the-dataset-temp-db}

Door gebrek, schrijft de Server van het Inzicht zijn dataset (temp.db) aan de zelfde aandrijving zoals de het programmadossiers van de Server van het Inzicht.

Als u bijvoorbeeld [!DNL Insight Server] op station C installeert, wordt de gegevensset naar station C geschreven.

Als u [!DNL Insight Server] de dataset op een verschillende aandrijving wilt handhaven, of als de hoeveelheid gegevens u verwacht te verzamelen het gebruik van veelvoudige aandrijving vereist, moet u [!DNL Disk Files.cfg] dossier bijwerken om te specificeren waar u [!DNL Insight Server] het [!DNL temp.db] dossier wilt schrijven.

**De locatie van temp.db configureren**

1. Navigeer naar de map [!DNL Components] in de map waarin u [!DNL Insight Server] hebt geïnstalleerd.

   Voorbeeld: [!DNL C:\Adobe\Server\Components]

1. Open het [!DNL Disk Files.cfg] dossier in een tekstredacteur zoals Blocnote.

   Standaard bevat dit bestand één item in de schijfbestandsstructuur, zoals hieronder wordt weergegeven.

   ```
   component = DiskSpaceManagerComponent:
     Disk Files = vector: 1 items
      0 = string: Temp\\temp.db
     Detect Disk Corruption = bool: true
   ```

1. Als u de locatie van [!DNL temp.db] wilt wijzigen, wijzigt u de definitie Schijfbestanden. In het volgende voorbeeld ziet u hoe u de configuratie kunt bewerken om het [!DNL temp.db]-bestand over stations C, D en E te verspreiden:

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
   >Let op het gebruik van de dubbele backslashes in de bovenstaande bestandsnamen. In [!DNL Insight Server] configuratiedossiers, is backslash karakter een vluchtkarakter. Deze wordt gebruikt om speciale controlereeksen (bijvoorbeeld \t voor een tabteken) in tekst uit te drukken. Als u een backslash wilt weergeven, moet u de backslash tweemaal typen (bijvoorbeeld \\) om de functie escape te overschrijven. Dit is alleen van toepassing wanneer u configuratiebestanden bewerkt in een teksteditor, zoals Kladblok.
