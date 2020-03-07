---
description: De dataset van de Transformatie omvat dossier voor een geërft profiel bevat parameters verbonden aan de transformatiefase van datasetconstructie.
solution: Analytics
title: Dataset transformatie bevat bestanden
topic: Data workbench
uuid: 46756f68-843c-4b0d-a79e-f107ef85db6c
translation-type: tm+mt
source-git-commit: 27600561841db3705f4eee6ff0aeb8890444bbc9

---


# Dataset transformatie bevat bestanden{#transformation-dataset-include-files}

De dataset van de Transformatie omvat dossier voor een geërft profiel bevat parameters verbonden aan de transformatiefase van datasetconstructie.

De eerste lijn van het dossier bepaalt een type [!DNL TransformationInclude] dat de Uitgebreide Dimensies, de Parameters, het Herproces, het Stadium, en de parameters van Transformaties steunt. Alle andere parameters moeten in het [!DNL Transformation.cfg] dossier in de folder van de Dataset van het datasetprofiel worden bepaald.

Met inbegrip van parameters buiten Uitgebreide Afmetingen, Parameters, Herproces, Stadium, en Transformaties in een [!DNL Transformation Dataset Include] dossier produceert fouten.

U kunt een [!DNL Transformation Dataset Include] dossier om het even wat noemen u wilt, maar zijn dossieruitbreiding moet zijn [!DNL .cfg]. Het dossier moet binnen de *geërfte profielnaam*\Dataset\Transformation directory worden opgeslagen. Omdat de dossiers recursief tijdens de transformatiefase van datasetconstructie worden geladen, kunt u de [!DNL Transformation Dataset Include] dossiers op om het even welk niveau binnen de folder opslaan (bijvoorbeeld, *geërfte profielnaam*\Dataset\Transformation\*mapnaam* \*include dossier - noem*.cfg).

>[!NOTE]
>
>Vele web-specifieke configuratieparameters voor Plaats worden bepaald in [!DNL Transformation Dataset Include] dossiers. Voor informatie over deze parameters, zie de Montages van de [Configuratie voor de Gegevens](../../../../home/c-dataset-const-proc/c-config-web-data/c-config-web-data.md#concept-9a306b65483a484bb3f6f3c1d7e77519)van het Web.

De volgende lijst beschrijft de parameters die in een [!DNL Transformation Dataset Include] dossier beschikbaar zijn:

<table id="table_7BD343888D9145BCBA889B531A4D18F8"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Parameter </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Uitgebreide afmetingen </td> 
   <td colname="col2"> Optioneel. Bepaalt de uitgebreide afmetingen. Zie <a href="../../../../home/c-dataset-const-proc/c-ex-dim/c-abt-ex-dim.md"> Uitgebreide afmetingen</a>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Parameters </td> 
   <td colname="col2"> Optioneel. Een variabele die u in andere configuratieparameters kunt van verwijzingen voorzien. Voor meer informatie, zie het <a href="../../../../home/c-dataset-const-proc/c-dataset-inc-files/c-def-param-dataset-inc-files/c-def-param-dataset-inc-files.md#concept-5ad06acc8dc44bf2a99643fafdd56b50"> Bepalen van Parameters in Dataset Dossiers</a>omvatten. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Opnieuw verwerken </td> 
   <td colname="col2"> <p>Optioneel. Om het even welk karakter of combinatie karakters kunnen hier zijn ingegaan. Het veranderen van deze parameter en het bewaren van het dossier stelt gegevensretransformatie in werking. </p> <p> Voor informatie over het opnieuw verwerken van uw gegevens, zie <a href="../../../../home/c-dataset-const-proc/c-reproc-retrans/c-unst-reproc-retrans.md"> Opwerking en Herschikking</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Stadium </td> 
   <td colname="col2"> <p>Optioneel. De naam van het verwerkingsstadium dat op deze Dataset van de <span class="wintitle"> Transformatie van toepassing is omvat</span> dossier. De verwerkingsstadia worden bepaald in de parameter van Staven in het <span class="filepath"> dossier Transformation.cfg</span> . </p> <p> <p>Opmerking: Wanneer u een Stadium specificeert, moet de naam van het Stadium precies de naam aanpassen die in de parameter van Fasen in het <span class="filepath"> Transformation.cfg</span> - dossier voor het datasetprofiel vermeld is. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Transformaties </td> 
   <td colname="col2"> Optioneel. Bepaalt de gegevenstransformaties die tijdens transformatie moeten worden toegepast. Voor informatie over de beschikbare transformatietypen, zie de Transformaties <a href="../../../../home/c-dataset-const-proc/c-data-trans/c-abt-transf.md"></a>van Gegevens. </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Voor beschrijvingen van de parameters in het [!DNL Transformation.cfg] dossier, zie het Dossier van de Configuratie van de [Transformatie](../../../../home/c-dataset-const-proc/c-trans-config-file/c-abt-trans-config-file.md).

U zou de volgende punten in mening moeten houden wanneer u met [!DNL Transformation Dataset Include] dossiers werkt:

* Het veranderen van om het even welke parameters in dit dossier vereist retransformation van de gegevens.
* [!DNL CrossRows], [!DNL ODBCLookup], [!DNL Sessionize], en [!DNL AppendURI] transformaties werken slechts wanneer bepaald in een [!DNL Transformation Dataset Configuration] dossier. Voor informatie over deze transformaties, zie de Transformaties van [Gegevens](../../../../home/c-dataset-const-proc/c-data-trans/c-abt-transf.md).

* U kunt om het even welke hierboven beschreven parameters aan het [!DNL Transformation Dataset Include] dossier toevoegen door het dossier in Blocnote te openen en uit te geven. Om het even welke veranderingen u aanbrengt en opslaat verschijnen wanneer u het dossier in gegevenswerkbank heropent. Wanneer het toevoegen van een nieuwe parameter, gebruik de Ruimtesleutel (niet de sleutel van het Lusje) om twee (2) ruimten rechts van het vorige rubriekniveau te kartelen.

Als u aan de de gegevensdienst van Adobe [!DNL IP Geo-location] of [!DNL IP Geo-intelligence] intekent, verstrekt Adobe u van een intern profiel dat uit een reeks gegevenstransformaties en uitgebreide afmetingen bestaat die specifiek voor de datadienst worden gecreeerd. De transformaties en de afmetingen worden bepaald in [!DNL Transformation Dataset Include] dossiers die in de folder van de Dataset van het interne profiel inbegrepen zijn. Raadpleeg de gebruikershandleiding bij de [!DNL IP Geo-location] gegevenswerkbank voor instructies voor het installeren van het interne profiel voor de [!DNL IP Geo-intelligence] of *gegevensservice*.
