---
description: De informatie over uw status van de Server van het Rapport en status van de rapportreeks.
solution: Analytics
title: Status beoordelingsrapport
topic: Data workbench
uuid: 0f78a9fd-83d5-4e05-b7d1-d841033a5616
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Status beoordelingsrapport{#reviewing-report-status}

De informatie over uw status van de Server van het Rapport en status van de rapportreeks.

* [Status Rapportserver](../../../home/c-rpt-oview/c-admin-rpt/c-rev-rpt-st.md#section-1a84f22439ee4a4ba2b3434e51e82ce0)
* [Status rapportset](../../../home/c-rpt-oview/c-admin-rpt/c-rev-rpt-st.md#section-8569b94266b74a1f85d2a85106a2aaef)

## Status Rapportserver {#section-1a84f22439ee4a4ba2b3434e51e82ce0}

**Aanbevolen frequentie:** Alleen indien nodig

[!DNL Report] verzendt statusinformatie naar de server van de gegevenswerkbank om de twee minuten betreffende de status van de [!DNL Report] Server. Deze informatie kan onder de [!DNL Report Server Status] knoop in de [!DNL Detailed Status] interface worden gezien.

**Om de[!DNL Detailed Status]visualisatie te openen**

1. In gegevenswerkbank, klik in een werkruimte met de rechtermuisknop aan en klik **[!UICONTROL Admin]** > **[!UICONTROL Servers]**.

1. In de [!DNL Servers] interface, klik het pictogram van de server van de gegevenswerkbank met de rechtermuisknop aan die de [!DNL Report] machine met verbindt en klikt **[!UICONTROL Detailed Status.]**

1. Klik op **[!UICONTROL Report Server Status]**.

Als meer dan één met de server van de gegevenswerkbank [!DNL Report] wordt verbonden, verschijnt een ingang voor elk [!DNL Report Server] in de vector van de Status. Het twee-minieme interval kan worden met voeten getreden door een waarde in de parameter van het Interval van de Status (seconden) in de [!DNL Reporting] knoop van het [!DNL ReportServer.cfg] dossier te specificeren.

Voor informatie over het [!DNL ReportServer.cfg] dossier, zie de Reeks [van het Rapport](../../../home/c-rpt-oview/c-work-rpt-sets/t-create-rpt-set/t-config-rpt-set/t-config-rpt-set.md#task-cfb2fd0c28bc48c2acdd582fe0d670d0)vormen. Voor informatie over het vormen [!DNL Report], zie het [Installeren van Rapport](../../../home/c-rpt-oview/c-inst-rpt/c-inst-rpt.md#concept-3b8696a5b7f04ebfaafec7ff55890d91).

Voor meer informatie over [!DNL Detailed Status], zie het Administratieve hoofdstuk van Interfaces van de Gids van de Gebruiker van de Werkbank van *Gegevens*.

## Status rapportset {#section-8569b94266b74a1f85d2a85106a2aaef}

**Aanbevolen frequentie:** Alleen indien nodig

[!DNL Report] brengt statusinformatie voor elk rapport over dat aan de server van de Werkbank van Gegevens wordt geplaatst. De basisinformatie, zoals wanneer een rapportreeks wordt geproduceerd en waar het wordt verspreid, toont in gegevenswerkbank boven het rapport dat in groene teksten wordt geplaatst. Terwijl het runnen van rapporten, [!DNL Report] voert de output van de Server een bericht om de twee minuten erop wijzend het percentage volledig van de huidige vragen uit. Dit twee-minieme interval kan worden met voeten getreden door een waarde in de parameter van het Interval van het Bericht van de Voltooiing (seconden) in de [!DNL Reporting] knoop van het [!DNL ReportServer.cfg] dossier te specificeren.

![](assets/report_status.png)

>[!NOTE]
>
>Als een fout terwijl het runnen van een rapport voorkwam, wordt de fout vermeld in rode teksten onder de duimnagel van dat rapport. U kunt de werkruimte met de rechtermuisknop aanklikken om de volledige foutenmelding te tonen.

