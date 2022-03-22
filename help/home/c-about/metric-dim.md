---
description: Creeer Dimension die door metrische attributen (Metrische Dims) worden bepaald gebruikend een geleidelijke tovenaar. Vervolgens test, bekijkt u een voorvertoning en slaat u de nieuwe metrische gedim op in de lijst met Dimension.
title: Metrische wizard (Dimension)
uuid: 411b2e28-0958-43bb-a853-7de7b3063818
exl-id: 4d283a00-409c-4d74-a558-40744caba71c
source-git-commit: 235b8816c7397ac1ab71df650a1d4c2d681b3b2d
workflow-type: tm+mt
source-wordcount: '486'
ht-degree: 1%

---

# wizard Metrische grijswaarden{#metric-dim-wizard}

Creeer Dimension die door metrische attributen (Metrische Dims) worden bepaald gebruikend een geleidelijke tovenaar. Vervolgens test, bekijkt u een voorvertoning en slaat u de nieuwe metrische gedim op in de lijst met Dimension.

Een metrische vorm zet metrisch om in een nieuwe afmeting. Met een metrische grijstint op basis van een meting van de paginaweergaven en het bezoekersniveau worden bijvoorbeeld dimensie-elementen weergegeven op basis van de totale paginaweergaven voor elke bezoeker. Het laat u momenteel bepaalde metrisch uitbreiden die op afmetingselementen wordt gebaseerd om als nieuwe afmeting tot stand te brengen en te bewaren.

## Stap 1: Dimension en metrisch selecteren {#section-58b6ea7bbba5487ba1a3c264aa3dcb95}

1. Open de wizard Metrische grijswaarden.

   Klik in een werkruimte met de rechtermuisknop en selecteer **[!UICONTROL Tools]** > **[!UICONTROL Create Metric Dim]**.

1. Geef de metrische gedim een naam.

   Standaard wordt het veld Naam automatisch ingevuld op basis van de selecties Niveau en Metrisch.

1. Selecteer een niveau Dimension.

   Het dimensieniveau is de bovenliggende dimensie die alle elementwaarden bevat waarmee invoer wordt gefilterd en een dimensietype wordt gedefinieerd.

   Tot de Dimension-niveaus behoren:

   * Klikken
   * Actief
   * Product
   * Bezoek
   * Bezoeker

1. Selecteer een metrisch object.

   Selecteer een vooraf gebouwde metrische waarde om uit te breiden en als metrische grootte te bewaren.

   ![](assets/6_4_workstation_metricdim_metric.png)

1. (Optioneel) Maak een metrische formule.

   Klik op het vak om een aangepaste metrische formule in te voeren. De berekende waarde van de Voorproef zal het bevestigen van de uitdrukking verschijnen.

   ![](assets/6_4_workstation_metricdim_create_metric.png)

   U kunt uw eigen [metrische expressie](https://experienceleague.adobe.com/docs/data-workbench/using/client/qry-lang-syntx/c-syntx-mtrc-exp.html) of knippen en plakken in een andere metrische editor of visualisatie. Syntaxisfouten, formulefouten, ongedefinieerde filters en andere fouten worden gerapporteerd in de wizard.

1. Klik op **[!UICONTROL Next]**.

## Stap 2: Emmers opmaken en instellen {#section-5bddf3cd306545d7806a501637f80f77}

1. Selecteer een indeling voor de nieuwe metrische gedim.

   ![](assets/6_4_workstation_metricdim_format_metric.png)

   Het formaat bepaalt hoe metrisch wanneer geopend in visualisatie zal worden voorgesteld. Deze indelingen zijn geselecteerd [printstandaarden](https://www.cplusplus.com/reference/cstdio/printf/), zoals hieronder gedefinieerd:

   ```
   %[flags][width][.precision][length][specifier]
   % 0.2lf = % _ [flags] 0 [width] .2 [.precision] l [length] f[ specifier]
   ```

   In de **[!UICONTROL Preview]** wordt een waarde weergegeven op basis van de geselecteerde metrische waarde en notatie.

1. Voeg expressie Aantal emmertjes toe.

   U kunt een metrische gedim met diverse waaiers, of emmers bepalen. Hiermee worden subsets van elementen geretourneerd op basis van grootte, zoals [0-4], [5-10],...). Elementen van het niveau Dimension hebben betrekking op de elementen waarvan het bereik de waarde van metrisch bevat. Zie de beschrijving van de bucket-expressie op [Syntaxis voor Dimension-expressies](https://experienceleague.adobe.com/docs/data-workbench/using/client/qry-lang-syntx/c-syntx-dim-exp.html).

1. Klikken **[!UICONTROL Preview]** om de tabel met waarden voor metrische grijswaarden te openen voordat u deze opslaat.

   ![](assets/6_4_workstation_metricdim_preview.png)

   De tabel geeft de metrische waarden per metrische afstand weer.

1. Klikken **[!UICONTROL Show in Dimension Menu]** om de nieuwe dimensie toe te voegen aan de **Dimension** in de **Finder**.

1. Klik op **[!UICONTROL Next]**.

## Stap 3: Voltooien en opslaan {#section-d9043235b18a425f9de0db668d4b1683}

1. Selecteer deze optie om de Metrische grijze editor, grafiekvisualisatie of tabel te starten na het opslaan.

   | Veld | Beschrijving |
   |---|---|
   | **[!UICONTROL Launch Metric Dim Editor]** | Open de Metrische grijze editor. |
   | **[!UICONTROL Launch Graph]** | Start een PNG-afbeelding van de tabel. |
   | **[!UICONTROL Launch Table]** | Start een tabel in de werkruimte met waarden in kolommen die de waarden van het nieuwe metrische element aangeven ten opzichte van de waarden van het geselecteerde metrische element. |

1. Klikken **[!UICONTROL Finish]** en opslaan.

   Er wordt een dialoogvenster voor opslaan geopend waarin u het bestand kunt opslaan. De geselecteerde opties voor het weergeven van waarden worden geopend in de werkruimte.
