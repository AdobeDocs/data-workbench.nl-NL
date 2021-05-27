---
description: Om een cluster te gebruiken, moet u één Server van het Inzicht in de cluster aanwijzen om als master Server van het Inzicht te handelen.
title: De Master Insight Server installeren
uuid: a73214f3-b175-4e9e-8802-7a8451d86d3a
exl-id: 710f1ffe-f620-4920-b4f9-a644cc68d4cc
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '197'
ht-degree: 0%

---

# De Master Insight Server installeren{#installing-the-master-insight-server}

Om een cluster te gebruiken, moet u één Server van het Inzicht in de cluster aanwijzen om als master Server van het Inzicht te handelen.

Een clientcomponent zoals [!DNL Insight] of [!DNL Report] maakt verbinding met de master [!DNL Insight Server] aan het begin van een sessie. Op volgende punten tijdens de sessie kan de client verbinding maken met andere [!DNL Insight Servers] in de cluster om een query uit te voeren. Deze volgende verbindingen tussen de client en de andere [!DNL Insight Servers] in de cluster worden door de master [!DNL Insight Server] tot stand gebracht en zijn transparant voor de client.

Naast tussenhandelverbindingen tussen een client en andere [!DNL Insight Servers] in de cluster, fungeert de master [!DNL Insight Server] als centraal beheerpunt voor de gehele cluster. Wanneer u een cluster beheert, werkt u master [!DNL Insight Server] bij. De administratieve veranderingen die u op master [!DNL Insight Server] aanbrengt worden teruggewonnen door andere [!DNL Insight Servers] in de cluster.

**De master[!DNL Insight Server]**

1. Bepaal welke machine als master [!DNL Insight Server] zal dienst doen.
1. Installeer en configureer [!DNL Insight Server] (doorgaans een [!DNL Insight Server] FSU) op deze computer zoals beschreven in [Insight Server](../../../../../../home/c-inst-svr/c-msr-server/c-msr-server.md).
1. Installeer [!DNL Insight] en configureer een verbinding met de master [!DNL Insight Server] zoals beschreven in de *[!DNL Insight]Handboek*.
