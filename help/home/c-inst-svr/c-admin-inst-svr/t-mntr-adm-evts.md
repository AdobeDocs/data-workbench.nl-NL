---
description: U zou regelmatig uw dossiers van het gebeurtenislogboek moeten controleren om de berichten van de het systeemgebeurtenis van de Server van het Inzicht te volgen, die aan de <YYYMMDD>-event.txt- dossiers worden geregistreerd die door gebrek in de omslag van Gebeurtenissen binnen de de installatiemap van de Server van het Inzicht worden gevestigd.
solution: Analytics
title: Bewaking van administratieve gebeurtenissen
uuid: 92d71478-0857-4af8-909c-0cf800b081f4
translation-type: tm+mt
source-git-commit: 34cdcfc83ae6bb620706db37228e200cff43ab2c
workflow-type: tm+mt
source-wordcount: '395'
ht-degree: 0%

---


# Bewaking van administratieve gebeurtenissen{#monitoring-administrative-events}

U zou regelmatig uw dossiers van het gebeurtenislogboek moeten controleren om de berichten van de het systeemgebeurtenis van de Server van het Inzicht te volgen, die aan de `<YYYYMMDD>-event.txt` dossiers worden geregistreerd die door gebrek in de omslag van Gebeurtenissen binnen de de installatiemap van de Server van het Inzicht worden gevestigd.

**Aanbevolen frequentie:** Elke 5-10 minuten

U kunt deze gebeurtenissen controleren met de [!DNL Server Files Manager] insteekmodule, het geautomatiseerde beheergereedschap, de [!DNL Insight][!DNL *-event.txt] bestanden of de Windows Event Viewer.

>[!NOTE]
>
>De administratieve Logboeken van de Gebeurtenis zijn volledig gescheiden van uw Logboek van de Gebeurtenissen van Vensters, maar bevat enkele zelfde gebeurtenissen. De beheergebeurtenislogboeken bevatten alleen informatie over [!DNL Insight Server] gebeurtenissen.

**U kunt de bestanden events.txt via het dialoogvenster[!DNL Server Files Manager]**

1. Klik in [!DNL Insight]het tabblad [!DNL Admin] > op de [!DNL Dataset and Profile] **[!UICONTROL Servers Manager]** miniatuur om de werkruimte van Servers Manager te openen.
1. Klik met de rechtermuisknop op het pictogram van een actieve toepassing [!DNL Insight Server] en klik op **[!UICONTROL Server Files]**.
1. Klik in de [!DNL Server Files Manager]werkruimte **[!UICONTROL Events]** om de inhoud weer te geven.
1. Klik met de rechtermuisknop op het vinkje in de kolom *Servernaam* naast het gewenste bestand en klik op **[!UICONTROL Make Local]**. Naast de bestandsnaam in de [!DNL Temp] kolom staat een vinkje.
1. Klik met de rechtermuisknop op het vinkje in de [!DNL Temp] kolom en klik op **[!UICONTROL Open]** > **[!UICONTROL in Notepad]**. Het gebeurtenisdossier verschijnt in een nieuw venster van de Blocnote van Microsoft Windows.

   ![Stapinfo](assets/vis_FileManager_eventfile.png)

   Het [!DNL Server.log] bestand in de [!DNL Trace] map in de [!DNL Insight Server] installatiemap bevat meer gedetailleerde logboekgegevens.

**Gebeurtenissen weergeven via de Windows Event Viewer**

* Klik op **[!UICONTROL Start]** > **[!UICONTROL Control Panel]** > **[!UICONTROL Administrative Tools]** > **[!UICONTROL Event Viewer]**.

**De map Administration Events Log wijzigen**

Het configuratiebestand Systeembeheer gebeurtenissenlogs geeft [!DNL Administrative Events Log.cfg]de map aan waarnaar gebeurtenislogbestanden worden uitgevoerd.

1. Klik in [!DNL Insight]het tabblad [!DNL Admin] > op de [!DNL Dataset and Profile] **[!UICONTROL Servers Manager]** miniatuur om de werkruimte van Servers Manager te openen.

1. Klik met de rechtermuisknop op het pictogram van het [!DNL Insight Server] object dat u wilt configureren en klik op **[!UICONTROL Server Files]**.

1. Klik in de [!DNL Server Files Manager]werkruimte **[!UICONTROL Components]** om de inhoud weer te geven. Het [!DNL Administrative Event Logs.cfg] bestand bevindt zich in deze map.

1. Klik met de rechtermuisknop op het vinkje in de kolom *Servernaam* voor [!DNL Administrative Event Logs.cfg] en klik op **[!UICONTROL Make Local]**. In de [!DNL Temp] kolom voor [!DNL Administrative Event Logs.cfg].

1. Klik met de rechtermuisknop op het nieuwe vinkje in de [!DNL Temp] kolom en klik op **[!UICONTROL Open]** > **[!UICONTROL in Insight]**.

1. Klik in het [!DNL Administrative Event Logs.cfg] venster **[!UICONTROL component]** om de inhoud weer te geven. Het standaardpad is de [!DNL Events] map in de [!DNL Insight Server] installatiemap.

   ![](assets/cfg_adminevents_examplevalues.png)

1. Typ in de parameter Path de naam van de map waarnaar u de logboekgegevens van gebeurtenissen wilt uitvoeren.
1. Sla de wijzigingen op de server op door het volgende te doen:

   1. Klik met de rechtermuisknop **[!UICONTROL (modified)]** boven in het venster en klik op **[!UICONTROL Save]**.
   1. Klik in het [!DNL Server Files Manager]dialoogvenster met de rechtermuisknop op het vinkje voor het bestand in de [!DNL Temp] kolom en selecteer **[!UICONTROL Save to]** > **[!UICONTROL server name]**.

