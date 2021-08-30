---
description: In deze sectie wordt uitgelegd hoe u metriek kunt maken in de Data Workbench.
title: Metrische instelling
uuid: 57c1410b-c09c-4a59-b3a1-575323e1b8e3
exl-id: a60c08d3-f708-43be-a14f-8b7f129f3ee5
source-git-commit: 232117a8cacaecf8e5d7fcaccc5290d6297947e5
workflow-type: tm+mt
source-wordcount: '466'
ht-degree: 0%

---

# Metrische instelling{#metrics-setup}

In deze sectie wordt uitgelegd hoe u metriek kunt maken in de Data Workbench.

## Werken met metriek {#section-f0412e851fcb4ac9886dca4003d42cec}

De metriek zijn kwantitatieve informatie over klantenactiviteit, zoals Bekijken, Orden, aantal gemaakte vraag, en Inkomsten. De metriek zijn de stichting van rapporten en helpen u gegevensverhoudingen bekijken en begrijpen.

Met Metrische Dimension kunt u metrische tellingen groeperen op een specifiek niveau. Het staat u ook toe om metrische tellingen door een specifiek niveau te groeperen.

## Nieuwe metriek maken {#section-60a413899d1b4707965e06fb5ef7fc4e}

Voer de onderstaande stappen uit om een nieuwe metrische waarde te maken:

1. Klik **Gereedschap** > **Metrische editor**.

1. In de metrische redacteur, ga de nieuwe Metrische naam en de formule in. ![](assets/dwb_impl_metrics1.png)

1. Sla het bestand op in de map Metrics. ![](assets/dwb_impl_metrics2.png)

## Afgeleide metriek maken en bewerken {#section-ebdcd3ec652f485e90e001d694eab6d0}

Gebruik een Metrische Redacteur om nieuwe metrische door naam, formule, en formaat te bepalen, die aan de [!DNL User\profile_name\Metrics] omslag voor later gebruik wordt bewaard.

1. Open een nieuwe Metrische Redacteur gebruikend **Admin > de menuoptie van het Profiel** of door de kolom van de Gebruiker voor de omslag met de rechtermuisknop te klikken waarin u metrisch wilt creëren en **creëren > Nieuwe Metrisch** te klikken. Er wordt een metrische editor weergegeven.

1. Typ in de parameter *Naam* een naam voor de nieuwe metrische waarde.

   >[!NOTE]
   >
   >Spaties ( ) zijn toegestaan terwijl onderstrepingstekens (_) dat niet doen. Bovendien kunt u de volgende symbolen niet gebruiken: + - * /

   ![](assets/dwb_impl_metrics3.png)

1. Typ in de parameter *Formule* een expressie voor de nieuwe metrische waarde.

   >[!NOTE]
   Filters moeten worden gedefinieerd tussen haakjes [ ] in de expressie. Zie [Syntaxis voor metrische expressies voor extra syntaxisregels voor metrische expressies.](https://experienceleague.adobe.com/docs/data-workbench/using/client/qry-lang-syntx/c-syntx-mtrc-exp.html)

   Deze lijst verstrekt steekproefuitdrukkingen voor uitgebreide metriek. ![](assets/dwb_impl_metrics4.png)

   >[!NOTE]
   Wanneer een aangewezen uitdrukking is ingegaan, toont de voorproeflijn de waarde van nieuwe metrisch. Als de expressie een fout bevat, wordt een foutbericht weergegeven in de voorbeeldregel.

1. Klik met de rechtermuisknop en selecteer **Opslaan**. Wanneer u metrisch bewaart, wordt een dossier dat nieuwe metrisch vertegenwoordigt gecreeerd op uw computer in de DWB *folder van de Installatie \User\profile name\Metrics* omslag.

## Bestaand afgeleide gegevens bewerken {#section-4b5b7baf885b45cc8b358d1bd774e925}

1. In de Manager van het Profiel of van Metriek, in de kolom van de profielnaam, klik het vinkje voor het metrische dossier met de rechtermuisknop aan dat u wilt uitgeven en **maken Lokaal** klikken.
1. Klik het vinkje voor het metrische dossier in de kolom van de Gebruiker met de rechtermuisknop aan en klik **Open** van de werkbank.

   >[!NOTE]
   U kunt een Metrische Redacteur ook openen door om het even welk metrisch-verwant gebied binnen een visualisatie met de rechtermuisknop aan te klikken om het metrische menu te tonen.

1. Bewerk en sla in de **Metrische editor** de metrische definitie zo nodig op met Stap 2-4 in *Nieuwe afgeleide metriek maken*.

   Als u wilt dat alle gebruikers van het profiel de metrische waarde gebruiken die u hebt bewerkt, moet u deze naar het werkprofiel publiceren met behulp van Profielbeheer.

Raadpleeg de documentatie voor meer hulp:

[Syntaxis voor metrische expressies](https://experienceleague.adobe.com/docs/data-workbench/using/client/qry-lang-syntx/c-syntx-mtrc-exp.html)

[Afgeleide metriek maken en bewerken](https://experienceleague.adobe.com/docs/data-workbench/using/client/admin-ui/profile-mgr/c-drvd-mtrcs.html)
