---
description: In het profiel Geografie wordt een verzameling afbeeldingslagen en bestanden opgeslagen.
title: Lagen weergeven
uuid: ebc7025d-e619-43dd-88da-7452ada3226b
exl-id: 12ec913f-c7e5-49b5-8792-db0881cb5cfe
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '267'
ht-degree: 0%

---

# Lagen weergeven{#display-layers}

{{eol}}

In het profiel Geografie wordt een verzameling afbeeldingslagen en bestanden opgeslagen.

Wanneer u een bol weergeeft, kunt u selecteren welke van de beschikbare lagen voor een bepaalde analystaak worden weergegeven:

* **Blauwe marmer 2 km:** In deze laag wordt de wereldbol weergegeven. Wanneer deze laag niet is geselecteerd, is de bol niet zichtbaar.
* **IP-coördinaten:** Deze laag van elementpunt toont de breedte en de lengte van plaatsen in uw dataset die op bezoekerIP adressen wordt gebaseerd.
* **Zip-punten:** In deze laag worden de breedte en lengte van locaties in uw gegevensset weergegeven op basis van een lijst met ZIP-codes van Verenigde Staten die door Adobe worden verschaft. De [!DNL Zip Points.txt] Het opzoekbestand bevat de ZIP-code, breedte- en lengtegegevens die moeten worden weergegeven, terwijl het [!DNL Zip Points.layer] bevat de configuratieparameters die nodig zijn om deze gegevens op de wereldbol weer te geven. Beide bestanden worden opgeslagen in de map Profiles\Geography\Maps in de installatiemap van de Data Workbench-server.

* ***Andere beschikbare laagnamen:*** Elke laagnaam vertegenwoordigt een [!DNL .layer] bestand dat is opgeslagen in de map Profielen\Geography\Maps, Profielen\IP Geo-location\Maps of de map Profiles\IP Geo-intelligence\Maps in de installatiemap van Insight Server.

>[!NOTE]
>
>Om IP Geo-plaats of IP Geo-intelligentieprofiel te hebben, moet u aan of de IP Geo-plaats of IP Geo-inlichtingendatadienst intekenen.

Als u de volgorde wilt bepalen waarin de lagen worden weergegeven, kunt u een [!DNL order.txt] bestand. Zie [Menu&#39;s aanpassen met Order.txt-bestanden](../../../../home/c-get-started/c-intf-anlys-ftrs/c-ctm-menus/t-cstm-menus-ordr-files.md#task-a391800a8dd444deb3e1516d5189f999).

**Lagen in een wereldbol in- of uitschakelen**

* Klik met de rechtermuisknop in de visualisatie en klik op de gewenste laagnaam. Een X links van de laag geeft aan dat de laag zichtbaar is.
