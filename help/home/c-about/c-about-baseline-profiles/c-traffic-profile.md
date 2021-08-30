---
description: Het profiel van het Verkeer bevat de volgende metriek om bezoekersverkeer te identificeren.
title: Metrische gegevens verkeersprofiel
uuid: 7dfa18ef-d2cd-44ae-8c56-a0630a9d5cf2
exl-id: 38f191e5-5b30-4fe0-a680-bcb33fe52eca
source-git-commit: 232117a8cacaecf8e5d7fcaccc5290d6297947e5
workflow-type: tm+mt
source-wordcount: '709'
ht-degree: 1%

---

# Metrische gegevens verkeersprofiel{#traffic-profile-metrics}

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
   <td colname="col1"> Geopend </td> 
   <td colname="col2">Formule: <span class="filepath"> Page_Views[no shift(None,Page_View, Session,-1)]</span><p>Niveau: Paginaweergave </p></td> 
   <td colname="col3"> Het aantal sessies dat de site op elke pagina heeft ingevoerd. Deze metrische waarde wordt alleen over de pagina-dimensie geëvalueerd. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Afsluitingsfrequentie </td> 
   <td colname="col2">Formule: <span class="filepath"> Afsluiten/Pagina_Weergaven </span><p>Niveau: Paginaweergave </p></td> 
   <td colname="col3"> Het percentage sessies waarmee de site van elke pagina is afgesloten. Metrische waarde voor Afsluitingssnelheid kan alleen worden geëvalueerd over de afmetingen van de pagina. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Gesloten </td> 
   <td colname="col2">Formule:<span class="filepath"> Page_Views[no shift(None,Page_View, Session,1)] </span><p>Niveau: Paginaweergave </p></td> 
   <td colname="col3"> Het aantal sessies dat de site heeft verlaten vanaf elke pagina. Deze metrische waarde wordt alleen over de pagina-dimensie geëvalueerd. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> LVCI90 </td> 
   <td colname="col2">Formule: <span class="filepath"> (raw(Visitors) - (raw(Visitors) + 0,69)^0,5 * 1,281551 - 1,2269))*(Visitors/raw(Visitors))</span><p>Niveau: Bezoeker </p></td> 
   <td colname="col3"> Een maat voor het laagste aantal mogelijke bezoekers zoals gerapporteerd door Insight. Wiskundig geeft dit het laagste aantal bezoekers met een waarschijnlijkheid van 90% aan. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Duur paginaweergave </td> 
   <td colname="col2"> <p>Formule: <span class="filepath"> som (exact_page_duration, page_view)*0.1/Page_Views[any Exact_Page_Duration]</span></p> <p>Niveau: Paginaweergave </p> </td> 
   <td colname="col3"> De gemiddelde tijdsduur (MM:SS) die aan een bepaalde pagina of een groep pagina's wordt doorgebracht. Deze metrische waarde wordt alleen over de pagina-dimensie geëvalueerd. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Paginaweergaven per sessie </td> 
   <td colname="col2"> <p>Formule: <span class="filepath"> Page_Views/ (Sessies per Page_View) </span></p> <p>Niveau: Sessie </p> </td> 
   <td colname="col3"> Het gemiddelde aantal paginaweergaven in elke sessie met paginaweergaven. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Paginaweergaven </td> 
   <td colname="col2">Formule: <span class="filepath"> sum(One, Page_View)</span><p>Niveau: Paginaweergave </p></td> 
   <td colname="col3"> Het aantal paginaweergaven. Een paginaweergave is een aanvraag voor een gedefinieerde pagina (toegang tot afbeeldingen en andere typen gefilterde inhoud wordt niet geteld). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Pct van paginaweergaven </td> 
   <td colname="col2">Formule: <span class="filepath"> Page_Views/total(Page_Views) </span><p>Niveau: Paginaweergave </p></td> 
   <td colname="col3"> Het percentage van de paginaweergaven. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Pct van sessies </td> 
   <td colname="col2">Formule: <span class="filepath"> Sessies/total(Sessions)</span><p>Niveau: Sessie </p></td> 
   <td colname="col3"> Het percentage sessies. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Pct van bezoekers </td> 
   <td colname="col2">Formule: <span class="filepath"> Bezoekers/totaal(Bezoekers) </span><p>Niveau: Bezoeker </p></td> 
   <td colname="col3"> Het percentage bezoekers. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Door PCT gerefereerde bezoekers </td> 
   <td colname="col2"> <p>Formule: Referred_Visitors/Visitors </p> <p>Niveau: Bezoeker </p> </td> 
   <td colname="col3"> Het percentage bezoekers dat van een andere site naar deze site is verwezen. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Verwezen sessies </td> 
   <td colname="col2"> <p>Formule: <span class="filepath"> Sessies[Referrer&lt;&gt; 'None' en Referrer&lt;&gt;'bookmarks']</span></p> <p>Niveau: Sessie </p> </td> 
   <td colname="col3"> Het aantal sessies dat van een andere site naar deze site is verwezen. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Bezoekers met verwijzing </td> 
   <td colname="col2"> <p>Formule: <span class="filepath"> Bezoekers[Visitor_Referrer&lt;&gt;'None' en Visitor_Referrer&lt;&gt;'book marks']</span></p> <p>Niveau: Bezoeker </p> </td> 
   <td colname="col3"> Het aantal bezoekers dat van een andere site naar deze site is verwezen. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Bewaren </td> 
   <td colname="col2"> <p>Formule: <span class="filepath"> Sessies[shift(Geen,Ses-versie,Bezoeker,1) = ""] / Sessies</span></p> <p>Niveau: Sessie </p> </td> 
   <td colname="col3"> Het percentage sessies dat niet de laatste bezoekerssessies is. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Sessieduur </td> 
   <td colname="col2"> <p>Formule: <span class="filepath"> (som (exact_Page_Duration, Session)*.1/Sessions)[Session_Duration &lt;= '01:00:00']</span></p> <p>Niveau: Sessie </p> </td> 
   <td colname="col3">De gemiddelde tijdsduur (MM:SS) een bezoeker besteedt in een zitting. <p><p>Opmerking: U kunt deze metrisch met de <a href="https://experienceleague.adobe.com/docs/data-workbench/using/client/t-open-ins.html#Segment_Export" format="http" scope="external"> eigenschap van de Uitvoer van het Segment gebruiken </a>. </p></p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> Sessies per paginaweergave </td> 
   <td colname="col2"> <p>Formule: <span class="filepath"> Sessies per Page_View</span></p> <p> Niveau: Sessie </p> </td> 
   <td colname="col3"> Het aantal sessies met een paginaweergave. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Sessies </td> 
   <td colname="col2"> <p>Formule: <span class="filepath"> sum(One, Session)</span></p> <p>Niveau: Sessie </p> </td> 
   <td colname="col3"> Een aantal bezoekerssessies. Een sessie is een periode van activiteit voor één bezoeker van een website. Afzonderlijke sessies voor elke bezoeker worden geïdentificeerd met behulp van cookies, time-outs en andere heuristica. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> SCI80 </td> 
   <td colname="col2"> <p>Formule: <span class="filepath"> betrouwbaarheid(sessies) * 1.281551 / Sessies</span></p> <p>Niveau: Bezoeker </p> </td> 
   <td colname="col3"> Een maat voor het vertrouwen van de metrische waarde van de sessies zoals gerapporteerd door de gegevenswerkbank. Het is wiskundig een percentage van +/- dat de waaier specificeert waarbinnen het daadwerkelijke antwoord 80% van de tijd zal liggen. Een verdubbeling van het GCB80-percentage geeft als regel dat het antwoord 99% van de tijd zal bedragen. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> UVCI90 </td> 
   <td colname="col2"> <p>Formule: <span class="filepath"> ((raw(Visitors) + 0,68)^0,5 * 1,281551 + 1,2269) + raw(Visitors))*(Visitors/raw(Visitors))</span></p> <p>Niveau: Bezoeker </p> </td> 
   <td colname="col3"> Een maat voor het hoogst mogelijke aantal bezoekers zoals gerapporteerd door Insight. Wiskundig geeft dit het hoogste aantal bezoekers met een waarschijnlijkheid van 90% aan. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> VCI80 </td> 
   <td colname="col2">Formule: <span class="filepath"> (raw(Visitors) + .68)^0,5 * 1.281551 + 1.2269) / raw(Visitors)</span><p>Niveau: Bezoeker </p></td> 
   <td colname="col3"> Een maat voor het vertrouwen van de metrische waarde van de bezoekers, zoals gerapporteerd door Insight. Het is wiskundig een percentage van +/- dat de waaier specificeert waarbinnen het daadwerkelijke antwoord 80% van de tijd zal liggen. Een verdubbeling van het VCI80-percentage geeft als regel dat het antwoord 99% van de tijd zal bedragen. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Bezoekers op basis van paginaweergave </td> 
   <td colname="col2"> <p>Formule: <span class="filepath"> Bezoekers door Page_View</span></p> <p>Niveau: Paginaweergave </p> </td> 
   <td colname="col3"> Het aantal bezoekers met een paginaweergave. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Bezoekers per sessie </td> 
   <td colname="col2"> <p>Formule: <span class="filepath"> Bezoekers per sessie </span></p> <p>Niveau: Sessie </p> </td> 
   <td colname="col3"> Het aantal bezoekers dat een sessie heeft gehad. </td> 
  </tr> 
 </tbody> 
</table>
