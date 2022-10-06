---
description: Om een cluster te gebruiken, moet u één Server van het Inzicht in de cluster aanwijzen om als master Server van het Inzicht te handelen.
title: De Master Insight Server installeren
uuid: a73214f3-b175-4e9e-8802-7a8451d86d3a
exl-id: 710f1ffe-f620-4920-b4f9-a644cc68d4cc
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '197'
ht-degree: 0%

---

# De Master Insight Server installeren{#installing-the-master-insight-server}

{{eol}}

Om een cluster te gebruiken, moet u één Server van het Inzicht in de cluster aanwijzen om als master Server van het Inzicht te handelen.

Een clientcomponent zoals [!DNL Insight] of [!DNL Report] verbindt met master [!DNL Insight Server] aan het begin van een sessie. Op volgende punten tijdens de sessie kan de client verbinding maken met andere [!DNL Insight Servers] in de cluster om een query uit te voeren. Deze volgende verbindingen tussen de client en de andere [!DNL Insight Servers] in de cluster wordt door de master [!DNL Insight Server] en zijn transparant voor de client.

Naast tussenhandelverbindingen tussen een cliënt en andere [!DNL Insight Servers] in de cluster, de master [!DNL Insight Server] fungeert als het centrale beheerpunt voor de gehele cluster. Wanneer u een cluster beheert, werkt u de master [!DNL Insight Server]. De administratieve wijzigingen die u aanbrengt op het master [!DNL Insight Server] worden opgehaald door de andere [!DNL Insight Servers] in de cluster.

**De master[!DNL Insight Server]**

1. Bepalen welke machine als master zal fungeren [!DNL Insight Server].
1. Installeren en configureren [!DNL Insight Server] (doorgaans een [!DNL Insight Server] FSU) op deze computer zoals beschreven in [Insight Server](../../../../../../home/c-inst-svr/c-msr-server/c-msr-server.md).
1. Installeren [!DNL Insight] en een verbinding met de master [!DNL Insight Server] zoals beschreven in de *[!DNL Insight]Handboek*.
