---
description: Een denormale dimensie heeft een één-op-één verhouding met zijn oudertelbare dimensie.
title: Denormale Dimension
uuid: f172fbce-e967-41ce-9958-9062561ecbcc
exl-id: 0c4fad38-bc7c-4b63-98ec-c9121e576a36
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '790'
ht-degree: 0%

---

# Denormale Dimension{#denormal-dimensions}

Een denormale dimensie heeft een één-op-één verhouding met zijn oudertelbare dimensie.

U zou een denormale afmeting bepalen wanneer de gewenste afmeting een uniek element voor elk element van zijn ouder bevat. [!DNL EMail Address] is bijvoorbeeld een denormale dimensie met een bovenliggend item van Visitor. Elke bezoeker heeft een e-mailadres en elk element in de e-mailadresdimensie is het e-mailadres van één bezoeker. Zelfs als twee bezoekers hetzelfde e-mailadres hebben, zijn de adressen verschillende elementen van de dimensie E-mailadres.

U kunt denormale afmetingen gebruiken in elke tabelvisualisatie, in gedetailleerde tabellen of om filters te maken. Daarnaast kunt u denormale afmetingen gebruiken met de functionaliteit voor het exporteren van segmenten van de gegevenswerkbank-server om waarden te exporteren van velden (zoals [!DNL Tracking ID] of [!DNL EMail Address]) met veel waarden. Omdat segmentgegevens die u wilt exporteren, moeten worden gedefinieerd als een dimensie binnen het profiel, moet u een denormale dimensie maken waarin de onbewerkte tekenreeksen van de gegevens van het veld worden opgeslagen.

>[!NOTE]
>
>Wanneer het gebruiken van een denormale afmeting in een lijst of andere visualisatie die een normale afmeting verwacht, wordt een afgeleide ontsporingsafmeting automatisch gecreeerd. De afgeleide denormale dimensie heeft een één-aan-vele verhouding met de ouderdimensie.

Voor informatie over de detail lijstvisualisatie en filters, zie het hoofdstuk van de Visualisaties van de Analyse in *de Gids van de Gebruiker van de Data Workbench*. Voor informatie over segmentuitvoer, zie het het Vormen hoofdstuk van de Eigenschappen van de Interface en van de Analyse in *de Gids van de Gebruiker van de Data Workbench*.

>[!NOTE]
>
>Denormale afmetingen kunnen zeer duur in vraagtijd en schijfruimte zijn. Een denormale afmeting met ouder [!DNL Page View]en een 50 byte gemiddelde inputkoord kon 25 GB van gegevens aan de buffers in een typische, grote dataset toevoegen, gelijkwaardig aan ongeveer 13 eenvoudige of numerieke afmetingen van de paginamening, of ongeveer 125 zittingsniveaudimensies. Voeg nooit een denormale dimensie aan een dataset zonder een zorgvuldige evaluatie van het prestatieseffect toe.

De denormale afmetingen worden bepaald door de volgende parameters:

<table id="table_532AD791E39B4CF296FFA1C33FB8302E"> 
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
   <td colname="col1"> Opmerkingen </td> 
   <td colname="col2"> Optioneel. Opmerkingen over de uitgebreide dimensie. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Voorwaarde </td> 
   <td colname="col2"> De voorwaarden waaronder de relatie tussen de bovenliggende waarde en de waarde van het invoerveld moet worden gemaakt. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Verborgen </td> 
   <td colname="col2"> Hiermee wordt bepaald of de dimensie wordt weergegeven in de interface van de gegevenswerkbank. Deze parameter is standaard ingesteld op false. Als de afmeting bijvoorbeeld alleen als basis van een metrische waarde moet worden gebruikt, kunt u deze parameter instellen op true om de afmeting te verbergen in de weergave op de werkbank. </td> 
   <td colname="col3"> true </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Invoer </td> 
   <td colname="col2"> De waarde die gerelateerd is aan de bovenliggende dimensie (parent). </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Genormaliseerde elementen </td> 
   <td colname="col2"> Een prestatie het stemmen parameter die het aantal afmetingselementen specificeert de waarvan namen in het systeemgeheugen moeten worden opgeslagen. Het plaatsen van deze parameter aan een hogere waarde veroorzaakt een denormale dimensie om meer RAM te gebruiken maar in snellere vragen resulteert. De standaardwaarde is 16383. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Bewerking </td> 
   <td colname="col2"> <p>De beschikbare bewerkingen zijn als volgt: </p> <p> 
     <ul id="ul_CCDC45838A3941BD949B6D21EA0492B3"> 
      <li id="li_F33898192A82437692B5C15684EFCF64"> EERSTE NONBLANK: De eerste niet-lege inputwaarde wordt gebruikt, ongeacht of het uit de eerste logboekingang komt. Als <span class="wintitle"> Invoer</span> een vectorgebied is, wordt de eerste rij in de vector voor de relevante logboekingang gebruikt. </li> 
      <li id="li_4ADD0A368BB74B64AD29126C8E7B333F"> EERSTE RIJ: De waarde voor de eerste logbestandvermelding die betrekking heeft op het bovenliggende dimensielement wordt gebruikt, zelfs als de invoer leeg is. Als <span class="wintitle"> Invoer</span> een vectorgebied is, wordt de eerste rij in de vector voor de relevante logboekingang gebruikt. Als deze waarde leeg is of geen getal, of als het relevante logbestandvermelding niet voldoet aan de voorwaarde van de dimensie, wordt geen waarde gebruikt. </li> 
      <li id="li_C93CA22ADA634F21A6488BB3BEE7CB23"> LAATSTE NONBLANK: De laatste niet-lege inputwaarde wordt gebruikt, ongeacht of het uit de laatste logboekingang komt. Als <span class="wintitle"> Invoer</span> een vectorgebied is, wordt de eerste rij in de vector voor de relevante logboekingang gebruikt. </li> 
      <li id="li_2FFE585521B14FE5ABBF66AAC47F22C4"> LAATSTE RIJ: De waarde voor de laatste logbestandvermelding die betrekking heeft op het bovenliggende dimensielement wordt gebruikt, zelfs als de invoer leeg is. Als <span class="wintitle"> Invoer</span> een vectorgebied is, wordt de eerste rij in de vector voor de relevante logboekingang gebruikt. Als deze waarde leeg is of geen getal, of als het relevante logbestandvermelding niet voldoet aan de voorwaarde van de dimensie, wordt geen waarde gebruikt. </li> 
     </ul> </p> <p> <p>Opmerking:  Als de Bewerking geen waarde oplevert, wordt een lege waarde ("") gebruikt. </p> </p> <p> Geef een bewerking op om ervoor te zorgen dat de dimensie op de juiste manier wordt gedefinieerd. </p> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Bovenliggend </td> 
   <td colname="col2"> De naam van de bovenliggende dimensie. Elke aftelbare dimensie kan een bovenliggende dimensie zijn. </td> 
   <td colname="col3"> </td> 
  </tr> 
 </tbody> 
</table>

De denormale afmeting die in dit voorbeeld wordt getoond neemt alle gegevens in het gebied x-trackingid als input en omvat het in een afmeting genoemd Bezoeker ID. Voor een segment bezoekers dat u hebt gemaakt, kunt u de gegevens in de dimensie Bezoeker-id (en elke andere gedefinieerde dimensie) exporteren.

![](assets/cfg_Transformation_Dim_Denormal.png)
