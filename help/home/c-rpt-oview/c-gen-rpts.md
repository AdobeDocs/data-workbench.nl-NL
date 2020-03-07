---
description: Produceer rapporten door werkruimten te verwerken en hen te specificeren als rapporten.
solution: Analytics
title: Rapporten genereren
topic: Data workbench
uuid: 90bc42b3-d7f2-46f2-8c68-5c682d163f3c
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Rapporten genereren{#generating-reports}

Produceer rapporten door werkruimten te verwerken en hen te specificeren als rapporten.

[!DNL Report] produceert uw rapporten met het interval dat in de [!DNL Every] parameter in het [!DNL Report.cfg] dossier wordt geplaatst (zoals [!DNL "day],&quot;dat het rapport op een dagelijkse basis) verwerkt, en gebaseerd op de andere [!DNL Report.cfg] dossiermontages.

Terwijl het produceren van rapporten, de percenten volledige vertoningen op het [!DNL Reports] lusje onder de duimnagel voor dat bepaalde rapport. Als [!DNL Report] ontmoet een probleem tijdens rapportgeneratie, de meest recente vertoningen van de foutenmelding op het [!DNL Reports] lusje in de omslag van de rapportreeks. Als [!DNL Report] ontmoet een fout voor een bepaald rapport, blijft het de andere rapporten in de reeks verwerken.

U kunt de rapporten in een rapport produceren dat in om het even welke of alle volgende formaten wordt geplaatst gebruikend de [!DNL Report Types] parameter in het [!DNL Report.cfg] dossier:

* Microsoft Excel-bestand ( [!DNL .xls] of [!DNL .xlsx])
* Portable network grafisch dossier ( [!DNL .png])
* Miniatuur ( [!DNL .jpg])

Samen met de gespecificeerde types van output, leidt [!DNL Report] tot een [!DNL .xml] dossier genoemd het zelfde als uw rapport. Dit *`<report name>`*.xml- dossier bevat de beschrijving van het rapport dat vertoningen in de Werkbank van Gegevens op het [!DNL Reports] lusje onder de duimnagel van het rapport toont. Dit maakt de beschrijving beschikbaar aan gebruik wanneer het verdelen van uw rapporten door een rapporteringsportaal. Voor informatie over [!DNL Report Portal], zie het [Werken met het Portaal](../../home/c-rpt-oview/c-rpt-portal/c-rpt-portal.md#concept-f692210cad494c00865dbf325eb5ed35)van het Rapport.

>[!NOTE]
>
>Als u interne metrisch opnieuw definieert, gedraagt het systeem zich onverwacht wegens de verkeerde waarde. Uw rapporten zullen niet produceren tenzij metrisch 100% leest. Men adviseert dat u metrische definities niet verandert.
