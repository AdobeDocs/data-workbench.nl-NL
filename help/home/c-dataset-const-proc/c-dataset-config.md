---
description: De configuratie van de dataset verwijst naar het proces om de configuratiedossiers uit te geven de waarvan parameters de regels voor datasetconstructie verstrekken.
solution: Analytics
title: Begrijpen van de Configuratie van de Dataset
topic: Data workbench
uuid: 813933d1-f52d-4584-8edd-ce9cd4aed74a
translation-type: tm+mt
source-git-commit: 27600561841db3705f4eee6ff0aeb8890444bbc9

---


# Begrijpen van de Configuratie van de Dataset{#understanding-dataset-configuration}

De configuratie van de dataset verwijst naar het proces om de configuratiedossiers uit te geven de waarvan parameters de regels voor datasetconstructie verstrekken.

De geconstrueerde dataset verblijft fysisch in het [!DNL temp.db] dossier dat op de de servercomputer van de gegevenswerkbank wordt opgeslagen, maar de configuratiedossiers voor de dataset verblijven binnen een folder voor een profiel. Een profiel bevat een reeks configuratiedossiers die een dataset (met inbegrip van zijn uitgebreide afmetingen) voor een specifiek analysedoel construeren. Bovendien bevat een profiel de definities van entiteiten zoals metriek, afgeleide afmetingen, werkruimten, rapporten, en visualisaties die analisten toelaten om met de dataset in wisselwerking te staan en informatie uit het te verkrijgen.

Het profiel de waarvan dossiers van de datasetconfiguratie u uitgeeft wordt bedoeld als uw datasetprofiel. Een verwijzing van het datasetprofiel veelvoudige geërfte profielen, die om het even welke profielen kan zijn die u creeert en handhaaft zodat u uw toepassing van Adobe kunt vormen om uw analysebehoeften het best te passen. Een datasetprofiel kan ook interne profielen van verwijzingen voorzien die van uw toepassing van Adobe worden verstrekt om de basis voor alle functionaliteit te vormen beschikbaar in uw toepassing.

Voor meer informatie over de verschillende types van profielen die met de toepassingen van Adobe beschikbaar zijn, zie de Gids *van de Gebruiker van de Werkbank van* Gegevens.

<!--
c_req_config_files.xml
-->

Een datasetprofiel voor om het even welke toepassing van Adobe moet de volgende configuratiedossiers op de machine van de Server van het Inzicht bevatten:

* **Profiel.cfg:** Maakt een lijst van de geërfte profielen en verwerkingsservers voor het profiel. De servers van de verwerking zijn de Server DPUs van het Inzicht die de gegevens voor het profiel verwerken. Als u een cluster van de Server van het Inzicht hebt geïnstalleerd, kunt u de veelvoudige computers van de Server van het Inzicht specificeren om één enkel profiel in werking te stellen.

   Voor instructies om geërfte profielen aan het [!DNL Profile.cfg] dossier van een datasetprofiel toe te voegen, zie de Gids *van de Installatie en van het Beleid van de Producten van de* Server. Voor informatie over het installeren van een cluster van de Server van het Inzicht of het vormen van een datasetprofiel om op een cluster van de Server van het Inzicht te lopen, zie de Gids *van de Installatie en van het Beleid van de Producten van de* Server.

* **Dataset\Log Processing.cfg:** Controleert de fase van de logboekverwerking van het proces van de datasetconstructie. Zie [Logverwerking](../../home/c-dataset-const-proc/c-dataset-constr.md#concept-8a63892878004dc389c7dad784fcb061). Voor meer informatie over het [!DNL Log Processing.cfg] dossier, zie het Dossier van de Configuratie van de [Verwerking van het Logboek](../../home/c-dataset-const-proc/c-log-proc-config-file/c-abt-log-proc-config-file.md).

* **Dataset\Transformation.cfg:** Controleert de transformatiefase van het proces van de datasetconstructie. Zie [Transformatie](../../home/c-dataset-const-proc/c-dataset-constr.md#concept-88f72e0897a744b5bc03df5039264dda). Het [!DNL Transformation.cfg] dossier vormt typisch de dataset voor profiel-specifieke analyse. Voor meer informatie over het [!DNL Transformation.cfg] dossier, zie het Dossier van de Configuratie van de [Transformatie](../../home/c-dataset-const-proc/c-trans-config-file/c-abt-trans-config-file.md).

* **Gegevensset bevat bestanden:** Een [!DNL dataset include] dossier bevat een ondergroep van de parameters in het [!DNL Log Processing.cfg] of [!DNL Transformation.cfg] dossier voor het datasetprofiel maar opgeslagen en beheerd binnen een geërft profiel. [!DNL Dataset include] de dossiers vullen de belangrijkste dossiers van de datasetconfiguratie aan. Voor meer informatie, zie [Dataset omvatten Dossiers](../../home/c-dataset-const-proc/c-dataset-inc-files/c-abt-dataset-inc-files.md).

Het datasetprofiel dat aan u tijdens de implementatie van uw toepassing van Adobe wordt verstrekt bevat een reeks dossiers van de datasetconfiguratie die u, het gebruiken van opent uitgeven en kunt bewaren [!DNL Profile Manager].

Voor informatie over [!DNL Profile Manager], zie de Gids *van de Gebruiker van het* Inzicht.

<!--
c_addl_config_files.xml
-->

Hoewel niet vereist voor alle datasets, laten deze dossiers u toe om andere aspecten van het proces van de datasetconstructie te controleren:

* **Logverwerkingsmodus.cfg:** Het [!DNL Log Processing Mode.cfg] dossier laat u pauzeren verwerking van gegevens in een dataset, off-line bronnen specificeren, of de frequentie specificeren waarbij de server van de gegevenswerkbank zijn staatsdossiers bewaart. Zie [Aanvullende configuratiebestanden](../../home/c-dataset-const-proc/c-add-config-files/c-add-config-files.md#concept-1afef4f88f1e467ab4326875fd1d3004).

* **Server.cfg:** Het [!DNL Server.cfg] dossier specificeert de standaardgrootte van het gegevensgeheime voorgeheugen (in bytes) voor de machines van de gegevenswerkbank die met de server van de gegevenswerkbank verbinden. Zie [Aanvullende configuratiebestanden](../../home/c-dataset-const-proc/c-add-config-files/c-add-config-files.md#concept-1afef4f88f1e467ab4326875fd1d3004).

* **Transform.cfg en Transform Mode.cfg:** Deze dossiers zijn beschikbaar slechts als u de functionaliteit van de gegevenstransformatie om met uw toepassing van Adobe hebt vergunning gegeven te gebruiken. Het [!DNL Transform.cfg] dossier bevat de parameters die de logboekbronnen en de gegevenstransformaties voor transformatiefunctionaliteit bepalen. De transformaties die u bepaalt manipuleren de brongegevens en de output het in een formaat dat u specificeert. Het [!DNL Insight Transform Mode.cfg] dossier laat u toe om verwerking van gegevens in een dataset te pauzeren, off-line bronnen te specificeren, of de frequentie te specificeren waarbij de de transformatiefunctionaliteit van de Server van het Inzicht lopende transformatie zijn staatsdossiers bewaart. Zie Functionaliteit [transformeren](https://docs.adobe.com/content/help/en/data-workbench/using/server-admin-install/transform/t-config-tfm.html).

<!--
c_next_steps.xml
-->

Voor informatie over de specifieke taken van de datasetconfiguratie, gebruik hieronder de lijst om van de taken van belang van u de plaats te bepalen en te lezen:

<table id="table_394CFB5135274545B5DA37952EC6943E"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Als je wilt... </th> 
   <th colname="col2" class="entry"> Zie.. </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Logbronnen definiëren </p> </td> 
   <td colname="col2"> <p><a href="../../home/c-dataset-const-proc/c-log-proc-config-file/c-log-sources.md#concept-6714c720fac044cbb9af003bf401b2ea"> Logbronnen </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Bepaal welke logboekingangen de dataset tijdens logboekverwerking ingaan </p> </td> 
   <td colname="col2"> <p> <a href="../../home/c-dataset-const-proc/c-log-proc-config-file/c-info-log-proc-param.md#concept-41bd49bf6b64442d91c232ec67529a3d"> Gegevensfilters</a> </p> <p> <a href="../../home/c-dataset-const-proc/c-log-proc-config-file/c-info-log-proc-param.md#concept-ecaff95cee4e40bc90f81e099c5fc934"> Status voor logboekinvoer</a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Laat de splitsing van het volgen IDs met grote hoeveelheden gebeurtenisgegevens toe </p> </td> 
   <td colname="col2"> <p><a href="../../home/c-dataset-const-proc/c-log-proc-config-file/c-info-log-proc-param.md#concept-64b416bbe42f4d689f90df246f7f7caf"> Key Splitsing</a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Vorm een Server van het Inzicht om als eenheid van de dossierserver te lopen </p> </td> 
   <td colname="col2"> <p><a href="../../home/c-dataset-const-proc/c-log-proc-config-file/c-ins-svr-file-svr-unit.md#concept-995abff3fce34e439fb3f7f47191c80d"> Het vormen van een Eenheid van de Server van het Dossier van de Server van het Inzicht </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Vorm een Server van het Inzicht om als gecentraliseerde normalisatieserver te lopen </p> </td> 
   <td colname="col2"> <p><a href="../../home/c-dataset-const-proc/c-log-proc-config-file/c-ins-svr-file-svr-unit.md#concept-995abff3fce34e439fb3f7f47191c80d"> Het vormen van een Eenheid van de Server van het Dossier van de Server van het Inzicht </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Plaats de tijdzone die voor het creëren van tijdafmetingen en het maken van tijdomzettingen moet worden gebruikt </p> </td> 
   <td colname="col2"> <p><a href="../../home/c-dataset-const-proc/c-trans-config-file/c-spec-trans-param/c-time-zones.md#concept-9cf16b1cb4874f7d85e1dd950fdb4956"> Tijdzones </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Breng minder belangrijke veranderingen in de dossiers van de datasetconfiguratie aan inbegrepen met de interne profielen die door Adobe worden verstrekt </p> </td> 
   <td colname="col2"> <p><a href="../../home/c-dataset-const-proc/c-dataset-inc-files/c-work-dataset-inc-files/t-edit-ex-dataset-inc-files.md#task-456c04e38ebc425fb35677a6bb6aa077"> Bestaande gegevensset bewerken Bestaande bestanden opnemen </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Specificeer nieuwe gebieden van gegevens die van logboekverwerking aan transformatie moeten worden overgegaan </p> </td> 
   <td colname="col2"> <p> <a href="../../home/c-dataset-const-proc/c-dataset-inc-files/c-work-dataset-inc-files/t-create-new-dataset-inc-files.md#task-b29f30605c374a6ca747ac843337b06e"> Het creëren van Nieuwe Dataset omvat Dossiers </a> </p> <p> <a href="../../home/c-dataset-const-proc/c-dataset-inc-files/c-types-dataset-inc-files/c-log-proc-dataset-inc-files/c-log-proc-dataset-inc-files.md#concept-999475a22519432e98844622ca95b6ab"> Gegevensverzameling logverwerking bevat bestanden </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Transformaties definiëren </p> </td> 
   <td colname="col2"> <p> <a href="../../home/c-dataset-const-proc/c-data-trans/c-abt-transf.md"> Gegevenstransformaties </a> </p> <p> <a href="../../home/c-dataset-const-proc/c-dataset-inc-files/c-work-dataset-inc-files/t-create-new-dataset-inc-files.md#task-b29f30605c374a6ca747ac843337b06e"> Het creëren van Nieuwe Dataset omvat Dossiers </a> </p> <p> <a href="../../home/c-dataset-const-proc/c-dataset-inc-files/c-types-dataset-inc-files/c-trans-dataset-inc-files.md#concept-c64aa78ed9ce40b8a0f4932c82ff5ace"> Dataset transformatie bevat bestanden </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Verlengde afmetingen maken </p> </td> 
   <td colname="col2"> <p> <a href="../../home/c-dataset-const-proc/c-ex-dim/c-abt-ex-dim.md"> Uitgebreide afmetingen </a> </p> <p> <a href="../../home/c-dataset-const-proc/c-dataset-inc-files/c-work-dataset-inc-files/t-create-new-dataset-inc-files.md#task-b29f30605c374a6ca747ac843337b06e"> Het creëren van Nieuwe Dataset omvat Dossiers </a> </p> <p> <a href="../../home/c-dataset-const-proc/c-dataset-inc-files/c-types-dataset-inc-files/c-trans-dataset-inc-files.md#concept-c64aa78ed9ce40b8a0f4932c82ff5ace"> Dataset transformatie bevat bestanden </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Bepaal parameters aan gebruik door logboekverwerking of transformatie </p> </td> 
   <td colname="col2"> <p><a href="../../home/c-dataset-const-proc/c-dataset-inc-files/c-def-param-dataset-inc-files/c-def-param-dataset-inc-files.md#concept-5ad06acc8dc44bf2a99643fafdd56b50"> Het bepalen van Parameters in Dataset omvat Dossiers </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Leer over de interfaces van het Inzicht die u toelaten om uw dataset te controleren of te beheren </p> </td> 
   <td colname="col2"> <p><a href="../../home/c-dataset-const-proc/c-dataset-config-tools/c-dataset-config-int/c-dataset-config-int.md#concept-0ea33a52ce234ec8951e7b4430fbc5ab"> Het werken met de Interfaces van de Configuratie van de Dataset </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Verberg bepaalde uitgebreide afmetingen zodat tonen zij niet op het afmetingsmenu in Inzicht </p> </td> 
   <td colname="col2"> <p><a href="../../home/c-dataset-const-proc/c-dataset-config-tools/c-hide-dataset-comp/c-hide-dataset-comp.md#concept-50d9a004736f42f6b0aa7cde0d6148ff"> Gegevensverzameling-onderdelen verbergen </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Treed bepaalde dossiers van de datasetconfiguratie in een profiel met voeten dat u niet kunt of wilt wijzigen </p> </td> 
   <td colname="col2"> <p><a href="../../home/c-dataset-const-proc/c-dataset-config-tools/c-hide-dataset-comp/c-hide-dataset-comp.md#concept-50d9a004736f42f6b0aa7cde0d6148ff"> Gegevensverzameling-onderdelen verbergen </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Uw dataset opnieuw verwerken </p> </td> 
   <td colname="col2"> <p><a href="../../home/c-dataset-const-proc/c-reproc-retrans/c-unst-reproc-retrans.md"> Opwerking en herverwerking </a> </p> </td> 
  </tr> 
 </tbody> 
</table>

