---
description: De dossiers van het controlelogboek volgen alle pogingen om verbindingen aan en los te maken van de Server van het Inzicht, elk van wie het programma wordt geopend <YYYMMDD>-access.txt dossiers die door gebrek in de omslag van de Controle binnen de de installatiemap van de Server van het Inzicht worden gevestigd.
title: Controleregroepen
uuid: 38af9328-3f72-48a4-a0de-bf7477fedc25
exl-id: 220330da-e5dc-4ac0-9b70-42b08ccb3577
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '196'
ht-degree: 0%

---

# Controleren op auditlogbestanden{#monitoring-audit-logs}

De dossiers van het logboek van de controle volgen alle pogingen verbindingen aan en losmakingen van de Server van het Inzicht, elk van waarvan het programma wordt geopend de `<YYYYMMDD>-access.txt` dossiers die door gebrek in de omslag van de Controle binnen de de installatiemap van de Server van het Inzicht worden gevestigd.

**Aanbevolen frequentie:** Dagelijks of indien nodig voor probleemoplossing

De logboeken van de controle kunnen zeer nuttig zijn wanneer het oplossen van problemenkwesties die met [!DNL Insight Server] verbinden. U kunt deze logboeken controleren met uw geautomatiseerde beheertool of door de [!DNL access.txt] dossiers direct te bekijken.

**Als u de bestanden access.txt via het dialoogvenster[!DNL Server Files Manager]**

1. Klik in [!DNL Insight] op het tabblad [!DNL Admin] > [!DNL Dataset and Profile] op de miniatuur **[!UICONTROL Servers Manager]** om de werkruimte Servers Manager te openen.
1. Klik met de rechtermuisknop op het pictogram van een actieve [!DNL Insight Server] en klik op **[!UICONTROL Server Files]**.
1. Klik in [!DNL Server Files Manager] op **[!UICONTROL Audit]** om de inhoud ervan weer te geven.
1. Klik met de rechtermuisknop op het vinkje in de kolom *servernaam* naast het gewenste bestand en klik op **[!UICONTROL Make Local]**. Er wordt een vinkje weergegeven naast de bestandsnaam in de kolom [!DNL Temp].
1. Klik met de rechtermuisknop op het nieuwe vinkje in de kolom [!DNL Temp] en klik op **[!UICONTROL Open]** > **[!UICONTROL in Notepad]**. Het controlelogboek verschijnt in een nieuw venster van de Blocnote van Microsoft Windows.

   ![Stapinfo](assets/cfg_accesscontrol_accessFile.png)
