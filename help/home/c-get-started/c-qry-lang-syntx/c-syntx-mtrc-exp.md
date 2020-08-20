---
description: Metrische gegevens kunnen worden bewerkt met de metrische editor en worden opgeslagen in de map Metriek van een profiel.
solution: Analytics
title: Syntaxis voor metrische expressies
topic: Data workbench
uuid: 801e265d-d7e4-4f0f-9698-d0b50dd00995
translation-type: tm+mt
source-git-commit: a276b16565634fea9b693206c8a55b528fada977
workflow-type: tm+mt
source-wordcount: '851'
ht-degree: 0%

---


# Syntaxis voor metrische expressies{#syntax-for-metric-expressions}

Metrische gegevens kunnen worden bewerkt met de metrische editor en worden opgeslagen in de map Metriek van een profiel.

Voor meer informatie, zie het [Creëren en het Uitgeven Afgeleide Metriek](../../../home/c-get-started/c-admin-intrf/c-prof-mgr/c-drvd-mtrcs.md#concept-e41723b342a849309874b26232224a40). Metrische expressies kunnen ook in werkbladen worden gebruikt. Zie [Werkbladen](../../../home/c-get-started/c-analysis-vis/c-wksts/c-wksts.md#concept-45b50aafc4d84709841f14aee8022581)voor meer informatie. De volgende syntaxis wordt gebruikt om metrische uitdrukkingen te bepalen.

Opmerkingen:

1. Onderstreept woorden moeten letterlijk in de expressietekst worden ingevoerd.
1. Het formulier `{TEXT}?` vertegenwoordigt optionele tekst.
1. Het formulier `{TEXT}*` vertegenwoordigt tekst die nul of meer keren kan voorkomen.
1. Het formulier `{A | B | C |...}` vertegenwoordigt tekst die uit exact een van de opgegeven opties bestaat, zoals A, B of C...
1. Het formulier `[A,B)` vertegenwoordigt een bereik van getallen, van A tot, maar niet inclusief B.

<table id="table_A6CA9C9F396448209398AA2A369E63FA"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Id </p> </td> 
   <td colname="col2"> <p>Een id verwijst naar een benoemde metrische waarde. Zie <a href="../../../home/c-get-started/c-qry-lang-syntx/c-syntx-id.md#concept-735fa36fc49643269b3646aaaa8f2fa8"> Syntaxis voor id's </a>. </p> <p>Voorbeeld: Opbrengst = Totaal_Prijs </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>(metrisch) </p> </td> 
   <td colname="col2"> <p>Het resultaat van (Metrisch) is hetzelfde als het resultaat van Metrisch. Haakjes geven de volgorde van bewerkingen in een expressie aan. </p> <p>Voorbeeld: Gemiddelde = (A + B) / 2 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>A + B </p> </td> 
   <td colname="col2"> <p>Som van de resultaten van metrisch A en metrisch B. </p> <p>Voorbeeld: Waarde = Inkomsten + Kosten_Besparingen </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>A - B </p> </td> 
   <td colname="col2"> <p>Verschil tussen de resultaten van metrisch A en metrisch B. </p> <p>Voorbeeld: Winst = Opbrengst - Kosten </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>A * B </p> </td> 
   <td colname="col2"> <p>Product van de resultaten van metrisch A en metrisch B. </p> <p>Voorbeeld: Dollars = Centen * 0,01 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>A / B </p> </td> 
   <td colname="col2"> <p>Verhouding van de resultaten van metrisch A en metrisch B. </p> <p>Voorbeeld: Revenue_per_Session = Inkomsten/sessies </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>A ^ B </p> </td> 
   <td colname="col2"> <p>Resultaat van metrisch A tot de macht van het resultaat van metrisch B. </p> <p>Voorbeeld: Gebied = Breedte^2 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>betrouwbaarheid (metrisch) </p> </td> 
   <td colname="col2"> <p>Een schatting van de standaardafwijking van de meting. Dit wordt berekend met behulp van een bemonsteringstechniek die bekend staat als jacnifing. </p> <p>Deze metrische waarde is geheugenintensief en mag niet worden gebruikt in grote tabellen. </p> <p>Als u deze syntaxis wilt gebruiken, moet u een jacnife-dimensie (met de naam "jackknife") met de juiste eigenschappen hebben. Neem voor meer informatie contact op met de Adobe Consulting Services. </p> <p>Voorbeeld: Trust(Gemiddelde_Score) </p> <p> <p>Opmerking:  De betrouwbaarheidsmetrische types, met inbegrip van vertrouwen (metrisch) en vertrouwen (metrisch, vechtmachine), zijn vooral nuttig wanneer het gebruiken van de gecontroleerde experimenteringsfunctionaliteit van Adobe. Als een metrische sprong van 12% aan 16% tijdens een gecontroleerd experiment, kon u een betrouwbaarheidsbijschrift gebruiken om de kansen te berekenen die de sprong aan willekeurige variatie toe te schrijven was. Dit kan u helpen voorkomen de verkeerde conclusies te trekken uit beperkt bewijsmateriaal, en omgekeerd de zekerheid te verschaffen dat een twijfelachtige verandering in werkelijkheid is. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>betrouwbaarheid (metrisch, jackrenkend) </p> </td> 
   <td colname="col2"> <p>Een schatting van de standaardafwijking van de meting. Dit wordt berekend met behulp van een bemonsteringstechniek die bekend staat als jacnifing. Deze syntaxis laat u toe om het vertrouwen van metrisch te bepalen gebruikend een afmeting jacknife genoemd iets buiten "jacknife." </p> <p>Deze metrische waarde is geheugenintensief en mag niet worden gebruikt in grote tabellen. </p> <p>Als u deze syntaxis wilt gebruiken, moet u een jacnife dimensie (iets anders dan "jackknife") met de juiste eigenschappen hebben. Neem voor meer informatie contact op met de Adobe Consulting Services. </p> <p>Voorbeeld: betrouwbaarheid (Gemiddelde_Score,Submonsters) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>eval(CellReference) </p> </td> 
   <td colname="col2"> <p>Behandelt de inhoud van de cel waarnaar u verwijst als een metrische expressie. Deze syntaxis kan slechts in een aantekenvelvisualisatie worden gebruikt. </p> <p>Voorbeeld: eval(B1) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>log (B, X) </p> </td> 
   <td colname="col2"> <p>De wiskundige logaritme functie: Metrisch X is de parameter en Metrisch B is de basis. </p> <p>Voorbeeld: dB = 20*log(Amplitude,10) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Metrisch[filter] </p> </td> 
   <td colname="col2"> <p>"Metrisch met filter": Een nieuwe metrische waarde die door het opgegeven filter wordt gefilterd. </p> <p>Voorbeeld: Jan_Sessions = Sessies[ Month="Jan" ] </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Metrisch met Dimension </p> </td> 
   <td colname="col2"> <p>Een metrische waarde die op het "niveau" van de dimensie wordt beoordeeld. Het resultaat van (M bij X)[F] (het resultaat van metrische "M bij X" geëvalueerd met filter "F") is het resultaat van M[F bij X] (het resultaat van metrische "M" geëvalueerd met filter "F bij X"). </p> <p>Voorbeeld: AB_Visitors = </p> <p>(Bezoekers op sessie)[Pagina="A" en Pagina="B"] = </p> <p>Bezoekers[(Page="A" en Page="B") per sessie] = </p> <p>Het aantal bezoekers dat pagina A en pagina B tijdens dezelfde sessie heeft bezocht. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>getal </p> </td> 
   <td colname="col2"> <p>Een metrische waarde met een vaste waarde. </p> <p>Voorbeeld: Pi = 3,1415 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>total(metrisch) </p> </td> 
   <td colname="col2"> <p>Negeert om het even welke afmeting waarover metrisch wordt geëvalueerd. Metrisch heeft de zelfde waarde voor elk element van die afmeting. </p> <p>Voorbeeld: Pct_of_Visitors = Bezoekers / totaal(Bezoekers) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>all (metrisch) </p> </td> 
   <td colname="col2"> <p>Hiermee worden filters genegeerd die op de metrische waarde worden toegepast. De metrische waarde wordt niet beïnvloed door selecties en andere filters. </p> <p>Voorbeeld: Benchmark_Sessions = all( sessies ) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>total(all(Metric)) </p> </td> 
   <td colname="col2"> <p>Hiermee worden alle filters en afmetingen genegeerd. Het heeft in een bepaald profiel dezelfde waarde, ongeacht welke filters of afmetingen worden toegepast. </p> <p>Voorbeeld: Dataset_Visitors = total(all(Visitors)) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>sum(One,Countable_Dimension) </p> </td> 
   <td colname="col2"> <p>Metrisch die de telling van een telbare afmeting zoals Bezoeker of Zitting geeft. </p> <p>Voorbeeld: Bezoekers = som(één,Bezoeker) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>sum(Numeric_ Dimension, Countable_ Dimension) </p> </td> 
   <td colname="col2"> <p>Een metrisch die de som van een numerieke afmeting over een telbare afmeting geeft. De rangtelwoorden (in tegenstelling tot de opgemaakte waarden) van de elementen van de numerieke dimensie worden gebruikt, zodat een schaalfactor vaak op het resultaat moet worden toegepast. </p> <p>Voorbeeld: Waarde = sum(Session_Value, Session)*0.01 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>min(A, B) </p> </td> 
   <td colname="col2"> <p>De laagste resultaten van metrische A en metrische B. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>max(A, B) </p> </td> 
   <td colname="col2"> <p>De grootste van de resultaten van metrisch A en metrisch B. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>formaat (A, B) </p> </td> 
   <td colname="col2"> <p>Een metrische waarde die identiek is aan metrische A, behalve het gebruikt de het formatteren functie van metrisch B. </p> </td> 
  </tr> 
 </tbody> 
</table>

