---
description: Om een cluster te gebruiken, moet u één Server van het Inzicht in de cluster aanwijzen om als master Server van het Inzicht te handelen.
solution: Analytics
title: De Master Insight Server installeren
uuid: a73214f3-b175-4e9e-8802-7a8451d86d3a
translation-type: tm+mt
source-git-commit: 34cdcfc83ae6bb620706db37228e200cff43ab2c
workflow-type: tm+mt
source-wordcount: '197'
ht-degree: 0%

---


# De Master Insight Server installeren{#installing-the-master-insight-server}

Om een cluster te gebruiken, moet u één Server van het Inzicht in de cluster aanwijzen om als master Server van het Inzicht te handelen.

Een clientcomponent zoals [!DNL Insight] of [!DNL Report] maakt verbinding met de master component [!DNL Insight Server] aan het begin van een sessie. Op volgende punten tijdens de sessie kan de client verbinding maken met andere componenten [!DNL Insight Servers] in de cluster om een query uit te voeren. Deze volgende verbindingen tussen de client en de andere [!DNL Insight Servers] in de cluster worden door de master tot stand gebracht [!DNL Insight Server] en zijn transparant voor de client.

Naast het tussenleggen van verbindingen tussen een cliënt en andere [!DNL Insight Servers] in de cluster, [!DNL Insight Server] fungeert de master als centraal administratief punt voor de gehele cluster. Wanneer u een cluster beheert, werkt u master bij [!DNL Insight Server]. De administratieve veranderingen die u op master aanbrengt [!DNL Insight Server] worden teruggewonnen door andere [!DNL Insight Servers] in de cluster.

**De master[!DNL Insight Server]**

1. Bepaal welke machine als master zal werken [!DNL Insight Server].
1. Installeer en configureer [!DNL Insight Server] (doorgaans een [!DNL Insight Server] FSU) op deze computer zoals beschreven in [Insight Server](../../../../../../home/c-inst-svr/c-msr-server/c-msr-server.md).
1. Installeer [!DNL Insight] en configureer een verbinding met de master server [!DNL Insight Server] zoals beschreven in de *[!DNL Insight]gebruikershandleiding*.
