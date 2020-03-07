---
description: Conceptuele informatie over gegevenssetcomponenten.
solution: Analytics
title: Gegevensset-componenten
topic: Data workbench
uuid: a5dde039-3b79-4543-9953-995eefc73b5f
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Gegevensset-componenten{#dataset-components}

Conceptuele informatie over gegevenssetcomponenten.

Het volgende cijfer toont een gebiedsdeelkaart de waarvan knopen de logboekbronnen, gebieden, transformaties, en uitgebreide afmetingen van een dataset vertegenwoordigen.

![](assets/vis_DependencyMap.png)

* Een geel-groene knoop vertegenwoordigt één of meerdere logboekbronnen of een filter (zoals een Voorwaarde van de Ingang van het Logboek) die in de dataset wordt bepaald.

   * Een knoop voor een logboekbron verschijnt altijd het verst aan de linkerzijde in de kaart. Als uw dataset één enkele logboekbron heeft, de Bron van het Logboek van kaartvertoningen: Naam *logbron*. Als uw dataset veelvoudige logboekbronnen heeft, de bronnen van het *aantal* van kaartvertoningenLogboek, waar het aantal de telling van logboekbronnen is. Bijvoorbeeld, als u drie logboekbronnen in uw dataset hebt, uw kaartvertoningen 3 Bronnen van het Logboek.

   * De kaart toont één knoop van de Voorwaarde van de Ingang van het Logboek voor elk [!DNL log processing dataset include] - dossier maar slechts één knoop van de Voorwaarde van de Ingang van het Logboek voor transformatie (indien bepaald in het [!DNL Transformation.cfg] dossier). Als de Voorwaarde van de Ingang van het Logboek leeg is, toont het niet op de kaart.

* Een grijze knoop vertegenwoordigt een gebied dat in de parameter van Gebieden in een [!DNL Log Processing.cfg] of [!DNL Log Processing include] dossier vermeld is.

* Een blauwe knoop vertegenwoordigt een transformatie.
* Een groene knoop vertegenwoordigt een uitgebreide dimensie.

>[!NOTE]
>
>Als de omslag van de Dataset van uw profiel het dossier bevat, toont de gebiedsdeelkaart de logboekbronnen, de transformaties, en de exporteurs die voor gebruik met Transformatie worden bepaald. [!DNL Insight Transform.cfg] Voor informatie over Transformatie, zie de Gids *van de Configuratie van de* Dataset.

Wanneer u de Include [!DNL File Blocks] vertoningsoptie toelaat, toont de kaart één enkele blauwe knoop voor alle transformaties die in één dossier van de datasetconfiguratie en één enkele groene knoop voor alle uitgebreide afmetingen worden bepaald die in één dossier van de datasetconfiguratie worden bepaald. Voor meer informatie over deze vertoningsoptie, zie het [Werken met de Blokken](../../../../../home/c-get-started/c-admin-intrf/c-dataset-mgrs/c-dep-maps/c-wkg-file-blocks.md#concept-3652bbabfbd34449a5f842d8aa598efc)van het Dossier.
