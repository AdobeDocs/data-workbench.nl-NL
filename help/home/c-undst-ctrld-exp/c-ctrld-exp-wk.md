---
description: In een experiment, kunt u om het even welk aantal testgroepen naast de controlegroep bepalen.
solution: Analytics,Analytics
title: Hoe werken gecontroleerde experimenten?
topic: Data workbench
uuid: 9549e2ab-dca9-4fb1-9729-65072f951900
translation-type: tm+mt
source-git-commit: 34cdcfc83ae6bb620706db37228e200cff43ab2c
workflow-type: tm+mt
source-wordcount: '265'
ht-degree: 0%

---


# Hoe werken gecontroleerde experimenten?{#how-do-controlled-experiments-work}

In een experiment, kunt u om het even welk aantal testgroepen naast de controlegroep bepalen.

Wanneer een experiment loopt, worden alle bezoekers aan uw website deel van het experiment, of als deel van een testgroep of van de controlegroep, zodra zij tot om het even welke pagina toegang hebben die bij het experiment betrokken is. Bezoekers worden willekeurig toegewezen aan uw experimentele groepen, in verhoudingen die tijdens de experimentele configuratie zijn gedefinieerd.

Gecontroleerde experimenten worden geïmplementeerd met de [!DNL Sensor] software die op elk van de inhoudsservers in uw webcluster is geïnstalleerd. Aangezien de inhoudsservers verzoeken ontvangen, selecteert willekeurig bezoekers voor uw testgroepen en richt hun paginaverzoeken aan de experimentele inhoud opnieuw. [!DNL Sensor] Wanneer [!DNL Sensor] een bezoeker selecteert om de testinhoud te bekijken, blijft de adresbar van oorspronkelijk gevraagde URI een lijst maken maar de bezoeker wordt verpletterd aan test URI. Omdat dit proces intern in de servertoepassing plaatsvindt, zijn de gebruikers zich niet bewust van wanneer zij worden getest, wat een belangrijke overweging voor onpartijdige experimenten is.

[!DNL Sensor] geeft de test-URI&#39;s, niet de oorspronkelijke URI die aan de gebruiker wordt weergegeven, door aan de logbestanden voor gebruik in analyse.

De resultaten van de experimenten kunnen eenvoudig worden geanalyseerd om na te gaan [!DNL Insight] of de experimentele hypothese die u hebt getest, juist is.

>[!NOTE]
>
>Adobe beveelt ten zeerste aan dat gecontroleerde experimenten worden gecoördineerd en uitgevoerd met input van de personen in uw organisatie die verantwoordelijk zijn voor het configureren en onderhouden van uw analysegegevens.

