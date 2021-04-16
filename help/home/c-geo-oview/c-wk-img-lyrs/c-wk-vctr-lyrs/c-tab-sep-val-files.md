---
description: Wanneer u een vectorlaag maakt die verwijst naar een bestand met door tabs gescheiden waarden (.tsv), worden de vectorgegevens verkregen door tekeninstructies en lengte- en breedtegegevens uit het .tsv-bestand op te halen.
title: Vectorlagen die verwijzen naar via tabs gescheiden waardebestanden
uuid: 42607b34-e9f2-420a-ba5a-05562598b480
exl-id: be16ba73-4a98-472b-98f1-1b32e671b763,7b0b0286-072b-4b31-b6ec-ced322da5236
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '352'
ht-degree: 0%

---

# Vectorlagen die verwijzen naar via tabs gescheiden waardebestanden{#vector-layers-referencing-tab-separated-values-files}

Wanneer u een vectorlaag maakt die verwijst naar een bestand met door tabs gescheiden waarden (.tsv), worden de vectorgegevens verkregen door tekeninstructies en lengte- en breedtegegevens uit het .tsv-bestand op te halen.

Als u een vectorlaag wilt definiëren die verwijst naar een [!DNL .tsv]-bestand, moet u het volgende hebben:

* **Een bestand  [!DNL .tsv]** dat de gegevens bevat die worden gebruikt om de vectoren op de wereld te tekenen, inclusief lengte- en breedtegegevens. Zie [Vector TSV-bestandsindeling](../../../../home/c-geo-oview/c-wk-img-lyrs/c-wk-vctr-lyrs/c-tab-sep-val-files.md#section-a29012c9ff4444ac8a6d41c68482828e) voor meer informatie over de vereiste indeling van het [!DNL .tsv]-bestand.

* **Een laagbestand** dat de locatie van het  [!DNL .tsv] bestand aangeeft. Zie [Vectorlaagbestandsindeling](../../../../home/c-geo-oview/c-wk-img-lyrs/c-wk-vctr-lyrs/c-tab-sep-val-files.md#section-c430923f341f4c93852e9f24b61e82bf) voor meer informatie over de vereiste indeling van het laagbestand.

## Vector TSV-bestandsindeling {#section-a29012c9ff4444ac8a6d41c68482828e}

Het [!DNL .tsv] dossier moet de volgende drie lusje gescheiden kolommen bevatten:

* **[!DNL Begin]:** Deze kolom zou moeten erop wijzen of met een nieuwe lijn te beginnen. De waarden in deze kolom kunnen 0 (begin geen nieuwe lijn) of 1 (begin een nieuwe lijn) zijn.
* **[!DNL Longitude]:** Deze kolom moet lengtewaarden bevatten.
* **[!DNL Latitude]:** Deze kolom moet breedtewaarden bevatten.

>[!NOTE]
>
>Eventuele extra kolommen worden genegeerd.

Hier volgt een voorbeeld van een [!DNL .tsv]-bestand dat gegevens voor een vectorlaag bevat:

![](assets/tsv_vectorlayer.png)

## Bestandsindeling voor vectorlagen {#section-c430923f341f4c93852e9f24b61e82bf}

Elk vectorlaagbestand dat verwijst naar [!DNL .tsv]-bestanden, moet worden opgemaakt met de volgende sjabloon:

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
   <td colname="col2"> <p>Pad(en) naar het <span class="filepath"> .tsv</span>-bestand(en) met de vectorgegevens. </p> <p>Voorbeeld: <span class="filepath"> Kaarten\\USVectorData.tsv</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Kleur </td> 
   <td colname="col2"> De RGB-kleurvector, die wordt uitgedrukt als (rood, groen, blauw). Voor elke kleur in de vector kunt u een waarde tussen 0,0 en 1,0 invoeren. (1,0, 0,0, 0,0) is bijvoorbeeld helderrood en (0,5, 0,5, 0,5, 0,5) is grijs. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Alfa </td> 
   <td colname="col2"> Hiermee regelt u de transparantie van de vectoren die op de wereldbol worden weergegeven. Het bereik loopt van 0 tot en met 1, waarbij 0 het meest transparant is. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Breedte </td> 
   <td colname="col2"> Optioneel. Hiermee stelt u de breedte van de gegevens in pixels in. Het aanbevolen bereik is 1 tot 4. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Foutfactor </td> 
   <td colname="col2"> Bepaalt hoe nauwkeurig de vectoren worden getekend. Voor grotere waarden worden de vectoren minder nauwkeurig maar sneller getekend. De standaardwaarde is 5. </td> 
  </tr> 
 </tbody> 
</table>
