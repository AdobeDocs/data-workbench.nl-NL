---
description: Het doel van het inhoudstype het filtreren van de sensor vermogen is de behoefte om informatie op te slaan en te verwerken die niet nuttig voor analysedoeleinden is.
title: Filteren op inhoudstype
uuid: 8a3b567b-8c7b-4ca2-bfcb-74a1addda2bd
exl-id: 0ed93a18-ef47-462b-8609-3ec98b037e6b
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '195'
ht-degree: 0%

---

# Filteren op inhoudstype{#filtering-by-content-type}

{{eol}}

Het doel van het inhoudstype het filtreren van de sensor vermogen is de behoefte om informatie op te slaan en te verwerken die niet nuttig voor analysedoeleinden is.

Veel van de aanvraaggegevens die beschikbaar zijn via de API van een webserver, zijn niet nuttig voor bedrijfsanalyses. Opslag en verwerking zijn duur en [!DNL Sensor’s] met filteren van inhoudstypen kunt u overbodige opslag en verwerking voorkomen.

Om de prestaties van de gegevensverwerking van het Weblogboek te maximaliseren en de hoeveelheid meetgegevens te verminderen die moet worden opgeslagen, [!DNL Site] verwerft meetgegevens (verzoekgegevens, logboekingangen, logboekgegevens, etc.) voor alle Web content-type verzoeken, behalve specifiek vermelde inhoudstypes (zoals cascading stijlbladen, beeldverzoeken, etc.), die uit worden gefilterd alvorens zij aan de server van de gegevenswerkbank door worden overgebracht [!DNL Sensor]. Dit filtreren kan voor een volledige Webserver onbruikbaar worden gemaakt, en het kan ook voor een bepaald inhoudsvoorwerp worden met voeten getreden door het naam-waarde paar &quot;Log=1&quot;aan het vraagkoord van een bepaald ingebed voorwerp (bijvoorbeeld toe te voegen) [!DNL https://www.mysite.com/advertisement.gif?Log=1]).
