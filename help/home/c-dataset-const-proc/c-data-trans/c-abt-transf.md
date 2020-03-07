---
description: De transformaties laten u toe om informatie te halen beschikbaar in uw gegevensdossiers en het te manipuleren in een nuttigere vorm.
solution: Analytics
title: Informatie over transformaties
topic: Data workbench
uuid: 9366f607-741d-4512-9e1b-4165f4291246
translation-type: tm+mt
source-git-commit: 27600561841db3705f4eee6ff0aeb8890444bbc9

---


# Informatie over transformaties{#about-transformations}

De transformaties laten u toe om informatie te halen beschikbaar in uw gegevensdossiers en het te manipuleren in een nuttigere vorm.

De transformaties werken op de logboekingangen (u kunt aan logboekingangen als rijen van gegevens denken) in uw logboekbronnen. Voor elke rij van gegevens, neemt de transformatie de waarde van het gespecificeerde inputgebied, voert een reeks verwerkingsstappen uit, en registreert het resultaat op het outputgebied dat u specificeert. U kunt transformaties bepalen die tijdens of de de logboekverwerking of transformatiefase van het proces van de datasetconstructie moeten worden uitgevoerd:

* **Tijdens de logboekverwerking:** De transformaties die tijdens de fase van de logboekverwerking van datasetconstructie worden uitgevoerd worden toegepast op elk verslag van gebeurtenisgegevens (logboekingang) om bestaande logboekgebieden bij te werken of nieuwe gebieden te produceren. De resultaten van de transformaties worden gebruikt samen met de voorwaarden van de logboekingang om te evalueren welke logboekingangen uit de dataset tijdens logboekverwerking worden gefiltreerd.
* **Tijdens de transformatie:** De transformaties die tijdens de transformatiefase van datasetconstructie worden uitgevoerd werken op de gebieden van gegevens die van logboekverwerking worden overgegaan om uitgebreide afmetingen tot stand te brengen die u in uw analyses kunt gebruiken. Zie [Uitgebreide afmetingen](../../../home/c-dataset-const-proc/c-ex-dim/c-abt-ex-dim.md).

>[!NOTE]
>
>De gegevens die aan transformatie van logboekverwerking worden ingevoerd worden bevolen door tijd en gegroepeerd door volgende identiteitskaart in uw brongegevens. Verscheidene transformaties vereisen dat het gegeven in deze vorm is en slechts werkt wanneer bepaald in tijdens transformatie.

Wijzigingen in transformaties moeten zorgvuldig worden aangebracht. De transformaties beïnvloeden niet welke logboekingangen in het proces van de datasetconstructie stromen, maar zij beïnvloeden de gepresenteerde resultaten. Dit maakt het mogelijk om veranderingen aan te brengen in wat wordt geanalyseerd zonder de gegevens waarop de analyse is gebaseerd te veranderen. Nochtans, kunnen de veranderingen in transformaties de waarden fundamenteel veranderen die in analyses worden geproduceerd.
