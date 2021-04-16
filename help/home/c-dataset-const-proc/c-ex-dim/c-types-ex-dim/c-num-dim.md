---
description: Een numerieke dimensie bestaat uit geordende, numerieke elementen en heeft een één-op-veel relatie met de bovenliggende telbare dimensie.
title: Numerieke Dimension
uuid: 19fab770-1535-41b2-bad1-811eba5f3575
exl-id: 69a4dfa6-8402-4c2b-8b04-e6e1a0fd5ccb
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '990'
ht-degree: 1%

---

# Numerieke Dimension{#numeric-dimensions}

Een numerieke dimensie bestaat uit geordende, numerieke elementen en heeft een één-op-veel relatie met de bovenliggende telbare dimensie.

U kunt een numerieke dimensie zien als een weergave van de numerieke eigenschappen van de elementen van de bovenliggende dimensie. Als u bijvoorbeeld met webgegevens werkt, kunt u de numerieke dimensie van de sessieopbrengst definiëren. Deze waarde definieert een bedrag aan inkomsten, in dollars, voor elke sessie in de dimensie Sessie. Elke zitting heeft één enkel bedrag van bijbehorende opbrengst, maar verscheidene zittingen kunnen de zelfde hoeveelheid bijbehorende opbrengst hebben. Daarom heeft de dimensie van de Inkomsten van de Zitting één-aan-vele verhouding met de dimensie van de Zitting.

De numerieke afmetingen worden vaak gebruikt om metriek te bepalen die de totale waarden, tellingsvoorkomen van een voorwaarde, of van een minimum of maximumwaarde de plaats bepalen. Een metrische naam met de naam &quot;Opbrengst&quot; kan bijvoorbeeld worden gedefinieerd met behulp van de dimensie Opbrengst sessie: sum(Session_Revenue, Session). Op deze manier wordt het totale bedrag aan inkomsten voor de geselecteerde sessies weergegeven in de maatstaf van de inkomsten.

Numerieke afmetingen kunnen geen bovenliggende elementen van andere dimensies zijn.

De numerieke afmetingen worden gedefinieerd door de volgende parameters:

<table id="table_15B849DD0BFC4D57AD6CF28898901324"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Parameter </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
   <th colname="col3" class="entry"> Standaard </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Naam </td> 
   <td colname="col2"> Beschrijvende naam van de dimensie zoals deze wordt weergegeven in de werkbank voor gegevens. De naam van de dimensie mag geen afbreekstreepje (-) bevatten. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Clipwaarden </td> 
   <td colname="col2"> Waar of onwaar. Geeft aan of de invoerwaarde (na Bewerking) moet worden bijgesneden tussen de waarden Min en Max. Als de Waarden van de Klem waar zijn, wordt de waarde geknipt aan dat waaier. Als de Waarden van de Klem vals zijn, wordt geen waarde teruggekeerd voor het element van de ouderafmeting. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Opmerkingen </td> 
   <td colname="col2"> Optioneel. Opmerkingen over de uitgebreide dimensie. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Voorwaarde </td> 
   <td colname="col2"> De omstandigheden waaronder het invoerveld bijdraagt tot het creëren van de numerieke dimensie. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Vaste grootte </td> 
   <td colname="col2"> Waar of onwaar. Hiermee bepaalt u het aantal elementen in een dimensie (cardinaliteit). Indien waar (true), worden alle elementen van Min. tot Max opgenomen in de dimensie. Indien onwaar, wordt de grootte van de dimensie groter wanneer waarden worden toegevoegd. </td> 
   <td colname="col3"> false </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Verborgen </td> 
   <td colname="col2"> Hiermee wordt bepaald of de dimensie wordt weergegeven in de interface van de gegevenswerkbank. Deze parameter is standaard ingesteld op false. Als de afmeting bijvoorbeeld alleen als basis van een metrische waarde moet worden gebruikt, kunt u deze parameter instellen op true om de afmeting te verbergen in de weergave op de werkbank. </td> 
   <td colname="col3"> false </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Invoer </td> 
   <td colname="col2"> <p>De waarde die moet worden gebruikt met de opgegeven bewerking of de invoerwaarde waarvan u het aantal exemplaren wilt tellen. </p> <p> Als dit veld een vector met tekenreeksen is, vindt de evaluatie plaats voor elk element in de vector. Een vector met lengte 3 en een bewerking van COUNT verhoogt bijvoorbeeld de telling met 3. </p> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Min </td> 
   <td colname="col2"> Lagere limiet voor het uiteindelijke afmetingsresultaat. </td> 
   <td colname="col3"> 0 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Max </td> 
   <td colname="col2"> Bovengrens van het uiteindelijke afmetingsresultaat. </td> 
   <td colname="col3"> 1e6 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Verschuiven </td> 
   <td colname="col2"> Zie Schalen in deze tabel. </td> 
   <td colname="col3"> 0 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Bewerking </td> 
   <td colname="col2"> <p>De beschikbare bewerkingen zijn als volgt: </p> <p> 
     <ul id="ul_E04733E5E8824A2BAAB90D9356078D99"> 
      <li id="li_CAEE9167D45540BEAC538345F250B509"> TELLING: Het totale aantal niet-lege waarden in het <span class="wintitle"> Invoerveld</span> in alle logitems die aan de voorwaarde van de dimensie voldoen, wordt gebruikt. Als het veld <span class="wintitle"> Invoer</span> een vectorveld is, wordt het totale aantal niet-lege waarden in elke logbestandvermelding geteld. </li> 
      <li id="li_64A4D671E78642BD9A9334F8098450B9"> EERSTE NONBLANK: De eerste niet-lege inputwaarde wordt gebruikt, ongeacht of het uit de eerste logboekingang komt. Als <span class="wintitle"> Invoer</span> een vectorgebied is, wordt de eerste rij in de vector voor de relevante logboekingang gebruikt. Wanneer de waarde geen getal is, wordt geen waarde gebruikt. </li> 
      <li id="li_C967964729BD4A638FF78D8883CE513F"> EERSTE RIJ: De waarde voor de eerste logbestandvermelding die betrekking heeft op het bovenliggende dimensielement wordt gebruikt, zelfs als de invoer leeg is. Als <span class="wintitle"> Invoer</span> een vectorgebied is, wordt de eerste rij in de vector voor de relevante logboekingang gebruikt. Als deze waarde leeg is of geen getal, of als het relevante logbestandvermelding niet voldoet aan de voorwaarde van de dimensie, wordt geen waarde gebruikt. </li> 
      <li id="li_74171B17F480478B8547E1A361B22DA4"> LAATSTE NONBLANK: De laatste niet-lege inputwaarde wordt gebruikt, ongeacht of het uit de laatste logboekingang komt. Als <span class="wintitle"> Invoer</span> een vectorgebied is, wordt de eerste rij in de vector voor de relevante logboekingang gebruikt. Wanneer de waarde geen getal is, wordt geen waarde gebruikt. </li> 
      <li id="li_1253ECF507BD4BBF97CBB2FA12915045"> LAATSTE RIJ: De waarde voor de laatste logbestandvermelding die betrekking heeft op het bovenliggende dimensielement wordt gebruikt, zelfs als de invoer leeg is. Als <span class="wintitle"> Invoer</span> een vectorgebied is, wordt de eerste rij in de vector voor de relevante logboekingang gebruikt. Als deze waarde leeg is of geen getal, of als het relevante logbestandvermelding niet voldoet aan de voorwaarde van de dimensie, wordt geen waarde gebruikt. </li> 
      <li id="li_20819E3944544F98853D6A02814F47B2"> SUM: Het totaal van alle numerieke waarden in het veld <span class="wintitle"> Invoer</span> voor alle logitems die aan de voorwaarde van de dimensie voldoen, wordt gebruikt. Als er geen logitems worden gevonden of geen numerieke waarden worden gevonden, wordt de numerieke waarde 0 gebruikt. </li> 
      <li id="li_086C2E57604B4645A9203A984C6F9A04">MIN of MAX: De minimale of maximale numerieke waarde die in het veld <span class="wintitle"> Invoer</span> wordt gevonden voor alle logitems die aan de voorwaarde van de dimensie voldoen, wordt gebruikt. Als er geen logitems of numerieke waarden zijn, wordt geen waarde gebruikt. </li> 
     </ul> </p> <p> <p>Opmerking:  Geef een bewerking op om ervoor te zorgen dat de dimensie op de juiste manier wordt gedefinieerd. </p> </p> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Bovenliggend </td> 
   <td colname="col2"> De naam van de bovenliggende dimensie. Elke aftelbare dimensie kan een bovenliggende dimensie zijn. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Schalen </td> 
   <td colname="col2"> <p>Om de normale waarde van de dimensie te verkrijgen, wordt het resultaat van de bewerking als volgt getransformeerd: </p> <p> (schaal * invoer) + offset </p> </td> 
   <td colname="col3"> 1,0 </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Als [!DNL Operation] geen waarde oplevert, of [!DNL Clip Values] vals is en de waarde niet tussen [!DNL Min] en [!DNL Max] is, is geen element van de numerieke dimensie verwant aan het element van de ouderafmeting.

Dit voorbeeld illustreert de definitie van een numerieke dimensie met behulp van gebeurtenisgegevens die zijn verzameld uit websiteverkeer. Deze numerieke dimensie, genaamd &#39;Teller advertentie-weergave&#39;, telt het aantal keren dat de bezoeker een advertentie ziet tijdens een bepaalde sessie. De veronderstelling is dat alle advertentiemiddelen van de Webserver met ad= als deel van cs-uri-vraag worden gevraagd. In het voorbeeld is het aantal keren (COUNT) dat de bezoeker een advertentie krijgt, de waarde van interesse, niet de werkelijke waarde in het veld.

![](assets/cfg_Transformation_Dim_Numeric.png)
