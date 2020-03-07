---
description: Binnen een werkruimte, vertegenwoordigt een visualisatie een reeks vraagresultaten.
solution: Analytics
title: Begrijpend hoe een Selectie Andere Visualisaties beïnvloedt
topic: Data workbench
uuid: d46f4e8d-df6f-4a7f-a796-eb9f11536ae5
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Begrijpend hoe een Selectie Andere Visualisaties beïnvloedt{#understanding-how-a-selection-affects-other-visualizations}

Binnen een werkruimte, vertegenwoordigt een visualisatie een reeks vraagresultaten.

Wanneer u een selectie maakt, de filters van de Werkbank van Gegevens de resultaten van de vragen die het gebruikt om de visualisaties in de werkruimte te veroorzaken. De specifieke filter varieert door visualisatie.

De volgende voorbeelden illustreren hoe de Werkbank van Gegevens een selectie op drie verschillende soorten visualisaties toepast. Het herzien van deze voorbeelden helpt u het het filtreren effect begrijpen dat de selecties op visualisaties hebben. Zij helpen u ook begrijpen hoe te om de resultaten te interpreteren die u in een gefiltreerde visualisatie ziet.

* [Het filtreren van een Visualisatie met een Metrische Zittingen](../../../../home/c-get-started/c-vis/c-sel-vis/c-sel-aff-vis.md#section-7cc06493ecb34cd4a696dbf0f0a7aaef)
* [Een visualisatie filteren met een metrische bezoeker](../../../../home/c-get-started/c-vis/c-sel-vis/c-sel-aff-vis.md#section-97d38c7f03e8457189a9c72d69514ed2)
* [Het filtreren van een Visualisatie met een Bezoeker-door-Zitting Metrische](../../../../home/c-get-started/c-vis/c-sel-vis/c-sel-aff-vis.md#section-f746182311d648dcb98716b0fe846e25)

## Het filtreren van een Visualisatie met een Metrische Zittingen {#section-7cc06493ecb34cd4a696dbf0f0a7aaef}

In dit voorbeeld, filtreert [!DNL /direct.asp/?ldPage=hme] URI in de visualisatie op de linkerzijde metrisch voor Zittingen die in de visualisatie op het recht worden getoond.

![](assets/client-vis1.png)

* **Effect van Selectie op de Vraag:** De Werkbank van gegevens filters de Zittingen voor geselecteerd URI. In dit voorbeeld, wordt de vraag die de waarde voor het [!DNL /pops/disclosure_pop.asp] element produceert gefiltreerd als volgt:

   ```
   Sessions[ URI="/pops/disclosure_pop.asp" AND URI="/direct.asp
   /?ldPage=hme"] by Page View by Session
   ```

* **Het interpreteren van de Visualisatie:** De gefiltreerde visualisatie vertegenwoordigt het aantal Zittingen die URIs omvatten die in de visualisatie en [!DNL /direct.asp/?ldPage=hme]worden vermeld. Dit voorbeeld toont aan dat er 1.113 zittingen waren waarin de bezoekers zowel [!DNL /pops/disclosure_pop.asp] pagina als [!DNL /direct.asp/?ldPage=hme] in de zelfde zitting bekeken.

## Een visualisatie filteren met een metrische bezoeker {#section-97d38c7f03e8457189a9c72d69514ed2}

In dit voorbeeld, filtreert [!DNL /direct.asp/?ldPage=home] URI in de visualisatie op de linkerzijde metrisch voor Bezoekers in de visualisatie op het recht.

![](assets/client-vis2.png)

* **Effect van Selectie op de Vraag:** De Werkbank van gegevens filters de Bezoekers voor geselecteerde URI. In dit voorbeeld, wordt de vraag die de waarde voor [!DNL /pops/disclosure_pop.asp] URI produceert gefiltreerd als volgt:

   ```
   Visitors[ URI="/pops/disclosure_pop.asp" by Page View by Visitor 
     AND URI="/direct.asp/?ldPage=hme" by Page View by Visitor ]
   ```

* **Het interpreteren van de Visualisatie:** De gefiltreerde visualisatie toont de Bezoekers die URIs hebben bekeken die in de visualisatie en [!DNL /direct.asp/?ldPage=hme] (hoewel niet noodzakelijk tijdens de zelfde zitting) worden vermeld. Uit het bovenstaande voorbeeld blijkt dat 2.041 bezoekers zowel [!DNL /pops/disclosure_pop.asp] als [!DNL /direct.asp/?ldPage=hme]hebben gezien.

## Het filtreren van een Visualisatie met een Bezoeker-door-Zitting Metrische {#section-f746182311d648dcb98716b0fe846e25}

In dit voorbeeld, filtreert [!DNL /direct.asp/?ldPage=hme] URI in de visualisatie op de linkerzijde metrisch voor bezoeker-door-zitting in de visualisatie op het recht.

![](assets/client-vis3.png)

* **Effect van Selectie op de Vraag:** De Werkbank van gegevens filters de Bezoekers door Zitting voor geselecteerde URI. Bijvoorbeeld, wordt de vraag die de waarde voor [!DNL /pops/disclosure_pop.asp] URI produceert gefiltreerd als volgt:

   ```
   Visitors[ ( URI="/pops/disclosure_pop.asp" by Page View 
     AND URI="/direct.asp/?ldPage=hme" by Page View ) by Session ]
   ```

* **Het interpreteren van de Visualisatie:** De gefiltreerde visualisatie toont de Bezoekers die beide URIs hebben bekeken die in de visualisatie en [!DNL /direct.asp/?ldPage=hme] tijdens de zelfde zitting worden vermeld. Dit voorbeeld toont aan dat 1.069 bezoekers zowel [!DNL /pops/disclosure_pop.asp] als [!DNL /direct.asp/?ldPage=hme] tijdens één enkele zitting zagen.

