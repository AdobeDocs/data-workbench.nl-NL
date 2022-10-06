---
description: De profielen en raadplegingsdossiers die Adobe voor uw bepaalde toepassing heeft ontwikkeld zijn interne profielen die de metriek, de afmetingen, en de werkruimten verstrekken die de analyse van uw dataset toelaten.
title: Profielen en opzoekbestanden installeren
uuid: edc670a6-ebc9-4a20-a66f-81dd4adf7433
exl-id: bf9a3bca-e849-47b6-b038-0349f8ec334a
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '528'
ht-degree: 0%

---

# Profielen en opzoekbestanden installeren{#installing-profiles-and-lookup-files}

{{eol}}

De profielen en raadplegingsdossiers die Adobe voor uw bepaalde toepassing heeft ontwikkeld zijn interne profielen die de metriek, de afmetingen, en de werkruimten verstrekken die de analyse van uw dataset toelaten.

Net als bij alle andere interne profielen die door Adobe worden geleverd, mogen deze profielen niet worden gewijzigd. Alle aanpassing moet in uw dataset of rol-specifieke profielen of andere profielen voorkomen die u creeert.

Adobe verspreidt het profiel en de raadplegingsdossiers voor uw toepassing als [!DNL .zip] bestand. Elk ZIP-bestand krijgt een naam voor de toepassing waarvan het profiel en de opzoekbestanden in het bestand staan. (Bijvoorbeeld: [!DNL Site52.zip] bevat de profielbestanden voor Site v5.2.) De [!DNL .zip] bestand bevat twee mappen ( [!DNL Lookups] en [!DNL Profiles]).

>[!NOTE]
>
>Als u nog geen installatiebestand hebt dat de profielen en opzoekbestanden voor uw toepassing bevat, downloadt u deze van de FTP-site Adobe voordat u begint.

U moet het profiel en de opzoekbestanden installeren op het tabblad [!DNL Insight Server] computer waarop u uw gegevenssetprofiel verwerkt en uitvoert. Als u een [!DNL Insight Server] , moet u de bestanden op de master server installeren. Voor informatie over datasetprofielen, zie *Configuratie-handleiding voor gegevensset*.

**Profielen voor uw Adobe-toepassing installeren**

1. Open de [!DNL Profiles] uit de [!DNL .zip] bestand dat door Adobe aan u wordt geleverd.

1. Alle mappen in de [!DNL Profiles] in de [!DNL .zip] aan de [!DNL Profiles] in uw [!DNL Insight Server] installatiemap. U wilt eindigen met [!DNL ...\Profielen\]*&lt; [!DNL internal profile name]>* mappen op uw [!DNL Insight Server] zoals getoond in het volgende voorbeeld. De werkelijke profielnamen kunnen afwijken.

   ![](assets/win_installprofiles.png)

1. Ga naar de  [!DNL Profiles\]*&lt; [!DNL dataset profile name]>* map in de map waarin u hebt geïnstalleerd [!DNL Insight Server] en zoek de [!DNL profile.cfg] in deze map.

   >[!NOTE]
   >
   >Als u profielen voor de eerste keer installeert, kunt u het verstrekte profiel van de Steekproef als uw datasetprofiel gebruiken. U kunt de [!DNL profile.cfg] bestand (mogelijk een naam zoals [!DNL profile.cfg.offline]) voor het monsterprofiel in het dialoogvenster [!DNL Profiles\Sample] in uw [!DNL Insight Server] installatiemap.

1. Open de [!DNL profile.cfg] het dossier gebruikend een tekstredacteur zoals Blocnote en doe het volgende:

   1. Voeg items toe voor de interne profielen in de vector Directory&#39;s. De profielnamen komen overeen met de namen van de mappen die u naar de [!DNL Profiles] map op de [!DNL Insight Server] machine.

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
      >De *serverCommonName* die u opgeeft voor de algemene naam in het dialoogvenster [!DNL profile.cfg] bestand komt overeen met de gemeenschappelijke servernaam voor het [!DNL Insight Server] computer waarop u het gegevenssetprofiel verwerkt en uitvoert. Voor instructies om bij te werken [!DNL profile.cfg] zodat het gegevenssetprofiel op een [!DNL Insight Server] cluster, zie [Insight Server Clusters](../../../../home/c-inst-svr/c-install-ins-svr/c-ins-svr-clstrs/c-abt-ins-svr-clsters.md).

1. Sla het bestand op. Sla het bestand op als [!DNL profile.cfg] als er een andere naam voor is opgegeven.

**De opzoekbestanden voor uw Adobe-toepassing installeren**

1. Open de [!DNL Lookups] uit de [!DNL .zip] bestand dat door Adobe aan u wordt geleverd.

1. Alle mappen in de [!DNL Lookups] in de [!DNL .zip] aan de [!DNL Lookups] in uw [!DNL Insight Server] installatiemap. U wilt eindigen met [!DNL ...\Lookups\]*&lt; [!DNL internal profile name]>* mappen op uw [!DNL Insight Server] zoals getoond in het volgende voorbeeld. De werkelijke profielnamen kunnen afwijken.

   ![](assets/win_installLookups.png)
