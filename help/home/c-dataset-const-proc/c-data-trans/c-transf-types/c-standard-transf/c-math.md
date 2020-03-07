---
description: De transformatie van de Wiskunde laat het gebruik van rekenkundige verrichtingen op gebieden binnen de logboekingangen toe.
solution: Analytics
title: Math
topic: Data workbench
uuid: 9e1a5950-8fb2-48e9-b9a1-82c5165fba10
translation-type: tm+mt
source-git-commit: 27600561841db3705f4eee6ff0aeb8890444bbc9

---


# Math{#math}

De transformatie van de Wiskunde laat het gebruik van rekenkundige verrichtingen op gebieden binnen de logboekingangen toe.

De verrichtingen kunnen decimale gehelen en drijvende puntconstanten omvatten.

<table id="table_FDF3DDF1960E43E391A67C9DC2A0E302"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Veld </th> 
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
   <td colname="col1"> Uitdrukking </td> 
   <td colname="col2"> <p>Een rekenkundige uitdrukking die de uit te voeren berekening beschrijft. </p> <p> U kunt om het even welke hieronder vermelde verrichtingen en functies gebruiken, en u kunt gebiedsnamen in de uitdrukking opnemen: </p> <p> Exploitatie 
     <ul id="ul_DB5915FADA0A41A3B11F1F48615F40A9">
      <li id="li_CA9EA97243F04760A81313C17EE057B3"> Toevoeging (+) </li>
      <li id="li_908A272EBA2340098C20F22AA8D9ED26"> Aftrekking (-) </li>
      <li id="li_C62257FF3AAB436D9148BBEA441621D7"> Vermenigvuldiging (*) </li>
      <li id="li_B5A9EAB3E49D4CB9A297172199F23542"> Sector (/) </li>
      <li id="li_D2D2B51DB2C8412A9B6F9D5F3CC03F8A"> Restbedrag (%) </li>
      <li id="li_07E7E368FFD2437A852B785E159848E5"> Uitstel (^) </li>
     </ul></p> <p>Functies 
     <ul id="ul_E335AE8D684340AA998C4A2633FFDEE1">
      <li id="li_E036FF0B5DF244DDBFEDA9BFEDC62251"> sgn(x). Geeft 1 terug als x positief is, 0 als x nul is, of -1 als x negatief is. </li>
      <li id="li_90CD8899DDC14778A95930C2768C82BC"> abs(x). Geeft de absolute waarde van x. </li>
      <li id="li_F4AF23F343F74BD88B7166B1C2BB065E"> vloer(x). Keert het grootste geheel terug minder dan of gelijk aan x. </li>
      <li id="li_A31379A3659240C3A629BFAF19A6DDF1"> ronde(x). Geeft het dichtstbijzijnde gehele getal op x. </li>
      <li id="li_9C0A0F3A4A304026B543F2A64B98B922"> log(b,x). Geeft de logaritme van x base b. </li>
      <li id="li_124D62C2CA5A42CBBCC5DB18FAA8920E"> min(x,y,...). Geeft de kleinste van al zijn argumenten terug. </li>
      <li id="li_3B7B9FC1C0BF4E7688F9F49130B97B7F"> max (x,y,...). Geeft de grootste van al zijn argumenten terug. </li>
     </ul></p> </td> 
   <td colname="col3"></td> 
  </tr> 
  <tr> 
   <td colname="col1"> Uitvoer </td> 
   <td colname="col2"> De naam van het gebied dat het resultaat van de rekenkundige verrichting bevat. </td> 
   <td colname="col3"></td> 
  </tr> 
 </tbody> 
</table>

In dit voorbeeld, dat gebieden van gegevens gebruikt die van websiteverkeer worden verzameld, wordt een nieuw gebied genoemd x-pagina-duur berekend door x-last-pv-timestamp van x-timestamp af te trekken, dan toevoegend 1. De output wordt berekend slechts als het user-defined gebied x-last-pv-timestamp (die timestamp van de laatste paginamening van een bezoeker vertegenwoordigt), bevolkt is, of &quot;niet leeg.&quot;

![](assets/cfg_TransformationType_Math.png)

Voor informatie over de [!DNL Not Empty] aandoening, zie [Voorwaarden](../../../../../home/c-dataset-const-proc/c-conditions/c-abt-cond.md).
