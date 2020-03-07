---
description: Belangrijke informatie om te overwegen wanneer het uitgeven van het dossier Transformation.cfg.
solution: Analytics
title: Overwegingen voor het dossier van de Configuratie van de Transformatie
topic: Data workbench
uuid: 1b64d023-966d-4f84-beb6-4f02b3504eea
translation-type: tm+mt
source-git-commit: 27600561841db3705f4eee6ff0aeb8890444bbc9

---


# Overwegingen voor het dossier van de Configuratie van de Transformatie{#considerations-for-the-transformation-configuration-file}

Belangrijke informatie om te overwegen wanneer het uitgeven van het dossier Transformation.cfg.

* Het veranderen van om het even welke parameters in dit dossier vereist retransformation van de gegevens.
* Als u de gegevens opnieuw verwerkt, kunt u de [!DNL Transformation Progress] parameter in de werkbank van gegevens controleren [!DNL Processing Legend].

   Voor informatie over het opnieuw verwerken van uw gegevens of [!DNL Processing Legend,] zie [Opwerking en Herschikking](../../../home/c-dataset-const-proc/c-reproc-retrans/c-unst-reproc-retrans.md).

* [!DNL CrossRows], [!DNL ODBCLookup], [!DNL Sessionize], en [!DNL AppendURI] transformaties werken slechts wanneer bepaald in een [!DNL Transformation Dataset Configuration] dossier. Voor informatie over deze transformaties, zie de Transformaties van [Gegevens](../../../home/c-dataset-const-proc/c-data-trans/c-abt-transf.md).

   >[!NOTE]
   >
   >Adobe adviseert bepalend transformaties voor de transformatiefase van datasetconstructie in één of meerdere [!DNL Transformation Dataset Include] dossiers. Voor informatie, zie de Dataset van de [Transformatie omvatten Dossiers](../../../home/c-dataset-const-proc/c-dataset-inc-files/c-types-dataset-inc-files/c-trans-dataset-inc-files.md#concept-c64aa78ed9ce40b8a0f4932c82ff5ace).

* U kunt om het even welke hierboven beschreven parameters aan het [!DNL Transformation.cfg] dossier toevoegen door het dossier in Blocnote te openen en uit te geven. Om het even welke veranderingen u aanbrengt en opslaat verschijnen wanneer u het dossier in gegevenswerkbank heropent. Wanneer het toevoegen van een nieuwe parameter, gebruik de Ruimtesleutel (niet de sleutel van het Lusje) om twee (2) ruimten rechts van het vorige rubriekniveau te kartelen.

   Om het even welke fouten die tijdens de transformatiefase van het proces van de datasetconstructie voor een datasetprofiel voorkomen worden getoond in de [!DNL Profiles] knoop van de [!DNL Detailed Status] interface in gegevenswerkbank. Voor informatie over de [!DNL Detailed Status] interface, zie de Gids *van de Gebruiker van de Werkbank van* Gegevens.

