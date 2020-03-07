---
description: Het doel van het tevreden-type van Sensor filtrerende vermogen is de behoefte te elimineren om informatie op te slaan en te verwerken die niet nuttig voor analysedoeleinden is.
solution: Analytics
title: Filtreren op inhoudstype
topic: Data workbench
uuid: 8a3b567b-8c7b-4ca2-bfcb-74a1addda2bd
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Filtreren op inhoudstype{#filtering-by-content-type}

Het doel van het tevreden-type van Sensor filtrerende vermogen is de behoefte te elimineren om informatie op te slaan en te verwerken die niet nuttig voor analysedoeleinden is.

Veel van het verzoekgegeven dat door API van een Webserver beschikbaar is is niet nuttig in bedrijfsanalyse. Opslag en verwerking zijn duur en het [!DNL Sensor’s] tevreden-type filtreren staat u toe om onnodige opslag en verwerking te vermijden.

Om de prestaties van de gegevensverwerking van het Weblogboek te maximaliseren en de hoeveelheid meetgegevens te verminderen die moeten worden opgeslagen, [!DNL Site] [!DNL Sensor]verwerft meetgegevens (verzoekgegevens, logboekingangen, logboekgegevens, etc.) voor alle Web content-type verzoeken, behalve specifiek vermelde inhoudstypes (zoals het draperen van stijlbladen, beeldverzoeken, etc.), die uit worden gefiltreerd alvorens zij aan de server van de gegevenswerkbank door worden overgebracht. Dit filtreren kan voor een volledige Webserver worden onbruikbaar gemaakt, en het kan ook voor een bepaald inhoudsvoorwerp worden met voeten getreden door het naam-waarde paar &quot;Log=1&quot;aan het vraagkoord van een bepaald ingebed voorwerp (bijvoorbeeld, [!DNL http://www.mysite.com/advertisement.gif?Log=1]) toe te voegen.
