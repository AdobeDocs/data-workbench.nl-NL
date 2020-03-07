---
description: Informatie over datasetcontrole en het toevoegen van nieuwe plaatsen voor gegevensopslag van de dataset.
solution: Insight
title: Gegevensverzameling bewaken Gegevensruimte
uuid: 0b7b95e7-b1bb-49cf-b465-fdbdc4ee214e
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Gegevensverzameling bewaken Gegevensruimte{#monitoring-dataset-data-space}

Informatie over datasetcontrole en het toevoegen van nieuwe plaatsen voor gegevensopslag van de dataset.

**Aanbevolen frequentie:** Om de 5-10 minuten

Door gebrek, [!DNL Insight Server] schrijft zijn dataset aan het [!DNL temp.db] dossier op de zelfde aandrijving zoals de [!DNL Insight Server] programmadossiers op de Eenheid van de Gegevensverwerking. De hoeveelheid gegevens van de dataset per [!DNL Insight Server] machine is beperkt tot het volgende, welke eerst voorkomt:

* 500 (500) miljoen records van gegevensinvoer voor die dataset
* Vijfhonderd (500) GB opgeslagen datasetgegevens
* Één (1) MB van datasetgegevens die per om het even welke wortel-vlakke afmeting worden opgeslagen (bijvoorbeeld, 5.000 verslagen per Bezoeker bij een gemiddelde 200 bytes per verslag)

Als u de dataset op een verschillende schijf wilt onderhouden of als de hoeveelheid gegevens die u wilt verzamelen het gebruik van meerdere stations vereist, moet u het configuratiebestand Schijfbestanden ( [!DNL Insight Server] ) bijwerken om te specificeren waar u de [!DNL Disk Files.cfg]bestanden wilt [!DNL Insight Server] [!DNL temp.db] schrijven. Het [!DNL Disk Files.cfg] dossier maakt een lijst van de schijfdossiers (een vector van koorden) en specificeert de plaats van de datasetgegevens die door [!DNL Insight Server] tijdens opwerking en verrichting worden gebruikt. Er is gewoonlijk één dossier per fysieke aandrijving.

>[!NOTE]
>
>De inhoud van het [!DNL Disk Files.cfg] bestand kan tijdens het installeren zijn gewijzigd [!DNL Insight Server]. Voor meer informatie, zie het [Vormen van de Plaats van de Dataset (temp.db)](../../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/t-cfg-loc-dtst.md#task-f645eefecb154e679acbb480a07c1f0e).

**Om nieuwe plaatsen voor de opslag van gegevensreeksen toe te voegen**

1. In [!DNL Insight], op het [!DNL Admin] > [!DNL Dataset and Profile] lusje, klik de **[!UICONTROL Servers Manager]** duimnagel om de werkruimte van de Manager van Servers te openen.
1. Klik het pictogram van het pictogram met de rechtermuisknop aan [!DNL Insight Server] u wilt vormen en klikken **[!UICONTROL Server Files]**.
1. In [!DNL Server Files Manager], klik **[!UICONTROL Components]** om zijn inhoud te bekijken. Het [!DNL Disk Files.cfg] dossier wordt gevestigd binnen deze folder.
1. Klik het vinkje in de kolom van de *servernaam* voor met de rechtermuisknop aan [!DNL Disk Files.cfg] en klik **[!UICONTROL Make Local]**. Een vinkje verschijnt in de [!DNL Temp] kolom voor [!DNL Disk Files.cfg].
1. Klik het pas gecreëerde vinkje in de [!DNL Temp] kolom met de rechtermuisknop aan en klik **[!UICONTROL Open]** > **[!UICONTROL in Insight]**.
1. In het [!DNL Disk Files.cfg] venster, klik **[!UICONTROL component]** om zijn inhoud te bekijken.

   ![Stapgegevens](assets/cfg_diskfiles_examplevalues.png)

   >[!NOTE]
   >
   >De parameter van de Corruptie van de Schijf detecteert wordt geplaatst aan waar door gebrek. De parameter van de Grootte van het Geheime voorgeheugen van de Schijf (MB) controleert de hoeveelheid geheugen die [!DNL Insight Server] gebruikt om de snelheid van de schijftoegang te verhogen en aan 128 door gebrek geplaatst. Tevreden om Adobe te contacteren alvorens één van beiden van deze parameters te veranderen.

1. Als u de schijfbestanden op het [!DNL Insight Server] systeem wilt wijzigen, klikt u met de rechtermuisknop **[!UICONTROL Disk Files]** en klikt u op **[!UICONTROL Add new]** > **[!UICONTROL Disk File]**.

   Om een schijfdossier te schrappen, klik het aantal van het schijfdossier met de rechtermuisknop aan en klik **[!UICONTROL Remove]**.

1. Voor het nieuwe schijfdossier, ga de folder en de naam van het dossier in dat door tijdens [!DNL Insight Server] opwerking en verrichting moet worden gebruikt.

   ![Stapgegevens](assets/cfg_diskfiles_exampleNewValues.png)

   >[!NOTE]
   >
   >De parameter van de Corruptie van de Schijf detecteert wordt geplaatst aan waar door gebrek. De parameter van de Grootte van het Geheime voorgeheugen van de Schijf (MB) controleert de hoeveelheid geheugen die [!DNL Insight Server] gebruikt om de snelheid van de schijftoegang te verhogen en aan 128 door gebrek geplaatst. Tevreden om Adobe te contacteren alvorens één van beiden van deze parameters te veranderen.

1. Sparen uw veranderingen in de server door het volgende te doen:

   1. Klik **[!UICONTROL (modified)]** bij de bovenkant van het venster met de rechtermuisknop aan en klik **[!UICONTROL Save]**.

   1. Klik in het [!DNL Server Files Manager]dialoogvenster met de rechtermuisknop op het vinkje voor het bestand in de [!DNL Temp] kolom en selecteer **[!UICONTROL Save to]** > *&lt;**[!UICONTROL server name]**>*.

