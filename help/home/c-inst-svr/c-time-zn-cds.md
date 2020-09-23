---
description: Instructies van het formaat over op tijd-gebaseerde parameters in de Server van het Inzicht.
solution: Analytics
title: Tijdzonecodes
uuid: dcc8aa15-5846-4f24-8b82-e25ff89871ba
translation-type: tm+mt
source-git-commit: 34cdcfc83ae6bb620706db37228e200cff43ab2c
workflow-type: tm+mt
source-wordcount: '364'
ht-degree: 2%

---


# Tijdzonecodes{#time-zone-codes}

Instructies van het formaat over op tijd-gebaseerde parameters in de Server van het Inzicht.

De meeste op tijd gebaseerde parameters in [!DNL Insight Server] worden gespecificeerd in het volgende formaat:

*DD maand, YYYY HH:MM:SS TimeZone*

Voorbeeld: 13 augustus 2013 22:30:00 EST

Tijdzones worden uitgedrukt in een systeemonafhankelijk tijdzoneformaat (Coordinated Universal Time) met de volgende notatie:

UTC + *humstrules*

Het teken (+) kan een plusteken (+) of een minteken (-) zijn, en *hhm* is de verschuiving van UTC in uren en minuten. De facultatieve veranderlijke *variabelen* specificeren een reeks regels om de Tijd van de Besparing van het Daglicht of een gelijkaardig klok-veranderende beleid uit te voeren.

Als u *termijnen* specificeert, een lusje-afgebakend dossier genoemd *&lt;[!DNL dstrules]>* [!DNL .dst] moet binnen de folder van Dataset \ TimeZone van of het profiel van de Basis (voor configuratiedossiers die niet met een bepaalde dataset worden geassocieerd) of het datasetprofiel (voor configuratiedossiers aanwezig zijn die dataset-specifiek zijn). In het bestand wordt een tijdzoneonafhankelijke set regels voor zomertijd opgegeven. Je kunt verschillende regels hebben voor verschillende jaren. In het [!DNL DST.dst] bestand dat door Adobe in het basisprofiel wordt verschaft, worden de standaardregels van de VS vastgelegd in de Energy Policy Act van 2005 (in feite vanaf 2007) en de regels van de VS voor voorgaande jaren.

Hier worden voorbeelden van tijdzone-items vermeld:

* U.S. Eastern Daylight Time: Tijdzone = tekenreeks: UTC -0500 DST
* UTC-tijd zonder verschuiving en zonder *details* (overeenkomend met GMT): Tijdzone = tekenreeks: UTC -0000

Wanneer deze indeling wordt gebruikt, hoeft de tijdzone van het systeem [!DNL Insight Server], [!DNL Insight]en de [!DNL Report] machines niet gelijk te zijn aan de opgegeven tijdzone. Bovendien hoeven voor alle actieve gegevenssetprofielen op een [!DNL Insight Server] computer niet dezelfde tijdzone-instelling te gelden.

De volgende tabel bevat de lijst met codes die u kunt gebruiken om tijdzones op te geven in op tijd gebaseerde parameters.

## Tijdzonecode tabel {#section-3cab225b864f4e54ac4f5bd83ab4ed36}

>[!NOTE]
>
>Als u de Tijd van de Besparing van het Daglicht of een gelijkaardig klok-veranderende beleid uitvoert, moet u het [!DNL .dst] dossier opslaan dat de aangewezen regels in de *profielnaam*\Dataset\Timezone directory on the [!DNL Insight Server] machine bevat.

| Code | Tijdzone | Verschuiving vanaf GMT |
|---|---|---|
| gmt | Greenwich Mean | 0 |
| testen | Eastern Standard | 5 |
| edt | Oosters daglicht | 5 |
| cst | Centrale standaard | 6 |
| cdt | Centraal daglicht | 6 |
| mst | Mountain Standard | 7 |
| mdt | Berg daglicht | 7 |
| pst | Pacific Standard | 8 |
| pdt | Pacific Daylight | 8 |

