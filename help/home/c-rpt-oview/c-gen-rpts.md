---
description: Genereer rapporten door werkruimten te verwerken en deze als rapporten op te geven.
title: Rapporten genereren
uuid: 90bc42b3-d7f2-46f2-8c68-5c682d163f3c
exl-id: 8e5765e8-71b6-4716-96fe-5c7f69407295
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '238'
ht-degree: 0%

---

# Rapporten genereren{#generating-reports}

{{eol}}

Genereer rapporten door werkruimten te verwerken en deze als rapporten op te geven.

[!DNL Report] genereert uw rapporten met het interval dat is ingesteld in het dialoogvenster [!DNL Every] in de [!DNL Report.cfg] bestand (zoals [!DNL "day],&quot; dat het rapport dagelijks verwerkt) en op basis van het andere [!DNL Report.cfg] bestandsinstellingen.

Tijdens het genereren van rapporten wordt het percentage voltooide weergegeven op het tabblad [!DNL Reports] onder de miniatuur voor dat specifieke rapport. Indien [!DNL Report] ontmoet een probleem tijdens rapportgeneratie, de meest recente vertoningen van het foutenbericht op [!DNL Reports] in de map van de rapportset. Indien [!DNL Report] Er wordt voor een bepaald rapport een fout aangetroffen. De overige rapporten in de set worden verder verwerkt.

U kunt de rapporten in een rapportreeks in om het even welke of alle volgende formaten produceren gebruikend [!DNL Report Types] in de [!DNL Report.cfg] bestand:

* Microsoft Excel-bestand ( [!DNL .xls] of [!DNL .xlsx])
* Portable Network Graphics-bestand ( [!DNL .png])
* Miniatuur ( [!DNL .jpg])

Samen met de gespecificeerde types van output, [!DNL Report] maakt een [!DNL .xml] bestand met dezelfde naam als uw rapport. Dit *`<report name>`*.xml het dossier bevat de beschrijving van het rapport dat in Data Workbench op het [!DNL Reports] onder de rapportminiatuur. Dit maakt de beschrijving beschikbaar aan gebruik wanneer het verspreiden van uw rapporten door een rapporterend portaal. Voor informatie over de [!DNL Report Portal], zie [Werken met rapportportal](../../home/c-rpt-oview/c-rpt-portal/c-rpt-portal.md#concept-f692210cad494c00865dbf325eb5ed35).

>[!NOTE]
>
>Als u een interne metrisch opnieuw definieert, gedraagt het systeem zich onverwacht wegens de verkeerde waarde. Uw rapporten zullen niet produceren tenzij metrisch 100% leest. Het wordt aanbevolen geen metrische definities te wijzigen.
