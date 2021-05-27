---
description: De bronnen van het logboek zijn dossiers die de gegevens bevatten die moeten worden gebruikt om een dataset te bouwen.
title: Logbronnen
uuid: ea21c3d7-9188-4ba8-bacd-052d678bd799
exl-id: 36e0799b-197d-4c59-84ae-7a4350584ab1
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '3664'
ht-degree: 0%

---

# Logbronnen{#log-sources}

De bronnen van het logboek zijn dossiers die de gegevens bevatten die moeten worden gebruikt om een dataset te bouwen.

De gegevens die beschikbaar zijn in de logbronnen worden gebeurtenisgegevens genoemd omdat elke gegevensrecord een transactierecord of één instantie van een gebeurtenis vertegenwoordigt. De gegevenswerkbankserver kan logbronnen verwerken die zijn afgeleid van gegevens die door [!DNL Sensors] zijn verzameld of uit andere gegevensbronnen zijn geëxtraheerd.

* **Gegevens verzameld door [!DNL Sensors]: ** Gegevens die door [!DNL Sensors] van HTTP- en toepassingsservers worden verzameld, worden verzonden naar workbench-servers voor gegevens, die de gegevens omzetten in zeer gecomprimeerde logbestanden ( [!DNL .vsl]). Zie [Sensorbestanden](../../../home/c-dataset-const-proc/c-log-proc-config-file/c-log-sources.md#concept-b25f11c477b54032a15b6117b3bf9009).

* **Gegevens die door de Server van het Inzicht worden getrokken:** De server van de gegevenswerkbank leest gebeurtenisgegevens in vlakke dossiers, de dossiers van XML, of ODBC-Volgzame gegevensbestanden, en gebruikt zijn decoders om de gewenste elementen van de gegevens te halen. Dergelijke gebeurtenisgegevens hoeven niet geheugen-ingezetene te zijn, maar de records die de gegevens bevatten moeten een tracking-id bevatten. Zie [Logbestanden](../../../home/c-dataset-const-proc/c-log-proc-config-file/c-log-sources.md#concept-3d4fb817c057447d90f166b1183b461e), [XML-logbronnen](../../../home/c-dataset-const-proc/c-log-proc-config-file/c-log-sources.md#concept-c7b154e93748447b986e97f6ef688887) en [ODBC-gegevensbronnen](../../../home/c-dataset-const-proc/c-log-proc-config-file/c-odbc-data-sources.md#concept-5f2cf635081d44beab826ef5ec8cf4e3).

**Een logbron toevoegen**

1. Open [!DNL Log Processing.cfg] in gegevenswerkbank.
1. Klik met de rechtermuisknop **[!UICONTROL Log Sources]** en klik vervolgens op **[!UICONTROL Add New]**.

1. Selecteer een van de volgende opties:

   * **[!UICONTROL Sensor]**
   * **[!UICONTROL Log File]**
   * **[!UICONTROL XML Log Source]**
   * **[!UICONTROL ODBC Data Source]**

1. De specifieke parameters die worden gebruikt om een dataset te bepalen variëren gebaseerd op het type van logboekbron dat in het de configuratieproces van de dataset moet worden gebruikt. Geef de parameters op zoals aangegeven in het gedeelte dat overeenkomt met de desbetreffende logbron:

   * [Sensorbestanden](../../../home/c-dataset-const-proc/c-log-proc-config-file/c-log-sources.md#concept-b25f11c477b54032a15b6117b3bf9009)
   * [Logbestanden](../../../home/c-dataset-const-proc/c-log-proc-config-file/c-log-sources.md#concept-3d4fb817c057447d90f166b1183b461e)
   * [XML-logbestanden](../../../home/c-dataset-const-proc/c-log-proc-config-file/c-log-sources.md#concept-c7b154e93748447b986e97f6ef688887)
   * [ODBC-gegevensbronnen](../../../home/c-dataset-const-proc/c-log-proc-config-file/c-odbc-data-sources.md#concept-5f2cf635081d44beab826ef5ec8cf4e3)

1. Nadat u uw logboekbron (en veranderingen in andere parameters) in het [!DNL Log Processing.cfg] dossier hebt bepaald, sparen het dossier plaatselijk en bewaar het aan uw profiel van de dataset op de server van de gegevenswerkbank.

   >[!NOTE]
   >
   >Een gegevenswerkbankserver [!DNL File Server Unit] kan [!DNL Sensor] dossiers, logboekdossiers, en de dossiers van XML ontvangen en opslaan en hen aan de server [!DNL Data Processing Units] leveren van de gegevenswerkbankserver die de dataset construeert. Zie [Een Eenheid van de Server van het Dossier van de Server van het Inzicht vormen](../../../home/c-dataset-const-proc/c-log-proc-config-file/c-ins-svr-file-svr-unit.md#concept-995abff3fce34e439fb3f7f47191c80d).

   U kunt de configuratie van om het even welke logboekbron van [!DNL Transformation Dependency Map] openen. Voor informatie over [!DNL Transformation Dependency Map], zie [Hulpmiddelen van de Configuratie van de Dataset](../../../home/c-dataset-const-proc/c-dataset-config-tools/c-dataset-config-tools.md#concept-6e058b7691834cf79dcfd1573f78d4f5).

<!--
c_sensor_files.xml
-->

## Vereisten {#section-d5901a4872774ad5bd01a18db114f1f2}

Gebeurtenisgegevens die door [!DNL Sensors] van HTTP- en toepassingsservers worden verzameld, worden verzonden naar workbench-servers voor gegevens, die de gegevens omzetten in bestanden met een sterk gecomprimeerd logbestand ( [!DNL .vsl]). De [!DNL .vsl]-bestandsindeling wordt beheerd door de gegevensworkbench-server en elk bestand heeft een naam met de volgende indeling:

YYYMMDD-*SENSORID*.VSL

waarbij JJJMMDD de datum van het bestand is, en *SENSORID* is de naam (toegewezen door uw organisatie) die aangeeft welke [!DNL Sensor] de gegevens heeft verzameld en naar de gegevenswerkbench-server heeft verzonden.

## Parameters {#section-5c3f1e341c284486aeba3452057da7f3}

Voor [!DNL Sensor]-bestanden zijn de volgende parameters beschikbaar:

<table id="table_F583B475600041AFA3B9399AE0592146"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Parameter </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Logpaden </td> 
   <td colname="col2"> <p>De directory's waar de <span class="filepath"> .vsl</span> bestanden worden opgeslagen. De standaardlocatie is de map Logs. Een relatief pad verwijst naar de installatiemap van de gegevenswerkbankserver. </p> <p>U kunt vervangingskarakters gebruiken om te specificeren welke <span class="filepath"> .vsl</span> dossiers te verwerken: 
     <ul id="ul_AE144ED0FAB94FE8B32599A058659DE1"> 
      <li id="li_1E4E4CFD72C34B5EB71A3C59877950A9"> * komt overeen met een willekeurig aantal tekens </li> 
      <li id="li_4664400FC12E44B39B28438B85D20ED8"> ? komt overeen met één teken </li> 
     </ul> </p> <p> Het logpad <span class="filepath"> Logs\*.vsl</span> komt bijvoorbeeld overeen met elk bestand in de map Logs dat eindigt op <span class="filepath"> .vsl</span>. Het logpad <span class="filepath"> Logs\*-SENSOR?.vsl</span> komt overeen met bestanden in de map Logs met een willekeurige datum (JJJJMMDD) en één teken na SENSOR, zoals in SENSOR1. </p> <p> Als u alle submappen van het opgegeven pad wilt doorzoeken, moet u de parameter Recursive instellen op true. </p> <p> <p>Opmerking: Als de bestanden moeten worden gelezen van de <span class="wintitle"> File Server Unit</span> van een gegevenswerkbankserver, moet u de juiste URI(s) invoeren in de parameter Log Paths. De <span class="filepath"> URI /Logs/*-*.vsl</span> komt bijvoorbeeld overeen met elk <span class="filepath"> .vsl</span>-bestand in de map Logs. Zie <a href="../../../home/c-dataset-const-proc/c-log-proc-config-file/c-ins-svr-file-svr-unit.md#concept-995abff3fce34e439fb3f7f47191c80d"> het Vormen van een Eenheid van de Server van het Dossier van de Server van het Inzicht</a>. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Logboekserver </td> 
   <td colname="col2">Informatie (Adres, Naam, Haven, etc.) noodzakelijk om met een dossierserver te verbinden. Als er een ingang in de parameter van de Server van het Logboek is, worden <span class="wintitle"> de Wegen van het Logboek </span> geïnterpreteerd als URIs. Anders worden ze geïnterpreteerd als lokale paden. Zie <a href="../../../home/c-dataset-const-proc/c-log-proc-config-file/c-ins-svr-file-svr-unit.md#concept-995abff3fce34e439fb3f7f47191c80d"> het Vormen van een Eenheid van de Server van het Dossier van de Server van het Inzicht</a>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Logbron-id </td> 
   <td colname="col2"> <p>De waarde van deze parameter kan elke tekenreeks zijn. Als een waarde wordt gespecificeerd, laat deze parameter u toe om logboekingangen van verschillende logboekbronnen voor bronidentificatie of gerichte verwerking te onderscheiden. Het veld x-log-source-id wordt gevuld met een waarde die de logbron voor elke logbestandvermelding identificeert. Bijvoorbeeld, als u logboekingangen van een <span class="wintitle"> Sensor</span> genoemd VSensor01 wilt identificeren, kon u <span class="filepath"> van VSensor01</span> typen, en dat koord zou tot het x-log-bron-id gebied voor elke logboekingang van die bron worden overgegaan. </p> <p> Zie <a href="../../../home/c-dataset-const-proc/c-ev-data-rec-fields.md#concept-06bda4be1a4649a2905a4422e9e6c42f"> Velden van gebeurtenisgegevensrecord</a> voor informatie over het veld x-log-source-id. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Recursief </td> 
   <td colname="col2"> Waar of onwaar. Indien ingesteld op true, worden alle submappen van elk pad dat is opgegeven in <span class="wintitle"> Logpaden</span> doorzocht naar bestanden die overeenkomen met de opgegeven bestandsnaam of het opgegeven jokertekenpatroon. De standaardwaarde is false. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Begin-/eindtijd gebruiken </td> 
   <td colname="col2"> <p>Waar of onwaar. Als deze optie is ingesteld op true en Begintijd of Eindtijd is opgegeven, moeten alle bestanden voor deze logbron bestandsnamen hebben die beginnen met datums in de ISO-indeling (JJJMMDD). Aangenomen wordt dat elk bestand gegevens bevat voor één GMT-dag (bijvoorbeeld het tijdbereik dat op één dag begint bij 0000 GMT en de volgende dag eindigt bij 0000 GMT). Als de logbronbestanden gegevens bevatten die niet overeenkomen met een GMT-dag, moet deze parameter op false worden ingesteld om onjuiste resultaten te voorkomen. </p> <p> <p>Opmerking: Standaard voldoen <span class="filepath"> .vsl </span>bestanden met gegevens die zijn verzameld door <span class="wintitle"> Sensor</span> automatisch aan de hierboven beschreven vereisten voor naamgeving en tijdbereik. Als u deze parameter op true instelt, verwerkt de server van de gegevenswerkbank altijd gegevens uit bestanden waarvan de namen bestaan uit ISO-datums die tussen de opgegeven begintijd en eindtijd vallen. Als u deze parameter op vals plaatst, leest de server van de gegevenswerkbank alle <span class="filepath"> .vsl</span> dossiers tijdens logboekverwerking om te bepalen welke dossiers gegevens binnen de Tijd van het Begin en de waaier van de Tijd van het Eind bevatten. </p> </p> <p> Voor informatie over de parameters van de Tijd van het Begin en van de Eind - tijd, zie <a href="../../../home/c-dataset-const-proc/c-log-proc-config-file/c-info-log-proc-param.md#concept-41bd49bf6b64442d91c232ec67529a3d"> de Filters van Gegevens</a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Gebruik niet de configuratieparameters voor [!DNL Sensor] gegevensbronnen om te bepalen welke logboekingangen binnen een logboekdossier in een dataset zouden moeten worden omvat. Stel in plaats daarvan de gegevensbron zo in dat deze naar alle logbestanden in een map verwijst. Dan gebruik de parameters van de Tijd van het Begin en van de Tijd van het Eind van [!DNL Log Processing.cfg] om te bepalen welke logboekingangen in het construeren van de dataset zouden moeten worden gebruikt. Zie [Gegevensfilters](../../../home/c-dataset-const-proc/c-log-proc-config-file/c-info-log-proc-param.md#concept-41bd49bf6b64442d91c232ec67529a3d).

<!--
c_log_files.xml
-->

Het bestand met de gebeurtenisgegevens moet aan de volgende vereisten voldoen:

* Elke record met gebeurtenisgegevens in het bestand moet op één regel worden weergegeven.
* De velden in een record moeten met een ASCII-scheidingsteken van elkaar worden gescheiden, of ze nu leeg zijn of niet. Voor de gegevenswerkbankserver hoeft u geen specifiek scheidingsteken te gebruiken. U kunt elk teken gebruiken dat geen regeleindeteken is en dat nergens in de gebeurtenisgegevens zelf wordt weergegeven.
* Elke record in het bestand moet het volgende bevatten:

   * Een id voor bijhouden
   * Een tijdstempel

* Als u begin- en eindtijd wilt opgeven voor gegevensverwerking, moet elke bestandsnaam de volgende notatie hebben:

   * [!DNL YYYYMMDD-SOURCE.log]

   waarbij *YYYMMDD* de GMT-dag (Greenwich Mean Time) van alle gegevens in het bestand is en *SOURCE* een variabele die de bron van de gegevens in het bestand identificeert.

   >[!NOTE]
   >
   >Neem contact op met de Adobe Consulting Services voor een overzicht van de logbestanden die u wilt opnemen in de gegevensset.

## Parameters {#section-83a861ac24954d54bbb9530e4d8bf23c}

Voor logbestandlogbronnen zijn de parameters in de volgende tabel beschikbaar.

>[!NOTE]
>
>Voor de verwerking van logbestandslogbronnen zijn aanvullende parameters vereist die zijn gedefinieerd in een [!DNL Log Processing Dataset Include]-bestand, dat een subset bevat van de parameters die in een [!DNL Log Processing.cfg]-bestand zijn opgenomen, en speciale parameters voor het definiëren van decoders voor het extraheren van gegevens uit het logbestand. Zie [Decoderingsgroepen voor tekstbestanden](../../../home/c-dataset-const-proc/c-dataset-inc-files/c-types-dataset-inc-files/c-log-proc-dataset-inc-files/c-text-file-dec-groups.md#concept-0db34988e17c41bfb1797f1d8e78aabd) voor informatie over het definiëren van decoders voor logbestandsbronnen.

<table id="table_F33735B5B90A48B0B21FA02D9198CCA9"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Parameter </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Naam </td> 
   <td colname="col2"> De id voor de bron van het logbestand. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Logpaden </td> 
   <td colname="col2"> <p>De mappen waarin de logbestanden zijn opgeslagen. De standaardlocatie is de map Logs. Een relatief pad verwijst naar de installatiemap van de gegevenswerkbankserver. </p> <p> U kunt jokertekens gebruiken om op te geven welke logbestanden moeten worden verwerkt: 
     <ul id="ul_1F02D26A08D846E2A3114E5C33F60ECF"> 
      <li id="li_ECAE1C03A1C448A1B86AE00B3A955708"> * komt overeen met een willekeurig aantal tekens. </li> 
      <li id="li_24FDB500C5934CAAA4124C435DF4B290"> ? komt overeen met één teken. </li> 
     </ul> </p> <p> Het logpad <span class="filepath"> Logs\*.log</span> komt bijvoorbeeld overeen met elk bestand in de map Logs dat eindigt op <span class="filepath"> .log</span>. </p> <p> Als u alle submappen van het opgegeven pad wilt doorzoeken, moet u de parameter Recursive instellen op true. </p> <p> Als de bestanden moeten worden gelezen van de <span class="wintitle"> File Server Unit</span> van een gegevenswerkbankserver, moet u de juiste URI(s) invoeren in de parameter Log Paths. De <span class="filepath"> URI/Logs/*.log</span> komt bijvoorbeeld overeen met elk <span class="filepath"> .log</span>-bestand in de map Logs. Zie <a href="../../../home/c-dataset-const-proc/c-log-proc-config-file/c-ins-svr-file-svr-unit.md#concept-995abff3fce34e439fb3f7f47191c80d"> het Vormen van een Eenheid van de Server van het Dossier van de Server van het Inzicht</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Logboekserver </td> 
   <td colname="col2"> Informatie (Adres, Naam, Haven, etc.) noodzakelijk om met een dossierserver te verbinden. Als er een ingang in de parameter van de Server van het Logboek is, worden <span class="wintitle"> de Wegen van het Logboek </span> geïnterpreteerd als URIs. Anders worden ze geïnterpreteerd als lokale paden. Zie <a href="../../../home/c-dataset-const-proc/c-log-proc-config-file/c-ins-svr-file-svr-unit.md#concept-995abff3fce34e439fb3f7f47191c80d"> het Vormen van een Eenheid van de Server van het Dossier van de Server van het Inzicht</a>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Gecomprimeerd </td> 
   <td colname="col2"> Waar of onwaar. Deze waarde moet worden ingesteld op true als de logbestanden die door de gegevenswerkbankserver moeten worden gelezen, gecomprimeerde gzip-bestanden zijn. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Decoderingsgroep </td> 
   <td colname="col2"> De naam van de decoderingsgroep voor tekstbestanden die moet worden toegepast op de logbestandlogbron. Deze naam moet exact overeenkomen met de naam van de corresponderende decoderingsgroep voor tekstbestanden die is opgegeven in het bestand <span class="wintitle"> Gegevensset voor logverwerking Include</span>. Zie <a href="../../../home/c-dataset-const-proc/c-dataset-inc-files/c-types-dataset-inc-files/c-log-proc-dataset-inc-files/c-text-file-dec-groups.md#concept-0db34988e17c41bfb1797f1d8e78aabd"> Decoderingsgroepen voor tekstbestanden</a>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Logbron-id </td> 
   <td colname="col2"> <p>De waarde van deze parameter kan elke tekenreeks zijn. Als een waarde wordt gespecificeerd, laat deze parameter u toe om logboekingangen van verschillende logboekbronnen voor bronidentificatie of gerichte verwerking te onderscheiden. Het veld x-log-source-id wordt gevuld met een waarde die de logbron voor elke logbestandvermelding identificeert. Bijvoorbeeld, als u logboekingangen van een logboekdossier genoemde bron LogFile01 wilt identificeren, kon u <span class="filepath"> van LogFile01</span> typen, en dat koord zou tot x-log-bron-id gebied voor elke logboekingang van die bron worden overgegaan. </p> <p> Zie <a href="../../../home/c-dataset-const-proc/c-ev-data-rec-fields.md#concept-06bda4be1a4649a2905a4422e9e6c42f"> Velden van gebeurtenisgegevensrecord</a> voor informatie over het veld x-log-source-id. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Maskerpatroon </td> 
   <td colname="col2"> <p>Een reguliere expressie met één vastgelegd subpatroon dat een consistente naam extraheert die wordt gebruikt om de bron van een reeks logbestanden te identificeren. Alleen de bestandsnaam wordt in overweging genomen. Het pad en de extensie worden niet in aanmerking genomen voor de overeenkomst van de reguliere expressie. Als u geen <span class="wintitle"> maskerpatroon</span> specificeert, dan wordt een masker automatisch geproduceerd. </p> <p> Voor de bestanden <span class="filepath"> Logs\010105server1.log</span> en <span class="filepath"> Logs\010105server2.log</span> is het <span class="wintitle"> maskerpatroon</span> <code>[0-9]{6}(.*)</code>. Dit patroon extraheert de tekenreeks "server1" of "server2" uit de bovenstaande bestandsnamen. </p> <p> Zie <a href="../../../home/c-dataset-const-proc/c-reg-exp.md#concept-070077baa419475094ef0469e92c5b9c"> Reguliere expressies</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Recursief </td> 
   <td colname="col2"> Waar of onwaar. Als deze parameter op true is ingesteld, worden alle submappen van elk pad dat is opgegeven in <span class="wintitle"> Logpaden</span> doorzocht naar bestanden die overeenkomen met de opgegeven bestandsnaam of het opgegeven jokertekenpatroon. De standaardwaarde is false. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Bestand negeren </td> 
   <td colname="col2"> Het pad en de bestandsnaam van het bestand met de logbestandvermeldingen die niet aan de voorwaarden van de decoder voldoen. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Begin-/eindtijd gebruiken </td> 
   <td colname="col2"> <p>Waar of onwaar. Als deze parameter is ingesteld op true en als Begintijd of Eindtijd is opgegeven, moeten alle bestanden voor deze logbron bestandsnamen hebben die beginnen met datums in de ISO-indeling (JJJMMDD). Aangenomen wordt dat elk bestand gegevens bevat voor één GMT-dag (bijvoorbeeld het tijdbereik dat op één dag begint bij 0000 GMT en de volgende dag eindigt bij 0000 GMT). Als de bestandsnamen van logbronnen niet beginnen met ISO-datums of als de bestanden gegevens bevatten die niet overeenkomen met een GMT-dag, moet deze parameter worden ingesteld op false om onjuiste resultaten te voorkomen. </p> <p> <p>Opmerking:  Als aan de hierboven beschreven vereisten voor naamgeving en tijdbereik is voldaan voor de logbestanden en u deze parameter instelt op true, beperkt de opgegeven decoderingsgroep van het tekstbestand de bestanden die worden gelezen tot de bestanden waarvan de namen ISO-datums hebben die tussen de opgegeven begintijd en eindtijd liggen. Als u deze parameter aan vals plaatst, leest de server van de gegevenswerkbank alle logboekdossiers tijdens logboekverwerking om te bepalen welke dossiers gegevens binnen de de Tijd van het Begin en de waaier van de Tijd van het Eind bevatten. </p> </p> <p> Voor informatie over de parameters van de Tijd van het Begin en van de Eind - tijd, zie <a href="../../../home/c-dataset-const-proc/c-log-proc-config-file/c-info-log-proc-param.md#concept-41bd49bf6b64442d91c232ec67529a3d"> de Filters van Gegevens</a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

In dit voorbeeld, wordt de dataset geconstrueerd van twee types van logboekbronnen.

Logbron 0 geeft logbestanden op die zijn gegenereerd op basis van gebeurtenisgegevens die zijn vastgelegd door [!DNL Sensor]. Deze gegevensbron verwijst naar een map met de naam Logs en naar alle bestanden in die map met de bestandsextensie [!DNL .vsl].

Logbron 1 verwijst naar alle bestanden in de map Logs met de bestandsextensie [!DNL .txt]. De decoderingsgroep voor deze logbron wordt &quot;Tekstlogboeken&quot; genoemd.

![](assets/cfg_LogProcessing_LogSources.png)

U zou logboekdossiers niet moeten schrappen of bewegen nadat de gegevensbronnen voor een dataset zijn bepaald. Alleen nieuwe logbestanden moeten aan de map voor de gegevensbronnen worden toegevoegd.

<!--
c_xml_log_sources.xml
-->

Het bestand met de gebeurtenisgegevens moet aan de volgende vereisten voldoen:

* Gebeurtenisgegevens moeten worden opgenomen in een XML-bestand met de juiste indeling met de juiste relatie bovenliggend-onderliggend.
* Voor elke XML-bestandsindeling moet een unieke decoderingsgroep bestaan. Zie [XML-decoderingsgroepen](../../../home/c-dataset-const-proc/c-dataset-inc-files/c-types-dataset-inc-files/c-log-proc-dataset-inc-files/c-xml-dec-grps.md#concept-5eda5ab253724674832f6951e2a0d1c3) voor informatie over het samenstellen van een decoderingsgroep.
* Elke bezoekersrecord in het bestand moet het volgende bevatten:

   * Een id voor bijhouden
   * Een tijdstempel

* Als u begin- en eindtijd voor gegevensverwerking wilt opgeven, moet elke bestandsnaam van het formulier zijn

[!DNL YYYYMMDD-SOURCE.log]

waarbij *YYYMMDD* de GMT-dag (Greenwich Mean Time) van alle gegevens in het bestand is en *SOURCE* een variabele die de bron van de gegevens in het bestand identificeert.

Zie [XML-decoderingsgroepen](../../../home/c-dataset-const-proc/c-dataset-inc-files/c-types-dataset-inc-files/c-log-proc-dataset-inc-files/c-xml-dec-grps.md#concept-5eda5ab253724674832f6951e2a0d1c3) voor een voorbeeld van een XML-bestand dat aan deze vereisten voldoet.

>[!NOTE]
>
>Neem contact op met de adviesservices van Adobe voor een overzicht van de XML-logbestanden die u wilt opnemen in de gegevensset.

## Parameters {#section-d07b96d7f6ad4affb9cc0a0bc1b88c4d}

Voor XML-logbronnen zijn de parameters in de volgende tabel beschikbaar.

>[!NOTE]
>
>Voor de verwerking van XML-logbronnen zijn aanvullende parameters vereist die zijn gedefinieerd in een [!DNL Log Processing Dataset Include]-bestand, dat een subset bevat van de parameters die in een [!DNL Log Processing.cfg]-bestand zijn opgenomen, en speciale parameters voor het definiëren van decoders voor het extraheren van gegevens uit het XML-bestand. Zie [XML-decoderingsgroepen](../../../home/c-dataset-const-proc/c-dataset-inc-files/c-types-dataset-inc-files/c-log-proc-dataset-inc-files/c-xml-dec-grps.md#concept-5eda5ab253724674832f6951e2a0d1c3) voor informatie over het definiëren van decoders voor XML-logbronnen.

<table id="table_86B849F379CF4FEBA9294ACEF8F55184"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Veld </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Naam </td> 
   <td colname="col2"> De id voor de XML-logbron. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Logpaden </td> 
   <td colname="col2"> <p>De mappen waarin de XML-logbronnen worden opgeslagen. De standaardlocatie is de map Logs. Een relatief pad verwijst naar de installatiemap van de gegevenswerkbankserver. </p> <p> U kunt jokertekens gebruiken om op te geven welke XML-logbronnen moeten worden verwerkt: 
     <ul id="ul_0AE5D0ADE0F64CFAA856492A49239F58"> 
      <li id="li_4CBC0D1733F04258B3A55CC6FA714538 "> * komt overeen met een willekeurig aantal tekens </li> 
      <li id="li_81B597436A1241FF94E73C18A0ABBFA1"> ? komt overeen met één teken </li> 
     </ul> </p> <p>Het logpad <span class="filepath"> Logs\*.xml</span> komt bijvoorbeeld overeen met elk bestand in de map Logs dat eindigt op <span class="filepath"> .xml</span>. </p> <p> Als u alle submappen van het opgegeven pad wilt doorzoeken, moet u het veld <span class="wintitle"> Recursive</span> instellen op true. </p> <p> <p>Opmerking: Als de bestanden moeten worden gelezen van de <span class="wintitle"> File Server Unit</span> van een gegevenswerkbankserver, moet u de juiste URI(s) invoeren in het veld <span class="wintitle"> Log Paths</span>. De <span class="filepath"> URI/Logs/*.xml</span> komt bijvoorbeeld overeen met elk <span class="filepath"> .xml</span> bestand in de map Logs. Zie <a href="../../../home/c-dataset-const-proc/c-log-proc-config-file/c-ins-svr-file-svr-unit.md#concept-995abff3fce34e439fb3f7f47191c80d"> het Vormen van een Eenheid van de Server van het Dossier van de Server van het Inzicht</a>. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Logboekserver </td> 
   <td colname="col2"> Informatie (Adres, Naam, Haven, etc.) noodzakelijk om met een dossierserver te verbinden. Als het veld <span class="wintitle"> Logserver</span> een item bevat, worden de <span class="wintitle"> logpaden</span> geïnterpreteerd als URI's. Anders worden ze geïnterpreteerd als lokale paden. Zie <a href="../../../home/c-dataset-const-proc/c-log-proc-config-file/c-ins-svr-file-svr-unit.md#concept-995abff3fce34e439fb3f7f47191c80d"> het Vormen van een Eenheid van de Server van het Dossier van de Server van het Inzicht</a>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Gecomprimeerd </td> 
   <td colname="col2"> Waar of onwaar. Deze waarde moet worden ingesteld op true als de XML-logbronnen die door de gegevenswerkbench-server moeten worden gelezen, gecomprimeerde gzip-bestanden zijn. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Decoderingsgroep </td> 
   <td colname="col2"> De naam van de XML-decoderingsgroep die op de XML-logbron moet worden toegepast. Deze naam moet exact overeenkomen met de naam van de corresponderende XML-decoderingsgroep die is opgegeven in het bestand <span class="wintitle"> Gegevensset voor logverwerking Include</span>. Zie <a href="../../../home/c-dataset-const-proc/c-dataset-inc-files/c-types-dataset-inc-files/c-log-proc-dataset-inc-files/c-xml-dec-grps.md#concept-5eda5ab253724674832f6951e2a0d1c3"> XML-decoderingsgroepen</a>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Logbron-id </td> 
   <td colname="col2"> <p>De waarde van dit veld kan elke willekeurige tekenreeks zijn. Als een waarde wordt gespecificeerd, laat dit gebied u toe om logboekingangen van verschillende logboekbronnen voor bronidentificatie of gerichte verwerking te onderscheiden. Het veld x-log-source-id wordt gevuld met een waarde die de logbron voor elke logbestandvermelding identificeert. Als u bijvoorbeeld logitems wilt identificeren uit een bron van een logbestand met de naam XMLFile01, kunt u <span class="filepath"> typen uit XMLFile01</span> en die tekenreeks wordt doorgegeven aan het veld x-log-source-id voor elke logbestandvermelding uit die bron. </p> <p> Zie <a href="../../../home/c-dataset-const-proc/c-ev-data-rec-fields.md#concept-06bda4be1a4649a2905a4422e9e6c42f"> Velden van gebeurtenisgegevensrecord</a> voor informatie over het veld x-log-source-id. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Maskerpatroon </td> 
   <td colname="col2"> <p>Een reguliere expressie met één vastgelegd subpatroon dat een consistente naam extraheert die wordt gebruikt om de bron van een reeks logbestanden te identificeren. Alleen de bestandsnaam wordt in overweging genomen. Het pad en de extensie worden niet in aanmerking genomen voor de overeenkomst van de reguliere expressie. Als u geen <span class="wintitle"> maskerpatroon</span> specificeert, dan wordt een masker automatisch geproduceerd. </p> <p> Voor de bestanden <span class="filepath"> Logs\010105server1.xml</span> en <span class="filepath"> Logs\010105server2.xml</span> is het maskerpatroon <code>[0-9]{6}(.*)</code>. Dit patroon extraheert de tekenreeks "server1" of "server2" uit de bovenstaande bestandsnamen. </p> <p> Zie <a href="../../../home/c-dataset-const-proc/c-reg-exp.md#concept-070077baa419475094ef0469e92c5b9c"> Reguliere expressies</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Recursief </td> 
   <td colname="col2"> Waar of onwaar. Als deze parameter op true is ingesteld, worden alle submappen van elk pad dat is opgegeven in <span class="wintitle"> Logpaden</span> doorzocht naar bestanden die overeenkomen met de opgegeven bestandsnaam of het opgegeven jokertekenpatroon. De standaardwaarde is false. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Bestand negeren </td> 
   <td colname="col2"> Het pad en de bestandsnaam van het bestand met de logbestandvermeldingen die niet aan de voorwaarden van de decoder voldoen. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Begin-/eindtijd gebruiken </td> 
   <td colname="col2"> <p>Waar of onwaar. Als deze parameter is ingesteld op true en als Begintijd of Eindtijd is opgegeven, moeten alle bestanden voor deze logbron bestandsnamen hebben die beginnen met datums in de ISO-indeling (JJJMMDD). Aangenomen wordt dat elk bestand gegevens bevat voor één GMT-dag (bijvoorbeeld het tijdbereik dat op één dag begint bij 0000 GMT en de volgende dag eindigt bij 0000 GMT). Als de bestandsnamen van logbronnen niet beginnen met ISO-datums of als de bestanden gegevens bevatten die niet overeenkomen met een GMT-dag, moet deze parameter worden ingesteld op false om onjuiste resultaten te voorkomen. </p> <p> <p>Opmerking:  Als de hierboven beschreven vereisten voor naamgeving en tijdbereik zijn vervuld voor de XML-bestanden en u deze parameter instelt op true, beperkt de opgegeven XML-decoderingsgroep de bestanden die worden gelezen tot de bestanden waarvan de namen ISO-datums hebben die tussen de opgegeven begintijd en eindtijd liggen. Als u deze parameter op vals plaatst, leest de server van de gegevenswerkbank alle dossiers van XML tijdens logboekverwerking om te bepalen welke dossiers gegevens binnen de Tijd van het Begin en de waaier van de Tijd van het Eind bevatten. </p> </p> <p> Voor informatie over de parameters van de Tijd van het Begin en van de Eind - tijd, zie <a href="../../../home/c-dataset-const-proc/c-log-proc-config-file/c-info-log-proc-param.md#concept-41bd49bf6b64442d91c232ec67529a3d"> de Filters van Gegevens</a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>U zou het logboekbronnen van XML niet moeten schrappen of bewegen nadat de gegevensbronnen voor een dataset zijn bepaald. Alleen nieuwe XML-bestanden moeten aan de map voor de gegevensbronnen worden toegevoegd.

<!--
AVRO-log-file.xml
-->

De Avro-gegevensinvoer biedt een efficiëntere manier om gegevens in de Data Workbench te integreren:

<!-- <a id="section_45E3105B971C4220AE9CF573BEBF6080"></a> -->

* Avro verstrekt een enig-bronformaat voor verkeer en handelsgegevens.
* De Avro-feed bestaat uit gecomprimeerde gegevens van meerdere bronchunks die per dag worden geleverd. Het voorziet slechts bevolkte gebieden en verstrekt controle en berichteigenschappen, toegang tot historische gegevens, en auto-terugwinning.
* Het schema, een zichzelf definiërende lay-out van Avro logboekdossiers, is inbegrepen aan het begin van elk dossier.
* Nieuwe velden worden toegevoegd met ondersteunende informatie voor het invoeren van gegevens van Data Workbench zonder dat de decoder wijzigingen hoeft aan te brengen. Deze omvatten:

   * Gebeurtenissen: 1-250 (voorheen 1-75)
   * Aangepaste gebeurtenissen: 1-1000 (versus 1-100)
   * Toegang tot oplossingsvariabelen voor mobiele, sociale en videogegevens

>[!NOTE]
>
>Bovendien staat het gebruiken van het voer van de Avro directe toegang tot om het even welke nieuwe gebieden in het voer zonder sluiting toe, toelatend de gebieden om zonder de vereisten van het de dienstuur worden bijgewerkt.

De Avro-gegevensfeed wordt ingesteld in afzonderlijke bestanden:

* An **Avro Log file**: Dit is het het logboekformaat van Avro dat van decoder wordt geproduceerd om verkeer en handelgegevens te formatteren.
* An **Avro Decoder file**: Met dit bestand kunt u waarden toewijzen aan de nieuwe Avro-indeling. U kunt de decoder instellen met de wizard Avro Decoder.

## Wizard Avro Decoder {#section-9a824b4c3d5549e7952a7111232035b2}

Deze wizard stelt het logbestand van de Avro-decoder in.

Als u wilt openen, klikt u met de rechtermuisknop in een werkruimte en selecteert u **Admin** > **Wizards** > **Wizard Decoder vro**.

**Stap 1:** **Selecteer een AIR-logbestand**.

In deze stap kunt u een bronbestand voor het Avro-schema selecteren. Schema&#39;s zijn toegankelijk vanuit een logbestand (.log) of een bestaand decoderingsbestand (.avro). Schema&#39;s kunnen uit een van beide bestanden worden opgehaald.

| **AV-logbestand ** | Klik om een logbestand (.log) te openen om het schema boven aan het logbestand weer te geven en een decoderingsbestand te genereren. |
|---|---|
| **Avro Decoder-bestand** | Klik om het schema van een bestaand decoderingsbestand (.avro) te openen en te bewerken. |

**Stap 2: Selecteer Invoervelden**.

Selecteer de invoervelden die in de gegevensset moeten worden gebruikt om de logverwerking te doorlopen. Alle velden in het bestand worden weergegeven, zodat u velden voor de feed kunt selecteren.

>[!NOTE]
>
>Er wordt een veld [!DNL x-product(Generates row)] opgegeven als er een array in de gegevens wordt aangetroffen. Dit veld genereert nieuwe rijen voor de geneste gegevens in een array als invoervelden. Als u bijvoorbeeld een Actief-rij hebt met veel productwaarden in een array, worden rijen gegenereerd in het invoerbestand voor elk product.

| **Standaardwaarden selecteren** | Selecteer velden die u wilt identificeren als een standaardset standaardvelden. |
|---|---|
| **Alles selecteren** | Selecteer alle velden in het bestand. |
| **Alle selecties opheffen** | Alle velden in het bestand wissen. |

**Stap 3: Selecteer velden die u wilt kopiëren om rijen te genereren.**

Omdat nieuwe rijen op basis van geneste waarden in een array kunnen worden gemaakt, moet elke nieuwe rij een tracking-id en een tijdstempel hebben. Met deze stap kunt u de velden selecteren die u wilt kopiëren naar rijen in de bovenliggende record, zoals een trackingid en tijdstempel. U kunt ook andere waarden selecteren die u aan elke rij wilt toevoegen.

| **Standaardwaarden selecteren** | Selecteer een standaardset standaardvelden waarvoor nieuwe kolomwaarden aan elke rij moeten worden toegevoegd, zoals een tracking-id en een tijdstempel. Een veld [!DNL hit_source] is bijvoorbeeld een standaardwaarde die aan elke nieuwe rij moet worden toegevoegd (het wordt gedefinieerd als een standaardwaarde in de lijst). U kunt desgewenst andere kolomwaarden aan elke rij toevoegen. |
|---|---|
| **Alles selecteren** | Selecteer alle velden in het bestand. |
| **Alle selecties opheffen** | Alle velden in het bestand wissen. |

Gebruik het vak **Zoeken** om waarden in de lijst te zoeken.

**Stap 4:De naam van de decoder opgeven**

Wijs een naam toe aan de groep velden en sla deze op als een decoderingsbestand. De naam moet overeenkomen met de naam van de Decoderingsgroep die is opgegeven in de logbron.

**Stap 5: Sla het decoderingsbestand op.**

Het bestandenmenu wordt geopend om het decoderingsbestand een naam te geven en op te slaan als een [!DNL .cfg]-bestand in de map **Logs**.
