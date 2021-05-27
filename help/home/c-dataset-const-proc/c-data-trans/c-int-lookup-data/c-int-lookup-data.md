---
description: De werkbank van gegevens verstrekt een reeks transformaties die de server van de gegevenswerkbank toelaat om raadplegingsgegevens in de dataset op te nemen.
title: Opzoekgegevens integreren
uuid: 35fd48f7-c0c4-4a83-919d-c15902f27495
exl-id: 150d3aae-4431-488f-8f19-b522637ee935
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '262'
ht-degree: 0%

---

# Opzoekgegevens integreren{#integrating-lookup-data}

De werkbank van gegevens verstrekt een reeks transformaties die de server van de gegevenswerkbank toelaat om raadplegingsgegevens in de dataset op te nemen.

De gegevens van de opzoekopdracht zijn externe gegevens van collectieve gegevensbestanden of raadplegingsdossiers die u met gebeurtenisgegevens kunt combineren om de dataset tot stand te brengen. Over het algemeen gebruikt u opzoekgegevens om de gebeurtenisgegevens uit uw logbronnen te vergroten. Conceptueel, kunt u denken aan het gebruiken van raadplegingsgegevens om de verslagen van gebeurtenisgegevens met extra kolommen van informatie te bevolken.

Wanneer u raadplegingsgegevens gebruikt, laadt u de gegevens in een geheugen-ingezeten raadplegingstabel. Een kolom in de tabel moet een algemene sleutel bevatten die ook bestaat in de records met gebeurtenisgegevens. De gegevens in de raadplegingstabel zelf kunnen van een vlak dossier of van een ODBC- gegevensbron worden geladen. De gegevens van de opzoekopdracht kunnen in de dataset tijdens de logboekverwerking of transformatiefase van het proces van de datasetconstructie worden opgenomen.

Om raadplegingsgegevens op te nemen, moet u een raadplegingsdossier eerst produceren of de informatie hebben nodig om tot een SQL gegevensbestand toegang te hebben, dan één of meerdere van de volgende transformaties in de dossiers van de datasetconfiguratie voor logboekverwerking en transformatie bepalen.

**Opzoekgegevens integreren in de gegevensset**

1. Genereer het opzoekbestand. Zie [De opzoektabel vullen](../../../../home/c-dataset-const-proc/c-data-trans/c-int-lookup-data/c-pop-lookup-table.md#concept-dd761338731a40e0997c33dfdabdcdf8).
1. Bepaal één van de volgende types van transformaties in de parameter van Transformaties in het aangewezen dossier van de datasetconfiguratie:

   * [!DNL Categorize]
   * [!DNL FlatFileLookup]
   * [!DNL ODBCLookup]

>[!NOTE]
>
>De [!DNL ODBCLookup]-transformatie werkt alleen wanneer deze is gedefinieerd in het [!DNL Transformation.cfg]-bestand of in een [!DNL Transformation Dataset Include]-bestand.
