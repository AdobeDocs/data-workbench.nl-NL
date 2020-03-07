---
description: De werkbank van gegevens steunt zowel breedtegraad-lengteprojecties als de Universele projecties van de Transverse Mercator (UTM) voor alle bronnen van de gebiedsbeeldlaag.
solution: Analytics
title: Specificeer projectieinformatie voor terreinbeelden
topic: Data workbench
uuid: cc1e1e35-6b23-4121-a9f5-489001cb2ef8
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Specificeer projectieinformatie voor terreinbeelden{#specify-projection-information-for-terrain-images}

De werkbank van gegevens steunt zowel breedtegraad-lengteprojecties als de Universele projecties van de Transverse Mercator (UTM) voor alle bronnen van de gebiedsbeeldlaag.

Projectie-informatie is vereist voor niet-geprojecteerde niet-geprojecteerde bitmaps en algemene afbeeldingen, niet geprojecteerd. U kunt projectieinformatie voor beelden met ingebedde projectieinformatie specificeren, hoewel het gewoonlijk niet wordt vereist omdat de parameters van de projectie automatisch van geodetische gegevens worden bepaald ingebed in het beeld zelf. De volgende secties verstrekken details over het specificeren van deze projectieformaten in het [!DNL Terrain Images.cfg] dossier.

## Latitude-breedteprojecties {#section-6e335357ec28462ba39c565e0a5986c7}

Het breedtegraad-projectieformaat (LatLonProjection) in het [!DNL Terrain Images.cfg] dossier wordt bepaald door vier parameters voor breedte en lengtegraad.

Om een LatLonProjection voor niet geprojecteerde beelden (ruwe niet geprojecteerde bitmaps en algemene beelden, niet geprojecteerd) te specificeren, kunt u montages voor LatLonProjection binnen het [!DNL Terrain Images.cfg] venster in de Werkbank van Gegevens ingaan.

Om een LatLonProjection voor beelden met ingebedde projectieinformatie te specificeren, moet u het [!DNL Terrain Images.cfg] dossier in een tekstredacteur zoals Blocnote openen, de parameter van Info van de Projectie plaatsen aan LatLonProjection, en montages toevoegen voor [!DNL LatLonProjection]het.

**Om een LatLonProjection voor niet geprojecteerde beelden te specificeren**

1. Open het [!DNL Terrain Images.cfg] dossier in de Werkbank van Gegevens en voeg een bron van de laag van het terreinbeeld toe zoals die in wordt beschreven [om een laag](../../../../home/c-get-started/c-im-layers/c-ter-img-layers/c-ter-img-layers.md#concept-f4b3a20969354ca38955e3fd5beb0f4f)van het terreinbeeld te bepalen.
1. Geef de parameters van Info van de Projectie uit gebruikend de volgende parameterlijst als gids:

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
   <td colname="col2"> <p>De breedtegraad van de bovenste rand van het beeld, in graden, waar 90 de Noordpool is en -90 de Zuidpool. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Lat1 </p> </td> 
   <td colname="col2"> <p>De breedtegraad van de onderste rand van het beeld. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Lon0 </p> </td> 
   <td colname="col2"> <p>De lengtegraad van de linkerrand van het beeld, in graden, waar de positieve aantallen oost zijn en de negatieve aantallen zijn westerlengte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Lon1 </p> </td> 
   <td colname="col2"> <p>De lengte van de rechterrand van het beeld. </p> </td> 
  </tr> 
 </tbody> 
</table>

1. Sparen het dossier door **[!UICONTROL (modified)]** bij de bovenkant van het venster met de rechtermuisknop aan te klikken en te klikken **[!UICONTROL Save]**.
1. Om de plaatselijk aangebrachte veranderingen in de de servercomputer van de Werkbank van Gegevens te bewaren, in de [!DNL Server Files Manager], klik het vinkje voor [!DNL Terrain Images.cfg] in de [!DNL Temp] kolom met de rechtermuisknop aan, dan klik **[!UICONTROL Save to]** > *&lt;**[!UICONTROL server name]**>*.

**Om een LatLonProjection voor beelden binnen ingebedde projectieinformatie te specificeren**

In [!DNL Server Files Manager], klik **[!UICONTROL Components]** om zijn inhoud te bekijken. Het [!DNL Terrain Images.cfg] dossier wordt gevestigd binnen deze folder.

Klik het vinkje in de kolom van de servernaam voor met de rechtermuisknop aan [!DNL Terrain Images.cfg], dan klik **[!UICONTROL Make Local]**. Een vinkje verschijnt in de [!DNL Temp] kolom voor [!DNL Terrain Images.cfg].

Klik het pas gecreëerde vinkje in de [!DNL Temp] kolom met de rechtermuisknop aan en klik **[!UICONTROL Open]** > **[!UICONTROL in Notepad]**. Het [!DNL Terrain Images.cfg] dossier verschijnt in een venster van de Blocnote.

Geef de parameters van Info van de Projectie uit gebruikend het volgende fragment van het steekproefdossier als gids. Ben zeker om het projectietype te specificeren zoals hieronder benadrukt. Voor beschrijvingen van de parameters, zie de lijst van Parameters LatLonProjection in de vorige procedure.

```
Projection Info = LatLonProjection:
  Lat0 = double: 90
  Lat1 = double: -90
  Lon0 = double: -180
  Lon1 = double: 180
```

## Universal Transverse Mercator-projecties {#section-606df0ed1c2d4a6bac3ff0fa2cfb3e82}

De Universal Transverse Mercator (UTM)-projectie wordt gedefinieerd door acht parameters. Wanneer u een Universal Transverse Mercator-projectie opgeeft voor een laag met een terreinafbeelding, moeten uw bestanden met een terreinafbeelding worden uitgelijnd met een false (geprojecteerd) noordwaarts naar de bovenkant van de afbeelding en met een false oost naar rechts van de afbeelding.

Om een projectie UTM voor om het even welke bron van het terreinbeeld te specificeren, moet u het [!DNL Terrain Images.cfg] dossier in een tekstredacteur zoals Blocnote openen, de parameter van Info van de Projectie plaatsen aan &quot;TransverseMercatorProjection&quot;, en montages toevoegen voor de projectie UTM.

**Om een Universal Transverse Mercator-projectie te specificeren**

1. In [!DNL Server Files Manager], klik **[!UICONTROL Components]** om zijn inhoud te bekijken. Het [!DNL Terrain Images.cfg] dossier wordt gevestigd binnen deze folder.
1. Klik het vinkje in de kolom van de servernaam voor met de rechtermuisknop aan [!DNL Terrain Images.cfg], dan klik **[!UICONTROL Make Local]**. Een vinkje verschijnt in de [!DNL Temp] kolom voor [!DNL Terrain Images.cfg.]
1. Klik het pas gecreëerde vinkje in de [!DNL Temp] kolom met de rechtermuisknop aan en klik **[!UICONTROL Open]** > **[!UICONTROL in Notepad]**. Het [!DNL Terrain Images.cfg] dossier verschijnt in een venster van de Blocnote.
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

<table id="table_71AEEAE808B9436B9846987A54D5D1D2"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Parameter </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Ellipsoïde inverse afvlakking, Ellipsoïde Semimajor-as </p> </td> 
   <td colname="col2"> <p>De parameters van de ellipsoïde die voor de projectie wordt gebruikt. De semimajoras wordt gespecificeerd in meters. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Valse zoekactie </p> </td> 
   <td colname="col2"> <p>De valse verassing van de middelste meridiaan van de projectie, in meter. Voor UTM is dit altijd 500.000. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>False Northing </p> </td> 
   <td colname="col2"> <p>Het valse noord van de evenaar in de projectie, in meters. Voor UTM, is dit 0 voor de gebieden van het noordelijk halfrond en 10.000 voor de gebieden van het zuidelijk halfrond. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Northwest Corner Coordinates, Coördinaten zuidoost Corner </p> </td> 
   <td colname="col2"> <p>De coördinaten (in geprojecteerde meters) van de hoogste linker en bodem juiste hoeken van het beeld. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Premier Meridian </p> </td> 
   <td colname="col2"> <p>De lengtegraad van de middelste meridiaan van de projectie, gespecificeerd in graden ten oosten van Greenwich. De negatieve aantallen kunnen worden gebruikt om graden west te specificeren. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Schaalfactor </p> </td> 
   <td colname="col2"> <p>De verhouding tussen de straal van de projectiekilinder en de puntbeeldas van de ellips. Voor UTM-projecties (Universal Transverse Mercator) is dit altijd 0,9996. </p> </td> 
  </tr> 
 </tbody> 
</table>

