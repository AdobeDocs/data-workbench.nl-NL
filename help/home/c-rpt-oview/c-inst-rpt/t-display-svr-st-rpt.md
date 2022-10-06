---
description: De Gedetailleerde interface van de Status in gegevenswerkbank is nuttig voor het oplossen van problemenfouten of andere kwesties met de Server van de Data Workbench en de machines van de Server van het Rapport die cliënten van de Server van de Data Workbench zijn.
title: Status rapportserver weergeven
uuid: 5260266d-5bd1-4905-9619-f67f6e1bc54c
exl-id: 3a717a81-7c5d-432d-b214-4ae0455b19b5
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '198'
ht-degree: 0%

---

# Status rapportserver weergeven{#displaying-report-server-status}

{{eol}}

De Gedetailleerde interface van de Status in gegevenswerkbank is nuttig voor het oplossen van problemenfouten of andere kwesties met de Server van de Data Workbench en de machines van de Server van het Rapport die cliënten van de Server van de Data Workbench zijn.

De status van het rapport weergeven in het dialoogvenster [!DNL Master Server Detailed Status] interface, moet u een server van de rapportstatus aan toevoegen [!DNL Servers] vector in gegevenswerkbankserver [!DNL Communications.cfg] bestand. De volgende procedure beschrijft hoe te om de server van de rapportstatus aan toe te voegen [!DNL Communications.cfg] bestand:

Meer informatie over [!DNL Detailed Status] interfaces, zie het Administratieve hoofdstuk van Interfaces van *Gebruikershandleiding voor Data Workbench*.

**Als u een[!DNL Report Status Server]**

1. Navigeer naar de omslag van Componenten in de folder waar u de server van de gegevenswerkbank (InsightServer64.exe.) installeerde

   Voorbeeld: [!DNL C:\Adobe\Server\Components]
1. Openen [!DNL Communications.cfg] in een teksteditor zoals Kladblok.
1. Zoek de [!DNL Servers] en voeg de rapportstatusserver toe aan deze vector zoals gemarkeerd in het volgende bestandsfragment.

   ```
    . . .
   Servers = vector: 17 items
       0 = FileServer: 
         Local Path = string: Audit\\
         URI = string: /Audit
       1 = FileServer: 
         Local Path = string: Bin\\
         URI = string: /Bin
       2 = FileServer: 
         Local Path = string: Components\\
         URI = string: /Components
     . . .
       16 = ReportStatusServer: 
         URI = string: /ReportStatus.vsp
   ```

1. Hiermee werkt u het aantal items voor de [!DNL Servers] Vector (dat wil zeggen, verhoog de itemwaarde met één), zoals in de vorige stap is gemarkeerd in het bestandsfragment.
1. Sla het bestand op.
