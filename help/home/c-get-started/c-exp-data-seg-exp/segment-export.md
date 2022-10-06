---
description: Segmenten exporteren met de wizard Segment exporteren
title: wizard Segment exporteren
uuid: 705bdf00-54e5-4992-8978-91afda8c7543
exl-id: 6f42c5c6-a158-4ddd-8949-4ef55a44ed1c
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '460'
ht-degree: 0%

---

# wizard Segment exporteren{#segment-export-wizard}

{{eol}}

Segmenten exporteren met de wizard Segment exporteren

De de uitvoertovenaar van het segment verstrekt een geleidelijke proces om segmenten eerder dan te vormen en uit te voeren [segmenten exporteren uit een detailtabel](https://experienceleague.adobe.com/docs/data-workbench/using/client/export-data/c-sgmt-expt.html).

## Segmenten exporteren met de wizard {#section-b30f2699dbc7490bad18512b91cb0cb3}

Als u de wizard wilt openen, klikt u met de rechtermuisknop in een werkruimte en selecteert u **Beheer** > **Wizards** > **Wizard Segment exporteren**.

>[!NOTE]
>
>Alleen de segmenten die zijn toegepast voordat de wizard wordt geopend, worden vastgelegd. Ook, kan de segmentuitvoer die van de tovenaar wordt gecreeerd geen externe bevelen kweken.

1. Selecteer de verschillende bovenliggende niveaus van de dimensies en metriek die u wilt toevoegen aan de exportbewerking.

   Welke niveaus worden weergegeven, is afhankelijk van het geselecteerde profiel. U kunt meerdere dimensieniveaus selecteren op basis van het profiel.

   ![](assets/seg_wizard_1.png)

1. Klikken **Volgende**.
1. Selecteer de Dimension en Metriek voor de geselecteerde niveaus.

   Nadat u bijvoorbeeld Paginaweergave hebt geselecteerd als hoofdniveau, kunt u de onderliggende afmetingen en maatstaven selecteren die beschikbaar zijn om te worden geëxporteerd.

1. Klikken **Volgende**.

   ![](assets/seg_wizard_2.png)

   ![](assets/seg_wizard_2_1.png)

1. Selecteer de exportindeling en voer een naam voor het exportbestand in.

   ![](assets/seg_wizard_3.png)

   CSV, TSV, de Uitvoer van het Segment, en de Uitvoer van het Segment met de types van Kopbal hebben geen extra configuratie nodig. Nochtans, moeten de Profielen en de Uitvoer van het Publiek, de Dienst van het Verslag van de Douane en de Uitvoer van Adobe Target in Stap 3 worden gevormd. Zie bijvoorbeeld de configuratievelden voor de exportopties Profielen en Publiek. Deze exporttypen configureren en klikken **Volgende**.

   ![](assets/seg_wizard_3_1.png)

   ![](assets/seg_wizard_3_2.png)

   ![](assets/seg_wizard_3_3.png)

1. Configureer het geselecteerde exporttype.

   Koptekst—Als Koptekst waar is, geeft u de naam **Uitvoerbestand** veld.

   Escape-veld—Instellen als **Waar** of **Onwaar**.

   Volgorde van velden—Selecteer een veld en ga omhoog of omlaag om de volgorde in te stellen in het exportbestand.

   ![](assets/seg_wizard_4.png)

   Klikken **Volgende**.

1. Geef het niveau en de toegepaste filters weer in dit dialoogvenster. Klikken **Volgende**. ![](assets/seg_wizard_5.png)

1. Indien **CSV**, **TSV**, **Segment exporteren** of **Segment exporteren met koptekst** is geselecteerd, zijn er drie opties:

   Algemeen exporteren - Het uitvoerbestand wordt door de server gegenereerd in de map Server/Export.

   ![](assets/seg_wizard_6.png)

   FTP-export - Het uitvoerbestand wordt overgebracht naar de geselecteerde server. (De serverlijst wordt gekozen uit het bestand FTPServerInfo.cfg.)

   ![](assets/seg_wizard_6_1.png)

   SFTP-export - Het uitvoerbestand wordt veilig overgebracht naar de geselecteerde server.

1. Klikken **Volgende**

   **Opmerking:** Als het geselecteerde exporttype is **Profielen en publiek exporteren**, **Aangepaste recordservice**, en **Adobe Target Export** De tekst is statisch op basis van de geselecteerde exportbewerking.

1. Configureer de planningsparameters.

   **Eén opname** kan worden ingesteld op Waar of Onwaar.

   **Geavanceerde planning** U kunt aan of van door de Geavanceerde knoop van de Configuratie van de Planning te klikken worden aangezet.

   ![](assets/seg_wizard_7.png)

   Als het uitvoeren van de Lijst van het Detail, zal Één Opname weggaan als het Geavanceerde Plaatsen is. Klikken **Volgende**.

1. Geef een voorvertoning van het exportbestand weer en klik op **Exporteren uitvoeren**.

   ![](assets/seg_wizard_8.png)

   ![](assets/seg_wizard_8_1.png)

De volgende exporttypen zijn beschikbaar met de wizard:

**Exporttypen voor segmenten**

* Algemeen
* FTP
* SFTP

**Segment exporteren met koptekst**

* Algemeen
* FTP
* SFTP

**CSV-export**

* Algemeen
* FTP
* SFTP

**TSV-export**

* Algemeen
* FTP
* SFTP
