---
description: Voor alle talen, vereist Server 6.0 van het Rapport en later het "inzicht.zbin"dossier dat aan de de wortelomslag van de Server van het Rapport wordt gekopieerd.
solution: Analytics
title: De Server van het Rapport van de update met een taaldossier (.zbin dossier)
topic: Data workbench
uuid: 2ecf2afc-bb5f-4fc7-8fb8-a904fb7ed407
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# De Server van het Rapport van de update met een taaldossier (.zbin dossier){#update-report-server-with-a-language-file-zbin-file}

Voor alle talen, vereist Server 6.0 van het Rapport en later het &quot;inzicht.zbin&quot;dossier dat aan de de wortelomslag van de Server van het Rapport wordt gekopieerd.

Werk de de taaldossiers van de Server van het Rapport bij:

1. Voeg het anders genoemde &quot;inzicht.zbin&quot;dossier aan de folder van wortelReportServer toe.
1. Het de configuratiedossier van de Server van het Rapport (reportserver.cfg) vereist doopvontmontages voor dubbel-byte talen. Bijvoorbeeld, vereist het Chinees de toevoeging van doopvonten gebruikend SimSun:

   ```
   <b>Report Server.cfg - Add Fonts</b> 
   
   Fonts = vector: 2 items 
     0 = string: SimSun 
     1 = string: Arial
   ```

1. Een parameter voor Server 6.0 van het Rapport moet in de bevellijn voor localisatie worden overgegaan, bijvoorbeeld:

   ```
   ReportServer.exe -Locale -zh-cn 
   ReportServer.exe -Locale -en-us
   ```

   >[!NOTE]
   >
   >Als een scène niet wordt gespecificeerd, dan blijft de Server van het Rapport aan het Engels in gebreke.

   Volg de stappen om ReportServer als dienst met de parameters van de Scène te lanceren:

   1. Lanceer een Herinnering van het Bevel als Beheerder.
   1. Navigeer aan ReportServer installeert omslag.
   1. Typ het volgende bevel om de dienst te beginnen:

      * Voor het Engels: [!DNL ReportServer.exe -RegServer -Locale -en-us]
      * Voor Chinees: [!DNL ReportServer.exe -RegServer -Locale -zh-cn]

1. Om te verifiëren als ReportServer met de correcte parameters loopt:

   1. Open Windows Service Manager.
   1. Klik met de rechtermuisknop [!DNL Adobe Insight Report Server - Properties].
   De weg aan uitvoerbaar zal de parameters bevatten:

   ```
   ReportServer.exe -Service ReportServer -Locale -en-us
   ```

