---
description: Het dossier van Access Control.cfg beheert toegang tot bepaalde eigenschappen in de Server van het Inzicht.
solution: Insight
title: Het bijwerken van het Dossier van het Toegangsbeheer
uuid: f73651e5-6a8b-45fc-8f36-6751304dc53c
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Het bijwerken van het Dossier van het Toegangsbeheer{#updating-the-access-control-file}

Het dossier van Access Control.cfg beheert toegang tot bepaalde eigenschappen in de Server van het Inzicht.

Het bepaalt entiteiten genoemd AccessGroups. Een AccessGroup identificeert een groep gebruikers die toestemming hebben om bepaalde eigenschappen van de server te gebruiken.

Alvorens u kunt verbinden met [!DNL Insight Server] , moet u de Beheerders AccessGroup bijwerken om één van de [!DNL Insight][!DNL Insight] vergunningen te omvatten die Adobe aan uw organisatie heeft uitgegeven. Deze AccessGroup identificeert gebruikers die worden toegelaten om administratieve functies door uit te voeren [!DNL Insight].

De volgende procedure beschrijft hoe te om een vergunning aan Beheerders AccessGroup toe te voegen. Om deze taak te voltooien, moet u bepalen welke [!DNL Insight] vergunning administratieve voorrechten voor uw organisatie heeft. (Voor aanvankelijke opstelling en configuratie, volstaat het verlenen van administratieve voorrechten aan één enkel vergunning. U kunt administratieve voorrechten aan extra vergunningen later verlenen.) U moet ook de &quot;gemeenschappelijke naam&quot;kennen die aan deze vergunning wordt toegewezen. Om deze waarde te verkrijgen, kunt u de vergunningscertificaten voor uw rekening in [https://aap.adobe.com](https://aap.adobe.com)onderzoeken.

Het doel van deze procedure is eenvoudig een vergunning gegeven exemplaar van te identificeren [!DNL Insight] dat u aan opstelling kunt aanvankelijk gebruiken en vormen [!DNL Insight Server]. Zodra u deze vergunning identificeert, kunt u alle verdere serverconfiguratie (met inbegrip van extra configuratie AccessGroup) uitvoeren gebruikend het vergunning gegeven exemplaar van [!DNL Insight]. Voor extra informatie over het controleren van toegang tot de server die AccessGroups gebruikt, zie het [Vormen Toegangsbeheer](../../../../home/c-inst-svr/c-admin-inst-svr/c-config-acs-ctrl/c-config-acs-ctrl.md#concept-ac385e870dbe4b57a72bf7266b60f93d).

**Om het dossier van de toegangscontrole bij te werken**

1. Navigeer aan de [!DNL Access Control] omslag in de folder waar u installeerde [!DNL Insight Server].

   Voorbeeld: [!DNL C:\Adobe\Server\Access Control]

1. Open het [!DNL Access Control.cfg] dossier in een tekstredacteur zoals Blocnote.
1. Bepaal de plaats van de ingang van CN in de Beheerders AccessGroup en vervang de bestaande waarde van deze ingang met de gemeenschappelijke naam die identificeert [!DNL Insight] dat u aan aanvankelijk opstelling zult gebruiken en zult beheren [!DNL Insight Server]. Het volgende dossierfragment illustreert waar u de gemeenschappelijke naam in het [!DNL Access Control.cfg] dossier opneemt.

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

   * O (Organisatie-ID): Deze ingang vertegenwoordigt identiteitskaart van de organisatie. Bijvoorbeeld, `1 = string: O:46F582D4582596B40A45491@ExampleOrg`. Deze ID is te vinden in de beheerdersconsole.
   * PLC - Deze ingang verleent toegang tot de gebruikers die voor een bepaalde productconfiguratie worden voorzien. Het kan in formaat worden gebruikt `Organization_Id-PLC`. Bijvoorbeeld, `1 = string: PLC:46F582D4582596B40A45491@ExampleOrg-DataworkbenchAdminUsers`. De gebruikers provisioned voor de Werkbank van Gegevens die PLC gebruiken `DataworkbenchAdminUsers` zullen toegang op hun servers krijgen.
   * E-mail - Deze ingang verleent toegang tot om het even welke individuele gebruiker. Zijn waarde zou het e-mailadres van de geleverde gebruiker moeten zijn. Bijvoorbeeld, `1 = string: Email:kim@exampleorg.com`.
   >[!NOTE]
   >
   >
   >    
   >    
   >    * De ingangen zijn gevoelig geval. U moet ervoor zorgen dat de waarden die voor O, PLC, en E-mail worden gespecificeerd precies het zelfde zijn zoals die in de Console Admin worden getoond.
   >    * Typ precies de gemeenschappelijke naam aangezien het op het certificaat verschijnt.
   >    * Gebruik niet de sleutel van het Lusje om whitespace in het [!DNL Access Control.cfg] dossier (of in een ander configuratiedossier voor een component van Adobe te produceren) te produceren. Gebruik alleen spaties om whitespace te maken. Een lusjekarakter verhindert het systeem het dossier correct te lezen.


1. Sparen en sluit het dossier.

