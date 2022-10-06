---
description: Informatie over uw status van de Server van het Rapport en de status van de rapportreeks.
title: Revisierapportstatus
uuid: 0f78a9fd-83d5-4e05-b7d1-d841033a5616
exl-id: a986f148-f019-457c-ade8-a4eaecbb1de7
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '293'
ht-degree: 0%

---

# Revisierapportstatus{#reviewing-report-status}

{{eol}}

Informatie over uw status van de Server van het Rapport en de status van de rapportreeks.

* [Serverstatus rapporteren](../../../home/c-rpt-oview/c-admin-rpt/c-rev-rpt-st.md#section-1a84f22439ee4a4ba2b3434e51e82ce0)
* [Status rapportset](../../../home/c-rpt-oview/c-admin-rpt/c-rev-rpt-st.md#section-8569b94266b74a1f85d2a85106a2aaef)

## Serverstatus rapporteren {#section-1a84f22439ee4a4ba2b3434e51e82ce0}

**Aanbevolen frequentie:** Alleen indien nodig

[!DNL Report] verzendt statusinformatie naar de server van de gegevenswerkbank elke twee minuten betreffende de status van [!DNL Report] Server. Deze informatie is te vinden onder de [!DNL Report Server Status] knooppunt in [!DNL Detailed Status] interface.

**Als u het dialoogvenster [!DNL Detailed Status] visualisatie**

1. Klik met de rechtermuisknop in een werkruimte op de werkbank Gegevens **[!UICONTROL Admin]** > **[!UICONTROL Servers]**.

1. In de [!DNL Servers] interface, klikt u met de rechtermuisknop op het pictogram van de gegevenswerkbankserver waarop de [!DNL Report] machine verbindt met en klikt **[!UICONTROL Detailed Status.]**

1. Klik op **[!UICONTROL Report Server Status]**.

Indien meer dan één [!DNL Report] is verbonden met de server van de gegevenswerkbank, verschijnt een ingang voor elke [!DNL Report Server] in de statusvector. Het interval van twee minuten kan worden genegeerd door een waarde in de parameter van het Interval van de Status (seconden) in te specificeren [!DNL Reporting] knooppunt van de [!DNL ReportServer.cfg] bestand.

Voor informatie over de [!DNL ReportServer.cfg] bestand, zie [De rapportset configureren](../../../home/c-rpt-oview/c-work-rpt-sets/t-create-rpt-set/t-config-rpt-set/t-config-rpt-set.md#task-cfb2fd0c28bc48c2acdd582fe0d670d0). Voor informatie over het configureren [!DNL Report], zie [Rapport wordt geïnstalleerd](../../../home/c-rpt-oview/c-inst-rpt/c-inst-rpt.md#concept-3b8696a5b7f04ebfaafec7ff55890d91).

Meer informatie over [!DNL Detailed Status], zie het hoofdstuk Administratieve Interfaces van *Gebruikershandleiding voor Data Workbench*.

## Status rapportset {#section-8569b94266b74a1f85d2a85106a2aaef}

**Aanbevolen frequentie:** Alleen indien nodig

[!DNL Report] verzendt statusinformatie voor elk rapport dat aan de server van de Data Workbench wordt geplaatst. De basisinformatie, zoals wanneer een rapportreeks wordt geproduceerd en waar het wordt verdeeld, toont in gegevenswerkbank boven de rapportreeks in groene teksten. Tijdens het uitvoeren van rapporten, [!DNL Report] De output van de server een bericht om de twee minuten erop wijst die op het percentage voltooide van de huidige vragen wijzen. Dit twee-minieme interval kan worden met voeten getreden door een waarde in de parameter van het Interval van het Bericht van de Voltooiing (seconden) in te specificeren [!DNL Reporting] knooppunt van de [!DNL ReportServer.cfg] bestand.

![](assets/report_status.png)

>[!NOTE]
>
>Als er een fout is opgetreden tijdens het uitvoeren van een rapport, wordt de fout aangegeven in rode tekst onder de miniatuur van dat rapport. U kunt met de rechtermuisknop op de werkruimte klikken om het volledige foutbericht weer te geven.
