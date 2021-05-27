---
description: De volgende afmetingen zijn beschikbaar voor gebruik in de gegevenswerkbank Historisch profiel.
title: Dimension in het historisch profiel van de Data Workbench
uuid: 6d93fba4-986b-46a4-9479-aeb54853dff5
exl-id: 9df1f317-a985-4132-b32e-f2263e0c23b2
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '1698'
ht-degree: 0%

---

# Dimension in het historisch profiel van de Data Workbench{#dimensions-in-the-data-workbench-historic-profile}

De volgende afmetingen zijn beschikbaar voor gebruik in de gegevenswerkbank Historisch profiel.

## Dimension in het historisch profiel van de Data Workbench {#section-96f1b64f5cb84411b630f97f227d888d}

De volgende afmetingen zijn beschikbaar voor gebruik in de gegevenswerkbank Historisch profiel.

<table id="table_3EAEA68E73BE431D841F7F2E83EDD6AC"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <b>Blok</b> </td> 
   <td colname="col2">Dit is het enige telbare in deze configuratie, is het de wortel voor alle dimensies. Een blok kan als een server worden beschouwd. Het veld x-trackingid wordt gebruikt. <p>Opmerking:  De blok-id is een hash van de servernaam plus de hostnaam. Er zal dus ongeveer één blok per server per profiel zijn. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Ping</b> </td> 
   <td colname="col2"> Dit is een aftelbare afmeting die van het Blok tellende wordt gebouwd. Elke rij gegevens in het profiel is pingelen van de controleagent. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Waarschuwing kritiek</b> </td> 
   <td colname="col2"> Numerieke Dimension die is opgebouwd op basis van de waarde cs-uri-query(ad). Het wordt gebouwd op het pingniveau geconditioneerd dat cs-uri-query(a) "1"aanpast. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Waarschuwing omlaag</b> </td> 
   <td colname="col2"> Numerieke Dimension die is opgebouwd uit de waarde cs-uri-query(ac). Het wordt gebouwd op het pingniveau, die dat cs-uri-query(a) "1"aanpast. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Waarschuwingswaarschuwing</b> </td> 
   <td colname="col2"> Numerieke Dimension die is opgebouwd uit de waarde cs-uri-query(ae). Het wordt gebouwd op het pingniveau geconditioneerd dat cs-uri-query(a) "1"aanpast. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Alle profielen opnieuw verwerken</b> </td> 
   <td colname="col2"> Numerieke Dimension die is opgebouwd uit de waarde cs-uri-query(aa). Het wordt gebouwd op het pingniveau geconditioneerd dat cs-uri-query(a) "1"aanpast en cs-uriquery (k) niet leeg is. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Vertraging minuten</b> </td> 
   <td colname="col2"> cs-uri-query(bi) wordt in het veld x-as-of-delay-minutes geplaatst en afgerond naar de dichtstbijzijnde minuut. Het wordt gebouwd op het pingniveau geconditioneerd dat cs-uri-query(a) "1"aanpast. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Percentage capaciteitsrij</b> </td> 
   <td colname="col2"> Numerieke Dimension die is opgebouwd uit de waarde cs-uri-query(r). Het wordt gebouwd op het pingniveau geconditioneerd dat cs-uri-query(a) "1"aanpast en cs-uriquery (k) niet leeg is. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Percentage capaciteitsgrootte</b> </td> 
   <td colname="col2"> Numerieke Dimension die is opgebouwd uit de waarde cs-uri-query(n). Het wordt gebouwd op het pingniveau geconditioneerd dat cs-uri-query(a) "1"aanpast en cs-uriquery (k) niet leeg is. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Componentcontrole voltooid</b> </td> 
   <td colname="col2"> Eenvoudige Dimension die is opgebouwd uit de waarde cs-uri-query(v). Het wordt gebouwd bij het Pingel niveau, en voorwaardelijk dat cs-uri-query(a) "1"aanpast. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Componenten in fout</b> </td> 
   <td colname="col2"> cs-uri-query(ao) wordt gesplitst door het scheidingsteken "|" en gekopieerd naar het veld x-components-in-error. Vele aan Vele Dimension die van het x-componenten-in-fout gebied wordt gebouwd. Gemaakt op pingniveau. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Gedetailleerde controle seconden</b> </td> 
   <td colname="col2"> Numerieke Dimension die is opgebouwd uit de waarde cs-uri-query(l). Het wordt gebouwd op het pingniveau geconditioneerd dat cs-uri-query (k) niet leeg is. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Gedetailleerde controle voltooid</b> </td> 
   <td colname="col2"> Eenvoudige Dimension die is opgebouwd uit de waarde cs-uri-query(k). Het wordt gebouwd op het pingniveau geconditioneerd dat cs-uri-query(a) "1"aanpast. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Dimension GigaBytes</b> </td> 
   <td colname="col2"> cs-uri-query(bc) wordt gekopieerd naar het veld x-dimensie-gigabytes. Het veld x-dimensie-gigabytes is gebruiker voor deze eenvoudige Dimension, op voorwaarde dat cs-uri-query(a) met "2" overeenkomt. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Percentage gebruikte schijf "x"</b> </td> 
   <td colname="col2"> Deze numerieke Dimension worden geconfigureerd op basis van de waarden voor cs-uri-query(ah, ai, aj, ak, al). Zij worden gebouwd op het pingniveau en op cs-uri-query(a) de gelijken "1"en cs-uri-query (k) worden geconditioneerd is niet leeg. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Geschatte wiepper dekaseconds</b> </td> 
   <td colname="col2"> Het veld x-estimated-sweep-dekaseconds wordt gebruikt in deze numerieke Dimension. Dit is de geschatte controletijd van de servers gedeeld door tien (verminderde resolutie van vegen meting om dimensie redelijker te maken). <p>Opmerking:  Deze dimensie is verborgen omdat het alleen nuttig is wanneer het gemiddelde in een metrische waarde wordt genomen. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Snelle invoer MegaBytes per minuut</b> </td> 
   <td colname="col2"> De waarde cs-uri-query(bj) wordt gebruikt voor deze dimensie. De laatste rij voor een blok wordt gebruikt als waarde voor de dimensie. Als de dataset Snelle Input deze Numerieke minieme waarde in zal tonen MB per waarbij het systeem gegevens invoert. <p>Opmerking:  Deze dimensie is verborgen omdat het alleen nuttig is wanneer het gemiddelde in een metrische waarde wordt genomen. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Snel MegaBytes samenvoegen per minuut</b> </td> 
   <td colname="col2">De waarde cs-uri-query(bk) wordt gebruikt voor deze dimensie. De laatste rij voor een blok wordt gebruikt als waarde voor de dimensie. Als de dataset Deze Numerieke waarde van de Fusie in Snelle is zal de MB per minuut tonen waarbij het systeem samenvoegt. <p><p>Opmerking:  Deze dimensie is verborgen omdat het alleen nuttig is wanneer het gemiddelde in een metrische waarde wordt genomen. </p></p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Veld GigaBytes</b> </td> 
   <td colname="col2">De waarde cs-uri-query(bg) wordt gebruikt voor deze dimensie. De waarde wordt gedeeld door 1000 en afgerond naar het dichtstbijzijnde gehele getal. Deze numerieke Dimension zal de hoeveelheid ruimte tonen de Gebieden in de dataset gebruiken. <p>Opmerking:  Deze dimensie is verborgen omdat het alleen nuttig is wanneer het gemiddelde in een metrische waarde wordt genomen. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Groep</b> </td> 
   <td colname="col2"> Eenvoudige Dimension die op pingniveau van cs-uri-query(x) waarde wordt gebouwd. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Host</b> </td> 
   <td colname="col2"> De waarde cs-uri-query(b) wordt gebruikt voor deze dimensie. De waarde van de eenvoudige dimensie is de Laatste Rij voor een Blok. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Laatste pingel</b> </td> 
   <td colname="col2"> het x-unixtime gebied wordt gekopieerd in x-last-pingelt en door 10 gedeeld om de kardinaliteit te verminderen. De numerieke Dimension wordt gebouwd op het niveau van het Blok en gebruikt x-last-pingelt gebied. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Gemiddelde belasting</b> </td> 
   <td colname="col2"> Dit is een Numerieke dimensie die de Laatste Rij voor de waarde van cs-uri-query(i) van een bepaalde Server gebruikt. De voorwaarde is dat cs-uri-query(k) niet leeg is. Deze dimensie wordt gebruikt om de gemiddelde lading op de servers in het systeem te berekenen die worden gecontroleerd. <p><p>Opmerking:  Deze dimensie is verborgen omdat het alleen nuttig is wanneer het gemiddelde in een metrische waarde wordt genomen. </p></p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Percentage voor logarittering</b> </td> 
   <td colname="col2">De waarde cs-uri-query(be) wordt gebruikt voor deze numerieke dimensie, die op pingniveau wordt gebouwd. Deze afmeting wordt gebruikt om het percentage logboeken te berekenen die worden gelezen. <p>Opmerking:  Deze dimensie is verborgen omdat het alleen nuttig is wanneer het gemiddelde in een metrische waarde wordt genomen. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Percentage geheugenpaginabestand</b> </td> 
   <td colname="col2"> Dit is een Numerieke dimensie die cs-uri-vraag (o) waarde gebruikt, die op het Pingniveau wordt gebouwd. De voorwaarde is dat cs-uri-query(k) niet leeg is en dat cs-uri-query(a) overeenkomt met "1". Deze dimensie wordt gebruikt om het percentage van het geheugengebruik van het paginadossier te berekenen. <p>Opmerking:  Deze dimensie is verborgen omdat het alleen nuttig is wanneer het gemiddelde in een metrische waarde wordt genomen. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Totaal aantal fysieke MegaBytes-geheugen</b> </td> 
   <td colname="col2">Dit is een Numerieke dimensie die de cs-uri-vraag (ag) waarde gebruikt, die op het Pingniveau wordt gebouwd. De methode is afhankelijk van cs-uri-query(k) die niet leeg is en van cs-uri-query(a) die overeenkomt met "1. <p>Opmerking:  Deze dimensie is verborgen omdat het alleen nuttig is wanneer het gemiddelde in een metrische waarde wordt genomen. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Fysiek percentage geheugen</b> </td> 
   <td colname="col2">Dit is een Numerieke dimensie die de cs-uri-vraag (ag) waarde gebruikt, die op het Pingniveau wordt gebouwd. De methode is afhankelijk van cs-uri-query(k) die niet leeg is en van cs-uri-query(a) die overeenkomt met "1. Deze dimensie wordt gebruikt om het percentage van fysiek geheugengebruik van elke Server te berekenen. <p>Opmerking:  Deze dimensie is verborgen omdat het alleen nuttig is wanneer het gemiddelde in een metrische waarde wordt genomen. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Percentage geheugenquery</b> </td> 
   <td colname="col2"> Dit is een numerieke dimensie die de cs-uri-vraag(s) waarde op pingniveau gebruikt. De voorwaarde is dat cs-uri-query(k) niet leeg is en dat cs-uri-query(a) overeenkomt met "1. Deze afmeting wordt gebruikt om het percentage van het gebruik van het vraaggeheugen van elke Server te berekenen. <p>Opmerking:  Deze dimensie is verborgen omdat het alleen nuttig is wanneer het gemiddelde in een metrische waarde wordt genomen. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Netwerkverbindingen</b> </td> 
   <td colname="col2"> Dit is een Numerieke dimensie die de cs-uri-vraag (q) waarde gebruikt die op het Pingniveau wordt gebouwd. De voorwaarde is dat cs-uri-query(k) niet leeg is en dat cs-uri-query(a) overeenkomt met "1. Dit wordt gebruikt om het aantal netwerkverbindingen te tonen er voor een bepaalde server zijn. <p>Opmerking:  Deze dimensie is verborgen omdat het alleen nuttig is wanneer het gemiddelde in een metrische waarde wordt genomen. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Rijen uitvoeren</b> </td> 
   <td colname="col2"> De waarde cs-uri-query(bh) wordt gedeeld door 100000 en gekopieerd naar het veld x-output-rows om de grootte van de dimensie te beperken. X-output-rows wordt gebruikt in een Numeric Dimension die op het Pingniveau wordt gebouwd, die dat cs-uri-query(a) "2"aanpast. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Type pingel-id</b> </td> 
   <td colname="col2"> Eenvoudige Dimension die gebruikend cs-uri-vraag (a) waarde op het Pingniveau wordt gebouwd. Dit toont wat voor soort Ping werd geregistreerd. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Centiseconden opiniepeilingvertraging</b> </td> 
   <td colname="col2">De waarde cs-uri-query(m) wordt gedeeld door 10 om afmeting te verminderen, en gekopieerd in het x-poll-latency-centiseconds gebied. Dit is een Numerieke afmeting die op het pingniveau wordt gebouwd, wordt bepaald dat cs-uri-query (k) niet leeg is, en cs-uri-query(a) past "1"aan/ Deze afmeting wordt gebruikt om de opiniepeilingslatentie te berekenen. <p>Opmerking:  Deze dimensie is verborgen omdat het alleen nuttig is wanneer het gemiddelde in een metrische waarde wordt genomen. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Verwerkingsmodus-id</b> </td> 
   <td colname="col2"> De waarde cs-uri-query(bb) wordt gebruikt voor deze Eenvoudige Dimension, die op pingniveau wordt gebouwd. Het wordt bepaald dat cs-uri-query(bb) niet leeg is, en dat cs-uri-query(a) "2"identiteitskaart van de Wijze van de Verwerking toestaat om te zien welke wijze van verwerking het systeem in (Snelle Invoer, Snelle Fusie, Echte Tijd) is. <p>Opmerking:  Deze dimensie wordt verborgen en vervolgens opnieuw blootgesteld aan vriendelijke waarden in de verwerkingsmodus voor afmetingen aan de clientzijde. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Profiel</b> </td> 
   <td colname="col2"> De cs-uri-query(ba) waarde wordt gebruikt voor deze Eenvoudige Dimension, wordt het gebouwd op pingniveau. Deze dimensie geeft de naam of namen weer van de profielen die momenteel worden gecontroleerd. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Seconden snel controleren</b> </td> 
   <td colname="col2"> De waarde cs-uri-query(h) wordt gebruikt voor deze numerieke Dimension. Het wordt gebouwd op het pingniveau geconditioneerd dat cs-uri-query(a) "1"aanpast. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Snelle controle voltooid</b> </td> 
   <td colname="col2"> Dit is een Eenvoudige afmeting die van de cs-uri-vraag (g) waarde wordt gebouwd die op het Pingsniveau wordt gebouwd. Deze wordt gebruikt om de metrische sneltoets te berekenen. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Processorpercentage in real time</b> </td> 
   <td colname="col2"> Numerieke Dimension die de cs-uri-vraag (t) waarde gebruikt op het Pingsniveau wordt gebouwd. De voorwaarde is dat cs-uri-query(a) overeenkomt met "1". </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Bron verder achter</b> </td> 
   <td colname="col2"> Eenvoudige Dimension die van de cs-uri-vraag (bl) waarde wordt gebouwd op het pingniveau. Deze afmeting toont wanneer het laatste contact met een gegevensbron voorkwam. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Ruimtepercentage tijdelijke database</b> </td> 
   <td colname="col2">Numerieke Dimension die wordt gebouwd gebruikend de cs-uri-vraag (een) waarde, die op het Pingniveau wordt gebouwd. Er is een voorwaarde voor dat cs-uri-query(k) niet leeg is en dat cs-uri-query(a) overeenkomt met "1". Deze wordt gebruikt om het percentage te berekenen van de gebruikte Temp DB-ruimte op een bepaalde server. <p>Opmerking:  Deze dimensie is verborgen omdat het alleen nuttig is wanneer het gemiddelde in een metrische waarde wordt genomen. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Transformatiepercentage</b> </td> 
   <td colname="col2">De waarde cs-uri-query(bf) wordt gebruikt voor deze numerieke dimensie. Het wordt gebouwd op pingniveau. Deze dimensie wordt gebruikt om het percentage van volledige gegevenstransformatie te berekenen. <p><p>Opmerking:  Deze dimensie is verborgen omdat het alleen nuttig is wanneer het gemiddelde in een metrische waarde wordt genomen. </p></p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Versie Data Workbench</b> </td> 
   <td colname="col2"> De waarde cs-uri-query(ab) wordt gebruikt voor deze eenvoudige Dimension. Het wordt gebouwd bij het Pingel niveau en op voorwaarde dat cs-uri-query(ab) niet leeg is, en cs-uri-query(a) past "1"aan. Hierdoor worden de versie(s) van de gegevenswerkbankserver weergegeven die op elke server wordt uitgevoerd. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Hoofdversie van Data Workbench</b> </td> 
   <td colname="col2"> De waarde cs-uri-query(ab) wordt gesplitst en de hoofdreleasewaarde wordt gekopieerd naar het veld x-insight-version-major. Het is een Eenvoudige Dimension die op het Pingel niveau wordt gebouwd en wordt bepaald dat x-insight-version-major niet leeg is, en cs-uri-query(a) past "1"aan. </td> 
  </tr> 
 </tbody> 
</table>

<!-- <a id="section_76D8A4B07BB947558EBED1123EA203D5"></a> -->
