---
description: Tabel die aangeeft welke conventies van toepassing zijn bij het samenstellen van transformaties.
title: Conventies voor het samenstellen van transformaties
uuid: 91dddca6-4c17-4107-b78b-0f8b8870ef8d
exl-id: c2552c52-c6d3-4c9f-8359-b5a58bf1a59f
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '384'
ht-degree: 0%

---

# Conventies voor het construeren van transformaties{#conventions-for-constructing-transformations}

Tabel die aangeeft welke conventies van toepassing zijn bij het samenstellen van transformaties.

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
   <td colname="col2"> <p>De transformaties binnen een dossier van de datasetconfiguratie worden toegepast op de logboekingangen opeenvolgend (namelijk in de orde waarin zij in het configuratiedossier worden vermeld). Transformaties moeten daarom worden vermeld in de volgorde waarin hun outputs als input voor andere transformaties worden gebruikt. Meer specifiek, als de output van één transformatie als input aan een andere transformatie wordt gebruikt, is het belangrijk dat die vroegere transformatie voorafgaand aan de laatstgenoemde transformatie in de dossiers van de datasetconfiguratie wordt vermeld. Anders genereert de gegevenswerkbankserver een fout. </p> <p> De stadia van de verwerking verstrekken een manier om tot de transformaties opdracht te geven die binnen veelvoudige dataset worden bepaald omvatten dossiers. Voor alle dataset omvat dossiers verbonden aan een bepaald verwerkingsstadium, worden de transformaties bevolen gebaseerd op hun input en output. Als meerdere datasets bovendien bestanden in een werkgebied bevatten die als gevolg van een transformatie worden uitgevoerd naar hetzelfde veld, genereert de gegevenswerkbankserver een fout. </p> <p> Voor meer informatie over stadia, zie <a href="../../../home/c-dataset-const-proc/c-log-proc-config-file/c-abt-log-proc-config-file.md"> het Dossier van de Configuratie van de Verwerking van het Logboek </a>, <a href="../../../home/c-dataset-const-proc/c-trans-config-file/c-abt-trans-config-file.md"> het Dossier van de Configuratie van de Transformatie</a>, en <a href="../../../home/c-dataset-const-proc/c-dataset-inc-files/c-abt-dataset-inc-files.md"> Gegevensreeks omvat Dossiers</a>. </p> <p>Een <span class="wintitle"> Transformation Dependency Map</span> kan tonen hoe een gebied door een reeks transformaties wordt gewijzigd. Zie <a href="../../../home/c-dataset-const-proc/c-dataset-config-tools/c-dataset-config-tools.md"> Hulpmiddelen voor de configuratie van gegevenssets</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Uitvoernamen </td> 
   <td colname="col2"> De meeste transformaties geven een uitvoerveld op. Als de uitvoer een door de gebruiker gedefinieerd uitgebreid veld is, moet de naam voor dit veld beginnen met "x-". Namen van uitvoervelden mogen geen spaties of speciale tekens bevatten. De namen van uitgebreide velden kunnen met hoofdletters en kleine letters worden geschreven, zoals "x-NewCampaignName" of "x-New-Campaign-Name" voor leesbaarheid, maar worden door de software als niet-hoofdlettergevoelig beschouwd. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Invoervelden </td> 
   <td colname="col2"> <p>Invoervelden verwijzen naar een van de basislijnvelden of een door de gebruiker gemaakt veld dat het resultaat is van een vorige transformatie. Wanneer een constante tekenreeks nodig is, kan een tekenreeks tussen aanhalingstekens worden gebruikt in plaats van een door de gebruiker gemaakt veld of basislijn. </p> <p> Zie <a href="../../../home/c-dataset-const-proc/c-ev-data-rec-fields.md"> Gegevensrecordvelden van gebeurtenissen</a> voor een lijst met een aantal algemeen gedefinieerde gegevensvelden die de gegevenswerkbankserver kan verwerken. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Eenvoudige tekenreeksen en vectoren van tekenreeksen </td> 
   <td colname="col2"> Alle transformaties werken op tekenreeksen en/of vectoren van tekenreeksen. Eenvoudige tekenreeksen zijn letterlijke tekenreeksen. Tekenreeksvectoren bevatten nul of meer eenvoudige tekenreeksen in een bepaalde volgorde. </td> 
  </tr> 
 </tbody> 
</table>
