---
description: De bronnen van het logboek zijn dossiers die de gegevens bevatten die moeten worden gebruikt om een dataset te bouwen.
title: Logbronnen
uuid: ea21c3d7-9188-4ba8-bacd-052d678bd799
exl-id: 36e0799b-197d-4c59-84ae-7a4350584ab1
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '3664'
ht-degree: 0%

---

# Logbronnen{#log-sources}

{{eol}}

De bronnen van het logboek zijn dossiers die de gegevens bevatten die moeten worden gebruikt om een dataset te bouwen.

De gegevens die beschikbaar zijn in de logbronnen worden gebeurtenisgegevens genoemd omdat elke gegevensrecord een transactierecord of één instantie van een gebeurtenis vertegenwoordigt. De server van de gegevenswerkbank kan logboekbronnen verwerken die uit gegevens worden afgeleid die door worden verzameld [!DNL Sensors] of uit andere gegevensbronnen worden geëxtraheerd.

* **Gegevens verzameld door [!DNL Sensors]: ** Gegevens verzameld door [!DNL Sensors] van HTTP en toepassingsservers wordt overgebracht naar de servers van de gegevenswerkbank, die de gegevens in hoogst samengeperst logboek ( [!DNL .vsl]). Zie [Sensorbestanden](../../../home/c-dataset-const-proc/c-log-proc-config-file/c-log-sources.md#concept-b25f11c477b54032a15b6117b3bf9009).

* **Gegevens geëxtraheerd door Insight Server:** De gegevenswerkbankserver leest gebeurtenisgegevens in vlakke dossiers, de dossiers van XML, of ODBC-Volgzame gegevensbestanden, en gebruikt zijn decoders om de gewenste elementen van de gegevens te halen. Dergelijke gebeurtenisgegevens hoeven niet geheugen-ingezetene te zijn, maar de records die de gegevens bevatten moeten een tracking-id bevatten. Zie [Logbestanden](../../../home/c-dataset-const-proc/c-log-proc-config-file/c-log-sources.md#concept-3d4fb817c057447d90f166b1183b461e), [XML-logbestanden](../../../home/c-dataset-const-proc/c-log-proc-config-file/c-log-sources.md#concept-c7b154e93748447b986e97f6ef688887), en [ODBC-gegevensbronnen](../../../home/c-dataset-const-proc/c-log-proc-config-file/c-odbc-data-sources.md#concept-5f2cf635081d44beab826ef5ec8cf4e3).

**Een logbron toevoegen**

1. Openen [!DNL Log Processing.cfg] in de werkbank voor gegevens.
1. Klikken met rechtermuisknop **[!UICONTROL Log Sources]** en klik vervolgens op **[!UICONTROL Add New]**.

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

1. Nadat u uw logboekbron (en veranderingen in andere parameters) in hebt bepaald [!DNL Log Processing.cfg] bestand, slaat u het bestand lokaal op en slaat u het op in het gegevenssetprofiel op de gegevenswerkbankserver.

   >[!NOTE]
   >
   >Een gegevenswerkbankserver [!DNL File Server Unit] kan ontvangen en opslaan [!DNL Sensor] bestanden, logbestanden en XML-bestanden en dienen deze bij de server op de werkbank van de database [!DNL Data Processing Units] die de gegevensset samenstellen. Zie [Een Insight Server-bestandsservereenheid configureren](../../../home/c-dataset-const-proc/c-log-proc-config-file/c-ins-svr-file-svr-unit.md#concept-995abff3fce34e439fb3f7f47191c80d).

   U kunt de configuratie van om het even welke logboekbron van een openen [!DNL Transformation Dependency Map]. Voor informatie over [!DNL Transformation Dependency Map], zie [Hulpprogramma&#39;s voor gegevensverzameling](../../../home/c-dataset-const-proc/c-dataset-config-tools/c-dataset-config-tools.md#concept-6e058b7691834cf79dcfd1573f78d4f5).

<!--
c_sensor_files.xml
-->

## Vereisten {#section-d5901a4872774ad5bd01a18db114f1f2}

Gebeurtenisgegevens verzameld door [!DNL Sensors] van HTTP en toepassingsservers wordt overgebracht naar de servers van de gegevenswerkbank, die de gegevens in hoogst samengeperst logboek ( [!DNL .vsl]). De [!DNL .vsl] De bestandsindeling wordt beheerd door de gegevenswerkbankserver en elk bestand heeft een naam in de volgende indeling:

JJJMMDD-*SENSORID*.VSL

waarbij JJJMMDD de datum van het bestand is, en *SENSORID* is de naam (toegewezen door uw organisatie) die erop wijst welke [!DNL Sensor] de gegevens verzameld en naar de gegevenswerkbankserver verzonden.

## Parameters {#section-5c3f1e341c284486aeba3452057da7f3}

Voor [!DNL Sensor] zijn de volgende parameters beschikbaar:

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
   <td colname="col2"> <p>De mappen waarin de <span class="filepath"> .vsl</span> worden opgeslagen. De standaardlocatie is de map Logs. Een relatief pad verwijst naar de installatiemap van de gegevenswerkbankserver. </p> <p>U kunt jokertekens gebruiken om op te geven welke <span class="filepath"> .vsl</span> te verwerken bestanden: 
     <ul id="ul_AE144ED0FAB94FE8B32599A058659DE1"> 
      <li id="li_1E4E4CFD72C34B5EB71A3C59877950A9"> * komt overeen met een willekeurig aantal tekens </li> 
      <li id="li_4664400FC12E44B39B28438B85D20ED8"> ? komt overeen met één teken </li> 
     </ul> </p> <p> Het logpad <span class="filepath"> Logs\*.vsl</span> komt overeen met elk bestand in de map Logs dat eindigt in <span class="filepath"> .vsl</span>. Het logpad <span class="filepath"> Logs\*-SENSOR?.vsl</span> bestanden in de map Logs komen overeen met elke datum (JJJMMDD) en één teken na SENSOR, zoals in SENSOR1. </p> <p> Als u alle submappen van het opgegeven pad wilt doorzoeken, moet u de parameter Recursive instellen op true. </p> <p> <p>Opmerking: Als de bestanden moeten worden gelezen van een server op de werkbank voor gegevens <span class="wintitle"> Bestandsservereenheid</span>, moet u de juiste URI('s) invoeren in de parameter Log Paths. De <span class="filepath"> URI /Logs/*-*.vsl</span> overeenkomende met <span class="filepath"> .vsl</span> in de map Logs. Zie <a href="../../../home/c-dataset-const-proc/c-log-proc-config-file/c-ins-svr-file-svr-unit.md#concept-995abff3fce34e439fb3f7f47191c80d"> Een Insight Server-bestandsservereenheid configureren</a>. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Logboekserver </td> 
   <td colname="col2">Informatie (Adres, Naam, Haven, etc.) noodzakelijk om met een dossierserver te verbinden. Als er een item is in de parameter Log Server, wordt <span class="wintitle"> Logpaden</span> worden geïnterpreteerd als URI's. Anders worden ze geïnterpreteerd als lokale paden. Zie <a href="../../../home/c-dataset-const-proc/c-log-proc-config-file/c-ins-svr-file-svr-unit.md#concept-995abff3fce34e439fb3f7f47191c80d"> Een Insight Server-bestandsservereenheid configureren</a>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Logbron-id </td> 
   <td colname="col2"> <p>De waarde van deze parameter kan elke tekenreeks zijn. Als een waarde wordt gespecificeerd, laat deze parameter u toe om logboekingangen van verschillende logboekbronnen voor bronidentificatie of gerichte verwerking te onderscheiden. Het veld x-log-source-id wordt gevuld met een waarde die de logbron voor elke logbestandvermelding identificeert. Als u bijvoorbeeld logitems wilt identificeren op basis van een <span class="wintitle"> Sensor</span> genoemd VSensor01, kon u typen <span class="filepath"> van VSensor01</span>en die tekenreeks wordt doorgegeven aan het veld x-log-source-id voor elke logbestandvermelding uit die bron. </p> <p> Voor informatie over het x-log-source-id veld raadpleegt u <a href="../../../home/c-dataset-const-proc/c-ev-data-rec-fields.md#concept-06bda4be1a4649a2905a4422e9e6c42f"> Gebeurtenisgegevensrecordvelden</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Recursief </td> 
   <td colname="col2"> Waar of onwaar. Indien ingesteld op true, worden alle submappen van elk pad opgegeven in <span class="wintitle"> Logpaden</span> worden gezocht naar bestanden die overeenkomen met de opgegeven bestandsnaam of het opgegeven jokertekenpatroon. De standaardwaarde is false. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Begin-/eindtijd gebruiken </td> 
   <td colname="col2"> <p>Waar of onwaar. Als deze optie is ingesteld op true en Begintijd of Eindtijd is opgegeven, moeten alle bestanden voor deze logbron bestandsnamen hebben die beginnen met datums in de ISO-indeling (JJJMMDD). Aangenomen wordt dat elk bestand gegevens bevat voor één GMT-dag (bijvoorbeeld het tijdbereik dat op één dag begint bij 0000 GMT en de volgende dag eindigt bij 0000 GMT). Als de logbronbestanden gegevens bevatten die niet overeenkomen met een GMT-dag, moet deze parameter op false worden ingesteld om onjuiste resultaten te voorkomen. </p> <p> <p>Opmerking: Standaard, <span class="filepath"> .vsl </span>bestanden met gegevens die zijn verzameld door <span class="wintitle"> Sensor</span> voldoen automatisch aan de hierboven beschreven vereisten voor naamgeving en tijdbereik. Als u deze parameter op true instelt, verwerkt de server van de gegevenswerkbank altijd gegevens uit bestanden waarvan de namen bestaan uit ISO-datums die tussen de opgegeven begintijd en eindtijd vallen. Als u deze parameter instelt op false, leest de gegevenswerkbankserver alle <span class="filepath"> .vsl</span> bestanden tijdens de logverwerking om te bepalen welke bestanden gegevens bevatten binnen het bereik Begintijd en Eindtijd. </p> </p> <p> Voor informatie over de parameters van de Tijd van het Begin en van de Eind - tijd, zie <a href="../../../home/c-dataset-const-proc/c-log-proc-config-file/c-info-log-proc-param.md#concept-41bd49bf6b64442d91c232ec67529a3d"> Gegevensfilters</a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Gebruik de configuratieparameters niet voor [!DNL Sensor] gegevensbronnen om te bepalen welke logboekingangen binnen een logboekdossier in een dataset zouden moeten worden omvat. Stel in plaats daarvan de gegevensbron zo in dat deze naar alle logbestanden in een map verwijst. Gebruik vervolgens de parameters Begintijd en Eindtijd van [!DNL Log Processing.cfg] om te bepalen welke logboekingangen in de bouw van de dataset zouden moeten worden gebruikt. Zie [Gegevensfilters](../../../home/c-dataset-const-proc/c-log-proc-config-file/c-info-log-proc-param.md#concept-41bd49bf6b64442d91c232ec67529a3d).

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

   waar *JJJMMDD* de GMT-dag (Greenwich Mean Time) is van alle gegevens in het bestand, en *BRON* is een variabele die de bron van de gegevens in het bestand identificeert.

   >[!NOTE]
   >
   >Neem contact op met de Adobe Consulting Services voor een overzicht van de logbestanden die u wilt opnemen in de gegevensset.

## Parameters {#section-83a861ac24954d54bbb9530e4d8bf23c}

Voor logbestandlogbronnen zijn de parameters in de volgende tabel beschikbaar.

>[!NOTE]
>
>De verwerking van de bronnen van het logboekdossier vereist extra parameters die in a worden bepaald [!DNL Log Processing Dataset Include] bestand, dat een subset bevat van de parameters die in een [!DNL Log Processing.cfg] en speciale parameters voor het definiëren van decoders voor het ophalen van gegevens uit het logbestand. Voor informatie over het bepalen van decoders voor de bronnen van het logboekdossier, zie [Decoderingsgroepen tekstbestand](../../../home/c-dataset-const-proc/c-dataset-inc-files/c-types-dataset-inc-files/c-log-proc-dataset-inc-files/c-text-file-dec-groups.md#concept-0db34988e17c41bfb1797f1d8e78aabd).

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
     </ul> </p> <p> Het logpad <span class="filepath"> Logbestanden\*.log</span> komt overeen met elk bestand in de map Logs dat eindigt in <span class="filepath"> .log</span>. </p> <p> Als u alle submappen van het opgegeven pad wilt doorzoeken, moet u de parameter Recursive instellen op true. </p> <p> Als de bestanden moeten worden gelezen van een server op de werkbank voor gegevens <span class="wintitle"> Bestandsservereenheid</span>, moet u de juiste URI('s) invoeren in de parameter Log Paths. De <span class="filepath"> URI/Logs/*.log</span> overeenkomende met <span class="filepath"> .log</span> in de map Logs. Zie <a href="../../../home/c-dataset-const-proc/c-log-proc-config-file/c-ins-svr-file-svr-unit.md#concept-995abff3fce34e439fb3f7f47191c80d"> Een Insight Server-bestandsservereenheid configureren</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Logboekserver </td> 
   <td colname="col2"> Informatie (Adres, Naam, Haven, etc.) noodzakelijk om met een dossierserver te verbinden. Als er een item is in de parameter Log Server, wordt <span class="wintitle"> Logpaden</span> worden geïnterpreteerd als URI's. Anders worden ze geïnterpreteerd als lokale paden. Zie <a href="../../../home/c-dataset-const-proc/c-log-proc-config-file/c-ins-svr-file-svr-unit.md#concept-995abff3fce34e439fb3f7f47191c80d"> Een Insight Server-bestandsservereenheid configureren</a>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Gecomprimeerd </td> 
   <td colname="col2"> Waar of onwaar. Deze waarde moet worden ingesteld op true als de logbestanden die door de gegevenswerkbankserver moeten worden gelezen, gecomprimeerde gzip-bestanden zijn. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Decoderingsgroep </td> 
   <td colname="col2"> De naam van de decoderingsgroep voor tekstbestanden die moet worden toegepast op de logbestandlogbron. Deze naam moet exact overeenkomen met de naam van de corresponderende decoderingsgroep voor tekstbestanden die is opgegeven in het dialoogvenster <span class="wintitle"> Gegevensset logbestandsverwerking opnemen</span> bestand. Zie <a href="../../../home/c-dataset-const-proc/c-dataset-inc-files/c-types-dataset-inc-files/c-log-proc-dataset-inc-files/c-text-file-dec-groups.md#concept-0db34988e17c41bfb1797f1d8e78aabd"> Decoderingsgroepen tekstbestand</a>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Logbron-id </td> 
   <td colname="col2"> <p>De waarde van deze parameter kan elke tekenreeks zijn. Als een waarde wordt gespecificeerd, laat deze parameter u toe om logboekingangen van verschillende logboekbronnen voor bronidentificatie of gerichte verwerking te onderscheiden. Het veld x-log-source-id wordt gevuld met een waarde die de logbron voor elke logbestandvermelding identificeert. Als u bijvoorbeeld logitems wilt identificeren uit een bron van een logbestand met de naam LogFile01, kunt u typen <span class="filepath"> uit LogFile01</span>en die tekenreeks wordt doorgegeven aan het veld x-log-source-id voor elke logbestandvermelding uit die bron. </p> <p> Voor informatie over het x-log-source-id veld raadpleegt u <a href="../../../home/c-dataset-const-proc/c-ev-data-rec-fields.md#concept-06bda4be1a4649a2905a4422e9e6c42f"> Gebeurtenisgegevensrecordvelden</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Maskerpatroon </td> 
   <td colname="col2"> <p>Een reguliere expressie met één vastgelegd subpatroon dat een consistente naam extraheert die wordt gebruikt om de bron van een reeks logbestanden te identificeren. Alleen de bestandsnaam wordt in overweging genomen. Het pad en de extensie worden niet in aanmerking genomen voor de overeenkomst van de reguliere expressie. Als u geen <span class="wintitle"> maskerpatroon</span>, wordt er automatisch een masker gegenereerd. </p> <p> Voor de bestanden <span class="filepath"> Logs\010105server1.log</span> en <span class="filepath"> Logs\010105server2.log</span>de <span class="wintitle"> maskerpatroon</span> zou <code>[0-9]{6}(.*)</code>. Dit patroon extraheert de tekenreeks "server1" of "server2" uit de bovenstaande bestandsnamen. </p> <p> Zie <a href="../../../home/c-dataset-const-proc/c-reg-exp.md#concept-070077baa419475094ef0469e92c5b9c"> Reguliere expressies</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Recursief </td> 
   <td colname="col2"> Waar of onwaar. Als deze parameter is ingesteld op true, worden alle submappen van elk pad opgegeven in <span class="wintitle"> Logpaden</span> worden gezocht naar bestanden die overeenkomen met de opgegeven bestandsnaam of het opgegeven jokertekenpatroon. De standaardwaarde is false. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Bestand negeren </td> 
   <td colname="col2"> Het pad en de bestandsnaam van het bestand met de logbestandvermeldingen die niet aan de voorwaarden van de decoder voldoen. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Begin-/eindtijd gebruiken </td> 
   <td colname="col2"> <p>Waar of onwaar. Als deze parameter is ingesteld op true en als Begintijd of Eindtijd is opgegeven, moeten alle bestanden voor deze logbron bestandsnamen hebben die beginnen met datums in de ISO-indeling (JJJMMDD). Aangenomen wordt dat elk bestand gegevens bevat voor één GMT-dag (bijvoorbeeld het tijdbereik dat op één dag begint bij 0000 GMT en de volgende dag eindigt bij 0000 GMT). Als de bestandsnamen van logbronnen niet beginnen met ISO-datums of als de bestanden gegevens bevatten die niet overeenkomen met een GMT-dag, moet deze parameter worden ingesteld op false om onjuiste resultaten te voorkomen. </p> <p> <p>Opmerking: Als aan de hierboven beschreven vereisten voor naamgeving en tijdbereik is voldaan voor de logbestanden en u deze parameter instelt op true, beperkt de opgegeven decoderingsgroep van het tekstbestand de bestanden die worden gelezen tot de bestanden waarvan de namen ISO-datums hebben die tussen de opgegeven begintijd en eindtijd liggen. Als u deze parameter aan vals plaatst, leest de server van de gegevenswerkbank alle logboekdossiers tijdens logboekverwerking om te bepalen welke dossiers gegevens binnen de de Tijd van het Begin en de waaier van de Tijd van het Eind bevatten. </p> </p> <p> Voor informatie over de parameters van de Tijd van het Begin en van de Eind - tijd, zie <a href="../../../home/c-dataset-const-proc/c-log-proc-config-file/c-info-log-proc-param.md#concept-41bd49bf6b64442d91c232ec67529a3d"> Gegevensfilters</a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

In dit voorbeeld, wordt de dataset geconstrueerd van twee types van logboekbronnen.

Logbron 0 geeft logbestanden op die zijn gegenereerd op basis van gebeurtenisgegevens die zijn vastgelegd door [!DNL Sensor]. Deze gegevensbron verwijst naar een map met de naam Logs en naar alle bestanden in die map met een [!DNL .vsl] bestandsnaamextensie.

Logbron 1 verwijst naar alle bestanden in de map Logs met een [!DNL .txt] bestandsnaamextensie. De decoderingsgroep voor deze logbron wordt &quot;Tekstlogboeken&quot; genoemd.

![](assets/cfg_LogProcessing_LogSources.png)

U zou logboekdossiers niet moeten schrappen of bewegen nadat de gegevensbronnen voor een dataset zijn bepaald. Alleen nieuwe logbestanden moeten aan de map voor de gegevensbronnen worden toegevoegd.

<!--
c_xml_log_sources.xml
-->

Het bestand met de gebeurtenisgegevens moet aan de volgende vereisten voldoen:

* Gebeurtenisgegevens moeten worden opgenomen in een XML-bestand met de juiste indeling met de juiste relatie bovenliggend-onderliggend.
* Voor elke XML-bestandsindeling moet een unieke decoderingsgroep bestaan. Voor informatie over het samenstellen van een decoderingsgroep raadpleegt u [XML-decoderingsgroepen](../../../home/c-dataset-const-proc/c-dataset-inc-files/c-types-dataset-inc-files/c-log-proc-dataset-inc-files/c-xml-dec-grps.md#concept-5eda5ab253724674832f6951e2a0d1c3).
* Elke bezoekersrecord in het bestand moet het volgende bevatten:

   * Een id voor bijhouden
   * Een tijdstempel

* Als u begin- en eindtijd voor gegevensverwerking wilt opgeven, moet elke bestandsnaam van het formulier zijn

[!DNL YYYYMMDD-SOURCE.log]

waar *JJJMMDD* de GMT-dag (Greenwich Mean Time) is van alle gegevens in het bestand, en *BRON* is een variabele die de bron van de gegevens in het bestand identificeert.

Voor een voorbeeld van een XML-bestand dat aan deze vereisten voldoet, raadpleegt u [XML-decoderingsgroepen](../../../home/c-dataset-const-proc/c-dataset-inc-files/c-types-dataset-inc-files/c-log-proc-dataset-inc-files/c-xml-dec-grps.md#concept-5eda5ab253724674832f6951e2a0d1c3).

>[!NOTE]
>
>Neem contact op met de adviesservices van Adobe voor een overzicht van de XML-logbestanden die u wilt opnemen in de gegevensset.

## Parameters {#section-d07b96d7f6ad4affb9cc0a0bc1b88c4d}

Voor XML-logbronnen zijn de parameters in de volgende tabel beschikbaar.

>[!NOTE]
>
>De verwerking van het logboekbronnen van XML vereist extra parameters die in a worden bepaald [!DNL Log Processing Dataset Include] bestand, dat een subset bevat van de parameters die in een [!DNL Log Processing.cfg] en speciale parameters voor het definiëren van decoders voor het extraheren van gegevens uit het XML-bestand. Voor informatie over het bepalen van decoders voor het logboekbronnen van XML, zie [XML-decoderingsgroepen](../../../home/c-dataset-const-proc/c-dataset-inc-files/c-types-dataset-inc-files/c-log-proc-dataset-inc-files/c-xml-dec-grps.md#concept-5eda5ab253724674832f6951e2a0d1c3).

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
     </ul> </p> <p>Het logpad <span class="filepath"> Logs\*.xml</span> komt overeen met elk bestand in de map Logs dat eindigt in <span class="filepath"> .xml</span>. </p> <p> Als u alle submappen van het opgegeven pad wilt doorzoeken, moet u de opdracht <span class="wintitle"> Recursief</span> veld naar waar. </p> <p> <p>Opmerking: Als de bestanden moeten worden gelezen van een server op de werkbank voor gegevens <span class="wintitle"> Bestandsservereenheid</span>, moet u de juiste URI(s) invoeren in het dialoogvenster <span class="wintitle"> Logpaden</span> veld. De <span class="filepath"> URI/Logs/*.xml</span> overeenkomende met <span class="filepath"> .xml</span> in de map Logs. Zie <a href="../../../home/c-dataset-const-proc/c-log-proc-config-file/c-ins-svr-file-svr-unit.md#concept-995abff3fce34e439fb3f7f47191c80d"> Een Insight Server-bestandsservereenheid configureren</a>. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Logboekserver </td> 
   <td colname="col2"> Informatie (Adres, Naam, Haven, etc.) noodzakelijk om met een dossierserver te verbinden. Als er een vermelding in het veld <span class="wintitle"> Logboekserver</span> in het veld <span class="wintitle"> Logpaden</span> worden geïnterpreteerd als URI's. Anders worden ze geïnterpreteerd als lokale paden. Zie <a href="../../../home/c-dataset-const-proc/c-log-proc-config-file/c-ins-svr-file-svr-unit.md#concept-995abff3fce34e439fb3f7f47191c80d"> Een Insight Server-bestandsservereenheid configureren</a>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Gecomprimeerd </td> 
   <td colname="col2"> Waar of onwaar. Deze waarde moet worden ingesteld op true als de XML-logbronnen die door de gegevenswerkbench-server moeten worden gelezen, gecomprimeerde gzip-bestanden zijn. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Decoderingsgroep </td> 
   <td colname="col2"> De naam van de XML-decoderingsgroep die op de XML-logbron moet worden toegepast. Deze naam moet exact overeenkomen met de naam van de corresponderende XML-decoderingsgroep die is opgegeven in het dialoogvenster <span class="wintitle"> Gegevensset logbestandsverwerking opnemen</span> bestand. Zie <a href="../../../home/c-dataset-const-proc/c-dataset-inc-files/c-types-dataset-inc-files/c-log-proc-dataset-inc-files/c-xml-dec-grps.md#concept-5eda5ab253724674832f6951e2a0d1c3"> XML-decoderingsgroepen</a>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Logbron-id </td> 
   <td colname="col2"> <p>De waarde van dit veld kan elke willekeurige tekenreeks zijn. Als een waarde wordt gespecificeerd, laat dit gebied u toe om logboekingangen van verschillende logboekbronnen voor bronidentificatie of gerichte verwerking te onderscheiden. Het veld x-log-source-id wordt gevuld met een waarde die de logbron voor elke logbestandvermelding identificeert. Als u bijvoorbeeld logitems wilt identificeren uit een bron van een logbestand met de naam XMLFile01, kunt u typen <span class="filepath"> vanuit XMLFile01</span>en die tekenreeks wordt doorgegeven aan het veld x-log-source-id voor elke logbestandvermelding uit die bron. </p> <p> Voor informatie over het x-log-source-id veld raadpleegt u <a href="../../../home/c-dataset-const-proc/c-ev-data-rec-fields.md#concept-06bda4be1a4649a2905a4422e9e6c42f"> Gebeurtenisgegevensrecordvelden</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Maskerpatroon </td> 
   <td colname="col2"> <p>Een reguliere expressie met één vastgelegd subpatroon dat een consistente naam extraheert die wordt gebruikt om de bron van een reeks logbestanden te identificeren. Alleen de bestandsnaam wordt in overweging genomen. Het pad en de extensie worden niet in aanmerking genomen voor de overeenkomst van de reguliere expressie. Als u geen <span class="wintitle"> maskerpatroon</span>, wordt er automatisch een masker gegenereerd. </p> <p> Voor de bestanden <span class="filepath"> Logs\010105server1.xml</span> en <span class="filepath"> Logs\010105server2.xml</span>het maskerpatroon <code>[0-9]{6}(.*)</code>. Dit patroon extraheert de tekenreeks "server1" of "server2" uit de bovenstaande bestandsnamen. </p> <p> Zie <a href="../../../home/c-dataset-const-proc/c-reg-exp.md#concept-070077baa419475094ef0469e92c5b9c"> Reguliere expressies</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Recursief </td> 
   <td colname="col2"> Waar of onwaar. Als deze parameter is ingesteld op true, worden alle submappen van elk pad opgegeven in <span class="wintitle"> Logpaden</span> worden gezocht naar bestanden die overeenkomen met de opgegeven bestandsnaam of het opgegeven jokertekenpatroon. De standaardwaarde is false. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Bestand negeren </td> 
   <td colname="col2"> Het pad en de bestandsnaam van het bestand met de logbestandvermeldingen die niet aan de voorwaarden van de decoder voldoen. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Begin-/eindtijd gebruiken </td> 
   <td colname="col2"> <p>Waar of onwaar. Als deze parameter is ingesteld op true en als Begintijd of Eindtijd is opgegeven, moeten alle bestanden voor deze logbron bestandsnamen hebben die beginnen met datums in de ISO-indeling (JJJMMDD). Aangenomen wordt dat elk bestand gegevens bevat voor één GMT-dag (bijvoorbeeld het tijdbereik dat op één dag begint bij 0000 GMT en de volgende dag eindigt bij 0000 GMT). Als de bestandsnamen van logbronnen niet beginnen met ISO-datums of als de bestanden gegevens bevatten die niet overeenkomen met een GMT-dag, moet deze parameter worden ingesteld op false om onjuiste resultaten te voorkomen. </p> <p> <p>Opmerking: Als de hierboven beschreven vereisten voor naamgeving en tijdbereik zijn vervuld voor de XML-bestanden en u deze parameter instelt op true, beperkt de opgegeven XML-decoderingsgroep de bestanden die worden gelezen tot de bestanden waarvan de namen ISO-datums hebben die tussen de opgegeven begintijd en eindtijd liggen. Als u deze parameter op vals plaatst, leest de server van de gegevenswerkbank alle dossiers van XML tijdens logboekverwerking om te bepalen welke dossiers gegevens binnen de Tijd van het Begin en de waaier van de Tijd van het Eind bevatten. </p> </p> <p> Voor informatie over de parameters van de Tijd van het Begin en van de Eind - tijd, zie <a href="../../../home/c-dataset-const-proc/c-log-proc-config-file/c-info-log-proc-param.md#concept-41bd49bf6b64442d91c232ec67529a3d"> Gegevensfilters</a>. </p> </td> 
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

* An **Avro-logbestand**: Dit is het het logboekformaat van Avro dat van decoder wordt geproduceerd om verkeer en handelgegevens te formatteren.
* An **Avro Decoder-bestand**: Met dit bestand kunt u waarden toewijzen aan de nieuwe Avro-indeling. U kunt de decoder instellen met de wizard Avro Decoder.

## Wizard Avro Decoder {#section-9a824b4c3d5549e7952a7111232035b2}

Deze wizard stelt het logbestand van de Avro-decoder in.

Klik met de rechtermuisknop in een werkruimte om deze te openen en selecteer **Beheer** > **Wizards** > **Wizard Avro Decoder**.

**Stap 1:** **Een Avro-logbestand selecteren**.

In deze stap kunt u een bronbestand voor het Avro-schema selecteren. Schema&#39;s zijn toegankelijk vanuit een logbestand (.log) of een bestaand decoderingsbestand (.avro). Schema&#39;s kunnen uit een van beide bestanden worden opgehaald.

| **AV-logbestand ** | Klik om een logbestand (.log) te openen om het schema boven aan het logbestand weer te geven en een decoderingsbestand te genereren. |
|---|---|
| **Avro Decoder-bestand** | Klik om het schema van een bestaand decoderingsbestand (.avro) te openen en te bewerken. |

**Stap 2: Invoervelden selecteren**.

Selecteer de invoervelden die in de gegevensset moeten worden gebruikt om de logverwerking te doorlopen. Alle velden in het bestand worden weergegeven, zodat u velden voor de feed kunt selecteren.

>[!NOTE]
>
>A [!DNL x-product(Generates row)] wordt gegeven als een serie in de gegevens wordt ontmoet. Dit veld genereert nieuwe rijen voor de geneste gegevens in een array als invoervelden. Als u bijvoorbeeld een Actief-rij hebt met veel productwaarden in een array, worden rijen gegenereerd in het invoerbestand voor elk product.

| **Standaardwaarden selecteren** | Selecteer velden die u wilt identificeren als een standaardset standaardvelden. |
|---|---|
| **Alles selecteren** | Selecteer alle velden in het bestand. |
| **Alle selecties opheffen** | Alle velden in het bestand wissen. |

**Stap 3: Selecteer velden die u wilt kopiëren om rijen te genereren.**

Omdat nieuwe rijen op basis van geneste waarden in een array kunnen worden gemaakt, moet elke nieuwe rij een tracking-id en een tijdstempel hebben. Met deze stap kunt u de velden selecteren die u wilt kopiëren naar rijen in de bovenliggende record, zoals een trackingid en tijdstempel. U kunt ook andere waarden selecteren die u aan elke rij wilt toevoegen.

| **Standaardwaarden selecteren** | Selecteer een standaardset standaardvelden waarvoor nieuwe kolomwaarden aan elke rij moeten worden toegevoegd, zoals een tracking-id en een tijdstempel. Bijvoorbeeld een [!DNL hit_source] Veld is een standaardwaarde die aan elke nieuwe rij moet worden toegevoegd (deze waarde wordt gedefinieerd als een standaardwaarde in de lijst). U kunt desgewenst andere kolomwaarden aan elke rij toevoegen. |
|---|---|
| **Alles selecteren** | Selecteer alle velden in het bestand. |
| **Alle selecties opheffen** | Alle velden in het bestand wissen. |

Gebruik de **Zoeken** om waarden in de lijst te zoeken.

**Stap 4:De naam van de decoder opgeven**

Wijs een naam toe aan de groep velden en sla deze op als een decoderingsbestand. De naam moet overeenkomen met de naam van de Decoderingsgroep die is opgegeven in de logbron.

**Stap 5: Sla het decoderingsbestand op.**

Het bestandenmenu wordt geopend om het decoderingsbestand een naam te geven en op te slaan als een [!DNL .cfg] in het **Logboeken** map.
