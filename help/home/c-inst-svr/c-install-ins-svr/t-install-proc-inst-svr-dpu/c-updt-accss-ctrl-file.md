---
description: Het bestand Access Control.cfg beheert de toegang tot bepaalde functies in Insight Server.
title: Het Access Control-bestand bijwerken
uuid: f73651e5-6a8b-45fc-8f36-6751304dc53c
exl-id: 551758c1-f24b-49e6-ab6e-09979511e4f4
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '490'
ht-degree: 1%

---

# Het dossier van het Toegangsbeheer{#updating-the-access-control-file} bijwerken

Het bestand Access Control.cfg beheert de toegang tot bepaalde functies in Insight Server.

Het bepaalt entiteiten genoemd Accessgroups. Een AccessGroup identificeert een groep gebruikers die toestemming hebben om bepaalde eigenschappen van de server te gebruiken.

Voordat u met [!DNL Insight Server] met [!DNL Insight] kunt verbinden, moet u de Beheerders AccessGroup bijwerken om één van de [!DNL Insight] vergunningen te omvatten die Adobe aan uw organisatie heeft uitgegeven. This AccessGroup identificeert gebruikers die worden toegelaten om administratieve functies door [!DNL Insight] uit te voeren.

De volgende procedure beschrijft hoe te om een vergunning aan de Beheerders AccessGroup toe te voegen. Om deze taak te voltooien, moet u bepalen welke [!DNL Insight] vergunning administratieve voorrechten voor uw organisatie heeft. (Voor de eerste configuratie en configuratie volstaat het verlenen van administratieve bevoegdheden aan één licentie. U kunt later beheerrechten toekennen aan extra licenties.) U moet ook de &quot;algemene naam&quot; weten die aan deze licentie is toegewezen. Om deze waarde te verkrijgen, kunt u de licentiecertificaten voor uw account bekijken op [https://aap.adobe.com](https://aap.adobe.com).

Het doel van deze procedure is eenvoudig een vergunning gegeven exemplaar van [!DNL Insight] te identificeren dat u kunt gebruiken om [!DNL Insight Server] aanvankelijk op te zetten en te vormen. Zodra u deze vergunning identificeert, kunt u alle verdere serverconfiguratie (met inbegrip van extra configuratie AccessGroup) uitvoeren gebruikend het vergunning gegeven exemplaar van [!DNL Insight]. Voor extra informatie over het controleren van toegang tot de server gebruikend Accessgroups, zie [het Vormen van Toegangsbeheer](../../../../home/c-inst-svr/c-admin-inst-svr/c-config-acs-ctrl/c-config-acs-ctrl.md#concept-ac385e870dbe4b57a72bf7266b60f93d).

**Het toegangsbeheerbestand bijwerken**

1. Navigeer naar de map [!DNL Access Control] in de map waarin u [!DNL Insight Server] hebt geïnstalleerd.

   Voorbeeld: [!DNL C:\Adobe\Server\Access Control]

1. Open het [!DNL Access Control.cfg] dossier in een tekstredacteur zoals Blocnote.
1. Zoek het CN-item in de beheerdersAccessGroup en vervang de bestaande waarde van dit item door de algemene naam die de [!DNL Insight] identificeert die u in eerste instantie zult gebruiken voor het instellen en beheren van [!DNL Insight Server]. Het volgende bestandsfragment illustreert waar u de algemene naam invoegt in het [!DNL Access Control.cfg]-bestand.

   ```
   Access Control Groups = vector: 5 items 
     0 = AccessGroup: 
       Members = vector: 2 items 
         0 = string: IP:127.0.0.1 
         1 = string: CN: CommonName 
       Name = string: Administrators 
       Read-Only Access = vector: 0 items 
       Read-Write Access = vector: 1 items 
         0 = string: / 
     1 = AccessGroup: 
     . . . 
   ```

   Als u op geloofsbrieven-gebaseerde authentificatie gebruikt, zullen een paar extra ingangen voor configuratie beschikbaar zijn. Deze vermeldingen zijn:

   * O (Organisatie-id): Dit item vertegenwoordigt de id van de organisatie. Bijvoorbeeld, `1 = string: O:46F582D4582596B40A45491@ExampleOrg`. Deze id is te vinden in de Admin Console.
   * PLC - Deze ingang verleent toegang tot de gebruikers die voor een bepaalde productconfiguratie worden voorzien. Het kan in formaat `Organization_Id-PLC` worden gebruikt. Bijvoorbeeld, `1 = string: PLC:46F582D4582596B40A45491@ExampleOrg-DataworkbenchAdminUsers`. Gebruikers die via de PLC `DataworkbenchAdminUsers` zijn ingericht voor Data Workbench, krijgen toegang op hun servers.
   * E-mail - Met dit bericht hebt u toegang tot elke afzonderlijke gebruiker. Zijn waarde zou het e-mailadres van de geleverde gebruiker moeten zijn. Bijvoorbeeld, `1 = string: Email:kim@exampleorg.com`.

   >[!NOTE]
   >
   >
   >    
   >    
   >    * De items zijn hoofdlettergevoelig. U moet ervoor zorgen dat de waarden die voor O, PLC en E-mail worden opgegeven exact gelijk zijn aan de waarden die in de Admin Console worden weergegeven.
   >    * Typ de algemene naam exact zoals deze op het certificaat wordt weergegeven.
   >    * Gebruik de Tab-toets niet om witruimte te genereren in het [!DNL Access Control.cfg]-bestand (of in een ander configuratiebestand voor een Adobe-component). Gebruik alleen spaties om witruimte te maken. Een tabteken voorkomt dat het systeem het bestand correct leest.


1. Sla het bestand op en sluit het.
