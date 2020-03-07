---
description: De tekst of de uitdrukkingen kunnen in om het even welke cel van een aantekenvel zijn ingegaan.
solution: Analytics
title: Werken met gegevens in werkbladen
topic: Data workbench
uuid: c2331fa5-aa07-4622-8f44-5124c22dffcb
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Werken met gegevens in werkbladen{#work-with-data-in-worksheets}

De tekst of de uitdrukkingen kunnen in om het even welke cel van een aantekenvel zijn ingegaan.

Alle uitdrukkingen in een aantekenvel worden voorafgegaan door een gelijk teken (=) tenzij het gebruiken [!DNL eval( )], dat de tekst in de referenced cel als uitdrukking behandelt.

Voor een volledige lijst van metrisch, afmeting, en de regels van de filtersyntaxis, zie de Syntaxis [van de Taal van de](../../../home/c-get-started/c-qry-lang-syntx/c-qry-lang-syntx.md#concept-15d1d3f5164a47d49468c5acb7299d9f)Vraag.

**Om gegevens in een aantekenvel te typen**

1. Klik tweemaal op een cel in de spreadsheet om in te gaan uitgeven wijze. De geselecteerde cel wordt gemarkeerd.
1. Typ of plak de gewenste gegevens in de cel.

**Om van één cel aan een andere te kopiëren en te kleven**

1. Klik de cel met de rechtermuisknop aan die de gegevens bevat die u wilt kopiëren en klikken **[!UICONTROL Copy]**.
1. Klik de cel met de rechtermuisknop aan waarin u de gekopieerde gegevens wilt kleven en klikken **[!UICONTROL Paste]**.

De Werkbank van gegevens werkt automatisch de verwijzingen in de nieuwe cel bij om naar de aangewezen kolommen en de rijen te verwijzen.

**Om van een groep cellen aan een andere te kopiëren en te kleven**

1. Selecteer de cellen die de gegevens bevatten die u wilt kopiëren.
1. Klik de cellen met de rechtermuisknop aan die de gegevens bevatten die u wilt kopiëren en klikken **[!UICONTROL Copy]**.
1. Klik de eerste cel met de rechtermuisknop aan waarin u wilt beginnen de gekopieerde gegevens te kleven en te klikken **[!UICONTROL Paste]**. De gegevens worden gekleefd in de eerste cel en eronder.

De Werkbank van gegevens werkt automatisch de verwijzingen in de nieuwe cel bij om naar de aangewezen kolommen en de rijen te verwijzen.

**Om een kolom op te nemen**

* Klik een kolom met de rechtermuisknop aan en klik **[!UICONTROL Insert Column]**. De nieuwe kolom wordt opgenomen links van de geselecteerde kolom.

**Om een kolom te schrappen**

* Klik de kolom met de rechtermuisknop aan die u wilt schrappen en klikken **[!UICONTROL Delete Column]**. De kolom wordt verwijderd.

**Om een rij op te nemen**

* Klik een rij met de rechtermuisknop aan en klik **[!UICONTROL Insert Row]**. De nieuwe rij wordt opgenomen boven de geselecteerde rij.

**Om een rij te schrappen**

* Klik de rij met de rechtermuisknop aan die u wilt schrappen en klikken **[!UICONTROL Delete Row]**. De rij wordt verwijderd.

**Resize een kolom**

1. In de rij van de kolomkopbal, plaats uw curseur over de scheidende lijn rechts van de kolom de waarvan grootte u wilt veranderen.
1. Klik en sleep aan het recht om de breedte van de kolom, of aan de linkerzijde te verhogen om de breedte van de kolom te verminderen.

**Een cel formatteren**

1. Klik met de rechtermuisknop op de cel en klik op **[!UICONTROL Format]**.

   ![](assets/mnu_Worksheet_Format.png)

1. Klik het gewenste formaat in het menu van beschikbare opties:

<table id="table_5788E01E52CC44E7927A0D23760D9EDD"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Menu Option </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Aantal </p> </td> 
   <td colname="col2"> <p>Past het geselecteerde numerieke formaat op uw gegevens, zoals tijd, datum, percentage, of decimaal toe. </p> <p>Klik <span class="uicontrol"> Gebrek</span> om het geselecteerde formatteren te verwijderen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Uitvullen </p> </td> 
   <td colname="col2"> <p>Hiermee worden de gegevens in de cel links, in het midden of rechts uitgevuld. De standaardrechtvaardiging wordt verlaten. </p> <p>Klik <span class="uicontrol"> Gebrek</span> om het geselecteerde formatteren te verwijderen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Kleur </p> </td> 
   <td colname="col2"> <p>Past de geselecteerde doopvontkleur op de gegevens binnen de cel toe. De standaarddoopvontkleur is wit. </p> <p>Klik <span class="uicontrol"> Gebrek</span> om het geselecteerde formatteren te verwijderen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Indicator </p> </td> 
   <td colname="col2"> <p>Creeert een metrische indicator gebruikend deze cel. Voor meer informatie, zie het <a href="../../../home/c-get-started/c-analysis-vis/c-wksts/c-metric-ind.md#concept-f0e911b23b2c4e8da3e1ea7b9ae04183"> Creëren van Metrische Indicatoren</a>. </p> <p>Klik <span class="uicontrol"> Gebrek</span> om het geselecteerde formatteren te verwijderen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Invoercel </p> </td> 
   <td colname="col2"> <p>Maakt van de geselecteerde cel een invoercel. Voor meer informatie, zie het <a href="../../../home/c-get-started/c-analysis-vis/c-wksts/c-input-cells.md#concept-08cd2c05a28a43dd9f7698b37e23e590"> Creëren van de Cellen</a>van de Input. </p> <p>Klik <span class="uicontrol"> Gebrek</span> om het geselecteerde formatteren te verwijderen. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Sneltoetsen {#section-05301f4d2c60418e86902635a7aeee20}

Binnen aantekenvellen kunt u veel van de basishet uitgeven toetsenbordkortere weg gebruiken die u in om het even welke tekstredacteur, zoals Blocnote of Microsoft Word kunt gebruiken.

De volgende lijst maakt een lijst van de basistoetsenbordkortere weg die u kunt gebruiken wanneer het ingaan van gegevens in een aantekenvel.

<table id="table_8E6F73F253B3451CA1DE45EE4F4E69EF"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Snelkoppeling </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Pijltoetsen </p> </td> 
   <td colname="col2"> <p>Verplaats van cel naar cel in uw aantekenvel met de pijltoetsen omhoog, omlaag, naar links en naar rechts. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>F2 </p> </td> 
   <td colname="col2"> <p>Geef de cel door uw curseur in de cel uit te plaatsen die u hebt geselecteerd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Voer </p> </td> 
   <td colname="col2"> <p>Voltooit het uitgeven van de cel die u hebt geselecteerd. Uw curseur wordt verwijderd uit de cel en de celinhoud wijst op uw het uitgeven. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Esc </p> </td> 
   <td colname="col2"> <p>Annuleer het uitgeven van de cel die u hebt geselecteerd. Uw curseur wordt verwijderd uit de cel en de celinhoud keert aan terug wat zij waren alvorens u begon uit te geven. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Verwijderen </p> </td> 
   <td colname="col2"> <p>Verwijder de inhoud van de cel(len). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Ctrl+A </p> </td> 
   <td colname="col2"> <p>Selecteer de inhoud van de cel. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Ctrl+c </p> </td> 
   <td colname="col2"> <p>Kopieer de inhoud van de cel(len). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Ctrl+x </p> <p>Shift+Verwijderen </p> </td> 
   <td colname="col2"> <p>Kopieer en verwijder de inhoud van de cel(len). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Ctrl+v </p> <p>Shift+Invoegen </p> </td> 
   <td colname="col2"> <p>Plak de inhoud van de cel(len) die u in de geselecteerde cel(len) hebt gekopieerd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Ctrl+z </p> </td> 
   <td colname="col2"> <p>Het typen ongedaan maken. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Ctrl+Shift+z </p> </td> 
   <td colname="col2"> <p>Opnieuw typen. </p> </td> 
  </tr> 
 </tbody> 
</table>

