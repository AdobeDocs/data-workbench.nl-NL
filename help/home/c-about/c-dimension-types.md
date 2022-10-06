---
description: Er zijn verschillende typen dimensies beschikbaar in de gegevenswerkbankserver. Als dusdanig, is het belangrijk om het afmetingstype te kennen wanneer het gebruiken van een afmeting om metriek, filters, of afgeleide dimensies tot stand te brengen.
title: Dimension-typen
uuid: 07659373-8d9b-473d-8daa-ca8e7ac4afe8
exl-id: cbc25504-2c1c-4622-adc1-c9bbac8e12fb
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '754'
ht-degree: 0%

---

# Dimension-typen{#dimension-types}

{{eol}}

Er zijn verschillende typen dimensies beschikbaar in de gegevenswerkbankserver. Als dusdanig, is het belangrijk om het afmetingstype te kennen wanneer het gebruiken van een afmeting om metriek, filters, of afgeleide dimensies tot stand te brengen.

De Server van het inzicht kan de volgende types van afmetingen tot stand brengen en handhaven:

<table id="table_1A79B6C57ED145B6AA3BB05DD37AAD1B"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Dimension-typen </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Tabelachtig </td> 
   <td colname="col2">Een type dimensie waarin het aantal elementen in de dimensie door het systeem kan worden geteld. De telbare afmetingen moeten worden afgeleid van andere aftelbare afmetingen. De tellende afmetingen kunnen ouders van andere dimensies of kinderen van andere telbare afmetingen zijn. <p>Voorbeelden: Bezoeker, Sessie, Paginaweergave, Boek en Volgorde. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> Eenvoudig </td> 
   <td colname="col2">Een dimensie die een één-aan-vele verhouding met een oudertelbare dimensie heeft. Een eenvoudige dimensie kan worden beschouwd als het vertegenwoordigen van een eigenschap van elementen van de bovenliggende dimensie. <p>Voorbeeld: Bezoekerreferentie is een eenvoudige dimensie met een bovenliggend element van de dimensie Bezoeker. Elke bezoeker kan slechts één Visitor Referrer (zijn eerste referentie van HTTP) hebben, maar vele Bezoekers kunnen de zelfde Referrer van de Bezoeker hebben. Daarom is de bezoekersreferentie "één-op-veel" met de dimensie Bezoeker. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> Numeriek </td> 
   <td colname="col2">Een dimensie die geordend, numerieke waarden en een één-op-vele verhouding met een oudertelbare dimensie heeft. Een numerieke dimensie kan worden beschouwd als het vertegenwoordigen van een numerieke eigenschap van elementen van de bovenliggende dimensie. De numerieke afmetingen worden vaak gebruikt om "som"metriek te bepalen. <p>Voorbeeld: De numerieke dimensie van de Ontvangsten van de Zitting bepaalt de opbrengst, in dollars, voor elke Zitting. Elke Zitting heeft één enkel bedrag van opbrengst, maar om het even welk aantal Zittingen zou de zelfde opbrengst kunnen hebben, zodat is de Inkomsten van de Zitting "één-aan-velen"met Zitting. Een metrische "Opbrengst" kan worden gedefinieerd als <span class="filepath"> sum(Session_Revenue, Sessie)</span>, met vermelding van het totale bedrag aan inkomsten voor de geselecteerde sessies. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> Velen-aan-Velen </td> 
   <td colname="col2">Een dimensie die een vele-aan-vele verhouding met een oudertelbare dimensie heeft. Een vele-aan-vele dimensie kan worden gedacht aan als het vertegenwoordigen van een "reeks"van waarden voor elk element van zijn ouderafmeting. Een veel-aan-vele dimensie is gelijkwaardig aan een (anonieme) telbare dimensie met zijn ouder en een Eenvoudige dimensie met een ouder van de anonieme telbare dimensie. <p>Voorbeeld: De veel-aan-vele phrase van het dimensieOnderzoek heeft een ouder van Zitting. Elke sessie kan nul of meer zoektermen gebruiken en een zoekwoordgroep kan in elk aantal sessies worden gebruikt. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> Denormal </td> 
   <td colname="col2">Een dimensie die een één-op-één verhouding met een ouder Countable afmeting heeft. De elementnamen van de denormale dimensie kunnen informatie over de overeenkomstige elementen van de ouderdimensie dragen. Een denormale dimensie kan worden beschouwd als het opslaan van een willekeurige tekenreekswaarde voor elk element van de ouder. De denormale afmetingen kunnen met het segmentuitvoervermogen van de Server van het Inzicht aan outputdetails over een ondergroep of "segment"van een telbare dimensie worden gebruikt. Bovendien kunnen denormale afmetingen worden vermeld in metrische formules en werkbladvisualisaties en kunnen worden gebruikt (met bepaalde beperkingen) om filters te definiëren. <p>Voorbeeld: Het denormale afmeting E-mailadres heeft een ouder van Bezoeker. Elke bezoeker heeft een E-mailadres, en elk element van de dimensie van het E-mailadres wordt geassocieerd met één enkele Bezoeker. Zelfs als twee bezoekers hetzelfde e-mailadres hebben, zijn hun adressen verschillende elementen van de dimensie E-mailadres. Een uitvoer van het Segment kan de dimensie van het Adres E-mail van verwijzingen voorzien om het E-mailadres van elke bezoeker in een Segment uit te voeren. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> Tijd </td> 
   <td colname="col2">Een dimensie waarmee u een set periodieke of absolute lokale tijdafmetingen (zoals Dag, Dag van Week, Uur, Uur van Dag, enzovoort) kunt maken op basis van een tijdstempelveld dat u opgeeft. Wanneer u tijdafmetingen definieert, kunt u ook een andere dag dan maandag kiezen die als het begin van een week moet worden gebruikt door de parameter Begindag week op te geven. <p>Voorbeeld: De tijd van de Sessie van de tijddimensie heeft ouder van Zitting. De dimensie definieert daarom een reeks tijddimensies (Dag, Dag van Week, Uur, Uur van Dag, Maand en Week) waarvan de elementen overeenkomen met de tijd waarop bezoekerssessies op de site zijn begonnen. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> Afgeleid </td> 
   <td colname="col2">Afgeleide afmetingen, eerder dan die in de datasetconfiguratie worden bepaald die op de gegevens wordt gebaseerd die worden verwerkt, worden bepaald in het profiel dat op andere afmetingen of metriek wordt gebaseerd. Vele afgeleide dimensies worden gecreeerd automatisch om verschillende types van visualisaties te drijven. <p>Bijvoorbeeld, wanneer een gebruiker een plaats of proceskaart bouwt, leidt de Server van het Inzicht stil tot een "Voorvoegsel"dimensie. Andere bestanden, zoals de afmetingen van de rapportagetijd, worden gedefinieerd door bestanden in de map Dimension van een profiel. </p></td> 
  </tr> 
 </tbody> 
</table>
