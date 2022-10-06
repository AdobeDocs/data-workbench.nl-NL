---
description: Een typische configuratie van de Plaats gebruikt koekjes om bezoekers aan uw website uniek te identificeren en hun gedrag in tijd te volgen.
solution: Analytics
title: Hoe kunnen bezoekers van de site worden geïdentificeerd?
uuid: e1e451b8-e827-4010-bda9-9147c3b09958
exl-id: 2783ee11-6d6a-463d-86b5-dd63e490201f
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '331'
ht-degree: 0%

---

# Hoe kunnen bezoekers van de site worden geïdentificeerd?{#how-does-site-identify-visitors}

{{eol}}

Een typische configuratie van de Plaats gebruikt koekjes om bezoekers aan uw website uniek te identificeren en hun gedrag in tijd te volgen.

De eerste keer dat een bepaalde browser (als bezoeker beschouwd) een aanvraag voor uw website indient, [!DNL Sensor] werkt samen met uw webserver om een permanente cookie in te stellen (standaard [!DNL cs(cookie)(v1st)]), die intern binnen het systeem wordt geïnterpreteerd als [!DNL x-trackingid]. Deze cookie wordt slechts eenmaal ingesteld, op het allereerste verzoek dat die bezoeker bij uw website indient. Deze wordt vervolgens bij die bezoeker verzameld telkens wanneer die browser in de toekomst een aanvraag voor uw website indient (pagina of verzoek om een ingesloten object).

Het accepteren van een permanente cookie is een beslissing van de browser. Als een gebruiker ervoor kiest om permanente cookies te blokkeren, worden de aanvragen voor de paginaweergave nog steeds geregistreerd, maar de meetgegevens van die aanvragen zijn niet gecorreleerd met een bepaalde bezoeker of hun sessies op de website, tenzij u een alternatieve methode voor bezoekersidentificatie implementeert, zoals het gebruik van de Hash-transformatie in de velden IP en UserAgent.

>[!NOTE]
>
>De experimenten van de plaats kunnen slechts in datasets worden geanalyseerd waar de enige methode van bezoekersidentificatie in gebruik is [!DNL Sensor] stelt de methode Persistent Cookie in. Sensoren die op J2EE-servers (JBoss, Tomcat, WebLogic en WebSphere) worden uitgevoerd, ondersteunen gecontroleerde experimenten niet.

Tijdens een gecontroleerd experiment kunnen gebruikers die geen cookies accepteren, in verschillende experimentele groepen van de ene klik naar de andere worden geplaatst. Dit wordt alleen een probleem als u de testanalyse uitvoert terwijl het filter Verbroken sessie is uitgeschakeld [!DNL Insight], die Adobe niet aanbeveelt.

Zie voor meer informatie over het filter Verbroken sessie de * [!DNL Insight] Gebruikershandleiding*.

Als een bezoeker het cookie tijdens een experiment wist, wordt aan de bezoeker een nieuw cookie toegewezen en kan deze mogelijk aan een andere groep worden toegewezen. Omdat Adobe de bezoeker identificeert als nieuw, wordt het experiment niet ongeldig gemaakt.
