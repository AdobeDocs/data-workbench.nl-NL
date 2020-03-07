---
description: Het DPU configuratiedossier, DPU.cfg, specificeert diverse prestatiesparameters voor de Server van het Inzicht.
solution: Insight
title: Het vormen DPU.cfg
uuid: c348622b-7d4b-4cfa-a8f8-a07d91e440d5
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Het vormen DPU.cfg{#configuring-dpu-cfg}

Het DPU configuratiedossier, DPU.cfg, specificeert diverse prestatiesparameters voor de Server van het Inzicht.

Hoe u deze parameters plaatst hangt van uw datasetgrootte en vele andere factoren af. Tevreden om de Raadplegende Diensten van Adobe voor hulp met prestaties het stemmen te contacteren.

**Aanbevolen frequentie:** Alleen indien nodig

**Om de prestatiesmontages te veranderen[!DNL Insight Server]DPU**

1. In [!DNL Insight], op het [!DNL Admin] > [!DNL Dataset and Profile] lusje, klik de **[!UICONTROL Servers Manager]** duimnagel om de werkruimte van de Manager van Servers te openen.
1. Klik het pictogram van het pictogram met de rechtermuisknop aan [!DNL Insight Server] u wilt vormen en klikken **[!UICONTROL Server Files]**.
1. In [!DNL Server Files Manager], klik **[!UICONTROL Components]** om zijn inhoud te bekijken. Het [!DNL DPU.cfg] dossier wordt gevestigd binnen deze folder.
1. Klik het vinkje in de kolom van de *servernaam* voor met de rechtermuisknop aan [!DNL DPU.cfg] en klik **[!UICONTROL Make Local]**. Een vinkje verschijnt in de [!DNL Temp] kolom voor [!DNL DPU.cfg].
1. Klik het pas gecreëerde vinkje in de [!DNL Temp] kolom met de rechtermuisknop aan en klik **[!UICONTROL Open]** > **[!UICONTROL in Insight]**.
1. In het [!DNL DPU.cfg] venster, klik component om zijn inhoud te bekijken.
1. De prestaties en de wegmontages van de verandering, zonodig. Voor een lijst van de parameters beschikbaar in dit dossier, zie de Montages [van Prestaties](../../../home/c-inst-svr/c-cfg-stgs-ref/c-dpu-perf-stgs.md#concept-477c4c526de44bda84176e62266c3df1)DPU.

   >[!NOTE]
   >
   >Tevreden om Adobe te contacteren alvorens om het even welke parameters in dit dossier te veranderen.

   ![](assets/cfg_DPU_egvalues.png)

1. Sparen uw veranderingen in de server door het volgende te doen:

   1. Klik **[!UICONTROL (modified)]** bij de bovenkant van het venster met de rechtermuisknop aan en klik **[!UICONTROL Save]**.

   1. Klik in het [!DNL Server Files Manager]dialoogvenster met de rechtermuisknop op het vinkje voor het bestand in de [!DNL Temp] kolom en selecteer **[!UICONTROL Save to]** > *&lt;**[!UICONTROL server name]**>*.

