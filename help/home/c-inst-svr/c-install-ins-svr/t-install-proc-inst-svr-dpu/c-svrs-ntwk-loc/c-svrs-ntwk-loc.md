---
description: De cliënten van de Server van het inzicht (Rapport en Inzicht) gebruiken gemeenschappelijke namen om naar de Servers van het Inzicht te verwijzen.
solution: Analytics
title: De netwerklocatie van de server definiëren
uuid: 9cf2f268-6fde-4427-b832-a238d126d697
translation-type: tm+mt
source-git-commit: 34cdcfc83ae6bb620706db37228e200cff43ab2c
workflow-type: tm+mt
source-wordcount: '233'
ht-degree: 0%

---


# De netwerklocatie van de server definiëren{#defining-the-server-s-network-location}

De cliënten van de Server van het inzicht (Rapport en Inzicht) gebruiken gemeenschappelijke namen om naar de Servers van het Inzicht te verwijzen.

Wanneer u bijvoorbeeld verbinding maakt [!DNL Insight] of een verbinding maakt [!DNL Report] met een server, identificeert u de server aan de hand van de algemene naam (bijvoorbeeld [!DNL Insight Server][!DNL Server.MyCompany.com]). Intern, lost de cliënt de gemeenschappelijke naam aan een numeriek IP adres op alvorens een verzoek naar de server te verzenden.

Om gemeenschappelijke namen aan IP adressen op te lossen, gebruiken de [!DNL Insight Server’s] cliënten een lokaal raadplegingsdossier genoemd het adresdossier. Het adresdossier maakt een lijst van de gemeenschappelijke namen van [!DNL Insight Servers] die bij uw organisatie worden geïnstalleerd en identificeert hun numerieke IP adressen. Een client ontvangt automatisch een kopie van het adresbestand wanneer er een profiel op het scherm wordt geopend [!DNL Insight Server].

Wanneer een client een aanvraag naar een server verzendt, [!DNL Insight Server]wordt geprobeerd de algemene naam van de server via het adresbestand op te lossen. Als het adresdossier een IP adres voor de gevraagde server identificeert, leidt de cliënt het verzoek aan het gespecificeerde adres. Als het adres niet wordt bepaald (bijvoorbeeld, bepaalt het adresdossier niet de gemeenschappelijke naam van de server), ontbreekt het verzoek. Naar keuze, kunt u cliënten vormen om adressen door het normale mechanisme van de Noemende Dienst van het Domein van het werkende milieu op te lossen (DNS) als een naam niet in het het adresdossier van de cliënt wordt bepaald. Voor instructies, zie de parameter van de Ouder in de lijst [van Parameters](../../../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/c-svrs-ntwk-loc/c-ntwk-loc.md#concept-18587827cbd24805801caa86bc816e05) NetworkLocation in de volgende sectie.
