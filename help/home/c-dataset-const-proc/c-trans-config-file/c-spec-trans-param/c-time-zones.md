---
description: De parameter van de Streek van de Tijd in het dossier Transformation.cfg controleert tijddimensies, tijdomzettingen (bijvoorbeeld, bepalend het x-lokaal-timekoordgebied), en het formatteren van alle lokale tijden in het datasetprofiel.
solution: Analytics
title: Tijdzones
topic: Data workbench
uuid: 7b253c5a-f2b1-410c-9433-f13ed1d7a8b3
translation-type: tm+mt
source-git-commit: 27600561841db3705f4eee6ff0aeb8890444bbc9

---


# Tijdzones{#time-zones}

De parameter van de Streek van de Tijd in het dossier Transformation.cfg controleert tijddimensies, tijdomzettingen (bijvoorbeeld, bepalend het x-lokaal-timekoordgebied), en het formatteren van alle lokale tijden in het datasetprofiel.

>[!NOTE]
>
>De parameter van de Streek van de Tijd beïnvloedt systeem-vlakke functionaliteit zoals timestamps in status en gebeurtenislogboeken niet, die in systeem lokale tijd worden uitgedrukt.

De parameter van de Streek van de Tijd steunt een systeem-onafhankelijk formaat van de tijdzone (&quot;Gecoördineerde Universele Tijd&quot;) van het volgende formaat:

Tijdzone = tekenreeks: UTC + hhmm-dstralen

Het teken (+) kan of plus (+) of een minus (-) teken zijn, en *hhmm* is de compensatie van UTC in uren en notulen. De facultatieve variabele *modules* specificeren een reeks regels om de Tijd van de Besparing van het Daglicht of een gelijkaardig klok-veranderend beleid uit te voeren.

Als u *modules* specificeert, moet een lusje-afgebakend dossier genoemd aanwezig [!DNL dstrules .dst] zijn binnen subdirectory van de Dataset \ TimeZone van het datasetprofiel. Het dossier specificeert een tijdzone onafhankelijke reeks regels voor de Tijd van de Besparing van het Daglicht. Je kunt verschillende regels hebben voor verschillende jaren. Het [!DNL DST.dst] dossier dat door Adobe in het profiel van de Basis wordt verstrekt specificeert de standaardregels van de V.S. die door de Akte van het Beleid van de Energie van 2005 (in feite beginnend 2007) worden vastgesteld en de regels van de V.S. voor voorafgaande jaren.

De ingangen van de Tijdzone van de steekproef zijn hieronder vermeld:

* US Eastern Daylight Time: Tijdzone = tekenreeks: UTC -0500 DST
* UTC-tijd zonder offset en zonder stralen: Tijdzone = tekenreeks: UTC -0000

Wanneer dit formaat wordt gebruikt, de streek van de systeemtijd van de server van de gegevenswerkbank, de gegevenswerkbank, en de machines te hoeven niet het zelfde als de gespecificeerde tijdzone te zijn. [!DNL Report] Bovendien moeten alle actieve datasetprofielen op een de servermachine van de gegevenswerkbank niet het zelfde tijdzone plaatsen hebben.

Adobe adviseert niet lopend meer dan één datasetprofiel op één enkele de servermachine van de gegevenswerkbank of cluster van de gegevenswerkbankserver.

De werkbankgebruikers van gegevens zullen gegevens in de de tijdzone van het datasetprofiel in plaats van hun streek van de systeemtijd zien. Adobe adviseert dat de streek van de systeemtijd voor een de servermachine van de gegevenswerkbank het zelfde als de tijdzone is die in zijn datasets wordt gebruikt.

>[!NOTE]
>
>U kunt een parameter van de Streek van de Tijd in het [!DNL Log Processing.cfg] dossier specificeren, waar het voor tijdomzettingen tijdens logboekverwerking wordt gebruikt. Voor informatie over de parameter van de Streek van de Tijd in het [!DNL Log Processing.cfg] dossier, zie het Dossier van de Configuratie van de [Verwerking van het Logboek](../../../../home/c-dataset-const-proc/c-log-proc-config-file/c-abt-log-proc-config-file.md).

