---
description: De Dataset van de Verwerking van het Logboek omvat dossier voor een geërft profiel bevat parameters verbonden aan de fase van de logboekverwerking van datasetconstructie.
solution: Analytics
title: Gegevensverzameling logverwerking bevat bestanden
topic: Data workbench
uuid: 8bf99c9a-f674-4a07-bb3e-de0d9efc9716
translation-type: tm+mt
source-git-commit: 27600561841db3705f4eee6ff0aeb8890444bbc9

---


# Gegevensverzameling logverwerking bevat bestanden{#log-processing-dataset-include-files}

De Dataset van de Verwerking van het Logboek omvat dossier voor een geërft profiel bevat parameters verbonden aan de fase van de logboekverwerking van datasetconstructie.

De eerste lijn van een [!DNL Log Processing Dataset Include] dossier bepaalt een type [!DNL LogProcessingInclude] dat de de Groepen van de Decoder, Gebieden, Voorwaarde van de Ingang van het Logboek, Parameters, het Herproces, Stadium, en parameters van Transformaties steunt. Alle andere parameters voor logboekverwerking moeten in het [!DNL Log Processing.cfg] dossier in de folder van de Dataset van het datasetprofiel worden bepaald. U kunt een [!DNL Log Processing Dataset Include] dossier om het even wat noemen u wilt, maar zijn dossieruitbreiding moet zijn [!DNL .cfg]. Het dossier moet binnen de *geërfte profielnaam*\Dataset\Log Processing directory worden opgeslagen. Omdat de dossiers recursief tijdens de fase van de logboekverwerking van datasetconstructie worden geladen, kunt u de [!DNL Log Processing Dataset Include] dossiers op om het even welk niveau binnen de folder opslaan (bijvoorbeeld, *geërfte profielnaam*\Dataset\Log Processing\*folder* \*include dossier - noem*.cfg).

>[!NOTE]
>
>Vele web-specifieke configuratieparameters voor Plaats worden bepaald in [!DNL Log Processing Dataset Include] dossiers. Voor informatie over deze parameters, zie de Montages van de [Configuratie voor de Gegevens](../../../../../home/c-dataset-const-proc/c-config-web-data/c-config-web-data.md#concept-9a306b65483a484bb3f6f3c1d7e77519)van het Web.

<table id="table_E2112652CCD443E889A529EEDC4ADF1C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Parameter </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Decodergroepen </td> 
   <td colname="col2"> <p>Vereist als u de bronnen van het logboekdossier of van het het dossierlogboek van XML in het <span class="filepath"> Logboek Processing.cfg</span> - dossier hebt bepaald. Het tekstdossier of de decoders van XML dat u bepaalt om gebieden van gegevens uit logboekdossier en het logboekbronnen van XML te halen. </p> <p> <b>Om een nieuwe decodergroep toe te voegen</b> 
     <ul id="ul_54087499003C48C8B0AD9660A2F46EA9"> 
      <li id="li_E361861E61D246DDB3964C97CC5187E9"> Klik de Groep <span class="uicontrol"> van de</span> Decoder met de rechtermuisknop aan en de klik <span class="uicontrol"> voegt nieuw</span> &gt; <span class="uicontrol"> TextFileDecoderGroup</span> of <span class="uicontrol"> XMLDecoderGroup</span>toe. </li> 
      <li id="li_B2D61A0763AD4FEDB619BF9550EF4602"> In de parameter van de Naam voor de nieuwe groep, ga de gewenste naam van de decodergroep in. </li> 
     </ul> </p> <p> <p>Opmerking:  Wanneer u een Groep van de Decoder in het dossier van het <span class="filepath"> Logboek Processing.cfg</span> voor het datasetprofiel specificeert, moet de naam precies de naam aanpassen die u hier ingaat. Voor meer informatie, zie de Dossiers <a href="../../../../../home/c-dataset-const-proc/c-log-proc-config-file/c-log-sources.md#concept-3d4fb817c057447d90f166b1183b461e"> van het</a>Logboek. </p> </p> <p> Voor informatie over de decoders die u voor elke groep kunt bepalen, zie de Groepen <a href="../../../../../home/c-dataset-const-proc/c-dataset-inc-files/c-types-dataset-inc-files/c-log-proc-dataset-inc-files/c-text-file-dec-groups.md#concept-0db34988e17c41bfb1797f1d8e78aabd"> van de Decoder van het Dossier van de</a> Tekst of de Groepen <a href="../../../../../home/c-dataset-const-proc/c-dataset-inc-files/c-types-dataset-inc-files/c-log-proc-dataset-inc-files/c-xml-dec-grps.md#concept-5eda5ab253724674832f6951e2a0d1c3"> van de Decoder van XML</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Gebieden </td> 
   <td colname="col2"> <p>Maakt een lijst van gebieden die in de Bronnen <span class="wintitle"> van het</span> Logboek of <span class="wintitle"> Transformaties</span> in een dossier van de Configuratie <span class="wintitle"> van de Dataset van de Verwerking van het</span> Logboek maar gebruikt in transformaties, voorwaarden, of uitgebreide afmetingen in een dossier van de Configuratie <span class="wintitle"> van de Dataset van de</span> Transformatie worden bepaald moet hier worden vermeld. </p> <p> Elk gebied hieronder moet in één of andere Dataset van de Verwerking van het <span class="wintitle"> Logboek worden vermeld omvat</span> dossier: 
     <ul id="ul_D1BB18A80D874C0B9B54DA361698EB30"> 
      <li id="li_7E8B5B697BDA408DBE10D9A63AF295AC"> x-trackingid </li> 
      <li id="li_F5DEE90A596A4A1C86AF874653C4048C"> x-timestamp </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Status voor logboekinvoer </td> 
   <td colname="col2"> <p>Optioneel. Bepaalt de regels waardoor de logboekingangen voor opneming in de dataset worden overwogen. Zie <a href="../../../../../home/c-dataset-const-proc/c-log-proc-config-file/c-info-log-proc-param.md#concept-ecaff95cee4e40bc90f81e099c5fc934"> Log Entry Condition</a>. </p> <p> <p>Opmerking:  Om in de dataset te worden omvat, moet een logboekingang aan de Voorwaarde <span class="wintitle"> van de Ingang van het</span> Logboek in het <span class="filepath"> Logboek Processing.cfg</span> - dossier en in elke Dataset van de Verwerking van het <span class="wintitle"> Logboek voldoen omvat</span> dossier. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Parameters </td> 
   <td colname="col2"> Optioneel. Een variabele die u in andere configuratieparameters kunt van verwijzingen voorzien. Voor meer informatie, zie het <a href="../../../../../home/c-dataset-const-proc/c-dataset-inc-files/c-def-param-dataset-inc-files/c-def-param-dataset-inc-files.md#concept-5ad06acc8dc44bf2a99643fafdd56b50"> Bepalen van Parameters in Dataset Dossiers</a>omvatten. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Opnieuw verwerken </td> 
   <td colname="col2"> <p>Optioneel. Om het even welk karakter of combinatie karakters kunnen hier zijn ingegaan. Het veranderen van deze parameter en het opslaan van het dossier in de server van de gegevenswerkbank stelt gegevensopwerking in werking. </p> <p> Voor informatie over het opnieuw verwerken van uw gegevens, zie <a href="../../../../../home/c-dataset-const-proc/c-reproc-retrans/c-unst-reproc-retrans.md"> Opwerking en Herschikking</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Stadium </td> 
   <td colname="col2"> <p>Optioneel. De naam van het verwerkingsstadium dat op deze Dataset van de Verwerking van het <span class="wintitle"> Logboek van toepassing is omvat</span> dossier. De verwerkingsstadia worden bepaald in de parameter van Staven in het dossier van het <span class="filepath"> Logboek Processing.cfg</span> . </p> <p> <p>Opmerking:  Wanneer u een Stadium specificeert, moet de naam van het Stadium precies de naam aanpassen die in de parameter van Staven in het dossier van het <span class="filepath"> Logboek Processing.cfg</span> voor het datasetprofiel vermeld is. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Transformaties </td> 
   <td colname="col2"> Optioneel. Bepaalt de gegevenstransformaties die tijdens logboekverwerking moeten worden toegepast. Voor informatie over de beschikbare transformatietypen, zie de Transformaties <a href="../../../../../home/c-dataset-const-proc/c-data-trans/c-abt-transf.md"></a>van Gegevens. </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Voor beschrijvingen van de parameters in het [!DNL Log Processing.cfg] dossier, zie het Dossier van de Configuratie van de [Verwerking van het Logboek](../../../../../home/c-dataset-const-proc/c-log-proc-config-file/c-abt-log-proc-config-file.md).

U zou de volgende punten in mening moeten houden wanneer u met [!DNL Log Processing Dataset Include] dossiers werkt:

* Het veranderen van om het even welke parameters in dit dossier vereist opwerking van alle gegevens.
* U kunt om het even welke hierboven beschreven parameters aan het [!DNL Log Processing Dataset Include] dossier toevoegen door het dossier in Blocnote te openen en uit te geven. Om het even welke veranderingen u aanbrengt en opslaat verschijnen wanneer u het dossier in gegevenswerkbank heropent. Wanneer het toevoegen van een nieuwe parameter, gebruik de Ruimtesleutel (niet de sleutel van het Lusje) om twee (2) ruimten rechts van het vorige rubriekniveau te kartelen.

