---
description: Evalueer een beslissingsstructuur met de optie Regressiestructuur met nieuwe bemonsterings- en visualisatiefuncties.
title: Regressieboomoptie voor beslissingsstructuur
uuid: 1e3b5d5f-1fed-49c9-9a4d-d220c28075ac
exl-id: e5f8d525-1530-4169-b246-cdaf30e984c0
source-git-commit: 232117a8cacaecf8e5d7fcaccc5290d6297947e5
workflow-type: tm+mt
source-wordcount: '429'
ht-degree: 0%

---

# Regressieboomoptie voor beslissingsstructuur{#regression-tree-option-for-decision-tree}

Evalueer een beslissingsstructuur met de optie Regressiestructuur met nieuwe bemonsterings- en visualisatiefuncties.

Evalueer een beslissingsstructuur met de optie Regressiestructuur door met de rechtermuisknop te klikken en Opties > **Regressiestructuur** te selecteren in een beslissingsboomstructuur.

**Bijgewerkte Beslissingsstructuurconstructor**: Het nieuwe algoritme werd geïntroduceerd voor het bouwen van een  [Beslissingsboom](https://experienceleague.adobe.com/docs/data-workbench/using/client/analysis-visualizations/decision-trees/c-decision-trees.html). Het behandelt meer algemene gegevens en verstrekt een informatieve visualisatie om de precisie van de voorspelling te verbeteren.

**Verbeterde gegevensbemonsteringsmodule**: Een bijgewerkt adaptief bemonsteringsplan helpt de Beslissingsboom en de Score van de Volheid hogere precisieresultaten bereiken.

![](assets/CART-RegressionTreeOptions.jpg)

Groen en rood geven true of false aan. De verzadiging van kleur, zoals diep rood versus lichtrood, wordt gebruikt om de waarschijnlijkheid aan te geven. Een knooppunt met dieprood heeft bijvoorbeeld een zeer grote kans op false, terwijl een knooppunt met lichtrood een lagere kans heeft op false. Een knooppunt met diepgroen heeft een zeer hoge waarschijnlijkheid om waar te zijn.

Alle besluitvormingsbomen hebben variërende takbreedten om het niveau van verkeer voor die tak van de boom te wijzen.

Klik in een beslissingsstructuur met de rechtermuisknop en selecteer Opties > **Regressiestructuur**. Als deze optie is geselecteerd, worden aanvullende instellingen opgegeven:

<table id="table_39E025A3E0B549B4BEDCE0D30A499211"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Regressie-instelling </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><b>Elke functie slechts eenmaal gebruiken</b> </p> </td> 
   <td colname="col2"> <p>Als u deze optie selecteert, wordt een functie niet meer dan één keer gebruikt (zoals de oorspronkelijke beslissingsstructuur). Als u vijf invoer hebt, is de structuur niet meer dan vijf niveaus en ziet de boomstructuur er ongeveer hetzelfde uit als een beslissingsstructuur (maar iets gecompliceerder). Met deze optie wordt het boomgebouw snel gemaakt door elk kenmerk maar één keer te gebruiken (zoals een oorspronkelijke beslissingsstructuur). Het gebruik van deze functie is een standaardinstelling. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>Instelling voor Regressiestructuurniveau  </b> </p> </td> 
   <td colname="col2"> <p>Met deze optie bepaalt u de complexiteit van de regressiestructuur. Afhankelijk van uw gegevens, zou u een <i>Fine</i> boom (met een gecompliceerde structuur met meer knopen) kunnen moeten bouwen om een zinvollere boomclassificatie te krijgen. Als u veel gegevens hebt, zou een relatief <i>grove</i> boom (minder gecompliceerd met minder boomknopen) goed kunnen werken. </p> <p> <p>Opmerking: <i>Typisch</i> is het gebrek dat plaatst. In sommige extreme gevallen werkt de instelling <i>Normaal</i> niet zo goed en kan de instelling <i>Grof</i> of <i>Fine</i> een betere weergave van de gegevens opleveren. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p><i>Fijn</i>: De meest complexe boomstructuur met de meest gedetailleerde rapportageniveaus en de meeste takken. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p><i>Normaal</i>: Het gemiddelde niveau van granulariteit en takken. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p><i>Grof</i>: De minst complexe boom met de minste bepaalde categorieën en de minste takken. </p> </td> 
  </tr> 
 </tbody> 
</table>
