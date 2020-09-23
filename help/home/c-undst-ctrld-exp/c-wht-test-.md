---
description: De testresultaten moeten duidelijk en zinvol zijn, zodat u er zeker van kunt zijn dat u op basis van die resultaten beslissingen neemt die in grote hoeveelheden worden genomen.
solution: Analytics,Analytics
title: Wat moet ik testen?
topic: Data workbench
uuid: 9dfe3685-885e-4098-ab1d-ac891ccc5199
translation-type: tm+mt
source-git-commit: 34cdcfc83ae6bb620706db37228e200cff43ab2c
workflow-type: tm+mt
source-wordcount: '431'
ht-degree: 0%

---


# Wat moet ik testen?{#what-should-i-test}

De testresultaten moeten duidelijk en zinvol zijn, zodat u er zeker van kunt zijn dat u op basis van die resultaten beslissingen neemt die in grote hoeveelheden worden genomen.

Hoewel u verschillende paginalay-outs met [!DNL Sensor] en Site kunt testen, stelt Adobe voor dat u zich richt op het testen van hoogwaardige, strategische bedrijfsinitiatieven of nieuwe of opnieuw ontworpen websitefunctionaliteit die de doelen die u voor uw website en voor uw bedrijf hebt gesteld, aanpakt. U kunt testen op problemen zoals de beste prijsgaranties, personalisatiefunctionaliteit, marktaanbiedingen (bijvoorbeeld pakketten of bundels), creatief ontwerp en toepassingsprocessen.

De volgende concepten zijn het belangrijkst wanneer het ontwikkelen van uw gecontroleerd experiment:

* **Begrijp de juiste veranderingen aan te brengen.** Hiervoor is wat onderzoek nodig naar de werking van uw website en de bedrijfsprocessen die aan de front-end website ten grondslag liggen. U wilt wijzigingen aanbrengen die de meeste impact hebben en eenvoudig kunnen worden getest.
* **Kleine wijzigingen kunnen een aanzienlijke invloed hebben.** Niet alle veranderingen die u test moeten drastisch zijn om een significante invloed op uw zaken te hebben. Altijd open staan voor kleine, maar zeer belangrijke wijzigingen.

## Ondersteunde methoden {#section-1071adaf54c64ba9bc5ef228c4a23635}

Veel typen experimenten met veel verschillende doelen kunnen worden uitgevoerd met Site. Hieronder volgen enkele voorbeelden:

* Pagina-, inhoud- en websiteprocessen wijzigen om de conversiesnelheden te verbeteren.
* Het veranderen van marketing campagnes, promoties, dwars-verkoopt, en omhoog-verkoopt om opbrengst te verhogen.
* De verschillende tijden van de paginadading om klantenkwaliteit van de dienst en de daadwerkelijke waarde van infrastructuurprestaties te begrijpen.

Om deze doelstellingen te bereiken, steunt de Plaats de volgende types van methodologieën voor gecontroleerde experimenteren en het testen:

* **Pagina vervangen:** Vervang statische URL X door statische URL Y. Deze methode is van beperkte toepassing in een dynamische omgeving.
* **Dynamische URI-vervanging:** Dit is een variant van Pagina Vervanging die statische pagina X met dynamische pagina Y vervangt om dynamische inhoud terug te geven.
* **Objectvervanging:** Vast object X vervangen door vast object Y.
* **Inhoud vervangen:** Vervang inhoudsset X (meerdere objecten, pagina&#39;s, tabel, enzovoort) door inhoudset Y.
* **Vervanging experimentele variabele:** Vervang het JavaScript-object /writeCookie_X.js door het JavaScript-object /writeCookie_Y.js om een cookie te schrijven die door een back-end systeem kan worden gebruikt om bepaalde inhoud te leveren.

>[!NOTE]
>
>De gecontroleerde experimenten zijn gebaseerd op de vervanging van URI, niet de vervanging van het vraagkoord. De URI binnen een bepaalde URL wordt in het volgende voorbeeld gemarkeerd:
>
>`http://www.omniture.com/index.asp?id=1`
>
>Bijvoorbeeld, in uw gecontroleerd experiment kon u specificeren dat de controlegroep URI met de testgroep URI [!DNL index.asp] wordt vervangen [!DNL index2.asp] om te bepalen welk paginaontwerp in meer waarde zou resulteren.
