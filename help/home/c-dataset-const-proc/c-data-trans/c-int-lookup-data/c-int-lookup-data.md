---
description: De werkbank van gegevens verstrekt een reeks transformaties die de server van de gegevenswerkbank toelaat om raadplegingsgegevens in de dataset op te nemen.
solution: Analytics
title: Integratie van zoekgegevens
topic: Data workbench
uuid: 35fd48f7-c0c4-4a83-919d-c15902f27495
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Integratie van zoekgegevens{#integrating-lookup-data}

De werkbank van gegevens verstrekt een reeks transformaties die de server van de gegevenswerkbank toelaat om raadplegingsgegevens in de dataset op te nemen.

De gegevens van de raadpleging zijn externe gegevens van collectieve gegevensbestanden of raadplegingsdossiers die u met gebeurtenisgegevens kunt combineren om de dataset tot stand te brengen. In het algemeen, gebruikt u raadplegingsgegevens om de gebeurtenisgegevens uit uw logboekbronnen te vergroten. Conceptueel, kunt u aan het gebruiken van raadplegingsgegevens denken om de verslagen van gebeurtenisgegevens met extra kolommen van informatie te bevolken.

Wanneer u raadplegingsgegevens gebruikt, laadt u de gegevens in een geheugen-ingezeten raadplegingslijst. Een kolom in de lijst moet een gemeenschappelijke sleutel bevatten die ook in de verslagen van gebeurtenisgegevens bestaat. De gegevens in de raadplegingslijst zelf kunnen van een vlak dossier of van een ODBC gegevensbron worden geladen. De gegevens van de raadpleging kunnen in de dataset tijdens de de logboekverwerking of transformatiefase van het proces van de datasetconstructie worden opgenomen.

Om raadplegingsgegevens op te nemen, moet u een raadplegingsdossier eerst produceren of de informatie hebben nodig om tot een SQL gegevensbestand toegang te hebben, dan één of meer van de volgende transformaties in de dossiers van de datasetconfiguratie voor logboekverwerking en transformatie bepalen.

**Om raadplegingsgegevens in de dataset te integreren**

1. Produceer uw raadplegingsdossier. Zie het [Bevolken van de Lijst](../../../../home/c-dataset-const-proc/c-data-trans/c-int-lookup-data/c-pop-lookup-table.md#concept-dd761338731a40e0997c33dfdabdcdf8)van de Raadpleging.
1. Bepaal één van de volgende types van transformaties in de parameter van Transformaties in het aangewezen dossier van de datasetconfiguratie:

   * [!DNL Categorize]
   * [!DNL FlatFileLookup]
   * [!DNL ODBCLookup]

>[!NOTE]
>
>Merk op dat de [!DNL ODBCLookup] transformatie slechts wanneer bepaald in het [!DNL Transformation.cfg] dossier of in een [!DNL Transformation Dataset Include] dossier werkt.

