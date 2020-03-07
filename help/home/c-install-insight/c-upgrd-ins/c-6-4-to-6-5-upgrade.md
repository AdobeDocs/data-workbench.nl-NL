---
description: Volg deze stappen om aan de Werkbank van Gegevens v6.5 te bevorderen.
title: Verbetering 6.4 tot 6.5
uuid: b90b7b0c-7467-405f-a5ca-c40e69975d49
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Verbetering 6.4 tot 6.5{#upgrading-to}

Volg deze stappen om aan de Werkbank van Gegevens v6.5 te bevorderen.

## Vereisten en aanbevelingen voor upgrades {#section-8704a9ac358246cd81233dd0982d534f}

Volg deze vereisten en aanbevelingen wanneer het bevordering aan de Werkbank van Gegevens 6.5.

* De veranderingen in het **[!DNL Components for Processing Servers\Communications.cfg]** dossier vereisen u om dit dossier voor de versie bij te werken DWB 6.5. De *ingangen SourceListServer*, *SegmentExportServer*, en *NormalizeServer* werden verwijderd. ( DPU&#39;s zouden geen *sourcelist*, *segmentuitvoer*, of *normaliseer servers* moeten in werking stellen. )

* Correlatiekoord, correlatiematrix, Associatiekoord, Associatiematrix, Propensiteitsscore en visualisaties van de Attributie van de Beste Geschikte zijn nu multi-pass visualisaties.

   Wanneer er meer dan één multipass visualisaties in een werkruimte zijn, zal de Server van het Rapport er niet in slagen om rapporten door gebrek met de fout te produceren:

   ```
   Too many Multipass visualizations in workspace ....... (has #, 1 allowed).
   ```

   Vermijd deze fout door uw [!DNL ReportServer.cfg] dossier bij te werken of deze lijn toe te voegen aan uw bestaand dossier in de sectie van de *Rapportering* .

   ```
   Max Multipass Per Slice = int: n
   ```

   waar n het maximumaantal multi-pass visualisaties is die door de Server van het Rapport in een werkruimte worden gesteund.

