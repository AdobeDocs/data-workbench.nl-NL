---
description: Gegevenswerkbank ondersteunt zowel breedtegraad-lengteprojecties als UTM-projecties (Universal Transverse Mercator) voor alle terreinafbeeldingslaagbronnen.
title: Projectiegegevens opgeven voor terreinbeelden
uuid: cc1e1e35-6b23-4121-a9f5-489001cb2ef8
exl-id: 2638c5d4-164d-411b-8464-0a3af81b6537
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '751'
ht-degree: 0%

---

# Projectiegegevens opgeven voor terreinbeelden{#specify-projection-information-for-terrain-images}

{{eol}}

Gegevenswerkbank ondersteunt zowel breedtegraad-lengteprojecties als UTM-projecties (Universal Transverse Mercator) voor alle terreinafbeeldingslaagbronnen.

Projectie-informatie is vereist voor onbewerkte, niet-geprojecteerde bitmaps en algemene afbeeldingen. U kunt projectiegegevens opgeven voor afbeeldingen met ingesloten projectiegegevens, maar dit is gewoonlijk niet nodig omdat de parameters van de projectie automatisch worden bepaald op basis van geordetische gegevens die in de afbeelding zelf zijn ingesloten. In de volgende secties vindt u informatie over het opgeven van deze projectindelingen in de [!DNL Terrain Images.cfg] bestand.

## Breedtegraad-lengteprojecties {#section-6e335357ec28462ba39c565e0a5986c7}

De breedte-lengteprojectie-indeling (LatLonProjection) in de [!DNL Terrain Images.cfg] bestand wordt gedefinieerd door vier parameters voor breedte en lengte.

Als u een LatLonProjection wilt opgeven voor niet-geprojecteerde afbeeldingen (onbewerkte niet-geprojecteerde bitmaps en algemene afbeeldingen, niet-geprojecteerd), kunt u instellingen voor de LatLonProjection opgeven in het gedeelte [!DNL Terrain Images.cfg] venster in Data Workbench.

Als u een LatLonProjection wilt opgeven voor afbeeldingen met ingesloten projectiegegevens, moet u het dialoogvenster [!DNL Terrain Images.cfg] bestand in een teksteditor, zoals Kladblok, stelt de parameter Projectie-info in op LatLonProjection en voegt instellingen voor de [!DNL LatLonProjection].

**Een LatLonProjection opgeven voor niet-geprojecteerde afbeeldingen**

1. Open de [!DNL Terrain Images.cfg] bestand in Data Workbench en voeg een laagbron voor terreinafbeelding toe zoals beschreven in [Een achtergrondafbeeldingslaag definiëren](../../../../home/c-get-started/c-im-layers/c-ter-img-layers/c-ter-img-layers.md#concept-f4b3a20969354ca38955e3fd5beb0f4f).
1. Bewerk de parameters voor projectie-info met behulp van de volgende parametertabel als richtlijn:

<table id="table_32F6EADB2DA34592ABD6FFAC9E00BB27"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Parameter </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Lat0 </p> </td> 
   <td colname="col2"> <p>De breedtegraad van de bovenrand van de afbeelding, in graden, waarbij 90 de Noordpool is en -90 de Zuidpool. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Lat1 </p> </td> 
   <td colname="col2"> <p>De breedtegraad van de onderrand van de afbeelding. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Lon0 </p> </td> 
   <td colname="col2"> <p>De lengtegraad van de linkerrand van de afbeelding, in graden, waarbij positieve getallen oost en negatieve getallen westerlengte zijn. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Lon1 </p> </td> 
   <td colname="col2"> <p>De lengtegraad van de rechterrand van de afbeelding. </p> </td> 
  </tr> 
 </tbody> 
</table>

1. Sla het bestand op door met de rechtermuisknop te klikken **[!UICONTROL (modified)]** boven aan het venster en klikken op **[!UICONTROL Save]**.
1. Om plaatselijk aangebrachte veranderingen in de servercomputer van de Data Workbench op te slaan, in [!DNL Server Files Manager], klikt u met de rechtermuisknop op het vinkje voor [!DNL Terrain Images.cfg] in de [!DNL Temp] kolom, klik vervolgens op **[!UICONTROL Save to]** > *&lt;**[!UICONTROL server name]**>*.

**Een LatLonProjection opgeven voor afbeeldingen binnen ingesloten projectiegegevens**

In de [!DNL Server Files Manager], klikt u op **[!UICONTROL Components]** om de inhoud te bekijken. De [!DNL Terrain Images.cfg] bestand bevindt zich in deze map.

Klik met de rechtermuisknop op het vinkje in de kolom Servernaam voor [!DNL Terrain Images.cfg]en klik vervolgens op **[!UICONTROL Make Local]**. Er verschijnt een vinkje in het dialoogvenster [!DNL Temp] kolom voor [!DNL Terrain Images.cfg].

Klik met de rechtermuisknop op het nieuwe vinkje in het dialoogvenster [!DNL Temp] kolom en klik op **[!UICONTROL Open]** > **[!UICONTROL in Notepad]**. De [!DNL Terrain Images.cfg] wordt weergegeven in een Kladblok-venster.

Bewerk de parameters voor projectie-info met behulp van het volgende voorbeeldbestandsfragment als richtlijn. Zorg ervoor dat u het projectietype opgeeft, zoals hieronder wordt gemarkeerd. Voor beschrijvingen van de parameters, zie de lijst van Parameters LatLonProjection in de vorige procedure.

```
Projection Info = LatLonProjection:
  Lat0 = double: 90
  Lat1 = double: -90
  Lon0 = double: -180
  Lon1 = double: 180
```

## Universal Transverse Mercator-projecties {#section-606df0ed1c2d4a6bac3ff0fa2cfb3e82}

De Universal Transverse Mercator (UTM)-projectie wordt gedefinieerd door acht parameters. Wanneer u een Universal Transverse Mercator-projectie opgeeft voor een achtergrondafbeeldingslaag, moeten de bestanden van de terreinafbeelding worden uitgelijnd met false (geprojecteerd) ten noorden in de richting van de bovenkant van de afbeelding en met false ten oosten rechts van de afbeelding.

Als u een UTM-projectie wilt opgeven voor een willekeurige terreinafbeeldingsbron, moet u het dialoogvenster [!DNL Terrain Images.cfg] in een teksteditor, zoals Kladblok, de parameter Projectie-info instellen op &quot;TransverseMercatorProjection&quot; en instellingen toevoegen voor de UTM-projectie.

**Een Universal Transverse Mercator-projectie opgeven**

1. In de [!DNL Server Files Manager], klikt u op **[!UICONTROL Components]** om de inhoud te bekijken. De [!DNL Terrain Images.cfg] bestand bevindt zich in deze map.
1. Klik met de rechtermuisknop op het vinkje in de kolom Servernaam voor [!DNL Terrain Images.cfg]en klik vervolgens op **[!UICONTROL Make Local]**. Er verschijnt een vinkje in het dialoogvenster [!DNL Temp] kolom voor [!DNL Terrain Images.cfg.]
1. Klik met de rechtermuisknop op het nieuwe vinkje in het dialoogvenster [!DNL Temp] kolom en klik op **[!UICONTROL Open]** > **[!UICONTROL in Notepad]**. De [!DNL Terrain Images.cfg] wordt weergegeven in een Kladblok-venster.
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

<table id="table_71AEEAE808B9436B9846987A54D5D1D2"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Parameter </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Ellipsoïde inverse Flatting, Ellipsoid Semimajor-as </p> </td> 
   <td colname="col2"> <p>De parameters van de ellipsoïde die voor de projectie worden gebruikt. De halfafbeeldingsas wordt opgegeven in meters. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Onjuiste bewerking </p> </td> 
   <td colname="col2"> <p>De onechte afdekking van de centrale meridiaan van de projectie, in meters. Voor UTM is dit altijd 500.000. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>False Northing </p> </td> 
   <td colname="col2"> <p>Het onwaar normaalpunt van de evenaar in de projectie, in meters. Voor UTM is dit 0 voor de noordelijke halfronde en 10.000 voor de zuidelijke halfronde gebieden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Northwest Corner Coordinates, coördinaten zuidoosthoek </p> </td> 
   <td colname="col2"> <p>De coördinaten (in geprojecteerde meters) van de linkerbovenhoek en rechteronderhoek van de afbeelding. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Premier Meridian </p> </td> 
   <td colname="col2"> <p>De lengtegraad van de centrale meridiaan van de projectie, in graden ten oosten van Greenwich. Negatieve getallen kunnen worden gebruikt om graden naar west op te geven. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Schaalfactor </p> </td> 
   <td colname="col2"> <p>De verhouding tussen de straal van de projectiefilter en de halve afbeeldingsas van de ellips. Voor UTM-projecties (Universal Transverse Mercator) is dit altijd 0,9996. </p> </td> 
  </tr> 
 </tbody> 
</table>
