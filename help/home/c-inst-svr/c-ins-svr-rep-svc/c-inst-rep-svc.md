---
description: De dienst van de Replicatie van de Server van het Inzicht laat u toe om de gebeurtenisgegevens over te brengen die op één machine van de Server van het Inzicht worden verzameld en worden opgeslagen aan een andere machine van de Server van het Inzicht.
solution: Insight
title: De replicatieservice installeren
uuid: a6467d5f-ca1c-4368-ba83-0b6bcabbe511
translation-type: tm+mt
source-git-commit: 27600561841db3705f4eee6ff0aeb8890444bbc9

---


# De replicatieservice installeren{#installing-the-replication-service}

De dienst van de Replicatie van de Server van het Inzicht laat u toe om de gebeurtenisgegevens over te brengen die op één machine van de Server van het Inzicht worden verzameld en worden opgeslagen aan een andere machine van de Server van het Inzicht.

Typisch, wordt de machine waarop het gegeven wordt verzameld en opgeslagen gevormd om als [!DNL Repeater] machine te lopen. Zie [Repeater Functionaliteit](../../../home/c-inst-svr/c-rptr-fntly/c-rptr-fntly.md). Het [!DNL Replication Service], dat door het [!DNL Replicate.cfg] dossier wordt gevormd, laat een [!DNL Insight Server] machine toe om gegevens van de [!DNL Repeater] machine terug te winnen en het plaatselijk op te slaan. De [!DNL Insight Server] machine wordt bedoeld als doelmachine. De veelvoudige [!DNL Insight Server] DPUs kan met één enkel verbinden [!DNL Repeater] om exemplaren van de gebeurtenisgegevens voor opneming in veelvoudige datasets te verzoeken.

U kunt [!DNL Replication Service] in netwerkinfrastructuur met veelvoudige lagen van het firewalling gebruiken om enig-haven aan enig-havenmededelingen tussen componenten te bereiken die door firewalls worden gescheiden.

**Om het[!DNL Replication Service]**

Het [!DNL Replicate.cfg] dossier zou als deel van uw [!DNL Insight Server] installatie moeten worden geïnstalleerd. U kunt het dossier binnen de [!DNL Components] omslag van uw [!DNL Insight Server] installatiefolder vinden. Als u dit dossier niet hebt, contacteer Adobe.
