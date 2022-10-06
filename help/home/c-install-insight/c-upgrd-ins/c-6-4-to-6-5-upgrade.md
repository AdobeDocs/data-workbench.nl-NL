---
description: Voer de volgende stappen uit om te upgraden naar Data Workbench v6.5.
title: Upgrade van 6.4 naar 6.5
uuid: b90b7b0c-7467-405f-a5ca-c40e69975d49
exl-id: bcfd1ab1-2fb8-4bcd-b6c9-329143274ca4
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '146'
ht-degree: 0%

---

# Upgrade van 6.4 naar 6.5{#upgrading-to}

{{eol}}

Voer de volgende stappen uit om te upgraden naar Data Workbench v6.5.

## Upgradevereisten en Recommendations {#section-8704a9ac358246cd81233dd0982d534f}

Volg deze eisen en aanbevelingen wanneer het bevorderen aan Data Workbench 6.5.

* Wijzigingen in de **[!DNL Components for Processing Servers\Communications.cfg]** moet u dit bestand bijwerken voor de DWB 6.5-release. De *SourceListServer*, *SegmentExportServer*, en *NormalizeServer* items zijn verwijderd. ( DPU&#39;s moeten niet worden uitgevoerd *sourcelist*, *segmentexport*, of *servers normaliseren*. )

* Correlatiekoord, correlatiematrix, Associatiekoord, Associatiematrix, Propensiteitsscore en Best Fit Attribution-visualisaties zijn nu visualisaties met meerdere controles.

   Wanneer er meer dan één multi-pass visualisaties in een werkruimte zijn, zal de Server van het Rapport er niet in slagen rapporten door gebrek met de fout te produceren:

   ```
   Too many Multipass visualizations in workspace ....... (has #, 1 allowed).
   ```

   Vermijd deze fout door uw [!DNL ReportServer.cfg] of voeg deze regel toe aan het bestaande bestand in het dialoogvenster *Rapportage* sectie.

   ```
   Max Multipass Per Slice = int: n
   ```

   waarin n het maximumaantal multi-pass visualisaties is die door de Server van het Rapport in een werkruimte worden gesteund.
