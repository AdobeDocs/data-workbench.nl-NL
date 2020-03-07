---
description: De profielen en de raadplegingsdossiers die Adobe voor uw bijzondere toepassing heeft ontwikkeld zijn interne profielen die de metriek, de afmetingen, en de werkruimten verstrekken die de analyse van uw dataset toelaten.
solution: Insight
title: Profielen en bestanden zoeken installeren
uuid: edc670a6-ebc9-4a20-a66f-81dd4adf7433
translation-type: tm+mt
source-git-commit: 27600561841db3705f4eee6ff0aeb8890444bbc9

---


# Profielen en bestanden zoeken installeren{#installing-profiles-and-lookup-files}

De profielen en de raadplegingsdossiers die Adobe voor uw bijzondere toepassing heeft ontwikkeld zijn interne profielen die de metriek, de afmetingen, en de werkruimten verstrekken die de analyse van uw dataset toelaten.

Zoals met alle andere interne profielen die door Adobe worden verstrekt, zouden deze profielen niet moeten worden veranderd. Al aanpassing moet in uw dataset of rol-specifieke profielen of andere profielen voorkomen die u creeert.

Adobe verdeelt de profiel en raadplegingsdossiers voor uw toepassing als [!DNL .zip] dossier. Elk pitdossier wordt genoemd voor de toepassing waarvan profiel en raadplegingsdossiers die het bevat. (Bijvoorbeeld, [!DNL Site52.zip] bevat de profieldossiers voor Plaats v5.2.) Het [!DNL .zip] dossier bevat twee omslagen ( [!DNL Lookups] en [!DNL Profiles]).

>[!NOTE]
>
>Als u reeds niet het installatiedossier hebt dat de profielen en de raadplegingsdossiers voor uw toepassing bevat, download hen van de plaats van FTP van Adobe alvorens u begint.

U moet het profiel en zijn raadplegingsdossiers op de [!DNL Insight Server] machine installeren waarop u verwerkt en uw datasetprofiel in werking stelt. Als u een [!DNL Insight Server] cluster in werking stelt, moet u de dossiers op de hoofdserver installeren. Voor informatie over datasetprofielen, zie de Gids *van de Configuratie van de* Dataset.

**Om profielen voor uw toepassing van Adobe te installeren**

1. Open de [!DNL Profiles] omslag van het [!DNL .zip] dossier dat aan u door Adobe wordt verstrekt.

1. Kopieer alle omslagen binnen de [!DNL Profiles] omslag in het [!DNL .zip] dossier aan de [!DNL Profiles] omslag in uw [!DNL Insight Server] installatiefolder. Je wilt eindigen met [!DNL ...\Profiles\]*&lt;[!DNL internal profile name]>* mappen op uw [!DNL Insight Server] zoals in het volgende voorbeeld wordt getoond. De werkelijke profielnamen kunnen afwijken.

   ![](assets/win_installprofiles.png)

1. Blader naar de map [!DNL-profielen\]*&lt;[!DNL dataset profile name]>* in de directory waarin u het bestand hebt geïnstalleerd [!DNL Insight Server] en zoek het [!DNL profile.cfg] bestand in deze directory.

   >[!NOTE]
   >
   >Als u profielen voor het eerst installeert, kunt u het verstrekte profiel van de Steekproef als uw datasetprofiel gebruiken. U kunt het [!DNL profile.cfg] dossier (het zou iets als [!DNL profile.cfg.offline]) voor het profiel van de Steekproef binnen de [!DNL Profiles\Sample] omslag in uw [!DNL Insight Server] installatiefolder kunnen worden genoemd.

1. Open het [!DNL profile.cfg] dossier gebruikend een tekstredacteur zoals Blocnote en doe het volgende:

   1. Voeg ingangen voor de interne profielen in de vector van Folders toe. De profielnamen beantwoorden aan de namen van de folders die u aan de [!DNL Profiles] omslag op de [!DNL Insight Server] machine kopieerde.

   1. Werk het aantal folders bij zoals aangewezen.
   1. Voeg de gemeenschappelijke naam van de server aan de Gemeenschappelijke lijn van de Naam in dit dossier toe, zoals hieronder benadrukt:

      ```
      Profile = profileInfo: 
      Directories = vector: n+1 items
        0 = string: Base\\
        1 = string: internal profile name 1\\
        2 = string: internal profile name 2\\
      . . .
        n = string: internal profile name n\\
      Processing Servers = vector: 1 items
        0 = ProfileServerInfo: 
          Common Name = string: serverCommonName
          Server = string: 
      ```

      >[!NOTE]
      >
      >De *serverCommonName* die u voor de Gemeenschappelijke Naam in het [!DNL profile.cfg] dossier specificeert beantwoordt de server gemeenschappelijke naam voor de [!DNL Insight Server] machine waarop u verwerkt en het datasetprofiel in werking stelt. Voor instructies om bij te werken [!DNL profile.cfg] zodat de looppas van het datasetprofiel op een [!DNL Insight Server] cluster, zie de Clusters van de Server van het [Inzicht](../../../../home/c-inst-svr/c-install-ins-svr/c-ins-svr-clstrs/c-abt-ins-svr-clsters.md).

1. Sla het bestand op. Ben zeker om het dossier op te slaan alsof [!DNL profile.cfg] het verschillend werd genoemd.

**Om de raadplegingsdossiers voor uw toepassing van Adobe te installeren**

1. Open de [!DNL Lookups] omslag van het [!DNL .zip] dossier dat aan u door Adobe wordt verstrekt.

1. Kopieer alle omslagen binnen de [!DNL Lookups] omslag in het [!DNL .zip] dossier aan de [!DNL Lookups] omslag in uw [!DNL Insight Server] installatiefolder. Je wilt eindigen met [!DNL ...\Lookups\]*&lt;[!DNL internal profile name]>* mappen op uw [!DNL Insight Server] zoals in het volgende voorbeeld wordt getoond. De werkelijke profielnamen kunnen afwijken.

   ![](assets/win_installLookups.png)

