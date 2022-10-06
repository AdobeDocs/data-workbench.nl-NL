---
description: In de werkbank data, toont een laag van het terrein beeldbeelden van de aarde.
title: Werken met Terrain Image Layers
uuid: 2f23a2c8-f551-4b84-bd87-5d7053910ab3
exl-id: 22026b41-4e12-4247-b019-461ae223bd07
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '1021'
ht-degree: 0%

---

# Werken met Terrain Image Layers{#working-with-terrain-image-layers}

{{eol}}

In de werkbank data, toont een laag van het terrein beeldbeelden van de aarde.

Terreinafbeeldingslagen worden opgeslagen in de [!DNL Geography] in een aangepaste indeling. Deze afbeeldingslagen kunnen worden gegenereerd door Adobe, anders kan een server met gegevenswerkbanken uw door de gebruiker geleverde terreinbeelden transformeren in terreinlagen die geschikt zijn voor gebruik op de wereldvisualisatie.

>[!NOTE]
>
>Als u wilt werken met achtergrondafbeeldingslagen, moet u de [!DNL Terrain Images.cfg] bestand opgegeven door Adobe. Voor installatie-instructies raadpleegt u [Data Workbench Geography installeren](../../../../home/c-geo-oview/c-inst-geo/c-inst-geo.md).

Als u een grondafbeeldingslaag wilt definiëren, moet u over het volgende beschikken:

* **Een of meer terreinafbeeldingsbestanden** met de afbeeldingen die op de wereldbol moeten worden weergegeven.
* **A Terrain Images.cfg** bestand dat aangeeft welk(e) terreinafbeeldingsbestand(en) voor de laag of lagen moet worden gebruikt. De [!DNL Terrain Images.cfg] kunt u een of meer bronnen toevoegen om een terreinafbeeldingslaag te maken. De indeling van het terreinafbeeldingsbestand bepaalt het type bron dat u wilt toevoegen. In de volgende tabel vindt u een beschrijving van de beschikbare bronnen voor grondafbeeldingslagen, inclusief de ondersteunde bestandsindelingen voor terreinafbeeldingen:

<table id="table_BF8D5933BFBE45039BD164C258D3B450"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Type </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Ongeprojecteerde bitmap, ruw </td> 
   <td colname="col2"> <p>Hiermee maakt u terreinafbeeldingslagen van 24-bits bestanden zonder RGB-koptekst die zijn uitgelijnd (niet-geprojecteerd) met de breedtegraad, waarbij noord de bovenkant van de afbeelding is en oost de rechterkant. </p> <p>Ondersteunde afbeeldingsindeling(en): RAW </p> <p> <p>Opmerking: Voor deze bron is projectie-informatie vereist. Voor informatie over projectie-indelingen raadpleegt u <a href="../../../../home/c-geo-oview/c-wk-img-lyrs/c-trn-img-lyrs/c-proj-info-trn-imgs/c-proj-info-trn-imgs.md#concept-69b0c668038f4de9bf430a3a468a2abd"> Projectie-informatie opgeven voor terreinafbeeldingen</a>. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Algemeen beeld, niet geprojecteerd </td> 
   <td colname="col2"> <p>Hiermee maakt u grondafbeeldingslagen van 24-bits, in lengtegraad uitgelijnde (niet-geprojecteerde) afbeeldingsindelingen, waarbij noord de bovenkant van de afbeelding is en oost de rechterzijde. </p> <p>Ondersteunde afbeeldingsindeling(en): BMP, JPG, PNG, TIFF </p> <p> <p>Opmerking: Voor deze bron is projectie-informatie vereist. Voor informatie over projectie-indelingen raadpleegt u <a href="../../../../home/c-geo-oview/c-wk-img-lyrs/c-trn-img-lyrs/c-proj-info-trn-imgs/c-proj-info-trn-imgs.md#concept-69b0c668038f4de9bf430a3a468a2abd"> Projectie-informatie opgeven voor terreinafbeeldingen</a>. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Afbeelding met ingesloten projectie </td> 
   <td colname="col2"> <p>Hiermee maakt u grondafbeeldingslagen op basis van afbeeldingsindelingen die geodetische gegevens in het afbeeldingsbestand insluiten. De projectiegegevens worden uit de afbeelding geëxtraheerd. </p> <p>Ondersteunde afbeeldingsindeling(en): Erdas (IMG), GeoTIFF </p> <p> <p>Opmerking: Deze bron vereist gewoonlijk geen projectieinformatie maar steunt de toevoeging van dergelijke informatie indien nodig. Voor informatie over projectie-indelingen raadpleegt u <a href="../../../../home/c-geo-oview/c-wk-img-lyrs/c-trn-img-lyrs/c-proj-info-trn-imgs/c-proj-info-trn-imgs.md#concept-69b0c668038f4de9bf430a3a468a2abd"> Projectie-informatie opgeven voor terreinafbeeldingen</a>. </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

**Een achtergrondafbeeldingslaag definiëren**

1. Op de werkbank Gegevens, op de [!DNL Admin] > [!DNL Dataset and Profile] klikt u op de knop **[!UICONTROL Servers Manager]** miniatuur om de [!DNL Servers Manager] werkruimte.

1. Binnen de [!DNL Servers Manager] venster, klikt u met de rechtermuisknop op het pictogram van de gewenste gegevenswerkbankserver en klikt u op **[!UICONTROL Server Files]**.

1. In de [!DNL Server Files Manager], klikt u op **[!UICONTROL Components]** om de inhoud te bekijken. De [!DNL Terrain Images.cfg] bestand bevindt zich in deze map.

1. Klik met de rechtermuisknop op het vinkje in de kolom Servernaam voor [!DNL Terrain Images.cfg]en klik vervolgens op **[!UICONTROL Make Local]**. Er verschijnt een vinkje in het dialoogvenster [!DNL Temp] kolom voor [!DNL Terrain Images.cfg.]

1. Klik met de rechtermuisknop op het nieuwe vinkje in het dialoogvenster [!DNL Temp] kolom en klik op **[!UICONTROL Open]** > **[!UICONTROL from the workbench]**. De [!DNL Terrain Images.cfg]wordt weergegeven.

1. In de [!DNL Terrain Images] venster, klikt u op **[!UICONTROL component]** om de inhoud te bekijken.

1. Klikken met rechtermuisknop **[!UICONTROL Sources]** > **[!UICONTROL Add new]** en kies een van de volgende brontypen:

   * **[!UICONTROL Raw unprojected bitmap]**. (Nadat dit brontype is toegevoegd, wordt het label RawTerrainSource in het dialoogvenster [!DNL Terrain Images] venster.)

   * **[!UICONTROL General image, unprojected]**. (Nadat dit brontype is toegevoegd, wordt het gelabeld GDALTerrainSource in het dialoogvenster [!DNL Terrain Images] venster.)

   * **[!UICONTROL Image with embedded projection]**. (Nadat dit brontype is toegevoegd, wordt het gelabeld GDALTerrainSource in het dialoogvenster [!DNL Terrain Images] venster.)

1. Bewerk indien nodig de parameters voor de bron met behulp van het volgende voorbeeldbestand en de tabel met parameters als hulplijnen.

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
   <td colname="col2"> Optioneel voor alle bronnen. Hiermee wordt gammacorrectie opgegeven die op de bronafbeelding moet worden toegepast. Dit kan wenselijk zijn omdat de werkbank van gegevens normaal met een hoge gamma het plaatsen loopt. De standaardwaarde is 1. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Hoogte </td> 
   <td colname="col2"> Vereist voor onbewerkte, niet-geprojecteerde bitmapafbeeldingen. De hoogte van de bronafbeelding in pixels. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Projectie-info </td> 
   <td colname="col2"> <p>Vereist voor onbewerkte, niet-geprojecteerde bitmapafbeeldingen en algemene afbeeldingen, maar ondersteund voor afbeeldingen met ingesloten projectie. Gegevenswerkbank<span class="wintitle"> Geografie</span> ondersteunt breedtegraad-lengteprojecties en Transverse Mercator (TM)-projecties voor terreinafbeeldingslagen. De standaardprojectie-indeling is de breedte-lengteprojectie (LatLonProjection). </p> <p>Voor informatie over projectie-indelingen raadpleegt u <a href="../../../../home/c-geo-oview/c-wk-img-lyrs/c-trn-img-lyrs/c-proj-info-trn-imgs/c-proj-info-trn-imgs.md#concept-69b0c668038f4de9bf430a3a468a2abd"> Projectie-informatie opgeven voor terreinafbeeldingen</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Bronafbeelding </td> 
   <td colname="col2">Vereist voor alle bronnen. De naam van het bronafbeeldingsbestand. Dit kan een bestandsnaam of een jokertekenpatroon zijn. Het gebruik van een patroon kan nuttig zijn als afbeeldingen voor hetzelfde gebied op verschillende datums bijvoorbeeld worden geüpload zonder dat de bijbehorende metagegevens worden gewijzigd. Daarom is een patroon als "<span class="filepath"> Tysons Corner *.raw</span>" zou lagen maken van <span class="filepath"> Tysons Corner 050211.raw</span>, <span class="filepath"> Tysons Corner 050218.raw</span>, enzovoort, als er nieuwe afbeeldingen worden toegevoegd, zonder extra configuratie als de parameters voor de bestanden anders identiek zijn. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Tegelcompressiekwaliteit </td> 
   <td colname="col2"> <p>Optioneel voor alle bronnen. Voor JPEG-compressie geeft een geheel getal van 0 tot en met 100 op hoe de afbeeldingsgrootte en -kwaliteit in evenwicht moeten worden gebracht. (De standaardwaarde is nul.) Een hoger getal resulteert in een betere beeldkwaliteit, maar geeft grotere afbeeldingen en langere downloadtijden voor gebruikers van een werkbank. </p> <p>Het comprimeren van afbeeldingen onder 70 kan resulteren in een verslechtering van de afbeelding. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Tegelcompressie </td> 
   <td colname="col2"> Optioneel voor alle bronnen. Hiermee geeft u op welke compressiemethode wordt gebruikt voor het schrijven van uitvoerbestanden. De enige momenteel ondersteunde methoden zijn RAWRGB (de standaardinstelling, zonder compressie) en JPEG. Gebruik JPEG-compressie om de grootte te beperken van lagen die tijdens profielsynchronisatie worden verzonden. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Breedte </td> 
   <td colname="col2"> Vereist voor onbewerkte, niet-geprojecteerde bitmapafbeeldingen. De breedte van de bronafbeelding in pixels. </td> 
  </tr> 
 </tbody> 
</table>

1. Bewerk de parameters Locatie bronafbeelding, Tijdelijke afbeeldingsopslag en Lagen schrijven naar aan de hand van de volgende tabel als richtlijn. Deze parameters zijn van toepassing op alle bronnen van het gebiedsbeeld die u in de Bronsectie van dit dossier bepaalt.

   | Parameter | Beschrijving |
   |---|---|
   | Locatie bronafbeelding | Vereist. De map die wordt gescand voor afbeeldingen die worden omgezet in grondlagen. Als het geen absoluut pad is, wordt het geïnterpreteerd ten opzichte van de installatiemap van de gegevenswerkbankserver. |
   | Temperatuur-afbeeldingsopslag | Optioneel. De naam van een map die wordt gebruikt voor de opslag van tijdelijke bestanden die worden gebruikt voor de omzetting van bronafbeeldingen in terreinlagen. Als het geen absoluut pad is, wordt het geïnterpreteerd ten opzichte van de installatiemap van de gegevenswerkbankserver. De standaardlocatie is de map Temperatuur. |
   | Lagen schrijven naar | Vereist. De map waarnaar grondlagen worden uitgevoerd. Doorgaans is dit de submap Maps van een profielmap, zodat de map [!DNL Globe] met visualisatie kunt u de lagen vinden. |

1. Sla het bestand op door met de rechtermuisknop te klikken **[!UICONTROL (modified)]** boven aan het venster en klikken op **[!UICONTROL Save]**.

1. Als u het bijgewerkte bestand wilt opslaan op de computer van de gegevenswerkbank, gaat u naar het [!DNL Server Files Manager], klikt u met de rechtermuisknop op het vinkje voor [!DNL Terrain Images.cfg] in de [!DNL Temp] kolom, klik vervolgens op **[!UICONTROL Save to]** > *&lt;**[!UICONTROL server name]**>*.
