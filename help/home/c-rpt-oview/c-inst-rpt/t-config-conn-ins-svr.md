---
description: Alvorens u rapporten en alarm kunt produceren, moet u de Server van het Rapport vormen om het adres van de server van het Inzicht te specificeren en de profielen te identificeren waarop u het wilt melden.
title: De verbinding met de Insight Server configureren
uuid: 2018b67e-90a6-41d7-b628-4b463869df6e
exl-id: a398a665-fe09-448a-977c-b0f9de4add09
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '195'
ht-degree: 0%

---

# De verbinding met de Insight Server configureren{#configuring-the-connection-to-the-insight-server}

{{eol}}

Alvorens u rapporten en alarm kunt produceren, moet u de Server van het Rapport vormen om het adres van de server van het Inzicht te specificeren en de profielen te identificeren waarop u het wilt melden.

>[!NOTE]
>
>Totdat u de Server van het Rapport zoals hieronder beschreven vormt, kunt u de Server van het Rapport niet met succes in werking stellen. Als u probeert om de Server van het Rapport met het niet-gevormde dossier in werking te stellen dat met het programma geïnstalleerd is, veroorzaakt de Server van het Rapport een stroom van fouten.

**Om de Server van het Rapport te vormen**

1. Met de Ontdekkingsreiziger van Vensters, navigeer aan de folder waar u de Server van het Rapport installeerde.
1. Open de [!DNL ReportServer.cfg] in Kladblok en wijzig het bestand naar wens.

   Het volgende voorbeeld [!DNL Report Server.cfg] bevat alleen de parameters die zijn opgenomen in de [!DNL Report Server.cfg] bestand standaard (en markeert de vereiste parameterinstellingen). Als u via een proxyserver contact opneemt met de Adobe-licentieserver, moet u de licentievector en de bijbehorende parameters toevoegen. Zie [De parameters van Server.cfg van het rapport](../../../home/c-rpt-oview/c-rpt-param-ref/c-rpt-svr-param.md#concept-53359b328fd140d593c3f2fc0031be06) voor een gedetailleerde beschrijving.

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

1. Sla het bestand op en sluit het.
