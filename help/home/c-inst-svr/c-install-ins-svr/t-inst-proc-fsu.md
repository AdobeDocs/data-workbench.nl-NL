---
description: De instructies voor het installeren van een Server FSU van het Inzicht en het vormen van het voor administratief gebruik zijn zeer gelijkaardig aan die voor het installeren van en het vormen van een DPU van de Server van het Inzicht.
title: Installatieprocedures voor een Insight Server FSU
uuid: ffed5095-f83c-4641-9ccc-4b94f51c3f95
exl-id: 7373af97-0ecf-47a2-bc27-dbfeb7ca3eaa
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '163'
ht-degree: 0%

---

# Installatieprocedures voor een Insight Server FSU{#installation-procedures-for-an-insight-server-fsu}

{{eol}}

De instructies voor het installeren van een Server FSU van het Inzicht en het vormen van het voor administratief gebruik zijn zeer gelijkaardig aan die voor het installeren van en het vormen van een DPU van de Server van het Inzicht.

Voor *MS System Center Endpoint Protection* in Windows 2012-servers moeten deze uitvoerbare bestanden worden toegevoegd aan de **Uitgesloten processen:**

* [!DNL InsightServer64.exe]
* [!DNL ReportServer.exe]
* [!DNL ExportIntegration.exe]

Om een [!DNL Insight Server] FSU, moet u de volgende taken voltooien:

1. Installeer de [!DNL Insight Server] programmabestanden.
1. Installeer de [!DNL Insight Server] digitaal certificaat.
1. Controleer de poortinstellingen in het dialoogvenster [!DNL Communications.cfg] bestand.
1. De [!DNL Access Control.cfg] bestand om administratieve toegang te verlenen tot [!DNL the Server] van [!DNL the Client].
1. De [!DNL server.address] bestand om de netwerklocatie van de server te definiëren.
1. Stel Windows-parameters voor geheugengebruik in zoals beschreven.
1. Registreren [!DNL Insight Server] als de dienst van Vensters zoals beschreven.

   Voor instructies om gegevensbronnen, toestemmingen, en mededelingen voor een te vormen [!DNL Insight Server] FSU, zie *Configuratie-handleiding voor gegevensset*.
