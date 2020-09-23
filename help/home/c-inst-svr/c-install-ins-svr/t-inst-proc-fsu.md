---
description: De instructies voor het installeren van een Server FSU van het Inzicht en het vormen van het voor administratief gebruik zijn zeer gelijkaardig aan die voor het installeren van en het vormen van een DPU van de Server van het Inzicht.
solution: Analytics
title: Installatieprocedures voor een Insight Server FSU
uuid: ffed5095-f83c-4641-9ccc-4b94f51c3f95
translation-type: tm+mt
source-git-commit: 34cdcfc83ae6bb620706db37228e200cff43ab2c
workflow-type: tm+mt
source-wordcount: '163'
ht-degree: 0%

---


# Installatieprocedures voor een Insight Server FSU{#installation-procedures-for-an-insight-server-fsu}

De instructies voor het installeren van een Server FSU van het Inzicht en het vormen van het voor administratief gebruik zijn zeer gelijkaardig aan die voor het installeren van en het vormen van een DPU van de Server van het Inzicht.

Voor de Bescherming *van het Eindpunt van het Centrum van het Systeem van* MS in Vensters 2012 Servers, moeten deze uitvoerbare lijnen aan de **Uitgesloten Processen worden toegevoegd:**

* [!DNL InsightServer64.exe]
* [!DNL ReportServer.exe]
* [!DNL ExportIntegration.exe]

Als u een [!DNL Insight Server] FSU wilt installeren en configureren, moet u de volgende taken uitvoeren:

1. Installeer de [!DNL Insight Server] programmabestanden.
1. Installeer het [!DNL Insight Server] digitale certificaat.
1. Controleer de poortinstellingen in het [!DNL Communications.cfg] bestand.
1. Wijzig het [!DNL Access Control.cfg] bestand om beheerderstoegang toe te staan [!DNL the Server] van [!DNL the Client].
1. Wijzig het [!DNL server.address] bestand om de netwerklocatie van de server te definiëren.
1. Stel Windows-parameters voor geheugengebruik in zoals beschreven.
1. Registreer [!DNL Insight Server] als dienst van Vensters zoals beschreven.

   Voor instructies om gegevensbronnen, toestemmingen, en mededelingen voor een [!DNL Insight Server] FSU te vormen, zie de Gids *van de Configuratie van de* Dataset.

