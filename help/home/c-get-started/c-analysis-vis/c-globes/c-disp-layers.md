---
description: In het profiel Geografie wordt een verzameling afbeeldingslagen en bestanden opgeslagen.
title: Lagen weergeven
uuid: ebc7025d-e619-43dd-88da-7452ada3226b
exl-id: 12ec913f-c7e5-49b5-8792-db0881cb5cfe
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '267'
ht-degree: 0%

---

# Lagen weergeven{#display-layers}

In het profiel Geografie wordt een verzameling afbeeldingslagen en bestanden opgeslagen.

Wanneer u een bol weergeeft, kunt u selecteren welke van de beschikbare lagen voor een bepaalde analystaak worden weergegeven:

* **Blauw marmer 2 km:** Deze laag geeft de wereldbol weer. Wanneer deze laag niet is geselecteerd, is de bol niet zichtbaar.
* **IP Coördinaten:** Deze laag van het elementenpunt toont de breedte en de lengtegraad van plaatsen in uw dataset die op bezoekerIP adressen wordt gebaseerd.
* **Zip de Punten:** Deze laag toont de breedtegraad en de lengtegraad van plaatsen in uw dataset die op een lijst van de Codes van het ZIP van de Verenigde Staten door Adobe wordt gebaseerd. Het opzoekbestand [!DNL Zip Points.txt] bevat de ZIP-code, breedte- en lengtegegevens die moeten worden weergegeven, terwijl het bestand [!DNL Zip Points.layer] de configuratieparameters bevat die nodig zijn om deze gegevens op de wereldschaal weer te geven. Beide bestanden worden opgeslagen in de map Profiles\Geography\Maps folder within the Data Workbench server installation directory.

* ***Andere beschikbare laagnamen:*** Elke laagnaam vertegenwoordigt een  [!DNL .layer] bestand dat is opgeslagen in de map Profiles\Geography\Maps folder, Profielen\IP Geo-location\Maps of Profielen\IP Geo-intelligence\Maps in de installatiemap van Insight Server.

>[!NOTE]
>
>Om IP Geo-plaats of IP Geo-intelligentieprofiel te hebben, moet u aan of de IP Geo-plaats of IP Geo-inlichtingendatadienst intekenen.

Als u de volgorde waarin de lagen worden weergegeven wilt bepalen, kunt u een [!DNL order.txt]-bestand gebruiken. Zie [Menu&#39;s aanpassen met Order.txt-bestanden](../../../../home/c-get-started/c-intf-anlys-ftrs/c-ctm-menus/t-cstm-menus-ordr-files.md#task-a391800a8dd444deb3e1516d5189f999).

**Lagen in een wereldbol in- of uitschakelen**

* Klik met de rechtermuisknop in de visualisatie en klik op de gewenste laagnaam. Een X links van de laag geeft aan dat de laag zichtbaar is.
