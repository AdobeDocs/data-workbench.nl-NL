---
description: Elke DPU waarvan het dashboard gegevens moet visualiseren moet een Vraag API vergunning hebben.
title: Inschakelen van Query API controleren
uuid: deedd1a4-c476-49f6-9278-556d914d2b93
exl-id: 3dde2958-0f99-45f8-b65b-207a92362292
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 0%

---

# Inschakelen van Query API controleren{#verifying-query-api-enablement}

{{eol}}

Elke DPU waarvan het dashboard gegevens moet visualiseren moet een Vraag API vergunning hebben.

Hieronder vindt u instructies voor het valideren van de geïnstalleerde en ingeschakelde query-API.

1. Zoek het certificaat van uw gegevenswerkbankserver.
1. Open dit certificaat in een teksteditor.
1. Zorg ervoor dat de lijn `Product = Query API` bestaat in het certificaat.
1. In de **[!UICONTROL Trace]** map, opent u de [!DNL InsightServer64.log] in een teksteditor.
1. In de recentste ingangen van het startlogboek, zorg ervoor dat de lijn `Enabling Query API (licensed)` wordt weergegeven.

* Als de API voor query niet is ingeschakeld, wordt de vermelding weergegeven `Not enabling Query API (not licensed)`.
* Als u geen logboekingangen ziet, of vermoedt dat de server van de gegevenswerkbank opnieuw is begonnen sinds de Vraag API werd toegevoegd, te beginnen gelieve de server van de gegevenswerkbank opnieuw en het logboek te controleren.

   Als u niet kunt controleren of de API voor zoekopdrachten is ingeschakeld, neemt u contact op met de Adobe ClientCare voor hulp.
