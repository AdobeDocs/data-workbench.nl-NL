---
description: De bronnen van het logboek zijn dossiers die de gegevens bevatten die moeten worden gebruikt om een dataset te bouwen.
solution: Analytics
title: Logbronnen
topic: Data workbench
uuid: ea21c3d7-9188-4ba8-bacd-052d678bd799
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Logbronnen{#log-sources}

De bronnen van het logboek zijn dossiers die de gegevens bevatten die moeten worden gebruikt om een dataset te bouwen.

De gegevens beschikbaar in de logboekbronnen worden genoemd gebeurtenisgegevens omdat elk gegevensverslag een transactieverslag of één enkel geval van een gebeurtenis vertegenwoordigt. De server van de gegevenswerkbank kan logboekbronnen verwerken die uit gegevens worden afgeleid die door [!DNL Sensors] of uit andere gegevensbronnen worden verzameld worden gehaald.

* **Gegevens verzameld door [!DNL Sensors]: ** De gegevens die door [!DNL Sensors] van HTTP en toepassingsservers worden verzameld worden overgebracht naar de servers van de gegevenswerkbank, die de gegevens in hoogst samengedrukte logboek ( [!DNL .vsl]) dossiers omzetten. Zie [Sensorbestanden](../../../home/c-dataset-const-proc/c-log-proc-config-file/c-log-sources.md#concept-b25f11c477b54032a15b6117b3bf9009).

* **Gegevens die door de Server van het Inzicht worden getrokken:** De server van de gegevenswerkbank leest gebeurtenisgegevens in vlakke dossiers, de dossiers van XML, of ODBC-Volgzame gegevensbestanden, en gebruikt zijn decoders om de gewenste elementen van de gegevens te halen. Dergelijke gebeurtenisgegevens hoeven geen geheugen-ingezetene te zijn, maar de verslagen die de gegevens bevatten moeten een volgende identiteitskaart omvatten. Zie de Dossiers [van het](../../../home/c-dataset-const-proc/c-log-proc-config-file/c-log-sources.md#concept-3d4fb817c057447d90f166b1183b461e)Logboek, de Bronnen [van het Logboek van](../../../home/c-dataset-const-proc/c-log-proc-config-file/c-log-sources.md#concept-c7b154e93748447b986e97f6ef688887)XML, en [Gegevensbronnen](../../../home/c-dataset-const-proc/c-log-proc-config-file/c-odbc-data-sources.md#concept-5f2cf635081d44beab826ef5ec8cf4e3)ODBC.

**Om een logboekbron toe te voegen**

1. Open [!DNL Log Processing.cfg] in gegevenswerkbank.
1. Klik **[!UICONTROL Log Sources]** met de rechtermuisknop en klik op **[!UICONTROL Add New]**.

1. Selecteer één van het volgende:

   * **[!UICONTROL Sensor]**
   * **[!UICONTROL Log File]**
   * **[!UICONTROL XML Log Source]**
   * **[!UICONTROL ODBC Data Source]**

1. De specifieke parameters die worden gebruikt om een dataset te bepalen variëren gebaseerd op het type van logboekbron dat in het de configuratieproces van de dataset moet worden gebruikt. Specificeer de parameters zoals vermeld in de sectie die aan de aangewezen logboekbron beantwoordt:

   * [Sensorbestanden](../../../home/c-dataset-const-proc/c-log-proc-config-file/c-log-sources.md#concept-b25f11c477b54032a15b6117b3bf9009)
   * [Logbestanden](../../../home/c-dataset-const-proc/c-log-proc-config-file/c-log-sources.md#concept-3d4fb817c057447d90f166b1183b461e)
   * [XML-logbestanden](../../../home/c-dataset-const-proc/c-log-proc-config-file/c-log-sources.md#concept-c7b154e93748447b986e97f6ef688887)
   * [ODBC-gegevensbronnen](../../../home/c-dataset-const-proc/c-log-proc-config-file/c-odbc-data-sources.md#concept-5f2cf635081d44beab826ef5ec8cf4e3)

1. Nadat u uw logboekbron (en veranderingen in andere parameters) in het [!DNL Log Processing.cfg] dossier hebt bepaald, sparen het dossier plaatselijk en sla het aan uw datasetprofiel op de server van de gegevenswerkbank op.

   >[!NOTE]
   >
   >Een server van de gegevenswerkbank [!DNL File Server Unit] kan [!DNL Sensor] dossiers, logboekdossiers, en de dossiers van XML ontvangen en opslaan en hen dienen aan de server van de gegevenswerkbank [!DNL Data Processing Units] die de dataset construeert. Zie het [Vormen van een Eenheid](../../../home/c-dataset-const-proc/c-log-proc-config-file/c-ins-svr-file-svr-unit.md#concept-995abff3fce34e439fb3f7f47191c80d)van de Server van het Dossier van het Inzicht.

   U kunt de configuratie van om het even welke logboekbron van een openen [!DNL Transformation Dependency Map]. Voor informatie over [!DNL Transformation Dependency Map], zie de Hulpmiddelen van de Configuratie van de [Dataset](../../../home/c-dataset-const-proc/c-dataset-config-tools/c-dataset-config-tools.md#concept-6e058b7691834cf79dcfd1573f78d4f5).

<!--
c_sensor_files.xml
-->

## Eisen {#section-d5901a4872774ad5bd01a18db114f1f2}

De gegevens van de gebeurtenis die door [!DNL Sensors] van HTTP en toepassingsservers worden verzameld worden overgebracht naar de servers van de gegevenswerkbank, die de gegevens in hoogst samengedrukte logboek ( [!DNL .vsl]) dossiers omzetten. Het [!DNL .vsl] dossierformaat wordt beheerd door de server van de gegevenswerkbank, en elk dossier heeft een naam van het formaat:

JJJJMMDD-*SENSORID*.VSL

waar JJJJMMDD de datum van het dossier is, en *SENSORID* is de naam (die door uw organisatie wordt toegewezen) die erop wijst welke [!DNL Sensor] verzamelde en de gegevens overbracht aan de server van de gegevenswerkbank.

## Parameters {#section-5c3f1e341c284486aeba3452057da7f3}

Voor [!DNL Sensor] dossiers, zijn de volgende parameters beschikbaar:

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
   <td colname="col2"> <p>De folders waar de <span class="filepath"> .vsl</span> - dossiers worden opgeslagen. De standaardplaats is de folder van Logboeken. Een relatieve weg verwijst naar de installatiefolder van de server van de gegevenswerkbank. </p> <p>U kunt vervangingskarakters gebruiken om te specificeren welke <span class="filepath"> .vsl</span> dossiers aan proces: 
     <ul id="ul_AE144ED0FAB94FE8B32599A058659DE1"> 
      <li id="li_1E4E4CFD72C34B5EB71A3C59877950A9"> * komt overeen met een willekeurig aantal tekens </li> 
      <li id="li_4664400FC12E44B39B28438B85D20ED8"> ? komt overeen met één teken </li> 
     </ul> </p> <p> Bijvoorbeeld, past de logboekweg Logs \*.vsl <span class="filepath"> aan om het even welk dossier in de folder van Logboeken die in</span> .vsl <span class="filepath"></span>beëindigt. De logweg <span class="filepath"> Logs\*-SENSOR?.vsl</span> past dossiers in de folder van Logboeken met om het even welke datum (JJJJJMMDD) en één enkel karakter na SENSOR, zoals in SENSOR1 aan. </p> <p> Als u alle subdirectories van de gespecificeerde weg wilt zoeken, moet u de Recursieve parameter aan waar plaatsen. </p> <p> <p>Opmerking: Als de bestanden moeten worden gelezen van de bestandsservereenheid <span class="wintitle"></span>van een gegevenswerkbankserver, moet u de juiste URI('s) invoeren in de parameter Log Paths. Bijvoorbeeld, past <span class="filepath"> URI /Logs/*-*.vsl</span> om het even welk <span class="filepath"> .vsl</span> dossier in de folder van Logboeken aan. Zie het <a href="../../../home/c-dataset-const-proc/c-log-proc-config-file/c-ins-svr-file-svr-unit.md#concept-995abff3fce34e439fb3f7f47191c80d"> Vormen van een Eenheid</a>van de Server van het Dossier van het Inzicht. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> logboekserver </td> 
   <td colname="col2">Informatie (Adres, Naam, Haven, etc.) noodzakelijk om met een dossierserver te verbinden. Als er een ingang in de parameter van de Server van het Logboek is, worden de Wegen <span class="wintitle"> van het</span> Logboek geïnterpreteerd als URIs. Anders, worden zij geïnterpreteerd als lokale wegen. Zie het <a href="../../../home/c-dataset-const-proc/c-log-proc-config-file/c-ins-svr-file-svr-unit.md#concept-995abff3fce34e439fb3f7f47191c80d"> Vormen van een Eenheid</a>van de Server van het Dossier van het Inzicht. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> ID Logbron </td> 
   <td colname="col2"> <p>De waarde van deze parameter kan om het even welk koord zijn. Als een waarde wordt gespecificeerd, laat deze parameter u toe om logboekingangen van verschillende logboekbronnen voor bronidentificatie of gerichte verwerking te onderscheiden. Het x-logboek-bron-identiteitskaart- gebied is bevolkt met een waarde die de logboekbron voor elke logboekingang identificeren. Bijvoorbeeld, als u logboekingangen van een <span class="wintitle"> Sensor</span> genoemd VSensor01 wilt identificeren, kon u <span class="filepath"> van VSensor01</span>typen, en dat koord zou tot het x-logboek-bron-identiteitskaart- gebied voor elke logboekingang uit die bron worden overgegaan. </p> <p> Voor informatie over het x-logboek-bron-identiteitskaart- gebied, zie de Gebieden <a href="../../../home/c-dataset-const-proc/c-ev-data-rec-fields.md#concept-06bda4be1a4649a2905a4422e9e6c42f"> van het Verslag van de Gegevens van de</a>Gebeurtenis. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Recursief </td> 
   <td colname="col2"> Waar of vals. Als de reeks aan waar, alle subdirectories van elke weg die in de Wegen <span class="wintitle"> van het</span> Logboek wordt gespecificeerd wordt gezocht naar dossiers die het gespecificeerde dossier - naam of vervangingspatroon aanpassen. De standaardwaarde is vals. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Begin-/eindtijden gebruiken </td> 
   <td colname="col2"> <p>Waar of vals. Als de reeks aan waar en de Tijd van het Begin of de Tijd van het Eind wordt gespecificeerd, dan moeten alle dossiers voor deze logboekbron dossiernamen hebben die met data in het formaat van ISO beginnen (JJJJMMDD). Aangenomen wordt dat elk dossier gegevens voor één GMT dag bevat (bijvoorbeeld, de tijdwaaier die bij 0000 GMT op één dag begint en die bij 0000 GMT de volgende dag eindigt). Als de logbrondossiers gegevens bevatten die niet aan een dag GMT beantwoorden, dan moet deze parameter aan vals worden geplaatst om onjuiste resultaten te vermijden. </p> <p> <p>Opmerking: Standaard voldoen <span class="filepath"> .vsl- </span>bestanden met gegevens die door de <span class="wintitle"> sensor</span> zijn verzameld, automatisch aan de vereisten voor naamgeving en tijdbereik die hierboven zijn beschreven. Als u deze parameter aan waar plaatst, verwerkt de server van de gegevenswerkbank altijd gegevens van dossiers de waarvan namen de data omvatten van ISO die tussen de gespecificeerde Tijd van het Begin en Tijd van het Eind vallen. Als u deze parameter aan vals plaatst, leest de server van de gegevenswerkbank alle <span class="filepath"> .vsl</span> dossiers tijdens logboekverwerking om te bepalen welke dossiers gegevens binnen de waaier van de Tijd van het Begin en van de Tijd van het Eind bevatten. </p> </p> <p> Voor informatie over de parameters van de Tijd van het Begin en van de Tijd van het Eind, zie de Filters <a href="../../../home/c-dataset-const-proc/c-log-proc-config-file/c-info-log-proc-param.md#concept-41bd49bf6b64442d91c232ec67529a3d"></a>van Gegevens. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Gebruik niet de configuratieparameters voor [!DNL Sensor] gegevensbronnen om te bepalen welke logboekingangen binnen een logboekdossier in een dataset zouden moeten worden omvat. In plaats daarvan, opstelling de gegevensbron om aan alle logboekdossiers binnen een folder te richten. Dan gebruik de parameters van de Tijd van het Begin en van de Tijd van het Eind van [!DNL Log Processing.cfg] om te bepalen welke logboekingangen in het construeren van de dataset zouden moeten worden gebruikt. Zie [Gegevensfilters](../../../home/c-dataset-const-proc/c-log-proc-config-file/c-info-log-proc-param.md#concept-41bd49bf6b64442d91c232ec67529a3d).

<!--
c_log_files.xml
-->

Het dossier dat de gebeurtenisgegevens bevat moet aan de volgende vereisten voldoen:

* Elk verslag van gebeurtenisgegevens in het dossier moet door één lijn worden vertegenwoordigd.
* De velden in een record moeten, al dan niet leeg, worden gescheiden door een ASCII-afbakening. De server van de gegevenswerkbank vereist u niet om een specifieke afbakening te gebruiken. U kunt om het even welk karakter gebruiken dat geen lijn-beëindigend karakter is en niet overal binnen de gebeurtenisgegevens zelf verschijnt.
* Elke record in het bestand moet het volgende bevatten:

   * Een volgnummer
   * Een tijdstempel

* Om begin en eindtijden voor gegevensverwerking te specificeren, moet elk dossier - de naam moet van de vorm zijn:

   * [!DNL YYYYMMDD-SOURCE.log]
   waar *JJJMMDD* de Greenwich Mean Time (GMT) dag van alle gegevens in het dossier is, en de BRON ** is een variabele die de bron van de gegevens identificeert in het dossier.

   >[!NOTE]
   >
   >Tevreden om de Raadplegende Diensten van Adobe voor een overzicht van de logboekdossiers te contacteren die u van plan bent om in de dataset op te nemen.

## Parameters {#section-83a861ac24954d54bbb9530e4d8bf23c}

Voor het logboekbronnen van logboekdossiers, zijn de parameters in de volgende lijst beschikbaar.

>[!NOTE]
>
>De verwerking van de bronnen van het logboekdossier vereist extra parameters die in een [!DNL Log Processing Dataset Include] dossier worden bepaald, dat een ondergroep van de parameters omvat in een [!DNL Log Processing.cfg] dossier evenals speciale parameters bevat voor het bepalen van decoders voor het halen van gegevens uit het logboekdossier. Voor informatie over het bepalen van decoders voor de bronnen van het logboekdossier, zie de Groepen [van de Decoder van het Dossier van de](../../../home/c-dataset-const-proc/c-dataset-inc-files/c-types-dataset-inc-files/c-log-proc-dataset-inc-files/c-text-file-dec-groups.md#concept-0db34988e17c41bfb1797f1d8e78aabd)Tekst.

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
   <td colname="col2"> Het herkenningsteken voor de bron van het logboekdossier. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Logpaden </td> 
   <td colname="col2"> <p>De folders waar de logboekdossiers worden opgeslagen. De standaardplaats is de folder van Logboeken. Een relatieve weg verwijst naar de installatiefolder van de server van de gegevenswerkbank. </p> <p> U kunt vervangingskarakters gebruiken om te specificeren welke logboekdossiers aan proces: 
     <ul id="ul_1F02D26A08D846E2A3114E5C33F60ECF"> 
      <li id="li_ECAE1C03A1C448A1B86AE00B3A955708"> * komt overeen met een willekeurig aantal tekens. </li> 
      <li id="li_24FDB500C5934CAAA4124C435DF4B290"> ? komt overeen met één teken. </li> 
     </ul> </p> <p> Bijvoorbeeld, past de logboekweg <span class="filepath"> Logs \*.log</span> om het even welk dossier in de folder van Logboeken aan die in <span class="filepath"> .log</span>beëindigt. </p> <p> Als u alle subdirectories van de gespecificeerde weg wilt zoeken, dan moet u de Recursieve parameter aan waar plaatsen. </p> <p> Als de bestanden moeten worden gelezen van de bestandsservereenheid <span class="wintitle"></span>van een gegevenswerkbankserver, moet u de juiste URI('s) invoeren in de parameter Log Paths. Bijvoorbeeld, past <span class="filepath"> URI/Logs/*.log</span> om het even welk <span class="filepath"> .log</span> dossier in de folder van Logboeken aan. Zie het <a href="../../../home/c-dataset-const-proc/c-log-proc-config-file/c-ins-svr-file-svr-unit.md#concept-995abff3fce34e439fb3f7f47191c80d"> Vormen van een Eenheid</a>van de Server van het Dossier van het Inzicht. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> logboekserver </td> 
   <td colname="col2"> Informatie (Adres, Naam, Haven, etc.) noodzakelijk om met een dossierserver te verbinden. Als er een ingang in de parameter van de Server van het Logboek is, worden de Wegen <span class="wintitle"> van het</span> Logboek geïnterpreteerd als URIs. Anders, worden zij geïnterpreteerd als lokale wegen. Zie het <a href="../../../home/c-dataset-const-proc/c-log-proc-config-file/c-ins-svr-file-svr-unit.md#concept-995abff3fce34e439fb3f7f47191c80d"> Vormen van een Eenheid</a>van de Server van het Dossier van het Inzicht. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Gecomprimeerd </td> 
   <td colname="col2"> Waar of vals. Deze waarde zou aan waar moeten worden geplaatst als de logboekdossiers die door de server van de gegevenswerkbank moeten worden gelezen gecomprimeerde gzip dossiers zijn. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Decodergroep </td> 
   <td colname="col2"> De naam van de decodergroep van het tekstdossier die op de logboekbron van het logboekdossier moet worden toegepast. Deze naam moet precies de naam van de overeenkomstige decodergroep van het tekstdossier aanpassen die in de Dataset van de Verwerking van het <span class="wintitle"> Logboek wordt gespecificeerd omvat</span> dossier. Zie <a href="../../../home/c-dataset-const-proc/c-dataset-inc-files/c-types-dataset-inc-files/c-log-proc-dataset-inc-files/c-text-file-dec-groups.md#concept-0db34988e17c41bfb1797f1d8e78aabd"> de Decodergroepen</a>van het Dossier van de Tekst. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> ID Logbron </td> 
   <td colname="col2"> <p>De waarde van deze parameter kan om het even welk koord zijn. Als een waarde wordt gespecificeerd, laat deze parameter u toe om logboekingangen van verschillende logboekbronnen voor bronidentificatie of gerichte verwerking te onderscheiden. Het x-logboek-bron-identiteitskaart- gebied is bevolkt met een waarde die de logboekbron voor elke logboekingang identificeren. Bijvoorbeeld, als u logboekingangen van een bron van het logboekdossier genoemde LogFile01 wilt identificeren, kon u <span class="filepath"> van LogFile01</span>typen, en dat koord zou worden overgegaan tot het x-logboek-bron-identiteitskaart- gebied voor elke logboekingang uit die bron. </p> <p> Voor informatie over het x-logboek-bron-identiteitskaart- gebied, zie de Gebieden <a href="../../../home/c-dataset-const-proc/c-ev-data-rec-fields.md#concept-06bda4be1a4649a2905a4422e9e6c42f"> van het Verslag van de Gegevens van de</a>Gebeurtenis. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Maskerpatroon </td> 
   <td colname="col2"> <p>Een regelmatige uitdrukking met één enkel vangend subpatroon dat een verenigbare naam haalt die wordt gebruikt om de bron van een reeks logboekdossiers te identificeren. Slechts wordt het dossier - naam overwogen. De weg en de uitbreiding worden niet overwogen voor de regelmatige uitdrukking aanpassing. Als u geen <span class="wintitle"> maskerpatroon</span>specificeert, dan wordt een masker automatisch geproduceerd. </p> <p> Voor de dossiers <span class="filepath"> Logs \ 010105server1.log</span> en <span class="filepath"> Logs \ 010105server2.log</span>, zou het <span class="wintitle"> maskerpatroon</span> [0-9] \ {6 \} (.*). Dit patroon haalt het koord "server1"of "server2"uit de dossiernamen hierboven. </p> <p> Zie <a href="../../../home/c-dataset-const-proc/c-reg-exp.md#concept-070077baa419475094ef0469e92c5b9c"> Regelmatige expressies</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Recursief </td> 
   <td colname="col2"> Waar of vals. Als deze parameter aan waar wordt geplaatst, worden alle subdirectories van elke weg die in de Wegen <span class="wintitle"> van het</span> Logboek wordt gespecificeerd gezocht naar dossiers die het gespecificeerde dossier - naam of vervangingspatroon aanpassen. De standaardwaarde is vals. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Bestand afwijzen </td> 
   <td colname="col2"> De weg en het dossier - noem van het dossier dat de logboekingangen bevat die niet aan de voorwaarden van de decoder voldoen. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Begin-/eindtijden gebruiken </td> 
   <td colname="col2"> <p>Waar of vals. Als deze parameter aan waar wordt geplaatst en de Tijd van het Begin of de Tijd van het Eind wordt gespecificeerd, dan moeten alle dossiers voor deze logboekbron dossiernamen hebben die met data in het formaat van ISO (JJJJMMDD) beginnen. Aangenomen wordt dat elk dossier gegevens voor één GMT dag bevat (bijvoorbeeld, de tijdwaaier die bij 0000 GMT op één dag begint en die bij 0000 GMT de volgende dag eindigt). Als de logboekbronnen dossiernamen niet met de data van ISO beginnen, of als de dossiers gegevens bevatten die niet aan een dag GMT beantwoorden, dan moet deze parameter aan vals worden geplaatst om onjuiste resultaten te vermijden. </p> <p> <p>Opmerking:  Als aan de hierboven beschreven vereisten voor het noemen en de tijdwaaier voor de logboekdossiers wordt voldaan en u plaatst deze parameter aan waar, beperkt de gespecificeerde groep van de decoder van het tekstdossier de dossiers die aan die worden gelezen de waarvan namen de data hebben van ISO die tussen de gespecificeerde Tijd van het Begin en Tijd van het Eind vallen. Als u deze parameter aan vals plaatst, leest de server van de gegevenswerkbank alle logboekdossiers tijdens logboekverwerking om te bepalen welke dossiers gegevens binnen de waaier van de Tijd van het Begin en van de Tijd van het Eind bevatten. </p> </p> <p> Voor informatie over de parameters van de Tijd van het Begin en van de Tijd van het Eind, zie de Filters <a href="../../../home/c-dataset-const-proc/c-log-proc-config-file/c-info-log-proc-param.md#concept-41bd49bf6b64442d91c232ec67529a3d"></a>van Gegevens. </p> </td> 
  </tr> 
 </tbody> 
</table>

In dit voorbeeld, wordt de dataset geconstrueerd van twee types van logboekbronnen.

Bron 0 van het logboek specificeert logboekdossiers die van gebeurtenisgegevens worden geproduceerd door worden gevangen [!DNL Sensor]. Deze gegevensbron richt aan een folder genoemd Logboeken en aan alle dossiers in die folder met een [!DNL .vsl] dossier - noem uitbreiding.

Bron van het logboek 1 richt aan alle dossiers in de folder van Logboeken met een [!DNL .txt] dossier - noem uitbreiding. De decodergroep voor deze logboekbron wordt genoemd &quot;de Logboeken van de Tekst.&quot;

![](assets/cfg_LogProcessing_LogSources.png)

U zou logboekdossiers niet moeten schrappen of bewegen nadat de gegevensbronnen voor een dataset zijn bepaald. Slechts zouden de pas gecreëerde logboekdossiers aan de folder voor de gegevensbronnen moeten worden toegevoegd.

<!--
c_xml_log_sources.xml
-->

Het dossier dat de gebeurtenisgegevens bevat moet aan de volgende vereisten voldoen:

* De gegevens van de gebeurtenis moeten in een behoorlijk geformatteerd dossier van XML met aangewezen ouder-kind verhoudingen worden omvat.
* Een unieke decodergroep moet voor elk het dossierformaat van XML bestaan. Voor informatie over het construeren van een decodergroep, zie de Groepen [van de Decoder van](../../../home/c-dataset-const-proc/c-dataset-inc-files/c-types-dataset-inc-files/c-log-proc-dataset-inc-files/c-xml-dec-grps.md#concept-5eda5ab253724674832f6951e2a0d1c3)XML.
* Elk bezoekersverslag in het dossier moet bevatten:

   * Een volgnummer
   * Een tijdstempel

* Om begin en eindtijden voor gegevensverwerking te specificeren, moet elk dossier - de naam moet van de vorm zijn

[!DNL YYYYMMDD-SOURCE.log]

waar *JJJMMDD* de Greenwich Mean Time (GMT) dag van alle gegevens in het dossier is, en de BRON ** is een variabele die de bron van de gegevens identificeert in het dossier.

Bij een voorbeeld van een dossier van XML dat aan deze vereisten voldoet, zie de Groepen [van de Decoder van](../../../home/c-dataset-const-proc/c-dataset-inc-files/c-types-dataset-inc-files/c-log-proc-dataset-inc-files/c-xml-dec-grps.md#concept-5eda5ab253724674832f6951e2a0d1c3)XML.

>[!NOTE]
>
>Tevreden om de Raadplegende Diensten van Adobe voor een overzicht van de het logboekdossiers van XML te contacteren die u van plan bent om in de dataset op te nemen.

## Parameters {#section-d07b96d7f6ad4affb9cc0a0bc1b88c4d}

Voor het logboekbronnen van XML, zijn de parameters in de volgende lijst beschikbaar.

>[!NOTE]
>
>De verwerking van het logboekbronnen van XML vereist extra parameters die in een [!DNL Log Processing Dataset Include] dossier worden bepaald, dat een ondergroep van de parameters omvat in een [!DNL Log Processing.cfg] dossier evenals speciale parameters bevat voor het bepalen van decoders voor het halen van gegevens uit het dossier van XML. Voor informatie over het bepalen van decoders voor het logboekbronnen van XML, zie de Groepen [van de Decoder van](../../../home/c-dataset-const-proc/c-dataset-inc-files/c-types-dataset-inc-files/c-log-proc-dataset-inc-files/c-xml-dec-grps.md#concept-5eda5ab253724674832f6951e2a0d1c3)XML.

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
   <td colname="col2"> Het herkenningsteken voor de het logboekbron van XML. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Logpaden </td> 
   <td colname="col2"> <p>De folders waar de het logboekbronnen van XML worden opgeslagen. De standaardplaats is de folder van Logboeken. Een relatieve weg verwijst naar de installatiefolder van de server van de gegevenswerkbank. </p> <p> U kunt vervangingskarakters gebruiken om te specificeren welke het logboekbronnen van XML aan proces te verwerken: 
     <ul id="ul_0AE5D0ADE0F64CFAA856492A49239F58"> 
      <li id="li_4CBC0D1733F04258B3A55CC6FA714538 "> * komt overeen met een willekeurig aantal tekens </li> 
      <li id="li_81B597436A1241FF94E73C18A0ABBFA1"> ? komt overeen met één teken </li> 
     </ul> </p> <p>Bijvoorbeeld, past de logboekweg <span class="filepath"> Logs \*.xml</span> om het even welk dossier in de folder van Logboeken aan die in <span class="filepath"> .xml</span>beëindigt. </p> <p> Als u alle subdirectories van de gespecificeerde weg wilt zoeken, moet u het <span class="wintitle"> Recursieve</span> gebied aan waar plaatsen. </p> <p> <p>Opmerking: Als de bestanden moeten worden gelezen van de <span class="wintitle"> File Server Unit</span>van een gegevenswerkbankserver, moet u de juiste URI('s) invoeren in het veld <span class="wintitle"> Log Paths</span> . Bijvoorbeeld, past <span class="filepath"> URI/Logs/*.xml</span> om het even welk <span class="filepath"> .xml</span> dossier in de folder van Logboeken aan. Zie het <a href="../../../home/c-dataset-const-proc/c-log-proc-config-file/c-ins-svr-file-svr-unit.md#concept-995abff3fce34e439fb3f7f47191c80d"> Vormen van een Eenheid</a>van de Server van het Dossier van het Inzicht. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> logboekserver </td> 
   <td colname="col2"> Informatie (Adres, Naam, Haven, etc.) noodzakelijk om met een dossierserver te verbinden. Als er een ingang op het gebied van de Server <span class="wintitle"> van het</span> Logboek is, worden de Wegen <span class="wintitle"> van het</span> Logboek geïnterpreteerd als URIs. Anders, worden zij geïnterpreteerd als lokale wegen. Zie het <a href="../../../home/c-dataset-const-proc/c-log-proc-config-file/c-ins-svr-file-svr-unit.md#concept-995abff3fce34e439fb3f7f47191c80d"> Vormen van een Eenheid</a>van de Server van het Dossier van het Inzicht. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Gecomprimeerd </td> 
   <td colname="col2"> Waar of vals. Deze waarde zou aan waar moeten worden geplaatst als de het logboekbronnen van XML die door de server van de gegevenswerkbank moeten worden gelezen gecomprimeerde gzip dossiers zijn. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Decodergroep </td> 
   <td colname="col2"> De naam van de de decodergroep van XML die op de het logboekbron van XML moet worden toegepast. Deze naam moet precies de naam van de overeenkomstige de decodergroep aanpassen van XML die in de Dataset van de Verwerking van het <span class="wintitle"> Logboek wordt gespecificeerd omvat</span> dossier. Zie <a href="../../../home/c-dataset-const-proc/c-dataset-inc-files/c-types-dataset-inc-files/c-log-proc-dataset-inc-files/c-xml-dec-grps.md#concept-5eda5ab253724674832f6951e2a0d1c3"> XML-decodergroepen</a>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> ID Logbron </td> 
   <td colname="col2"> <p>De waarde van dit gebied kan om het even welk koord zijn. Als een waarde wordt gespecificeerd, laat dit gebied u toe om logboekingangen van verschillende logboekbronnen voor bronidentificatie of gerichte verwerking te onderscheiden. Het x-logboek-bron-identiteitskaart- gebied is bevolkt met een waarde die de logboekbron voor elke logboekingang identificeren. Bijvoorbeeld, als u logboekingangen van een bron van het logboekdossier genoemde XMLFile01 wilt identificeren, kon u <span class="filepath"> van XMLFile01</span>typen, en dat koord zou worden overgegaan tot het x-logboek-bron-identiteitskaart- gebied voor elke logboekingang uit die bron. </p> <p> Voor informatie over het x-logboek-bron-identiteitskaart- gebied, zie de Gebieden <a href="../../../home/c-dataset-const-proc/c-ev-data-rec-fields.md#concept-06bda4be1a4649a2905a4422e9e6c42f"> van het Verslag van de Gegevens van de</a>Gebeurtenis. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Maskerpatroon </td> 
   <td colname="col2"> <p>Een regelmatige uitdrukking met één enkel vangend subpatroon dat een verenigbare naam haalt die wordt gebruikt om de bron van een reeks logboekdossiers te identificeren. Slechts wordt het dossier - naam overwogen. De weg en de uitbreiding worden niet overwogen voor de regelmatige uitdrukking aanpassing. Als u geen <span class="wintitle"> maskerpatroon</span>specificeert, dan wordt een masker automatisch geproduceerd. </p> <p> Voor de dossiers <span class="filepath"> Logs \ 010105server1.xml</span> en <span class="filepath"> Logs \ 010105server2.xml</span>, zou het maskerpatroon [0-9] \ {6 \} zijn (.*). Dit patroon haalt het koord "server1"of "server2"uit de dossiernamen hierboven. </p> <p> Zie <a href="../../../home/c-dataset-const-proc/c-reg-exp.md#concept-070077baa419475094ef0469e92c5b9c"> Regelmatige expressies</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Recursief </td> 
   <td colname="col2"> Waar of vals. Als deze parameter aan waar wordt geplaatst, worden alle subdirectories van elke weg die in de Wegen <span class="wintitle"> van het</span> Logboek wordt gespecificeerd gezocht naar dossiers die het gespecificeerde dossier - naam of vervangingspatroon aanpassen. De standaardwaarde is vals. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Bestand afwijzen </td> 
   <td colname="col2"> De weg en het dossier - noem van het dossier dat de logboekingangen bevat die niet aan de voorwaarden van de decoder voldoen. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Begin-/eindtijden gebruiken </td> 
   <td colname="col2"> <p>Waar of vals. Als deze parameter aan waar wordt geplaatst en de Tijd van het Begin of de Tijd van het Eind wordt gespecificeerd, dan moeten alle dossiers voor deze logboekbron dossiernamen hebben die met data in het formaat van ISO (JJJJMMDD) beginnen. Aangenomen wordt dat elk dossier gegevens voor één GMT dag bevat (bijvoorbeeld, de tijdwaaier die bij 0000 GMT op één dag begint en die bij 0000 GMT de volgende dag eindigt). Als de logboekbronnen dossiernamen niet met de data van ISO beginnen, of als de dossiers gegevens bevatten die niet aan een dag GMT beantwoorden, dan moet deze parameter aan vals worden geplaatst om onjuiste resultaten te vermijden. </p> <p> <p>Opmerking:  Als de het noemen en tijdwaaiervereisten hierboven worden beschreven voor de dossiers van XML worden tevredengesteld en u plaatst deze parameter aan waar, beperkt de gespecificeerde de decodergroep van XML de dossiers die aan die worden gelezen de waarvan namen de data hebben van ISO die tussen de gespecificeerde Tijd van het Begin en Tijd van het Eind vallen. Als u deze parameter aan vals plaatst, leest de server van de gegevenswerkbank alle dossiers van XML tijdens logboekverwerking om te bepalen welke dossiers gegevens binnen de waaier van de Tijd van het Begin en van de Tijd van het Eind bevatten. </p> </p> <p> Voor informatie over de parameters van de Tijd van het Begin en van de Tijd van het Eind, zie de Filters <a href="../../../home/c-dataset-const-proc/c-log-proc-config-file/c-info-log-proc-param.md#concept-41bd49bf6b64442d91c232ec67529a3d"></a>van Gegevens. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>U zou de het logboekbronnen van XML niet moeten schrappen of bewegen nadat de gegevensbronnen voor een dataset zijn bepaald. Slechts zouden de pas gecreëerde dossiers van XML aan de folder voor de gegevensbronnen moeten worden toegevoegd.

<!--
AVRO-log-file.xml
-->

De Avro-gegevensfeed biedt een efficiëntere manier om gegevens te integreren in een gegevenswerkbank:

<!-- <a id="section_45E3105B971C4220AE9CF573BEBF6080"></a> -->

* Avro verstrekt een enig-bronformaat voor verkeer en handelsgegevens.
* Het voer Avro is samengeperste gegevens van veelvoudige bronkoeken die per dag worden verstrekt. Het voorziet slechts bevolkte gebieden en verstrekt controle en berichteigenschappen, toegang tot historische gegevens, en auto-terugwinning.
* Het schema, een zelf-bepalende lay-out van het logboekdossiers van Avro, is inbegrepen aan het begin van elk dossier.
* De nieuwe gebieden worden toegevoegd met ondersteunende informatie om de gegevens van de Werkbank van Gegevens zonder enige veranderingen in de decoder worden vereist in te nemen. Deze omvatten:

   * Evenementen: 1-250 (voorheen 1-75)
   * Aangepaste gebeurtenissen: 1-1000 (versus 1-100)
   * Toegang tot oplossingsvariabelen voor mobiele, sociale en videogegevens

>[!NOTE]
>
>Bovendien staat het gebruiken van het voer van de Avro directe toegang tot om het even welke nieuwe gebieden in het voer zonder sluiting toe, die de gebieden toestaat om zonder de vereisten van het de dienstuur worden bijgewerkt.

De Avro-gegevensinvoer wordt in afzonderlijke bestanden ingesteld:

* Een **Avro-logbestand**: Dit is het het logboekformaat van de Avro dat van de decoder wordt geproduceerd om verkeer en handelsgegevens te formatteren.
* Een dossier van de **Avro decoder**: Dit dossier laat u waarden in het nieuwe formaat van het Avro in kaart brengen. U kunt opstelling de decoder gebruikend de Tovenaar van de Decoder van de Avro.

## wizard Avro Decoder {#section-9a824b4c3d5549e7952a7111232035b2}

Deze tovenaar plaatst - omhoog het dossier van het decoderlogboek van de Avro.

Om te openen, klik in een werkruimte met de rechtermuisknop aan en selecteer **Admin** > **Tovenaar** > de Tovenaar **van de Decoder van de** Avro.

**Stap 1:** **Selecteer een Avro- logboekbestand**.

In deze stap, kunt u een brondossier voor het schema van de Router selecteren. De schema&#39;s kunnen van een logboekdossier (.log) of een bestaand decoderdossier (.avro) worden betreden. Schema&#39;s kunnen uit een van beide bestanden worden gehaald.

| **Bestandslogbestand van AV *** | Klik om een logboek (.log) dossier te openen om het schema bij de bovenkant van het logboekdossier te bekijken en decoderdossier te produceren. |
|---|---|
| **Avro-decoderbestand** | Klik om het schema van een bestaand decoder (.avro) dossier te openen en uit te geven. |

**Stap 2: Selecteer Invoervelden**.

Selecteer de inputgebieden die in de gegevensreeks moeten worden gebruikt om door logboekverwerking over te gaan. Alle gebieden in het dossier zullen worden getoond, toestaand u om gebieden voor het voer te selecteren.

>[!NOTE]
>
>Er wordt een [!DNL x-product(Generates row)] veld opgegeven als er een array in de gegevens wordt aangetroffen. Dit gebied produceert nieuwe rijen voor de genestelde gegevens in een serie als inputgebieden. Bijvoorbeeld, als u een rij van de Hit met vele waarden van het Product in een serie hebt, dan zullen de rijen in het inputdossier voor elk product worden geproduceerd.

| **Standaardwaarden selecteren** | Selecteer gebieden om als standaardreeks standaardgebieden te identificeren. |
|---|---|
| **Alles selecteren** | Selecteer alle velden in het bestand. |
| **Alles deselecteren** | Ontruim alle gebieden in het dossier. |

**Stap 3: Selecteer gebieden die worden gekopieerd om rijen te produceren.**

Omdat de nieuwe rijen van genestelde waarden in een serie kunnen worden gecreeerd, moet elke nieuwe gecreeerde rij een volgende identiteitskaart en een timestamp hebben. Deze stap staat u toe om de gebieden te selecteren die aan rijen van het ouderverslag, zoals een volgende identiteitskaart en timestamp moeten worden gekopieerd. U kunt andere waarden ook selecteren u aan elke rij wilt toevoegen.

| **Standaardwaarden selecteren** | Selecteer een standaardreeks standaardgebieden die nieuwe kolomwaarden vereisen die aan elke rij, zoals een volgende identiteitskaart en timestamp worden toegevoegd. Bijvoorbeeld, is een [!DNL hit_source] gebied een standaardwaarde die wordt vereist om aan elke nieuwe rij (het wordt gedefinieerd als standaardwaarde in de lijst) te worden toegevoegd. U kunt andere kolomwaarden aan elke rij toevoegen zoals nodig. |
|---|---|
| **Alles selecteren** | Selecteer alle velden in het bestand. |
| **Alles deselecteren** | Ontruim alle gebieden in het dossier. |

Gebruik het vakje van het **Onderzoek** om waarden in de lijst te vinden.

**Stap 4:De decodernaam opgeven**

Wijs een naam voor de groep gebieden toe en spaar als decoderdossier op. De naam zou de de groepsnaam van de Decoder moeten aanpassen die in uw logboekbron wordt gespecificeerd.

**Stap 5: Sparen het decoderdossier.**

Het dossiermenu zal openen om het decoderdossier te noemen en als [!DNL .cfg] dossier in de omslag van **Logboeken** op te slaan.
