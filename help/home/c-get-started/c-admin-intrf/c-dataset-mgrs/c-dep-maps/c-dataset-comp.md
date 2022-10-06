---
description: Conceptuele informatie over gegevenssetcomponenten.
title: Dataset-componenten
uuid: a5dde039-3b79-4543-9953-995eefc73b5f
exl-id: 6be625c5-1a2e-4b0d-9c34-5f3baec4ba81
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '278'
ht-degree: 0%

---

# Dataset-componenten{#dataset-components}

{{eol}}

Conceptuele informatie over gegevenssetcomponenten.

Het volgende cijfer toont een gebiedsdeelkaart de waarvan knopen de logboekbronnen, gebieden, transformaties, en uitgebreide dimensies van een dataset vertegenwoordigen.

![](assets/vis_DependencyMap.png)

* Een geel-groene knoop vertegenwoordigt één of meerdere logboekbronnen of een filter (zoals een Voorwaarde van de Ingang van het Logboek) die in de dataset wordt bepaald.

   * Een knooppunt voor een logbron wordt altijd het verst naar links op de kaart weergegeven. Als uw dataset één enkele logboekbron heeft, toont de kaart Bron van het Logboek: *naam van logbron*. Als uw dataset veelvoudige logboekbronnen heeft, de kaartvertoningen *getal* De Bronnen van het logboek, waar het aantal de telling van logboekbronnen is. Bijvoorbeeld, als u drie logboekbronnen in uw dataset hebt, toont uw kaart 3 Bronnen van het Logboek.

   * De kaart toont één knoop van de Voorwaarde van de Ingang van het Logboek voor elke [!DNL log processing dataset include] bestand maar slechts één Log Entry Condition-knooppunt voor transformatie (indien gedefinieerd in het [!DNL Transformation.cfg] bestand). Als de voorwaarde van de Ingang van het Logboek leeg is, toont het niet op de kaart.

* Een grijze node vertegenwoordigt een veld dat wordt weergegeven in de parameter Fields in een [!DNL Log Processing.cfg] of [!DNL Log Processing include] bestand.

* Een blauw knooppunt vertegenwoordigt een transformatie.
* Een groene knoop vertegenwoordigt een uitgebreide afmeting.

>[!NOTE]
>
>Als de map Gegevensset van uw profiel het bestand bevat [!DNL Insight Transform.cfg], toont de gebiedsdeelkaart de logboekbronnen, de transformaties, en de exporteurs die voor gebruik met Transformatie worden bepaald. Voor informatie over Transformatie, zie *Configuratie-handleiding voor gegevensset*.

Als u Inclusief [!DNL File Blocks] de vertoningsoptie, toont de kaart één enkele blauwe knoop voor alle die transformaties in één dossier van de datasetconfiguratie en één enkele groene knoop voor alle uitgebreide dimensies worden bepaald in één dossier van de datasetconfiguratie. Voor meer informatie over deze weergaveoptie raadpleegt u [Werken met bestandsblokken](../../../../../home/c-get-started/c-admin-intrf/c-dataset-mgrs/c-dep-maps/c-wkg-file-blocks.md#concept-3652bbabfbd34449a5f842d8aa598efc).
