---
description: Insight Server is beschikbaar onder twee licentietypen.
title: Informatie over Insight Server-licentiecomponenten
uuid: e6a48b00-4dc1-416c-9039-01c01b86abbf
exl-id: 82d6fa29-d36e-480d-a975-f5a5e60a32d2
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '239'
ht-degree: 0%

---

# Informatie over Insight Server-licentiecomponenten{#about-insight-server-license-units}

{{eol}}

Insight Server is beschikbaar onder twee licentietypen.

De volgende twee typen licenties zijn van toepassing:

* [Gegevensverwerkingseenheid (DPU)](../../../home/c-inst-svr/c-install-ins-svr/c-abt-inst-svr-lic-units.md#section-bf589e13cf5c43a58f8f85a457de6f65)
* [File Server Unit (FSU)](../../../home/c-inst-svr/c-install-ins-svr/c-abt-inst-svr-lic-units.md#section-8f3a5c8521a34913bbed10f5794b1a0a)

## Gegevensverwerkingseenheid (DPU) {#section-bf589e13cf5c43a58f8f85a457de6f65}

Dit type van [!DNL Insight Server] kan gegevens van een gegevensset Adobe verwerken, opslaan en leveren. Het kan naar keuze de logboekdossiers opslaan die de brongegevens bevatten waarvan de dataset wordt geconstrueerd, of het kan die gegevens van een ontvangen [!DNL Insight Server] File Server Unit (FSU). Een DPU is het type van [!DNL Insight Server] waarmee [!DNL Insight] en [!DNL Report] de cliënten interactie direct.

Als u een [!DNL Insight Server] DPU, zie [Installatieprocedures voor een DPU van een Insight Server](../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/t-install-proc-inst-svr-dpu.md#task-ce1ac85294604467ab750b24176d25bc).

## File Server Unit (FSU) {#section-8f3a5c8521a34913bbed10f5794b1a0a}

Dit type server is geconfigureerd voor het ontvangen en opslaan van gebeurtenisgegevens van een of meer [!DNL Sensor] of instanties voor gegevensreplicatie van gebeurtenissen ( [!DNL Repeater] functies die bij een speciale gebruikslicentie worden geleverd) en de gegevens naar een of meer [!DNL Insight Server] De Eenheden van de Gegevensverwerking (DPUs) voor het construeren van Adobe datasets. DPUs communiceert met FSU gebruikend een protocol dat de overdracht van gebeurtenisgegevens aan DPU optimaliseert en beduidend sneller dan het handhaven van logboekdossiers op gewone dossierservers is. Het gebruik van een FSU verlaagt ook de hardwarekosten doordat loggegevens kunnen worden opgeslagen op goedkopere opslaghardware en de administratieve complexiteit vermindert doordat meerdere [!DNL Sensors] naar één [!DNL Insight Server].

Als u een [!DNL Insight Server] FSU, zie [Installatieprocedures voor een Insight Server FSU](../../../home/c-inst-svr/c-install-ins-svr/t-inst-proc-fsu.md#task-e4a4a791b6694119ba45b36f3e573016).
