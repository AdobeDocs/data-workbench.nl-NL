---
description: De REMatch-transformatie is een patroonovereenkomende transformatie die gebruikmaakt van reguliere expressies om een of meer patronen op te geven die moeten worden gezocht en vastgelegd in de invoer.
title: REMatch
uuid: 8ef80bfa-aea2-45a1-a7d9-38ad33043886
exl-id: 571e6f1c-f557-49c3-9e7c-c31f06132ec7
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '291'
ht-degree: 1%

---

# REMatch{#rematch}

De REMatch-transformatie is een patroonovereenkomende transformatie die gebruikmaakt van reguliere expressies om een of meer patronen op te geven die moeten worden gezocht en vastgelegd in de invoer.

De transformatie maakt een uitvoerveld voor elk onderpatroon van vastlegging in de reguliere expressie. Als de reguliere expressie niet overeenkomt met het invoerveld, zijn de uitvoer leeg en als het uitvoerveld al bestaat, worden de waarden vervangen door de lege waarden. Voor een korte gids aan het gebruiken van regelmatige uitdrukkingen, zie [Gewone Uitdrukkingen](../../../../../home/c-dataset-const-proc/c-reg-exp.md#concept-070077baa419475094ef0469e92c5b9c).

>[!NOTE]
>
>De [!DNL REMatch]-transformatie werkt op dezelfde manier als de [!DNL RETransform]-transformatie (zie [RETransform](../../../../../home/c-dataset-const-proc/c-data-trans/c-transf-types/c-standard-transf/c-retransform.md#concept-23f80aa0bc204565b337e5c4931f6a74)), die reguliere expressies gebruikt om een tekenreeks vast te leggen en die tekenreeks op te slaan in één uitvoerveld.

[!DNL REMatch] parseert een tekenreeks efficiënter dan meerdere  [!DNL RETransform] transformaties of één  [!DNL RETransform] transformatie gevolgd door een  [!DNL Flatten] transformatie. Zie [Afvlakken](../../../../../home/c-dataset-const-proc/c-data-trans/c-transf-types/c-standard-transf/c-flatten.md#concept-7acd351a6d2444bd960ca412ae3333ce).

<table id="table_7077578512B249E986BC79AE770CBD9A"> 
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
   <td colname="col2"> Beschrijvende naam van de transformatie. U kunt hier elke naam invoeren. </td> 
   <td colname="col3"></td> 
  </tr> 
  <tr> 
   <td colname="col1"> Hoofdlettergevoelig </td> 
   <td colname="col2"> Waar of onwaar. Geeft aan of de overeenkomst hoofdlettergevoelig is. </td> 
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
   <td colname="col2"> De reguliere expressie die wordt gebruikt voor overeenkomsten. </td> 
   <td colname="col3"></td> 
  </tr> 
  <tr> 
   <td colname="col1"> Invoer </td> 
   <td colname="col2"> Het veld waartegen de reguliere expressie wordt geëvalueerd. </td> 
   <td colname="col3"></td> 
  </tr> 
  <tr> 
   <td colname="col1"> Uitvoer </td> 
   <td colname="col2"> <p>De naam van de uitvoertekenreeks of vector. In het geval van tekenreeksvectoren als invoer zijn de uitvoer ook tekenreeksvectoren. </p> <p> Er moet een uitvoerveld aanwezig zijn voor elk onderpatroon dat wordt vastgelegd in de expressie. </p> </td> 
   <td colname="col3"></td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>[!DNL REMatch] transformaties kunnen zeer traag zijn en kunnen een groot deel van de verwerkingstijd voor gegevens veroorzaken.

In dit voorbeeld wordt met een transformatie [!DNL REMatch] een datum met de notatie YYYY-MM-DD geparseerd in de velden x-year, x-month en x-day. Voor de datum 2007-01-02 zijn de waarden van x-year, x-month en x-day respectievelijk 2007, 01 en 02.

![](assets/cfg_TransformationType_REMatch.png)
