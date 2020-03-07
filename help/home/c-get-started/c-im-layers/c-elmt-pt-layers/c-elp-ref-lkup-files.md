---
description: Wanneer het creëren van een laag van het elementenpunt die verwijzingen een raadplegingsdossier om breedtegraad en lengtegegevens te verkrijgen, wordt de plaats van het punt verkregen door elk element en zijn bijbehorende breedtegraad en lengtegraad uit het raadplegingsdossier terug te winnen.
solution: Analytics
title: Bepaal de lagen van het elementenpunt die raadplegingsdossiers van verwijzingen voorzien
topic: Data workbench
uuid: 32c8de7a-4316-4f91-9810-7f584bc7fb0b
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Bepaal de lagen van het elementenpunt die raadplegingsdossiers van verwijzingen voorzien{#define-element-point-layers-referencing-lookup-files}

Wanneer het creëren van een laag van het elementenpunt die verwijzingen een raadplegingsdossier om breedtegraad en lengtegegevens te verkrijgen, wordt de plaats van het punt verkregen door elk element en zijn bijbehorende breedtegraad en lengtegraad uit het raadplegingsdossier terug te winnen.

>[!NOTE]
>
>In plaats van het gebruiken van een raadplegingsdossier, kunt u de Dynamische functionaliteit van Punten gebruiken, die de breedte en de lengtegraad van een plaats in de naam van elk element van een afmeting inbedt. Zie het [bepalen van de Lagen van het Punt van het Element Gebruikend Dynamische Punten](../../../../home/c-get-started/c-im-layers/c-elmt-pt-layers/c-elmt-pt-dyn-pts.md#concept-51adc5e1df8a48e7bd7a582967e4c512).

Om een laag van het elementenpunt te bepalen dat de verwijzingen een raadplegingsdossier, u moeten tot stand brengen of reeds beschikbaar het volgende hebben:

* **Een dimensie** die in het [!DNL Transformation.cfg file] of een [!DNL transformation dataset include] dossier wordt bepaald. Voor informatie over de dossiers van de transformatieconfiguratie, zie de Gids *van de Configuratie van de* Dataset.

* **Een raadplegingsdossier** dat de gegevens bevat die worden gebruikt om elk gegevenspunt te plot. Dit dossier moet minstens drie kolommen van gegevens voor elk gegevenspunt bevatten: de sleutel, de lengtegraad, en de breedtegraad. Voor meer informatie over het vereiste formaat van het raadplegingsdossier, zie het Formaat [van het Dossier van de Laag van het Punt van het](../../../../home/c-get-started/c-im-layers/c-elmt-pt-layers/c-elp-ref-lkup-files.md#section-52d7e92be8354d979af9e7a2210b76f2)Element.

* **Een laagdossier** dat de plaats van het raadplegingsdossier specificeert en de verwante afmeting en metrisch evenals de sleutel, de lengtegraad, en de namen van de breedtelijn in het raadplegingsdossier identificeert. Voor meer informatie over het vereiste formaat van het laagdossier, zie het Formaat [van het Dossier van de Laag van het Punt van het](../../../../home/c-get-started/c-im-layers/c-elmt-pt-layers/c-elp-ref-lkup-files.md#section-52d7e92be8354d979af9e7a2210b76f2)Element.

   >[!NOTE]
   >
   >Het [!DNL Zip Points.layer] dossier, dat van het [!DNL Geography] profiel wordt voorzien, is een laag van het elementenpunt die het [!DNL Zipcode.dim] dossier, het [!DNL Sessions.metric] dossier, het [!DNL Zip Points.txt] raadplegingsdossier, en de namen van de sleutel, de lengte, de breedtegraad, en de naamkolommen in het raadplegingsdossier identificeert.

## Het dossierformaat van de puntraadpleging van het element {#section-0bc8c652c1bd40eb84078f2af71a5c06}

Het de raadplegingsdossier van de elementenpuntlaag moet minstens de volgende drie kolommen bevatten:

* **[!DNL Key]kolom:**Deze kolom zou gemeenschappelijke zeer belangrijke gegevens moeten bevatten, die de server van de Werkbank van Gegevens toelaat om de gegevens in het raadplegingsdossier met dat in de dataset te verbinden. De[!DNL key]kolom moet de eerste kolom in het raadplegingsdossier zijn. Elke rij in deze kolom identificeert een element van de afmeting.

* **[!DNL Longitude]kolom:**Deze kolom zou de lengtegraad voor elk gegevenspunt in de[!DNL Key]kolom moeten bevatten.

* **[!DNL Latitude]kolom:**Deze kolom zou de breedtegraad voor elk gegevenspunt in de[!DNL Key]kolom moeten bevatten.

* **[!DNL Name]kolom (facultatief):**Als u een naam wilt specificeren die op de kaart voor elk gegevenspunt moet worden getoond, kunt u een[!DNL Name]kolom in het raadplegingsdossier omvatten.

Elke rij in het [!DNL Zip Points.txt] raadplegingsdossier bevat een Code van het PIT in de eerste kolom die door de lengtegraad, de breedtegraad, en de bijbehorende stadsnaam wordt gevolgd.

```
tude, and associated city name.
ZIP_CODE LATITUDE LONGITUDE NAME
00210 +43.005895 -071.013202 PORTSMOUTH, NH
00211 +43.005895 -071.013202 PORTSMOUTH, NH
...
```

## Bestandsindeling voor elementenlaag {#section-52d7e92be8354d979af9e7a2210b76f2}

Elk [!DNL .layer] dossier van de elementenpuntlaag dat de verwijzingen een raadplegingsdossier moeten worden geformatteerd gebruikend het volgende malplaatje:

```
Layer = ElementPointLayer:
  Data Paths = vector: 1 items
    0 = Path: Maps\\Lookup File Name.txt
  Longitude Column = string: Longitude Column Name
  Latitude Column = string: Latitude Column Name
  Name Column = string: Location Column Name
  Key Column = string: Key Column Name
  Dimension = ref: wdata/model/dim/Dimension Name
  Metric = ref: wdata/model/metric/Metric Name
  Scale = double: Scale
  Color = v3d: RGB Color Vector
  Rendering Mode = int: Mode Number
```

<table id="table_7287F8869DD04886BE1477CBB11EB796"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Parameter </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Gegevenspaden </td> 
   <td colname="col2"> Weg aan het raadplegingsdossier dat breedte en lengtegegevens bevat. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Lengtegronden </td> 
   <td colname="col2"> De naam van de kolom in het raadplegingsdossier dat de lengtegegevens bevat. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Latitude-kolom </td> 
   <td colname="col2"> De naam van de kolom in het raadplegingsdossier dat de breedtegraad gegevens bevat. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Naam kolom </td> 
   <td colname="col2"> Optioneel. De naam van de kolom in het raadplegingsdossier dat de namen van de plaatsen bevat die door de breedtegraad en lengtegegevens worden vertegenwoordigd. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Sleutelkolom </td> 
   <td colname="col2"> <p>De naam van de kolom in het raadplegingsdossier dat de gemeenschappelijke zeer belangrijke gegevens bevat, die de server van de Werkbank van Gegevens toelaat om de gegevens in het raadplegingsdossier in de dataset te integreren. Dit moet de eerste kolom in het raadplegingsdossier zijn. </p> <p>Elke rij in deze kolom is een element van een afmeting. Deze dimensie moet in het <span class="filepath"> Transformation.cfg</span> - dossier of een <span class="wintitle"> transformatiedataset worden bepaald omvat</span> dossier en in de parameter van de Dimensie van dit dossier gespecificeerd. Voor meer informatie over de dossiers van de transformatieconfiguratie, zie de Gids <i>van de Configuratie van de</i>Dataset. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Afmetingen </td> 
   <td colname="col2">De naam van de afmeting (die in een dossier van de transformatieconfiguratie wordt bepaald) die elementen bevat die aan de gegevensrijen in de <span class="wintitle"> Zeer belangrijke</span> kolom beantwoorden. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Metrisch </td> 
   <td colname="col2"> De naam van metrisch die over de afmeting wordt geëvalueerd die in de parameter van de Afmeting wordt gespecificeerd. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Schaal </td> 
   <td colname="col2"> Optioneel. Waarde die wordt gebruikt om de punten in de laag te rangschikken. De standaardwaarde is 100. De grotere waarden maken de punten groter, en de kleinere waarden maken hen kleiner. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Kleur </td> 
   <td colname="col2"> Optioneel. De RGB kleurenvector, die als (rood, groen, blauw) wordt uitgedrukt. Voor elke kleur in de vector, kunt u een waarde van 0.0 tot 1.0 ingaan. Bijvoorbeeld, (1.0, 0.0, 0.0) is fel rood, en (0.5, 0.5, 0.5, 0.5) is grijs. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Rendermodus </td> 
   <td colname="col2"> <p>Optioneel. De waarde die van het geheel de teruggevende wijze vertegenwoordigt voor de laag te gebruiken. De drie beschikbare wijzen zijn als volgt: 
     <ul id="ul_F15E43B3BFE54CDD8026837027E25819"> 
      <li id="li_5405D939540E4D0FA7828D2623D72C44">Rendermodus 1. De grootte van punten wordt bepaald in het schermruimte (de punten blijven een constante grootte met betrekking tot het computerscherm). De punten worden teruggegeven gebruikend veelhoeken, zodat is er geen bovengrens op puntgrootte. Dit is het gebrek dat wijze teruggeeft. </li> 
      <li id="li_61C5AA926777449E8804C7BCE9E46F9B">Rendermodus 2. De grootte van het punt wordt bepaald in wereldruimte (de punten blijven een constante grootte met betrekking tot de bol). De punten worden teruggegeven gebruikend veelhoeken, zodat is er geen bovengrens op puntgrootte. </li> 
      <li id="li_C00527F959354D3BB7422EFFE1FB5135">Rendermodus 3. De grootte van het punt wordt bepaald in het schermruimte. De punten worden teruggegeven gebruikend gladde punten OpenGL. </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

Het [!DNL Zip Points.layer] bestand is als volgt geformatteerd:

```
Layer = ElementPointLayer:
  Data Paths = vector: 1 items
    0 = Path: Maps\\Zip Points.txt
  Longitude Column = string: LONGITUDE
  Latitude Column = string: LATITUDE
  Name Column = string: NAME
  Key Column = string: ZIP_CODE
  Dimension = ref: wdata/model/dim/Zipcode
  Metric = ref: wdata/model/metric/Sessions
```

