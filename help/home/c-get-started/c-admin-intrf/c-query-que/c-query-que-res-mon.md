---
description: De vector van de middelmonitor bevat de Monitor van de Begroting van het Geheugen en het Aantal de Monitor van Vragen.
solution: Analytics
title: Bronnenmonitoren voor query Queue
topic: Data workbench
uuid: 6b516bed-7f9a-4821-869e-19e720f20313
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Bronnenmonitoren voor query Queue{#query-queue-resource-monitors}

De vector van de middelmonitor bevat de Monitor van de Begroting van het Geheugen en het Aantal de Monitor van Vragen.

De volgende lijst beschrijft de gebieden van de middelmonitor die voor vraag het een rij vormen worden gebruikt.

<table id="table_9991EED2647A460FACA2DC80D4973A8E"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Veld </th> 
   <th colname="col2" class="entry"> Type </th> 
   <th colname="col3" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Memory Budget Monitor </p> </td> 
   <td colname="col2"> </td> 
   <td colname="col3"> <p>Controleert het vraaggeheugen dat door de huidige gebruikersgroep wordt gebruikt. Als het huidige gebruik tussen de Lage Drempel en de Hoge Drempel is, worden geen nieuwe bundels gepland tot het geheugengebruik aan onder de Lage waarde van de Drempel terugkeert, bijvoorbeeld, als resultaat van gebruikers die hun werkruimten sluiten. Geplande trossen mogen groeien. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Hoge drempelwaarde </p> </td> 
   <td colname="col2"> <p>dubbeltje </p> </td> 
   <td colname="col3"> <p>De hoge drempel voor geheugengebruik (bytes). Als het geheugengebruik boven deze waarde is, komt geen het plannen voor, en de laagste prioriteit-geplande bunches zijn unscheduled tegelijkertijd, over een periode, tot het geheugengebruik aan onder deze waarde wordt gebracht. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Lage drempelwaarde </p> </td> 
   <td colname="col2"> <p>dubbeltje </p> </td> 
   <td colname="col3"> <p>De lage drempel voor geheugengebruik (bytes). Als de waarde voor de <span class="wintitle"> Memory Budget Monitor</span> onder deze waarde ligt, mogen nieuwe bunches worden gepland en kunnen geplande bunches groeien. Bijvoorbeeld de bundels groeien wanneer een gebruiker een visualisatie aan een werkruimte toevoegt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Reactietijd </p> </td> 
   <td colname="col2"> <p>dubbeltje </p> </td> 
   <td colname="col3"> <p>De tijdconstante voor het gladmaken van de schatting van het geheugengebruik. Met vloeiende waarden wordt geen reactie op pieken in het gebruik voorkomen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Aantal de Monitor van Vragen </p> </td> 
   <td colname="col2"> </td> 
   <td colname="col3"> <p>Controleert het totale aantal vragen die momenteel voor het profiel gepland zijn. Deze middelmonitor laat u bunches plannen als het totale aantal vragen onder de waarde op het Laag gebied van de Drempel blijft. Deze monitor staat momenteel-geplande bunches toe om te groeien als het totale aantal vragen onder de waarde op het Hoge gebied van de Drempel blijft. Bovendien verwijdert deze monitor bundels met een lage prioriteit om grotere prioriteitsbunches te kunnen plannen of groeien. Deze instelling doet echter geen afbreuk aan bunches met een hogere prioriteit dan die welke in het veld Onaanraakbare prioriteit is opgegeven. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Hoge drempelwaarde </p> </td> 
   <td colname="col2"> </td> 
   <td colname="col3"> <p>De hoge drempel voor geheugengebruik (bytes). Als het geheugengebruik boven deze waarde ligt, treedt geen planning op, en de laagste prioritaire geplande bunches worden niet gepland tegelijkertijd, over een periode, tot het geheugengebruik onder deze waarde wordt gebracht. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Lage drempelwaarde </p> </td> 
   <td colname="col2"> </td> 
   <td colname="col3"> <p>De lage drempel voor geheugengebruik (bytes). Als de waarde voor de <span class="wintitle"> Memory Budget Monitor</span> onder deze waarde ligt, kunnen nieuwe bunches worden gepland en kunnen geplande bunches groeien. </p> </td> 
  </tr> 
 </tbody> 
</table>

