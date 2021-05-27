---
description: Dimension-expressies worden nooit alleen gebruikt, maar kunnen overal worden gebruikt waar een dimensie wordt aangeroepen in een metrische expressie of filterexpressie.
title: Syntaxis voor dimensie-expressies
uuid: c437cc52-4eb3-4202-a0b4-e23889f9c8a2
exl-id: 58609e31-8ad8-418b-9a9f-40462d6443f7
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '1855'
ht-degree: 0%

---

# Syntaxis voor dimensie-expressies{#syntax-for-dimension-expressions}

Dimension-expressies worden nooit alleen gebruikt, maar kunnen overal worden gebruikt waar een dimensie wordt aangeroepen in een metrische expressie of filterexpressie.

1. Onderstreept woorden moeten letterlijk in de expressietekst worden ingevoerd.
1. Het formulier `{TEXT}?` vertegenwoordigt optionele tekst.
1. Het formulier `{TEXT}*` vertegenwoordigt tekst die nul of meer keren kan voorkomen.
1. Het formulier `{A | B | C |...}` vertegenwoordigt tekst die uit exact een van de opgegeven opties bestaat, zoals A, B of C...
1. De vorm `[A,B)` vertegenwoordigt een waaier van aantallen, van A tot maar zonder B.

<table id="table_2D9AE1E2397843C284E838330370A1EE"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Id </p> </td> 
   <td colname="col2"> <p>Een id verwijst naar een benoemde dimensie. Zie <a href="../../../home/c-get-started/c-qry-lang-syntx/c-syntx-id.md#concept-735fa36fc49643269b3646aaaa8f2fa8"> Syntaxis voor id's </a> voor de regels die van toepassing zijn op wettelijke id's. </p> <p>Voorbeeld: Sessies[ Session_Number = "1" ] is het aantal sessies met het sessienummer "1." Sessienummer is een benoemde dimensie waarnaar wordt verwezen door de id. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>(Dimension) </p> </td> 
   <td colname="col2"> <p>Het resultaat van (Dimension) is hetzelfde als het resultaat van Dimension. Haakjes geven de volgorde van bewerkingen in een expressie aan. </p> <p>Voorbeeld: Sessies[ (Pagina) = "/home" ] is het aantal sessies dat de pagina "/home" bezoekt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Verkleinen op niveau </p> </td> 
   <td colname="col2"> <p>Definieert een dimensie met dezelfde elementen als de dimensie Dim, maar die betrekking heeft op andere dimensies door het dimensieniveau. </p> <p>Meer bepaald heeft een element van de nieuwe dimensie betrekking op dezelfde niveauelementen als hetzelfde element van Dim en heeft het betrekking op die elementen van een andere dimensie die betrekking hebben op een van die niveauelementen. </p> <p>Voorbeeld: Sessions[ (Pagina door bezoeker)="/home" ] is het aantal sessies van bezoekers dat de pagina "/home" heeft bezocht. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>shift(Dim,Niveau,Groep,N) </p> </td> 
   <td colname="col2"> <p>Definieert een dimensie met dezelfde elementen als de dimensie Dim. Het twintigste element van het dimensieniveau heeft betrekking op hetzelfde element van de nieuwe dimensie als het element van de demping dat verband houdt met het e+de element van Niveau, op voorwaarde dat de eth- en e+de-de elementen van het niveau betrekking hebben op hetzelfde element van de dimensiegroep. </p> <p>Voorbeeld: Page_Views[ shift(Page, Page_View, Session, 1)="/home" ] is het aantal paginaweergaven waarvoor de volgende pagina die in dezelfde sessie wordt weergegeven, "/home" is. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>next(Dim,Level,Group,N) </p> </td> 
   <td colname="col2"> <p>Vergelijkbaar met shift (Dim,Niveau,Groep,N), behalve dat als er lege waarden in de dimensie zijn, deze worden overgeslagen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>segment(Level {,String-&gt;Filter}*) </p> </td> 
   <td colname="col2"> <p> Definieert een dimensie die elementen van Niveau classificeert op basis van een lijst met filters. De elementen van de nieuwe dimensie zijn de tekenreeksen die als argumenten worden gegeven. Elk element van Niveau heeft betrekking op het eerste element van de segmentdimensie waarvan de filter het element van Niveau toewijst. Dit is gelijkaardig aan segmentvisualisatie. </p> <p>Voorbeeld: segment(Visitor, "One-Time Visitors" -&gt; Visitor_Sessions = 1, "Erg loyale Bezoekers" -&gt; Visitor_Sessions &gt; 10, "Iedereen anders" -&gt; Waar) creëert een dimensie die bezoekers in drie groepen indeelt — Eenmalige Bezoekers zijn bezoekers die slechts één sessie hebben, en wie er meer dan tien sessies heeft, en alle andere bezoekers hebben de waarde "Iedereen anders." </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>bucket(Level, Metric, Count, Format {, Start {, Size}? }?) </p> </td> 
   <td colname="col2"> <p>Definieert een dimensie waarvan de elementen reeksen getallen zijn (van vaste grootte, bijvoorbeeld [0-9], [10-19],...). Elementen van Niveau hebben betrekking op het element van het emmertje waarvan het bereik de waarde van Metrisch voor dat element van niveau bevat. Format is de tekenreeks voor de afdrukindeling die wordt gebruikt om de elementen van Metric op te maken. </p> <p>Voorbeeld: Als Page_Duration_Minutes een pagina mening-vlakke afmeting vertegenwoordigt die het aantal notulen aan elke pagina wordt doorgebracht, dan is emmertje (Zitting, som(Page_Duration_Minutes, Page_View), 100, "%0.0f notulen", 0, 5) een zitting-vlakke afmeting die het aantal notulen vertegenwoordigt dat in elke Zitting wordt doorgebracht; de elementen zijn intervallen van 5 minuten <code>{[0-5), [5-10),...,[495-500)}</code>. </p> <p>Het begin is de beginnende waarde van het eerste interval (gebrek: 0) en Size is de grootte van het interval (gebrek: 1). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>prefix(Level {,ElementName-&gt;(Prefix{,Prefix}* )}* ) </p> </td> 
   <td colname="col2"> <p>Definieert een dimensie waarvan de elementen de opgegeven reeksen ElementName zijn en die zijn gekoppeld aan de corresponderende reeksen van prefix-tekenreeksen. Elementen van Niveau hebben betrekking op het element van het voorvoegsel dim, dat is gekoppeld aan het langste voorvoegsel dat overeenkomt met de naam van het opgegeven element van niveau. Voorvoegsels die eindigen met het speciale teken '$', moeten exact overeenkomen. </p> <p>Met het voorvoegsel (URI, "Products" -&gt; ("/products/"), "Services" -&gt; ("/services/", "/products/service/"), "Warranties" -&gt; ("/products/warranty.html$", "/services/warranty.html$", "All Else" -&gt; ("/") wordt bijvoorbeeld een dimensie gemaakt waarmee URI's in de vier vermelde categorieën worden ingedeeld. Het effect op verschillende pagina's is als volgt: </p> <p>/products/warranty.html gaat naar de garantie, aangezien deze precies overeenkomt met het voorvoegsel /products/warranty.html$. </p> <p>/products/cars/specialcar.html gaat in Producten, aangezien het /products/ prefix en niet meer aanpast </p> <p>/products/service/something.html gaat in de Diensten, aangezien het /products/service/ prefix aanpast die langer is dan het /products/ prefix. </p> <p>/companyinfo/aboutus.html Hiermee gaat u naar de categorie "Alle andere", omdat het enige voorvoegsel dat overeenkomt met "/" is. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>latency (Level, Clip, Dim, Filter, MaxBefore, MaxAfter, FormatString) </p> </td> 
   <td colname="col2"> <p>Zie <a href="../../../home/c-get-started/c-intf-anlys-ftrs/c-config-ltcy-tbls/t-create-ltncy-dims.md#task-6d46ea8c89a047318d9c71bf105ef64a"> Dimension voor latentie maken </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>cartesiaans_product(Scheidingsteken {,Dim}*) </p> </td> 
   <td colname="col2"> <p>Definieert een dimensie waarvan de elementen alle combinaties ("het cartesische product") van de elementen van de opgegeven afmetingen zijn. De naam van elk element is opgebouwd uit de samenvoeging van de corresponderende elementen in de invoerafmetingen, gescheiden door de opgegeven scheidingstekenreeks. </p> <p>Als de dimensie D1 bijvoorbeeld de elementen {"a", "b"} heeft en dimensie D2 de elementen {"x", "y"} heeft, heeft het cartesische product("-", D1, D2) de elementen {"a-x", "a-y", "b-x", "b-y"}. </p> <p>Intern worden alle invoerdimensies behandeld alsof het aantal elementen het eerstvolgende hogere vermogen van twee is. Hierdoor heeft het cartesische product enkele dummy elementen. Wanneer u de Data Workbench-API gebruikt, kunnen deze elementen, afhankelijk van de uitvoerindeling, worden aangeroepen, of worden ze weergegeven als "#nnn", waarbij nnn het rangschikkende element is (en door de client moet worden genegeerd). </p> <p>In het bovenstaande voorbeeld zou, als D2 bijvoorbeeld de drie elementen {"x", "y", "z"} had, het worden behandeld alsof het vier elementen had, en het cartesische product de elementen {"a-x", "a-y", "a-z", "#3", "b-x", "b-y", "b-z" en "#7". </p> <p>Als geen dimensies worden gegeven, is het resultaat een afmeting met één element, "#0", dat aan niets afmeting gelijkwaardig is. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>nearest_countable(Dim) </p> </td> 
   <td colname="col2"> <p>Verwijst naar een reeds bestaande dimensie: de dichtstbijzijnde telbare voorouder van Dim in het schema. De dichtstbijzijnde teller (URI) is bijvoorbeeld gelijk aan Page_View. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>genormaliseerd (grijs, Aantal) </p> </td> 
   <td colname="col2"> <p>Bepaalt een genormaliseerde afmeting van de denormale afmeting Dim, met tot de elementen van de Telling. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>last_n(Dim, TimeMetric, FormatString, Count, Offset, TrimToData {, WeekStart}?) </p> </td> 
   <td colname="col2"> <p>Definieert een dimensie met een subset van de elementen van de dimensie Dim, waarvan de elementen tijdssegmenten vertegenwoordigen, bijvoorbeeld dagen, weken of jaren. </p> <p>De subset is een bereik rond een opgegeven tijd, de waarde van de constante metrische TimeMetric, die wordt geïnterpreteerd als een tijdwaarde in seconden sinds middernacht UTC van 1 januari 1970. De waaier heeft de elementen van de Telling, het laatste waarvan de elementen van de Verschuiving na het bepaalde element van de Mam zijn de waarvan naam het resultaat van het formatteren van de waarde metrisch met het bepaalde koord FormatString is. FormatString gebruikt dezelfde escape % als de standaard C-bibliotheekfunctie strftime. </p> <p>Als trimToData waar is, dan worden om het even welke elementen aan het begin van de resulterende afmeting, die vóór het begin van Duim zou zijn, verwijderd. Wanneer het vals is, zal er altijd het nauwkeurige aantal elementen zijn die door Aantal worden gespecificeerd. Merk op dat er altijd elementen aan het eind van de resulterende afmeting kunnen zijn die eigenlijk niet in Dim zijn. </p> <p>De optionele WeekStart, indien opgegeven, moet een van de volgende waarden hebben: { "Sun", "Mon", "Tue", "Wed", "Thu", "Fri", "Sat" }. Het wijzigt TimeMetric door het terug naar het meest recente voorkomen van die weekdag te bewegen. </p> <p>Voorbeeld: Indien de week de elementen { "10/03/10", "10/10/10", ..., "12/12/10" } en de ingebouwde vanaf metrisch heeft de waarde 1292348109 (die een tijd in het midden van 14 december vertegenwoordigt) 10), last n(Week, As_Of, "%m/%d/%y", 4, 0, false, "Sun") definieert de dimensie met de elementen { "12/12/10", "12/19/10", "12/23/10", "12/30/10" }. </p> <p>Voorbeeld 2: Als de afmetingen van de week alleen de elementen {"12/19/10", "12/26/10", ..., "01/30/11"} en de metrische waarden zoals hierboven zijn, geeft de laatste n(Week, As_Of, "%m/%d/%y", 4, 0, true, "Sun") een dimensie met de elementen {12/19/10", "12/23/10", "12/30/10"}. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>days_of_previous_month(Dim, TimeMetric, FormatString, nMonths, includeThisMonth, TrimToData) </p> </td> 
   <td colname="col2"> <p>Bepaalt een afmeting die een ondergroep van de elementen van Dim heeft, de waarvan elementen dagen vertegenwoordigen. De subset is een bereik rond een opgegeven tijd, de waarde van de constante metrische TimeMetric, die wordt geïnterpreteerd als een tijdwaarde in seconden sinds middernacht UTC van 1 januari 1970. Het bereik bevat de elementen die overeenkomen met elke dag in de maanden voorafgaand aan de opgegeven tijd. Als includeThisMonth waar is, omvat de waaier ook elke dag van de maand die de gespecificeerde tijd bevat. </p> <p>FormatString geeft de opmaak van de elementen van Dim aan, waarbij escape "%" wordt gebruikt, zoals in de standaard C-bibliotheekfunctie strftime. </p> <p>Als trimToData waar is, dan worden om het even welke elementen aan het begin van de resulterende afmeting, die vóór het begin van Duim zou zijn, verwijderd. Wanneer het vals is, zal er altijd het nauwkeurige aantal elementen zijn die door Aantal worden gespecificeerd. Merk op dat er altijd elementen aan het eind van de resulterende afmeting kunnen zijn die eigenlijk niet in Dim zijn. </p> <p>Voorbeeld: Als Dag de elementen { "01/01/10", "01/02/10", ..., "12/31/10" } heeft en ingebouwde als van metrisch heeft de waarde 1292348109 (die een tijd in het midden van 14 december vertegenwoordigt) 10), dan hebben dagen van vorige maanden (Dag, As_Of, "%m/%d/%y", 2, false, false) de elementen { "10/01/10", "10/02/10", ..., "11/30/10" }. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>days_of_current_month(Dim, TimeMetric, FormatString, allMonth, trimToData) </p> </td> 
   <td colname="col2"> <p>Gelijkaardig aan dagen van vorige maanden, behalve beantwoorden de elementen slechts aan dagen van de zelfde maand zoals de tijd die door TimeMetric wordt gespecificeerd. Als alle maanden waar is, zal er een element voor elke dag van de aangewezen maand zijn; anders maken alleen dagen vanaf de eerste van de desbetreffende maand tot en met de dag die de opgegeven tijd bevat, deel uit van de dimensie. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>days_of_future_month(Dim, TimeMetric, FormatString, nMonths, includeThisMonth, TrimToData) </p> </td> 
   <td colname="col2"> <p>Vergelijkbaar met dagen van voorgaande maanden, behalve dat de elementen overeenkomen met de dagen van maanden na, in plaats van vóór, de maand met de tijd die door de TimeMetric wordt gespecificeerd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>hours_of_day(Dim, Metric, TimeFormatString, nDaysForward, TrimData) </p> </td> 
   <td colname="col2"> <p>Definieert een dimensie die een subset van de elementen van Dim heeft, waarvan de elementen uren vertegenwoordigen. De subset is een bereik rond een opgegeven tijd, de waarde van de constante metrische TimeMetric, die wordt geïnterpreteerd als een tijdwaarde in seconden sinds middernacht UTC van 1 januari 1970. De waaier omvat de elementen die aan elk uur van de dag nDaysForward na de dag beantwoorden die de tijd door TimeMetric wordt gespecificeerd. </p> <p>FormatString geeft de opmaak van de elementen van Dim aan, waarbij escape "%" wordt gebruikt, zoals in de standaard C-bibliotheekfunctie strftime. De formaatkoord zou altijd een koord moeten uitvoeren dat middernacht aan het begin van de dag van de overgegaane tijd vertegenwoordigt. </p> <p>Als trimToData waar is, dan worden om het even welke elementen aan het begin van de resulterende afmeting, die vóór het begin van Duim zou zijn, verwijderd. Wanneer het vals is, zal er altijd het nauwkeurige aantal elementen zijn die door Aantal worden gespecificeerd. Merk op dat er altijd elementen aan het eind van de resulterende afmeting kunnen zijn die eigenlijk niet in Dim zijn. </p> <p>Voorbeeld: Als Uur de elementen { "01/01/10 00:00", "01/01/10 01:00", ..., "12/31/10 23:00" } heeft, en de ingebouwde vanaf metrisch heeft de waarde 1292348 109 (voor een tijd halverwege 14 december 2010), dan uren van dag (Uur, As_Of, "%x 00:00", 0, false) heeft elementen { "12/12/10 00:00", "12/12/10 01:0" , ..., "12/12/10 23:00" }. </p> </td> 
  </tr> 
 </tbody> 
</table>
