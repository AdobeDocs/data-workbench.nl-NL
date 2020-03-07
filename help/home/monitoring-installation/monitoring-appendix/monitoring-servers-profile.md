---
description: De volgende afmetingen zijn beschikbaar voor gebruik in het profiel Server Status van de gegevenswerkbank.
solution: Analytics
title: Afmetingen in het statusprofiel van een gegevenswerkbank
topic: Data workbench
uuid: 4cfe882a-2797-4af9-bd6d-75bc31ee909c
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Afmetingen in het statusprofiel van een gegevenswerkbank{#dimensions-in-the-data-workbench-server-status-profile}

De volgende afmetingen zijn beschikbaar voor gebruik in het profiel Server Status van de gegevenswerkbank.

<table id="table_10DFAD7A0C5946B0A2458F6C08D04FC5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <b>Server</b> </td> 
   <td colname="col2"> Gebouwd van het x-trackingid gebied, vertegenwoordigt deze telbare dimensie de Servers die momenteel gegevenswerkbank in werking stellen. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Versie agent</b> </td> 
   <td colname="col2"> De cs-uri-vraag (af) waarde wordt gebruikt voor deze Eenvoudige Dimensie. Het is de Laatste waarde Nonblank voor een Server. Dit toont de bouwstijldatum en de tijd voor de versie(s) van de bewakingsagent die loopt. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Alle profielopwerking</b> </td> 
   <td colname="col2"> Het cs-uri-vraag(a) gebied wordt gebruikt voor deze Numerieke Dimensie, is het de waarde van de Laatste Rij voor een bepaalde Server, voorwaardelijk op cs-uri-vraag (k) is niet leeg. Deze dimensie wordt gebruikt om erop te wijzen of om het even welke profielen Reprocessing zijn. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Percentage capaciteitsrijen</b> </td> 
   <td colname="col2"> Het cs-uri-vraag(r) gebied wordt gebruikt voor deze Numerieke Dimensie, is het de waarde van de Laatste Rij voor een bepaalde Server, voorwaardelijk op cs-uri-vraag (k) is niet leeg. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Capaciteitsgrootte percentage</b> </td> 
   <td colname="col2"> Het cs-uri-vraag(n) gebied wordt gebruikt voor deze Numerieke Dimensie, is het de waarde van de Laatste Rij voor een bepaalde Server, voorwaardelijk op cs-uri-vraag (k) is niet leeg. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Algemene naam</b> </td> 
   <td colname="col2"> Het sc-ur-vraag (am) gebied wordt gebruikt voor deze Eenvoudige Dimensie, is het de waarde van de Laatste waarde Nonblank voor een bepaalde Server. Het toont de Gemeenschappelijke Naam van de servers die worden gecontroleerd. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Succesvol componentcontrole</b> </td> 
   <td colname="col2"> Het cs-uri-vraag(v) gebied wordt gebruikt voor deze Eenvoudige Dimensie, is het de waarde van de Laatste Rij voor een bepaalde Server. Deze afmeting controleert de componenten van de server om te verifiëren zij behoorlijk functioneren. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Componenten in fout</b> </td> 
   <td colname="col2"> Een transformatie van Crossrows neemt de Laatste waarde van de Rij van cs-uri-vraag (ao) en kopieert het in het x-componenten-in-foutengebied. Dit velen aan Vele afmetingsvertoningen om het even welke componenten in fout op servers die worden gecontroleerd. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Milieu</b> </td> 
   <td colname="col2">De cs-uri-vraag(c) waarde wordt gebruikt voor identiteitskaart van het Milieu. De Laatste Rij voor een Blok wordt gebruikt als waarde voor de afmeting. Deze Eenvoudige Dimensie zal de Milieu tonen waarin uw Servers lopen (op voorwaarde dat het behoorlijk wordt gevormd). <p><p>Opmerking:  Deze dimensie wordt geplaatst in insight_monitor_agent.cfg. </p></p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Geschatte Sweep Dekaseconds</b> </td> 
   <td colname="col2"> Het x-geschatte-veeg-dekaseconds gebied wordt gebruikt in deze Numerieke Dimensie. Dit is de geschatte sweep time van de servers gedeeld door tien (verminderde resolutie van sweep meting om afmeting redelijker te maken). <p><p>Opmerking:  Deze afmeting is verborgen omdat het slechts nuttig wanneer gemiddeld in metrisch is. </p></p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Gastheer</b> </td> 
   <td colname="col2"> De waarde van cs-uri-query(b) wordt gebruikt voor deze dimensie. De waarde van de Eenvoudige afmeting is de Laatste Rij voor een Blok. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Laatste pingelen</b> </td> 
   <td colname="col2"> x-last-pingel is x-unixtime verdelen door 10 (om de beperkingen van de Numerieke grootte aan te passen). Laatste pingel is de Laatste Rij voor een bepaald Blok, en het vertegenwoordigt de laatste tijd de controleagent de systeemgezondheid registreerde. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Belastingsgemiddelde</b> </td> 
   <td colname="col2"> Dit is een Numerieke dimensie die de Laatste Rij voor de cs-uri-vraag(i) waarde van een bepaalde Server gebruikt. Het wordt geconditioneerd op cs-uri-vraag (k) die niet leeg is. Deze dimensie wordt gebruikt om de gemiddelde lading op de servers in het systeem te berekenen die worden gecontroleerd. <p>Opmerking:  Deze afmeting is verborgen omdat het slechts nuttig wanneer gemiddeld in metrisch is. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Percentage bestanden op geheugenpagina</b> </td> 
   <td colname="col2"> Dit is een Numerieke dimensie die de Laatste Rij voor de cs-uri-vraag (o) waarde van een bepaalde Server gebruikt. Het wordt geconditioneerd op cs-uri-vraag (k) die niet leeg is. Deze dimensie wordt gebruikt om het percentage van het geheugengebruik van het paginadossier te berekenen. <p>Opmerking:  Deze afmeting is verborgen omdat het slechts nuttig wanneer gemiddeld in metrisch is. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Geheugen fysiek MegaBytes totaal</b> </td> 
   <td colname="col2"> Dit is een Numerieke dimensie die de Laatste Rij voor de cs-uri-vraag (ag) waarde van een bepaalde Server gebruikt. Het wordt geconditioneerd op cs-uri-vraag (k) die niet leeg is. <p>Opmerking:  Deze afmeting is verborgen omdat het slechts nuttig wanneer gemiddeld in metrisch is. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Fysiek percentage geheugen</b> </td> 
   <td colname="col2"> Dit is een Numerieke dimensie die de Laatste Rij voor de cs-uri-vraag (ag) waarde van een bepaalde Server gebruikt. Het wordt geconditioneerd op cs-uri-vraag (k) die niet leeg is. Deze dimensie wordt gebruikt om het percentage van fysiek geheugengebruik van elke Server te berekenen. <p>Opmerking:  Deze afmeting is verborgen omdat het slechts nuttig wanneer gemiddeld in metrisch is. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Percentage geheugenquery</b> </td> 
   <td colname="col2"> Dit is een numerieke dimensie met behulp van de laatste rij voor de waarde van de cs-uri-query(s) van een bepaalde server. Het wordt geconditioneerd op cs-uri-vraag (k) die niet leeg is. Deze afmeting wordt gebruikt om het percentage van het gebruik van het vraaggeheugen van elke Server te berekenen. <p>Opmerking:  Deze afmeting is verborgen omdat het slechts nuttig wanneer gemiddeld in metrisch is. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Netwerkverbindingen</b> </td> 
   <td colname="col2"> Dit is een Numerieke dimensie die de Laatste Rij voor de cs-uri-vraag (q) waarde van een bepaalde Server gebruikt. Het wordt geconditioneerd op cs-uri-vraag (k) die niet leeg is. Dit wordt gebruikt om het aantal netwerkverbindingen te tonen er voor een bepaalde server zijn. <p>Opmerking:  Deze afmeting is verborgen omdat het slechts nuttig wanneer gemiddeld in metrisch is. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Latentiecursussen voor opiniepeiling</b> </td> 
   <td colname="col2"> Deze dimensie wordt gebruikt om de opiniepeilingslatentie te berekenen. De cs-uri-vraag (m) waarde wordt verdeeld door 10 om afmetingsgrootte te verminderen, en gekopieerd in het x-opiniepeiling-latentie-centisecondengebied. Dit is een numerieke dimensie die de Laatste Rij voor een bepaalde server neemt. <p>Opmerking:  Deze afmeting is verborgen omdat het slechts nuttig wanneer gemiddeld in metrisch is. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Snel controleren geslaagd</b> </td> 
   <td colname="col2"> Dit is een Eenvoudige dimensie die van de cs-uri-vraag (g) waarde van de Laatste Rij voor een bepaalde Server wordt gebouwd. Het wordt gebruikt om de snelle metrische controle te berekenen. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Temperatuur DB-ruimtepercentage</b> </td> 
   <td colname="col2"> De laatste rij van de cs-uri-vraag (een) waarde wordt gekopieerd in het x-temp-db-ruimte-percentagegebied. Dit is een Numerieke Dimensie die wordt gebruikt om het percentage van de gebruikte ruimte van de OB van Temp op een bepaalde server te berekenen. <p>Opmerking:  Deze afmeting is verborgen omdat het slechts nuttig wanneer gemiddeld in metrisch is. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Versie Inzicht</b> </td> 
   <td colname="col2"> De cs-uri-vraag (ab) waarde wordt gebruikt voor deze Eenvoudige Dimensie. Het is de Laatste waarde Nonblank voor een Server. Dit toont de versie(s) van de server van de gegevenswerkbank die op elke server loopt. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Groep</b> </td> 
   <td colname="col2"> Het woord van de groepering dat u een andere manier geeft om de resulterende dataset te filtreren. <p>Opmerking:  Deze dimensie wordt geplaatst in insight_monitor_agent.cfg. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Metriek</b> </td> 
   <td colname="col2"> De volgende lijst maakt een lijst van de metriek inbegrepen in het Profiel van de Controle van het Profiel van de gegevenswerkbank en hoe zij worden afgeleid. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Totale capaciteit</b> </td> 
   <td colname="col2"> Dit is de metrische tijden van de Grootte van de Capaciteit twee plus metrische de Rij van de Capaciteit die door 3 wordt verdeeld. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Capaciteitsrij</b> </td> 
   <td colname="col2"> Dit is de som het Percentage van de Rij van de Capaciteit voor elke Server die door metrische Servers wordt verdeeld. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Capaciteitsgrootte</b> </td> 
   <td colname="col2"> Dit is de som het Percentage van de Grootte van de Capaciteit voor elke Server die door metrische Servers wordt verdeeld. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Componentcontrole</b> </td> 
   <td colname="col2"> Dit is het aantal Servers waar het Succes van de Controle van de Component één evenaart, verdeeld door de Server waar de Dienst DPU of FSU is, allen vermenigvuldigd met 100 (om het een percentage te maken). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Schijf "x"</b> </td> 
   <td colname="col2"> De metriek van de Schijf wordt berekend door de som van hun Schijf te nemen Gebruikte Percentage voor elke Server, die door metrische Servers wordt verdeeld. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Geschatte zweepminuten</b> </td> 
   <td colname="col2"> Dit is de som geschat van de Dekaseconds van de Zwenk voor elke Server, die door de metrische Servers wordt gedeeld waar de Geschatte Dekaseconds van de Wieg groter is dan nul, allen gedeeld door 6. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Laatste pingtijd</b> </td> 
   <td colname="col2"> De som van Laatste pingelt voor elk Blok dat door Blokken wordt verdeeld, dan vermenigvuldigd met 10. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Belasting</b> </td> 
   <td colname="col2"> Dit is de som van het Gemiddelde van de Lading voor elke Server, die door de metrische Servers wordt verdeeld. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Geheugenpaginabestand</b> </td> 
   <td colname="col2"> Dit is de som van het Percentage van het Dossier van de Pagina van het Geheugen voor elke Server, die door metrische Servers wordt verdeeld. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Fysiek geheugen</b> </td> 
   <td colname="col2"> Dit is de som Fysiek Percentage van het Geheugen voor elke Server, die door de metrische Servers wordt verdeeld. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Geheugenquery</b> </td> 
   <td colname="col2"> Dit is de som van het Percentage van de Vraag van het Geheugen voor elke Server, die door metrische Servers wordt verdeeld. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Netwerkverbindingen</b> </td> 
   <td colname="col2"> Dit is de som die van de Verbindingen van het Netwerk voor elke Server door metrische Servers wordt verdeeld. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>De Latentie van de opiniepeiling milliseconden</b> </td> 
   <td colname="col2"> Dit is de som van de Latentie van de Opiniepeiling Centiseconden voor elke Server, die door de metrische Servers wordt verdeeld, die allen met 10 wordt vermenigvuldigd. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Snelle controle</b> </td> 
   <td colname="col2"> Dit is het aantal Servers waar het Snelle Succes van de Controle één evenaart, die door de metrische Servers wordt verdeeld, allen die met 100 wordt vermenigvuldigd. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Servers</b> </td> 
   <td colname="col2"> Dit is de som van één voor elke Server, of het totale aantal gecontroleerde Servers. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Temp. DB</b> </td> 
   <td colname="col2"> Dit is de som van het de Ruimtepercentage van DB van Temp voor elke Server, die door metrische Servers wordt verdeeld. </td> 
  </tr> 
 </tbody> 
</table>

