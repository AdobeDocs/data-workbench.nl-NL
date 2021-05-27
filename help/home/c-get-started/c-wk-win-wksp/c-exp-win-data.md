---
description: U kunt de gegevens in bepaalde vensters exporteren naar een Excel-bestand (.xls of .xlsx) of naar een bestand met door tabs gescheiden waarden (.tsv).
title: Venstergegevens exporteren
uuid: 71a93f35-1096-41ae-8808-e5b94813a52c
exl-id: ab931453-d366-4d3a-990e-7a368328da2d
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '376'
ht-degree: 0%

---

# Venstergegevens exporteren{#export-window-data}

U kunt de gegevens in bepaalde vensters exporteren naar een Excel-bestand (.xls of .xlsx) of naar een bestand met door tabs gescheiden waarden (.tsv).

Gegevens worden niet geëxporteerd uit grafieken, padbrowsers, procesafbeeldingen, verstrooiingspunten en globes.

## Venstergegevens exporteren naar Microsoft Excel {#section-b660adf7f4f64a2b9be7287c591b67b0}

Als u afzonderlijke venstergegevens wilt exporteren naar Microsoft Excel, moet aan de volgende vereisten worden voldaan:

* Microsoft Excel moet op dezelfde computer zijn geïnstalleerd als Data Workbench.
* De gebruikersrekening waaronder het proces van de Data Workbench loopt moet toestemming hebben om tot Microsoft Excel toegang te hebben.
* Wanneer u gegevens als dossiers van Excel uitvoert, opent u een nieuw geval van Excel.
* Hoewel de Data Workbench meer dan 256 kolommen en 65.536 rijen van gegevens steunt, de versies van Microsoft Excel voorafgaand aan 8.0 niet.

Als aan deze vereisten wordt voldaan, begint de Data Workbench automatisch Microsoft Excel en voert de gegevens naar een nieuw werkboek van Excel uit wanneer u **[!UICONTROL Export To Excel]** menuoptie selecteert.

**Venstergegevens exporteren naar een .xls- of .xlsx-bestand**

Klik met de rechtermuisknop op de bovenrand van het venster en klik op **[!UICONTROL Export]** > **[!UICONTROL Export to Excel]**.

![](assets/mnu_window_TitleBar_Export.png)

Excel opent een nieuw werkboek dat de uitgevoerde gegevens bevat. Tenzij u een titel van de Douane (zoals die in de volgende sectie wordt beschreven) hebt verstrekt, wordt dit werkboek genoemd gebruikend [!DNL Export title] (de Lijst van de Dag in het bovenstaande voorbeeld).

## Aangepaste titels toepassen {#section-2a6559df812a470685e43923b7b9024e}

Als u een aangepaste titel voor een venster opgeeft (met het veld [!DNL Custom title] in het menu [!DNL Export]), wordt in het werkblad waarnaar de Data Workbench de gegevens exporteert, de naam van deze aangepaste titel gebruikt in plaats van de titel in het veld [!DNL Export title] (Tabel op dag in het bovenstaande voorbeeld).

**Een aangepaste titel toepassen op een visualisatie**

1. Klik met de rechtermuisknop op de bovenrand van het venster en klik in het veld **[!UICONTROL Custom title]**.
1. u

![](assets/mnu_window_TitleBar_Export.png)

Wanneer u de visualisatie naar Excel exporteert, wordt het werkblad met de gegevens voor dit venster benoemd met de titel die u hebt opgegeven in plaats van de titel in het veld [!DNL Export title].

## Venstergegevens exporteren naar een TSV-bestand {#section-93c6b24f7338430aaf5a63b99b9489e8}

**Een venster exporteren naar een .tsv-bestand**

Klik met de rechtermuisknop op de bovenrand van het venster en klik op **[!UICONTROL Export]** > **[!UICONTROL Export TSV]**.

1. Het dialoogvenster [!DNL Save Window] wordt weergegeven.
1. Navigeer naar de map waarin u het bestand wilt opslaan. Wijzig indien nodig de naam van het bestand en klik op **[!UICONTROL Save]**.
