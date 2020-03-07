---
description: De interface van het Schema van de Dataset toont de uitgebreide afmetingen (telbare, eenvoudige, veel-aan-velen, numeriek, denormale, en tijddimensies) die in om het even welk dossier van de Configuratie van de Dataset van de Transformatie en het verband tussen die afmetingen worden bepaald.
solution: Analytics
title: Dataset Schema
topic: Data workbench
uuid: 4ef5f14b-dc19-4118-a2f2-d680ded8092c
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Dataset Schema{#dataset-schema}

De interface van het Schema van de Dataset toont de uitgebreide afmetingen (telbare, eenvoudige, veel-aan-velen, numeriek, denormale, en tijddimensies) die in om het even welk dossier van de Configuratie van de Dataset van de Transformatie en het verband tussen die afmetingen worden bepaald.

Bovendien toont de [!DNL Dataset Schema] interface om het even welke afgeleide afmetingen die u hebt bepaald, evenals om het even welke uitgebreide afmetingen die om worden gevormd verborgen.

![](assets/vis_DatasetSchema_Example.png)

Deze sectie bespreekt de volgende onderwerpen:

* [Om afmetingstype te interpreteren dat de interface van het Schema van de Dataset gebruikt](../../../../home/c-dataset-const-proc/c-dataset-config-tools/c-dataset-config-int/c-dataset-schema.md#section-16a0a12b11334c07bec558c0b7d260b1)
* [Om de standaardvisualisatie voor een afmeting te tonen](../../../../home/c-dataset-const-proc/c-dataset-config-tools/c-dataset-config-int/c-dataset-schema.md#section-1bbb73a5cbb34ffb844eb1932db85318)
* [Om een specifieke visualisatie voor een afmeting te tonen](../../../../home/c-dataset-const-proc/c-dataset-config-tools/c-dataset-config-int/c-dataset-schema.md#section-d46626df90bc4c44ae60c4b71eaeac7f)

## Om het Type van Dimensie te interpreteren Gebruikend de Interface van het Schema van de Dataset {#section-16a0a12b11334c07bec558c0b7d260b1}

De volgende lijst maakt een lijst van de afmetingstypes en de kleuren waarin hun namen in de [!DNL Dataset Schema] interface verschijnen. Ouders voor de afmetingen van de steekproef (uit het bovenstaande voorbeeld) worden eveneens genoteerd.

<table id="table_20D1A9EAAED247338476C475C63255F5"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Afmetingstype </th> 
   <th colname="col2" class="entry"> Kleur </th> 
   <th colname="col3" class="entry"> Afmetingen en bovenliggende elementen </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Veelzeggend </td> 
   <td colname="col2"> Roze </td> 
   <td colname="col3"> <p>Bezoeker - In dit schema, is de Bezoeker een wortel telbare afmeting. </p> <p> Sessie - ouder is bezoeker. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Denormal </td> 
   <td colname="col2"> Geel </td> 
   <td colname="col3"> DenormalPage - de ouder is de Mening van de Pagina. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Afgeleid </td> 
   <td colname="col2"> Blauw </td> 
   <td colname="col3"> Volgende pagina - de ouder is de Mening van de Pagina. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Velen-aan-Velen </td> 
   <td colname="col2"> Roze en Groen (de stam van de ouder is roze, terwijl de afmetingsnaam groen is.) </td> 
   <td colname="col3"> Zoektermijn - bovenliggende is sessie. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Numeriek </td> 
   <td colname="col2"> Groen </td> 
   <td colname="col3"> De nauwkeurige Duur van de Pagina - de ouder is de Mening van de Pagina in dit voorbeeld, is de Exacte Duur van de Pagina een verborgen numerieke dimensie. Zie het Verborgen afmetingstype in deze lijst. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Eenvoudig </td> 
   <td colname="col2"> Groen </td> 
   <td colname="col3"> Pagina - de ouder is de Mening van de Pagina. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Tijd </td> 
   <td colname="col2"> Groen </td> 
   <td colname="col3"> Uur - ouder is sessie. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Verborgen </td> 
   <td colname="col2"> De verborgen afmetingen zijn een donkerdere versie van de aangewezen afmetingstype kleur. Bijvoorbeeld, is een verborgen numerieke dimensie een donkerder, minder heldergroen. </td> 
   <td colname="col3"> De nauwkeurige Duur van de Pagina - de ouder is de Mening van de Pagina. </td> 
  </tr> 
 </tbody> 
</table>

## Om de standaardvisualisatie voor een Dimension weer te geven {#section-1bbb73a5cbb34ffb844eb1932db85318}

* In de [!DNL Dataset Schema] interface, klik de gewenste afmeting. De standaardvisualisatievertoningen. Bijvoorbeeld, als de standaardvisualisatie een lijst is die Zittingen en de geselecteerde afmeting toont, en u de afmeting van URI klikt, toont de gegevenswerkbank een lijst met URI door Zittingen.

>[!NOTE]
>
>Als u de standaardvisualisatie wilt veranderen die toont, zie het het Vormen hoofdstuk van de Eigenschappen van de Interface en van de Analyse in de Gids *van de Gebruiker van de Werkbank van* Gegevens.

## Een specifieke visualisatie voor een dimensie weergeven {#section-d46626df90bc4c44ae60c4b71eaeac7f}

* In de [!DNL Dataset Schema] interface, klik de gewenste afmeting met de rechtermuisknop aan en klik **[!UICONTROL Add Visualization]** > *&lt;**[!UICONTROL visualization type]**>*.

