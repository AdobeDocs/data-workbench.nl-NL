---
description: De dienst van de Replicatie van ServerReplication van het Inzicht laat u toe om de gebeurtenisgegevens over te brengen die op één machine van de Server van het Inzicht worden verzameld en worden opgeslagen aan een andere machine van de Server van het Inzicht.
solution: Analytics
title: De replicatieservice installeren
uuid: a6467d5f-ca1c-4368-ba83-0b6bcabbe511
translation-type: tm+mt
source-git-commit: 34cdcfc83ae6bb620706db37228e200cff43ab2c
workflow-type: tm+mt
source-wordcount: '184'
ht-degree: 0%

---


# De replicatieservice installeren{#installing-the-replication-service}

De dienst van de Replicatie van ServerReplication van het Inzicht laat u toe om de gebeurtenisgegevens over te brengen die op één machine van de Server van het Inzicht worden verzameld en worden opgeslagen aan een andere machine van de Server van het Inzicht.

De computer waarop de gegevens worden verzameld en opgeslagen, is doorgaans geconfigureerd om als een [!DNL Repeater] computer te worden uitgevoerd. Zie [Repeater-functionaliteit](../../../home/c-inst-svr/c-rptr-fntly/c-rptr-fntly.md). Met [!DNL Replication Service]dit bestand, dat door het [!DNL Replicate.cfg] bestand wordt geconfigureerd, kan een [!DNL Insight Server] computer gegevens ophalen van de [!DNL Repeater] computer en deze lokaal opslaan. De [!DNL Insight Server] machine wordt de doelmachine genoemd. De veelvoudige [!DNL Insight Server] DPUs kan met één enkele verbinding verbinden [!DNL Repeater] om exemplaren van de gebeurtenisgegevens voor opneming in veelvoudige datasets te verzoeken.

U kunt [!DNL Replication Service] in netwerkinfrastructuur met veelvoudige lagen van het vuurwerk gebruiken om enig-haven aan enig-haven mededelingen tussen componenten te bereiken die door firewalls worden gescheiden.

**Als u het dialoogvenster[!DNL Replication Service]**

Het [!DNL Replicate.cfg] bestand moet als onderdeel van de [!DNL Insight Server] installatie worden geïnstalleerd. U kunt het bestand vinden in de [!DNL Components] map van de [!DNL Insight Server] installatiemap. Neem contact op met Adobe als u dit bestand niet hebt.
