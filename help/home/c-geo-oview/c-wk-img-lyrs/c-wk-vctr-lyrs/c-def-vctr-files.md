---
description: U kunt een vectorlaag maken die verwijst naar een of meer vectorbestanden (.vec), die de gegevens bevat die de vectoren definiëren die op de wereld moeten worden getekend.
title: Vectorlagen definiëren die verwijzen naar vectorbestanden
uuid: 162d4ecc-d305-42e3-a5d4-0c1609a40f29
exl-id: c6da3cd9-f42a-4e9c-ae48-9f4ffdc42f7b
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '281'
ht-degree: 0%

---

# Vectorlagen definiëren die verwijzen naar vectorbestanden{#defining-vector-layers-referencing-vector-files}

U kunt een vectorlaag maken die verwijst naar een of meer vectorbestanden (.vec), die de gegevens bevat die de vectoren definiëren die op de wereld moeten worden getekend.

Als u een vectorlaag wilt definiëren die verwijst naar een of meer [!DNL .vec]bestanden, moet u het volgende hebben:

* Een of meer [!DNL .vec]bestanden die de gegevens bevatten die worden gebruikt om de vectoren op de wereld te tekenen.

   >[!NOTE]
   >
   >Neem contact op met Adobe om [!DNL .vec] bestanden op te halen die u met uw vectorlagen wilt gebruiken.

* Een laagbestand dat de locatie van de [!DNL .vec]-bestanden aangeeft. Zie [Vectorlaagbestandsindeling](../../../../home/c-geo-oview/c-wk-img-lyrs/c-wk-vctr-lyrs/c-def-vctr-files.md#section-530d03f41ede4a339aebbb680e15240a) voor meer informatie over de vereiste indeling van het laagbestand.

   >[!NOTE]
   >
   >Het [!DNL Boundaries.layer]-bestand met het profiel [!DNL Geography] is een vectorlaag die verwijst naar de bestanden [!DNL mwnation.vec], [!DNL mwstate.vec], [!DNL mwcoast.vec], [!DNL mwlake.vec] en [!DNL mwisland.vec].

## Bestandsindeling vectorlaag {#section-530d03f41ede4a339aebbb680e15240a}

Elk vectorlaagbestand dat verwijst naar [!DNL .vec]bestanden, moet worden opgemaakt met de volgende sjabloon:

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
| Vec-bestanden | Pad(en) naar het [!DNL .vec]-bestand(en) met de vectorgegevens. |
| Kleur | De RGB-kleurvector, die wordt uitgedrukt als (rood, groen, blauw). Voor elke kleur in de vector kunt u een waarde tussen 0,0 en 1,0 invoeren. (1,0, 0,0, 0,0) is bijvoorbeeld helderrood en (0,5, 0,5, 0,5, 0,5) is grijs. |
| Alfa | Hiermee regelt u de transparantie van de vectoren die op de wereldbol worden weergegeven. Het bereik loopt van 0 tot en met 1, waarbij 0 het meest transparant is. |
| Breedte | Optioneel. Hiermee stelt u de breedte van de gegevens in pixels in. Het aanbevolen bereik is 1 tot 4. |
| Foutfactor | Bepaalt hoe nauwkeurig de vectoren worden getekend. Voor grotere waarden worden de vectoren minder nauwkeurig maar sneller getekend. De standaardwaarde is 5. |

Het [!DNL Boundaries.layer]-bestand is als volgt opgemaakt:

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
