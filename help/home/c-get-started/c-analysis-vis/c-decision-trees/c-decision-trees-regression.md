---
description: Evalueer een Beslissingsboom gebruikend de optie van de Boom van de Regressie met nieuwe bemonstering en visualiseringseigenschappen.
title: Optie voor regressiestructuur voor beslissingsstructuur
uuid: 1e3b5d5f-1fed-49c9-9a4d-d220c28075ac
translation-type: tm+mt
source-git-commit: cb3ca4b3b993f5f04f6b6cee25850600ff3d8986

---


# Optie voor regressiestructuur voor beslissingsstructuur{#regression-tree-option-for-decision-tree}

Evalueer een Beslissingsboom gebruikend de optie van de Boom van de Regressie met nieuwe bemonstering en visualiseringseigenschappen.

Evalueer een Beslissingsboom gebruikend de optie van de Boom van de Regressie door Opties met de rechtermuisknop aan te klikken en te selecteren > de Boom **van de** Regressie binnen een visualisatie van de Beslissingsboom.

**Geactualiseerde beslissingsstructuur**: Het nieuwe algoritme werd geïntroduceerd voor de bouw van een [Besluitboom](https://docs.adobe.com/content/help/en/data-workbench/using/client/analysis-visualizations/decision-trees/c-decision-trees.html). Het behandelt meer algemene gegevens en verstrekt een meer informatieve visualisatie om de precisie van de voorspelling te verbeteren.

**Verbeterde gegevensbemonsteringsmodule**: Een bijgewerkt adaptief bemonsteringsplan helpt de Beslissingshiërarchie en de Score van de Propensiteit hogere precisieresultaten bereiken.

![](assets/CART-RegressionTreeOptions.jpg)

Groen en rood wijzen op waar of vals. De verzadiging van kleur-zulke als diep rood tegenover licht rood-wordt gebruikt om op waarschijnlijkheid te wijzen. Bijvoorbeeld, heeft een knoop met diep rood een zeer hoge waarschijnlijkheid om vals te zijn, terwijl een knoop met lichtrood een lagere waarschijnlijkheid heeft om vals te zijn. Een knoop met diep groen heeft een zeer hoge waarschijnlijkheid om waar te zijn.

Alle Bomen van het Besluit hebben variërende takbreedten om op het niveau van verkeer voor die tak van de boom te wijzen.

In een visualisatie van de Beslissingshiërarchie, klik en selecteer Opties > de Boom van de **Regressie** met de rechtermuisknop aan. Wanneer geselecteerd, worden de extra montages verstrekt:

<table id="table_39E025A3E0B549B4BEDCE0D30A499211"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Regressie instellen </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><b>Elke functie slechts één keer gebruiken</b> </p> </td> 
   <td colname="col2"> <p>Het selecteren van deze optie zal geen eigenschap meer dan eens (als de originele besluitboom)-zodat als u vijf input hebt, zal de boom niet meer dan vijf niveaus zijn en de boomstructuur zal gelijkaardig aan een Boom van de Beslissing (maar een beetje ingewikkelder) kijken. Deze optie zal de boombouw snel maken door elke eigenschap slechts eenmaal te gebruiken (als een originele Boom van de Beslissing). Het gebruiken van deze eigenschap is standaard het plaatsen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>Instelling Regressiegrootniveau </b> </p> </td> 
   <td colname="col2"> <p>Deze optie controleert de ingewikkeldheid van de Boom van de Regressie. Afhankelijk van uw gegevens, zou u een boom van de <i>Fijne</i> (met een ingewikkelde structuur met meer knopen) kunnen moeten bouwen om een zinvollere boomclassificatie te krijgen. Als u veel gegevens hebt, dan kon een vrij <i>Grove</i> boom (minder gecompliceerd met minder boomknopen) goed werken. </p> <p> <p>Opmerking: <i>Typisch</i> is standaard het plaatsen. Er zijn sommige extreme gevallen waar het <i>Typische</i> plaatsen niet eveneens werkt en het <i>Groot</i> of <i>fijn</i> plaatsen kan een betere mening van de gegevens verstrekken. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p><i>Prima</i>: De meest complexe boom met de korrelste niveaus van rapportering en de meeste takken. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p><i>Typisch</i>: Het gemiddelde niveau van granularity en takken. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p><i>Groot</i>: De minst complexe boom met de minst bepaalde categorieën en de minste takken. </p> </td> 
  </tr> 
 </tbody> 
</table>

