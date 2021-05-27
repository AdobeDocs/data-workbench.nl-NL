---
description: Administratieve waarschuwingen verzenden e-mailmeldingen naar de opgegeven e-mailadressen wanneer tijdens de normale werking fouten worden gedetecteerd door de Insight Server.
title: Beheerswaarschuwingen configureren
uuid: 398e088b-ff83-46ae-a20c-ba0b50d85702
exl-id: 886e390f-fb2c-4922-8b01-9e5133a94e1b
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '300'
ht-degree: 0%

---

# Het vormen Administratieve Alarm{#configuring-administrative-alerts}

Administratieve waarschuwingen verzenden e-mailmeldingen naar de opgegeven e-mailadressen wanneer tijdens de normale werking fouten worden gedetecteerd door de Insight Server.

**Aanbevolen frequentie:** vóór productie

>[!NOTE]
>
>Het gebruik van administratieve alarm vereist dat [!DNL Insight Server] toegang tot een het door:sturen server SMTP heeft om alarm door e-mail te verzenden.

De ontvangers van de e-mailmeldingen moeten het belangrijkste personeel van de systeemadministratie en de primaire belanghebbenden zijn.

Het Administratieve dossier van Alarm, [!DNL Administrative Alerts.cfg], wordt gebruikt om de administratieve alarm voor [!DNL Insight Server] te vormen.

>[!NOTE]
>
>Als u een cluster in werking stelt, moet u alarm over master [!DNL Insight Server] in de cluster tot stand brengen of wijzigen.

**Een beheerwaarschuwing maken of wijzigen**

1. Klik in [!DNL Insight] op het tabblad [!DNL Admin] > [!DNL Dataset and Profile] op de miniatuur **[!UICONTROL Servers Manager]** om de werkruimte Servers Manager te openen.
1. Klik met de rechtermuisknop op het pictogram van de [!DNL Insight Server] die u wilt configureren en klik op **[!UICONTROL Server Files]**.
1. Klik in [!DNL Server Files Manager] op **[!UICONTROL Components]** om de inhoud ervan weer te geven. Het [!DNL Administrative Alerts.cfg]-bestand bevindt zich in deze map.
1. Klik met de rechtermuisknop op het vinkje in de kolom *servernaam *voor [!DNL Administrative Alerts.cfg] en klik op **[!UICONTROL Make Local]**. In de kolom [!DNL Temp] wordt een vinkje weergegeven voor [!DNL Administrative Alerts.cfg].
1. Klik met de rechtermuisknop op het nieuwe vinkje in de kolom [!DNL Temp] en klik op **[!UICONTROL Open]** > **[!UICONTROL in Insight]**.
1. Klik in het venster [!DNL Administrative Alerts.cfg] op **[!UICONTROL component]** om de inhoud ervan weer te geven.
1. Vul de parameters naar wens in. Voor een lijst van de parameters beschikbaar in dit dossier, zie [Administratieve Montages van de Configuratie van Alarm](../../../home/c-inst-svr/c-cfg-stgs-ref/c-admin-alts-cfg-stgs.md#concept-14c3c3ed797f47c5900ec04cae2fc491).

   ![Stapinfo](assets/cfg_adminalerts_examplevalues.png)

1. Sla de wijzigingen op de server op door het volgende te doen:

   1. Klik met de rechtermuisknop **[!UICONTROL (modified)]** boven in het venster en klik **[!UICONTROL Save]**.

   1. Klik in [!DNL Server Files Manager] met de rechtermuisknop op het vinkje voor het bestand in de kolom [!DNL Temp] en selecteer **[!UICONTROL Save to]** > *&lt;**[!UICONTROL server name]**>*.

1. (Optioneel) Als u in een cluster werkt en u dezelfde beheerwaarschuwingen wilt toepassen op elke gegevensverwerkingseenheid, moet u het bijgewerkte [!DNL Administrative Alerts.cfg]-bestand kopiëren en in de map [!DNL Components for Processing Servers] in de master [!DNL Insight Server]-installatiemap plakken.
