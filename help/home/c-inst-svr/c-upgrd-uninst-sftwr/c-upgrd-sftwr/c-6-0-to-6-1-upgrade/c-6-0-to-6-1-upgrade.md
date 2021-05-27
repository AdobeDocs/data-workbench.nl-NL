---
description: Voer de volgende stappen uit om een update uit te voeren naar gegevenswerkbank v6.1 van uw gegevenswerkbank v6.0x-installatie.
title: Data Workbench 6.0 tot 6.1-upgrade
uuid: 4671c2bf-06ab-49c4-8dd1-24115facd83b
exl-id: 559e1942-561c-4270-9670-550177730cdb,2a337d2e-c70e-4f35-a6c2-c3a7f50a0800
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '753'
ht-degree: 0%

---

# Data Workbench 6.0 tot 6.1 Upgrade{#data-workbench-to-upgrade}

Voer de volgende stappen uit om een update uit te voeren naar gegevenswerkbank v6.1 van uw gegevenswerkbank v6.0x-installatie.

**Stap 1**:  [Serverupgrade](../../../../../home/c-inst-svr/c-upgrd-uninst-sftwr/c-upgrd-sftwr/c-6-0-to-6-1-upgrade/c-6-0-to-6-1-upgrade.md#section-7845393f76214aa7ad53ac4b2cca9e5b)

**Stap 2**:  [Upgrade van rapportserver](../../../../../home/c-inst-svr/c-upgrd-uninst-sftwr/c-upgrd-sftwr/c-6-0-to-6-1-upgrade/c-6-0-to-6-1-upgrade.md#section-afd9560a446242e9b06490e5f98aaaec)

**Stap 3**:  [Clientupgrade](../../../../../home/c-inst-svr/c-upgrd-uninst-sftwr/c-upgrd-sftwr/c-6-0-to-6-1-upgrade/c-6-0-to-6-1-upgrade.md#section-c896e57ecd2847afb18f4d8ef7cc0e06)

>[!IMPORTANT]
>
>De server, de rapportserver, en de cliëntcomponenten worden bevorderd om op werkende systemen met 64 bits van Vensters te lopen.

## Server-upgrade {#section-7845393f76214aa7ad53ac4b2cca9e5b}

Ga als volgt te werk om de **[!UICONTROL Server v6.1]** componenten bij te werken:

1. Open met het profiel **[!UICONTROL Software and Docs]** de werkruimte **[!UICONTROL Start Here]** en download alle benodigde serverpakketten naar een lokale map.

   * Download **[!UICONTROL Server Packages]** \ **[!UICONTROL v6.1]** ZIP-mappen en extraheer alle bestanden.

      Het serverpakket bevat **[!UICONTROL Lookup]**- en **[!UICONTROL Profile]**-mappen met **[!UICONTROL Base]**- en **[!UICONTROL Transform]**-profielen om de server bij te werken.

      * Download de mappen **[!UICONTROL Profiles]**.
      * Download de mappen **[!UICONTROL Lookup]**.
      * Download het **[!UICONTROL Report Server]** \ **[!UICONTROL v6.1]** pakket.
      * Download indien nodig extra **[!UICONTROL Sensor]**-, **[!UICONTROL Documentation]**- en **[!UICONTROL Dashboard]**-bestanden voor uw systeem.

1. Stop de **[!UICONTROL Adobe Insight Server]** service.

   ![](assets/install_server_download1.png)

1. Vanuit het gedownloade **[!UICONTROL Server]**-pakket:

   1. Vervang de map [!DNL Server\Bin] om de [!DNL InsightServer64.exe] en de ondersteunende bestanden bij te werken.

   1. Vervang de map [!DNL Server\Profiles]. U kunt alle bestanden overschrijven.
   1. Werk de map [!DNL Server\Lookups] bij. U wilt de nieuw gedownloade bestanden toevoegen aan de aangepaste bestanden die zich al in de map bevinden.
   1. De [!DNL Server\Software]-map vervangen om [!DNL Insight.exe] en [!DNL ReportServer.exe] bij te werken
   1. [!DNL Server\Scripts] om [!DNL TnTSend.exe] bij te werken.

1. Als u **[!UICONTROL DeviceAtlas]** in dienst neemt, dan zult u [de bundel](https://docs.adobe.com/content/help/en/data-workbench/using/dataset/trans-config-file/c-deviceatlas-update.html) in [!DNL Server\Lookups] omslag moeten bijwerken.

1. Configureer het [!DNL Profile.cfg]-bestand om ervoor te zorgen dat de vector wordt bijgewerkt met het aantal items voor elk profiel.

   Als u bijvoorbeeld het profiel **[!UICONTROL Predictive Analytics]** wilt inschakelen, moet u deze instelling bijwerken.

   ```
   Directories = vector: 5 items 
       0 = string: Base\\ 
       1 = string: Geography\\ 
       2 = string: Predictive Analytics\\ 
       3 = string: Adobe SC\\ 
       4 = string: Profile Name\\
   ```

1. Configureer het bestand PAServer.cfg en sla dit op voor de functie Predictive Analytics.

   Als u taken voor voorspellende analyse wilt indienen bij de servers, moet u het [!DNL Server > Predictive Analytics > Dataset > PAServer.cfg]-bestand configureren voor het beheer van clusteringverzendingen op de server.

   Het aangepaste profiel moet de instellingen overnemen van het configuratieprofiel voor voorspellende analyse, zodat u het [!DNL PAServer.cfg]-bestand kunt configureren en opslaan op basis van de implementatie van uw site.

1. Definieer de **[!UICONTROL Log Source ID]**.

   **[!UICONTROL Recording of Rows per Log Source]** is toegevoegd in **[!UICONTROL v6.04]** en gedefinieerd in het [!DNL Log Processing.cfg]-bestand van het aangepaste profiel door een unieke naam toe te voegen **[!UICONTROL Log Source ID]**.

   ```
   Log Processing.cfg
   Log Source ID = string: <Name your ID Here>
   ```

   Als u geen Logbron-id hebt gedefinieerd, treedt de volgende fout op:

   ```
   Missing Log Source ID in log processing.cfg.  
   Log Source ID must be defined for all log sources.
   ```

1. Omdat [!DNL EventMessages.dll] is bijgewerkt, is het vereist dat u de registratie ongedaan maakt en vervolgens **[!UICONTROL Adobe Insight Server]** over de cluster registreert.

   * [!DNL InsightServer64.exe /unregserver]
   * [!DNL InsightServer64.exe /regserver]

1. Start de **[!UICONTROL Adobe Insight Server]**-service in de cluster.

De serverinstallatie is nu voltooid.

## Upgrade van rapportserver {#section-afd9560a446242e9b06490e5f98aaaec}

>[!IMPORTANT]
>
>Voordat u een upgrade uitvoert naar **[!UICONTROL Report Server v6.1]**, moet u eerst een upgrade uitvoeren naar **[!UICONTROL Server v6.1]**.

1. Download **[!UICONTROL Software and Docs]** met het profiel **[!UICONTROL v6.1]** van het **[!UICONTROL Report Server]**-pakket naar een lokale map.

1. Kopieer **[!UICONTROL Report Server 6.1]** uit het gedownloade pakket en vervang de profielpakketten.

   >[!NOTE]
   >
   >Het [!DNL Insight.zbin]-bestand in de map [!DNL install] is een back-upbestand dat wordt gebruikt voor lokalisatie en moet aanwezig zijn in de map [!DNL install]. Dit bestand of andere [!DNL .zbin] bestanden worden gebruikt, afhankelijk van de opdrachtregelinstellingen die bij het opstarten worden doorgegeven.

1. (optioneel) Gegevenswerkbank biedt momenteel ondersteuning voor Engels (-en-us) en Chinees (-zh-cn). U moet een lettertype instellen ter ondersteuning van single- en double-bytetekens:

   ```
   Report Server.cfg - Add Fonts 
      Fonts = vector: 2 items  
      0 = string: SimSun  
      1 = string: Arial 
   ```

   De vermelde lettertypen moeten ook op het Windows-besturingssysteem zijn geïnstalleerd.

1. Configureer [!DNL Report Server v6.1] voor lokalisatie.

   1. Stop de **[!UICONTROL Adobe Insight Report Server]** service.
   1. Start een opdrachtprompt als &quot;Beheerder&quot;.
   1. Navigeer naar de map Report Server [!DNL install].
   1. Schrap de dienst van de Server van het Rapport gebruikend het volgende bevel:

      ```
      ReportServer.exe /unregserver
      ```

   1. Start de service op basis van taalinstellingen:

      ```
      ReportServer.exe -RegServer -Locale -en-us (English)  
      ReportServer.exe -RegServer -Locale -zh-cn (Simplified Chinese)
      ```

1. Om te controleren dat de Server van het Rapport met de correcte montages loopt, open **[!UICONTROL Windows Service Manager]** en klik **[!UICONTROL Adobe Insight Report Server - Properties]** met de rechtermuisknop aan. Het pad naar het uitvoerbare bestand geeft de bijgewerkte opdrachtregelinstellingen weer.

De installatie van de rapportserver is nu voltooid.

## Clientupgrade {#section-c896e57ecd2847afb18f4d8ef7cc0e06}

>[!IMPORTANT]
>
>Voordat u de upgrade naar **[!UICONTROL Client v6.1]** uitvoert, moet de beheerder eerst een upgrade uitvoeren naar **[!UICONTROL Insight Server v6.1.]**

1. Start [!DNL Insight.exe], maar maak geen verbinding met profielen.
1. Bewerk het bestand [!DNL Insight.cfg].

   ```
   Update Software = bool: true
   ```

1. Maak verbinding met uw profiel.

   De client synchroniseren met de server en de client wordt bijgewerkt met de nieuwste v6.1-clientprofielen, uitvoerbare bestanden en configuratiebestanden.

   >[!NOTE]
   >
   >Het [!DNL Insight.zbin]-bestand in de map [!DNL install] is een back-upbestand dat wordt gebruikt voor lokalisatie en moet aanwezig zijn. Dit bestand of andere [!DNL .zbin] bestanden worden gebruikt, afhankelijk van de opdrachtregelinstellingen die bij het opstarten worden doorgegeven.

   Zie [gelokaliseerde talen instellen](../../../../../home/c-inst-svr/c-upgrd-uninst-sftwr/c-upgrd-sftwr/c-6-0-to-6-1-upgrade/c-localized-ime.md#concept-86d7602cd6ec416b8d4a518f325e001e) om een [!DNL insight.zbin]-bestand toe te voegen dat vereist is voor gelokaliseerde instellingen.

**Aanvullende clientinstellingen**

Voordat u [!DNL Insight.exe] kunt configureren en bestanden kunt ondersteunen, moet u de clienttoepassing afsluiten.

Vereenvoudigd Chinees installeren:

1. Maak een sneltoets die de opdrachtregelinstelling doorgeeft aan het bestand [!DNL Insight.exe].

   ```
   Insight.exe -zh-cn
   ```

1. Configureer [!DNL Insight.cfg] om single- en double-byte lettertypetekens te ondersteunen.

   De werkbank voor gegevens ondersteunt momenteel zowel Engels als Vereenvoudigd Chinees. U kunt lettertypen selecteren die beide talen ondersteunen:

   ```
   Fonts = vector: 2 items 
   0 = string: SimSun 
   1 = string: Arial 
   ```

   De gevraagde lettertypen moeten ook op het Windows-besturingssysteem zijn geïnstalleerd.

1. Start de sneltoets die u hebt gemaakt om de profielen en de bijgewerkte versie te synchroniseren. [!DNL zbin] bestand.

De invoermethode-editor (IME) gebruiken.

Met IME kunt u internationale tekens invoeren.

1. Werk het [!DNL Insight.cfg] dossier met deze montages bij:

   ```
   Localized IME = bool: true
   ```

1. Start de sneltoets die u hebt gemaakt om profielen en het bijgewerkte [!DNL .zbin]-bestand te synchroniseren.

De clientinstallatie is nu voltooid.
