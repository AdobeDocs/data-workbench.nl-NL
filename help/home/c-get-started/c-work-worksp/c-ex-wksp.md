---
description: U kunt een werkruimte exporteren als een .png-afbeeldingsbestand of de gegevens uit bepaalde vensters exporteren naar een Excel-bestand (.xls of .xlsx).
title: Een werkruimte exporteren
uuid: 59ea6e46-d2e9-41f9-9c8f-e3071eb65424
exl-id: 87416ddf-2ac0-4f95-ae8e-71051061c757
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '774'
ht-degree: 0%

---

# Een werkruimte exporteren{#export-a-workspace}

U kunt een werkruimte exporteren als een .png-afbeeldingsbestand of de gegevens uit bepaalde vensters exporteren naar een Excel-bestand (.xls of .xlsx).

## Een werkruimte exporteren als een PNG-bestand {#section-f9fbe0f0a1c341e2b063cce106cac35e}

U kunt een momentopname van een werkruimte in Portable Network Graphic formaat (`.png` dossiers) opslaan. De volgende kleuropties zijn beschikbaar wanneer u werkruimten opslaat als `.png`-bestanden:

* **De zwarte** achtergrond kopieert de werkruimte zoals getoond.
* **De witte** achtergrond kopieert de elementen van de werkruimte in kleur en toont hen op een witte achtergrond.
* **De witte achtergrond (B&amp;W)** kopieert de elementen van de werkruimte in grijswaarden en toont hen op een witte achtergrond.

**Een werkruimte exporteren als een .png-bestand**

Klik in het menu van de titelbalk van een werkruimte op **[!UICONTROL Export]** > **[!UICONTROL Export PNG]** > *&lt;**[!UICONTROL color option]**>*.

Het dialoogvenster [!UICONTROL Save Image As] wordt weergegeven.

Navigeer naar de map waarin u het bestand wilt opslaan, wijzig indien nodig de naam van het bestand en klik op **[!UICONTROL Save]**.

## Werkruimtegegevens exporteren naar Microsoft Excel {#section-fe214e3dbc364d2eba3834d62d295acb}

Wanneer het uitvoeren van een werkruimte naar Excel, voert de Data Workbench gegevens van bepaalde visualisaties, afmeting en waardelegenda, en tekstannotaties naar een nieuw werkboek van Excel met één visualisatie per aantekenvel uit.

Als u werkruimten en afzonderlijke vensters wilt exporteren naar Microsoft Excel, moet aan de volgende vereisten worden voldaan:

* Microsoft Excel moet op dezelfde computer zijn geïnstalleerd als Data Workbench.
* De gebruikersrekening waaronder het proces van de Data Workbench loopt moet toestemming hebben om tot Microsoft Excel toegang te hebben.

>[!NOTE]
>
>* Wanneer u gegevens als dossiers van Excel uitvoert, opent u een nieuw geval van Excel. Zie [http://support.microsoft.com/kb/257757](http://support.microsoft.com/kb/257757) voor meer informatie over dit proces.
>* Hoewel de Data Workbench meer dan 256 kolommen en 65.536 rijen van gegevens steunt, de versies van Microsoft Excel voorafgaand aan 8.0 niet.
>



Als aan deze vereisten wordt voldaan, begint de Data Workbench automatisch Microsoft Excel en voert de gegevens naar een nieuw werkboek van Excel uit. Gegevens worden niet geëxporteerd uit de volgende visualisaties: grafieken, wegbrowsers, proceskaarten, verstrooiingspunten, en globes.

## Aangepaste titels toepassen {#section-a332e157554546cb8e88922a8d7a4fa2}

Tenzij u een titel van de Douane voor het venster op [!UICONTROL Export] menu hebt gespecificeerd, [!UICONTROL Export title] vermeld (bijvoorbeeld, de Lijst van de Plaats) wordt gebruikt als aantekenvelnaam.

1. Klik met de rechtermuisknop op de bovenrand van het venster en klik in het veld **[!UICONTROL Custom title]**.
1. Typ de titel die u op het venster wilt toepassen.

   ![](assets/mnu_window_TitleBar_Export.png)

>[!NOTE]
>
>Als u een afbreekstreepje (-) in het [!UICONTROL Custom title] gebied ingaat, wordt deze visualisatie niet uitgevoerd met de werkruimte.

Wanneer u de werkruimte naar Excel exporteert, wordt het werkblad met de gegevens voor dit venster benoemd met de titel die u hebt opgegeven in plaats van de titel in het veld [!UICONTROL Export title].

## Een werkruimte of zijbalk exporteren naar Excel {#section-360438b66d5f4734826ab463b4a01a75}

**Werkruimtegegevens exporteren naar een nieuw  [!DNL .xls] of  [!DNL .xlsx] bestand**

1. Klik in de titelbalk van de werkruimte op **[!UICONTROL Export]** > **[!UICONTROL Export]**.
1. Geef op of u de werkruimte, het zijpaneel of beide wilt exporteren.

## Exporteren naar een Excel-sjabloonbestand {#section-814772929ca64cf6b92b89d3fdd02302}

U kunt gegevens in uw werkruimte naar een dossier van malplaatjeExcel (`.xls` of `.xlsx`) uitvoeren. Als u een sjabloonbestand gebruikt, kan de hoeveelheid tijd die u besteedt aan het opmaken van de gegevens telkens wanneer de werkruimte wordt geëxporteerd, afnemen.

>[!NOTE]
>
>Dit sjabloonbestand moet een `.xls`- of `.xlsx`-bestand zijn, geen `.xlt`-bestand.

Wanneer de gegevens worden geëxporteerd, worden de bestaande tabbladen in de sjabloon (die elk één visualisatie vertegenwoordigen) opnieuw gevuld met de meest recente gegevens uit de werkruimte, terwijl nieuwe vensters die niet in de sjabloon aanwezig zijn als tabbladen worden genegeerd. Alle andere tabbladen in het sjabloonbestand blijven ongewijzigd.

Bovendien als u een macro hebt die in het dossier van malplaatjeExcel wordt bepaald dat u automatisch zou willen lopen wanneer het rapport wordt geproduceerd, noem de macro &quot;VSExport.&quot;

Stel dat u geëxporteerde campagnegegevens uit een tabelvisualisatie wilt gebruiken in een cirkeldiagram op een ander tabbladblad in een Excel-bestand en deze gegevens elke week wilt bijwerken. U kunt een sjabloon gebruiken zodat u de verwijzingen uit het tabbladblad van de tabel niet telkens opnieuw hoeft te maken naar het tabbladblad van het cirkeldiagram wanneer u de gegevens wilt bijwerken. De tabelgegevens worden bij het exporteren bijgewerkt. Hiermee wordt het cirkeldiagram automatisch bijgewerkt.

**Werkruimtegegevens exporteren naar een sjabloon  [!DNL .xls] of  [!DNL .xlsx] bestand**

1. Klik met de rechtermuisknop op de titelbalk van de werkruimte en klik op **[!UICONTROL Export]** > **[!UICONTROL Export to Excel from Template]**.
1. Geef op of u een werkruimte, zijbalk of beide wilt exporteren.

   Het dialoogvenster [!UICONTROL Select a template worksheet] wordt geopend.

1. Voer een van de volgende stappen uit:

   * Als u een `.xls` malplaatjedossier gebruikt:

      1. Blader naar het sjabloonbestand `.xls` en selecteer dit.
      1. Klik op **[!UICONTROL Open]**.
   * Als u een `.xlsx` malplaatjedossier gebruikt:

      1. Blader naar de locatie van het sjabloonbestand. De bestandsnaam `.xlsx` wordt niet weergegeven.
      1. Typ `.xlsx` in het veld [!UICONTROL File name] en klik op **[!UICONTROL Open]**. Alle `.xlsx` bestandsnamen worden weergegeven in de bestandenlijst.

      1. Selecteer het sjabloon `.xlsx` bestand.
      1. Klik op **[!UICONTROL Open]**.
