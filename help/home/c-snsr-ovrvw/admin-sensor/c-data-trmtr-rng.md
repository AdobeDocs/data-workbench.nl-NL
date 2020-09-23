---
description: Controleer of de zender actief is door waarschuwingen in te stellen, de systeemstatus van de sensor te controleren en nog veel meer.
solution: Analytics
title: Bevestigend dat de Transmitter van Gegevens loopt
uuid: 8dd6307c-e7d2-4800-88c7-f93385b33ca5
translation-type: tm+mt
source-git-commit: 34cdcfc83ae6bb620706db37228e200cff43ab2c
workflow-type: tm+mt
source-wordcount: '276'
ht-degree: 0%

---


# Bevestigend dat de Transmitter van Gegevens loopt{#confirming-that-the-data-transmitter-is-running}

Controleer of de zender actief is door waarschuwingen in te stellen, de systeemstatus van de sensor te controleren en nog veel meer.

**Aanbevolen frequentie:** Elke 5-10 minuten

* [Controleer of het verzendproces actief is.](../../../home/c-snsr-ovrvw/admin-sensor/c-data-trmtr-rng.md#section-79806fa3b7034a8eaf571a66e24874d7)
* [Stel beheerderswaarschuwingen in op Insight Server.](../../../home/c-snsr-ovrvw/admin-sensor/c-data-trmtr-rng.md#section-d98e0f18b8fb45a78419fe75610a3b1e)
* [Controleer de systeemstatus van de sensor.](../../../home/c-snsr-ovrvw/admin-sensor/c-data-trmtr-rng.md#section-de9d7e359242487a9fbead4ed65aebbc)

## Het verzendingsproces controleren {#section-79806fa3b7034a8eaf571a66e24874d7}

U kunt controleren of de zender actief is door te controleren of het [!DNL Sensor] verzendproces wordt uitgevoerd op elke webserver waarop een [!DNL Sensor] instantie is geïnstalleerd. Het verzendproces wordt als &#39;txlogd&#39; weergegeven in de lijst met processen van de webserver. U kunt deze controle uitvoeren met behulp van een systeemcontroleprogramma.

## Het Administratieve Alarm van de vestiging in de Server van de Data Workbench {#section-d98e0f18b8fb45a78419fe75610a3b1e}

Een andere manier om te verifiëren dat de zender in werking is, is het opzetten van geautomatiseerde administratieve alarm in [!DNL data workbench server]. Wanneer administratieve alarm is gevormd, [!DNL data workbench server] produceert de e-mailalarm wanneer het geen gegevens van gevormd heeft ontvangen en eerder verbonden [!DNL Sensor] binnen het tijdkader dat in de parameter van de [!DNL Sensor] Dringende Tijd (min) in het [!DNL data workbench server’s] [!DNL Administrative Alerts.cfg] dossier wordt gespecificeerd. Voor meer informatie over vestiging administratieve alarm, zie de Gids *van de Installatie en van het Beleid van de Producten van de* Server.

## De systeemstatus van de sensor controleren {#section-de9d7e359242487a9fbead4ed65aebbc}

Nog een andere manier om te verifiëren dat de zender loopt is manueel het [!DNL Servers Manager] in Data Workbench te controleren.

**Als u het dialoogvenster[!DNL Servers Manager]**

* Klik in Data Workbench met de rechtermuisknop in een werkruimte, klik **[!UICONTROL Admin]** en klik vervolgens onder [!DNL Manage]en klik **[!UICONTROL Servers]**.

Als het pictogram voor een [!DNL Sensor] groene kleur is, wordt de zender uitgevoerd.

Voor meer informatie over het [!DNL Servers Manager], zie het Administratieve hoofdstuk van Interfaces van de *Gids[!DNL Sensor]van de* Data Workbench.
