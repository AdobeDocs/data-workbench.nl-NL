---
description: Met transformaties kunt u gegevens uit uw gegevensbestanden extraheren en deze in een nuttiger vorm bewerken.
title: Informatie over transformaties
uuid: 9366f607-741d-4512-9e1b-4165f4291246
exl-id: 9bd533ef-a87e-400a-9bb0-5af1851cca0a
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '307'
ht-degree: 0%

---

# Info over Transformaties{#about-transformations}

Met transformaties kunt u gegevens uit uw gegevensbestanden extraheren en deze in een nuttiger vorm bewerken.

De transformaties werken op de logboekingangen (u kunt van logboekingangen als rijen van gegevens denken) in uw logboekbronnen. Voor elke rij gegevens neemt de transformatie de waarde van het opgegeven invoerveld, voert een reeks verwerkingsstappen uit en registreert het resultaat in het uitvoerveld dat u opgeeft. U kunt transformaties bepalen die tijdens of de logboekverwerking of transformatiefase van het proces van de datasetconstructie moeten worden uitgevoerd:

* **Tijdens logboekverwerking:De** Transformaties die tijdens de fase van de logboekverwerking van datasetconstructie worden uitgevoerd worden toegepast op elk verslag van gebeurtenisgegevens (logboekingang) om bestaande logboekgebieden bij te werken of nieuwe gebieden te produceren. De resultaten van de transformaties worden gebruikt samen met de voorwaarden van de logboekingang om te evalueren welke logboekingangen uit de dataset tijdens logboekverwerking worden gefiltreerd.
* **Tijdens transformatie:De** Transformaties die tijdens de transformatiefase van datasetconstructie worden uitgevoerd werken op de gebieden van gegevens die van logboekverwerking worden overgegaan om uitgebreide afmetingen tot stand te brengen die u in uw analyses kunt gebruiken. Zie [Uitgebreide Dimension](../../../home/c-dataset-const-proc/c-ex-dim/c-abt-ex-dim.md).

>[!NOTE]
>
>De gegevensinvoer naar transformatie van logverwerking wordt geordend door tijd en gegroepeerd door volgende identiteitskaart in uw brongegevens. Voor verschillende transformaties moeten de gegevens in dit formulier worden geschreven en alleen werken wanneer ze tijdens de transformatie worden gedefinieerd.

Wijzigingen in transformaties moeten met zorg worden aangebracht. De transformaties beïnvloeden niet welke logboekingangen in het proces van de datasetconstructie stromen, maar zij beïnvloeden de gepresenteerde resultaten. Hierdoor kunnen wijzigingen worden aangebracht in wat wordt geanalyseerd zonder dat de gegevens waarop de analyse is gebaseerd, worden gewijzigd. Wijzigingen in transformaties kunnen de waarden die in analyses worden geproduceerd, echter fundamenteel wijzigen.
