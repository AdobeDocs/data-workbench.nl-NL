---
description: De lijsten van het detail laten u toe om extra informatie over een ondergroep van gegevens te bekijken, die door de selecties wordt bepaald die u in andere visualisaties maakt.
solution: Analytics
title: Details tabel
topic: Data workbench
uuid: 2becff5e-c78d-4ac7-8cda-814ad0193efd
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Details tabel{#detail-table}

De lijsten van het detail laten u toe om extra informatie over een ondergroep van gegevens te bekijken, die door de selecties wordt bepaald die u in andere visualisaties maakt.

De extra informatie die u ziet is een steekproef van alle beschikbare gegevens.

![](assets/vis_details.png)

De volgende lijst beschrijft de elementen van een detaillijst.

<table id="table_C88C7F7F5AEA4820B908923E45CC0A62"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Element </th> 
   <th colname="col02" class="entry"> Kleur </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Niveau </p> </td> 
   <td colname="col02"> <p>Roze </p> </td> 
   <td colname="col2"> <p>Om het even welke telbare afmeting waarvoor u gedetailleerde attributen en metrische informatie wilt bekijken. Het niveau wordt voorafgegaan door het aantal elementen dat uit het aantal beschikbare elementen wordt getoond, bijvoorbeeld wijst 6/444 erop dat 6 elementen uit een mogelijke 444 worden getoond. In het voorbeeld hierboven, wijst de niveauBezoekers erop dat alle verstrekte detail op bezoeker gebaseerd is. De meningen van de niveaupagina wijzen erop dat alle verstrekte detail op paginamening gebaseerd is. Het bekijken van veelvoudige niveaus tezelfdertijd is nuttig wanneer u gegevens wilt analyseren die verschillende telbare ouders hebben. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Attribuut </p> </td> 
   <td colname="col02"> <p>Groen </p> </td> 
   <td colname="col2"> <p>Om het even welke dimensie die één-aan-velen of één-aan-één met het niveau is, zoals Stad aan Bezoekers. Elke rij toont het element met betrekking tot elk element van het niveau u selecteerde. In het voorbeeld hierboven, maken een lijst van de attributen van het Domein en van de Stad van het domein en de stad voor elk van de steekproefbezoekers een lijst. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Metrisch </p> </td> 
   <td colname="col02"> <p>Blauw </p> </td> 
   <td colname="col2"> <p>Metrische details over het geselecteerde niveau. In het voorbeeld hierboven, met het niveau dat aan Bezoekers wordt geplaatst, tonen de metrische Meningen van de Pagina het aantal paginameningen voor een individuele bezoeker, terwijl het niveau van de Meningen van de Pagina het detail over elk van die paginameningen verstrekt. </p> </td> 
  </tr> 
 </tbody> 
</table>

Laten wij zeggen u met websitegegevens werkt en wilt te weten komen welke pagina&#39;s bezoekers in bepaalde steden en van bepaalde domeinen bezocht tijdens een bepaald tijdkader.

Eerst moet u een visualisatie tot stand brengen die het tijdkader toont waarin u geinteresseerd bent, dan moet u dat tijdkader selecteren. Nu kunt u een detaillijst toevoegen om de gewenste details voor een steekproefaantal bezoekers in de dataset te bekijken.

Om de hierboven beschreven details te bekijken, moet u de volgende stappen uitvoeren:

1. Klik binnen de detailslijst met de rechtermuisknop aan en klik **[!UICONTROL Add Level]** > **[!UICONTROL Visitor]**.
1. Klik binnen de detailslijst met de rechtermuisknop aan en klik **[!UICONTROL Add Level]** > **[!UICONTROL Page View]**.
1. Klik de **[!UICONTROL Visitors]** niveaurubriek met de rechtermuisknop aan en klik **[!UICONTROL Add Attribute]** > **[!UICONTROL Geography]** > **[!UICONTROL Domain]**.
1. Klik binnen de het niveaurubriek van Bezoekers met de rechtermuisknop aan en klik **[!UICONTROL Add Attribute]** > **[!UICONTROL Geography]** > **[!UICONTROL City]**.
1. Klik binnen de het niveaurubriek van Bezoekers met de rechtermuisknop aan en klik **[!UICONTROL Add Metric]** > **[!UICONTROL Page Views]**.
1. Klik binnen de het niveaurubriek van de Meningen van de Pagina met de rechtermuisknop aan en klik **[!UICONTROL Add Attribute]** > **[!UICONTROL Page]** > **[!UICONTROL Page]**.

De volgende steekproefwerkruimte toont u de verwante details voor een willekeurige steekproef van zes bezoekers aan de plaats tijdens het tijdkader u specificeerde.

![](assets/client-tab1.png)

## Een niveau toevoegen {#section-f948d3361fd84906ac4d9ebce520bfd0}

* Klik binnen de detaillijst met de rechtermuisknop aan en klik **[!UICONTROL Add Level]** > *&lt;**[!UICONTROL dimension name]**>*.

![](assets/mnu_DetailsTable_AddLevel.png)

## Niveau verwijderen {#section-a8c820e0b656451e98e5ea75373edefc}

* Klik de bestaande niveaurubriek met de rechtermuisknop aan en klik **[!UICONTROL Remove Level]** > *&lt;**[!UICONTROL dimension name]**>*.

![](assets/mnu_DetailsTable_Level.png)

## Eigenschappen en maatstaven toevoegen {#section-cdda2df3c9a448d5b9770686c8b8efb3}

* Klik een attribuut of metrische rubriek met de rechtermuisknop aan en klik **[!UICONTROL Add Attribute]** > *&lt;**[!UICONTROL attribute name]**>* of **[!UICONTROL Add Metric]** > *&lt;**[!UICONTROL metric name]**>*.

![](assets/mnu_DetailsTable.png)

## Eigenschappen en waarden verwijderen {#section-4002ac957a2846678f9940270987d651}

* Klik met de rechtermuisknop op de kolom die u wilt verwijderen en klik op **[!UICONTROL Remove Attribute]** > *&lt;**[!UICONTROL attribute name]**>* of **[!UICONTROL Remove Metric]** > *&lt;**[!UICONTROL metric name]**>*.

![](assets/mnu_DetailsTable.png)

## Exporteren naar Microsoft Excel {#section-a9eaba63c88a4598836a34669ba8cac1}

Voor informatie over het uitvoeren van vensters, zie het [Uitvoeren van de Gegevens](../../../home/c-get-started/c-wk-win-wksp/c-exp-win-data.md#concept-8df61d64ed434cc5a499023c44197349)van het Venster.
