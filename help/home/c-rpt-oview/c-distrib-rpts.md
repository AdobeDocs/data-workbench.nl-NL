---
description: Nadat de rapporten zijn geproduceerd, verspreidt het Rapport de rapporten in de reeks die op de montages in zijn Report.cfg- dossier wordt gebaseerd.
solution: Analytics
title: Rapporten distribueren
topic: Data workbench
uuid: 0e993635-1aa8-4314-91aa-b4f8f002fa09
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Rapporten distribueren{#distributing-reports}

Nadat de rapporten zijn geproduceerd, verspreidt het Rapport de rapporten in de reeks die op de montages in zijn Report.cfg- dossier wordt gebaseerd.

[!DNL Report] laat u toe om de rapporten in een reeks te verdelen gebruikend de volgende methodes:

* **E-mail:** Om rapporten als dossiers van Excel, [!DNL .png] dossiers, of duimnagels via e-mail (in-lijn of als gehechtheid) te verdelen, specificeer de parameters van het Rapport van de Post in het [!DNL Report.cfg] dossier van de rapportreeks. Alle rapporten in die reeks worden per e-mail verzonden in één bericht aan de gespecificeerde ontvangers.

* **Gedeelde Folder:** Om rapporten als dossiers van Excel, [!DNL .png] dossiers, of duimnagels aan een gedeelde folder te verdelen, specificeer de folder in de parameter van de Wortel van de Output in het [!DNL Report.cfg] dossier van de rapportreeks.

* **Rapporterend portaal:** Een rapporterend portaal laat u toe om rapporten door uw Webbrowser te bekijken. De de [!DNL Report Portal] vertoningenrapporten van Adobe die als Excel of [!DNL .png] - dossiers worden geproduceerd, maar niet die geproduceerd als duimnagels ( [!DNL .jpg]). Om rapporten aan een portaal te verdelen, specificeer de documentwortel van de Webserver die voor het portaal in de parameter van de Wortel van de Output in het [!DNL Report.cfg] dossier van de rapportreeks wordt gebruikt. Voor meer informatie over het installeren van en het gebruiken van [!DNL Report Portal], zie het [Werken met het Portaal](../../home/c-rpt-oview/c-rpt-portal/c-rpt-portal.md#concept-f692210cad494c00865dbf325eb5ed35)van het Rapport.

>[!NOTE]
>
>Om de output te lezen die momenteel wordt ondersteund door, moet u een toepassing hebben die de rapporten in de gewenste indeling(en) kan weergeven. [!DNL Report] Bijvoorbeeld, om [!DNL .xlsx] dossiers te bekijken, moet u Microsoft Excel 2007 of later hebben.

U kunt een combinatie deze generatie en distributieopties ook gebruiken. Bijvoorbeeld, als u de [!DNL Report Types] parameter plaatst om een rapport te produceren dat als Excel en [!DNL .png] - dossiers wordt geplaatst, en dan de [!DNL Mail Report]en [!DNL Output Root] parameters te plaatsen, worden alle rapporten in die reeks verdeeld aan de gespecificeerde outputfolder (misschien te bekijken in een portaal) en in één e-mail aan ontvangers per e-mail per e-mail per e-mail per e-mail per e-mail verstuurd.

Voor stappen om uw rapportreeksen te vormen, zie het [Werken met de Reeksen](../../home/c-rpt-oview/c-work-rpt-sets/c-work-rpt-sets.md#concept-a5f078668e1245e684cb2a778c8803d5)van het Rapport. Voor meer informatie over de specifieke [!DNL Report.cfg] parameters, zie Parameters [Report.cfg](../../home/c-rpt-oview/c-rpt-param-ref/c-rpt-param.md#concept-838e59d72d3f4cb29ee15f5c7eb0ceff).
