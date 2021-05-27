---
description: De configuratie van de gegevensset verwijst naar het proces om de configuratiedossiers uit te geven de waarvan parameters de regels voor datasetconstructie verstrekken.
title: Datasetconfiguratie begrijpen
uuid: 813933d1-f52d-4584-8edd-ce9cd4aed74a
exl-id: 1358d08e-d81c-453d-a3a3-c1f279f38192
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '916'
ht-degree: 0%

---

# Datasetconfiguratie begrijpen{#understanding-dataset-configuration}

De configuratie van de gegevensset verwijst naar het proces om de configuratiedossiers uit te geven de waarvan parameters de regels voor datasetconstructie verstrekken.

De geconstrueerde dataset bevindt zich fysiek in het [!DNL temp.db] dossier dat op de computer van de gegevenswerkbankserver wordt opgeslagen, maar de configuratiedossiers voor de dataset verblijven binnen een folder voor een profiel. Een profiel bevat een reeks configuratiedossiers die een dataset (met inbegrip van zijn uitgebreide afmetingen) voor een specifiek analysedoel construeren. Bovendien bevat een profiel de definities van entiteiten zoals metriek, afgeleide dimensies, werkruimten, rapporten, en visualisaties die analisten toelaten om met de dataset in wisselwerking te staan en informatie van het te verkrijgen.

Het profiel waarvan de dossiers van de datasetconfiguratie u uitgeeft wordt bedoeld als uw profiel van de dataset. Een datasetprofiel verwijst naar veelvoudige geërfte profielen, die om het even welke profielen kunnen zijn die u creeert en handhaaft zodat u uw toepassing van de Adobe kunt vormen om uw analysebehoeften het best te passen. Een gegevenssetprofiel kan ook naar interne profielen verwijzen die met uw toepassing van de Adobe worden verstrekt om de basis voor alle functionaliteit te vormen beschikbaar in uw toepassing.

Voor meer informatie over de verschillende types van profielen die met de toepassingen van Adobe beschikbaar zijn, zie *de Gids van de Gebruiker van de Data Workbench*.

<!--
c_req_config_files.xml
-->

Een datasetprofiel voor om het even welke toepassing van Adobe moet de volgende configuratiedossiers op de machine van de Server van het Inzicht bevatten:

* **Profile.cfg:** Hier worden de overgeërfde profielen en verwerkingsservers voor het profiel weergegeven. De servers van de verwerking zijn DPUs van de Server van het Inzicht die de gegevens voor het profiel verwerken. Als u een cluster van de Server van het Inzicht hebt geïnstalleerd, kunt u veelvoudige computers van de Server van het Inzicht specificeren om één enkel profiel in werking te stellen.

   Voor instructies om geërfte profielen aan het [!DNL Profile.cfg] dossier van een datasetprofiel toe te voegen, zie *de Gids van de Installatie en van het Beleid van de Producten van de Server*. Voor informatie over het installeren van een cluster van de Server van het Inzicht of het vormen van een datasetprofiel om op een cluster van de Server van het Inzicht in werking te stellen, zie *de Gids van de Installatie en van het Beleid van de Producten van de Server*.

* **Dataset \ Logboek Verwerking.cfg:** controleert de logboekverwerkingsfase van het proces van de datasetconstructie. Zie [Logverwerking](../../home/c-dataset-const-proc/c-dataset-constr.md#concept-8a63892878004dc389c7dad784fcb061). Voor meer informatie over het [!DNL Log Processing.cfg] dossier, zie [Dossier van de Configuratie van de Verwerking van het Logboek](../../home/c-dataset-const-proc/c-log-proc-config-file/c-abt-log-proc-config-file.md).

* **Dataset\Transformation.cfg:** regelt de transformatiefase van het constructieproces van de gegevensset. Zie [Transformatie](../../home/c-dataset-const-proc/c-dataset-constr.md#concept-88f72e0897a744b5bc03df5039264dda). Het [!DNL Transformation.cfg] dossier vormt typisch de dataset voor profiel-specifieke analyse. Zie [Transformation Configuration File](../../home/c-dataset-const-proc/c-trans-config-file/c-abt-trans-config-file.md) voor meer informatie over het [!DNL Transformation.cfg]-bestand.

* **Dataset bevat bestanden:** Een  [!DNL dataset include] bestand bevat een subset van de parameters in het  [!DNL Log Processing.cfg] of  [!DNL Transformation.cfg] bestand voor het gegevenssetprofiel, maar wordt opgeslagen en beheerd binnen een overgenomen profiel. [!DNL Dataset include] de dossiers vullen de belangrijkste dossiers van de datasetconfiguratie aan. Voor meer informatie, zie [Dataset omvat Dossiers](../../home/c-dataset-const-proc/c-dataset-inc-files/c-abt-dataset-inc-files.md).

Het gegevenssetprofiel dat u tijdens de implementatie van uw toepassing van Adobe wordt verstrekt bevat een reeks dossiers van de datasetconfiguratie die u kunt openen, uitgeven en opslaan gebruikend [!DNL Profile Manager].

Voor informatie over [!DNL Profile Manager], zie *de Gids van de Gebruiker van het Inzicht*.

<!--
c_addl_config_files.xml
-->

Hoewel niet vereist voor alle datasets, laten deze dossiers u toe om andere aspecten van het proces van de datasetconstructie te controleren:

* **Modus voor logverwerking.cfg:** in het  [!DNL Log Processing Mode.cfg] bestand kunt u de verwerking van gegevens in een gegevensset onderbreken, offline bronnen opgeven of de frequentie opgeven waarmee de werkbankserver de statusbestanden opslaat. Zie [Aanvullende configuratiebestanden](../../home/c-dataset-const-proc/c-add-config-files/c-add-config-files.md#concept-1afef4f88f1e467ab4326875fd1d3004).

* **Server.cfg:** Het  [!DNL Server.cfg] dossier specificeert de standaardgrootte van het gegevensgeheime voorgeheugen (in bytes) voor gegevens werkbankmachines die met de server van de gegevenswerkbank verbinden. Zie [Aanvullende configuratiebestanden](../../home/c-dataset-const-proc/c-add-config-files/c-add-config-files.md#concept-1afef4f88f1e467ab4326875fd1d3004).

* **Transform.cfg en Transform Mode.cfg:** Deze bestanden zijn alleen beschikbaar als u een licentie hebt verkregen voor de functionaliteit voor gegevenstransformatie die u kunt gebruiken met uw Adobe-toepassing. Het [!DNL Transform.cfg]-bestand bevat de parameters die de logbronnen en gegevenstransformaties voor transformatiefunctionaliteit definiëren. Met de transformaties die u definieert, worden de brongegevens gemanipuleerd en uitgevoerd in een indeling die u opgeeft. Het [!DNL Insight Transform Mode.cfg] dossier laat u toe om verwerking van gegevens in een dataset te pauzeren, off-line bronnen te specificeren, of de frequentie te specificeren waarbij de Server van het Inzicht die transformatiefunctionaliteit in werking stelt zijn staatsdossiers bewaart. Zie [Transformatiefunctionaliteit](https://docs.adobe.com/content/help/en/data-workbench/using/server-admin-install/transform/t-config-tfm.html).

<!--
c_next_steps.xml
-->

Voor informatie over specifieke taken van de datasetconfiguratie, gebruik de lijst hieronder om van de taken van belang van u de plaats te bepalen en te lezen:

<table id="table_394CFB5135274545B5DA37952EC6943E"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Als u... </th> 
   <th colname="col2" class="entry"> Zie... </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Logbronnen definiëren </p> </td> 
   <td colname="col2"> <p><a href="../../home/c-dataset-const-proc/c-log-proc-config-file/c-log-sources.md#concept-6714c720fac044cbb9af003bf401b2ea"> Logbronnen  </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Bepaal welke logboekingangen de dataset tijdens logboekverwerking ingaan </p> </td> 
   <td colname="col2"> <p> <a href="../../home/c-dataset-const-proc/c-log-proc-config-file/c-info-log-proc-param.md#concept-41bd49bf6b64442d91c232ec67529a3d"> Gegevensfilters</a> </p> <p> <a href="../../home/c-dataset-const-proc/c-log-proc-config-file/c-info-log-proc-param.md#concept-ecaff95cee4e40bc90f81e099c5fc934"> Voorwaarde logbestandvermelding</a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>De splitsing van tracking-id's met grote hoeveelheden gebeurtenisgegevens inschakelen </p> </td> 
   <td colname="col2"> <p><a href="../../home/c-dataset-const-proc/c-log-proc-config-file/c-info-log-proc-param.md#concept-64b416bbe42f4d689f90df246f7f7caf"> Key Splitsen</a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Een Insight Server configureren om als een bestandsservereenheid te worden uitgevoerd </p> </td> 
   <td colname="col2"> <p><a href="../../home/c-dataset-const-proc/c-log-proc-config-file/c-ins-svr-file-svr-unit.md#concept-995abff3fce34e439fb3f7f47191c80d"> Een Insight Server-bestandsservereenheid configureren  </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Vorm een Server van het Inzicht om als gecentraliseerde normaliseringsserver in werking te stellen </p> </td> 
   <td colname="col2"> <p><a href="../../home/c-dataset-const-proc/c-log-proc-config-file/c-ins-svr-file-svr-unit.md#concept-995abff3fce34e439fb3f7f47191c80d"> Een Insight Server-bestandsservereenheid configureren  </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>De tijdzone instellen die moet worden gebruikt voor het maken van tijdafmetingen en het maken van tijdconversies </p> </td> 
   <td colname="col2"> <p><a href="../../home/c-dataset-const-proc/c-trans-config-file/c-spec-trans-param/c-time-zones.md#concept-9cf16b1cb4874f7d85e1dd950fdb4956"> Tijdzones </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Breng kleine veranderingen in de dossiers van de datasetconfiguratie inbegrepen met de interne profielen aan die door Adobe worden verstrekt </p> </td> 
   <td colname="col2"> <p><a href="../../home/c-dataset-const-proc/c-dataset-inc-files/c-work-dataset-inc-files/t-edit-ex-dataset-inc-files.md#task-456c04e38ebc425fb35677a6bb6aa077"> Bestaande gegevensset met include-bestanden bewerken  </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Geef nieuwe gegevensvelden op die moeten worden doorgegeven van logverwerking naar transformatie </p> </td> 
   <td colname="col2"> <p> <a href="../../home/c-dataset-const-proc/c-dataset-inc-files/c-work-dataset-inc-files/t-create-new-dataset-inc-files.md#task-b29f30605c374a6ca747ac843337b06e"> Nieuwe gegevensset maken met include-bestanden  </a> </p> <p> <a href="../../home/c-dataset-const-proc/c-dataset-inc-files/c-types-dataset-inc-files/c-log-proc-dataset-inc-files/c-log-proc-dataset-inc-files.md#concept-999475a22519432e98844622ca95b6ab"> Gegevensset logbestandsverwerking inclusief bestanden  </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Transformaties definiëren </p> </td> 
   <td colname="col2"> <p> <a href="../../home/c-dataset-const-proc/c-data-trans/c-abt-transf.md"> Gegevenstransformaties  </a> </p> <p> <a href="../../home/c-dataset-const-proc/c-dataset-inc-files/c-work-dataset-inc-files/t-create-new-dataset-inc-files.md#task-b29f30605c374a6ca747ac843337b06e"> Nieuwe gegevensset maken met include-bestanden  </a> </p> <p> <a href="../../home/c-dataset-const-proc/c-dataset-inc-files/c-types-dataset-inc-files/c-trans-dataset-inc-files.md#concept-c64aa78ed9ce40b8a0f4932c82ff5ace"> Gegevensset transformatie bevat bestanden  </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Uitgebreide afmetingen maken </p> </td> 
   <td colname="col2"> <p> <a href="../../home/c-dataset-const-proc/c-ex-dim/c-abt-ex-dim.md"> Uitgebreide Dimension  </a> </p> <p> <a href="../../home/c-dataset-const-proc/c-dataset-inc-files/c-work-dataset-inc-files/t-create-new-dataset-inc-files.md#task-b29f30605c374a6ca747ac843337b06e"> Nieuwe gegevensset maken met include-bestanden  </a> </p> <p> <a href="../../home/c-dataset-const-proc/c-dataset-inc-files/c-types-dataset-inc-files/c-trans-dataset-inc-files.md#concept-c64aa78ed9ce40b8a0f4932c82ff5ace"> Gegevensset transformatie bevat bestanden  </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Parameters definiëren die tijdens de logverwerking of transformatie moeten worden gebruikt </p> </td> 
   <td colname="col2"> <p><a href="../../home/c-dataset-const-proc/c-dataset-inc-files/c-def-param-dataset-inc-files/c-def-param-dataset-inc-files.md#concept-5ad06acc8dc44bf2a99643fafdd56b50"> Parameters definiëren in gegevensset met include-bestanden  </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Leer over de interfaces van het Inzicht die u toelaten om uw dataset te controleren of te beheren </p> </td> 
   <td colname="col2"> <p><a href="../../home/c-dataset-const-proc/c-dataset-config-tools/c-dataset-config-int/c-dataset-config-int.md#concept-0ea33a52ce234ec8951e7b4430fbc5ab"> Werken met de interfaces van de Configuratie van Dataset  </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Verberg bepaalde uitgebreide afmetingen zodat deze niet worden weergegeven in het menu Dimensie in Inzicht </p> </td> 
   <td colname="col2"> <p><a href="../../home/c-dataset-const-proc/c-dataset-config-tools/c-hide-dataset-comp/c-hide-dataset-comp.md#concept-50d9a004736f42f6b0aa7cde0d6148ff"> Dataset-componenten verbergen  </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Overschrijf bepaalde dossiers van de datasetconfiguratie in een profiel dat u niet kunt of wilt wijzigen </p> </td> 
   <td colname="col2"> <p><a href="../../home/c-dataset-const-proc/c-dataset-config-tools/c-hide-dataset-comp/c-hide-dataset-comp.md#concept-50d9a004736f42f6b0aa7cde0d6148ff"> Dataset-componenten verbergen  </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Uw gegevensset opnieuw verwerken </p> </td> 
   <td colname="col2"> <p><a href="../../home/c-dataset-const-proc/c-reproc-retrans/c-unst-reproc-retrans.md"> Opwerking en heromzetting  </a> </p> </td> 
  </tr> 
 </tbody> 
</table>
