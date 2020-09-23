---
description: Administratieve waarschuwingen verzenden e-mailmeldingen naar de opgegeven e-mailadressen wanneer tijdens de normale werking fouten worden gedetecteerd door de Insight Server.
solution: Analytics
title: Beheerswaarschuwingen configureren
uuid: 398e088b-ff83-46ae-a20c-ba0b50d85702
translation-type: tm+mt
source-git-commit: 34cdcfc83ae6bb620706db37228e200cff43ab2c
workflow-type: tm+mt
source-wordcount: '300'
ht-degree: 0%

---


# Beheerswaarschuwingen configureren{#configuring-administrative-alerts}

Administratieve waarschuwingen verzenden e-mailmeldingen naar de opgegeven e-mailadressen wanneer tijdens de normale werking fouten worden gedetecteerd door de Insight Server.

**Aanbevolen frequentie:** Vóór de productie

>[!NOTE]
>
>Het gebruik van administratieve alarm vereist dat toegang tot een het door:sturen server SMTP heeft om alarm door e-mail te verzenden. [!DNL Insight Server]

De ontvangers van de e-mailmeldingen moeten het belangrijkste personeel van de systeemadministratie en de primaire belanghebbenden zijn.

Het Administratieve dossier van Alarm, [!DNL Administrative Alerts.cfg], wordt gebruikt om de administratieve alarm voor te vormen [!DNL Insight Server].

>[!NOTE]
>
>Als u een cluster uitvoert, moet u waarschuwingen voor de master code [!DNL Insight Server] in de cluster maken of wijzigen.

**Een beheerwaarschuwing maken of wijzigen**

1. Klik in [!DNL Insight]het tabblad [!DNL Admin] > op de [!DNL Dataset and Profile] **[!UICONTROL Servers Manager]** miniatuur om de werkruimte van Servers Manager te openen.
1. Klik met de rechtermuisknop op het pictogram van het [!DNL Insight Server] object dat u wilt configureren en klik op **[!UICONTROL Server Files]**.
1. Klik in de [!DNL Server Files Manager]werkruimte **[!UICONTROL Components]** om de inhoud weer te geven. Het [!DNL Administrative Alerts.cfg] bestand bevindt zich in deze map.
1. Klik met de rechtermuisknop op het vinkje in de kolom *servernaam *voor [!DNL Administrative Alerts.cfg] en klik op **[!UICONTROL Make Local]**. In de [!DNL Temp] kolom voor [!DNL Administrative Alerts.cfg].
1. Klik met de rechtermuisknop op het nieuwe vinkje in de [!DNL Temp] kolom en klik op **[!UICONTROL Open]** > **[!UICONTROL in Insight]**.
1. Klik in het [!DNL Administrative Alerts.cfg] venster **[!UICONTROL component]** om de inhoud weer te geven.
1. Vul de parameters naar wens in. Voor een lijst van de parameters beschikbaar in dit dossier, zie de [Administratieve Montages](../../../home/c-inst-svr/c-cfg-stgs-ref/c-admin-alts-cfg-stgs.md#concept-14c3c3ed797f47c5900ec04cae2fc491)van de Configuratie van Alarm.

   ![Stapinfo](assets/cfg_adminalerts_examplevalues.png)

1. Sla de wijzigingen op de server op door het volgende te doen:

   1. Klik met de rechtermuisknop **[!UICONTROL (modified)]** boven in het venster en klik op **[!UICONTROL Save]**.

   1. Klik in het [!DNL Server Files Manager]dialoogvenster met de rechtermuisknop op het vinkje voor het bestand in de [!DNL Temp] kolom en selecteer **[!UICONTROL Save to]** > *&lt;**[!UICONTROL server name]**>*.

1. (Optioneel) Als u in een cluster werkt en u dezelfde beheerwaarschuwingen wilt toepassen op elke gegevensverwerkingseenheid, moet u het bijgewerkte [!DNL Administrative Alerts.cfg] bestand kopiëren en in de [!DNL Components for Processing Servers] map in de master [!DNL Insight Server] installatiemap plakken.
