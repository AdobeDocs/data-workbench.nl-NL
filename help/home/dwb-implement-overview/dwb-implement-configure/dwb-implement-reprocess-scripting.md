---
description: Deze sectie is een snelle gids die u de minimale stappen geeft die worden vereist om manuscripten op te zetten en te plannen om uw logboekdossiers wekelijks te verwerken. Dit kan als naslaggids worden gebruikt om uw profielen in te stellen of te wijzigen.
title: Scripting voor wekelijkse herverwerking
uuid: d3cd163d-6129-4883-ac7c-b2f75b5eb247
exl-id: f1b6f12e-629e-47c7-aa15-41f76d1c3192
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '434'
ht-degree: 0%

---

# Scripting voor wekelijkse herverwerking{#scripting-to-weekly-reprocess}

{{eol}}

Deze sectie is een snelle gids die u de minimale stappen geeft die worden vereist om manuscripten op te zetten en te plannen om uw logboekdossiers wekelijks te verwerken. Dit kan als naslaggids worden gebruikt om uw profielen in te stellen of te wijzigen.

## Wat is opnieuw verwerken {#section-7e335aacc199488592e78a835e2649fe}

De gegevens laden naar DWB op basis van wijzigingen in gegevensbronnen, offlinegegevensbronnen of tijdsperiode. Het script verwerkt de begindatumparameter in *Logverwerking.cfg* bestand.

## Vereisten {#section-804acce5df4942469c9313535627038a}

De Reeks ID van het rapport, Aantal maandgegevens zou in DWB beschikbaar moeten zijn. De map Perl64 moet beschikbaar zijn in uw C:\ drive.

## Logbestanden opnieuw verwerken {#section-565d3e1f0df14127a97d9beecd14f02f}

Verstrek hierboven details (eerste vereisten) in het manuscript van het venstersbevel *Opnieuw verwerken.bat* beschikbaar in map *\scripts\Log Processing* op de hoofdserver van de FSU.

Dit script roept intern twee clientspecifieke scripts op: Eén om de gegevens opnieuw te verwerken en een andere voor een e-mailwaarschuwing. Deze twee scripts zijn ook beschikbaar in het dialoogvenster *\scripts\Log Processing* map.

Het script wijzigt de parameters voor opnieuw verwerken in het dialoogvenster *Logverwerking.cfg* bestand.

## Rolvenster voor logbestanden {#section-ed5f44d890b34523ab33da7aa0ae3990}

Verstrek details (eerste vereisten) in het manuscript van het venstersbevel *logprocessingDate.bat* beschikbaar in map *\scripts\Scripting* op de overeenkomstige FSU-server. Dit script roept intern twee clientspecifieke scripts op: Eén voor het instellen van de begindatum van logboeken en een andere voor e-mailwaarschuwingen. Deze twee scripts zijn ook beschikbaar in* \scripts\Scripts*

Geef de rapportsuite-id en het aantal maanden op in het bestand* logprocessing date.bat*.

Het script wijzigt de begindatumparameter in *Logverwerking.cfg*.

>[!NOTE]
>
>Als de *Scriptplaats* de map is niet beschikbaar, volgt u het onderstaande proces om de map te kopiëren *Scriptplaats* en breng wijzigingen aan in bovenstaande bestanden met gebruik van specifieke gegevens voor de klant. Geef uw e-mailadres op om een waarschuwing op te halen in het geval van een fout.

## Scripts plannen {#section-063cf0c755dc47d28d60947d8d43d0e9}

Volg deze stappen om de manuscripten in de taakplanner van Vensters te plannen.

1. Plan het manuscript in de taakplanner van Vensters.

   * Taakplanner openen: Klik met de rechtermuisknop op de knop **Taakplanningsbibliotheek** en klik op **Taak maken**.

   * In de **Algemeen** tabblad geeft een taaknaam op en selecteert u **Opties**.

   * Onder de **Triggers** tabblad, klikt u op **Nieuw** en er wordt een nieuw venster geopend.

   * Onder de **Handelingen** tabblad, klikt u op **Nieuw** en er wordt een nieuw venster geopend. Geef vervolgens scriptdetails en andere opties op. (Begin in zal een weg hebben waar het manuscript wordt geplaatst).

1. Validatie: Klik met de rechtermuisknop en voer de taak uit en controleer de wijzigingen in het dialoogvenster *Logverwerking.cfg* bestand. Er wordt een e-mail verzonden naar de e-mailid die in het script is opgegeven.
