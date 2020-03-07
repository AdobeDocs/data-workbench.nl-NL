---
description: Wanneer het creëren van een vectorlaag die verwijzingen een lusje gescheiden waarden (.tsv) dossier, wordt het vectorgegeven verkregen door tekeningsinstructies evenals lengtegraad en breedtecijfers van het .tsv dossier terug te winnen.
solution: Analytics
title: Vectorlagen die van labels voorzien scheiden waardendossiers
topic: Data workbench
uuid: 42607b34-e9f2-420a-ba5a-05562598b480
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Vectorlagen die van labels voorzien scheiden waardendossiers{#vector-layers-referencing-tab-separated-values-files}

Wanneer het creëren van een vectorlaag die verwijzingen een lusje gescheiden waarden (.tsv) dossier, wordt het vectorgegeven verkregen door tekeningsinstructies evenals lengtegraad en breedtecijfers van het .tsv dossier terug te winnen.

Om een vectorlaag te bepalen die verwijzingen een [!DNL .tsv] dossiers, moet u het volgende hebben:

* **Een[!DNL .tsv]dossier** dat de gegevens bevat die worden gebruikt om de vectoren op de aardbol, met inbegrip van lengte en breedtecijfers te trekken. Voor meer informatie over het vereiste formaat van het [!DNL .tsv] dossier, zie het [VectorFormaat](../../../../home/c-geo-oview/c-wk-img-lyrs/c-wk-vctr-lyrs/c-tab-sep-val-files.md#section-a29012c9ff4444ac8a6d41c68482828e)van het Dossier TSV.

* **Een laagdossier** dat de plaats van het [!DNL .tsv] dossier specificeert. Voor meer informatie over het vereiste formaat van het laagdossier, zie het Formaat [van het Dossier van de](../../../../home/c-geo-oview/c-wk-img-lyrs/c-wk-vctr-lyrs/c-tab-sep-val-files.md#section-c430923f341f4c93852e9f24b61e82bf)VectorLaag.

## Vector TSV-bestandsindeling {#section-a29012c9ff4444ac8a6d41c68482828e}

Het [!DNL .tsv] dossier moet de volgende drie lusje gescheiden kolommen bevatten:

* **[!DNL Begin]:**Deze kolom zou moeten erop wijzen of om met een nieuwe lijn te beginnen. De waarden in deze kolom kunnen of 0 zijn (begin geen nieuwe lijn) of 1 (begin een nieuwe lijn).
* **[!DNL Longitude]:**Deze kolom zou lengtewaarden moeten bevatten.
* **[!DNL Latitude]:**Deze kolom zou breedtegraden waarden moeten bevatten.

>[!NOTE]
>
>Om het even welke extra kolommen worden genegeerd.

Na is een steekproefdossier [!DNL .tsv] dat gegevens voor een vectorlaag bevat:

![](assets/tsv_vectorlayer.png)

## Vector-laagbestandsindeling {#section-c430923f341f4c93852e9f24b61e82bf}

Elk vectorlaagdossier van verwijzingen voorzien van dossiers [!DNL .tsv] moet worden geformatteerd gebruikend het volgende malplaatje:

```
Layer = VectorLayer:
  TSV Files = vector: n items
    0 = string: Maps\\File Name.tsv
    1 = string: Maps\\File Name.tsv
    . . .
    n-1 = string: Maps\\File Name.tsv
  Color = v3d: color vector
  Alpha = double: alpha
  Width = double: width
  Error Factor = double: error factor
```

<table id="table_152F73536AB9403AB43854B81D6A9A15"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Parameter </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> TSV-bestanden </td> 
   <td colname="col2"> <p>Pad(en) naar het (de) <span class="filepath"> .tsv</span> -bestand(en) met de vectorgegevens. </p> <p>Voorbeeld: <span class="filepath"> Kaarten\\USVectorData.tsv</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Kleur </td> 
   <td colname="col2"> De RGB kleurenvector, die als (rood, groen, blauw) wordt uitgedrukt. Voor elke kleur in de vector, kunt u een waarde van 0.0 tot 1.0 ingaan. Bijvoorbeeld, (1.0, 0.0, 0.0) is fel rood, en (0.5, 0.5, 0.5, 0.5) is grijs. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Alpha </td> 
   <td colname="col2"> Controleert de transparantie van de vectoren die op de wereld worden getoond. De waaier is 0 tot 1, met 0 die het meest transparant zijn. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Breedte </td> 
   <td colname="col2"> Optioneel. Plaatst de breedte van de gegevens in pixel. Het aanbevolen bereik is 1 tot 4. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Foutfactor </td> 
   <td colname="col2"> Controleert hoe nauwkeurig de vectoren worden getrokken. Voor grotere waarden, worden de vectoren minder nauwkeurig maar sneller getrokken. De standaardwaarde is 5. </td> 
  </tr> 
 </tbody> 
</table>

