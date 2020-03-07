---
description: De Universal Transverse Mercator (UTM)-projectie wordt gedefinieerd door acht parameters.
solution: Analytics
title: Universal Transverse Mercator-projecties
topic: Data workbench
uuid: 55421412-5c68-4a4f-88d6-650d5999a77c
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Universal Transverse Mercator-projecties{#universal-transverse-mercator-projections}

De Universal Transverse Mercator (UTM)-projectie wordt gedefinieerd door acht parameters.

Wanneer u een Universal Transverse Mercator-projectie opgeeft voor een laag met een terreinafbeelding, moeten uw bestanden met een terreinafbeelding worden uitgelijnd met een false (geprojecteerd) noordwaarts naar de bovenkant van de afbeelding en met een false oost naar rechts van de afbeelding.

Om een projectie UTM voor om het even welke bron van het terreinbeeld te specificeren, moet u het [!DNL Terrain Images.cfg] dossier in een tekstredacteur zoals Blocnote openen, de parameter van Info van de Projectie plaatsen aan &quot;TransverseMercatorProjection&quot;, en montages toevoegen voor de projectie UTM.

**Om een Universal Transverse Mercator-projectie te specificeren**

1. In [!DNL Server Files Manager], klik **[!UICONTROL Components]** om zijn inhoud te bekijken. Het [!DNL Terrain Images.cfg] dossier wordt gevestigd binnen deze folder.

1. Klik het vinkje in de kolom van de *servernaam* voor met de rechtermuisknop aan, dan klik [!DNL Terrain Images.cfg]**[!UICONTROL Make Local]**. Een vinkje verschijnt in de [!DNL Temp] kolom voor [!DNL Terrain Images.cfg].

1. Klik het pas gecreëerde vinkje in de [!DNL Temp] kolom met de rechtermuisknop aan en klik **[!UICONTROL Open]** > **[!UICONTROL in Notepad]**. Het [!DNL Terrain Images.cfg]dossier verschijnt in een venster van de Blocnote.

1. Geef de parameters van Info van de Projectie uit gebruikend het volgende fragment van het steekproefdossier en de parameterlijst als gidsen. Ben zeker om het projectietype te specificeren zoals hieronder benadrukt.

   ```
   Projection Info = TransverseMercatorProjection:
     Ellipsoid Inverse Flattening = double: 294.9786982139006
     Ellipsoid Semimajor Axis = double: 6378206.4000000004
     False Easting = double: 500000
     False Northing = double: 0
     Northwest Corner Coordinates = v3d: (550339, 5.42059e+006, 0)
     Prime Meridian = double: -123
     Scale Factor = double: 0.9996
     Southeast Corner Coordinates = v3d: (555099, 5.41356e+006, 0)
   ```

| Parameter | Beschrijving |
|---|---|
| Ellipsoïde inverse afvlakking, Ellipsoïde Semimajor-as | De parameters van de ellipsoïde die voor de projectie wordt gebruikt. De semimajoras wordt gespecificeerd in meters. |
| Valse zoekactie | De valse verassing van de middelste meridiaan van de projectie, in meter. Voor UTM is dit altijd 500.000. |
| False Northing | Het valse noord van de evenaar in de projectie, in meters. Voor UTM, is dit 0 voor de gebieden van het noordelijk halfrond en 10.000 voor de gebieden van het zuidelijk halfrond. |
| Northwest Corner Coordinates, Coördinaten zuidoost Corner | De coördinaten (in geprojecteerde meters) van de hoogste linker en bodem juiste hoeken van het beeld. |
| Premier Meridian | De lengtegraad van de middelste meridiaan van de projectie, gespecificeerd in graden ten oosten van Greenwich. De negatieve aantallen kunnen worden gebruikt om graden west te specificeren. |
| Schaalfactor | De verhouding tussen de straal van de projectiekilinder en de puntbeeldas van de ellips. Voor UTM-projecties (Universal Transverse Mercator) is dit altijd 0,9996. |

