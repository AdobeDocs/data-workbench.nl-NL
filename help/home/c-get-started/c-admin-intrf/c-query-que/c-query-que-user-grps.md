---
description: Lijst die de parameters van de Groep van de Gebruiker bepaalt.
solution: Analytics
title: Gebruikersgroepen voor zoekwachtrijen
topic: Data workbench
uuid: 90d9058c-1809-4579-a8c6-930a07affc83
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Gebruikersgroepen voor zoekwachtrijen{#query-queue-user-groups}

Lijst die de parameters van de Groep van de Gebruiker bepaalt.

<table id="table_670A47E25A7A43F0B599BD7ABB173E69"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Veld </th> 
   <th colname="col2" class="entry"> Type </th> 
   <th colname="col3" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Naam </p> </td> 
   <td colname="col2"> <p>touwtje </p> </td> 
   <td colname="col3"> <p>Een user-defined naam van de gebruikersgroep, zoals Analysts. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Beleid </p> </td> 
   <td colname="col2"> <p>vectorvector </p> </td> 
   <td colname="col3"> <p>Specificeert een beleidstype. Klik met de rechtermuisknop om Standaardbeleid of Dagelijks Programma te kiezen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Standaardbeleid </p> </td> 
   <td colname="col2"> </td> 
   <td colname="col3"> <p>Een StandaardBeleid zorgt ervoor dat de gebruikers met een lage prioriteit oplopend worden bewogen omhoog de rij en gepland, zelfs als de hogere prioritaire gebruikers de rij ingaan. U kunt veelvoudige beleid van het zelfde type in een groep toevoegen, en hun effect is cumulatief. 
     <ul id="ul_F7F60D23DC934F61AF2183177A11FA65"> 
      <li id="li_805ED3E740814FAEBFF2B411BAB3D248"><b>Prioriteitslimiet:</b> De grens waarboven de prioriteit niet wordt verhoogd. De maximumprioritaire waarde. U kunt deze waarde gebruiken om de prioriteiten te houden die door dit beleid worden geproduceerd in een specifieke waaier (bijvoorbeeld, zodat de prioriteiten voor sommige andere groep gebruikers altijd hoger zijn, of zodat stijgen zij niet boven de Onaantastbare Prioriteit. </li> 
     </ul> </p> <p> <b>Standaardbeleidsverhogingen</b> </p> <p>De toenamemontages voor het StandaardBeleid verhogen de prioriteit van een vraagbos aangezien de tijd overgaat. Dit dwingt niet de trossen om worden gepland, maar u kunt deze montages gebruiken om aan gebruikers voorrang te geven die lang hebben gewacht. De een rij gevormde parameters beïnvloeden vragen die momenteel een rij worden gevormd (zoals op greep toe te schrijven aan ontoereikende middelen om hen te voltooien). De geplande parameters beïnvloeden vragen die worden beantwoord. De prioriteit van een vraag stijgt door het aantal dat in de aangewezen toename en de gebieden van het toenameinterval wordt gespecificeerd: 
     <ul id="ul_7A5EE18CE10E4484A203B938525C806C"> 
      <li id="li_4B5CD827AF3848DA811A96C851340518"><b>Verhoging in een rij:</b> Plaatst de prioritaire toename per update terwijl een rij gevormd. Dit het plaatsen zorgt ervoor dat de laag prioritaire gebruikers omhoog de het plannen rij worden bewogen. </li> 
      <li id="li_91CA798235234A1CAC7AB32A7FB1CE84"><b>Het in een rij gevormde Interval van de Stijging:</b> Plaatst het aantal seconden tussen updates terwijl een rij gevormd. </li> 
      <li id="li_079275E21ABA43B796A853624A6BDC29"><b>Geplande verhoging:</b> Plaatst de prioritaire toename per update terwijl gepland. </li> 
      <li id="li_3AE2EC3EBE6C4670BA0FA1BBD03FEBBD"><b>Gepland toenameinterval:</b> Plaatst het aantal seconden tussen updates terwijl gepland. <p> <p>Opmerking:  Het plaatsen van de de toename en intervalupdate tarieven hoger voor een rij gevormde bunches dan voor geplande bunches kan oscillatie veroorzaken. (Bijvoorbeeld, veronderstel u de Opeengemaakte waarde van de Toename aan 100 en de Geplande Toename aan 0 plaatst, en de Een rij gevormde waarde van het Interval van de Toename aan 1 en de Onaantastbare Prioriteit plaatst om hoog te zijn. Als twee vraagbundels binnen met een basisprioriteit van 0 komen, en er niet genoeg middelen zijn om beide vragen tezelfdertijd in werking te stellen, dan is één van hen gepland. Na één seconde, heeft de vraag die niet gepland was een prioriteit van 100, en loopt vooruit die gepland was. Na nog eens twee seconden, heeft degene die nu werd voorgetrokken een prioriteit van 200, en de twee schakelaarplaatsen opnieuw. Geen van beide vraag eindigt, omdat om de twee seconden de vraag die wordt gegevens verwerkt preempted is zodat kan de andere vraag lopen.) </p> </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Dagelijks planningsbeleid </p> </td> 
   <td colname="col2"> </td> 
   <td colname="col3"> <p>Laat u de prioriteit op specifieke tijden van de dag veranderen. Dit programma is nuttig voor geautomatiseerde cliënten, zoals de Server <span class="wintitle"> van het</span>Rapport, en wanneer de gebruikers van het systeem in verschillende tijdzones leven. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Wijzigingen </p> </td> 
   <td colname="col2"> <p>verf </p> </td> 
   <td colname="col3"> <p>Klik met de rechtermuisknop om een geplande prioriteitswijziging toe te voegen. De Tijd van de Verandering is de tijd van dag waarop de verandering voorkomt. Het formaat is uur:notulen AM/PM. Als AM of PM niet is ingegaan, gebruikt het systeem militaire tijd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Prioriteitslimiet </p> </td> 
   <td colname="col2"> <p>verf </p> </td> 
   <td colname="col3"> <p>De maximumprioritaire waarde resulterend uit een verandering. De prioritaire Verandering is het bedrag dat aan de prioriteit wordt toegevoegd. Bijvoorbeeld, keert een waarde van 0 op een standaardprioriteit terug. Om het even welke andere waarde resulteert in een prioriteit van de standaardprioriteit plus dit aantal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Gebruikers </p> </td> 
   <td colname="col2"> <p>vectorvector </p> </td> 
   <td colname="col3"> <p>Maakt een lijst van de gebruikers die lid van de groep zijn. </p> <p> <b>Naam:</b> De naam van de gebruiker aangezien het op het Gemeenschappelijke gebied van de Naam in het certificaat van de gebruiker verschijnt. </p> <p> <b>Extra prioriteit:</b> Verstrekt extra prioriteit aan de basisprioriteit van de gebruikersgroep om de beginnende prioriteit voor die gebruiker te bepalen. </p> </td> 
  </tr> 
 </tbody> 
</table>

