---
description: Met de gesplitste transformatie wordt een tekenreeks gesplitst in een vector met subtekenreeksen op basis van een opgegeven scheidingsteken.
title: Splitsen
uuid: 116e8465-8fb1-41eb-9a28-412cee54ab87
exl-id: ea85b095-1306-4938-906d-35d421db6c98
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '319'
ht-degree: 1%

---

# Splitsen{#split}

{{eol}}

Met de gesplitste transformatie wordt een tekenreeks gesplitst in een vector met subtekenreeksen op basis van een opgegeven scheidingsteken.

[!DNL Split] is met name nuttig voor het extraheren van individuele waarden uit een verzameling waarden die zijn gekoppeld aan één URI-querynaamwaarde.

<table id="table_C97DA4E45DA844FAB8D61AABA22FF809"> 
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
   <td colname="col1"> Scheidingsteken </td> 
   <td colname="col2"> <p>Tekenreeks die wordt gebruikt om de invoertekenreeks in subtekenreeksen te scheiden. Moet één teken lang zijn. </p> <p> Als u de Ctrl-toets ingedrukt houdt en met de rechtermuisknop in de parameter Scheidingsteken klikt, wordt het menu Invoegen weergegeven. Dit menu bevat een lijst met speciale tekens die vaak als scheidingstekens worden gebruikt. </p> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Invoer </td> 
   <td colname="col2"> De naam van het veld waarvan de waarde wordt gesplitst om de uitvoertekenreeksvector te maken. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Uitvoer </td> 
   <td colname="col2"> De naam van het uitvoerveld. </td> 
   <td colname="col3"> </td> 
  </tr> 
 </tbody> 
</table>

Neem bijvoorbeeld een website waar de producten die een klant heeft aangeschaft, als onderdeel van de waarde cs-uri-query worden weergegeven wanneer de bevestigingspagina die aan een geslaagde aankoop is gekoppeld, wordt geopend. Hier volgt een voorbeeld van een dergelijke tekenreeks:

* /checkout/confirmed.asp?prod_selected=B57481,C46355,Z97123

Het veld cs-uri-stem wordt gebruikt om te bepalen of de pagina die door de logbestandvermelding wordt aangevraagd, de bevestigingspagina is. De codes voor de producten die de klant heeft gekocht zijn vermeld als komma-gescheiden waarden van de naam prod_selected in cs-uri-query. De [!DNL Split] transformatie kan worden gebruikt om deze informatie te extraheren door de productcodes onder een komma te splitsen als de waarde van cs-uri-stem overeenkomt met de waarde die in het [!DNL String Match] voorwaarde. Zie [Tekenreeks afstemmen](../../../../../home/c-dataset-const-proc/c-conditions/c-test-ops/c-test-op-con.md#section-f8d132085c6b4500bfbe4515b848142f). In de volgende transformatie wordt de oplossing voor dit probleem beschreven.

![](assets/cfg_TransformationType_Split.png)

Hier is het uitvoerveld x-products, waarmee de gewenste uitgebreide dimensie wordt gemaakt waarmee de aangeschafte producten worden toegewezen aan de sessies waarin de aankoop is gedaan.
