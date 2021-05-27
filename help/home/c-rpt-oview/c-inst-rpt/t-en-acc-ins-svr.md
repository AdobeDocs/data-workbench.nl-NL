---
description: Om met een server van de gegevenswerkbank te verbinden, moet de Server van het Rapport toestemming hebben om tot die server toegang te hebben.
title: Toegang tot de server van de Data Workbench inschakelen
uuid: e112ac2a-34fe-40a2-9324-262f5cb1f681
exl-id: bf409413-470e-4e05-9bd2-b5b511bbe4a5
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '283'
ht-degree: 0%

---

# Toegang tot de server van de Data Workbench inschakelen{#enabling-access-to-the-data-workbench-server}

Om met een server van de gegevenswerkbank te verbinden, moet de Server van het Rapport toestemming hebben om tot die server toegang te hebben.

U verleent toegang tot een server van de gegevenswerkbank door de gemeenschappelijke naam van de Server van het Rapport (zoals die op het digitale certificaat van de Server van het Rapport wordt toegewezen) aan het de toegangsbeheerdossier van de server toe te voegen.

>[!NOTE]
>
>Wanneer het werken in een gegroepeerd milieu, zou de Server van het Rapport moeten worden gevormd om tot de master server van de gegevenswerkbank toegang te hebben om synchronisatiekwesties te vermijden. In de werkbank voor gegevens kunt u informatie bekijken over het verwerken van servers in uw cluster met de menuoptie [!DNL Related Servers] in [!DNL Servers Manager]. Voor meer informatie over [!DNL Servers Manager], zie het Administratieve hoofdstuk van Interfaces van *de Gids van de Gebruiker van de Data Workbench*.

De volgende procedure beschrijft hoe te om de Server van het Rapport aan het dossier van de toegangscontrole op een server van de gegevenswerkbank manueel toe te voegen. Als u het toegangsbeheerbestand op deze manier wilt bijwerken, moet u toegang hebben tot het bestandssysteem op de computer waarop de gegevenswerkbankserver is geïnstalleerd.

U kunt het toegangsbeheerbestand van de server ook bijwerken met behulp van [!DNL Server Files Manager] in de werkbank voor gegevens. Hiervoor moet de client van uw gegevenswerkbank over beheerdersrechten op de server beschikken.

Voor meer informatie over [!DNL Server Files Manager], zie het Administratieve hoofdstuk van Interfaces van *de Gids van de Gebruiker van de Data Workbench*.

**Om toegang tot een server van de gegevenswerkbank te vormen**

1. Navigeer naar de omslag van het Toegangsbeheer in de folder waar u de server van de gegevenswerkbank (InsightServer64.exe) installeerde.

   Voorbeeld: [!DNL C:\Adobe\Server\Access Control]

1. Open [!DNL Access Control.cfg] in een tekstredacteur zoals Blocnote.
1. Zoek de [!DNL Report Server AccessGroup] en voeg [!DNL Report Server’s] gemeenschappelijke naam aan deze groep toe zoals benadrukt in het volgende dossierfragment. (Typ de algemene naam exact zoals deze wordt weergegeven op het digitale certificaat [!DNL Report Server’s].)

   ```
   . . .
     5 = AccessGroup: 
       Members = vector: 1 items
         0 = string: CN: ReportCommonName
       Name = string: Report Server
       Read-Only Access = vector: 5 items
         0 = string: /Profiles/$
         1 = string: /Status/
         3 = string: /Software/
         4 = string: /Addresses/
         5 = string: /Users/$
       Read-Write Access = vector: 3 items
         0 = string: /Profiles/
         1 = string: /Users/%CN%/
         2 = string: /ReportStatus.vsp
      . . .
   ```

1. Sla het bestand op.
