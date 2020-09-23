---
description: De dossiers van het controlelogboek volgen alle pogingen om verbindingen aan en los te maken van de Server van het Inzicht, elk van wie het programma wordt geopend <YYYMMDD>-access.txt dossiers die door gebrek in de omslag van de Controle binnen de de installatiemap van de Server van het Inzicht worden gevestigd.
solution: Analytics
title: Controleregroepen
uuid: 38af9328-3f72-48a4-a0de-bf7477fedc25
translation-type: tm+mt
source-git-commit: 34cdcfc83ae6bb620706db37228e200cff43ab2c
workflow-type: tm+mt
source-wordcount: '196'
ht-degree: 0%

---


# Controleregroepen{#monitoring-audit-logs}

De dossiers van het logboek van de controle volgen alle pogingen verbindingen aan en losverbindingen van de Server van het Inzicht, elk waarvan het programma wordt geopend de `<YYYYMMDD>-access.txt` dossiers die door gebrek in de omslag van de Controle binnen de de installatiemap van de Server van het Inzicht worden gevestigd.

**Aanbevolen frequentie:** Dagelijks of indien nodig voor probleemoplossing

De logboeken van de controle kunnen zeer nuttig zijn wanneer het oplossen van problemenkwesties die met verbinden [!DNL Insight Server]. U kunt deze logboeken controleren met uw geautomatiseerde beheertool of door de [!DNL access.txt] bestanden rechtstreeks weer te geven.

**Als u de bestanden access.txt via het dialoogvenster[!DNL Server Files Manager]**

1. Klik in [!DNL Insight]het tabblad [!DNL Admin] > op de [!DNL Dataset and Profile] **[!UICONTROL Servers Manager]** miniatuur om de werkruimte van Servers Manager te openen.
1. Klik met de rechtermuisknop op het pictogram van een actieve toepassing [!DNL Insight Server] en klik op **[!UICONTROL Server Files]**.
1. Klik in de [!DNL Server Files Manager]werkruimte **[!UICONTROL Audit]** om de inhoud weer te geven.
1. Klik met de rechtermuisknop op het vinkje in de kolom *Servernaam* naast het gewenste bestand en klik op **[!UICONTROL Make Local]**. Naast de bestandsnaam in de [!DNL Temp] kolom staat een vinkje.
1. Klik met de rechtermuisknop op het nieuwe vinkje in de [!DNL Temp] kolom en klik op **[!UICONTROL Open]** > **[!UICONTROL in Notepad]**. Het controlelogboek verschijnt in een nieuw venster van de Blocnote van Microsoft Windows.

   ![Stapinfo](assets/cfg_accesscontrol_accessFile.png)

