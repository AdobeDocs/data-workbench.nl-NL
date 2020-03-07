---
description: Om met een server van de gegevenswerkbank te verbinden, moet de Server van het Rapport toestemming hebben om tot die server toegang te hebben.
solution: Analytics
title: Het toelaten van Toegang tot de Server van de Werkbank van Gegevens
topic: Data workbench
uuid: e112ac2a-34fe-40a2-9324-262f5cb1f681
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Het toelaten van Toegang tot de Server van de Werkbank van Gegevens{#enabling-access-to-the-data-workbench-server}

Om met een server van de gegevenswerkbank te verbinden, moet de Server van het Rapport toestemming hebben om tot die server toegang te hebben.

U verleent toegang tot een server van de gegevenswerkbank door de gemeenschappelijke naam van de Server van het Rapport (zoals die op het digitale certificaat van de Server van het Rapport wordt toegewezen) aan het de toegangsbeheerdossier van de server toe te voegen.

>[!NOTE]
>
>Wanneer het werken in een gegroepeerd milieu, zou de Server van het Rapport moeten worden gevormd om tot de hoofdserver van de gegevenswerkbank toegang te hebben om synchronisatiekwesties te vermijden. In de werkbank van gegevens kunt u informatie over verwerkingsservers in uw cluster bekijken gebruikend het [!DNL Related Servers] menupunt in het [!DNL Servers Manager]. Voor meer informatie over [!DNL Servers Manager], zie het Administratieve hoofdstuk van Interfaces van de Gids van de Gebruiker van de Werkbank van *Gegevens*.

De volgende procedure beschrijft hoe te om de Server van het Rapport aan het dossier van de toegangscontrole op een server van de gegevenswerkbank manueel toe te voegen. Om het toegangsbeheerdossier op deze manier bij te werken, moet u dossier-systeem toegang op de machine hebben waar de server van de gegevenswerkbank geïnstalleerd is.

U kunt het de toegangsbeheerdossier van de server ook bijwerken gebruikend [!DNL Server Files Manager] in gegevenswerkbank. Om dit te doen, moet uw cliënt van de gegevenswerkbank administratieve voorrechten op de server hebben.

Voor meer informatie over [!DNL Server Files Manager], zie het Administratieve hoofdstuk van Interfaces van de Gids van de Gebruiker van de Werkbank van *Gegevens*.

**Om toegang tot een server van de gegevenswerkbank te vormen**

1. Navigeer aan de omslag van het Toegangsbeheer in de folder waar u de server van de gegevenswerkbank (InsightServer64.exe) installeerde.

   Voorbeeld: [!DNL C:\Adobe\Server\Access Control]

1. Open [!DNL Access Control.cfg] in een tekstredacteur zoals Blocnote.
1. Bepaal de plaats van de [!DNL Report Server AccessGroup] en voeg [!DNL Report Server’s] gemeenschappelijke naam aan deze groep toe zoals die in het volgende dossierfragment wordt benadrukt. (Typ precies de gemeenschappelijke naam aangezien het op [!DNL Report Server’s] digitaal certificaat. verschijnt)

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
