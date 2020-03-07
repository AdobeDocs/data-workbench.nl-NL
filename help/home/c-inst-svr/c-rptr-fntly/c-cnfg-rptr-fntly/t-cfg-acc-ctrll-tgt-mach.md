---
description: De machines van de Server van het Inzicht van het doel die de Dienst van de Replicatie van de Server van het Inzicht in werking stellen van het Inzicht moeten de logboekdossiers op deze repeaterserver kunnen lezen.
solution: Insight
title: Het vormen Toegangsbeheer voor de Machines van het Doel
uuid: 35e032cf-6c1d-4348-88ce-4f4a6a30b16f
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Het vormen Toegangsbeheer voor de Machines van het Doel{#configuring-access-control-for-target-machines}

De machines van de Server van het Inzicht van het doel die de Dienst van de Replicatie van de Server van het Inzicht in werking stellen van het Inzicht moeten de logboekdossiers op deze repeaterserver kunnen lezen.

De toegang tot de doelmachines wordt verleend gebruikend het [!DNL Access Control.cfg] dossier.

**Om het Toegangsbeheer voor toegang door[!DNL Insight Server]doelmachines te vormen**

1. Navigeer aan de [!DNL Access Control] omslag in de folder waar u repeaterfunctionaliteit installeerde.

   Voorbeeld: [!DNL D:\Adobe\Repeater\Access Control]

1. Open [!DNL Access Control.cfg] in een tekstredacteur zoals Blocnote.
1. Creeer een toegangsgroep voor de [!DNL Insight Server] machines die tot de logboekdossiers op deze repeaterserver moeten toegang hebben. Geef deze toegangsgroep een naam iets als &quot;de Targets van de Replicatie.&quot;

       Het volgende dossierfragment toont hoe de toegangsgroep zou moeten kijken.
       
       ```
       . . .
       6 = AccessGroup:
       Leden = vector: N items
     0 = string: IP:Machine0IPAddress
     1 = koord: IP:Machine1IPAddress
     . . .
       N = string: IP:MachineNIPAddress
     Naam = koord: Replicatiedoelen
     alleen-lezen toegang = vector: 1 punten
     0 = koord: EventDataLocation
     read-write Toegang = vector: 0 objecten
     . . .
       &quot;
   
   1. In de sectie van Leden, specificeer het IP adres voor elke machine.
   1. Werk de punttelling voor de vector van Leden bij om op het aantal machineIP adressen te wijzen u opnam.
   1. In de read-only sectie van de Toegang, specificeer de plaats van de gebeurtenisgegevens die de replicatiedoelstellingen toegang hebben. Gebruik voorwaartse schuine strepen in de wegspecificatie (/). De standaardplaats is de [!DNL Logs] omslag op de machine van de Repeater (/Logboeken/).
   1. Werk de punttelling voor de read-only vector van de Toegang bij om op het aantal plaatsen te wijzen u opnam.

1. Werk het aantal toegangsgroepen in de vector van de Groepen van het Toegangsbeheer bij bij de bovenkant van het dossier om op de toevoeging van de nieuwe toegangsgroep te wijzen.

   ```
   Access Control Groups = vector: n items
   ```

1. Sla het bestand op.
