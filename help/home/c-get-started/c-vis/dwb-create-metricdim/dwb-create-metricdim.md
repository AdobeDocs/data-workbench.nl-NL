---
description: Gebruik de Metrische tovenaar van de Mam om een nieuwe Metrische Dimensie tot stand te brengen.
title: wizard Metrische schijf
uuid: 77b9bc8e-7625-4fef-9de4-f113f9b2debd
translation-type: tm+mt
source-git-commit: cb3ca4b3b993f5f04f6b6cee25850600ff3d8986

---


# wizard Metrische schijf{#metric-dim-wizard}

Gebruik de Metrische tovenaar van de Mam om een nieuwe Metrische Dimensie tot stand te brengen.

Een metrische Duim zet metrisch in een nieuwe dimensie om. Bijvoorbeeld, zal een Metrische Mam die op metrisch van de Meningen van de Pagina en het niveau van Bezoeker wordt gebaseerd afmetingselementen tonen die op de totale Meningen van de Pagina voor elke Bezoeker worden gebaseerd. Het laat u momenteel bepaalde metrisch uitbreiden gebaseerd op afmetingselementen om als nieuwe afmeting tot stand te brengen en te bewaren.

## Stap 1: uitgezochte afmeting en metrisch {#section-58b6ea7bbba5487ba1a3c264aa3dcb95}

1. **Open de Metrische Tovenaar** van de Mam.

   In een werkruimte, klik en selecteer **Hulpmiddelen** met de rechtermuisknop aan > **creeer Metrische Duim**.

1. **Noem de Metrische Dim**.

   Als gebrek, zal het gebied van de Naam op Niveau en de Metrische selecties worden gebaseerd automatisch bevolken.

1. **Selecteer een Dimension-niveau.** Het afmetingsniveau is de ouderafmeting die alle samenstellende elementenwaarden aan filterinput bevat en een afmetingstype bepaalt.

   De niveaus van de afmetingen omvatten:

   * Klikken
   * Hit
   * Product
   * Bezoek
   * Bezoeker

1. **Selecteer een metrisch**.

   Selecteer vooraf ingebouwd metrisch om zich uit te breiden en te bewaren als metrische mijl.

   ![](assets/6_4_workstation_metricdim_metric.png)

1. (facultatief) **creeer een Metrische Formule**.

   Klik de doos om een douane metrische formule in te gaan. De berekende waarde van de Voorproef zal het bevestigen van de uitdrukking lijken.

   ![](assets/6_4_workstation_metricdim_create_metric.png)

   U kunt uw eigen [metrische uitdrukking](https://docs.adobe.com/content/help/en/data-workbench/using/client/qry-lang-syntx/c-syntx-mtrc-exp.html) of besnoeiing en deeg van een andere metrische redacteur of visualisatie toevoegen. De fouten van de syntaxis, formulefouten, niet gedefiniëerde filters, en andere fouten worden gemeld in de tovenaar.

1. Klik op **Volgende**.

## Stap 2: formaat en vastgestelde emmers {#section-5bddf3cd306545d7806a501637f80f77}

U kunt het metrische formaat selecteren en de bucketwaarden voor een afmetingsuitdrukking plaatsen.

1. Selecteer een **Formaat** voor de nieuwe metrische mijl.

   ![](assets/6_4_workstation_metricdim_format_metric.png)

   Het formaat bepaalt hoe metrisch wanneer geopend in een visualisatie zal worden voorgesteld. Deze formaten worden geselecteerd [druk normen](http://www.cplusplus.com/reference/cstdio/printf/), die hieronder worden bepaald:

   ```
   %[flags][width][.precision][length][specifier]
   %
   0.2lf = % _ [flags] 0 [width] .2 [.precision] l [length] f[ specifier]
   ```

   Op het gebied van de **Voorproef** , zal een waarde gebaseerd op metrisch en geselecteerd formaat verschijnen.

1. Voeg de uitdrukking van de Telling van de **Emmer** toe.

   U kunt een metrische diepte met diverse waaiers, of emmers bepalen. Dit keert ondergroepen van elementen terug die op grootte worden gebaseerd, zoals [0-4], [5-10],...). De elementen van het Niveau van de Dimensie hebben op de elementen betrekking de waarvan waaier de waarde van metrisch bevat. Zie de beschrijving van de emmer uitdrukking bij [Syntax voor de Uitdrukkingen](https://docs.adobe.com/content/help/en/data-workbench/using/client/qry-lang-syntx/c-syntx-dim-exp.html)van de Dimensie.

1. Klik **Voorproef** aan open lijst van de Metrische waarden van de Duim alvorens te bewaren.

   ![](assets/6_4_workstation_metricdim_preview.png)

   De lijst detailleert metrische waarden per metrische diepte.

1. Klik **tonen in het Menu** van de Dimensie om de pas gecreëerde dimensie aan het lusje van de **Dimensie** in de **Vinder** toe te voegen.
1. Klik op **Volgende**.

## Stap 3: afwerken en opslaan {#section-d9043235b18a425f9de0db668d4b1683}

1. Selecteer om de Metrische Redacteur van de Duim, grafiekvisualisatie, of lijst na besparing te lanceren.

   | Veld | Beschrijving |
   |---|---|
   | Metrische map starten | Open de Metrische Redacteur van de Duim. |
   | Grafiek starten | Start een PNG-afbeelding van de tabel. |
   | Tabel starten | Lanceer een lijst in de werkruimte met waarden in kolommen die van de nieuwe metrische mijl een lijst maken vergeleken met waarden van geselecteerde metrisch. |

1. Klik op **Voltooien** en sla deze op.

   Een sparen dialoog zal openen toestaand u om het dossier op te slaan. De geselecteerde opties aan meningswaarden zullen in de werkruimte openen.

