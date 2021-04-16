---
description: Genereer rapporten door werkruimten te verwerken en deze als rapporten op te geven.
title: Rapporten genereren
uuid: 90bc42b3-d7f2-46f2-8c68-5c682d163f3c
exl-id: 8e5765e8-71b6-4716-96fe-5c7f69407295
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '238'
ht-degree: 0%

---

# Rapporten genereren{#generating-reports}

Genereer rapporten door werkruimten te verwerken en deze als rapporten op te geven.

[!DNL Report] Hiermee genereert u rapporten met het interval dat is ingesteld in de  [!DNL Every] parameter in het  [!DNL Report.cfg] bestand (bijvoorbeeld  [!DNL "day],&quot; dat het rapport dagelijks verwerkt) en op basis van de andere  [!DNL Report.cfg] bestandsinstellingen.

Tijdens het genereren van rapporten wordt het percentage voltooide weergegeven op het tabblad [!DNL Reports] onder de miniatuur voor dat specifieke rapport. Als [!DNL Report] een probleem tijdens rapportgeneratie ontmoet, toont het meest recente foutenbericht op [!DNL Reports] lusje in de omslag van de rapportreeks. Als [!DNL Report] een fout voor een bepaald rapport ontmoet, blijft het de andere rapporten in de reeks verwerken.

U kunt de rapporten in een rapportreeks in om het even welk of alle volgende formaten produceren gebruikend de [!DNL Report Types] parameter in het [!DNL Report.cfg] dossier:

* Microsoft Excel-bestand ( [!DNL .xls] of [!DNL .xlsx])
* Portable Network graphic file ( [!DNL .png])
* Miniatuur ( [!DNL .jpg])

Samen met de gespecificeerde types van output, [!DNL Report] leidt tot een [!DNL .xml] dossier genoemd het zelfde als uw rapport. Dit *`<report name>`*.xml- dossier bevat de beschrijving van het rapport dat in Data Workbench op [!DNL Reports] lusje onder de duimnagel van het rapport toont. Dit maakt de beschrijving beschikbaar aan gebruik wanneer het verspreiden van uw rapporten door een rapporterend portaal. Voor informatie over [!DNL Report Portal], zie [Werken met het Portaal van het Rapport](../../home/c-rpt-oview/c-rpt-portal/c-rpt-portal.md#concept-f692210cad494c00865dbf325eb5ed35).

>[!NOTE]
>
>Als u een interne metrisch opnieuw definieert, gedraagt het systeem zich onverwacht wegens de verkeerde waarde. Uw rapporten zullen niet produceren tenzij metrisch 100% leest. Het wordt aanbevolen geen metrische definities te wijzigen.
