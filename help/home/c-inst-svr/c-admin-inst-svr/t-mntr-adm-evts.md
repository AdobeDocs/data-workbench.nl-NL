---
description: U zou uw dossiers van het gebeurtenislogboek regelmatig moeten controleren om de berichten van de het systeemgebeurtenis van de Server van het Inzicht te volgen, die aan worden geregistreerd <yyyymmdd>-event.txt bestanden die standaard in de map Events in de installatiemap van Insight Server staan.
title: Bewaking van beheergebeurtenissen (Insight Server)
uuid: 92d71478-0857-4af8-909c-0cf800b081f4
exl-id: e468a7d0-ed09-4367-88ce-b68964511e76
source-git-commit: 235b8816c7397ac1ab71df650a1d4c2d681b3b2d
workflow-type: tm+mt
source-wordcount: '397'
ht-degree: 0%

---

# Bewaking van administratieve gebeurtenissen{#monitoring-administrative-events}

U zou uw dossiers van het gebeurtenislogboek regelmatig moeten controleren om de berichten van de het systeemgebeurtenis van de Server van het Inzicht te volgen, die aan worden geregistreerd `<YYYYMMDD>-event.txt` bestanden die standaard in de map Events in de installatiemap van Insight Server staan.

**Aanbevolen frequentie:** Elke 5-10 minuten

U kunt deze gebeurtenissen controleren met de [!DNL Server Files Manager] in [!DNL Insight], uw geautomatiseerde beheertool, de [!DNL *-event.txt] of de Windows Event Viewer.

>[!NOTE]
>
>De administratieve Logboeken van de Gebeurtenis zijn volledig gescheiden van uw Logboek van de Gebeurtenissen van Vensters, maar bevat enkele zelfde gebeurtenissen. De beheergebeurtenislogboeken bevatten alleen informatie over [!DNL Insight Server] gebeurtenissen.

**U kunt de bestanden events.txt via het dialoogvenster[!DNL Server Files Manager]**

1. In [!DNL Insight]over de [!DNL Admin] > [!DNL Dataset and Profile] klikt u op de knop **[!UICONTROL Servers Manager]** om de werkruimte van Servers Manager te openen.
1. Klik met de rechtermuisknop op het pictogram van een actieve [!DNL Insight Server] en klik op **[!UICONTROL Server Files]**.
1. In de [!DNL Server Files Manager], klikt u op **[!UICONTROL Events]** om de inhoud te bekijken.
1. Klik met de rechtermuisknop op het vinkje in het dialoogvenster *servernaam* kolom naast het gewenste bestand en klik op **[!UICONTROL Make Local]**. Er wordt een vinkje weergegeven naast de bestandsnaam in het dialoogvenster [!DNL Temp] kolom.
1. Klik met de rechtermuisknop op het vinkje in het dialoogvenster [!DNL Temp] kolom en klik op **[!UICONTROL Open]** > **[!UICONTROL in Notepad]**. Het gebeurtenisbestand wordt weergegeven in een nieuw Microsoft Windows-laptopvenster.

   ![Stapinfo](assets/vis_FileManager_eventfile.png)

   De [!DNL Server.log] in het [!DNL Trace] in de [!DNL Insight Server] De installatiemap bevat meer gedetailleerde logboekgegevens.

**Gebeurtenissen weergeven via de Windows Event Viewer**

* Klik op **[!UICONTROL Start]** > **[!UICONTROL Control Panel]** > **[!UICONTROL Administrative Tools]** > **[!UICONTROL Event Viewer]**.

**De map Administration Events Log wijzigen**

Het configuratiebestand van het beheergebeurtenislogboek, [!DNL Administrative Events Log.cfg], geeft de map aan waarnaar gebeurtenislogboekregistratie wordt uitgevoerd.

1. In [!DNL Insight]over de [!DNL Admin] > [!DNL Dataset and Profile] klikt u op de knop **[!UICONTROL Servers Manager]** om de werkruimte van Servers Manager te openen.

1. Klik met de rechtermuisknop op het pictogram van het dialoogvenster [!DNL Insight Server] u wilt vormen en klikken **[!UICONTROL Server Files]**.

1. In de [!DNL Server Files Manager], klikt u op **[!UICONTROL Components]** om de inhoud te bekijken. De [!DNL Administrative Event Logs.cfg] bestand bevindt zich in deze map.

1. Klik met de rechtermuisknop op het vinkje in het dialoogvenster *servernaam* kolom voor [!DNL Administrative Event Logs.cfg] en klik op **[!UICONTROL Make Local]**. Er verschijnt een vinkje in het dialoogvenster [!DNL Temp] kolom voor [!DNL Administrative Event Logs.cfg].

1. Klik met de rechtermuisknop op het nieuwe vinkje in het dialoogvenster [!DNL Temp] kolom en klik op **[!UICONTROL Open]** > **[!UICONTROL in Insight]**.

1. In de [!DNL Administrative Event Logs.cfg] venster, klikt u op **[!UICONTROL component]** om de inhoud te bekijken. Het standaardpad is [!DNL Events] in de [!DNL Insight Server] installatiemap.

   ![](assets/cfg_adminevents_examplevalues.png)

1. Typ in de parameter Path de naam van de map waarnaar u de logboekgegevens van gebeurtenissen wilt uitvoeren.
1. Sla de wijzigingen op de server op door het volgende te doen:

   1. Klikken met rechtermuisknop **[!UICONTROL (modified)]** boven aan het venster en klik op **[!UICONTROL Save]**.
   1. In de [!DNL Server Files Manager]klikt u met de rechtermuisknop op het vinkje voor het bestand in het dialoogvenster [!DNL Temp] kolom en selecteer **[!UICONTROL Save to]** > **[!UICONTROL server name]**.
