---
description: De instructies van het formaat over op tijd-gebaseerde parameters in de Server van het Inzicht.
solution: Insight
title: Code tijdzone
uuid: dcc8aa15-5846-4f24-8b82-e25ff89871ba
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Code tijdzone{#time-zone-codes}

De instructies van het formaat over op tijd-gebaseerde parameters in de Server van het Inzicht.

De meeste op tijd-gebaseerde parameters in [!DNL Insight Server] worden gespecificeerd in het volgende formaat:

*Maand DD, JJJJ UU:MM:SS TimeZone*

Voorbeeld: 13 augustus 2013 22:30:00 EST

De tijdzones worden uitgedrukt in een systeem-onafhankelijk formaat van de tijdzone (gecoördineerde Universele Tijd) van het volgende formaat:

UTC + *hhmm dstrules*

Het teken (+) kan of plus (+) of een minus (-) teken zijn, en *hhmm* is de compensatie van UTC in uren en notulen. De facultatieve variabele *modules* specificeren een reeks regels om de Tijd van de Besparing van het Daglicht of een gelijkaardig klok-veranderend beleid uit te voeren.

Als u *parameters* specificeert, moet een lusje-afgebakend dossier genoemd *&lt;[!DNL dstrules]>* [!DNL .dst] aanwezig zijn binnen de folder van de Dataset \ TimeZone van of het profiel van de Basis (voor configuratiedossiers die niet met een bepaalde dataset worden geassocieerd) of het datasetprofiel (voor configuratiedossiers die dataset-specifiek zijn). Het dossier specificeert een tijdzone onafhankelijke reeks regels voor de Tijd van de Besparing van het Daglicht. Je kunt verschillende regels hebben voor verschillende jaren. Het [!DNL DST.dst] dossier dat door Adobe in het profiel van de Basis wordt verstrekt specificeert de standaardregels van de V.S. die door de Akte van het Beleid van de Energie van 2005 (in feite beginnend 2007) worden vastgesteld en de regels van de V.S. voor voorafgaande jaren.

De ingangen van de de tijdzone van de steekproef zijn hieronder vermeld:

* US Eastern Daylight Time: Tijdzone = tekenreeks: UTC -0500 DST
* UTC-tijd zonder offset en zonder *ondergrond* (overeenkomend met GMT): Tijdzone = tekenreeks: UTC -0000

Wanneer dit formaat wordt gebruikt, te hoeven de de systeemtijdzone van, [!DNL Insight Server][!DNL Insight][!DNL Report] en machines niet het zelfde te zijn als de gespecificeerde tijdzone. Bovendien hoeven alle actieve datasetprofielen op een [!DNL Insight Server] machine niet de zelfde tijdzone het plaatsen te hebben.

De volgende lijst bevat de lijst van codes u kunt gebruiken om tijdstreken in op tijd-gebaseerde parameters te specificeren.

## Tabel met tijdzonecode {#section-3cab225b864f4e54ac4f5bd83ab4ed36}

>[!NOTE]
>
>Als u de Tijd van de Besparing van het Daglicht of een gelijkaardig klok-verschuivend beleid uitvoert, moet u het [!DNL .dst] dossier bewaren dat de aangewezen regels in de *profielnaam*\Dataset\Timezone directory on the [!DNL Insight Server] machine bevat.

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

