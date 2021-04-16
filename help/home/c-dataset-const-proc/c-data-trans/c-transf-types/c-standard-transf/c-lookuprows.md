---
description: De transformatie LookupRows onderzoekt andere logboekingangen met zelfde volgende identiteitskaart en plaatst de waarde van het outputgebied aan de waarde van een aangewezen gebied in de inputrij.
title: LookupRows
uuid: 4cff7cf1-00c8-4ab1-8adc-3805518226d3
exl-id: caa9a311-b056-4fe8-bb11-1605cc690375
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '946'
ht-degree: 0%

---

# LookupRows{#lookuprows}

De transformatie LookupRows onderzoekt andere logboekingangen met zelfde volgende identiteitskaart en plaatst de waarde van het outputgebied aan de waarde van een aangewezen gebied in de inputrij.

Omdat de [!DNL LookupRows] transformatie zijn raadpleging op logboekingangen en niet raadplegingsdossiers uitvoert, is het zeer gelijkaardig aan de [!DNL CrossRows] transformatie. Zie [CrossRows](../../../../../home/c-dataset-const-proc/c-data-trans/c-transf-types/c-standard-transf/c-crossrows.md#concept-fcace08804f54db397ed631cc13ff4f2).

Om te werken, vereist de [!DNL LookupRows] transformatie dat de gegevens in tijd worden bevolen en door volgende identiteitskaart in uw brongegevens worden gegroepeerd. [!DNL LookupRows] werkt daarom alleen wanneer dit is gedefinieerd in het [!DNL Transformation.cfg]-bestand of in een [!DNL Transformation Dataset Include]-bestand.

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
   <td colname="col2">Accepteert invoer voor de transformatie van alleen bepaalde invoerrijen. Als aan de voorwaarde <span class="wintitle"> Invoer</span> voor een bepaalde inputrij niet wordt voldaan, wordt het inputgebied van die rij genegeerd en beïnvloedt geen andere outputrijen. Het uitvoerveld van die rij wordt echter nog steeds gewijzigd volgens de opgegeven voorwaarde. </td> 
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
   <td colname="col2"> <p>Een bewerking die voor elke uitvoerrij wordt toegepast op alle invoerrijen die voldoen aan alle voorwaarden die zijn gedefinieerd door de parameters <span class="wintitle"> Invoer</span> Condition and Input Row Key Input om een uitvoer te produceren: 
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
   <td colname="col2">De naam van het veld in de uitvoerrij waarvan de waarde uit het veld in de invoerrijwaarde-invoerparameter wordt gekopieerd als aan alle voorwaarden is voldaan. Alle uitvoerrijen met dezelfde waarden voor x-trackingid en <span class="wintitle"> Invoer uitvoerrij </span>hebben dezelfde waarde voor <span class="wintitle"> Waarde uitvoerrij</span>. </td> 
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

* Lege sleutelwaarden komen nooit overeen. Zelfs als er invoerrijen met lege sleutels en nonblank waarden zijn die [!DNL Input Condition] aanpassen, zal een [!DNL Output Row Key Input] van &quot;&quot; altijd een [!DNL Output Row Value Output] van &quot;&quot; produceren.

* Als de [!DNL Input Condition] dit niet toestaat, kan een rij zichzelf opzoeken als de [!DNL Input Row Key Input]- en [!DNL Output Row Key Input]-waarden gelijk zijn.

Als u veelvoudige zeer belangrijke waarden hebt, kunt u hen combineren gebruikend een [!DNL Format] transformatie (zie [Formaat](../../../../../home/c-dataset-const-proc/c-data-trans/c-transf-types/c-standard-transf/c-format.md#concept-3de04869181e4694ab072b092186684b)) alvorens een [!DNL LookupRows] transformatie toe te passen.

Stel dat u een website hebt met een pagina voor dierenregistratie, waar de naam en het ras worden ingevoerd, en een latere pagina &quot;speelgoed kopen&quot; waarop alleen de naam van het gezelschapsdier wordt gebruikt. U wilt de naam van het gezelschapsdier kunnen koppelen aan het dierenras dat op de registratiepagina is ingevoerd. Hiervoor kunt u de volgende [!DNL LookupRows]-transformatie maken:

![](assets/cfg_TransformationType_LookupRows.png)

Dit voorbeeld analyseren met de vorige omtrek:

* Voor elke uitvoerrij die voldoet aan een niet-lege waarde van cs-uri-query(petname):

   * Zoek de LAATSTE invoerrij zodanig dat

      * de invoerrij bevat een niet-lege waarde van cs-uri-query (petras), en
      * de x-trackingID van de invoerrij gelijk is aan de x-trackingID van de uitvoerrij, en
      * de waarde van cs-uri-query(petname) van de invoerrij is gelijk aan de waarde van cs-uri-query(petname) van de uitvoerrij;

* en stel de waarde van het x-pet-ras van de uitvoerrij in op de waarde van cs-uri-query(petras) van de invoerrij.

Bij de [!DNL LookupRows]-transformatie wordt de naam van het gezelschapsdier (de sleutel) gebruikt om ervoor te zorgen dat het gezelschapsras gekoppeld is aan zowel de registratie van gezelschapsdieren als de pagina&#39;s voor speelgoed, zodat u het speelgoed kunt analyseren dat voor elk gezelschapsras is gekocht, zelfs voor bezoekers met meerdere huisdieren.
