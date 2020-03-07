---
description: Een laag van het terreinbeeld toont terreinbeelden van de aarde.
solution: Analytics
title: Afbeeldingslagen op het terrein
topic: Data workbench
uuid: 17968293-1ad2-4040-a174-d33f418af9b7
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Afbeeldingslagen op het terrein{#terrain-image-layers}

Een laag van het terreinbeeld toont terreinbeelden van de aarde.

[!DNL Terrain image layers] worden opgeslagen in het [!DNL Geography] profiel in een douaneformaat. Deze beeldlagen kunnen door Adobe worden geproduceerd, of de server van de Werkbank van Gegevens kan uw gebruiker-geleverde terreinbeelden in terreinlagen omzetten geschikt voor gebruik op de globale visualisatie.

>[!NOTE]
>
>Om met te werken, moet u het [!DNL terrain image layers][!DNL Terrain Images.cfg] dossier installeren dat door Adobe wordt verstrekt.

Om een laag van het terreinbeeld te bepalen, moet u het volgende hebben:

* **Één of meerdere dossiers** van het terreinbeeld die de beelden bevatten die op de aardbol moeten worden getoond.
* **Een[!DNL Terrain Images.cfg]bestand** waarin de bestanden met terreinafbeelding worden opgegeven die voor de laag(en) moeten worden gebruikt. Het [!DNL Terrain Images.cfg] dossier laat u toe om één of meerdere bronnen toe te voegen om tot een [!DNL terrain image layer]te leiden. Het formaat van uw dossier van het terreinbeeld bepaalt het type van bron dat u zou moeten toevoegen. De volgende lijst verstrekt beschrijvingen van de beschikbare bronnen van de de laaglaag van het terreinbeeld, met inbegrip van de gesteunde dossierformaten van het terreinbeeld:

<table id="table_CFDF5E61FCCD40B29A9D35FFA42F68D1"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Type </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Ruwe niet-geprojecteerde bitmap </p> </td> 
   <td colname="col2"> <p>Creeert de lagen <span class="wintitle"> van het</span> terreinbeeld van 24 - beetje kopballoze RGB dossiers die breedtegraad-lengtegraad gericht (niet geprojecteerd) zijn, waar het noorden de bovenkant van het beeld is, en het oosten is het recht. </p> <p>Ondersteunde afbeeldingsindeling(en): RAUW </p> <p> <p>Opmerking: Deze bron vereist projectieinformatie. Voor informatie over projectieformaten, zie het <a href="../../../../home/c-get-started/c-im-layers/c-ter-img-layers/c-proj-info-ter-imgs.md#concept-eec35baa01744895b847a02e69dad04e"> Specificeren van de Informatie van de Projectie voor de Beelden</a>van het Terrein. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Algemeen beeld, niet geprojecteerd </p> </td> 
   <td colname="col2"> <p>Creeert de lagen <span class="wintitle"> van het</span> terreinbeeld van 24 - beetje, breedtegraad-gerichte (niet geprojecteerde) beeldformaten, waar het noorden de bovenkant van het beeld is, en het oosten is het recht. </p> <p>Ondersteunde afbeeldingsindeling(en): BMP, JPG, PNG, TIFF </p> <p> <p>Opmerking: Deze bron vereist projectieinformatie. Voor informatie over projectieformaten, zie het <a href="../../../../home/c-get-started/c-im-layers/c-ter-img-layers/c-proj-info-ter-imgs.md#concept-eec35baa01744895b847a02e69dad04e"> Specificeren van de Informatie van de Projectie voor de Beelden</a>van het Terrein. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Afbeelding met ingebouwde projectie </p> </td> 
   <td colname="col2"> <p>Creeert de lagen <span class="wintitle"> van het</span> terreinbeeld van beeldformaten die geodetische gegevens in het beelddossier inbedden. De projectieinformatie wordt uit het beeld gehaald. </p> <p>Ondersteunde afbeeldingsindeling(en): Erdas (IMG), GeoTIFF </p> <p> <p>Opmerking: Deze bron vereist gewoonlijk geen projectieinformatie maar steunt de toevoeging van dergelijke informatie indien nodig. Voor informatie over projectieformaten, zie het <a href="../../../../home/c-get-started/c-im-layers/c-ter-img-layers/c-proj-info-ter-imgs.md#concept-eec35baa01744895b847a02e69dad04e"> Specificeren van de Informatie van de Projectie voor de Beelden</a>van het Terrein. </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

**Om een laag van het terreinbeeld te bepalen**

1. In de Werkbank van Gegevens, op het **[!UICONTROL Admin]** > **[!UICONTROL Dataset and Profile]** lusje, klik de **[!UICONTROL Servers Manager]** duimnagel om de [!DNL Servers Manager] werkruimte te openen.
1. Klik in het [!DNL Servers Manager] venster met de rechtermuisknop op het pictogram van de gewenste server voor een gegevenswerkbank en klik op **[!UICONTROL Server Files]**.
1. In [!DNL Server Files Manager], klik **[!UICONTROL Components]** om zijn inhoud te bekijken. Het [!DNL Terrain Images.cfg] dossier wordt gevestigd binnen deze folder.
1. Klik het vinkje in de kolom van de servernaam voor met de rechtermuisknop aan [!DNL Terrain Images.cfg], dan klik **[!UICONTROL Make Local]**. Een vinkje verschijnt in de [!DNL Temp] kolom voor [!DNL Terrain Images.cfg].
1. Klik het pas gecreëerde vinkje in de **[!UICONTROL Temp]** kolom met de rechtermuisknop aan en klik **[!UICONTROL Open]** > **[!UICONTROL from the workbench]**. Het [!DNL Terrain Images.cfg] venster wordt weergegeven.
1. In het [!DNL Terrain Images] venster, klik **[!UICONTROL component]** om zijn inhoud te bekijken.
1. Klik met de rechtermuisknop **[!UICONTROL Sources]** > **[!UICONTROL Add new]** en kies een van de volgende brontypen:

   * **[!UICONTROL Raw unprojected bitmap]**. (Zodra toegevoegd, wordt dit brontype geëtiketteerd RawTerrainSource in het [!DNL Terrain Images] venster.)

   * **[!UICONTROL General image, unprojected]**. (Zodra toegevoegd, wordt dit brontype geëtiketteerd [!DNL GDALTerrainSource] in het [!DNL Terrain Images] venster.)

   * **[!UICONTROL Image with embedded projection]**. (Zodra toegevoegd, wordt dit brontype geëtiketteerd [!DNL GDALTerrainSource] in het [!DNL Terrain Images] venster.)

1. Geef zonodig de parameters voor de bron uit gebruikend het volgende steekproefdossier en de lijst van parameters als gidsen.

   ![](assets/cfg_TerrainImages_ALL.png)

<table id="table_345ACB4C48524516AADB731D87FC6792"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Parameter </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Gamma </p> </td> 
   <td colname="col2"> <p>Optioneel voor alle bronnen. Specificeert gammacorrectie die op het bronbeeld moet worden toegepast. Dit kan wenselijk zijn omdat de Werkbank van Gegevens normaal met het hoge gamma plaatsen loopt. De standaardwaarde is 1. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Hoogte </p> </td> 
   <td colname="col2"> <p>Vereist voor ruwe niet-geprojecteerde bitmap beelden. De hoogte van het bronbeeld in pixel. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Projectiegegevens </p> </td> 
   <td colname="col2"> <p>Vereist voor ruwe niet-geprojecteerde bitmap beelden en algemene beelden, niet geprojecteerd, maar gesteund voor beelden met ingebedde projectie. De Werkbank van gegevens steunt breedtegraad-lengteprojecties en de projecties van de Transverse Mercator (TM) voor de lagen van het terreinbeeld. Het standaardprojectieformaat is de breedtegraad-projectie (LatLonProjection). </p> <p>Voor informatie over projectieformaten, zie het <a href="../../../../home/c-get-started/c-im-layers/c-ter-img-layers/c-proj-info-ter-imgs.md#concept-eec35baa01744895b847a02e69dad04e"> Specificeren van de Informatie van de Projectie voor de Beelden</a>van het Terrein. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Bronafbeelding </p> </td> 
   <td colname="col2"> <p>Vereist voor alle bronnen. De naam van het bronbeelddossier. Dit kan een dossier zijn - noem of een vervangingspatroon. Het gebruiken van een patroon kan nuttig zijn als, bijvoorbeeld, de beelden voor het zelfde gebied op verschillende data worden geupload, zonder verandering in de bijbehorende meta-gegevens. Daarom zou een patroon zoals de Hoek van <span class="filepath"> Tysons *.raw</span> lagen van de <span class="filepath"> Hoek 050211.raw</span>van Tysons, <span class="filepath"> Tysons Corner 050218.raw</span>, etc. tot stand brengen aangezien de nieuwe beelden worden toegevoegd, zonder extra configuratie noodzakelijk als de parameters voor de dossiers anders identiek zijn. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>De Compressiekwaliteit van de Tegel </p> </td> 
   <td colname="col2"> <p>Optioneel voor alle bronnen. Voor compressie JPEG, een geheel van 0 tot 100 specificerend hoe te om beeldgrootte en kwaliteit in evenwicht te brengen. (De standaardwaarde is nul.) Een hoger aantal resulteert in betere beeldkwaliteit, maar veroorzaakt grotere beelden en langere downloadtijden voor de gebruikers van de Werkbank van Gegevens. </p> <p> <p>Opmerking:  Het samenpersen van beelden onder 70 kan in beelddegradatie resulteren. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Tile compressor </p> </td> 
   <td colname="col2"> <p>Optioneel voor alle bronnen. Specificeert welke compressiemethode wordt gebruikt om outputdossiers te schrijven. De enige momenteel gesteunde methodes zijn RAWRGB (het gebrek, resulterend in geen compressie) en JPEG. De compressie van JPEG van het gebruik om de grootte van lagen te verminderen die tijdens profielsynchronisatie worden overgebracht. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Breedte </p> </td> 
   <td colname="col2"> <p>Vereist voor ruwe niet-geprojecteerde bitmap beelden. De breedte van het bronbeeld in pixel. </p> </td> 
  </tr> 
 </tbody> 
</table>

1. Geef de Plaats van het BronBeeld, de Opslag van het Beeld van Temperaturen uit, en schrijf Lagen aan parameters gebruikend de volgende lijst als gids. Deze parameters zijn op alle bronnen van het terreinbeeld van toepassing die u in de [!DNL Sources] sectie van dit dossier bepaalt.

<table id="table_103F02C54ED94C6C922450F5B2781CAE"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Parameter </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Locatie bronafbeelding </p> </td> 
   <td colname="col2"> <p>Vereist. De folder die voor beelden wordt afgetast om in terreinlagen te vertalen. Als het geen absolute weg is, wordt het geïnterpreteerd met betrekking tot de de serverinstallatiefolder van de Werkbank van Gegevens. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Temperatuurbeeldopslag </p> </td> 
   <td colname="col2"> <p>Optioneel. De naam van een folder die voor opslag van tijdelijke dossiers wordt gebruikt die in de vertaling van bronbeelden aan terreinlagen worden gebruikt. Als het geen absolute weg is, wordt het geïnterpreteerd met betrekking tot de de serverinstallatiefolder van de Werkbank van Gegevens. De standaardplaats is de folder van <span class="wintitle"> Temperaturen</span> . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Lagen schrijven naar </p> </td> 
   <td colname="col2"> <p>Vereist. De folder waaraan de terreinlagen output is. Doorgaans, is dit subdirectory van Kaarten van een profielfolder, zodat de visualisatie van de Globe de lagen kan vinden. </p> </td> 
  </tr> 
 </tbody> 
</table>

1. Sparen het dossier door **[!UICONTROL (modified)]** bij de bovenkant van het venster met de rechtermuisknop aan te klikken en te klikken **[!UICONTROL Save]**.
1. Als u een bijgewerkt bestand wilt opslaan op de computer met de Data Workbench-server, klikt u in de [!DNL Server Files Manager]kolom met de rechtermuisknop op het vinkje voor [!DNL Terrain Images.cfg] in de [!DNL Temp] kolom en klikt u op **[!UICONTROL Save to]** > *&lt;**[!UICONTROL server name]**>*.

