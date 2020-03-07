---
description: Het menu van de Boom van de Beslissing omvat eigenschappen om het positieve gebruiksgeval, de filters, de opties van de bladdistributie, de verwarringsmatrijs, en andere geavanceerde opties te plaatsen.
title: Opties voor beslissingshiërarchie
uuid: 6439c6d4-60ac-4324-b870-b452a63b7ba1
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Opties voor beslissingshiërarchie{#decision-tree-options}

Het menu van de Boom van de Beslissing omvat eigenschappen om het positieve gebruiksgeval, de filters, de opties van de bladdistributie, de verwarringsmatrijs, en andere geavanceerde opties te plaatsen.

<table id="table_0CBCCB0856E2469EBE8846B413CAB114"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Werkbalkknoppen </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Ga weg </td> 
   <td colname="col2"> Klik om het algoritme van de besluitboom in werking te stellen en de visualisatie te tonen. Dit is grijs-uit tot er input is. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Terugzetten </td> 
   <td colname="col2"> Ontruimt input en besluitboommodel en stelt het proces terug. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Opslaan </td> 
   <td colname="col2"><b>Sla de beslissingshiërarchie</b>op. U kunt de beslissingshiërarchie in verschillende indelingen opslaan: 
    <ul id="ul_F7C7836C06D64912893113E8EEA05704"> 
     <li id="li_D2D8451A679243F1BC67C3B80CA5F83F">Predictive Markup Language (<b>PMML</b>), een op XML gebaseerd dossierformaat dat door toepassingen wordt gebruikt om besluitvormingsboommodellen te beschrijven en te ruilen. </li> 
     <li id="li_88C4B3E050CA4EFC9B7FA8BD446A9C55"><b>Tekst</b> die eenvoudige kolommen en rijen van waar of vals toont, percentages, aantal leden, en inputwaarden. </li> 
     <li id="li_3F871B88F3FA41E9B95EFF5A181E3D57">Een <b>dimensie</b> met bijkantoren die overeenkomt met voorspelde uitkomstelementen. </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Opties </td> 
   <td colname="col2"> Zie onderstaande tabel voor het menu Opties. </td> 
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
   <td colname="col1"> Positieve kwestie instellen </td> 
   <td colname="col2"> Bepaalt de huidige werkruimteselectie als Positief Geval van het model. Ontruimt de zaak als geen selectie bestaat. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Opnamefilter instellen </td> 
   <td colname="col2"> Bepaalt de huidige werkruimteselectie als Filter van de Bevolking van het model en zal van bezoekers worden getrokken die aan deze voorwaarde voldoen. Het gebrek is "Iedereen." </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Complexe filterbeschrijving weergeven </td> 
   <td colname="col2"> De beschrijvingen van vertoningen van de bepaalde filters. Klik om de het filtreren manuscripten voor het Positieve Geval en de Filter van de Bevolking te bekijken. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Knooppunten verbergen </td> 
   <td colname="col2"> De knopen van huiden met slechts een klein percentage van de bevolking. Dit menubevel toont slechts wanneer de besluitboom wordt getoond. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Verwarde matrix </td> 
   <td colname="col2"> <p>Klik op <span class="uicontrol"> Opties</span> &gt; <span class="uicontrol"> Verfusiematrix</span> om de waarden Accuracy, Recall, Precision en F-Score weer te geven. Hoe dichter bij 100 procent, hoe beter de score. </p> <p>De fusiematrix geeft vier nauwkeurigheidsgetallen van het model met behulp van een combinatie van waarden: 
     <ul id="ul_D9D512F5D74B44BDBD27B1912DF4CB02"> 
      <li id="li_28C541DF1CB543FEAF2D13C2F329DB52">Werkelijk positief (AP) </li> 
      <li id="li_56233006A1544D95A72CE096CA55C1E6">Voorspeld positief (PP) </li> 
      <li id="li_375FB2D6A0A3418A9AD377C9EBB65386">Werkelijk negatief (AN) </li> 
      <li id="li_07A5D23A36BA4D448C25C1414836EB8E">Voorspeld negatief (PN) </li> 
     </ul> </p> <p>Tip:  Deze aantallen worden verkregen door het resulterende het noteren model van de 20 percenten het testen gegevens toe te passen die worden ingehouden en reeds gekend als het ware antwoord. Als de score groter is dan 50 percenten, wordt het voorspeld als positief geval (dat de bepaalde filter aanpast). Dan, Nauwkeurigheid = (TP + TN)/(TP + FP + TN + FN), Rappel = TP / (TP + FN), en Precision = TP / (TP + FP). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Legenda weergeven </td> 
   <td colname="col2">Staat u toe om een legendesleutel in en uit in de Beslissingsboom van een knevel te voorzien. <img placement="break" id="image_D5B9415A48C04619955BD96970F720A1" src="assets/decison_tree_legend.png" />Dit menubevel toont slechts wanneer de besluitboom wordt getoond. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Geavanceerd </td> 
   <td colname="col2"> Klik om Geavanceerd menu voor diepgaand gebruik van de Boom van de Beslissing te openen. Zie onderstaande tabel voor menuopties. </td> 
  </tr> 
 </tbody> 
</table>

<table id="table_91E4A74BFB224ABD889147324AC2910F"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Geavanceerd menu </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Grootte van trainingsset </td> 
   <td colname="col2"> <p>Controleert de grootte van de opleidingsreeks die voor het modelgebouw wordt gebruikt. Grotere sets duren langer om te trainen, kleinere sets nemen minder tijd in beslag. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Invoernormalisatie </td> 
   <td colname="col2"> <p> Staat de gebruiker toe om te specificeren of om de Min-Maximum of de techniek van de Score van Z te gebruiken om input in het model te normaliseren. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> SMOTE-overbemonsteringsfactor </td> 
   <td colname="col2"> Wanneer het Positieve Geval niet zeer vaak (minder dan 10 percenten) in de trainingssteekproef voorkomt, wordt SMOTE gebruikt om extra steekproeven te verstrekken. Deze optie staat de gebruiker toe om op te wijzen hoeveel meer steekproeven om het gebruiken van SMOTE tot stand te brengen. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Drempelwaarde voor de verdeling van de bladklasse </td> 
   <td colname="col2"> Staat u toe om de drempel te plaatsen die voor een blad tijdens het proces van de boombouw wordt verondersteld. Door gebrek, moeten alle leden van een knoop identiek zijn voor het om een blad (voorafgaand aan het snoeien stadium) te zijn. </td> 
  </tr> 
 </tbody> 
</table>

