---
description: De het logboekdossiers van de controle volgen alle pogingen om verbindingen aan en verbindingen van de Server van het Inzicht te ontkoppelen, elk waarvan het programma de <YYYYMMDD>-access.txt dossiers wordt geopend die door gebrek in de omslag van de Controle binnen de de installatiefolder van de Server van het Inzicht worden gevestigd.
solution: Insight
title: Controle van controleverslagen
uuid: 38af9328-3f72-48a4-a0de-bf7477fedc25
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Controle van controleverslagen{#monitoring-audit-logs}

De het logboekdossiers van de controle volgen alle pogingen om verbindingen aan en verbindingen van de Server van het Inzicht te sluiten, elk waarvan het programma wordt geopend de `<YYYYMMDD>-access.txt` dossiers die door gebrek in de omslag van de Controle binnen de de installatiefolder van de Server van het Inzicht worden gevestigd.

**Aanbevolen frequentie:** Dagelijks of indien nodig voor probleemoplossing

De logboeken van de controle kunnen zeer nuttig zijn wanneer het oplossen van problemenkwesties verbinden met [!DNL Insight Server]. U kunt deze logboeken controleren gebruikend uw geautomatiseerd beheersinstrument of door de [!DNL access.txt] dossiers direct te bekijken.

**Om access.txt dossiers door te bekijken[!DNL Server Files Manager]**

1. In [!DNL Insight], op het [!DNL Admin] > [!DNL Dataset and Profile] lusje, klik de **[!UICONTROL Servers Manager]** duimnagel om de werkruimte van de Manager van Servers te openen.
1. Klik het pictogram van actief met de rechtermuisknop aan [!DNL Insight Server] en klik **[!UICONTROL Server Files]**.
1. In [!DNL Server Files Manager], klik **[!UICONTROL Audit]** om zijn inhoud te bekijken.
1. Klik het vinkje in de kolom van de *servernaam* naast het gewenste dossier met de rechtermuisknop aan en klik **[!UICONTROL Make Local]**. Een vinkje verschijnt naast het dossier - noem in de [!DNL Temp] kolom.
1. Klik het nieuwe vinkje in de [!DNL Temp] kolom met de rechtermuisknop aan en klik **[!UICONTROL Open]** > **[!UICONTROL in Notepad]**. Het controlelogboek verschijnt in een nieuw venster van de Blocnote van Microsoft Windows.

   ![Stapgegevens](assets/cfg_accesscontrol_accessFile.png)

