---
description: Dit document beschrijft de profielen met hun gebieden, afmetingen, en metriek die door het Profiel van de Controle van de gegevenswerkbank worden gebruikt.
solution: Analytics
title: Afmetingen en statistieken van het profiel van de gegevenswerkbank
topic: Data workbench
uuid: 42ef154f-fd8b-4609-8685-96d9dbf32a3d
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Afmetingen en statistieken van het profiel van de gegevenswerkbank{#data-workbench-profile-dimensions-and-metrics}

Dit document beschrijft de profielen met hun gebieden, afmetingen, en metriek die door het Profiel van de Controle van de gegevenswerkbank worden gebruikt.

Om de servers van de gegevenswerkbank te controleren, wordt het gegeven verzameld gebruikend een manuscript dat de Gedetailleerde Status ontleedt terwijl ook het vangen van specifieke serverinformatie. De de serverinformatie van de werkbank van gegevens wordt dan overgegaan tot een vraag van de paginarag naar de sensor van de gegevenswerkbank om aan een VSL- dossier te verzamelen en op te slaan.

## Profielen die door het Profiel van de Controle van de Werkbank van Gegevens worden gebruikt {#section-b5b1234f55c3407dae8e68b031b7cd7f}

Deze profielen verstrekken afmetingen en metriek die u toestaan om serverstaat en prestatiesgegevens te bekijken:

* [Afmetingen in het profiel Status van het Profiel van het Inzicht](../../../home/monitoring-installation/monitoring-appendix/monitoring-profile-status.md#concept-d4cd7da41c8a42bab4aea25418264e64)
* [Afmetingen in het profiel Insight Server Status](../../../home/monitoring-installation/monitoring-appendix/monitoring-servers-profile.md#concept-8cbeb91e99bc42e2b52b22d551423f8a)
* [Afmetingen in het historisch profiel van het Inzicht](../../../home/monitoring-installation/monitoring-appendix/monitoring-historical.md#concept-a42837c9c9274f83ad5bc5a6720f02b0)
* [Metriek in het Historische Profiel van de Controle van het Inzicht](../../../home/monitoring-installation/monitoring-appendix/monitoring-hist-metrics.md#concept-8fece88b1f014637bbc7c8372ee93203)

De profielen van de Status staan u toe om te zien hoe de gegevenswerkbank momenteel vanuit een operationeel perspectief presteert. Het profiel **Profielstatus** en het profiel voor de **serverstatus** verzamelen gegevens van de gedetailleerde status en de servers van de gegevenswerkbank. Alle verzamelde gegevens worden geplaatst in het `cs-uri-query` gebied voor gebruik.

De **Historische profielen** staan u toe om het effect van configuratie en hardwareveranderingen te beoordelen gebruikend historische gegevens. Het historische profiel kan het nuttigst zijn omdat het u toestaat om het effect van configuratie en hardwareveranderingen in tijd te beoordelen.
