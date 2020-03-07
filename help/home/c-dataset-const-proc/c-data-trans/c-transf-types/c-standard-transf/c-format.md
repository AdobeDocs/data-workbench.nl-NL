---
description: De transformatie van het Formaat neemt een reeks input en formatteert hen om een output tot stand te brengen die de bepaalde structuur aanpast.
solution: Analytics
title: Formaat
topic: Data workbench
uuid: c596902e-21bc-4ce6-9ca4-7ca86dfc0a6c
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Formaat{#format}

De transformatie van het Formaat neemt een reeks input en formatteert hen om een output tot stand te brengen die de bepaalde structuur aanpast.

De transformatie werkt op of eenvoudige koorden of koordvectoren en veroorzaakt output door het bepaalde formaat op elke inputwaarde toe te passen tot alle inputwaarden zijn omgezet.

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
   <td colname="col2"> Beschrijvende naam van de transformatie. U kunt om het even welke naam hier ingaan. </td> 
   <td colname="col3"></td> 
  </tr> 
  <tr> 
   <td colname="col1"> Opmerkingen </td> 
   <td colname="col2"> Optioneel. Opmerkingen over de transformatie. </td> 
   <td colname="col3"></td> 
  </tr> 
  <tr> 
   <td colname="col1"> Toestand </td> 
   <td colname="col2"> De omstandigheden waaronder deze transformatie wordt toegepast. </td> 
   <td colname="col3"></td> 
  </tr> 
  <tr> 
   <td colname="col1"> Formaat </td> 
   <td colname="col2"> <p>Een het formatteren koord dat wordt gebruikt om te specificeren hoe de output zal kijken. </p> <p> %1% verwijst naar een waarde van de eerste invoervector, %2% verwijst naar een waarde van de tweede inputvector, etc. </p> </td> 
   <td colname="col3"></td> 
  </tr> 
  <tr> 
   <td colname="col1"> Ingangen </td> 
   <td colname="col2"> <p>Gebieden die of eenvoudige koorden of koordvectoren bevatten. In het geval van koordvectoren als input, zal de output ook een koordvector zijn die uit de toepassing van de parameter van het <span class="wintitle"> Formaat</span> aan elke reeks inputwaarden resulteert. </p> <p> <p>Opmerking:  De nummering van input begint bij 0, maar de nummering van de waarden van de formaatsubstitutie begint bij %1%. </p> </p> </td> 
   <td colname="col3"></td> 
  </tr> 
  <tr> 
   <td colname="col1"> Uitvoer </td> 
   <td colname="col2"> De naam van het gebied dat wordt gecreeerd om de resultaten van de transformatie te bevatten. Als de input koordvectoren zijn, zal de lengte van de vector van het outputkoord de lengte van de langste inputvector zijn. Als sommige vectoren van het inputkoord van kortere lengte zijn, worden de lege koorden gebruikt voor hun positie in het formaatkoord tot de lengte van de outputvector wordt bereikt. </td> 
   <td colname="col3"></td> 
  </tr> 
 </tbody> 
</table>

In dit voorbeeld, worden twee vectoren, één een vector van koorden die productcategorieën vertegenwoordigen en andere een overeenkomstige koordvector die de hoeveelheid van elk gekocht product vertegenwoordigen, omgezet in één enkele vector van gelijkwaardige lengte die de vorm neemt: Product %1%, Hoeveelheid %2%.

![](assets/cfg_TransformationType_Format.png)

Als de inputvectoren productcategorieën van (683, 918) en hoeveelheden van (10, 4) bevatten, zou het resultaat één definitieve outputvector zijn die de volgende twee koorden bevat: (&quot;Product 683, Hoeveelheid 10&quot;, &quot;Product 918, Hoeveelheid 4&quot;).
