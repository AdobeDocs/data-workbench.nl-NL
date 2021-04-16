---
description: Wanneer u een elementpuntlaag maakt met behulp van dynamische punten, worden de breedte- en lengtegegevens ingesloten in elk element van de dimensie.
title: Elementpuntlagen definiëren met behulp van dynamische punten
uuid: 5f1b4638-fe45-40be-b963-18dcd5d09afa
exl-id: ad849fe7-b909-40ef-835f-f1764e008de9
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '457'
ht-degree: 1%

---

# Elementpuntlagen definiëren met behulp van dynamische punten{#defining-element-point-layers-using-dynamic-points}

Wanneer u een elementpuntlaag maakt met behulp van dynamische punten, worden de breedte- en lengtegegevens ingesloten in elk element van de dimensie.

Als u een elementpuntlaag wilt definiëren met behulp van dynamische punten, moet u het volgende maken of al beschikbaar hebben:

* **Een dimensie**, die in het  [!DNL Transformation.cfg] dossier of een transformatiedataset wordt bepaald omvat dossier, waarin elk element de koord &quot;breedtegraad, lengtegraad&quot;of &quot;breedtegraad, lengtegraad, naam bevat.&quot;

   Voor stappen om een afmeting tot stand te brengen, zie *de Gids van de Configuratie van de Dataset*.

* **Een laagbestand** dat de gerelateerde dimensie opgeeft.

   Voor meer informatie over het vereiste formaat van het laagdossier, zie [het Formaat van het Dossier van de Laag van het Punt van het Element](../../../../../../home/c-geo-oview/c-wk-img-lyrs/c-elmt-pt-lyrs/c-elmt-pt-lyrs-ref-lkp-files/c-elmt-pt-lyr-file-frmt/c-elmt-pt-lyr-file-frmt.md#concept-678a95cb69644105a7af1b86ad5a5981).

>[!NOTE]
>
>Wanneer u [!DNL Dynamic Points] gebruikt, is het van essentieel belang dat de kardinaliteit van de afmetingen die in het laagbestand zijn opgegeven redelijk is. Als elke rij van een gegevensset een andere breedte en lengte heeft, wordt de afmeting snel gevuld en vallen de meeste rijen in een element Small Elements. Omdat het element Small Elements geen breedte en lengte heeft, wordt het niet op de wereldschaal weergegeven.

## Bestandsindeling van elementpuntlaag {#section-bbcc2baa2f754dba81eba93339a97cbd}

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

<table id="table_71AD13D7A9234782A4495DFBBD959F76"> 
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
     <ul id="ul_49069B74AF5A4CE28E20BB3B98BB2D89"> 
      <li id="li_296010E3A513424A86AFA09E4DA2DFA4">37.5181-77.1903 </li> 
      <li id="li_352D380B55044DD5AAB9B6FF8335AAC6">35.3317, -77.8126,ergens </li> 
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
     <ul id="ul_771F0E43E3CD45259918520F092BCCE4"> 
      <li id="li_2B4CF2EC50174143AAD589A08C7457F8">Rendermethode 1. De puntgrootte wordt gedefinieerd in de schermruimte (punten blijven een constante grootte ten opzichte van het computerscherm). Punten worden met veelhoeken gerenderd, dus er is geen bovengrens voor de puntgrootte. Dit is de standaard renderingmodus. </li> 
      <li id="li_5F0737A941474EF5898735ECD0563D8D">Rendermethode 2. De puntgrootte wordt gedefinieerd in de wereldruimte (punten blijven een constante grootte ten opzichte van de bol). Punten worden met veelhoeken gerenderd, dus er is geen bovengrens voor de puntgrootte. </li> 
      <li id="li_4B9EDE5FFA8348B9A50E5232CEB98F17">Rendermethode 3. De puntgrootte wordt gedefinieerd in de schermruimte. Punten worden weergegeven met vloeiende OpenGL-punten. </li> 
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
