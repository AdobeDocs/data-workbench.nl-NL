---
description: Beslissingsbomen zijn een voorspellende analytische visualisatie die wordt gebruikt om de kenmerken en relaties van bezoekers te evalueren. De opbouwfunctie voor beslissingsstructuur genereert een visualisatie van de beslissingsstructuur op basis van een opgegeven positief geval en een reeks ingangen.
title: Beslissingsstructuur maken
uuid: 1f7e91ea-e5d9-4d8e-9fcf-cae4de42dfdd
exl-id: d93e6a34-be59-4af5-84c3-c13deb98b57b
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '445'
ht-degree: 0%

---

# Beslissingsstructuur maken{#decision-tree-builder}

{{eol}}

Beslissingsbomen zijn een voorspellende analytische visualisatie die wordt gebruikt om de kenmerken en relaties van bezoekers te evalueren. De opbouwfunctie voor beslissingsstructuur genereert een visualisatie van de beslissingsstructuur op basis van een opgegeven positief geval en een reeks ingangen.

Een beslissingsstructuur is een binaire classificator met een set regels (of filters) die bezoekers identificeert die voldoen aan specifieke regels op basis van een positief geval. In een beslissingsstructuur worden regels vastgesteld voor de classificatie van bezoekers die tevreden zijn (of niet tevreden zijn) over dit positieve geval. Deze regels genereren een boomstructuur om een betrouwbaarheidsniveau te bieden om aan deze positieve resultaten te voldoen.

Een beslissingsstructuur wordt samengesteld door de invoer op elk niveau te onderzoeken en de structuur te kiezen die een maximale gegevensversterking op een opgegeven splitsingspunt biedt. De splitsingspunten voor elk veranderlijk niveau produceren twee reeksen:

* Waarden die kleiner zijn dan of gelijk zijn aan het splitsingspunt, en
* Waarden groter dan het splitspunt.

Beslissingsbomen gebruiken voor

* Voer zinvolle analyse en interpretatie uit in minder tijd.
* Gebruik geautomatiseerde segmentgeneratie.
* Maak snel conclusies op basis van een model op basis van een grote hoeveelheid gegevens.

![](assets/decision_tree_parts.png)

<table id="table_FCC5D63EF8A843D79B2338BD951025EA"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><b>Werkbalk en menu's</b> </p> <p>De werkbalk bevat knoppen en menuopdrachten voor de beslissingsstructuur, waaronder functies om het positieve hoofdlettergebruik in te stellen en invoerlijsten toe te voegen. </p> <p>Net als andere visualisaties kan de <span class="uicontrol"> Element</span> kunt u Dimension en Elements slepen en neerzetten, maar u kunt ook rechtstreeks vanuit het deelvenster Finders slepen. </p> <p>Zie voor meer informatie <a href="../../../../home/c-get-started/c-analysis-vis/c-decision-trees/c-decision-trees-menu.md#concept-bfc4e80651a243d3966cc770b205606c"> Opties beslissingstructuur</a>. </p> </td> 
   <td colname="col2"> <p><b>Invoerlijst</b> </p> <p>In dit gebied worden de invoer in het structuurmodel weergegeven. De kleuren worden zo gekleurd dat ze overeenkomen met de knooppunten in het gebied Structuurweergave. </p> <p>Als u met de rechtermuisknop op een invoer klikt, kunt u de invoer uit het model verwijderen en opnieuw instellen. </p> <p>Als u de cursor boven een structuurknooppunt houdt, worden de splitsingsvoorwaarden langs de vertakking naar dat knooppunt en de voorspelling bij dat knooppunt met de betrouwbaarheidswaarde weergegeven. </p> </td> 
   <td colname="col3"> <p><b>Boomstructuurweergave</b> </p> <p>In dit gebied wordt het structuurmodel weergegeven met bladknooppunten met kleurcodes op basis van de voorspelling: groen voor een True-voorspelling van het positieve geval en rood voor een False-voorspelling. </p> <p>De gesplitste knooppunten hebben een kleurcode die overeenkomt met de invoer die overeenkomt met hun selectie. Als u de cursor boven een knooppunt houdt, wordt informatie over de splitsing weergegeven en wordt de lijst met ingangen uitgebreid, zodat de splitsingspunten in de vertakking en de distributie van de trainingsset worden weergegeven. </p> <p>Knooppunten onder een drempel worden niet standaard weergegeven. Klik op een uitbreidbaar knooppunt (aangeduid door een plus-symbool) om een vertakking te verkennen. Klik op het basisknooppunt om terug te keren naar de volledige structuurweergave. </p> </td> 
  </tr> 
 </tbody> 
</table>

<!-- <a id="section_E800327344194A6DBF37F273D8462E2A"></a> -->
