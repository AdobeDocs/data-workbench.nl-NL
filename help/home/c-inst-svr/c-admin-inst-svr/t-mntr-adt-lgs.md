---
description: De dossiers van het controlelogboek volgen alle pogingen verbindingen aan en losverbindingen van de Server van het Inzicht, elk waarvan het programma wordt geopend <yyyymmdd>-access.txt dossiers die door gebrek in de omslag van de Controle binnen de de installatiemap van de Server van het Inzicht worden gevestigd.
title: Controleregroepen
uuid: 38af9328-3f72-48a4-a0de-bf7477fedc25
exl-id: 220330da-e5dc-4ac0-9b70-42b08ccb3577
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '196'
ht-degree: 0%

---

# Controleregroepen{#monitoring-audit-logs}

{{eol}}

De dossiers van het controlelogboek volgen alle pogingen verbindingen aan en losverbindingen van de Server van het Inzicht, elk waarvan het programma wordt geopend `<YYYYMMDD>-access.txt` bestanden die standaard in de map Audit in de installatiemap van Insight Server staan.

**Aanbevolen frequentie:** Dagelijks of indien nodig voor probleemoplossing

De logboeken van de controle kunnen zeer nuttig zijn wanneer het oplossen van problemenkwesties verbinden met [!DNL Insight Server]. U kunt deze logboeken controleren met uw geautomatiseerde beheertool of door de [!DNL access.txt] rechtstreeks.

**Als u de bestanden access.txt via het dialoogvenster[!DNL Server Files Manager]**

1. In [!DNL Insight]over de [!DNL Admin] > [!DNL Dataset and Profile] klikt u op de knop **[!UICONTROL Servers Manager]** om de werkruimte van Servers Manager te openen.
1. Klik met de rechtermuisknop op het pictogram van een actieve [!DNL Insight Server] en klik op **[!UICONTROL Server Files]**.
1. In de [!DNL Server Files Manager], klikt u op **[!UICONTROL Audit]** om de inhoud te bekijken.
1. Klik met de rechtermuisknop op het vinkje in het dialoogvenster *servernaam* kolom naast het gewenste bestand en klik op **[!UICONTROL Make Local]**. Er wordt een vinkje weergegeven naast de bestandsnaam in het dialoogvenster [!DNL Temp] kolom.
1. Klik met de rechtermuisknop op het nieuwe vinkje in het dialoogvenster [!DNL Temp] kolom en klik op **[!UICONTROL Open]** > **[!UICONTROL in Notepad]**. Het controlelogboek verschijnt in een nieuw venster van de Blocnote van Microsoft Windows.

   ![Stapinfo](assets/cfg_accesscontrol_accessFile.png)
