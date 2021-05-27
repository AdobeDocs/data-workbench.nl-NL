---
description: De werkbank van gegevens gebruikt regelmatige uitdrukkingen (regex) voor onderzoek en soortverrichtingen.
title: Reguliere expressies
uuid: dc8c1e88-4d95-4011-8a38-70fae0c5cf6d
exl-id: bb1be6d8-3b7a-47e4-bb29-4a65de99666b
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 0%

---

# Reguliere expressies{#regular-expressions}

De werkbank van gegevens gebruikt regelmatige uitdrukkingen (regex) voor onderzoek en soortverrichtingen.

In het veld **[!UICONTROL Search]** kunt u een zoekopdracht uitvoeren na de instructie &quot;re:&quot; met behulp van algemene expressies, bijvoorbeeld:

```
<b>re: *.s</b>
```

<table id="table_BA125AB039794EE382B33003BE4E0AFB"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> metateken </th> 
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
   <td colname="col2"> <p>Komt overeen met 0 of 1 van de vorige expressie om minimale overeenkomsten af te dwingen, bijvoorbeeld: <span class="filepath"> xy?z </span> komt overeen met "xy" en "xyz". </p> </td> 
  </tr> 
 </tbody> 
</table>

Aanvullende reguliere expressies kunnen ook worden gebruikt om complexere zoekreeksen te maken. Reguliere expressies worden gebruikt in alle zoekvelden van Data Workbench, inclusief de deelvensters voor query-entiteiten.

Zie gedetailleerde informatie bij [reguliere expressies](https://docs.adobe.com/content/help/en/data-workbench/using/dataset/c-dataset-constr.html#Regular_Expressions).
