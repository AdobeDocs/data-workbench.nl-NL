---
description: U kunt een werkruimte als .png beelddossier uitvoeren of de gegevens van bepaalde vensters uitvoeren naar een dossier van Excel (.xls of .xlsx).
solution: Analytics
title: Een werkruimte exporteren
topic: Data workbench
uuid: 59ea6e46-d2e9-41f9-9c8f-e3071eb65424
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Een werkruimte exporteren{#export-a-workspace}

U kunt een werkruimte als .png beelddossier uitvoeren of de gegevens van bepaalde vensters uitvoeren naar een dossier van Excel (.xls of .xlsx).

## Een werkruimte exporteren als een PNG-bestand {#section-f9fbe0f0a1c341e2b063cce106cac35e}

U kunt een momentopname van een werkruimte in het Draagbare formaat van het Netwerk Grafische (`.png` dossiers) bewaren. De volgende kleurenopties zijn beschikbaar wanneer het bewaren van werkruimten als `.png` dossiers:

* **De zwarte achtergrond** kopieert de werkruimte zoals getoond.
* **De witte achtergrond** kopieert de elementen van de werkruimte in kleur en toont hen op een witte achtergrond.
* **De witte achtergrond (B&amp;W)** kopieert de elementen van de werkruimte in grayscale en toont hen op een witte achtergrond.

**Om een werkruimte als .png dossier uit te voeren**

In het menu van de titelbar van een werkruimte, klik **[!UICONTROL Export]** > **[!UICONTROL Export PNG]** > *&lt;**[!UICONTROL color option]**>*.

De [!UICONTROL Save Image As] dialoogdoos verschijnt.

Navigeer aan de folder waarin u het dossier wilt bewaren, de naam van het dossier indien nodig veranderen, en klikken **[!UICONTROL Save]**.

## De werkruimtegegevens van de uitvoer naar Microsoft Excel {#section-fe214e3dbc364d2eba3834d62d295acb}

Wanneer het uitvoeren van een werkruimte naar Excel, voert de Werkbank van Gegevens gegevens gegevens van bepaalde visualisaties, afmeting en waardelegends, en tekstannotaties aan een nieuw werkboek van Excel met één visualisatie per aantekenvel uit.

Om werkruimten en individuele vensters naar Microsoft Excel uit te voeren, moet aan de volgende vereisten worden voldaan:

* Microsoft Excel moet op het zelfde systeem worden geïnstalleerd zoals de Werkbank van Gegevens.
* De gebruikersrekening waaronder het proces van de Werkbank van Gegevens loopt moet toestemming hebben om tot Microsoft Excel toegang te hebben.

>[!NOTE]
>
>* Wanneer u gegevens als dossiers van Excel uitvoert, opent u een nieuw geval van Excel. Voor meer informatie over dit proces, zie [http://support.microsoft.com/kb/257757](http://support.microsoft.com/kb/257757).
>* Hoewel de Werkbank van Gegevens meer dan 256 kolommen en 65.536 rijen van gegevens steunt, de versies van Microsoft Excel voorafgaand aan 8.0 niet.
>



Als aan deze vereisten wordt voldaan, begint de Werkbank van Gegevens automatisch Microsoft Excel en voert de gegevens naar een nieuw werkboek van Excel uit. De gegevens worden niet uitgevoerd uit de volgende visualisaties: grafieken, wegbrowsers, proceskaarten, verspreidingspercelen, en globes.

## Aangepaste titels toepassen {#section-a332e157554546cb8e88922a8d7a4fa2}

Tenzij u een titel van de Douane voor het venster op het [!UICONTROL Export] menu hebt gespecificeerd, wordt [!UICONTROL Export title] vermeld (bijvoorbeeld, de Lijst van de Stad) gebruikt als aantekenvelnaam.

1. Klik de hoogste grens van het venster met de rechtermuisknop aan en klik op het **[!UICONTROL Custom title]** gebied.
1. Typ de titel die u op het venster wilt toepassen.

   ![](assets/mnu_window_TitleBar_Export.png)

>[!NOTE]
>
>Als u een koppelteken (-) op het [!UICONTROL Custom title] gebied ingaat, wordt deze visualisatie niet uitgevoerd met de werkruimte.

Wanneer u de werkruimte naar Excel uitvoert, wordt het aantekenvel dat de gegevens voor dit venster bevat genoemd gebruikend de titel die u in plaats van de titel op het [!UICONTROL Export title] gebied specificeerde.

## Voer een werkruimte of sidebar naar Excel uit {#section-360438b66d5f4734826ab463b4a01a75}

**Om werkruimtegegevens naar een nieuw[!DNL .xls]of[!DNL .xlsx]dossier uit te voeren**

1. In titelbar van de werkruimte, klik **[!UICONTROL Export]** > **[!UICONTROL Export]**.
1. Specificeer of om de werkruimte, sidebar, of allebei uit te voeren.

## De uitvoer naar een dossier van malplaatjeExcel {#section-814772929ca64cf6b92b89d3fdd02302}

U kunt gegevens in uw werkruimte naar een dossier van malplaatjeExcel uitvoeren (`.xls` of `.xlsx`). Het gebruiken van een malplaatjedossier kan de hoeveelheid tijd verminderen dat u het formatteren van uw gegevens besteedt telkens als de werkruimte wordt uitgevoerd.

>[!NOTE]
>
>Dit malplaatjedossier moet een `.xls` of `.xlsx` dossier, niet een `.xlt` dossier zijn.

Wanneer het gegeven wordt uitgevoerd, worden de bestaande van labels voorzien bladen in het malplaatje (elk die één visualisatie vertegenwoordigen) herhaald met de meest recente gegevens van de werkruimte, terwijl om het even welke nieuwe vensters die niet aanwezig in het malplaatje zijn aangezien de van labels voorzien bladen worden genegeerd. Om het even welke andere van labels voorzien bladen in het malplaatjedossier blijven onveranderd.

Bovendien als u een macro hebt die in het dossier van malplaatjeExcel wordt bepaald dat u automatisch zou willen lopen wanneer het rapport wordt geproduceerd, noem de macro &quot;VSExport.&quot;

Zeg dat u uitgevoerde campagnegegevens van een lijstvisualisatie in een cirkeldiagram op een ander van labels voorzien blad in een dossier van Excel wilt gebruiken en deze informatie willen elke week bijwerken. U kunt een malplaatje gebruiken zodat u niet uw verwijzingen van het van labels voorzien blad van de lijst aan het van labels voorzien blad van het cirkeldiagram moet ontspannen telkens als u de gegevens wilt bijwerken. De lijstgegevens worden bijgewerkt bij de uitvoer, die automatisch het cirkeldiagram bijwerkt.

**Om werkruimtegegevens naar een malplaatje[!DNL .xls]of een[!DNL .xlsx]dossier uit te voeren**

1. Klik de titelbar van de werkruimte met de rechtermuisknop aan en klik **[!UICONTROL Export]** > **[!UICONTROL Export to Excel from Template]**.
1. Specificeer of om een werkruimte, sidebar, of allebei uit te voeren.

   Het [!UICONTROL Select a template worksheet] dialoogvenster wordt geopend.

1. Voer een van de volgende stappen uit, indien van toepassing:

   * Als u een `.xls` sjabloonbestand gebruikt:

      1. Blader naar en selecteer het sjabloonbestand `.xls` .
      1. Klik op **[!UICONTROL Open]**.
   * Als u een `.xlsx` sjabloonbestand gebruikt:

      1. Doorblader aan de plaats van het malplaatjedossier. De `.xlsx` bestandsnaam wordt niet weergegeven.
      1. Typ in het [!UICONTROL File name] veld `.xlsx` en klik op **[!UICONTROL Open]**. Alle `.xlsx` dossiernamen tonen in de dossierlijst.

      1. Selecteer het `.xlsx` sjabloonbestand.
      1. Klik op **[!UICONTROL Open]**.


