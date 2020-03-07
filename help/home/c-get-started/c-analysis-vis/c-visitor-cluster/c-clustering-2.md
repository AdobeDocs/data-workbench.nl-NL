---
description: De Bouwer van de Cluster omvat nu een KMeans++ algoritme (slechts werd het algoritme KMeans eerder gesteund) dat een snellere benadering gebruikt om centra voor een versneld cluster-generatieproces te vinden.
title: Clustering 2.0
uuid: 14462bd3-06d1-4622-a2d8-f96aadb357f3
translation-type: tm+mt
source-git-commit: cb3ca4b3b993f5f04f6b6cee25850600ff3d8986

---


# Clustering 2.0{#clustering}

De Bouwer van de Cluster omvat nu een KMeans++ algoritme (slechts werd het algoritme KMeans eerder gesteund) dat een snellere benadering gebruikt om centra voor een versneld cluster-generatieproces te vinden.

## KMeans-algoritmen {#section-92383a1be1d6402c95a25c902e90b850}

In de Bouwer [van de](https://docs.adobe.com/help/en/data-workbench/using/client/analysis-visualizations/visitor-cluster/c-visitor-cluster.html)Cluster, kunt u **[!UICONTROL Options]** > nu selecteren **[!UICONTROL Algorithm]** om algoritmen te selecteren wanneer het bepalen van clusters.

* **[!UICONTROL KMeans]**. Dit algoritme gebruikt canopy zich groeperen om de centra van de cluster te bepalen.
* **[!UICONTROL KMeans++]**. Dit algoritme bevordert clusterbouw wanneer het lopen tegen grote reeksen gegevens.

<!-- <a id="section_8193A6D60C5540BB985085BE670B4544"></a> -->

KMeans++ is een betere implementatie van KMeans die algoritme groeperen omdat het betere initialisering van aanvankelijke k- centra verstrekt. (Het oorspronkelijke KMeans algoritme kiest willekeurig aanvankelijke centra.) KMeans++ selecteert het eerste centrum willekeurig. De resterende k-1 centra zullen één voor één worden gekozen gebaseerd op de afstand een gegevenspunt aan het dichtste bestaande centrum is. De verste gegevenspunten hebben een betere kans om als nieuw centrum te worden gekozen dan nabijgelegen gegevenspunten. Nadat het aanvankelijke centrum wordt gekozen, wordt de procedure uitgevoerd precies het zelfde als het originele KMeans groeperen zich.

Het werkschema voor KMeans++ is precies het zelfde als het werkschema voor KMeans zich groeperen, behalve dat moet u **Opties** > **Algoritme** > **KMeans++** in de clusteraannemer selecteren.

>[!NOTE]
>
>Elke DPU stelt zijn eigen procedure KMeans++ op zijn eigen gegevensgedeelte in werking. Als DPU genoeg beschikbaar geheugen (de verhouding is configureerbaar in het PAServer.cfg- dossier) heeft, dan zullen de gegevens van die betrokken variabelen in geheugen worden gebracht. De resterende k-1 aanvankelijke centrumselectie en convergerende herhalingen gebeuren allemaal in geheugen, dat sneller is dan de vorige KMeans zich groeperen.

