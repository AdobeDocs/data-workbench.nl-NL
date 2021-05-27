---
description: In de werkbank data, toont een laag van het terrein beeldbeelden van de aarde.
title: Werken met Terrain Image Layers
uuid: 2f23a2c8-f551-4b84-bd87-5d7053910ab3
exl-id: 22026b41-4e12-4247-b019-461ae223bd07
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '1021'
ht-degree: 0%

---

# Werken met Terrain Image Layers{#working-with-terrain-image-layers}

In de werkbank data, toont een laag van het terrein beeldbeelden van de aarde.

Terreinafbeeldingslagen worden in een aangepaste indeling opgeslagen in het profiel [!DNL Geography]. Deze afbeeldingslagen kunnen worden gegenereerd door Adobe, anders kan een server met gegevenswerkbanken uw door de gebruiker geleverde terreinbeelden transformeren in terreinlagen die geschikt zijn voor gebruik op de wereldvisualisatie.

>[!NOTE]
>
>Als u wilt werken met grondafbeeldingslagen, moet u het [!DNL Terrain Images.cfg]-bestand van Adobe installeren. Zie [Data Workbench Geography](../../../../home/c-geo-oview/c-inst-geo/c-inst-geo.md) installeren voor installatie-instructies.

Als u een grondafbeeldingslaag wilt definiëren, moet u over het volgende beschikken:

* **Een of meer terreinafbeeldingsbestanden** met de afbeeldingen die op de wereldbol moeten worden weergegeven.
* **A Terrain Images.** cfgfile that specifies the Terrain image file(s) to be used for the layer(s). Met het [!DNL Terrain Images.cfg]-bestand kunt u een of meer bronnen toevoegen om een terreinafbeeldingslaag te maken. De indeling van het terreinafbeeldingsbestand bepaalt het type bron dat u wilt toevoegen. In de volgende tabel vindt u een beschrijving van de beschikbare bronnen voor grondafbeeldingslagen, inclusief de ondersteunde bestandsindelingen voor terreinafbeeldingen:

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
   <td colname="col2"> <p>Hiermee maakt u grondafbeeldingslagen van 24-bits, niet-geprojecteerde (niet-geprojecteerde), waarbij het noorden de bovenkant van de afbeelding is en het oosten de rechterkant. </p> <p>Ondersteunde afbeeldingsindeling(en): RAW </p> <p> <p>Opmerking: Voor deze bron is projectie-informatie vereist. Zie <a href="../../../../home/c-geo-oview/c-wk-img-lyrs/c-trn-img-lyrs/c-proj-info-trn-imgs/c-proj-info-trn-imgs.md#concept-69b0c668038f4de9bf430a3a468a2abd"> Projectie-informatie voor terreinafbeeldingen opgeven</a> voor informatie over projectie-indelingen. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Algemeen beeld, niet geprojecteerd </td> 
   <td colname="col2"> <p>Hiermee maakt u grondafbeeldingslagen van 24-bits, in lengtegraad uitgelijnde (niet-geprojecteerde) afbeeldingsindelingen, waarbij noord de bovenkant van de afbeelding is en oost de rechterzijde. </p> <p>Ondersteunde afbeeldingsindeling(en): BMP, JPG, PNG, TIFF </p> <p> <p>Opmerking: Voor deze bron is projectie-informatie vereist. Zie <a href="../../../../home/c-geo-oview/c-wk-img-lyrs/c-trn-img-lyrs/c-proj-info-trn-imgs/c-proj-info-trn-imgs.md#concept-69b0c668038f4de9bf430a3a468a2abd"> Projectie-informatie voor terreinafbeeldingen opgeven</a> voor informatie over projectie-indelingen. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Afbeelding met ingesloten projectie </td> 
   <td colname="col2"> <p>Hiermee maakt u grondafbeeldingslagen op basis van afbeeldingsindelingen die geodetische gegevens in het afbeeldingsbestand insluiten. De projectiegegevens worden uit de afbeelding geëxtraheerd. </p> <p>Ondersteunde afbeeldingsindeling(en): Erdas (IMG), GeoTIFF </p> <p> <p>Opmerking: Deze bron vereist gewoonlijk geen projectieinformatie maar steunt de toevoeging van dergelijke informatie indien nodig. Zie <a href="../../../../home/c-geo-oview/c-wk-img-lyrs/c-trn-img-lyrs/c-proj-info-trn-imgs/c-proj-info-trn-imgs.md#concept-69b0c668038f4de9bf430a3a468a2abd"> Projectie-informatie voor terreinafbeeldingen opgeven</a> voor informatie over projectie-indelingen. </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

**Een achtergrondafbeeldingslaag definiëren**

1. Klik op de **[!UICONTROL Servers Manager]**-miniatuur op de tab [!DNL Admin] > [!DNL Dataset and Profile] in de gegevenswerkbank om de [!DNL Servers Manager]-werkruimte te openen.

1. Klik in het venster [!DNL Servers Manager] met de rechtermuisknop op het pictogram van de gewenste gegevenswerkbankserver en klik op **[!UICONTROL Server Files]**.

1. Klik in [!DNL Server Files Manager] op **[!UICONTROL Components]** om de inhoud ervan weer te geven. Het [!DNL Terrain Images.cfg]-bestand bevindt zich in deze map.

1. Klik met de rechtermuisknop op het vinkje in de kolom Servernaam voor [!DNL Terrain Images.cfg] en klik vervolgens op **[!UICONTROL Make Local]**. Een vinkje verschijnt in [!DNL Temp] kolom voor [!DNL Terrain Images.cfg.]

1. Klik met de rechtermuisknop op het nieuwe vinkje in de kolom [!DNL Temp] en klik op **[!UICONTROL Open]** > **[!UICONTROL from the workbench]**. Het venster [!DNL Terrain Images.cfg]verschijnt.

1. Klik in het venster [!DNL Terrain Images] op **[!UICONTROL component]** om de inhoud ervan weer te geven.

1. Klik met de rechtermuisknop op **[!UICONTROL Sources]** > **[!UICONTROL Add new]** en kies een van de volgende brontypen:

   * **[!UICONTROL Raw unprojected bitmap]**. (Nadat dit brontype is toegevoegd, wordt het aangeduid met RawTerrainSource in het venster [!DNL Terrain Images].)

   * **[!UICONTROL General image, unprojected]**. (Nadat dit brontype is toegevoegd, wordt het gelabeld GDALTerrainSource in het venster [!DNL Terrain Images].)

   * **[!UICONTROL Image with embedded projection]**. (Nadat dit brontype is toegevoegd, wordt het gelabeld GDALTerrainSource in het venster [!DNL Terrain Images].)

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
   <td colname="col2"> <p>Vereist voor onbewerkte, niet-geprojecteerde bitmapafbeeldingen en algemene afbeeldingen, maar ondersteund voor afbeeldingen met ingesloten projectie. Gegevenswerkbank<span class="wintitle"> Geografie</span> ondersteunt breedtegraadprojecties en projecties van Transverse Mercator (TM) voor beeldlagen op het terrein. De standaardprojectie-indeling is de breedte-lengteprojectie (LatLonProjection). </p> <p>Zie <a href="../../../../home/c-geo-oview/c-wk-img-lyrs/c-trn-img-lyrs/c-proj-info-trn-imgs/c-proj-info-trn-imgs.md#concept-69b0c668038f4de9bf430a3a468a2abd"> Projectie-informatie voor terreinafbeeldingen opgeven</a> voor informatie over projectie-indelingen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Bronafbeelding </td> 
   <td colname="col2">Vereist voor alle bronnen. De naam van het bronafbeeldingsbestand. Dit kan een bestandsnaam of een jokertekenpatroon zijn. Het gebruik van een patroon kan nuttig zijn als afbeeldingen voor hetzelfde gebied op verschillende datums bijvoorbeeld worden geüpload zonder dat de bijbehorende metagegevens worden gewijzigd. Daarom zou een patroon als "<span class="filepath"> Tysons Corner *.raw</span>"lagen van <span class="filepath"> Tysons Corner 050211.raw</span>, <span class="filepath"> Tysons Corner 050218.raw</span> tot stand brengen, etc. als de nieuwe beelden, zonder extra configuratie noodzakelijk worden toegevoegd anders identiek zijn. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Tegelcompressiekwaliteit </td> 
   <td colname="col2"> <p>Optioneel voor alle bronnen. Voor JPEG-compressie geeft een geheel getal van 0 tot en met 100 op hoe de afbeeldingsgrootte en -kwaliteit in evenwicht moeten worden gebracht. (De standaardwaarde is nul.) Een hoger getal resulteert in een betere beeldkwaliteit, maar geeft grotere afbeeldingen en langere downloadtijden voor gebruikers van een werkbank. </p> <p>Het comprimeren van afbeeldingen onder 70 kan resulteren in een verslechtering van de afbeelding. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Tegelcompressie </td> 
   <td colname="col2"> Optioneel voor alle bronnen. Hiermee geeft u op welke compressiemethode wordt gebruikt voor het schrijven van uitvoerbestanden. De enige momenteel ondersteunde methoden zijn RAWRGB (de standaardinstelling, zonder compressie) en JPEG. Gebruik JPEG-compressie om de grootte te reduceren van lagen die tijdens profielsynchronisatie worden verzonden. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Breedte </td> 
   <td colname="col2"> Vereist voor onbewerkte, niet-geprojecteerde bitmapafbeeldingen. De breedte van de bronafbeelding in pixels. </td> 
  </tr> 
 </tbody> 
</table>

1. Bewerk de parameters Locatie bronafbeelding, Opslag tijdelijke afbeelding en Lagen schrijven naar aan de hand van de volgende tabel als richtlijn. Deze parameters zijn van toepassing op alle bronnen van het gebiedsbeeld die u in de Bronsectie van dit dossier bepaalt.

   | Parameter | Beschrijving |
   |---|---|
   | Locatie bronafbeelding | Vereist. De map die wordt gescand voor afbeeldingen die worden omgezet in grondlagen. Als het geen absoluut pad is, wordt het geïnterpreteerd ten opzichte van de installatiemap van de gegevenswerkbankserver. |
   | Temperatuur-afbeeldingsopslag | Optioneel. De naam van een map die wordt gebruikt voor de opslag van tijdelijke bestanden die worden gebruikt voor de omzetting van bronafbeeldingen in terreinlagen. Als het geen absoluut pad is, wordt het geïnterpreteerd ten opzichte van de installatiemap van de gegevenswerkbankserver. De standaardlocatie is de map Temperatuur. |
   | Lagen schrijven naar | Vereist. De map waarnaar grondlagen worden uitgevoerd. Doorgaans is dit de submap Kaarten van een profielmap, zodat de lagen kunnen worden gevonden met de visualisatie [!DNL Globe]. |

1. Sla het bestand op door met de rechtermuisknop op **[!UICONTROL (modified)]** boven in het venster te klikken en op **[!UICONTROL Save]** te klikken.

1. Als u het bijgewerkte bestand wilt opslaan op de gegevenswerkbankservercomputer, klikt u in [!DNL Server Files Manager] met de rechtermuisknop op het vinkje voor [!DNL Terrain Images.cfg] in de kolom [!DNL Temp] en vervolgens op **[!UICONTROL Save to]** > *&lt;**[!UICONTROL server name]**>*.
