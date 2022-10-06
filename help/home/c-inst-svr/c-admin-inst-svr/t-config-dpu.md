---
description: Het DPU- configuratiedossier, DPU.cfg, specificeert diverse prestatiesparameters voor de Server van het Inzicht.
title: DPU.cfg configureren
uuid: c348622b-7d4b-4cfa-a8f8-a07d91e440d5
exl-id: 55e4ea7f-fee3-4af7-9cbc-d121e79e6ab2
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '206'
ht-degree: 0%

---

# DPU.cfg configureren{#configuring-dpu-cfg}

{{eol}}

Het DPU- configuratiedossier, DPU.cfg, specificeert diverse prestatiesparameters voor de Server van het Inzicht.

Hoe u deze parameters plaatst hangt van uw datasetgrootte en vele andere factoren af. Neem contact op met de Adobe Consulting Services voor hulp bij het afstemmen van de prestaties.

**Aanbevolen frequentie:** Alleen indien nodig

**Wijzigen [!DNL Insight Server] DPU-prestatieinstellingen**

1. In [!DNL Insight]over de [!DNL Admin] > [!DNL Dataset and Profile] klikt u op de knop **[!UICONTROL Servers Manager]** om de werkruimte van Servers Manager te openen.
1. Klik met de rechtermuisknop op het pictogram van het dialoogvenster [!DNL Insight Server] u wilt vormen en klikken **[!UICONTROL Server Files]**.
1. In de [!DNL Server Files Manager], klikt u op **[!UICONTROL Components]** om de inhoud te bekijken. De [!DNL DPU.cfg] bestand bevindt zich in deze map.
1. Klik met de rechtermuisknop op het vinkje in het dialoogvenster *servernaam* kolom voor [!DNL DPU.cfg] en klik op **[!UICONTROL Make Local]**. Er verschijnt een vinkje in het dialoogvenster [!DNL Temp] kolom voor [!DNL DPU.cfg].
1. Klik met de rechtermuisknop op het nieuwe vinkje in het dialoogvenster [!DNL Temp] kolom en klik op **[!UICONTROL Open]** > **[!UICONTROL in Insight]**.
1. In de [!DNL DPU.cfg] klikt u op component om de inhoud ervan weer te geven.
1. Wijzig desgewenst de prestatie- en padinstellingen. Zie voor een lijst met de parameters die beschikbaar zijn in dit bestand [DPU-prestatieinstellingen](../../../home/c-inst-svr/c-cfg-stgs-ref/c-dpu-perf-stgs.md#concept-477c4c526de44bda84176e62266c3df1).

   >[!NOTE]
   >
   >Neem contact op met Adobe voordat u een van de parameters in dit bestand wijzigt.

   ![](assets/cfg_DPU_egvalues.png)

1. Sla de wijzigingen op de server op door het volgende te doen:

   1. Klikken met rechtermuisknop **[!UICONTROL (modified)]** boven aan het venster en klik op **[!UICONTROL Save]**.

   1. In de [!DNL Server Files Manager]klikt u met de rechtermuisknop op het vinkje voor het bestand in het dialoogvenster [!DNL Temp] kolom en selecteer **[!UICONTROL Save to]** > *&lt;**[!UICONTROL server name]**>*.
