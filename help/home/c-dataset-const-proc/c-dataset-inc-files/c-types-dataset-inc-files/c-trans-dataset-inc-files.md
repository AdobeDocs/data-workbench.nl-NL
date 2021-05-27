---
description: Het gegevensbestand van de Dataset van de Transformatie omvat dossier voor een geërft profiel bevat parameters verbonden aan de transformatiefase van datasetconstructie.
title: Gegevensset transformatie bevat bestanden
uuid: 46756f68-843c-4b0d-a79e-f107ef85db6c
exl-id: 58793f82-162a-4d43-aea9-163716c82db6
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '529'
ht-degree: 1%

---

# Gegevensset transformatie bevat bestanden{#transformation-dataset-include-files}

Het gegevensbestand van de Dataset van de Transformatie omvat dossier voor een geërft profiel bevat parameters verbonden aan de transformatiefase van datasetconstructie.

De eerste regel van het bestand definieert een type [!DNL TransformationInclude] dat de parameters Uitgebreide Dimension, Parameters, Opnieuw verwerken, Werkgebied en Transformaties ondersteunt. Alle andere parameters moeten in het [!DNL Transformation.cfg] dossier in de folder van de Dataset van het datasetprofiel worden bepaald.

Als u andere parameters dan Extended Dimension, Parameters, Opnieuw verwerken, Stage en Transformaties opneemt in een [!DNL Transformation Dataset Include]-bestand, worden er fouten gegenereerd.

U kunt een [!DNL Transformation Dataset Include] dossier om het even wat noemen u wilt, maar zijn dossieruitbreiding moet [!DNL .cfg] zijn. Het bestand moet worden opgeslagen in de *overgenomen profielnaam*\Dataset\Transformation directory. Omdat de bestanden recursief worden geladen tijdens de transformatiefase van de constructie van gegevenssets, kunt u de [!DNL Transformation Dataset Include]-bestanden op elk niveau in de map opslaan (bijvoorbeeld *overgeërfde profielnaam*\Dataset\Transformation\*mapnaam*\*include-bestandsnaam*.cfg).

>[!NOTE]
>
>Veel webspecifieke configuratieparameters voor Site worden gedefinieerd in [!DNL Transformation Dataset Include]-bestanden. Voor informatie over deze parameters, zie [Montages van de Configuratie voor de Gegevens van het Web](../../../../home/c-dataset-const-proc/c-config-web-data/c-config-web-data.md#concept-9a306b65483a484bb3f6f3c1d7e77519).

In de volgende tabel worden de parameters beschreven die beschikbaar zijn in een [!DNL Transformation Dataset Include]-bestand:

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
   <td colname="col2"> Optioneel. Een variabele waarnaar u in andere configuratieparameters kunt verwijzen. Zie <a href="../../../../home/c-dataset-const-proc/c-dataset-inc-files/c-def-param-dataset-inc-files/c-def-param-dataset-inc-files.md#concept-5ad06acc8dc44bf2a99643fafdd56b50"> Parameters definiëren in Dataset Inclusief bestanden</a> voor meer informatie. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Opnieuw verwerken </td> 
   <td colname="col2"> <p>Optioneel. Elk teken of elke combinatie van tekens kan hier worden ingevoerd. Als u deze parameter wijzigt en het bestand opslaat, worden de gegevens opnieuw getransformeerd. </p> <p> Zie <a href="../../../../home/c-dataset-const-proc/c-reproc-retrans/c-unst-reproc-retrans.md"> Opwerking en hertransformatie</a> voor informatie over het opnieuw verwerken van uw gegevens. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Werkgebied </td> 
   <td colname="col2"> <p>Optioneel. De naam van het verwerkingswerkgebied dat van toepassing is op dit <span class="wintitle">-bestand voor de gegevensset voor transformatie Include</span>. De verwerkingsstadia worden gedefinieerd in de parameter Stages in het bestand <span class="filepath"> Transformation.cfg</span>. </p> <p> <p>Opmerking: Wanneer u een werkgebied opgeeft, moet de naam van het werkgebied exact overeenkomen met de naam die wordt vermeld in de parameter Stage in het bestand <span class="filepath"> Transformation.cfg</span> voor het gegevenssetprofiel. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Transformaties </td> 
   <td colname="col2"> Optioneel. Definieert de gegevenstransformaties die moeten worden toegepast tijdens de transformatie. Voor informatie over de beschikbare transformatietypen, zie <a href="../../../../home/c-dataset-const-proc/c-data-trans/c-abt-transf.md"> Transformaties van Gegevens</a>. </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Zie [Transformation Configuration File](../../../../home/c-dataset-const-proc/c-trans-config-file/c-abt-trans-config-file.md) voor beschrijvingen van de parameters in het [!DNL Transformation.cfg]-bestand.

Houd rekening met de volgende punten wanneer u met [!DNL Transformation Dataset Include] bestanden werkt:

* Als u een van de parameters in dit bestand wijzigt, moeten de gegevens opnieuw worden getransformeerd.
* [!DNL CrossRows],  [!DNL ODBCLookup],  [!DNL Sessionize]en  [!DNL AppendURI] transformaties werken alleen wanneer deze in een  [!DNL Transformation Dataset Configuration] bestand zijn gedefinieerd. Voor informatie over deze transformaties, zie [Transformaties van Gegevens](../../../../home/c-dataset-const-proc/c-data-trans/c-abt-transf.md).

* U kunt om het even welke hierboven beschreven parameters aan het [!DNL Transformation Dataset Include] dossier toevoegen door het dossier in Blocnote te openen en uit te geven. Wijzigingen die u aanbrengt en opslaat, worden weergegeven wanneer u het bestand opnieuw opent in de werkbank Gegevens. Wanneer u een nieuwe parameter toevoegt, gebruikt u de toets Ruimte (niet de Tab-toets) om twee (2) spaties rechts van het vorige kopniveau te laten inspringen.

Als u zich abonneert op de gegevensservice [!DNL IP Geo-location] of [!DNL IP Geo-intelligence], verschaft Adobe u een intern profiel dat bestaat uit een set gegevenstransformaties en uitgebreide dimensies die specifiek voor de gegevensservice zijn gemaakt. De transformaties en afmetingen worden gedefinieerd in [!DNL Transformation Dataset Include]-bestanden die worden opgenomen in de map Dataset van het interne profiel. Raadpleeg de *Handleiding voor Data Workbench* voor instructies voor het installeren van het interne profiel voor de [!DNL IP Geo-location]- of [!DNL IP Geo-intelligence]-gegevensservice.
