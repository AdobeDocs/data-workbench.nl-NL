---
description: Bij de visualisatie van de dichtheidskaart worden elementen weergegeven als gearceerde rechthoeken binnen een vierkante kaart.
title: Dichtheid-overzicht
uuid: c13cecee-f322-4757-aa90-12039173ff9f
exl-id: da37d954-cadb-42a6-a44b-9b38c0354a5d
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '610'
ht-degree: 0%

---

# Dichtheid-overzicht{#density-map}

Bij de visualisatie van de dichtheidskaart worden elementen weergegeven als gearceerde rechthoeken binnen een vierkante kaart.

De grootte van de rechthoeken is afhankelijk van elementwaarden, waarbij grotere waarden worden vertegenwoordigd door rechthoeken met een groter gebied. Net als bij een cirkeldiagram kunt u met deze visualisatie snel zien welke elementen het grootste percentage van de geselecteerde dimensie vormen.

![](assets/density_map_day_visits.png)

Een dichtheidsoverzicht maken:

1. Open een nieuwe werkruimte.

   Nadat u een nieuwe werkruimte hebt geopend, moet u mogelijk **Toevoegen** > **Tijdelijk ontgrendelen** klikken.
1. Klik op **[!UICONTROL Visualization]** > **[!UICONTROL Density Map]**.

1. Selecteer een **[!UICONTROL Dimension]** van het menu.

   Selecteer bijvoorbeeld **[!UICONTROL Time]** > **[!UICONTROL Days]**.

   Als u daarentegen **[!UICONTROL Time]** > **[!UICONTROL Hours]** selecteert, krijgt u meer elementen met kleinere waarden die als kleinere rechthoeken worden weergegeven.

   >[!NOTE]
   >
   >U zult een afmeting met veelvoudige elementen willen kiezen aan uw behoeften. De huidige limiet is 200 van de grootste elementen voor elke dimensie.

1. U kunt de weergave van dimensies wijzigen door **[!UICONTROL Visualization]** > **[!UICONTROL Table]** te openen en elementen in de tabel te selecteren die u wilt weergeven op de kaart.

   ![](assets/density_map_day_selections.png)

   De kaart reageert op selecties uit de tabel.

1. Als u de muis boven kleine elementen houdt, worden de naam en de waarde van de elementen weergegeven in tekst die bij de muiscursor wordt weergegeven.
1. Maskerelementen door met de rechtermuisknop te klikken en **[!UICONTROL Mask]** te selecteren en vervolgens een optie te kiezen.

   ![](assets/density_map_day_mask.png)

   Selecteer **[!UICONTROL Unhide All]** om alle gemaskerde knooppunten weer te geven.

1. Spotlight-elementen door met de rechtermuisknop te klikken en **[!UICONTROL Spotlight]** te selecteren en vervolgens een optie te kiezen. Met spotlicht kunt u elementen in een bereik markeren en dimmen.
1. Voeg een legenda van de kleur aan de werkruimte toe. U kunt waarden op de kaart identificeren met behulp van de legenda van de kleur.

   U kunt een legenda aan de werkruimte toevoegen en de knooppunten veranderen de kleur op basis van de extra dimensie van gegevens.
1. Wijzig de afmetingen of de metrische waarde door met de rechtermuisknop op de titel van de kaart te klikken en een optie in het menu te selecteren.

   ![](assets/density_map_change_dim.png)

1. Voeg callouts toe door een cel met de rechtermuisknop aan te klikken en **[!UICONTROL Add Callout]** te selecteren. U kunt verschillende typen of visualisaties selecteren in het menu.

   ![](assets/density_map_callout.png)

1. Zoals in alle visualisaties, kunt u boven de titelbar voor basisbevelen met de rechtermuisknop klikken om te sluiten, sparen, de Uitvoer naar Microsoft Excel, Orde, Exporteer, Exemplaar, minimaliseert, en Randen om een visualisatie zonder een grens te tonen.

   ![](assets/density_map_export.png)

1. Met de dichtheidskaart kunt u meerdere elementen selecteren die op andere visualisaties lijken.

* Klik met de linkermuisknop om een element te selecteren.
* Houd Ctrl ingedrukt en klik om meerdere elementen te selecteren.
* Houd Shift ingedrukt en klik om de selectie van een element op te heffen.
* Klik met de rechtermuisknop in de geselecteerde elementen om een menu te openen. Kies vervolgens **[!UICONTROL Deselect]** of **[!UICONTROL Deselect All]** om geselecteerde elementen te wissen.

## Aanvullende opties {#section-d77defb012424de4a7ced8e5c93115bc}

Klik met de rechtermuisknop op de dichtheidskaart om een menu met de volgende opties te openen:

<table id="table_3ADA85031C834792BFD041E186962A41"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Optie </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Bijschrift toevoegen </td> 
   <td colname="col2">Voeg een tekst of afbeelding toe als een bijschrift in de visualisatie om een element nader te identificeren of te beschrijven. <p>U kunt ook een leeg metrisch Legend, Lijst, de Grafiek van de Lijn, of de Grafiek van de Spreiding selecteren die op het geselecteerde element in de Kaart van de Dichtheid wordt gebaseerd. U kunt metriek en afmetingen aan deze lege visualisaties dan toevoegen zoals nodig. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Masker </td> 
   <td colname="col2">Met maskeropties kunt u geselecteerde elementen verbergen. Klik met de rechtermuisknop om maskeropties weer te geven. <p><span class="uicontrol"> Dit element</span> verbergen - Kies deze optie om één element te maskeren dat u hebt geselecteerd. </p> <p><span class="uicontrol"> Geselecteerde</span> elementen verbergen - Kies deze optie om meerdere geselecteerde elementen te maskeren. </p> <p><span class="uicontrol"> Bovenkant</span> tonen - Kies deze optie als u alleen de bovenste elementen van 100, 50, 25 of 10 wilt weergeven op basis van de waarden in de dichtheidstoewijzing. </p> <p><span class="uicontrol"> Onder</span> tonen - Kies deze optie als u alleen de bovenste elementen van 100, 50, 25 of 10 wilt weergeven op basis van de waarden in de dichtheidstoewijzing. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Spotlicht </td> 
   <td colname="col2"> Met spotlicht kunt u elementen in een bereik markeren en dimmen. Klik met de rechtermuisknop om een optiemenu te openen. <p><span class="uicontrol"> Bovenkant</span> tonen - Kies deze optie om alleen de bovenste elementen van 100, 50, 25 of 10 te markeren op basis van waarden in de dichtheidstoewijzing. </p> <p><span class="uicontrol"> Onder</span> tonen - Kies deze optie om alleen de bovenste elementen van 100, 50, 25 of 10 weer te geven op basis van waarden in de dichtheidstoewijzing. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Deselecteren </p> <p>Alle selecties opheffen </p> </td> 
   <td colname="col2"> <p> Selecteer deze opdrachten om de selectie van het huidige element op te heffen, indien geselecteerd, of schakel alle geselecteerde elementen uit. </p> </td> 
  </tr> 
 </tbody> 
</table>
