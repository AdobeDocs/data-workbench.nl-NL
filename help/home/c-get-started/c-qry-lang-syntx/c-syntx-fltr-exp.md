---
description: Een filter is een uitdrukking die een ondergroep van de gegevens in een dataset bepaalt.
solution: Analytics
title: Syntaxis voor filterexpressies
topic: Data workbench
uuid: faeb6847-3295-48ab-9d1c-db00f57647ba
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Syntaxis voor filterexpressies{#syntax-for-filter-expressions}

Een filter is een uitdrukking die een ondergroep van de gegevens in een dataset bepaalt.

Een filter geeft toe of verwerpt elk element van elke afmeting volgens het verband tussen afmetingen.

De filters kunnen worden uitgegeven gebruikend [!DNL Filter Editor]. Zie [Filtereditors](../../../home/c-get-started/c-analysis-vis/c-filter-editors/c-filter-editors.md#concept-2f343ecbed8240f18b0c1f1eccef11e3).

In de volgende lijst, omvat elke syntaxisbeschrijving een voorbeeld van een metrische uitdrukking gebruikend die filter. Bijvoorbeeld, is[SessionsTrue] metrisch bepaald gebruikend de &quot;Waar&quot;filter. Metrisch[SessionsTrue] is het zelfde als metrisch de Zittingen omdat de Waar filter elk element van de dimensie van de Zitting toelaat.

<table id="table_5D66E6C11B384460BAAA7A6130214594"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Waar </p> </td> 
   <td colname="col2"> <p>Constante filter. Geeft elk element van elke dimensie toe </p> <p>Voorbeeld: Sessies[ True ] is hetzelfde als sessies. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Vals </p> </td> 
   <td colname="col2"> <p>Constante filter. Verwerpt elk element van elke dimensie. </p> <p>Voorbeeld: Zittingen[ Vals] is altijd nul. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>niet filteren </p> </td> 
   <td colname="col2"> <p>Geeft elementen toe die Filter afwijst. </p> <p>Voorbeeld: Sessions[ not Page="A" ] is het aantal sessies dat pagina A niet bezocht. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>FilterA en FilterB </p> </td> 
   <td colname="col2"> <p>Geeft elementen toe die FilterA en FilterB toegeven. </p> <p>Voorbeeld: Sessies[ Page="A" en Page="B"] is het aantal sessies dat zowel pagina A als pagina B bezocht. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>FilterA of FilterB </p> </td> 
   <td colname="col2"> <p>Geeft elementen toe die FilterA of FilterB toegeven. </p> <p>Voorbeeld: Sessies[ Page="A" of Page="B"] is het aantal sessies dat pagina A, pagina B of beide bezocht. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Filteren op schijf </p> </td> 
   <td colname="col2"> <p>Geeft de reeks elementen van de afmetingAfmeting toe die door Filter worden toegelaten. </p> <p>Voorbeeld: Zittingen[ Page="/home" door Bezoeker] is het aantal Zittingen die tot een Bezoeker behoren en de pagina "/home" zagen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Identificator </p> </td> 
   <td colname="col2"> <p>De filters van de verwijzing die anders in het profiel worden bepaald. </p> <p>Voorbeeld: Sessions[ Broken_Session_Filter] is het aantal sessies dat wordt toegelaten door de Broken Session Filter. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Dim = "Waarde" </p> </td> 
   <td colname="col2"> <p>Geeft het gegeven element van de afmeting toe - afd. </p> <p>Voorbeeld: Sessies[ Page="A"] is het aantal sessies dat pagina A bezocht. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Dim &lt;&gt; "Waarde" </p> <p>Dom!= "Waarde" </p> </td> 
   <td colname="col2"> <p>Geeft elk ander element van de afmeting toe - Duim. </p> <p>Voorbeeld: Zittingen[ Pagina&lt;&gt;"A"] is het aantal Zittingen die om het even welke pagina buiten A bezochten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Dim = #Ordinal </td> 
   <td colname="col2"> <p>Geeft het element van de afmetingAfmeting toe met de bepaalde normale waarde. </p> <p>Voorbeeld: De zittingen [ Month=#0] is het aantal Zittingen in de eerste maand van de dataset. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Dim &lt;&gt; #Ordinal </p> <p>Dom!= #Ordinal </p> </td> 
   <td colname="col2"> <p>Geeft elk ander element van de afmeting toe - Duim. </p> <p>Voorbeeld: Sessies[ Session_Value &lt;&gt; #0] is het aantal sessies met een waarde voor niet-nul sessies. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>De gelijken van de wijzerplaat "Expr" </p> </td> 
   <td colname="col2"> <p>Geeft de elementen van de afmeting toe die de bepaalde regelmatige uitdrukking aanpassen. De rand mag geen denormale of aftelbare dimensie zijn. </p> <p>Voorbeeld: Sessies[ URI komt overeen met ".*/product/.*"] is het aantal Zittingen die om het even welke pagina in een productfolder bezochten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>De notaties van de rand "uitbreiden" </p> </td> 
   <td colname="col2"> <p>Geeft de elementen van de afmeting toe die niet de bepaalde regelmatige uitdrukking aanpassen. De rand mag geen denormale of aftelbare dimensie zijn. </p> <p>Voorbeeld: Sessions[ URI-notaties ".*\.jsp"] is het aantal Zittingen die om het even welke pagina bezochten die geen JSP pagina was. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Dim &lt; "Waarde" </p> </td> 
   <td colname="col2"> <p>Geeft de elementen van de afmetingAfmeting toe met normale waarden minder dan de normale waarde van het element "Waarde." Als "Waarde"geen element van afmeting is, dan wordt het verondersteld om groter te zijn dan om het even welk huidig element van de afmeting. </p> <p>Voorbeeld: Zittingen[ Maand &lt; "jul. 04" ] is het aantal sessies dat vóór juli 2004 heeft plaatsgevonden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Dim &gt; "Waarde" </p> </td> 
   <td colname="col2"> <p>Hiermee geeft u de elementen van de afmeting Afdim toe met normale waarden die groter zijn dan de normale waarde van het element "Waarde". Als "Waarde"geen element van afmeting is, dan wordt het verondersteld om groter te zijn dan om het even welk huidig element van de afmeting. </p> <p>Voorbeeld: Zittingen[ Maand &gt; "jul "04" ] is het aantal zittingen dat na juli 2004 heeft plaatsgevonden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Dim &lt;= "Waarde" </p> </td> 
   <td colname="col2"> <p>Geeft de elementen van de afmetingMom met normale waarden toe minder dan of gelijk aan de normale waarde van het element "Waarde." Als "Waarde"geen element van afmeting is, dan wordt het verondersteld om groter te zijn dan om het even welk huidig element van de afmeting. </p> <p>Voorbeeld: Sessions[ Session_Number &lt;= "2" ] is het aantal sessies dat de eerste of tweede sessie voor een bezoeker was. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Dim &gt;= "Waarde" </td> 
   <td colname="col2"> <p>Geeft de elementen van de afmetingAfmeting toe met normale waarden groter dan of gelijk aan de normale waarde van het element "Waarde." Als "Waarde"geen element van afmeting is, dan wordt het verondersteld om groter te zijn dan om het even welk huidig element van de afmeting. </p> <p>Voorbeeld: Sessies[ Session_Number &gt;= "5" ] is het aantal sessies dat de vijfde of grotere sessie was voor een bezoeker. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>om het even welke Duik </p> </td> 
   <td colname="col2"> <p>Geeft alle elementen van de afmeting toe Afwijken. </p> <p>Voorbeeld: Zittingen[ om het even welke Page_View] is het aantal zittingen met minstens één paginamening. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>geen dim </p> </td> 
   <td colname="col2"> <p>Geeft elementen toe die elke Dim afwijst. </p> <p>Voorbeeld: Sessies[ geen Page_View] is het aantal sessies zonder paginaweergave. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>(FILTER) </p> </td> 
   <td colname="col2"> <p>Hetzelfde als FILTER; gebruikt om een deel van een filteruitdrukking te groeperen. </p> </td> 
  </tr> 
 </tbody> 
</table>

