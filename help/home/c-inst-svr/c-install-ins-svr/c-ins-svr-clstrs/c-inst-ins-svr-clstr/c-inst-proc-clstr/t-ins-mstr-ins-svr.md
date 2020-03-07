---
description: Om een cluster te gebruiken, moet u één Server van het Inzicht in de cluster aanwijzen om als hoofdServer van het Inzicht te handelen.
solution: Insight
title: Het installeren van de HoofdServer van het Inzicht
uuid: a73214f3-b175-4e9e-8802-7a8451d86d3a
translation-type: tm+mt
source-git-commit: 27600561841db3705f4eee6ff0aeb8890444bbc9

---


# Het installeren van de HoofdServer van het Inzicht{#installing-the-master-insight-server}

Om een cluster te gebruiken, moet u één Server van het Inzicht in de cluster aanwijzen om als hoofdServer van het Inzicht te handelen.

Een cliëntcomponent zoals [!DNL Insight] of [!DNL Report] verbindt met de meester [!DNL Insight Server] aan het begin van een zitting. Op verdere punten tijdens de zitting, zou de cliënt met andere [!DNL Insight Servers] in de cluster kunnen verbinden om een vraag uit te voeren. Deze verdere verbindingen tussen de cliënt en andere [!DNL Insight Servers] in de cluster worden door de meester bemiddeld [!DNL Insight Server] en zijn transparant aan de cliënt.

Naast het bemiddelen van verbindingen tussen een cliënt en andere [!DNL Insight Servers] in de cluster, [!DNL Insight Server] doet de meester dienst als centraal administratief punt voor de volledige cluster. Wanneer u een cluster beheert, werkt u de meester bij [!DNL Insight Server]. De administratieve veranderingen die u op de meester aanbrengt [!DNL Insight Server] worden teruggewonnen door andere [!DNL Insight Servers] in de cluster.

**Om de meester te installeren[!DNL Insight Server]**

1. Bepaal welke machine als meester zal werken [!DNL Insight Server].
1. Installeer en vorm [!DNL Insight Server] (typisch, een [!DNL Insight Server] FSU) op deze machine zoals die in de Server [van het](../../../../../../home/c-inst-svr/c-msr-server/c-msr-server.md)Inzicht wordt beschreven.
1. Installeer [!DNL Insight] en vorm een verbinding aan de meester [!DNL Insight Server] zoals die in de Gids *[!DNL Insight]van de *Gebruiker wordt beschreven.
