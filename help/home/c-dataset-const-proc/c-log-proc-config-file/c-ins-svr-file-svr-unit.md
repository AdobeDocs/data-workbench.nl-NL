---
description: Informatie over de eenheden van de het dossierserver van de Server van het Inzicht en het proces van de de configuratie van de dossierserver.
solution: Analytics
title: Het vormen van een Eenheid van de Server van het Dossier van de Server van de Werkbank van Gegevens
topic: Data workbench
uuid: ccb65952-f017-4434-b2f8-74c274450834
translation-type: tm+mt
source-git-commit: 72761a57e4bb9f230581b2cd37bff04ba7be8e37

---


# Het vormen van een Eenheid van de Server van het Dossier van de Server van de Werkbank van Gegevens{#configuring-a-data-workbench-server-file-server-unit}

Informatie over de eenheden van de het dossierserver van de Server van het Inzicht en het proces van de de configuratie van de dossierserver.

<!--
c_abt_file_svr_units.xml
-->

U kunt de server van de gegevenswerkbank (InsightServer64.exe) vormen om als Eenheid van de Server van het Dossier (FSU) te lopen door de parameters in de **[!UICONTROL Log Sources]** > **[!UICONTROL Log Server]** knoop van het [!DNL Log Processing.cfg] dossier te voltooien. Wanneer de server van de gegevenswerkbank wordt gevormd om als FSU te lopen, slaat het brondossiers ( [!DNL .vsl] dossiers, tekstdossiers, of de dossiers van XML) op die snel door veelvoudige verwerkingsservers (DPUs) kunnen worden betreden. Wanneer DPUs in een cluster van de server van de gegevenswerkbank tot FSU toegang heeft om de logboekdossiers te lezen, verdelen zij de logboekdossiers onder hen en waarborgen dat het zelfde dossier niet meer dan eens wordt verwerkt.

>[!NOTE]
>
>Wanneer u een FSU configureert die een servercluster met een gegevenswerkbank met vijf tot tien DPU&#39;s bedient, moet u de master-server van het cluster de FSU maken.

Voor informatie over het installeren van een de servercluster van de gegevenswerkbank, zie de Gids *van de Installatie en van het Beleid van de Producten van de* Server.

<!--
c_file_svr_config_proc.xml
-->

Als de locatie een externe locatie is, wordt het gegevenswerkbankserversysteem dat de gegevens verwerkt, verbonden met het aangewezen externe systeem om de logs te lezen.

Op de server van de gegevenswerkbank die wordt aangewezen om als FSU te lopen, laat het [!DNL Access Control.cfg] dossier DPUs met FSU verbinden, en het [!DNL Communications.cfg] dossier brengt de plaats van de verre gegevensdossiers in kaart. De processtappen om een FSU te vormen zijn als volgt:

1. In het [!DNL Log Processing.cfg] dossier op uw hoofdserver van de gegevenswerkbank, specificeer het type van gegevensbron en de plaats van de bron. Zie het [Specificeren van de Gegevensbron](../../../home/c-dataset-const-proc/c-log-proc-config-file/c-ins-svr-file-svr-unit.md#section-d2b545db7ab142ffb4be32e040395383).

1. In het [!DNL Access Control.cfg] dossier op FSU, geef de toestemmingen uit om DPUs toe te staan om met FSU te verbinden om de logboekgegevens te lezen. Zie [Uitgeven de Toestemmingen op de Eenheid](../../../home/c-dataset-const-proc/c-log-proc-config-file/c-ins-svr-file-svr-unit.md#section-b4a54b591b4e4435a728a67f194057ef)van de Server van het Dossier.

1. In het [!DNL Communications.cfg] dossier op FSU, geef de montages voor de [!DNL LoggingServer] en [!DNL FileServer] ingangen uit om de plaats van de logboekdossiers te specificeren. Zie [het specificeren van de Plaats van de Dossiers](../../../home/c-dataset-const-proc/c-log-proc-config-file/c-ins-svr-file-svr-unit.md#section-f9a649bf1b2544feb10ad8820384edb0)van het Logboek.

1. Als u uw datasetprofiel configureert om op een cluster van de gegevenswerkbankserver te lopen, moet u FSU van het cluster ook de server maken waar alle afmetingen van het profiel worden geconstrueerd:
(Alleen voor gegevenswerkbankserverclusters) In de [!DNL Communications.cfg] en [!DNL cluster.cfg] bestanden op de FSU voegt u items toe voor een &quot;normalisatieserver&quot; om de FSU tot de server binnen het cluster te maken waar alle afmetingen zijn geconstrueerd. Zie het [Creëren van een Centrale Server van de Normalisatie voor een Cluster](../../../home/c-dataset-const-proc/c-log-proc-config-file/c-ins-svr-file-svr-unit.md#section-2c1f57b683f94cc193bc069e886bba28).

Voor instructies om een datasetprofiel te vormen dat door een de servercluster van de gegevenswerkbank moet worden verwerkt, zie de Gids *van de Installatie en van het Beleid van de Producten van de* Server.

>[!NOTE]
>
>De volgende instructies veronderstellen dat alle logboekdossiers in de standaardfolder verblijven. Als u logboeken in een andere folder wilt opslaan of veelvoudige logboekwegen tot stand brengen, contacteer de Raadplegende Diensten van Adobe om uw specifieke configuratie te bespreken.

## Het specificeren van de Gegevensbron {#section-d2b545db7ab142ffb4be32e040395383}

Wanneer het specificeren van verre gegevensbronnen voor een dataset, moet u het type van gegevensbron en de plaats van de logboekdossiers op uw server van de hoofdgegevenswerkbank specificeren.

**Om de gegevensbron en zijn plaats te specificeren**

1. Open het [!DNL Log Processing.cfg] bestand. Zie het [Uitgeven van het Dossier](../../../home/c-dataset-const-proc/c-log-proc-config-file/t-edit-log-proc-config-file.md#task-6a2fa1b735cb4eefad730f0a3a7858e5)van de Configuratie van de Verwerking van het Logboek.

1. Voeg een [!DNL Sensor], logboekdossier, of de gegevensbron van XML toe. Zie [logbestanden](../../../home/c-dataset-const-proc/c-log-proc-config-file/c-log-sources.md#concept-3d4fb817c057447d90f166b1183b461e).

1. Voltooi de parameter van de Wegen van het Logboek. Zie [de Dossiers](../../../home/c-dataset-const-proc/c-log-proc-config-file/c-log-sources.md#concept-b25f11c477b54032a15b6117b3bf9009)van de Sensor, de Dossiers [van het](../../../home/c-dataset-const-proc/c-log-proc-config-file/c-log-sources.md#concept-3d4fb817c057447d90f166b1183b461e)Logboek, of de Bronnen [van het Logboek van](../../../home/c-dataset-const-proc/c-log-proc-config-file/c-log-sources.md#concept-c7b154e93748447b986e97f6ef688887)XML. Ben zeker om geldige URI te specificeren.

1. Voltooi de parameters van de Server van het Logboek die in de volgende lijst worden bepaald:

<table id="table_5881B8DEFF984BC7A620CEEA3A637912"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Parameter </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Naam </td> 
   <td colname="col2"> Naam die de verre dossierserver identificeert. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Algemene naam van SSL-server </td> 
   <td colname="col2"> <p> <span class="wintitle"> De Gemeenschappelijke Naam</span> van de server die op het SSL certificaat van de dossierserver wordt vermeld. </p> <p> Deze parameter is facultatief als SSL <span class="wintitle"> van het</span> Gebruik aan vals wordt geplaatst. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Adres </td> 
   <td colname="col2"> <p>Adres van het bestandsserversysteem. Kan leeg worden gelaten als de <span class="wintitle"> Naam</span> SSL de Gemeenschappelijke Naam <span class="wintitle"></span>van de Server aanpast. </p> <p> Bijvoorbeeld: <span class="filepath"> visual.mycompany.com</span> of 192.168.1.90. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Poort </td> 
   <td colname="col2"> Haven waardoor de de servermachine van de gegevenswerkbank met de dossierserver communiceert. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> SSL-clientcertificaat </td> 
   <td colname="col2"> Naam van het <span class="wintitle"> SSL certificaatdossier</span> voor de server van de gegevenswerkbank (<span class="filepath"> server_cert.pem</span>). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> SSL gebruiken </td> 
   <td colname="col2"> Waar of vals. Waar wijst erop dat de dossierserver <span class="wintitle"> SSL</span>gebruikt. </td> 
  </tr> 
 </tbody> 
</table>

Als een volmachtsserver voor DPUs om met FSU wordt vereist te verbinden, moet u de volgende parameters voltooien:

| Parameter | Beschrijving |
|---|---|
| Proxyadres | Het adres van een volmachtsserver die de server van de gegevenswerkbank moet gebruiken om tot de dossierserver toegang te hebben. |
| Wachtwoord voor proxy | Optioneel. Het wachtwoord aan de volmachtsserver. |
| Proxypoort | De haven van de volmachtsserver. Het gebrek is 8080. |
| Gebruikersnaam proxy | Optioneel. De gebruikersnaam voor de volmachtsserver. |

Na is een voorbeeld van een bepaald [!DNL Log Server] in het [!DNL Log Processing.cfg] dossier. Bron logboek #1 is een bron LogFile die aan een folder genoemd Logs richt (neem nota van URI die in de parameter van de Wegen van het Logboek wordt gespecificeerd) op het systeem genoemd FSU01.

![](assets/cfg_LogProcessing_LogServer.png)

## Het uitgeven van de Toestemmingen op de Eenheid van de Server van het Dossier {#section-b4a54b591b4e4435a728a67f194057ef}

In het vorige proces, vormde u een profiel voor een bepaalde dataset om logboekdossiers van een FSU te lezen. Nu moet u de toestemmingen op FSU uitgeven om verbindingen van DPUs toe te staan die het profiel in werking stellen. De volgende stappen lopen u door het uitgeven van het toestemmingendossier [!DNL Access Control.cfg].

**Om toestemmingen op FSU uit te geven**

1. Open het systeem [!DNL Server Files Manager] voor de server van de gegevenswerkbank die u als FSU vestigt en klik **[!UICONTROL Access Control]** om zijn inhoud te tonen.

   Voor informatie over het openen van en het werken met [!DNL Server Files Manager], zie de Gids van de Gebruiker van de Werkbank van *Gegevens*.

1. In het [!DNL Server Files Manager] venster, klik **[!UICONTROL Access Control]** om zijn inhoud te tonen. Het [!DNL Access Control.cfg] dossier wordt gevestigd binnen deze folder.

1. Klik het vinkje in de kolom van de servernaam voor met de rechtermuisknop aan [!DNL Access Control.cfg], dan klik **[!UICONTROL Make Local]**. Een vinkje verschijnt in de [!DNL Temp] kolom voor [!DNL Access Control.cfg].

1. Klik het pas gecreëerde vinkje onder de [!DNL Temp] kolom met de rechtermuisknop aan en klik **[!UICONTROL Open]** > **[!UICONTROL in Workstation]**.

1. In het [!DNL Access Control] venster, klik **[!UICONTROL Access Control Groups]** om zijn inhoud te tonen.

1. Klik het numerieke etiket voor de definitieve [!DNL AccessGroup] in de lijst met de rechtermuisknop aan en klik **[!UICONTROL Add new]** > **[!UICONTROL Group]**.

1. Ga een [!DNL Name] voor het nieuwe in [!DNL AccessGroup]. Voorbeeld: Servers aansluiten.

1. Klik **[!UICONTROL Member]** onder het nieuwe [!DNL AccessGroup]met de rechtermuisknop aan, dan klik **[!UICONTROL Add new]** > **[!UICONTROL Member]**.

1. Ga het IP adres voor DPU van de server van de gegevenswerkbank in die met deze dossierserver verbindt.
1. Herhaal stappen 4 en 5 voor een andere server DPUs van de gegevenswerkbank die met dit FSU, met inbegrip van de server DPUs van de gegevenswerkbank in een cluster verbinden die tot de logboekdossiers moet toegang hebben.
1. Klik **[!UICONTROL Read-Only Access]** onder het nieuwe [!DNL AccessGroup]met de rechtermuisknop aan, dan klik **[!UICONTROL Add new]** > **[!UICONTROL URI]**.

1. Ga de plaats van de opgeslagen logboekdossiers op het systeem van de dossierserver in. Gebruik voorwaartse schuine strepen (/) in de wegspecificatie. De standaardplaats is /Logs/.
1. Klik **[!UICONTROL (modified)]** bij de bovenkant van het venster met de rechtermuisknop aan, dan klik **[!UICONTROL Save]**.

1. Klik in het [!DNL Server Files Manager] venster met de rechtermuisknop op het vinkje voor [!DNL Access Control.cfg] in de [!DNL Temp] kolom en klik vervolgens op **[!UICONTROL Save to]** > **[!UICONTROL server name]** om de lokaal aangebrachte wijzigingen op te slaan in de FSU van de server van de gegevenswerkbank.

## De locatie van de logbestanden opgeven {#section-f9a649bf1b2544feb10ad8820384edb0}

U moet het [!DNL Communications.cfg] dossier op FSU uitgeven om de plaats van de logboekdossiers te specificeren.

**Om de plaats van de logboekdossiers te specificeren**

1. In het [!DNL Server Files Manager] venster, klik **[!UICONTROL Components]** om zijn inhoud te tonen. Het [!DNL Communications.cfg] dossier wordt gevestigd binnen deze folder.

1. Klik het vinkje in de kolom van de servernaam voor met de rechtermuisknop aan [!DNL Communications.cfg], dan klik **[!UICONTROL Make Local]**. Een vinkje verschijnt in de [!DNL Temp] kolom voor [!DNL Communications.cfg].

1. Klik het pas gecreëerde vinkje onder de [!DNL Temp] kolom met de rechtermuisknop aan en klik **[!UICONTROL Open]** > **[!UICONTROL in Workstation.]**.

1. In het [!DNL Communications.cfg] venster, klik **[!UICONTROL component]** om zijn inhoud te tonen.

1. In het [!DNL Communications.cfg] venster, klik **[!UICONTROL Servers]** om zijn inhoud te tonen. Er kunnen meerdere servers worden weergegeven: Bestandsservers, logboekservers, IP-servers, statusservers, servers verzenden of servers repliceren.

1. (Voor [!DNL Sensor] logboekbronnen slechts) vind [!DNL LoggingServer], die is waar zijn logboekdossiers [!DNL Sensor] schrijft die door de server van de gegevenswerkbank moeten worden verwerkt, dan zijn aantal klikken om het menu te bekijken. Geef de parameter van de Folder van het Logboek uit om op de gewenste plaats van de logboekdossiers te wijzen. De standaardlogboekfolder is de omslag van Logs binnen de de installatiefolder van de server van de gegevenswerkbank.

   Wijzig geen andere parameters voor de [!DNL LoggingServer].

   ![](assets/cfg_Communications_LoggingServer.png)

1. Vind FileServer die de plaats van logboekdossiers specificeert. Er kunnen verscheidene Servers van het Dossier zijn die onder Servers worden vermeld, zodat kunt u de inhoud voor veel van hen (door het serveraantal te klikken) moeten bekijken om de gewenste server te vinden.
1. Geef de parameters [!DNL Local Path] en van URI voor FileServer uit om op de plaats van de logboekdossiers te wijzen. Het volgende voorbeeld toont aan dat de logboekdossiers in de omslag van Logs binnen de de installatiefolder van de server van de gegevenswerkbank verblijven:

   ![](assets/cfg_Communications_FS.png)

   >[!NOTE]
   >
   >Als de parameters [!DNL Local Path] en van URI zoals getoond bevolkt zijn, kunt u tot de logboekdossiers op FSU van om het even welke server van de gegevenswerkbank toegang hebben door [!DNL Logs] in te klikken [!DNL Server Files Manager].

1. Klik **[!UICONTROL (modified)]** bij de bovenkant van het configuratievenster met de rechtermuisknop aan, dan klik **[!UICONTROL Save]**.

1. Klik in het [!DNL Server Files Manager] venster met de rechtermuisknop op het vinkje voor [!DNL Communications.cfg] in de [!DNL Temp] kolom en klik vervolgens op **[!UICONTROL Save to]** > *&lt;**[!UICONTROL server name]**>* om de lokaal aangebrachte wijzigingen in de FSU van de gegevenswerkbankserver op te slaan.

## Het creëren van een Centrale Server van de Normalisatie voor een Cluster {#section-2c1f57b683f94cc193bc069e886bba28}

Als u uw datasetprofiel configureert om op een cluster van de gegevenswerkbankserver te lopen, dan zou u FSU van het cluster de server moeten maken waar alle afmetingen van het profiel worden geconstrueerd.

Adobe adviseert sterk dat FSU van het cluster als hoofdserver van de cluster en zijn gecentraliseerde normalisatieserver dient.

Om van FSU de gecentraliseerde normalisatieserver te maken, moet u de FSU-bestanden [!DNL Communications.cfg] en - [!DNL Cluster.cfg] bestanden openen en bewerken.

**Om van de FSU de gecentraliseerde normalisatieserver te maken**

1. Voeg een [!DNL NormalizeServer] ingang aan het [!DNL Communications.cfg] dossier op FSU toe.

   >[!NOTE]
   >
   >Als u het volledige releasepakket voor de server van de gegevenswerkbank v5.0 of later hebt geïnstalleerd, zou het [!DNL Communications.cfg] dossier op uw FSU reeds een [!DNL NormalizeServer] ingang moeten hebben. U kunt de stappen hieronder volgen om te bevestigen dat de ingang bestaat.

   1. Open het [!DNL Communications.cfg] dossier in gegevenswerkbank zoals die in het [Specificeren van de Plaats van de Dossiers](#section-f9a649bf1b2544feb10ad8820384edb0)van het Logboek wordt beschreven.

   1. Klik **[!UICONTROL component]** om zijn inhoud te tonen.
   1. Klik met de rechtermuisknop **[!UICONTROL Servers]** en klik op **[!UICONTROL Add New]** > **[!UICONTROL Centralized Normalization Server]**.

   1. In de parameter van URI voor [!DNL NormalizeServer], type [!DNL /Cluster/].

      ![](assets/cfg_Communications_NormalizeServer.png)

   1. Klik **[!UICONTROL (modified)]** bij de bovenkant van het venster met de rechtermuisknop aan, en klik **[!UICONTROL Save]**.

   1. Klik in het [!DNL Server Files Manager] venster met de rechtermuisknop op het vinkje voor [!DNL Communications.cfg] in de [!DNL Temp] kolom en klik vervolgens op **[!UICONTROL Save to]** > *&lt;**[!UICONTROL server]**>* om de lokaal aangebrachte wijzigingen in de FSU-server van de gegevenswerkbank op te slaan.

1. Bepaal de gecentraliseerde normalisatieserver in het [!DNL Cluster.cfg] dossier op de hoofdserver in uw cluster van de Server van de gegevenswerkbank.

   >[!NOTE]
   >
   >Als FSU waarop u vestiging uw gecentraliseerde normalisatieserver niet de hoofdserver van de gegevenswerkbank in uw cluster bent, moet u de IP adressen van DPUs in de cluster aan de [!DNL Cluster Servers] toegangsgroep in het [!DNL Access Control.cfg] dossier van FSU toevoegen. Voor instructies om servers aan de [!DNL Cluster Servers] groep toe te voegen, zie het Bijwerken van het Dossier van het Toegangsbeheer voor een sectie van de Cluster in de Gids van de Installatie en van het Beleid van de Producten van de *Server.*

   1. Open het [!DNL Profile Manager] binnen uw datasetprofiel, dan klik **[!UICONTROL Dataset]** om zijn inhoud te tonen. Het [!DNL Cluster.cfg] dossier wordt gevestigd binnen deze folder.

   1. Klik het vinkje naast [!DNL Cluster.cfg]met de rechtermuisknop aan, dan klik **[!UICONTROL Make Local]**. Een vinkje voor dit dossier verschijnt in de [!DNL User] kolom.

   1. Klik het pas gecreëerde vinkje met de rechtermuisknop aan en klik **[!UICONTROL Open]** > **[!UICONTROL in Notepad]**.

   1. Voeg de tekst toe die in het volgende dossierfragment wordt benadrukt:

      [!DNL Cluster = ClusterConfig:]

      [!DNL Normalize Server = serverInfo:]

      [!DNL Address = string:]

      [!DNL Port = int: 80]

      [!DNL SSL Server Common Name = string: server common name]

      [!DNL Use SSL = bool: false]

      >[!NOTE]
      >
      >Wanneer u de gemeenschappelijke naam van FSU voor de SSL parameter van de Naam van de Server Gemeenschappelijke ingaat, gebruikt FSU zijn [!DNL .address] dossier om de gemeenschappelijke naam op te lossen. Voor informatie over het [!DNL .address] dossier, zie de Gids *van de Installatie en van het Beleid van de Producten van de* Server.

   1. Sla het bestand op.
   1. In [!DNL Profile Manager], klik het vinkje voor [!DNL Cluster.cfg] in de [!DNL User] kolom met de rechtermuisknop aan, dan klik **[!UICONTROL Save to]** > ***[!UICONTROL dataset profile name]*** om de plaatselijk aangebrachte veranderingen in het datasetprofiel te bewaren.
