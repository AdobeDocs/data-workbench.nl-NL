---
description: Controleer of de zender werkt door waarschuwingen in te stellen, de systeemstatus van de sensor te controleren en meer.
solution: Insight
title: Bevestigend dat de Overdracht van Gegevens loopt
uuid: 8dd6307c-e7d2-4800-88c7-f93385b33ca5
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Bevestigend dat de Overdracht van Gegevens loopt{#confirming-that-the-data-transmitter-is-running}

Controleer of de zender werkt door waarschuwingen in te stellen, de systeemstatus van de sensor te controleren en meer.

**Aanbevolen frequentie:** Om de 5-10 minuten

* [Controleer of het verzendproces actief is.](../../../home/c-snsr-ovrvw/admin-sensor/c-data-trmtr-rng.md#section-79806fa3b7034a8eaf571a66e24874d7)
* [Het administratieve alarm van de opstelling in de Server van het Inzicht.](../../../home/c-snsr-ovrvw/admin-sensor/c-data-trmtr-rng.md#section-d98e0f18b8fb45a78419fe75610a3b1e)
* [Controleer de systeemstatus van de sensor.](../../../home/c-snsr-ovrvw/admin-sensor/c-data-trmtr-rng.md#section-de9d7e359242487a9fbead4ed65aebbc)

## Controle van het verzendproces {#section-79806fa3b7034a8eaf571a66e24874d7}

Één manier om te verifiëren dat de zender loopt is te controleren dat het [!DNL Sensor] transmissieproces op elke Webserver loopt waar een [!DNL Sensor] instantie geïnstalleerd is. Het transmissieproces verschijnt als &quot;txlogd&quot;in de lijst van de Webserver van processen. U kunt deze controle uitvoeren gebruikend een systeem controlehulpmiddel.

## De Administratieve Alarm van de vestiging in de Server van de Werkbank van Gegevens {#section-d98e0f18b8fb45a78419fe75610a3b1e}

Een andere manier om te verifiëren dat de zender loopt is aan opstelling geautomatiseerd administratief alarm in het [!DNL data workbench server]. Wanneer het administratieve alarm is gevormd, [!DNL data workbench server] produceert de e-mailwaakzaamheid wanneer het geen gegevens van gevormd heeft ontvangen en eerder [!DNL Sensor] binnen het tijdkader verbonden dat in de [!DNL Sensor] Waakzame parameter van de Onderbreking (min) in het [!DNL data workbench server’s] - [!DNL Administrative Alerts.cfg] dossier wordt gespecificeerd. Voor meer informatie over vestiging zien het administratieve alarm, de Gids *van de Installatie en van het Beleid van de Producten van de* Server.

## De systeemstatus van de sensor controleren {#section-de9d7e359242487a9fbead4ed65aebbc}

Nog een andere manier om te verifiëren dat de zender loopt is manueel te controleren [!DNL Servers Manager] in de Werkbank van Gegevens.

**Om de[!DNL Servers Manager]**

* In de Werkbank van Gegevens, klik binnen een werkruimte met de rechtermuisknop aan, klik **[!UICONTROL Admin]**, dan onder [!DNL Manage], klik **[!UICONTROL Servers]**.

Als het pictogram voor een [!DNL Sensor] groen is, loopt de zender.

Voor meer informatie over [!DNL Servers Manager], zie het Administratieve hoofdstuk van Interfaces van de *Gids[!DNL Sensor]van de Werkbank van* Gegevens.
