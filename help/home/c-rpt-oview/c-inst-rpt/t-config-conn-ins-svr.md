---
description: Alvorens u rapporten en alarm kunt produceren, moet u de Server van het Rapport vormen om het adres van de server van het Inzicht te specificeren en de profielen te identificeren dat u het waartegen wilt rapporteren.
solution: Analytics
title: Het vormen van de Verbinding aan de Server van het Inzicht
topic: Data workbench
uuid: 2018b67e-90a6-41d7-b628-4b463869df6e
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Het vormen van de Verbinding aan de Server van het Inzicht{#configuring-the-connection-to-the-insight-server}

Alvorens u rapporten en alarm kunt produceren, moet u de Server van het Rapport vormen om het adres van de server van het Inzicht te specificeren en de profielen te identificeren dat u het waartegen wilt rapporteren.

>[!NOTE]
>
>Tot u de Server van het Rapport zoals hieronder beschreven vormt, kunt u de Server van het Rapport niet met succes in werking stellen. Als u probeert om de Server van het Rapport met het niet-gevormde dossier in werking te stellen dat met het programma geïnstalleerd is, veroorzaakt de Server van het Rapport een stroom van fouten.

**Om de Server van het Rapport te vormen**

1. Met de Ontdekkingsreiziger van Vensters, navigeer aan de folder waar u de Server van het Rapport installeerde.
1. Open het [!DNL ReportServer.cfg] dossier in Blocnote en wijzig het dossier zoals gewenst.

   De volgende steekproef [!DNL Report Server.cfg] bevat slechts de parameters inbegrepen in het [!DNL Report Server.cfg] dossier door gebrek (en benadrukt de vereiste parametermontages). Als u de Server van de Vergunning van Adobe door een volmachtsserver contacteert, moet u de het Verlenen van vergunningen vector en zijn parameters toevoegen. Zie de parameters [van](../../../home/c-rpt-oview/c-rpt-param-ref/c-rpt-svr-param.md#concept-53359b328fd140d593c3f2fc0031be06) het Rapport Server.cfg voor een gedetailleerde beschrijving.

   ```
   Fonts = vector: 0 items
   Gamma = float: 1.6
   Network Location = string: NetworkLocationName
   Servers = vector: 1 items
     0 = serverInfo:
       Address = string: ServerIPAddress
       Name = string: 
       Port = int: 443
       Proxy Address = string:
       Proxy Password = string:
       Proxy Port = int: 8080
       Proxy User Name = string:
       SSL Client Certificate = string: ReportCertFileName.pem
       SSL Server Common Name = string: ServerCommonName
       Use SSL = bool: true
   Result Memory Limit (KB) = double: 100000
   Maximum Slice Size = int: 30
   Use OpenGL Hardware Rendering = bool: true
   Reporting = :
     Profiles = vector: 1 items
       0 = ReportProfile:
         Server = string: ServerCommonName
         Profile = string: ProfileName
     Update Interval (minutes) = int: 10
     Completion Message Interval (seconds) = int: 600
     Status interval (seconds) = int: 600
     SMTP Server for Errors = string: SMTPServerHostName
     SMTP Server for Errors Username = string: SMTPServerUsername
     SMTP Server for Errors Password = string: SMTPServerPassword
     SMTP Server for Errors Send From = string: SenderAddress
     SMTP Server for Errors Send To = string: RecipientAddresses
   ```

1. Sparen en sluit het dossier.
