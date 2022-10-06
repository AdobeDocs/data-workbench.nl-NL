---
description: In het Portaal van het Rapport, kunt u rapporten bekijken die door de Server van het Rapport als dossiers van Excel (.xls of .xlsx) of .png- dossiers worden geproduceerd.
title: Report.cfg-bestanden configureren
uuid: b6ce1621-283f-458d-a88d-a062539d243b
exl-id: 5af5abaa-77bf-447b-b341-8f44e228f37a
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 0%

---

# Report.cfg-bestanden configureren{#configuring-report-cfg-files}

{{eol}}

In het Portaal van het Rapport, kunt u rapporten bekijken die door de Server van het Rapport als dossiers van Excel (.xls of .xlsx) of .png- dossiers worden geproduceerd.

Een rapportset weergeven in het dialoogvenster [!DNL Report Portal]moet u de volgende parameters instellen in het dialoogvenster [!DNL Report.cfg] dossier voor die rapportreeks:

* In de **[!UICONTROL Output Root]** geeft u de hoofdmap van het document op van de webserver die voor uw portal wordt gebruikt.
* In de **[!UICONTROL Report Types]** geeft u Excel, png en/of miniaturen op als de rapporttypen die u wilt genereren.

Wanneer [!DNL Report Server] genereert de rapporten in de formaten die u specificeerde, het plaatst die dossiers in de documentwortel van de Webserver, die tijdens installatie is waar u vormt [!DNL Report Portal] toegang tot de rapporten.

Meer informatie over de specifieke [!DNL Report.cfg] parameters, zie [Report.cfg-parameters](../../../home/c-rpt-oview/c-rpt-param-ref/c-rpt-param.md#concept-838e59d72d3f4cb29ee15f5c7eb0ceff).
