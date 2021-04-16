---
description: Gegevenswerkbank bevat ingebouwde afmetingen.
title: Ingebouwde Dimension
uuid: 0aabbc52-266d-46c1-a4b3-dd575c0f2c72
exl-id: c08a487d-60b8-4db7-8776-7ae1b9f1f27c
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 7%

---

# Ingebouwde Dimension{#built-in-dimensions}

Gegevenswerkbank bevat ingebouwde afmetingen.

In de volgende tabel worden de beschikbare ingebouwde afmetingen voor de gegevenswerkbank weergegeven:

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
   <td colname="col4">Bevat één element "" dat betrekking heeft op alle elementen van alle dimensies. Het evalueren van metrisch over niets is als het evalueren van het over geen afmeting. <p>Het <span class="filepath">-filter [None=""]</span> komt overeen met <span class="filepath"> [True]</span>. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> Eén (verborgen) </td> 
   <td colname="col2"> Numeriek </td> 
   <td colname="col3"> N.v.t. </td> 
   <td colname="col4">Het element "1", dat ook de normale waarde <span class="filepath"> = 1</span> heeft, heeft betrekking op alle elementen van alle dimensies. Één afmeting wordt normaal gebruikt om tellingen te construeren door deze syntaxis te gebruiken: <p><span class="filepath"> sum(one,Countable_Dimension)</span></p></td> 
  </tr> 
 </tbody> 
</table>
