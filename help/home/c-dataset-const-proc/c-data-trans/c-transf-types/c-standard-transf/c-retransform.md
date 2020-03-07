---
description: De transformatie RETransform (regelmatige uitdrukking) is een patroon-passende transformatie die regelmatige uitdrukkingen gebruikt om een patroon te specificeren om in de input te zoeken en te vangen en het gevangen koord op een aangewezen outputgebied op te slaan.
solution: Analytics
title: RETransform
topic: Data workbench
uuid: 60b5b60e-678a-416d-b5c3-57b1bbefce7d
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# RETransform{#retransform}

De transformatie RETransform (regelmatige uitdrukking) is een patroon-passende transformatie die regelmatige uitdrukkingen gebruikt om een patroon te specificeren om in de input te zoeken en te vangen en het gevangen koord op een aangewezen outputgebied op te slaan.

De regelmatige uitdrukkingen worden geëvalueerd tegen het volledige inputkoord. Als de input niet het patroon aanpast dat in de regelmatige uitdrukking wordt gespecificeerd, wordt geen gegeven gevangen. Voor een korte gids aan het gebruiken van regelmatige uitdrukkingen, zie [Regelmatige Uitdrukkingen](../../../../../home/c-dataset-const-proc/c-reg-exp.md#concept-070077baa419475094ef0469e92c5b9c).

>[!NOTE]
>
>De [!DNL RETransform] transformatie werkt zo ook aan de [!DNL REMatch] transformatie (zie [REMatch](../../../../../home/c-dataset-const-proc/c-data-trans/c-transf-types/c-standard-transf/c-rematch.md#concept-7f0b1caad1df46aabef4448f88261a8e)), die een outputgebied voor elk het vangen subpatroon in de regelmatige uitdrukking construeert. Je kunt denken aan [!DNL RETransform] een combinatie van [!DNL REMatch] en [!DNL Format] transformaties. Als de parameter van de Actie (zie Actie in de volgende lijst) aan &quot;RESULTATEN wordt geplaatst,&quot;dan [!DNL RETransform] werkt als een combinatie van [!DNL REMatch] en [!DNL Union] transformaties.

<table id="table_51B7342E6A5E4E31913BD0F6A6ACC424"> 
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
   <td colname="col1"> Standaard </td> 
   <td colname="col2"> De standaardwaarde om te gebruiken als de voorwaarde wordt voldaan aan en de inputwaarde of niet beschikbaar is of de regelmatige uitdrukking past niet de inputwaarde aan. </td> 
   <td colname="col3"></td> 
  </tr> 
  <tr> 
   <td colname="col1"> Actie </td> 
   <td colname="col2"> <p>Specificeert hoe het resultaat wordt behandeld. Standaard het plaatsen van RESULTATEN neemt eenvoudig de aangepaste patronen en leidt tot een vector van koorden van de patronen die worden gehaald. </p> <p> Alternatief, kan de actie een het formatteren koord zijn om een eenvoudige koordoutput van een bepaald formaat tot stand te brengen. Met deze techniek, specificeert u het aantal dat aan de plaats van elk aangepast patroon tussen % tekens beantwoordt. Bijvoorbeeld, zou het eerste aangepaste patroon %1% zijn, en het derde aangepaste patroon zou %3% zijn. U zou andere karakters in het formatterende koord letterlijk specificeren. </p> </td> 
   <td colname="col3"> RESULTATEN </td> 
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
   <td colname="col1"> Uitvoer </td> 
   <td colname="col2"> De naam van het outputkoord. </td> 
   <td colname="col3"></td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>[!DNL RETransform] de transformaties kunnen zeer langzaam zijn en kunnen voor veel van de gegevensverwerkingstijd rekenschap geven.

Dit voorbeeld isoleert de versie van het werkende systeem van Vensters dat een websitebezoeker gebruikt en leidt tot een gebied x-vensters-versie van die waarde. De outputwaarde in dit geval zou eenvoudig het versieaantal zijn.

![](assets/cfg_TransformationType_RegularExpression.png)

Als u het koord &quot;Versie&quot;voor het versieaantal voor leesbaarheid wilde omvatten, zou u de parameter van de Actie van &quot;RESULTATEN&quot;in &quot;Versie %1%&quot;veranderen.&quot; Om een letterlijk percententeken (%) in uw output te omvatten, ontsnappend het met een tweede percententeken, zoals in &quot;%%.&quot;
