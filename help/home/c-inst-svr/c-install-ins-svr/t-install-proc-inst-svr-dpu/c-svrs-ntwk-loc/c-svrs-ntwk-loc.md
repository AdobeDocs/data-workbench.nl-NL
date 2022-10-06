---
description: De cliënten van de Server van het inzicht (Rapport en Inzicht) gebruiken gemeenschappelijke namen om naar de Servers van het Inzicht te verwijzen.
title: De netwerklocatie van de server definiëren
uuid: 9cf2f268-6fde-4427-b832-a238d126d697
exl-id: def360b8-f146-45ca-ae61-fd213adef68b
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '233'
ht-degree: 0%

---

# De netwerklocatie van de server definiëren{#defining-the-server-s-network-location}

{{eol}}

De cliënten van de Server van het inzicht (Rapport en Inzicht) gebruiken gemeenschappelijke namen om naar de Servers van het Inzicht te verwijzen.

Wanneer u bijvoorbeeld verbinding maakt [!DNL Insight] of [!DNL Report] aan een [!DNL Insight Server], identificeert u de server met de algemene naam (bijvoorbeeld [!DNL Server.MyCompany.com]). Intern, lost de cliënt de gemeenschappelijke naam aan een numeriek IP adres op alvorens een verzoek naar de server te verzenden.

Om gemeenschappelijke namen aan IP adressen op te lossen, [!DNL Insight Server’s] clients gebruiken een lokaal opzoekbestand met de naam Adresbestand. In het adresbestand worden de algemene namen van [!DNL Insight Servers] geïnstalleerd bij uw organisatie en identificeert hun numerieke IP adressen. Een client ontvangt automatisch een kopie van het adresbestand wanneer een profiel wordt geopend op het tabblad [!DNL Insight Server].

Wanneer een klant een aanvraag aan een [!DNL Insight Server], wordt geprobeerd de algemene naam van de server via het adresbestand op te lossen. Als het adresdossier een IP adres voor de gevraagde server identificeert, leidt de cliënt het verzoek aan het gespecificeerde adres. Als het adres niet wordt bepaald (bijvoorbeeld, bepaalt het adresdossier niet de gemeenschappelijke naam van de server), ontbreekt het verzoek. Naar keuze, kunt u cliënten vormen om adressen door het normale mechanisme van de Noemende Dienst van het Domein van het werkende milieu op te lossen (DNS) als een naam niet in het het adresdossier van de cliënt wordt bepaald. Zie de parameter Bovenliggend in het dialoogvenster [NetworkLocation-parametertabel](../../../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/c-svrs-ntwk-loc/c-ntwk-loc.md#concept-18587827cbd24805801caa86bc816e05) in de volgende paragraaf.
