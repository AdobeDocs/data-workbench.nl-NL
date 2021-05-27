---
description: De Gedetailleerde interface van de Status in gegevenswerkbank is nuttig voor het oplossen van problemenfouten of andere kwesties met de Server van de Data Workbench en de machines van de Server van het Rapport die cliënten van de Server van de Data Workbench zijn.
title: Status rapportserver weergeven
uuid: 5260266d-5bd1-4905-9619-f67f6e1bc54c
exl-id: 3a717a81-7c5d-432d-b214-4ae0455b19b5
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '198'
ht-degree: 0%

---

# De status van de rapportserver weergeven{#displaying-report-server-status}

De Gedetailleerde interface van de Status in gegevenswerkbank is nuttig voor het oplossen van problemenfouten of andere kwesties met de Server van de Data Workbench en de machines van de Server van het Rapport die cliënten van de Server van de Data Workbench zijn.

Als u de status van Rapport wilt weergeven in de [!DNL Master Server Detailed Status]-interface, moet u een rapportstatusserver toevoegen aan de [!DNL Servers]-vector in het [!DNL Communications.cfg]-bestand van de gegevenswerkbankserver. De volgende procedure beschrijft hoe te om de server van de rapportstatus aan het [!DNL Communications.cfg] dossier toe te voegen:

Voor meer informatie over [!DNL Detailed Status] interfaces, zie het Administratieve hoofdstuk van Interfaces van *de Gids van de Gebruiker van de Data Workbench*.

**Als u een[!DNL Report Status Server]**

1. Navigeer naar de omslag van Componenten in de folder waar u de server van de gegevenswerkbank (InsightServer64.exe.) installeerde

   Voorbeeld: [!DNL C:\Adobe\Server\Components]
1. Open [!DNL Communications.cfg] in een tekstredacteur zoals Blocnote.
1. Zoek de vector [!DNL Servers] en voeg de rapportstatusserver toe aan deze vector zoals gemarkeerd in het volgende bestandsfragment.

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

1. Werk het aantal items bij voor de [!DNL Servers]-vector (dat wil zeggen de itemwaarde met één verhogen), zoals in de vorige stap in het bestandsfragment is gemarkeerd.
1. Sla het bestand op.
