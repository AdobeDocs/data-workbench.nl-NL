---
description: De metriek kan worden uitgegeven gebruikend de Hoofdmetrische Redacteur en in de folder van Metriek van een profiel worden bewaard.
solution: Analytics
title: Syntaxis voor metrische uitdrukkingen
topic: Data workbench
uuid: 801e265d-d7e4-4f0f-9698-d0b50dd00995
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Syntaxis voor metrische uitdrukkingen{#syntax-for-metric-expressions}

De metriek kan worden uitgegeven gebruikend de Hoofdmetrische Redacteur en in de folder van Metriek van een profiel worden bewaard.

Voor meer informatie, zie het [Creëren van en het Uitgeven van Voortgekomen Metriek](../../../home/c-get-started/c-admin-intrf/c-prof-mgr/c-drvd-mtrcs.md#concept-e41723b342a849309874b26232224a40). De metrische uitdrukkingen kunnen ook in aantekenvellen worden gebruikt. Voor meer informatie, zie [Aantekenvellen](../../../home/c-get-started/c-analysis-vis/c-wksts/c-wksts.md#concept-45b50aafc4d84709841f14aee8022581). De volgende syntaxis wordt gebruikt om metrische uitdrukkingen te bepalen.

Opmerkingen:

1. De onderstreepte woorden zouden in de uitdrukkingstekst letterlijk moeten zijn ingegaan.
1. De vorm {TEKST}? vertegenwoordigt facultatieve tekst.
1. De vorm {TEXT}* vertegenwoordigt tekst die nul of meer tijden kan voorkomen.
1. De vorm {A| B| C|...} vertegenwoordigt tekst die uit precies één van de bepaalde opties bestaat, zoals A of B of C....
1. Het formulier [A,B] vertegenwoordigt een reeks getallen, van A tot maar zonder B.

<table id="table_A6CA9C9F396448209398AA2A369E63FA"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Identificator </p> </td> 
   <td colname="col2"> <p>Een herkenningstekenverwijzingen genoemd metrisch. Voor de regels inzake juridische identificatoren, zie <a href="../../../home/c-get-started/c-qry-lang-syntx/c-syntx-id.md#concept-735fa36fc49643269b3646aaaa8f2fa8"> Syntax for Identifiers </a>. </p> <p>Voorbeeld: Opbrengsten = Totaal_Prijs </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>(metrisch) </p> </td> 
   <td colname="col2"> <p>Het resultaat van (Metrisch) is het zelfde als het resultaat van Metrisch. De haakjes specificeren de orde van verrichtingen in een uitdrukking. </p> <p>Voorbeeld: Gemiddelde = (A + B) / 2 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>A + B </p> </td> 
   <td colname="col2"> <p>Som van de resultaten van metrisch A en metrisch B. </p> <p>Voorbeeld: Waarde = Opbrengsten + Kosten_Besparingen </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>A - B </p> </td> 
   <td colname="col2"> <p>Verschil tussen de resultaten van metrisch A en metrisch B. </p> <p>Voorbeeld: Winst = Opbrengsten - Kosten </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>A * B </p> </td> 
   <td colname="col2"> <p>Product verkregen door de resultaten van metrisch A en metrisch B. </p> <p>Voorbeeld: Dollar = Centen * 0,01 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>A/B </p> </td> 
   <td colname="col2"> <p>Verhouding tussen de resultaten van metrisch A en metrisch B. </p> <p>Voorbeeld: Revenue_per_Session = Opbrengsten / Sessies </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>A ^ B </p> </td> 
   <td colname="col2"> <p>Resultaat van metrische A verhoogd tot het vermogen van het resultaat van metrische B. </p> <p>Voorbeeld: Gebied = Breedte^2 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>betrouwbaarheid (metrisch) </p> </td> 
   <td colname="col2"> <p>Een schatting van de standaardafwijking van de metrische waarde. Dit wordt berekend met behulp van een bemonsteringstechniek die bekend staat als het aanjagen van een darm. </p> <p>Dit metrisch is geheugen-intensief en zou niet in grote lijsten moeten worden gebruikt. </p> <p>Om deze syntaxis te gebruiken, moet u een jackknife dimensie (genoemd "jackknife") met de aangewezen eigenschappen hebben. Voor meer informatie, contacteer de Raadplegende Diensten van Adobe. </p> <p>Voorbeeld: vertrouwen (Average_Score) </p> <p> <p>Opmerking:  De vertrouwen metrische types, met inbegrip van vertrouwen (metrisch) en vertrouwen (metrisch, jacknife), zijn vooral nuttig wanneer het gebruiken van de gecontroleerde experimenteerfunctionaliteit van Adobe. Als een metrisch sprong van 12% aan 16% tijdens een gecontroleerd experiment, kon u een betrouwbaarheidscallout gebruiken om de kansen te berekenen dat de sprong aan willekeurige variatie toe te schrijven was. Dit kan u helpen voorkomen dat u de verkeerde conclusies trekt uit beperkt bewijsmateriaal en, omgekeerd, de verzekering geven dat een twijfelachtige verandering in werkelijkheid is. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>betrouwbaarheidsinterval (metrisch, jaknife) </p> </td> 
   <td colname="col2"> <p>Een schatting van de standaardafwijking van de metrische waarde. Dit wordt berekend met behulp van een bemonsteringstechniek die bekend staat als het aanjagen van een darm. Deze syntaxis laat u toe om het vertrouwen van metrisch te bepalen gebruikend een afmeting jackknife genoemd iets buiten "jackknife." </p> <p>Dit metrisch is geheugen-intensief en zou niet in grote lijsten moeten worden gebruikt. </p> <p>Om deze syntaxis te gebruiken, moet u een jackknife dimensie (genoemd iets buiten "jackknife") met de aangewezen eigenschappen hebben. Voor meer informatie, contacteer de Raadplegende Diensten van Adobe. </p> <p>Voorbeeld: betrouwbaarheid (Average_Score, SubSamples) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>eval (CellReference) </p> </td> 
   <td colname="col2"> <p>Behandelt de inhoud van de cel u als metrische uitdrukking van verwijzingen voorziet. Deze syntaxis kan slechts in een aantekenvelvisualisatie worden gebruikt. </p> <p>Voorbeeld: verdamping (B1) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>log (B, X) </p> </td> 
   <td colname="col2"> <p>De wiskundige logaritme functie: Metrisch X is de parameter, en Metrisch B is de basis. </p> <p>Voorbeeld: dB = 20*log(omvang,10) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Metrisch[Filter] </p> </td> 
   <td colname="col2"> <p>"Metrisch bij filter": Een nieuwe metrische die door het bepaalde filter wordt gefiltreerd. </p> <p>Voorbeeld: Jan_Sessions = Sessions[ Month="Jan" ] </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Metrisch naar afmetingen </p> </td> 
   <td colname="col2"> <p>Een metrisch geëvalueerd op het "niveau"van afmeting. Het resultaat van (M door X)[F] (het resultaat van metrische "M door X" geëvalueerd met filter "F") is het resultaat van M[F door X] (het resultaat van metrische "M" geëvalueerd met filter "F door X"). </p> <p>Voorbeeld: AB_Visitors = </p> <p>(Bezoekers op sessie)[Page="A" en Page="B"] = </p> <p>Bezoekers[(Page="A" en Page="B") per sessie] = </p> <p>Het aantal Bezoekers die pagina A en pagina B in de zelfde Zitting bezochten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>nummer </p> </td> 
   <td colname="col2"> <p>Metrisch met een vaste waarde. </p> <p>Voorbeeld: Pi = 3,1415 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>totaal (metrisch) </p> </td> 
   <td colname="col2"> <p>Negeert om het even welke afmeting waarover metrisch wordt geëvalueerd. Metrisch heeft de zelfde waarde voor elk element van die afmeting. </p> <p>Voorbeeld: Pct_of_Visitors = Bezoekers / totaal(Bezoekers) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>alle (metrisch) </p> </td> 
   <td colname="col2"> <p>Negeert filters die op metrisch van toepassing zijn. Metrisch wordt niet beïnvloed door selecties en andere filters. </p> <p>Voorbeeld: Benchmark_Sessions = all( Sessions ) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>totaal (alle (metrisch)) </p> </td> 
   <td colname="col2"> <p>Negeert alle filters en afmetingen. Het heeft de zelfde waarde door een bepaald profiel ongeacht welke filters of afmetingen worden toegepast. </p> <p>Voorbeeld: Dataset_Visitors = totaal (alle (Bezoekers)) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>som (One,Countable_Dimension) </p> </td> 
   <td colname="col2"> <p>Metrisch die de telling van een telbare afmeting zoals Bezoeker of Zitting geeft. </p> <p>Voorbeeld: Bezoekers = som (één, bezoeker) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>som (Numeric_ Dimension, Countable_ Dimension) </p> </td> 
   <td colname="col2"> <p>Metrisch die de som van een numerieke afmeting over een telbare afmeting geeft. De rangschikkende waarden (in tegenstelling tot de geformatteerde waarden) van de elementen van de numerieke dimensie worden gebruikt, zodat moet een schaalfactor vaak op het resultaat worden toegepast. </p> <p>Voorbeeld: Waarde = som (Session_Value, Sessie)*0.01 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>min(A, B) </p> </td> 
   <td colname="col2"> <p>De minste resultaten van metrische A en metrische B. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>max (A, B) </p> </td> 
   <td colname="col2"> <p>De grootste van de resultaten van metrisch A en metrisch B. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>formaat (A, B) </p> </td> 
   <td colname="col2"> <p>Metrisch die aan metrisch A identiek is, behalve gebruikt het de formatterende functie van metrisch B. </p> </td> 
  </tr> 
 </tbody> 
</table>

