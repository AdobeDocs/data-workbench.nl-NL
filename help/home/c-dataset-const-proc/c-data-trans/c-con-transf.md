---
description: Lijst die welke overeenkomsten tonen wanneer het construeren van transformaties van toepassing zijn.
solution: Analytics
title: Conventies voor de bouw van transformaties
topic: Data workbench
uuid: 91dddca6-4c17-4107-b78b-0f8b8870ef8d
translation-type: tm+mt
source-git-commit: 27600561841db3705f4eee6ff0aeb8890444bbc9

---


# Conventies voor de bouw van transformaties{#conventions-for-constructing-transformations}

Lijst die welke overeenkomsten tonen wanneer het construeren van transformaties van toepassing zijn.

<table id="table_BEB0F6C416D144B5A2DD3D1A21613B21"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Conventie </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Opeenvolgende uitvoering </td> 
   <td colname="col2"> <p>De transformaties binnen een dossier van de datasetconfiguratie worden toegepast op de logboekingangen opeenvolgend (namelijk in de orde waarin zij in het configuratiedossier vermeld zijn). Daarom moeten de transformaties in de orde worden vermeld hun output als input aan andere transformaties wordt gebruikt. Meer specifiek, als de output van één transformatie als input aan een andere transformatie wordt gebruikt, is het belangrijk dat die vroegere transformatie voorafgaand aan de laatstgenoemde transformatie in de dossiers van de datasetconfiguratie wordt vermeld. Anders, produceert de server van de gegevenswerkbank een fout. </p> <p> De stadia van de verwerking verstrekken een manier om tot de transformaties opdracht te geven die binnen veelvoudige dataset worden bepaald omvatten dossiers. Voor alle dataset omvat dossiers verbonden aan een bepaald verwerkingsstadium, worden de transformaties bevolen gebaseerd op hun input en output. Bovendien als de veelvoudige dataset dossiers binnen een gegevens van de stadiumoutput aan het zelfde gebied als resultaat van een transformatie omvat, produceert de server van de gegevenswerkbank een fout. </p> <p> Voor meer informatie over stadia, zie het Dossier <a href="../../../home/c-dataset-const-proc/c-log-proc-config-file/c-abt-log-proc-config-file.md"> van de Configuratie van de Verwerking van het</a>Logboek, het <a href="../../../home/c-dataset-const-proc/c-trans-config-file/c-abt-trans-config-file.md"> Dossier</a>van de Configuratie van de Transformatie, en de <a href="../../../home/c-dataset-const-proc/c-dataset-inc-files/c-abt-dataset-inc-files.md"> Dataset omvat Dossiers</a>. </p> <p>Een kaart <span class="wintitle"> van het Gedeelte van de</span> Transformatie kan tonen hoe een gebied door een reeks transformaties wordt gewijzigd. Zie de <a href="../../../home/c-dataset-const-proc/c-dataset-config-tools/c-dataset-config-tools.md"> Hulpmiddelen</a>van de Configuratie van de Dataset. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Uitvoernamen </td> 
   <td colname="col2"> De meeste transformaties specificeren een outputgebied. Als de output een user-defined uitgebreid gebied is, moet de naam voor dit gebied met "x- beginnen." De namen van het outputgebied kunnen geen ruimten of speciale karakters bevatten. De namen van uitgebreide gebieden kunnen met gemengd-geval, zoals "x-NewCampaignName,"of "x-nieuw-campagne-Naam"voor leesbaarheid worden geschreven, maar zij worden behandeld door de software als case-insensitive. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Invoervelden </td> 
   <td colname="col2"> <p>De gebieden van de input verwijzen naar één van de basislijngebieden of een door de gebruiker gecreeerd gebied resulterend uit de output van een vorige transformatie. Als een constant koord nodig is, kan een geciteerd koord in plaats van een basislijn of een user-gecreeerd gebied worden gebruikt. </p> <p> Voor een lijst van enkele algemeen bepaalde gebieden van gegevens die de server van de gegevenswerkbank kan verwerken, zie de Gebieden <a href="../../../home/c-dataset-const-proc/c-ev-data-rec-fields.md"> van het Verslag van de Gegevens van de</a>Gebeurtenis. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Eenvoudige snaren en vectoren van snaren </td> 
   <td colname="col2"> Alle transformaties werken op strings en/of vectoren van strings. De eenvoudige koorden zijn letterlijke opeenvolgingen van karakters. De vectoren van het koord bevatten nul of meer eenvoudige koorden in een specifieke orde. </td> 
  </tr> 
 </tbody> 
</table>

