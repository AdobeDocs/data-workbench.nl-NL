---
description: Het breedtegraad-projectieformaat (LatLonProjection) in het Terrain Images.cfg-bestand wordt gedefinieerd door vier parameters voor breedte en lengte.
solution: Analytics
title: Latitude-breedteprojecties
topic: Data workbench
uuid: 0ac947d6-3cd6-4272-96ae-456d2835e63f
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Latitude-breedteprojecties{#latitude-longitude-projections}

Het breedtegraad-projectieformaat (LatLonProjection) in het Terrain Images.cfg-bestand wordt gedefinieerd door vier parameters voor breedte en lengte.

Om een LatLonProjection voor niet geprojecteerde beelden (ruwe niet geprojecteerde bitmaps en algemene beelden, niet geprojecteerd) te specificeren, kunt u montages voor LatLonProjection binnen het [!DNL Terrain Images.cfg] venster in de werkbank van gegevens ingaan. Zie [Een LatLonProjection opgeven voor niet-geprojecteerde afbeeldingen](../../../../../home/c-geo-oview/c-wk-img-lyrs/c-trn-img-lyrs/c-proj-info-trn-imgs/c-lat-long-proj.md#section-26554eefe645481faba68396fa13756a).

Om een LatLonProjection voor beelden met ingebedde projectieinformatie te specificeren, moet u het [!DNL Terrain Images.cfg] dossier in een tekstredacteur zoals Blocnote openen, de parameter van Info van de Projectie aan &quot;LatLonProjection&quot;plaatsen, en montages toevoegen voor LatLonProjection. Zie [Om een LatLonProjection voor beelden binnen ingebedde projectieinformatie te specificeren...](../../../../../home/c-geo-oview/c-wk-img-lyrs/c-trn-img-lyrs/c-proj-info-trn-imgs/c-lat-long-proj.md#section-174f4e00fad84a7ca0c995423dd37ae1).

* [Om een LatLonProjection voor Niet geprojecteerde Beelden te specificeren](../../../../../home/c-geo-oview/c-wk-img-lyrs/c-trn-img-lyrs/c-proj-info-trn-imgs/c-lat-long-proj.md#section-26554eefe645481faba68396fa13756a)
* [Om een LatLonProjection voor Beelden te specificeren binnen de Geïntegreerde Informatie van de Projectie...](../../../../../home/c-geo-oview/c-wk-img-lyrs/c-trn-img-lyrs/c-proj-info-trn-imgs/c-lat-long-proj.md#section-174f4e00fad84a7ca0c995423dd37ae1)

## Om een LatLonProjection voor Niet geprojecteerde Beelden te specificeren {#section-26554eefe645481faba68396fa13756a}

1. Open het [!DNL Terrain Images.cfg] dossier in gegevenswerkbank en voeg een bron van de laag van het terreinbeeld toe zoals die in wordt beschreven [om een laag](../../../../../home/c-geo-oview/c-wk-img-lyrs/c-trn-img-lyrs/c-trn-img-lyrs.md#concept-8a0a16013e824ac29f35a0349b5d8ccf)van het terreinbeeld te bepalen.

1. Geef de parameters van Info van de Projectie uit gebruikend de volgende parameterlijst als gids:

   | Parameter | Beschrijving |
   |---|---|
   | Lat0 | De breedtegraad van de bovenste rand van het beeld, in graden, waar 90 de Noordpool is en -90 de Zuidpool. |
   | Lat1 | De breedtegraad van de onderste rand van het beeld. |
   | Lon0 | De lengtegraad van de linkerrand van het beeld, in graden, waar de positieve aantallen oost zijn en de negatieve aantallen zijn westerlengte. |
   | Lon1 | De lengte van de rechterrand van het beeld. |

1. Sparen het dossier door **[!UICONTROL (modified)]** bij de bovenkant van het venster met de rechtermuisknop aan te klikken en te klikken **[!UICONTROL Save]**.

1. Als u de lokaal aangebrachte wijzigingen in het systeem van de gegevenswerkbank wilt opslaan, klikt u in het [!DNL Server Files Manager]selectievakje met de rechtermuisknop op het vinkje voor [!DNL Terrain Images.cfg] in de [!DNL Temp] kolom en klikt u op **[!UICONTROL Save to]** > *&lt;**[!UICONTROL server name]**>*.

## Om een LatLonProjection voor Beelden binnen de ingebedde Informatie van de Projectie te specificeren {#section-174f4e00fad84a7ca0c995423dd37ae1}

1. In [!DNL Server Files Manager], klik **[!UICONTROL Components]** om zijn inhoud te bekijken. Het [!DNL Terrain Images.cfg] dossier wordt gevestigd binnen deze folder.

1. Klik het vinkje in de kolom van de servernaam voor met de rechtermuisknop aan [!DNL Terrain Images.cfg], dan klik **[!UICONTROL Make Local]**. Een vinkje verschijnt in de [!DNL Temp] kolom voor [!DNL Terrain Images.cfg].

1. Klik het pas gecreëerde vinkje in de [!DNL Temp] kolom met de rechtermuisknop aan en klik **[!UICONTROL Open]** > **[!UICONTROL in Notepad]**. Het [!DNL Terrain Images.cfg] dossier verschijnt in een venster van de Blocnote.

1. Geef de parameters van Info van de Projectie uit gebruikend het volgende fragment van het steekproefdossier als gids. Ben zeker om het projectietype te specificeren zoals hieronder benadrukt. Voor beschrijvingen van de parameters, zie de lijst van Parameters LatLonProjection in de vorige procedure.

   ```
   Projection Info = LatLonProjection: 
     Lat0 = double: 90
     Lat1 = double: -90
     Lon0 = double: -180
     Lon1 = double: 180
   ```

