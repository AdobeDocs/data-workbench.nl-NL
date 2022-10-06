---
description: Conceptuele informatie over de componenten van het vraagmodel.
title: Componenten van query-modellen
uuid: 708fab0b-dc10-4306-b410-49268069ac3b
exl-id: 1f5d0a3a-6647-4762-ab20-9d80e467d48f
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 0%

---

# Componenten van query-modellen{#query-model-components}

{{eol}}

Conceptuele informatie over de componenten van het vraagmodel.

Het volgende cijfer toont een gebiedsdeelkaart de waarvan knopen de metriek van een vraagmodel, afgeleide dimensies, en filters vertegenwoordigen die in de Dimension, Metriek, en de omslagen van Filters binnen het profiel worden bepaald evenals de uitgebreide dimensies die in de dataset worden bepaald die op hen op één of andere manier betrekking hebben.

![](assets/vis_DependencyMap_QueryModel.png)

* Een geel-groene knoop vertegenwoordigt een filter.
* Een paarse knoop vertegenwoordigt metrisch.
* Een blauw-groene knoop vertegenwoordigt een afgeleide dimensie.
* Een groene knoop vertegenwoordigt een uitgebreide dimensie (die in de dataset wordt bepaald).
* Een rode knoop vertegenwoordigt metrische, afgeleide afmeting, of filter met gebroken of cirkelgebiedsdeel of een andere fout.

>[!NOTE]
>
>Omdat de gebiedsdeelkaart wordt ontworpen om acyclische gebiedsdelen aan te passen, kunnen de knopen betrokken bij cirkelgebiedsdelen niet behoorlijk op de kaart tonen. U kunt naar kringafhankelijkheden zoeken door &quot;kringafhankelijkheden&quot; te typen in het dialoogvenster [!DNL Search] tekstvak. Voor meer informatie over de [!DNL Search] functie, zie [Zoeken binnen een kaart](../../../../../home/c-get-started/c-admin-intrf/c-dataset-mgrs/c-dep-maps/t-srch-map.md#task-a1e7065a538d46c78a7d28676d880dfb).
