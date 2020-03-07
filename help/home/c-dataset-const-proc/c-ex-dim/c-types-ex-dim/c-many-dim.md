---
description: Een vele-aan-vele dimensie heeft een vele-aan-vele verhouding met zijn ouder telbare dimensie.
solution: Analytics
title: Vele-aan-Vele Afmetingen
topic: Data workbench
uuid: 42c909e8-1228-4210-9406-ffc0d92372fa
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Vele-aan-Vele Afmetingen{#many-to-many-dimensions}

Een vele-aan-vele dimensie heeft een vele-aan-vele verhouding met zijn ouder telbare dimensie.

U kunt aan een vele-aan-vele dimensie als vertegenwoordiging van een reeks waarden voor elk element in zijn ouderafmeting denken. Bijvoorbeeld, is de vele-aan-vele Weg van het afmetingsOnderzoek een zitting-vlakke afmeting (het heeft een ouder van Zitting). Het vertegenwoordigt de reeks onderzoeksuitdrukkingen verbonden aan elke zitting in de dimensie van de Zitting. Één enkele onderzoeksuitdrukking kan in om het even welk aantal zittingen worden gebruikt, en één enkele zitting kan nul of meer onderzoeksuitdrukkingen omvatten. Daarom heeft de dimensie van de Woorden van het Onderzoek een veel-aan-vele verhouding met de dimensie van de Zitting.

Vele-aan-vele dimensies worden bepaald door de volgende parameters:

<table id="table_A6D495008DFF4DD28A3ECD718D775E54"> 
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
   <td colname="col2"> Beschrijvende naam van de afmeting aangezien het aan de gebruiker in gegevenswerkbank verschijnt. De afmetingsnaam kan geen koppelteken (-) omvatten. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Opmerkingen </td> 
   <td colname="col2"> Optioneel. Opmerkingen over de uitgebreide dimensie. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Toestand </td> 
   <td colname="col2"> De voorwaarden waaronder de verhouding tussen de ouder en de waarde van het inputgebied zou moeten worden gecreeerd. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Verborgen </td> 
   <td colname="col2"> Bepaalt of de afmeting in de interface van de gegevenswerkbank verschijnt. Door gebrek, wordt deze parameter geplaatst aan vals. Als, bijvoorbeeld, de afmeting slechts als basis van metrisch moet worden gebruikt, kunt u deze parameter aan waar plaatsen om de afmeting van de vertoning van de gegevenswerkbank te verbergen. </td> 
   <td colname="col3"> vals </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Invoer </td> 
   <td colname="col2"> <p>De waarde die met de ouderdimensie (Ouder) verwant is. Als dit gebied een vector van koorden is, dan heeft elk element van de vector zijn eigen verhouding met de ouder. </p> <p> <p>Opmerking:  Als de inputwaarde voor elke logboekingang voor een element van de ouderdimensie leeg is, zal geen element van de vele-aan-vele dimensie op dat element van de ouderdimensie betrekking hebben. </p> </p> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Ouder </td> 
   <td colname="col2"> De naam van de ouderafmeting. Om het even welke telbare afmeting kan een ouderafmeting zijn. </td> 
   <td colname="col3"> </td> 
  </tr> 
 </tbody> 
</table>

Dit voorbeeld illustreert de definitie van een vele-aan-vele dimensie gebruikend gebeurtenisgegevens die van websiteverkeer worden verzameld. Deze vele-aan-vele dimensie, genoemd &quot;Geselecteerd Product,&quot;heeft zittingen betrekking op de producten die door de bezoeker tijdens die zitting worden gekocht. Het x-productgebied bevat een vector van waarden, elk waarvan met een paginamening wordt geassocieerd, die, beurtelings, met een zitting wordt geassocieerd.

![](assets/cfg_Transformation_Dim_ManytoMany.png)

Door zulk een transformatie tot stand te brengen, kunt u een visualisatie in gegevenswerkbank tot stand brengen die het verband tussen de geselecteerde productdimensie en het aantal zittingen toont die elk van de producten impliceren.
