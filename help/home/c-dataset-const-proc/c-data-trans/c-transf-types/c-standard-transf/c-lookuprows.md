---
description: De transformatie LookupRows onderzoekt andere logboekingangen met zelfde volgende identiteitskaart en plaatst de waarde van het outputgebied aan de waarde van een aangewezen gebied in de inputrij.
title: LookupRows
uuid: 4cff7cf1-00c8-4ab1-8adc-3805518226d3
exl-id: caa9a311-b056-4fe8-bb11-1605cc690375
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '946'
ht-degree: 0%

---

# LookupRows{#lookuprows}

{{eol}}

De transformatie LookupRows onderzoekt andere logboekingangen met zelfde volgende identiteitskaart en plaatst de waarde van het outputgebied aan de waarde van een aangewezen gebied in de inputrij.

Omdat [!DNL LookupRows] de transformatie voert zijn raadpleging op logboekingangen uit en niet raadplegingsdossiers, is het zeer gelijkaardig aan [!DNL CrossRows] transformatie. Zie [CrossRows](../../../../../home/c-dataset-const-proc/c-data-trans/c-transf-types/c-standard-transf/c-crossrows.md#concept-fcace08804f54db397ed631cc13ff4f2).

Om te werken, [!DNL LookupRows] voor transformatie moeten de gegevens in de tijd worden geordend en met de tracking-id in de brongegevens worden gegroepeerd. Daarom [!DNL LookupRows] werkt alleen wanneer deze zijn gedefinieerd in het dialoogvenster [!DNL Transformation.cfg] of in een [!DNL Transformation Dataset Include] bestand.

Let op het volgende terwijl u de beschrijvingen van de parameters in de volgende tabel bekijkt:

* De uitvoerrij is de gegevensrij waaraan de transformatie op een bepaald tijdpunt werkt.
* Invoerrijen zijn alle andere rijen met gegevens (voor, na of inclusief de uitvoerrij) waarvan de waarden van het invoerveld fungeren als invoer voor de transformatie.

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
   <td colname="col2"> Beschrijvende naam van de transformatie. U kunt hier elke naam invoeren. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Opmerkingen </td> 
   <td colname="col2"> Optioneel. Opmerkingen over de transformatie. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Voorwaarde </td> 
   <td colname="col2"> Hiermee wordt de uitvoer van de transformatie beperkt tot bepaalde logitems. Als voor een bepaald logbestandvermelding niet aan de voorwaarde wordt voldaan, blijft het veld in de uitvoerwaarde van de rij ongewijzigd. De invoer kan nog worden gebruikt om andere logboekingangen te beïnvloeden. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Invoervoorwaarde </td> 
   <td colname="col2">Accepteert invoer voor de transformatie van alleen bepaalde invoerrijen. Als de <span class="wintitle"> Invoer</span> Er wordt niet voldaan aan de voorwaarde voor een bepaalde invoerrij, het invoerveld van die rij wordt genegeerd en heeft geen invloed op andere uitvoerrijen. Het uitvoerveld van die rij wordt echter nog steeds gewijzigd volgens de opgegeven voorwaarde. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Invoer rijtoets </td> 
   <td colname="col2"> De naam van het veld dat moet worden gebruikt als de sleutel voor de invoerrijen. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Invoer rijwaarde invoeren </td> 
   <td colname="col2"> De naam van het veld in de invoerrij waarvan de waarde naar het veld in de uitvoerwaarde van de rij wordt gekopieerd als aan alle voorwaarden is voldaan. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Bewerking </td> 
   <td colname="col2"> <p>Een bewerking die voor elke uitvoerrij wordt toegepast op alle invoerrijen die voldoen aan alle voorwaarden die zijn gedefinieerd in de <span class="wintitle"> Invoer</span> De parameters Condition en Input Row Key Input om een uitvoer te produceren: 
     <ul id="ul_16FB152CB558497794DDED72A2F05CDD"> 
      <li id="li_22DA9F814E4E42D0B21E90B63A2A7A0E"> EERST geeft als uitvoer de waarde van het veld in de invoerrij-waarde-invoerparameter uit de eerste overeenkomende invoerrij in de gegevens (niet de eerste overeenkomende rij na de uitvoerrij). </li> 
      <li id="li_45E00C3DE0494A1CB5C09B942088F161"> Bij LAATST wordt de waarde van het veld in de invoerrij-invoerparameter uitgevoerd vanaf de laatste invoerrij in de gegevens (niet de laatste overeenkomende rij vóór de uitvoerrij). </li> 
     </ul> </p> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Invoer van rijsleutel uitvoeren </td> 
   <td colname="col2"> De naam van het veld dat moet worden gebruikt als de sleutel voor de uitvoerrij. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Uitvoer van rijwaarde uitvoeren </td> 
   <td colname="col2">De naam van het veld in de uitvoerrij waarvan de waarde uit het veld in de invoerrijwaarde-invoerparameter wordt gekopieerd als aan alle voorwaarden is voldaan. Alle uitvoerrijen met dezelfde x-trackingid en <span class="wintitle"> Invoer van rijsleutel uitvoeren </span>waarden hebben dezelfde <span class="wintitle"> Uitvoer van rijwaarde uitvoeren</span> waarde. </td> 
   <td colname="col3"> </td> 
  </tr> 
 </tbody> 
</table>

De invoerrijsleutelinvoer, de invoer van de Waarde van de Rij, en de parameters van de Voorwaarde van de Input samen bepalen het raadplegingsdossier voor elke volgende identiteitskaart, terwijl de Sleutelinput van de Rij van de Output, de Invoer van de Waarde van de Rij van de Output, en de parameters van de Voorwaarde bepalen wat in het dossier wordt gezocht en welke waarde op het gebied wordt opgeslagen dat door de Output van de Waarde van de Rij wordt gespecificeerd.

Neem de volgende omtrek om de werking van de transformatie beter te begrijpen:

* Voor elke uitvoerrij die aan de voorwaarde voldoet en een niet-lege invoer van de Rij van de Output heeft:

   * Zoek de EERSTE of LAATSTE invoerrij zodanig dat

      * de invoerrij voldoet aan de invoervoorwaarde, en
      * de x-trackingID van de invoerrij gelijk is aan de x-trackingID van de uitvoerrij, en
      * De invoer van de Sleutelinput van de Rij van de Input van de inputrij is gelijk de Sleutelinput van de Rij van de Output van de outputrij.

* en stelt de Output Row Value Output van de uitvoerrij in op de Input Row Value Input van de invoerrij.

Overwegingen voor [!DNL LookupRows]

* Lege sleutelwaarden komen nooit overeen. Zelfs als er invoerrijen zijn met lege sleutels en niet-lege waarden die overeenkomen met [!DNL Input Condition], en [!DNL Output Row Key Input] van &quot;&quot; zal altijd een [!DNL Output Row Value Output] van &quot;&quot;.

* Indien niet verboden door de [!DNL Input Condition], kan een rij zichzelf opzoeken als [!DNL Input Row Key Input] en [!DNL Output Row Key Input] waarden zijn hetzelfde.

Als u meerdere sleutelwaarden hebt, kunt u deze combineren met behulp van een [!DNL Format] transformatie (zie [Indeling](../../../../../home/c-dataset-const-proc/c-data-trans/c-transf-types/c-standard-transf/c-format.md#concept-3de04869181e4694ab072b092186684b)) vóór toepassing van een [!DNL LookupRows] transformatie.

Stel dat u een website hebt met een pagina voor dierenregistratie, waar de naam en het ras worden ingevoerd, en een latere pagina &quot;speelgoed kopen&quot; waarop alleen de naam van het gezelschapsdier wordt gebruikt. U wilt de naam van het gezelschapsdier kunnen koppelen aan het dierenras dat op de registratiepagina is ingevoerd. Hiertoe kunt u het volgende maken: [!DNL LookupRows] transformatie:

![](assets/cfg_TransformationType_LookupRows.png)

Dit voorbeeld analyseren met de vorige omtrek:

* Voor elke uitvoerrij die voldoet aan een niet-lege waarde van cs-uri-query(petname):

   * Zoek de LAATSTE invoerrij zodanig dat

      * de invoerrij bevat een niet-lege waarde van cs-uri-query (petras), en
      * de x-trackingID van de invoerrij gelijk is aan de x-trackingID van de uitvoerrij, en
      * de waarde van cs-uri-query(petname) van de invoerrij is gelijk aan de waarde van cs-uri-query(petname) van de uitvoerrij;

* en stel de waarde van het x-pet-ras van de uitvoerrij in op de waarde van cs-uri-query(petras) van de invoerrij.

De [!DNL LookupRows] bij transformatie wordt de naam van het gezelschapsdier ( de sleutel ) gebruikt om ervoor te zorgen dat het gezelschapsras gekoppeld is aan zowel de registratie als de aankoop van speelgoedpagina &#39; s , zodat u het gekochte speelgoed voor elk gezelschapsras kunt analyseren , zelfs voor bezoekers met meerdere huisdieren .
