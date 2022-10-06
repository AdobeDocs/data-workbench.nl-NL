---
description: Administratieve waarschuwingen verzenden e-mailmeldingen naar de opgegeven e-mailadressen wanneer tijdens de normale werking fouten worden gedetecteerd door de Insight Server.
title: Beheerswaarschuwingen configureren
uuid: 398e088b-ff83-46ae-a20c-ba0b50d85702
exl-id: 886e390f-fb2c-4922-8b01-9e5133a94e1b
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '300'
ht-degree: 0%

---

# Beheerswaarschuwingen configureren{#configuring-administrative-alerts}

{{eol}}

Administratieve waarschuwingen verzenden e-mailmeldingen naar de opgegeven e-mailadressen wanneer tijdens de normale werking fouten worden gedetecteerd door de Insight Server.

**Aanbevolen frequentie:** Vóór de productie

>[!NOTE]
>
>Het gebruik van administratieve waarschuwingen vereist dat [!DNL Insight Server] heeft toegang tot een het door:sturen server SMTP om alarm door e-mail te verzenden.

De ontvangers van de e-mailmeldingen moeten het belangrijkste personeel van de systeemadministratie en de primaire belanghebbenden zijn.

Het bestand met administratieve waarschuwingen, [!DNL Administrative Alerts.cfg], wordt gebruikt om administratieve alarm voor te vormen [!DNL Insight Server].

>[!NOTE]
>
>Als u een cluster uitvoert, moet u waarschuwingen voor de master [!DNL Insight Server] in de cluster.

**Een beheerwaarschuwing maken of wijzigen**

1. In [!DNL Insight]over de [!DNL Admin] > [!DNL Dataset and Profile] klikt u op de knop **[!UICONTROL Servers Manager]** om de werkruimte van Servers Manager te openen.
1. Klik met de rechtermuisknop op het pictogram van het dialoogvenster [!DNL Insight Server] u wilt vormen en klikken **[!UICONTROL Server Files]**.
1. In de [!DNL Server Files Manager], klikt u op **[!UICONTROL Components]** om de inhoud te bekijken. De [!DNL Administrative Alerts.cfg] bestand bevindt zich in deze map.
1. Klik met de rechtermuisknop op het vinkje in de kolom *servernaam *voor [!DNL Administrative Alerts.cfg] en klik op **[!UICONTROL Make Local]**. Er verschijnt een vinkje in het dialoogvenster [!DNL Temp] kolom voor [!DNL Administrative Alerts.cfg].
1. Klik met de rechtermuisknop op het nieuwe vinkje in het dialoogvenster [!DNL Temp] kolom en klik op **[!UICONTROL Open]** > **[!UICONTROL in Insight]**.
1. In de [!DNL Administrative Alerts.cfg] venster, klikt u op **[!UICONTROL component]** om de inhoud te bekijken.
1. Vul de parameters naar wens in. Zie voor een lijst met de parameters die beschikbaar zijn in dit bestand [Configuratie-instellingen voor administratieve waarschuwingen](../../../home/c-inst-svr/c-cfg-stgs-ref/c-admin-alts-cfg-stgs.md#concept-14c3c3ed797f47c5900ec04cae2fc491).

   ![Stapinfo](assets/cfg_adminalerts_examplevalues.png)

1. Sla de wijzigingen op de server op door het volgende te doen:

   1. Klikken met rechtermuisknop **[!UICONTROL (modified)]** boven aan het venster en klik op **[!UICONTROL Save]**.

   1. In de [!DNL Server Files Manager]klikt u met de rechtermuisknop op het vinkje voor het bestand in het dialoogvenster [!DNL Temp] kolom en selecteer **[!UICONTROL Save to]** > *&lt;**[!UICONTROL server name]**>*.

1. (Optioneel) Als u in een cluster werkt en u dezelfde beheerwaarschuwingen wilt toepassen op elke gegevensverwerkingseenheid, moet u de bijgewerkte [!DNL Administrative Alerts.cfg] in het bestand [!DNL Components for Processing Servers] binnen de master map [!DNL Insight Server] installatiemap.
