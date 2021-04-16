---
description: Een server van het verwerkende Inzicht is identiek aan een master Server van het Inzicht behalve de inhoud van zijn folder van Componenten.
title: De servers van het Inzicht van de Verwerking installeren en Vormen
uuid: 186675f7-8b63-4675-89ec-51b0837a64d8
exl-id: 21f7e31b-a2fb-4257-972e-5228bb1efa01
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '303'
ht-degree: 0%

---

# Installeren en het Vormen van de Servers van het Inzicht van de Verwerking{#installing-and-configuring-the-processing-insight-servers}

Een server van het verwerkende Inzicht is identiek aan een master Server van het Inzicht behalve de inhoud van zijn folder van Componenten.

De folder van Componenten op een verwerking [!DNL Insight Server] bevat een speciale reeks dossiers die specifiek voor verwerking [!DNL Insight Servers] worden gevormd. Deze bestanden worden afgeleid van de map Components for Processing Servers op de master [!DNL Insight Server].

Wanneer u een verwerking [!DNL Insight Server] installeert, doet u het volgende aan opstelling zijn folder van Componenten:

1. Verwijder de originele map Components op de verwerking [!DNL Insight Server].
1. Wijzig de naam van de componenten voor het verwerken van de map Servers in Componenten.
1. Wijzig [!DNL Synchronize.cfg] in de folder van Componenten om aan master [!DNL Insight Server] te richten.

**Een verwerking installeren en configureren[!DNL Insight Server]**

1. Installeer de [!DNL Insight Server] programmabestanden zoals beschreven in [Bestanden van het Insight Server Program](../../../../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/t-install-prgm-files.md#task-1e6251fd39714186baa40d38f23d0088) installeren. Vergeet niet de mapstructuur te dupliceren die op de master [!DNL Insight Server] is gebruikt. Als [!DNL Insight Server] bijvoorbeeld is geïnstalleerd in [!DNL C:\Adobe\Server] op de master [!DNL Insight Server], moet u deze ook installeren in [!DNL C:\Adobe\Server] op de verwerking [!DNL Insight Servers].
1. Installeer het digitale certificaat dat door Adobe is uitgegeven voor deze specifieke verwerking [!DNL Insight Server]. Zie [Digitale certificaten downloaden en installeren](../../../../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/c-dnld-dgtl-cert/c-dnld-dgtl-cert.md#concept-4f79c240492f4e52b6375b4b3bbefa17) voor instructies.
1. Gebruikend de Ontdekkingsreiziger van Vensters, doe het volgende op de verwerking [!DNL Insight Server]:

   1. Verwijder de map **[!UICONTROL Components]**.
   1. Wijzig de naam van de map [!DNL Components for Processing Servers] in Componenten.

1. Gebruikend een tekstredacteur zoals Blocnote, open het [!DNL Synchronize.cfg] dossier in de folder van Componenten op de verwerking [!DNL Insight Server].
1. Voeg het IP adres van master (primair) [!DNL Insight Server] aan de tweede lijn van dit dossier zoals aangetoond in het volgende dossierfragment toe. Bewerk verder niets in dit bestand.

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
1. Start [!DNL Insight Server] zoals beschreven in [Insight Server registreren als een Windows-service](../../../../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/c-reg-wdws-svc.md#concept-f2c7aa891d544a2595aa01d0d796a540).

   U hebt nu de installatie van uw [!DNL Insight Server] cluster voltooid. Vervolgens configureert u het gegevenssetprofiel om in de cluster uit te voeren zoals in de volgende sectie wordt beschreven.
