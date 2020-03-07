---
description: Informatie over de codes en formaten van de Tijdzone.
solution: Analytics
title: Code tijdzone
topic: Data workbench
uuid: 5698882a-9682-41d8-88d3-8471578a22cc
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Code tijdzone{#time-zone-codes}

Informatie over de codes en formaten van de Tijdzone.

De meeste op tijd-gebaseerde parameters in de server van de gegevenswerkbank worden gespecificeerd in het volgende formaat:

* maand DD , JJJJ UU :MM :SS Tone
* Voorbeeld: 13 augustus 2013 22:30:00 EST

De tijdzones worden uitgedrukt in een systeem-onafhankelijk formaat van de tijdzone (gecoördineerde Universele Tijd) van het volgende formaat:

* UTC + hhmm-dstralen

Het teken (+) kan of plus (+) of een minus (-) teken zijn, en hhmm is de compensatie van UTC in uren en notulen. De facultatieve veranderlijke variabelen specificeren een reeks regels om de Tijd van de Besparing van het Daglicht of een gelijkaardig klok-veranderend beleid uit te voeren.

Als u modules specificeert, [!DNL dstrules.dst] moet een lusje-afgebakend dossier genoemd aanwezig zijn binnen de folder van de Dataset \ TimeZone van of het [!DNL Base] profiel (voor configuratiedossiers die niet met een bepaalde dataset worden geassocieerd) of het datasetprofiel (voor configuratiedossiers die dataset-specifiek zijn). Het dossier specificeert een tijdzone onafhankelijke reeks regels voor de Tijd van de Besparing van het Daglicht. Je kunt verschillende regels hebben voor verschillende jaren. Het [!DNL DST.dst] dossier dat door Adobe in het [!DNL Base] profiel wordt verstrekt specificeert de standaardregels van de V.S. die door de Akte van het Beleid van de Energie van 2005 (in feite beginnend 2007) worden opgesteld en de regels van de V.S. voor voorafgaande jaren.

De ingangen van de de tijdzone van de steekproef zijn hieronder vermeld:

* US Eastern Daylight Time: Tijdzone = tekenreeks: UTC -0500 DST
* UTC-tijd zonder offset en zonder strules (overeenkomend met GMT): Tijdzone = tekenreeks: UTC -0000

Wanneer dit formaat wordt gebruikt, de streek van de systeemtijd van de server van de gegevenswerkbank, gegevenswerkbank, en de machines van het Rapport te hoeven niet het zelfde als de gespecificeerde tijdzone te zijn. Bovendien moeten alle actieve datasetprofielen op een de servermachine van de gegevenswerkbank niet het zelfde tijdzone plaatsen hebben.

De volgende lijst bevat de lijst van codes u kunt gebruiken om tijdstreken in op tijd-gebaseerde parameters te specificeren.

## Tabel met tijdzonecode {#section-b4f965b872c543e2ac52a3c94410d076}

Als u de Tijd van de Besparing van het Daglicht of een gelijkaardig klok-verschuivend beleid uitvoert, moet u het [!DNL .dst] dossier opslaan dat de aangewezen regels in de folder van de profielnaam op de de servermachine van de gegevenswerkbank bevat [!DNL \Dataset\Timezone] .

| Code | Tijdzone | Compensatie van GMT |
|---|---|---|
| grip | Greenwich Mean | 0 |
| testen | Oostelijke standaard | 5 |
| edt | Oostelijk daglicht | 5 |
| verknallen | Centrale standaard | 6 |
| cit | Centraal daglicht | 6 |
| mest | Mountain Standard | 7 |
| mdt | Berg Daylight | 7 |
| pesten | Pacifische standaard | 8 |
| pdt | Pacifische daglicht | 8 |

