---
description: De werkbank van gegevens gebruikt regelmatige uitdrukkingen (regex) voor onderzoek en soortverrichtingen.
solution: Analytics
title: Regelmatige expressies
topic: Data workbench
uuid: dc8c1e88-4d95-4011-8a38-70fae0c5cf6d
translation-type: tm+mt
source-git-commit: 2e4991206394ca0c463210990ea44dfb700341a5

---


# Regelmatige expressies{#regular-expressions}

De werkbank van gegevens gebruikt regelmatige uitdrukkingen (regex) voor onderzoek en soortverrichtingen.

Binnen het **[!UICONTROL Search]** gebied kunt u een onderzoek na &quot;re:&quot;verklaring uitvoeren gebruikend gemeenschappelijke uitdrukkingen, bijvoorbeeld:

```
<b>re: *.s</b>
```

<table id="table_BA125AB039794EE382B33003BE4E0AFB"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> metacharacter </th> 
   <th colname="col2" class="entry"> beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>. (punt) </p> </td> 
   <td colname="col2"> <p>Komt overeen met één teken, bijvoorbeeld: <span class="filepath"> re:x.z </span> komt overeen met "xyz" of "xxz". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>* (ster) </p> </td> 
   <td colname="col2"> <p>Komt overeen met een of meer tekens, bijvoorbeeld: <span class="filepath"> re:Z* </span> komt overeen met "ZZZ". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>? (jokerteken) </p> </td> 
   <td colname="col2"> <p>De gelijken 0 of 1 van vorige uitdrukking aan kracht minimum aanpassing, bijvoorbeeld: <span class="filepath"> xy?z </span> komt overeen met "xy" en "xyz". </p> </td> 
  </tr> 
 </tbody> 
</table>

De extra gemeenschappelijke regelmatige uitdrukkingen kunnen ook worden gebruikt om complexere onderzoekskoorden tot stand te brengen. De regelmatige uitdrukkingen worden gebruikt over alle het onderzoeksgebieden van de Werkbank van Gegevens met inbegrip van de panelen van de vraagentiteit.

Zie diepgaande informatie bij [regelmatige uitdrukkingen](https://docs.adobe.com/content/help/en/data-workbench/using/dataset/c-dataset-constr.html#Regular_Expressions).
