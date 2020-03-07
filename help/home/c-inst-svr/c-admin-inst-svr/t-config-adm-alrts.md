---
description: Administratieve waarschuwingen sturen e-mailberichten naar de opgegeven e-mailadressen wanneer er tijdens de normale werking fouten worden gedetecteerd door de Insight Server.
solution: Insight
title: Administratieve waarschuwingen configureren
uuid: 398e088b-ff83-46ae-a20c-ba0b50d85702
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Administratieve waarschuwingen configureren{#configuring-administrative-alerts}

Administratieve waarschuwingen sturen e-mailberichten naar de opgegeven e-mailadressen wanneer er tijdens de normale werking fouten worden gedetecteerd door de Insight Server.

**Aanbevolen frequentie:** Vóór de productie

>[!NOTE]
>
>Het gebruik van administratieve alarm vereist dat toegang tot een het door:sturen server SMTP [!DNL Insight Server] heeft om alarm per e-mail te verzenden.

De ontvangers van de e-mailmeldingen moeten het belangrijkste personeel van de systeemadministratie en de belangrijkste betrokkenen zijn.

Het administratieve dossier van het Alarm, [!DNL Administrative Alerts.cfg], wordt gebruikt om het administratieve alarm voor te vormen [!DNL Insight Server].

>[!NOTE]
>
>Als u een cluster in werking stelt, moet u alarm op de meester [!DNL Insight Server] in de cluster tot stand brengen of wijzigen.

**Om een administratief alarm te creëren of te wijzigen**

1. In [!DNL Insight], op het [!DNL Admin] > [!DNL Dataset and Profile] lusje, klik de **[!UICONTROL Servers Manager]** duimnagel om de werkruimte van de Manager van Servers te openen.
1. Klik het pictogram van het pictogram met de rechtermuisknop aan [!DNL Insight Server] u wilt vormen en klikken **[!UICONTROL Server Files]**.
1. In [!DNL Server Files Manager], klik **[!UICONTROL Components]** om zijn inhoud te bekijken. Het [!DNL Administrative Alerts.cfg] dossier wordt gevestigd binnen deze folder.
1. Klik het vinkje in de *server naam *column voor met de rechtermuisknop aan [!DNL Administrative Alerts.cfg] en klik **[!UICONTROL Make Local]**. Een vinkje verschijnt in de [!DNL Temp] kolom voor [!DNL Administrative Alerts.cfg].
1. Klik het pas gecreëerde vinkje in de [!DNL Temp] kolom met de rechtermuisknop aan en klik **[!UICONTROL Open]** > **[!UICONTROL in Insight]**.
1. In het [!DNL Administrative Alerts.cfg] venster, klik **[!UICONTROL component]** om zijn inhoud te bekijken.
1. Vul de parameters uit zoals gewenst. Voor een lijst van de parameters beschikbaar in dit dossier, zie de [Administratieve Montages](../../../home/c-inst-svr/c-cfg-stgs-ref/c-admin-alts-cfg-stgs.md#concept-14c3c3ed797f47c5900ec04cae2fc491)van de Configuratie van het Alarm.

   ![Stapgegevens](assets/cfg_adminalerts_examplevalues.png)

1. Sparen uw veranderingen in de server door het volgende te doen:

   1. Klik **[!UICONTROL (modified)]** bij de bovenkant van het venster met de rechtermuisknop aan en klik **[!UICONTROL Save]**.

   1. Klik in het [!DNL Server Files Manager]dialoogvenster met de rechtermuisknop op het vinkje voor het bestand in de [!DNL Temp] kolom en selecteer **[!UICONTROL Save to]** > *&lt;**[!UICONTROL server name]**>*.

1. (Facultatief) als u in een cluster werkt en u het zelfde administratieve alarm wilt dat op elke Eenheid van de Verwerking van Gegevens wordt toegepast, moet u het bijgewerkte [!DNL Administrative Alerts.cfg] dossier in de [!DNL Components for Processing Servers] omslag binnen de hoofdinstallatiefolder kopiëren en kleven [!DNL Insight Server] .
