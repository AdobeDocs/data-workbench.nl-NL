---
description: De dienst van de Replicatie van ServerReplication van het Inzicht laat u toe om de gebeurtenisgegevens over te brengen die op één machine van de Server van het Inzicht worden verzameld en worden opgeslagen aan een andere machine van de Server van het Inzicht.
title: De replicatieservice installeren
uuid: a6467d5f-ca1c-4368-ba83-0b6bcabbe511
exl-id: a235fe75-a6d0-4c20-8ea2-8b1cbad12da7
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '184'
ht-degree: 0%

---

# De replicatieservice installeren{#installing-the-replication-service}

{{eol}}

De dienst van de Replicatie van ServerReplication van het Inzicht laat u toe om de gebeurtenisgegevens over te brengen die op één machine van de Server van het Inzicht worden verzameld en worden opgeslagen aan een andere machine van de Server van het Inzicht.

Meestal wordt de computer waarop de gegevens worden verzameld en opgeslagen geconfigureerd om als een [!DNL Repeater] machine. Zie [Repeater-functionaliteit](../../../home/c-inst-svr/c-rptr-fntly/c-rptr-fntly.md). De [!DNL Replication Service], die door de [!DNL Replicate.cfg] bestand, schakelt een [!DNL Insight Server] computer om gegevens van [!DNL Repeater] en lokaal opslaan. De [!DNL Insight Server] De machine wordt de doelmachine genoemd. Meerdere [!DNL Insight Server] DPUs kan met één enkele verbinden [!DNL Repeater] om kopieën van de gebeurtenisgegevens te vragen voor opname in meerdere gegevensreeksen.

U kunt de [!DNL Replication Service] in netwerkinfrastructuur met veelvoudige lagen van het vuurwerk om enig-haven aan enig-haven mededelingen tussen componenten te bereiken die door firewalls worden gescheiden.

**Als u het dialoogvenster[!DNL Replication Service]**

De [!DNL Replicate.cfg] moet als onderdeel van uw [!DNL Insight Server] installatie. U kunt het bestand vinden in het dialoogvenster [!DNL Components] map van uw [!DNL Insight Server] installatiemap. Neem contact op met Adobe als u dit bestand niet hebt.
