---
description: De breedte-lengteprojectie-indeling (LatLonProjection) in het bestand Terrain Images.cfg wordt gedefinieerd door vier parameters voor breedte en lengte.
title: Breedtegraad-lengteprojecties
uuid: 0ac947d6-3cd6-4272-96ae-456d2835e63f
exl-id: 67ebc7a8-3046-4524-b3a0-0b6da2f235fc
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '386'
ht-degree: 1%

---

# Breedtegraad-lengteprojecties{#latitude-longitude-projections}

{{eol}}

De breedte-lengteprojectie-indeling (LatLonProjection) in het bestand Terrain Images.cfg wordt gedefinieerd door vier parameters voor breedte en lengte.

Als u een LatLonProjection wilt opgeven voor niet-geprojecteerde afbeeldingen (onbewerkte niet-geprojecteerde bitmaps en algemene afbeeldingen, niet-geprojecteerd), kunt u instellingen voor de LatLonProjection opgeven in het gedeelte [!DNL Terrain Images.cfg] venster in de werkbank voor gegevens. Zie [Een LatLonProjection opgeven voor niet-geprojecteerde afbeeldingen](../../../../../home/c-geo-oview/c-wk-img-lyrs/c-trn-img-lyrs/c-proj-info-trn-imgs/c-lat-long-proj.md#section-26554eefe645481faba68396fa13756a).

Als u een LatLonProjection wilt opgeven voor afbeeldingen met ingesloten projectiegegevens, moet u het dialoogvenster [!DNL Terrain Images.cfg] in een teksteditor zoals Kladblok de parameter Projectie-info instellen op &quot;LatLonProjection&quot; en instellingen voor LatLonProjection toevoegen. Zie [Een LatLonProjection opgeven voor afbeeldingen binnen ingesloten projectiegegevens...](../../../../../home/c-geo-oview/c-wk-img-lyrs/c-trn-img-lyrs/c-proj-info-trn-imgs/c-lat-long-proj.md#section-174f4e00fad84a7ca0c995423dd37ae1).

* [Een LatLonProjection opgeven voor niet-geprojecteerde afbeeldingen](../../../../../home/c-geo-oview/c-wk-img-lyrs/c-trn-img-lyrs/c-proj-info-trn-imgs/c-lat-long-proj.md#section-26554eefe645481faba68396fa13756a)
* [Een LatLonProjection opgeven voor afbeeldingen binnen ingesloten projectiegegevens...](../../../../../home/c-geo-oview/c-wk-img-lyrs/c-trn-img-lyrs/c-proj-info-trn-imgs/c-lat-long-proj.md#section-174f4e00fad84a7ca0c995423dd37ae1)

## Een LatLonProjection opgeven voor niet-geprojecteerde afbeeldingen {#section-26554eefe645481faba68396fa13756a}

1. Open de [!DNL Terrain Images.cfg] bestand in gegevenswerkbank en voeg een terreinafbeeldingslaagbron toe zoals beschreven in [Een achtergrondafbeeldingslaag definiëren](../../../../../home/c-geo-oview/c-wk-img-lyrs/c-trn-img-lyrs/c-trn-img-lyrs.md#concept-8a0a16013e824ac29f35a0349b5d8ccf).

1. Bewerk de parameters voor projectie-info met behulp van de volgende parametertabel als richtlijn:

   | Parameter | Beschrijving |
   |---|---|
   | Lat0 | De breedtegraad van de bovenrand van de afbeelding, in graden, waarbij 90 de Noordpool is en -90 de Zuidpool. |
   | Lat1 | De breedtegraad van de onderrand van de afbeelding. |
   | Lon0 | De lengtegraad van de linkerrand van de afbeelding, in graden, waarbij positieve getallen oost en negatieve getallen westerlengte zijn. |
   | Lon1 | De lengtegraad van de rechterrand van de afbeelding. |

1. Sla het bestand op door met de rechtermuisknop te klikken **[!UICONTROL (modified)]** boven aan het venster en klikken op **[!UICONTROL Save]**.

1. Als u de lokaal aangebrachte wijzigingen wilt opslaan in de computer met de gegevenswerkbankserver, gaat u naar [!DNL Server Files Manager], klikt u met de rechtermuisknop op het vinkje voor [!DNL Terrain Images.cfg] in de [!DNL Temp] kolom, klik vervolgens op **[!UICONTROL Save to]** > *&lt;**[!UICONTROL server name]**>*.

## Een LatLonProjection opgeven voor afbeeldingen binnen ingesloten projectiegegevens {#section-174f4e00fad84a7ca0c995423dd37ae1}

1. In de [!DNL Server Files Manager], klikt u op **[!UICONTROL Components]** om de inhoud te bekijken. De [!DNL Terrain Images.cfg] bestand bevindt zich in deze map.

1. Klik met de rechtermuisknop op het vinkje in de kolom Servernaam voor [!DNL Terrain Images.cfg]en klik vervolgens op **[!UICONTROL Make Local]**. Er verschijnt een vinkje in het dialoogvenster [!DNL Temp] kolom voor [!DNL Terrain Images.cfg].

1. Klik met de rechtermuisknop op het nieuwe vinkje in het dialoogvenster [!DNL Temp] kolom en klik op **[!UICONTROL Open]** > **[!UICONTROL in Notepad]**. De [!DNL Terrain Images.cfg] wordt weergegeven in een Kladblok-venster.

1. Bewerk de parameters voor projectie-info met behulp van het volgende voorbeeldbestandsfragment als richtlijn. Zorg ervoor dat u het projectietype opgeeft, zoals hieronder wordt gemarkeerd. Voor beschrijvingen van de parameters, zie de lijst van Parameters LatLonProjection in de vorige procedure.

   ```
   Projection Info = LatLonProjection: 
     Lat0 = double: 90
     Lat1 = double: -90
     Lon0 = double: -180
     Lon1 = double: 180
   ```
