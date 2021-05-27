---
description: Met een tijddimensie kunt u een set periodieke of absolute lokale tijdafmetingen maken (zoals Dag, Dag van Week, Uur van Dag, Reserveringstijd enzovoort) op basis van een tijdstempelveld dat u opgeeft voor de parameter Invoertijd (1970 tijdperk).
title: Dimension tijd
uuid: b633cf4f-0db4-4378-9e59-43b6ad8f772d
exl-id: f9534b24-3a16-4220-bac2-bc541e121005
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '465'
ht-degree: 1%

---

# Tijd Dimension{#time-dimensions}

Met een tijddimensie kunt u een set periodieke of absolute lokale tijdafmetingen maken (zoals Dag, Dag van Week, Uur van Dag, Reserveringstijd enzovoort) op basis van een tijdstempelveld dat u opgeeft voor de parameter Invoertijd (1970 tijdperk).

Wanneer u tijdafmetingen definieert, kunt u ook een andere dag dan maandag kiezen die als het begin van een week moet worden gebruikt door de parameter Begindag week op te geven. U kunt meer dan één reeks tijddimensies in uw dataset bepalen zolang de afmetingen verschillende namen hebben.

De tijdafmetingen worden gedefinieerd door de volgende parameters:

<table id="table_9734F6CD7ABA4661A2F9A5FB948A7282"> 
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
   <td colname="col2"> Beschrijvende naam van de dimensie zoals deze wordt weergegeven in de werkbank voor gegevens. De naam van de dimensie mag geen afbreekstreepje (-) bevatten. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Opmerkingen </td> 
   <td colname="col2"> Optioneel. Opmerkingen over de uitgebreide dimensie. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Dimensies </td> 
   <td colname="col2"> <p>U kunt dimensienamen voor om het even welke volgende periodes specificeren: </p> <p> 
     <ul id="ul_EB0837DD66BE4004A615A6029EEF4CD5"> 
      <li id="li_2E46E6DB004E443C8CC831DCEE743D60"> Dag </li> 
      <li id="li_F59A27779EBE4E2A84E0972EE8BCDFA7"> Weekdag </li> 
      <li id="li_7D74CD547ED1449091EF7B2E0E8C46DE"> Uur </li> 
      <li id="li_706AF9D385CB44C098DEBACA3BA2CD4B"> Uur van dag </li> 
      <li id="li_76FBF69B25954885A0192D308A155E41"> Maand </li> 
      <li id="li_3C16955BE5C54291A25E25CD31259661"> Week </li> 
     </ul> </p> <p> De namen die u hier invoert zijn de namen die in dimensiemenu's en in visualisaties in gegevenswerkbank verschijnen. Als u de naam van een tijddimensie leeg verlaat, wordt de dimensie niet gecreeerd in de dataset. </p> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Verborgen </td> 
   <td colname="col2"> Hiermee wordt bepaald of de dimensie wordt weergegeven in de interface van de gegevenswerkbank. Deze parameter is standaard ingesteld op false. Als de afmeting bijvoorbeeld alleen als basis van een metrische waarde moet worden gebruikt, kunt u deze parameter instellen op true om de afmeting te verbergen in de weergave op de werkbank. </td> 
   <td colname="col3"> true </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Invoertijd (1970 tijdperk) </td> 
   <td colname="col2"> <p>De naam van het tijdstempelveld dat als invoer moet worden gebruikt. </p> <p> <p>Opmerking:  De waarden van het veld moeten het aantal seconden weergeven dat is verstreken sinds 1 januari 1970, 00:00:01. Als de invoertijd geen geldige tijd is (1970 tot 2037), zal het transformatieproces ontbreken, en de server van de gegevenswerkbank zal een fout produceren. </p> </p> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Bovenliggend </td> 
   <td colname="col2"> De naam van de bovenliggende dimensie. Elke aftelbare dimensie kan een bovenliggende dimensie zijn. Voor webgegevens is Sessie de bovenliggende map. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Begindag week </td> 
   <td colname="col2"> <p>De dag die als de eerste dag van een week moet worden gebruikt. </p> <p> Deze parameter beïnvloedt de Weekdimensie, de dimensie van de Dag van Week, en om het even welke rapporteringstijddimensies die in termen van weken worden bepaald. </p> </td> 
   <td colname="col3"> Mon </td> 
  </tr> 
 </tbody> 
</table>

In dit voorbeeld wordt een set tijdafmetingen gemaakt op basis van het door de gebruiker gedefinieerde invoerveld x-time-1970. De reeks tijdafmetingen heeft de naam &quot;Sessietijd&quot;. Omdat de ouder van elke afmeting de afmeting van de Zitting is, beantwoordt elk element van de tijddimensies aan de tijd waarop een zitting begon. De parameter van de Dag van het Begin van de Week specificeert dat elke week van de dimensie van de Week op maandag begint.

![](assets/cfg_Transformation_Dim_TimeDim.png)
