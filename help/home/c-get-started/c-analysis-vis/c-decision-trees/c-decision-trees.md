---
description: Beslissingsbomen zijn een voorspellende beeldvorming die wordt gebruikt om de kenmerken en relaties van de bezoeker te evalueren. De bouwer van de Boom van de Beslissing produceert een visualisatie van de beslissingsboom die op een gespecificeerd positief geval en een reeks input wordt gebaseerd.
solution: Analytics
title: Beslissingshiërarchie
topic: Data workbench
uuid: 1f7e91ea-e5d9-4d8e-9fcf-cae4de42dfdd
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Beslissingshiërarchie{#decision-tree-builder}

Beslissingsbomen zijn een voorspellende beeldvorming die wordt gebruikt om de kenmerken en relaties van de bezoeker te evalueren. De bouwer van de Boom van de Beslissing produceert een visualisatie van de beslissingsboom die op een gespecificeerd positief geval en een reeks input wordt gebaseerd.

Een beslissingshiërarchie is een binaire classificator met een set regels (of filters) die bezoekers identificeren die voldoen aan specifieke regels op basis van een positief geval. In een beslissingsstructuur worden regels vastgesteld voor het classificeren van bezoekers die deze positieve zaak al dan niet tevredenstellen. Deze regels produceren een boomkaart om een niveau van vertrouwen te verstrekken om deze positieve gevalsresultaten te ontmoeten.

Een Beslissingsboom wordt gebouwd door input op elk niveau te onderzoeken en te kiezen die een maximumaanwinst van informatie op een gespecificeerd spleetpunt verstrekt. De gespleten punten voor elk veranderlijk-niveau produceren twee reeksen:

* waarden die kleiner zijn dan of gelijk zijn aan het gesplitste punt, en
* Waarden groter dan het gespleten punt.

Beslissingsbomen gebruiken voor

* Voer zinvolle analyse en interpretatie uit in minder tijd.
* Gebruik geautomatiseerde segmentgeneratie.
* Maak snel conclusies van een model dat op een grote hoeveelheid gegevens wordt gebaseerd.

![](assets/decision_tree_parts.png)

<table id="table_FCC5D63EF8A843D79B2338BD951025EA"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><b>Werkbalk en menu's</b> </p> <p>De werkbalk bevat knoppen en menuopdrachten voor de beslissingshiërarchie, inclusief functies om de positieve draagtas in te stellen en invoeraanbiedingen toe te voegen. </p> <p>Als andere visualisaties, laat de doos van het <span class="uicontrol"> Element</span> u Dimensie en Elementen slepen en laten vallen, hoewel u direct van de ruit van Vinders kunt ook slepen. </p> <p>Voor meer informatie, zie de Opties <a href="../../../../home/c-get-started/c-analysis-vis/c-decision-trees/c-decision-trees-menu.md#concept-bfc4e80651a243d3966cc770b205606c"> van de Boom van de</a>Beslissing. </p> </td> 
   <td colname="col2"> <p><b>Aanbieding invoeren</b> </p> <p>Dit gebied toont de input in het boommodel. Zij zijn kleur gecodeerd om knopen in het gebied van de Vertoning van de Boom aan te passen. </p> <p>Als u met de rechtermuisknop op een invoer klikt, kunt u de invoer uit het model verwijderen en opnieuw instellen. </p> <p>Als u over een boomknoop hangt, zal het de gespleten voorwaarden langs de tak aan die knoop en de voorspelling bij die knoop met zijn vertrouwenswaarde tonen. </p> </td> 
   <td colname="col3"> <p><b>Structuurweergave</b> </p> <p>Dit gebied toont het boommodel met bladknopen color-coded gebaseerd op zijn voorspelling: groen voor een Ware voorspelling van de Positieve Geval, en rood voor een Vals voorspelling. </p> <p>De gespleten knopen zijn kleur die aan de input wordt gecodeerd die hun selectievoorwaarde aanpassen. Het hangen over een knoop toont informatie over de spleet en breidt de inputlijst uit om de gespleten punten langs de tak en de distributie van de opleidingsreeks te tonen. </p> <p>De knopen onder een drempel worden niet getoond door gebrek. Klik op een uitbreidbare knoop (die door een + symbool wordt vermeld) om een tak te onderzoeken. Klik op de wortelknoop om aan de volledige boomvertoning terug te keren. </p> </td> 
  </tr> 
 </tbody> 
</table>

<!-- <a id="section_E800327344194A6DBF37F273D8462E2A"></a> -->

