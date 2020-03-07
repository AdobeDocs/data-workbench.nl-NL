---
description: Conceptuele informatie over vraag modelcomponenten.
solution: Analytics
title: Modelonderdelen voor zoekopdrachten
topic: Data workbench
uuid: 708fab0b-dc10-4306-b410-49268069ac3b
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Modelonderdelen voor zoekopdrachten{#query-model-components}

Conceptuele informatie over vraag modelcomponenten.

Het volgende cijfer toont een gebiedsdeelkaart de waarvan knopen de metriek van een vraagmodel, afgeleide afmetingen, en filters vertegenwoordigen die in de Afmetingen, de Metriek, en de omslagen van Filters binnen het profiel evenals de uitgebreide afmetingen worden bepaald die in de dataset worden bepaald die op één of andere manier op hen betrekking hebben.

![](assets/vis_DependencyMap_QueryModel.png)

* Een geel-groene knoop vertegenwoordigt een filter.
* Een paarse knoop vertegenwoordigt metrisch.
* Een blauw-groene knoop vertegenwoordigt een afgeleide afmeting.
* Een groene knoop vertegenwoordigt een uitgebreide dimensie (die in de dataset wordt bepaald).
* Een rode knoop vertegenwoordigt metrisch, een afgeleide afmeting, of een filter met een gebroken of cirkelgebiedsdeel of een andere fout.

>[!NOTE]
>
>Omdat de gebiedsdeelkaart wordt ontworpen om acyclische gebiedsdelen aan te passen, kunnen de knopen betrokken bij cirkelgebiedsdelen niet behoorlijk op de kaart tonen. U kunt naar cirkelgebiedsdelen zoeken door &quot;cirkelgebiedsdeel&quot;in het [!DNL Search] tekstvakje te typen. Voor meer informatie over de [!DNL Search] eigenschap, zie het [Zoeken binnen een Kaart](../../../../../home/c-get-started/c-admin-intrf/c-dataset-mgrs/c-dep-maps/t-srch-map.md#task-a1e7065a538d46c78a7d28676d880dfb).

