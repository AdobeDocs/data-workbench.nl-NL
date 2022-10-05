---
description: Het verkeersprofiel bevat de volgende afmetingen om bezoekersacties te identificeren.
title: Dimension verkeersprofiel
uuid: 9c0dabfc-67c9-4772-99ac-4c503c06ea78
exl-id: 1e7d2904-aa5d-4848-a398-5d4669953be9
source-git-commit: 4ab43bfbad96096fb2cebd77a8be8fa6d49fa7dc
workflow-type: tm+mt
source-wordcount: '987'
ht-degree: 2%

---

# Dimension verkeersprofiel{#traffic-profile-dimensions}

{{eol}}

Het verkeersprofiel bevat de volgende afmetingen om bezoekersacties te identificeren.

De afmetingen in de volgende lijst worden bepaald in de transformatiedataset omvat dossiers in de folder van de Transformatie \ van de Dataset \ van het Verkeer.

| Naam | Type | Niveau | Beschrijving |
|---|---|---|---|
| Dag | Eenvoudig | Sessie | De dag van de eerste logboekingang van de zitting. |
| Weekdag | Eenvoudig | Sessie | De dag van de week van de eerste logboekingang van een zitting. |
| Exacte duur pagina (verborgen) | Numeriek | Paginaweergave | De duur in milliseconden van de paginaweergave, gemeten door de tijd van de volgende paginaweergave af te trekken van de tijd van die paginaweergave. De exacte duur van de laatste paginaweergave in een sessie is altijd 0. |
| Uur | Eenvoudig | Sessie | Het uur van de eerste logboekingang van een zitting. |
| Uur van dag | Eenvoudig | Sessie | Het uur van dag van de eerste logboekingang van een zitting. |
| Maand | Eenvoudig | Sessie | De maand van de eerste logboekingang van een zitting. |
| Paginaweergave | Tabelachtig | Sessie | Een logbestandvermelding of &quot;Gebeurtenisgegevensrecord&quot; die voldoet aan de weergavevoorwaarde voor de pagina. |
| Referrer | Eenvoudig | Sessie | Het tweede niveaudomein van de verwijzer van de eerste logboekingang van de zitting (of niets als het een intern verwijzingsdomein is). |
| Sessie | Tabelachtig | Bezoeker | Een periode van gerelateerde aaneengesloten activiteit door een bezoeker. Het wordt afgebakend door een periode van 30 minuten van inactiviteit en een extern verwijzersdomein of een maximum van de Duur van de Zitting 48 uur. Zowel die onderbrekingen als de reeks domeinen die als intern worden beschouwd kunnen in worden gevormd [!DNL Transformation.cfg] bestand. |
| URI | Eenvoudig | Paginaweergave | De URI-stam van een paginaweergave. De URI-dimensie kan opnieuw worden gedefinieerd met de transformaties ReplaceURI, PrependURI en AppendURI. |
| Bezoeker | Tabelachtig | N.v.t. | Een unieke waarde van x-trackingid. Komt meestal overeen met een unieke browser als permanente cookies worden gebruikt. De x-trackingid kan anders op IP aantal of één of ander ander ander uniek herkenningsteken zoals x.509 gemeenschappelijke naam worden gebaseerd. |
| Week | Eenvoudig | Sessie | De week van de eerste logboekingang van een zitting. |

De afmetingen in de volgende tabel worden gedefinieerd in de map Dimension van het verkeersprofiel:

<table id="table_02AC8DAD1B62443A96FABCB75C37F23A"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Dimension </th> 
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
   <td colname="col3"> Het type gebruikersagent dat door de bezoeker wordt gebruikt, met inbegrip van het versienummer (bijvoorbeeld, MSIE 6.0.) </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Browsertype </td> 
   <td colname="col2"> Eenvoudig </td> 
   <td colname="col03"> Bezoeker </td> 
   <td colname="col3"> Het type gebruikersagent dat door de bezoeker wordt gebruikt (bijvoorbeeld MSIE). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Zoekmachine </td> 
   <td colname="col2"> Eenvoudig </td> 
   <td colname="col03">Sessie <p>EERSTE RIJ </p></td> 
   <td colname="col3"> Het eerste zoekprogramma in de sessie van een bezoeker wanneer een bezoeker heeft gezocht vanuit een benoemde zoekfunctie. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Volgende URI </td> 
   <td colname="col2"> Afgeleid (ShiftDim gebaseerd op de afmeting van URI) </td> 
   <td colname="col03"> Paginaweergave </td> 
   <td colname="col3"> De URI van de volgende URI na de geselecteerde URI. Deze afgeleide dimensie wordt gebruikt om een analyse uit te voeren over wat bezoekers na om het even welke bepaalde URI doen. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Eenmaal versus Herhalen </td> 
   <td colname="col2"> Voortgekomen (SegmentDim die op de metriek van de Bezoekers van de Herhaling en van Eenmalige Bezoekers wordt gebaseerd) </td> 
   <td colname="col03"> Bezoeker </td> 
   <td colname="col3"> Het type bezoeker: eenmalig of herhaald. Eenmalige bezoekers hebben slechts één sessie op de site gehad, terwijl herhaalde bezoekers meer dan één sessie hebben gehad. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Pagina </td> 
   <td colname="col2"> Afgeleid (RenameDim op basis van URI-dimensie) </td> 
   <td colname="col03"> Paginaweergave </td> 
   <td colname="col3"> De naam van elke pagina die tijdens een sessie is bezocht. In eerste instantie is de naam van elke pagina gelijk aan die van de URI, maar deze naam kan worden gewijzigd voor een betere interpretatie. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Referenter </td> 
   <td colname="col2"> Overgenomen van de ingebouwde dimensie Referrer </td> 
   <td colname="col03"> Sessie </td> 
   <td colname="col3"> De domeinnaam op het tweede niveau van de website die eerst een sessie naar de site verwees (zoals opgegeven door de browser van de bezoeker). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Zoekwoordgroep </td> 
   <td colname="col2"> Eenvoudig </td> 
   <td colname="col03">Sessie <p>EERSTE RIJ </p></td> 
   <td colname="col3"> De eerste zoekfrase in de sessie van een bezoeker zoals doorgegeven door een zoekfunctie wanneer een bezoeker heeft gezocht via een benoemde zoekfunctie. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Zoekterm </td> 
   <td colname="col2"> Velen-aan-Velen </td> 
   <td colname="col03"> Sessie </td> 
   <td colname="col3"> Elke zoekterm die door een zoekmachine wordt doorgegeven, wanneer een bezoeker een doorzoekfunctie voor een zoekverwijzing heeft die een benoemde zoekfunctie heeft. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Sessieduur </td> 
   <td colname="col2"> Afgeleid (MetricDim die op Exacte metrische de Duur van de Pagina wordt gebaseerd) </td> 
   <td colname="col03"> Sessie </td> 
   <td colname="col3"> De duur van een sessie in stappen van 30 seconden. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Sessienummer </td> 
   <td colname="col2"> Eenvoudig </td> 
   <td colname="col03"> Sessie </td> 
   <td colname="col3"> Het aantal keren dat een bezoeker de site heeft bezocht. Eerste bezoekers hebben bijvoorbeeld het sessienummer "1", tweede bezoekers hebben het sessienummer "2", enzovoort. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Weergaven van sessiepagina </td> 
   <td colname="col2"> Afgeleid (MetricDim op basis van metrische paginaweergaven) </td> 
   <td colname="col03"> Sessie </td> 
   <td colname="col3"> Het aantal paginaweergaven in een sessie. Als u bijvoorbeeld "3" selecteert in de dimensie Weergaven voor sessiepagina, worden alle sessies met exact 3 paginaweergaven geselecteerd. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Zoekmachine </td> 
   <td colname="col2"> Eenvoudig </td> 
   <td colname="col03"> Sessie </td> 
   <td colname="col3"> De domeinnaam op het tweede niveau van de eerste website die een benoemde zoekfunctie is die tijdens een sessie een bezoeker naar de site heeft verwezen (zoals opgegeven door de browser van de bezoeker). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Dimension tijd </td> 
   <td colname="col2"> Eenvoudig </td> 
   <td colname="col03"> Sessie </td> 
   <td colname="col3"> Het uur, de dag, het uur van dag, de week, de dag van week, de maand, het kwartaal of het jaar waarin een Zitting begon. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Dimension voor tijdrapportage </td> 
   <td colname="col2"> Voortgekomen (LastN en noem dimensies anders die op ingebouwde tijddimensies worden gebaseerd) </td> 
   <td colname="col03"> Sessie </td> 
   <td colname="col3"> Dimension inclusief dagen geleden, dagen van vorige maand, dagen van vorige week, dagen van deze maand, dagen van deze week, dagen van deze week, uren van vandaag, uren van gisteren, afgelopen 12 maanden, afgelopen 2 weken, afgelopen 2 weken, afgelopen 24 uur, afgelopen 3 maanden, afgelopen 4 weken, afgelopen 6 maanden, afgelopen 7 dagen, afgelopen 7 dagen en vandaag, afgelopen 8 Weken, afgelopen 9 maanden, vorige maand, vorige week, maanden geleden, deze maand, deze week, deze en afgelopen 14 dagen, dit en afgelopen 6 maanden, deze en afgelopen 8 weken, vandaag, vandaag Rapportering, vandaag en afgelopen 30 dagen, weken geleden en gisteren bieden een handige manier om een werkruimte of rapport te maken waarin altijd een deel van gegevens in de Dataset wordt getoond. Elk is gebaseerd op wanneer een zitting begon. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> URI </td> 
   <td colname="col2"> Overgenomen van de ingebouwde Dimension URI </td> 
   <td colname="col03"> Paginaweergave </td> 
   <td colname="col3"> De URI van elke weergegeven pagina. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Weergaven bezoekerspagina </td> 
   <td colname="col2"> Afgeleid (MetricDim op basis van metrische paginaweergaven) </td> 
   <td colname="col03"> Bezoeker </td> 
   <td colname="col3"> Het aantal paginaweergaven tot op heden voor een bezoeker. Als u bijvoorbeeld "3" selecteert in de dimensie Weergaven bezoekerspagina, worden alle bezoekers met exact 3 paginaweergaven geselecteerd voor alle sessies. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Referentiebezoeker </td> 
   <td colname="col2"> Overgenomen van de ingebouwde dimensieverwijzing </td> 
   <td colname="col03"> Bezoeker </td> 
   <td colname="col3"> De domeinnaam op het tweede niveau van de website die eerst een bezoeker naar de site verwees voor zijn eerste sessie (zoals opgegeven door de browser van de bezoeker). </td> 
  </tr> 
 </tbody> 
</table>
