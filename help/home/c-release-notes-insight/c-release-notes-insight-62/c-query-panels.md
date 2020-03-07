---
description: De panelen van de Vinder van het gebruik in de Werkbank van Gegevens om metriek, afmetingen, en filters te selecteren. Deze panelen verstrekken onderzoekssteun, sorterende opties, en belemmering en dalingsmogelijkheden.
solution: Analytics
title: Vinders
topic: Data workbench
uuid: 7a4144f5-133f-48ed-9613-1e42b1313120
translation-type: tm+mt
source-git-commit: 2e4991206394ca0c463210990ea44dfb700341a5

---


# Vinders{#finders}

De panelen van de Vinder van het gebruik in de Werkbank van Gegevens om metriek, afmetingen, en filters te selecteren. Deze panelen verstrekken onderzoekssteun, sorterende opties, en belemmering en dalingsmogelijkheden.

Een paneel van de Vinder kan in de linkerzijbalk of binnen een werkruimte worden geopend.

![](assets/query_entity_panel_main.png)

<table id="table_3E43DBA0646842898F14F31374F9E39C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Afmetingen zoeken </th> 
   <th colname="col2" class="entry"> Metrische zoeker </th> 
   <th colname="col3" class="entry"> Filterzoeker </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Een lijst van alle afmetingen in uw vraagmodel. </p><img placement="break" id="image_D7D317D84C0843BE8D324E5B9F7AF20D" src="assets/query_entity_dim_panel.png" /> </td> 
   <td colname="col2"> <p>Een lijst van alle metriek in uw vraagmodel. </p><img placement="break" id="image_04553B2F2C6A48FE897B4EFF002BED59" src="assets/query_entity_metric_panel.png" /> </td> 
   <td colname="col3"> <p>Een lijst van alle filters die voor uw organisatie worden gecreeerd. </p><img placement="break" id="image_920E72D795644634A82D1955CB64B355" src="assets/query_entity_filters_panel.png" /> </td> 
  </tr> 
 </tbody> 
</table>

**Een zoeker openen:**

* Klik in een werkruimte met de rechtermuisknop aan en selecteer **[!UICONTROL Tools]** > **[!UICONTROL Finder]**.

   De ruit van de Vinder met lusjes voor Metriek, Dimensies, en Filters zal in de werkruimte openen.

* Klik in de linkerzijbalk met de rechtermuisknop aan en selecteer **[!UICONTROL Add]** > **[!UICONTROL Finder]**.

   De ruit van de Vinder zal in het linkerpaneel openen.

De **Vinder** omvat de volgende eigenschappen:

<table id="table_072047E919204577AE85789BAE0F4EE8"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Functies zoeken </th> 
   <th colname="col2" class="entry"> Details </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"><b>Slepen en neerzetten</b> </td> 
   <td colname="col2"> <p> U kunt afmetingen of metriek van het paneel slepen en laten vallen aan een visualisatie in de werkruimte om de afmeting te veranderen of nieuwe metriek toe te voegen. </p> 
    <ol id="ol_612DC76EC04C4FCE938B20B388C43CE8"> 
     <li id="li_7F73B781141E4B8CAE9800F580F62E44">Houd de toetsen <span class="uicontrol"> &lt;Ctrl&gt;</span> en <span class="uicontrol"> &lt;Alt&gt;</span> ingedrukt en selecteer de afmeting of de metrisch in het deelvenster Vinder. </li> 
     <li id="li_631D57976F71415AA61F33EBBFDD128A">Sleep een nieuwe dimensie van de ruit en laat vallen het aan de visualisatie om afmetingen te veranderen of toe te voegen. </li> 
     <li id="li_5329FB82225F46EBBE3A996A641058DE">Om metriek toe te voegen, sleep nieuwe metrisch van de ruit en laat vallen het op de metrische kopbal van de geselecteerde visualisatie. </li> 
    </ol> <p>Dit zal voor alle relevante visualisaties, met inbegrip van lijsten, bezoekerscluster, correlatiematrix, spreidingspercelen, en de grafiek van de 2-D bar werken (afhankelijk van de as). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"><b>Zoeken</b> </td> 
   <td colname="col2">Een <span class="uicontrol"> vakje van het Onderzoek</span> in de panelen van de Vinder laat u namen voor Afmetingen, Metriek, en Filters filtreren. 
    <ul id="ul_0F6F377E9906472E99008EBE7483F689"> 
     <li id="li_75857895EDB045C8B2960393854B257D"> <p>Patroonmatching (eenvoudig globaal zoeken). Het begin die de naam van een vereiste afmeting, metrisch, of filterentiteit op het gebied van het Onderzoek typt en slechts zal de passende koorden overal in de naam bevat worden gefiltreerd en in de ruit van Vinders getoond. </p> <p>Bijvoorbeeld, ga binnen: </p> <code><b>Search:</b>click</code> <p>U kon de volgende resultaten in de Vinder van Afmetingen krijgen: </p> <p><img placement="break" id="image_7CBAAABA92BB47658B7F9F5C0263CF20" src="assets/finders_glob_search.png" /> </p> <p>De standaard patroon aanpassing laat u de vervangingskarakters, zoals gebruiken. (punt), "?" en "*" (ster). </p> </li> 
     <li id="li_044F9EC1399B44CD81E1852F85137704"> <p>Regelmatige expressies. De complexere regelmatige uitdrukkingen worden ook gesteund voor toegevoegd onderzoeksvermogen. Voeg de prefix "re:"vóór uw onderzoekstermijn (geen ruimten) toe om als regelmatige uitdrukking te interpreteren. </p> <p>Bijvoorbeeld, ga binnen: </p> <code><b>Search:</b>re.*ip</code> <p>U kon de volgende resultaten in de Vinder van Afmetingen krijgen: </p> <p><img placement="break" id="image_F47DB90B36504997AA1C509855B89A47" src="assets/finders_regex_search.png" /> </p> </li> 
    </ul> <p>Voor diepgaande onderzoeksinformatie, zie <a href="https://docs.adobe.com/content/help/en/data-workbench/using/dataset/c-reg-exp.html" format="http" scope="external"> regelmatige uitdrukkingen</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"><b>Afmetingstype</b> </td> 
   <td colname="col2">In het lusje van de Dimensie, kunt u op de lusjerubriek met de rechtermuisknop klikken om door het type van afmeting te sorteren. <p><img id="image_FB44D0F4D36B4AD7A6165E0432211AB6" placement="break" src="assets/query_entity_search_types.png" /> 
     <ul id="ul_D36B8474730F4859BC7AA015CC1B8EF0"> 
      <li id="li_4AE1D5699D0E45AF880A134F886B8B19">Attributen-afmetingen die op kenmerken van de bezoeker, de producten, de aardrijkskunde, de tijd, de video, en andere attributen worden gebouwd worden gebaseerd die. </li> 
      <li id="li_0B2A08F8CBE94356AC506F95DC268C47">De clusters-afmetingen die binnen de clusterbouwer worden gebouwd. </li> 
      <li id="li_4BC3396A680B49A4B6BDAAD066826864">Scores-Afmetingen die binnen het nevenscoren worden gebouwd. </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"><b>Etiket</b> </td> 
   <td colname="col2">In elk lusje, kunt u met de rechtermuisknop klikken en <span class="uicontrol"> Etiket</span> selecteren om de ruit van de Vinder anders te noemen. <p><img placement="break" id="image_F61C57F6548646069242DFB2490C67B9" src="assets/label_change.png" /> </p> <p>De standaardinmetingen, de Metriek, en de etiketten van Filters kunnen in een lusjenaam worden veranderd die aan de overeenkomsten van uw organisatie voldoet. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"><b>Object toevoegen</b> </td> 
   <td colname="col2">In elk lusje, kunt u klikken en selecteren <span class="uicontrol"> voeg Punt</span> toe om een lijst te openen en manueel Afmetingen, Metriek en Filters toe te voegen. </td> 
  </tr> 
  <tr> 
   <td colname="col1"><b>Vinderbalk</b> </td> 
   <td colname="col2">Klik in de bar van <span class="uicontrol"> Vinden</span> in de linkerzijbalk met de rechtermuisknop aan om een menu voor extra eigenschappen te openen. <p><img placement="break" id="image_4DA4930294B84308A1E627C828C35663" src="assets/finders_menu.png" /> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"><b>Sluiten</b> </td> 
   <td colname="col2">Klik in de bar van <span class="uicontrol"> Vinden</span> met de rechtermuisknop aan en selecteer <span class="uicontrol"> dicht</span> om een ruit van Vinders te sluiten. </td> 
  </tr> 
  <tr> 
   <td colname="col1"><b>Opslaan</b> </td> 
   <td colname="col2">Sparen plaatselijk de lijst door in de kopbalbar met de rechtermuisknop aan te klikken en <span class="uicontrol"> te selecteren sparen</span> optie. </td> 
  </tr> 
  <tr> 
   <td colname="col1"><b>Uitvoeren</b> </td> 
   <td colname="col2">U kunt een lijst van geselecteerde afmetingen, metriek, of filters van het paneel van de Vinder uitvoeren door in de bar van Vinders met de rechtermuisknop te klikken en de <span class="uicontrol"> Uitvoer</span> van het menu te selecteren. <p> Voeg een naam toe en voer naar Microsoft Excel uit. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"><b>Kopiëren</b> </td> 
   <td colname="col2"> Kopieer een lijst van Afmetingen, Metriek, of Filters. U kunt als dossier of als grafisch in Donkere Achtergrond, Lichte Achtergrond, of Monochroom kopiëren. </td> 
  </tr> 
  <tr> 
   <td colname="col1"><b>Minimaliseren</b> </td> 
   <td colname="col2"> Minimaliseer de ruit van de Vinder. Slechts zal de bar van Vinders verschijnen. </td> 
  </tr> 
  <tr> 
   <td colname="col1"><b>grenzeloos</b> </td> 
   <td colname="col2"> Toont een ruit zonder grenslijnen voor Vinders in de werkruimte (maar niet in linkersidebar). </td> 
  </tr> 
 </tbody> 
</table>

