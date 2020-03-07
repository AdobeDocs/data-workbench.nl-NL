---
description: De transformatie van de Fusie neemt de waarden van het inputgebied (typisch een vector van koorden), combineert hen in één enkel koord dat door de bepaalde afbakening wordt gescheiden, en plaatst het resulterende koord op het bepaalde outputgebied.
solution: Analytics
title: Samenvoegen
topic: Data workbench
uuid: 9ca2ab22-d854-47b0-8189-f563c1e83d1c
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Samenvoegen{#merge}

De transformatie van de Fusie neemt de waarden van het inputgebied (typisch een vector van koorden), combineert hen in één enkel koord dat door de bepaalde afbakening wordt gescheiden, en plaatst het resulterende koord op het bepaalde outputgebied.

<table id="table_2458E008C9A14B31A774E6819D07E9BE"> 
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
   <td colname="col2"> Beschrijvende naam van de transformatie. U kunt om het even welke naam hier ingaan. </td> 
   <td colname="col3"></td> 
  </tr> 
  <tr> 
   <td colname="col1"> Opmerkingen </td> 
   <td colname="col2"> Optioneel. Opmerkingen over de transformatie. </td> 
   <td colname="col3"></td> 
  </tr> 
  <tr> 
   <td colname="col1"> Toestand </td> 
   <td colname="col2"> De omstandigheden waaronder deze transformatie wordt toegepast. </td> 
   <td colname="col3"></td> 
  </tr> 
  <tr> 
   <td colname="col1"> Standaard </td> 
   <td colname="col2"> De standaardwaarde om te gebruiken als aan de voorwaarde wordt voldaan en de inputwaarde niet beschikbaar is. </td> 
   <td colname="col3"></td> 
  </tr> 
  <tr> 
   <td colname="col1"> Afbakening </td> 
   <td colname="col2"> <p>Koord dat wordt gebruikt om de individuele elementen van de vector van het inputkoord in het enige outputkoord te scheiden. </p> <p> Als u de sleutel van CTRL onderdrukt en binnen de parameter van de Afbakening met de rechtermuisknop aanklikt, verschijnt een menu van het <span class="wintitle"> Tussenvoegsel</span> . Dit menu bevat een lijst van speciale karakters die vaak als afbakeningen worden gebruikt. </p> </td> 
   <td colname="col3"></td> 
  </tr> 
  <tr> 
   <td colname="col1"> Invoer </td> 
   <td colname="col2"> Een vector van koordwaarden die worden gecombineerd om het outputkoord te vormen. </td> 
   <td colname="col3"></td> 
  </tr> 
  <tr> 
   <td colname="col1"> Uitvoer </td> 
   <td colname="col2"> De naam van het outputkoord. </td> 
   <td colname="col3"></td> 
  </tr> 
 </tbody> 
</table>

In dit voorbeeld, wordt een inputvector van koorden verondersteld om een reeks producten te bevatten die voor aankoop werden geselecteerd. Deze producten worden geplaatst in één enkele outputkoord en door &quot;::&quot;gescheiden (twee dubbelpunten).

![](assets/cfg_TransformationType_Merge.png)

Dus als de x-producten van het inputgebied de koordwaarden B57481, C46355, en Z97123 bevatte, zou de resulterende x-show-producten van de outputkoord B57481 zijn::C46355::Z9712332330000000000000000000000000000000000000000000
