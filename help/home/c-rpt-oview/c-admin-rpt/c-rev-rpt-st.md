---
description: Informatie over uw status van de Server van het Rapport en de status van de rapportreeks.
title: Revisierapportstatus
uuid: 0f78a9fd-83d5-4e05-b7d1-d841033a5616
exl-id: a986f148-f019-457c-ade8-a4eaecbb1de7
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '293'
ht-degree: 0%

---

# Revisierapportstatus{#reviewing-report-status}

Informatie over uw status van de Server van het Rapport en de status van de rapportreeks.

* [Serverstatus rapporteren](../../../home/c-rpt-oview/c-admin-rpt/c-rev-rpt-st.md#section-1a84f22439ee4a4ba2b3434e51e82ce0)
* [Status rapportset](../../../home/c-rpt-oview/c-admin-rpt/c-rev-rpt-st.md#section-8569b94266b74a1f85d2a85106a2aaef)

## Serverstatus {#section-1a84f22439ee4a4ba2b3434e51e82ce0} rapporteren

**Aanbevolen frequentie:** Alleen indien nodig

[!DNL Report] verzendt statusinformatie naar de server van de gegevenswerkbank om de twee minuten betreffende de status van de  [!DNL Report] Server. Deze informatie kan onder de [!DNL Report Server Status] knoop in [!DNL Detailed Status] interface worden gezien.

**De  [!DNL Detailed Status] visualisatie openen**

1. Klik met de rechtermuisknop in een werkruimte op de werkbank Gegevens en klik op **[!UICONTROL Admin]** > **[!UICONTROL Servers]**.

1. Klik in de [!DNL Servers]-interface met de rechtermuisknop op het pictogram van de gegevenswerkbench-server waarmee de [!DNL Report]-computer verbinding maakt en klik op **[!UICONTROL Detailed Status.]**

1. Klik op **[!UICONTROL Report Server Status]**.

Als meer dan één [!DNL Report] met de server van de gegevenswerkbank wordt verbonden, verschijnt een ingang voor elke [!DNL Report Server] in de vector van de Status. Het interval van twee minuten kan worden overschreven door een waarde in de parameter van het Interval van de Status (seconden) in de [!DNL Reporting] knoop van het [!DNL ReportServer.cfg] dossier te specificeren.

Voor informatie over het [!DNL ReportServer.cfg] dossier, zie [vorm de Reeks van het Rapport](../../../home/c-rpt-oview/c-work-rpt-sets/t-create-rpt-set/t-config-rpt-set/t-config-rpt-set.md#task-cfb2fd0c28bc48c2acdd582fe0d670d0). Voor informatie over het vormen [!DNL Report], zie [Installing Report](../../../home/c-rpt-oview/c-inst-rpt/c-inst-rpt.md#concept-3b8696a5b7f04ebfaafec7ff55890d91).

Voor meer informatie over [!DNL Detailed Status], zie het Administratieve hoofdstuk van Interfaces van *de Gids van de Gebruiker van de Data Workbench*.

## Status rapportset {#section-8569b94266b74a1f85d2a85106a2aaef}

**Aanbevolen frequentie:** Alleen indien nodig

[!DNL Report] verzendt statusinformatie voor elk rapport dat aan de server van de Data Workbench wordt geplaatst. De basisinformatie, zoals wanneer een rapportreeks wordt geproduceerd en waar het wordt verdeeld, toont in gegevenswerkbank boven de rapportreeks in groene teksten. Tijdens het runnen van rapporten, [!DNL Report] de output van de Server een bericht om de twee minuten erop wijst die het percentage voltooide van de huidige vragen wijst. Dit interval van twee minuten kan worden met voeten getreden door een waarde in de parameter van het Interval van het Bericht van de Voltooiing (seconden) in de [!DNL Reporting] knoop van het [!DNL ReportServer.cfg] dossier te specificeren.

![](assets/report_status.png)

>[!NOTE]
>
>Als er een fout is opgetreden tijdens het uitvoeren van een rapport, wordt de fout aangegeven in rode tekst onder de miniatuur van dat rapport. U kunt met de rechtermuisknop op de werkruimte klikken om het volledige foutbericht weer te geven.
