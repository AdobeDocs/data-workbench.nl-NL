---
description: Het DPU- configuratiedossier, DPU.cfg, specificeert diverse prestatiesparameters voor de Server van het Inzicht.
solution: Analytics
title: DPU.cfg configureren
uuid: c348622b-7d4b-4cfa-a8f8-a07d91e440d5
translation-type: tm+mt
source-git-commit: 34cdcfc83ae6bb620706db37228e200cff43ab2c
workflow-type: tm+mt
source-wordcount: '206'
ht-degree: 0%

---


# DPU.cfg configureren{#configuring-dpu-cfg}

Het DPU- configuratiedossier, DPU.cfg, specificeert diverse prestatiesparameters voor de Server van het Inzicht.

Hoe u deze parameters plaatst hangt van uw datasetgrootte en vele andere factoren af. Neem contact op met de Adobe Consulting Services voor hulp bij het afstemmen van de prestaties.

**Aanbevolen frequentie:** Alleen indien nodig

**DPU-prestatieinstellingen wijzigen[!DNL Insight Server]**

1. Klik in [!DNL Insight]het tabblad [!DNL Admin] > op de [!DNL Dataset and Profile] **[!UICONTROL Servers Manager]** miniatuur om de werkruimte van Servers Manager te openen.
1. Klik met de rechtermuisknop op het pictogram van het [!DNL Insight Server] object dat u wilt configureren en klik op **[!UICONTROL Server Files]**.
1. Klik in de [!DNL Server Files Manager]werkruimte **[!UICONTROL Components]** om de inhoud weer te geven. Het [!DNL DPU.cfg] bestand bevindt zich in deze map.
1. Klik met de rechtermuisknop op het vinkje in de kolom *Servernaam* voor [!DNL DPU.cfg] en klik op **[!UICONTROL Make Local]**. In de [!DNL Temp] kolom voor [!DNL DPU.cfg].
1. Klik met de rechtermuisknop op het nieuwe vinkje in de [!DNL Temp] kolom en klik op **[!UICONTROL Open]** > **[!UICONTROL in Insight]**.
1. Klik in het [!DNL DPU.cfg] venster op de component om de inhoud ervan weer te geven.
1. Wijzig desgewenst de prestatie- en padinstellingen. Voor een lijst van de parameters beschikbaar in dit dossier, zie de Montages [van Prestaties](../../../home/c-inst-svr/c-cfg-stgs-ref/c-dpu-perf-stgs.md#concept-477c4c526de44bda84176e62266c3df1)DPU.

   >[!NOTE]
   >
   >Neem contact op met Adobe voordat u een van de parameters in dit bestand wijzigt.

   ![](assets/cfg_DPU_egvalues.png)

1. Sla de wijzigingen op de server op door het volgende te doen:

   1. Klik met de rechtermuisknop **[!UICONTROL (modified)]** boven in het venster en klik op **[!UICONTROL Save]**.

   1. Klik in het [!DNL Server Files Manager]dialoogvenster met de rechtermuisknop op het vinkje voor het bestand in de [!DNL Temp] kolom en selecteer **[!UICONTROL Save to]** > *&lt;**[!UICONTROL server name]**>*.

