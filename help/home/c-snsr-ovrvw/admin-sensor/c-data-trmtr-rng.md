---
description: Controleer of de zender actief is door waarschuwingen in te stellen, de systeemstatus van de sensor te controleren en nog veel meer.
title: Bevestigend dat de Transmitter van Gegevens loopt
uuid: 8dd6307c-e7d2-4800-88c7-f93385b33ca5
exl-id: 10ba704e-85be-425f-8a5d-9429100f367d
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '276'
ht-degree: 0%

---

# Bevestigend dat de Transmitter van Gegevens loopt{#confirming-that-the-data-transmitter-is-running}

{{eol}}

Controleer of de zender actief is door waarschuwingen in te stellen, de systeemstatus van de sensor te controleren en nog veel meer.

**Aanbevolen frequentie:** Elke 5-10 minuten

* [Controleer of het verzendproces actief is.](../../../home/c-snsr-ovrvw/admin-sensor/c-data-trmtr-rng.md#section-79806fa3b7034a8eaf571a66e24874d7)
* [Stel beheerderswaarschuwingen in op Insight Server.](../../../home/c-snsr-ovrvw/admin-sensor/c-data-trmtr-rng.md#section-d98e0f18b8fb45a78419fe75610a3b1e)
* [Controleer de systeemstatus van de sensor.](../../../home/c-snsr-ovrvw/admin-sensor/c-data-trmtr-rng.md#section-de9d7e359242487a9fbead4ed65aebbc)

## Het verzendingsproces controleren {#section-79806fa3b7034a8eaf571a66e24874d7}

Één manier om te verifiëren dat de zender loopt is te controleren dat de [!DNL Sensor] verzendproces wordt uitgevoerd op elke webserver waarop een [!DNL Sensor] -instantie is geïnstalleerd. Het verzendproces wordt als &#39;txlogd&#39; weergegeven in de lijst met processen van de webserver. U kunt deze controle uitvoeren met behulp van een systeemcontroleprogramma.

## Het Administratieve Alarm van de vestiging in de Server van de Data Workbench {#section-d98e0f18b8fb45a78419fe75610a3b1e}

Een andere manier om te controleren of de zender actief is, is het instellen van geautomatiseerde administratieve waarschuwingen in de [!DNL data workbench server]. Wanneer het administratieve alarm is gevormd, [!DNL data workbench server] genereert een e-mailwaarschuwing wanneer deze geen gegevens heeft ontvangen van een geconfigureerde en eerder verbonden [!DNL Sensor] binnen de in de [!DNL Sensor] De parameter Timeout (min) van de alarm in [!DNL data workbench server’s] [!DNL Administrative Alerts.cfg] bestand. Voor meer informatie over het instellen van administratieve waarschuwingen raadpleegt u de *Handleiding voor installatie en beheer van serverproducten*.

## De systeemstatus van de sensor controleren {#section-de9d7e359242487a9fbead4ed65aebbc}

Nog een andere manier om te verifiëren dat de zender in werking wordt gesteld is manueel te controleren [!DNL Servers Manager] in de Data Workbench.

**Als u het dialoogvenster[!DNL Servers Manager]**

* Klik in Data Workbench met de rechtermuisknop in een werkruimte en klik op **[!UICONTROL Admin]** vervolgens onder [!DNL Manage], klikt u op **[!UICONTROL Servers]**.

Als het pictogram voor een [!DNL Sensor] groen is, de zender wordt uitgevoerd.

Voor meer informatie over de [!DNL Servers Manager], zie het hoofdstuk Administratieve Interfaces van *Data Workbench [!DNL Sensor] Hulplijn*.
