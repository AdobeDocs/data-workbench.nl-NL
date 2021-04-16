---
description: Een grondbeeldlaag toont terreinbeelden van de aarde.
title: Terreaire afbeeldingslagen
uuid: 17968293-1ad2-4040-a174-d33f418af9b7
exl-id: 754211a7-0b1f-4353-86f8-9c634d70cd83
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '992'
ht-degree: 0%

---

# Terreaire afbeeldingslagen{#terrain-image-layers}

Een grondbeeldlaag toont terreinbeelden van de aarde.

[!DNL Terrain image layers] worden opgeslagen in het  [!DNL Geography] profiel in een aangepaste indeling. Deze afbeeldingslagen kunnen worden gegenereerd door Adobe of de server van de Data Workbench kan door de gebruiker geleverde terreinbeelden transformeren in terreinlagen die geschikt zijn voor gebruik op de wereldvisualisatie.

>[!NOTE]
>
>Als u met [!DNL terrain image layers] wilt werken, moet u het [!DNL Terrain Images.cfg]-bestand van Adobe installeren.

Als u een grondafbeeldingslaag wilt definiëren, moet u over het volgende beschikken:

* **Een of meer terreinafbeeldingsbestanden** met de afbeeldingen die op de wereldbol moeten worden weergegeven.
* **Een  [!DNL Terrain Images.cfg]** bestand dat aangeeft welk(e) terreinafbeeldingsbestand(en) moet worden gebruikt voor de laag of lagen. Met het bestand [!DNL Terrain Images.cfg] kunt u een of meer bronnen toevoegen om een [!DNL terrain image layer] te maken. De indeling van het terreinafbeeldingsbestand bepaalt het type bron dat u wilt toevoegen. In de volgende tabel vindt u een beschrijving van de beschikbare bronnen voor grondafbeeldingslagen, inclusief de ondersteunde bestandsindelingen voor terreinafbeeldingen:

<table id="table_CFDF5E61FCCD40B29A9D35FFA42F68D1"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Type </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Ongeprojecteerde bitmap, ruw </p> </td> 
   <td colname="col2"> <p>Hiermee maakt u <span class="wintitle"> terrain image layers</span> van 24-bits headerless RGB-bestanden die zijn uitgelijnd met de lengte-breedtegraad (niet geprojecteerd), waarbij noord de bovenkant van de afbeelding is en oost de rechterkant. </p> <p>Ondersteunde afbeeldingsindeling(en): RAW </p> <p> <p>Opmerking: Voor deze bron is projectie-informatie vereist. Zie <a href="../../../../home/c-get-started/c-im-layers/c-ter-img-layers/c-proj-info-ter-imgs.md#concept-eec35baa01744895b847a02e69dad04e"> Projectie-informatie voor terreinafbeeldingen opgeven</a> voor informatie over projectie-indelingen. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Algemeen beeld, niet geprojecteerd </p> </td> 
   <td colname="col2"> <p>Hiermee maakt u <span class="wintitle"> terreinafbeeldingslagen</span> van 24-bits afbeeldingsindelingen die zijn uitgelijnd met de breedtegraad (niet-geprojecteerd), waarbij noord de bovenkant van de afbeelding is en oost de rechterzijde. </p> <p>Ondersteunde afbeeldingsindeling(en): BMP, JPG, PNG, TIFF </p> <p> <p>Opmerking: Voor deze bron is projectie-informatie vereist. Zie <a href="../../../../home/c-get-started/c-im-layers/c-ter-img-layers/c-proj-info-ter-imgs.md#concept-eec35baa01744895b847a02e69dad04e"> Projectie-informatie voor terreinafbeeldingen opgeven</a> voor informatie over projectie-indelingen. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Afbeelding met ingesloten projectie </p> </td> 
   <td colname="col2"> <p>Hiermee maakt u <span class="wintitle"> terreinafbeeldingslagen</span> op basis van afbeeldingsindelingen die geodetische gegevens in het afbeeldingsbestand insluiten. De projectiegegevens worden uit de afbeelding geëxtraheerd. </p> <p>Ondersteunde afbeeldingsindeling(en): Erdas (IMG), GeoTIFF </p> <p> <p>Opmerking: Deze bron vereist gewoonlijk geen projectieinformatie maar steunt de toevoeging van dergelijke informatie indien nodig. Zie <a href="../../../../home/c-get-started/c-im-layers/c-ter-img-layers/c-proj-info-ter-imgs.md#concept-eec35baa01744895b847a02e69dad04e"> Projectie-informatie voor terreinafbeeldingen opgeven</a> voor informatie over projectie-indelingen. </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

**Een achtergrondafbeeldingslaag definiëren**

1. Klik in Data Workbench op het tabblad **[!UICONTROL Admin]** > **[!UICONTROL Dataset and Profile]** op de miniatuur **[!UICONTROL Servers Manager]** om de werkruimte [!DNL Servers Manager] te openen.
1. Klik in het venster [!DNL Servers Manager] met de rechtermuisknop op het pictogram van de gewenste Data Workbench-server en klik op **[!UICONTROL Server Files]**.
1. Klik in [!DNL Server Files Manager] op **[!UICONTROL Components]** om de inhoud ervan weer te geven. Het [!DNL Terrain Images.cfg]-bestand bevindt zich in deze map.
1. Klik met de rechtermuisknop op het vinkje in de kolom Servernaam voor [!DNL Terrain Images.cfg] en klik vervolgens op **[!UICONTROL Make Local]**. In de kolom [!DNL Temp] wordt een vinkje weergegeven voor [!DNL Terrain Images.cfg].
1. Klik met de rechtermuisknop op het nieuwe vinkje in de kolom **[!UICONTROL Temp]** en klik op **[!UICONTROL Open]** > **[!UICONTROL from the workbench]**. Het venster [!DNL Terrain Images.cfg] verschijnt.
1. Klik in het venster [!DNL Terrain Images] op **[!UICONTROL component]** om de inhoud ervan weer te geven.
1. Klik met de rechtermuisknop op **[!UICONTROL Sources]** > **[!UICONTROL Add new]** en kies een van de volgende brontypen:

   * **[!UICONTROL Raw unprojected bitmap]**. (Nadat dit brontype is toegevoegd, wordt het aangeduid met RawTerrainSource in het venster [!DNL Terrain Images].)

   * **[!UICONTROL General image, unprojected]**. (Na toevoeging van dit brontype wordt [!DNL GDALTerrainSource] geëtiketteerd in [!DNL Terrain Images] venster.)

   * **[!UICONTROL Image with embedded projection]**. (Na toevoeging van dit brontype wordt [!DNL GDALTerrainSource] geëtiketteerd in [!DNL Terrain Images] venster.)

1. Bewerk indien nodig de parameters voor de bron met behulp van het volgende voorbeeldbestand en de tabel met parameters als hulplijnen.

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
   <td colname="col2"> <p>Optioneel voor alle bronnen. Hiermee wordt gammacorrectie opgegeven die op de bronafbeelding moet worden toegepast. Dit kan wenselijk zijn vanwege het feit dat Data Workbench gewoonlijk met een hoge gammainstelling wordt uitgevoerd. De standaardwaarde is 1. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Hoogte </p> </td> 
   <td colname="col2"> <p>Vereist voor onbewerkte, niet-geprojecteerde bitmapafbeeldingen. De hoogte van de bronafbeelding in pixels. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Projectie-info </p> </td> 
   <td colname="col2"> <p>Vereist voor onbewerkte, niet-geprojecteerde bitmapafbeeldingen en algemene afbeeldingen, maar ondersteund voor afbeeldingen met ingesloten projectie. Data Workbench ondersteunt breedtegraad-lengteprojecties en Transverse Mercator (TM)-projecties voor grondafbeeldingslagen. De standaardprojectie-indeling is de breedte-lengteprojectie (LatLonProjection). </p> <p>Zie <a href="../../../../home/c-get-started/c-im-layers/c-ter-img-layers/c-proj-info-ter-imgs.md#concept-eec35baa01744895b847a02e69dad04e"> Projectie-informatie voor terreinafbeeldingen opgeven</a> voor informatie over projectie-indelingen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Bronafbeelding </p> </td> 
   <td colname="col2"> <p>Vereist voor alle bronnen. De naam van het bronafbeeldingsbestand. Dit kan een bestandsnaam of een jokertekenpatroon zijn. Het gebruik van een patroon kan nuttig zijn als afbeeldingen voor hetzelfde gebied op verschillende datums bijvoorbeeld worden geüpload zonder dat de bijbehorende metagegevens worden gewijzigd. Een patroon als <span class="filepath"> Tysons Corner *.raw</span> zou daarom lagen maken van <span class="filepath"> Tysons Corner 050211.raw</span>, <span class="filepath"> Tysons Corner 050218.raw</span>, enzovoort, wanneer nieuwe afbeeldingen worden toegevoegd, zonder extra configuratie nodig als de parameters voor de parameters de bestanden zijn verder identiek. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Tegelcompressiekwaliteit </p> </td> 
   <td colname="col2"> <p>Optioneel voor alle bronnen. Voor JPEG-compressie geeft een geheel getal van 0 tot en met 100 op hoe de afbeeldingsgrootte en -kwaliteit in evenwicht moeten worden gebracht. (De standaardwaarde is nul.) Een hogere waarde resulteert in een betere beeldkwaliteit, maar geeft grotere afbeeldingen en langere downloadtijden voor Data Workbench. </p> <p> <p>Opmerking:  Het comprimeren van afbeeldingen onder 70 kan resulteren in een verslechtering van de afbeelding. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Tegelcompressie </p> </td> 
   <td colname="col2"> <p>Optioneel voor alle bronnen. Hiermee geeft u op welke compressiemethode wordt gebruikt voor het schrijven van uitvoerbestanden. De enige momenteel ondersteunde methoden zijn RAWRGB (de standaardinstelling, zonder compressie) en JPEG. Gebruik JPEG-compressie om de grootte te reduceren van lagen die tijdens profielsynchronisatie worden verzonden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Breedte </p> </td> 
   <td colname="col2"> <p>Vereist voor onbewerkte, niet-geprojecteerde bitmapafbeeldingen. De breedte van de bronafbeelding in pixels. </p> </td> 
  </tr> 
 </tbody> 
</table>

1. Bewerk de parameters Locatie bronafbeelding, Opslag tijdelijke afbeelding en Lagen schrijven naar aan de hand van de volgende tabel als richtlijn. Deze parameters zijn van toepassing op alle grondafbeeldingsbronnen die u in de sectie [!DNL Sources] van dit bestand definieert.

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
   <td colname="col2"> <p>Vereist. De map die wordt gescand voor afbeeldingen die worden omgezet in grondlagen. Als het geen absoluut pad is, wordt het geïnterpreteerd ten opzichte van de installatiemap van de Data Workbench-server. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Temperatuur-afbeeldingsopslag </p> </td> 
   <td colname="col2"> <p>Optioneel. De naam van een map die wordt gebruikt voor de opslag van tijdelijke bestanden die worden gebruikt voor de omzetting van bronafbeeldingen in terreinlagen. Als het geen absoluut pad is, wordt het geïnterpreteerd ten opzichte van de installatiemap van de Data Workbench-server. De standaardlocatie is de map <span class="wintitle"> Temp</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Lagen schrijven naar </p> </td> 
   <td colname="col2"> <p>Vereist. De map waarnaar grondlagen worden uitgevoerd. Doorgaans is dit de submap Maps van een profielmap, zodat de wereldvisualisatie de lagen kan vinden. </p> </td> 
  </tr> 
 </tbody> 
</table>

1. Sla het bestand op door met de rechtermuisknop op **[!UICONTROL (modified)]** boven in het venster te klikken en op **[!UICONTROL Save]** te klikken.
1. Als u een bijgewerkt bestand wilt opslaan op de Data Workbench-servercomputer, klikt u in [!DNL Server Files Manager] met de rechtermuisknop op het vinkje voor [!DNL Terrain Images.cfg] in de kolom [!DNL Temp] en klikt u vervolgens op **[!UICONTROL Save to]** > *&lt;**[!UICONTROL server name]**>*.
