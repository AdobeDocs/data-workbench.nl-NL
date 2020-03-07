---
description: Conceptueel, dient het adresdossier het zelfde doel zoals het dossier van de HOSTS van ETC \ op een genetwerkte machine.
solution: Insight
title: Netwerklocaties
uuid: a2097eca-dd75-4d43-b8a8-fb4c768df38d
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Netwerklocaties{#network-locations}

Conceptueel, dient het adresdossier het zelfde doel zoals het dossier van de HOSTS van ETC \ op een genetwerkte machine.

Nochtans, in tegenstelling tot het dossier van GASTHEREN, dat één enkele inzameling van namen beschrijft, bevat het adresdossier veelvoudige inzamelingen van namen genoemd netwerkplaatsen.

Een netwerkplaats is een genoemde inzameling van adresdefinities. Elke adresdefinitie in de inzameling associeert een gemeenschappelijke naam met een IP adres.

In het adresdossier, wordt een netwerkplaats bepaald in een structuur genoemd een NetworkLocation. NetworkLocation in het volgende voorbeeld bepaalt een netwerkplaats genoemd &quot;MyCorporate Intranet.&quot; Het bevat een adresdefinitie die de gemeenschappelijke naam [!DNL VS01.myCompany.com] aan het IP adres &quot;10.2.1.70 in kaart brengt.&quot;

```
0 = NetworkLocation: 
  Addresses = vector: 1 items
    0 = AddressDefinition: 
      Address = string: 10.2.1.70
      Name = string: VS01.myCompany.com
  Name = string: MyCorporateIntranet
  Parent = string: 
```

Zoals aangetoond in het voorbeeld hierboven, bestaat de structuur NetworkLocation uit drie belangrijke parameters:

<table id="table_9142A0EFA15E4C37975E7ACE234F6FDD"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Parameter </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Adressen </td> 
   <td colname="col2"> Bepaalt nul of meer AddressDefinitions. Elke AddressDefintion associeert een gemeenschappelijke naam met een IP adres. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Naam </td> 
   <td colname="col2"> Wijst een naam aan NetworkLocation toe. De naam die aan een NetworkLocation wordt toegewezen moet binnen het adresdossier uniek zijn. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Ouder </td> 
   <td colname="col2"> <p>Specificeert de naam van een andere NetworkLocation de waarvan leden in dit NetworkLocation inbegrepen zijn. Deze parameter laat één NetworkLocation toe om een andere uit te breiden. </p> <p>U kunt de parameter van de Ouder aan "DNS plaatsen,"om een NetworkLocation tot het normale DNS systeem van de cliënt uit te breiden. </p> <p>Voorbeeld: Ouder = string: DNS </p> <p>Wanneer DNS de ouder is, proberen de cliënten om een gemeenschappelijke naam op te lossen gebruikend het DNS van de cliëntmachine systeem wanneer zij niet de naam door NetworkLocation kunnen oplossen. </p> </td> 
  </tr> 
 </tbody> 
</table>

