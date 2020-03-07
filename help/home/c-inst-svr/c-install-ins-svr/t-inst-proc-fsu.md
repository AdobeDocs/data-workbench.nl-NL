---
description: De instructies voor het installeren van een Server FSU van het Inzicht en het vormen van het voor administratief gebruik zijn zeer gelijkaardig aan die voor het installeren van en het vormen van een Server DPU van het Inzicht.
solution: Insight
title: Installatieprocedures voor een Insight Server FSU
uuid: ffed5095-f83c-4641-9ccc-4b94f51c3f95
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Installatieprocedures voor een Insight Server FSU{#installation-procedures-for-an-insight-server-fsu}

De instructies voor het installeren van een Server FSU van het Inzicht en het vormen van het voor administratief gebruik zijn zeer gelijkaardig aan die voor het installeren van en het vormen van een Server DPU van het Inzicht.

Voor de Bescherming *van het Eindpunt van het Centrum van het Systeem van* MS in Vensters 2012 Servers, moeten deze uitvoerbare voorwerpen aan de **Uitgesloten Processen worden toegevoegd:**

* [!DNL InsightServer64.exe]
* [!DNL ReportServer.exe]
* [!DNL ExportIntegration.exe]

Om een [!DNL Insight Server] FSU te installeren en te configureren, moet u de volgende taken uitvoeren:

1. Installeer de [!DNL Insight Server] programmadossiers.
1. Installeer het [!DNL Insight Server] digitale certificaat.
1. Controleer de havenmontages in het [!DNL Communications.cfg] dossier.
1. Wijzig het [!DNL Access Control.cfg] dossier om administratieve toegang tot van [!DNL the Server] te verlenen [!DNL the Client].
1. Wijzig het [!DNL server.address] dossier om de het netwerkplaats van de server te bepalen.
1. De vastgestelde parameters van het het geheugengebruik van Vensters zoals beschreven.
1. Register [!DNL Insight Server] als dienst van Vensters zoals beschreven.

   Voor instructies om gegevensbronnen, toestemmingen, en mededelingen voor een [!DNL Insight Server] FSU te vormen, zie de Gids *van de Configuratie van de* Dataset.

