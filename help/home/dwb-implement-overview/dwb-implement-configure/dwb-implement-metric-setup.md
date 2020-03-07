---
description: Deze sectie verklaart hoe te om metriek in de Werkbank van Gegevens tot stand te brengen.
title: Metriek instellen
uuid: 57c1410b-c09c-4a59-b3a1-575323e1b8e3
translation-type: tm+mt
source-git-commit: ded50c4eeadea80156c17a4cad985d0ceddd5500

---


# Metriek instellen{#metrics-setup}

Deze sectie verklaart hoe te om metriek in de Werkbank van Gegevens tot stand te brengen.

## Inzicht in metriek {#section-f0412e851fcb4ac9886dca4003d42cec}

De metriek zijn kwantitatieve informatie over klantenactiviteit, zoals Meningen, Orden, aantal gemaakte vraag, en Opbrengsten. De metriek zijn de stichting van rapporten en helpen u gegevensverhoudingen bekijken en begrijpen.

De metrische Dimensie staat u toe om metrische tellingen door een specifiek Niveau te groeperen. Het staat u ook toe om metrische tellingen door een specifiek niveau te groeperen.

## Nieuwe statistieken maken {#section-60a413899d1b4707965e06fb5ef7fc4e}

Volg de stappen hieronder om nieuwe metrisch tot stand te brengen:

1. Klik **Hulpmiddel** > **Metrische Redacteur**.

1. In de metrische redacteur, ga de nieuwe Metrische naam en de formule in. ![](assets/dwb_impl_metrics1.png)

1. Sparen het aan de omslag van Metriek. ![](assets/dwb_impl_metrics2.png)

## Het creëren van en het Uitgeven van Voortgekomen Metriek {#section-ebdcd3ec652f485e90e001d694eab6d0}

Gebruik een Metrische Redacteur om nieuwe metrisch door naam, formule, en formaat te bepalen, die aan de [!DNL User\profile_name\Metrics] omslag voor recenter gebruik wordt bewaard.

1. Open een nieuwe Metrische Redacteur gebruikend **Admin > het menuoptie van het Profiel** of door de kolom van de Gebruiker voor de omslag met de rechtermuisknop aan te klikken waarin u metrisch wilt tot stand brengen en het klikken **creeert > Nieuw Metrisch**. Een metrische vertoningen van de Redacteur.

1. In de parameter van de *Naam* , typ een naam voor nieuwe metrisch.

   >[!NOTE]
   >
   >Merk op dat de ruimten () worden toegestaan terwijl de onderstreepingen (_) niet zijn. Bovendien kunt u niet de volgende symbolen gebruiken: + - * /

   ![](assets/dwb_impl_metrics3.png)

1. In de parameter van de *Formule* , typ een uitdrukking voor nieuwe metrisch.

   >[!NOTE]
   De filters moeten binnen steunen worden bepaald [ ] in de uitdrukking. Voor de extra metrische regels van de uitdrukkingssyntaxis, zie [Syntaxis voor Metrische Uitdrukkingen.](https://docs.adobe.com/content/help/en/data-workbench/using/client/qry-lang-syntx/c-syntx-mtrc-exp.html)

   Deze lijst verstrekt steekproefuitdrukkingen voor uitgebreide metriek. ![](assets/dwb_impl_metrics4.png)

   >[!NOTE]
   Wanneer een aangewezen uitdrukking is ingegaan, toont de voorproeflijn de waarde van nieuwe metrisch. Als er een fout in de uitdrukking is, toont de voorproeflijn een foutenmelding.

1. Klik met de rechtermuisknop en selecteer **Opslaan**. Wanneer u sparen metrisch, wordt een dossier dat nieuwe metrisch vertegenwoordigt gecreeerd op uw computer in de folder van de *Installatie DWB \User\profile name\Metrics* omslag.

## Bestaande afgeleide waarden bewerken {#section-4b5b7baf885b45cc8b358d1bd774e925}

1. In de Manager van het Profiel of de Manager van Metriek, in de kolom van de profielnaam, klik het vinkje voor het metrische dossier met de rechtermuisknop aan dat u wilt uitgeven en **maken Lokaal** klikken.
1. Klik het vinkje voor het metrische dossier in de kolom van de Gebruiker met de rechtermuisknop aan en klik **Open** van de werkbank.

   >[!NOTE]
   U kunt een Metrische Redacteur ook openen door om het even welk metrisch-verwant gebied binnen een visualisatie met de rechtermuisknop aan te klikken om het metrische menu te tonen.

1. In de **Metrische Redacteur**, geef en bewaar de metrische definitie uit zonodig gebruikend Stappen 2-4 in het *Creëren van Nieuwe Voortgekomen Metriek*.

   Als u alle gebruikers van het profiel zou willen metrisch gebruiken die u uitgeeft, moet u het aan het werkende profiel publiceren gebruikend de Manager van het Profiel.

Raadpleeg de documentatie voor meer hulp:

[Syntaxis voor metrische expressies](https://docs.adobe.com/content/help/en/data-workbench/using/client/qry-lang-syntx/c-syntx-mtrc-exp.html)

[Het creëren van en het Uitgeven van Voortgekomen Metriek](https://docs.adobe.com/content/help/en/data-workbench/using/client/admin-ui/profile-mgr/c-drvd-mtrcs.html)
