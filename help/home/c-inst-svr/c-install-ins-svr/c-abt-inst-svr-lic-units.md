---
description: Insight Server is beschikbaar onder twee licentietypen.
title: Informatie over Insight Server-licentiecomponenten
uuid: e6a48b00-4dc1-416c-9039-01c01b86abbf
exl-id: 82d6fa29-d36e-480d-a975-f5a5e60a32d2
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '239'
ht-degree: 0%

---

# Info over Insight Server-licentieeenheden{#about-insight-server-license-units}

Insight Server is beschikbaar onder twee licentietypen.

De volgende twee typen licenties zijn van toepassing:

* [Gegevensverwerkingseenheid (DPU)](../../../home/c-inst-svr/c-install-ins-svr/c-abt-inst-svr-lic-units.md#section-bf589e13cf5c43a58f8f85a457de6f65)
* [File Server Unit (FSU)](../../../home/c-inst-svr/c-install-ins-svr/c-abt-inst-svr-lic-units.md#section-8f3a5c8521a34913bbed10f5794b1a0a)

## Gegevensverwerkingseenheid (DPU) {#section-bf589e13cf5c43a58f8f85a457de6f65}

Dit type van [!DNL Insight Server] kan gegevens van een dataset van de Adobe verwerken, opslaan en dienen. Het kan naar keuze de logboekdossiers opslaan die de brongegevens bevatten waarvan de dataset wordt geconstrueerd, of het kan die gegevens van een [!DNL Insight Server] Eenheid van de Server van het Dossier (FSU) ontvangen. Een DPU is het type van [!DNL Insight Server] waarmee [!DNL Insight] en [!DNL Report] cliënten direct interactie aangaan.

Als u een [!DNL Insight Server] DPU installeert, zie [Installatie Procedures voor een DPU](../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/t-install-proc-inst-svr-dpu.md#task-ce1ac85294604467ab750b24176d25bc) van de Server van het Inzicht.

## File Server Unit (FSU) {#section-8f3a5c8521a34913bbed10f5794b1a0a}

Dit type server is geconfigureerd voor het ontvangen en opslaan van gebeurtenisgegevens van een of meer [!DNL Sensor]- of gebeurtenisgegevensreplicatie-instanties ( [!DNL Repeater]-functionaliteit voorzien van een speciale gebruikslicentie) en het streamen van de gegevens naar een of meer [!DNL Insight Server] Data Processing Units (DPU&#39;s) voor het samenstellen van Adobe-gegevenssets. DPUs communiceert met FSU gebruikend een protocol dat de overdracht van gebeurtenisgegevens aan DPU optimaliseert en beduidend sneller dan het handhaven van logboekdossiers op gewone dossierservers is. Het gebruik van een FSU verlaagt ook de hardwarekosten doordat loggegevens kunnen worden opgeslagen op goedkopere opslaghardware en de administratieve complexiteit vermindert doordat meerdere [!DNL Sensors] naar één [!DNL Insight Server] kunnen wijzen.

Als u een [!DNL Insight Server] FSU installeert, zie [Installatieprocedures voor een Insight Server FSU](../../../home/c-inst-svr/c-install-ins-svr/t-inst-proc-fsu.md#task-e4a4a791b6694119ba45b36f3e573016).
