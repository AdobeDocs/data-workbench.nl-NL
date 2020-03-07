---
description: Door gebrek, schrijft de Server van het Inzicht zijn dataset (temp.db) aan de zelfde aandrijving zoals de het programmadossiers van de Server van het Inzicht.
solution: Insight
title: Het vormen van de Plaats van de Dataset (temp.db)
uuid: a6884cad-70ed-4bc6-853c-700d301fb178
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Het vormen van de Plaats van de Dataset (temp.db){#configuring-the-location-of-the-dataset-temp-db}

Door gebrek, schrijft de Server van het Inzicht zijn dataset (temp.db) aan de zelfde aandrijving zoals de het programmadossiers van de Server van het Inzicht.

Bijvoorbeeld, als u [!DNL Insight Server] op aandrijving C installeert, schrijft het de dataset aan aandrijving C.

Als u de dataset op een verschillende aandrijving wilt handhaven, of als de hoeveelheid gegevens u verwacht te verzamelen het gebruik van veelvoudige aandrijving vereist, moet u het [!DNL Insight Server] dossier bijwerken om te specificeren waar u het [!DNL Disk Files.cfg] dossier wilt [!DNL Insight Server] [!DNL temp.db] schrijven.

**Om de plaats van temp.db te vormen**

1. Navigeer aan de [!DNL Components] omslag in de folder waar u installeerde [!DNL Insight Server].

   Voorbeeld: [!DNL C:\Adobe\Server\Components]

1. Open het [!DNL Disk Files.cfg] dossier in een tekstredacteur zoals Blocnote.

   Door gebrek, bevat dit dossier één enkele ingang in de structuur van de Dossiers van de Schijf zoals hieronder getoond.

   ```
   component = DiskSpaceManagerComponent:
     Disk Files = vector: 1 items
      0 = string: Temp\\temp.db
     Detect Disk Corruption = bool: true
   ```

1. Om de plaats van te veranderen, wijzig de definitie van de Dossiers van de Schijf [!DNL temp.db]. Het volgende voorbeeld illustreert hoe u de configuratie zou uitgeven om het [!DNL temp.db] dossier over aandrijving C, D, en E uit te spreiden:

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
   >Neem nota van het gebruik van de dubbele backslashes in de dossiernamen hierboven. In [!DNL Insight Server] configuratiedossiers, is het backslash karakter een vluchtkarakter. Het wordt gebruikt om speciale controleopeenvolgingen (bijvoorbeeld, \ t voor een lusjekarakter) in tekst uit te drukken. Om een daadwerkelijk backslash karakter te vertegenwoordigen, moet u backslash tweemaal typen (bijvoorbeeld, \ \) om de vluchtfunctie met voeten te treden. Dit is van toepassing slechts wanneer het uitgeven van configuratiedossiers in een tekstredacteur zoals Blocnote.

