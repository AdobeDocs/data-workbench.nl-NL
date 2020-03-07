---
description: De werkbank van gegevens omvat ingebouwde afmetingen.
solution: Analytics
title: Ingebouwde afmetingen
topic: Data workbench
uuid: 0aabbc52-266d-46c1-a4b3-dd575c0f2c72
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Ingebouwde afmetingen{#built-in-dimensions}

De werkbank van gegevens omvat ingebouwde afmetingen.

De volgende lijst maakt een lijst van de beschikbare ingebouwde afmetingen voor gegevenswerkbank:

<table id="table_40796088B3484F98889859C59D525AD7"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Naam </th> 
   <th colname="col2" class="entry"> Details </th> 
   <th colname="col3" class="entry"> Niveau </th> 
   <th colname="col4" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Geen </td> 
   <td colname="col2"> Afgeleid </td> 
   <td colname="col3"> N.v.t. </td> 
   <td colname="col4">Heeft één enkel element "" dat op alle elementen van alle dimensies betrekking heeft. Het evalueren van metrisch over niets is als het evalueren van het over geen dimensie. <p>Het <span class="filepath"> Filter [None="]</span> is gelijk aan <span class="filepath"> [True]</span>. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> Eén (verborgen) </td> 
   <td colname="col2"> Numeriek </td> 
   <td colname="col3"> N.v.t. </td> 
   <td colname="col4">Het element "1", dat ook de normale waarde <span class="filepath"> =1</span>heeft, heeft betrekking op alle elementen van alle afmetingen. Één afmeting wordt normaal gebruikt om tellingen te construeren door deze syntaxis te gebruiken: <p><span class="filepath"> som (één,Countable_Dimension)</span></p></td> 
  </tr> 
 </tbody> 
</table>

