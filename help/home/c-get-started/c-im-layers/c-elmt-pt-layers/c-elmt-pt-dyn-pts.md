---
description: Wanneer u een elementpuntlaag maakt met behulp van dynamische punten, worden de breedte- en lengtegegevens ingesloten in elk element van de dimensie.
title: Elementpuntlagen definiëren met behulp van dynamische punten
uuid: f4b41969-329a-4c33-a8db-8d85597fa577
exl-id: 5f6e264c-5804-47fa-a3ca-8608a3f7e9d3
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '454'
ht-degree: 1%

---

# Elementpuntlagen definiëren met behulp van dynamische punten{#define-element-point-layers-using-dynamic-points}

Wanneer u een elementpuntlaag maakt met behulp van dynamische punten, worden de breedte- en lengtegegevens ingesloten in elk element van de dimensie.

Als u een elementpuntlaag wilt definiëren met behulp van dynamische punten, moet u het volgende maken of al beschikbaar hebben:

* Een dimensie, gedefinieerd in het [!DNL Transformation.cfg]-bestand of een [!DNL transformation dataset include]-bestand, waarin elk element de tekenreeks &quot;latitude,longitude&quot; of &quot;latitude,longitude,name&quot; bevat.

   Voor stappen om een afmeting tot stand te brengen, zie *de Gids van de Configuratie van de Dataset*.

* Een laagbestand dat de gerelateerde dimensie opgeeft.

Voor meer informatie over het vereiste formaat van het laagdossier, zie [het Formaat van het Dossier van de Laag van het Punt van het Element](../../../../home/c-get-started/c-im-layers/c-elmt-pt-layers/c-elmt-pt-dyn-pts.md#section-0645fbc761c14bb986f3d6f02df407a0).

>[!NOTE]
>
>Wanneer u [!DNL Dynamic Points] gebruikt, is het van essentieel belang dat de kardinaliteit van de afmetingen die in het laagbestand zijn opgegeven redelijk is. Als elke rij van een gegevensset een andere breedte en lengte heeft, wordt de afmeting snel gevuld en vallen de meeste rijen in een element Small Elements. Omdat het element Small Elements geen breedte en lengte heeft, wordt het niet op de wereldschaal weergegeven.

## Bestandsindeling voor elementpuntlagen {#section-0645fbc761c14bb986f3d6f02df407a0}

Elk elementpuntlaagbestand dat gebruikmaakt van dynamische punten, moet worden opgemaakt met de volgende sjabloon:

```
Layer = ElementPointLayer:
  Dimension = ref: wdata/model/dim/Dimension Name
  Metric = ref: wdata/model/metric/Metric Name
  Dynamic Points = bool: true
  Scale = double: Scale
  Color = v3d: RGB Color Vector
  Rendering Mode = int: Mode Number
```

<table id="table_8756BDCC49F447C0855BA64BC0078A0C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Parameter </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Dimension </td> 
   <td colname="col2"> <p>De naam van de dimensie (gedefinieerd in een transformatieconfiguratiebestand) die elementen moet bevatten met de tekenreeks "latitude,longitude" of "latitude,longitude,name", zoals in de volgende voorbeelden wordt getoond: 
     <ul id="ul_CC12F05459C640F5AB3C295932B04F83"> 
      <li id="li_9023CFA04A0F407E9DF0E1A4D71BB18C">37.5181-77.1903 </li> 
      <li id="li_F002AB3AB98049A4AF1588B51167C7FA">35.3317, -77.8126,ergens </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Metrisch </td> 
   <td colname="col2"> De naam van metrisch die over de afmeting wordt geëvalueerd die in de parameter van Dimension wordt gespecificeerd. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Dynamische punten </td> 
   <td colname="col2"> Hiermee schakelt u dynamische punten in. Ingesteld op true. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Schalen </td> 
   <td colname="col2"> Optioneel. Waarde die wordt gebruikt om de punten in de laag te vergroten of te verkleinen. De standaardwaarde is 100. Bij hogere waarden worden de punten groter en bij lagere waarden worden ze kleiner. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Kleur </td> 
   <td colname="col2"> Optioneel. De RGB-kleurvector, die wordt uitgedrukt als (rood, groen, blauw). Voor elke kleur in de vector kunt u een waarde tussen 0,0 en 1,0 invoeren. (1,0, 0,0, 0,0) is bijvoorbeeld helderrood en (0,5, 0,5, 0,5, 0,5) is grijs. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Rendermodus </td> 
   <td colname="col2"> <p>Optioneel. Geheel getal dat de renderingmodus vertegenwoordigt die voor de laag moet worden gebruikt. De drie beschikbare modi zijn als volgt: 
     <ul id="ul_C7A74B9B085741C8B7116E4F110DF830"> 
      <li id="li_75CC2BE35C594B6895F743A1967A2E07">Rendermethode 1. De puntgrootte wordt gedefinieerd in de schermruimte (punten blijven een constante grootte ten opzichte van het computerscherm). Punten worden met veelhoeken gerenderd, dus er is geen bovengrens voor de puntgrootte. Dit is de standaard renderingmodus. </li> 
      <li id="li_5B19C5B0F59548E28DCE7F7CD319E210">Rendermethode 2. De puntgrootte wordt gedefinieerd in de wereldruimte (punten blijven een constante grootte ten opzichte van de bol). Punten worden met veelhoeken gerenderd, dus er is geen bovengrens voor de puntgrootte. </li> 
      <li id="li_DF0C9AEFE82642C9BD5AEA79770D2896">Rendermethode 3. De puntgrootte wordt gedefinieerd in de schermruimte. Punten worden weergegeven met vloeiende OpenGL-punten. </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

Het [!DNL IP Coordinates.layer]-bestand is als volgt opgemaakt:

```
Layer = ElementPointLayer:
  Dimension = ref: wdata/model/dim/Coordinates
  Metric = ref: wdata/model/metric/Visitors
  Dynamic Points = bool: true
```
