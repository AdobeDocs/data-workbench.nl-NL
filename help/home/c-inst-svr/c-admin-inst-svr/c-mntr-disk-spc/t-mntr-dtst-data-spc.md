---
description: Informatie over datasetcontrole en het toevoegen van nieuwe plaatsen voor gegevensopslag.
solution: Analytics
title: Gegevensruimte controleren
uuid: 0b7b95e7-b1bb-49cf-b465-fdbdc4ee214e
translation-type: tm+mt
source-git-commit: 34cdcfc83ae6bb620706db37228e200cff43ab2c
workflow-type: tm+mt
source-wordcount: '464'
ht-degree: 0%

---


# Gegevensruimte controleren{#monitoring-dataset-data-space}

Informatie over datasetcontrole en het toevoegen van nieuwe plaatsen voor gegevensopslag.

**Aanbevolen frequentie:** Elke 5-10 minuten

Door gebrek, [!DNL Insight Server] schrijft zijn dataset aan het [!DNL temp.db] dossier op de zelfde aandrijving zoals de [!DNL Insight Server] programmadossiers op de Eenheid van de Gegevensverwerking. De hoeveelheid gegevenssetgegevens per [!DNL Insight Server] machine is beperkt tot het volgende, afhankelijk van wat zich het eerst voordoet:

* 500 (500) miljoen records van gegevensinvoer voor die gegevensset
* Vijfhonderd (500) GB opgeslagen gegevenssetgegevens
* Één (1) MB gegevens van datasets die per om het even welke één wortel-vlakke afmeting worden opgeslagen (bijvoorbeeld, 5.000 verslagen per Bezoeker bij een gemiddelde 200 bytes per verslag)

Als u de dataset op een verschillende aandrijving wilt handhaven, of als de hoeveelheid gegevens u verwacht te verzamelen het gebruik van veelvoudige aandrijving vereist, moet u het de configuratiedossier van de Dossiers van de Schijf ( [!DNL Insight Server] ) bijwerken om te specificeren waar u [!DNL Disk Files.cfg]het [!DNL Insight Server] [!DNL temp.db] (a)dossier(en) wilt schrijven. Het [!DNL Disk Files.cfg] bestand bevat een lijst met de schijfbestanden (een vector met tekenreeksen) en geeft de locatie op van de gegevenssetgegevens die worden gebruikt door [!DNL Insight Server] tijdens het opnieuw verwerken en bewerken. Er is meestal één bestand per fysieke schijf.

>[!NOTE]
>
>De inhoud van het [!DNL Disk Files.cfg] bestand kan tijdens de installatie zijn gewijzigd [!DNL Insight Server]. Voor meer informatie, zie het [Vormen van de Plaats van de Dataset (temp.db)](../../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/t-cfg-loc-dtst.md#task-f645eefecb154e679acbb480a07c1f0e).

**Nieuwe locaties toevoegen voor gegevensopslag van gegevenssets**

1. Klik in [!DNL Insight]het tabblad [!DNL Admin] > op de [!DNL Dataset and Profile] **[!UICONTROL Servers Manager]** miniatuur om de werkruimte van Servers Manager te openen.
1. Klik met de rechtermuisknop op het pictogram van het [!DNL Insight Server] object dat u wilt configureren en klik op **[!UICONTROL Server Files]**.
1. Klik in de [!DNL Server Files Manager]werkruimte **[!UICONTROL Components]** om de inhoud weer te geven. Het [!DNL Disk Files.cfg] bestand bevindt zich in deze map.
1. Klik met de rechtermuisknop op het vinkje in de kolom *Servernaam* voor [!DNL Disk Files.cfg] en klik op **[!UICONTROL Make Local]**. In de [!DNL Temp] kolom voor [!DNL Disk Files.cfg].
1. Klik met de rechtermuisknop op het nieuwe vinkje in de [!DNL Temp] kolom en klik op **[!UICONTROL Open]** > **[!UICONTROL in Insight]**.
1. Klik in het [!DNL Disk Files.cfg] venster **[!UICONTROL component]** om de inhoud weer te geven.

   ![Stapinfo](assets/cfg_diskfiles_examplevalues.png)

   >[!NOTE]
   >
   >De parameter Schijfbeschadiging detecteren is standaard ingesteld op true. De parameter van de Grootte van het Geheime voorgeheugen van de Schijf (MB) controleert de hoeveelheid geheugen die [!DNL Insight Server] gebruikt om de snelheid van de schijftoegang te verhogen en aan 128 door gebrek wordt geplaatst. Neem contact op met Adobe voordat u een van deze parameters wijzigt.

1. Als u de schijfbestanden op de [!DNL Insight Server] computer wilt wijzigen, klikt u met de rechtermuisknop **[!UICONTROL Disk Files]** en klikt u op **[!UICONTROL Add new]** > **[!UICONTROL Disk File]**.

   Als u een schijfbestand wilt verwijderen, klikt u met de rechtermuisknop op het nummer van het schijfbestand en klikt u op **[!UICONTROL Remove]**.

1. Voer voor het nieuwe schijfbestand de map en de naam in van het bestand dat tijdens de [!DNL Insight Server] verwerking en bewerking moet worden gebruikt.

   ![Stapinfo](assets/cfg_diskfiles_exampleNewValues.png)

   >[!NOTE]
   >
   >De parameter Schijfbeschadiging detecteren is standaard ingesteld op true. De parameter van de Grootte van het Geheime voorgeheugen van de Schijf (MB) controleert de hoeveelheid geheugen die [!DNL Insight Server] gebruikt om de snelheid van de schijftoegang te verhogen en aan 128 door gebrek wordt geplaatst. Neem contact op met Adobe voordat u een van deze parameters wijzigt.

1. Sla de wijzigingen op de server op door het volgende te doen:

   1. Klik met de rechtermuisknop **[!UICONTROL (modified)]** boven in het venster en klik op **[!UICONTROL Save]**.

   1. Klik in het [!DNL Server Files Manager]dialoogvenster met de rechtermuisknop op het vinkje voor het bestand in de [!DNL Temp] kolom en selecteer **[!UICONTROL Save to]** > *&lt;**[!UICONTROL server name]**>*.

