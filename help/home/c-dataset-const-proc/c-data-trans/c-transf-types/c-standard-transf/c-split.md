---
description: De gespleten transformatie verdeelt een koord in een vector van substrings die op een bepaald afbakeningskarakter wordt gebaseerd.
solution: Analytics
title: Gespleten
topic: Data workbench
uuid: 116e8465-8fb1-41eb-9a28-412cee54ab87
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Gespleten{#split}

De gespleten transformatie verdeelt een koord in een vector van substrings die op een bepaald afbakeningskarakter wordt gebaseerd.

[!DNL Split] is bijzonder nuttig om individuele waarden uit een inzameling van waarden te halen verbonden aan één enkele waarde van de de vraagnaam van URI.

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
   <td colname="col1"> Afbakening </td> 
   <td colname="col2"> <p>Koord dat wordt gebruikt om het inputkoord in substrings te scheiden. Moet één enkel karakter in lengte zijn. </p> <p> Als u de sleutel van CTRL onderdrukt en binnen de parameter van de Afbakening met de rechtermuisknop klikt, verschijnt een menu van het Tussenvoegsel. Dit menu bevat een lijst van speciale karakters die vaak als afbakeningen worden gebruikt. </p> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Invoer </td> 
   <td colname="col2"> De naam van het gebied de waarvan waarde wordt gesplitst om de vector van het outputkoord tot stand te brengen. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Uitvoer </td> 
   <td colname="col2"> De naam van het outputgebied. </td> 
   <td colname="col3"> </td> 
  </tr> 
 </tbody> 
</table>

Overweeg een website waarin de producten die door een klant worden gekocht als deel van de cs-uri-vraag waarde vermeld zijn wanneer de bevestigingspagina verbonden aan een succesvolle aankoop wordt betreden. Het volgende is een voorbeeld van zulk een koord:

* /checkout/confirmed.asp?prod_selected=B57481,C46355,Z97123

Het cs-uri-stenstengebied wordt gebruikt om te bepalen of de pagina die door de logboekingang wordt gevraagd de bevestigingspagina is. De codes voor de producten die de klant kocht zijn vermeld als komma-gescheiden waarden van de prod_selected naam in cs-uri-vraag. De [!DNL Split] transformatie kan worden gebruikt om deze informatie te extraheren door de productcodes op de komma te splitsen als de waarde van de cs-uri-stengel overeenkomt met de in de [!DNL String Match] toestand aangegeven waarde. Zie [Koord-overeenstemming](../../../../../home/c-dataset-const-proc/c-conditions/c-test-ops/c-test-op-con.md#section-f8d132085c6b4500bfbe4515b848142f). De volgende transformatie detailleert de oplossing aan dit probleem.

![](assets/cfg_TransformationType_Split.png)

Hier, is het outputgebied x-producten, die zouden worden gebruikt om de gewenste uitgebreide dimensie tot stand te brengen die de producten in kaart brengt die aan de zittingen worden gekocht waarin de aankoop werd gemaakt.
