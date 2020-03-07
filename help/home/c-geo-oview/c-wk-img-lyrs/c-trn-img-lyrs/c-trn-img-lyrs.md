---
description: Op een werkbank voor data toont een laag van het terreinbeeld de beelden van het terrein van de aarde.
solution: Analytics
title: Werken met Terrain Image Layers
topic: Data workbench
uuid: 2f23a2c8-f551-4b84-bd87-5d7053910ab3
translation-type: tm+mt
source-git-commit: 948c6dd04819e939b45745db573a53c8be51ce37

---


# Werken met Terrain Image Layers{#working-with-terrain-image-layers}

Op een werkbank voor data toont een laag van het terreinbeeld de beelden van het terrein van de aarde.

De het beeldlagen van het terrein worden opgeslagen in het [!DNL Geography] profiel, in een douaneformaat. Deze beeldlagen kunnen door Adobe worden geproduceerd, of de server van de gegevenswerkbank kan uw gebruiker-geleverde terreinbeelden in terreinlagen omzetten geschikt voor gebruik op de globale visualisatie.

>[!NOTE]
>
>Om met de lagen van het terreinbeeld te werken, moet u het [!DNL Terrain Images.cfg] dossier installeren dat door Adobe wordt verstrekt. Voor installatieinstructies, zie de [Installerende Geografie van de Werkbank van Gegevens](../../../../home/c-geo-oview/c-inst-geo/c-inst-geo.md).

Om een laag van het terreinbeeld te bepalen, moet u het volgende hebben:

* **Één of meerdere dossiers** van het terreinbeeld die de beelden bevatten die op de aardbol moeten worden getoond.
* **Een Terrain Images.cfg** -bestand dat de bestanden met terreinafbeeldingen aangeeft die voor de laag(en) moeten worden gebruikt. Het [!DNL Terrain Images.cfg] dossier laat u toe om één of meerdere bronnen toe te voegen om een laag van het terreinbeeld tot stand te brengen. Het formaat van uw dossier van het terreinbeeld bepaalt het type van bron dat u zou moeten toevoegen. De volgende lijst verstrekt beschrijvingen van de beschikbare bronnen van de de laaglaag van het terreinbeeld, met inbegrip van de gesteunde dossierformaten van het terreinbeeld:

<table id="table_BF8D5933BFBE45039BD164C258D3B450"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Type </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Ruwe niet-geprojecteerde bitmap </td> 
   <td colname="col2"> <p>Creeert de lagen van het terreinbeeld van 24 - beetje kopballoze RGB dossiers die breedtegraad-lengtegraad gericht (niet geprojecteerd) zijn, waar het noorden de bovenkant van het beeld is, en het oosten is het recht. </p> <p>Ondersteunde afbeeldingsindeling(en): RAUW </p> <p> <p>Opmerking: Deze bron vereist projectieinformatie. Voor informatie over projectieformaten, zie het <a href="../../../../home/c-geo-oview/c-wk-img-lyrs/c-trn-img-lyrs/c-proj-info-trn-imgs/c-proj-info-trn-imgs.md#concept-69b0c668038f4de9bf430a3a468a2abd"> Specificeren van de Informatie van de Projectie voor de Beelden</a>van het Terrein. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Algemeen beeld, niet geprojecteerd </td> 
   <td colname="col2"> <p>Creeert de lagen van het terreinbeeld van 24 - beetje, breedtegraad-lengtegraad gerichte (niet geprojecteerde) beeldformaten, waar het noorden de bovenkant van het beeld is, en het oosten is het recht. </p> <p>Ondersteunde afbeeldingsindeling(en): BMP, JPG, PNG, TIFF </p> <p> <p>Opmerking: Deze bron vereist projectieinformatie. Voor informatie over projectieformaten, zie het <a href="../../../../home/c-geo-oview/c-wk-img-lyrs/c-trn-img-lyrs/c-proj-info-trn-imgs/c-proj-info-trn-imgs.md#concept-69b0c668038f4de9bf430a3a468a2abd"> Specificeren van de Informatie van de Projectie voor de Beelden</a>van het Terrein. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Afbeelding met ingebouwde projectie </td> 
   <td colname="col2"> <p>Creeert de lagen van het terreinbeeld van beeldformaten die geodetische gegevens in het beelddossier inbedden. De projectieinformatie wordt uit het beeld gehaald. </p> <p>Ondersteunde afbeeldingsindeling(en): Erdas (IMG), GeoTIFF </p> <p> <p>Opmerking: Deze bron vereist gewoonlijk geen projectieinformatie maar steunt de toevoeging van dergelijke informatie indien nodig. Voor informatie over projectieformaten, zie het <a href="../../../../home/c-geo-oview/c-wk-img-lyrs/c-trn-img-lyrs/c-proj-info-trn-imgs/c-proj-info-trn-imgs.md#concept-69b0c668038f4de9bf430a3a468a2abd"> Specificeren van de Informatie van de Projectie voor de Beelden</a>van het Terrein. </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

**Om een laag van het terreinbeeld te bepalen**

1. In gegevenswerkbank, op het [!DNL Admin] > [!DNL Dataset and Profile] lusje, klik de **[!UICONTROL Servers Manager]** duimnagel om de [!DNL Servers Manager] werkruimte te openen.

1. Klik in het [!DNL Servers Manager] venster met de rechtermuisknop op het pictogram van de gewenste server op de gegevenswerkbank en klik op **[!UICONTROL Server Files]**.

1. In [!DNL Server Files Manager], klik **[!UICONTROL Components]** om zijn inhoud te bekijken. Het [!DNL Terrain Images.cfg] dossier wordt gevestigd binnen deze folder.

1. Klik het vinkje in de kolom van de servernaam voor met de rechtermuisknop aan [!DNL Terrain Images.cfg], dan klik **[!UICONTROL Make Local]**. Een vinkje verschijnt in de [!DNL Temp] kolom voor [!DNL Terrain Images.cfg.]

1. Klik het pas gecreëerde vinkje in de [!DNL Temp] kolom met de rechtermuisknop aan en klik **[!UICONTROL Open]** > **[!UICONTROL from the workbench]**. Het [!DNL Terrain Images.cfg]venster wordt weergegeven.

1. In het [!DNL Terrain Images] venster, klik **[!UICONTROL component]** om zijn inhoud te bekijken.

1. Klik met de rechtermuisknop **[!UICONTROL Sources]** > **[!UICONTROL Add new]** en kies een van de volgende brontypen:

   * **[!UICONTROL Raw unprojected bitmap]**. (Zodra toegevoegd, wordt dit brontype geëtiketteerd RawTerrainSource in het [!DNL Terrain Images] venster.)

   * **[!UICONTROL General image, unprojected]**. (Zodra toegevoegd, wordt dit brontype geëtiketteerd GDALTerrainSource in het [!DNL Terrain Images] venster.)

   * **[!UICONTROL Image with embedded projection]**. (Zodra toegevoegd, wordt dit brontype geëtiketteerd GDALTerrainSource in het [!DNL Terrain Images] venster.)

1. Geef zonodig de parameters voor de bron uit gebruikend het volgende steekproefdossier en de lijst van parameters als gidsen.

   ![](assets/cfg_TerrainImages_ALL.png)

<table id="table_83171CB58F8B4816BCCA9BFFD5ECD92A"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Parameter </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Gamma </td> 
   <td colname="col2"> Optioneel voor alle bronnen. Specificeert gammacorrectie die op het bronbeeld moet worden toegepast. Dit kan wenselijk zijn wegens het feit dat de gegevenswerkbank normaal met een hoge gamma het plaatsen loopt. De standaardwaarde is 1. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Hoogte </td> 
   <td colname="col2"> Vereist voor ruwe niet-geprojecteerde bitmap beelden. De hoogte van het bronbeeld in pixel. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Projectiegegevens </td> 
   <td colname="col2"> <p>Vereist voor ruwe niet-geprojecteerde bitmap beelden en algemene beelden, niet geprojecteerd, maar gesteund voor beelden met ingebedde projectie. De werkbank<span class="wintitle"> van gegevens Geography</span> steunt breedtegraad-lengteprojecties en de projecties van Transverse Mercator (TM) voor de lagen van het terreinbeeld. Het standaardprojectieformaat is de breedtegraad-projectie (LatLonProjection). </p> <p>Voor informatie over projectieformaten, zie het <a href="../../../../home/c-geo-oview/c-wk-img-lyrs/c-trn-img-lyrs/c-proj-info-trn-imgs/c-proj-info-trn-imgs.md#concept-69b0c668038f4de9bf430a3a468a2abd"> Specificeren van de Informatie van de Projectie voor de Beelden</a>van het Terrein. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Bronafbeelding </td> 
   <td colname="col2">Vereist voor alle bronnen. De naam van het bronbeelddossier. Dit kan een dossier zijn - noem of een vervangingspatroon. Het gebruiken van een patroon kan nuttig zijn als, bijvoorbeeld, de beelden voor het zelfde gebied op verschillende data worden geupload, zonder verandering in de bijbehorende meta-gegevens. Daarom zou een patroon als "<span class="filepath"> de Hoek van Tysons *.raw</span>"lagen van de <span class="filepath"> Hoek 050211.raw</span>van Tysons, <span class="filepath"> de Corner 050218.raw</span>van Tysons, etc. tot stand brengen aangezien de nieuwe beelden worden toegevoegd, zonder extra configuratie noodzakelijk als de parameters voor de dossiers anders identiek zijn. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> De Compressiekwaliteit van de Tegel </td> 
   <td colname="col2"> <p>Optioneel voor alle bronnen. Voor compressie JPEG, een geheel van 0 tot 100 specificerend hoe te om beeldgrootte en kwaliteit in evenwicht te brengen. (De standaardwaarde is nul.) Een hoger aantal resulteert in betere beeldkwaliteit, maar veroorzaakt grotere beelden en langere downloadtijden voor de gebruikers van de gegevenswerkbank. </p> <p>Het samenpersen van beelden onder 70 kan in beelddegradatie resulteren. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Tile compressor </td> 
   <td colname="col2"> Optioneel voor alle bronnen. Specificeert welke compressiemethode wordt gebruikt om outputdossiers te schrijven. De enige momenteel gesteunde methodes zijn RAWRGB (het gebrek, resulterend in geen compressie) en JPEG. De compressie van JPEG van het gebruik om de grootte van lagen te verminderen die tijdens profielsynchronisatie worden overgebracht. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Breedte </td> 
   <td colname="col2"> Vereist voor ruwe niet-geprojecteerde bitmap beelden. De breedte van het bronbeeld in pixel. </td> 
  </tr> 
 </tbody> 
</table>

1. Geef de Plaats van het BronBeeld, de Opslag van het Beeld van Temperaturen uit, en schrijf Lagen aan parameters gebruikend de volgende lijst als gids. Deze parameters zijn op alle bronnen van het terreinbeeld van toepassing die u in de Bronsectie van dit dossier bepaalt.

   | Parameter | Beschrijving |
   |---|---|
   | Locatie bronafbeelding | Vereist. De folder die voor beelden wordt afgetast om in terreinlagen te vertalen. Als het geen absolute weg is, wordt het geïnterpreteerd met betrekking tot de folder van de de serverinstallatie van de gegevenswerkbank. |
   | Temperatuurbeeldopslag | Optioneel. De naam van een folder die voor opslag van tijdelijke dossiers wordt gebruikt die in de vertaling van bronbeelden aan terreinlagen worden gebruikt. Als het geen absolute weg is, wordt het geïnterpreteerd met betrekking tot de folder van de de serverinstallatie van de gegevenswerkbank. De standaardplaats is de folder van Temperaturen. |
   | Lagen schrijven naar | Vereist. De folder waaraan de terreinlagen output zijn. Doorgaans, is dit subdirectory van Kaarten van een profielfolder, zodat de [!DNL Globe] visualisatie de lagen kan vinden. |

1. Sparen het dossier door **[!UICONTROL (modified)]** bij de bovenkant van het venster met de rechtermuisknop aan te klikken en te klikken **[!UICONTROL Save]**.

1. Als u een bijgewerkt bestand wilt opslaan op het systeem van de gegevenswerkbank, klikt u in het [!DNL Server Files Manager]veld met de rechtermuisknop op het vinkje voor [!DNL Terrain Images.cfg] in de [!DNL Temp] kolom en klikt u op **[!UICONTROL Save to]** > *&lt;**[!UICONTROL server name]**>*.

