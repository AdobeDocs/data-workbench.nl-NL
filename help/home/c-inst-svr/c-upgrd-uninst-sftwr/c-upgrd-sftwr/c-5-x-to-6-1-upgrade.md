---
description: Voer de volgende stappen uit om een update uit te voeren naar de gegevenswerkbank v6.1 van uw Insight v5.5x-installatie.
title: Data Workbench 5.5 tot 6.1-upgrade
uuid: 14e3612e-11a2-402a-9478-904ec55df23c
exl-id: c730f6d5-2171-4d97-a967-509dc2517c86,3f25917b-b929-4e3b-84f0-1a81b30ba641
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '767'
ht-degree: 0%

---

# Data Workbench 5.5 tot 6.1 Upgrade{#data-workbench-to-upgrade}

Voer de volgende stappen uit om een update uit te voeren naar de gegevenswerkbank v6.1 van uw Insight v5.5x-installatie.

**Stap 1**:  [Upgrade van server](../../../../home/c-inst-svr/c-upgrd-uninst-sftwr/c-upgrd-sftwr/c-5-x-to-6-1-upgrade.md#section-08bd6fe3da8740fcb19688e8cac6f223)

**Stap 2**:  [Upgrade van rapportserver](../../../../home/c-inst-svr/c-upgrd-uninst-sftwr/c-upgrd-sftwr/c-5-x-to-6-1-upgrade.md#section-afd9560a446242e9b06490e5f98aaaec)

**Stap 3**:  [Clientupgrade](../../../../home/c-inst-svr/c-upgrd-uninst-sftwr/c-upgrd-sftwr/c-5-x-to-6-1-upgrade.md#section-c896e57ecd2847afb18f4d8ef7cc0e06)

>[!IMPORTANT]
>
>De server, de rapportserver, en de cliëntcomponenten worden bevorderd om op werkende systemen met 64 bits van Vensters te lopen.

## Server-upgrade {#section-08bd6fe3da8740fcb19688e8cac6f223}

Ga als volgt te werk om de **[!UICONTROL Server v6.1]** componenten bij te werken:

1. Open met het profiel **[!UICONTROL Software and Docs]** de werkruimte **[!UICONTROL Start Here]** en download alle benodigde serverpakketten naar een lokale map.

   * Download **[!UICONTROL Server Packages]** \ **[!UICONTROL v6.1]** ZIP-mappen en extraheer alle bestanden.

      Het **[!UICONTROL Server]**-pakket bevat **[!UICONTROL Lookup]**- en **[!UICONTROL Profile]**-mappen met de opzoekbestanden **[!UICONTROL Base]** en **[!UICONTROL Transform]** die moeten worden toegevoegd en vervangen om de server bij te werken.

   * Download nieuwe **[!UICONTROL Profiles]** mappen.
   * Updates **[!UICONTROL Lookup]**-mappen downloaden.
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
1. Stel [!DNL Directories] in het [!DNL Profile.cfg]-bestand in om ervoor te zorgen dat de vector wordt bijgewerkt met het aantal items voor elk profiel.

   Als u bijvoorbeeld het profiel **[!UICONTROL Predictive Analytics]** wilt inschakelen, moet u deze instelling bijwerken.

   ```
   Directories = vector: 5 items 
       0 = string: Base\\ 
       1 = string: Geography\\ 
       2 = string: Predictive Analytics\\ 
       3 = string: Adobe SC\\ 
       4 = string: Profile Name\\
   ```

1. Configureer het bestand [!DNL PAServer.cfg] en sla dit op om de functie Analytics voor voorspellingen bij te werken.

   Als u taken voor voorspellende analyse wilt indienen bij de servers, moet u het [!DNL Server > Predictive Analytics > Dataset > PAServer.cfg]-bestand configureren voor het beheer van clusteringverzendingen op de server.

   Het aangepaste profiel moet de instellingen overnemen van het configuratieprofiel voor voorspellende analyse, zodat u [!DNL PAServer.cfg] kunt configureren en opslaan op basis van de implementatie van uw site.

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

1. (optioneel) Wijzig het configuratiebestand van de rapportserver om double-bytetekens te ondersteunen.

   De werkbank voor gegevens biedt momenteel ondersteuning voor Engels (-en-us) en Chinees (-zh-cn). U moet een lettertype instellen ter ondersteuning van single- en double-bytetekens:

   ```
   Report Server.cfg - Add Fonts 
      Fonts = vector: 2 items  
      0 = string: SimSun  
      1 = string: Arial 
   ```

   De vermelde lettertypen moeten ook op het Windows-besturingssysteem zijn geïnstalleerd.

1. Configureren [!DNL Report Server v6.1].

   1. Stop de **[!UICONTROL Adobe Insight Report Server]** service.
   1. Start een opdrachtprompt als &quot;Beheerder&quot;.
   1. Navigeer naar de map Report Server [!DNL install].
   1. Schrap de dienst van de Server van het Rapport gebruikend het volgende bevel:

      ```
      ReportServer.exe /unregserver
      ```

1. Start de service op basis van de taalinstellingen:

   ```
   ReportServer.exe -RegServer -Locale -en-us (English) 
   ReportServer.exe -RegServer -Locale -zh-cn (Simplified Chinese)
   ```

1. Om te controleren dat de Server van het Rapport met de correcte montages loopt, open **[!UICONTROL Windows Service Manager]** en klik **[!UICONTROL Adobe Insight Report Server - Properties]** met de rechtermuisknop aan. Het pad naar het uitvoerbare bestand geeft de bijgewerkte opdrachtregelinstellingen weer.

De installatie van de rapportserver is nu voltooid.

## Clientupgrade {#section-c896e57ecd2847afb18f4d8ef7cc0e06}

>[!IMPORTANT]
>
>Voordat u de upgrade naar **[!UICONTROL Client v6.1]** uitvoert, moet de beheerder eerst een upgrade uitvoeren naar **[!UICONTROL Server v6.1.]**

1. Start [!DNL Insight.exe], maar maak geen verbinding met profielen.
1. Bewerk het [!DNL Insight.cfg]-bestand om de software niet automatisch bij te werken.

   ```
   Update Software = bool: false
   ```

1. Verbind met profiel **[!UICONTROL Software and Docs]** (softdocs).
1. Download [!DNL Software\Insight Client\v6.10].
1. (optioneel) Wijzig [!DNL insight.cfg] om double-bytetekens te ondersteunen.

   De werkbank voor gegevens ondersteunt momenteel zowel Engels als Vereenvoudigd Chinees. Selecteer lettertypen die beide talen ondersteunen:

   ```
   Fonts = vector: 2 items  
   0 = string: SimSun 
   1 = string: Arial
   ```

1. Sluit de client af.
1. Kopieer de bestanden in het gedownloade **v6.1**-clientpakket naar de map [!DNL Install].

   >[!NOTE]
   >
   >Het [!DNL Insight.zbin]-bestand in de installatiemap is een back-upbestand dat wordt gebruikt voor lokalisatie en moet aanwezig zijn in de installatiemap. Dit bestand of andere [!DNL .zbin] bestanden worden gebruikt, afhankelijk van de opdrachtregelinstellingen die bij het opstarten worden doorgegeven.
   >
   >Als u bijvoorbeeld Vereenvoudigd Chinees wilt starten, maakt u een sneltoets die de opdrachtregelinstelling doorgeeft.
   >
   >
   ```
   >Insight.exe -zh-cn
   >```
   >
   >Als u in het Engels wilt lanceren (gebrek), dan is geen bevel-lijn verandering noodzakelijk.

1. Start [!DNL Insight.exe] voor Engels of de sneltoets die u voor een andere taal hebt gemaakt.
1. Maak verbinding met uw profiel en zorg dat de client kan synchroniseren met de server.
1. (optioneel) Als u de IME wilt gebruiken, brengt u de volgende wijzigingen aan in het [!DNL Insight.cfg]-bestand:

   ```
   Localized IME = bool: true
   ```

   Met de IME (Input Method Editor) kunt u internationale tekens invoeren.

1. (optioneel) Bewerk het [!DNL Insight.cfg]-bestand om software automatisch bij te werken:

   ```
   Update Software = bool: true
   ```

   Zie de instructies voor het implementeren van de IME.
1. Start opnieuw na de profielsynchronisatie om het meest recente [!DNL .zbin]-bestand te gebruiken.

De clientinstallatie is nu voltooid.
