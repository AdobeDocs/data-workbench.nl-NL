---
description: Het profiel van het Verkeer bevat de volgende metriek om bezoekersverkeer te identificeren.
solution: Analytics
title: Metrische verkeersprofielen
topic: Data workbench
uuid: 7dfa18ef-d2cd-44ae-8c56-a0630a9d5cf2
translation-type: tm+mt
source-git-commit: 2e4991206394ca0c463210990ea44dfb700341a5

---


# Metrische verkeersprofielen{#traffic-profile-metrics}

Het profiel van het Verkeer bevat de volgende metriek om bezoekersverkeer te identificeren.

<table id="table_D981FB9F8B734E3C845A9628548565F1"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Metrisch </th> 
   <th colname="col2" class="entry"> Metrische formule en niveau </th> 
   <th colname="col3" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Ingangen </td> 
   <td colname="col2">Formule: <span class="filepath"> Page_Views[geen verschuiving (niets, Page_View, Zitting,-1)]</span><p>Niveau: Paginaweergave </p></td> 
   <td colname="col3"> Het aantal zittingen dat de plaats op elke pagina inging. Dit metrisch wordt geëvalueerd over de slechts afmeting van de Pagina. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Afloopsnelheid </td> 
   <td colname="col2">Formule: <span class="filepath"> Uitgangen/Page_Views </span><p>Niveau: Paginaweergave </p></td> 
   <td colname="col3"> Het percentage zittingen die de plaats van elke pagina verlieten. Metrisch het Tarief van de Uitgang kan slechts over de paginadimensie worden geëvalueerd. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Afsluiten </td> 
   <td colname="col2">Formule:<span class="filepath"> Page_Views[geen verschuiving (niets, Page_View, Zitting, 1)] </span><p>Niveau: Paginaweergave </p></td> 
   <td colname="col3"> Het aantal zittingen die de plaats van elke pagina verlieten. Dit metrisch wordt geëvalueerd over de slechts afmeting van de Pagina. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> LVCI90 </td> 
   <td colname="col2">Formule: <span class="filepath"> (ruw(Bezoekers) - (ruw(Bezoekers) + 0,69)^0,5 * 1,281551 - 1,2269)*(Bezoekers/ruw(Bezoekers))</span><p>Niveau: Bezoeker </p></td> 
   <td colname="col3"> Een maat voor het laagste aantal mogelijke bezoekers, zoals aangegeven door Insight. Wiskundig gezien geeft het het laagste aantal bezoekers aan met een waarschijnlijkheid van 90%. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Duur paginaweergave </td> 
   <td colname="col2"> <p>Formule: <span class="filepath"> som (exact_page_duration, page_view)*0.1/Page_Views [om het even welke Exact_Page_Duration]</span></p> <p>Niveau: Paginaweergave </p> </td> 
   <td colname="col3"> De gemiddelde tijdsduur (MM.:SS) besteed aan een bepaalde pagina of een groep pagina's. Dit metrisch wordt geëvalueerd over de slechts afmeting van de Pagina. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Pagina-weergaven per sessie </td> 
   <td colname="col2"> <p>Formule: <span class="filepath"> Page_Views/ (Zittingen door Page_View) </span></p> <p>Niveau: Sessie </p> </td> 
   <td colname="col3"> Het gemiddelde aantal paginameningen in elke zitting die paginameningen heeft. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Paginaweergaven </td> 
   <td colname="col2">Formule: <span class="filepath"> som (één, Page_View)</span><p>Niveau: Paginaweergave </p></td> 
   <td colname="col3"> Het aantal paginameningen. Een paginamening is een verzoek om een bepaalde pagina (de toegang tot beelden en andere types van gefiltreerde inhoud worden niet geteld). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Pagina-weergaven </td> 
   <td colname="col2">Formule: <span class="filepath"> Page_Views/totaal(Page_Views) </span><p>Niveau: Paginaweergave </p></td> 
   <td colname="col3"> Het percentage paginameningen. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Pct van de zittingen </td> 
   <td colname="col2">Formule: <span class="filepath"> Zittingen/totaal (sessies)</span><p>Niveau: Sessie </p></td> 
   <td colname="col3"> Het percentage van zittingen. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Gedeelte van bezoekers </td> 
   <td colname="col2">Formule: <span class="filepath"> Bezoekers/totaal(Bezoekers) </span><p>Niveau: Bezoeker </p></td> 
   <td colname="col3"> Het percentage bezoekers. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Pct - Bezoekers </td> 
   <td colname="col2"> <p>Formule: Referred_Visitors/Visitors </p> <p>Niveau: Bezoeker </p> </td> 
   <td colname="col3"> Het percentage bezoekers dat van een andere plaats naar deze plaats werd verwezen. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Verwezen zittingen </td> 
   <td colname="col2"> <p>Formule: <span class="filepath"> Zittingen[Referrer&lt;&gt; 'Geen' en Referrer&lt;&gt;'bookmarks]</span></p> <p>Niveau: Sessie </p> </td> 
   <td colname="col3"> Het aantal zittingen die naar deze plaats van een andere plaats werden doorverwezen. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Bezoekers </td> 
   <td colname="col2"> <p>Formule: <span class="filepath"> Bezoekers[Visitor_ Referrer&lt;&gt;'Geen' en Visitor_Referrer&lt;&gt;'book marks']</span></p> <p>Niveau: Bezoeker </p> </td> 
   <td colname="col3"> Het aantal bezoekers die naar deze plaats van een andere plaats werden doorverwezen. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Bewaring </td> 
   <td colname="col2"> <p>Formule: <span class="filepath"> Sessies[verschuiving (geen, Ses sion, Visitor, 1) = ""] / Sessies</span></p> <p>Niveau: Sessie </p> </td> 
   <td colname="col3"> Het percentage van zittingen die niet de bezoekers zijn laatste zittingen. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Sessieduur </td> 
   <td colname="col2"> <p>Formule: <span class="filepath"> (som (Exact_Page_Duration, Zitting)*.1/Zittingen) [Session_ Duration &lt;= '01:00:00']</span></p> <p>Niveau: Sessie </p> </td> 
   <td colname="col3">De gemiddelde tijdsduur (MM.:SS) een bezoeker doorbrengt in een zitting. <p><p>Opmerking: U kunt dit metrisch met de eigenschap van de Uitvoer <a href="https://docs.adobe.com/content/help/en/data-workbench/using/client/t-open-ins.html#Segment_Export" format="http" scope="external"> van het</a> Segment gebruiken. </p></p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> Zittingen op paginaweergave </td> 
   <td colname="col2"> <p>Formule: <span class="filepath"> Zittingen op Page_View</span></p> <p> Niveau: Sessie </p> </td> 
   <td colname="col3"> Het aantal zittingen die een paginamening hadden. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Zittingen </td> 
   <td colname="col2"> <p>Formule: <span class="filepath"> som (één, sessie)</span></p> <p>Niveau: Sessie </p> </td> 
   <td colname="col3"> Een aantal bezoekerssessies. Een sessie is een periode van activiteit voor één bezoeker van een website. De individuele zittingen voor elke bezoeker worden geïdentificeerd gebruikend koekjes, onderbrekingen, en andere heuristiek. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> SCI80 </td> 
   <td colname="col2"> <p>Formule: <span class="filepath"> Vertrouwen (sessies) * 1.281551 / Zittingen</span></p> <p>Niveau: Bezoeker </p> </td> 
   <td colname="col3"> Een maat van vertrouwen van metrisch Sessies zoals die door de gegevenswerkbank wordt gemeld. Mathematisch, is het een +/- percentage specificerend de waaier waarbinnen het daadwerkelijke antwoord 80% van de tijd zal liggen. Als vuistregel, zal het verdubbelen van het percentage SCI80 een waaier geven waarbinnen het daadwerkelijke antwoord 99% van de tijd zal liggen. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> UVCI90 </td> 
   <td colname="col2"> <p>Formule: <span class="filepath"> ((ruw(Bezoekers) + .68)^0,5 * 1,281551 + 1,2269) + ruw (Bezoekers))*( Bezoekers/ruw(Bezoekers))</span></p> <p>Niveau: Bezoeker </p> </td> 
   <td colname="col3"> Een maat voor het hoogste aantal mogelijke bezoekers, zoals aangegeven door Insight. Wiskundig gezien geeft het het hoogste aantal bezoekers aan met een waarschijnlijkheid van 90%. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> VCI80 </td> 
   <td colname="col2">Formule: <span class="filepath"> (ruw(Bezoekers) + 0,68)^0,5 * 1,281551 + 1,2269) / ruw (Bezoekers)</span><p>Niveau: Bezoeker </p></td> 
   <td colname="col3"> Een maat voor het vertrouwen van de bezoekers metrisch volgens Insight. Mathematisch, is het een +/- percentage specificerend de waaier waarbinnen het daadwerkelijke antwoord 80% van de tijd zal liggen. Als regel-van-duim, zal het verdubbelen van het percentage VCI80 een waaier geven waarbinnen het daadwerkelijke antwoord 99% van de tijd zal liggen. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Bezoekers op paginaweergave </td> 
   <td colname="col2"> <p>Formule: <span class="filepath"> Bezoekers op Page_View</span></p> <p>Niveau: Paginaweergave </p> </td> 
   <td colname="col3"> Het aantal bezoekers dat een paginamening had. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Bezoekers per sessie </td> 
   <td colname="col2"> <p>Formule: <span class="filepath"> Bezoekers per sessie </span></p> <p>Niveau: Sessie </p> </td> 
   <td colname="col3"> Het aantal bezoekers dat een zitting had. </td> 
  </tr> 
 </tbody> 
</table>

