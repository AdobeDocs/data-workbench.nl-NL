---
description: U kunt een vectorlaag tot stand brengen die verwijzingen één of meerdere vectordossiers (.vec), die de gegevens bevat die de vectoren die op de bol moeten worden getrokken bepalen.
solution: Analytics
title: Vectorlagen definiëren die verwijzen naar vectorbestanden
topic: Data workbench
uuid: 162d4ecc-d305-42e3-a5d4-0c1609a40f29
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Vectorlagen definiëren die verwijzen naar vectorbestanden{#defining-vector-layers-referencing-vector-files}

U kunt een vectorlaag tot stand brengen die verwijzingen één of meerdere vectordossiers (.vec), die de gegevens bevat die de vectoren die op de bol moeten worden getrokken bepalen.

Om een vectorlaag te bepalen die verwijzingen één of meerdere [!DNL .vec]dossiers, moet u het volgende hebben:

* Één of meerdere [!DNL .vec]dossiers die de gegevens bevatten die worden gebruikt om de vectoren op de aardbol te trekken.

   >[!NOTE]
   >
   >Om [!DNL .vec] dossiers te verkrijgen om met uw vectorlagen te gebruiken, contacteer Adobe.

* Een laagdossier dat de plaats van de [!DNL .vec] dossiers specificeert. Voor meer informatie over het vereiste formaat van het laagdossier, zie het Formaat [van het Dossier van de](../../../../home/c-geo-oview/c-wk-img-lyrs/c-wk-vctr-lyrs/c-def-vctr-files.md#section-530d03f41ede4a339aebbb680e15240a)VectorLaag.

   >[!NOTE]
   >
   >Het [!DNL Boundaries.layer] dossier, dat van het [!DNL Geography] profiel wordt voorzien, is een vectorlaag die verwijzingen de [!DNL mwnation.vec], [!DNL mwstate.vec], [!DNL mwcoast.vec], [!DNL mwlake.vec], en [!DNL mwisland.vec] dossiers.

## Vector Layer File Format {#section-530d03f41ede4a339aebbb680e15240a}

Elk vectorlaagdossier dat van verwijzingen voorziet [!DNL .vec]dossiers moet worden geformatteerd gebruikend het volgende malplaatje:

```
Layer = VectorLayer:
  Vec Files = vector: n items
    0 = string: Maps\\.vec file 1
    1 = string: Maps\\.vec file 2
    . . .
    n-1 = string: Maps\\.vec file n
  Color = v3d: color vector
  Alpha = double: alpha
  Width = double: width
  Error Factor = double: error factor
```

| Parameter | Beschrijving |
|---|---|
| Vec-bestanden | Pad(en) naar het (de) [!DNL .vec] bestand(en) dat (die) de vectorgegevens bevat (bevatten). |
| Kleur | De RGB kleurenvector, die als (rood, groen, blauw) wordt uitgedrukt. Voor elke kleur in de vector, kunt u een waarde van 0.0 tot 1.0 ingaan. Bijvoorbeeld, (1.0, 0.0, 0.0) is fel rood, en (0.5, 0.5, 0.5, 0.5) is grijs. |
| Alpha | Controleert de transparantie van de vectoren die op de wereld worden getoond. De waaier is 0 tot 1, met 0 die het meest transparant zijn. |
| Breedte | Optioneel. Plaatst de breedte van de gegevens in pixel. Het aanbevolen bereik is 1 tot 4. |
| Foutfactor | Controleert hoe nauwkeurig de vectoren worden getrokken. Voor grotere waarden, worden de vectoren minder nauwkeurig maar sneller getrokken. De standaardwaarde is 5. |

Het [!DNL Boundaries.layer] bestand is als volgt geformatteerd:

```
 Boundaries.layer file is formatted as follows:
Layer = VectorLayer:
  Vec Files = vector: 5 items
    0 = string: Maps\\mwnation.vec
    1 = string: Maps\\mwstate.vec
    2 = string: Maps\\mwcoast.vec
    3 = string: Maps\\mwlake.vec
    4 = string: Maps\\mwisland.vec
  Color = v3d: (.5,.5,1)
  Alpha = double: .5
  Error Factor = double: 4
```

