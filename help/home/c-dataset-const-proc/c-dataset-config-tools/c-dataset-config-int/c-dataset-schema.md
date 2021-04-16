---
description: De interface van het Schema van de Dataset toont de uitgebreide dimensies (telbare, eenvoudige, vele-aan-vele, numerieke, denormale, en tijddimensies) die in om het even welk dossier van de Configuratie van de Dataset van de Transformatie en de verhoudingen tussen die dimensies worden bepaald.
title: Dataset-schema
uuid: 4ef5f14b-dc19-4118-a2f2-d680ded8092c
exl-id: b80e6e8e-9147-46ec-8602-2d7e5d33f077
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '380'
ht-degree: 0%

---

# Datasetschema{#dataset-schema}

De interface van het Schema van de Dataset toont de uitgebreide dimensies (telbare, eenvoudige, vele-aan-vele, numerieke, denormale, en tijddimensies) die in om het even welk dossier van de Configuratie van de Dataset van de Transformatie en de verhoudingen tussen die dimensies worden bepaald.

Bovendien toont de [!DNL Dataset Schema] interface om het even welke afgeleide dimensies die u, evenals om het even welke uitgebreide dimensies hebt bepaald die om worden gevormd verborgen.

![](assets/vis_DatasetSchema_Example.png)

In deze sectie worden de volgende onderwerpen besproken:

* [Om dimensietype te interpreteren gebruikend de interface van het Schema van de Dataset](../../../../home/c-dataset-const-proc/c-dataset-config-tools/c-dataset-config-int/c-dataset-schema.md#section-16a0a12b11334c07bec558c0b7d260b1)
* [De standaardvisualisatie voor een dimensie weergeven](../../../../home/c-dataset-const-proc/c-dataset-config-tools/c-dataset-config-int/c-dataset-schema.md#section-1bbb73a5cbb34ffb844eb1932db85318)
* [Een specifieke visualisatie voor een dimensie weergeven](../../../../home/c-dataset-const-proc/c-dataset-config-tools/c-dataset-config-int/c-dataset-schema.md#section-d46626df90bc4c44ae60c4b71eaeac7f)

## Om Dimension Type te interpreteren gebruikend de Interface {#section-16a0a12b11334c07bec558c0b7d260b1} van het Schema van de Dataset

De volgende lijst maakt een lijst van de afmetingstypes en de kleuren waarin hun namen in de [!DNL Dataset Schema] interface verschijnen. Ook de bovenliggende elementen voor de steekproefafmetingen (uit het bovenstaande voorbeeld) worden vermeld.

<table id="table_20D1A9EAAED247338476C475C63255F5"> 
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
   <td colname="col3"> <p>Bezoeker - In dit schema is de bezoeker een telbare basisdimensie. </p> <p> Sessie - bovenliggende item is Bezoeker. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Denormal </td> 
   <td colname="col2"> Geel </td> 
   <td colname="col3"> DenormalPage - bovenliggend item is Paginaweergave. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Afgeleid </td> 
   <td colname="col2"> Blauw </td> 
   <td colname="col3"> Volgende pagina - bovenliggend item is Paginaweergave. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Velen-aan-Velen </td> 
   <td colname="col2"> Roze en groen (de stam van de ouder is roze, terwijl de afmetingsnaam groen is.) </td> 
   <td colname="col3"> Zoekterm - bovenliggend item is sessie. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Numeriek </td> 
   <td colname="col2"> Groen </td> 
   <td colname="col3"> Exacte duur pagina - bovenliggend element is de paginaweergave In dit voorbeeld is de exacte duur van de pagina een verborgen numerieke dimensie. Zie het type Verborgen dimensie in deze tabel. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Eenvoudig </td> 
   <td colname="col2"> Groen </td> 
   <td colname="col3"> Pagina - bovenliggend element is Paginaweergave. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Tijd </td> 
   <td colname="col2"> Groen </td> 
   <td colname="col3"> Uur - bovenliggend item is Sessie. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Verborgen </td> 
   <td colname="col2"> Verborgen afmetingen zijn een donkerdere versie van het juiste dimensietype. Een verborgen numerieke dimensie is bijvoorbeeld een donkerdere, minder heldere groene dimensie. </td> 
   <td colname="col3"> Exacte duur van pagina - bovenliggend element is Paginaweergave. </td> 
  </tr> 
 </tbody> 
</table>

## De standaardvisualisatie voor een Dimension {#section-1bbb73a5cbb34ffb844eb1932db85318} weergeven

* Klik in de interface [!DNL Dataset Schema] op de gewenste dimensie. De standaardvisualisatie wordt weergegeven. Als de standaardvisualisatie bijvoorbeeld een tabel is waarin de sessies en de geselecteerde dimensie worden weergegeven en u klikt op de URI-dimensie, wordt in de werkbank voor gegevens een tabel weergegeven met URI per sessie.

>[!NOTE]
>
>Als u de standaardvisualisatie wilt veranderen die toont, zie het Vormen het hoofdstuk van de Eigenschappen van de Interface en van de Analyse in *de Gids van de Gebruiker van de Data Workbench*.

## Een specifieke visualisatie voor een Dimension tonen {#section-d46626df90bc4c44ae60c4b71eaeac7f}

* Klik in de [!DNL Dataset Schema]-interface met de rechtermuisknop op de gewenste dimensie en klik op **[!UICONTROL Add Visualization]** > *&lt;**[!UICONTROL visualization type]**>*.
