---
description: Gebruik het historisch profiel van de gegevenswerkbank om te zien hoe de configuratie, de hardware, en andere veranderingen prestaties, stabiliteit, en servercapaciteit in tijd beïnvloeden.
solution: Analytics
title: Werkbank voor gegevens — Historisch werkgebied
topic: Data workbench
uuid: 61c45cae-f255-4d20-bb6b-f318c8dd8214
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Werkbank voor gegevens — Historisch werkgebied{#data-workbench-historic-workspace}

Gebruik het historisch profiel van de gegevenswerkbank om te zien hoe de configuratie, de hardware, en andere veranderingen prestaties, stabiliteit, en servercapaciteit in tijd beïnvloeden.

Het historische profiel omvat een op profiel-gebaseerde dataset van de Prestaties [van het](../../../home/monitoring-installation/monitoring-profiles/monitoring-historical-using.md#section-184a86f9de054970bf68515bb9dea85d) Profiel en de op server-gebaseerde dataset van de Prestaties [van de](../../../home/monitoring-installation/monitoring-profiles/monitoring-historical-using.md#section-5dad5870384b40e094d50173fcd90a09) Server onder het **[!UICONTROL Performance]** tabel. Dit zijn de het meest meestal gebruikte datasets die voor een voorbij perspectief van de de serverprestaties van de gegevenswerkbank worden bekeken. Bovendien kunt u de [Componenten](../../../home/monitoring-installation/monitoring-profiles/monitoring-historical-using.md#section-5be7223abb384784bafe7b37c764ea66) en de Wijze [van de](../../../home/monitoring-installation/monitoring-profiles/monitoring-historical-using.md#section-5be7223abb384784bafe7b37c764ea66) Verwerking bekijken door de **[!UICONTROL Up Time]** tabel te selecteren.

![](assets/Historic_Performance.png)

Bovendien kunt u de [Componenten](../../../home/monitoring-installation/monitoring-profiles/monitoring-historical-using.md#section-5be7223abb384784bafe7b37c764ea66) en de Wijze [van de](../../../home/monitoring-installation/monitoring-profiles/monitoring-historical-using.md#section-5be7223abb384784bafe7b37c764ea66) Verwerking bekijken door de **[!UICONTROL Up Time]** tabel te selecteren.

Voor extra verwijzingsinformatie over de afmetingen die in het historisch profiel van de gegevenswerkbank worden gebruikt, zie [Afmetingen in het Historische profiel van het Inzicht.](../../../home/monitoring-installation/monitoring-appendix/monitoring-historical.md#concept-a42837c9c9274f83ad5bc5a6720f02b0)

## Werkruimte voor profielprestaties {#section-184a86f9de054970bf68515bb9dea85d}

Deze dataset omvat de volgende relevante metriek voor de controle van de gegevenswerkbank.

* Snelle input MegaBytes per minuut-metriek die zware gegevensinput tijdens aanvankelijke logboekverwerking tonen.
* De snelle Fusie MegaBytes per minuut-metriek die transformatie tonen.

![](assets/Historic_Profile_Performance.png)

>[!NOTE]
>
>Om een echte prestatiesbeoordeling van uw profiel te doen, bekijk tarief eerder dan verstreken kalendertijd. Het tarief wordt gemeten als veranderde waarden tussen opiniepeiling om de tien minuten.

## Werkruimte voor serverprestaties {#section-5dad5870384b40e094d50173fcd90a09}

Deze dataset controleert servermetriek voorbij het werkingsgebied van inbegrepen profielen, en omvat de volgende relevante servermetriek voor de controle van de gegevenswerkbank.

* Geschatte zweepminuten — Geschatte tijd van de vraagresolutie.
* Polllatentie-milliseconden — Indicator van hoe bezige software door te meten is hoeveel lang het vergt om door een volledige cyclus van het onderhouden van elke component te krijgen.

![](assets/Historic_Server_Performance.png)

## Werkruimte onderdelen {#section-5be7223abb384784bafe7b37c764ea66}

Deze dataset wordt gevestigd onder de Omhooggaande Tijd tabel.

![](assets/Up_Time.png)

De dataset van Componenten omvat twee aspecten voor componentengezondheid:

* Metrische communicatie — Reageerde het proces van de gegevenswerkbankserver?
* Alle metrische componenten — Boven de Gedetailleerde pagina van de Status is een lijst van componenten de gastheer binnen de de serverprocessen van de gegevenswerkbank onderhoudt. Als om het even welke component in een foutenstaat is dan is het vermeld onder de Componenten in de lijst van de Fout.

![](assets/Up_Time_components.png)

## Werkruimte verwerkingsmodus {#section-3e1dedb9474e4b4ba513240943e76817}

Deze werkruimte wordt gevestigd onder de Omhooggaande Tijd tabel. Deze werkruimte laat u waarnemen hoeveel tijd in snelle input, snelle fusie, en wijzen in real time wordt genomen.

![](assets/Up_Time_Processing_mode.png)

Deze dataset verstrekt belangrijke kenmerken van de serverlading, zoals het identificeren van gegevenslading voor

* Dag van de week (bijvoorbeeld een Snelle Invoersnelheid op dinsdag en woensdag),
* Uur van Dag (welk percentage van de dag is het op Snelle wijze van de Input?)

