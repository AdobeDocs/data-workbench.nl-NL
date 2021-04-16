---
description: Nadat de rapporten zijn geproduceerd, verspreidt het Rapport de rapporten in de reeks die op de montages in zijn Report.cfg- dossier wordt gebaseerd.
title: Rapporten distribueren
uuid: 0e993635-1aa8-4314-91aa-b4f8f002fa09
exl-id: ead1d8ef-7319-4307-9155-0101a9c1959d
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '315'
ht-degree: 0%

---

# Rapporten distribueren{#distributing-reports}

Nadat de rapporten zijn geproduceerd, verspreidt het Rapport de rapporten in de reeks die op de montages in zijn Report.cfg- dossier wordt gebaseerd.

[!DNL Report] kunt u de rapporten in een set verdelen met de volgende methoden:

* **E-mail:** Om rapporten als dossiers van Excel,  [!DNL .png] dossiers, of duimnagels via e-mail (in-lijn of als gehechtheid) te verspreiden, specificeer de parameters van het Rapport van de Post in het  [!DNL Report.cfg] dossier van de rapportreeks. Alle rapporten in die reeks worden gemaild in één bericht aan de gespecificeerde ontvangers.

* **Gedeelde Folder:** om rapporten als dossiers van Excel,  [!DNL .png] dossiers, of duimnagels aan een gedeelde folder te verdelen, specificeer de folder in de parameter van de Wortel van de Output in het  [!DNL Report.cfg] dossier van de rapportreeks.

* **Rapporterend Portaal:** Een rapporterend portaal laat u toe om rapporten door uw Webbrowser te bekijken. Adobe geeft rapporten weer die zijn gegenereerd als Excel- of [!DNL .png]-bestanden, maar niet als miniaturen ( [!DNL .jpg]). [!DNL Report Portal] Als u rapporten wilt verspreiden naar een portal, geeft u de hoofdmap van het document van de webserver op die voor het portaal wordt gebruikt in de hoofdparameter Uitvoer in het bestand [!DNL Report.cfg] van de rapportset. Voor meer informatie over het installeren van en het gebruiken van [!DNL Report Portal], zie [Werken met het Portaal van het Rapport](../../home/c-rpt-oview/c-rpt-portal/c-rpt-portal.md#concept-f692210cad494c00865dbf325eb5ed35).

>[!NOTE]
>
>Als u de uitvoer wilt lezen die momenteel wordt ondersteund door [!DNL Report], moet u een toepassing hebben waarmee de rapporten in de gewenste indeling(en) kunnen worden weergegeven. Als u bijvoorbeeld [!DNL .xlsx]-bestanden wilt weergeven, hebt u Microsoft Excel 2007 of hoger nodig.

U kunt ook een combinatie van deze opties voor genereren en verdelen gebruiken. Als u bijvoorbeeld de parameter [!DNL Report Types] instelt om een rapportset te genereren als Excel- en [!DNL .png]-bestanden en vervolgens de parameters [!DNL Mail Report]en [!DNL Output Root] instelt, worden alle rapporten in die set gedistribueerd naar de opgegeven uitvoermap (wellicht te bekijken in een portal) en per e-mail naar ontvangers gemaild.

Voor stappen om uw rapportreeksen te vormen, zie [Werken met de Reeksen van het Rapport](../../home/c-rpt-oview/c-work-rpt-sets/c-work-rpt-sets.md#concept-a5f078668e1245e684cb2a778c8803d5). Voor meer informatie over de specifieke [!DNL Report.cfg] parameters, zie [Report.cfg Parameters](../../home/c-rpt-oview/c-rpt-param-ref/c-rpt-param.md#concept-838e59d72d3f4cb29ee15f5c7eb0ceff).
