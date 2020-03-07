---
description: De vergelijkingsvoorwaarde en de voorwaarde van de Waaier vereisen dat u het type van vergelijking specificeert dat voor de voorwaarde moet worden gemaakt.
solution: Analytics
title: Testtypen voor testactiviteiten
topic: Data workbench
uuid: dc0433dd-a35e-472e-8975-f58347512c11
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Testtypen voor testactiviteiten{#test-types-for-test-operations}

De vergelijkingsvoorwaarde en de voorwaarde van de Waaier vereisen dat u het type van vergelijking specificeert dat voor de voorwaarde moet worden gemaakt.

De volgende lijst beschrijft de beschikbare types ( [!DNL LEXICAL], [!DNL NUMERIC], en [!DNL DATETIME]).

<table id="table_1B3AD8BDF0414D0AB8EE0E6D1B53E2CE"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Testtype </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
   <th colname="col3" class="entry"> Opmerkingen </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="wintitle"> INTEGER</span> </p> </td> 
   <td colname="col2"> <p>Zet eerst het inputgebied in een geheel om. Als dit niet mogelijk is, wordt een waarde van nul gebruikt. De test keert waar terug slechts als de resulterende waarde van de geheelinput groter dan of gelijk aan de gespecificeerde minimumwaarde en minder dan of gelijk aan de gespecificeerde maximumwaarde is. </p> </td> 
   <td colname="col3"> <p>Als één van beiden van min of maximum gebieden leeg wordt verlaten, gebruikt het systeem de aangewezen min of maximum waarde beschikbaar aan met 64 bits ondertekende gehelen. </p> <p> Als de min of de maximumwaarde die in de voorwaarde wordt gespecificeerd niet met succes aan een geheelwaarde ontleedt, substitueert het systeem nul en houdt niet op met verwerking van de dataset. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="wintitle"> DATETIJD</span> </p> </td> 
   <td colname="col2"> <p>Eerst verandert het inputgebied in een datum. Als het inputgebied niet in een geldige datum kan worden veranderd, keert de voorwaardentest vals terug. Als het gebied in een datum kan worden veranderd, keert de test waar terug slechts als de inputdatum op of na de gespecificeerde minimumdatum en op of vóór de gespecificeerde maximumdatum valt. </p> </td> 
   <td colname="col3"> <p>Als de min en de maximumdata niet geldig zijn, wordt de dataset niet geconstrueerd. </p> <p> Als de min- of max-datums niet worden geleverd, vervangt het systeem de min-datum (1 januari 1600) of de max-datum (ergens in de 24e eeuw). </p> <p> Adobe adviseert gebruikend één van de volgende formaten voor <span class="wintitle"> DATETIME</span>: </p> 
    <ul id="ul_44F469CC5D974382AF70D7B1975CF077"> 
     <li id="li_DB5FD4AFD6B34436ACD7C13282F64956"> 1 januari 2013 UUR:MM.:SS EDT </li> 
     <li id="li_307580C3F97D495BB16F1212DB38CE37"> 1 januari 2013 UUR:MM:SS GMT </li> 
    </ul> <p> De tijdzone blijft aan GMT in gebreke als gespecificeerd niet. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="wintitle"> LEXISCH</span> </p> </td> 
   <td colname="col2"> <p>Keert waar terug slechts als het inputgebied lexisch groter dan of gelijk aan het koord is dat als minimum wordt gespecificeerd en minder dan of gelijk aan het koord dat in de maximumwaarde wordt gespecificeerd. </p> </td> 
   <td colname="col3"> <p>De klinische vergelijking gebruikt de waarde van ASCII van karakters in de koorden die zich van links naar rechts het vergelijken van de karakters bewegen. Voor het eerste karakter dat niet aanpast, wordt degene met de grotere waarde van ASCII beschouwd als om groter van twee te zijn. In het geval dat één koord korter is dan andere, maar tot dat punt zijn alle karakters het zelfde geweest, wordt het langere koord beschouwd als groter van twee. Als de koorden karakter voor karakterequivalent en de nauwkeurige zelfde lengte zijn, worden zij beschouwd lexisch gelijkwaardig. </p> </td> 
  </tr> 
 </tbody> 
</table>

