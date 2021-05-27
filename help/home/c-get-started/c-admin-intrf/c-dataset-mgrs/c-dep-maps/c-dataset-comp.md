---
description: Conceptuele informatie over gegevenssetcomponenten.
title: Dataset-componenten
uuid: a5dde039-3b79-4543-9953-995eefc73b5f
exl-id: 6be625c5-1a2e-4b0d-9c34-5f3baec4ba81
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '278'
ht-degree: 0%

---

# Dataset-componenten{#dataset-components}

Conceptuele informatie over gegevenssetcomponenten.

Het volgende cijfer toont een gebiedsdeelkaart de waarvan knopen de logboekbronnen, gebieden, transformaties, en uitgebreide dimensies van een dataset vertegenwoordigen.

![](assets/vis_DependencyMap.png)

* Een geel-groene knoop vertegenwoordigt één of meerdere logboekbronnen of een filter (zoals een Voorwaarde van de Ingang van het Logboek) die in de dataset wordt bepaald.

   * Een knooppunt voor een logbron wordt altijd het verst naar links op de kaart weergegeven. Als uw dataset één enkele logboekbron heeft, toont de kaart Bron van het Logboek: *logbronnaam*. Als uw dataset veelvoudige logboekbronnen heeft, toont de kaart *number* de Bronnen van het Logboek, waar het aantal de telling van logboekbronnen is. Bijvoorbeeld, als u drie logboekbronnen in uw dataset hebt, toont uw kaart 3 Bronnen van het Logboek.

   * Op de kaart wordt één Log Entry Condition-knooppunt weergegeven voor elk [!DNL log processing dataset include]-bestand, maar slechts één Log Entry Condition-knooppunt voor transformatie (indien gedefinieerd in het [!DNL Transformation.cfg]-bestand). Als de voorwaarde van de Ingang van het Logboek leeg is, toont het niet op de kaart.

* Een grijze node vertegenwoordigt een veld dat wordt weergegeven in de parameter Fields in een [!DNL Log Processing.cfg]- of [!DNL Log Processing include]-bestand.

* Een blauw knooppunt vertegenwoordigt een transformatie.
* Een groene knoop vertegenwoordigt een uitgebreide afmeting.

>[!NOTE]
>
>Als de omslag van de Dataset van uw profiel het dossier [!DNL Insight Transform.cfg] bevat, toont de gebiedsdeelkaart de logboekbronnen, de transformaties, en de exporteurs die voor gebruik met Transformatie worden bepaald. Voor informatie over Transformatie, zie *de Gids van de Configuratie van de Dataset*.

Wanneer u Include [!DNL File Blocks] vertoningsoptie toelaat, toont de kaart één enkele blauwe knoop voor alle transformaties die in één dossier van de datasetconfiguratie en één enkele groene knoop voor alle uitgebreide dimensies worden bepaald die in één dossier van de datasetconfiguratie worden bepaald. Zie [Werken met File Blocks](../../../../../home/c-get-started/c-admin-intrf/c-dataset-mgrs/c-dep-maps/c-wkg-file-blocks.md#concept-3652bbabfbd34449a5f842d8aa598efc) voor meer informatie over deze weergaveoptie.
