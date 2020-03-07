---
description: Volg deze stappen om vanaf de installatie van uw gegevenswerkbank v6.0x bij te werken naar de gegevenswerkbank v6.1.
solution: Analytics
title: Data Workbench 6.0-6.1-upgrade
topic: Data workbench
uuid: 4671c2bf-06ab-49c4-8dd1-24115facd83b
translation-type: tm+mt
source-git-commit: cb3ca4b3b993f5f04f6b6cee25850600ff3d8986

---


# Data Workbench 6.0-6.1-upgrade{#data-workbench-to-upgrade}

Volg deze stappen om vanaf de installatie van uw gegevenswerkbank v6.0x bij te werken naar de gegevenswerkbank v6.1.

**Stap 1**: [Serverupgrade](../../../../../home/c-inst-svr/c-upgrd-uninst-sftwr/c-upgrd-sftwr/c-6-0-to-6-1-upgrade/c-6-0-to-6-1-upgrade.md#section-7845393f76214aa7ad53ac4b2cca9e5b)

**Stap 2**: De verbetering van de Server van het [Rapport](../../../../../home/c-inst-svr/c-upgrd-uninst-sftwr/c-upgrd-sftwr/c-6-0-to-6-1-upgrade/c-6-0-to-6-1-upgrade.md#section-afd9560a446242e9b06490e5f98aaaec)

**Stap 3**: [Clientupgrade](../../../../../home/c-inst-svr/c-upgrd-uninst-sftwr/c-upgrd-sftwr/c-6-0-to-6-1-upgrade/c-6-0-to-6-1-upgrade.md#section-c896e57ecd2847afb18f4d8ef7cc0e06)

>[!IMPORTANT]
>
>De server, de rapportserver, en de cliëntcomponenten worden bevorderd om op de werkende systemen met 64 bits van Vensters te lopen.

## Serverupgrade {#section-7845393f76214aa7ad53ac4b2cca9e5b}

Volg deze stappen om de **[!UICONTROL Server v6.1]** componenten bij te werken:

1. Open met het **[!UICONTROL Software and Docs]** profiel de **[!UICONTROL Start Here]** werkruimte en download alle benodigde serverpakketten naar een lokale map.

   * Download **[!UICONTROL Server Packages]** \ **[!UICONTROL v6.1]** zip omslagen en haal alle dossiers.

      Het serverpakket bevat **[!UICONTROL Lookup]** en **[!UICONTROL Profile]** mappen met **[!UICONTROL Base]** en **[!UICONTROL Transform]** profielen om de server bij te werken.

      * Download de **[!UICONTROL Profiles]** mappen.
      * Download de **[!UICONTROL Lookup]** mappen.
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

1. Vorm het [!DNL Profile.cfg] dossier om ervoor te zorgen dat de vector wordt bijgewerkt om op het aantal punten voor elk profiel te wijzen.

   Bijvoorbeeld, om het **[!UICONTROL Predictive Analytics]** profiel toe te laten zult u dit het plaatsen moeten bijwerken.

   ```
   Directories = vector: 5 items 
       0 = string: Base\\ 
       1 = string: Geography\\ 
       2 = string: Predictive Analytics\\ 
       3 = string: Adobe SC\\ 
       4 = string: Profile Name\\
   ```

1. Vorm en sla het PAServer.cfg- dossier voor de Predictive eigenschap van Analytics op.

   Als u de taken van de Analyse van de Predictive aan de servers wilt voorleggen, dan zult u het [!DNL Server > Predictive Analytics > Dataset > PAServer.cfg] dossier moeten vormen om server-zij groeperende voorstellingen te beheren.

   Het douaneprofiel zou de montages van het Predictive de configuratieprofiel van de Analyse moeten erven, toestaand u om het [!DNL PAServer.cfg] dossier te vormen en op te slaan dat op de implementatie van uw plaats wordt gebaseerd.

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

1. (facultatief) de werkbank van gegevens steunt momenteel Engels (-en-us) en Chinees (-zh-cn). U moet een doopvont plaatsen om enige en dubbel-bytekarakters te steunen:

   ```
   Report Server.cfg - Add Fonts 
      Fonts = vector: 2 items  
      0 = string: SimSun  
      1 = string: Arial 
   ```

   Het werkende systeem van Vensters moet de vermelde geïnstalleerde doopvonten ook hebben.

1. Vorm [!DNL Report Server v6.1] voor localisatie.

   1. Stop de **[!UICONTROL Adobe Insight Report Server]** service.
   1. Lanceer een bevelherinnering als &quot;Beheerder&quot;.
   1. Navigeer aan de [!DNL install] omslag van de Server van het Rapport.
   1. Schrap de dienst van de Server van het Rapport gebruikend het volgende bevel:

      ```
      ReportServer.exe /unregserver
      ```

   1. Start de service op basis van taalinstellingen:

      ```
      ReportServer.exe -RegServer -Locale -en-us (English)  
      ReportServer.exe -RegServer -Locale -zh-cn (Simplified Chinese)
      ```

1. Om te verifiëren dat de Server van het Rapport met de correcte montages loopt, open **[!UICONTROL Windows Service Manager]** en klik met de rechtermuisknop aan **[!UICONTROL Adobe Insight Report Server - Properties]**. De weg aan uitvoerbaar zal de bijgewerkte bevel-lijn montages tonen.

De installatie van de rapportserver is nu volledig.

## Clientupgrade {#section-c896e57ecd2847afb18f4d8ef7cc0e06}

>[!IMPORTANT]
>
>Alvorens te bevorderen aan **[!UICONTROL Client v6.1]**, moet de beheerder eerst bevorderen aan **[!UICONTROL Insight Server v6.1.]**

1. Start [!DNL Insight.exe] maar maak geen verbinding met profielen.
1. Bewerk het [!DNL Insight.cfg] bestand.

   ```
   Update Software = bool: true
   ```

1. Maak verbinding met uw profiel.

   Laat de client synchroniseren met de server en uw client wordt bijgewerkt met de nieuwste v6.1client-profielen, uitvoerbare bestanden en configuratiebestanden.

   >[!NOTE]
   >
   >Het [!DNL Insight.zbin] dossier in de [!DNL install] omslag is een reservedossier dat voor localisatie wordt gebruikt en moet aanwezig zijn. Dit dossier of andere [!DNL .zbin] dossiers zullen afhankelijk van de bevel-lijn overgegaane montages worden gebruikt wanneer het beginnen.

   Zie [vestiging gelokaliseerde talen](../../../../../home/c-inst-svr/c-upgrd-uninst-sftwr/c-upgrd-sftwr/c-6-0-to-6-1-upgrade/c-localized-ime.md#concept-86d7602cd6ec416b8d4a518f325e001e) om een [!DNL insight.zbin] dossier toe te voegen dat voor gelokaliseerde montages wordt vereist.

**Extra clientinstellingen**

Alvorens dossiers te vormen [!DNL Insight.exe] en te steunen, moet u de cliënttoepassing weggaan.

Om Vereenvoudigd Chinees te installeren:

1. Creeer een kortere weg die in de bevel-lijn overgaat die aan het [!DNL Insight.exe] dossier plaatst.

   ```
   Insight.exe -zh-cn
   ```

1. Vorm [!DNL Insight.cfg] om enige en dubbel-byte doopvontkarakters te steunen.

   De werkbank van gegevens steunt momenteel zowel Engels als Vereenvoudigd Chinees. U kunt doopvonten selecteren om beide talen te steunen:

   ```
   Fonts = vector: 2 items 
   0 = string: SimSun 
   1 = string: Arial 
   ```

   Het werkende systeem van Vensters moet de gevraagde geïnstalleerde doopvonten ook hebben.

1. Lanceer de kortere weg die u creeerde om profielen en bijgewerkte te synchroniseren. [!DNL zbin] bestand.

Om de Redacteur van de Methode van de Input (IME) aan te wenden.

Met IME kunt u internationale tekens invoeren.

1. Werk het [!DNL Insight.cfg] dossier met deze montages bij:

   ```
   Localized IME = bool: true
   ```

1. Lanceer de kortere weg die u creeerde om profielen en het bijgewerkte [!DNL .zbin] dossier te synchroniseren.

De installatie van de client is nu voltooid.
