---
description: De Server van het zicht is beschikbaar onder twee vergunningstypes.
solution: Insight
title: Informatie over Insight Server-licentieeenheden
uuid: e6a48b00-4dc1-416c-9039-01c01b86abbf
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Informatie over Insight Server-licentieeenheden{#about-insight-server-license-units}

De Server van het zicht is beschikbaar onder twee vergunningstypes.

Het volgende is de twee vergunningstypes:

* [Gegevensverwerkingseenheid (DPU)](../../../home/c-inst-svr/c-install-ins-svr/c-abt-inst-svr-lic-units.md#section-bf589e13cf5c43a58f8f85a457de6f65)
* [File Server Unit (FSU)](../../../home/c-inst-svr/c-install-ins-svr/c-abt-inst-svr-lic-units.md#section-8f3a5c8521a34913bbed10f5794b1a0a)

## Gegevensverwerkingseenheid (DPU) {#section-bf589e13cf5c43a58f8f85a457de6f65}

Dit type van [!DNL Insight Server] kan, gegevens van een dataset van Adobe verwerken opslaan en dienen. Het kan naar keuze de logboekdossiers opslaan die de brongegevens bevatten waarvan de dataset wordt geconstrueerd, of het kan die gegevens van een Eenheid van de Server van het [!DNL Insight Server] Dossier (FSU) ontvangen. Een DPU is het type van [!DNL Insight Server] waarmee [!DNL Insight] en de [!DNL Report] cliënten direct in wisselwerking staan.

Als u een [!DNL Insight Server] DPU installeert, zie de Procedures van de [Installatie voor een DPU](../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/t-install-proc-inst-svr-dpu.md#task-ce1ac85294604467ab750b24176d25bc)van de Server van het Inzicht.

## File Server Unit (FSU) {#section-8f3a5c8521a34913bbed10f5794b1a0a}

Dit type van server wordt gevormd om gebeurtenisgegevens van één of meerdere instanties van de de replicatie van gebeurtenisgegevens te ontvangen en op te slaan ( [!DNL Sensor] functionaliteit die van een speciale gebruiksvergunning wordt voorzien) en de gegevens te stromen aan één of meerdere [!DNL Repeater] [!DNL Insight Server] eenheden van de Gegevensverwerking (DPUs) voor het construeren van de datasets van Adobe. DPUs communiceert met een FSU gebruikend een protocol dat de overdracht van gebeurtenisgegevens aan DPU optimaliseert en beduidend sneller is dan het handhaven van logboekdossiers op gewone dossierservers. Het gebruik van een FSU verlaagt ook de hardwarekosten doordat logboekgegevens kunnen worden opgeslagen op goedkopere opslaghardware en vermindert de administratieve complexiteit doordat meerdere gebruikers [!DNL Sensors] naar één opslaglocatie kunnen wijzen [!DNL Insight Server].

Als u een [!DNL Insight Server] FSU installeert, zie de Procedures van de [Installatie voor een Server FSU](../../../home/c-inst-svr/c-install-ins-svr/t-inst-proc-fsu.md#task-e4a4a791b6694119ba45b36f3e573016)van het Inzicht.
