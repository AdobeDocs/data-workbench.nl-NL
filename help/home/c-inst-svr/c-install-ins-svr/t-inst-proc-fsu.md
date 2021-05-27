---
description: De instructies voor het installeren van een Server FSU van het Inzicht en het vormen van het voor administratief gebruik zijn zeer gelijkaardig aan die voor het installeren van en het vormen van een DPU van de Server van het Inzicht.
title: Installatieprocedures voor een Insight Server FSU
uuid: ffed5095-f83c-4641-9ccc-4b94f51c3f95
exl-id: 7373af97-0ecf-47a2-bc27-dbfeb7ca3eaa
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '163'
ht-degree: 0%

---

# Installatieprocedures voor een Insight Server FSU{#installation-procedures-for-an-insight-server-fsu}

De instructies voor het installeren van een Server FSU van het Inzicht en het vormen van het voor administratief gebruik zijn zeer gelijkaardig aan die voor het installeren van en het vormen van een DPU van de Server van het Inzicht.

Voor *MS System Center Endpoint Protection* in Windows 2012-servers moeten deze uitvoerbare bestanden worden toegevoegd aan de **Uitgesloten processen:**

* [!DNL InsightServer64.exe]
* [!DNL ReportServer.exe]
* [!DNL ExportIntegration.exe]

Als u een [!DNL Insight Server] FSU wilt installeren en configureren, moet u de volgende taken uitvoeren:

1. Installeer de [!DNL Insight Server] programmabestanden.
1. Installeer het [!DNL Insight Server] digitale certificaat.
1. Controleer de poortinstellingen in het [!DNL Communications.cfg]-bestand.
1. Wijzig het [!DNL Access Control.cfg] dossier om administratieve toegang tot [!DNL the Server] van [!DNL the Client] toe te staan.
1. Wijzig het [!DNL server.address]-bestand om de netwerklocatie van de server te definiëren.
1. Stel Windows-parameters voor geheugengebruik in zoals beschreven.
1. Registreer [!DNL Insight Server] als dienst van Vensters zoals beschreven.

   Voor instructies om gegevensbronnen, toestemmingen, en mededelingen voor [!DNL Insight Server] FSU te vormen, zie *de Gids van de Configuratie van de Dataset*.
