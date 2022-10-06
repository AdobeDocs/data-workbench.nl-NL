---
description: De transformatie IPLookup neemt IP geo-plaats of IP geo-intelligentie gegevens (die door om het even welke verkoper van dergelijke gegevens worden verstrekt en in merkgebonden formaat door Adobe worden omgezet) en zet de gegevens in geografische informatie om die in analyse kan worden gebruikt.
title: IPLookup
uuid: 6fccee39-761f-4854-a7fd-3f8b453e0698
exl-id: 3e9dba44-8d31-49af-8ce0-fecaf92edeb7
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '257'
ht-degree: 2%

---

# IPLookup{#iplookup}

{{eol}}

De transformatie IPLookup neemt IP geo-plaats of IP geo-intelligentie gegevens (die door om het even welke verkoper van dergelijke gegevens worden verstrekt en in merkgebonden formaat door Adobe worden omgezet) en zet de gegevens in geografische informatie om die in analyse kan worden gebruikt.

Twee [!DNL IPLookup] transformaties worden vermeld in het menu Add new > *Transformation type *:

* [!DNL IPLookup] Quova voor [!DNL IP geo-location] data

* [!DNL IPLookup] Digitale gezant voor [!DNL IP geo-intelligence] data

Wanneer u een [!DNL IPLookup] transformatie, kies de aangewezen transformatie voor uw [!DNL IP geo-location] of [!DNL IP geo-intelligence] gegevens.

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
   <td colname="col2"> Beschrijvende naam van de transformatie. U kunt hier elke naam invoeren. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Opmerkingen </td> 
   <td colname="col2"> Optioneel. Opmerkingen over de transformatie. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Voorwaarde </td> 
   <td colname="col2"> De omstandigheden waaronder deze transformatie wordt toegepast. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Bestand </td> 
   <td colname="col2"> Pad en bestandsnaam van het opzoekbestand. Relatieve paden hebben betrekking op de installatiemap van de gegevenswerkbankserver. Dit bestand bevindt zich gewoonlijk in de map Lookups in de installatiemap van de gegevenswerkbank. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> IP-adres </td> 
   <td colname="col2"> Het veld waaruit het IP-adres moet worden gelezen. </td> 
   <td colname="col3"> c-ip </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Uitvoer </td> 
   <td colname="col2"> <p>De namen van de uitvoertekenreeksen. </p> <p> De <span class="wintitle"> IPLookup</span> Quova en <span class="wintitle"> IPLookup</span> Transformaties van Digital Envoy hebben verschillende uitvoerparameters. Ben zeker om de aangewezen transformatie voor uw IP raadplegingsgegevens te gebruiken. </p> </td> 
   <td colname="col3"> </td> 
  </tr> 
 </tbody> 
</table>

In dit voorbeeld: [!DNL IP geo-location] gegevens (in het opzoekbestand) [!DNL Quova.bin]) wordt gebruikt om de weergegeven uitvoervelden te maken. De output (AOL, ASN, de Code van het Gebied, etc.) kan worden gebruikt om dimensies voor geografische analyse van bezoekersverkeer tot stand te brengen.

![](assets/cfg_TransformationType_IPLookup.png)
