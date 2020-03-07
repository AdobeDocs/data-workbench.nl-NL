---
description: Het formatteren van informatie over het de laagdossier van het elementenpunt.
solution: Analytics
title: Element Point Layer File Format
topic: Data workbench
uuid: a8b3d2f4-0ed2-480d-a2a6-75d43025a579
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Element Point Layer File Format{#element-point-layer-file-format}

Het formatteren van informatie over het de laagdossier van het elementenpunt.

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

<table id="table_B2BC5FE8C80E4680B9A565878192D75B"> 
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
   <td colname="col2"> <p>De naam van de kolom in het raadplegingsdossier dat de gemeenschappelijke zeer belangrijke gegevens bevat, die de server van de gegevenswerkbank toelaat om de gegevens in het raadplegingsdossier in de dataset te integreren. Dit moet de eerste kolom in het raadplegingsdossier zijn. </p> <p>Elke rij in deze kolom is een element van een afmeting. Deze dimensie moet in het <span class="filepath"> Transformation.cfg</span> - dossier of een transformatiedataset worden bepaald omvat dossier en gespecificeerd in de parameter van de Dimensie van dit dossier. Voor meer informatie over de dossiers van de transformatieconfiguratie, zie de Gids <i>van de Configuratie van de</i>Dataset. </p> </td> 
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
     <ul id="ul_CBB26B32505846A39FEB85E831E1C7AB"> 
      <li id="li_B31528A8858C4418ABCDFF0B4EFB25D7">Rendermodus 1. De grootte van punten wordt bepaald in het schermruimte (de punten blijven een constante grootte met betrekking tot het computerscherm). De punten worden teruggegeven gebruikend veelhoeken, zodat is er geen bovengrens op puntgrootte. Dit is het gebrek dat wijze teruggeeft. </li> 
      <li id="li_CA0C3E0DBF004ADBB4D7819C0BF192FC">Rendermodus 2. De grootte van het punt wordt bepaald in wereldruimte (de punten blijven een constante grootte met betrekking tot de bol). De punten worden teruggegeven gebruikend veelhoeken, zodat is er geen bovengrens op puntgrootte. </li> 
      <li id="li_8F8729976DDB434D869E81D4381E2688">Rendermodus 3. De grootte van het punt wordt bepaald in het schermruimte. De punten worden teruggegeven gebruikend gladde punten OpenGL. </li> 
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

