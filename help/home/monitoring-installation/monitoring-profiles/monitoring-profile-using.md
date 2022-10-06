---
description: Het statusprofiel van het gegevenswerkbankprofiel biedt huidige informatie over de serverstatus van de gegevenswerkbank op basis van het profiel in plaats van serverwaarden of historische gegevens.
title: De werkruimte Status profiel Data Workbench
uuid: b54713c8-863d-4376-8ebf-4a2985e28c76
exl-id: 40b9b0bf-4fd9-48d8-875b-514921c520cd
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '217'
ht-degree: 0%

---

# De werkruimte Status profiel Data Workbench{#data-workbench-profile-status-workspace}

{{eol}}

Het statusprofiel van het gegevenswerkbankprofiel biedt huidige informatie over de serverstatus van de gegevenswerkbank op basis van het profiel in plaats van serverwaarden of historische gegevens.

## Status van profiel Data Workbench {#section-65d1fa393cfd450cbacef3cba823fcc1}

Dit statusprofiel biedt de serverinformatie van de gegevenswerkbank die actueel is, maar niet echt real-time omdat de agent elke tien minuten wordt gepolled en de rapportage altijd deze latentie van tien minuten omvat. Meer bepaald, verstrekken de datasets die door dit profiel worden geproduceerd de recentste observatie van de server van de agent, die het vaakst een standaardopiniepeilingsperiode van tien minuten heeft.

Zie voor meer informatie over de afmetingen die worden gebruikt in het statusprofiel van het gegevenswerkbank Profile [Status profiel van zichtprofiel](../../../home/monitoring-installation/monitoring-profiles/monitoring-profile-using.md#concept-d4cd7da41c8a42bab4aea25418264e64).

![](assets/Status_General_Status.png)

Dit rapport is meer voor het controleren van verrichtingen dan componenten of specifieke verkeersschommelingen.

![](assets/Status_General_page.png)

Dit geeft ons een idee wie in welke modus is: Als er een hoge snelheid bij invoer voor een bepaald profiel wordt weergegeven, bevindt dat profiel zich in de modus Snelinvoer.

Als Geroepen metrisch 1 is, dan wordt de server geïnstalleerd. Als de waarde 0 is, dan wordt de server niet geïnstalleerd.

**Logboek lezen voor grote batchladingen**

![](assets/Status_General_stalled_log.png)
