---
description: Voor alle talen, vereist Server 6.0 van het Rapport en later het "inzicht.zbin"dossier dat aan de de wortelomslag van de Server van het Rapport wordt gekopieerd.
title: Rapportserver bijwerken met een taalbestand (.zbin-bestand)
uuid: 2ecf2afc-bb5f-4fc7-8fb8-a904fb7ed407
exl-id: a76b7c01-83f0-4cf2-97a9-07d51cc75b3c
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '186'
ht-degree: 0%

---

# Rapportserver bijwerken met een taalbestand (.zbin-bestand){#update-report-server-with-a-language-file-zbin-file}

{{eol}}

Voor alle talen, vereist Server 6.0 van het Rapport en later het &quot;inzicht.zbin&quot;dossier dat aan de de wortelomslag van de Server van het Rapport wordt gekopieerd.

Werk de de taaldossiers van de Server van het Rapport bij:

1. Voeg het anders genoemde &quot;inzicht.zbin&quot;dossier aan de folder van root ReportServer toe.
1. Voor het configuratiebestand Report Server (reportServer.cfg) zijn fontinstellingen voor double-bytetalen vereist. Chinees vereist bijvoorbeeld de toevoeging van lettertypen met SimSun:

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

   Volg de stappen om ReportServer als dienst met de parameters van de Landinstelling te lanceren:

   1. Start een opdrachtprompt als beheerder.
   1. Navigeer naar de installatiemap van ReportServer.
   1. Typ het volgende bevel om de dienst te beginnen:

      * Voor het Engels: [!DNL ReportServer.exe -RegServer -Locale -en-us]
      * Voor Chinees: [!DNL ReportServer.exe -RegServer -Locale -zh-cn]

1. Om te verifiëren als ReportServer met de correcte parameters loopt:

   1. Open Windows Service Manager.
   1. Klik met de rechtermuisknop [!DNL Adobe Insight Report Server - Properties].

   Het pad naar het uitvoerbare bestand bevat de parameters:

   ```
   ReportServer.exe -Service ReportServer -Locale -en-us
   ```
