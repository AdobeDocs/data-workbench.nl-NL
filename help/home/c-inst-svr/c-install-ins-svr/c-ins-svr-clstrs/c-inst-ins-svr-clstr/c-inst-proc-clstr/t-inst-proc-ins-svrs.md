---
description: Een server van het verwerkende Inzicht is identiek aan een master Server van het Inzicht behalve de inhoud van zijn folder van Componenten.
title: De servers van het Inzicht van de Verwerking installeren en Vormen
uuid: 186675f7-8b63-4675-89ec-51b0837a64d8
exl-id: 21f7e31b-a2fb-4257-972e-5228bb1efa01
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '303'
ht-degree: 0%

---

# De servers van het Inzicht van de Verwerking installeren en Vormen{#installing-and-configuring-the-processing-insight-servers}

{{eol}}

Een server van het verwerkende Inzicht is identiek aan een master Server van het Inzicht behalve de inhoud van zijn folder van Componenten.

De map Components in een verwerking [!DNL Insight Server] bevat een speciale set bestanden die specifiek zijn geconfigureerd voor verwerking [!DNL Insight Servers]. Deze bestanden zijn afgeleid van de map Components for Processing Servers op de master [!DNL Insight Server].

Wanneer u een verwerking installeert [!DNL Insight Server], doet u het volgende aan opstellings zijn folder van Componenten:

1. Verwijder de originele map Components op de verwerking [!DNL Insight Server].
1. Wijzig de naam van de componenten voor het verwerken van de map Servers in Componenten.
1. De [!DNL Synchronize.cfg] in de map Components om te wijzen naar de master [!DNL Insight Server].

**Een verwerking installeren en configureren[!DNL Insight Server]**

1. Installeer de [!DNL Insight Server] programmabestanden zoals beschreven in [De bestanden van het Insight Server-programma installeren](../../../../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/t-install-prgm-files.md#task-1e6251fd39714186baa40d38f23d0088). Let erop dat u de mappenstructuur dupliceert die is gebruikt voor de master [!DNL Insight Server]. Als [!DNL Insight Server] is geïnstalleerd in [!DNL C:\Adobe\Server] over de master [!DNL Insight Server], moet u de toepassing installeren in [!DNL C:\Adobe\Server] over de verwerking [!DNL Insight Servers] ook.
1. Installeer het digitale certificaat dat Adobe voor deze specifieke verwerking heeft uitgegeven [!DNL Insight Server]. Zie [Digitale certificaten downloaden en installeren](../../../../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/c-dnld-dgtl-cert/c-dnld-dgtl-cert.md#concept-4f79c240492f4e52b6375b4b3bbefa17) voor instructies.
1. Gebruikend de Ontdekkingsreiziger van Vensters, doe het volgende op de verwerking [!DNL Insight Server]:

   1. Verwijder de **[!UICONTROL Components]** map.
   1. De naam van de [!DNL Components for Processing Servers] naar Componenten.

1. Open met een teksteditor, zoals Kladblok, de [!DNL Synchronize.cfg] bestand in de map Components op de verwerking [!DNL Insight Server].
1. Voeg het IP adres van master (primaire) toe [!DNL Insight Server] op de tweede regel van dit bestand, zoals wordt weergegeven in het volgende bestandsfragment. Bewerk verder niets in dit bestand.

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
1. Start de [!DNL Insight Server] zoals beschreven in [Insight Server registreren als Windows-service](../../../../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/c-reg-wdws-svc.md#concept-f2c7aa891d544a2595aa01d0d796a540).

   U hebt nu de installatie van uw [!DNL Insight Server] cluster. Vervolgens configureert u het gegevenssetprofiel om in de cluster uit te voeren zoals in de volgende sectie wordt beschreven.
