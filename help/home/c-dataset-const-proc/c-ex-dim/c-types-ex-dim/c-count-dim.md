---
description: De elementen van een telbare dimensie kunnen door het systeem worden geteld.
solution: Analytics
title: Afmetingen telbaar
topic: Data workbench
uuid: 3312f5eb-69b9-43af-b32a-5c40e3050b29
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Afmetingen telbaar{#countable-dimensions}

De elementen van een telbare dimensie kunnen door het systeem worden geteld.

De tellbare afmetingen worden typisch gebruikt om samenvattingsmetriek tot stand te brengen, die de telling, of de som, van alle elementen van de afmeting terugkeren. U kunt telbare afmetingen bepalen om instanties zoals reserveringsboekingen of productorden te tellen. Bijvoorbeeld, kon u de telbare afmetingsOrden bepalen de waarvan elementen (logboekingangen die aan orden van uw online opslag beantwoorden) zouden kunnen worden geteld. Als u een telling van orden binnen een visualisatie wilt tonen, zou u de metrische som van Orden bepalen, die over een afmeting kan worden geëvalueerd of filters hebt die op het worden toegepast.

Veelzijdige dimensies kunnen ouders van andere dimensies of kinderen van andere aftelbare afmetingen zijn.

>[!NOTE]
>
>Als u een afmeting nodig hebt die slechts een telling van iets verstrekt, zou u een numerieke afmeting met een verrichting van TELLING moeten gebruiken. Zie [Numerieke afmetingen](../../../../home/c-dataset-const-proc/c-ex-dim/c-types-ex-dim/c-num-dim.md#concept-8513b9afaff447c8b334410b565b91ed).

De meetbare afmetingen worden bepaald door de volgende parameters:

<table id="table_9F3F093F5B074EA68CA4DCE731161F6C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Parameter </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
   <th colname="col3" class="entry"> Standaard </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Naam </td> 
   <td colname="col2"> Beschrijvende naam van de afmeting zoals aan de gebruiker in gegevenswerkbank verschijnt. De afmetingsnaam kan geen koppelteken (-) omvatten. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Opmerkingen </td> 
   <td colname="col2"> Optioneel. Opmerkingen over de uitgebreide dimensie. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Toestand </td> 
   <td colname="col2"> De omstandigheden waaronder het inputgebied tot de verwezenlijking van de tellbare dimensie bijdraagt. Indien gespecificeerd, beperkt een voorwaarde de reeks logboekingangen zichtbaar tot de afmeting en elk van zijn kinderen in het datasetschema. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Verborgen </td> 
   <td colname="col2"> Bepaalt of de afmeting in de interface van de gegevenswerkbank verschijnt. Door gebrek, wordt deze parameter geplaatst aan vals. Als, bijvoorbeeld, de afmeting slechts als basis van metrisch moet worden gebruikt, kunt u deze parameter aan waar plaatsen om de afmeting van de vertoning van de gegevenswerkbank te verbergen. </td> 
   <td colname="col3"> vals </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Sleutel </td> 
   <td colname="col2"> <p>Optioneel. De naam van het gebied aan gebruik als sleutel. Als u deze parameter bepaalt, bestaat een element van de telbare afmeting voor elke combinatie van een element van de ouder van de telbare afmeting en een verschillende waarde van het gebied dat als sleutel wordt gespecificeerd. </p> <p> Elk element van de telbare afmeting wordt vereist om op een aangrenzende reeks logboekingangen betrekking te hebben. Daarom als de logboekingangen niet door de sleutel worden bevolen, wordt een element van de telbare dimensie gecreeerd telkens als de belangrijkste gebiedsveranderingen. Om deze situatie te verhinderen, adviseert Adobe dat u een unieke sleutel gebruikt die aangrenzend in tijdorde is. </p> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Ouder </td> 
   <td colname="col2"> <p>De naam van de ouderafmeting. Om het even welke telbare afmeting kan een ouderafmeting zijn. Om een afmeting te maken de top-level afmeting in het schema van de dataset, plaats de parameter aan "wortel." De bepaalde afmeting wordt de wortel telbare afmeting voor de dataset. Bijvoorbeeld, als u met Plaats werkt, is de dimensie van de Bezoeker de wortel telbare afmeting voor uw dataset. </p> <p> <p>Opmerking:  Hoewel uw wortel telbare afmeting niet met het volgen IDs in de gegevens moet worden geassocieerd, adviseert Adobe dat u de wortel telbare afmeting van uw dataset vormt om het volgende identiteitskaart- gebied (x-trackingidentiteitskaart) als zijn Sleutel te gebruiken. Dientengevolge, wordt elk element van de wortel telbaar geassocieerd met een unieke waarde van x-trackingid, en alle gegevens over elk element wordt gegroepeerd. Als u uw dataset verschillend zou willen vormen, contacteer Adobe. </p> </p> </td> 
   <td colname="col3"> </td> 
  </tr> 
 </tbody> 
</table>

Dit voorbeeld illustreert de definitie van een telbare dimensie gebruikend gebeurtenisgegevens die van websiteverkeer worden verzameld. De telbare afmeting telt de gebeurtenissen van de Webcampagne binnen een bepaalde zitting. De veronderstelling is dat alle middelen van de e-mailcampagne van de Webserver met &quot;email=&quot;als deel van cs-uri-vraag worden gevraagd. In het voorbeeld, is het aantal tijden dat de bezoeker aan een e-mailcampagne tijdens een bepaalde zitting antwoordt van belang, niet de daadwerkelijke waarde van het cs-uri-vraag (e-mail) gebied.

![](assets/cfg_Transformation_Dim_Countable.png)

Dit voorbeeld illustreert ook de definitie van een telbare dimensie gebruikend gebeurtenisgegevens die van websiteverkeer worden verzameld, maar het heeft een bepaalde Belangrijkste parameter. De telbare dimensie van de Zitting gebruikt het x-zitting-zeer belangrijke gebied als zijn sleutel. (Het x-zitting-zeer belangrijke gebied is de output van de [!DNL Sessionize] transformatie en heeft een unieke waarde voor elke zitting.) Elke unieke combinatie van een element van de dimensie van de Bezoeker (de ouder) en het x-zitting-zeer belangrijke gebied is een element van de dimensie van de Zitting.

![](assets/cfg_Transformation_Dim_Countable2.png)

