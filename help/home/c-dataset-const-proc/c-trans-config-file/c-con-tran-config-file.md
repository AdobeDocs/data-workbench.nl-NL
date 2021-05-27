---
description: Belangrijke informatie die u moet overwegen bij het bewerken van het bestand Transformation.cfg.
title: Overwegingen bij het configuratiebestand van de transformatie
uuid: 1b64d023-966d-4f84-beb6-4f02b3504eea
exl-id: 7164ccb5-269c-4968-a3b4-1ff046a57f92
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 0%

---

# Overwegingen voor het Dossier van de Configuratie van de Transformatie{#considerations-for-the-transformation-configuration-file}

Belangrijke informatie die u moet overwegen bij het bewerken van het bestand Transformation.cfg.

* Als u een van de parameters in dit bestand wijzigt, moeten de gegevens opnieuw worden getransformeerd.
* Als u de gegevens opnieuw verwerkt, kunt u de [!DNL Transformation Progress] parameter in gegevens controleren werkbank [!DNL Processing Legend].

   Zie [Opwerking en hertransformatie](../../../home/c-dataset-const-proc/c-reproc-retrans/c-unst-reproc-retrans.md) voor informatie over het opnieuw verwerken van uw gegevens of de [!DNL Processing Legend,].

* [!DNL CrossRows],  [!DNL ODBCLookup],  [!DNL Sessionize]en  [!DNL AppendURI] transformaties werken alleen wanneer deze in een  [!DNL Transformation Dataset Configuration] bestand zijn gedefinieerd. Voor informatie over deze transformaties, zie [Transformaties van Gegevens](../../../home/c-dataset-const-proc/c-data-trans/c-abt-transf.md).

   >[!NOTE]
   >
   >Adobe raadt aan transformaties te definiëren voor de transformatiefase van de constructie van gegevenssets in een of meer [!DNL Transformation Dataset Include]-bestanden. Zie [Gegevensset transformatie Inclusief bestanden](../../../home/c-dataset-const-proc/c-dataset-inc-files/c-types-dataset-inc-files/c-trans-dataset-inc-files.md#concept-c64aa78ed9ce40b8a0f4932c82ff5ace) voor meer informatie.

* U kunt om het even welke hierboven beschreven parameters aan het [!DNL Transformation.cfg] dossier toevoegen door het dossier in Blocnote te openen en uit te geven. Wijzigingen die u aanbrengt en opslaat, worden weergegeven wanneer u het bestand opnieuw opent in de werkbank Gegevens. Wanneer u een nieuwe parameter toevoegt, gebruikt u de toets Ruimte (niet de Tab-toets) om twee (2) spaties rechts van het vorige kopniveau te laten inspringen.

   Om het even welke fouten die tijdens de transformatiefase van het proces van de datasetconstructie voor een datasetprofiel voorkomen worden getoond in de [!DNL Profiles] knoop van de [!DNL Detailed Status] interface in gegevenswerkbank. Voor informatie over de [!DNL Detailed Status] interface, zie *Gids van de Gebruiker van de Data Workbench*.
