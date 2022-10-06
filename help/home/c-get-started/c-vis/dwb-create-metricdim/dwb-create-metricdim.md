---
description: Met de wizard Metrische grijswaarden kunt u een nieuwe metrische Dimension maken.
title: wizard Metrische grijswaarden
uuid: 77b9bc8e-7625-4fef-9de4-f113f9b2debd
exl-id: 109fbefc-5608-493d-aec9-8337f21eaa70
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '493'
ht-degree: 0%

---

# wizard Metrische grijswaarden{#metric-dim-wizard}

{{eol}}

Met de wizard Metrische grijswaarden kunt u een nieuwe metrische Dimension maken.

Een metrische vorm zet metrisch om in een nieuwe afmeting. Met een metrische grijstint op basis van een meting van de paginaweergaven en het bezoekersniveau worden bijvoorbeeld dimensie-elementen weergegeven op basis van de totale paginaweergaven voor elke bezoeker. Het laat u momenteel bepaalde metrisch uitbreiden die op afmetingselementen wordt gebaseerd om als nieuwe afmeting tot stand te brengen en te bewaren.

## Stap 1: dimensie en metrisch selecteren {#section-58b6ea7bbba5487ba1a3c264aa3dcb95}

1. **De wizard Metrische grijswaarden openen**.

   Klik in een werkruimte met de rechtermuisknop en selecteer **Gereedschappen** > **Metrische grijswaarden maken**.

1. **Geef de metrische vorm een naam**.

   Standaard wordt het veld Naam automatisch ingevuld op basis van de selecties Niveau en Metrisch.

1. **Selecteer een niveau Dimension.** Het dimensieniveau is de bovenliggende dimensie die alle elementwaarden bevat waarmee invoer wordt gefilterd en een dimensietype wordt gedefinieerd.

   Tot de Dimension-niveaus behoren:

   * Klikken
   * Actief
   * Product
   * Bezoek
   * Bezoeker

1. **Een metrisch object selecteren**.

   Selecteer een vooraf gebouwde metrische waarde om uit te breiden en als metrische grootte te bewaren.

   ![](assets/6_4_workstation_metricdim_metric.png)

1. (optioneel) **Een metrische formule maken**.

   Klik op het vak om een aangepaste metrische formule in te voeren. De berekende waarde van de Voorproef zal het bevestigen van de uitdrukking verschijnen.

   ![](assets/6_4_workstation_metricdim_create_metric.png)

   U kunt uw eigen [metrische expressie](https://experienceleague.adobe.com/docs/data-workbench/using/client/qry-lang-syntx/c-syntx-mtrc-exp.html) of knippen en plakken in een andere metrische editor of visualisatie. Syntaxisfouten, formulefouten, ongedefinieerde filters en andere fouten worden gerapporteerd in de wizard.

1. Klikken **Volgende**.

## Stap 2: formaat en vastgestelde emmers {#section-5bddf3cd306545d7806a501637f80f77}

U kunt de metrische indeling selecteren en de emmerwaarden instellen voor een dimensie-expressie.

1. Selecteer een **Indeling** voor de nieuwe metrische gedim.

   ![](assets/6_4_workstation_metricdim_format_metric.png)

   Het formaat bepaalt hoe metrisch wanneer geopend in visualisatie zal worden voorgesteld. Deze indelingen zijn geselecteerd [printstandaarden](https://www.cplusplus.com/reference/cstdio/printf/), zoals hieronder gedefinieerd:

   ```
   %[flags][width][.precision][length][specifier]
   %
   0.2lf = % _ [flags] 0 [width] .2 [.precision] l [length] f[ specifier]
   ```

   In de **Voorvertoning** wordt een waarde weergegeven op basis van de geselecteerde metrische waarde en notatie.

1. Toevoegen **Aantal emmertjes** expressie.

   U kunt een metrische gedim met diverse waaiers, of emmers bepalen. Hiermee worden subsets van elementen geretourneerd op basis van grootte, zoals [0-4], [5-10],...). Elementen van het niveau Dimension hebben betrekking op de elementen waarvan het bereik de waarde van metrisch bevat. Zie de beschrijving van de bucket-expressie op [Syntaxis voor Dimension-expressies](https://experienceleague.adobe.com/docs/data-workbench/using/client/qry-lang-syntx/c-syntx-dim-exp.html).

1. Klikken **Voorvertoning** om de tabel met waarden voor metrische grijswaarden te openen voordat u deze opslaat.

   ![](assets/6_4_workstation_metricdim_preview.png)

   De tabel geeft de metrische waarden per metrische afstand weer.

1. Klikken **Tonen in menu Dimension** om de nieuwe dimensie toe te voegen aan de **Dimension** in de **Finder**.
1. Klikken **Volgende**.

## Stap 3: voltooien en opslaan {#section-d9043235b18a425f9de0db668d4b1683}

1. Selecteer deze optie om de Metrische grijze editor, grafiekvisualisatie of tabel te starten na het opslaan.

   | Veld | Beschrijving |
   |---|---|
   | Metrische grijswaarden-editor starten | Open de Metrische grijze editor. |
   | Grafiek starten | Start een PNG-afbeelding van de tabel. |
   | Tabel starten | Start een tabel in de werkruimte met waarden in kolommen die de waarden van het nieuwe metrische element aangeven ten opzichte van de waarden van het geselecteerde metrische element. |

1. Klikken **Voltooien** en opslaan.

   Er wordt een dialoogvenster voor opslaan geopend waarin u het bestand kunt opslaan. De geselecteerde opties voor het weergeven van waarden worden geopend in de werkruimte.
