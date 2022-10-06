---
description: Het Communicatie configuratiedossier, Communications.cfg, bevat het netwerkmontages van de Server van het Inzicht en de weg aan het dossier van Access Control.cfg.
title: Communicatie configureren
uuid: 04d08206-17b1-4348-a945-0c907c9a494c
exl-id: af5e788e-8904-4c68-b02a-c95b523b076d
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '189'
ht-degree: 0%

---

# Communicatie configureren{#configuring-communications}

{{eol}}

Het Communicatie configuratiedossier, Communications.cfg, bevat het netwerkmontages van de Server van het Inzicht en de weg aan het dossier van Access Control.cfg.

Met deze instellingen kunt u verbinding maken met [!DNL Insight Server].

**Aanbevolen frequentie:** Alleen indien nodig

**Communicatie-instellingen weergeven en wijzigen in[!DNL Insight]**

1. In [!DNL Insight]over de [!DNL Admin] > [!DNL Dataset and Profile] klikt u op de knop **[!UICONTROL Servers Manager]** om de werkruimte van Servers Manager te openen.
1. Klik met de rechtermuisknop op het pictogram van het dialoogvenster [!DNL Insight Server] u wilt vormen en klikken **[!UICONTROL Server Files]**.
1. In de [!DNL Server Files Manager], klikt u op **[!UICONTROL Components]** om de inhoud te bekijken. De [!DNL Communications.cfg] bestand bevindt zich in deze map.
1. Klik met de rechtermuisknop op het vinkje in het dialoogvenster *servernaam* kolom voor [!DNL Communications.cfg] en klik op **[!UICONTROL Make Local]**. Er verschijnt een vinkje in het dialoogvenster [!DNL Temp] kolom voor [!DNL Communications.cfg].
1. Klik met de rechtermuisknop op het nieuwe vinkje in het dialoogvenster [!DNL Temp] kolom en klik op **[!UICONTROL Open]** > **[!UICONTROL in Insight]**.
1. In de [!DNL Communications.cfg] venster, klikt u op **[!UICONTROL component]** om de inhoud te bekijken.
1. Wijzig desgewenst de instellingen. Voor informatie over de parameters beschikbaar in dit dossier, zie [Configuratie-instellingen voor communicatie](../../../home/c-inst-svr/c-cfg-stgs-ref/c-comm-cfg-stgs.md#concept-aed00587c7a1432fb487bd154aaea6b1).

   ![Stapinfo](assets/cfg_communications_examplevalues.png)

1. Sla de wijzigingen op de server op door het volgende te doen:

   1. Klikken met rechtermuisknop **[!UICONTROL (modified)]** boven aan het venster en klik op **[!UICONTROL Save]**.

   1. In de [!DNL Server Files Manager]klikt u met de rechtermuisknop op het vinkje voor het bestand in het dialoogvenster [!DNL Temp] kolom en selecteer **[!UICONTROL Save to]** > *&lt;**[!UICONTROL server name]**>*.
