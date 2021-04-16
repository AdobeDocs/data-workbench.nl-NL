---
description: De breedte-lengteprojectie-indeling (LatLonProjection) in het bestand Terrain Images.cfg wordt gedefinieerd door vier parameters voor breedte en lengte.
title: Breedtegraad-lengteprojecties
uuid: 0ac947d6-3cd6-4272-96ae-456d2835e63f
exl-id: 67ebc7a8-3046-4524-b3a0-0b6da2f235fc
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '386'
ht-degree: 1%

---

# Breedtegraad-lengteprojecties{#latitude-longitude-projections}

De breedte-lengteprojectie-indeling (LatLonProjection) in het bestand Terrain Images.cfg wordt gedefinieerd door vier parameters voor breedte en lengte.

Als u een LatLonProjection wilt opgeven voor niet-geprojecteerde afbeeldingen (onbewerkte niet-geprojecteerde bitmaps en algemene afbeeldingen, niet geprojecteerd), kunt u instellingen voor de LatLonProjection invoeren in het venster [!DNL Terrain Images.cfg] in de werkbank voor gegevens. Zie [Een LatLonProjection opgeven voor niet-geprojecteerde afbeeldingen](../../../../../home/c-geo-oview/c-wk-img-lyrs/c-trn-img-lyrs/c-proj-info-trn-imgs/c-lat-long-proj.md#section-26554eefe645481faba68396fa13756a).

Als u een LatLonProjection wilt opgeven voor afbeeldingen met ingesloten projectiegegevens, moet u het [!DNL Terrain Images.cfg]-bestand openen in een teksteditor zoals Kladblok, de parameter Projectie-info instellen op &quot;LatLonProjection&quot; en instellingen toevoegen voor LatLonProjection. Zie [Een LatLonProjection opgeven voor afbeeldingen binnen ingesloten projectiegegevens...](../../../../../home/c-geo-oview/c-wk-img-lyrs/c-trn-img-lyrs/c-proj-info-trn-imgs/c-lat-long-proj.md#section-174f4e00fad84a7ca0c995423dd37ae1).

* [Een LatLonProjection opgeven voor niet-geprojecteerde afbeeldingen](../../../../../home/c-geo-oview/c-wk-img-lyrs/c-trn-img-lyrs/c-proj-info-trn-imgs/c-lat-long-proj.md#section-26554eefe645481faba68396fa13756a)
* [Een LatLonProjection opgeven voor afbeeldingen binnen ingesloten projectiegegevens...](../../../../../home/c-geo-oview/c-wk-img-lyrs/c-trn-img-lyrs/c-proj-info-trn-imgs/c-lat-long-proj.md#section-174f4e00fad84a7ca0c995423dd37ae1)

## Een LatLonProjection opgeven voor niet-geprojecteerde afbeeldingen {#section-26554eefe645481faba68396fa13756a}

1. Open het [!DNL Terrain Images.cfg] dossier in gegevenswerkbank en voeg een bron van de de beeldlaag van het terrein toe zoals die in [wordt beschreven om een laag van het gebiedsbeeld te bepalen](../../../../../home/c-geo-oview/c-wk-img-lyrs/c-trn-img-lyrs/c-trn-img-lyrs.md#concept-8a0a16013e824ac29f35a0349b5d8ccf).

1. Bewerk de parameters voor projectie-info met behulp van de volgende parametertabel als richtlijn:

   | Parameter | Beschrijving |
   |---|---|
   | Lat0 | De breedtegraad van de bovenrand van de afbeelding, in graden, waarbij 90 de Noordpool is en -90 de Zuidpool. |
   | Lat1 | De breedtegraad van de onderrand van de afbeelding. |
   | Lon0 | De lengtegraad van de linkerrand van de afbeelding, in graden, waarbij positieve getallen oost en negatieve getallen westerlengte zijn. |
   | Lon1 | De lengtegraad van de rechterrand van de afbeelding. |

1. Sla het bestand op door met de rechtermuisknop op **[!UICONTROL (modified)]** boven in het venster te klikken en op **[!UICONTROL Save]** te klikken.

1. Als u de lokaal aangebrachte wijzigingen in de gegevenswerkbankservercomputer wilt opslaan, klikt u in [!DNL Server Files Manager] met de rechtermuisknop op het vinkje voor [!DNL Terrain Images.cfg] in de kolom [!DNL Temp] en vervolgens op **[!UICONTROL Save to]** > *&lt;**[!UICONTROL server name]**>*.

## Een LatLonProjection opgeven voor afbeeldingen binnen ingesloten projectiegegevens {#section-174f4e00fad84a7ca0c995423dd37ae1}

1. Klik in [!DNL Server Files Manager] op **[!UICONTROL Components]** om de inhoud ervan weer te geven. Het [!DNL Terrain Images.cfg]-bestand bevindt zich in deze map.

1. Klik met de rechtermuisknop op het vinkje in de kolom Servernaam voor [!DNL Terrain Images.cfg] en klik vervolgens op **[!UICONTROL Make Local]**. In de kolom [!DNL Temp] wordt een vinkje weergegeven voor [!DNL Terrain Images.cfg].

1. Klik met de rechtermuisknop op het nieuwe vinkje in de kolom [!DNL Temp] en klik op **[!UICONTROL Open]** > **[!UICONTROL in Notepad]**. Het [!DNL Terrain Images.cfg] dossier verschijnt in een venster van de Blocnote.

1. Bewerk de parameters voor projectie-info met behulp van het volgende voorbeeldbestandsfragment als richtlijn. Zorg ervoor dat u het projectietype opgeeft, zoals hieronder wordt gemarkeerd. Voor beschrijvingen van de parameters, zie de lijst van Parameters LatLonProjection in de vorige procedure.

   ```
   Projection Info = LatLonProjection: 
     Lat0 = double: 90
     Lat1 = double: -90
     Lon0 = double: -180
     Lon1 = double: 180
   ```
