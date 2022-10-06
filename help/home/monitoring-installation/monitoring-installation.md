---
description: Richtingen voor het installeren van het gegevenswerkbankmonitorprofiel.
title: Het controleprofiel installeren
uuid: e0d6fc61-d9b9-4c4b-94e1-2acfd0ff4de6
exl-id: 368e489c-75c9-4402-a709-a4f5987459b6
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '1052'
ht-degree: 0%

---

# Het controleprofiel installeren{#installing-the-monitoring-profile}

{{eol}}

Richtingen voor het installeren van het gegevenswerkbankmonitorprofiel.

## Installatiestappen {#section-d4355dbea8a447f48ab168db6ccff612}

1. Vorm een nieuwe instantie van de Sensor alsof het voor geëtiketteerde Webpagina gegevensinzameling zal worden gebruikt. Zorg ervoor dat het bestand zig.gif zich in de hoofdmap van het document van de Sensor-webserver bevindt. Sensor kan op dezelfde host worden uitgevoerd als de monitorprofielen. (Dit is geen kwestie als het gebruiken van een tekstdossier voor dit doel.)

   >[!NOTE]
   >
   >Deze instantie van de Sensor moet aan het ontvangen van slechts verkeer van de Controleagenten worden gewijd. Ook, kan de Sensor worden gevormd om op een verschillende haven in werking te stellen als u een Webserver voor deze inzameling opnieuw gebruikt.

1. In de [!DNL txlogd.conf] bestand is de standaardregel:

   ```
   <b>ContentFilterExclude</b> image/,text/css,application/x-javascript,text/javascript
   ```

   Voor de toepassing Bewakingsprofiel van de gegevenswerkbank (of om het even welke &quot;geëtiketteerde&quot;paginaimplementatie), moet het beeldtype worden verwijderd om via een dossier van het GIF te verzamelen. De bijgewerkte regel is:

   ```
   <b>ContentFilterExclude </b>text/css,application/x-javascript,text/javascript
   ```

1. Kopieer de [!DNL insight_monitor.zip/insight_monitor_agent] naar een tijdelijke locatie.
1. Bijwerken [!DNL insight_monitor_agent.cfg] bestand voor uw omgeving. Volg de opmerkingen in het configuratiebestand:

   **Het configuratiebestand Bewaking:**

   ![](assets/monitor_agent_cfg_sensor.png)

   Bepaal waar u alle informatie verzamelt en URL-adres opgeeft. Dit moet een speciale sensor zijn en geen verkeer behalve deze toepassing ontvangen.

   ![](assets/monitor_agent_cfg_dump.png)

   Er zijn paden die ervan uitgaan dat er een e is: schijf. U kunt dit pad voor uw omgeving wijzigen.

   ![](assets/monitor_agent_cfg_quickcheck.png)

   Soms wanneer een transformatieprofiel wordt uitgevoerd, reageert de werkbank gegevens mogelijk niet. Met deze waarde kunt u een waarschuwing verzenden als het proces driemaal achter elkaar niet reageert. Dit is een manier om valse positieve waarschuwingen te verminderen.

   ![](assets/monitor_agent_cfg_groups.png)

   Hier stelt u de omgeving en groepsafmetingen in. Dit kan van gastheer aan gastheer verschillend zijn.

   Dit is w ![](assets/monitor_agent_cfg_debug.png)Hier kunt u precies zien wat de monitoragent doet door foutenlogboeken in dit pad te bekijken.

   ![](assets/monitor_agent_cfg_tempdb.png)

   Dit is om temp db intern te gebruiken. Het kan worden gewaarschuwd wanneer de capaciteit wordt bereikt. Dit is anders dan fysiek schijfgebruik.

1. Kopieer de *insight_monitor_agent* map naar elke DPU- en FSU-host waarop de gegevensworkbench-server wordt uitgevoerd. De standaardlocatie zoals aangegeven in het configuratiebestand is [!DNL e:\insight_monitor_agent] maar u kunt deze locatie wijzigen .

1. Voeg een Vensters geplande taak toe om de agent om de 10 minuten aan te halen (deze periode wordt verondersteld in de berekeningen van het verwerkingstarief). Het programma is [!DNL e:insight_monitor/insight_monitor_agent.exe]. Het argument is config-dossier e:\insight_monitor\insight_monitor.cfg. Begin in e:\insight_monitor. De gebruiker die de taak uitvoert, moet toestemming hebben om te lezen/schrijven [!DNL e:\insight_monitor] en lees het Win32 OLE-object [!DNL root\CIMV2] (vereist om de de dienstbeginwijze van de gegevenswerkbankserver te verifiëren en het percentage ruimte op lokale schijven te controleren)

1. Bevestig dat het VSL bestand begint te groeien naarmate monitorrecords zich ophopen. Dit zal wat tijd vergen aangezien het verkeersvolume in een kleine installatie uiterst laag zal zijn (elke 10 minuten verzendt de agent slechts één klap voor de gastheer-specifieke gegevens, plus één klap per verwerkingsprofiel).
1. Unzip insight_monitor.zip\profiles\Insight Historisch naar een tijdelijke locatie.
1. Hostnaam bijwerken in [!DNL profile.cfg], [!DNL dataset\cluster.cfg]en de [!DNL dataset\segment export.cfg].

1. Werk de bestanden bij naar de map met gegevenswerkbankprofielen.
1. Logserver en pad bijwerken in [!DNL dataset\log processing.cfg] naar de locatie waar de VSL zich ophopen.
1. [Optioneel] hetzelfde doen met de profielen [!DNL Insight Profile Status] en [!DNL Insight Server Status]. Bovendien moeten de statusprofielen iedere avond opnieuw worden verwerkt met een navolgend venster van twee dagen. Voeg een Windows-geplande taak toe: Het programma is [!DNL e:\insight_monitor\insight_reprocess.exe]. Het argument is [!DNL --profile-path="PATH TO PROFILES\insight profile status" --start-days-ago=2]. Verlaten [!DNL start in] leeg. Een andere geplande taak toevoegen voor *&quot;status van inzichteserver&quot;*. *insight_reprocess.exe* vereist lees-/schrijftoegang tot *logverwerking.cfg* om de begintijd bij te werken.

1. Bovendien moeten de statusprofielen iedere avond opnieuw worden verwerkt met een navolgend venster van twee dagen. Voeg een Windows-geplande taak toe: Het programma is *e:\insight_monitor\insight_reprocess.exe*. Het argument is - [!DNL -profile-path="PATH TO PROFILES\insight profile status" --start-days-ago=2]. Verlaten *beginnen bij* leeg. Een andere geplande taak toevoegen voor [!DNL "insight server status"]. [!DNL insight_reprocess.exe] vereist lees-/schrijftoegang tot [!DNL log processing.cfg] om de begintijd bij te werken. Bevestig dat elk profiel de VSL van de monitor tijdens de accumulatie leest. Nogmaals, zal dit wat tijd-waarschijnlijk uren-wegens het uiterst lage volume vergen.

## Installatieopmerkingen {#section-17722441ab0046fcbcb46b957d56230a}

* **Het controleprofiel configureren in een testomgeving met licentie**. Het testomgevingspakket wordt opgenomen in uw implementatie van de gegevenswerkbank, zodat u de toepassing kunt installeren en configureren. Als het installeren op een productieFSU of server DPU, dan zult u de server moeten vormen om op een afzonderlijke haven te lopen.
* **Een nieuwe sensor implementeren voor het controleprofiel**. U moet een nieuw exemplaar van Sensor installeren op de server waarop het controleprofiel wordt uitgevoerd. Dit is een aanvulling op de productie-instantie van Sensor. (Er zijn geen extra kosten voor het installeren van Sensor op een productie- of niet-productieserver specifiek voor het monitoringprofiel.)
* **De monitoragent uitschakelen tijdens het onderhoud van de werkbank**. Om de uptime en prestatiesmetriek te vermijden, kunt u de wijze van het de dienstbegin aan hand voor de dienst InsightServer (de Server van Omniture Insight) plaatsen. Een handig PowerShell-bevel is *set-service -name insightserver -startuptype manual*. Stel deze na het onderhoud weer in op automatisch: *set-service -name insightserver -startuptype automatic*. Een andere optie is tijdelijk de geplande taak van de monitoragent onbruikbaar te maken.
* **Voor de statusprofielen is een venster aan het einde nodig** om oude hosts en profielen en oude toewijzingen voor het hostprofiel te neerzetten. Nochtans, als de hoeveelheid gebeurtenisgegevens zo klein is dat de gegevenswerkbank het binnen niet zal bufferen, dan kunt u de grootte van het venster vrij een beetje moeten uitbreiden om het aan proces te krijgen.
* **De agent verzamelt het algemene en oudste als-van-tijd van de gedetailleerde status van de gegevenswerkbank**, die in lokale gastheertijd wordt gemeld veronderstellend de tijdstempels van het gebeurtenisgegevenslogboek in UTC (zoals in VSL dossiers) zijn. Als de tijdstempels van de gebeurtenisgegevens zich in een niet-UTC-tijdzone bevinden, wordt de tijdsduur in het resulterende statusprofiel van het Inzichtsprofiel verschoven. Indien **alles** van uw tijdstempels van gebeurtenisgegevens bevindt zich in dezelfde tijdzone die u kunt toevoegen aan *Status\metriek\as van vertragminuten.metrisch*.

* **Twee nieuwe dimensies werden geïntroduceerd om de klant te helpen hun servers groeperen als zij in verschillende staten zijn**, zoals productie, het opvoeren, het testen van servers, en servers in andere staten. Als u bijvoorbeeld &quot;uptime&quot; zoekt, ziet u alleen servers in de productiemodus. Dientengevolge, is de dimensie van de Groep enkel een andere manier om servers voor uw behoeften willekeurig te groeperen. Bijvoorbeeld, in het dossier van de Configuratie van de Controle kunt u plaatsen, welke gastheer uw afdeling, zoals Verrichtingen, Ontwikkeling, of Marketing onderhoudt.
