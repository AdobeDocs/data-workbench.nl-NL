---
description: Het bestand Access Control.cfg beheert de toegang tot bepaalde functies in Insight Server.
title: Het Access Control-bestand bijwerken
uuid: f73651e5-6a8b-45fc-8f36-6751304dc53c
exl-id: 551758c1-f24b-49e6-ab6e-09979511e4f4
source-git-commit: 5ce5b8f8b35d2d4f319076f54347e300e5f133df
workflow-type: tm+mt
source-wordcount: '472'
ht-degree: 1%

---

# Het Access Control-bestand bijwerken{#updating-the-access-control-file}

{{eol}}

Het bestand Access Control.cfg beheert de toegang tot bepaalde functies in Insight Server.

Het bepaalt entiteiten genoemd Accessgroups. Een AccessGroup identificeert een groep gebruikers die toestemming hebben om bepaalde eigenschappen van de server te gebruiken.

Voordat u verbinding kunt maken met [!DNL Insight Server] with [!DNL Insight], moet u de Beheerders AccessGroup bijwerken om een van de [!DNL Insight] licenties die Adobe aan uw organisatie heeft uitgegeven. Deze AccessGroup identificeert gebruikers die beheerfuncties mogen uitvoeren via [!DNL Insight].

De volgende procedure beschrijft hoe te om een vergunning aan de Beheerders AccessGroup toe te voegen. Om deze taak te voltooien, moet u bepalen welke [!DNL Insight] licentie heeft beheerdersrechten voor uw organisatie. (Voor de eerste configuratie en configuratie volstaat het verlenen van administratieve bevoegdheden aan één licentie. U kunt later beheerrechten toekennen aan extra licenties.) U moet ook de &quot;algemene naam&quot; weten die aan deze licentie is toegewezen.

Het doel van deze procedure is simpelweg een gelicentieerde kopie van [!DNL Insight] die u kunt gebruiken aanvankelijk opstelling en vormen [!DNL Insight Server]. Zodra u deze vergunning identificeert, kunt u alle verdere serverconfiguratie (met inbegrip van extra configuratie AccessGroup) uitvoeren gebruikend het vergunning gegeven exemplaar van [!DNL Insight]. Voor extra informatie over het controleren van toegang tot de server gebruikend AccessGroup, zie [Toegangsbeheer configureren](../../../../home/c-inst-svr/c-admin-inst-svr/c-config-acs-ctrl/c-config-acs-ctrl.md#concept-ac385e870dbe4b57a72bf7266b60f93d).

**Het toegangsbeheerbestand bijwerken**

1. Ga naar de [!DNL Access Control] map in de map waarin u hebt geïnstalleerd [!DNL Insight Server].

   Voorbeeld: [!DNL C:\Adobe\Server\Access Control]

1. Open de [!DNL Access Control.cfg] bestand in een teksteditor, zoals Kladblok.
1. Zoek het CN-item in de beheerdersAccessGroup en vervang de bestaande waarde van dit item door de gemeenschappelijke naam die het [!DNL Insight] die u in eerste instantie zult gebruiken voor het instellen en beheren [!DNL Insight Server]. Het volgende bestandsfragment illustreert waar u de algemene naam invoegt in het dialoogvenster [!DNL Access Control.cfg] bestand.

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
   * PLC - Deze ingang verleent toegang tot de gebruikers die voor een bepaalde productconfiguratie worden voorzien. Het kan in formaat worden gebruikt `Organization_Id-PLC`. Bijvoorbeeld, `1 = string: PLC:46F582D4582596B40A45491@ExampleOrg-DataworkbenchAdminUsers`. De gebruikers provisioned voor Data Workbench gebruikend PLC `DataworkbenchAdminUsers` krijgen toegang op hun servers.
   * E-mail - Met dit bericht hebt u toegang tot elke afzonderlijke gebruiker. Zijn waarde zou het e-mailadres van de geleverde gebruiker moeten zijn. Bijvoorbeeld, `1 = string: Email:kim@exampleorg.com`.

   >[!NOTE]
   >
   >
   >    
   >    
   >    * De items zijn hoofdlettergevoelig. U moet ervoor zorgen dat de waarden die voor O, PLC en E-mail worden opgegeven exact gelijk zijn aan de waarden die in de Admin Console worden weergegeven.
   >    * Typ de algemene naam exact zoals deze op het certificaat wordt weergegeven.
   >    * Gebruik de Tab-toets niet om witruimte te genereren in het dialoogvenster [!DNL Access Control.cfg] bestand (of in een ander configuratiebestand voor een Adobe-component). Gebruik alleen spaties om witruimte te maken. Een tabteken voorkomt dat het systeem het bestand correct leest.


1. Sla het bestand op en sluit het.
