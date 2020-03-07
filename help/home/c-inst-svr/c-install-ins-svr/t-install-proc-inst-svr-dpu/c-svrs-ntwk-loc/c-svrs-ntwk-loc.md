---
description: De cliënten van de Server van het inzicht (het Rapport en het Inzicht) gebruiken gemeenschappelijke namen om naar de Servers van het Inzicht te verwijzen.
solution: Insight
title: De netwerklocatie van de server definiëren
uuid: 9cf2f268-6fde-4427-b832-a238d126d697
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# De netwerklocatie van de server definiëren{#defining-the-server-s-network-location}

De cliënten van de Server van het inzicht (het Rapport en het Inzicht) gebruiken gemeenschappelijke namen om naar de Servers van het Inzicht te verwijzen.

Bijvoorbeeld, wanneer u verbindt [!DNL Insight] of [!DNL Report] met een [!DNL Insight Server], identificeert u de server door zijn gemeenschappelijke naam (bijvoorbeeld, [!DNL Server.MyCompany.com]). Intern, lost de cliënt de gemeenschappelijke naam aan een numeriek IP adres op alvorens een verzoek naar de server te verzenden.

Om gemeenschappelijke namen aan IP adressen op te lossen, gebruiken de [!DNL Insight Server’s] cliënten een lokaal raadplegingsdossier genoemd het adresdossier. Het adresdossier maakt een lijst van de gemeenschappelijke namen van [!DNL Insight Servers] geïnstalleerd bij uw organisatie en identificeert hun numerieke IP adressen. Een cliënt ontvangt automatisch een exemplaar van het adresdossier wanneer het een profiel op opent [!DNL Insight Server].

Wanneer een cliënt een verzoek aan een [!DNL Insight Server]uitgeeft, probeert het om de gemeenschappelijke naam van de server door het adresdossier op te lossen. Als het adresdossier een IP adres voor de gevraagde server identificeert, leidt de cliënt het verzoek aan het gespecificeerde adres. Als het adres niet wordt bepaald (bijvoorbeeld, bepaalt het adresdossier niet de gemeenschappelijke naam van de server), ontbreekt het verzoek. Naar keuze, kunt u cliënten vormen om adressen door het normale het Noemen van het Domein van het werkende milieu mechanisme van de Dienst (DNS) op te lossen als een naam niet in het het adresdossier van de cliënt wordt bepaald. Voor instructies, zie de parameter van de Ouder in de lijst [van Parameters](../../../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/c-svrs-ntwk-loc/c-ntwk-loc.md#concept-18587827cbd24805801caa86bc816e05) NetworkLocation in de volgende sectie.
