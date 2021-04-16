---
description: Met de Math-transformatie kunt u rekenkundige bewerkingen toepassen op velden in de logbestandvermeldingen.
title: Math
uuid: 9e1a5950-8fb2-48e9-b9a1-82c5165fba10
exl-id: d8b9cacd-67d1-447c-94dd-7028aa371dfa
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '256'
ht-degree: 1%

---

# Math{#math}

Met de Math-transformatie kunt u rekenkundige bewerkingen toepassen op velden in de logbestandvermeldingen.

De bewerkingen kunnen decimale gehele getallen en constanten met drijvende komma bevatten.

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
   <td colname="col2"> Beschrijvende naam van de transformatie. U kunt hier elke naam invoeren. </td> 
   <td colname="col3"></td> 
  </tr> 
  <tr> 
   <td colname="col1"> Opmerkingen </td> 
   <td colname="col2"> Optioneel. Opmerkingen over de transformatie. </td> 
   <td colname="col3"></td> 
  </tr> 
  <tr> 
   <td colname="col1"> Voorwaarde </td> 
   <td colname="col2"> De omstandigheden waaronder deze transformatie wordt toegepast. </td> 
   <td colname="col3"></td> 
  </tr> 
  <tr> 
   <td colname="col1"> Uitdrukking </td> 
   <td colname="col2"> <p>Een rekenkundige expressie die de uit te voeren berekening beschrijft. </p> <p> U kunt alle hieronder vermelde bewerkingen en functies gebruiken en u kunt veldnamen in de expressie opnemen: </p> <p> Bewerkingen 
     <ul id="ul_DB5915FADA0A41A3B11F1F48615F40A9">
      <li id="li_CA9EA97243F04760A81313C17EE057B3"> Optellen (+) </li>
      <li id="li_908A272EBA2340098C20F22AA8D9ED26"> Aftrekken (-) </li>
      <li id="li_C62257FF3AAB436D9148BBEA441621D7"> Vermenigvuldigen (*) </li>
      <li id="li_B5A9EAB3E49D4CB9A297172199F23542"> Sector (/) </li>
      <li id="li_D2D2B51DB2C8412A9B6F9D5F3CC03F8A"> Herinnering (%) </li>
      <li id="li_07E7E368FFD2437A852B785E159848E5"> Exponentiatie (^) </li>
     </ul></p> <p>Functies 
     <ul id="ul_E335AE8D684340AA998C4A2633FFDEE1">
      <li id="li_E036FF0B5DF244DDBFEDA9BFEDC62251"> sgn(x). Retourneert 1 als x positief is, 0 als x nul is, of -1 als x negatief is. </li>
      <li id="li_90CD8899DDC14778A95930C2768C82BC"> abs(x). Retourneert de absolute waarde van x. </li>
      <li id="li_F4AF23F343F74BD88B7166B1C2BB065E"> floor(x). Retourneert het grootste gehele getal dat kleiner dan of gelijk is aan x. </li>
      <li id="li_A31379A3659240C3A629BFAF19A6DDF1"> round(x). Retourneert het dichtstbijzijnde gehele getal tot x. </li>
      <li id="li_9C0A0F3A4A304026B543F2A64B98B922"> log(b,x). Retourneert de logaritme van x base b. </li>
      <li id="li_124D62C2CA5A42CBBCC5DB18FAA8920E"> min(x,y,...). Retourneert het kleinste van alle argumenten. </li>
      <li id="li_3B7B9FC1C0BF4E7688F9F49130B97B7F"> max(x,y,...). Retourneert het grootste van alle argumenten. </li>
     </ul></p> </td> 
   <td colname="col3"></td> 
  </tr> 
  <tr> 
   <td colname="col1"> Uitvoer </td> 
   <td colname="col2"> De naam van het veld dat het resultaat van de rekenkundige bewerking bevat. </td> 
   <td colname="col3"></td> 
  </tr> 
 </tbody> 
</table>

In dit voorbeeld, dat gegevensvelden gebruikt die uit websiteverkeer worden verzameld, wordt een nieuw gebied genoemd x-page-duration berekend door x-last-pv-timestamp van x-timestamp af te trekken, dan toevoegend 1. De uitvoer wordt alleen berekend als het door de gebruiker gedefinieerde veld x-last-pv-timestamp (die de tijdstempel van de laatste paginaweergave van een bezoeker vertegenwoordigt) is ingevuld of &quot;niet leeg&quot; is.

![](assets/cfg_TransformationType_Math.png)

Voor informatie over [!DNL Not Empty] voorwaarde, zie [Voorwaarden](../../../../../home/c-dataset-const-proc/c-conditions/c-abt-cond.md).
