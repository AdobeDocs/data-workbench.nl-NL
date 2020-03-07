---
description: Deze sectie verklaart hoe te om timestamps voor een dataset van de Werkbank van Gegevens tot stand te brengen.
title: Tijd van de Gebeurtenis van de vestiging
uuid: 0230154d-05a2-44cf-9456-0a27e55f58ef
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Tijd van de Gebeurtenis van de vestiging{#setting-up-event-time}

Deze sectie verklaart hoe te om timestamps voor een dataset van de Werkbank van Gegevens tot stand te brengen.

## Het begrip van de Tijd van de Gebeurtenis {#section-e10ef2b5b6244dc5b215836e3c77d663}

De Tijd van de gebeurtenis is de datum en de tijd waarop het verzoek (of de gebeurtenis) voorkomt.

Gewoonlijk, voor online gegevens, wordt *x_hit_time_gmt* gebruikt als timestamp gebied. De tijd van de vraag kan als timestamp voor off-line gegevens (zoals de gegevens van het vraagcentrum) worden gebruikt. Dit is een verplicht veld en alle gegevensbronnen moeten één veld hebben dat als tijdstempel kan worden gebruikt. Deze informatie zou door uw organisatie moeten worden verstrekt.

In DWB, vangen de volgende vooraf bepaalde variabelen timestamp:

<table id="table_C24BD56CEB4E42F68D645EBB65585D16"> 
 <tbody> 
  <tr> 
   <td colname="col1"><i>x-timestamp</i> </td> 
   <td colname="col2"> <p> De datum en de tijd (GMT) waarop het verzoek door de server werd ontvangen. De tijd wordt uitgedrukt als het aantal van 100 nanoseconden sinds 1 januari 1600. </p> <p>Voorbeeld: 12771098932000000 zou de <i>x-timestamp</i> waarde zijn voor 11:28:52.00000 op dinsdag 13 september 2005. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"><i>x-timestring</i> </td> 
   <td colname="col2"> <i>x-timestamp</i> in het formaat JJJJ-MM-DD HH:MM.:SS.mmm. </td> 
  </tr> 
  <tr> 
   <td colname="col1"><i>x-unixtime</i> </td> 
   <td colname="col2"> <i>x-unixtime</i> is de epoc tijd die het aantal seconden vertegenwoordigt sinds 1 Januari, 1970, bij 00:00:01. </td> 
  </tr> 
 </tbody> 
</table>

Gebaseerd op het formaat van datumgebied, wordt x-timestamp of x-unixtime of x-timestring gebruikt. Bijvoorbeeld, als de inkomende gegevens in het formaat JJJJ-MM-DD zijn, dan moet x-timestring worden gebruikt.

timestamp wordt bepaald in één van de formaten en DWB intern produceert de andere twee formaten. Ook, zijn deze vooraf bepaalde DWB- gebieden en de zelfde naam zou niet voor een ander gebied moeten worden gebruikt.

## Tijdzones gedefinieerd in DWB {#section-3cdd12254342442b917376661e1d9c9f}

Als het datumveld een van de onderstaande tijdzones bevat, neemt DWB de hele rij in die specifieke tijdzone in aanmerking. Bijvoorbeeld, heeft één dossier de datum die als 2015-01-01 00:00 wordt bepaald gmtand en een ander dossier heeft de waarde als 2015-01-01 00:00:00 kosten, dan zal de datum van het eerste dossier in GMT timezone worden overwogen terwijl de datum van het tweede dossier in zal zijn CST-tijdzone.

| Code | Tijdzone |
|---|---|
| grip | Greenwich Mean |
| testen | Oostelijke standaard |
| edt | Oostelijk daglicht |
| verknallen | Centrale standaard |
| cit | Centraal daglicht |
| mest | Mountain Standard |
| mdt | Berg Daylight |
| pesten | Pacifische standaard |
| pdt | Pacifische daglicht |

>[!NOTE]
>
>DWB verwerkt alleen de bovengenoemde tijdzones.

## Aangepaste tijdzones instellen {#section-7c351921f22b439b81c73f40d5b47536}

DWB verwerkt niet de compensatie in de Streek van de Tijd. Om de compensatie in de Streek van de Tijd te overwegen, zouden de gegevens in die compensatietijdzone moeten worden geformatteerd.

Voorbeeld: om het datumformaat in CST tijdzone te overwegen, zouden de gegevens in JJJJ-MM-DD HH moeten komen:MM.:SS UTC +/-HHMM formaat van de cliënt.

2015-10-18 05:00:00 UTC -0200

## Hoe te om de Tijd van de Gebeurtenis/Timestamp te plaatsen {#section-81507080f0b44ae6b83d3650ba019812}

Gebaseerd op het formaat van het datumgebied, wordt *x-timestamp, x-unixtime* of *x-timestring* variabele gebruikt. In het voorbeeld hieronder, aangezien *x-hit_time_gmt* in unix epoc formaat komt, wordt *x-unixtime* gebruikt.

In het DWB- [!DNL foundation.cfg] - dossier (of een ander configuratiedossier onder de omslag van de het logboekverwerking van de Dataset), gebruik de transformatie van het Exemplaar om de Tijd van de Gebeurtenis te plaatsen zoals getoond:

Gebaseerd op het formaat van het datumgebied, wordt x-timestamp, x-unixtime of x-timestring variabele gebruikt. In het voorbeeld hieronder, aangezien x-hit_time_gmt in unix epoc formaat komt, wordt x-unixtime gebruikt.

In het inzicht foundation.cfg (of een andere config onder de omslag van de het logboekverwerking van Datasetà), gebruik de transformatie van het Exemplaar om de Tijd van de Gebeurtenis zoals hieronder getoond te plaatsen: ![](assets/dwb_impl_timestamp1.png)

Als de datum in JJJJ-MM-DD HH is:MM.:SS.mmm formaat, wordt x-timestring gebruikt. ![](assets/dwb_impl_timestamp2.png)Voorbeeld: Als het datumgebied in het formaat buiten dat in DWB wordt bepaald is zeg JJJJ/MM/DD, dan eerst formaat het in één van het timestamp formaat dat door DWB wordt goedgekeurd en wijs het dan aan de overeenkomstige variabele toe. In het hieronder ontsproten scherm, wordt de datum eerst omgezet in formaat JJJJ-MM-DD en dan toegewezen aan *x-timestring *variable. ![](assets/dwb_impl_timestamp3.png)

