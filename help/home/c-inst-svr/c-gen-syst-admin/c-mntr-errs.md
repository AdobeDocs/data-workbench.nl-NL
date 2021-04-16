---
description: Als u systeem- en toepassingsfouten zo snel mogelijk wilt detecteren en deze wilt verhelpen voordat ze grote problemen of storingen veroorzaken, moet u regelmatig uw gebeurtenislogboeken controleren.
title: Gebeurtenissen controleren op fouten
uuid: 09bb34db-e24d-4bc5-84d2-7fc37df60681
exl-id: 88f48594-5c73-4ae3-8014-b8543e689426
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 0%

---

# Gebeurtenissen controleren op fouten{#monitoring-events-for-errors}

Als u systeem- en toepassingsfouten zo snel mogelijk wilt detecteren en deze wilt verhelpen voordat ze grote problemen of storingen veroorzaken, moet u regelmatig uw gebeurtenislogboeken controleren.

**Aanbevolen frequentie:** elke 5-10 minuten

Als u de softwareproducten van uw Adobe-server wilt controleren, kunt u uw geautomatiseerde beheertool zo instellen dat het gebeurtenissenlogboek op fouten met de bron &quot;Adobe&quot; wordt gecontroleerd en dat het juiste personeel wordt gewaarschuwd voor problemen die mogelijk interventie vereisen.

In Windows worden foutberichten van de toepassing uitgevoerd naar het logboek Toepassingsgebeurtenis in Windows, dat u kunt openen met de Windows Event Viewer. In Unix, worden de berichten van de toepassingsfout output aan Unix syslog gebruikend de faciliteit LOG_DAEMON.

**De Windows Event Viewer openen**

* Klik op **[!UICONTROL Start]** > **[!UICONTROL Control Panel]** > **[!UICONTROL Administrative Tools]** > **[!UICONTROL Event Viewer]**.
