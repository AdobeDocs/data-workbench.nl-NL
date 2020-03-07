---
description: Conceptuele informatie over ondergroepen.
solution: Analytics
title: Ondergroepen begrijpen
topic: Data workbench
uuid: ed185b63-dbb3-4ed4-9403-cf4dc8be2ff1
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Ondergroepen begrijpen{#understanding-subsets}

Conceptuele informatie over ondergroepen.

Wanneer het gebruiken van een ondergroep, te houden gelieve de volgende dingen in mening:

* Al uw benchmarks hebben nu betrekking op uw subset, niet op de volledige dataset, die veel nuttiger is bij het analyseren van een specifieke subset. Zie Benchmarks [begrijpen](../../../../home/c-get-started/c-vis/c-ustd-benchmks.md#concept-c7b0f4102e92458096f8c4765cbe2914).
* Het gebruiken van een ondergroep beïnvloedt elk van uw werkruimten omdat de ondergroep globaal op de Werkbank van Gegevens wordt toegepast.
* De ondergroepen beïnvloeden slechts metriek en denormale afmetingen, niet normale afmetingen.
* Wanneer het gebruiken [!DNL Report], beïnvloeden de ondergroepen niet de gegevens in rapporten die voor anderen aan mening worden gepubliceerd.
* Zodra toegepast, is uw ondergroep in feite voor al verder werk in het profiel, met inbegrip van de volgende tijd dat u deze instantie van de Werkbank van Gegevens opent, tot u het verwijdert.
* De enige plaats die erop wijst dat een ondergroep is toegepast is het contextmenu dat u door binnen een werkruimte met de rechtermuisknop aan te klikken bereikt.

   ![](assets/mnu_Subset.png)

* U moet online werken om een ondergroep te veranderen of te verwijderen. Als u offline werkt en een ondergroep hebt toegepast, kunt u geen resultaten van de volledige dataset bekijken. Zie Offline en online [werken](../../../../home/c-get-started/c-off-on.md#concept-cef8758ede044b18b3558376c5eb9f54).

   >[!NOTE]
   >
   >De grootte van uw ondergroep is beperkt tot de hoeveelheid gegevens in uw filter die op één enkele server van de Werkbank van Gegevens verblijft. Daarom als uw dataset een de servercluster van de Werkbank van Gegevens overspant, komen de gegevens voor uw ondergroep uit slechts één server van de Werkbank van Gegevens in de cluster.

Een gebruiker bij een grote detailhandelaar wil een ondergroep (lokaal geheime voorgeheugen) van één bepaalde het werkweek van gegevens tot stand brengen en dan vragen in werking stellen slechts op die week van gegevens. Om dit te doen, leidt de gebruiker tot een ondergroep voor de dagen van belang.

Het volgende voorbeeld toont u een bargrafiek van Bezoekers in tijd en een metrische legende van het Verkeer. Het eerste cijfer bevat geen selecties: alle gegevens in de dataset worden vertegenwoordigd. Het tweede cijfer toont gegevens voor een ondergroep van Dagen = {...} door Bezoekers, waarin de Dagen op een selectie van de elementen 1 april door 5 april in de dimensie van de Dag gebaseerd is.

![](assets/client-sub1.png)

