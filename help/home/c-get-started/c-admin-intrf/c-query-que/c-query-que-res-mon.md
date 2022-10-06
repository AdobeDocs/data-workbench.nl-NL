---
description: De vector van de middelmonitor bevat de Monitor van de Begroting van het Geheugen en het Aantal Monitor van Vragen.
title: Bronnen voor query-wachtrij
uuid: 6b516bed-7f9a-4821-869e-19e720f20313
exl-id: 6d445a4d-a415-41ce-9d45-1bdd0e726edd
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '399'
ht-degree: 0%

---

# Bronnen voor query-wachtrij{#query-queue-resource-monitors}

{{eol}}

De vector van de middelmonitor bevat de Monitor van de Begroting van het Geheugen en het Aantal Monitor van Vragen.

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
   <td colname="col1"> <p>Geheugenbudgetcontrole </p> </td> 
   <td colname="col2"> </td> 
   <td colname="col3"> <p>Controleert het vraaggeheugen dat door de huidige gebruikersgroep wordt gebruikt. Als het huidige gebruik tussen de Lage Drempel en de Hoge Drempel is, worden geen nieuwe bunches gepland tot het geheugengebruik aan onder de Lage Waarde terugkeert, bijvoorbeeld, als resultaat van gebruikers die hun werkruimten sluiten. Gepland bos mag groeien. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Hoge drempel </p> </td> 
   <td colname="col2"> <p>double </p> </td> 
   <td colname="col3"> <p>De hoge drempel voor geheugengebruik (bytes). Als het geheugengebruik boven deze waarde is, komt geen het plannen voor, en de laagste prioriteit-geplande bundels zijn niet gepland één voor één, over een periode, tot het geheugengebruik aan onder deze waarde wordt gebracht. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Lage drempelwaarde </p> </td> 
   <td colname="col2"> <p>double </p> </td> 
   <td colname="col3"> <p>De lage drempel voor geheugengebruik (bytes). Indien <span class="wintitle"> Geheugenbudgetcontrole</span> de waarde is lager dan deze waarde, nieuwe bunches mogen worden gepland en geplande bunches mogen groeien. Stapels groeien bijvoorbeeld wanneer een gebruiker een visualisatie toevoegt aan een werkruimte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Reactietijd </p> </td> 
   <td colname="col2"> <p>double </p> </td> 
   <td colname="col3"> <p>De tijdconstante voor het vloeiend maken van de schatting van het geheugengebruik. Met Vloeiende waarden vermijdt u reacties op gebruikspieken. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Aantal Monitor van Vragen </p> </td> 
   <td colname="col2"> </td> 
   <td colname="col3"> <p>Controleert het totale aantal vragen die momenteel voor het profiel gepland zijn. Deze middelmonitor laat u bunches plannen als het totale aantal vragen onder de waarde op het Lage gebied van de Drempel blijft. Deze monitor staat momenteel-geplande bunches toe om te groeien als het totale aantal vragen onder de waarde op het Hoge gebied van de Drempel blijft. Bovendien verwijdert deze monitor bunches met een lage prioriteit zodat er grotere prioriteitsbunches kunnen worden gepland of gegroeid. Deze instelling heeft echter geen voorrang op bunches met een hogere prioriteit dan is opgegeven in het veld Onaanraakbare prioriteit. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Hoge drempel </p> </td> 
   <td colname="col2"> </td> 
   <td colname="col3"> <p>De hoge drempel voor geheugengebruik (bytes). Als het geheugengebruik boven deze waarde is, komt geen het plannen voor, en de laagste prioriteit geplande bundels is niet gepland één voor één, over een periode, tot het geheugengebruik aan onder deze waarde wordt gebracht. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Lage drempelwaarde </p> </td> 
   <td colname="col2"> </td> 
   <td colname="col3"> <p>De lage drempel voor geheugengebruik (bytes). Indien <span class="wintitle"> Geheugenbudgetcontrole</span> de waarde ligt onder deze waarde, nieuwe bunches kunnen worden gepland en geplande bunches kunnen groeien. </p> </td> 
  </tr> 
 </tbody> 
</table>
