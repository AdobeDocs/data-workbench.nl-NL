---
description: Een server van het verwerkende Inzicht is identiek aan een master Server van het Inzicht behalve de inhoud van zijn folder van Componenten.
solution: Analytics
title: De servers van het Inzicht van de Verwerking installeren en Vormen
uuid: 186675f7-8b63-4675-89ec-51b0837a64d8
translation-type: tm+mt
source-git-commit: 34cdcfc83ae6bb620706db37228e200cff43ab2c
workflow-type: tm+mt
source-wordcount: '303'
ht-degree: 0%

---


# De servers van het Inzicht van de Verwerking installeren en Vormen{#installing-and-configuring-the-processing-insight-servers}

Een server van het verwerkende Inzicht is identiek aan een master Server van het Inzicht behalve de inhoud van zijn folder van Componenten.

De folder van Componenten op een verwerking [!DNL Insight Server] bevat een speciale reeks dossiers die specifiek voor verwerking worden gevormd [!DNL Insight Servers]. Deze bestanden zijn afgeleid van de map Components for Processing Servers in het master bestand [!DNL Insight Server].

Wanneer u een verwerking installeert [!DNL Insight Server], doet u het volgende aan opstelling zijn folder van Componenten:

1. Verwijder de originele map Components op de verwerking [!DNL Insight Server].
1. Wijzig de naam van de componenten voor het verwerken van de map Servers in Componenten.
1. Wijzig het [!DNL Synchronize.cfg] in de folder van Componenten om aan master te richten [!DNL Insight Server].

**Een verwerking installeren en configureren[!DNL Insight Server]**

1. Installeer de [!DNL Insight Server] programmadossiers zoals die in het [Installeren van de Dossiers](../../../../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/t-install-prgm-files.md#task-1e6251fd39714186baa40d38f23d0088)van het Programma van de Server van het Inzicht worden beschreven. Vergeet niet de mapstructuur te dupliceren die op het master bestand is gebruikt [!DNL Insight Server]. Als u de software bijvoorbeeld in [!DNL Insight Server] het master hebt geïnstalleerd [!DNL C:\Adobe\Server] , moet u deze [!DNL Insight Server]ook op de verwerking installeren [!DNL C:\Adobe\Server] [!DNL Insight Servers] .
1. Installeer het digitale certificaat dat Adobe voor deze specifieke verwerking heeft uitgegeven [!DNL Insight Server]. Zie Digitale certificaten [downloaden en installeren](../../../../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/c-dnld-dgtl-cert/c-dnld-dgtl-cert.md#concept-4f79c240492f4e52b6375b4b3bbefa17) voor instructies.
1. Gebruikend de Ontdekkingsreiziger van Vensters, doe het volgende op de verwerking [!DNL Insight Server]:

   1. Verwijder de **[!UICONTROL Components]** map.
   1. Wijzig de naam van de [!DNL Components for Processing Servers] map in Componenten.

1. Gebruikend een tekstredacteur zoals Blocnote, open het [!DNL Synchronize.cfg] dossier in de folder van Componenten op de verwerking [!DNL Insight Server].
1. Voeg het IP-adres van de master (primaire) [!DNL Insight Server] toe aan de tweede regel van dit bestand, zoals wordt weergegeven in het volgende bestandsfragment. Bewerk verder niets in dit bestand.

   ```
   component = SynchronizeComponent:
     Cluster Primary Server Address = string: PrimaryIPAddress
     Directories = vector: 7 items
       0 = SynchronizeDir:
         Local Path = string: Profiles\\
         Remote URI = string: /Profiles/
       1 = SynchronizeDir:
         Local Path = string: Lookups\\
         Remote URI = string: /Lookups/
       . . .
   ```

1. Sla het bestand op.
1. Begin [!DNL Insight Server] zoals die in het [Registreren van de Server van het Inzicht als Dienst](../../../../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/c-reg-wdws-svc.md#concept-f2c7aa891d544a2595aa01d0d796a540)van Vensters wordt beschreven.

   U hebt de installatie van uw [!DNL Insight Server] cluster nu voltooid. Vervolgens configureert u het gegevenssetprofiel om in de cluster uit te voeren zoals in de volgende sectie wordt beschreven.

