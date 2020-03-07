---
description: In een experiment, kunt u om het even welk aantal testgroepen naast de controlegroep bepalen.
solution: Insight,Analytics
title: Hoe werken gecontroleerde experimenten?
topic: Data workbench
uuid: 9549e2ab-dca9-4fb1-9729-65072f951900
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Hoe werken gecontroleerde experimenten?{#how-do-controlled-experiments-work}

In een experiment, kunt u om het even welk aantal testgroepen naast de controlegroep bepalen.

Wanneer een experiment loopt, worden alle bezoekers aan uw website deel van het experiment, of als deel van een testgroep of van de controlegroep, zodra zij tot om het even welke pagina toegang hebben betrokken bij het experiment. De bezoekers worden toegewezen aan uw experimentele groepen willekeurig, in aandelen die tijdens de experimentele configuratie worden bepaald.

De gecontroleerde experimenten worden uitgevoerd gebruikend de [!DNL Sensor] software die op elk van de inhoudsservers in uw Webcluster geïnstalleerd is. Aangezien de inhoudsservers verzoeken ontvangen, selecteert willekeurig [!DNL Sensor] bezoekers voor uw testgroepen en richt hun paginaverzoeken aan de experimentele inhoud opnieuw. Wanneer [!DNL Sensor] selecteert een bezoeker om de testinhoud te bekijken, blijft de adresbar van oorspronkelijk gevraagd URI een lijst maken maar de bezoeker wordt verpletterd aan de test URI. Omdat dit proces intern in de servertoepassing plaatsvindt, zijn de gebruikers zich niet bewust van wanneer zij worden getest, wat een belangrijke overweging voor onbevooroordeelde experimenten is.

[!DNL Sensor] gaat de test URIs, niet originele URI over die aan de gebruiker wordt getoond, tot de logboekdossiers voor gebruik in analyse.

De resultaten van de experimenten kunnen gemakkelijk worden geanalyseerd met behulp van [!DNL Insight] om vast te stellen of de experimentele hypothese die je testte juist is.

>[!NOTE]
>
>Adobe adviseert sterk dat de gecontroleerde experimenten met input van die individuen in uw organisatie worden gecoördineerd en worden uitgevoerd die voor het vormen van en het handhaven van uw analysedatasets verantwoordelijk zijn.

