---
description: Gebruik de deelvensters Finder in Data Workbench om metriek, afmetingen en filters te selecteren. Deze deelvensters bieden ondersteuning voor zoeken, sorteeropties en slepen en neerzetten.
title: Finders
uuid: 7a4144f5-133f-48ed-9613-1e42b1313120
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '640'
ht-degree: 0%

---


# Finders{#finders}

Gebruik de deelvensters Finder in Data Workbench om metriek, afmetingen en filters te selecteren. Deze deelvensters bieden ondersteuning voor zoeken, sorteeropties en slepen en neerzetten.

U kunt een deelvenster Finder openen in de linkerzijbalk of in een werkruimte.

![](assets/query_entity_panel_main.png)

<table id="table_3E43DBA0646842898F14F31374F9E39C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Dimension Finder </th> 
   <th colname="col2" class="entry"> Metrische Finder </th> 
   <th colname="col3" class="entry"> Filters Finder </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Een lijst van alle afmetingen in uw vraagmodel. </p><img placement="break" id="image_D7D317D84C0843BE8D324E5B9F7AF20D" src="assets/query_entity_dim_panel.png" /> </td> 
   <td colname="col2"> <p>Een lijst van alle metriek in uw vraagmodel. </p><img placement="break" id="image_04553B2F2C6A48FE897B4EFF002BED59" src="assets/query_entity_metric_panel.png" /> </td> 
   <td colname="col3"> <p>Een lijst met alle filters die voor uw organisatie zijn gemaakt. </p><img placement="break" id="image_920E72D795644634A82D1955CB64B355" src="assets/query_entity_filters_panel.png" /> </td> 
  </tr> 
 </tbody> 
</table>

**Een Finder openen:**

* Klik met de rechtermuisknop in een werkruimte en selecteer **[!UICONTROL Tools]** > **[!UICONTROL Finder]**.

   Het deelvenster Finder met tabbladen voor Metriek, Dimension en Filters wordt geopend in de werkruimte.

* Klik met de rechtermuisknop op de linkerzijbalk en selecteer **[!UICONTROL Add]** > **[!UICONTROL Finder]**.

   Het deelvenster Finder wordt geopend in het linkerdeelvenster.

De **Finder** bevat de volgende functies:

<table id="table_072047E919204577AE85789BAE0F4EE8"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Finder-functies </th> 
   <th colname="col2" class="entry"> Details </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"><b>Slepen en neerzetten</b> </td> 
   <td colname="col2"> <p> U kunt afmetingen of metriek van het deelvenster naar een visualisatie in de werkruimte slepen om de dimensie te wijzigen of nieuwe metriek toe te voegen. </p> 
    <ol id="ol_612DC76EC04C4FCE938B20B388C43CE8"> 
     <li id="li_7F73B781141E4B8CAE9800F580F62E44">Houd <span class="uicontrol"> &lt;Ctrl&gt;</span> en <span class="uicontrol"> &lt;Alt&gt;</span> ingedrukt en selecteer de dimensie of metrisch in het paneel van de Vinder. </li> 
     <li id="li_631D57976F71415AA61F33EBBFDD128A">Sleep een nieuwe dimensie van de ruit en laat vallen het aan visualisatie om dimensies te veranderen of toe te voegen. </li> 
     <li id="li_5329FB82225F46EBBE3A996A641058DE">Als u metriek wilt toevoegen, sleept u een nieuwe metrische waarde uit het deelvenster en zet u deze neer op de metrische koptekst van de geselecteerde visualisatie. </li> 
    </ol> <p>Dit werkt voor alle relevante visualisaties, waaronder tabellen, bezoekerscluster, correlatiematrix, spreidingspercelen en de 2-D staafgrafiek (afhankelijk van de as). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"><b>Zoeken</b> </td> 
   <td colname="col2">Met het vak <span class="uicontrol"> Zoeken</span> in de deelvensters Finder kunt u namen filteren voor Dimension, Metriek en Filters. 
    <ul id="ul_0F6F377E9906472E99008EBE7483F689"> 
     <li id="li_75857895EDB045C8B2960393854B257D"> <p>Patroonovereenkomst (eenvoudige zoekopdracht op een glob). Begin de naam van een vereiste afmeting, metrisch, of filterentiteit in het gebied van het Onderzoek te typen en slechts passende koorden overal in de naam zullen worden gefiltreerd en in de ruit van Vinders getoond. </p> <p>Voer bijvoorbeeld het volgende in: </p> <code><b>Search:</b>click</code> <p>U kunt de volgende resultaten ophalen in de Finder Dimension: </p> <p><img placement="break" id="image_7CBAAABA92BB47658B7F9F5C0263CF20" src="assets/finders_glob_search.png" /> </p> <p>Met de standaardpatroonovereenkomst kunt u jokertekens gebruiken, zoals . (punt), "?" en "*" (ster). </p> </li> 
     <li id="li_044F9EC1399B44CD81E1852F85137704"> <p>Reguliere expressies. Complexere reguliere expressies worden ook ondersteund voor extra zoekmogelijkheden. Voeg het voorvoegsel "re:" toe vóór de zoekterm (geen spaties) die u als een reguliere expressie wilt interpreteren. </p> <p>Voer bijvoorbeeld het volgende in: </p> <code><b>Search:</b>re.*ip</code> <p>U kunt de volgende resultaten ophalen in de Finder Dimension: </p> <p><img placement="break" id="image_F47DB90B36504997AA1C509855B89A47" src="assets/finders_regex_search.png" /> </p> </li> 
    </ul> <p>Zie <a href="https://docs.adobe.com/content/help/en/data-workbench/using/dataset/c-reg-exp.html" format="http" scope="external"> reguliere expressies</a> voor diepgaande zoekinformatie. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"><b>Type Dimension</b> </td> 
   <td colname="col2">Op het tabblad Dimension kunt u met de rechtermuisknop op de tabkop klikken om te sorteren op het type dimensie. <p><img id="image_FB44D0F4D36B4AD7A6165E0432211AB6" placement="break" src="assets/query_entity_search_types.png" /> 
     <ul id="ul_D36B8474730F4859BC7AA015CC1B8EF0"> 
      <li id="li_4AE1D5699D0E45AF880A134F886B8B19">Attributen—Dimension die zijn gebaseerd op kenmerken van de bezoeker, producten, geografie, tijd, video en andere kenmerken. </li> 
      <li id="li_0B2A08F8CBE94356AC506F95DC268C47">Clusters—Dimension die in de clusterbuilder zijn gemaakt. </li> 
      <li id="li_4BC3396A680B49A4B6BDAAD066826864">Scores—Dimension die zijn gemaakt in de densiteitsscoring. </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"><b>Label</b> </td> 
   <td colname="col2">In elk lusje, kunt u met de rechtermuisknop klikken en <span class="uicontrol"> Etiket </span> selecteren om de ruit van de Vinder anders te noemen. <p><img placement="break" id="image_F61C57F6548646069242DFB2490C67B9" src="assets/label_change.png" /> </p> <p>De standaardlabels Dimension, Metriek en Filters kunnen worden gewijzigd in een tabnaam die voldoet aan de conventies van uw organisatie. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"><b>Item toevoegen</b> </td> 
   <td colname="col2">In elk lusje, kunt u met de rechtermuisknop klikken en <span class="uicontrol"> toevoegen Punt</span> selecteren om een lijst te openen en manueel Dimension, Metriek en Filters toe te voegen. </td> 
  </tr> 
  <tr> 
   <td colname="col1"><b>Zoekbalk</b> </td> 
   <td colname="col2">Klik met de rechtermuisknop op de balk <span class="uicontrol"> Finders</span> in de linkerzijbalk om een menu voor extra functies te openen. <p><img placement="break" id="image_4DA4930294B84308A1E627C828C35663" src="assets/finders_menu.png" /> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"><b>Sluiten</b> </td> 
   <td colname="col2">Klik met de rechtermuisknop op de balk <span class="uicontrol"> Finders</span> en selecteer <span class="uicontrol"> Close</span> om het venster Finders te sluiten. </td> 
  </tr> 
  <tr> 
   <td colname="col1"><b>Opslaan</b> </td> 
   <td colname="col2">Sla de lijst lokaal op door met de rechtermuisknop in de koptekstbalk te klikken en de optie <span class="uicontrol"> Opslaan</span> te selecteren. </td> 
  </tr> 
  <tr> 
   <td colname="col1"><b>Exporteren</b> </td> 
   <td colname="col2">U kunt een lijst met geselecteerde afmetingen, metriek, of filters van het paneel van de Vinder uitvoeren door in de bar van Vinders met de rechtermuisknop te klikken en <span class="uicontrol"> de Uitvoer </span> van het menu te selecteren. <p> Voeg een naam toe en voer naar Microsoft Excel uit. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"><b>Kopiëren</b> </td> 
   <td colname="col2"> Kopieer een lijst met Dimension, Metriek of Filters. U kunt als bestand of als afbeelding kopiëren in Donkere achtergrond, Lichte achtergrond of Monochroom. </td> 
  </tr> 
  <tr> 
   <td colname="col1"><b>Minimaliseren</b> </td> 
   <td colname="col2"> Minimaliseer de ruit van de Vinder. Alleen de Finders-balk wordt weergegeven. </td> 
  </tr> 
  <tr> 
   <td colname="col1"><b>Rand</b> </td> 
   <td colname="col2"> Hiermee geeft u een deelvenster zonder randlijnen voor Finders weer in de werkruimte (maar niet in de linkerzijbalk). </td> 
  </tr> 
 </tbody> 
</table>

