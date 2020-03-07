---
description: Wanneer het creëren van een laag van het elementenpunt die dynamische punten gebruikt, worden de breedtegraad en de lengtegegevens ingebed in elk element van de afmeting.
solution: Analytics
title: Het bepalen van de Lagen van het Punt van het Element die Dynamische Punten gebruiken
topic: Data workbench
uuid: 5f1b4638-fe45-40be-b963-18dcd5d09afa
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Het bepalen van de Lagen van het Punt van het Element die Dynamische Punten gebruiken{#defining-element-point-layers-using-dynamic-points}

Wanneer het creëren van een laag van het elementenpunt die dynamische punten gebruikt, worden de breedtegraad en de lengtegegevens ingebed in elk element van de afmeting.

Om een laag van het elementenpunt te bepalen die dynamische punten gebruikt, moet u tot stand brengen of reeds beschikbaar het volgende hebben:

* **Een dimensie**, die in het [!DNL Transformation.cfg] dossier of een transformatiedataset wordt bepaald omvat dossier, waarin elk element het koord &quot;breedtegraad, lengtegraad&quot;of &quot;breedtegraad, lengtegraad, naam.&quot;bevat

   Voor stappen om een afmeting tot stand te brengen, zie de Gids *van de Configuratie van de* Dataset.

* **Een laagdossier** dat de verwante afmeting specificeert.

   Voor meer informatie over het vereiste formaat van het laagdossier, zie het Formaat [van het Dossier van de Laag van het Punt van het](../../../../../../home/c-geo-oview/c-wk-img-lyrs/c-elmt-pt-lyrs/c-elmt-pt-lyrs-ref-lkp-files/c-elmt-pt-lyr-file-frmt/c-elmt-pt-lyr-file-frmt.md#concept-678a95cb69644105a7af1b86ad5a5981)Element.

>[!NOTE]
>
>Wanneer het gebruiken [!DNL Dynamic Points], is het essentieel om ervoor te zorgen dat de kardinaliteit van de afmeting die in het laagdossier wordt gespecificeerd redelijk is. Als elke rij van een dataset een verschillende breedte en lengtegraad heeft, vult de afmeting snel en de meeste rijen vallen in een Klein element van Elementen. Omdat het element Kleine Elementen geen breedte en geen lengte heeft, verschijnt het niet op de wereld.

## Element Point Layer File Format {#section-bbcc2baa2f754dba81eba93339a97cbd}

Elk dossier van de elementenpuntlaag dat dynamische punten gebruikt moet worden geformatteerd gebruikend het volgende malplaatje:

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
   <td colname="col1"> Afmetingen </td> 
   <td colname="col2"> <p>De naam van de afmeting (die in een dossier van de transformatieconfiguratie wordt bepaald), die elementen met het koord "breedtegraad, lengtegraad"of "breedtegraad, lengtegraad, naam"zoals aangetoond in de volgende voorbeelden moet bevatten: 
     <ul id="ul_49069B74AF5A4CE28E20BB3B98BB2D89"> 
      <li id="li_296010E3A513424A86AFA09E4DA2DFA4">37.5181,-77.1903 </li> 
      <li id="li_352D380B55044DD5AAB9B6FF8335AAC6">35.3317, -77.8126, ergens </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Metrisch </td> 
   <td colname="col2"> De naam van metrisch die over de afmeting wordt geëvalueerd die in de parameter van de Afmeting wordt gespecificeerd. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Dynamische punten </td> 
   <td colname="col2"> Laat dynamische Punten toe. Reeks op waar. </td> 
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
     <ul id="ul_771F0E43E3CD45259918520F092BCCE4"> 
      <li id="li_2B4CF2EC50174143AAD589A08C7457F8">Rendermodus 1. De grootte van punten wordt bepaald in het schermruimte (de punten blijven een constante grootte met betrekking tot het computerscherm). De punten worden teruggegeven gebruikend veelhoeken, zodat is er geen bovengrens op puntgrootte. Dit is het gebrek dat wijze teruggeeft. </li> 
      <li id="li_5F0737A941474EF5898735ECD0563D8D">Rendermodus 2. De grootte van het punt wordt bepaald in wereldruimte (de punten blijven een constante grootte met betrekking tot de bol). De punten worden teruggegeven gebruikend veelhoeken, zodat is er geen bovengrens op puntgrootte. </li> 
      <li id="li_4B9EDE5FFA8348B9A50E5232CEB98F17">Rendermodus 3. De grootte van het punt wordt bepaald in het schermruimte. De punten worden teruggegeven gebruikend gladde punten OpenGL. </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

Het [!DNL IP Coordinates.layer] bestand is als volgt geformatteerd:

```
Layer = ElementPointLayer:
  Dimension = ref: wdata/model/dim/Coordinates
  Metric = ref: wdata/model/metric/Visitors
  Dynamic Points = bool: true
```

