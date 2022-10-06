---
description: Het menu Beslissingsstructuur bevat functies voor het instellen van het positieve gebruiksscenario, filters, opties voor bladdistributie, de verwarringsmatrix en andere geavanceerde opties.
title: Opties beslissingstructuur
uuid: 6439c6d4-60ac-4324-b870-b452a63b7ba1
exl-id: e139562d-4613-4159-a858-2a78a2e896dd
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '532'
ht-degree: 0%

---

# Opties beslissingstructuur{#decision-tree-options}

{{eol}}

Het menu Beslissingsstructuur bevat functies voor het instellen van het positieve gebruiksscenario, filters, opties voor bladdistributie, de verwarringsmatrix en andere geavanceerde opties.

<table id="table_0CBCCB0856E2469EBE8846B413CAB114"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Werkbalkknoppen </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Ga </td> 
   <td colname="col2"> Klik om het algoritme van de beslissingsboom in werking te stellen en de visualisatie te tonen. Dit is grijs-uit tot er input zijn. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Herstellen </td> 
   <td colname="col2"> Hiermee wist u de invoer- en beslissingsboomstructuur en herstelt u het proces. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Opslaan </td> 
   <td colname="col2"><b>De beslissingsstructuur opslaan</b>. U kunt de beslissingsstructuur in verschillende indelingen opslaan: 
    <ul id="ul_F7C7836C06D64912893113E8EEA05704"> 
     <li id="li_D2D8451A679243F1BC67C3B80CA5F83F">Predictive Markup Language (<b>PMML</b>), een op XML gebaseerde bestandsindeling die door toepassingen wordt gebruikt om besluitvormingsboommodellen te beschrijven en uit te wisselen. </li> 
     <li id="li_88C4B3E050CA4EFC9B7FA8BD446A9C55"><b>Tekst</b> het tonen van eenvoudige kolommen en rijen van waar of vals, percentages, aantal leden, en inputwaarden. </li> 
     <li id="li_3F871B88F3FA41E9B95EFF5A181E3D57">A <b>Dimension</b> met vertakkingen die overeenkomen met elementen van voorspelde resultaten. </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Opties </td> 
   <td colname="col2"> Zie de onderstaande tabel voor het menu Opties. </td> 
  </tr> 
 </tbody> 
</table>

<table id="table_24D84440D0354C70928E8927624DB255"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Menu Opties </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Positief hoofdlettergebruik instellen </td> 
   <td colname="col2"> Hiermee definieert u de huidige werkruimte als het positieve hoofdlettergebruik van het model. Hiermee wist u het geval als er geen selectie is. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Populatiefilter instellen </td> 
   <td colname="col2"> Definieert de huidige werkruimteselectie als het populatiefilter van het model en wordt getekend door bezoekers die aan deze voorwaarde voldoen. De standaardwaarde is "Iedereen". </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Omschrijving complex filter tonen </td> 
   <td colname="col2"> Hiermee worden beschrijvingen van de gedefinieerde filters weergegeven. Klik om de filtrerende manuscripten voor het Positieve HoofdHoofdHoofd en de Filter van de Bevolking te bekijken. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Knooppunten verbergen </td> 
   <td colname="col2"> Hiermee verbergt u knooppunten met slechts een klein percentage van de populatie. Dit menubevel toont slechts wanneer de beslissingsboom wordt getoond. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Verwardmatrix </td> 
   <td colname="col2"> <p>Klikken <span class="uicontrol"> Opties</span> &gt; <span class="uicontrol"> Verwardmatrix</span> om de waarden Accuracy, Recall, Precision en F-Score weer te geven. Hoe dichter bij 100 procent, hoe beter de score. </p> <p>De Verwaringsmatrix geeft vier nauwkeurigheidsgetallen van het model met behulp van een combinatie van waarden: 
     <ul id="ul_D9D512F5D74B44BDBD27B1912DF4CB02"> 
      <li id="li_28C541DF1CB543FEAF2D13C2F329DB52">Werkelijk positief (AP) </li> 
      <li id="li_56233006A1544D95A72CE096CA55C1E6">Voorspeld positief (PP) </li> 
      <li id="li_375FB2D6A0A3418A9AD377C9EBB65386">Werkelijk negatief (AN) </li> 
      <li id="li_07A5D23A36BA4D448C25C1414836EB8E">Voorspeld negatief (PN) </li> 
     </ul> </p> <p>Tip: Deze aantallen worden verkregen door het resulterende scoremodel toe te passen van de 20 percenten testgegevens ingehouden en reeds gekend als ware antwoord. Als de score groter is dan 50 procent, wordt deze voorspeld als een positief geval (dat overeenkomt met het gedefinieerde filter). Dan, Nauwkeurigheid = (TP + TN)/(TP + FP + TN + FN), Herinnering = TP / (TP + FN), en Precisie = TP / (TP + FP). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Legenda weergeven </td> 
   <td colname="col2">Hiermee kunt u een legenda-sleutel in- en uitschakelen in de beslissingsstructuur. <img placement="break" id="image_D5B9415A48C04619955BD96970F720A1" src="assets/decison_tree_legend.png" />Dit menubevel toont slechts wanneer de beslissingsboom wordt getoond. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Geavanceerd </td> 
   <td colname="col2"> Klik om het menu Geavanceerd te openen voor een diepgaand gebruik van de beslissingsstructuur. Zie onderstaande tabel voor menuopties. </td> 
  </tr> 
 </tbody> 
</table>

<table id="table_91E4A74BFB224ABD889147324AC2910F"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Het menu Geavanceerd </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Formaat trainingsset </td> 
   <td colname="col2"> <p>Bepaalt de grootte van de trainingsset die wordt gebruikt voor het modelgebouw. Grotere sets duren langer om te trainen, kleinere sets nemen minder tijd in beslag. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Invoer normaliseren </td> 
   <td colname="col2"> <p> Staat de gebruiker toe om te specificeren of om de Min-Max of de techniek van de Score van Z te gebruiken om input in het model te normaliseren. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> VLOEIENDE overbemonsteringsfactor </td> 
   <td colname="col2"> Wanneer het positieve geval niet zeer vaak (minder dan 10 percenten) in de trainingssteekproef voorkomt, wordt SMOTE gebruikt om extra steekproeven te verstrekken. Met deze optie kan de gebruiker aangeven hoeveel extra samples er met SMOTE worden gemaakt. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Distribution Threshold, klasse Leaf </td> 
   <td colname="col2"> Staat u toe om de drempel te plaatsen die voor een blad tijdens het boombouwproces wordt verondersteld. Standaard moeten alle leden van een knooppunt identiek zijn, anders is het geen blad (vóór het weghalen van het werkgebied). </td> 
  </tr> 
 </tbody> 
</table>
