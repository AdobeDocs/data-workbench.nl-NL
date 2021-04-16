---
description: Conceptuele informatie over subsets.
title: Subsets begrijpen
uuid: ed185b63-dbb3-4ed4-9403-cf4dc8be2ff1
exl-id: a75b36f9-d34d-4a4a-8a2c-15ae5461823c
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '333'
ht-degree: 0%

---

# Subsets{#understanding-subsets}

Conceptuele informatie over subsets.

Houd rekening met het volgende wanneer u een subset gebruikt:

* Al uw benchmarks hebben nu betrekking op uw subset, niet op de gehele dataset, die veel nuttiger is wanneer het analyseren van een specifieke subset. Zie [Benchmarks](../../../../home/c-get-started/c-vis/c-ustd-benchmks.md#concept-c7b0f4102e92458096f8c4765cbe2914) begrijpen.
* Het gebruik van een subset is van invloed op al uw werkruimten, omdat de subset globaal wordt toegepast op de Data Workbench.
* Subsets hebben alleen invloed op metrieke en denormale afmetingen, niet op normale afmetingen.
* Als u [!DNL Report] gebruikt, hebben subsets geen invloed op de gegevens in rapporten die worden gepubliceerd voor anderen om deze te bekijken.
* Nadat de subset is toegepast, geldt deze voor alle volgende bewerkingen in het profiel, inclusief de volgende keer dat u deze instantie van Data Workbench opent, totdat u deze verwijdert.
* De enige plaats die erop wijst dat een ondergroep is toegepast is het contextmenu dat u door binnen een werkruimte met de rechtermuisknop te klikken bereikt.

   ![](assets/mnu_Subset.png)

* U moet online werken om een subset te wijzigen of te verwijderen. Als u offline werkt en een subset hebt toegepast, kunt u de resultaten van de gehele gegevensset niet weergeven. Zie [Offline werken en Online](../../../../home/c-get-started/c-off-on.md#concept-cef8758ede044b18b3558376c5eb9f54).

   >[!NOTE]
   >
   >De grootte van de subset is beperkt tot de hoeveelheid gegevens in het filter dat zich op één Data Workbench-server bevindt. Daarom als uw dataset een de servercluster van de Data Workbench overspant, komen de gegevens voor uw ondergroep uit slechts één server van de Data Workbench in de cluster.

Een gebruiker bij een grote detailhandelaar wil een ondergroep (lokaal geheime voorgeheugen) van één bepaalde het werkweek van gegevens tot stand brengen en dan vragen slechts op die week van gegevens in werking stellen. Hiervoor maakt de gebruiker een subset voor de dagen van interesse.

Het volgende voorbeeld toont u een staafgrafiek van Bezoekers in tijd en een metrische legenda van het Verkeer. De eerste afbeelding bevat geen selecties: alle gegevens in de gegevensset worden vertegenwoordigd. In de tweede figuur worden gegevens weergegeven voor een subset van Dagen = {...} door bezoekers, waarbij Dagen gebaseerd is op een selectie van de elementen 1 april tot en met 5 april in de dimensie Dag.

![](assets/client-sub1.png)
