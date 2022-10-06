---
description: Belangrijke informatie die u moet overwegen bij het bewerken van het bestand Transformation.cfg.
title: Overwegingen bij het configuratiebestand van de transformatie
uuid: 1b64d023-966d-4f84-beb6-4f02b3504eea
exl-id: 7164ccb5-269c-4968-a3b4-1ff046a57f92
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 0%

---

# Overwegingen bij het configuratiebestand van de transformatie{#considerations-for-the-transformation-configuration-file}

{{eol}}

Belangrijke informatie die u moet overwegen bij het bewerken van het bestand Transformation.cfg.

* Als u een van de parameters in dit bestand wijzigt, moeten de gegevens opnieuw worden getransformeerd.
* Als u de gegevens opnieuw verwerkt, kunt u de [!DNL Transformation Progress] parameter in werkbank gegevens [!DNL Processing Legend].

   Voor informatie over het opnieuw verwerken van uw gegevens of de [!DNL Processing Legend,] zie [Opwerking en heromzetting](../../../home/c-dataset-const-proc/c-reproc-retrans/c-unst-reproc-retrans.md).

* [!DNL CrossRows], [!DNL ODBCLookup], [!DNL Sessionize], en [!DNL AppendURI] transformaties werken alleen wanneer ze zijn gedefinieerd in een [!DNL Transformation Dataset Configuration] bestand. Voor informatie over deze transformaties raadpleegt u [Gegevenstransformaties](../../../home/c-dataset-const-proc/c-data-trans/c-abt-transf.md).

   >[!NOTE]
   >
   >Adobe beveelt aan transformaties voor de transformatiefase van de constructie van gegevenssets in een of meer [!DNL Transformation Dataset Include] bestanden. Zie voor meer informatie [Gegevensset transformatie bevat bestanden](../../../home/c-dataset-const-proc/c-dataset-inc-files/c-types-dataset-inc-files/c-trans-dataset-inc-files.md#concept-c64aa78ed9ce40b8a0f4932c82ff5ace).

* U kunt alle hierboven beschreven parameters toevoegen aan de [!DNL Transformation.cfg] door het bestand te openen en te bewerken in Kladblok. Wijzigingen die u aanbrengt en opslaat, worden weergegeven wanneer u het bestand opnieuw opent in de werkbank Gegevens. Wanneer u een nieuwe parameter toevoegt, gebruikt u de toets Ruimte (niet de Tab-toets) om twee (2) spaties rechts van het vorige kopniveau te laten inspringen.

   Om het even welke fouten die tijdens de transformatiefase van het proces van de datasetconstructie voor een datasetprofiel voorkomen worden getoond in [!DNL Profiles] knooppunt van de [!DNL Detailed Status] interface in gegevenswerkbank. Voor informatie over de [!DNL Detailed Status] interface, zie *Gebruikershandleiding voor Data Workbench*.
