---
description: Een typische configuratie van de Plaats gebruikt koekjes om bezoekers aan uw website uniek te identificeren en hun gedrag in tijd te volgen.
solution: Analytics,Analytics
title: Hoe kunnen bezoekers van de site worden geïdentificeerd?
uuid: e1e451b8-e827-4010-bda9-9147c3b09958
exl-id: 2783ee11-6d6a-463d-86b5-dd63e490201f
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '331'
ht-degree: 0%

---

# Hoe identificeert de plaats bezoekers?{#how-does-site-identify-visitors}

Een typische configuratie van de Plaats gebruikt koekjes om bezoekers aan uw website uniek te identificeren en hun gedrag in tijd te volgen.

De eerste keer dat een bepaalde browser (als bezoeker beschouwd) een verzoek indient van uw website, werkt [!DNL Sensor] samen met uw webserver om een permanente cookie in te stellen (standaard [!DNL cs(cookie)(v1st)]), die intern in het systeem wordt geïnterpreteerd als [!DNL x-trackingid]. Deze cookie wordt slechts eenmaal ingesteld, op het allereerste verzoek dat die bezoeker bij uw website indient. Deze wordt vervolgens bij die bezoeker verzameld telkens wanneer die browser in de toekomst een aanvraag voor uw website indient (pagina of verzoek om een ingesloten object).

Het accepteren van een permanente cookie is een beslissing van de browser. Als een gebruiker ervoor kiest om permanente cookies te blokkeren, worden de aanvragen voor de paginaweergave nog steeds geregistreerd, maar de meetgegevens van die aanvragen zijn niet gecorreleerd met een bepaalde bezoeker of hun sessies op de website, tenzij u een alternatieve methode voor bezoekersidentificatie implementeert, zoals het gebruik van de Hash-transformatie in de velden IP en UserAgent.

>[!NOTE]
>
>Siteexperimenten kunnen alleen worden geanalyseerd in datasets waarbij de enige methode voor bezoekersidentificatie in gebruik de [!DNL Sensor] ingestelde permanente cookie methode is. Sensoren die op J2EE-servers (JBoss, Tomcat, WebLogic en WebSphere) worden uitgevoerd, ondersteunen gecontroleerde experimenten niet.

Tijdens een gecontroleerd experiment kunnen gebruikers die geen cookies accepteren, in verschillende experimentele groepen van de ene klik naar de andere worden geplaatst. Dit wordt alleen een probleem als u de testanalyse uitvoert terwijl het filter Verbroken sessie is uitgeschakeld in [!DNL Insight], wat Adobe niet aanbeveelt.

Zie de * [!DNL Insight] Gebruikershandleiding* voor meer informatie over het filter Verbroken sessie.

Als een bezoeker het cookie tijdens een experiment wist, wordt aan de bezoeker een nieuw cookie toegewezen en kan deze mogelijk aan een andere groep worden toegewezen. Omdat Adobe de bezoeker identificeert als nieuw, wordt het experiment niet ongeldig gemaakt.
