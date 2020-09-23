---
description: Insight Server is beschikbaar onder twee licentietypen.
solution: Analytics
title: Informatie over Insight Server-licentiecomponenten
uuid: e6a48b00-4dc1-416c-9039-01c01b86abbf
translation-type: tm+mt
source-git-commit: 34cdcfc83ae6bb620706db37228e200cff43ab2c
workflow-type: tm+mt
source-wordcount: '239'
ht-degree: 0%

---


# Informatie over Insight Server-licentiecomponenten{#about-insight-server-license-units}

Insight Server is beschikbaar onder twee licentietypen.

De volgende twee typen licenties zijn van toepassing:

* [Gegevensverwerkingseenheid (DPU)](../../../home/c-inst-svr/c-install-ins-svr/c-abt-inst-svr-lic-units.md#section-bf589e13cf5c43a58f8f85a457de6f65)
* [File Server Unit (FSU)](../../../home/c-inst-svr/c-install-ins-svr/c-abt-inst-svr-lic-units.md#section-8f3a5c8521a34913bbed10f5794b1a0a)

## Gegevensverwerkingseenheid (DPU) {#section-bf589e13cf5c43a58f8f85a457de6f65}

Dit type van [!DNL Insight Server] kan, gegevens van een dataset van de Adobe verwerken opslaan en dienen. Het kan naar keuze de logboekdossiers opslaan die de brongegevens bevatten waarvan de dataset wordt geconstrueerd, of het kan die gegevens van een Eenheid van de Server van het [!DNL Insight Server] Dossier (FSU) ontvangen. Een DPU is het type van [!DNL Insight Server] waarmee [!DNL Insight] en de [!DNL Report] cliënten direct interactie aangaan.

Als u een [!DNL Insight Server] DPU installeert, zie de Procedures van de [Installatie voor een DPU](../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/t-install-proc-inst-svr-dpu.md#task-ce1ac85294604467ab750b24176d25bc)van de Server van het Inzicht.

## File Server Unit (FSU) {#section-8f3a5c8521a34913bbed10f5794b1a0a}

Dit type van server wordt gevormd om gebeurtenisgegevens van één of meerdere instanties van de [!DNL Sensor] of replicatie van gebeurtenisgegevens te ontvangen en op te slaan ( [!DNL Repeater] functionaliteit die met een speciale gebruiksvergunning wordt verstrekt) en de gegevens te stromen aan één of meerdere [!DNL Insight Server] Eenheden van de Gegevensverwerking (DPUs) voor het construeren van gegevensreeksen van Adobe. DPUs communiceert met FSU gebruikend een protocol dat de overdracht van gebeurtenisgegevens aan DPU optimaliseert en beduidend sneller dan het handhaven van logboekdossiers op gewone dossierservers is. Het gebruik van een FSU verlaagt ook de hardwarekosten doordat loggegevens kunnen worden opgeslagen op goedkopere opslaghardware en de administratieve complexiteit vermindert doordat meerdere apparaten [!DNL Sensors] naar één locatie kunnen verwijzen [!DNL Insight Server].

Als u een [!DNL Insight Server] FSU installeert, zie de Procedures van de [Installatie voor een Server FSU](../../../home/c-inst-svr/c-install-ins-svr/t-inst-proc-fsu.md#task-e4a4a791b6694119ba45b36f3e573016)van het Inzicht.
