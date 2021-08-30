---
description: Met de wizard Metrische grijswaarden kunt u een nieuwe metrische Dimension maken.
title: wizard Metrische grijswaarden
uuid: 77b9bc8e-7625-4fef-9de4-f113f9b2debd
exl-id: 109fbefc-5608-493d-aec9-8337f21eaa70
source-git-commit: 232117a8cacaecf8e5d7fcaccc5290d6297947e5
workflow-type: tm+mt
source-wordcount: '493'
ht-degree: 0%

---

# wizard Metrische grijswaarden{#metric-dim-wizard}

Met de wizard Metrische grijswaarden kunt u een nieuwe metrische Dimension maken.

Een metrische vorm zet metrisch om in een nieuwe afmeting. Met een metrische grijstint op basis van een meting van de paginaweergaven en het bezoekersniveau worden bijvoorbeeld dimensie-elementen weergegeven op basis van de totale paginaweergaven voor elke bezoeker. Het laat u momenteel bepaalde metrisch uitbreiden die op afmetingselementen wordt gebaseerd om als nieuwe afmeting tot stand te brengen en te bewaren.

## Stap 1: dimensie en metrisch selecteren {#section-58b6ea7bbba5487ba1a3c264aa3dcb95}

1. **Open de wizard** Metrische grijswaarden.

   Klik in een werkruimte met de rechtermuisknop en selecteer **Gereedschappen** > **Metrische gedim maken**.

1. **Geef de metrische gedim** een naam.

   Standaard wordt het veld Naam automatisch ingevuld op basis van de selecties Niveau en Metrisch.

1. **Selecteer een niveau Dimension.** Het dimensieniveau is de bovenliggende dimensie die alle elementwaarden bevat waarmee invoer wordt gefilterd en een dimensietype wordt gedefinieerd.

   Tot de Dimension-niveaus behoren:

   * Klikken
   * Actief
   * Product
   * Bezoek
   * Bezoeker

1. **Selecteer een metrisch**.

   Selecteer een vooraf gebouwde metrische waarde om uit te breiden en als metrische grootte te bewaren.

   ![](assets/6_4_workstation_metricdim_metric.png)

1. (optioneel) **Een metrische formule maken**.

   Klik op het vak om een aangepaste metrische formule in te voeren. De berekende waarde van de Voorproef zal het bevestigen van de uitdrukking verschijnen.

   ![](assets/6_4_workstation_metricdim_create_metric.png)

   U kunt uw eigen [metrische uitdrukking](https://experienceleague.adobe.com/docs/data-workbench/using/client/qry-lang-syntx/c-syntx-mtrc-exp.html) of besnoeiing en deeg van een andere metrische redacteur of visualisatie toevoegen. Syntaxisfouten, formulefouten, ongedefinieerde filters en andere fouten worden gerapporteerd in de wizard.

1. Klik **Volgende**.

## Stap 2: formaat en vastgestelde emmers {#section-5bddf3cd306545d7806a501637f80f77}

U kunt de metrische indeling selecteren en de emmerwaarden instellen voor een dimensie-expressie.

1. Selecteer een **formaat** voor de nieuwe metrische dimensie.

   ![](assets/6_4_workstation_metricdim_format_metric.png)

   Het formaat bepaalt hoe metrisch wanneer geopend in visualisatie zal worden voorgesteld. Deze indelingen zijn geselecteerd [afdrukstandaarden](http://www.cplusplus.com/reference/cstdio/printf/), zoals hieronder gedefinieerd:

   ```
   %[flags][width][.precision][length][specifier]
   %
   0.2lf = % _ [flags] 0 [width] .2 [.precision] l [length] f[ specifier]
   ```

   In het veld **Voorvertoning** wordt een waarde weergegeven op basis van de geselecteerde metrische waarde en indeling.

1. Voeg **Aantal emmertjes** uitdrukking toe.

   U kunt een metrische gedim met diverse waaiers, of emmers bepalen. Hiermee worden subsets van elementen geretourneerd op basis van grootte, zoals [0-4], [5-10],...). Elementen van het niveau Dimension hebben betrekking op de elementen waarvan het bereik de waarde van metrisch bevat. Zie de beschrijving van de bucket-expressie bij [Syntaxis voor Dimension-expressies](https://experienceleague.adobe.com/docs/data-workbench/using/client/qry-lang-syntx/c-syntx-dim-exp.html).

1. Klik **Voorvertoning** om de tabel met waarden voor metrische grijstinten te openen voordat u deze opslaat.

   ![](assets/6_4_workstation_metricdim_preview.png)

   De tabel geeft de metrische waarden per metrische afstand weer.

1. Klik **Tonen in menu Dimension** om de nieuwe dimensie toe te voegen aan het tabblad **Dimension** in **Finder**.
1. Klik **Volgende**.

## Stap 3: voltooien en opslaan {#section-d9043235b18a425f9de0db668d4b1683}

1. Selecteer deze optie om de Metrische grijze editor, grafiekvisualisatie of tabel te starten na het opslaan.

   | Veld | Beschrijving |
   |---|---|
   | Metrische grijswaarden-editor starten | Open de Metrische grijze editor. |
   | Grafiek starten | Start een PNG-afbeelding van de tabel. |
   | Tabel starten | Start een tabel in de werkruimte met waarden in kolommen die de waarden van het nieuwe metrische element aangeven ten opzichte van de waarden van het geselecteerde metrische element. |

1. Klik **Voltooien** en sparen.

   Er wordt een dialoogvenster voor opslaan geopend waarin u het bestand kunt opslaan. De geselecteerde opties voor het weergeven van waarden worden geopend in de werkruimte.
