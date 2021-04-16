---
description: U zou regelmatig uw dossiers van het gebeurtenislogboek moeten controleren om de berichten van de het systeemgebeurtenis van de Server van het Inzicht te volgen, die aan de <YYYMMDD>-event.txt- dossiers worden geregistreerd die door gebrek in de omslag van Gebeurtenissen binnen de de installatiemap van de Server van het Inzicht worden gevestigd.
title: Bewaking van administratieve gebeurtenissen
uuid: 92d71478-0857-4af8-909c-0cf800b081f4
exl-id: e468a7d0-ed09-4367-88ce-b68964511e76
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '395'
ht-degree: 0%

---

# Bewaking van beheergebeurtenissen{#monitoring-administrative-events}

U zou uw dossiers van het gebeurtenislogboek regelmatig moeten controleren om de berichten van de het systeemgebeurtenis van de Server van het Inzicht te volgen, die aan de `<YYYYMMDD>-event.txt` dossiers worden geregistreerd die door gebrek in de omslag van Gebeurtenissen binnen de de installatiemap van de Server van het Inzicht worden gevestigd.

**Aanbevolen frequentie:** elke 5-10 minuten

U kunt deze gebeurtenissen controleren met de [!DNL Server Files Manager] in [!DNL Insight], uw geautomatiseerde beheertool, de [!DNL *-event.txt]-bestanden of de Windows Event Viewer.

>[!NOTE]
>
>De administratieve Logboeken van de Gebeurtenis zijn volledig gescheiden van uw Logboek van de Gebeurtenissen van Vensters, maar bevat enkele zelfde gebeurtenissen. De beheergebeurtenislogboeken bevatten alleen informatie over gebeurtenissen [!DNL Insight Server].

**U kunt de bestanden events.txt via het dialoogvenster[!DNL Server Files Manager]**

1. Klik in [!DNL Insight] op het tabblad [!DNL Admin] > [!DNL Dataset and Profile] op de miniatuur **[!UICONTROL Servers Manager]** om de werkruimte Servers Manager te openen.
1. Klik met de rechtermuisknop op het pictogram van een actieve [!DNL Insight Server] en klik op **[!UICONTROL Server Files]**.
1. Klik in [!DNL Server Files Manager] op **[!UICONTROL Events]** om de inhoud ervan weer te geven.
1. Klik met de rechtermuisknop op het vinkje in de kolom *servernaam* naast het gewenste bestand en klik op **[!UICONTROL Make Local]**. Er wordt een vinkje weergegeven naast de bestandsnaam in de kolom [!DNL Temp].
1. Klik met de rechtermuisknop op het vinkje in de kolom [!DNL Temp] en klik op **[!UICONTROL Open]** > **[!UICONTROL in Notepad]**. Het gebeurtenisdossier verschijnt in een nieuw venster van de Blocnote van Microsoft Windows.

   ![Stapinfo](assets/vis_FileManager_eventfile.png)

   Het [!DNL Server.log]-bestand in de map [!DNL Trace] in de installatiemap [!DNL Insight Server] bevat meer gedetailleerde logboekgegevens.

**Gebeurtenissen weergeven via de Windows Event Viewer**

* Klik op **[!UICONTROL Start]** > **[!UICONTROL Control Panel]** > **[!UICONTROL Administrative Tools]** > **[!UICONTROL Event Viewer]**.

**De map Administration Events Log wijzigen**

Het configuratiebestand [!DNL Administrative Events Log.cfg] van de beheergebeurtenis geeft de map aan waarnaar gebeurtenislogbestanden worden uitgevoerd.

1. Klik in [!DNL Insight] op het tabblad [!DNL Admin] > [!DNL Dataset and Profile] op de miniatuur **[!UICONTROL Servers Manager]** om de werkruimte Servers Manager te openen.

1. Klik met de rechtermuisknop op het pictogram van de [!DNL Insight Server] die u wilt configureren en klik op **[!UICONTROL Server Files]**.

1. Klik in [!DNL Server Files Manager] op **[!UICONTROL Components]** om de inhoud ervan weer te geven. Het [!DNL Administrative Event Logs.cfg]-bestand bevindt zich in deze map.

1. Klik met de rechtermuisknop op het vinkje in de kolom *servernaam* voor [!DNL Administrative Event Logs.cfg] en klik op **[!UICONTROL Make Local]**. In de kolom [!DNL Temp] wordt een vinkje weergegeven voor [!DNL Administrative Event Logs.cfg].

1. Klik met de rechtermuisknop op het nieuwe vinkje in de kolom [!DNL Temp] en klik op **[!UICONTROL Open]** > **[!UICONTROL in Insight]**.

1. Klik in het venster [!DNL Administrative Event Logs.cfg] op **[!UICONTROL component]** om de inhoud ervan weer te geven. Het standaardpad is de map [!DNL Events] in de installatiemap [!DNL Insight Server].

   ![](assets/cfg_adminevents_examplevalues.png)

1. Typ in de parameter Path de naam van de map waarnaar u de logboekgegevens van gebeurtenissen wilt uitvoeren.
1. Sla de wijzigingen op de server op door het volgende te doen:

   1. Klik met de rechtermuisknop **[!UICONTROL (modified)]** boven in het venster en klik **[!UICONTROL Save]**.
   1. Klik in [!DNL Server Files Manager] met de rechtermuisknop op het vinkje voor het bestand in de kolom [!DNL Temp] en selecteer **[!UICONTROL Save to]** > **[!UICONTROL server name]**.
