---
description: Informatie over de gebieden van gegevens die de server van de gegevenswerkbank kan verwerken om een dataset te construeren.
title: Gebeurtenisgegevensrecordvelden
uuid: b0232bfa-0a3b-4e3d-876e-6a15a3764eae
exl-id: 35433b87-991a-4fb9-ba6a-3217e89eb769
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '1089'
ht-degree: 0%

---

# Gebeurtenisgegevensrecordvelden{#event-data-record-fields}

{{eol}}

Informatie over de gebieden van gegevens die de server van de gegevenswerkbank kan verwerken om een dataset te construeren.

* [Gebeurtenisgegevens](../../home/c-dataset-const-proc/c-ev-data-rec-fields.md#section-3a0705f8c1824017aa4effed9903efbe)
* [Gegevensrecordvelden basislijngebeurtenis](../../home/c-dataset-const-proc/c-ev-data-rec-fields.md#section-a882ed7aa6af41eeb45a55bf8c1ca3d7)
* [Afgeleide velden](../../home/c-dataset-const-proc/c-ev-data-rec-fields.md#section-b6c57ee2aa31469fbd5dab90e52bc677)

## Gebeurtenisgegevens {#section-3a0705f8c1824017aa4effed9903efbe}

De gebeurtenisgegevens die worden gebruikt om een dataset te bouwen verblijven in dossiers die als logboekbronnen worden bedoeld. De gegevens in de logbronnen worden gebeurtenisgegevens genoemd omdat elke gegevensrecord een transactierecord of één instantie van een gebeurtenis met een bijbehorende tijdstempel vertegenwoordigt.

De gebeurtenisgegevens van een logbron worden in real time verzameld door [!DNL Sensors]. Gebeurtenisgegevens verzameld door [!DNL Sensors] van HTTP en toepassingsservers wordt overgebracht naar de servers van de gegevenswerkbank, die de gegevens in gecomprimeerd logboek ( [!DNL .vsl]). Gebeurtenisgegevens die zich in een plat bestand, XML-bestand of een ODBC-gegevensbron bevinden, worden gelezen door de gegevensworkbench-server. Deze server biedt decoders die u definieert om een algemene set gegevensvelden uit deze verschillende indelingen te extraheren.

De volgende secties bevatten informatie over de gegevensvelden (ook wel recordvelden of velden voor logitems genoemd) die worden verzameld door [!DNL Sensors] of lezen en beschikbaar stellen aan de server van de gegevenswerkbank.

>[!NOTE]
>
>De namen van de velden volgen over het algemeen de naamgevingsconventie voor de indeling van het W3C-logbestand voor extensies. Veel velden hebben voorvoegsels die de bron van de informatie in het veld aangeven:

* cs wijst op mededeling van de cliënt aan de server.
* sc verwijst naar communicatie van de server naar de client.
* s geeft informatie van de server aan.
* c geeft informatie van de client aan.
* x geeft informatie aan die door een Adobe-softwareproduct wordt gemaakt.

## Gegevensrecordvelden basislijngebeurtenis {#section-a882ed7aa6af41eeb45a55bf8c1ca3d7}

Log ( [!DNL .vsl]) bevatten de velden met gebeurtenisgegevens die van servers worden verzameld door [!DNL Sensors] en gebruikt door de server van de gegevenswerkbank in het proces van de datasetconstructie. De volgende tabel bevat een lijst met velden in een gegevensrecord voor typische gebeurtenissen zoals opgenomen door [!DNL Sensor]:

<table id="table_98E135FE4EAF44D6ADEB3C6C1C0BF6A4">
 <thead>
  <tr>
   <th colname="col1" class="entry"> Veld </th>
   <th colname="col2" class="entry"> Beschrijving </th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td colname="col1"> c-ip </td>
   <td colname="col2"> <p>Het IP-adres van de client, zoals opgenomen in het verzoek aan de server. </p> <p> Voorbeeld: 207 68 146,68 </p> </td>
  </tr>
  <tr>
   <td colname="col1"> cs(cookie) </td>
   <td colname="col2"> <p>De cookies die door de client met de aanvraag worden verzonden. </p> <p> Voorbeeld: v1st=42FDF66DE610CF36; ASPSESSIONIDQCATDAQC=GPIBKEIBFIPLOJMKCAAEPM; </p> </td>
  </tr>
  <tr>
   <td colname="col1"> cs(referentie) </td>
   <td colname="col2"> <p>De tekenreeks van de HTTP-referentie die door de client bij de aanvraag naar de server is verzonden. </p> <p> Voorbeeld: <span class="filepath"> https://www.mysite.net/cgi-bin/websearch?qry </span> </p> </td>
  </tr>
  <tr>
   <td colname="col1"> cs (user-agent) </td>
   <td colname="col2"> <p>De tekenreeks die door de client met zijn verzoek naar de server wordt verzonden en die aangeeft welk type gebruikersagent de client is. </p> <p> Voorbeeld: Mozilla/5.0 (Windows; U; Windows NT 5.1; en-US; rv:1.7) Gecko/20040707 Firefox/0.9.2 </p> </td>
  </tr>
  <tr>
   <td colname="col1"> cs-method </td>
   <td colname="col2"> <p>Het methodetype van het HTTP- verzoek. </p> <p> Voorbeeld: GET </p> <p> Referentie: <span class="filepath"> https://www.w3.org/TR/2000/NOTE-shoplogfileformat-20001115/#field_method </span> </p> </td>
  </tr>
  <tr>
   <td colname="col1"> cs-uri-query </td>
   <td colname="col2"> <p>Het gedeelte van de querytekenreeks van URI (stem + querytekenreeks = URI). Dit wordt voorafgegaan door een vraagteken (?) en kan een of meer naam-waardeparen bevatten die door ampersands (&amp;) worden gescheiden. </p> <p> Voorbeeld: page=homepage </p> </td>
  </tr>
  <tr>
   <td colname="col1"> cs-uri-stem </td>
   <td colname="col2"> <p>Het stamgedeelte van URI (stem + query string = URI). De stam is de daadwerkelijke of logische weg aan het gevraagde middel op de server. </p> <p> Voorbeeld: <span class="filepath"> /index.asp </span> </p> </td>
  </tr>
  <tr>
   <td colname="col1"> sc (inhoudstype) </td>
   <td colname="col2"> <p>Het inhoudstype van het middel dat door de cliënt wordt gevraagd zoals die door de server wordt gemeld. </p> <p> Voorbeelden: text/html, image/png, image/gif, video/mpeg </p> </td>
  </tr>
  <tr>
   <td colname="col1"> sc-bytes </td>
   <td colname="col2"> <p>Het aantal bytes aan gegevens dat door de server naar de client is verzonden als reactie op de aanvraag </p> <p> Voorbeeld: 4996 </p> </td>
  </tr>
  <tr>
   <td colname="col1"> sc-status </td>
   <td colname="col2"> <p>De statuscode die door de server aan de client wordt geretourneerd. </p> <p> Voorbeeld: 200 </p> <p> Referentie: <span class="filepath"> https://www.w3.org/Protocols/rfc2616/rfc2616-sec10.html </span> </p> </td>
  </tr>
  <tr>
   <td colname="col1"> s-dns </td>
   <td colname="col2"> <p>Het volledig - gekwalificeerde domeinnaam of IP adres van de gastheer van het gevraagde middel. </p> <p> Voorbeeld: <span class="filepath"> www.adobe.com </span> </p> </td>
  </tr>
  <tr>
   <td colname="col1"> x-experiment </td>
   <td colname="col2"> <p>De lijst met alle gecontroleerde experimentele namen en groepen waarvan de client lid is op het moment van de aanvraag. </p> <p> Voorbeeld: VSHome_Exp.Group_1,VSRegistration_Exp.Group_2 </p> </td>
  </tr>
  <tr>
   <td colname="col1"> x-timestamp </td>
   <td colname="col2"> <p>De datum en tijd (GMT) waarop het verzoek door de server is ontvangen. De tijd wordt uitgedrukt als het aantal 100 nanoseconden sinds 1 januari 1600. </p> <p> Voorbeeld: 127710989320000000 zou de x-tijdstempelwaarde voor 11 zijn:28:52.000000 op dinsdag 13 september 2005. </p> </td>
  </tr>
  <tr>
   <td colname="col1"> x-trackingid </td>
   <td colname="col2"> <p>De hexadecimale 64-bits waarde van de unieke browser-id die wordt gevonden in een permanente cookie, zoals ingesteld door een <span class="wintitle"> Sensor </span> en door de client worden verstrekt met een aanvraag aan een server. </p> <p> Voorbeeld: 42FDF66DE610CF36 </p> </td>
  </tr>
 </tbody>
</table>

## Afgeleide velden {#section-b6c57ee2aa31469fbd5dab90e52bc677}

In de onderstaande tabel staan voorbeelden van velden die door de gegevensworkbench-server zijn afgeleid van de recordvelden voor basislijngegevens:

<table id="table_3B008F1314804A69AE69E8F94908F497">
 <thead>
  <tr>
   <th colname="col1" class="entry"> Veld </th>
   <th colname="col2" class="entry"> Beschrijving </th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td colname="col1"> cs(cookie)(name) </td>
   <td colname="col2"> De waarde van een bepaald naam-waardepaar binnen een cookie. </td>
  </tr>
  <tr>
   <td colname="col1"> cs(reference-domain) </td>
   <td colname="col2"> <p>De domeinnaam of het IP-adres van de HTTP-verwijzende URI. </p> <p> <p>Opmerking: Dit veld is alleen-lezen. </p> </p> </td>
  </tr>
  <tr>
   <td colname="col1"> cs(referentie-host) </td>
   <td colname="col2"> <p>De volledige hostnaam van de verwijzende. </p> <p> Voorbeeld: Als cs(referencerer) is <span class="filepath"> https://my.domain.com/my/page </span>, cs(reference-host) is <span class="filepath"> my.domain.com </span>. </p> </td>
  </tr>
  <tr>
   <td colname="col1"> cs(reference-query)(name) </td>
   <td colname="col2"> <p>De waarde van een queryqueryqueryqueryqueryqueryqueryqueryqueryqueryqueryqueryqueryqueryqueryreeks. </p> <p> <p>Opmerking: U hebt geen toegang tot een stringwaarde van een verwijzersquery via het veld cs(reference)(name). </p> </p> </td>
  </tr>
  <tr>
   <td colname="col1"> cs-uri </td>
   <td colname="col2"> <p>De volledige URI (stem + querytekenreeks = gehele URI). </p> <p> Voorbeeld: <span class="filepath"> /shopping/checkout.html?product1=8Track&amp;product2=casette&amp;product3=cd </span> </p> </td>
  </tr>
  <tr>
   <td colname="col1"> cs-uri-query(name) </td>
   <td colname="col2"> <p>De waarde die aan de opgegeven naam is gekoppeld. Als er meerdere waarden bestaan voor de opgegeven naam, wordt in dit veld het laatste van deze waarden geretourneerd. </p> Voorbeelden:
    <ul id="ul_47BBB2E3076A46629BFCDB2A460F700B">
     <li id="li_AC9BB29505A54AE4AFF49438530C9EA4"> Voor de URI <span class="filepath"> /shopping/checkout.html?product1=8Track&amp;product2=casette&amp;product3=cd </span>, cs-uri-query(product3) retourneert cd. </li>
     <li id="li_B036C1D0B25748E0A155DDC9B1B999CB"> Voor de URI <span class="filepath"> /shopping/checkout.html?product1=8Track&amp;product1=casette </span>, <span class="wintitle"> cs-uri-query(product1) </span> retourneert casette. </li>
    </ul> <p> </p> </td>
  </tr>
  <tr>
   <td colname="col1"> ctime </td>
   <td colname="col2"> x-timestamp uitgedrukt als seconden sinds 1 januari 1970. Dit veld wordt ook x-unixtime genoemd. </td>
  </tr>
  <tr>
   <td colname="col1"> date </td>
   <td colname="col2"> x-timestamp in de notatie YYYY-MM-DD. </td>
  </tr>
  <tr>
   <td colname="col1"> tijd </td>
   <td colname="col2"> x-timestamp in de notatie HH:MM:SS. </td>
  </tr>
  <tr>
   <td colname="col1"> x-local-timestring </td>
   <td colname="col2"> <p>x-timestamp omgezet in lokale timezone die in wordt gespecificeerd <span class="filepath"> Transformation.cfg </span> bestand voor de gegevensset. De notatie is YYY-MM-DD HH:MM:SS.mmm. </p> <p> <p>Opmerking: U kunt ook tijdconversies, zoals x-local-timestring, definiëren in het dialoogvenster <span class="filepath"> Logverwerking.cfg </span> bestand. Zie voor meer informatie <a href="../../home/c-dataset-const-proc/c-log-proc-config-file/c-abt-log-proc-config-file.md"> Logboekverwerkingsconfiguratiebestand </a>. </p> </p> </td>
  </tr>
  <tr>
   <td colname="col1"> x-log-source-id </td>
   <td colname="col2"> <p>De id die overeenkomt met de logbron voor een bepaald logbestandvermelding. Als u de id wilt opnemen, moet u deze opgeven in het dialoogvenster <span class="wintitle"> Logbron-id </span> van het <span class="filepath"> Logverwerking.cfg </span> bestand bij definiëren <span class="wintitle"> Sensor </span>, logbestand of ODBC-gegevensbronnen. Zie voor meer informatie <a href="../../home/c-dataset-const-proc/c-log-proc-config-file/c-abt-log-proc-config-file.md"> Logboekverwerkingsconfiguratiebestand </a>. </p> <p> Voorbeeld: VSensor01. </p> </td>
  </tr>
  <tr>
   <td colname="col1"> x-mask </td>
   <td colname="col2"> Het maskerpatroon van het dialoogvenster <span class="wintitle"> Sensor </span> gegevensbronnen (afgeleid van de <span class="filepath"> .vsl </span> bestandsnamen). Voor een bestand waarvan de naam de indeling heeft <span class="filepath"> JJJMMDD-SENSORID.VSL </span>, x-mask is SENSORID. </td>
  </tr>
  <tr>
   <td colname="col1"> x-timestring </td>
   <td colname="col2"> x-timestamp in de notatie YYYY-MM-DD HH:MM:SS.mmm. </td>
  </tr>
  <tr>
   <td colname="col1"> x-unixtime </td>
   <td colname="col2"> De decimale UNIX-tijd die is afgeleid van x-timestamp. </td>
  </tr>
 </tbody>
</table>

[!DNL Sensor]Wanneer deze gegevens op een server worden gebruikt, kunnen ze velden met gebeurtenisgegevens verzamelen van elke geldige HTTP-aanvraag- of antwoordheader of variabele die beschikbaar is via de API van de server. Als u dergelijke gegevensvelden wilt verzamelen, moet u de gewenste koptekstvelden of variabelen opgeven in het dialoogvenster [!DNL txlogd.conf]configuratiebestand voor [!DNL Sensor]. Zie voor meer informatie de *Data Workbench [!DNL Sensor] Hulplijn*.
