---
description: Het dossier van Dataset van de Verwerking van het Logboek omvat voor een geërft profiel bevat parameters verbonden aan de fase van de logboekverwerking van datasetconstructie.
title: Gegevensset logbestandsverwerking inclusief bestanden
uuid: 8bf99c9a-f674-4a07-bb3e-de0d9efc9716
exl-id: 06d8046d-6bac-4ccd-bcef-06f7c9ec7619
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '660'
ht-degree: 0%

---

# Gegevensset van logverwerkingsdatabase bevat bestanden{#log-processing-dataset-include-files}

Het dossier van Dataset van de Verwerking van het Logboek omvat voor een geërft profiel bevat parameters verbonden aan de fase van de logboekverwerking van datasetconstructie.

De eerste regel van een [!DNL Log Processing Dataset Include]-bestand definieert een type [!DNL LogProcessingInclude] dat de parameters Decoderingsgroepen, Velden, Voorwaarde logbestandvermelding, Parameters, Opnieuw verwerken, Werkgebied en Transformaties ondersteunt. Alle andere parameters voor logboekverwerking moeten in het [!DNL Log Processing.cfg] dossier in de folder van de Dataset van het gegevenssetprofiel van de dataset worden bepaald. U kunt een [!DNL Log Processing Dataset Include] dossier om het even wat noemen u wilt, maar zijn dossieruitbreiding moet [!DNL .cfg] zijn. Het bestand moet worden opgeslagen in de *overgenomen profielnaam*\Dataset\Log Processing directory. Omdat de bestanden recursief worden geladen tijdens de verwerkingsfase van het logbestand van de gegevenssetconstructie, kunt u de [!DNL Log Processing Dataset Include]-bestanden op elk niveau in de map opslaan (bijvoorbeeld *overgenomen profielnaam*\Dataset\Log Processing\*mapnaam*\*bestandsnaam*.cfg opnemen).

>[!NOTE]
>
>Veel webspecifieke configuratieparameters voor Site worden gedefinieerd in [!DNL Log Processing Dataset Include]-bestanden. Voor informatie over deze parameters, zie [Montages van de Configuratie voor de Gegevens van het Web](../../../../../home/c-dataset-const-proc/c-config-web-data/c-config-web-data.md#concept-9a306b65483a484bb3f6f3c1d7e77519).

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
   <td colname="col2"> <p>Vereist als u logbestand- of XML-bestandslogbronnen hebt gedefinieerd in het bestand <span class="filepath"> Log Processing.cfg</span>. Het tekstbestand of de XML-decoders die u definieert om gegevensvelden te extraheren uit logbestanden en XML-logbronnen. </p> <p> <b>Een nieuwe decoderingsgroep toevoegen</b> 
     <ul id="ul_54087499003C48C8B0AD9660A2F46EA9"> 
      <li id="li_E361861E61D246DDB3964C97CC5187E9"> Klik met de rechtermuisknop op <span class="uicontrol"> Decoderingsgroep</span> en klik op <span class="uicontrol"> Nieuwe </span> &gt; <span class="uicontrol"> TextFileDecoderGroup</span> of <span class="uicontrol"> XMLDecoderGroup</span>. </li> 
      <li id="li_B2D61A0763AD4FEDB619BF9550EF4602"> Voer in de parameter Naam voor de nieuwe groep de gewenste naam van de decoderingsgroep in. </li> 
     </ul> </p> <p> <p>Opmerking:  Wanneer u een Decoderingsgroep in het <span class="filepath"> dossier van het Logboek Processing.cfg</span> voor het datasetprofiel specificeert, moet de naam precies de naam aanpassen die u hier ingaat. Zie <a href="../../../../../home/c-dataset-const-proc/c-log-proc-config-file/c-log-sources.md#concept-3d4fb817c057447d90f166b1183b461e"> Logbestanden</a> voor meer informatie. </p> </p> <p> Voor informatie over de decoders die u voor elke groep kunt bepalen, zie <a href="../../../../../home/c-dataset-const-proc/c-dataset-inc-files/c-types-dataset-inc-files/c-log-proc-dataset-inc-files/c-text-file-dec-groups.md#concept-0db34988e17c41bfb1797f1d8e78aabd"> de Groepen van de Decoder van het Dossier van de Tekst </a> of <a href="../../../../../home/c-dataset-const-proc/c-dataset-inc-files/c-types-dataset-inc-files/c-log-proc-dataset-inc-files/c-xml-dec-grps.md#concept-5eda5ab253724674832f6951e2a0d1c3"> de DecoderingsGroepen van XML</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Velden </td> 
   <td colname="col2"> <p>Hiermee geeft u velden weer die zijn gedefinieerd in <span class="wintitle"> Logbronnen</span> of <span class="wintitle"> Transformaties</span> in een <span class="wintitle">-bestand met een configuratie van de logverwerkingsdatabase</span>, maar die worden gebruikt in transformaties, voorwaarden of uitgebreide afmetingen in een <span class="wintitle">-bestand Configuratie transformatiedatum</span> moet hier worden vermeld. </p> <p> Elk veld hieronder moet worden vermeld in een bestand <span class="wintitle"> Gegevensset voor logverwerking Include</span>: 
     <ul id="ul_D1BB18A80D874C0B9B54DA361698EB30"> 
      <li id="li_7E8B5B697BDA408DBE10D9A63AF295AC"> x-trackingid </li> 
      <li id="li_F5DEE90A596A4A1C86AF874653C4048C"> x-timestamp </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Voorwaarde logbestandvermelding </td> 
   <td colname="col2"> <p>Optioneel. Bepaalt de regels waardoor de logboekingangen voor opneming in de dataset worden overwogen. Zie <a href="../../../../../home/c-dataset-const-proc/c-log-proc-config-file/c-info-log-proc-param.md#concept-ecaff95cee4e40bc90f81e099c5fc934"> Logboekinvoervoorwaarde</a>. </p> <p> <p>Opmerking:  Om in de dataset te worden opgenomen, moet een logboekingang <span class="wintitle"> de Voorwaarde van de Ingang </span> in <span class="filepath"> het dossier van Logprocessing.cfg</span> en in elk <span class="wintitle"> dossier van de Dataset van de Dataset van de Verwerking van het Logboek omvatten</span>. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Parameters </td> 
   <td colname="col2"> Optioneel. Een variabele waarnaar u in andere configuratieparameters kunt verwijzen. Zie <a href="../../../../../home/c-dataset-const-proc/c-dataset-inc-files/c-def-param-dataset-inc-files/c-def-param-dataset-inc-files.md#concept-5ad06acc8dc44bf2a99643fafdd56b50"> Parameters definiëren in Dataset Inclusief bestanden</a> voor meer informatie. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Opnieuw verwerken </td> 
   <td colname="col2"> <p>Optioneel. Elk teken of elke combinatie van tekens kan hier worden ingevoerd. Als u deze parameter wijzigt en het bestand opslaat op de gegevenswerkbankserver, worden de gegevens opnieuw verwerkt. </p> <p> Zie <a href="../../../../../home/c-dataset-const-proc/c-reproc-retrans/c-unst-reproc-retrans.md"> Opwerking en hertransformatie</a> voor informatie over het opnieuw verwerken van uw gegevens. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Werkgebied </td> 
   <td colname="col2"> <p>Optioneel. De naam van het verwerkingswerkgebied dat van toepassing is op dit <span class="wintitle"> Gegevensset van logverwerking Include</span>-bestand. De verwerkingsfasen worden gedefinieerd in de parameter Stages in het bestand <span class="filepath"> Log Processing.cfg</span>. </p> <p> <p>Opmerking:  Wanneer u een werkgebied opgeeft, moet de naam van het werkgebied exact overeenkomen met de naam die wordt vermeld in de parameter Stage in het bestand <span class="filepath"> Log Processing.cfg</span> voor het gegevenssetprofiel. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Transformaties </td> 
   <td colname="col2"> Optioneel. Bepaalt de gegevenstransformaties die tijdens logboekverwerking moeten worden toegepast. Voor informatie over de beschikbare transformatietypen, zie <a href="../../../../../home/c-dataset-const-proc/c-data-trans/c-abt-transf.md"> Transformaties van Gegevens</a>. </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Voor beschrijvingen van de parameters in het [!DNL Log Processing.cfg] dossier, zie [Logbestand van de Configuratie van de Verwerking](../../../../../home/c-dataset-const-proc/c-log-proc-config-file/c-abt-log-proc-config-file.md).

Houd rekening met de volgende punten wanneer u met [!DNL Log Processing Dataset Include] bestanden werkt:

* Als u een van de parameters in dit bestand wijzigt, moeten alle gegevens opnieuw worden verwerkt.
* U kunt om het even welke hierboven beschreven parameters aan het [!DNL Log Processing Dataset Include] dossier toevoegen door het dossier in Blocnote te openen en uit te geven. Wijzigingen die u aanbrengt en opslaat, worden weergegeven wanneer u het bestand opnieuw opent in de werkbank Gegevens. Wanneer u een nieuwe parameter toevoegt, gebruikt u de toets Ruimte (niet de Tab-toets) om twee (2) spaties rechts van het vorige kopniveau te laten inspringen.
