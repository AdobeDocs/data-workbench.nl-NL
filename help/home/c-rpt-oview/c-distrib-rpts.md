---
description: Nadat de rapporten zijn geproduceerd, verspreidt het Rapport de rapporten in de reeks die op de montages in zijn Report.cfg- dossier wordt gebaseerd.
title: Rapporten distribueren
uuid: 0e993635-1aa8-4314-91aa-b4f8f002fa09
exl-id: ead1d8ef-7319-4307-9155-0101a9c1959d
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '315'
ht-degree: 0%

---

# Rapporten distribueren{#distributing-reports}

{{eol}}

Nadat de rapporten zijn geproduceerd, verspreidt het Rapport de rapporten in de reeks die op de montages in zijn Report.cfg- dossier wordt gebaseerd.

[!DNL Report] kunt u de rapporten in een set verdelen met de volgende methoden:

* **E-mail:** Om rapporten als dossiers van Excel te verdelen, [!DNL .png] bestanden, of miniaturen via e-mail (in-line of als bijlagen), geeft u de parameters E-mailrapport op in de rapportset [!DNL Report.cfg] bestand. Alle rapporten in die reeks worden gemaild in één bericht aan de gespecificeerde ontvangers.

* **Gedeelde map:** Om rapporten als dossiers van Excel te verdelen, [!DNL .png] bestanden, of miniaturen naar een gedeelde map, geeft u de map op in de parameter Uitvoer in de rapportset [!DNL Report.cfg] bestand.

* **Portaal rapporteren:** Met een portal voor rapportage kunt u rapporten weergeven via uw webbrowser. Adobe [!DNL Report Portal] geeft rapporten weer die zijn gegenereerd als Excel of [!DNL .png] bestanden, maar deze zijn niet als miniaturen gegenereerd ( [!DNL .jpg]). Als u rapporten naar een portal wilt distribueren, geeft u de hoofdmap van het document op van de webserver die voor het portaal wordt gebruikt in de hoofdparameter Uitvoer in de rapportset [!DNL Report.cfg] bestand. Meer informatie over installeren en gebruiken [!DNL Report Portal], zie [Werken met rapportportal](../../home/c-rpt-oview/c-rpt-portal/c-rpt-portal.md#concept-f692210cad494c00865dbf325eb5ed35).

>[!NOTE]
>
>De uitvoer lezen die momenteel wordt ondersteund door [!DNL Report]hebt u een toepassing nodig waarmee de rapporten in de gewenste indeling(en) kunnen worden weergegeven. Bijvoorbeeld om [!DNL .xlsx] bestanden hebt, moet u Microsoft Excel 2007 of hoger gebruiken.

U kunt ook een combinatie van deze opties voor genereren en verdelen gebruiken. Als u bijvoorbeeld de opdracht [!DNL Report Types] parameter om een rapport te produceren dat als Excel wordt geplaatst en [!DNL .png] en stelt vervolgens de [!DNL Mail Report]en [!DNL Output Root] parameters, worden alle rapporten in die reeks verdeeld aan de gespecificeerde outputfolder (misschien om in een portaal te bekijken) en in één e-mail aan ontvangers gemaild.

Voor stappen om uw rapportreeksen te vormen, zie [Werken met rapportsets](../../home/c-rpt-oview/c-work-rpt-sets/c-work-rpt-sets.md#concept-a5f078668e1245e684cb2a778c8803d5). Meer informatie over de specifieke [!DNL Report.cfg] parameters, zie [Report.cfg-parameters](../../home/c-rpt-oview/c-rpt-param-ref/c-rpt-param.md#concept-838e59d72d3f4cb29ee15f5c7eb0ceff).
