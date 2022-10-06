---
description: Informatie over datasetcontrole en het toevoegen van nieuwe plaatsen voor gegevensopslag.
title: Gegevensruimte controleren
uuid: 0b7b95e7-b1bb-49cf-b465-fdbdc4ee214e
exl-id: eb34d5fe-73c6-461f-8bb0-85833d8f824f
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '464'
ht-degree: 0%

---

# Gegevensruimte controleren{#monitoring-dataset-data-space}

{{eol}}

Informatie over datasetcontrole en het toevoegen van nieuwe plaatsen voor gegevensopslag.

**Aanbevolen frequentie:** Elke 5-10 minuten

Standaard, [!DNL Insight Server] schrijft zijn dataset aan de [!DNL temp.db] bestand op hetzelfde station als het [!DNL Insight Server] programmabestanden op de gegevensverwerkingseenheid. De hoeveelheid gegevenssetgegevens per [!DNL Insight Server] de machine is beperkt tot:

* 500 (500) miljoen records van gegevensinvoer voor die gegevensset
* Vijfhonderd (500) GB opgeslagen gegevenssetgegevens
* Één (1) MB gegevens van datasets die per om het even welke één wortel-vlakke afmeting worden opgeslagen (bijvoorbeeld, 5.000 verslagen per Bezoeker bij een gemiddelde 200 bytes per verslag)

Als u [!DNL Insight Server] om de dataset op een verschillende aandrijving te handhaven, of als de hoeveelheid gegevens u verwacht te verzamelen het gebruik van veelvoudige aandrijving vereist, moet u het de configuratiedossier van de Dossiers van de Schijf bijwerken ( [!DNL Disk Files.cfg]) om aan te geven waar u wilt [!DNL Insight Server] om de [!DNL temp.db] bestand(en). De [!DNL Disk Files.cfg] het dossier maakt een lijst van de schijfdossiers (een vector van koorden) en specificeert de plaats van de datasetgegevens die door worden gebruikt [!DNL Insight Server] tijdens de opwerking en het bedrijf. Er is meestal één bestand per fysieke schijf.

>[!NOTE]
>
>De inhoud van de [!DNL Disk Files.cfg] bestand is mogelijk gewijzigd tijdens installeren [!DNL Insight Server]. Zie voor meer informatie [Het vormen van de Plaats van de Dataset (temp.db)](../../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/t-cfg-loc-dtst.md#task-f645eefecb154e679acbb480a07c1f0e).

**Nieuwe locaties toevoegen voor gegevensopslag van gegevenssets**

1. In [!DNL Insight]over de [!DNL Admin] > [!DNL Dataset and Profile] klikt u op de knop **[!UICONTROL Servers Manager]** om de werkruimte van Servers Manager te openen.
1. Klik met de rechtermuisknop op het pictogram van het dialoogvenster [!DNL Insight Server] u wilt vormen en klikken **[!UICONTROL Server Files]**.
1. In de [!DNL Server Files Manager], klikt u op **[!UICONTROL Components]** om de inhoud te bekijken. De [!DNL Disk Files.cfg] bestand bevindt zich in deze map.
1. Klik met de rechtermuisknop op het vinkje in het dialoogvenster *servernaam* kolom voor [!DNL Disk Files.cfg] en klik op **[!UICONTROL Make Local]**. Er verschijnt een vinkje in het dialoogvenster [!DNL Temp] kolom voor [!DNL Disk Files.cfg].
1. Klik met de rechtermuisknop op het nieuwe vinkje in het dialoogvenster [!DNL Temp] kolom en klik op **[!UICONTROL Open]** > **[!UICONTROL in Insight]**.
1. In de [!DNL Disk Files.cfg] venster, klikt u op **[!UICONTROL component]** om de inhoud te bekijken.

   ![Stapinfo](assets/cfg_diskfiles_examplevalues.png)

   >[!NOTE]
   >
   >De parameter Schijfbeschadiging detecteren is standaard ingesteld op true. Met de parameter Grootte schijfcache (MB) bepaalt u de hoeveelheid geheugen die [!DNL Insight Server] gebruikt om de snelheid van de schijftoegang te verhogen en is standaard ingesteld op 128. Neem contact op met Adobe voordat u een van deze parameters wijzigt.

1. De schijfbestanden wijzigen in het dialoogvenster [!DNL Insight Server] computer, rechtsklikken **[!UICONTROL Disk Files]** en klik op **[!UICONTROL Add new]** > **[!UICONTROL Disk File]**.

   Als u een schijfbestand wilt verwijderen, klikt u met de rechtermuisknop op het nummer van het schijfbestand en klikt u op **[!UICONTROL Remove]**.

1. Voer voor het nieuwe schijfbestand de map en naam in van het bestand dat moet worden gebruikt door [!DNL Insight Server] tijdens de opwerking en het bedrijf.

   ![Stapinfo](assets/cfg_diskfiles_exampleNewValues.png)

   >[!NOTE]
   >
   >De parameter Schijfbeschadiging detecteren is standaard ingesteld op true. Met de parameter Grootte schijfcache (MB) bepaalt u de hoeveelheid geheugen die [!DNL Insight Server] gebruikt om de snelheid van de schijftoegang te verhogen en is standaard ingesteld op 128. Neem contact op met Adobe voordat u een van deze parameters wijzigt.

1. Sla de wijzigingen op de server op door het volgende te doen:

   1. Klikken met rechtermuisknop **[!UICONTROL (modified)]** boven aan het venster en klik op **[!UICONTROL Save]**.

   1. In de [!DNL Server Files Manager]klikt u met de rechtermuisknop op het vinkje voor het bestand in het dialoogvenster [!DNL Temp] kolom en selecteer **[!UICONTROL Save to]** > *&lt;**[!UICONTROL server name]**>*.
