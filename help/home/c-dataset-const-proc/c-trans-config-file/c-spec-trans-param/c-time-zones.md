---
description: De parameter van de Tijdzone in het dossier Transformation.cfg controleert tijddimensies, tijdomzettingen (bijvoorbeeld, bepalend het x-lokaal-timekoordgebied), en het formatteren van alle lokale tijden in het datasetprofiel.
title: Tijdzones
uuid: 7b253c5a-f2b1-410c-9433-f13ed1d7a8b3
exl-id: c8dc49d5-3245-428a-bfb9-42970df73d3e
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '396'
ht-degree: 1%

---

# Tijdzones{#time-zones}

De parameter van de Tijdzone in het dossier Transformation.cfg controleert tijddimensies, tijdomzettingen (bijvoorbeeld, bepalend het x-lokaal-timekoordgebied), en het formatteren van alle lokale tijden in het datasetprofiel.

>[!NOTE]
>
>De parameter van de Zone van de Tijd beïnvloedt systeem-vlakke functionaliteit zoals timestamps in status en gebeurtenislogboeken, die in systeem lokale tijd worden uitgedrukt.

De parameter van de Zone van de Tijd steunt een systeem-onafhankelijke formaat van de tijdzone (&quot;Coordinated Universal Time&quot;) van het volgende formaat:

Tijdzone = tekenreeks: UTC + humstralen

Het teken (+) kan een plusteken (+) of een minteken (-) zijn, en *hhm* is de compensatie van UTC in uren en notulen. De facultatieve variabele *dstrules* specificeert een reeks regels om de Tijd van de Besparing van het Daglicht of een gelijkaardig klok-veranderende beleid uit te voeren.

Als u *dstrules* specificeert, moet een lusje-afgebakend dossier genoemd [!DNL dstrules .dst] binnen de Dataset \ TimeZone subdirectory van de datasetprofiel aanwezig zijn. In het bestand wordt een tijdzoneonafhankelijke set regels voor zomertijd opgegeven. Je kunt verschillende regels hebben voor verschillende jaren. In het [!DNL DST.dst]-bestand dat door Adobe in het basisprofiel wordt aangeboden, worden de standaard Amerikaanse regels opgegeven die zijn vastgelegd in de Energy Policy Act van 2005 (in feite vanaf 2007) en de Amerikaanse regels voor voorgaande jaren.

De items in de tijdzone van het voorbeeld worden hieronder weergegeven:

* U.S. Eastern Daylight Time: Tijdzone = tekenreeks: UTC -0500 DST
* UTC-tijd zonder verschuiving en zonder kenmerken: Tijdzone = tekenreeks: UTC -0000

Wanneer deze indeling wordt gebruikt, hoeft de tijdzone van de systeemwerkbankserver, de gegevenswerkbank en [!DNL Report] niet gelijk te zijn aan de opgegeven tijdzone. Bovendien hoeven voor alle actieve gegevenssetprofielen op een werkbankservercomputer niet dezelfde tijdzone-instelling te worden ingesteld.

Adobe raadt niet aan meer dan één gegevenssetprofiel uit te voeren op één gegevenswerkbankservercomputer of gegevenswerkbench servercluster.

De werkbankgebruikers van gegevens zullen gegevens in de de tijdzone van het datasetprofiel in plaats van hun systeemtijdzone zien. Adobe adviseert dat de systeemtijdzone voor een machine van de gegevenswerkbankserver het zelfde als de tijdzone is die in zijn datasets wordt gebruikt.

>[!NOTE]
>
>U kunt een parameter van de Tijdzone in het [!DNL Log Processing.cfg] dossier specificeren, waar het voor tijdomzettingen tijdens logboekverwerking wordt gebruikt. Voor informatie over de parameter van de Tijdzone in het [!DNL Log Processing.cfg] dossier, zie [Dossier van de Configuratie van de Verwerking van het Logboek](../../../../home/c-dataset-const-proc/c-log-proc-config-file/c-abt-log-proc-config-file.md).
