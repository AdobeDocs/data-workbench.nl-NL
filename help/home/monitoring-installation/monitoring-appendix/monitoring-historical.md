---
description: De volgende afmetingen zijn beschikbaar voor gebruik in het historisch profiel van de gegevenswerkbank.
solution: Analytics
title: Afmetingen in historisch profiel van de gegevensbank
topic: Data workbench
uuid: 6d93fba4-986b-46a4-9479-aeb54853dff5
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Afmetingen in historisch profiel van de gegevensbank{#dimensions-in-the-data-workbench-historic-profile}

De volgende afmetingen zijn beschikbaar voor gebruik in het historisch profiel van de gegevenswerkbank.

## Afmetingen in historisch profiel van de gegevensbank {#section-96f1b64f5cb84411b630f97f227d888d}

De volgende afmetingen zijn beschikbaar voor gebruik in het historisch profiel van de gegevenswerkbank.

<table id="table_3EAEA68E73BE431D841F7F2E83EDD6AC"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <b>Blokkeren</b> </td> 
   <td colname="col2">Dit is de enige telbare in deze configuratie, is het de wortel voor alle afmetingen. Een blok kan als een server worden beschouwd. Het gebruikt het x-trackingid veld. <p>Opmerking:  De blokidentiteitskaart is een knoeiboel van de servernaam plus gastheernaam, zodat zal er ongeveer één blok per server per profiel zijn. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>pingelen</b> </td> 
   <td colname="col2"> Dit is een aftelbare afmeting die van het Blok telbaar wordt gebouwd. Elke rij van gegevens in het profiel is pingelt van de controleagent. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Waarschuwingskritiek</b> </td> 
   <td colname="col2"> Numerieke afmetingen die zijn gemaakt op basis van de waarde cs-uri-query(ad). Het wordt gebouwd op het pingel geconditioneerde niveau dat cs-uri-vraag (a) "1"aanpast. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Waarschuwing uitgeschakeld</b> </td> 
   <td colname="col2"> Numerieke afmetingen die zijn gemaakt op basis van de waarde cs-uri-query(ac). Het wordt gebouwd op het pingelt niveau, op voorwaarde dat cs-uri-query(a) "1"aanpast. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Waarschuwingswaarschuwing</b> </td> 
   <td colname="col2"> Numerieke afmetingen die zijn gemaakt op basis van de waarde cs-uri-query(ae). Het wordt gebouwd op het pingel geconditioneerde niveau dat cs-uri-vraag (a) "1"aanpast. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Alle profielopwerking</b> </td> 
   <td colname="col2"> Numerieke afmetingen die zijn gemaakt op basis van de waarde van cs-uri-query(aa). Het wordt gebouwd op het pingelt geconditioneerde niveau dat cs-uri-query(a) "1"aanpast en cs-uriquery (k) niet leeg is. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Vanaf vertragingsminuten</b> </td> 
   <td colname="col2"> cs-uri-vraag (bi) wordt geplaatst in het x-as-van-vertraging-notulen gebied en rond gemaakt aan de dichtstbijzijnde minuut. Het wordt gebouwd op het pingel geconditioneerde niveau dat cs-uri-vraag (a) "1"aanpast. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Percentage capaciteitsrijen</b> </td> 
   <td colname="col2"> Numerieke afmetingen die zijn gemaakt op basis van de waarde voor cs-uri-query(r). Het wordt gebouwd op het pingelt geconditioneerde niveau dat cs-uri-query(a) "1"aanpast en cs-uriquery (k) niet leeg is. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Capaciteitsgrootte percentage</b> </td> 
   <td colname="col2"> Numerieke dimensie die is opgebouwd uit de waarde van cs-uri-query(n). Het wordt gebouwd op het pingelt geconditioneerde niveau dat cs-uri-query(a) "1"aanpast en cs-uriquery (k) niet leeg is. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Succesvol componentcontrole</b> </td> 
   <td colname="col2"> Eenvoudige afmeting gebouwd van de waarde cs-uri-query(v). Het wordt gebouwd op het Ping niveau, en geconditioneerd dat cs-uri-vraag (a) "1"aanpast. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Componenten in fout</b> </td> 
   <td colname="col2"> cs-uri-vraag (ao) wordt verdeeld door de "|"afbakening en gekopieerd in het x-componenten-in-foutengebied. Vele tot Vele Dimensie die van het x-componenten-in-foutengebied wordt gebouwd. Gebouwd op het pingniveau. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Gedetailleerde controle-seconden</b> </td> 
   <td colname="col2"> Numerieke afmetingen die zijn gemaakt op basis van de waarde cs-uri-query(l). Het wordt gebouwd op het pingelt geconditioneerde niveau dat cs-uri-vraag (k) niet leeg is. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Gedetailleerd controlesucces</b> </td> 
   <td colname="col2"> Eenvoudige dimensie die is opgebouwd uit de waarde cs-uri-query(k). Het wordt gebouwd op het pingel geconditioneerde niveau dat cs-uri-vraag (a) "1"aanpast. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Dimension GigaBytes</b> </td> 
   <td colname="col2"> cs-uri-vraag (bc) wordt gekopieerd in het x-afmeting-gigabytegebied. Het x-dimensie-gigabytes gebied is gebruiker voor deze Eenvoudige Dimensie, die op cs-uri-vraag (a) wordt geconditioneerd die "2"aanpast. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Schijf "x" Gebruikt percentage</b> </td> 
   <td colname="col2"> Deze Numerieke Afmetingen worden gevormd van de cs-uri-vraag (ah, ai, aj, ak, al) waarden. Zij worden gebouwd op het pingel niveau en op cs-uri-vraag (a) de gelijken "1"geconditioneerd en cs-uri-vraag (k) is niet leeg. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Geschatte Sweep Dekaseconds</b> </td> 
   <td colname="col2"> Het x-geschatte-veeg-dekaseconds gebied wordt gebruikt in deze Numerieke Dimensie. Dit is de geschatte sweep time van de servers gedeeld door tien (verminderde resolutie van sweep meting om afmeting redelijker te maken). <p>Opmerking:  Deze afmeting is verborgen omdat het slechts nuttig wanneer gemiddeld in metrisch is. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Snelle invoer MegaBytes per minuut</b> </td> 
   <td colname="col2"> De cs-uri-vraag (bj) waarde wordt gebruikt voor deze afmeting. De Laatste Rij voor een blok wordt gebruikt als waarde voor de afmeting. Als de dataset in Snelle Input is, zal deze numerieke waarde van de Dimensie de MB per minuut tonen waarbij het systeem gegevens invoert. <p>Opmerking:  Deze afmeting is verborgen omdat het slechts nuttig wanneer gemiddeld in metrisch is. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Snel MegaBytes samenvoegen per minuut</b> </td> 
   <td colname="col2">De cs-uri-vraag (bk) waarde wordt gebruikt voor deze afmeting. De Laatste Rij voor een Blok wordt gebruikt als waarde voor de afmeting. Als de dataset in Snelle Fusie is zal Deze numerieke waarde van de Dimensie MB per minuut tonen waarbij het systeem samenvoegt. <p><p>Opmerking:  Deze afmeting is verborgen omdat het slechts nuttig wanneer gemiddeld in metrisch is. </p></p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Field GigaBytes</b> </td> 
   <td colname="col2">De cs-uri-vraag (bg) waarde wordt gebruikt voor deze afmeting. De waarde wordt gedeeld door 1000 en afgerond op het dichtstbijzijnde gehele getal. De waarde van deze Numerieke Dimensie zal de hoeveelheid ruimte tonen de Gebieden in de dataset gebruiken. <p>Opmerking:  Deze afmeting is verborgen omdat het slechts nuttig wanneer gemiddeld in metrisch is. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Groep</b> </td> 
   <td colname="col2"> Eenvoudige die Dimensie op het pingniveau van de cs-uri-vraag (x) waarde wordt gebouwd. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Gastheer</b> </td> 
   <td colname="col2"> De waarde van cs-uri-query(b) wordt gebruikt voor deze dimensie. De waarde van de Eenvoudige afmeting is de Laatste Rij voor een Blok. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Laatste pingelen</b> </td> 
   <td colname="col2"> het x-unixtime gebied wordt gekopieerd in x-last-pingelen en door 10 verdeeld om de kardinaliteit te verminderen. De numerieke dimensie wordt gebouwd op het niveau van het Blok en gebruikt x-last-pingelt gebied. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Belastingsgemiddelde</b> </td> 
   <td colname="col2"> Dit is een Numerieke dimensie die de Laatste Rij voor de cs-uri-vraag(i) waarde van een bepaalde Server gebruikt. Het wordt geconditioneerd op cs-uri-vraag (k) die niet leeg is. Deze dimensie wordt gebruikt om de gemiddelde lading op de servers in het systeem te berekenen die worden gecontroleerd. <p><p>Opmerking:  Deze afmeting is verborgen omdat het slechts nuttig wanneer gemiddeld in metrisch is. </p></p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Percentage logboeklezingen</b> </td> 
   <td colname="col2">wordt de cs-uri-vraag(be) waarde gebruikt voor deze numerieke dimensie, die op het Ping niveau wordt gebouwd. Deze afmeting wordt gebruikt om het percentage logboeken te berekenen die worden gelezen. <p>Opmerking:  Deze afmeting is verborgen omdat het slechts nuttig wanneer gemiddeld in metrisch is. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Percentage bestanden op geheugenpagina</b> </td> 
   <td colname="col2"> Dit is een Numerieke dimensie die de waarde van cs-uri-vraag (o) gebruikt, die op het Ping niveau wordt gebouwd. Het wordt geconditioneerd op cs-uri-vraag (k) die niet leeg is, en cs-uri-vraag (a) die "1"aanpassen. Deze dimensie wordt gebruikt om het percentage van het geheugengebruik van het paginadossier te berekenen. <p>Opmerking:  Deze afmeting is verborgen omdat het slechts nuttig wanneer gemiddeld in metrisch is. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Geheugen fysiek MegaBytes totaal</b> </td> 
   <td colname="col2">Dit is een Numerieke dimensie die de cs-uri-vraag (ag) waarde gebruikt, die op het Ping niveau wordt gebouwd. Het wordt geconditioneerd op cs-uri-vraag (k) die niet leeg is, en cs-uri-vraag (a) die "1 aanpassen. <p>Opmerking:  Deze afmeting is verborgen omdat het slechts nuttig wanneer gemiddeld in metrisch is. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Fysiek percentage geheugen</b> </td> 
   <td colname="col2">Dit is een Numerieke dimensie die de cs-uri-vraag (ag) waarde gebruikt, die op het Ping niveau wordt gebouwd. Het wordt geconditioneerd op cs-uri-vraag (k) die niet leeg is, en cs-uri-vraag (a) die "1 aanpassen. Deze dimensie wordt gebruikt om het percentage van fysiek geheugengebruik van elke Server te berekenen. <p>Opmerking:  Deze afmeting is verborgen omdat het slechts nuttig wanneer gemiddeld in metrisch is. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Percentage geheugenquery</b> </td> 
   <td colname="col2"> Dit is een numerieke dimensie met behulp van de waarde van de cs-uri-query(s) op het pingniveau. Het is afhankelijk van cs-uri-query(k) die niet leeg is en cs-uri-query(a) die overeenkomt met "1. Deze afmeting wordt gebruikt om het percentage van het gebruik van het vraaggeheugen van elke Server te berekenen. <p>Opmerking:  Deze afmeting is verborgen omdat het slechts nuttig wanneer gemiddeld in metrisch is. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Netwerkverbindingen</b> </td> 
   <td colname="col2"> Dit is een Numerieke dimensie die de cs-uri-vraag (q) waarde gebruikt die op het Ping niveau wordt gebouwd. Het is afhankelijk van cs-uri-query(k) die niet leeg is en cs-uri-query(a) die overeenkomt met "1. Dit wordt gebruikt om het aantal netwerkverbindingen te tonen er voor een bepaalde server zijn. <p>Opmerking:  Deze afmeting is verborgen omdat het slechts nuttig wanneer gemiddeld in metrisch is. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Uitvoerrijen</b> </td> 
   <td colname="col2"> cs-uri-vraag (bh) de waarde wordt verdeeld door 100000 en gekopieerd in het x-output-rijen gebied om de grootte van de afmeting te verminderen. De x-output-rijen worden gebruikt in een Numerieke Dimensie die op het Pingel niveau wordt gebouwd, op voorwaarde dat cs-uri-query(a) "2"aanpast. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Pingel Type ID</b> </td> 
   <td colname="col2"> De eenvoudige die Dimensie gebruikend de cs-uri-vraag (a) waarde op het pingniveau wordt gebouwd. Dit laat zien wat voor soort Ping werd geregistreerd. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Latentiecursussen voor opiniepeiling</b> </td> 
   <td colname="col2">De cs-uri-vraag (m) waarde wordt verdeeld door 10 om afmetingsgrootte te verminderen, en gekopieerd in het x-opiniepeiling-latentie-centisecondengebied. Dit is een Numerieke dimensie die op het pingniveau wordt gebouwd, op voorwaarde dat cs-uri-query(k) niet leeg is, en cs-uri-query(a) past "1"aan/ Deze dimensie wordt gebruikt om de opiniepeilingslatentie te berekenen. <p>Opmerking:  Deze afmeting is verborgen omdat het slechts nuttig wanneer gemiddeld in metrisch is. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>ID Verwerkingsmodus</b> </td> 
   <td colname="col2"> De cs-uri-vraag (bb) waarde wordt gebruikt voor deze Eenvoudige Dimensie, die op het pingniveau wordt gebouwd. Het wordt geconditioneerd dat cs-uri-vraag (bb) niet leeg is, en dat cs-uri-vraag (a) identiteitskaart van de Wijze van de Verwerking "2"toestaat om te zien welke wijze van verwerking het systeem binnen is (Snelle Input, Snelle Fusie, Echte tijd). <p>Opmerking:  Deze afmeting wordt verborgen dan opnieuw blootgesteld met vriendschappelijke waarden in de cliënt-zijafmetingWijze van de Verwerking. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Profiel</b> </td> 
   <td colname="col2"> De cs-uri-vraag (ba) waarde wordt gebruikt voor deze Eenvoudige Dimensie, wordt het gebouwd op het pingniveau. Deze dimensie geeft de naam weer van het (de) profiel(en) dat (die) momenteel wordt (worden) bewaakt. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Snel controleren seconden</b> </td> 
   <td colname="col2"> De cs-uri-vraag (h) waarde wordt gebruikt voor deze Numerieke Dimensie. Het wordt gebouwd op het pingel geconditioneerde niveau dat cs-uri-vraag (a) "1"aanpast. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Snel controleren geslaagd</b> </td> 
   <td colname="col2"> Dit is een Eenvoudige dimensie die van de cs-uri-vraag (g) waarde wordt gebouwd die op het pingniveau wordt gebouwd. Het wordt gebruikt om de snelle metrische controle te berekenen. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Realtime verwerkingspercentage</b> </td> 
   <td colname="col2"> Numerieke afmetingen die de cs-uri-query(t) waarde gebruiken die op het pingniveau wordt gebouwd. Er is een voorwaarde dat cs-uri-query(a) overeenkomt met "1". </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Bron: Furthest Behind</b> </td> 
   <td colname="col2"> Eenvoudige Afmeting die van de waarde van cs-uri-query (bl) wordt gebouwd die op het pingniveau wordt gebouwd. Deze afmeting toont wanneer het laatste contact met een gegevensbron voorkwam. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Temperatuur DB-ruimtepercentage</b> </td> 
   <td colname="col2">De numerieke Dimensie die gebruikend de cs-uri-vraag (een) waarde wordt gebouwd, die op het Ping niveau wordt gebouwd. Het wordt geconditioneerd dat cs-uri-vraag (k) niet leeg is, en cs-uri-vraag (a) past "1"aan. Het wordt gebruikt om het percentage te berekenen van de gebruikte ruimte van DB van Temp op een bepaalde server. <p>Opmerking:  Deze afmeting is verborgen omdat het slechts nuttig wanneer gemiddeld in metrisch is. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Transformatiepercentage</b> </td> 
   <td colname="col2">de cs-uri-vraag (bf) waarde wordt gebruikt voor deze numerieke dimensie. Het wordt gebouwd op het pingniveau. Deze dimensie wordt gebruikt om het percentage van volledige gegevenstransformatie te berekenen. <p><p>Opmerking:  Deze afmeting is verborgen omdat het slechts nuttig wanneer gemiddeld in metrisch is. </p></p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Versie gegevenswerkbank</b> </td> 
   <td colname="col2"> De cs-uri-vraag (ab) waarde wordt gebruikt voor deze Eenvoudige Dimensie. Het wordt gebouwd op het pingniveau en op voorwaarde dat cs-uri-query(ab) niet leeg is, en cs-uri-query(a) "1"aanpast. Dit toont de versie(s) van de server van de gegevenswerkbank die op elke server loopt. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Gegevenswerkbankversie Belangrijk</b> </td> 
   <td colname="col2"> De cs-uri-vraag (ab) waarde is verdeeld en de belangrijkste versiewaarde wordt gekopieerd in het x-inzicht-versie-belangrijkste gebied. Het is een Eenvoudige Dimensie die op het pingniveau wordt gebouwd en wordt geconditioneerd dat x-inzicht-versie-belangrijk niet leeg is, en cs-uri-vraag (a) past "1"aan. </td> 
  </tr> 
 </tbody> 
</table>

<!-- <a id="section_76D8A4B07BB947558EBED1123EA203D5"></a> -->

