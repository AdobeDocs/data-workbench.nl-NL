---
description: Het Communicatie configuratiedossier, Communications.cfg, bevat het netwerkmontages van de Server van het Inzicht en de weg aan het dossier van Access Control.cfg.
title: Communicatie configureren
uuid: 04d08206-17b1-4348-a945-0c907c9a494c
exl-id: af5e788e-8904-4c68-b02a-c95b523b076d
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '189'
ht-degree: 0%

---

# Communicatie{#configuring-communications} configureren

Het Communicatie configuratiedossier, Communications.cfg, bevat het netwerkmontages van de Server van het Inzicht en de weg aan het dossier van Access Control.cfg.

Met deze instellingen kunt u verbinding maken met [!DNL Insight Server].

**Aanbevolen frequentie:** Alleen indien nodig

**Communicatie-instellingen weergeven en wijzigen in[!DNL Insight]**

1. Klik in [!DNL Insight] op het tabblad [!DNL Admin] > [!DNL Dataset and Profile] op de miniatuur **[!UICONTROL Servers Manager]** om de werkruimte Servers Manager te openen.
1. Klik met de rechtermuisknop op het pictogram van de [!DNL Insight Server] die u wilt configureren en klik op **[!UICONTROL Server Files]**.
1. Klik in [!DNL Server Files Manager] op **[!UICONTROL Components]** om de inhoud ervan weer te geven. Het [!DNL Communications.cfg]-bestand bevindt zich in deze map.
1. Klik met de rechtermuisknop op het vinkje in de kolom *servernaam* voor [!DNL Communications.cfg] en klik op **[!UICONTROL Make Local]**. In de kolom [!DNL Temp] wordt een vinkje weergegeven voor [!DNL Communications.cfg].
1. Klik met de rechtermuisknop op het nieuwe vinkje in de kolom [!DNL Temp] en klik op **[!UICONTROL Open]** > **[!UICONTROL in Insight]**.
1. Klik in het venster [!DNL Communications.cfg] op **[!UICONTROL component]** om de inhoud ervan weer te geven.
1. Wijzig desgewenst de instellingen. Voor informatie over de parameters beschikbaar in dit dossier, zie [Communicatie Montages van de Configuratie](../../../home/c-inst-svr/c-cfg-stgs-ref/c-comm-cfg-stgs.md#concept-aed00587c7a1432fb487bd154aaea6b1).

   ![Stapinfo](assets/cfg_communications_examplevalues.png)

1. Sla de wijzigingen op de server op door het volgende te doen:

   1. Klik met de rechtermuisknop **[!UICONTROL (modified)]** boven in het venster en klik **[!UICONTROL Save]**.

   1. Klik in [!DNL Server Files Manager] met de rechtermuisknop op het vinkje voor het bestand in de kolom [!DNL Temp] en selecteer **[!UICONTROL Save to]** > *&lt;**[!UICONTROL server name]**>*.
