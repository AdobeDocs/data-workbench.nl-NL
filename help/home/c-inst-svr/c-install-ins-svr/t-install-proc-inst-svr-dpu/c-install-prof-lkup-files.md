---
description: De profielen en raadplegingsdossiers die Adobe voor uw bepaalde toepassing heeft ontwikkeld zijn interne profielen die de metriek, de afmetingen, en de werkruimten verstrekken die de analyse van uw dataset toelaten.
solution: Analytics
title: Profielen en opzoekbestanden installeren
uuid: edc670a6-ebc9-4a20-a66f-81dd4adf7433
translation-type: tm+mt
source-git-commit: 34cdcfc83ae6bb620706db37228e200cff43ab2c
workflow-type: tm+mt
source-wordcount: '524'
ht-degree: 0%

---


# Profielen en opzoekbestanden installeren{#installing-profiles-and-lookup-files}

De profielen en raadplegingsdossiers die Adobe voor uw bepaalde toepassing heeft ontwikkeld zijn interne profielen die de metriek, de afmetingen, en de werkruimten verstrekken die de analyse van uw dataset toelaten.

Net als bij alle andere interne profielen die door Adobe worden geleverd, mogen deze profielen niet worden gewijzigd. Alle aanpassing moet in uw dataset of rol-specifieke profielen of andere profielen voorkomen die u creeert.

Adobe verspreidt het profiel en de raadplegingsdossiers voor uw toepassing als [!DNL .zip] dossier. Elk ZIP-bestand krijgt een naam voor de toepassing waarvan het profiel en de opzoekbestanden in het bestand staan. (Bevat bijvoorbeeld [!DNL Site52.zip] de profielbestanden voor Site v5.2.) Het [!DNL .zip] bestand bevat twee mappen ( [!DNL Lookups] en [!DNL Profiles]).

>[!NOTE]
>
>Als u nog geen installatiebestand hebt dat de profielen en opzoekbestanden voor uw toepassing bevat, downloadt u deze van de FTP-site Adobe voordat u begint.

U moet het profiel en zijn raadplegingsdossiers op de [!DNL Insight Server] machine installeren waarop u verwerkt en uw profiel van de dataset in werking stelt. Als u een [!DNL Insight Server] cluster uitvoert, moet u de bestanden op de master server installeren. Voor informatie over datasetprofielen, zie de Gids *van de Configuratie van de* Dataset.

**Profielen voor uw Adobe-toepassing installeren**

1. Open de [!DNL Profiles] map vanuit het [!DNL .zip] bestand dat u van Adobe hebt ontvangen.

1. Kopieer alle mappen in de [!DNL Profiles] map in het [!DNL .zip] bestand naar de [!DNL Profiles] map in de [!DNL Insight Server] installatiemap. U wilt uitkomen met  [!DNL ...\Profiles\]*&lt;[!DNL internal profile name]>* mappen op uw [!DNL Insight Server] computer, zoals in het volgende voorbeeld wordt getoond. De werkelijke profielnamen kunnen afwijken.

   ![](assets/win_installprofiles.png)

1. Navigeer naar de map  [!DNL Profiles\]*&lt;[!DNL dataset profile name]>* in de map waarin u hebt geïnstalleerd [!DNL Insight Server] en zoek het [!DNL profile.cfg] bestand in deze map.

   >[!NOTE]
   >
   >Als u profielen voor de eerste keer installeert, kunt u het verstrekte profiel van de Steekproef als uw datasetprofiel gebruiken. U kunt het [!DNL profile.cfg] bestand (het krijgt een naam zoals [!DNL profile.cfg.offline]) voor het voorbeeldprofiel in de [!DNL Profiles\Sample] map in de [!DNL Insight Server] installatiemap vinden.

1. Open het [!DNL profile.cfg] bestand met een teksteditor, zoals Kladblok, en voer de volgende handelingen uit:

   1. Voeg items toe voor de interne profielen in de vector Directory&#39;s. De profielnamen komen overeen met de namen van de directory&#39;s die u naar de [!DNL Profiles] map op de [!DNL Insight Server] computer hebt gekopieerd.

   1. Werk het aantal mappen naar wens bij.
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
      >De *serverCommonName* die u voor de Gemeenschappelijke Naam in het [!DNL profile.cfg] dossier specificeert beantwoordt de server gemeenschappelijke naam voor de [!DNL Insight Server] machine waarop u verwerkt en het gegevenssetprofiel in werking stelt. Voor instructies om bij te werken [!DNL profile.cfg] zodat het datasetprofiel op een [!DNL Insight Server] cluster loopt, zie de Clusters [van de Server van het](../../../../home/c-inst-svr/c-install-ins-svr/c-ins-svr-clstrs/c-abt-ins-svr-clsters.md)Inzicht.

1. Sla het bestand op. Sla het bestand op alsof de naam anders is [!DNL profile.cfg] .

**De opzoekbestanden voor uw Adobe-toepassing installeren**

1. Open de [!DNL Lookups] map vanuit het [!DNL .zip] bestand dat u van Adobe hebt ontvangen.

1. Kopieer alle mappen in de [!DNL Lookups] map in het [!DNL .zip] bestand naar de [!DNL Lookups] map in de [!DNL Insight Server] installatiemap. U wilt uitkomen met  [!DNL ...\Lookups\]*&lt;[!DNL internal profile name]>* mappen op uw [!DNL Insight Server] computer, zoals in het volgende voorbeeld wordt getoond. De werkelijke profielnamen kunnen afwijken.

   ![](assets/win_installLookups.png)

