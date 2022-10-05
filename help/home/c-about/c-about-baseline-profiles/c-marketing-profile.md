---
description: De dimensie van de Campagne wordt bepaald in het de Marketing van de Plaats profiel om de mogelijkheden van de campagneanalyse te verstrekken.
title: Dimension voor marketingprofielen
uuid: 034b4318-58e6-4638-9b13-fac83ff9f826
exl-id: 93804fba-a44b-4cdc-8d67-d4ec0656e742
source-git-commit: 4ab43bfbad96096fb2cebd77a8be8fa6d49fa7dc
workflow-type: tm+mt
source-wordcount: '246'
ht-degree: 1%

---

# Dimension voor marketingprofielen{#marketing-profile-dimensions}

{{eol}}

De dimensie van de Campagne wordt bepaald in het de Marketing van de Plaats profiel om de mogelijkheden van de campagneanalyse te verstrekken.

<table id="table_27A4B8247F6D4E18BD61041CED7D8805"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Dimension </th> 
   <th colname="col2" class="entry"> Type </th> 
   <th colname="col3" class="entry"> Niveau </th> 
   <th colname="col4" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Campaign </td> 
   <td colname="col2"> Naam Eenvoudig wijzigen </td> 
   <td colname="col3">Sessie <p>EERSTE RIJ, bewerking </p></td> 
   <td colname="col4"> De campagne-id die is opgehaald uit een waarde in het eerste verzoek van de bezoeker. </td> 
  </tr> 
 </tbody> 
</table>

**Voorbeelden van Dimension van Aangepast marketingprofiel**

U kunt extra afmetingen van gegevens voor verdere analyse opnemen. Deze afmetingen worden toegevoegd door extra informatie in de stroom van gegevens op te nemen die voor analyse wordt verzameld. De volgende tabel bevat bijvoorbeeld enkele aangepaste marketingdimensies die zijn toegevoegd in implementaties voor klanten in verschillende bedrijfstakken:

| Dimension (aangepast) | Beschrijving |
|---|---|
| Datum e-mailcampagne | Parseert de campagnecadatum (eerste waarde) van de koorden van de campagnevraag van de e-mail. |
| E-mailcampagnedetail | Verzamelt het waardekoord in bijlage aan de de reeksvariabele van de e-mailcampagnevraag. |
| Segment e-mailcampagne | Parseert het campagtiesegment (derde waarde) van de koorden van de campagnevraag van de e-mail. |
| Type e-mailcampagne | Parseert het campagneretype (tweede waarde) van de koorden van de campagnevraag van de e-mail. |
| Details marketingcampagne | Verzamelt de waardekoord in bijlage aan de het vraagreeksvariabelen van de de campagnerag van de marketing. |
| Eigenaar van marketingcampagne | Parseert de campagneeigenaar (vierde waarde) van de koorden van de campagnevraag van de marketing. |
| Bron marketingcampagne | Parseert de campagnebron (eerste waarde) van de koorden van de campagnevraag van de marketing. |
| Type marketingcampagne | Parseert het campagnetype (tweede waarde) van de koorden van de campagnevraag van de marketing. |
| Details PPC-campagne | Collects the value string attached to the ppc query string variable. |
