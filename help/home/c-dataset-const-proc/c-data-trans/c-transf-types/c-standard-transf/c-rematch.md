---
description: De transformatie REMatch is een patroon-passende transformatie die regelmatige uitdrukkingen gebruikt om één of meerdere patronen te specificeren om in de input te zoeken en te vangen.
solution: Analytics
title: REMatch
topic: Data workbench
uuid: 8ef80bfa-aea2-45a1-a7d9-38ad33043886
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# REMatch{#rematch}

De transformatie REMatch is een patroon-passende transformatie die regelmatige uitdrukkingen gebruikt om één of meerdere patronen te specificeren om in de input te zoeken en te vangen.

De transformatie construeert een outputgebied voor elke het vangen subpatroon in de regelmatige uitdrukking. Als de regelmatige uitdrukking niet het inputgebied aanpast, zijn de output leeg, en als het outputgebied reeds bestaat, worden de waarden vervangen door de lege waarden. Voor een korte gids aan het gebruiken van regelmatige uitdrukkingen, zie [Regelmatige Uitdrukkingen](../../../../../home/c-dataset-const-proc/c-reg-exp.md#concept-070077baa419475094ef0469e92c5b9c).

>[!NOTE]
>
>De [!DNL REMatch] transformatie werkt zo ook aan de [!DNL RETransform] transformatie (zie [RETransform](../../../../../home/c-dataset-const-proc/c-data-trans/c-transf-types/c-standard-transf/c-retransform.md#concept-23f80aa0bc204565b337e5c4931f6a74)), die regelmatige uitdrukkingen gebruikt om een koord te vangen en dat koord op één enkel outputgebied op te slaan.

[!DNL REMatch] ontleedt een koord efficiënter dan veelvoudige [!DNL RETransform] transformaties of één enkele [!DNL RETransform] transformatie die door een [!DNL Flatten] transformatie wordt gevolgd. Zie [Flatten](../../../../../home/c-dataset-const-proc/c-data-trans/c-transf-types/c-standard-transf/c-flatten.md#concept-7acd351a6d2444bd960ca412ae3333ce).

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
   <td colname="col2"> Beschrijvende naam van de transformatie. U kunt om het even welke naam hier ingaan. </td> 
   <td colname="col3"></td> 
  </tr> 
  <tr> 
   <td colname="col1"> Gevallengevoelig </td> 
   <td colname="col2"> Waar of vals. Specificeert of de gelijke case-sensitive is. </td> 
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
   <td colname="col2"> De regelmatige uitdrukking die voor aanpassing wordt gebruikt. </td> 
   <td colname="col3"></td> 
  </tr> 
  <tr> 
   <td colname="col1"> Invoer </td> 
   <td colname="col2"> Het gebied waartegen de regelmatige uitdrukking wordt geëvalueerd. </td> 
   <td colname="col3"></td> 
  </tr> 
  <tr> 
   <td colname="col1"> Resultaten </td> 
   <td colname="col2"> <p>De naam van het outputkoord of de vector. In het geval van koordvectoren als input, zijn de output ook koordvectoren. </p> <p> Een outputgebied moet voor elk het vangen subpatroon in de uitdrukking bestaan. </p> </td> 
   <td colname="col3"></td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>[!DNL REMatch] de transformaties kunnen zeer langzaam zijn en kunnen voor veel van de gegevensverwerkingstijd rekenschap geven.

In dit voorbeeld, ontleedt een [!DNL REMatch] transformatie een datum van het formaat JJJJ-MM-DD in de gebieden x-jaar, x-maand, en x-dag. Voor de datum 2007-01-02 zouden de waarden van x jaar, x maand, en x-dag respectievelijk 2007, 01, en 02 zijn.

![](assets/cfg_TransformationType_REMatch.png)

