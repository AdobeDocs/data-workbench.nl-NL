---
description: Het profiel van het Verkeer bevat de volgende afmetingen helpen bezoekersacties identificeren.
solution: Analytics
title: Afmetingen verkeersprofiel
topic: Data workbench
uuid: 9c0dabfc-67c9-4772-99ac-4c503c06ea78
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Afmetingen verkeersprofiel{#traffic-profile-dimensions}

Het profiel van het Verkeer bevat de volgende afmetingen helpen bezoekersacties identificeren.

De afmetingen in de volgende lijst worden bepaald in de transformatiedataset omvat dossiers in Traffic\Dataset\Transformation directory.

| Naam | Type | Niveau | Beschrijving |
|---|---|---|---|
| Dag | Eenvoudig | Sessie | De dag van de eerste logboekingang van de zitting. |
| Weekdag | Eenvoudig | Sessie | De dag van week van de eerste logboekingang van een zitting. |
| De nauwkeurige Duur van de Pagina (Verborgen) | Numeriek | Paginaweergave | De duur in milliseconden van paginamening zoals die door de tijd van de volgende paginamening van de tijd van die paginamening wordt gemeten af te trekken. De nauwkeurige duur van de laatste paginamening in een zitting is altijd 0. |
| Uur | Eenvoudig | Sessie | Het uur van de eerste logboekingang van een zitting. |
| Uur van Dag | Eenvoudig | Sessie | Het uur van dag van de eerste logboekingang van een zitting. |
| Maand | Eenvoudig | Sessie | De maand van de eerste logboekingang van een zitting. |
| Paginaweergave | Veelzeggend | Sessie | Een logboekingang of &quot;het Verslag van de Gegevens van de Gebeurtenis&quot;die aan de Voorwaarde van de Mening van de Pagina voldoen. |
| Referentieuse | Eenvoudig | Sessie | Het tweede niveaudomein van de verwijzer van de eerste logboekingang van de zitting (of niets als het een intern verwijzingsdomein is). |
| Sessie | Veelzeggend | Bezoeker | Een periode van verwante aaneengesloten activiteit door een bezoeker. Het wordt afgebakend door een periode van 30 minuten van inactiviteit en een extern verwijzingsdomein of een maximumDuur van de Zitting van 48 uur. Beide onderbrekingen en de reeks domeinen die als intern worden beschouwd kunnen in het [!DNL Transformation.cfg] dossier worden gevormd. |
| URI | Eenvoudig | Paginaweergave | De stam van URI van een paginamening. De dimensie van URI kan worden opnieuw gedefinieerd gebruikend de transformaties ReplaceURI, PrependURI, en AppendURI. |
| Bezoeker | Veelzeggend | N.v.t. | Een unieke waarde van x-trackingid. Gewoonlijk komt dit overeen met een unieke browser als er permanente cookies worden gebruikt. De x-trackingidentiteitskaart kan anders op IP aantal of één of ander ander uniek herkenningsteken zoals x.509 worden gebaseerd gemeenschappelijke naam. |
| Week | Eenvoudig | Sessie | De week van de eerste logboekingang van een zitting. |

De afmetingen in de volgende lijst worden bepaald in de folder van de Dimensie van het profiel van het Verkeer:

<table id="table_02AC8DAD1B62443A96FABCB75C37F23A"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Afmetingen </th> 
   <th colname="col2" class="entry"> Type </th> 
   <th colname="col03" class="entry"> Niveau </th> 
   <th colname="col3" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Browser </td> 
   <td colname="col2"> Eenvoudig </td> 
   <td colname="col03"> Bezoeker </td> 
   <td colname="col3"> Het type van gebruikersagent die door de bezoeker wordt gebruikt, met inbegrip van het versieaantal (bijvoorbeeld, MSIE 6.0.) </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Soort browser </td> 
   <td colname="col2"> Eenvoudig </td> 
   <td colname="col03"> Bezoeker </td> 
   <td colname="col3"> Het type van gebruikersagent die door de bezoeker (bijvoorbeeld, MSIE) wordt gebruikt. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Zoekmachine </td> 
   <td colname="col2"> Eenvoudig </td> 
   <td colname="col03">Sessie <p>EERSTE WEG </p></td> 
   <td colname="col3"> De eerste onderzoeksmotor in de zitting van een bezoeker wanneer een bezoeker van een genoemde onderzoeksmotor heeft gezocht. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Volgende URI </td> 
   <td colname="col2"> Voortgekomen (ShiftDim die op de dimensie van URI wordt gebaseerd) </td> 
   <td colname="col03"> Paginaweergave </td> 
   <td colname="col3"> URI van volgende URI na momenteel geselecteerd URI. Deze afgeleide afmeting wordt gebruikt om analyse over te leiden wat de bezoekers daarna na om het even welk bepaald URI doen. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Eenmaal versus herhalen </td> 
   <td colname="col2"> Voortgekomen (SegmentDim die op de Bezoekers van de Herhaling en de metriek van Eenmalige Bezoekers wordt gebaseerd) </td> 
   <td colname="col03"> Bezoeker </td> 
   <td colname="col3"> Het type bezoeker: éénmaal of herhaald. Eenmalige bezoekers hebben slechts één sessie gehad op de site, terwijl meermaals bezoekers meer dan één sessie hebben gehad. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Pagina </td> 
   <td colname="col2"> Voortgekomen (RenameDim die op de dimensie van URI wordt gebaseerd) </td> 
   <td colname="col03"> Paginaweergave </td> 
   <td colname="col3"> De naam van elke bezochte pagina tijdens een zitting. Aanvankelijk, is de naam van elke pagina het zelfde als URI maar kan voor gemakkelijkere interpretatie worden veranderd. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Referentieuse </td> 
   <td colname="col2"> Geërft van de ingebouwde afmeting van de Referrer </td> 
   <td colname="col03"> Sessie </td> 
   <td colname="col3"> De tweede naam van het niveaudomein van de website die eerst een zitting naar de plaats (zoals die door browser van de bezoeker wordt geleverd.) verwees </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Zoekterm </td> 
   <td colname="col2"> Eenvoudig </td> 
   <td colname="col03">Sessie <p>EERSTE WEG </p></td> 
   <td colname="col3"> De eerste onderzoeksuitdrukking in de zitting van een bezoeker zoals doorgegeven door een onderzoeksmotor wanneer een bezoeker van een genoemde onderzoeksmotor heeft gezocht. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Zoekterm </td> 
   <td colname="col2"> Velen-aan-Velen </td> 
   <td colname="col03"> Sessie </td> 
   <td colname="col3"> Elke onderzoekstermijn zoals die door een onderzoeksmotor wordt doorgegeven wanneer een bezoeker een onderzoeksverwijzingsklik-door van een genoemde onderzoeksmotor heeft. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Sessieduur </td> 
   <td colname="col2"> Voortgekomen (MetricDim die op de Exacte metrische Duur van de Pagina wordt gebaseerd) </td> 
   <td colname="col03"> Sessie </td> 
   <td colname="col3"> De duur van een zitting in 30 tweede toename. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Sessienummer </td> 
   <td colname="col2"> Eenvoudig </td> 
   <td colname="col03"> Sessie </td> 
   <td colname="col3"> Het aantal keren dat een bezoeker de site heeft bezocht. Bijvoorbeeld, hebben de eerste bezoekers een Aantal van de Zitting van "1", hebben de tweede bezoekers een Aantal van de Zitting van "2", enz. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Weergaven sessiepagina </td> 
   <td colname="col2"> Voortgekomen (MetricDim die op metrisch de Meningen van de Pagina wordt gebaseerd) </td> 
   <td colname="col03"> Sessie </td> 
   <td colname="col3"> Het aantal paginameningen in een zitting. Bijvoorbeeld, zou het selecteren van "3"in de dimensie van de Meningen van de Pagina van de Zitting alle zittingen met precies 3 paginameningen selecteren. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Zoekmachine </td> 
   <td colname="col2"> Eenvoudig </td> 
   <td colname="col03"> Sessie </td> 
   <td colname="col3"> De tweede naam van het niveaudomein van de eerste website die een genoemde onderzoeksmotor is die een bezoeker naar de plaats tijdens een zitting (zoals die door browser van de bezoeker wordt geleverd) verwees. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Afmetingen tijd </td> 
   <td colname="col2"> Eenvoudig </td> 
   <td colname="col03"> Sessie </td> 
   <td colname="col3"> Het uur, de dag, het uur van dag, de week, de dag van week, maand, kwartaal of jaar waarin een Zitting begon. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Tijdrapporteringsafmetingen </td> 
   <td colname="col2"> Voortgekomen (LastN en noem afmetingen anders die op ingebouwde tijdafmetingen worden gebaseerd) </td> 
   <td colname="col03"> Sessie </td> 
   <td colname="col3"> Afmetingen inclusief dagen geleden, dagen van vorige maand, dagen van vorige week, dagen van deze maand, dagen van deze week, dagen van deze week, uren van vandaag, uren van gisteren, afgelopen 12 maanden, afgelopen 2 maanden, afgelopen 2 weken, afgelopen 24 uur, afgelopen 3 maanden, afgelopen 4 weken, afgelopen 6 maanden, afgelopen 7 dagen, afgelopen 7 dagen en afgelopen 8 dagen, Weken, afgelopen 9 maanden, afgelopen maand, afgelopen week, afgelopen week, maanden geleden, deze maand, deze week, deze en afgelopen 14 dagen, dit en afgelopen 6 maanden, dit en afgelopen 8 weken, vandaag, vandaag, vandaag, en afgelopen 30 dagen, Weken geleden en Gisteren verstrekken een geschikte manier om een Werkruimte of een Rapport te bouwen die altijd een gedeelte van gegevens in de Dataset toont. Elk is gebaseerd op wanneer een zitting begon. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> URI </td> 
   <td colname="col2"> Geërfd van de ingebouwde Dimension URI </td> 
   <td colname="col03"> Paginaweergave </td> 
   <td colname="col3"> URI van elke bekeken pagina. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Bezoekerpagina bekijken </td> 
   <td colname="col2"> Voortgekomen (MetricDim die op metrisch de Meningen van de Pagina wordt gebaseerd) </td> 
   <td colname="col03"> Bezoeker </td> 
   <td colname="col3"> Het aantal paginameningen tot op heden voor een bezoeker. Bijvoorbeeld, zou het selecteren van "3"in de Afmeting van de Meningen van de Pagina van de Bezoeker alle bezoekers met precies 3 paginameningen over elk van hun zittingen selecteren. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Bezoeker </td> 
   <td colname="col2"> Geërft van de ingebouwde afmetingsreferentie </td> 
   <td colname="col03"> Bezoeker </td> 
   <td colname="col3"> De domeinnaam op het tweede niveau van de website die eerst een bezoeker naar de site verwees voor zijn eerste sessie (zoals die door de browser van de bezoeker wordt geleverd). </td> 
  </tr> 
 </tbody> 
</table>

