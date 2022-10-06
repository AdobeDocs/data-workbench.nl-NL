---
description: De transformatie van het Formaat neemt een reeks input en formatteert hen om tot een output te leiden die de bepaalde structuur aanpast.
title: Indeling
uuid: c596902e-21bc-4ce6-9ca4-7ca86dfc0a6c
exl-id: 842b502e-cd16-45b3-ada8-6f2d899f1d54
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '327'
ht-degree: 1%

---

# Indeling{#format}

{{eol}}

De transformatie van het Formaat neemt een reeks input en formatteert hen om tot een output te leiden die de bepaalde structuur aanpast.

De transformatie werkt op eenvoudige tekenreeksen of tekenreeksvectoren en produceert uitvoer door de opgegeven indeling toe te passen op elke invoerwaarde totdat alle invoerwaarden zijn getransformeerd.

<table id="table_3953C993167248AA9A47964A51C4AB5D"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Parameter </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
   <th colname="col3" class="entry"> Standaard </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Naam </td> 
   <td colname="col2"> Beschrijvende naam van de transformatie. U kunt hier elke naam invoeren. </td> 
   <td colname="col3"></td> 
  </tr> 
  <tr> 
   <td colname="col1"> Opmerkingen </td> 
   <td colname="col2"> Optioneel. Opmerkingen over de transformatie. </td> 
   <td colname="col3"></td> 
  </tr> 
  <tr> 
   <td colname="col1"> Voorwaarde </td> 
   <td colname="col2"> De omstandigheden waaronder deze transformatie wordt toegepast. </td> 
   <td colname="col3"></td> 
  </tr> 
  <tr> 
   <td colname="col1"> Indeling </td> 
   <td colname="col2"> <p>A formatting string used to specify how the output will look. </p> <p> %1% verwijst naar een waarde van de eerste invoervector, %2% verwijst naar een waarde van de tweede invoervector, enzovoort. </p> </td> 
   <td colname="col3"></td> 
  </tr> 
  <tr> 
   <td colname="col1"> Invoer </td> 
   <td colname="col2"> <p>Velden met eenvoudige tekenreeksen of tekenreeksvectoren. In het geval van tekenreeksvectoren als invoer is de uitvoer ook een tekenreeksvector die het resultaat is van de toepassing van de <span class="wintitle"> Indeling</span> aan elke reeks inputwaarden. </p> <p> <p>Opmerking: De nummering van invoer begint bij 0, maar de nummering van de vervangende waarden voor indeling begint bij %1%. </p> </p> </td> 
   <td colname="col3"></td> 
  </tr> 
  <tr> 
   <td colname="col1"> Uitvoer </td> 
   <td colname="col2"> De naam van het veld dat is gemaakt om de resultaten van de transformatie te bevatten. Als de invoer tekenreeksvectoren zijn, is de lengte van de uitvoertekenreeksvector de lengte van de langste invoervector. Als sommige van de invoertekenreeksvectoren van kortere lengte zijn, worden lege tekenreeksen gebruikt voor hun positie in de indelingstekenreeks totdat de lengte van de uitvoervector is bereikt. </td> 
   <td colname="col3"></td> 
  </tr> 
 </tbody> 
</table>

In dit voorbeeld worden twee vectoren, een vector met tekenreeksen die productcategorieën vertegenwoordigen en de andere een overeenkomende tekenreeksvector die de hoeveelheid van elk aangeschaft product vertegenwoordigt, getransformeerd in één vector met een gelijkwaardige lengte die de vorm aanneemt: Product %1%, Aantal %2%.

![](assets/cfg_TransformationType_Format.png)

Als de inputvectoren productcategorieën (683, 918) en hoeveelheden (10, 4) bevatten, zou het resultaat één uiteindelijke outputvector zijn die de volgende twee tekenreeksen bevat: (&quot;Product 683, Hoeveelheid 10&quot;, &quot;Product 918, Hoeveelheid 4&quot;).
