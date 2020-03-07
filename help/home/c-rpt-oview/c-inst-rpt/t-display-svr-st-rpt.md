---
description: De gedetailleerde interface van de Status in gegevenswerkbank is nuttig voor het oplossen van problemenfouten of andere kwesties met de Server van de Werkbank van Gegevens en de machines van de Server van het Rapport die cliënten van de Server van de Werkbank van Gegevens zijn.
solution: Analytics
title: Status rapportserver weergeven
topic: Data workbench
uuid: 5260266d-5bd1-4905-9619-f67f6e1bc54c
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Status rapportserver weergeven{#displaying-report-server-status}

De gedetailleerde interface van de Status in gegevenswerkbank is nuttig voor het oplossen van problemenfouten of andere kwesties met de Server van de Werkbank van Gegevens en de machines van de Server van het Rapport die cliënten van de Server van de Werkbank van Gegevens zijn.

Om de status van het Rapport in de [!DNL Master Server Detailed Status] interface te bekijken, moet u een server van de rapportstatus aan de [!DNL Servers] vector in het [!DNL Communications.cfg] dossier van de server van de gegevenswerkbank toevoegen. De volgende procedure beschrijft hoe te om de server van de rapportstatus aan het [!DNL Communications.cfg] dossier toe te voegen:

Voor meer informatie over [!DNL Detailed Status] interfaces, zie het Administratieve hoofdstuk van Interfaces van de Gids *van de Gebruiker van de Werkbank van* Gegevens.

**Om een[!DNL Report Status Server]**

1. Navigeer aan de omslag van Componenten in de folder waar u de server van de gegevenswerkbank (InsightServer64.exe.) installeerde

   Voorbeeld: [!DNL C:\Adobe\Server\Components]
1. Open [!DNL Communications.cfg] in een tekstredacteur zoals Blocnote.
1. Bepaal de plaats van de [!DNL Servers] vector en voeg de server van de rapportstatus aan deze vector toe zoals die in het volgende dossierfragment wordt benadrukt.

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

1. Werk de punttelling voor de [!DNL Servers] vector (namelijk toename de puntwaarde door één) bij zoals benadrukt in het dossierfragment in de vorige stap.
1. Sla het bestand op.
