---
description: De transformatie LookupRows bekijkt andere logboekingangen met zelfde volgende identiteitskaart en plaatst de waarde van het outputgebied aan de waarde van een aangewezen gebied in de inputrij.
solution: Analytics
title: LookupRows
topic: Data workbench
uuid: 4cff7cf1-00c8-4ab1-8adc-3805518226d3
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# LookupRows{#lookuprows}

De transformatie LookupRows bekijkt andere logboekingangen met zelfde volgende identiteitskaart en plaatst de waarde van het outputgebied aan de waarde van een aangewezen gebied in de inputrij.

Omdat de [!DNL LookupRows] transformatie zijn raadpleging op logboekingangen en niet raadplegingsdossiers uitvoert, is het zeer gelijkaardig aan de [!DNL CrossRows] transformatie. Zie [CrossRows](../../../../../home/c-dataset-const-proc/c-data-trans/c-transf-types/c-standard-transf/c-crossrows.md#concept-fcace08804f54db397ed631cc13ff4f2).

Om te werken, vereist de [!DNL LookupRows] transformatie dat het gegeven in tijd wordt bevolen en door volgende identiteitskaart in uw brongegevens gegroepeerd. Daarom werkt het [!DNL LookupRows] slechts wanneer bepaald in het [!DNL Transformation.cfg] dossier of in een [!DNL Transformation Dataset Include] dossier.

Aangezien u de beschrijvingen van de parameters in de volgende lijst herziet, herinner het volgende:

* De outputrij is de rij van gegevens waaraan de transformatie op een bepaald punt in tijd werkt.
* De rijen van de input zijn alle andere rijen van gegevens (vóór, na, of met inbegrip van de outputrij) de waarvan waarden van het inputgebied als input aan de transformatie dienen.

<table id="table_AB68A89ECD5C45F39B8433F994BBD7D8"> 
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
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Opmerkingen </td> 
   <td colname="col2"> Optioneel. Opmerkingen over de transformatie. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Toestand </td> 
   <td colname="col2"> Beperkt de output van de transformatie tot bepaalde logboekingangen. Als de voorwaarde niet aan voor een bepaalde logboekingang wordt voldaan, wordt het gebied in de parameter van de Output van de Output van de Waarde van de Rij onveranderd verlaten. De input kan nog worden gebruikt om andere logboekingangen te beïnvloeden. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Invoerconditie </td> 
   <td colname="col2">Accepteert input voor de transformatie van slechts bepaalde inputrijen. Als de Voorwaarde van de <span class="wintitle"> Input</span> niet met voor een bepaalde inputrij wordt voldaan, wordt het inputgebied van die rij genegeerd en beïnvloedt andere outputrijen niet. Nochtans, wordt het outputgebied van die rij nog gewijzigd per de gespecificeerde Voorwaarde. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Invoer van de Rij-sleutel </td> 
   <td colname="col2"> De naam van het gebied aan gebruik als sleutel voor de inputrijen. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Invoerwaarde voor rij </td> 
   <td colname="col2"> De naam van het gebied in de inputrij de waarvan waarde aan het gebied in de parameter van de Output van de Waarde van de Rij van de Output wordt gekopieerd als alle voorwaarden worden tevredengesteld. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Exploitatie </td> 
   <td colname="col2"> <p>Een verrichting die, voor elke outputrij, wordt toegepast op alle inputrijen die aan alle voorwaarden voldoen die door de Belangrijkste parameters van de Input van de Voorwaarde van de <span class="wintitle"> Input</span> en van de Rij van de Input worden bepaald om een output te veroorzaken: 
     <ul id="ul_16FB152CB558497794DDED72A2F05CDD"> 
      <li id="li_22DA9F814E4E42D0B21E90B63A2A7A0E"> EERSTE output de waarde van het gebied in de parameter van de Invoer van de Waarde van de Rij van de Input van de eerste passende inputrij in de gegevens (niet de eerste passende rij na de outputrij). </li> 
      <li id="li_45E00C3DE0494A1CB5C09B942088F161"> LAATSTE output de waarde van het gebied in de parameter van de Invoer van de Waarde van de Rij van de Input van de laatste inputrij in de gegevens (niet de laatste passende rij vóór de outputrij). </li> 
     </ul> </p> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Invoer uitvoerkabel </td> 
   <td colname="col2"> De naam van het gebied aan gebruik als sleutel voor de outputrij. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Uitvoer van de waarde van de Rij van de output </td> 
   <td colname="col2">De naam van het gebied in de outputrij de waarvan waarde van het gebied in de parameter van de Invoer van de Waarde van de Rij van de Input wordt gekopieerd als alle voorwaarden worden tevredengesteld. Alle outputrijen met zelfde x-trackingidentiteitskaart en de Zeer belangrijke <span class="wintitle"> waarden van de Input van de Rij van de </span>Output hebben de zelfde waarde van de Output van de Waarde van de <span class="wintitle"> Rij</span> van de Output. </td> 
   <td colname="col3"> </td> 
  </tr> 
 </tbody> 
</table>

De zeer belangrijke Input van de Rij van de Input, de Input van de Waarde van de Rij van de Input, en de parameters van de Voorwaarde van de Voorwaarde van de Invoer samen bepalen het raadplegingsdossier voor elke volgende identiteitskaart, terwijl de Zeer belangrijke Input van de Rij van de Output, de Input van de Waarde van de Rij van de Output, en de parameters van de Voorwaarde controleren wat omhoog in het dossier wordt gezocht en welke waarde op het gebied wordt opgeslagen dat door de Output wordt gespecificeerd.

Om de verrichting van de transformatie beter te begrijpen, overweeg het volgende overzicht:

* Voor elke outputrij die aan de Toestand voldoet en een niet lege Zeer belangrijke Input van de Rij van de Output heeft:

   * Vind de EERSTE of LAATSTE inputrij dusdanig dat

      * de invoerrij voldoet aan de invoervoorwaarde, en
      * de x-trackingidentiteitskaart van de inputrij gelijk is aan x-trackingidentiteitskaart van de outputrij, en
      * de input van de Rij van de Input Zeer belangrijke Input van de inputrij is de Zeer belangrijke Input van de Rij van de Output van de outputrij;

* en stel de Uitvoer van de Waarde van de Rij van de Output van de outputrij aan de Invoer van de Waarde van de Rij van de Input van de inputrij in.

Overwegingen voor [!DNL LookupRows]

* De lege zeer belangrijke waarden passen nooit om het even wat aan. Zelfs als er inputrijen met lege sleutels en nonblank waarden zijn die aanpassen [!DNL Input Condition], zal een [!DNL Output Row Key Input] van &quot;&quot; altijd een [!DNL Output Row Value Output] van &quot;&quot; veroorzaken.

* Als het niet door wordt verboden, kan een rij omhoog kijken als zijn [!DNL Input Condition]en [!DNL Input Row Key Input] [!DNL Output Row Key Input] waarden het zelfde zijn.

Als u veelvoudige zeer belangrijke waarden hebt, kunt u hen combineren gebruikend een [!DNL Format] transformatie (zie [Formaat](../../../../../home/c-dataset-const-proc/c-data-trans/c-transf-types/c-standard-transf/c-format.md#concept-3de04869181e4694ab072b092186684b)) alvorens een [!DNL LookupRows] transformatie toe te passen.

Veronderstel dat u een website hebt met een pagina voor de registratie van gezelschapsdieren, waar de naam en het ras worden ingevoerd, en een recentere pagina &quot;koop speelgoed&quot;waar slechts de naam van het gezelschapsdier wordt gebruikt. U zou de gezelschapsnaam willen kunnen verbinden met het huisdierenras dat op de registratiepagina wordt ingegaan. Om dit te doen, kon u de volgende [!DNL LookupRows] transformatie tot stand brengen:

![](assets/cfg_TransformationType_LookupRows.png)

Analyseer dit voorbeeld gebruikend het vorige overzicht:

* Voor elke uitvoerrij die voldoet aan een niet-lege waarde van cs-uri-query(petname):

   * Vind de LAATSTE inputrij dusdanig dat

      * de invoerrij bevat een niet-lege waarde van cs-uri-query(petras), en
      * de x-trackingidentiteitskaart van de inputrij gelijk is aan x-trackingidentiteitskaart van de outputrij, en
      * de waarde van cs-uri-query(petname) van de invoerrij is gelijk aan de waarde van cs-uri-query(petname) van de uitvoerrij;

* en stel de waarde van x-pet-ras van de outputrij aan de waarde van cs-uri-vraag (petras) van de inputrij vast.

Bij de [!DNL LookupRows] transformatie wordt de naam van het gezelschapsdier (de sleutel) gebruikt om ervoor te zorgen dat het gezelschapsras gekoppeld is aan zowel de registratie van het gezelschapsdier als de aankoop van speelgoedpagina&#39;s, zodat u het speelgoed dat voor elk gezelschapsras wordt gekocht, kunt analyseren, zelfs voor bezoekers met meerdere huisdieren.
