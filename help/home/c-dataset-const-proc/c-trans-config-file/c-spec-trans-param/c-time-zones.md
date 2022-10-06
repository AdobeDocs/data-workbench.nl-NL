---
description: De parameter van de Tijdzone in het dossier Transformation.cfg controleert tijddimensies, tijdomzettingen (bijvoorbeeld, bepalend het x-lokaal-timekoordgebied), en het formatteren van alle lokale tijden in het datasetprofiel.
title: Tijdzones
uuid: 7b253c5a-f2b1-410c-9433-f13ed1d7a8b3
exl-id: c8dc49d5-3245-428a-bfb9-42970df73d3e
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '396'
ht-degree: 1%

---

# Tijdzones{#time-zones}

{{eol}}

De parameter van de Tijdzone in het dossier Transformation.cfg controleert tijddimensies, tijdomzettingen (bijvoorbeeld, bepalend het x-lokaal-timekoordgebied), en het formatteren van alle lokale tijden in het datasetprofiel.

>[!NOTE]
>
>De parameter van de Zone van de Tijd beïnvloedt systeem-vlakke functionaliteit zoals timestamps in status en gebeurtenislogboeken, die in systeem lokale tijd worden uitgedrukt.

De parameter van de Zone van de Tijd steunt een systeem-onafhankelijke formaat van de tijdzone (&quot;Coordinated Universal Time&quot;) van het volgende formaat:

Tijdzone = tekenreeks: UTC + humstralen

Het teken (+) kan een plusteken (+) of een minteken (-) zijn, en *hmmhmmhhhhhhumhhumhhumhumhumhumhumhumhumhumhumhumhumhumhumhumhumhumhumhumhhumhumhumhumhumhumhumhhuhhhhuhhhhhmhhhhhhhhhhhhhhhhhhhhhhmhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhmhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhh* is de verschuiving van UTC in uren en minuten. De optionele variabele *dstralen* Hiermee geeft u een set regels op voor het uitvoeren van zomertijd of een vergelijkbaar beleid voor het verschuiven van de klok.

Als u *dstralen*, een door tabs gescheiden bestand met de naam [!DNL dstrules .dst] moet aanwezig zijn binnen de subdirectory Dataset\TimeZone van het profiel van de dataset. In het bestand wordt een tijdzoneonafhankelijke set regels voor zomertijd opgegeven. Je kunt verschillende regels hebben voor verschillende jaren. De [!DNL DST.dst] bestand dat door Adobe in het basisprofiel wordt verschaft, specificeert de standaard Amerikaanse regels die zijn vastgelegd in de Energy Policy Act van 2005 (die in feite van kracht is vanaf 2007) en de Amerikaanse regels voor voorgaande jaren.

De items in de tijdzone van het voorbeeld worden hieronder weergegeven:

* U.S. Eastern Daylight Time: Tijdzone = tekenreeks: UTC -0500 DST
* UTC-tijd zonder verschuiving en zonder kenmerken: Tijdzone = tekenreeks: UTC -0000

Wanneer dit formaat wordt gebruikt, de systeemtijdzone van de server van de gegevenswerkbank, gegevenswerkbank, en [!DNL Report] machines hoeven niet hetzelfde te zijn als de opgegeven tijdzone. Bovendien hoeven voor alle actieve gegevenssetprofielen op een werkbankservercomputer niet dezelfde tijdzone-instelling te worden ingesteld.

Adobe raadt niet aan meer dan één gegevenssetprofiel uit te voeren op één gegevenswerkbankservercomputer of gegevenswerkbench servercluster.

De werkbankgebruikers van gegevens zullen gegevens in de de tijdzone van het datasetprofiel in plaats van hun systeemtijdzone zien. Adobe adviseert dat de systeemtijdzone voor een machine van de gegevenswerkbankserver het zelfde als de tijdzone is die in zijn datasets wordt gebruikt.

>[!NOTE]
>
>U kunt een parameter Tijdzone opgeven in het dialoogvenster [!DNL Log Processing.cfg] bestand, waarbij het wordt gebruikt voor tijdconversies tijdens de logbestandverwerking. Voor informatie over de parameter Tijdzone in het dialoogvenster [!DNL Log Processing.cfg] bestand, zie [Logboekverwerkingsconfiguratiebestand](../../../../home/c-dataset-const-proc/c-log-proc-config-file/c-abt-log-proc-config-file.md).
