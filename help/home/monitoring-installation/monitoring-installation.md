---
description: Richtingen voor het installeren van het Profiel van de Controle van de gegevenswerkbank.
solution: Analytics
title: Het controleprofiel installeren
topic: Data workbench
uuid: e0d6fc61-d9b9-4c4b-94e1-2acfd0ff4de6
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Het controleprofiel installeren{#installing-the-monitoring-profile}

Richtingen voor het installeren van het Profiel van de Controle van de gegevenswerkbank.

## Installatiestappen {#section-d4355dbea8a447f48ab168db6ccff612}

1. Vorm een nieuwe instantie van de Sensor alsof het voor geëtiketteerde Web-pagina gegevensinzameling zal worden gebruikt. Zeker ben het dossier zig.gif in de het documentwortel van de het Webserver van de Sensor is. De sensor kan op de zelfde gastheer worden in werking gesteld zoals de monitorprofielen. (Dit is geen kwestie als het gebruiken van een tekstdossier voor dit doel.)

   >[!NOTE]
   >
   >Deze instantie van de Sensor moet aan het ontvangen van slechts verkeer van de Controleagenten worden gewijd. Ook, kan de Sensor worden gevormd om op een verschillende haven te lopen als u een Webserver voor deze inzameling opnieuw probeert.

1. In het [!DNL txlogd.conf] dossier is er de standaardlijn:

   ```
   <b>ContentFilterExclude</b> image/,text/css,application/x-javascript,text/javascript
   ```

   Voor de toepassing van het Profiel van de Controle van de gegevenswerkbank (of om het even welke &quot;geëtiketteerde&quot;paginaimplementatie), moet het beeldtype worden verwijderd om via een GIF- dossier te verzamelen. De bijgewerkte lijn is:

   ```
   <b>ContentFilterExclude </b>text/css,application/x-javascript,text/javascript
   ```

1. Kopieer het [!DNL insight_monitor.zip/insight_monitor_agent] naar een tijdelijke locatie.
1. Het [!DNL insight_monitor_agent.cfg] bestand bijwerken voor uw omgeving. Volg de commentaren binnen het configuratiedossier:

   **Het de configuratiedossier van de Controle:**

   ![](assets/monitor_agent_cfg_sensor.png)

   Bepaal waar u alle informatie verzamelt en URL adres verstrekt. Dit moet een specifieke sensor zijn en zou geen verkeer behalve deze toepassing moeten ontvangen.

   ![](assets/monitor_agent_cfg_dump.png)

   Er zijn wegen veronderstellen er een e is: schijf. U kunt deze weg voor uw milieu willen veranderen.

   ![](assets/monitor_agent_cfg_quickcheck.png)

   Wanneer u een transformatieprofiel uitvoert, reageert de werkbank soms niet meer. Deze waarde laat u een alarm verzenden als drie keer in een rij het proces niet ontvankelijk is. Dit is een manier om vals-positieve waarschuwingen te verminderen.

   ![](assets/monitor_agent_cfg_groups.png)

   Dit is waar u het milieu en groepsdimensies plaatst. Dit kan van gastheer aan gastheer verschillend zijn.

   Dit is wij ![](assets/monitor_agent_cfg_debug.png)hier u kunt precies zien wat de monitoragent doet door foutenlogboeken in deze weg te bekijken.

   ![](assets/monitor_agent_cfg_tempdb.png)

   Dit is om temp db intern te gebruiken. Het kan worden gewaarschuwd wanneer het bereiken van capaciteit. Dit is verschillend dan fysiek schijfgebruik.

1. Kopieer de omslag *insight_monitor_agent* aan elke gastheer DPU en FSU die de server van de gegevenswerkbank in werking stelt. De standaardplaats zoals die in het configuratiedossier wordt vermeld is [!DNL e:\insight_monitor_agent] maar u kunt deze plaats veranderen.

1. Voeg een Vensters geplande taak toe om de agent om de 10 minuten aan te halen (deze periode wordt verondersteld in de berekeningen van het verwerkingstarief). Het programma is [!DNL e:insight_monitor/insight_monitor_agent.exe]. Het argument is config-dossier e:\insight_monitor\insight_monitor.cfg. Begin in e:\insight_monitor. De gebruiker die de taak uitvoert moet toestemming hebben om het voorwerp van Win32 te lezen/te schrijven [!DNL e:\insight_monitor] en te lezen OLE [!DNL root\CIMV2] (die wordt vereist om de het beginwijze van de de dienstdienst van de gegevenswerkbankserver te verifiëren en het percentage ruimte op lokale schijven te controleren)

1. Bevestig dat het VSL- dossier begint te groeien aangezien de monitorverslagen accumuleren. Dit zal wat tijd vergen aangezien het verkeersvolume in een kleine installatie uiterst laag zal zijn (om de 10 minuten verzendt de agent slechts één klap voor de gastheer-specifieke gegevens, plus één klap per verwerkingsprofiel).
1. Unzip insight_monitor.zip\profiles\Insight Historic to a temporary location.
1. De gastheernaam van de update in [!DNL profile.cfg], [!DNL [!DNL dataset\cluster.cfg]], en [!DNL [!DNL dataset\segment export.cfg]].

1. Werk de dossiers aan de folder van de gegevenswerkbankprofielen bij.
1. De het logboekserver en weg van de update binnen [!DNL dataset\log processing.cfg] aan de plaats waar de Sensor VSLs accumuleert.
1. [Naar keuze] doe het zelfde met de profielen [!DNL Insight Profile Status] en [!DNL Insight Server Status]. Bovendien zouden de statusprofielen nightly met het slepen twee dagen venster moeten worden opnieuw verwerkt. Een geplande Windows-taak toevoegen: Het programma is [!DNL e:\insight_monitor\insight_reprocess.exe]. Het argument is [!DNL --profile-path="PATH TO PROFILES\insight profile status" --start-days-ago=2]. Laat [!DNL start in] leeg. Voeg een andere geplande taak voor de status van de *&quot;inzichtserver&quot;* toe. *inzicht_reprocess.exe* vereist lees-schrijftoegang tot *logboek processing.cfg* om de begintijd bij te werken.

1. Bovendien zouden de statusprofielen nightly met het slepen twee dagen venster moeten worden opnieuw verwerkt. Een geplande Windows-taak toevoegen: Het programma is *e:\insight_monitor\insight_reprocess.exe*. Het argument is - [!DNL -profile-path="PATH TO PROFILES\insight profile status" --start-days-ago=2]. Laat *beginnen in* leeg. Voeg een andere geplande taak toe voor [!DNL "insight server status"]. [!DNL insight_reprocess.exe] vereist lees-schrijftoegang om de begintijd bij [!DNL log processing.cfg] te werken. Bevestig dat elk profiel de monitor VSLs leest aangezien zij zich accumuleren. Opnieuw, zal dit wat tijd-waarschijnlijk uren-wegens het uiterst lage volume vergen.

## Installatienotities {#section-17722441ab0046fcbcb46b957d56230a}

* **Het vormen van het Profiel van de Controle in een vergunning gegeven testmilieu**. Het pakket van het testmilieu is inbegrepen met uw implementatie van gegevenswerkbank, die u toestaat om de toepassing te installeren en te vormen. Als het installeren op een productieFSU of server DPU, dan zult u de server moeten vormen om op een afzonderlijke haven te lopen.
* **Het opstellen van een nieuwe sensor specifiek voor het Profiel** van de Controle. U zult een nieuw geval van Sensor aan de server moeten installeren die het Profiel van de Controle in werking stelt. Dit komt bovenop de productie-installatie van Sensor. (Er zijn geen extra kosten voor het installeren van Sensor op of een productie of niet productieserver specifiek voor het Profiel van de Controle.)
* **Schakel de monitoragent uit tijdens het onderhoud** van de gegevenswerkbank. Om te vermijden vervuilend de uptime en prestatiesmetriek, kunt u de wijze van het de dienstbegin aan hand voor de dienstInsightServer (de Server van het Inzicht van het Meubelen) plaatsen. Een handig bevel van PowerShell is *reeks-dienst - naam inzichtserver - startuptype hand*. Stel deze na het onderhoud in op automatisch: de *reeks-dienst - naam inzichtserver - startuptype automatisch*. Een andere optie is de geplande taak van de monitoragent tijdelijk onbruikbaar te maken.
* **De profielen van de Status vergen een het slepen venster** om oude gastheren en profielen evenals oude gastheer-profiel afbeeldingen te laten vallen. Nochtans, als de hoeveelheid gebeurtenisgegevens zo klein is dat de gegevenswerkbank het niet binnen zal bufferen, dan kunt u de grootte van het venster vrij een beetje moeten uitbreiden om het aan proces te krijgen.
* **De agent verzamelt het algemene en oudste zoals-van-tijd van de gedetailleerde status** van de gegevenswerkbank, die in lokale gastheertijd wordt gemeld veronderstellend de de tijdstempels van het gebeurtenisgegevenslogboek in UTC (zoals in VSL- dossiers) zijn. Als de tijdstempels van gebeurtenisgegevens in een niet-UTC tijdzone zijn zal de as-of-tijd in het resulterende profiel van de Status van het Profiel van het Inzicht worden gecompenseerd. Als **elk** van uw de tijdstempels van gebeurtenisgegevens in de zelfde tijdzone zijn kunt u die compensatie aan het Profiel van het *Inzicht toevoegen Status\metrics\as of delay minutes.metric*.

* **Twee nieuwe dimensies werden geïntroduceerd om de klant te helpen hun servers groeperen als zij in verschillende staten**, zoals productie, het opvoeren, het testen van servers, en servers in andere staten zijn. Bijvoorbeeld als u &quot;uptime&quot;zoekt, dan bekijkt u servers slechts op productiemodus. Dientengevolge, is de dimensie van de Groep enkel een andere manier om servers willekeurig voor uw behoeften te groeperen. Bijvoorbeeld, in het dossier van de Configuratie van de Controle kunt u plaatsen, welke gastheer uw afdeling, zoals Verrichtingen, Ontwikkeling, of Marketing onderhoudt.

