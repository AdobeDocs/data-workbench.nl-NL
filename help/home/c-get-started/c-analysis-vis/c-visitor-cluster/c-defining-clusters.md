---
description: Selecteer inputvariabelen, het aantal clusters, en een doelpopulatie (indien gewenst) om clusters in uw dataset te bepalen.
solution: Analytics
title: Clusters bouwen
topic: Data workbench
uuid: f8462445-b7d2-48ae-aed7-2a3abc491cfb
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Clusters bouwen{#building-clusters}

Selecteer inputvariabelen, het aantal clusters, en een doelpopulatie (indien gewenst) om clusters in uw dataset te bepalen.

**Clusters bouwen**

1. Open de **[!UICONTROL Cluster Builder]**.

   Klik op **Visualisatie** > **Predictive Analytics** > **Clustering** > **Cluster Builder**.

   ![](assets/cluster-builder-step1.png)

1. Selecteer inputvariabelen.

   * Voeg metriek aan de **[!UICONTROL Input Variables]** lijst toe door van het **[!UICONTROL Metric]** menu in de toolbar te selecteren.

      ![](assets/cluster_metric_select.png)

   * Voeg afmetingselementen aan de **[!UICONTROL Input Variables]** lijst toe door hen van de lijst van een Dimensie te slepen.

      De pers **[!UICONTROL Ctrl + Alt]** en sleept geselecteerde afmetingselementen aan de **[!UICONTROL Input Variables]** lijst of aan de **[!UICONTROL Element]** doos in de toolbar.

      ![](assets/cluster_dim_select.png)
   Door gebrek, wordt het groeperen uitgevoerd op de volledige dataset. U kunt alle inputvariabelen in de linkerruit zien. **[!UICONTROL Preprocessing]**
1. Gebruik het **[!UICONTROL Options]** menu om het gewenste aantal clusters te selecteren.

   ![](assets/build_cluster_2.png)

1. Als u een ondergroep van de Bezoekers in uw dataset wilt groeperen, kunt u een Filter van de Bevolking bepalen.

   ![](assets/build_cluster_3.png)

   Begin door de gewenste ondergroep te bepalen gebruikend selecties in uw Werkruimte of door te gebruiken **[!UICONTROL Filter Editor]**. Zodra u de gewenste geselecteerde ondergroep hebt, plaats de Bevolking van het Doel in het **[!UICONTROL Options]** menu. Men adviseert dat u de gerichte groep een identificatienaam geeft.

   Het **[!UICONTROL Options]** menu heeft ook montages om het maximumaantal passen en de aanvaardbare drempel voor centrumconvergentie te controleren.

1. Nadat de input en de opties zijn gevormd, klik de **Go** knoop om het groeperen plaatselijk in werking te stellen of te drukken **[!UICONTROL Submit]** om de taak naar de Predictive Server van de Analyse te verzenden. De voorlegging aan de server zal de resulterende afmeting aan de dataset bewaren wanneer de convergentie volledig is.

   Wanneer het lopen plaatselijk, zult u de beweging van de Bouwer van de Cluster door vier boomcultuur zien die stadia groeperen aangezien het intelligente centra bepaalt die op de input worden gebaseerd.

   Zodra de centra van de clusters ophouden veranderend meer dan de gespecificeerde convergentiedrempel, wordt de Dimensie van de Cluster samengekomen en de vertoningen van de Bouwer van de Cluster extra informatie over hoe relevant een input aan elke cluster was.

1. Pas de clusters aan.

   Het met de rechtermuisknop klikken op de de kleurenbar van statistieken opent een contextmenu dat u toestaat om de relevantiedrempels aan te passen, en in het geval van de verdelingen van het afmetingselement, om te kiezen welke test wordt getoond.

   ![](assets/build_cluster_7.png)

   De metrische input verstrekt een t-test voor elke cluster, terwijl de input van het afmetingselement drie distributietests (Chi kwadraat, een entropy U- statistiek, en Cramer&#39;s V- statistiek) voor elke cluster verstrekt.

   >[!NOTE]
   >
   >Als u toevoegt of input tijdens convergentie verwijdert, zal het proces pauzeren tot u **Go** opnieuw drukt.

   Na het bouwen van clusters, kunt u de kleurenplukker openen om kleuren voor verschillende distributieresultaten toe te wijzen.

   ![](assets/build_cluster_5.png)

1. Met de geconvergeerde Dimensie van de Cluster, kunt u metriek aan de lijst toevoegen en selecties maken zoals normaal. U kunt ook op de elementennamen (Cluster 1, Cluster 2, enz.) met de rechtermuisknop klikken om het contextmenu te openen om hen aan iets zinvoller anders te noemen.

   ![](assets/build_cluster_6.png)

1. Als u wenst om deze clusterdimensie in andere visualisaties te gebruiken, kunt u het plaatselijk of **[!UICONTROL Save]** **[!UICONTROL Submit]** het aan de server gebruiken.

Als u wenst om convergentie opnieuw in werking te stellen of de relevantie van input te zien, kan de Bouwer van de Cluster bestaande clusterdimensies ook laden.

>[!TIP]
>
>Wanneer geselecteerd, **[!UICONTROL Reset]** zal volledig alle inputvariabelen vrijgeven en zal u een lege visualisatie van de clusterbouwer geven om nieuwe clusters te bepalen.

