---
description: Conceptuele informatie die in overweging moet worden genomen bij het bewerken van het bestand Log Processing.cfg.
title: Overwegingen voor het configuratiebestand van de logbestandverwerking
uuid: 2ccedf63-12d9-40e9-912a-aee030191b1e
exl-id: 278a4a10-d382-4d9f-b3f4-bcc4783eb50c
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '306'
ht-degree: 0%

---

# Overwegingen voor het dossier van de Configuratie van de Verwerking van het Logboek{#considerations-for-the-log-processing-configuration-file}

Conceptuele informatie die in overweging moet worden genomen bij het bewerken van het bestand Log Processing.cfg.

* De dossiers van gegevens zouden niet tussen folders moeten worden bewogen nadat de bronnen voor een dataset zijn bepaald. De enige aanvullende bestanden die een directory moet ontvangen, zijn nieuw gemaakte bestanden die het resultaat zijn van de gegevenswerkbankserver die gegevens van de sensor(en) ontvangt.
* Als u een van de parameters in dit bestand wijzigt, moeten alle gegevens opnieuw worden verwerkt. De parameter Pause in het [!DNL Log Processing Mode.cfg]-bestand moet op false worden ingesteld om opnieuw te kunnen worden verwerkt. (De standaardwaarde van deze parameter is false, dus het wijzigen van de parameter is mogelijk niet vereist.) Voor informatie over het [!DNL Log Processing Mode.cfg] dossier, zie [Extra Dossiers van de Configuratie](../../../home/c-dataset-const-proc/c-add-config-files/c-add-config-files.md#concept-1afef4f88f1e467ab4326875fd1d3004).

* Als u de gegevens opnieuw verwerkt, kunt u de parameter van de Voortgang van de Verwerking van het Logboek in gegevens controleren werkbank [!DNL Processing Legend].

   Zie [Opwerking en hertransformatie](../../../home/c-dataset-const-proc/c-reproc-retrans/c-unst-reproc-retrans.md) voor informatie over het opnieuw verwerken van uw gegevens. Zie [Legend verwerken](../../../home/c-get-started/c-admin-intrf/c-pro-lgd.md#concept-233e27c9c84c426f8c178a27cc7ff828).

* Het [!DNL Log Processing.cfg] dossier kan door veelvoudige datasetprofielen worden gedeeld. Transformaties die in het [!DNL Log Processing.cfg] dossier worden bepaald worden toegepast op alle datasetprofielen die dit configuratiedossier delen.

   >[!NOTE]
   >
   >Adobe raadt aan transformaties te definiëren voor de logverwerking in een of meer logbestanden die [!DNL dataset include] verwerken. Zie [Gegevensset van logverwerking Inclusief bestanden](../../../home/c-dataset-const-proc/c-dataset-inc-files/c-types-dataset-inc-files/c-log-proc-dataset-inc-files/c-log-proc-dataset-inc-files.md#concept-999475a22519432e98844622ca95b6ab) voor meer informatie.

* U kunt om het even welke hierboven beschreven parameters aan het [!DNL Log Processing.cfg] dossier toevoegen door het dossier in Blocnote te openen en uit te geven. Wijzigingen die u aanbrengt en opslaat, worden weergegeven wanneer u het bestand opnieuw opent in de werkbank Gegevens. Wanneer u een nieuwe parameter toevoegt, gebruikt u de toets Ruimte (niet de Tab-toets) om twee (2) spaties rechts van het vorige kopniveau te laten inspringen.

   Om het even welke fouten die tijdens de fase van de logboekverwerking van het proces van de datasetconstructie voor een datasetprofiel voorkomen worden getoond in de [!DNL Profiles] knoop van de [!DNL Detailed Status] interface in gegevenswerkbank. Voor informatie over de [!DNL Detailed Status] interface, zie *Gids van de Gebruiker van de Data Workbench*.
