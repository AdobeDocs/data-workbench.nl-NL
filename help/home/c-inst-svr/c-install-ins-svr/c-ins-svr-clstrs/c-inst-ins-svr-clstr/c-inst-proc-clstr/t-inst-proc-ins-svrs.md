---
description: Een server van het verwerkende Inzicht is identiek aan een hoofdserver van het Inzicht behalve de inhoud van zijn folder van Componenten.
solution: Insight
title: Het installeren van en het Vormen van de Servers van het Inzicht van de Verwerking
uuid: 186675f7-8b63-4675-89ec-51b0837a64d8
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Het installeren van en het Vormen van de Servers van het Inzicht van de Verwerking{#installing-and-configuring-the-processing-insight-servers}

Een server van het verwerkende Inzicht is identiek aan een hoofdserver van het Inzicht behalve de inhoud van zijn folder van Componenten.

De folder van Componenten op een verwerking [!DNL Insight Server] bevat een speciale reeks dossiers die specifiek voor verwerking worden gevormd [!DNL Insight Servers]. Deze dossiers worden afgeleid uit de Componenten voor de folder van de Servers van de Verwerking op de meester [!DNL Insight Server].

Wanneer u een verwerking installeert [!DNL Insight Server], doet u het volgende aan opstelling zijn folder van Componenten:

1. Schrap de originele folder van Componenten op de verwerking [!DNL Insight Server].
1. Noem de Componenten voor de folder van de Servers van de Verwerking aan Componenten anders.
1. Wijzig [!DNL Synchronize.cfg] in de folder van Componenten om aan de meester te richten [!DNL Insight Server].

**Om een verwerking te installeren en te vormen[!DNL Insight Server]**

1. Installeer de [!DNL Insight Server] programmadossiers zoals die in het [Installeren van de Dossiers](../../../../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/t-install-prgm-files.md#task-1e6251fd39714186baa40d38f23d0088)van het Programma van de Server van het Inzicht worden beschreven. Ben zeker om de folderstructuur te dupliceren die op de meester werd gebruikt [!DNL Insight Server]. Bijvoorbeeld, als [!DNL Insight Server] in [!DNL C:\Adobe\Server] op de meester geïnstalleerd is [!DNL Insight Server], moet u het binnen [!DNL C:\Adobe\Server] op de verwerking [!DNL Insight Servers] eveneens installeren.
1. Installeer het digitale certificaat dat Adobe voor deze bepaalde verwerking heeft uitgegeven [!DNL Insight Server]. Zie De digitale certificaten [downloaden en installeren](../../../../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/c-dnld-dgtl-cert/c-dnld-dgtl-cert.md#concept-4f79c240492f4e52b6375b4b3bbefa17) voor instructies.
1. Gebruikend de Ontdekkingsreiziger van Vensters, doe het volgende op de verwerking [!DNL Insight Server]:

   1. Schrap de **[!UICONTROL Components]** omslag.
   1. Noem de [!DNL Components for Processing Servers] omslag aan Componenten anders.

1. Gebruikend een tekstredacteur zoals Blocnote, open het [!DNL Synchronize.cfg] dossier in de folder van Componenten op de verwerking [!DNL Insight Server].
1. Voeg het IP adres van de (primaire) meester [!DNL Insight Server] aan de tweede lijn van dit dossier zoals aangetoond in het volgende dossierfragment toe. Bewerk niets anders in dit bestand.

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
1. Begin [!DNL Insight Server] zoals die in de Server van het [Inzicht van het Registreren als Dienst](../../../../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/c-reg-wdws-svc.md#concept-f2c7aa891d544a2595aa01d0d796a540)van Vensters wordt beschreven.

   U hebt nu de installatie van uw [!DNL Insight Server] cluster voltooid. Daarna, vorm het datasetprofiel om op de cluster te lopen zoals die in de volgende sectie wordt beschreven.

