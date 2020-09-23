---
description: De machines van de Server van het Inzicht van het doel die de Dienst van de Replicatie van de Server van het Inzicht in werking stellen moeten de logboekdossiers op deze repeaterserver kunnen lezen.
solution: Analytics
title: Toegangsbeheer voor doelapparaten configureren
uuid: 35e032cf-6c1d-4348-88ce-4f4a6a30b16f
translation-type: tm+mt
source-git-commit: 34cdcfc83ae6bb620706db37228e200cff43ab2c
workflow-type: tm+mt
source-wordcount: '245'
ht-degree: 0%

---


# Toegangsbeheer voor doelapparaten configureren{#configuring-access-control-for-target-machines}

De machines van de Server van het Inzicht van het doel die de Dienst van de Replicatie van de Server van het Inzicht in werking stellen moeten de logboekdossiers op deze repeaterserver kunnen lezen.

Toegang tot de doelapparaten wordt verleend gebruikend het [!DNL Access Control.cfg] dossier.

**Om Toegangsbeheer voor toegang door[!DNL Insight Server]doelmachines te vormen**

1. Navigeer naar de [!DNL Access Control] map in de map waarin u de herhalingsfunctionaliteit hebt geïnstalleerd.

   Voorbeeld: [!DNL D:\Adobe\Repeater\Access Control]

1. Openen [!DNL Access Control.cfg] in een teksteditor, zoals Kladblok.
1. Creeer een toegangsgroep voor de [!DNL Insight Server] machines die tot de logboekdossiers op deze repeaterserver moeten toegang hebben. Geef deze toegangsgroep een naam zoals &quot;Replicatiedoelen&quot;.

   Het volgende dossierfragment toont hoe de toegangsgroep zou moeten kijken.

   ```
   . . . 
     6 = AccessGroup: 
       Members = vector: N items 
         0 = string: IP:Machine0IPAddress 
         1 = string: IP:Machine1IPAddress 
   . . . 
         N = string: IP:MachineNIPAddress 
       Name = string: Replication Targets 
       Read-Only Access = vector: 1 items 
         0 = string: EventDataLocation 
       Read-Write Access = vector: 0 items 
   . . .
   ```

   1. Geef in de sectie Leden het IP-adres voor elke computer op.
   1. Werk de punttelling voor de vector van Leden bij om op het aantal machineIP adressen te wijzen u opnam.
   1. In de read-Only sectie van de Toegang, specificeer de plaats van de gebeurtenisgegevens die de replicatie toegang richt. Gebruik slashes in de padspecificatie (/). De standaardlocatie is de [!DNL Logs] map op de computer Repeater (/Logs/).
   1. Werk de punttelling voor de read-only vector van de Toegang bij om op het aantal plaatsen te wijzen u opnam.

1. Werk het aantal toegangsgroepen in de vector van de Groepen van het Toegangsbeheer bij bij de bovenkant van het dossier om op de toevoeging van de nieuwe toegangsgroep te wijzen.

   ```
   Access Control Groups = vector: n items
   ```

1. Sla het bestand op.
