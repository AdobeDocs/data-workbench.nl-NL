---
description: Deze sectie is een snelle gids die u de minimumstappen geeft die aan opstelling worden vereist en manuscripten plannen om uw logboekdossiers wekelijks te verwerken. Dit kan als verwijzingsgids aan opstelling worden gebruikt of uw profielen wijzigen.
title: Scripting voor wekelijkse herverwerking
uuid: d3cd163d-6129-4883-ac7c-b2f75b5eb247
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Scripting voor wekelijkse herverwerking{#scripting-to-weekly-reprocess}

Deze sectie is een snelle gids die u de minimumstappen geeft die aan opstelling worden vereist en manuscripten plannen om uw logboekdossiers wekelijks te verwerken. Dit kan als verwijzingsgids aan opstelling worden gebruikt of uw profielen wijzigen.

## Wat is opnieuw verwerken {#section-7e335aacc199488592e78a835e2649fe}

Het laden van de gegevens aan DWB die op veranderingen in gegevensbronnen, off-line gegevensbronnen, of tijdspanne wordt gebaseerd. Het manuscript zal de parameter van de begindatum in het dossier van het *Logboek Processing.cfg* opnieuw verwerken.

## Voorwaarden {#section-804acce5df4942469c9313535627038a}

ID van de Reeks van het rapport, het Aantal maandgegevens zou in DWB beschikbaar moeten zijn. De omslag Perl64 zou in uw C:\ drive beschikbaar moeten zijn.

## Logbestanden opnieuw verwerken {#section-565d3e1f0df14127a97d9beecd14f02f}

Verstrek hierboven details (eerste vereisten) in het manuscript van het venstersbevel *Reprocess.bat* beschikbaar bij omslag *\scripts\Log Processing* bij de Belangrijkste server van FSU.

Dit manuscript zal intern twee cliënt-specifieke manuscripten roepen: Een om de gegevens en andere voor e-mailberichten opnieuw te verwerken. Deze twee manuscripten zijn ook beschikbaar in de omslag *\scripts\Log Processing* .

Het manuscript zal herprocesparameters in het *Logboek Processing.cfg* - dossier veranderen.

## Rollend Venster voor Logboeken {#section-ed5f44d890b34523ab33da7aa0ae3990}

Verstrek details (eerste vereisten) in het manuscript van het venstersbevel *logprocessing date.bat* beschikbaar bij omslag *\scripts\Scripository* op de server van de maing FSU. Dit manuscript zal intern twee cliënt-specifieke manuscripten roepen: Eén voor het instellen van begindatum van logboeken en een andere voor e-mailwaarschuwingen. Deze twee scripts zijn ook beschikbaar in* \scripts\Scripository*

Verstrek de Reeks van het Rapport identiteitskaart en aantal maanden in het* logprocessing date.bat* dossier.

Het manuscript zal de parameter van de begindatum in *Logboek Processing.cfg* veranderen.

>[!NOTE]
>
>Als de map *Bewaarplaats* niet beschikbaar is, volgt u het onderstaande proces om de map *Bewaarplaats* te kopiëren en wijzigingen in bovenstaande bestanden aan te brengen met behulp van specifieke gegevens voor de klant. En geef je e-mailadres op om een melding te ontvangen in het geval van een fout.

## Scripts plannen {#section-063cf0c755dc47d28d60947d8d43d0e9}

Volg deze stappen om de manuscripten in de de taakplanner van Vensters te plannen.

1. Plan het manuscript in de taakplanner van Vensters.

   * Open taakplanner: Klik met de rechtermuisknop op de **taakplannerbibliotheek** en klik op **Taak** maken.

   * In het **Algemene** lusje verstrek een taaknaam en selecteer **Opties**.

   * Onder het lusje van **Trekkers** , klik **Nieuw** en een nieuw venster zal openen.

   * Onder het lusje van **Acties** , klik **Nieuw** en een nieuw venster zal openen. Dan verstrek manuscriptdetails en andere opties. (Het Begin binnen zal een weg hebben waar het manuscript wordt geplaatst).

1. Validatie: Klik en stel de baan in werking en verifieer veranderingen in het *Logprocessing.cfg* - dossier met de rechtermuisknop aan. Er wordt een e-mail gestuurd naar de e-mailid die in het script wordt opgegeven.

