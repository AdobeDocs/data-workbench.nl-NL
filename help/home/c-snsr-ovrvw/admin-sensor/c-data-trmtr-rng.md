---
description: Controleer of de zender actief is door waarschuwingen in te stellen, de systeemstatus van de sensor te controleren en nog veel meer.
title: Bevestigend dat de Transmitter van Gegevens loopt
uuid: 8dd6307c-e7d2-4800-88c7-f93385b33ca5
exl-id: 10ba704e-85be-425f-8a5d-9429100f367d
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '276'
ht-degree: 0%

---

# Bevestigend dat de Transmitter van Gegevens{#confirming-that-the-data-transmitter-is-running} loopt

Controleer of de zender actief is door waarschuwingen in te stellen, de systeemstatus van de sensor te controleren en nog veel meer.

**Aanbevolen frequentie:** elke 5-10 minuten

* [Controleer of het verzendproces actief is.](../../../home/c-snsr-ovrvw/admin-sensor/c-data-trmtr-rng.md#section-79806fa3b7034a8eaf571a66e24874d7)
* [Stel beheerderswaarschuwingen in op Insight Server.](../../../home/c-snsr-ovrvw/admin-sensor/c-data-trmtr-rng.md#section-d98e0f18b8fb45a78419fe75610a3b1e)
* [Controleer de systeemstatus van de sensor.](../../../home/c-snsr-ovrvw/admin-sensor/c-data-trmtr-rng.md#section-de9d7e359242487a9fbead4ed65aebbc)

## Het verzendproces {#section-79806fa3b7034a8eaf571a66e24874d7} controleren

Een manier om te controleren of de zender wordt uitgevoerd, is te controleren of het verzendproces [!DNL Sensor] wordt uitgevoerd op elke webserver waarop een [!DNL Sensor]-instantie is geïnstalleerd. Het verzendproces wordt als &#39;txlogd&#39; weergegeven in de lijst met processen van de webserver. U kunt deze controle uitvoeren met behulp van een systeemcontroleprogramma.

## Administratieve waarschuwingen instellen in de Data Workbench-server {#section-d98e0f18b8fb45a78419fe75610a3b1e}

Een andere manier om te verifiëren dat de zender in werking wordt gesteld is geautomatiseerde administratieve alarm in [!DNL data workbench server]. Wanneer beheerwaarschuwingen zijn geconfigureerd, genereert de [!DNL data workbench server] een e-mailwaarschuwing wanneer deze geen gegevens heeft ontvangen van een geconfigureerd en eerder verbonden [!DNL Sensor] binnen het tijdsbestek dat is opgegeven in de parameter [!DNL Sensor] Alert Timeout (min) in het [!DNL data workbench server’s] [!DNL Administrative Alerts.cfg]-bestand. Voor meer informatie over vestiging administratieve alarm, zie *de Gids van de Installatie en van het Beleid van de Producten van de Server*.

## De systeemstatus van de sensor controleren {#section-de9d7e359242487a9fbead4ed65aebbc}

Nog een andere manier om te verifiëren dat de zender loopt is [!DNL Servers Manager] in Data Workbench manueel te controleren.

**Als u het dialoogvenster[!DNL Servers Manager]**

* Klik in Data Workbench met de rechtermuisknop in een werkruimte, klik op **[!UICONTROL Admin]** en klik vervolgens onder [!DNL Manage] op **[!UICONTROL Servers]**.

Als het pictogram voor een [!DNL Sensor] groen is, wordt de zender uitgevoerd.

Voor meer informatie over [!DNL Servers Manager], zie het Administratieve hoofdstuk van Interfaces van *Data Workbench [!DNL Sensor] Gids*.
