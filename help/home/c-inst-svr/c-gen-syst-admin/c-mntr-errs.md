---
description: Als u systeem- en toepassingsfouten zo snel mogelijk wilt detecteren en deze wilt verhelpen voordat ze grote problemen of storingen veroorzaken, moet u regelmatig uw gebeurtenislogboeken controleren.
solution: Analytics
title: Gebeurtenissen controleren op fouten
uuid: 09bb34db-e24d-4bc5-84d2-7fc37df60681
translation-type: tm+mt
source-git-commit: 34cdcfc83ae6bb620706db37228e200cff43ab2c
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 0%

---


# Gebeurtenissen controleren op fouten{#monitoring-events-for-errors}

Als u systeem- en toepassingsfouten zo snel mogelijk wilt detecteren en deze wilt verhelpen voordat ze grote problemen of storingen veroorzaken, moet u regelmatig uw gebeurtenislogboeken controleren.

**Aanbevolen frequentie:** Elke 5-10 minuten

Als u de softwareproducten van uw Adobe-server wilt controleren, kunt u uw geautomatiseerde beheertool zo instellen dat het gebeurtenissenlogboek op fouten met de bron &quot;Adobe&quot; wordt gecontroleerd en dat het juiste personeel wordt gewaarschuwd voor problemen die mogelijk interventie vereisen.

In Windows worden foutberichten van de toepassing uitgevoerd naar het logboek Toepassingsgebeurtenis in Windows, dat u kunt openen met de Windows Event Viewer. In Unix, worden de berichten van de toepassingsfout output aan Unix syslog gebruikend de faciliteit LOG_DAEMON.

**De Windows Event Viewer openen**

* Klik op **[!UICONTROL Start]** > **[!UICONTROL Control Panel]** > **[!UICONTROL Administrative Tools]** > **[!UICONTROL Event Viewer]**.

