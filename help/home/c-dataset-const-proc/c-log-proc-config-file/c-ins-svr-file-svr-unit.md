---
description: Informatie over de eenheden van de het dossierserver van de Server van het Inzicht en het configuratieproces van de dossierserver.
title: Een Data Workbench Server File Server-eenheid configureren
uuid: ccb65952-f017-4434-b2f8-74c274450834
exl-id: 19b8c08a-e9f2-47ab-ad9f-1fddfbd9d249
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '1784'
ht-degree: 0%

---

# Het vormen van een Eenheid van de Server van het Dossier van de Server van de Data Workbench{#configuring-a-data-workbench-server-file-server-unit}

Informatie over de eenheden van de het dossierserver van de Server van het Inzicht en het configuratieproces van de dossierserver.

<!--
c_abt_file_svr_units.xml
-->

U kunt de gegevenswerkbankserver (InsightServer64.exe) configureren om als eenheid van de Server van het Dossier (FSU) te lopen door de parameters in **[!UICONTROL Log Sources]** > **[!UICONTROL Log Server]** knoop van het [!DNL Log Processing.cfg] dossier te voltooien. Wanneer de server van de gegevenswerkbank wordt gevormd om als FSU in werking te stellen, slaat het brondossiers ( [!DNL .vsl] dossiers, tekstdossiers, of de dossiers van XML) op die snel door veelvoudige verwerkingsservers (DPUs) kunnen worden betreden. Wanneer DPUs in een de servercluster van de gegevenswerkbank tot FSU toegang heeft om de logboekdossiers te lezen, verdelen zij de logboekdossiers onder hen en waarborgen dat het zelfde dossier niet meer dan eens wordt verwerkt.

>[!NOTE]
>
>Wanneer u een FSU instelt die een servercluster van een gegevenswerkbank aanbiedt dat uit vijf tot tien DPU&#39;s bestaat, moet u van de master server van de cluster de FSU maken.

Voor informatie over het installeren van een servercluster van de gegevenswerkbank, zie *de Gids van de Installatie en van het Beleid van de Producten van de Server*.

<!--
c_file_svr_config_proc.xml
-->

Als de locatie een externe locatie is, maakt de gegevenswerkbankservercomputer die de gegevens verwerkt, verbinding met de aangewezen externe computer om de logbestanden te lezen.

Op de computer van de gegevenswerkbankserver die als FSU wordt aangewezen, laat het [!DNL Access Control.cfg] dossier DPUs met FSU verbinden, en [!DNL Communications.cfg] dossier brengt de plaats van de verre gegevensdossiers in kaart. De processtappen om FSU te vormen zijn als volgt:

1. Geef in het [!DNL Log Processing.cfg]-bestand op de master werkbankserver het type gegevensbron en de locatie van de bron op. Zie [De gegevensbron specificeren](../../../home/c-dataset-const-proc/c-log-proc-config-file/c-ins-svr-file-svr-unit.md#section-d2b545db7ab142ffb4be32e040395383).

1. In het [!DNL Access Control.cfg] dossier op FSU, geef de toestemmingen uit om DPUs toe te staan om met FSU te verbinden om de logboekgegevens te lezen. Zie [Machtigingen bewerken op de eenheid Bestandsserver](../../../home/c-dataset-const-proc/c-log-proc-config-file/c-ins-svr-file-svr-unit.md#section-b4a54b591b4e4435a728a67f194057ef).

1. Bewerk in het [!DNL Communications.cfg]-bestand op de FSU de instellingen voor de vermeldingen [!DNL LoggingServer] en [!DNL FileServer] om de locatie van de logbestanden op te geven. Zie [De locatie van de logbestanden opgeven](../../../home/c-dataset-const-proc/c-log-proc-config-file/c-ins-svr-file-svr-unit.md#section-f9a649bf1b2544feb10ad8820384edb0).

1. Als u uw gegevenssetprofiel om op een cluster van de gegevenswerkbankserver vormt te lopen, moet u ook van de FSU van de cluster de server maken waar alle dimensies van het profiel worden geconstrueerd:
(Alleen voor gegevensworkbench-serverclusters) Voeg in de [!DNL Communications.cfg]- en [!DNL cluster.cfg]-bestanden op de FSU items toe voor een &quot;normalize server&quot; om van de FSU de server in de cluster te maken waar alle dimensies worden geconstrueerd. Zie [Een gecentraliseerde normalisatieserver maken voor een cluster](../../../home/c-dataset-const-proc/c-log-proc-config-file/c-ins-svr-file-svr-unit.md#section-2c1f57b683f94cc193bc069e886bba28).

Voor instructies om een gegevenssetprofiel te vormen dat door een servercluster van de gegevenswerkbank moet worden verwerkt, zie *de Gids van de Installatie en van het Beleid van de Producten van de Server*.

>[!NOTE]
>
>In de volgende instructies wordt ervan uitgegaan dat alle logbestanden zich in de standaardmap bevinden. Als u logboeken in een andere folder wilt opslaan of veelvoudige logboekwegen tot stand brengen, contacteer de Raadplegende Diensten van de Adobe om uw specifieke configuratie te bespreken.

## De gegevensbron {#section-d2b545db7ab142ffb4be32e040395383} opgeven

Wanneer het specificeren van verre gegevensbronnen voor een dataset, moet u het type van gegevensbron en de plaats van de logboekdossiers op uw master server van de gegevenswerkbank specificeren.

**De gegevensbron en de locatie opgeven**

1. Open het [!DNL Log Processing.cfg] dossier. Zie [Het configuratiebestand van de logbestandverwerking bewerken](../../../home/c-dataset-const-proc/c-log-proc-config-file/t-edit-log-proc-config-file.md#task-6a2fa1b735cb4eefad730f0a3a7858e5) bewerken.

1. Voeg een [!DNL Sensor], logbestand of XML-gegevensbron toe. Zie [Logbestanden](../../../home/c-dataset-const-proc/c-log-proc-config-file/c-log-sources.md#concept-3d4fb817c057447d90f166b1183b461e).

1. Voltooi de parameter van de Wegen van het Logboek. Zie [Sensorbestanden](../../../home/c-dataset-const-proc/c-log-proc-config-file/c-log-sources.md#concept-b25f11c477b54032a15b6117b3bf9009), [Logbestanden](../../../home/c-dataset-const-proc/c-log-proc-config-file/c-log-sources.md#concept-3d4fb817c057447d90f166b1183b461e) of [XML-logbronnen](../../../home/c-dataset-const-proc/c-log-proc-config-file/c-log-sources.md#concept-c7b154e93748447b986e97f6ef688887). Geef een geldige URI op.

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
   <td colname="col2"> Naam die de externe bestandsserver identificeert. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Algemene naam SSL-server </td> 
   <td colname="col2"> <p> <span class="wintitle"> Server Common </span> Namelisted op het SSL-certificaat van de bestandsserver. </p> <p> Deze parameter is optioneel als <span class="wintitle"> SSL</span> gebruiken is ingesteld op false. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Adres </td> 
   <td colname="col2"> <p>Adres van de bestandsserver. Kan leeg worden gelaten als <span class="wintitle"> Naam</span> overeenkomt met <span class="wintitle"> Algemene naam SSL-server</span>. </p> <p> Bijvoorbeeld: <span class="filepath"> visual.mijnbedrijf.com</span> of 192.168.1.90. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Poort </td> 
   <td colname="col2"> Poort waardoor de gegevenswerkbankservercomputer communiceert met de bestandsserver. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> SSL-clientcertificaat </td> 
   <td colname="col2"> Naam van het <span class="wintitle"> SSL-certificaat</span>-bestand voor de gegevensworkbench-server (<span class="filepath"> server_cert.pem</span>). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> SSL gebruiken </td> 
   <td colname="col2"> Waar of onwaar. True geeft aan dat de bestandsserver <span class="wintitle"> SSL</span> gebruikt. </td> 
  </tr> 
 </tbody> 
</table>

Als een volmachtsserver voor DPUs wordt vereist om met FSU te verbinden, moet u de volgende parameters voltooien:

| Parameter | Beschrijving |
|---|---|
| Proxyadres | Het adres van een proxyserver die de gegevenswerkbankserver moet gebruiken om toegang te krijgen tot de bestandsserver. |
| Proxywachtwoord | Optioneel. Het wachtwoord voor de proxyserver. |
| Proxypoort | De poort van de proxyserver. De standaardwaarde is 8080. |
| Gebruikersnaam proxy | Optioneel. De gebruikersnaam voor de proxyserver. |

Hieronder ziet u een voorbeeld van een gedefinieerde [!DNL Log Server] in het bestand [!DNL Log Processing.cfg]. Logbron #1 is een LogFile-bron die verwijst naar een map met de naam Logs (let op de URI die is opgegeven in de parameter Log Paths) op de computer met de naam FSU01.

![](assets/cfg_LogProcessing_LogServer.png)

## Bewerkingen in de eenheid Bestandsserver {#section-b4a54b591b4e4435a728a67f194057ef}

In het vorige proces, vormde u een profiel voor een bepaalde dataset om logboekdossiers van FSU te lezen. Nu moet u de toestemmingen op FSU uitgeven om verbindingen van DPUs toe te staan die het profiel in werking stellen. In de volgende stappen wordt het bewerken van het machtigingenbestand [!DNL Access Control.cfg] doorlopen.

**Machtigingen bewerken op de FSU**

1. Open [!DNL Server Files Manager] voor de gegevenswerkbankservermachine die u als FSU plaatst en klik **[!UICONTROL Access Control]** om zijn inhoud te tonen.

   Voor informatie over het openen en het werken met [!DNL Server Files Manager], zie *de Gids van de Gebruiker van de Data Workbench*.

1. Klik in het venster [!DNL Server Files Manager] op **[!UICONTROL Access Control]** om de inhoud ervan weer te geven. Het [!DNL Access Control.cfg]-bestand bevindt zich in deze map.

1. Klik met de rechtermuisknop op het vinkje in de kolom Servernaam voor [!DNL Access Control.cfg] en klik vervolgens op **[!UICONTROL Make Local]**. In de kolom [!DNL Temp] wordt een vinkje weergegeven voor [!DNL Access Control.cfg].

1. Klik met de rechtermuisknop op het nieuwe vinkje onder de kolom [!DNL Temp] en klik op **[!UICONTROL Open]** > **[!UICONTROL in Workstation]**.

1. Klik in het venster [!DNL Access Control] op **[!UICONTROL Access Control Groups]** om de inhoud ervan weer te geven.

1. Klik met de rechtermuisknop op het numerieke label voor het laatste [!DNL AccessGroup] in de lijst en klik op **[!UICONTROL Add new]** > **[!UICONTROL Group]**.

1. Voer een [!DNL Name] in voor de nieuwe [!DNL AccessGroup]. Voorbeeld: Servers aansluiten.

1. Klik met de rechtermuisknop **[!UICONTROL Member]** onder het nieuwe [!DNL AccessGroup] en klik vervolgens op **[!UICONTROL Add new]** > **[!UICONTROL Member]**.

1. Ga het IP adres voor DPU van de server van de gegevenswerkbank in die met deze dossierserver verbindt.
1. Herhaal stap 4 en 5 voor andere DPU&#39;s van de server van de gegevenswerkbank die met dit FSU, met inbegrip van de serverDPUs van de gegevenswerkbank in een cluster verbinden die tot de logboekdossiers moet toegang hebben.
1. Klik met de rechtermuisknop **[!UICONTROL Read-Only Access]** onder het nieuwe [!DNL AccessGroup] en klik vervolgens op **[!UICONTROL Add new]** > **[!UICONTROL URI]**.

1. Voer de locatie van de opgeslagen logbestanden op de bestandsserver in. Gebruik slashes (/) in de padspecificatie. De standaardlocatie is /Logs/.
1. Klik met de rechtermuisknop **[!UICONTROL (modified)]** boven in het venster en klik vervolgens op **[!UICONTROL Save]**.

1. Klik in het venster [!DNL Server Files Manager] met de rechtermuisknop op het vinkje voor [!DNL Access Control.cfg] in de kolom [!DNL Temp] en klik vervolgens op **[!UICONTROL Save to]** > **[!UICONTROL server name]** om de lokaal aangebrachte wijzigingen in de FSU van de gegevenswerkbench-server op te slaan.

## De locatie van de logbestanden opgeven {#section-f9a649bf1b2544feb10ad8820384edb0}

U moet het [!DNL Communications.cfg] dossier op FSU uitgeven om de plaats van de logboekdossiers te specificeren.

**De locatie van de logbestanden opgeven**

1. Klik in het venster [!DNL Server Files Manager] op **[!UICONTROL Components]** om de inhoud ervan weer te geven. Het [!DNL Communications.cfg]-bestand bevindt zich in deze map.

1. Klik met de rechtermuisknop op het vinkje in de kolom Servernaam voor [!DNL Communications.cfg] en klik vervolgens op **[!UICONTROL Make Local]**. In de kolom [!DNL Temp] wordt een vinkje weergegeven voor [!DNL Communications.cfg].

1. Klik met de rechtermuisknop op het nieuwe vinkje onder de kolom [!DNL Temp] en klik op **[!UICONTROL Open]** > **[!UICONTROL in Workstation.]**.

1. Klik in het venster [!DNL Communications.cfg] op **[!UICONTROL component]** om de inhoud ervan weer te geven.

1. Klik in het venster [!DNL Communications.cfg] op **[!UICONTROL Servers]** om de inhoud ervan weer te geven. Er kunnen verschillende servers worden weergegeven: Bestandsservers, Logging Servers, Init Servers, Statusservers, Send Servers of Replicate Servers.

1. (Alleen voor [!DNL Sensor] logbronnen) Zoek [!DNL LoggingServer]. In deze map schrijft [!DNL Sensor] de logbestanden die door de gegevenswerkbankserver moeten worden verwerkt. Klik vervolgens op het nummer om het menu weer te geven. Geef de parameter van de Folder van het Logboek uit om op de gewenste plaats van de logboekdossiers te wijzen. De standaardlogmap is de map Logs in de installatiemap van de gegevenswerkbankserver.

   Wijzig geen andere parameters voor [!DNL LoggingServer].

   ![](assets/cfg_Communications_LoggingServer.png)

1. Zoek naar FileServer die de plaats van logboekdossiers specificeert. Onder Servers kunnen meerdere bestandsservers worden vermeld, zodat u de inhoud voor veel van deze servers (door op het servernummer te klikken) mogelijk moet bekijken om de gewenste server te vinden.
1. Bewerk de parameters [!DNL Local Path] en URI voor de FileServer om de locatie van de logbestanden te weerspiegelen. In het volgende voorbeeld wordt getoond dat de logbestanden zich in de map Logs in de installatiemap van de gegevenswerkbankserver bevinden:

   ![](assets/cfg_Communications_FS.png)

   >[!NOTE]
   >
   >Als de parameters [!DNL Local Path] en URI worden gevuld, zoals getoond, kunt u tot de logboekdossiers op FSU van om het even welke server van de gegevenswerkbank toegang hebben door [!DNL Logs] in [!DNL Server Files Manager] te klikken.

1. Klik **[!UICONTROL (modified)]** bij de bovenkant van het configuratievenster met de rechtermuisknop aan, dan klik **[!UICONTROL Save]**.

1. Klik in het venster [!DNL Server Files Manager] met de rechtermuisknop op het vinkje voor [!DNL Communications.cfg] in de kolom [!DNL Temp] en klik vervolgens op **[!UICONTROL Save to]** > *&lt;**[!UICONTROL server name]**>* om de lokaal aangebrachte wijzigingen in de FSU van de gegevenswerkbench-server op te slaan.

## Een gecentraliseerde normalisatieserver maken voor een cluster {#section-2c1f57b683f94cc193bc069e886bba28}

Als u uw gegevenssetprofiel om op een cluster van de gegevenswerkbankserver vormt te lopen, dan zou u FSU van de cluster de server moeten maken waar alle afmetingen van het profiel worden geconstrueerd.

Adobe raadt ten zeerste aan dat de FSU van het cluster fungeert als de master server van het cluster en de gecentraliseerde normalisatieserver.

Als u van de FSU de gecentraliseerde normalisatieserver wilt maken, moet u de [!DNL Communications.cfg]- en [!DNL Cluster.cfg]-bestanden op de FSU openen en bewerken.

**De FSU tot de gecentraliseerde normalisatieserver maken**

1. Voeg een [!DNL NormalizeServer] ingang aan het [!DNL Communications.cfg] dossier op FSU toe.

   >[!NOTE]
   >
   >Als u het volledige releasepakket voor gegevenswerkbankserver v5.0 of hoger hebt geïnstalleerd, moet het [!DNL Communications.cfg]-bestand op uw FSU al een [!DNL NormalizeServer]-item hebben. U kunt de onderstaande stappen volgen om te bevestigen dat de invoer bestaat.

   1. Open het [!DNL Communications.cfg] dossier in gegevenswerkbank zoals die in [wordt beschreven het Specificeren van de Plaats van de Dossiers van het Logboek](#section-f9a649bf1b2544feb10ad8820384edb0).

   1. Klik **[!UICONTROL component]** om de inhoud ervan weer te geven.
   1. Klik met de rechtermuisknop **[!UICONTROL Servers]** en klik **[!UICONTROL Add New]** > **[!UICONTROL Centralized Normalization Server]**.

   1. Typ [!DNL /Cluster/] in de URI-parameter voor [!DNL NormalizeServer].

      ![](assets/cfg_Communications_NormalizeServer.png)

   1. Klik met de rechtermuisknop **[!UICONTROL (modified)]** boven in het venster en klik **[!UICONTROL Save]**.

   1. Klik in het venster [!DNL Server Files Manager] met de rechtermuisknop op het vinkje voor [!DNL Communications.cfg] in de kolom [!DNL Temp] en klik vervolgens op **[!UICONTROL Save to]** > *&lt;**[!UICONTROL server]***> om de lokaal aangebrachte wijzigingen in de FSU van de gegevenswerkbench-server op te slaan.

1. Definieer de gecentraliseerde normalisatieserver in het [!DNL Cluster.cfg]-bestand op de master server in de servercluster van de gegevenswerkbank.

   >[!NOTE]
   >
   >Als de FSU waarop u uw gecentraliseerde normalisatieserver plaatst niet de master server van de gegevenswerkbank in uw cluster is, moet u de IP adressen van DPUs in de cluster aan [!DNL Cluster Servers] toegangsgroep in het [!DNL Access Control.cfg] dossier van FSU toevoegen. Voor instructies om servers aan de [!DNL Cluster Servers] groep toe te voegen, zie het Bijwerken van het Dossier van de Controle van de Toegang voor een sectie van de Cluster in de *Gids van de Installatie en van het Beleid van de Producten van de Server*.

   1. Open [!DNL Profile Manager] binnen uw datasetprofiel, dan klik **[!UICONTROL Dataset]** om zijn inhoud te tonen. Het [!DNL Cluster.cfg]-bestand bevindt zich in deze map.

   1. Klik met de rechtermuisknop op het vinkje naast [!DNL Cluster.cfg] en klik vervolgens op **[!UICONTROL Make Local]**. Er wordt een vinkje voor dit bestand weergegeven in de kolom [!DNL User].

   1. Klik met de rechtermuisknop op het nieuwe vinkje en klik op **[!UICONTROL Open]** > **[!UICONTROL in Notepad]**.

   1. Voeg de tekst toe die is gemarkeerd in het volgende bestandsfragment:

      [!DNL Cluster = ClusterConfig:]

      [!DNL Normalize Server = serverInfo:]

      [!DNL Address = string:]

      [!DNL Port = int: 80]

      [!DNL SSL Server Common Name = string: server common name]

      [!DNL Use SSL = bool: false]

      >[!NOTE]
      >
      >Wanneer u de gemeenschappelijke naam van FSU voor de SSL parameter van de Naam van de Server Gemeenschappelijke gebruikt, gebruikt FSU zijn [!DNL .address] dossier om de gemeenschappelijke naam op te lossen. Voor informatie over het [!DNL .address] dossier, zie *de Gids van de Installatie en van het Beleid van de Producten van de Server*.

   1. Sla het bestand op.
   1. Klik in [!DNL Profile Manager] met de rechtermuisknop op het vinkje voor [!DNL Cluster.cfg] in de kolom [!DNL User] en klik vervolgens op **[!UICONTROL Save to]** > ***[!UICONTROL dataset profile name]*** om de lokaal aangebrachte wijzigingen in het gegevenssetprofiel op te slaan.
