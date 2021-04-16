---
description: Lijst die de parameters van de Gebruikersgroep bepaalt.
title: Gebruikersgroepen Query-wachtrij
uuid: 90d9058c-1809-4579-a8c6-930a07affc83
exl-id: e9586ad4-4c0b-48b7-b533-4d23a0f4a216
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '611'
ht-degree: 0%

---

# Gebruikersgroepen{#query-queue-user-groups}

Lijst die de parameters van de Gebruikersgroep bepaalt.

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
   <td colname="col2"> <p>string </p> </td> 
   <td colname="col3"> <p>Een door de gebruiker gedefinieerde naam van de gebruikersgroep, zoals Analysts. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Beleid </p> </td> 
   <td colname="col2"> <p>vector </p> </td> 
   <td colname="col3"> <p>Hiermee wordt een beleidstype opgegeven. Klik met de rechtermuisknop om Standaardbeleid of Dagelijks schema te kiezen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Standaardbeleid </p> </td> 
   <td colname="col2"> </td> 
   <td colname="col3"> <p>Een Standaardbeleid zorgt ervoor dat de gebruikers met een lage prioriteit incrementeel omhoog de rij en gepland worden bewogen, zelfs als de hogere prioritaire gebruikers de rij ingaan. U kunt meerdere beleidsregels van hetzelfde type in een groep toevoegen. Het effect ervan is cumulatief. 
     <ul id="ul_F7F60D23DC934F61AF2183177A11FA65"> 
      <li id="li_805ED3E740814FAEBFF2B411BAB3D248"><b>Prioriteitslimiet:</b> de limiet waarboven de prioriteit niet wordt verhoogd. De maximale prioritaire waarde. U kunt deze waarde gebruiken om de prioriteiten die door dit beleid worden gegenereerd, binnen een specifiek bereik te houden (bijvoorbeeld zodat de prioriteiten voor een andere groep gebruikers altijd hoger zijn of niet hoger liggen dan de onaanraakbare prioriteit. </li> 
     </ul> </p> <p> <b>Standaardbeleidsverhogingen</b> </p> <p>De verhogingsmontages voor het Standaard Beleid verhogen de prioriteit van een vraaggroep aangezien de tijd overgaat. Dit dwingt niet de bunches om worden gepland, maar u kunt deze montages gebruiken om aan gebruikers voorrang te geven die lange tijd hebben gewacht. De een rij gevormde parameters beïnvloeden vragen die momenteel een rij worden gevormd (zoals op greep toe te schrijven aan ontoereikende middelen om hen te voltooien). De geplande parameters beïnvloeden vragen die worden beantwoord. De prioriteit van een vraag stijgt met het aantal dat in de aangewezen toename en verhogingsintervalgebieden wordt gespecificeerd: 
     <ul id="ul_7A5EE18CE10E4484A203B938525C806C"> 
      <li id="li_4B5CD827AF3848DA811A96C851340518"><b>Een rij gevormde Toename:</b> Plaatst de prioritaire verhoging per update terwijl een rij gevormd. Dit het plaatsen zorgt ervoor dat de lage prioritaire gebruikers omhoog de het plannen rij worden bewogen. </li> 
      <li id="li_91CA798235234A1CAC7AB32A7FB1CE84"><b>Het in de rij gevormde Interval van de Toename:</b> Plaatst het aantal seconden tussen updates terwijl een rij gevormd. </li> 
      <li id="li_079275E21ABA43B796A853624A6BDC29"><b>Geplande verhoging:</b> Plaatst de prioritaire verhoging per update terwijl gepland. </li> 
      <li id="li_3AE2EC3EBE6C4670BA0FA1BBD03FEBBD"><b>Gepland interval van de Toename:</b> Plaatst het aantal seconden tussen updates terwijl gepland. <p> <p>Opmerking:  Door de update-snelheden voor verhogen en interval voor bunches in de wachtrij in te stellen dan voor geplande bunches, kan oscillatie optreden. (Bijvoorbeeld, veronderstel u de In de rij gevormde waarde van de Toename aan 100 en de Geplande Toename aan 0 plaatst, en de in de rij gevormde waarde van het Interval van de Toename aan 1 plaatst en de Onaanraakbare Prioriteit om hoog te zijn. Als twee vraagbunches binnen met een basisprioriteit van 0 komen, en er niet genoeg middelen zijn om beide vragen tezelfdertijd in werking te stellen, dan is één van hen gepland. Na één seconde, heeft de vraag die niet gepland was een prioriteit van 100, en verkort die gepland was. Na nog twee seconden, heeft die die nu wordt voorgespiegeld een prioriteit van 200, en de twee schakelaar plaatst opnieuw. Geen vraag eindigt, omdat om de twee seconden de vraag die wordt berekend preempted is zodat de andere vraag kan lopen.) </p> </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Beleid voor dagelijkse planning </p> </td> 
   <td colname="col2"> </td> 
   <td colname="col3"> <p>Hiermee kunt u de prioriteit op specifieke tijdstippen van de dag wijzigen. Dit schema is nuttig voor geautomatiseerde cliënten, zoals <span class="wintitle"> de Server van het Rapport </span>, en wanneer de gebruikers van het systeem in verschillende tijdstreken leven. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Wijzigingen </p> </td> 
   <td colname="col2"> <p>int </p> </td> 
   <td colname="col3"> <p>Klik met de rechtermuisknop om een geplande prioriteitswijziging toe te voegen. De tijd van de Verandering is de tijd van dag waarop de verandering voorkomt. De notatie is uur:minuten AM/PM. Als AM of PM niet is ingegaan, gebruikt het systeem militaire tijd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Prioriteitslimiet </p> </td> 
   <td colname="col2"> <p>int </p> </td> 
   <td colname="col3"> <p>De maximale prioritaire waarde die het gevolg is van een wijziging. De prioritaire Verandering is het bedrag dat aan de prioriteit wordt toegevoegd. Bijvoorbeeld, keert een waarde van 0 aan een standaardprioriteit terug. Elke andere waarde resulteert in een prioriteit van de standaardprioriteit plus dit getal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Gebruikers </p> </td> 
   <td colname="col2"> <p>vector </p> </td> 
   <td colname="col3"> <p>Hiermee geeft u de gebruikers weer die lid zijn van de groep. </p> <p> <b>Naam:</b> De naam van de gebruiker zoals deze wordt weergegeven in het veld Algemene naam in het certificaat van de gebruiker. </p> <p> <b>Extra Prioriteit:</b> Verstrekt extra prioriteit aan de basisprioriteit van de gebruikersgroep om de beginnende prioriteit voor die gebruiker te bepalen. </p> </td> 
  </tr> 
 </tbody> 
</table>
