---
description: Het gegevensbestand van de Dataset van de Transformatie omvat dossier voor een geërft profiel bevat parameters verbonden aan de transformatiefase van datasetconstructie.
title: Gegevensset transformatie bevat bestanden
uuid: 46756f68-843c-4b0d-a79e-f107ef85db6c
exl-id: 58793f82-162a-4d43-aea9-163716c82db6
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '529'
ht-degree: 1%

---

# Gegevensset transformatie bevat bestanden{#transformation-dataset-include-files}

{{eol}}

Het gegevensbestand van de Dataset van de Transformatie omvat dossier voor een geërft profiel bevat parameters verbonden aan de transformatiefase van datasetconstructie.

De eerste regel van het bestand definieert een type [!DNL TransformationInclude] die de uitgebreide Dimension, Parameters, Opnieuw verwerken, Stadium, en de parameters van Transformaties steunt. Alle andere parameters moeten in [!DNL Transformation.cfg] bestand in de map DataSet van het profiel van de gegevensset.

Met inbegrip van andere parameters dan Uitgebreide Dimension, Parameters, Opnieuw verwerken, Stadium, en Transformaties in a [!DNL Transformation Dataset Include] bestand genereert fouten.

U kunt een [!DNL Transformation Dataset Include] bestand alles wat u wilt, maar de bestandsextensie moet [!DNL .cfg]. Het bestand moet in het *overgenomen profielnaam*\Dataset\Transformation directory. Omdat de dossiers recursief tijdens de transformatiefase van datasetbouw worden geladen, kunt u opslaan [!DNL Transformation Dataset Include] bestanden op elk niveau in de map (bijvoorbeeld *overgenomen profielnaam*\Dataset\Transformation\*mapnaam*\*bestandsnaam opnemen*.cfg).

>[!NOTE]
>
>Veel webspecifieke configuratieparameters voor Site worden gedefinieerd in [!DNL Transformation Dataset Include] bestanden. Voor informatie over deze parameters raadpleegt u [Configuratie-instellingen voor webgegevens](../../../../home/c-dataset-const-proc/c-config-web-data/c-config-web-data.md#concept-9a306b65483a484bb3f6f3c1d7e77519).

In de volgende tabel worden de parameters beschreven die beschikbaar zijn in een [!DNL Transformation Dataset Include] bestand:

<table id="table_7BD343888D9145BCBA889B531A4D18F8"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Parameter </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Uitgebreide Dimension </td> 
   <td colname="col2"> Optioneel. Hiermee definieert u de uitgebreide afmetingen. Zie <a href="../../../../home/c-dataset-const-proc/c-ex-dim/c-abt-ex-dim.md"> Uitgebreide Dimension</a>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Parameters </td> 
   <td colname="col2"> Optioneel. Een variabele waarnaar u in andere configuratieparameters kunt verwijzen. Zie voor meer informatie <a href="../../../../home/c-dataset-const-proc/c-dataset-inc-files/c-def-param-dataset-inc-files/c-def-param-dataset-inc-files.md#concept-5ad06acc8dc44bf2a99643fafdd56b50"> Parameters definiëren in gegevensset met include-bestanden</a>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Opnieuw verwerken </td> 
   <td colname="col2"> <p>Optioneel. Elk teken of elke combinatie van tekens kan hier worden ingevoerd. Als u deze parameter wijzigt en het bestand opslaat, worden de gegevens opnieuw getransformeerd. </p> <p> Voor informatie over het opnieuw verwerken van uw gegevens raadpleegt u <a href="../../../../home/c-dataset-const-proc/c-reproc-retrans/c-unst-reproc-retrans.md"> Opwerking en heromzetting</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Werkgebied </td> 
   <td colname="col2"> <p>Optioneel. De naam van het verwerkingsstadium dat op dit gebied van toepassing is <span class="wintitle"> Gegevensset transformatie inclusief</span> bestand. De verwerkingsfasen worden gedefinieerd in de parameter Stadium in het dialoogvenster <span class="filepath"> Transformation.cfg</span> bestand. </p> <p> <p>Opmerking: Wanneer u een werkgebied opgeeft, moet de naam van het werkgebied exact overeenkomen met de naam die wordt vermeld in de parameter Stage in het dialoogvenster <span class="filepath"> Transformation.cfg</span> bestand voor het gegevenssetprofiel. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Transformaties </td> 
   <td colname="col2"> Optioneel. Definieert de gegevenstransformaties die moeten worden toegepast tijdens de transformatie. Voor informatie over de beschikbare transformatietypen raadpleegt u <a href="../../../../home/c-dataset-const-proc/c-data-trans/c-abt-transf.md"> Gegevenstransformaties</a>. </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Voor beschrijvingen van de parameters in de [!DNL Transformation.cfg] bestand, zie [Configuratiebestand transformatie](../../../../home/c-dataset-const-proc/c-trans-config-file/c-abt-trans-config-file.md).

Wanneer u met [!DNL Transformation Dataset Include] bestanden:

* Als u een van de parameters in dit bestand wijzigt, moeten de gegevens opnieuw worden getransformeerd.
* [!DNL CrossRows], [!DNL ODBCLookup], [!DNL Sessionize], en [!DNL AppendURI] transformaties werken alleen wanneer ze zijn gedefinieerd in een [!DNL Transformation Dataset Configuration] bestand. Voor informatie over deze transformaties raadpleegt u [Gegevenstransformaties](../../../../home/c-dataset-const-proc/c-data-trans/c-abt-transf.md).

* U kunt alle hierboven beschreven parameters toevoegen aan de [!DNL Transformation Dataset Include] door het bestand te openen en te bewerken in Kladblok. Wijzigingen die u aanbrengt en opslaat, worden weergegeven wanneer u het bestand opnieuw opent in de werkbank Gegevens. Wanneer u een nieuwe parameter toevoegt, gebruikt u de toets Ruimte (niet de Tab-toets) om twee (2) spaties rechts van het vorige kopniveau te laten inspringen.

Als u zich abonneert op Adobe [!DNL IP Geo-location] of [!DNL IP Geo-intelligence] Adobe, de gegevensdienst, voorziet u van een intern profiel dat uit een reeks gegevenstransformaties en uitgebreide dimensies bestaat die specifiek voor de datadienst worden gecreeerd. De transformaties en afmetingen zijn gedefinieerd in [!DNL Transformation Dataset Include] bestanden die zijn opgenomen in de map Dataset van het interne profiel. Voor instructies voor het installeren van het interne profiel voor de [!DNL IP Geo-location] of [!DNL IP Geo-intelligence] de datadienst, zie *Gebruikershandleiding voor Data Workbench*.
