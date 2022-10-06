---
description: Gebruik het historisch profiel van de gegevenswerkbank om te zien hoe configuratie, hardware, en andere veranderingen prestaties, stabiliteit, en servercapaciteit in tijd beïnvloeden.
title: De werkruimte Historisch van Data Workbench
uuid: 61c45cae-f255-4d20-bb6b-f318c8dd8214
exl-id: e6d7e924-641e-468c-a828-16ebe1c8724f
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '400'
ht-degree: 0%

---

# De werkruimte Historisch van Data Workbench{#data-workbench-historic-workspace}

{{eol}}

Gebruik het historisch profiel van de gegevenswerkbank om te zien hoe configuratie, hardware, en andere veranderingen prestaties, stabiliteit, en servercapaciteit in tijd beïnvloeden.

Het profiel Historisch bevat een op een profiel gebaseerd profiel [Profielprestaties](../../../home/monitoring-installation/monitoring-profiles/monitoring-historical-using.md#section-184a86f9de054970bf68515bb9dea85d) dataset en op server-gebaseerde [Serverprestaties](../../../home/monitoring-installation/monitoring-profiles/monitoring-historical-using.md#section-5dad5870384b40e094d50173fcd90a09) gegevensset onder de **[!UICONTROL Performance]** tab. Dit zijn de het meest algemeen gebruikte datasets die voor een verleden perspectief van de prestaties van de gegevenswerkbankserver worden bekeken. Bovendien kunt u de [Componenten](../../../home/monitoring-installation/monitoring-profiles/monitoring-historical-using.md#section-5be7223abb384784bafe7b37c764ea66) en [Verwerkingsmodus](../../../home/monitoring-installation/monitoring-profiles/monitoring-historical-using.md#section-5be7223abb384784bafe7b37c764ea66) door **[!UICONTROL Up Time]** tab.

![](assets/Historic_Performance.png)

Bovendien kunt u de [Componenten](../../../home/monitoring-installation/monitoring-profiles/monitoring-historical-using.md#section-5be7223abb384784bafe7b37c764ea66) en [Verwerkingsmodus](../../../home/monitoring-installation/monitoring-profiles/monitoring-historical-using.md#section-5be7223abb384784bafe7b37c764ea66) door **[!UICONTROL Up Time]** tab.

Zie voor meer informatie over de afmetingen die worden gebruikt in het historisch profiel van de werkbank Gegevens [Dimension in het historisch profiel van het Inzicht.](../../../home/monitoring-installation/monitoring-appendix/monitoring-historical.md#concept-a42837c9c9274f83ad5bc5a6720f02b0)

## Werkruimte Profielprestaties {#section-184a86f9de054970bf68515bb9dea85d}

Deze dataset omvat de volgende relevante metriek voor de controle van de gegevenswerkbank.

* Snelle input MegaBytes per minuut-metriek die zware gegevensinput tijdens aanvankelijke logboekverwerking tonen.
* Snel MegaBytes samenvoegen per minuut - maateenheden die transformatie weergeven.

![](assets/Historic_Profile_Performance.png)

>[!NOTE]
>
>Als u een echte prestatiebeoordeling van uw profiel wilt uitvoeren, bekijkt u de snelheid in plaats van de verstreken kalendertijd. De snelheid wordt gemeten als de gewijzigde waarden tussen de opiniepeiling om de tien minuten.

## Werkruimte Serverprestaties {#section-5dad5870384b40e094d50173fcd90a09}

Deze dataset controleert servermetriek voorbij het werkingsgebied van inbegrepen profielen, en omvat de volgende relevante servermetriek voor gegevenswerkbench controle.

* Geschatte duur van controleminuten — Geschatte tijd voor queryresolutie.
* Milliseconden van de Latentie van de opiniepeiling — Indicator van hoe bezige software is door te meten hoe lang het duurt om door een volledige cyclus van het onderhouden van elke component te krijgen.

![](assets/Historic_Server_Performance.png)

## De werkruimte Componenten {#section-5be7223abb384784bafe7b37c764ea66}

Deze dataset wordt gevestigd onder de Up Tijd tabel.

![](assets/Up_Time.png)

De dataset van Componenten omvat twee aspecten voor componentengezondheid:

* Communicatie metrisch — beantwoordde het proces van de gegevenswerkbankserver?
* Alle metrische componenten — Bovenaan de Gedetailleerde pagina van de Status is een lijst van componenten de gastheer binnen de processen van de gegevenswerkbankserver onderhoudt. Als een component zich in een foutstatus bevindt, wordt deze weergegeven onder Componenten in de tabel Error.

![](assets/Up_Time_components.png)

## Werkruimte Verwerkingsmodus {#section-3e1dedb9474e4b4ba513240943e76817}

Deze werkruimte bevindt zich onder het tabblad Up Time. In deze werkruimte kunt u zien hoeveel tijd er wordt besteed in de modus voor snel invoeren, snel samenvoegen en realtime.

![](assets/Up_Time_Processing_mode.png)

Deze dataset verstrekt belangrijke eigenschappen van de serverlading, zoals het identificeren van gegevenslading voor

* Dag van de week (bijvoorbeeld een snelle Invoersnelheid op dinsdag en woensdag),
* Uur van Dag (welk percentage van de dag is het op Snelle wijze van de Input?)
