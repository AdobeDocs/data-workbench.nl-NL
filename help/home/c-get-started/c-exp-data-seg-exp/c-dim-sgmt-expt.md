---
description: Gegevens die u wilt exporteren, moeten worden gedefinieerd als een dimensie binnen het profiel.
title: Afmetingen maken voor gebruik met segmentexport
uuid: 7fdc043e-b2c5-4eac-adf4-bf60df6a3953
exl-id: 0f16c242-10f6-4014-b848-ea001e9d085c
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '164'
ht-degree: 0%

---

# Afmetingen maken voor gebruik met segmentexport{#create-dimensions-for-use-with-segment-export}

{{eol}}

Gegevens die u wilt exporteren, moeten worden gedefinieerd als een dimensie binnen het profiel.

Als de dimensie nog niet in het profiel bestaat, moet u deze maken. U kunt afmetingen maken met een van de volgende methoden:

* Een dimensie toevoegen aan de [!DNL Transformation.cfg] bestand. Zie de *Configuratie-handleiding voor gegevensset*.

* Een nieuwe [!DNL .dim] bestand. Zie [Afgeleide Dimension maken en bewerken](../../../home/c-get-started/c-admin-intrf/c-prof-mgr/c-dvrd-dim.md#concept-ece3c3ea8cdf4fc796680173993bff93).

* Maak selecties in een visualisatie zoals een proceskaart of een segment en sla de selecties op als een dimensie. Zie [Dimension opslaan van proceskaarten](../../../home/c-get-started/c-analysis-vis/c-proc-maps/t-dim-proc-maps.md#task-44d9e555d4a944e6aa81993eef703051) en [Segment-Dimension maken](../../../home/c-get-started/c-analysis-vis/c-seg/c-create-seg-dim.md#concept-70b363edcad14185ba8051646ad3d44e).

Wanneer u een gegevensveld exporteert, zoals de tracking-id of het e-mailadres (dat veel elementen kan bevatten), moet u een denormale dimensie maken waarin de onbewerkte gegevensreeksen worden opgeslagen.

Voor meer informatie over denormale afmetingen raadpleegt u de *Configuratie-handleiding voor gegevensset*.
