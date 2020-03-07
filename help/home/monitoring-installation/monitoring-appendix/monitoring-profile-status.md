---
description: De volgende afmetingen zijn beschikbaar voor gebruik in het profiel Profielstatus van de gegevenswerkbank.
solution: Analytics
title: Afmetingen in het profiel Status van het profiel van het profiel van de gegevenswerkbank
topic: Data workbench
uuid: bd84a3e5-d1ea-4768-9dac-62f5dfbad49a
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Afmetingen in het profiel Status van het profiel van het profiel van de gegevenswerkbank{#dimensions-in-the-data-workbench-profile-status-profile}

De volgende afmetingen zijn beschikbaar voor gebruik in het profiel Profielstatus van de gegevenswerkbank.

<table id="table_DD143B4F15FF446DAD24BD2473B485B9"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <b>Blokkeren</b> </td> 
   <td colname="col2"> Dit is de enige telbare in deze configuratie en bestaat als wortel voor alle afmetingen. Een blok kan als een server worden beschouwd. Het gebruikt het x-trackingid veld. De blokidentiteitskaart is een knoeiboel van de servernaam plus gastheernaam, zodat zal er ongeveer één blok per server per profiel zijn. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Vanaf vertragingsminuten</b> </td> 
   <td colname="col2"> cs-uri-vraag (bi) wordt geplaatst in het x-as-van-vertraging-notulen gebied en rond gemaakt aan de dichtstbijzijnde minuut. Vanaf de Notulen van de Vertraging is een numerieke dimensie die de Laatste Rij van x-as-van-vertraging-notulen voor een blok neemt. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Milieu</b> </td> 
   <td colname="col2"> De cs-uri-vraag(c) waarde wordt gebruikt voor identiteitskaart van het Milieu. De Laatste Rij voor een Blok wordt gebruikt als waarde voor de afmeting. Deze Eenvoudige Dimensie zal de Milieu tonen waarin uw Servers lopen (op voorwaarde dat het behoorlijk wordt gevormd). <p>Dit kan in het inzichten_monitor_agent.cfg- dossier worden geplaatst </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Snelle invoer MegaBytes per minuut</b> </td> 
   <td colname="col2"> De cs-uri-vraag (bj) waarde wordt gebruikt voor deze afmeting. De Laatste Rij voor een blok wordt gebruikt als waarde voor de afmeting. Als de dataset in Snelle Input is, zal deze numerieke waarde van de Dimensie de MB per minuut tonen waarbij het systeem gegevens invoert. <p>Opmerking:  Deze afmeting is verborgen omdat het slechts nuttig wanneer gemiddeld in metrisch is. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Snel MegaBytes samenvoegen per minuut</b> </td> 
   <td colname="col2">De cs-uri-vraag (bk) waarde wordt gebruikt voor deze afmeting. De Laatste Rij voor een Blok wordt gebruikt als waarde voor de afmeting. Als de dataset in Snelle Fusie is zal Deze numerieke waarde van de Dimensie MB per minuut tonen waarbij het systeem samenvoegt. <p>Opmerking:  Deze afmeting is verborgen omdat het slechts nuttig wanneer gemiddeld in metrisch is. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Field GigaBytes</b> </td> 
   <td colname="col2"> De cs-uri-vraag (bg) waarde wordt gebruikt voor deze afmeting. De waarde wordt gedeeld door 1000 en afgerond op het dichtstbijzijnde gehele getal. De waarde van deze Numerieke Dimensie zal de hoeveelheid ruimte tonen de Gebieden in de dataset gebruiken. <p>Opmerking:  Deze afmeting is verborgen omdat het slechts nuttig wanneer gemiddeld in metrisch is. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Gastheer</b> </td> 
   <td colname="col2"> De waarde van cs-uri-query(b) wordt gebruikt voor deze dimensie. De waarde van de Eenvoudige afmeting is de Laatste Rij voor een Blok. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Laatste pingelen</b> </td> 
   <td colname="col2">x-last-pingel is x-unixtime verdelen door 10 (om de beperkingen van de Numerieke grootte aan te passen). Laatste pingel is de Laatste Rij voor een bepaald Blok, en het vertegenwoordigt de laatste tijd de controleagent de systeemgezondheid registreerde. <p>Opmerking:  Deze afmeting is verborgen omdat het slechts nuttig wanneer gemiddeld in metrisch is. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Percentage logboeklezingen</b> </td> 
   <td colname="col2">wordt de cs-uri-vraag(be) waarde gebruikt voor deze numerieke dimensie. Het is de Laatste Rij voor een bepaald Blok. Deze afmeting wordt gebruikt om het percentage logboeken te berekenen die worden gelezen. <p>Opmerking:  Deze afmeting is verborgen omdat het slechts nuttig wanneer gemiddeld in metrisch is. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>ID Verwerkingsmodus</b> </td> 
   <td colname="col2"> De cs-uri-vraag (bb) waarde wordt gebruikt voor deze Eenvoudige Dimensie. Het is de Laatste Rij voor een bepaald Blok. Identiteitskaart van de Wijze van de verwerking staat toe om te zien welke wijze van verwerking het systeem binnen is (Snelle Input, Snelle Fusie, Echte Tijd). <p>Opmerking:  Deze afmeting wordt verborgen dan opnieuw blootgesteld met vriendschappelijke waarden in de cliënt-zijafmetingWijze van de Verwerking. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Verwerking geblokkeerd</b> </td> 
   <td colname="col2"> Het x-verwerkings-geblokkeerde gebied wordt gecreeerd door diverse voorwaarden om erop te wijzen of het profiel momenteel loopt of niet. Het is een simpele dimensie. <p>Opmerking:  Deze afmeting werkt het best wanneer er een groot aantal inputlogboeken zijn om onder DPUs eerlijk te verdelen. Als er, bijvoorbeeld, slechts één groot die dossier is per dag wordt geladen, dan kan de gegevenswerkbank schijnen "te stallen"voor een uur of meer resulterend in een valse positieve lezing van deze afmeting. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Profiel</b> </td> 
   <td colname="col2"> De cs-uri-vraag (ba) waarde wordt gebruikt voor deze Eenvoudige Dimensie. Deze dimensie geeft de naam/namen weer van de profielen die momenteel worden gecontroleerd. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Bron: Furthest Behind</b> </td> 
   <td colname="col2"> De laatste rij van cs-uri-vraag (bl) wordt gekopieerd in het x-bron-verst-achter gebied. De eenvoudige Dimensie gebruikt de Laatste Rij voor een bepaald Blok. Deze afmeting toont wanneer het laatste contact met een gegevensbron voorkwam. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Transformatiepercentage</b> </td> 
   <td colname="col2"> de cs-uri-vraag (bf) waarde wordt gebruikt voor deze numerieke dimensie. Het is de Laatste Rij voor een bepaald Blok. Deze dimensie wordt gebruikt om het percentage van volledige gegevenstransformatie te berekenen. <p>Opmerking:  Deze afmeting is verborgen omdat het slechts nuttig wanneer gemiddeld in metrisch is. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Afmetingen tijd</b> </td> 
   <td colname="col2"> Uur, Dag, Week, Maand, Uur van Dag, en Dag van Week zijn allen afgeleid van het x-timestamp gebied. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Groep</b> </td> 
   <td colname="col2"> Het woord van de groepering dat u een andere manier geeft om de resulterende dataset te filtreren. In het bestand insight_monitor_agent.cfg. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Metriek</b> </td> 
   <td colname="col2"> De volgende lijst maakt een lijst van de metriek inbegrepen in het Profiel van de Controle van het Profiel van de gegevenswerkbank en hoe zij worden afgeleid. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Vanaf vertragingsminuten</b> </td> 
   <td colname="col2"> Dit metrisch is de som van de notulen van de Vertraging van elk Blok, dan verdeeld door metrische Blokken. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Vanaf vertragingsseconden</b> </td> 
   <td colname="col2"> Dit metrisch is de som van de seconden van de Vertraging van per Blok, en gedeeld door het totale aantal Blokken. (Vanaf vertragingshoogte is de Dimension niet uit de verpakking geconfigureerd) </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Blokken</b> </td> 
   <td colname="col2"> Som één voor elk Blok. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Snelle invoer MB per minuut</b> </td> 
   <td colname="col2"> De som Snelle Input MegaBytes per Minuut voor elk Blok dat door het aantal Blokken wordt verdeeld wanneer de Snelle Input MegaBytes per Minuut groter is dan nul. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Snel MB samenvoegen per minuut</b> </td> 
   <td colname="col2"> De som Snelle Fusie MegaBytes per Minuut voor elk Blok dat door het aantal Blokken wordt verdeeld wanneer de Snelle Fusie MegaBytes per Minuut groter is dan nul. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Field GigaBytes</b> </td> 
   <td colname="col2"> De som van het Gebied Gigabytes voor elk Blok dat door metrische Blokken wordt gedeeld. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Laatste pingleeftijd</b> </td> 
   <td colname="col2"> De van tijd minus laatste pingelt tijd. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Laatste pingtijd</b> </td> 
   <td colname="col2"> De som van Laatste pingelt voor elk Blok dat door Blokken wordt verdeeld, dan vermenigvuldigd met 10. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Lezen van logbestanden</b> </td> 
   <td colname="col2"> Wanneer het Percentage van de Lezing van het Logboek groter is dan nul, is de Lezing van het Logboek de som Percentage van de Lezing van het Logboek voor elk Blok, dat door metrische Blokken wordt gedeeld, die door 10 wordt verdeeld. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Verwerking geblokkeerd</b> </td> 
   <td colname="col2"> De som van de Verwerking Geroepen Dimensie voor elk Blok, dat door metrisch Blokken wordt verdeeld. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Transformatie</b> </td> 
   <td colname="col2"> De som van het Percentage van de Transformatie voor elk Blok dat door metrisch Blokken wordt verdeeld, wanneer het Percentage van de Transformatie groter is dan nul, allen gedeeld door 10. </td> 
  </tr> 
 </tbody> 
</table>

