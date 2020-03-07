---
description: Een numerieke dimensie bestaat uit bevolen, numerieke elementen en heeft een één-aan-vele verhouding met zijn ouder telbare dimensie.
solution: Analytics
title: Numerieke afmetingen
topic: Data workbench
uuid: 19fab770-1535-41b2-bad1-811eba5f3575
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Numerieke afmetingen{#numeric-dimensions}

Een numerieke dimensie bestaat uit bevolen, numerieke elementen en heeft een één-aan-vele verhouding met zijn ouder telbare dimensie.

U kunt aan een numerieke dimensie als vertegenwoordiging van de numerieke eigenschappen van de elementen van de ouderdimensie denken. Bijvoorbeeld, als u met Webgegevens werkt, kon u de numerieke Inkomsten van de Afmetingszitting bepalen, die een hoeveelheid opbrengst, in dollars, voor elke zitting in de dimensie van de Zitting bepaalt. Elke zitting heeft één enkel bedrag van bijbehorende opbrengst, maar verscheidene zittingen kunnen de zelfde hoeveelheid bijbehorende opbrengst hebben. Daarom heeft de dimensie van de Opbrengst van de Zitting een één-aan-vele verhouding met de dimensie van de Zitting.

De numerieke afmetingen worden vaak gebruikt om metriek te bepalen die de som waarden, tellingsvoorkomen van een voorwaarde, of van een minimum of maximumwaarde de plaats bepalen. Bijvoorbeeld, zou metrisch genoemd &quot;Opbrengst&quot;kunnen worden bepaald gebruikend de dimensie van de Opbrengst van de Zitting: som (Session_Revenue, Sessie). Gedefinieerd deze manier, zou metrisch de Opbrengst het totale bedrag van opbrengst voor de geselecteerde zittingen geven.

Numerieke afmetingen kunnen geen ouders van andere afmetingen zijn.

De numerieke afmetingen worden bepaald door de volgende parameters:

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
   <td colname="col2"> Beschrijvende naam van de afmeting aangezien het in gegevenswerkbank verschijnt. De afmetingsnaam kan geen koppelteken (-) omvatten. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Knipwaarden </td> 
   <td colname="col2"> Waar of vals. Specificeert of de inputwaarde (na Verrichting) moet worden geknipt om tussen de waarden van Min en Max te zijn. Als de Waarden van de Klem waar zijn, wordt de waarde geknipt aan die waaier. Als de Waarden van de Klem vals zijn, is geen waarde teruggekeerd voor het element van de ouderafmeting. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Opmerkingen </td> 
   <td colname="col2"> Optioneel. Opmerkingen over de uitgebreide dimensie. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Toestand </td> 
   <td colname="col2"> De voorwaarden waaronder het inputgebied tot de verwezenlijking van de numerieke dimensie bijdraagt. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Vaste grootte </td> 
   <td colname="col2"> Waar of vals. Controleert het aantal elementen in een afmeting (kardinaliteit). Als waar, zijn alle elementen van Min aan Max inbegrepen in de afmeting. Als vals, groeit de grootte van de afmeting aangezien de waarden worden toegevoegd. </td> 
   <td colname="col3"> vals </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Verborgen </td> 
   <td colname="col2"> Bepaalt of de afmeting in de interface van de gegevenswerkbank verschijnt. Door gebrek, wordt deze parameter geplaatst aan vals. Als, bijvoorbeeld, de afmeting slechts als basis van metrisch moet worden gebruikt, kunt u deze parameter aan waar plaatsen om de afmeting van de vertoning van de gegevenswerkbank te verbergen. </td> 
   <td colname="col3"> vals </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Invoer </td> 
   <td colname="col2"> <p>De waarde aan gebruik met de gespecificeerde Verrichting of de inputwaarde waarvoor u voorkomen wilt tellen. </p> <p> Als dit gebied een vector van koorden is, komt de evaluatie voor elk element in de vector voor. Zo bijvoorbeeld, voegt een vector met lengte 3 en een Verrichting van TEKST 3 aan de telling toe. </p> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Min </td> 
   <td colname="col2"> Lagere grens op het eindafmetingsresultaat. </td> 
   <td colname="col3"> 0 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Max </td> 
   <td colname="col2"> Bovengrens op het eindafmetingsresultaat. </td> 
   <td colname="col3"> 1e6 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Compensatie </td> 
   <td colname="col2"> Zie Schalen in deze tabel. </td> 
   <td colname="col3"> 0 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Exploitatie </td> 
   <td colname="col2"> <p>De beschikbare verrichtingen zijn als volgt: </p> <p> 
     <ul id="ul_E04733E5E8824A2BAAB90D9356078D99"> 
      <li id="li_CAEE9167D45540BEAC538345F250B509"> TELLING: Het totale aantal nonblank waarden op het gebied van de <span class="wintitle"> Input</span> over alle logboekingangen die aan de Voorwaarde van de afmeting voldoen wordt gebruikt. Als het gebied van de <span class="wintitle"> Input</span> een vectorgebied is, wordt het totale aantal nonblank waarden in elke logboekingang geteld. </li> 
      <li id="li_64A4D671E78642BD9A9334F8098450B9"> EERSTE NONBLANK: De eerste niet-lege inputwaarde wordt gebruikt, ongeacht of het uit de eerste logboekingang komt. Als de <span class="wintitle"> Input</span> een vectorgebied is, wordt de eerste rij in de vector voor de relevante logboekingang gebruikt. Als de waarde geen aantal is, wordt geen waarde gebruikt. </li> 
      <li id="li_C967964729BD4A638FF78D8883CE513F"> EERSTE RIJ: De waarde voor de eerste logboekingang met betrekking tot het element van de ouderafmeting wordt gebruikt, zelfs als de input leeg is. Als de <span class="wintitle"> Input</span> een vectorgebied is, wordt de eerste rij in de vector voor de relevante logboekingang gebruikt. Als deze waarde leeg is of geen aantal, of als de relevante logboekingang niet aan de Voorwaarde van de afmeting voldoet, wordt geen waarde gebruikt. </li> 
      <li id="li_74171B17F480478B8547E1A361B22DA4"> LAATSTE NONBLANK: De laatste niet-lege inputwaarde wordt gebruikt, ongeacht of het uit de laatste logboekingang komt. Als de <span class="wintitle"> Input</span> een vectorgebied is, wordt de eerste rij in de vector voor de relevante logboekingang gebruikt. Als de waarde geen aantal is, wordt geen waarde gebruikt. </li> 
      <li id="li_1253ECF507BD4BBF97CBB2FA12915045"> LAATSTE RIJ: De waarde voor de laatste logboekingang met betrekking tot het element van de ouderafmeting wordt gebruikt, zelfs als de input leeg is. Als de <span class="wintitle"> Input</span> een vectorgebied is, wordt de eerste rij in de vector voor de relevante logboekingang gebruikt. Als deze waarde leeg is of geen aantal, of als de relevante logboekingang niet aan de Voorwaarde van de afmeting voldoet, wordt geen waarde gebruikt. </li> 
      <li id="li_20819E3944544F98853D6A02814F47B2"> SUM: Het totaal van alle numerieke waarden op het gebied van de <span class="wintitle"> Input</span> over alle logboekingangen die aan de Voorwaarde van de afmeting voldoen wordt gebruikt. Als er geen dergelijke logboekingangen of geen numerieke gevonden waarden zijn, wordt de numerieke waarde 0 gebruikt. </li> 
      <li id="li_086C2E57604B4645A9203A984C6F9A04">MIN of MAX: De minimum of maximumnumerieke waarde die op het gebied van de <span class="wintitle"> Input</span> over alle logboekingangen wordt gevonden die de Voorwaarde van de afmeting voldoen wordt gebruikt. Als er geen dergelijke logboekingangen of geen numerieke waarden zijn, wordt geen waarde gebruikt. </li> 
     </ul> </p> <p> <p>Opmerking:  U zou een verrichting moeten specificeren om ervoor te zorgen dat de afmeting zoals bedoeld wordt bepaald. </p> </p> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Ouder </td> 
   <td colname="col2"> De naam van de ouderafmeting. Om het even welke telbare afmeting kan een ouderafmeting zijn. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Schaal </td> 
   <td colname="col2"> <p>Om de normale waarde van de afmeting op te leveren, wordt het resultaat van de bewerking als volgt getransformeerd: </p> <p> (schaal * invoer) + offset </p> </td> 
   <td colname="col3"> 1.0 </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Als [!DNL Operation] geen waarde oplevert, of [!DNL Clip Values] vals is en de waarde niet tussen [!DNL Min] en [!DNL Max]is, is geen element van de numerieke dimensie verwant met het element van de ouderdimensie.

Dit voorbeeld illustreert de definitie van een numerieke dimensie gebruikend gebeurtenisgegevens die van websiteverkeer worden verzameld. Deze numerieke dimensie, genoemd &quot;de Teller van de Mening van de Advertentie,&quot;telt het aantal tijden dat de bezoeker een reclame tijdens een bepaalde zitting ziet. De veronderstelling is dat alle reclame middelen van de Webserver met ad= als deel van cs-uri-vraag worden gevraagd. In het voorbeeld, is het aantal tijden (TELLING) dat de bezoeker met een reclame wordt voorgesteld de waarde van belang, niet de daadwerkelijke waarde op het gebied.

![](assets/cfg_Transformation_Dim_Numeric.png)

