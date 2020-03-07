---
description: Informatie over de gebieden van gegevens die de server van de gegevenswerkbank kan verwerken om een dataset te construeren.
solution: Analytics
title: Gegevensrecordvelden voor gebeurtenissen
topic: Data workbench
uuid: b0232bfa-0a3b-4e3d-876e-6a15a3764eae
translation-type: tm+mt
source-git-commit: 27600561841db3705f4eee6ff0aeb8890444bbc9

---


# Gegevensrecordvelden voor gebeurtenissen{#event-data-record-fields}

Informatie over de gebieden van gegevens die de server van de gegevenswerkbank kan verwerken om een dataset te construeren.

* [Informatie over gebeurtenisgegevens](../../home/c-dataset-const-proc/c-ev-data-rec-fields.md#section-3a0705f8c1824017aa4effed9903efbe)
* [Gegevensrecordvelden voor basisgebeurtenissen](../../home/c-dataset-const-proc/c-ev-data-rec-fields.md#section-a882ed7aa6af41eeb45a55bf8c1ca3d7)
* [Afgeleide Gebieden](../../home/c-dataset-const-proc/c-ev-data-rec-fields.md#section-b6c57ee2aa31469fbd5dab90e52bc677)

## Informatie over gebeurtenisgegevens {#section-3a0705f8c1824017aa4effed9903efbe}

De gebeurtenisgegevens die worden gebruikt om een dataset te bouwen verblijven in dossiers die als logboekbronnen worden bedoeld. De gegevens beschikbaar in de logboekbronnen worden genoemd gebeurtenisgegevens omdat elk gegevensverslag een transactieverslag of één enkel geval van een gebeurtenis met bijbehorende timestamp vertegenwoordigt.

De de gebeurtenisgegevens van een logboekbron worden verzameld in real time door [!DNL Sensors]. De gegevens van de gebeurtenis die door [!DNL Sensors] van HTTP en toepassingsservers worden verzameld worden overgebracht naar de servers van de gegevenswerkbank, die de gegevens in samengeperste logboek ( [!DNL .vsl]) dossiers omzetten. De gegevens van de gebeurtenis die in een vlak dossier, het dossier van XML, of een ODBC- gegevensbron verblijven worden gelezen door de server van de gegevenswerkbank, die decoders verstrekt die u bepaalt om een gemeenschappelijke reeks gegevensgebieden uit deze verschillende formaten te halen.

De volgende secties verstrekken informatie over de gegevensgebieden (die als de gebieden van het het verslag van gebeurtenisgegevens of de gebieden van de logboekingang worden bedoeld) die door worden verzameld of gelezen en aan de server van de gegevenswerkbank ter beschikking gesteld. [!DNL Sensors]

>[!NOTE]
>
>De namen van de gebieden volgen over het algemeen de noemende overeenkomst voor het W3C uitgebreide formaat van het logboekdossier. Veel van de gebieden hebben prefixen die op de bron van de informatie wijzen bevat op het gebied:

* cs wijst op mededeling van de cliënt aan de server.
* sc wijst op mededeling van de server aan de cliënt.
* s wijst op informatie van de server.
* c geeft informatie van de cliënt aan.
* x wijst op informatie die door een de softwareproduct van Adobe wordt gecreeerd.

## Gegevensrecordvelden voor basisgebeurtenissen {#section-a882ed7aa6af41eeb45a55bf8c1ca3d7}

De dossiers van het logboek ( [!DNL .vsl]) bevatten de gebieden van gebeurtenisgegevens die van servers door worden verzameld [!DNL Sensors] en door de server van de gegevenswerkbank in het proces van de datasetconstructie worden gebruikt. De volgende lijst maakt een lijst van de gebieden in een typisch verslag van gebeurtenisgegevens zoals geregistreerd door [!DNL Sensor]:

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
   <td colname="col2"> <p>Het IP adres van de cliënt zoals inbegrepen in het verzoek dat aan de server wordt gemaakt. </p> <p> Voorbeeld: 207 68 146 68 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> cs (cookie) </td> 
   <td colname="col2"> <p>De koekjes die door de cliënt met het verzoek worden verzonden. </p> <p> Voorbeeld: v1st=42FDF66DE610CF36; ASPSESSIONIDQCATDAQC=GPIBKEIBFIPLOJMKCAAEPM; </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> cs (referentie) </td> 
   <td colname="col2"> <p>Het de verwijzingskoord van HTTP dat door de cliënt naar de server met het verzoek wordt verzonden. </p> <p> Voorbeeld: <span class="filepath"> http://www.mysite.net/cgi-bin/websearch?qry </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> cs (gebruikersagent) </td> 
   <td colname="col2"> <p>Het koord dat door de cliënt met zijn verzoek wordt verzonden naar de server die op welk type van gebruikersagent wijst de cliënt is. </p> <p> Voorbeeld: Mozilla/5.0 (Windows; U; Windows NT 5.1; en-VS; Rv.1.7) Gecko/20040707 Firefox/0.9.2 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> cs-methode </td> 
   <td colname="col2"> <p>Het methodetype van het HTTP- verzoek. </p> <p> Voorbeeld: KRIJGEN </p> <p> Referentie: <span class="filepath"> http://www.w3.org/TR/2000/NOTE-shoplogfileformat-20001115/#field_method </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> cs-uri-query </td> 
   <td colname="col2"> <p>Het gedeelte van het vraagkoord van URI (stem + vraagkoord = URI). Dit wordt voorafgegaan door een vraagteken (?) en kan één of meerdere naam-waarde paren bevatten die door ampersands (&amp;) worden gescheiden. </p> <p> Voorbeeld: page=homepage </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> cs-uri-stengel </td> 
   <td colname="col2"> <p>Het stamgedeelte van URI (stam + vraagkoord = URI). De stam is de daadwerkelijke of logische weg aan het gevraagde middel op de server. </p> <p> Voorbeeld: <span class="filepath"> /index.asp </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> SC(inhoudstype) </td> 
   <td colname="col2"> <p>Het inhoudstype van het middel dat door de cliënt wordt gevraagd zoals die door de server wordt gemeld. </p> <p> Voorbeelden: tekst/html, beeld/png, beeld/gif, video/mpeg </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> sc-bytes </td> 
   <td colname="col2"> <p>Het aantal bytes van gegevens die van de server naar de cliënt in antwoord op het verzoek worden verzonden </p> <p> Voorbeeld: 4996 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> SC-status </td> 
   <td colname="col2"> <p>De statuscode die door de server aan de cliënt is teruggekeerd. </p> <p> Voorbeeld: 200 </p> <p> Referentie: <span class="filepath"> http://www.w3.org/Protocols/rfc2616/rfc2616-sec10.html </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> s-dns </td> 
   <td colname="col2"> <p>Volledig - gekwalificeerde domeinnaam of IP adres van de gastheer van het gevraagde middel. </p> <p> Voorbeeld: <span class="filepath"> www.adobe.com </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> x-experiment </td> 
   <td colname="col2"> <p>De lijst van alle gecontroleerde experimentele namen en groepen waarvan de cliënt een lid op het tijdstip van het verzoek is. </p> <p> Voorbeeld: VSHome_Exp.Group_1,VSRegistration_Exp.Group_2 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> x-timestamp </td> 
   <td colname="col2"> <p>De datum en de tijd (GMT) waarop het verzoek door de server werd ontvangen. De tijd wordt uitgedrukt als het aantal van 100 nanoseconden sinds 1 januari 1600. </p> <p> Voorbeeld: 12771098932000000 zou de x-timestamp waarde zijn voor 11:28:52.00000 op dinsdag 13 september 2005. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> x-trackingid </td> 
   <td colname="col2"> <p>De hexadecimale waarde met 64 bits van het unieke browser herkenningsteken dat in een blijvend koekje wordt gevonden zoals die door een <span class="wintitle"> Sensor wordt geplaatst </span> en door de cliënt met een verzoek aan een server wordt verstrekt. </p> <p> Voorbeeld: 42FDF66DE610CF36 </p> </td> 
  </tr> 
 </tbody> 
</table>

## Afgeleide Gebieden {#section-b6c57ee2aa31469fbd5dab90e52bc677}

De lijst hieronder maakt een lijst van voorbeelden van gebieden die door de server van de gegevenswerkbank van de het gegevensverslaggebieden van de basislijngebeurtenis worden afgeleid:

<table id="table_3B008F1314804A69AE69E8F94908F497"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Veld </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> cs(cookie)(naam) </td> 
   <td colname="col2"> De waarde van een bepaald naam-waarde paar binnen een koekje. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> cs (referentie-domein) </td> 
   <td colname="col2"> <p>De domeinnaam of IP adres van HTTP dat URI verwijst. </p> <p> <p>Opmerking:  Dit veld is alleen-lezen. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> cs (referentie-host) </td> 
   <td colname="col2"> <p>De volledige hostname van de verwijzende. </p> <p> Voorbeeld: Als cs (referrer) <span class="filepath"> http://my.domain.com/my/page is </span>, is cs (referrer-gastheer) <span class="filepath"> my.domain.com </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> cs (referentie-query)(naam) </td> 
   <td colname="col2"> <p>De waarde van een verwijzingsvraagkoord. </p> <p> <p>Opmerking:  U kunt niet tot een waarde van het verwijzingsvraagkoord toegang hebben gebruikend cs (referrer) (naam) gebied. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> cs-uri </td> 
   <td colname="col2"> <p>Volledige URI (stam + vraagkoord = volledig URI). </p> <p> Voorbeeld: <span class="filepath"> /shopping/checkout.html?product1=8Track&amp;product2=casette&amp;product3=cd </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> cs-uri-vraag (naam) </td> 
   <td colname="col2"> <p>De waarde verbonden aan de voornaam. Als de veelvoudige waarden voor de voornaam bestaan, keert dit gebied de laatste van die waarden terug. </p> Voorbeelden: 
    <ul id="ul_47BBB2E3076A46629BFCDB2A460F700B"> 
     <li id="li_AC9BB29505A54AE4AFF49438530C9EA4"> Voor URI <span class="filepath"> /shopping/checkout.html?product1=8Track&amp;product2=casette&amp;product3=cd </span>, cs-uri-query(product3) zou cd terugkeren. </li> 
     <li id="li_B036C1D0B25748E0A155DDC9B1B999CB"> Voor URI <span class="filepath"> /shopping/checkout.html?product1=8Track&amp;product1=casette </span>, <span class="wintitle"> cs-uri-query(product1) </span> zou casette terugkeren. </li> 
    </ul> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> tijdsduur </td> 
   <td colname="col2"> x-timestamp uitgedrukt als seconden sinds 1 Januari, 1970. Dit gebied wordt ook genoemd x-unixtime. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> datum </td> 
   <td colname="col2"> x-timestamp in het formaat YYYY-MM-DD. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> tijd </td> 
   <td colname="col2"> x-timestamp in het formaat HH:MM.:SS. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> x-local-timestring </td> 
   <td colname="col2"> <p>x-timestamp omgezet in lokale timezone die in het <span class="filepath"> Transformation.cfg- </span> dossier voor de dataset wordt gespecificeerd. Het formaat is JJJ-MM-DD UU:MM.:SS.mmm. </p> <p> <p>Opmerking:  U kunt ook tijdomzettingen zoals x-lokaal-timestring in het <span class="filepath"> Logboek Processing.cfg- </span> dossier bepalen. Voor informatie, zie het Dossier van de Configuratie van de Verwerking van het <a href="../../home/c-dataset-const-proc/c-log-proc-config-file/c-abt-log-proc-config-file.md"> Logboek </a>. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> x-log-bron-id </td> 
   <td colname="col2"> <p>Het herkenningsteken dat aan de logboekbron voor een bepaalde logboekingang beantwoordt. Voor het herkenningsteken dat moet worden geregistreerd, moet u het op het Van het Bron <span class="wintitle"> Logboek identiteitskaart- </span> gebied van het <span class="filepath"> Logboek Processing.cfg- </span> dossier specificeren wanneer het bepalen van de <span class="wintitle"> Sensor </span>, het logboekdossier, of ODBC- gegevensbronnen. Voor meer informatie, zie het Dossier van de Configuratie van de Verwerking van het <a href="../../home/c-dataset-const-proc/c-log-proc-config-file/c-abt-log-proc-config-file.md"> Logboek </a>. </p> <p> Voorbeeld: van VSensor01. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> x-masker </td> 
   <td colname="col2"> Het maskerpatroon van de de gegevensbronnen van de <span class="wintitle"> Sensor </span> (die uit de <span class="filepath"> .vsl- </span> dossiernamen wordt afgeleid). Voor een dossier de waarvan naam van het formaat <span class="filepath"> JJJJMMDD-SENSORID.VSL is </span>, is het x-masker SENSORID. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> x-timestring </td> 
   <td colname="col2"> x-timestamp in het formaat JJJJ-MM-DD HH:MM.:SS.mmm. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> x-unixtime </td> 
   <td colname="col2"> De decimale tijd van UNIX die uit x-timestamp wordt afgeleid. </td> 
  </tr> 
 </tbody> 
</table>

[!DNL Sensor], wanneer gebruikt op een server, kan gebieden van gebeurtenisgegevens van om het even welke geldige HTTP- verzoek of reactiekopbal verzamelen of variabele beschikbaar aan het door API van de server. Om dergelijke gebieden van gegevens te verzamelen, moet u de gewenste kopbalgebieden of de variabelen in het [!DNL txlogd.conf]configuratiedossier voor specificeren [!DNL Sensor]. Voor meer informatie, zie de *Gids van de Werkbank van Gegevens[!DNL Sensor]*.
