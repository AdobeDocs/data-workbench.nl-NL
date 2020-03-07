---
description: In het Portaal van het Rapport, kunt u rapporten bekijken die door de Server van het Rapport als dossiers van Excel (.xls of .xlsx) worden geproduceerd of .png dossiers.
solution: Analytics
title: Het vormen Report.cfg- Dossiers
topic: Data workbench
uuid: b6ce1621-283f-458d-a88d-a062539d243b
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Het vormen Report.cfg- Dossiers{#configuring-report-cfg-files}

In het Portaal van het Rapport, kunt u rapporten bekijken die door de Server van het Rapport als dossiers van Excel (.xls of .xlsx) worden geproduceerd of .png dossiers.

Om een rapport te tonen dat in wordt geplaatst, moet u de volgende parameters in het [!DNL Report Portal][!DNL Report.cfg] dossier voor die rapportreeks plaatsen:

* In de **[!UICONTROL Output Root]** parameter, specificeer de documentwortel van de Webserver die voor uw portaal wordt gebruikt.
* In de **[!UICONTROL Report Types]** parameter, specificeer Excel, png, en/of duimnagel als rapporttypes die u wilt produceren.

Wanneer [!DNL Report Server] produceert de rapporten in de formaten die u specificeerde, plaatst het die dossiers in de documentwortel van de Webserver, die is waar tijdens installatie u vormt om tot de rapporten toegang [!DNL Report Portal] te hebben.

Voor meer informatie over de specifieke [!DNL Report.cfg] parameters, zie Parameters [Report.cfg](../../../home/c-rpt-oview/c-rpt-param-ref/c-rpt-param.md#concept-838e59d72d3f4cb29ee15f5c7eb0ceff).
