---
description: Een filter is een uitdrukking die een ondergroep van de gegevens in een dataset bepaalt.
title: Syntaxis voor filterexpressies
uuid: faeb6847-3295-48ab-9d1c-db00f57647ba
exl-id: 515c1645-69c8-4990-a913-d2d505c6fe51
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '789'
ht-degree: 0%

---

# Syntaxis voor filterexpressies{#syntax-for-filter-expressions}

{{eol}}

Een filter is een uitdrukking die een ondergroep van de gegevens in een dataset bepaalt.

Een filter geeft elk element van elke dimensie toe of wijst dit af op basis van de relaties tussen de dimensies.

Filters kunnen worden bewerkt met de opdracht [!DNL Filter Editor]. Zie [Filtereditors](../../../home/c-get-started/c-analysis-vis/c-filter-editors/c-filter-editors.md#concept-2f343ecbed8240f18b0c1f1eccef11e3).

In de volgende tabel bevat elke syntaxisbeschrijving een voorbeeld van een metrische expressie die dat filter gebruikt. Bijvoorbeeld sessies[Waar] is metrisch bepaald gebruikend de &quot;Waar&quot;filter. De sessies[Waar] De metrische waarde is het zelfde als metrische zittingen omdat de Ware filter elk element van de dimensie van de Zitting toewijst.

<table id="table_5D66E6C11B384460BAAA7A6130214594"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Waar </p> </td> 
   <td colname="col2"> <p>Constante filter. Hiermee wordt elk element van elke dimensie toegestaan </p> <p>Voorbeeld: Sessies[ True] is hetzelfde als sessies. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Onwaar </p> </td> 
   <td colname="col2"> <p>Constante filter. Verwerpt elk element van elke dimensie. </p> <p>Voorbeeld: Sessies[ False ] is altijd nul. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Niet filteren </p> </td> 
   <td colname="col2"> <p>Hiermee geeft u elementen toe die door Filter worden afgewezen. </p> <p>Voorbeeld: Sessies[ not Page="A" ] is het aantal sessies dat pagina A niet heeft bezocht. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>FilterA en FilterB </p> </td> 
   <td colname="col2"> <p>Geeft elementen toe die door FilterA en FilterB worden geaccepteerd. </p> <p>Voorbeeld: Sessies[ Page="A" en Page="B" ] is het aantal sessies dat pagina A en pagina B heeft bezocht. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>FilterA of FilterB </p> </td> 
   <td colname="col2"> <p>Geeft elementen toe die door FilterA of FilterB worden geaccepteerd. </p> <p>Voorbeeld: Sessies[ Page="A" of Page="B" ] is het aantal sessies dat pagina A, pagina B of beide heeft bezocht. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Filteren op dimmen </p> </td> 
   <td colname="col2"> <p>Hiermee geeft u de set elementen van de dimensie Dim toe die door Filter worden toegelaten. </p> <p>Voorbeeld: Sessies[ Page="/home" door bezoeker ] is het aantal sessies dat hoort bij een bezoeker die de pagina "/home" heeft gezien. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Id </p> </td> 
   <td colname="col2"> <p>Referentiefilters die anders in het profiel zijn gedefinieerd. </p> <p>Voorbeeld: Sessies[ Broken_Session_Filter ] is het aantal sessies dat door het filter Verbroken sessie wordt toegelaten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Dim = "Waarde" </p> </td> 
   <td colname="col2"> <p>Geeft het opgegeven element van de dimensie Dim toe. </p> <p>Voorbeeld: Sessies[ Page="A" ] is het aantal sessies dat pagina A heeft bezocht. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Dim &lt;&gt; "Value" </p> <p>Vergroten!= "Waarde" </p> </td> 
   <td colname="col2"> <p>Hiermee geeft u elk ander element van de dimensie Dim toe. </p> <p>Voorbeeld: Sessies[ Pagina&lt;&gt;"A" ] is het aantal sessies dat een andere pagina dan A heeft bezocht. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Dim = #Ordinal </td> 
   <td colname="col2"> <p>Hiermee geeft u het element van de afmeting Afmeting Afkappen toe met de opgegeven rangtelwaarde. </p> <p>Voorbeeld: Sessies[ Month=#0] is het aantal sessies in de eerste maand van de dataset. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Afm &lt;&gt; #rangtelwoord </p> <p>Vergroten!= #Ordinal </p> </td> 
   <td colname="col2"> <p>Hiermee geeft u elk ander element van de dimensie Dim toe. </p> <p>Voorbeeld: Sessies[ Session_Value &lt;&gt; #0] is het aantal sessies met een sessiewaarde die niet gelijk is aan nul. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>DIM komt overeen met "Expr" </p> </td> 
   <td colname="col2"> <p>Geeft de elementen van de dimensie Dim toe die overeenkomen met de opgegeven reguliere expressie. Dim mag geen denormale of telbare dimensie hebben. </p> <p>Voorbeeld: Sessies[ URI komt overeen met ".*/product/.*" ] is het aantal sessies dat een pagina in een productmap heeft bezocht. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Dim komt niet overeen met "Expr" </p> </td> 
   <td colname="col2"> <p>Hiermee geeft u toe dat de elementen van de dimensie Dim niet overeenkomen met de opgegeven reguliere expressie. Dim mag geen denormale of telbare dimensie hebben. </p> <p>Voorbeeld: Sessies[ URI komt niet overeen met ".*\.jsp" ] is het aantal sessies dat een pagina heeft bezocht die geen JSP-pagina was. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Afm &lt; "Waarde" </p> </td> 
   <td colname="col2"> <p>Geeft de elementen van de dimensie Dim met rangtelwoorden weer die lager zijn dan de normale waarde van het element "Waarde". Als "Waarde" geen element van afmeting is, wordt aangenomen dat het groter is dan elk huidig element van de dimensie. </p> <p>Voorbeeld: Sessies[ Maand &lt; "Juli "04" ] is het aantal sessies dat heeft plaatsgevonden vóór juli 2004. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Dim &gt; "Waarde" </p> </td> 
   <td colname="col2"> <p>Geeft de elementen van de dimensie Dim met rangtelwoorden die groter zijn dan de normale waarde van het element "Waarde" toe. Als "Waarde" geen element van afmeting is, wordt aangenomen dat het groter is dan elk huidig element van de dimensie. </p> <p>Voorbeeld: Sessies[ Maand &gt; "Juli "04" ] is het aantal sessies dat heeft plaatsgevonden na juli 2004. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Dim &lt;= "Value" </p> </td> 
   <td colname="col2"> <p>Geeft de elementen van de dimensie Dim met rangtelwoorden aan die kleiner zijn dan of gelijk zijn aan de rangtelwoorden van de waarde van het element "Waarde". Als "Waarde" geen element van afmeting is, wordt aangenomen dat het groter is dan elk huidig element van de dimensie. </p> <p>Voorbeeld: Sessies[ Session_Number &lt;= "2" ] is het aantal sessies dat de eerste of tweede sessie voor een bezoeker was. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Dim &gt;= "Waarde" </td> 
   <td colname="col2"> <p>Geeft de elementen van de dimensie Dim met rangtelwoorden groter dan of gelijk aan de ordinale waarde van het element "Waarde" toe. Als "Waarde" geen element van afmeting is, wordt aangenomen dat het groter is dan elk huidig element van de dimensie. </p> <p>Voorbeeld: Sessies[ Session_Number &gt;= "5" ] is het aantal sessies dat de vijfde of hogere sessie voor een bezoeker was. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>om het even welke Duim </p> </td> 
   <td colname="col2"> <p>Hiermee geeft u alle elementen van de dimensie Dim toe. </p> <p>Voorbeeld: Sessies[ elke Page_View ] is het aantal sessies met ten minste één paginaweergave. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Geen grijs </p> </td> 
   <td colname="col2"> <p>Geeft elementen toe die door een willekeurige grijstint worden afgewezen. </p> <p>Voorbeeld: Sessies[ no Page_View ] is het aantal sessies zonder paginaweergave. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>(FILTER) </p> </td> 
   <td colname="col2"> <p>Hetzelfde als FILTER; gebruikt om een deel van een filterexpressie te groeperen. </p> </td> 
  </tr> 
 </tbody> 
</table>
