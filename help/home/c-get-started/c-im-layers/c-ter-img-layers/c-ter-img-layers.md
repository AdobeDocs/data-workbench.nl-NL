---
description: Een grondbeeldlaag toont terreinbeelden van de aarde.
title: Terreaire afbeeldingslagen
uuid: 17968293-1ad2-4040-a174-d33f418af9b7
exl-id: 754211a7-0b1f-4353-86f8-9c634d70cd83
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '992'
ht-degree: 0%

---

# Terreaire afbeeldingslagen{#terrain-image-layers}

{{eol}}

Een grondbeeldlaag toont terreinbeelden van de aarde.

[!DNL Terrain image layers] worden opgeslagen in het [!DNL Geography] gebruiken in een aangepaste indeling. Deze afbeeldingslagen kunnen worden gegenereerd door Adobe of de server van de Data Workbench kan door de gebruiker geleverde terreinbeelden transformeren in terreinlagen die geschikt zijn voor gebruik op de wereldvisualisatie.

>[!NOTE]
>
>Werken met [!DNL terrain image layers], moet u de [!DNL Terrain Images.cfg] bestand opgegeven door Adobe.

Als u een grondafbeeldingslaag wilt definiëren, moet u over het volgende beschikken:

* **Een of meer terreinafbeeldingsbestanden** met de afbeeldingen die op de wereldbol moeten worden weergegeven.
* **A [!DNL Terrain Images.cfg] file** waarmee wordt aangegeven welke terreinafbeeldingsbestanden voor de laag of lagen moeten worden gebruikt. De [!DNL Terrain Images.cfg] kunt u een of meer bronnen toevoegen om een [!DNL terrain image layer]. De indeling van het terreinafbeeldingsbestand bepaalt het type bron dat u wilt toevoegen. In de volgende tabel vindt u een beschrijving van de beschikbare bronnen voor grondafbeeldingslagen, inclusief de ondersteunde bestandsindelingen voor terreinafbeeldingen:

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
   <td colname="col2"> <p>Creates <span class="wintitle"> grondafbeeldingslagen</span> uit 24-bits bestanden zonder koptekst met een lengtegraad die zijn uitgelijnd (niet-geprojecteerd), waarbij noord de bovenkant van de afbeelding is en oost de rechterkant. </p> <p>Ondersteunde afbeeldingsindeling(en): RAW </p> <p> <p>Opmerking: Voor deze bron is projectie-informatie vereist. Voor informatie over projectie-indelingen raadpleegt u <a href="../../../../home/c-get-started/c-im-layers/c-ter-img-layers/c-proj-info-ter-imgs.md#concept-eec35baa01744895b847a02e69dad04e"> Projectie-informatie opgeven voor terreinafbeeldingen</a>. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Algemeen beeld, niet geprojecteerd </p> </td> 
   <td colname="col2"> <p>Creates <span class="wintitle"> grondafbeeldingslagen</span> vanuit 24-bits, uitgelijnde (niet-geprojecteerde) afbeeldingsindelingen in de lengtegraad, waarbij het noorden de bovenkant van de afbeelding is en het oosten rechts. </p> <p>Ondersteunde afbeeldingsindeling(en): BMP, JPG, PNG, TIFF </p> <p> <p>Opmerking: Voor deze bron is projectie-informatie vereist. Voor informatie over projectie-indelingen raadpleegt u <a href="../../../../home/c-get-started/c-im-layers/c-ter-img-layers/c-proj-info-ter-imgs.md#concept-eec35baa01744895b847a02e69dad04e"> Projectie-informatie opgeven voor terreinafbeeldingen</a>. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Afbeelding met ingesloten projectie </p> </td> 
   <td colname="col2"> <p>Creates <span class="wintitle"> grondafbeeldingslagen</span> van afbeeldingsindelingen die geodetische gegevens in het afbeeldingsbestand insluiten. De projectiegegevens worden uit de afbeelding geëxtraheerd. </p> <p>Ondersteunde afbeeldingsindeling(en): Erdas (IMG), GeoTIFF </p> <p> <p>Opmerking: Deze bron vereist gewoonlijk geen projectieinformatie maar steunt de toevoeging van dergelijke informatie indien nodig. Voor informatie over projectie-indelingen raadpleegt u <a href="../../../../home/c-get-started/c-im-layers/c-ter-img-layers/c-proj-info-ter-imgs.md#concept-eec35baa01744895b847a02e69dad04e"> Projectie-informatie opgeven voor terreinafbeeldingen</a>. </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

**Een achtergrondafbeeldingslaag definiëren**

1. In Data Workbench, op **[!UICONTROL Admin]** > **[!UICONTROL Dataset and Profile]** klikt u op de knop **[!UICONTROL Servers Manager]** miniatuur om de [!DNL Servers Manager] werkruimte.
1. Binnen de [!DNL Servers Manager] venster, klikt u met de rechtermuisknop op het pictogram van de gewenste Data Workbench-server en klikt u op **[!UICONTROL Server Files]**.
1. In de [!DNL Server Files Manager], klikt u op **[!UICONTROL Components]** om de inhoud te bekijken. De [!DNL Terrain Images.cfg] bestand bevindt zich in deze map.
1. Klik met de rechtermuisknop op het vinkje in de kolom Servernaam voor [!DNL Terrain Images.cfg]en klik vervolgens op **[!UICONTROL Make Local]**. Er verschijnt een vinkje in het dialoogvenster [!DNL Temp] kolom voor [!DNL Terrain Images.cfg].
1. Klik met de rechtermuisknop op het nieuwe vinkje in het dialoogvenster **[!UICONTROL Temp]** kolom en klik op **[!UICONTROL Open]** > **[!UICONTROL from the workbench]**. De [!DNL Terrain Images.cfg] wordt weergegeven.
1. In de [!DNL Terrain Images] venster, klikt u op **[!UICONTROL component]** om de inhoud te bekijken.
1. Klikken met rechtermuisknop **[!UICONTROL Sources]** > **[!UICONTROL Add new]** en kies een van de volgende brontypen:

   * **[!UICONTROL Raw unprojected bitmap]**. (Nadat dit brontype is toegevoegd, wordt het label RawTerrainSource in het dialoogvenster [!DNL Terrain Images] venster.)

   * **[!UICONTROL General image, unprojected]**. (Na toevoeging wordt dit brontype gelabeld [!DNL GDALTerrainSource] in de [!DNL Terrain Images] venster.)

   * **[!UICONTROL Image with embedded projection]**. (Na toevoeging wordt dit brontype gelabeld [!DNL GDALTerrainSource] in de [!DNL Terrain Images] venster.)

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
   <td colname="col2"> <p>Vereist voor onbewerkte, niet-geprojecteerde bitmapafbeeldingen en algemene afbeeldingen, maar ondersteund voor afbeeldingen met ingesloten projectie. Data Workbench ondersteunt breedtegraad-lengteprojecties en Transverse Mercator (TM)-projecties voor grondafbeeldingslagen. De standaardprojectie-indeling is de breedte-lengteprojectie (LatLonProjection). </p> <p>Voor informatie over projectie-indelingen raadpleegt u <a href="../../../../home/c-get-started/c-im-layers/c-ter-img-layers/c-proj-info-ter-imgs.md#concept-eec35baa01744895b847a02e69dad04e"> Projectie-informatie opgeven voor terreinafbeeldingen</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Bronafbeelding </p> </td> 
   <td colname="col2"> <p>Vereist voor alle bronnen. De naam van het bronafbeeldingsbestand. Dit kan een bestandsnaam of een jokertekenpatroon zijn. Het gebruik van een patroon kan nuttig zijn als afbeeldingen voor hetzelfde gebied op verschillende datums bijvoorbeeld worden geüpload zonder dat de bijbehorende metagegevens worden gewijzigd. Daarom een patroon als <span class="filepath"> Tysons Corner *.raw</span> zou lagen maken van <span class="filepath"> Tysons Corner 050211.raw</span>, <span class="filepath"> Tysons Corner 050218.raw</span>, enzovoort, als er nieuwe afbeeldingen worden toegevoegd, zonder extra configuratie als de parameters voor de bestanden anders identiek zijn. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Tegelcompressiekwaliteit </p> </td> 
   <td colname="col2"> <p>Optioneel voor alle bronnen. Voor JPEG-compressie geeft een geheel getal van 0 tot en met 100 op hoe de afbeeldingsgrootte en -kwaliteit in evenwicht moeten worden gebracht. (De standaardwaarde is nul.) Een hogere waarde resulteert in een betere beeldkwaliteit, maar geeft grotere afbeeldingen en langere downloadtijden voor Data Workbench. </p> <p> <p>Opmerking: Het comprimeren van afbeeldingen onder 70 kan resulteren in een verslechtering van de afbeelding. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Tegelcompressie </p> </td> 
   <td colname="col2"> <p>Optioneel voor alle bronnen. Hiermee geeft u op welke compressiemethode wordt gebruikt voor het schrijven van uitvoerbestanden. De enige momenteel ondersteunde methoden zijn RAWRGB (de standaardinstelling, zonder compressie) en JPEG. Gebruik JPEG-compressie om de grootte te beperken van lagen die tijdens profielsynchronisatie worden verzonden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Breedte </p> </td> 
   <td colname="col2"> <p>Vereist voor onbewerkte, niet-geprojecteerde bitmapafbeeldingen. De breedte van de bronafbeelding in pixels. </p> </td> 
  </tr> 
 </tbody> 
</table>

1. Bewerk de parameters Locatie bronafbeelding, Tijdelijke afbeeldingsopslag en Lagen schrijven naar aan de hand van de volgende tabel als richtlijn. Deze parameters zijn van toepassing op alle grondafbeeldingsbronnen die u in het dialoogvenster [!DNL Sources] van dit bestand.

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
   <td colname="col2"> <p>Optioneel. De naam van een map die wordt gebruikt voor de opslag van tijdelijke bestanden die worden gebruikt voor de omzetting van bronafbeeldingen in terreinlagen. Als het geen absoluut pad is, wordt het geïnterpreteerd ten opzichte van de installatiemap van de Data Workbench-server. De standaardlocatie is <span class="wintitle"> Temperatuur</span> directory. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Lagen schrijven naar </p> </td> 
   <td colname="col2"> <p>Vereist. De map waarnaar grondlagen worden uitgevoerd. Doorgaans is dit de submap Maps van een profielmap, zodat de wereldvisualisatie de lagen kan vinden. </p> </td> 
  </tr> 
 </tbody> 
</table>

1. Sla het bestand op door met de rechtermuisknop te klikken **[!UICONTROL (modified)]** boven aan het venster en klikken op **[!UICONTROL Save]**.
1. Als u een bijgewerkt bestand wilt opslaan op de computer van de Data Workbench-server, gaat u in het dialoogvenster [!DNL Server Files Manager], klikt u met de rechtermuisknop op het vinkje voor [!DNL Terrain Images.cfg] in de [!DNL Temp] kolom, klik vervolgens op **[!UICONTROL Save to]** > *&lt;**[!UICONTROL server name]**>*.
