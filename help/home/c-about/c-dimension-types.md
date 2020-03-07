---
description: Verscheidene types van afmetingen zijn beschikbaar in de server van de gegevenswerkbank. Als dusdanig, is het belangrijk om het afmetingstype te kennen wanneer het gebruiken van een afmeting om metriek, filters, of afgeleide afmetingen tot stand te brengen.
solution: Analytics
title: Afmetingstypen
topic: Data workbench
uuid: 07659373-8d9b-473d-8daa-ca8e7ac4afe8
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Afmetingstypen{#dimension-types}

Verscheidene types van afmetingen zijn beschikbaar in de server van de gegevenswerkbank. Als dusdanig, is het belangrijk om het afmetingstype te kennen wanneer het gebruiken van een afmeting om metriek, filters, of afgeleide afmetingen tot stand te brengen.

De Server van het inzicht kan de volgende soorten afmetingen tot stand brengen en handhaven:

<table id="table_1A79B6C57ED145B6AA3BB05DD37AAD1B"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Afmetingstypen </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Veelzeggend </td> 
   <td colname="col2">Een afmetingstype waarin het aantal elementen in de afmeting door het systeem kan worden geteld. De aftelbare afmetingen moeten worden afgeleid van andere aftelbare afmetingen. Veelzijdige dimensies kunnen ouders van andere dimensies of kinderen van andere aftelbare afmetingen zijn. <p>Voorbeelden: Bezoeker, sessie, paginaweergave, boeken en bestelling. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> Eenvoudig </td> 
   <td colname="col2">Een dimensie die een één-aan-vele verhouding met een ouder telbare dimensie heeft. Een eenvoudige afmeting kan van zoals het vertegenwoordigen van een bezit van elementen van zijn ouderafmeting worden gedacht. <p>Voorbeeld: De Verwijzing van de bezoeker is een eenvoudige afmeting met een ouder van de afmeting van de Bezoeker. Elke bezoeker kan slechts één Referrer van de Bezoeker (hun eerste verwijzing van HTTP) hebben, maar vele Bezoekers zouden de zelfde Referrer van de Bezoeker kunnen hebben. Daarom is de Verwijzing van de Bezoeker "één-aan-velen"met de dimensie van de Bezoeker. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> Numeriek </td> 
   <td colname="col2">Een dimensie die, numerieke waarden en een één-aan-vele verhouding met een ouder telbare dimensie heeft bevolen. Een numerieke dimensie kan van zoals het vertegenwoordigen van een numeriek bezit van elementen van zijn ouderafmeting worden gedacht. De numerieke afmetingen worden vaak gebruikt om "som"metriek te bepalen. <p>Voorbeeld: De numerieke dimensieDe Opbrengst van de Zitting bepaalt de opbrengst, in dollars, voor elke Zitting. Elke Zitting heeft één enkel bedrag van opbrengst, maar om het even welk aantal Zittingen zou de zelfde opbrengst kunnen hebben, zodat is de Opbrengst van de Zitting "één-aan-velen"met Zitting. Een metrische "Opbrengst"zou als <span class="filepath"> som (Session_Revenue, Zitting)</span>kunnen worden bepaald, die het totale bedrag van opbrengst voor de geselecteerde Zittingen geeft. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> Velen-aan-Velen </td> 
   <td colname="col2">Een dimensie die een veel-aan-vele verhouding met een ouder telbare dimensie heeft. Een vele-aan-vele dimensie kan van als het vertegenwoordigen van een "reeks"van waarden voor elk element van zijn ouderdimensie worden gedacht. Een vele-aan-vele dimensie is gelijkwaardig aan een (anonieme) telbare dimensie met zijn ouder en een Eenvoudige dimensie met een ouder van de anonieme telbare dimensie. <p>Voorbeeld: De vele-aan-vele Weg van het afmetingsOnderzoek heeft een ouder van Zitting. Elke Zitting kan nul of meer de Falen van het Onderzoek gebruiken, en een Woorden van het Onderzoek kan in om het even welk aantal Zittingen worden gebruikt. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> Denormal </td> 
   <td colname="col2">Een dimensie die een één-op-één verhouding met een ouderCountable afmeting heeft. De elementennamen van de denormale afmeting kunnen informatie over de overeenkomstige elementen van de ouderafmeting dragen. Een denormale dimensie kan van als het opslaan van een willekeurige koordwaarde voor elk element van de ouder worden gedacht. De theoretische afmetingen kunnen met het vermogen van de het segmentuitvoer van de Server van het Inzicht aan outputdetails over een ondergroep of "segment"van een telbare afmeting worden gebruikt. Bovendien kunnen de denormale afmetingen in metrische formules en aantekenvelvisualisaties worden van verwijzingen voorzien en kunnen (met bepaalde beperkingen) worden gebruikt om filters te bepalen. <p>Voorbeeld: De ontsporingsdimensie van het Adres van EMail heeft een ouder van Bezoeker. Elke bezoeker heeft een Adres EMail, en elk element van de dimensie van het Adres EMail wordt geassocieerd met één enkele Bezoeker. Zelfs als twee bezoekers het zelfde e-mailadres hebben, zullen hun adressen verschillende elementen van de dimensie van het Adres van EMail zijn. Een uitvoer van het Segment kan de dimensie van het Adres EMail aan output van het Adres EMail van elke bezoeker in een Segment van verwijzingen voorzien. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> Tijd </td> 
   <td colname="col2">Een dimensie die u toelaat om een reeks periodieke of absolute lokale tijddimensies (zoals Dag, Dag van Week, Uur, Uur van Dag, etc.) tot stand te brengen die op een timestamp gebied wordt gebaseerd dat u specificeert. Wanneer het bepalen van tijdafmetingen, kunt u ook een dag buiten Maandag kiezen die als begin van een week moet worden gebruikt door de parameter van de Dag van het Begin van de Week te specificeren. <p>Voorbeeld: De tijd van de Zitting van de tijddimensie heeft ouder van Zitting. Daarom bepaalt de dimensie een reeks tijddimensies (Dag, Dag van Week, Uur, Uur van Dag, Maand, en Week) de waarvan elementen aan de tijden beantwoorden waarop de bezoekerszittingen op de plaats begonnen te zijn. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> Afgeleid </td> 
   <td colname="col2">De afgeleide afmetingen, eerder dan die in de datasetconfiguratie worden bepaald die op de gegevens wordt gebaseerd die worden verwerkt, worden bepaald in het profiel dat op andere afmetingen of metriek wordt gebaseerd. Vele afgeleide afmetingen worden gecreeerd automatisch om verschillende soorten visualisaties te drijven. <p>Voorbeeld, wanneer een gebruiker een plaats of een proceskaart bouwt, leidt de Server van het Inzicht tot een "Prefix"dimensie stil. Anderen, zoals de rapporteringstijddimensies, worden bepaald door dossiers in de folder van Afmetingen van een profiel. </p></td> 
  </tr> 
 </tbody> 
</table>

