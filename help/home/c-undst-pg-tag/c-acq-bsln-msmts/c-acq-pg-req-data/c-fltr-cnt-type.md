---
description: Het doel van het inhoudstype het filtreren van de sensor vermogen is de behoefte om informatie op te slaan en te verwerken die niet nuttig voor analysedoeleinden is.
title: Filteren op inhoudstype
uuid: 8a3b567b-8c7b-4ca2-bfcb-74a1addda2bd
exl-id: 0ed93a18-ef47-462b-8609-3ec98b037e6b
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '195'
ht-degree: 0%

---

# Filteren op inhoudstype{#filtering-by-content-type}

Het doel van het inhoudstype het filtreren van de sensor vermogen is de behoefte om informatie op te slaan en te verwerken die niet nuttig voor analysedoeleinden is.

Veel van de aanvraaggegevens die beschikbaar zijn via de API van een webserver, zijn niet nuttig voor bedrijfsanalyses. Opslag en verwerking zijn duur en u kunt overbodige opslag en verwerking vermijden door inhoud te filteren.[!DNL Sensor’s]

Om de prestaties van de gegevensverwerking van het Weblogboek te maximaliseren en de hoeveelheid meetgegevens te verminderen die moet worden opgeslagen, [!DNL Site] verwerft meetgegevens (verzoekgegevens, logboekingangen, logboekgegevens, etc.) voor alle Web content-type verzoeken, behalve specifiek vermelde inhoudstypes (zoals het draperen van stijlbladen, beeldverzoeken, etc.), die uit worden gefilterd alvorens zij aan de server van de gegevenswerkbank door [!DNL Sensor] worden overgebracht. Dit filtreren kan voor een volledige Webserver worden onbruikbaar gemaakt, en het kan ook voor een bepaald inhoudsvoorwerp worden met voeten getreden door het naam-waardepaar &quot;Log=1&quot;aan het vraagkoord van een bepaald ingebed voorwerp (bijvoorbeeld, [!DNL http://www.mysite.com/advertisement.gif?Log=1]) toe te voegen.
