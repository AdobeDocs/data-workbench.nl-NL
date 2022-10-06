---
description: Opmaakgegevens over het elementpuntlaagbestand.
title: Laagbestandsindeling voor elementpunt
uuid: a8b3d2f4-0ed2-480d-a2a6-75d43025a579
exl-id: 125796f6-a447-4f12-bcf2-3e669783cf1e
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '418'
ht-degree: 1%

---

# Laagbestandsindeling voor elementpunt{#element-point-layer-file-format}

{{eol}}

Opmaakgegevens over het elementpuntlaagbestand.

Elke elementpuntlaag [!DNL .layer] bestand dat verwijst naar een opzoekbestand, moet worden opgemaakt met de volgende sjabloon:

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
   <td colname="col2"> Pad naar het opzoekbestand met breedte- en lengtegegevens. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Lengtegraad kolom </td> 
   <td colname="col2"> De naam van de kolom in het opzoekbestand die de longitude-gegevens bevat. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Latitude-kolom </td> 
   <td colname="col2"> De naam van de kolom in het opzoekbestand die de breedtegraadgegevens bevat. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Kolom benoemen </td> 
   <td colname="col2"> Optioneel. De naam van de kolom in het opzoekbestand met de namen van de locaties die worden vertegenwoordigd door de breedte- en lengtegegevens. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Toetskolom </td> 
   <td colname="col2"> <p>De naam van de kolom in het raadplegingsdossier dat de gemeenschappelijke zeer belangrijke gegevens bevat, die de server van de gegevenswerkbank toelaat om de gegevens in het raadplegingsdossier in de dataset te integreren. Dit moet de eerste kolom in het opzoekbestand zijn. </p> <p>Elke rij in deze kolom is een element van een dimensie. Deze dimensie moet worden gedefinieerd in het <span class="filepath"> Transformation.cfg</span> bestand of een gegevensset met transformaties bevat bestand en opgegeven in de parameter Dimension van dit bestand. Voor meer informatie over de dossiers van de transformatieconfiguratie, zie <i>Configuratie-handleiding voor gegevensset</i>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Dimension </td> 
   <td colname="col2">De naam van de dimensie (gedefinieerd in een transformatieconfiguratiebestand) die elementen bevat die overeenkomen met de gegevensrijen in de <span class="wintitle"> Sleutel</span> kolom. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Metrisch </td> 
   <td colname="col2"> De naam van metrisch die over de afmeting wordt geëvalueerd die in de parameter van Dimension wordt gespecificeerd. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Schalen </td> 
   <td colname="col2"> Optioneel. Waarde die wordt gebruikt om de punten in de laag te vergroten of te verkleinen. De standaardwaarde is 100. Bij hogere waarden worden de punten groter en bij lagere waarden worden ze kleiner. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Kleur </td> 
   <td colname="col2"> Optioneel. De kleurvector RGB, die wordt uitgedrukt als (rood, groen, blauw). Voor elke kleur in de vector kunt u een waarde tussen 0,0 en 1,0 invoeren. (1,0, 0,0, 0,0) is bijvoorbeeld helderrood en (0,5, 0,5, 0,5, 0,5) is grijs. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Rendermodus </td> 
   <td colname="col2"> <p>Optioneel. Geheel getal dat de renderingmodus vertegenwoordigt die voor de laag moet worden gebruikt. De drie beschikbare modi zijn als volgt: 
     <ul id="ul_CBB26B32505846A39FEB85E831E1C7AB"> 
      <li id="li_B31528A8858C4418ABCDFF0B4EFB25D7">Rendermethode 1. De puntgrootte wordt gedefinieerd in de schermruimte (punten blijven een constante grootte ten opzichte van het computerscherm). Punten worden met veelhoeken gerenderd, dus er is geen bovengrens voor de puntgrootte. Dit is de standaard renderingmodus. </li> 
      <li id="li_CA0C3E0DBF004ADBB4D7819C0BF192FC">Rendermethode 2. De puntgrootte wordt gedefinieerd in de wereldruimte (punten blijven een constante grootte ten opzichte van de bol). Punten worden met veelhoeken gerenderd, dus er is geen bovengrens voor de puntgrootte. </li> 
      <li id="li_8F8729976DDB434D869E81D4381E2688">Rendermethode 3. De puntgrootte wordt gedefinieerd in de schermruimte. Punten worden weergegeven met vloeiende OpenGL-punten. </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

De [!DNL Zip Points.layer] bestand is als volgt opgemaakt:

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
