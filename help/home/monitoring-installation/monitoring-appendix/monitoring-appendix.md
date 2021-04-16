---
description: In dit document worden de profielen beschreven met de velden, afmetingen en metriek die worden gebruikt door het controleprofiel van de gegevenswerkbank.
title: Dimension en cijfers voor profiel Data Workbench
uuid: 42ef154f-fd8b-4609-8685-96d9dbf32a3d
exl-id: cfad9897-2ea3-47e4-aa36-416e0fde9358
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '233'
ht-degree: 0%

---

# Data Workbench Profile Dimension and Metrics{#data-workbench-profile-dimensions-and-metrics}

In dit document worden de profielen beschreven met de velden, afmetingen en metriek die worden gebruikt door het controleprofiel van de gegevenswerkbank.

Om gegevens te controleren werkbankservers, worden de gegevens verzameld gebruikend een manuscript dat de Gedetailleerde Status ontleedt terwijl ook het vangen van specifieke serverinformatie. Gegevens werkbankgegevens worden vervolgens doorgegeven aan een pagina-tagaanroep van de gegevenswerkbankensor om deze te verzamelen en op te slaan naar een VSL bestand.

## Profielen die worden gebruikt door het monitorprofiel {#section-b5b1234f55c3407dae8e68b031b7cd7f} van de Data Workbench

Deze profielen bieden afmetingen en metriek waarmee u de status en prestatiegegevens van de server kunt weergeven:

* [Dimension in het statusprofiel van het profiel Insight](../../../home/monitoring-installation/monitoring-appendix/monitoring-profile-status.md#concept-d4cd7da41c8a42bab4aea25418264e64)
* [Dimension in het statusprofiel van de Insight Server](../../../home/monitoring-installation/monitoring-appendix/monitoring-servers-profile.md#concept-8cbeb91e99bc42e2b52b22d551423f8a)
* [Dimension in het historisch profiel van het Inzicht](../../../home/monitoring-installation/monitoring-appendix/monitoring-historical.md#concept-a42837c9c9274f83ad5bc5a6720f02b0)
* [Metriek in het historisch controleprofiel van het Inzicht](../../../home/monitoring-installation/monitoring-appendix/monitoring-hist-metrics.md#concept-8fece88b1f014637bbc7c8372ee93203)

Met de statusprofielen kunt u zien hoe de werkbank voor gegevens momenteel vanuit een operationeel perspectief presteert. Het profiel **Profielstatus** en het profiel **Serverstatus** verzamelen gegevens van de gedetailleerde status en de servers van de gegevenswerkbank. Alle verzamelde gegevens worden in het veld `cs-uri-query` geplaatst voor gebruik.

Met de **Historische profielen** kunt u het effect van configuratie- en hardwarewijzigingen beoordelen aan de hand van historische gegevens. Het historische profiel kan het nuttigst zijn omdat het u toestaat om het effect van configuratie en hardwareveranderingen in tijd te beoordelen.
