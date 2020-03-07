---
description: De uitdrukkingen van de afmeting worden nooit gebruikt alleen, maar kunnen overal worden gebruikt een afmeting wordt gevraagd in een metrische of filteruitdrukking.
solution: Analytics
title: Syntaxis voor dimensies expressies
topic: Data workbench
uuid: c437cc52-4eb3-4202-a0b4-e23889f9c8a2
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Syntaxis voor dimensies expressies{#syntax-for-dimension-expressions}

De uitdrukkingen van de afmeting worden nooit gebruikt alleen, maar kunnen overal worden gebruikt een afmeting wordt gevraagd in een metrische of filteruitdrukking.

1. De onderstreepte woorden zouden in de uitdrukkingstekst letterlijk moeten zijn ingegaan.
1. De vorm {TEKST}? vertegenwoordigt facultatieve tekst.
1. De vorm {TEXT}* vertegenwoordigt tekst die nul of meer tijden kan voorkomen.
1. De vorm {A| B| C|...} vertegenwoordigt tekst die uit precies één van de bepaalde opties bestaat, zoals A of B of C....
1. Het formulier [A,B] vertegenwoordigt een reeks getallen, van A tot maar zonder B.

<table id="table_2D9AE1E2397843C284E838330370A1EE"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Identificator </p> </td> 
   <td colname="col2"> <p>Een herkenningstekenverwijzingen een genoemde dimensie. Voor de regels inzake juridische identificatoren, zie <a href="../../../home/c-get-started/c-qry-lang-syntx/c-syntx-id.md#concept-735fa36fc49643269b3646aaaa8f2fa8"> Syntax for Identifiers </a>. </p> <p>Voorbeeld: Sessions[ Session_Number = "1" ] is het aantal sessies met een sessienummer van "1." Het Aantal van de zitting is een genoemde dimensie die door herkenningsteken van verwijzingen wordt voorzien. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>(Dimension) </p> </td> 
   <td colname="col2"> <p>Het resultaat van (Dimension) is hetzelfde als het resultaat van Dimension. De haakjes specificeren de orde van verrichtingen in een uitdrukking. </p> <p>Voorbeeld: Sessions[ (Pagina) = "/home" ] is het aantal sessies dat de pagina "/home" bezoekt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Dim op Niveau </p> </td> 
   <td colname="col2"> <p>Bepaalt een afmeting die de zelfde elementen heeft zoals de afmetingMom, maar met betrekking tot andere afmetingen door het afmetingsniveau. </p> <p>Specifiek, heeft een element van de nieuwe dimensie op de zelfde elementen van niveau betrekking zoals het zelfde element van Duim, en heeft op die elementen van een andere dimensie betrekking die op om het even welke elementen van niveau betrekking hebben. </p> <p>Voorbeeld: Zittingen[ (Pagina door Bezoeker)="/home"] is het aantal Zittingen van Bezoekers die de Pagina "/home" bezochten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>verschuiving (Dim, Niveau, Groep, N) </p> </td> 
   <td colname="col2"> <p>Bepaalt een afmeting die de zelfde elementen heeft zoals afmeting Dim. Het tiende element van het afmetingsniveau heeft betrekking op hetzelfde element van de nieuwe dimensie als het element Dim dat verband houdt met het e+Nth-element van Niveau, op voorwaarde dat de eth- en e+Nth-elementen van niveau betrekking hebben op hetzelfde element van de afmetingsgroep. </p> <p>Voorbeeld: Page_Views[ shift(Page, Page_View, Session, 1)="/home"] is het aantal paginaweergaven waarvoor de volgende pagina die in dezelfde sessie wordt weergegeven, "/home" is. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>volgende (Dim, Niveau, Groep, N) </p> </td> 
   <td colname="col2"> <p>Gelijkaardig aan verschuiving (Dim, Niveau, Groep, N), behalve dat als er lege waarden in de afmeting zijn, worden zij overgeslagen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>segment (Niveau {, Koord-&gt;Filter}*) </p> </td> 
   <td colname="col2"> <p> Bepaalt een dimensie die elementen van Niveau classificeert die op een lijst van filters wordt gebaseerd. De elementen van de nieuwe dimensie zijn de koorden die als argumenten worden gegeven. Elk element van Niveau heeft op het 1ste element van de segmentdimensie betrekking de waarvan filter het element van Niveau toelaat. Dit is gelijkaardig aan de segmentvisualisatie. </p> <p>Voorbeeld: segmentatie (Bezoeker, "One-Time Visitors" -&gt; Visitor_Sessions = 1, "Zeer Koninklijke Bezoekers" -&gt; Visitor_Sessions &gt; 10, "Iedereen anders" -&gt; Waar) creëert een dimensie die bezoekers in drie groepen indeelt — Eenmalige Bezoekers zijn bezoekers met slechts één sessie, Zeer verlichte Bezoekers zijn bezoekers met meer dan tien sessies, en Alle andere bezoekers hebben een waarde van "Iedereen Else." </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>emmer (Niveau, Metrisch, Telling, Formaat {, Begin {, Grootte}? }?) </p> </td> 
   <td colname="col2"> <p>Bepaalt een afmeting waarvan de elementen waaiers van aantallen (van vaste grootte, b.v. [0-9] zijn, [10-19],...). De elementen van Niveau hebben op het element van de emmer dim betrekking de waarvan waaier de waarde van Metrisch voor dat element van niveau bevat. Het formaat is het printf formaatkoord dat wordt gebruikt om de elementen van Metrisch te formatteren. </p> <p>Voorbeeld: Als Page_Duration_Minutes een de mening-vlakke afmeting is van de Pagina die het aantal notulen vertegenwoordigt die aan elke pagina worden doorgebracht, dan is de emmer (Zitting, som (Page_Duration_Minutes, Page_View), 100, "%0.0f notulen", 0, 5) een zitting-vlakke afmeting die het aantal notulen vertegenwoordigt dat in elke Zitting wordt doorgebracht; de elementen zijn 5 minuten intervallen {[0-5), [5-10),...,[495-500)}. </p> <p>Het begin is de beginnende waarde van het eerste interval (gebrek: 0) en de Grootte is de grootte van het interval (gebrek: 1). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>prefix(Niveau {,ElementName-&gt;(Prefix{,Prefix} * )} * ) </p> </td> 
   <td colname="col2"> <p>Bepaalt een afmeting de waarvan elementen de bepaalde koorden ElementName zijn en met de overeenkomstige reeksen koorden van de Prefix worden geassocieerd. De elementen van Niveau hebben op het element van de prefixomslag betrekking, die met de langste prefix wordt geassocieerd die door de naam van het bepaalde element van niveau wordt aangepast. Voorvoegsels die eindigen met het speciale teken '$' moeten exact worden aangepast. </p> <p>Bijvoorbeeld, de prefix (URI, "Producten" -&gt; ("/producten/"), "Diensten" -&gt; ("/services/", "/producten/service/"), "Garanties" -&gt; ("/products/warranty.html$", "/services/warranty.html$", "Alles anders" -&gt; ("/")) creeert een dimensie die URIs in de vier vermelde categorieën classificeert. Het effect op diverse pagina's is als volgt: </p> <p>/products/warranty.html gaat naar garantie, omdat het precies overeenkomt met het prefix /products/warranty.html$. </p> <p>/products/cars/specialcar.html Komt in Producten, aangezien het /products/prefix aanpast en niet meer prefix </p> <p>/products/service/something.html Gaat in de Diensten, aangezien het /products/service/ prefix aanpast die langer is dan de /products/ prefix. </p> <p>/companyinfo/aboutus.html gaat in de categorie "Alles anders", aangezien de enige prefix die het aanpast "/" is. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>latentie (Niveau, Klem, Duim, Filter, Maxbefore, MaxAfter, FormatString) </p> </td> 
   <td colname="col2"> <p>Zie <a href="../../../home/c-get-started/c-intf-anlys-ftrs/c-config-ltcy-tbls/t-create-ltncy-dims.md#task-6d46ea8c89a047318d9c71bf105ef64a"> Latentieafmetingen maken </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>cartesian_product (Separator {, Dim} *) </p> </td> 
   <td colname="col2"> <p>Bepaalt een afmeting de waarvan elementen alle combinaties ("het cartesiaanse product") van de elementen van de gegeven afmetingen zijn. De naam van elk element wordt gemaakt uit de aaneenschakeling van de overeenkomstige elementen in de inputafmetingen, die door het bepaalde koord van de Scheider worden gescheiden. </p> <p>Bijvoorbeeld, als de afmeting D1 elementen {"a", "b"} heeft en de afmeting D2 de elementen {"x", "y"} heeft, dan heeft het cartesiaanse product ("-", D1, D2) de elementen {"a-x", "a-y", "b-x", "b-y"}. </p> <p>Merk op dat intern, elk van de inputafmetingen wordt behandeld alsof het aantal zijn elementen het volgende hogere vermogen van twee is. Dit leidt ertoe dat het cartesiaanse product enkele dummy elementen bevat. Wanneer het gebruiken van de Werkbank API van Gegevens, afhankelijk van het outputformaat, kunnen deze elementen worden begaan, of zij kunnen als "#nnn"worden getoond, waar nnn de rangschikking van het element is (en door de cliënt zou moeten worden genegeerd). </p> <p>Bijvoorbeeld, in het voorbeeld hierboven, als D2 de drie elementen had {"x", "y", "z"}, zou het worden behandeld alsof het vier elementen had, en het cartesiaanse product de elementen {"a-x", "a-y", "a-z", "#3", "b-x", "b-y", "b-z", "#7"} zou hebben. </p> <p>Als geen afmetingen worden gegeven, is het resultaat een afmeting met één element, "#0", dat aan niets afmeting gelijkwaardig is. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>meest dichtbijgelegen_teltable (Duim) </p> </td> 
   <td colname="col2"> <p>Verwijst naar een reeds bestaande dimensie: de dichtstbijzijnde telbare voorouder van Mam in het schema. Bijvoorbeeld, is de meest dichtbijgelegen telbare (URI) identiek aan Page_View. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>genormaliseerd (Dim, Telling) </p> </td> 
   <td colname="col2"> <p>Bepaalt een genormaliseerde afmeting van de denormale afmetingAfwijking, met tot de elementen van de Telling. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>last_n (Dim, TimeMetric, FormatString, Telling, Compensatie, TrimToData {, WeekStart}?) </p> </td> 
   <td colname="col2"> <p>Bepaalt een afmeting die een ondergroep van de elementen van de afmetingMam heeft, de waarvan elementen plakken van tijd vertegenwoordigen — bijvoorbeeld, dagen, weken, of jaren. </p> <p>De ondergroep is een waaier rond een gespecificeerde tijd, de waarde van constante metrische TimeMetric, die als tijdwaarde in seconden sinds middernacht UTC van 1 Januari, 1970 wordt geïnterpreteerd. De waaier heeft de elementen van de Telling, het laatst waarvan elementen van de Compensatie na het bepaalde element van de Mam is de waarvan naam het resultaat van het formatteren van de waarde van metrisch met het bepaalde koord FormatString is. FormatString gebruikt zelfde % ontsnapt zoals de standaardC bibliotheekfunctie strftime. </p> <p>Als trimToData waar is dan worden om het even welke elementen aan het begin van de resulterende afmeting, die vóór het begin van Duim zou zijn, verwijderd. Wanneer het vals is, zal er altijd het nauwkeurige aantal elementen zijn die door Telling worden gespecificeerd. Merk op dat er altijd elementen aan het eind van de resulterende afmeting kunnen zijn die niet eigenlijk in Duik zijn. </p> <p>De facultatieve WeekStart, indien gespecificeerd, moet één van {"Zon", "Mon", "Tue", "Wed", "Thu", "Fri", "Zat"} zijn. Het wijzigt TimeMetric door het terug naar het meest recente voorkomen van die weekdag te verplaatsen. </p> <p>Voorbeeld: Indien de elementen van de week { "10/03/10", "10/10/10", ..., "12/12/10"} en de ingebouwde as Of Metrisch de waarde hebben 1292348109 (die een tijd in het midden van 14 december vertegenwoordigen) 10), dan laatste n (Week, As_Of, "%m/%d/%y", 4, 0, vals, "Zon") bepaalt de afmeting met elementen {"12/12/10", "12/19/10", "12/23/10", "12/30/10}" ... </p> <p>Voorbeeld 2: Als de Weekdimensie alleen elementen heeft {"12/19/10", "12/26/10", ..., "01/30/11"}, en de as van metrisch is zoals hierboven, dan geeft de laatste n(Week, As_Of, "%m/%d/%y", 4, 0, waar, "Zon") dimensie met elementen {"12/19/10", "12/23/10", "12/30/10"}. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>days_of_previ_month(Dim, TimeMetric, FormatString, nMonths, includeThisMonth, TrimToData) </p> </td> 
   <td colname="col2"> <p>Bepaalt een afmeting die een ondergroep van de elementen van Duim heeft, de waarvan elementen dagen vertegenwoordigen. De ondergroep is een waaier rond een gespecificeerde tijd, de waarde van constante metrische TimeMetric, die als tijdwaarde in seconden sinds middernacht UTC van 1 Januari, 1970 wordt geïnterpreteerd. De waaier zal de elementen omvatten die aan elke dag in de maanden voorafgaand aan de gespecificeerde tijd beantwoorden. Als includeThisMonth waar is, omvat de waaier ook elke dag van de maand die de gespecificeerde tijd bevat. </p> <p>FormatString specificeert het formatteren van de elementen van Duim, gebruikend "%"ontsnapt zoals in de standaardC bibliotheekfunctie strftime. </p> <p>Als trimToData waar is dan worden om het even welke elementen aan het begin van de resulterende afmeting, die vóór het begin van Duim zou zijn, verwijderd. Wanneer het vals is, zal er altijd het nauwkeurige aantal elementen zijn die door Telling worden gespecificeerd. Merk op dat er altijd elementen aan het eind van de resulterende afmeting kunnen zijn die niet eigenlijk in Duik zijn. </p> <p>Voorbeeld: Als Dag de elementen {"01/01/10", "01/02/10", ..., "12/31/10"} en de ingebouwde as van metrisch heeft de waarde 1292348109 (die een tijd in het midden van 14 december vertegenwoordigen) 10), dan zullen de dagen van vorige maanden (Dag, As_Of, "%m/%d/%y", 2, vals, vals) elementen hebben {"10/01/10", "10/02/10", ..., "11/30/10"}. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>days_of_current_month (Dim, TimeMetric, FormatString, allMonth, trimToData) </p> </td> 
   <td colname="col2"> <p>Gelijkaardig aan dagen van vorige maanden, behalve beantwoorden de elementen slechts aan dagen van de zelfde maand zoals de tijd die door TimeMetric wordt gespecificeerd. Als alle Maand waar is, zal er een element voor elke dag van de aangewezen maand zijn; anders zullen slechts dagen vanaf de eerste van de desbetreffende maand tot en met de dag die de aangegeven tijd bevat, deel uitmaken van de dimensie. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>days_of_future_month(Dim, TimeMetric, FormatString, nMonths, includeThisMonth, TrimToData) </p> </td> 
   <td colname="col2"> <p>Vergelijkbaar met dagen van vorige maanden, behalve dat de elementen aan de dagen van maanden na, eerder dan vóór, de maand beantwoorden die de tijd door TimeMetric wordt gespecificeerd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>uren_of_day (Dim, Metrisch, TimeFormatString, nDaysForward, TrimData) </p> </td> 
   <td colname="col2"> <p>Bepaalt een afmeting die een ondergroep van de elementen van Duim heeft, de waarvan elementen uren vertegenwoordigen. De ondergroep is een waaier rond een gespecificeerde tijd, de waarde van constante metrische TimeMetric, die als tijdwaarde in seconden sinds middernacht UTC van 1 Januari, 1970 wordt geïnterpreteerd. De waaier omvat de elementen die aan elk uur van de dag nDaysForward na de dag beantwoorden die de tijd bevat die door TimeMetric wordt gespecificeerd. </p> <p>FormatString specificeert het formatteren van de elementen van Duim, gebruikend "%"ontsnapt zoals in de standaardC bibliotheekfunctie strftime. Het formaatkoord zou altijd output een koord moeten vertegenwoordigen dat middernacht aan het begin van de dag van de tijd vertegenwoordigt binnen overging. </p> <p>Als trimToData waar is dan worden om het even welke elementen aan het begin van de resulterende afmeting, die vóór het begin van Duim zou zijn, verwijderd. Wanneer het vals is, zal er altijd het nauwkeurige aantal elementen zijn die door Telling worden gespecificeerd. Merk op dat er altijd elementen aan het eind van de resulterende afmeting kunnen zijn die niet eigenlijk in Duik zijn. </p> <p>Voorbeeld: Als het Uur de elementen {"01/01/10 00:00"heeft, "01/01/10 01:00", ..., "12/31/10 23:00"}, en de ingebouwde Vanaf metrisch heeft waarde 1292348 109 (wat een tijd in het midden van 14 december 2010 vertegenwoordigt), toen uren van dag (Uur, As_Of, "%x 00:00", 0, vals) bevat elementen { "12/12/10 00:00", "12/12/10 01:0" , ..., "12/12/10 23:00" }. </p> </td> 
  </tr> 
 </tbody> 
</table>

