---
description: De transformatie IPLookup neemt IP geo-plaats of IP geo-inlichtingen gegevens (die door om het even welke verkoper van dergelijke gegevens worden verstrekt en in een merkgebonden formaat door Adobe worden omgezet) en zet de gegevens in geografische informatie om die in analyse kan worden gebruikt.
solution: Analytics
title: IPLookup
topic: Data workbench
uuid: 6fccee39-761f-4854-a7fd-3f8b453e0698
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# IPLookup{#iplookup}

De transformatie IPLookup neemt IP geo-plaats of IP geo-inlichtingen gegevens (die door om het even welke verkoper van dergelijke gegevens worden verstrekt en in een merkgebonden formaat door Adobe worden omgezet) en zet de gegevens in geografische informatie om die in analyse kan worden gebruikt.

Twee [!DNL IPLookup] transformaties zijn vermeld in Add nieuw > *Transformation type *menu:

* [!DNL IPLookup] Quova voor [!DNL IP geo-location] gegevens

* [!DNL IPLookup] Digitale gezant voor [!DNL IP geo-intelligence] gegevens

Wanneer het bepalen van een [!DNL IPLookup] transformatie, kies de aangewezen transformatie voor uw [!DNL IP geo-location] of [!DNL IP geo-intelligence] gegevens.

<table id="table_C438A30AB5E64160A5C486D6887B1D7E"> 
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
   <td colname="col2"> Beschrijvende naam van de transformatie. U kunt om het even welke naam hier ingaan. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Opmerkingen </td> 
   <td colname="col2"> Optioneel. Opmerkingen over de transformatie. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Toestand </td> 
   <td colname="col2"> De omstandigheden waaronder deze transformatie wordt toegepast. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Bestand </td> 
   <td colname="col2"> Weg en dossier - naam van het raadplegingsdossier. De relatieve wegen zijn met betrekking tot de installatiefolder voor de server van de gegevenswerkbank. Dit dossier wordt typisch gevestigd in de folder van Raadplegingen binnen de de installatiefolder van de gegevenswerkbank. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> IP-adres </td> 
   <td colname="col2"> Het gebied waarvan om het IP adres te lezen. </td> 
   <td colname="col3"> c-ip </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Resultaten </td> 
   <td colname="col2"> <p>De namen van de outputkoorden. </p> <p> De <span class="wintitle"> IPLookup</span> Quova en <span class="wintitle"> IPLookup</span> Digitale transformaties van de Envoy hebben verschillende outputparameters. Ben zeker om de aangewezen transformatie voor uw IP raadplegingsgegevens te gebruiken. </p> </td> 
   <td colname="col3"> </td> 
  </tr> 
 </tbody> 
</table>

In dit voorbeeld, wordt het [!DNL IP geo-location] gegeven (in het raadplegingsdossier [!DNL Quova.bin]) gebruikt om de vermelde outputgebieden tot stand te brengen. De output (AOL, ASN, de Code van het Gebied, etc.) kan worden gebruikt om afmetingen voor geografische analyse van bezoekersverkeer te creëren.

![](assets/cfg_TransformationType_IPLookup.png)

