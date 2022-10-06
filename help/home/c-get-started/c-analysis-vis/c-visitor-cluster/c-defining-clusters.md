---
description: Selecteer inputvariabelen, het aantal clusters, en een doelpopulatie (indien gewenst) om clusters in uw dataset te bepalen.
title: Clusters samenstellen
uuid: f8462445-b7d2-48ae-aed7-2a3abc491cfb
exl-id: 60bc75bf-2f89-455b-8be9-aa20bb837752
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '508'
ht-degree: 0%

---

# Clusters samenstellen{#building-clusters}

{{eol}}

Selecteer inputvariabelen, het aantal clusters, en een doelpopulatie (indien gewenst) om clusters in uw dataset te bepalen.

**Clusters samenstellen**

1. Open de **[!UICONTROL Cluster Builder]**.

   Klikken **Visualisatie** > **Predictieve analyse** > **Clustering** > **Cluster Builder**.

   ![](assets/cluster-builder-step1.png)

1. Selecteer invoervariabelen.

   * Metrische gegevens toevoegen aan de **[!UICONTROL Input Variables]** lijst door uit de lijst te selecteren **[!UICONTROL Metric]** op de werkbalk.

      ![](assets/cluster_metric_select.png)

   * Dimensie-elementen toevoegen aan de **[!UICONTROL Input Variables]** lijst door hen van een Dimension te slepen.

      Druk **[!UICONTROL Ctrl + Alt]** en sleep geselecteerde dimensie-elementen naar de **[!UICONTROL Input Variables]** of de **[!UICONTROL Element]** in de werkbalk.

      ![](assets/cluster_dim_select.png)
   Door gebrek, wordt het groeperen uitgevoerd op de volledige dataset. Alle invoervariabelen worden links weergegeven **[!UICONTROL Preprocessing]** venster.
1. Gebruik de **[!UICONTROL Options]** om het gewenste aantal clusters te selecteren.

   ![](assets/build_cluster_2.png)

1. Als u een ondergroep van de Bezoekers in uw dataset wilt groeperen, kunt u een Filter van de Bevolking bepalen.

   ![](assets/build_cluster_3.png)

   Begin door de gewenste ondergroep te bepalen gebruikend selecties in uw Werkruimte of door te gebruiken **[!UICONTROL Filter Editor]**. Als u de gewenste subset hebt geselecteerd, stelt u de doelpopulatie in het dialoogvenster **[!UICONTROL Options]** -menu. U wordt aangeraden de doelgroep een identificatienaam te geven.

   De **[!UICONTROL Options]** menu heeft ook instellingen om het maximumaantal controles en de aanvaardbare drempel voor centrumconvergentie te bepalen.

1. Nadat de input en de opties zijn gevormd, klik **Ga** knoop om het groeperen plaatselijk in werking te stellen of druk **[!UICONTROL Submit]** om de taak naar de Predictive Analytics Server te verzenden. De voorlegging aan de server zal de resulterende afmeting aan de dataset bewaren wanneer de convergentie volledig is.

   Wanneer het lopen plaatselijk, zult u de Bouwer van de Cluster door vier kanopie zich groeperende stadia zien aangezien het intelligente centra bepaalt die op de input worden gebaseerd.

   Zodra de centra van de clusters ophouden veranderend meer dan de gespecificeerde convergentiedrempel, wordt de Dimension van de Cluster samengekomen en de Bouwer van de Cluster toont extra informatie over hoe relevant een input aan elke cluster was.

1. Pas de clusters aan.

   Als u met de rechtermuisknop op de kleurenbalk van de statistiek klikt, wordt een contextmenu geopend waarin u de relevantiedrempels kunt aanpassen. In het geval van de distributies van het dimensie-element kunt u kiezen welke test wordt weergegeven.

   ![](assets/build_cluster_7.png)

   De metrische input verstrekt t-test voor elke cluster, terwijl de metingselementinput drie distributietests (Chi kwadraat, een entropie U statistiek, en de V statistiek van Cramer) voor elke cluster verstrekt.

   >[!NOTE]
   >
   >Als u input tijdens convergentie toevoegt of verwijdert, zal het proces pauzeren tot u drukt **Ga** opnieuw.

   Nadat u clusters hebt gemaakt, kunt u de kleurkiezer openen om kleuren toe te wijzen voor verschillende distributieresultaten.

   ![](assets/build_cluster_5.png)

1. Met de Dimension van de Cluster samengekomen, kunt u metriek aan de lijst toevoegen en selecties maken zoals normaal. U kunt ook met de rechtermuisknop op de elementnamen (Cluster 1, Cluster 2, enz.) klikken om het contextmenu te openen en de naam van de elementen te wijzigen in iets wat zinvoller is.

   ![](assets/build_cluster_6.png)

1. Als u deze clusterdimensie in andere visualisaties wilt gebruiken, kunt u **[!UICONTROL Save]** lokaal of **[!UICONTROL Submit]** naar de server.

Als u convergentie wilt opnieuw in werking stellen of de relevantie van input zien, kan de Bouwer van de Cluster bestaande clusterdimensies ook laden.

>[!TIP]
>
>Wanneer geselecteerd, **[!UICONTROL Reset]** geeft alle invoervariabelen volledig vrij en geeft u een lege clusterbouwer visualisatie om nieuwe clusters te bepalen.
