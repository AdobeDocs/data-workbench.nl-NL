---
description: Wanneer u een elementpuntlaag maakt die verwijst naar een opzoekbestand om breedte- en lengtegegevens te verkrijgen, wordt de locatie van het punt opgehaald door elk element en de bijbehorende breedte en lengte op te halen uit het opzoekbestand.
title: Elementpuntlagen definiëren die verwijzen naar opzoekbestanden
uuid: 32c8de7a-4316-4f91-9810-7f584bc7fb0b
exl-id: 2275fa8e-82fe-49e4-ab3e-91ec6ecb6233
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '846'
ht-degree: 0%

---

# Elementpuntlagen definiëren die verwijzen naar opzoekbestanden{#define-element-point-layers-referencing-lookup-files}

{{eol}}

Wanneer u een elementpuntlaag maakt die verwijst naar een opzoekbestand om breedte- en lengtegegevens te verkrijgen, wordt de locatie van het punt opgehaald door elk element en de bijbehorende breedte en lengte op te halen uit het opzoekbestand.

>[!NOTE]
>
>In plaats van een opzoekbestand te gebruiken, kunt u de functie Dynamische punten gebruiken, waarmee de breedte en lengte van een locatie worden ingesloten in de naam van elk element van een dimensie. Zie [Elementpuntlagen definiëren met behulp van dynamische punten](../../../../home/c-get-started/c-im-layers/c-elmt-pt-layers/c-elmt-pt-dyn-pts.md#concept-51adc5e1df8a48e7bd7a582967e4c512).

Als u een elementpuntlaag wilt definiëren die verwijst naar een opzoekbestand, moet u het volgende maken of al beschikbaar hebben:

* **Een dimensie** in de [!DNL Transformation.cfg file] of [!DNL transformation dataset include] bestand. Voor informatie over de dossiers van de transformatieconfiguratie, zie *Configuratie-handleiding voor gegevensset*.

* **Een opzoekbestand** met de gegevens die worden gebruikt om elk gegevenspunt te plotten. Dit bestand moet ten minste drie kolommen gegevens bevatten voor elk gegevenspunt: de sleutel, de lengtegraad en de breedtegraad. Voor meer informatie over het vereiste formaat van het raadplegingsdossier, zie [Laagbestandsindeling voor elementpunt](../../../../home/c-get-started/c-im-layers/c-elmt-pt-layers/c-elp-ref-lkup-files.md#section-52d7e92be8354d979af9e7a2210b76f2).

* **Een laagbestand** Hiermee geeft u de locatie van het opzoekbestand op en geeft u de gerelateerde afmetingen en metrische waarde, alsmede de namen van de kolommen sleutel, lengte en breedte in het opzoekbestand aan. Ga voor meer informatie over de vereiste indeling van het laagbestand naar [Laagbestandsindeling voor elementpunt](../../../../home/c-get-started/c-im-layers/c-elmt-pt-layers/c-elp-ref-lkup-files.md#section-52d7e92be8354d979af9e7a2210b76f2).

   >[!NOTE]
   >
   >De [!DNL Zip Points.layer] het dossier, verstrekt met [!DNL Geography] profiel, is een elementpuntlaag die de [!DNL Zipcode.dim] bestand, de [!DNL Sessions.metric] bestand, de [!DNL Zip Points.txt] opzoekbestand en de namen van de kolommen key, longitude, latitude en name in het opzoekbestand.

## Opzoekbestandsindeling voor elementpunten {#section-0bc8c652c1bd40eb84078f2af71a5c06}

Het opzoekbestand van de elementpuntlaag moet ten minste de volgende drie kolommen bevatten:

* **[!DNL Key]kolom:** Deze kolom zou gemeenschappelijke zeer belangrijke gegevens moeten bevatten, die de server van de Data Workbench toelaat om de gegevens in het raadplegingsdossier met dat in de dataset te verbinden. De [!DNL key] de kolom moet de eerste kolom in het raadplegingsdossier zijn. Elke rij in deze kolom identificeert een element van de dimensie.

* **[!DNL Longitude]kolom:** Deze kolom moet de lengtegraad bevatten voor elk gegevenspunt in het dialoogvenster [!DNL Key] kolom.

* **[!DNL Latitude]kolom:** Deze kolom moet de breedtegraad bevatten voor elk gegevenspunt in het dialoogvenster [!DNL Key] kolom.

* **[!DNL Name]kolom (optioneel):** Als u een naam wilt opgeven die voor elk gegevenspunt op de kaart moet worden weergegeven, kunt u een [!DNL Name] in het opzoekbestand.

Elke rij in de [!DNL Zip Points.txt] Het opzoekbestand bevat een ZIP-code in de eerste kolom gevolgd door de lengte, breedtegraad en de naam van de desbetreffende stad.

```
tude, and associated city name.
ZIP_CODE LATITUDE LONGITUDE NAME
00210 +43.005895 -071.013202 PORTSMOUTH, NH
00211 +43.005895 -071.013202 PORTSMOUTH, NH
...
```

## Bestandsindeling elementpuntlaag {#section-52d7e92be8354d979af9e7a2210b76f2}

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
   <td colname="col2"> <p>De naam van de kolom in het raadplegingsdossier dat de gemeenschappelijke zeer belangrijke gegevens bevat, die de server van de Data Workbench toelaat om de gegevens in het raadplegingsdossier in de dataset te integreren. Dit moet de eerste kolom in het opzoekbestand zijn. </p> <p>Elke rij in deze kolom is een element van een dimensie. Deze dimensie moet worden gedefinieerd in het <span class="filepath"> Transformation.cfg</span> of een <span class="wintitle"> gegevensset voor transformatie bevat</span> en opgegeven in de parameter Dimension van dit bestand. Voor meer informatie over de dossiers van de transformatieconfiguratie, zie <i>Configuratie-handleiding voor gegevensset</i>. </p> </td> 
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
     <ul id="ul_F15E43B3BFE54CDD8026837027E25819"> 
      <li id="li_5405D939540E4D0FA7828D2623D72C44">Rendermethode 1. De puntgrootte wordt gedefinieerd in de schermruimte (punten blijven een constante grootte ten opzichte van het computerscherm). Punten worden met veelhoeken gerenderd, dus er is geen bovengrens voor de puntgrootte. Dit is de standaard renderingmodus. </li> 
      <li id="li_61C5AA926777449E8804C7BCE9E46F9B">Rendermethode 2. De puntgrootte wordt gedefinieerd in de wereldruimte (punten blijven een constante grootte ten opzichte van de bol). Punten worden met veelhoeken gerenderd, dus er is geen bovengrens voor de puntgrootte. </li> 
      <li id="li_C00527F959354D3BB7422EFFE1FB5135">Rendermethode 3. De puntgrootte wordt gedefinieerd in de schermruimte. Punten worden weergegeven met vloeiende OpenGL-punten. </li> 
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
