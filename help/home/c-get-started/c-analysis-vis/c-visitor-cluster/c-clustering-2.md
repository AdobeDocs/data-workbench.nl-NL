---
description: Cluster Builder bevat nu een algoritme KMeans++ (alleen het algoritme KMeans werd eerder ondersteund) dat een snellere benadering gebruikt om centra te zoeken voor een versneld clustergeneratieproces.
title: Clustering 2.0
uuid: 14462bd3-06d1-4622-a2d8-f96aadb357f3
exl-id: 6a779ddc-c8f1-4c55-9c17-1119fe1aa791
source-git-commit: 050468bf6a9ef9c07719ded79c8ab68753d58647
workflow-type: tm+mt
source-wordcount: '288'
ht-degree: 0%

---

# Clustering 2.0{#clustering}

Cluster Builder bevat nu een algoritme KMeans++ (alleen het algoritme KMeans werd eerder ondersteund) dat een snellere benadering gebruikt om centra te zoeken voor een versneld clustergeneratieproces.

## KMeans-algoritmen {#section-92383a1be1d6402c95a25c902e90b850}

In [Cluster Builder](https://experienceleague.adobe.com/docs/data-workbench/using/client/analysis-visualizations/visitor-cluster/c-visitor-cluster.html?lang=en) kunt u **[!UICONTROL Options]** > **[!UICONTROL Algorithm]** nu selecteren om algoritmen te selecteren wanneer het bepalen van clusters.

* **[!UICONTROL KMeans]**. Dit algoritme gebruikt kanopy zich groeperen om de centra van de cluster te bepalen.
* **[!UICONTROL KMeans++]**. Dit algoritme versnelt het bouwen van clusters wanneer het lopen tegen grote reeksen gegevens.

<!-- <a id="section_8193A6D60C5540BB985085BE670B4544"></a> -->

KMeans++ is een betere implementatie van het KMeans groeperend algoritme omdat het betere initialisering van aanvankelijke k centra verstrekt. (Het oorspronkelijke algoritme KMeans kiest willekeurig aanvankelijke centra.) Met KMeans++ wordt het eerste middelpunt willekeurig geselecteerd. De resterende k-1 centra zullen één voor één worden gekozen gebaseerd op de afstand een gegevenspunt aan het dichtstbijzijnde bestaande centrum is. De verst mogelijke gegevenspunten hebben een betere kans om als nieuw centrum te worden gekozen dan nabijgelegen gegevenspunten. Nadat het aanvankelijke centrum wordt gekozen, wordt de procedure uitgevoerd precies het zelfde als oorspronkelijke KMeans zich groeperen.

De werkstroom voor KMeans++ is precies het zelfde als de werkschema voor KMeans groeperen, behalve dat moet u **Opties** > **Algorithm** > **KMeans++** in de clusteraannemer selecteren.

>[!NOTE]
>
>Elke DPU stelt zijn eigen KMeans++ procedure op zijn eigen gegevensgedeelte in werking. Als DPU genoeg beschikbaar geheugen (de verhouding is configureerbaar in het PAServer.cfg- dossier) heeft, dan zullen de gegevens van die betrokken variabelen in geheugen worden gebracht. De resterende k-1 initiële centrumselectie en convergerende herhalingen gebeuren allemaal in het geheugen, wat sneller is dan de vorige KMeans zich groeperen.
