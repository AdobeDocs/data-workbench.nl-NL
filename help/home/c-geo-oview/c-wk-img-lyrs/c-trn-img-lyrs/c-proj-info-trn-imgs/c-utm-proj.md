---
description: De Universal Transverse Mercator (UTM)-projectie wordt gedefinieerd door acht parameters.
title: Universal Transverse Mercator-projecties
uuid: 55421412-5c68-4a4f-88d6-650d5999a77c
exl-id: 7d7610c3-14e7-474e-b792-ad413c86a2ef
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '333'
ht-degree: 0%

---

# Universal Transverse Mercator-projecties{#universal-transverse-mercator-projections}

{{eol}}

De Universal Transverse Mercator (UTM)-projectie wordt gedefinieerd door acht parameters.

Wanneer u een Universal Transverse Mercator-projectie opgeeft voor een achtergrondafbeeldingslaag, moeten de bestanden van de terreinafbeelding worden uitgelijnd met false (geprojecteerd) ten noorden in de richting van de bovenkant van de afbeelding en met false ten oosten rechts van de afbeelding.

Als u een UTM-projectie wilt opgeven voor een willekeurige terreinafbeeldingsbron, moet u het dialoogvenster [!DNL Terrain Images.cfg] in een teksteditor, zoals Kladblok, de parameter Projectie-info instellen op &quot;TransverseMercatorProjection&quot; en instellingen toevoegen voor de UTM-projectie.

**Een Universal Transverse Mercator-projectie opgeven**

1. In de [!DNL Server Files Manager], klikt u op **[!UICONTROL Components]** om de inhoud te bekijken. De [!DNL Terrain Images.cfg] bestand bevindt zich in deze map.

1. Klik met de rechtermuisknop op het vinkje in het dialoogvenster *servernaam* kolom voor [!DNL Terrain Images.cfg]en klik vervolgens op **[!UICONTROL Make Local]**. Er verschijnt een vinkje in het dialoogvenster [!DNL Temp] kolom voor [!DNL Terrain Images.cfg].

1. Klik met de rechtermuisknop op het nieuwe vinkje in het dialoogvenster [!DNL Temp] kolom en klik op **[!UICONTROL Open]** > **[!UICONTROL in Notepad]**. De [!DNL Terrain Images.cfg]wordt weergegeven in een Kladblok-venster.

1. Bewerk de parameters voor projectie-info met behulp van het volgende voorbeeldbestandsfragment en de parametertabel als hulplijnen. Zorg ervoor dat u het projectietype opgeeft, zoals hieronder wordt gemarkeerd.

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
| Ellipsoïde inverse Flatting, Ellipsoid Semimajor-as | De parameters van de ellipsoïde die voor de projectie worden gebruikt. De halfafbeeldingsas wordt opgegeven in meters. |
| Onjuiste bewerking | De onechte afdekking van de centrale meridiaan van de projectie, in meters. Voor UTM is dit altijd 500.000. |
| False Northing | Het onwaar normaalpunt van de evenaar in de projectie, in meters. Voor UTM is dit 0 voor de noordelijke halfronde en 10.000 voor de zuidelijke halfronde gebieden. |
| Northwest Corner Coordinates, coördinaten zuidoosthoek | De coördinaten (in geprojecteerde meters) van de linkerbovenhoek en rechteronderhoek van de afbeelding. |
| Premier Meridian | De lengtegraad van de centrale meridiaan van de projectie, in graden ten oosten van Greenwich. Negatieve getallen kunnen worden gebruikt om graden naar west op te geven. |
| Schaalfactor | De verhouding tussen de straal van de projectiefilter en de halve afbeeldingsas van de ellips. Voor UTM-projecties (Universal Transverse Mercator) is dit altijd 0,9996. |
