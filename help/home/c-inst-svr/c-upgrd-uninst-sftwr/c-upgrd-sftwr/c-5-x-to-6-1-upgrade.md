---
description: Volg deze stappen om vanaf de installatie van Insight v5.5x bij te werken naar de gegevenswerkbank v6.1.
solution: Analytics
title: Data Workbench 5.5-6.1-upgrade
topic: Data workbench
uuid: 14e3612e-11a2-402a-9478-904ec55df23c
translation-type: tm+mt
source-git-commit: cb3ca4b3b993f5f04f6b6cee25850600ff3d8986

---


# Data Workbench 5.5-6.1-upgrade{#data-workbench-to-upgrade}

Volg deze stappen om vanaf de installatie van Insight v5.5x bij te werken naar de gegevenswerkbank v6.1.

**Stap 1**: [Serverupgrade](../../../../home/c-inst-svr/c-upgrd-uninst-sftwr/c-upgrd-sftwr/c-5-x-to-6-1-upgrade.md#section-08bd6fe3da8740fcb19688e8cac6f223)

**Stap 2**: [Report Server-upgrade](../../../../home/c-inst-svr/c-upgrd-uninst-sftwr/c-upgrd-sftwr/c-5-x-to-6-1-upgrade.md#section-afd9560a446242e9b06490e5f98aaaec)

**Stap 3**: [Clientupgrade](../../../../home/c-inst-svr/c-upgrd-uninst-sftwr/c-upgrd-sftwr/c-5-x-to-6-1-upgrade.md#section-c896e57ecd2847afb18f4d8ef7cc0e06)

>[!IMPORTANT]
>
>De server, de rapportserver, en de cliëntcomponenten worden bevorderd om op de werkende systemen met 64 bits van Vensters te lopen.

## Serverupgrade {#section-08bd6fe3da8740fcb19688e8cac6f223}

Volg deze stappen om de **[!UICONTROL Server v6.1]** componenten bij te werken:

1. Open met het **[!UICONTROL Software and Docs]** profiel de **[!UICONTROL Start Here]** werkruimte en download alle benodigde serverpakketten naar een lokale map.

   * Download **[!UICONTROL Server Packages]** \ **[!UICONTROL v6.1]** zip omslagen en haal alle dossiers.

      Het **[!UICONTROL Server]** pakket omvat **[!UICONTROL Lookup]** en **[!UICONTROL Profile]** omslagen met de **[!UICONTROL Base]** en **[!UICONTROL Transform]** raadplegingsdossiers om toe te voegen en te vervangen om de server bij te werken.

   * Download nieuwe **[!UICONTROL Profiles]** mappen.
   * Download bijgewerkte **[!UICONTROL Lookup]** mappen.
   * Download het **[!UICONTROL Report Server]** \ **[!UICONTROL v6.1]** pakket.
   * Download extra **[!UICONTROL Sensor]**, **[!UICONTROL Documentation]**, en **[!UICONTROL Dashboard]** dossiers zoals nodig voor uw systeem.

1. Stop de **[!UICONTROL Adobe Insight Server]** service.

   ![](assets/install_server_download1.png)

1. Van het gedownloade **[!UICONTROL Server]** pakket:

   1. Vervang de [!DNL Server\Bin] omslag om de [!DNL InsightServer64.exe] en ondersteunende dossiers bij te werken.

   1. Vervang de [!DNL Server\Profiles] omslag. U kunt alle dossiers beschrijven.
   1. Werk de [!DNL Server\Lookups] map bij. U zult de onlangs gedownloade dossiers aan de douanedossiers willen toevoegen die reeds in de omslag worden gevestigd.
   1. Vervang de bij te werken [!DNL Server\Software] map [!DNL Insight.exe] en [!DNL ReportServer.exe]

   1. Werk de [!DNL Server\Scripts] omslag bij om bij te werken [!DNL TnTSend.exe].

1. Als u **[!UICONTROL DeviceAtlas]**, dan zult u de bundel [moeten](https://docs.adobe.com/content/help/en/data-workbench/using/dataset/trans-config-file/c-deviceatlas-update.html) bijwerken die in de [!DNL Server\Lookups] omslag wordt gevestigd.
1. Reeks [!DNL Directories] in het [!DNL Profile.cfg] dossier om ervoor te zorgen dat de vector wordt bijgewerkt om op het aantal punten voor elk profiel te wijzen.

   Bijvoorbeeld, om het **[!UICONTROL Predictive Analytics]** profiel toe te laten zult u dit het plaatsen moeten bijwerken.

   ```
   Directories = vector: 5 items 
       0 = string: Base\\ 
       1 = string: Geography\\ 
       2 = string: Predictive Analytics\\ 
       3 = string: Adobe SC\\ 
       4 = string: Profile Name\\
   ```

1. Vorm en sla het [!DNL PAServer.cfg] dossier op om de Predictive Analytics eigenschap te bevorderen.

   Als u de taken van de Analyse van de Predictive aan de servers wilt voorleggen, dan zult u het [!DNL Server > Predictive Analytics > Dataset > PAServer.cfg] dossier moeten vormen om server-zij groeperende voorstellingen te beheren.

   Het douaneprofiel zou de montages van het Predictive de configuratieprofiel van de Analyse moeten erven, toestaand u om te vormen en te bewaren [!DNL PAServer.cfg] gebaseerd op de implementatie van uw plaats.

1. Definieer het **[!UICONTROL Log Source ID]**.

   Het **[!UICONTROL Recording of Rows per Log Source]** werd toegevoegd in **[!UICONTROL v6.04]** en in het [!DNL Log Processing.cfg] dossier van het douaneprofiel bepaald door een uniek genoemd toe te voegen **[!UICONTROL Log Source ID]**.

   ```
   Log Processing.cfg
   Log Source ID = string: <Name your ID Here>
   ```

   Als u geen bepaalde Van het Bron logboek identiteitskaart hebt, dan zult u de volgende fout krijgen:

   ```
   Missing Log Source ID in log processing.cfg.  
   Log Source ID must be defined for all log sources.
   ```

1. Omdat [!DNL EventMessages.dll] is bijgewerkt, wordt het vereist dat u desregistreert en dan het **[!UICONTROL Adobe Insight Server]** over de cluster registreert.

   * [!DNL InsightServer64.exe /unregserver]
   * [!DNL InsightServer64.exe /regserver]

1. Begin de **[!UICONTROL Adobe Insight Server]** dienst over de cluster.

De serverinstallatie is nu voltooid.

## Rapportserverupgrade {#section-afd9560a446242e9b06490e5f98aaaec}

>[!IMPORTANT]
>
>Voordat u gaat upgraden naar **[!UICONTROL Report Server v6.1]**, moet u eerst upgraden naar **[!UICONTROL Server v6.1]**.

1. Download het **[!UICONTROL Software and Docs]** profiel **[!UICONTROL v6.1]** van het **[!UICONTROL Report Server]** pakket naar een lokale map.
1. Kopieer **[!UICONTROL Report Server 6.1]** van het gedownloade pakket en vervang de profielpakketten.

   >[!NOTE]
   >
   >Het [!DNL Insight.zbin] dossier in de [!DNL install] omslag is een reservedossier dat voor localisatie wordt gebruikt, en moet in de [!DNL install] folder aanwezig zijn. Dit dossier of andere [!DNL .zbin] dossiers zullen afhankelijk van de bevel-lijn overgegaane montages worden gebruikt wanneer het beginnen.

1. (facultatief) wijzig het de configuratiedossier van de rapportserver om dubbel-bytekarakters te steunen.

   De werkbank van gegevens steunt momenteel Engels (-en-us) en Chinees (-zh-cn). U moet een doopvont plaatsen om enige en dubbel-bytekarakters te steunen:

   ```
   Report Server.cfg - Add Fonts 
      Fonts = vector: 2 items  
      0 = string: SimSun  
      1 = string: Arial 
   ```

   Het werkende systeem van Vensters moet de vermelde geïnstalleerde doopvonten ook hebben.

1. Configureren [!DNL Report Server v6.1].

   1. Stop de **[!UICONTROL Adobe Insight Report Server]** service.
   1. Lanceer een bevelherinnering als &quot;Beheerder&quot;.
   1. Navigeer aan de [!DNL install] omslag van de Server van het Rapport.
   1. Schrap de dienst van de Server van het Rapport gebruikend het volgende bevel:

      ```
      ReportServer.exe /unregserver
      ```

1. Start de service op basis van de taalinstellingen:

   ```
   ReportServer.exe -RegServer -Locale -en-us (English) 
   ReportServer.exe -RegServer -Locale -zh-cn (Simplified Chinese)
   ```

1. Om te verifiëren dat de Server van het Rapport met de correcte montages loopt, open **[!UICONTROL Windows Service Manager]** en klik met de rechtermuisknop aan **[!UICONTROL Adobe Insight Report Server - Properties]**. De weg aan uitvoerbaar zal de bijgewerkte bevel-lijn montages tonen.

De installatie van de rapportserver is nu volledig.

## Clientupgrade {#section-c896e57ecd2847afb18f4d8ef7cc0e06}

>[!IMPORTANT]
>
>Alvorens te bevorderen aan **[!UICONTROL Client v6.1]**, moet de beheerder eerst bevorderen aan **[!UICONTROL Server v6.1.]**

1. Start [!DNL Insight.exe] maar maak GEEN verbinding met profielen.
1. Geef het [!DNL Insight.cfg] dossier uit om geen software automatisch bij te werken.

   ```
   Update Software = bool: false
   ```

1. Verbind met **[!UICONTROL Software and Docs]** profiel (softdocs).
1. Download [!DNL Software\Insight Client\v6.10].
1. (facultatief) wijzig me [!DNL insight.cfg] om dubbel-bytekarakters te steunen.

   De werkbank van gegevens steunt momenteel zowel Engels als Vereenvoudigd Chinees. Selecteer doopvonten om beide talen te steunen:

   ```
   Fonts = vector: 2 items  
   0 = string: SimSun 
   1 = string: Arial
   ```

1. Afsluiten uit de client.
1. Kopieer de dossiers in het gedownloade **v6.1** cliëntpakket aan de [!DNL Install] omslag.

   >[!NOTE]
   >
   >Het [!DNL Insight.zbin] dossier in installeert omslag is een reservedossier dat voor localisatie wordt gebruikt, en moet aanwezig zijn in installeert folder. Dit dossier of andere [!DNL .zbin] dossiers zullen afhankelijk van de bevel-lijn overgegaane montages worden gebruikt wanneer het beginnen.
   >
   >Bijvoorbeeld, om Vereenvoudigd Chinees te lanceren, creeer een kortere weg die in bevel-lijn het plaatsen overgaat.
   >
   >
   ```
   >Insight.exe -zh-cn
   >```
   >
   >Als u in het Engels (gebrek) wilt lanceren, dan is geen bevel-lijn verandering noodzakelijk.

1. Lancering [!DNL Insight.exe] voor het Engels of de kortere weg die u voor een andere taal creeerde.
1. Verbind met uw profiel en sta de cliënt toe om met de server te synchroniseren.
1. (facultatief) om IME aan te wenden, breng deze veranderingen in het [!DNL Insight.cfg] dossier aan:

   ```
   Localized IME = bool: true
   ```

   De redacteur van de Methode van de Input (IME) staat u toe om internationale karakters in te voeren.

1. (facultatief) geef het [!DNL Insight.cfg] dossier uit om software automatisch bij te werken:

   ```
   Update Software = bool: true
   ```

   Zie de instructies voor het implementeren van de IME.
1. Begin opnieuw na de profielsynchronisatie om het meest recente [!DNL .zbin] dossier aan te wenden.

De installatie van de client is nu voltooid.
