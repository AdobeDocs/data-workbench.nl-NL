---
description: Informatie over de codes en notaties voor tijdzones.
title: Tijdzonecodes
uuid: 5698882a-9682-41d8-88d3-8471578a22cc
exl-id: 2829c4ca-af6f-4ddb-acce-b33c3b552ba7
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '376'
ht-degree: 2%

---

# Tijdzonecodes{#time-zone-codes}

Informatie over de codes en notaties voor tijdzones.

De meeste op tijd gebaseerde parameters in de server van de gegevenswerkbank worden gespecificeerd in het volgende formaat:

* DD maand, YYYY HH:MM:SS Tone
* Voorbeeld: 13 augustus 2013 22:30:00 EST

Tijdzones worden uitgedrukt in een systeemonafhankelijk tijdzoneformaat (Coordinated Universal Time) met de volgende notatie:

* UTC + humstralen

Het teken (+) kan een plusteken (+) of een minteken (-) zijn, en hhm is de verschuiving van UTC in uren en minuten. De facultatieve veranderlijke parameters specificeert een reeks regels om de Tijd van de Besparing van het Daglicht of een gelijkaardig klok-veranderende beleid uit te voeren.

Als u modules opgeeft, moet een door tabs gescheiden bestand met de naam [!DNL dstrules.dst] aanwezig zijn in de map Dataset\TimeZone van het profiel [!DNL Base] (voor configuratiebestanden die niet zijn gekoppeld aan een bepaalde dataset) of het gegevenssetprofiel (voor configuratiebestanden die specifiek zijn voor gegevenssets). In het bestand wordt een tijdzoneonafhankelijke set regels voor zomertijd opgegeven. Je kunt verschillende regels hebben voor verschillende jaren. In het [!DNL DST.dst]-bestand dat door Adobe in het [!DNL Base]-profiel wordt aangeboden, worden de standaard Amerikaanse regels vastgelegd in de Energy Policy Act van 2005 (die in feite van kracht is vanaf 2007) en de Amerikaanse regels voor voorgaande jaren.

Hier worden voorbeelden van tijdzone-items vermeld:

* U.S. Eastern Daylight Time: Tijdzone = tekenreeks: UTC -0500 DST
* UTC-tijd zonder verschuiving en zonder parameters (overeenkomend met GMT): Tijdzone = tekenreeks: UTC -0000

Wanneer dit formaat wordt gebruikt, moet de systeemtijdzone van de server van de gegevenswerkbank, gegevenswerkbank, en de machines van het Rapport niet het zelfde als de gespecificeerde tijdzone zijn. Bovendien hoeven voor alle actieve gegevenssetprofielen op een werkbankservercomputer niet dezelfde tijdzone-instelling te worden ingesteld.

De volgende tabel bevat de lijst met codes die u kunt gebruiken om tijdzones op te geven in op tijd gebaseerde parameters.

## Tijdzonecode tabel {#section-b4f965b872c543e2ac52a3c94410d076}

Als u zomertijd of een gelijkaardig klok-veranderende beleid uitvoert, moet u [!DNL .dst] dossier opslaan die de aangewezen regels in de profielnaam [!DNL \Dataset\Timezone] folder op de machine van de gegevenswerkbankserver bevat.

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
