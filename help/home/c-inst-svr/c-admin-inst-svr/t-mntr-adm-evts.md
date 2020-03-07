---
description: U zou uw dossiers van het gebeurtenislogboek regelmatig moeten controleren om de de gebeurtenisberichten van de Server van het Inzicht te volgen, die aan de <YYYYMMDD>-event.txt dossiers worden geregistreerd die door gebrek in de omslag van Gebeurtenissen binnen de de installatiefolder van de Server van het Inzicht worden gevestigd.
solution: Insight
title: Toezicht op administratieve gebeurtenissen
uuid: 92d71478-0857-4af8-909c-0cf800b081f4
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Toezicht op administratieve gebeurtenissen{#monitoring-administrative-events}

U zou uw dossiers van het gebeurtenislogboek aan de gebeurtenisberichten van de Server van het zicht regelmatig moeten controleren, die aan de `<YYYYMMDD>-event.txt` dossiers worden geregistreerd die door gebrek in de omslag van Gebeurtenissen binnen de de installatiefolder van de Server van het Inzicht worden gevestigd.

**Aanbevolen frequentie:** Om de 5-10 minuten

U kunt deze gebeurtenissen controleren gebruikend [!DNL Server Files Manager] binnen, uw geautomatiseerd beheershulpmiddel, de [!DNL Insight][!DNL *-event.txt] dossiers, of de Kijker van de Gebeurtenis van Vensters.

>[!NOTE]
>
>De administratieve Logboeken van de Gebeurtenis zijn volledig gescheiden van uw Logboek van de Gebeurtenissen van Vensters, maar bevat enkele zelfde gebeurtenissen. De administratieve Logboeken van de Gebeurtenis bevatten slechts informatie over [!DNL Insight Server] gebeurtenissen.

**Om gebeurtenissen.txt- dossiers door te bekijken[!DNL Server Files Manager]**

1. In [!DNL Insight], op het [!DNL Admin] > [!DNL Dataset and Profile] lusje, klik de **[!UICONTROL Servers Manager]** duimnagel om de werkruimte van de Manager van Servers te openen.
1. Klik het pictogram van actief met de rechtermuisknop aan [!DNL Insight Server] en klik **[!UICONTROL Server Files]**.
1. In [!DNL Server Files Manager], klik **[!UICONTROL Events]** om zijn inhoud te bekijken.
1. Klik het vinkje in de kolom van de *servernaam* naast het gewenste dossier met de rechtermuisknop aan en klik **[!UICONTROL Make Local]**. Een vinkje verschijnt naast het dossier - noem in de [!DNL Temp] kolom.
1. Klik het vinkje in de [!DNL Temp] kolom met de rechtermuisknop aan en klik **[!UICONTROL Open]** > **[!UICONTROL in Notepad]**. Het gebeurtenisdossier verschijnt in een nieuw venster van de Blocnote van Microsoft Windows.

   ![Stapgegevens](assets/vis_FileManager_eventfile.png)

   Het [!DNL Server.log] dossier in de [!DNL Trace] omslag binnen de [!DNL Insight Server] installatiefolder bevat meer gedetailleerde registrereninformatie.

**Om Gebeurtenissen door de Kijker van de Gebeurtenis van Vensters te bekijken**

* Klik op **[!UICONTROL Start]** > **[!UICONTROL Control Panel]** > **[!UICONTROL Administrative Tools]** > **[!UICONTROL Event Viewer]**.

**Om de Administratieve folder van het Logboek van Gebeurtenissen te veranderen**

Het administratieve dossier van de Logboeken van de Gebeurtenis, [!DNL Administrative Events Log.cfg], specificeert de folder waaraan het gebeurtenisregistreren output is.

1. In [!DNL Insight], op het [!DNL Admin] > [!DNL Dataset and Profile] lusje, klik de **[!UICONTROL Servers Manager]** duimnagel om de werkruimte van de Manager van Servers te openen.

1. Klik het pictogram van het pictogram met de rechtermuisknop aan [!DNL Insight Server] u wilt vormen en klikken **[!UICONTROL Server Files]**.

1. In [!DNL Server Files Manager], klik **[!UICONTROL Components]** om zijn inhoud te bekijken. Het [!DNL Administrative Event Logs.cfg] dossier wordt gevestigd binnen deze folder.

1. Klik het vinkje in de kolom van de *servernaam* voor met de rechtermuisknop aan [!DNL Administrative Event Logs.cfg] en klik **[!UICONTROL Make Local]**. Een vinkje verschijnt in de [!DNL Temp] kolom voor [!DNL Administrative Event Logs.cfg].

1. Klik het pas gecreëerde vinkje in de [!DNL Temp] kolom met de rechtermuisknop aan en klik **[!UICONTROL Open]** > **[!UICONTROL in Insight]**.

1. In het [!DNL Administrative Event Logs.cfg] venster, klik **[!UICONTROL component]** om zijn inhoud te bekijken. De standaardweg is de [!DNL Events] omslag binnen de [!DNL Insight Server] installatiefolder.

   ![](assets/cfg_adminevents_examplevalues.png)

1. In de parameter van de Weg, typ de naam van de folder waaraan u het registreren van de outputgebeurtenis gegevens wilt.
1. Sparen uw veranderingen in de server door het volgende te doen:

   1. Klik **[!UICONTROL (modified)]** bij de bovenkant van het venster met de rechtermuisknop aan en klik **[!UICONTROL Save]**.
   1. Klik in het [!DNL Server Files Manager]dialoogvenster met de rechtermuisknop op het vinkje voor het bestand in de [!DNL Temp] kolom en selecteer **[!UICONTROL Save to]** > **[!UICONTROL server name]**.

