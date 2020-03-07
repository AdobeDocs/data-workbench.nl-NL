---
description: De afmetingen van de latentie worden geconstrueerd van een ouder telbare afmeting, zoals Zittingen, en een tijddimensie, zoals Dag.
solution: Analytics
title: Creeer een latentiedimensie
topic: Data workbench
uuid: 531d8bf6-a66f-4b02-9d81-05664fb9c988
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Creeer een latentiedimensie{#create-a-latency-dimension}

De afmetingen van de latentie worden geconstrueerd van een ouder telbare afmeting, zoals Zittingen, en een tijddimensie, zoals Dag.

Wanneer u een latentietabel maakt in Data Workbench, voegt u automatisch een latentiedimensie toe aan het visualisatiebestand (.vw). U kunt de latentiedimensie van een lijst uitgeven door de hieronder stappen te volgen.

**Om een latentiedimensie uit te geven**

1. Open de latentielijst die u in een tekstredacteur zoals Blocnote creeerde. Het wordt gevestigd in de Gebruiker > `working profile name` > de omslag van het Werk binnen uw de installatiefolder van de Werkbank van Gegevens.

   De bepaalde latentiedimensie omvat de parameters die in het volgende voorbeeld worden getoond. (De definitie van uw latentiedimensie kan extra parameters omvatten.) Het [!DNL line entity = LatencyDim:] wijst op het begin van de definitie van de latentiedimensie.

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

1. Geef de waarden voor de Naam, het Niveau, de Klem, de Tijd, het Formaat, de Tijd vóór, of de Tijd na parameters uit gebruikend de volgende lijst als gids:

   <table id="table_13DF30B8B7314F118D0ED5DF9EA70B9B"> 
   <thead> 
   <tr> 
      <th colname="col1" class="entry"> Voor deze parameter... </th> 
      <th colname="col2" class="entry"> Verstrek deze informatie... </th> 
   </tr> 
   </thead>
   <tbody> 
   <tr> 
      <td colname="col1"> <p>Naam </p> </td> 
      <td colname="col2"> <p>Optioneel. De naam van de latentiedimensie die in het contextmenu verschijnt wanneer u het afmetingsetiket of de elementen met de rechtermuisknop aanklikt. </p> </td> 
   </tr> 
   <tr> 
      <td colname="col1"> <p>Niveau </p> </td> 
      <td colname="col2"> <p>Een telbare dimensie die de ouder van de latentiedimensie is. De voorbeelden omvatten Zitting, Bezoeker, en de Mening van de Pagina. </p> </td> 
   </tr> 
   <tr> 
      <td colname="col1"> <p>Clip </p> </td> 
      <td colname="col2"> <p>Een telbare dimensie die een één-aan-vele verhouding met het niveau van de latentiedimensie heeft. De latentie wordt niet berekend over de grenzen van deze afmeting. Bijvoorbeeld, als u een niveau van de Mening van de Pagina en een klem van Zitting specificeert, worden de latenties berekend voor die paginameningen die tijdens de zelfde zitting zoals de gebeurtenis voorkwamen. </p> <p>Voor informatie over één-aan-vele (eenvoudige) afmetingen, zie de Gids <i>van de Configuratie van de</i>Dataset. </p> </td> 
   </tr> 
   <tr> 
      <td colname="col1"> <p>Tijd </p> </td> 
      <td colname="col2"> <p>De dimensie die wordt gebruikt om verstreken tijd voor de latentiedimensie te meten. Deze dimensie kan een tijddimensie, zoals Dag of Uur, of een telbare afmeting, zoals Bezoeker, Zitting, of de Mening van de Pagina zijn. </p> </td> 
   </tr> 
   <tr> 
      <td colname="col1"> Formaat </td> 
      <td colname="col2"> <p>Optioneel. Specificeert de verschijning van de latentievisualisatie in de Werkbank van Gegevens. Binnen de parameter van het Formaat, kunt u de volgende waarden uitgeven: 
      <ul id="ul_ABF4C17BDE2E4F6C9CBDD933674DE861"> 
         <li id="li_5ED6A7267C81444983AF8507ADC6A5AB">Tijdskoord. De eenheid van tijd die in de latentivisualisatie wordt getoond, zoals dag of week. Ben zeker om het tijdkoord te veranderen wanneer u de tijddimensie verandert. </li> 
         <li id="li_E3B517ECE1494221AAE90455CC0AAB42">Compensatie. Een geheel aantal dat aan negatief van de waarde voor Tijd vóór gelijk is. Bijvoorbeeld, als de Tijd vóór 7 is, zou de compensatie -7 moeten zijn. </li> 
      </ul> </p> </td> 
   </tr> 
   <tr> 
      <td colname="col1"> <p>Tijd voor </p> </td> 
      <td colname="col2"> <p>De maximale hoeveelheid tijd (uitgedrukt in de eenheden van de tijddimensie) vóór de gebeurtenis waarvoor latentie wordt berekend. Als deze waarde aan 0 of niet geplaatst bij allen wordt geplaatst, wordt de latentie berekend slechts voor de voorwaartse richting. </p> <p>Als u deze waarde verandert, ben zeker om de compensatiewaarde in de parameter van het Formaat te veranderen: De compensatie is negatief van de waarde voor Tijd vóór. </p> </td> 
   </tr> 
   <tr> 
      <td colname="col1"> <p>Tijd na </p> </td> 
      <td colname="col2"> <p>De maximale hoeveelheid tijd (uitgedrukt in de eenheden van de tijddimensie) na de gebeurtenis waarvoor latentie wordt berekend. </p> </td> 
   </tr> 
   </tbody> 
   </table>

1. Sla het [!DNL .vw] bestand op in de map User\*working profile name*\Work.

   Na zijn de montages voor de standaardlatentiedimensie:

   ```
   entity = LatencyDim:
   Name = string: 
   Level = ref: wdata/model/dim/Session
   Clip = ref: wdata/model/dim/Visitor
   Time = ref: wdata/model/dim/Day
   Time Before = int: 7
   Time After = int: 7
   ```

   In de volgende latentiedimensie, wordt de latentie van elke zittingsgebeurtenis berekend in uren en de Tijd alvorens aan nul wordt geplaatst. Daarom wordt de latentie berekend voor slechts die zittingen die binnen 24 uur na de bepaalde gebeurtenis voorkwamen.

   ```
   entity = LatencyDim:
   Name = string:
   Level = ref: wdata/model/dim/Session
   Clip = ref: wdata/model/dim/Visitor
   Time = ref: wdata/model/dim/Hour
   Time Before = int: 0
   Time After = int: 24
   ```
