---
description: De interface van het Schema van de Dataset toont de uitgebreide dimensies (telbare, eenvoudige, vele-aan-vele, numerieke, denormale, en tijddimensies) die in om het even welk configuratiedossier van de transformatiedataset worden bepaald en verstrekt een mening van het verband tussen die dimensies.
title: Dataset-schema-interface
uuid: 3726e568-d3ea-47f8-8ac4-582c97fbbe0a
exl-id: a8d4cf02-4ff7-4fcc-9062-425c1fe1fb28
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '414'
ht-degree: 0%

---

# Datasetschema-interface{#dataset-schema-interface}

De interface van het Schema van de Dataset toont de uitgebreide dimensies (telbare, eenvoudige, vele-aan-vele, numerieke, denormale, en tijddimensies) die in om het even welk configuratiedossier van de transformatiedataset worden bepaald en verstrekt een mening van het verband tussen die dimensies.

Bovendien toont de [!DNL Dataset Schema] interface om het even welke afgeleide dimensies die u, evenals om het even welke uitgebreide dimensies hebt bepaald die om worden gevormd verborgen.

![](assets/vis_DatasetSchema_Example2.png)

>[!NOTE]
>
>U kunt naar dimensies zoeken vanuit het schemadiagram. De naam van de afmetingen die door de zoekreeks worden gevonden, wordt gemarkeerd en de regels van de bovenliggende klasse wijzigen de kleur voor alle resultaten die in ondergeschikte onderliggende afmetingen worden gevonden. De aftelbare afmetingen blijven zichtbaar wanneer u schuift om een zichtbare hiërarchie en context te bieden.

**Een dimensietype interpreteren met de  [!DNL Dataset Schema] interface**

De volgende lijst maakt een lijst van de afmetingstypes en de kleuren waarin hun namen in de [!DNL Dataset Schema] interface verschijnen. Ook de bovenliggende elementen voor de steekproefafmetingen (uit het bovenstaande voorbeeld) worden vermeld.

<table id="table_CF888522626E49A4A10D87085CAB5CC1"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Type Dimension </th> 
   <th colname="col2" class="entry"> Kleur </th> 
   <th colname="col3" class="entry"> Voorbeeld van Dimension en bovenliggend item </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Tabelachtig </td> 
   <td colname="col2"> Roze </td> 
   <td colname="col3"> <p>Bezoeker - In dit schema is de bezoeker een telbare basisdimensie. </p> <p>Sessie - bovenliggende item is bezoeker </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Denormal </td> 
   <td colname="col2"> Geel </td> 
   <td colname="col3"> DenormalPage - bovenliggend item is Paginaweergave </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Afgeleid </td> 
   <td colname="col2"> Blauw </td> 
   <td colname="col3"> Volgende pagina - bovenliggend item is Paginaweergave </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Velen-aan-Velen </td> 
   <td colname="col2"> Roze en groen (de stam van de ouder is roze, terwijl de afmetingsnaam groen is.) </td> 
   <td colname="col3"> Zoekterm - bovenliggende item is sessie </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Numeriek </td> 
   <td colname="col2"> Groen </td> 
   <td colname="col3"> Exacte duur van pagina - bovenliggend element is Paginaweergave. In dit voorbeeld is de exacte duur van de pagina een verborgen numerieke dimensie. Zie het type Verborgen dimensie in deze tabel. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Eenvoudig </td> 
   <td colname="col2"> Groen </td> 
   <td colname="col3"> Pagina - bovenliggend item is paginaweergave </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Tijd </td> 
   <td colname="col2"> Groen </td> 
   <td colname="col3"> Uur - bovenliggende item is sessie </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Verborgen </td> 
   <td colname="col2"> Verborgen afmetingen zijn een donkerdere versie van het juiste dimensietype. Een verborgen numerieke dimensie is bijvoorbeeld een donkerdere, minder heldere groene dimensie. </td> 
   <td colname="col3"> Exacte duur pagina - bovenliggend element is Paginaweergave </td> 
  </tr> 
 </tbody> 
</table>

Voor meer informatie over deze afmetingtypes, zie *de Gids van de Configuratie van de Dataset*.

**De standaardvisualisatie voor een dimensie weergeven**

* Klik in de interface [!DNL Dataset Schema] op de gewenste dimensie. De standaardvisualisatie wordt weergegeven. Als de standaardvisualisatie bijvoorbeeld een tabel is waarin de sessies en de geselecteerde dimensie worden weergegeven en u klikt op de URI-dimensie, geeft de Data Workbench een tabel weer met URI per sessie.

   >[!NOTE]
   >
   >Als u de standaardvisualisatie wilt veranderen die toont, zie [De Interface van het Schema van de Dataset](../../../home/c-get-started/c-admin-intrf/c-dtst-sch-intrf.md#concept-e147b3a5b542453ca2b121e1c85bb175).

**Een specifieke visualisatie voor een dimensie weergeven**

* Klik in de [!DNL Dataset Schema]-interface met de rechtermuisknop op de gewenste dimensie en klik op **[!UICONTROL Add Visualization]** > *&lt;**[!UICONTROL visualization type]**>*.
