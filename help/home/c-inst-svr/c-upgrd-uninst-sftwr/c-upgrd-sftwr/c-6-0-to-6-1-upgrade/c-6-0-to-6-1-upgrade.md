---
description: Voer de volgende stappen uit om een update uit te voeren naar gegevenswerkbank v6.1 van uw gegevenswerkbank v6.0x-installatie.
title: Data Workbench 6.0 tot 6.1-upgrade
uuid: 4671c2bf-06ab-49c4-8dd1-24115facd83b
exl-id: 559e1942-561c-4270-9670-550177730cdb,2a337d2e-c70e-4f35-a6c2-c3a7f50a0800
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '743'
ht-degree: 0%

---

# Data Workbench 6.0 tot 6.1-upgrade{#data-workbench-to-upgrade}

{{eol}}

Voer de volgende stappen uit om een update uit te voeren naar gegevenswerkbank v6.1 van uw gegevenswerkbank v6.0x-installatie.

**Stap 1**: [Serverupgrade](../../../../../home/c-inst-svr/c-upgrd-uninst-sftwr/c-upgrd-sftwr/c-6-0-to-6-1-upgrade/c-6-0-to-6-1-upgrade.md#section-7845393f76214aa7ad53ac4b2cca9e5b)

**Stap 2**: [Upgrade van rapportserver](../../../../../home/c-inst-svr/c-upgrd-uninst-sftwr/c-upgrd-sftwr/c-6-0-to-6-1-upgrade/c-6-0-to-6-1-upgrade.md#section-afd9560a446242e9b06490e5f98aaaec)

**Stap 3**: [Clientupgrade](../../../../../home/c-inst-svr/c-upgrd-uninst-sftwr/c-upgrd-sftwr/c-6-0-to-6-1-upgrade/c-6-0-to-6-1-upgrade.md#section-c896e57ecd2847afb18f4d8ef7cc0e06)

>[!IMPORTANT]
>
>De server, de rapportserver, en de cliëntcomponenten worden bevorderd om op werkende systemen met 64 bits van Vensters te lopen.

## Upgrade van server {#section-7845393f76214aa7ad53ac4b2cca9e5b}

Ga als volgt te werk om de **[!UICONTROL Server v6.1]** componenten:

1. Met de **[!UICONTROL Software and Docs]** profiel openen **[!UICONTROL Start Here]** en download alle benodigde serverpakketten naar een lokale map.

   * Downloaden **[!UICONTROL Server Packages]** \ **[!UICONTROL v6.1]** ZIP-mappen en extraheer alle bestanden.

      Het serverpakket bevat **[!UICONTROL Lookup]** en **[!UICONTROL Profile]** mappen met **[!UICONTROL Base]** en **[!UICONTROL Transform]** profielen om de server bij te werken.

      * Download de **[!UICONTROL Profiles]** mappen.
      * Download de **[!UICONTROL Lookup]** mappen.
      * Download de **[!UICONTROL Report Server]** \ **[!UICONTROL v6.1]** pakket.
      * Meer downloaden **[!UICONTROL Sensor]**, **[!UICONTROL Documentation]**, en **[!UICONTROL Dashboard]** bestanden voor uw systeem.

1. Stop de **[!UICONTROL Adobe Insight Server]** service.

   ![](assets/install_server_download1.png)

1. Van het gedownloade **[!UICONTROL Server]** pakket:

   1. Vervang de [!DNL Server\Bin] map om de [!DNL InsightServer64.exe] en ondersteunende bestanden.

   1. Vervang de [!DNL Server\Profiles] map. U kunt alle bestanden overschrijven.
   1. Werk de [!DNL Server\Lookups] map. U wilt de nieuw gedownloade bestanden toevoegen aan de aangepaste bestanden die zich al in de map bevinden.
   1. Vervang de [!DNL Server\Software] bij te werken map [!DNL Insight.exe] en [!DNL ReportServer.exe]
   1. Werk de [!DNL Server\Scripts] bij te werken map [!DNL TnTSend.exe].

1. Als u **[!UICONTROL DeviceAtlas]** moet u [de bundel bijwerken](/help/home/c-inst-svr/c-upgrd-uninst-sftwr/c-upgrd-sftwr/c-6-0-to-6-1-upgrade/c-deviceatlas-update.md) in de [!DNL Server\Lookups] map.

1. Configureer de [!DNL Profile.cfg] om ervoor te zorgen dat de vector wordt bijgewerkt om het aantal items voor elk profiel weer te geven.

   Als u bijvoorbeeld de opdracht **[!UICONTROL Predictive Analytics]** -profiel moet u deze instelling bijwerken.

   ```
   Directories = vector: 5 items
       0 = string: Base\\
       1 = string: Geography\\
       2 = string: Predictive Analytics\\
       3 = string: Adobe SC\\
       4 = string: Profile Name\\
   ```

1. Configureer het bestand PAServer.cfg en sla dit op voor de functie Predictive Analytics.

   Als u taken voor voorspellende analyse naar de servers wilt verzenden, moet u de [!DNL Server > Predictive Analytics > Dataset > PAServer.cfg] bestand voor het beheer van serverclusteringverzendingen.

   Het aangepaste profiel moet de instellingen overnemen van het configuratieprofiel voor voorspellende analyse, zodat u het [!DNL PAServer.cfg] bestand op basis van de implementatie van uw site.

1. Definieer de **[!UICONTROL Log Source ID]**.

   De **[!UICONTROL Recording of Rows per Log Source]** is toegevoegd in **[!UICONTROL v6.04]** en gedefinieerd in het aangepaste profiel [!DNL Log Processing.cfg] bestand door een unieke naam toe te voegen **[!UICONTROL Log Source ID]**.

   ```
   Log Processing.cfg
   Log Source ID = string: <Name your ID Here>
   ```

   Als u geen Logbron-id hebt gedefinieerd, treedt de volgende fout op:

   ```
   Missing Log Source ID in log processing.cfg.
   Log Source ID must be defined for all log sources.
   ```

1. Omdat [!DNL EventMessages.dll] is bijgewerkt, moet u de registratie ongedaan maken en vervolgens de **[!UICONTROL Adobe Insight Server]** in de cluster.

   * [!DNL InsightServer64.exe /unregserver]
   * [!DNL InsightServer64.exe /regserver]

1. Start de **[!UICONTROL Adobe Insight Server]** de dienst over de cluster.

De serverinstallatie is nu voltooid.

## Upgrade van rapportserver {#section-afd9560a446242e9b06490e5f98aaaec}

>[!IMPORTANT]
>
>Voordat u gaat upgraden naar **[!UICONTROL Report Server v6.1]**, moet u eerst upgraden naar **[!UICONTROL Server v6.1]**.

1. Met de **[!UICONTROL Software and Docs]** profiel, downloaden **[!UICONTROL v6.1]** van de **[!UICONTROL Report Server]** in een lokale map te plaatsen.

1. Kopiëren **[!UICONTROL Report Server 6.1]** uit het gedownloade pakket en vervang de profielpakketten.

   >[!NOTE]
   >
   >De [!DNL Insight.zbin] in het [!DNL install] de map is een back-upbestand dat wordt gebruikt voor lokalisatie en moet aanwezig zijn in de [!DNL install] directory. Dit bestand of een ander bestand [!DNL .zbin] worden gebruikt, afhankelijk van de opdrachtregelinstellingen die bij het opstarten worden doorgegeven.

1. (optioneel) Gegevenswerkbank biedt momenteel ondersteuning voor Engels (-en-us) en Chinees (-zh-cn). U moet een lettertype instellen ter ondersteuning van single- en double-bytetekens:

   ```
   Report Server.cfg - Add Fonts
      Fonts = vector: 2 items
      0 = string: SimSun
      1 = string: Arial
   ```

   De vermelde lettertypen moeten ook op het Windows-besturingssysteem zijn geïnstalleerd.

1. Configureren [!DNL Report Server v6.1] voor lokalisatie.

   1. Stop de **[!UICONTROL Adobe Insight Report Server]** service.
   1. Start een opdrachtprompt als &quot;Beheerder&quot;.
   1. Ga naar de rapportserver [!DNL install] map.
   1. Schrap de dienst van de Server van het Rapport gebruikend het volgende bevel:

      ```
      ReportServer.exe /unregserver
      ```

   1. Start de service op basis van taalinstellingen:

      ```
      ReportServer.exe -RegServer -Locale -en-us (English)
      ReportServer.exe -RegServer -Locale -zh-cn (Simplified Chinese)
      ```

1. Om te verifiëren dat de Server van het Rapport met de correcte montages loopt, open omhoog **[!UICONTROL Windows Service Manager]** en klik met de rechtermuisknop **[!UICONTROL Adobe Insight Report Server - Properties]**. Het pad naar het uitvoerbare bestand geeft de bijgewerkte opdrachtregelinstellingen weer.

De installatie van de rapportserver is nu voltooid.

## Clientupgrade {#section-c896e57ecd2847afb18f4d8ef7cc0e06}

>[!IMPORTANT]
>
>Voordat u gaat upgraden naar **[!UICONTROL Client v6.1]** moet de beheerder eerst een upgrade uitvoeren naar **[!UICONTROL Insight Server v6.1.]**

1. Starten [!DNL Insight.exe] maar maak geen verbinding met profielen.
1. Bewerk de [!DNL Insight.cfg] bestand.

   ```
   Update Software = bool: true
   ```

1. Maak verbinding met uw profiel.

   De client synchroniseren met de server en de client wordt bijgewerkt met de nieuwste v6.1-clientprofielen, uitvoerbare bestanden en configuratiebestanden.

   >[!NOTE]
   >
   >De [!DNL Insight.zbin] in het [!DNL install] Deze map is een back-upbestand dat wordt gebruikt voor lokalisatie en moet aanwezig zijn. Dit bestand of een ander bestand [!DNL .zbin] worden gebruikt, afhankelijk van de opdrachtregelinstellingen die bij het opstarten worden doorgegeven.

   Zie [gelokaliseerde talen instellen](../../../../../home/c-inst-svr/c-upgrd-uninst-sftwr/c-upgrd-sftwr/c-6-0-to-6-1-upgrade/c-localized-ime.md#concept-86d7602cd6ec416b8d4a518f325e001e) om een [!DNL insight.zbin] bestand vereist voor gelokaliseerde instellingen.

**Aanvullende clientinstellingen**

Voor het configureren [!DNL Insight.exe] en ondersteunende bestanden, moet u de clienttoepassing afsluiten.

Vereenvoudigd Chinees installeren:

1. Maak een sneltoets die de opdrachtregelinstelling doorgeeft aan de [!DNL Insight.exe] bestand.

   ```
   Insight.exe -zh-cn
   ```

1. Configureren [!DNL Insight.cfg] ondersteunen van single- en double-byte lettertypen.

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

1. Werk de [!DNL Insight.cfg] bestand met deze instellingen:

   ```
   Localized IME = bool: true
   ```

1. De sneltoets starten die u hebt gemaakt voor het synchroniseren van profielen en de bijgewerkte [!DNL .zbin] bestand.

De clientinstallatie is nu voltooid.
