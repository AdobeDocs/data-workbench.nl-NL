---
description: Informatie over datasetcontrole en het toevoegen van nieuwe plaatsen voor gegevensopslag.
title: Gegevensruimte controleren
uuid: 0b7b95e7-b1bb-49cf-b465-fdbdc4ee214e
exl-id: eb34d5fe-73c6-461f-8bb0-85833d8f824f
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '464'
ht-degree: 0%

---

# Gegevensgegevensruimte controleren{#monitoring-dataset-data-space}

Informatie over datasetcontrole en het toevoegen van nieuwe plaatsen voor gegevensopslag.

**Aanbevolen frequentie:** elke 5-10 minuten

[!DNL Insight Server] schrijft standaard zijn dataset naar het [!DNL temp.db] dossier op de zelfde aandrijving zoals [!DNL Insight Server] programmadossiers op de Eenheid van de Gegevensverwerking. De hoeveelheid gegevenssetgegevens per [!DNL Insight Server] machine is beperkt tot het volgende, welke eerst voorkomt:

* 500 (500) miljoen records van gegevensinvoer voor die gegevensset
* Vijfhonderd (500) GB opgeslagen gegevenssetgegevens
* Één (1) MB gegevens van datasets die per om het even welke één wortel-vlakke afmeting worden opgeslagen (bijvoorbeeld, 5.000 verslagen per Bezoeker bij een gemiddelde 200 bytes per verslag)

Als u [!DNL Insight Server] de dataset op een verschillende aandrijving wilt handhaven, of als de hoeveelheid gegevens u verwacht te verzamelen het gebruik van veelvoudige aandrijving vereist, moet u het de configuratiedossier van de Dossiers van de Schijf ( [!DNL Disk Files.cfg]) bijwerken om te specificeren waar u [!DNL Insight Server] om [!DNL temp.db] dossier(s) wilt schrijven. Het [!DNL Disk Files.cfg] dossier maakt een lijst van de schijfdossiers (een vector van koorden) en specificeert de plaats van de datasetgegevens die door [!DNL Insight Server] tijdens herverwerking en verrichting worden gebruikt. Er is meestal één bestand per fysieke schijf.

>[!NOTE]
>
>De inhoud van het [!DNL Disk Files.cfg]-bestand is mogelijk gewijzigd tijdens de installatie van [!DNL Insight Server]. Voor meer informatie, zie [Vormend de Plaats van de Dataset (temp.db)](../../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/t-cfg-loc-dtst.md#task-f645eefecb154e679acbb480a07c1f0e).

**Nieuwe locaties toevoegen voor gegevensopslag van gegevenssets**

1. Klik in [!DNL Insight] op het tabblad [!DNL Admin] > [!DNL Dataset and Profile] op de miniatuur **[!UICONTROL Servers Manager]** om de werkruimte Servers Manager te openen.
1. Klik met de rechtermuisknop op het pictogram van de [!DNL Insight Server] die u wilt configureren en klik op **[!UICONTROL Server Files]**.
1. Klik in [!DNL Server Files Manager] op **[!UICONTROL Components]** om de inhoud ervan weer te geven. Het [!DNL Disk Files.cfg]-bestand bevindt zich in deze map.
1. Klik met de rechtermuisknop op het vinkje in de kolom *servernaam* voor [!DNL Disk Files.cfg] en klik op **[!UICONTROL Make Local]**. In de kolom [!DNL Temp] wordt een vinkje weergegeven voor [!DNL Disk Files.cfg].
1. Klik met de rechtermuisknop op het nieuwe vinkje in de kolom [!DNL Temp] en klik op **[!UICONTROL Open]** > **[!UICONTROL in Insight]**.
1. Klik in het venster [!DNL Disk Files.cfg] op **[!UICONTROL component]** om de inhoud ervan weer te geven.

   ![Stapinfo](assets/cfg_diskfiles_examplevalues.png)

   >[!NOTE]
   >
   >De parameter Schijfbeschadiging detecteren is standaard ingesteld op true. De parameter van de Grootte van het Geheime voorgeheugen van de Schijf (MB) controleert de hoeveelheid geheugen die [!DNL Insight Server] gebruikt om de snelheid van de schijftoegang te verhogen en aan 128 door gebrek wordt geplaatst. Neem contact op met Adobe voordat u een van deze parameters wijzigt.

1. Als u de schijfbestanden op de [!DNL Insight Server]-computer wilt wijzigen, klikt u met de rechtermuisknop **[!UICONTROL Disk Files]** en klikt u **[!UICONTROL Add new]** > **[!UICONTROL Disk File]**.

   Als u een schijfbestand wilt verwijderen, klikt u met de rechtermuisknop op het nummer van het schijfbestand en klikt u op **[!UICONTROL Remove]**.

1. Voor het nieuwe schijfdossier, ga de folder en de naam van het dossier in dat door [!DNL Insight Server] tijdens herverwerking en verrichting moet worden gebruikt.

   ![Stapinfo](assets/cfg_diskfiles_exampleNewValues.png)

   >[!NOTE]
   >
   >De parameter Schijfbeschadiging detecteren is standaard ingesteld op true. De parameter van de Grootte van het Geheime voorgeheugen van de Schijf (MB) controleert de hoeveelheid geheugen die [!DNL Insight Server] gebruikt om de snelheid van de schijftoegang te verhogen en aan 128 door gebrek wordt geplaatst. Neem contact op met Adobe voordat u een van deze parameters wijzigt.

1. Sla de wijzigingen op de server op door het volgende te doen:

   1. Klik met de rechtermuisknop **[!UICONTROL (modified)]** boven in het venster en klik **[!UICONTROL Save]**.

   1. Klik in [!DNL Server Files Manager] met de rechtermuisknop op het vinkje voor het bestand in de kolom [!DNL Temp] en selecteer **[!UICONTROL Save to]** > *&lt;**[!UICONTROL server name]**>*.
