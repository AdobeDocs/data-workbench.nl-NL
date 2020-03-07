---
description: Elke DPU waarvan het dashboard gegevens moet visualiseren moet een vergunning van de Vraag hebben API.
solution: Analytics
title: Het verifiëren van Vraag API Enablement
topic: Data workbench
uuid: deedd1a4-c476-49f6-9278-556d914d2b93
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Het verifiëren van Vraag API Enablement{#verifying-query-api-enablement}

Elke DPU waarvan het dashboard gegevens moet visualiseren moet een vergunning van de Vraag hebben API.

Hieronder zijn sommige instructies op hoe te om te bevestigen dat de Vraag API geïnstalleerd en toegelaten is.

1. Vind het certificaat van uw server van de gegevenswerkbank.
1. Open dit certificaat in een tekstredacteur.
1. Zorg ervoor dat de lijn in het certificaat `Product = Query API` bestaat.
1. In de **[!UICONTROL Trace]** omslag, open [!DNL InsightServer64.log] in een tekstredacteur.
1. In de recentste beginlogboekingangen, zorg ervoor dat de lijn `Enabling Query API (licensed)` verschijnt.

* Als de Vraag API niet wordt toegelaten, zult u de ingang zien `Not enabling Query API (not licensed)`.
* Als u geen logboekingangen ziet, of verdacht dat de server van de gegevenswerkbank opnieuw is begonnen sinds de Vraag API werd toegevoegd, te beginnen gelieve de server van de gegevenswerkbank opnieuw opnieuw en het logboek te controleren.

   Als u niet kunt bevestigen dat de Vraag API wordt toegelaten, te contacteren gelieve Adobe ClientCare voor hulp.
