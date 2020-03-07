---
description: Een denormale dimensie heeft een één-op-één verhouding met zijn ouder telbare dimensie.
solution: Analytics
title: Denormale Afmetingen
topic: Data workbench
uuid: f172fbce-e967-41ce-9958-9062561ecbcc
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Denormale Afmetingen{#denormal-dimensions}

Een denormale dimensie heeft een één-op-één verhouding met zijn ouder telbare dimensie.

U zou een denormale dimensie bepalen wanneer de gewenste dimensie een uniek element voor elk element van zijn ouder bevat. Bijvoorbeeld, [!DNL EMail Address] is een denormale afmeting met een ouder van Bezoeker. Elke bezoeker heeft een e-mailadres, en elk element in de dimensie van het Adres EMail is het e-mailadres van één enkele bezoeker. Zelfs als twee bezoekers het zelfde e-mailadres hebben, zijn de adressen verschillende elementen van de dimensie van het Adres EMail.

U kunt denormale afmetingen in om het even welke lijstvisualisatie, in detaillijsten gebruiken, of filters tot stand brengen. Bovendien kunt u denormale afmetingen met de het segmentuitvoer van de server van de gegevenswerkbank van de het segmentuitvoer aan de uitvoerwaarden van gebieden (zoals [!DNL Tracking ID] of [!DNL EMail Address]) gebruiken die heel wat waarden hebben. Omdat om het even welke segmentgegevens die u wilt uitvoeren als afmeting binnen het profiel moet worden bepaald, moet u een denormale afmeting tot stand brengen die de ruwe koorden van de gegevens van het gebied opslaat.

>[!NOTE]
>
>Wanneer het gebruiken van een denormale afmeting in een lijst of andere visualisatie die een normale afmeting verwacht, wordt een afgeleide denormale afmeting automatisch gecreeerd. De afgeleide denormale dimensie heeft een één-aan-vele verhouding met de ouderdimensie.

Voor informatie over de de visualisatie en filters van de detaillijst, zie het hoofdstuk van de Visualisaties van de Analyse in de Gids *van de Gebruiker van de Werkbank van* Gegevens. Voor informatie over de segmentuitvoer, zie het het Vormen hoofdstuk van de Eigenschappen van de Interface en van de Analyse in de Gids van de Gebruiker van de Werkbank van *Gegevens*.

>[!NOTE]
>
>De formele afmetingen kunnen in vraagtijd en schijfruimte zeer duur zijn. Een denormale afmeting met ouder [!DNL Page View]en een 50 byte gemiddelde inputkoord kon 25 GB van gegevens aan de buffers in een typische, grote dataset, gelijkwaardig aan ongeveer 13 eenvoudige of numerieke dimensies van de paginamening, of ongeveer 125 zittingsniveauafmetingen toevoegen. Voeg nooit een denormale dimensie aan een dataset zonder een zorgvuldige evaluatie van het prestatieseffect toe.

De theoretische afmetingen worden bepaald door de volgende parameters:

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
   <td colname="col2"> Beschrijvende naam van de afmeting aangezien het in gegevenswerkbank verschijnt. De afmetingsnaam kan geen koppelteken (-) omvatten. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Opmerkingen </td> 
   <td colname="col2"> Optioneel. Opmerkingen over de uitgebreide dimensie. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Toestand </td> 
   <td colname="col2"> De voorwaarden waaronder de verhouding tussen de Ouder en de waarde van het inputgebied zou moeten worden gecreeerd. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Verborgen </td> 
   <td colname="col2"> Bepaalt of de afmeting in de interface van de gegevenswerkbank verschijnt. Door gebrek, wordt deze parameter geplaatst aan vals. Als, bijvoorbeeld, de afmeting slechts als basis van metrisch moet worden gebruikt, kunt u deze parameter aan waar plaatsen om de afmeting van de vertoning van de gegevenswerkbank te verbergen. </td> 
   <td colname="col3"> waar </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Invoer </td> 
   <td colname="col2"> De waarde die met de ouderdimensie (Ouder) verwant is. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Genormaliseerde elementen </td> 
   <td colname="col2"> Een prestaties het stemmen parameter die het aantal afmetingselementen specificeert de waarvan namen in systeemgeheugen moeten worden opgeslagen. Het plaatsen van deze parameter aan een hogere waarde veroorzaakt een denormale afmeting om meer RAM te gebruiken maar resulteert in snellere vragen. De standaardwaarde is 16383. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Exploitatie </td> 
   <td colname="col2"> <p>De beschikbare verrichtingen zijn als volgt: </p> <p> 
     <ul id="ul_CCDC45838A3941BD949B6D21EA0492B3"> 
      <li id="li_F33898192A82437692B5C15684EFCF64"> EERSTE NONBLANK: De eerste niet-lege inputwaarde wordt gebruikt, ongeacht of het uit de eerste logboekingang komt. Als de <span class="wintitle"> Input</span> een vectorgebied is, wordt de eerste rij in de vector voor de relevante logboekingang gebruikt. </li> 
      <li id="li_4ADD0A368BB74B64AD29126C8E7B333F"> EERSTE RIJ: De waarde voor de eerste logboekingang met betrekking tot het element van de ouderafmeting wordt gebruikt, zelfs als de input leeg is. Als de <span class="wintitle"> Input</span> een vectorgebied is, wordt de eerste rij in de vector voor de relevante logboekingang gebruikt. Als deze waarde leeg is of geen aantal, of als de relevante logboekingang niet aan de Voorwaarde van de afmeting voldoet, wordt geen waarde gebruikt. </li> 
      <li id="li_C93CA22ADA634F21A6488BB3BEE7CB23"> LAATSTE NONBLANK: De laatste niet-lege inputwaarde wordt gebruikt, ongeacht of het uit de laatste logboekingang komt. Als de <span class="wintitle"> Input</span> een vectorgebied is, wordt de eerste rij in de vector voor de relevante logboekingang gebruikt. </li> 
      <li id="li_2FFE585521B14FE5ABBF66AAC47F22C4"> LAATSTE RIJ: De waarde voor de laatste logboekingang met betrekking tot het element van de ouderafmeting wordt gebruikt, zelfs als de input leeg is. Als de <span class="wintitle"> Input</span> een vectorgebied is, wordt de eerste rij in de vector voor de relevante logboekingang gebruikt. Als deze waarde leeg is of geen aantal, of als de relevante logboekingang niet aan de Voorwaarde van de afmeting voldoet, wordt geen waarde gebruikt. </li> 
     </ul> </p> <p> <p>Opmerking:  Als de Verrichting geen waarde oplevert, wordt een lege waarde ("") gebruikt. </p> </p> <p> U zou een verrichting moeten specificeren om ervoor te zorgen dat de afmeting zoals bedoeld wordt bepaald. </p> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Ouder </td> 
   <td colname="col2"> De naam van de ouderafmeting. Om het even welke telbare afmeting kan een ouderafmeting zijn. </td> 
   <td colname="col3"> </td> 
  </tr> 
 </tbody> 
</table>

De denormale afmeting die in dit voorbeeld wordt getoond neemt alle gegevens in het gebied x-trackingid als input en omvat het in een afmeting genoemd identiteitskaart van de Bezoeker. Voor een segment van bezoekers dat u hebt gecreeerd, kunt u de gegevens in de dimensie van identiteitskaart van de Bezoeker (evenals een andere bepaalde dimensie) uitvoeren.

![](assets/cfg_Transformation_Dim_Denormal.png)

