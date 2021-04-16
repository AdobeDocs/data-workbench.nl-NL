---
description: Het DPU- configuratiedossier, DPU.cfg, specificeert diverse prestatiesparameters voor de Server van het Inzicht.
title: DPU.cfg configureren
uuid: c348622b-7d4b-4cfa-a8f8-a07d91e440d5
exl-id: 55e4ea7f-fee3-4af7-9cbc-d121e79e6ab2
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '206'
ht-degree: 0%

---

# DPU.cfg{#configuring-dpu-cfg} configureren

Het DPU- configuratiedossier, DPU.cfg, specificeert diverse prestatiesparameters voor de Server van het Inzicht.

Hoe u deze parameters plaatst hangt van uw datasetgrootte en vele andere factoren af. Neem contact op met de Adobe Consulting Services voor hulp bij het afstemmen van de prestaties.

**Aanbevolen frequentie:** Alleen indien nodig

**De instellingen voor  [!DNL Insight Server] DPU-prestaties wijzigen**

1. Klik in [!DNL Insight] op het tabblad [!DNL Admin] > [!DNL Dataset and Profile] op de miniatuur **[!UICONTROL Servers Manager]** om de werkruimte Servers Manager te openen.
1. Klik met de rechtermuisknop op het pictogram van de [!DNL Insight Server] die u wilt configureren en klik op **[!UICONTROL Server Files]**.
1. Klik in [!DNL Server Files Manager] op **[!UICONTROL Components]** om de inhoud ervan weer te geven. Het [!DNL DPU.cfg]-bestand bevindt zich in deze map.
1. Klik met de rechtermuisknop op het vinkje in de kolom *servernaam* voor [!DNL DPU.cfg] en klik op **[!UICONTROL Make Local]**. In de kolom [!DNL Temp] wordt een vinkje weergegeven voor [!DNL DPU.cfg].
1. Klik met de rechtermuisknop op het nieuwe vinkje in de kolom [!DNL Temp] en klik op **[!UICONTROL Open]** > **[!UICONTROL in Insight]**.
1. Klik in het venster [!DNL DPU.cfg] op component om de inhoud ervan weer te geven.
1. Wijzig desgewenst de prestatie- en padinstellingen. Voor een lijst van de parameters beschikbaar in dit dossier, zie [de Montages van Prestaties van DPU](../../../home/c-inst-svr/c-cfg-stgs-ref/c-dpu-perf-stgs.md#concept-477c4c526de44bda84176e62266c3df1).

   >[!NOTE]
   >
   >Neem contact op met Adobe voordat u een van de parameters in dit bestand wijzigt.

   ![](assets/cfg_DPU_egvalues.png)

1. Sla de wijzigingen op de server op door het volgende te doen:

   1. Klik met de rechtermuisknop **[!UICONTROL (modified)]** boven in het venster en klik **[!UICONTROL Save]**.

   1. Klik in [!DNL Server Files Manager] met de rechtermuisknop op het vinkje voor het bestand in de kolom [!DNL Temp] en selecteer **[!UICONTROL Save to]** > *&lt;**[!UICONTROL server name]**>*.
