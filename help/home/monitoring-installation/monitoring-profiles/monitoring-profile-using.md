---
description: Het profiel Profielstatus van de gegevenswerkbank biedt actuele informatie over de serverstatus van de gegevenswerkbank op basis van het profiel in plaats van servergegevens of historische gegevens.
solution: Analytics
title: Werkruimte voor status van gegevenswerkbankprofiel
topic: Data workbench
uuid: b54713c8-863d-4376-8ebf-4a2985e28c76
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Werkruimte voor status van gegevenswerkbankprofiel{#data-workbench-profile-status-workspace}

Het profiel Profielstatus van de gegevenswerkbank biedt actuele informatie over de serverstatus van de gegevenswerkbank op basis van het profiel in plaats van servergegevens of historische gegevens.

## Status van gegevenswerkbankprofiel {#section-65d1fa393cfd450cbacef3cba823fcc1}

Dit statusprofiel verstrekt de de serverinformatie van de gegevenswerkbank die huidig is, maar niet vrij real-time omdat de agent om de tien minuten wordt gepolled en de rapportering omvat altijd deze tien-minieme latentie. Meer bepaald, verstrekken de datasets die door dit profiel worden geproduceerd de recentste waarneming van de server van de agent, die het vaakst een standaardopiniepeilingsperiode van tien minuten heeft.

Zie het profiel [van de status van het profiel van het](../../../home/monitoring-installation/monitoring-profiles/monitoring-profile-using.md#concept-d4cd7da41c8a42bab4aea25418264e64)zichtprofiel van het zichtprofiel van het gezichtsveld voor meer informatie over de afmetingen die worden gebruikt in het profiel van de profielstatus van de gegevenswerkbank.

![](assets/Status_General_Status.png)

Dit verslag is meer bedoeld voor het monitoren van operaties dan voor componenten of specifieke verkeersfluctuaties.

![](assets/Status_General_page.png)

Dit geeft ons een gevoel van wie in welke wijze is: Als we een hoge snelheid bij de invoer voor een bepaald profiel zien, wordt dat profiel in de modus Snelle invoer weergegeven.

Als Verpletterd metrisch 1 is, dan wordt de server geblokkeerd. Als de waarde 0 is, dan wordt de server niet gestormd.

**De Lezing van het logboek voor grote partijladingen**

![](assets/Status_General_stalled_log.png)

