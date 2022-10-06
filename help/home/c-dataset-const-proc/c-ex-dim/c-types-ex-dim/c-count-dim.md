---
description: De elementen van een telbare dimensie kunnen door het systeem worden geteld.
title: Vertelbare Dimension
uuid: 3312f5eb-69b9-43af-b32a-5c40e3050b29
exl-id: c607c15d-de85-4daf-af76-79b460f51b38
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '685'
ht-degree: 0%

---

# Vertelbare Dimension{#countable-dimensions}

{{eol}}

De elementen van een telbare dimensie kunnen door het systeem worden geteld.

De telbare afmetingen worden typisch gebruikt om samenvattingsmetriek tot stand te brengen, die de telling, of de som, van alle elementen van de afmeting terugkeren. U kunt aftelbare afmetingen definiëren om instanties zoals boekingen of productbestellingen te tellen. Bijvoorbeeld, kon u de telbare afmetingsorden bepalen waarvan de elementen (logboekingangen die aan orden van uw online opslag beantwoorden) konden worden geteld. Als u een telling van orden binnen een visualisatie wilt tonen, zou u metrische de som van Orden bepalen, die over een afmeting kan worden geëvalueerd of filters hebben op het worden toegepast.

De tellende afmetingen kunnen ouders van andere dimensies of kinderen van andere telbare afmetingen zijn.

>[!NOTE]
>
>Als u een afmeting nodig hebt die slechts een telling van iets verstrekt, zou u een numerieke afmeting met een verrichting van COUNT moeten gebruiken. Zie [Numerieke Dimension](../../../../home/c-dataset-const-proc/c-ex-dim/c-types-ex-dim/c-num-dim.md#concept-8513b9afaff447c8b334410b565b91ed).

De telbare afmetingen worden bepaald door de volgende parameters:

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
   <td colname="col2"> Beschrijvende naam van de dimensie die de gebruiker in de werkbank voor gegevens ziet. De naam van de dimensie mag geen afbreekstreepje (-) bevatten. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Opmerkingen </td> 
   <td colname="col2"> Optioneel. Opmerkingen over de uitgebreide dimensie. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Voorwaarde </td> 
   <td colname="col2"> De omstandigheden waaronder het inputgebied tot de verwezenlijking van de telbare dimensie bijdraagt. Indien gespecificeerd, beperkt een voorwaarde de reeks logboekingangen zichtbaar aan de dimensie en al zijn kinderen in het datasetschema. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Verborgen </td> 
   <td colname="col2"> Hiermee wordt bepaald of de dimensie wordt weergegeven in de interface van de gegevenswerkbank. Deze parameter is standaard ingesteld op false. Als de afmeting bijvoorbeeld alleen als basis van een metrische waarde moet worden gebruikt, kunt u deze parameter instellen op true om de afmeting te verbergen in de weergave op de werkbank. </td> 
   <td colname="col3"> false </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Sleutel </td> 
   <td colname="col2"> <p>Optioneel. De naam van het veld dat als sleutel moet worden gebruikt. Als u deze parameter definieert, bestaat er een element van de aftelbare dimensie voor elke combinatie van een element van het bovenliggende element van de aftelbare dimensie en een specifieke waarde van het veld dat als de sleutel is opgegeven. </p> <p> Elk element van de telbare dimensie wordt vereist om op een aangrenzende reeks logboekingangen betrekking te hebben. Daarom als de logboekingangen niet door de sleutel worden bevolen, wordt een element van de telbare dimensie gecreeerd telkens als de belangrijkste gebiedsveranderingen. Om deze situatie te voorkomen, raadt Adobe u aan een unieke sleutel te gebruiken die in de tijdvolgorde aaneengesloten is. </p> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Bovenliggend </td> 
   <td colname="col2"> <p>De naam van de bovenliggende dimensie. Elke aftelbare dimensie kan een bovenliggende dimensie zijn. Om een afmeting de top-level afmeting in het schema van de dataset te maken, plaats de parameter aan "wortel." De bepaalde afmeting wordt de wortel telbare afmeting voor de dataset. Bijvoorbeeld, als u met Plaats werkt, is de dimensie van de Bezoeker de wortel telbare dimensie voor uw dataset. </p> <p> <p>Opmerking: Hoewel uw wortel telbare afmeting niet met het volgen IDs in de gegevens moet worden geassocieerd, adviseert Adobe dat u de wortel telbare afmeting van uw dataset vormt om het volgende gebied van identiteitskaart (x-trackingid) als zijn Sleutel te gebruiken. Dientengevolge, wordt elk element van de wortel telbaar geassocieerd met een unieke waarde van x-trackingid, en alle gegevens over elk element worden gegroepeerd. Als u uw dataset verschillend zou willen vormen, contacteer Adobe. </p> </p> </td> 
   <td colname="col3"> </td> 
  </tr> 
 </tbody> 
</table>

In dit voorbeeld wordt de definitie van een aftelbare dimensie getoond aan de hand van gebeurtenisgegevens die uit websiteverkeer zijn verzameld. De aftelbare dimensie telt de gebeurtenissen van de Webcampagne binnen een bepaalde zitting. De aanname is dat alle bronnen voor e-mailcampagnes worden aangevraagd bij de webserver met &quot;email=&quot; als onderdeel van cs-uri-query. In het voorbeeld is het aantal keren dat de bezoeker reageert op een e-mailcampagne tijdens een bepaalde sessie van belang, niet de werkelijke waarde van het veld cs-uri-query(e-mail).

![](assets/cfg_Transformation_Dim_Countable.png)

In dit voorbeeld wordt ook de definitie van een aftelbare dimensie getoond aan de hand van gebeurtenisgegevens die uit websiteverkeer zijn verzameld, maar met een gedefinieerde parameter Key. De telbare dimensie van de Zitting gebruikt het x-zitting-zeer belangrijke gebied als zijn sleutel. (Het veld x-session-key is de uitvoer van het [!DNL Sessionize] transformatie en heeft een unieke waarde voor elke sessie.) Elke unieke combinatie van een element van de dimensie van de Bezoeker (ouder) en het x-session-zeer belangrijke gebied is een element van de dimensie van de Zitting.

![](assets/cfg_Transformation_Dim_Countable2.png)
