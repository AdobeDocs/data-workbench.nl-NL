---
description: Wanneer het creëren van een laag van het elementenpunt die dynamische punten gebruikt, worden de breedtegraad en de lengtegegevens ingebed in elk element van de afmeting.
solution: Analytics
title: Bepaal de lagen van het elementenpunt gebruikend dynamische punten
topic: Data workbench
uuid: f4b41969-329a-4c33-a8db-8d85597fa577
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Bepaal de lagen van het elementenpunt gebruikend dynamische punten{#define-element-point-layers-using-dynamic-points}

Wanneer het creëren van een laag van het elementenpunt die dynamische punten gebruikt, worden de breedtegraad en de lengtegegevens ingebed in elk element van de afmeting.

Om een laag van het elementenpunt te bepalen die dynamische punten gebruikt, moet u tot stand brengen of reeds beschikbaar het volgende hebben:

* Een afmeting, die in het [!DNL Transformation.cfg] dossier of een [!DNL transformation dataset include] dossier wordt bepaald, waarin elk element het koord &quot;breedtegraad, lengtegraad&quot;of &quot;breedtegraad, lengtegraad, naam.&quot; bevat

   Voor stappen om een afmeting tot stand te brengen, zie de Gids *van de Configuratie van de* Dataset.

* Een laagdossier dat de verwante afmeting specificeert.

Voor meer informatie over het vereiste formaat van het laagdossier, zie het Formaat [van het Dossier van de Laag van het Punt van het](../../../../home/c-get-started/c-im-layers/c-elmt-pt-layers/c-elmt-pt-dyn-pts.md#section-0645fbc761c14bb986f3d6f02df407a0)Element.

>[!NOTE]
>
>Wanneer het gebruiken [!DNL Dynamic Points], is het essentieel om ervoor te zorgen dat de kardinaliteit van de afmeting die in het laagdossier wordt gespecificeerd redelijk is. Als elke rij van een dataset een verschillende breedte en lengtegraad heeft, vult de afmeting snel en de meeste rijen vallen in een Klein element van Elementen. Omdat het element Kleine Elementen geen breedte en geen lengte heeft, verschijnt het niet op de wereld.

## Bestandsindeling voor elementenlaag {#section-0645fbc761c14bb986f3d6f02df407a0}

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

<table id="table_8756BDCC49F447C0855BA64BC0078A0C"> 
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
     <ul id="ul_CC12F05459C640F5AB3C295932B04F83"> 
      <li id="li_9023CFA04A0F407E9DF0E1A4D71BB18C">37.5181,-77.1903 </li> 
      <li id="li_F002AB3AB98049A4AF1588B51167C7FA">35.3317, -77.8126, ergens </li> 
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
     <ul id="ul_C7A74B9B085741C8B7116E4F110DF830"> 
      <li id="li_75CC2BE35C594B6895F743A1967A2E07">Rendermodus 1. De grootte van punten wordt bepaald in het schermruimte (de punten blijven een constante grootte met betrekking tot het computerscherm). De punten worden teruggegeven gebruikend veelhoeken, zodat is er geen bovengrens op puntgrootte. Dit is het gebrek dat wijze teruggeeft. </li> 
      <li id="li_5B19C5B0F59548E28DCE7F7CD319E210">Rendermodus 2. De grootte van het punt wordt bepaald in wereldruimte (de punten blijven een constante grootte met betrekking tot de bol). De punten worden teruggegeven gebruikend veelhoeken, zodat is er geen bovengrens op puntgrootte. </li> 
      <li id="li_DF0C9AEFE82642C9BD5AEA79770D2896">Rendermodus 3. De grootte van het punt wordt bepaald in het schermruimte. De punten worden teruggegeven gebruikend gladde punten OpenGL. </li> 
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

