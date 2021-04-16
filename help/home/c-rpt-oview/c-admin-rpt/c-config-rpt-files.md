---
description: In het Portaal van het Rapport, kunt u rapporten bekijken die door de Server van het Rapport als dossiers van Excel (.xls of .xlsx) of .png- dossiers worden geproduceerd.
title: Report.cfg-bestanden configureren
uuid: b6ce1621-283f-458d-a88d-a062539d243b
exl-id: 5af5abaa-77bf-447b-b341-8f44e228f37a
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 0%

---

# Het vormen Report.cfg- Dossiers{#configuring-report-cfg-files}

In het Portaal van het Rapport, kunt u rapporten bekijken die door de Server van het Rapport als dossiers van Excel (.xls of .xlsx) of .png- dossiers worden geproduceerd.

Als u een rapportset wilt weergeven in de [!DNL Report Portal], moet u de volgende parameters in het [!DNL Report.cfg]-bestand voor die rapportset instellen:

* Geef in de parameter **[!UICONTROL Output Root]** de hoofdmap van het document op van de webserver die voor uw portal wordt gebruikt.
* In de **[!UICONTROL Report Types]** parameter, specificeer Excel, png, en/of duimnagel als rapporttypes die u wilt produceren.

Wanneer [!DNL Report Server] de rapporten in de formaten produceert die u specificeerde, plaatst het die dossiers in de documentwortel van de Webserver, die is waar tijdens installatie u [!DNL Report Portal] vormt om tot de rapporten toegang te hebben.

Voor meer informatie over de specifieke [!DNL Report.cfg] parameters, zie [Report.cfg Parameters](../../../home/c-rpt-oview/c-rpt-param-ref/c-rpt-param.md#concept-838e59d72d3f4cb29ee15f5c7eb0ceff).
