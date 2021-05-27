---
description: Met detailtabellen kunt u aanvullende informatie over een subset gegevens weergeven. Deze informatie wordt gedefinieerd door de selecties die u in andere visualisaties maakt.
title: Detailtabel
uuid: 2becff5e-c78d-4ac7-8cda-814ad0193efd
exl-id: d7f0b768-f341-41e8-904b-ec98a25f7aa9
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '498'
ht-degree: 0%

---

# Detail tabel{#detail-table}

Met detailtabellen kunt u aanvullende informatie over een subset gegevens weergeven. Deze informatie wordt gedefinieerd door de selecties die u in andere visualisaties maakt.

De extra informatie die u ziet is een steekproef van alle beschikbare gegevens.

![](assets/vis_details.png)

In de volgende tabel worden de elementen van een detailtabel beschreven.

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
   <td colname="col2"> <p>Om het even welke telbare afmeting waarvoor u gedetailleerde attributen en metrische informatie wilt bekijken. Het niveau wordt voorafgegaan door het aantal elementen dat wordt weergegeven uit het aantal beschikbare elementen, bijvoorbeeld 6/444 geeft aan dat 6 elementen worden weergegeven uit een mogelijk 444. In het bovenstaande voorbeeld geven de niveau-bezoekers aan dat alle opgegeven details zijn gebaseerd op bezoekers. In de Level Page Views wordt aangegeven dat alle details zijn gebaseerd op de paginaweergave. Het tegelijkertijd bekijken van meerdere niveaus is nuttig wanneer u gegevens wilt analyseren die verschillende telbare ouders hebben. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Kenmerk </p> </td> 
   <td colname="col02"> <p>Groen </p> </td> 
   <td colname="col2"> <p>Elke dimensie die een-op-een-op-een met het niveau is, zoals Stad voor bezoekers. In elke rij wordt het element weergegeven dat betrekking heeft op elk element van het niveau dat u hebt geselecteerd. In het bovenstaande voorbeeld geven de kenmerken Domein en Stad het domein en de stad voor elk van de voorbeeldbezoekers weer. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Metrisch </p> </td> 
   <td colname="col02"> <p>Blauw </p> </td> 
   <td colname="col2"> <p>Metrische details over het niveau dat u hebt geselecteerd. In het bovenstaande voorbeeld wordt met het niveau ingesteld op Bezoekers het aantal paginaweergaven voor een individuele bezoeker weergegeven in de weergave Metrische pagina, terwijl het niveau Paginaweergaven het detailniveau voor elk van deze paginaweergaven bevat. </p> </td> 
  </tr> 
 </tbody> 
</table>

Stel dat u werkt met websitegegevens en wilt weten welke pagina&#39;s bezoekers in bepaalde steden en bepaalde domeinen gedurende een bepaald tijdsbestek hebben bezocht.

Eerst moet u een visualisatie creëren die het tijdkader toont waarin u geinteresseerd bent, dan moet u dat tijdkader selecteren. Nu kunt u een detaillijst toevoegen om de gewenste details voor een steekproefaantal bezoekers in de dataset te bekijken.

Voer de volgende stappen uit om de hierboven beschreven details weer te geven:

1. Klik met de rechtermuisknop in de tabel met details en klik op **[!UICONTROL Add Level]** > **[!UICONTROL Visitor]**.
1. Klik met de rechtermuisknop in de tabel met details en klik op **[!UICONTROL Add Level]** > **[!UICONTROL Page View]**.
1. Klik met de rechtermuisknop op de niveaukop **[!UICONTROL Visitors]** en klik op **[!UICONTROL Add Attribute]** > **[!UICONTROL Geography]** > **[!UICONTROL Domain]**.
1. Klik met de rechtermuisknop in de kop Bezoekersniveau en klik op **[!UICONTROL Add Attribute]** > **[!UICONTROL Geography]** > **[!UICONTROL City]**.
1. Klik met de rechtermuisknop in de kop Bezoekersniveau en klik op **[!UICONTROL Add Metric]** > **[!UICONTROL Page Views]**.
1. Klik met de rechtermuisknop in de kop Pagina-weergaven en klik op **[!UICONTROL Add Attribute]** > **[!UICONTROL Page]** > **[!UICONTROL Page]**.

In de volgende voorbeeldwerkruimte ziet u de verwante details voor een willekeurige sampling van zes bezoekers van de site tijdens de opgegeven tijdsperiode.

![](assets/client-tab1.png)

## Een niveau {#section-f948d3361fd84906ac4d9ebce520bfd0} toevoegen

* Klik met de rechtermuisknop in de tabel met details en klik op **[!UICONTROL Add Level]** > *&lt;**[!UICONTROL dimension name]***.

![](assets/mnu_DetailsTable_AddLevel.png)

## Een niveau {#section-a8c820e0b656451e98e5ea75373edefc} verwijderen

* Klik met de rechtermuisknop op de kop van het bestaande niveau en klik op **[!UICONTROL Remove Level]** > *&lt;**[!UICONTROL dimension name]***.

![](assets/mnu_DetailsTable_Level.png)

## Kenmerken en meetgegevens toevoegen {#section-cdda2df3c9a448d5b9770686c8b8efb3}

* Klik met de rechtermuisknop op een kenmerk of metrische kop en klik op **[!UICONTROL Add Attribute]** > *&lt;**[!UICONTROL attribute name]**>* of **[!UICONTROL Add Metric]** > *&lt;**[!UICONTROL metric name]***.

![](assets/mnu_DetailsTable.png)

## Kenmerken en meetgegevens verwijderen {#section-4002ac957a2846678f9940270987d651}

* Klik met de rechtermuisknop op de kolom die u wilt verwijderen en klik op **[!UICONTROL Remove Attribute]** > *&lt;**[!UICONTROL attribute name]*** of **[!UICONTROL Remove Metric]** > *&lt;**[!UICONTROL metric name]**>*.

![](assets/mnu_DetailsTable.png)

## Exporteren naar Microsoft Excel {#section-a9eaba63c88a4598836a34669ba8cac1}

Zie [Venstergegevens exporteren](../../../home/c-get-started/c-wk-win-wksp/c-exp-win-data.md#concept-8df61d64ed434cc5a499023c44197349) voor informatie over het exporteren van vensters.
