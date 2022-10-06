---
description: Conceptuele informatie die in overweging moet worden genomen bij het bewerken van het bestand Log Processing.cfg.
title: Overwegingen voor het configuratiebestand van de logbestandverwerking
uuid: 2ccedf63-12d9-40e9-912a-aee030191b1e
exl-id: 278a4a10-d382-4d9f-b3f4-bcc4783eb50c
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '306'
ht-degree: 0%

---

# Overwegingen voor het configuratiebestand van de logbestandverwerking{#considerations-for-the-log-processing-configuration-file}

{{eol}}

Conceptuele informatie die in overweging moet worden genomen bij het bewerken van het bestand Log Processing.cfg.

* De dossiers van gegevens zouden niet tussen folders moeten worden bewogen nadat de bronnen voor een dataset zijn bepaald. De enige aanvullende bestanden die een directory moet ontvangen, zijn nieuw gemaakte bestanden die het resultaat zijn van de gegevenswerkbankserver die gegevens van de sensor(en) ontvangt.
* Als u een van de parameters in dit bestand wijzigt, moeten alle gegevens opnieuw worden verwerkt. De parameter Pauzeren in het dialoogvenster [!DNL Log Processing Mode.cfg] bestand moet op false worden ingesteld om opnieuw te kunnen worden verwerkt. (De standaardwaarde van deze parameter is false, dus het wijzigen van de parameter is mogelijk niet vereist.) Voor informatie over de [!DNL Log Processing Mode.cfg] bestand, zie [Aanvullende configuratiebestanden](../../../home/c-dataset-const-proc/c-add-config-files/c-add-config-files.md#concept-1afef4f88f1e467ab4326875fd1d3004).

* Als u de gegevens opnieuw verwerkt, kunt u de parameter van de Voortgang van de Verwerking van het Logboek in gegevenswerkbank controleren [!DNL Processing Legend].

   Voor informatie over het opnieuw verwerken van uw gegevens raadpleegt u [Opwerking en heromzetting](../../../home/c-dataset-const-proc/c-reproc-retrans/c-unst-reproc-retrans.md). Zie [Legenda verwerken](../../../home/c-get-started/c-admin-intrf/c-pro-lgd.md#concept-233e27c9c84c426f8c178a27cc7ff828).

* De [!DNL Log Processing.cfg] bestand kan worden gedeeld door meerdere gegevenssetprofielen. Transformaties die zijn gedefinieerd in het dialoogvenster [!DNL Log Processing.cfg] het dossier wordt toegepast op alle datasetprofielen die dit configuratiedossier delen.

   >[!NOTE]
   >
   >Adobe raadt aan transformaties voor de logverwerking in een of meer logbestanden te definiëren. [!DNL dataset include] bestanden. Zie voor meer informatie [Gegevensset logbestandsverwerking inclusief bestanden](../../../home/c-dataset-const-proc/c-dataset-inc-files/c-types-dataset-inc-files/c-log-proc-dataset-inc-files/c-log-proc-dataset-inc-files.md#concept-999475a22519432e98844622ca95b6ab).

* U kunt alle hierboven beschreven parameters toevoegen aan de [!DNL Log Processing.cfg] door het bestand te openen en te bewerken in Kladblok. Wijzigingen die u aanbrengt en opslaat, worden weergegeven wanneer u het bestand opnieuw opent in de werkbank Gegevens. Wanneer u een nieuwe parameter toevoegt, gebruikt u de toets Ruimte (niet de Tab-toets) om twee (2) spaties rechts van het vorige kopniveau te laten inspringen.

   Om het even welke fouten die tijdens de fase van de logboekverwerking van het proces van de datasetconstructie voor een datasetprofiel voorkomen worden getoond in [!DNL Profiles] knooppunt van de [!DNL Detailed Status] interface in gegevenswerkbank. Voor informatie over de [!DNL Detailed Status] interface, zie *Gebruikershandleiding voor Data Workbench*.
