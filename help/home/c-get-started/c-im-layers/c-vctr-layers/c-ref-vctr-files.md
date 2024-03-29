---
description: U kunt een vectorlaag maken die verwijst naar een of meer vectorbestanden (.vec), die de gegevens bevat die de vectoren definiëren die op de wereldbol moeten worden getekend.
title: Vectorlagen definiëren die verwijzen naar vectorbestanden
uuid: fe6639fb-98fb-4246-9cc1-1a928df6ae0a
exl-id: d78fa7ea-e2a9-42b7-9071-5f72409c5b7a
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '281'
ht-degree: 0%

---

# Vectorlagen definiëren die verwijzen naar vectorbestanden{#define-vector-layers-referencing-vector-files}

{{eol}}

U kunt een vectorlaag maken die verwijst naar een of meer vectorbestanden (.vec), die de gegevens bevat die de vectoren definiëren die op de wereldbol moeten worden getekend.

Een vectorlaag definiëren die verwijst naar een of meer [!DNL .vec] hebt, moet u het volgende hebben:

* **Een of meer [!DNL .vec] bestanden** die de gegevens bevatten die worden gebruikt om de vectoren op de wereld te tekenen.

   >[!NOTE]
   >
   >Om [!DNL .vec] Als u bestanden wilt gebruiken met uw vectorlagen, neemt u contact op met Adobe.

* **Een laagbestand** die de locatie van de [!DNL .vec] bestanden. Ga voor meer informatie over de vereiste indeling van het laagbestand naar [Bestandsindeling voor vectorlagen](../../../../home/c-get-started/c-im-layers/c-vctr-layers/c-ref-vctr-files.md#section-83a0077cf0c8479b9e7b2939bc761af1).

   >[!NOTE]
   >
   >De [!DNL Boundaries.layer] het dossier, verstrekt met [!DNL Geography] profiel, is een vectorlaag die verwijst naar de [!DNL mwnation.vec], [!DNL mwstate.vec], [!DNL mwcoast.vec], [!DNL mwlake.vec], en [!DNL mwisland.vec] bestanden.

## Bestandsindeling voor vectorlagen {#section-83a0077cf0c8479b9e7b2939bc761af1}

Elk vectorlaagbestand verwijst naar [!DNL .vec] bestanden moeten worden opgemaakt met de volgende sjabloon:

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
| Vec-bestanden | Pad(en) naar de [!DNL .vec] bestand(en) met de vectorgegevens. |
| Kleur | De kleurvector RGB, die wordt uitgedrukt als (rood, groen, blauw). Voor elke kleur in de vector kunt u een waarde tussen 0,0 en 1,0 invoeren. (1,0, 0,0, 0,0) is bijvoorbeeld helderrood en (0,5, 0,5, 0,5, 0,5) is grijs. |
| Alfa | Hiermee regelt u de transparantie van de vectoren die op de wereld worden weergegeven. Het bereik loopt van 0 tot en met 1, waarbij 0 het meest transparant is. |
| Breedte | Optioneel. Hiermee stelt u de breedte van de gegevens in pixels in. Het aanbevolen bereik is 1 tot 4. |
| Foutfactor | Bepaalt hoe nauwkeurig de vectoren worden getekend. Voor grotere waarden worden de vectoren minder nauwkeurig maar sneller getekend. De standaardwaarde is 5. |

De [!DNL Boundaries.layer] bestand is als volgt opgemaakt:

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
