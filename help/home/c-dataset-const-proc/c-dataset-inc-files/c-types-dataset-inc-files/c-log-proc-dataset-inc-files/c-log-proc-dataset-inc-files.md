---
description: Het dossier van Dataset van de Verwerking van het Logboek omvat voor een geërft profiel bevat parameters verbonden aan de fase van de logboekverwerking van datasetconstructie.
title: Gegevensset logbestandsverwerking inclusief bestanden
uuid: 8bf99c9a-f674-4a07-bb3e-de0d9efc9716
exl-id: 06d8046d-6bac-4ccd-bcef-06f7c9ec7619
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '660'
ht-degree: 0%

---

# Gegevensset logbestandsverwerking inclusief bestanden{#log-processing-dataset-include-files}

{{eol}}

Het dossier van Dataset van de Verwerking van het Logboek omvat voor een geërft profiel bevat parameters verbonden aan de fase van de logboekverwerking van datasetconstructie.

De eerste regel van een [!DNL Log Processing Dataset Include] bestand definieert een type [!DNL LogProcessingInclude] die de Decoderingsgroepen, de Gebieden, Voorwaarde van de Ingang van het Logboek, Parameters, Herproces, Stadium, en de parameters van Transformaties steunt. Alle andere parameters voor logverwerking moeten worden gedefinieerd in de [!DNL Log Processing.cfg] bestand in de map DataSet van het profiel van de gegevensset. U kunt een [!DNL Log Processing Dataset Include] bestand alles wat u wilt, maar de bestandsextensie moet [!DNL .cfg]. Het bestand moet in het *overgenomen profielnaam*\Dataset\Log Processing directory. Omdat de dossiers recursief tijdens de fase van de logboekverwerking van datasetbouw worden geladen, kunt u opslaan [!DNL Log Processing Dataset Include] bestanden op elk niveau in de map (bijvoorbeeld *overgenomen profielnaam*\Dataset\Log Processing\*mapnaam*\*bestandsnaam*.cfg opnemen).

>[!NOTE]
>
>Veel webspecifieke configuratieparameters voor Site worden gedefinieerd in [!DNL Log Processing Dataset Include] bestanden. Voor informatie over deze parameters raadpleegt u [Configuratie-instellingen voor webgegevens](../../../../../home/c-dataset-const-proc/c-config-web-data/c-config-web-data.md#concept-9a306b65483a484bb3f6f3c1d7e77519).

<table id="table_E2112652CCD443E889A529EEDC4ADF1C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Parameter </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Decoderingsgroepen </td> 
   <td colname="col2"> <p>Vereist als u logbestand- of XML-bestandslogbronnen hebt gedefinieerd in het dialoogvenster <span class="filepath"> Logverwerking.cfg</span> bestand. Het tekstbestand of de XML-decoders die u definieert om gegevensvelden te extraheren uit logbestanden en XML-logbronnen. </p> <p> <b>Een nieuwe decoderingsgroep toevoegen</b> 
     <ul id="ul_54087499003C48C8B0AD9660A2F46EA9"> 
      <li id="li_E361861E61D246DDB3964C97CC5187E9"> Klikken met rechtermuisknop <span class="uicontrol"> Decoderingsgroep</span> en klik op <span class="uicontrol"> Nieuw toevoegen</span> &gt; <span class="uicontrol"> TextFileDecoderGroup</span> of <span class="uicontrol"> XMLDecoderGroup</span>. </li> 
      <li id="li_B2D61A0763AD4FEDB619BF9550EF4602"> Voer in de parameter Naam voor de nieuwe groep de gewenste naam van de decoderingsgroep in. </li> 
     </ul> </p> <p> <p>Opmerking: Wanneer u een Decoderingsgroep opgeeft in het dialoogvenster <span class="filepath"> Logverwerking.cfg</span> bestand voor het gegevenssetprofiel, moet de naam exact overeenkomen met de naam die u hier invoert. Zie voor meer informatie <a href="../../../../../home/c-dataset-const-proc/c-log-proc-config-file/c-log-sources.md#concept-3d4fb817c057447d90f166b1183b461e"> Logbestanden</a>. </p> </p> <p> Voor informatie over de decoders die u voor elke groep kunt bepalen, zie <a href="../../../../../home/c-dataset-const-proc/c-dataset-inc-files/c-types-dataset-inc-files/c-log-proc-dataset-inc-files/c-text-file-dec-groups.md#concept-0db34988e17c41bfb1797f1d8e78aabd"> Decoderingsgroepen tekstbestand</a> of <a href="../../../../../home/c-dataset-const-proc/c-dataset-inc-files/c-types-dataset-inc-files/c-log-proc-dataset-inc-files/c-xml-dec-grps.md#concept-5eda5ab253724674832f6951e2a0d1c3"> XML-decoderingsgroepen</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Velden </td> 
   <td colname="col2"> <p>Hiermee geeft u velden weer die zijn gedefinieerd in <span class="wintitle"> Logbronnen</span> of <span class="wintitle"> Transformaties</span> in een <span class="wintitle"> Gegevensconfiguratie logverwerkingsdatabase</span> bestand, maar gebruikt in transformaties, voorwaarden of uitgebreide afmetingen in een <span class="wintitle"> Configuratie van gegevensset voor transformatie</span> bestand moet hier worden vermeld. </p> <p> Elk veld hieronder moet in sommige velden worden vermeld <span class="wintitle"> Gegevensset logbestandsverwerking opnemen</span> bestand: 
     <ul id="ul_D1BB18A80D874C0B9B54DA361698EB30"> 
      <li id="li_7E8B5B697BDA408DBE10D9A63AF295AC"> x-trackingid </li> 
      <li id="li_F5DEE90A596A4A1C86AF874653C4048C"> x-timestamp </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Voorwaarde logbestandvermelding </td> 
   <td colname="col2"> <p>Optioneel. Bepaalt de regels waardoor de logboekingangen voor opneming in de dataset worden overwogen. Zie <a href="../../../../../home/c-dataset-const-proc/c-log-proc-config-file/c-info-log-proc-param.md#concept-ecaff95cee4e40bc90f81e099c5fc934"> Voorwaarde logbestandvermelding</a>. </p> <p> <p>Opmerking: Om in de dataset te worden opgenomen, moet een logboekingang voldoen aan <span class="wintitle"> Voorwaarde logbestandvermelding</span> in de <span class="filepath"> Logverwerking.cfg</span> en in elke <span class="wintitle"> Gegevensset logbestandsverwerking opnemen</span> bestand. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Parameters </td> 
   <td colname="col2"> Optioneel. Een variabele waarnaar u in andere configuratieparameters kunt verwijzen. Zie voor meer informatie <a href="../../../../../home/c-dataset-const-proc/c-dataset-inc-files/c-def-param-dataset-inc-files/c-def-param-dataset-inc-files.md#concept-5ad06acc8dc44bf2a99643fafdd56b50"> Parameters definiëren in gegevensset met include-bestanden</a>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Opnieuw verwerken </td> 
   <td colname="col2"> <p>Optioneel. Elk teken of elke combinatie van tekens kan hier worden ingevoerd. Als u deze parameter wijzigt en het bestand opslaat op de gegevenswerkbankserver, worden de gegevens opnieuw verwerkt. </p> <p> Voor informatie over het opnieuw verwerken van uw gegevens raadpleegt u <a href="../../../../../home/c-dataset-const-proc/c-reproc-retrans/c-unst-reproc-retrans.md"> Opwerking en heromzetting</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Werkgebied </td> 
   <td colname="col2"> <p>Optioneel. De naam van het verwerkingsstadium dat op dit gebied van toepassing is <span class="wintitle"> Gegevensset logbestandsverwerking opnemen</span> bestand. De verwerkingsfasen worden gedefinieerd in de parameter Stadium in het dialoogvenster <span class="filepath"> Logverwerking.cfg</span> bestand. </p> <p> <p>Opmerking: Wanneer u een werkgebied opgeeft, moet de naam van het werkgebied exact overeenkomen met de naam die wordt vermeld in de parameter Stage in het dialoogvenster <span class="filepath"> Logverwerking.cfg</span> bestand voor het gegevenssetprofiel. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Transformaties </td> 
   <td colname="col2"> Optioneel. Bepaalt de gegevenstransformaties die tijdens logboekverwerking moeten worden toegepast. Voor informatie over de beschikbare transformatietypen raadpleegt u <a href="../../../../../home/c-dataset-const-proc/c-data-trans/c-abt-transf.md"> Gegevenstransformaties</a>. </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Voor beschrijvingen van de parameters in de [!DNL Log Processing.cfg] bestand, zie [Logboekverwerkingsconfiguratiebestand](../../../../../home/c-dataset-const-proc/c-log-proc-config-file/c-abt-log-proc-config-file.md).

Wanneer u met [!DNL Log Processing Dataset Include] bestanden:

* Als u een van de parameters in dit bestand wijzigt, moeten alle gegevens opnieuw worden verwerkt.
* U kunt alle hierboven beschreven parameters toevoegen aan de [!DNL Log Processing Dataset Include] door het bestand te openen en te bewerken in Kladblok. Wijzigingen die u aanbrengt en opslaat, worden weergegeven wanneer u het bestand opnieuw opent in de werkbank Gegevens. Wanneer u een nieuwe parameter toevoegt, gebruikt u de toets Ruimte (niet de Tab-toets) om twee (2) spaties rechts van het vorige kopniveau te laten inspringen.
