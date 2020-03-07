---
description: De interface van het Schema van de Dataset toont de uitgebreide afmetingen (telbare, eenvoudige, veel-aan-velen, numeriek, denormal, en tijddimensies) die in om het even welk de configuratiedossier van de transformatiedataset worden bepaald en verstrekt een mening van het verband tussen die afmetingen.
solution: Analytics
title: Dataset Schema-interface
topic: Data workbench
uuid: 3726e568-d3ea-47f8-8ac4-582c97fbbe0a
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Dataset Schema-interface{#dataset-schema-interface}

De interface van het Schema van de Dataset toont de uitgebreide afmetingen (telbare, eenvoudige, veel-aan-velen, numeriek, denormal, en tijddimensies) die in om het even welk de configuratiedossier van de transformatiedataset worden bepaald en verstrekt een mening van het verband tussen die afmetingen.

Bovendien toont de [!DNL Dataset Schema] interface om het even welke afgeleide afmetingen die u hebt bepaald, evenals om het even welke uitgebreide afmetingen die om worden gevormd verborgen.

![](assets/vis_DatasetSchema_Example2.png)

>[!NOTE]
>
>U kunt naar afmetingen van binnen het schemadiagram zoeken. De naam van de afmetingen die door het onderzoekskoord worden gevonden worden benadrukt, en de lijnen van de de veranderingskleur van de ouderklasse voor om het even welke klappen die in ondergeschikte kindafmetingen worden gevonden. De meetbare afmetingen blijven zichtbaar aangezien u scrolt om viewable hiërarchie en context te verstrekken.

**Om een afmetingstype te interpreteren dat de[!DNL Dataset Schema]interface gebruikt**

De volgende lijst maakt een lijst van de afmetingstypes en de kleuren waarin hun namen in de [!DNL Dataset Schema] interface verschijnen. Ouders voor de afmetingen van de steekproef (uit het bovenstaande voorbeeld) worden eveneens genoteerd.

<table id="table_CF888522626E49A4A10D87085CAB5CC1"> 
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
   <td colname="col3"> <p>Bezoeker - In dit schema, is de Bezoeker een wortel telbare afmeting. </p> <p>Sessie - ouder is bezoeker </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Denormal </td> 
   <td colname="col2"> Geel </td> 
   <td colname="col3"> DenormalPage - ouder is de Mening van de Pagina </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Afgeleid </td> 
   <td colname="col2"> Blauw </td> 
   <td colname="col3"> Volgende pagina - ouder is Paginaweergave </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Velen-aan-Velen </td> 
   <td colname="col2"> Roze en Groen (de stam van de ouder is roze, terwijl de afmetingsnaam groen is.) </td> 
   <td colname="col3"> Zoektermijn - bovenliggende is sessie </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Numeriek </td> 
   <td colname="col2"> Groen </td> 
   <td colname="col3"> De nauwkeurige Duur van de Pagina - de ouder is de Mening van de Pagina. In dit voorbeeld, is de Exacte Duur van de Pagina een verborgen numerieke dimensie. Zie het Verborgen afmetingstype in deze lijst. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Eenvoudig </td> 
   <td colname="col2"> Groen </td> 
   <td colname="col3"> Pagina - bovenliggend is Paginaweergave </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Tijd </td> 
   <td colname="col2"> Groen </td> 
   <td colname="col3"> Uur - ouder is sessie </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Verborgen </td> 
   <td colname="col2"> De verborgen afmetingen zijn een donkerdere versie van de aangewezen afmetingstype kleur. Bijvoorbeeld, is een verborgen numerieke dimensie een donkerder, minder heldergroen. </td> 
   <td colname="col3"> De exacte Duur van de Pagina - de ouder is de Mening van de Pagina </td> 
  </tr> 
 </tbody> 
</table>

Voor meer informatie over deze afmetingstypes, zie de Gids *van de Configuratie van de* Dataset.

**Om de standaardvisualisatie voor een afmeting te tonen**

* In de [!DNL Dataset Schema] interface, klik de gewenste afmeting. De standaardvisualisatievertoningen. Bijvoorbeeld, als de standaardvisualisatie een lijst is die Zittingen en de geselecteerde afmeting toont en u de afmeting van URI klikt, toont de Werkbank van Gegevens een lijst met URI door Zittingen.

   >[!NOTE]
   >
   >Als u de standaardvisualisatie wilt veranderen die toont, zie [de Interface](../../../home/c-get-started/c-admin-intrf/c-dtst-sch-intrf.md#concept-e147b3a5b542453ca2b121e1c85bb175)van het Schema van de Dataset.

**Om een specifieke visualisatie voor een afmeting te tonen**

* In de [!DNL Dataset Schema] interface, klik de gewenste afmeting met de rechtermuisknop aan en klik **[!UICONTROL Add Visualization]** > *&lt;**[!UICONTROL visualization type]**>*.

