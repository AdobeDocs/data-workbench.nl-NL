---
description: De afmetingen van de latentie worden geconstrueerd van een oudertelbare afmeting, zoals Zittingen, en een tijdafmeting, zoals Dag.
title: Een latentiedimensie maken
uuid: 531d8bf6-a66f-4b02-9d81-05664fb9c988
exl-id: 38b470ef-9409-455b-b2b8-b0391f80b800
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '542'
ht-degree: 0%

---

# Een latentiedimensie maken{#create-a-latency-dimension}

De afmetingen van de latentie worden geconstrueerd van een oudertelbare afmeting, zoals Zittingen, en een tijdafmeting, zoals Dag.

Wanneer u een latentietabel in Data Workbench maakt, voegt u automatisch een latentiedimensie toe aan het visualisatiebestand (.vw). U kunt de latentiedimensie van een tabel bewerken door de onderstaande stappen te volgen.

**Een latentiedimensie bewerken**

1. Open de latentietabel die u in een teksteditor zoals Kladblok hebt gemaakt. U vindt deze in de map Gebruiker > `working profile name` > Werkmap in de installatiemap van de Data Workbench.

   De gedefinieerde latentiedimensie bevat de parameters die in het volgende voorbeeld worden getoond. (De definitie van de latentiedimensie kan aanvullende parameters bevatten.) De [!DNL line entity = LatencyDim:] geeft het begin van de definitie van de latentiedimensie aan.

   ```
   entity = LatencyDim:
   Name = string: dimension name
   Level = ref: wdata/model/dim/level
   Clip = ref: wdata/model/dim/clip
   Time = ref: wdata/model/dim/time dimension
   Format = printf_format: 
   format = string: %+0.0f time string
   offset = double: offset
   Time Before = int: time before
   Time After = int: time after
   ```

1. Bewerk de waarden voor de parameters Naam, Niveau, Clip, Tijd, Indeling, Tijd voor of Tijd na met behulp van de volgende tabel als richtlijn:

   <table id="table_13DF30B8B7314F118D0ED5DF9EA70B9B"> 
   <thead> 
   <tr> 
      <th colname="col1" class="entry"> Voor deze parameter... </th> 
      <th colname="col2" class="entry"> Deze informatie opgeven... </th> 
   </tr> 
   </thead>
   <tbody> 
   <tr> 
      <td colname="col1"> <p>Naam </p> </td> 
      <td colname="col2"> <p>Optioneel. De naam van de latentieafmeting die in het contextmenu verschijnt wanneer u het afmetingsetiket of de elementen met de rechtermuisknop aanklikt. </p> </td> 
   </tr> 
   <tr> 
      <td colname="col1"> <p>Niveau </p> </td> 
      <td colname="col2"> <p>Een aftelbare dimensie die de ouder van de latentiedimensie is. Voorbeelden zijn Sessie, Bezoeker en Paginaweergave. </p> </td> 
   </tr> 
   <tr> 
      <td colname="col1"> <p>Clip </p> </td> 
      <td colname="col2"> <p>Een aftelbare dimensie die een één-op-vele verhouding met het niveau van de latentiedimensie heeft. Latentie wordt niet berekend over de grenzen van deze dimensie. Als u bijvoorbeeld een niveau van paginaweergave en een clip van sessie opgeeft, worden latentie berekend voor de paginaweergaven die tijdens dezelfde sessie als de gebeurtenis hebben plaatsgevonden. </p> <p>Voor informatie over één-aan-vele (eenvoudige) afmetingen, zie <i>Gids van de Configuratie van de Dataset</i>. </p> </td> 
   </tr> 
   <tr> 
      <td colname="col1"> <p>Tijd </p> </td> 
      <td colname="col2"> <p>De dimensie die wordt gebruikt om de verstreken tijd voor de latentiedimensie te meten. Deze dimensie kan een tijddimensie zijn, zoals Dag of Uur, of een aftelbare dimensie, zoals Bezoeker, Zitting, of de Mening van de Pagina. </p> </td> 
   </tr> 
   <tr> 
      <td colname="col1"> Indeling </td> 
      <td colname="col2"> <p>Optioneel. Hiermee bepaalt u de vormgeving van de latentie-visualisatie in de Data Workbench. Binnen de parameter van het Formaat, kunt u de volgende waarden uitgeven: 
      <ul id="ul_ABF4C17BDE2E4F6C9CBDD933674DE861"> 
         <li id="li_5ED6A7267C81444983AF8507ADC6A5AB">Tijdreeks. De tijdseenheid die wordt getoond in de latentie visualisatie, zoals dag of week. Vergeet niet de tijdtekenreeks te wijzigen wanneer u de tijddimensie wijzigt. </li> 
         <li id="li_E3B517ECE1494221AAE90455CC0AAB42">Verschuiving. Een geheel getal dat gelijk is aan het negatieve getal van de waarde voor Tijd voor. Als Tijd voor bijvoorbeeld 7 is, moet de verschuiving -7 zijn. </li> 
      </ul> </p> </td> 
   </tr> 
   <tr> 
      <td colname="col1"> <p>Tijd voor </p> </td> 
      <td colname="col2"> <p>De maximale tijdsduur (uitgedrukt in de eenheden van de tijddimensie) vóór de gebeurtenis waarvoor latentie wordt berekend. Als deze waarde is ingesteld op 0 of helemaal niet, wordt de vertraging alleen voor de voorwaartse richting berekend. </p> <p>Als u deze waarde wijzigt, moet u de verschuivingswaarde wijzigen in de parameter Format: De verschuiving is het negatief van de waarde voor Tijd voor. </p> </td> 
   </tr> 
   <tr> 
      <td colname="col1"> <p>Tijd na </p> </td> 
      <td colname="col2"> <p>De maximale tijdsduur (uitgedrukt in de eenheden van de tijddimensie) na de gebeurtenis waarvoor latentie wordt berekend. </p> </td> 
   </tr> 
   </tbody> 
   </table>

1. Sla het [!DNL .vw]-bestand op in de map User\*working profile name*\Work.

   Hier volgen de instellingen voor de standaardlatentiedimensie:

   ```
   entity = LatencyDim:
   Name = string: 
   Level = ref: wdata/model/dim/Session
   Clip = ref: wdata/model/dim/Visitor
   Time = ref: wdata/model/dim/Day
   Time Before = int: 7
   Time After = int: 7
   ```

   In de volgende latentiedimensie, wordt de latentie van elke zittingsgebeurtenis berekend in uren en Tijd vóór wordt geplaatst aan nul. Daarom wordt de latentie alleen berekend voor de sessies die binnen 24 uur na de gedefinieerde gebeurtenis hebben plaatsgevonden.

   ```
   entity = LatencyDim:
   Name = string:
   Level = ref: wdata/model/dim/Session
   Clip = ref: wdata/model/dim/Visitor
   Time = ref: wdata/model/dim/Hour
   Time Before = int: 0
   Time After = int: 24
   ```
