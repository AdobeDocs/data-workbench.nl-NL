---
description: De volgende afmetingen zijn beschikbaar voor gebruik in het profiel van de Status van de Server van de werkbank van gegevens.
title: Dimension in het statusprofiel van de Server van de Data Workbench
uuid: 4cfe882a-2797-4af9-bd6d-75bc31ee909c
exl-id: 002f6b95-f151-41d9-ae28-9c01c1f621ee
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '1366'
ht-degree: 0%

---

# Dimension in het statusprofiel van de Server van de Data Workbench{#dimensions-in-the-data-workbench-server-status-profile}

De volgende afmetingen zijn beschikbaar voor gebruik in het profiel van de Status van de Server van de werkbank van gegevens.

<table id="table_10DFAD7A0C5946B0A2458F6C08D04FC5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <b>Server</b> </td> 
   <td colname="col2"> Deze aftelbare dimensie, die van het x-trackingid gebied wordt gebouwd, vertegenwoordigt de Servers die momenteel gegevenswerkbank in werking stellen. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Versie agent</b> </td> 
   <td colname="col2"> De waarde cs-uri-query(af) wordt gebruikt voor deze eenvoudige Dimension. Dit is de laatste niet-lege waarde voor een server. Dit toont de bouwstijldatum en de tijd voor de versie(s) van de controleagent die loopt. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Alle profielen opnieuw verwerken</b> </td> 
   <td colname="col2"> Het cs-uri-query(aa) gebied wordt gebruikt voor deze Numerieke Dimension, is het de waarde van de Laatste Rij voor een bepaalde Server, voorwaardelijk op cs-uri-query (k) is niet leeg. Deze dimensie wordt gebruikt om aan te geven of om het even welke profielen Reprocessing zijn. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Percentage capaciteitsrij</b> </td> 
   <td colname="col2"> Het veld cs-uri-query(r) wordt gebruikt voor deze numerieke Dimension. Dit is de waarde van de laatste rij voor een bepaalde server, voorwaardelijk op cs-uri-query(k) is niet leeg. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Percentage capaciteitsgrootte</b> </td> 
   <td colname="col2"> Het cs-uri-query(n) gebied wordt gebruikt voor deze Numerieke Dimension, is het de waarde van de Laatste Rij voor een bepaalde Server, voorwaardelijk op cs-uri-query (k) is niet leeg. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Algemene naam</b> </td> 
   <td colname="col2"> Het sc-ur-query(am) gebied wordt gebruikt voor deze Eenvoudige Dimension, is het de waarde van de Laatste nonblank waarde voor een bepaalde Server. Het toont de Gemeenschappelijke Naam van de servers die worden gecontroleerd. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Componentcontrole voltooid</b> </td> 
   <td colname="col2"> Het cs-uri-query(v) gebied wordt gebruikt voor deze Eenvoudige Dimension, is het de waarde van de Laatste Rij voor een bepaalde Server. Deze dimensie controleert de componenten van de server om te verifiëren zij behoorlijk functioneren. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Componenten in fout</b> </td> 
   <td colname="col2"> Een transformatie Crossrows neemt de Laatste waarde van de Rij van cs-uri-query (ao) en kopieert het in het x-components-in-foutengebied. Dit Vele aan Vele afmeting toont om het even welke componenten in fout op servers die worden gecontroleerd. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Omgeving</b> </td> 
   <td colname="col2">De waarde cs-uri-query(c) wordt gebruikt voor de milieu-id. De laatste rij voor een blok wordt gebruikt als waarde voor de dimensie. Deze Eenvoudige Dimension zal het Milieu tonen waarin uw Servers lopen (op voorwaarde dat het behoorlijk wordt gevormd). <p><p>Opmerking:  Deze dimensie wordt geplaatst in insight_monitor_agent.cfg. </p></p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Geschatte wiepper dekaseconds</b> </td> 
   <td colname="col2"> Het veld x-estimated-sweep-dekaseconds wordt gebruikt in deze numerieke Dimension. Dit is de geschatte controletijd van de servers gedeeld door tien (verminderde resolutie van vegen meting om dimensie redelijker te maken). <p><p>Opmerking:  Deze dimensie is verborgen omdat het alleen nuttig is wanneer het gemiddelde in een metrische waarde wordt genomen. </p></p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Host</b> </td> 
   <td colname="col2"> De waarde cs-uri-query(b) wordt gebruikt voor deze dimensie. De waarde van de eenvoudige dimensie is de Laatste Rij voor een Blok. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Laatste pingel</b> </td> 
   <td colname="col2"> x-last-pingel is x-unixtime verdelen door 10 (om numerieke groottebeperkingen aan te passen). Laatste pingelt is de Laatste Rij voor een bepaald Blok, en het vertegenwoordigt de laatste tijd de controleagent het programma opende de systeemgezondheid. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Gemiddelde belasting</b> </td> 
   <td colname="col2"> Dit is een Numerieke dimensie die de Laatste Rij voor de waarde van cs-uri-query(i) van een bepaalde Server gebruikt. De voorwaarde is dat cs-uri-query(k) niet leeg is. Deze dimensie wordt gebruikt om de gemiddelde lading op de servers in het systeem te berekenen die worden gecontroleerd. <p>Opmerking:  Deze dimensie is verborgen omdat het alleen nuttig is wanneer het gemiddelde in een metrische waarde wordt genomen. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Percentage geheugenpaginabestand</b> </td> 
   <td colname="col2"> Dit is een Numerieke dimensie die de Laatste Rij voor de cs-uri-vraag (o) waarde van een bepaalde Server gebruikt. De voorwaarde is dat cs-uri-query(k) niet leeg is. Deze dimensie wordt gebruikt om het percentage van het geheugengebruik van het paginadossier te berekenen. <p>Opmerking:  Deze dimensie is verborgen omdat het alleen nuttig is wanneer het gemiddelde in een metrische waarde wordt genomen. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Totaal aantal fysieke MegaBytes-geheugen</b> </td> 
   <td colname="col2"> Dit is een Numerieke dimensie die de Laatste Rij voor de waarde van cs-uri-query(ag) van een bepaalde Server gebruikt. De voorwaarde is dat cs-uri-query(k) niet leeg is. <p>Opmerking:  Deze dimensie is verborgen omdat het alleen nuttig is wanneer het gemiddelde in een metrische waarde wordt genomen. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Fysiek percentage geheugen</b> </td> 
   <td colname="col2"> Dit is een Numerieke dimensie die de Laatste Rij voor de waarde van cs-uri-query(ag) van een bepaalde Server gebruikt. De voorwaarde is dat cs-uri-query(k) niet leeg is. Deze dimensie wordt gebruikt om het percentage van fysiek geheugengebruik van elke Server te berekenen. <p>Opmerking:  Deze dimensie is verborgen omdat het alleen nuttig is wanneer het gemiddelde in een metrische waarde wordt genomen. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Percentage geheugenquery</b> </td> 
   <td colname="col2"> Dit is een numerieke dimensie die de Laatste Rij voor de cs-uri-vraag van een bepaalde Server waarde gebruikt. De voorwaarde is dat cs-uri-query(k) niet leeg is. Deze afmeting wordt gebruikt om het percentage van het gebruik van het vraaggeheugen van elke Server te berekenen. <p>Opmerking:  Deze dimensie is verborgen omdat het alleen nuttig is wanneer het gemiddelde in een metrische waarde wordt genomen. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Netwerkverbindingen</b> </td> 
   <td colname="col2"> Dit is een Numerieke dimensie die de Laatste Rij voor de waarde van cs-uri-query (q) van een bepaalde Server gebruikt. De voorwaarde is dat cs-uri-query(k) niet leeg is. Dit wordt gebruikt om het aantal netwerkverbindingen te tonen er voor een bepaalde server zijn. <p>Opmerking:  Deze dimensie is verborgen omdat het alleen nuttig is wanneer het gemiddelde in een metrische waarde wordt genomen. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Centiseconden opiniepeilingvertraging</b> </td> 
   <td colname="col2"> Deze dimensie wordt gebruikt om de opiniepeilingslatentie te berekenen. De waarde cs-uri-query(m) wordt gedeeld door 10 om afmeting te verminderen, en gekopieerd in het x-poll-latency-centiseconds gebied. Dit is een numerieke dimensie die de Laatste Rij voor een bepaalde server neemt. <p>Opmerking:  Deze dimensie is verborgen omdat het alleen nuttig is wanneer het gemiddelde in een metrische waarde wordt genomen. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Snelle controle voltooid</b> </td> 
   <td colname="col2"> Dit is een Eenvoudige afmeting die van de cs-uri-vraag (g) waarde van de Laatste Rij voor een bepaalde Server wordt gebouwd. Deze wordt gebruikt om de metrische sneltoets te berekenen. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Ruimtepercentage tijdelijke database</b> </td> 
   <td colname="col2"> De laatste rij van de waarde cs-uri-query(an) wordt gekopieerd naar het veld x-temp-db-space-percentage. Dit is een numerieke Dimension die wordt gebruikt om het percentage te berekenen van de gebruikte Temp DB-ruimte op een bepaalde server. <p>Opmerking:  Deze dimensie is verborgen omdat het alleen nuttig is wanneer het gemiddelde in een metrische waarde wordt genomen. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Inzichtsversie</b> </td> 
   <td colname="col2"> De waarde cs-uri-query(ab) wordt gebruikt voor deze eenvoudige Dimension. Dit is de laatste niet-lege waarde voor een server. Hierdoor worden de versie(s) van de gegevenswerkbankserver weergegeven die op elke server wordt uitgevoerd. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Groep</b> </td> 
   <td colname="col2"> Het groeperen van woord dat u een andere manier geeft om de resulterende dataset te filtreren. <p>Opmerking:  Deze dimensie wordt geplaatst in insight_monitor_agent.cfg. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Cijfers</b> </td> 
   <td colname="col2"> Hieronder ziet u een overzicht van de meetgegevens die zijn opgenomen in het controleprofiel van de gegevenswerkbank en de manier waarop deze zijn afgeleid. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Totale capaciteit</b> </td> 
   <td colname="col2"> Dit is de metrische tijden van de Grootte van de Capaciteit twee plus metrische die de Rij van de Capaciteit door 3 wordt gedeeld. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Capaciteitsrij</b> </td> 
   <td colname="col2"> Dit is de som van het percentage van de Rij van de Capaciteit voor elke Server gedeeld door metrische Servers. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Capaciteitsgrootte</b> </td> 
   <td colname="col2"> Dit is de som van het percentage van de Grootte van de Capaciteit voor elke Server gedeeld door metrische Servers. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Componentcontrole</b> </td> 
   <td colname="col2"> Dit is het aantal Servers waar het Succes van de Controle van de Component één, gedeeld door de Server waar de Dienst DPU of FSU is, allen vermenigvuldigd met 100 (om het een percentage te maken) evenaart. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Schijf "x"</b> </td> 
   <td colname="col2"> De metriek van de Schijf wordt berekend door de som van hun Schijf te nemen Gebruikt Percentage voor elke Server, die door metrische Servers wordt gedeeld. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Geschatte zweepminuten</b> </td> 
   <td colname="col2"> Dit is de som geschat Dekaseconds van de Veeg voor elke Server, gedeeld door metrisch van Servers waar de Geschatte Dekaseconds van de Veeg groter is dan nul, allen gedeeld door 6. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Laatste pingstijd</b> </td> 
   <td colname="col2"> De som van Laatste pingelt voor elk Blok gedeeld door Blokken, dan vermenigvuldigd met 10. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Laden</b> </td> 
   <td colname="col2"> Dit is de som Gemiddelde van de Lading voor elke Server, die door metrische Servers wordt gedeeld. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Geheugenpaginabestand</b> </td> 
   <td colname="col2"> Dit is de som van het percentage van het Dossier van de Pagina van het Geheugen voor elke Server, gedeeld door metrische Servers. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Fysiek geheugen</b> </td> 
   <td colname="col2"> Dit is de som Fysiek Percentage van het Geheugen voor elke Server, die door metrische Servers wordt gedeeld. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Geheugenquery</b> </td> 
   <td colname="col2"> Dit is de som van het Percentage van de Vraag van het Geheugen voor elke Server, die door metrische Servers wordt gedeeld. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Netwerkverbindingen</b> </td> 
   <td colname="col2"> Dit is de som van de Verbindingen van het Netwerk voor elke Server die door metrische Servers wordt verdeeld. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Milliseconden opiniepeilingen</b> </td> 
   <td colname="col2"> Dit is de som van de Centiseconden van de Latentie van de Opiniepeiling voor elke Server, die door metrische Servers wordt gedeeld, allen die met 10 wordt vermenigvuldigd. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Snelle controle</b> </td> 
   <td colname="col2"> Dit is het aantal Servers waar het Snelle Succes van de Controle één evenaart, gedeeld door metrische Servers, die allen met 100 wordt vermenigvuldigd. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Servers</b> </td> 
   <td colname="col2"> Dit is de som van één voor elke Server, of het totale aantal gecontroleerde Servers. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Temp DB</b> </td> 
   <td colname="col2"> Dit is de som van het tijdelijke DB-ruimtepercentage voor elke server, gedeeld door de metrische waarde van de servers. </td> 
  </tr> 
 </tbody> 
</table>
