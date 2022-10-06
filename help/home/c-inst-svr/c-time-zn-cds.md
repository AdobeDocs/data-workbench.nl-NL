---
description: Instructies van het formaat over op tijd-gebaseerde parameters in de Server van het Inzicht.
title: Tijdzonecodes (Insight Server)
uuid: dcc8aa15-5846-4f24-8b82-e25ff89871ba
exl-id: d8923b01-24fe-4a70-9800-f2eedf567c6a
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '365'
ht-degree: 2%

---

# Tijdzonecodes{#time-zone-codes}

{{eol}}

Instructies van het formaat over op tijd-gebaseerde parameters in de Server van het Inzicht.

Meest op tijd gebaseerde parameters in [!DNL Insight Server] worden gespecificeerd in de volgende indeling:

*DD maand, YYYY HH:MM:SS TimeZone*

Voorbeeld: 13 augustus 2013 22:30:00 EST

Tijdzones worden uitgedrukt in een systeemonafhankelijk tijdzoneformaat (Coordinated Universal Time) met de volgende notatie:

UTC +humuis *dstralen*

Het teken (+) kan een plusteken (+) of een minteken (-) zijn, en *hmmhmmhhhhhhumhhumhhumhumhumhumhumhumhumhumhumhumhumhumhumhumhumhumhumhumhhumhumhumhumhumhumhumhhuhhhhuhhhhhmhhhhhhhhhhhhhhhhhhhhhhmhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhmhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhh* is de verschuiving van UTC in uren en minuten. De optionele variabele *dstralen* Hiermee geeft u een set regels op voor het uitvoeren van zomertijd of een vergelijkbaar beleid voor het verschuiven van de klok.

Als u *dstralen*, een door tabs gescheiden bestand met de naam *&lt; [!DNL dstrules]>* [!DNL .dst] moet aanwezig zijn binnen de folder van Dataset \ TimeZone van of het profiel van de Basis (voor configuratiedossiers die niet met een bepaalde dataset worden geassocieerd) of het datasetprofiel (voor configuratiedossiers die dataset-specifiek zijn). In het bestand wordt een tijdzoneonafhankelijke set regels voor zomertijd opgegeven. Je kunt verschillende regels hebben voor verschillende jaren. De [!DNL DST.dst] bestand dat door Adobe in het basisprofiel wordt verschaft, specificeert de standaard Amerikaanse regels die zijn vastgelegd in de Energy Policy Act van 2005 (die in feite van kracht is vanaf 2007) en de Amerikaanse regels voor voorgaande jaren.

Hier worden voorbeelden van tijdzone-items vermeld:

* U.S. Eastern Daylight Time: Tijdzone = tekenreeks: UTC -0500 DST
* UTC-tijd zonder verschuiving en zonder *dstralen* (komt overeen met GMT): Tijdzone = tekenreeks: UTC -0000

Wanneer dit formaat wordt gebruikt, de streek van de systeemtijd van [!DNL Insight Server], [!DNL Insight], en [!DNL Report] machines hoeven niet hetzelfde te zijn als de opgegeven tijdzone. Daarnaast worden alle actieve gegevenssetprofielen op een [!DNL Insight Server] de machine hoeft niet dezelfde tijdzone-instelling te hebben.

De volgende tabel bevat de lijst met codes die u kunt gebruiken om tijdzones op te geven in op tijd gebaseerde parameters.

## Tijdzonecode tabel {#section-3cab225b864f4e54ac4f5bd83ab4ed36}

>[!NOTE]
>
>Als u de Tijd van de Besparing van het Daglicht of een gelijkaardig klok-veranderende beleid uitvoert, moet u sparen [!DNL .dst] het dossier met de toepasselijke regels in het *profielnaam*\Dataset\Timezone directory op de [!DNL Insight Server] machine.

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
