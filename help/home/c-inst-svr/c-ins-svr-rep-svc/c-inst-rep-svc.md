---
description: De dienst van de Replicatie van ServerReplication van het Inzicht laat u toe om de gebeurtenisgegevens over te brengen die op één machine van de Server van het Inzicht worden verzameld en worden opgeslagen aan een andere machine van de Server van het Inzicht.
title: De replicatieservice installeren
uuid: a6467d5f-ca1c-4368-ba83-0b6bcabbe511
exl-id: a235fe75-a6d0-4c20-8ea2-8b1cbad12da7
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '184'
ht-degree: 0%

---

# De replicatieservice installeren{#installing-the-replication-service}

De dienst van de Replicatie van ServerReplication van het Inzicht laat u toe om de gebeurtenisgegevens over te brengen die op één machine van de Server van het Inzicht worden verzameld en worden opgeslagen aan een andere machine van de Server van het Inzicht.

Gewoonlijk wordt de computer waarop de gegevens worden verzameld en opgeslagen geconfigureerd om te worden uitgevoerd als een [!DNL Repeater]-computer. Zie [Herstellerfunctionaliteit](../../../home/c-inst-svr/c-rptr-fntly/c-rptr-fntly.md). Met de [!DNL Replication Service], die wordt geconfigureerd door het [!DNL Replicate.cfg]-bestand, kan een [!DNL Insight Server]-computer gegevens ophalen van de [!DNL Repeater]-computer en deze lokaal opslaan. De [!DNL Insight Server] machine wordt bedoeld als doelmachine. Meerdere [!DNL Insight Server] DPU&#39;s kunnen verbinding maken met één [!DNL Repeater] om kopieën van de gebeurtenisgegevens aan te vragen voor opname in meerdere datasets.

U kunt [!DNL Replication Service] in netwerkinfrastructuur met veelvoudige lagen van het vuurwerk gebruiken om enig-haven aan enig-haven mededelingen tussen componenten te bereiken die door firewalls worden gescheiden.

**Als u het dialoogvenster[!DNL Replication Service]**

Het [!DNL Replicate.cfg] dossier zou als deel van uw [!DNL Insight Server] installatie moeten worden geïnstalleerd. U kunt het bestand vinden in de map [!DNL Components] van de installatiemap van [!DNL Insight Server]. Neem contact op met Adobe als u dit bestand niet hebt.
