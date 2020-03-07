---
description: De verwerking van de dossiers van XML als logboekbronnen om decoders te bepalen voor het halen van gegevens uit het dossier van XML.
solution: Analytics
title: XML-decodergroepen
topic: Data workbench
uuid: 8fc9ab80-9a71-4fe2-a646-e830ffeb67b9
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# XML-decodergroepen{#xml-decoder-groups}

De verwerking van de dossiers van XML als logboekbronnen om decoders te bepalen voor het halen van gegevens uit het dossier van XML.

>[!NOTE]
>
>Het bepalen van de decodergroepen van XML voor het logboekbronnen van XML vereist kennis van de structuur en de inhoud van het dossier van XML, de te halen gegevens, en de gebieden waarin dat gegeven wordt opgeslagen. Deze sectie verstrekt basisbeschrijvingen van de parameters die u voor decoders kunt specificeren. De manier waarin u om het even welke decoder gebruikt hangt van het dossier van XML af dat uw brongegevens bevat.

Voor informatie over formaatvereisten voor het logboekbronnen van XML, zie de [Bronnen](../../../../../home/c-dataset-const-proc/c-log-proc-config-file/c-log-sources.md#concept-6714c720fac044cbb9af003bf401b2ea)van het Logboek. Voor hulp bij het bepalen van de decoders van XML, contacteer Adobe.

Het hoogste niveau van een decoder van XML is een decodergroep (XMLDecoderGroup), die een reeks decoderlijsten is die u gebruikt om gegevens uit een dossier van XML van een bepaald formaat te halen. Als u de dossiers van XML van verschillende formaten hebt, dan moet u een decodergroep voor elk formaat bepalen. Elke decodergroep bestaat uit één of meerdere decoderlijsten.

De volgende lijst beschrijft de parameter van Lijsten en alle subparameters die u moet specificeren om een de decodergroep van XML te bepalen.

<table id="table_06C40C5149E94548A1B0C2ED4397624B"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Parameter </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Tabellen </td> 
   <td colname="col2"> <p>Elke lijst in een decodergroep vertegenwoordigt één niveau van gegevens die uit het dossier van XML moeten worden gehaald. Bijvoorbeeld, als u gegevens over bezoekers wilt halen, dan zou u een decoderlijst creëren die uit de informatie bestaat u voor elke bezoeker wilt halen. U kunt decoderlijsten binnen decoderlijsten ook tot stand brengen (zie Kinderen). </p> <p> <b>Om een lijst aan een decodergroep toe te voegen</b> 
     <ul id="ul_C73CAD77440B4465B9FCE08BF4FA0749"> 
      <li id="li_C4B8CC5A85D942898F1EB76778105818"> Klik <span class="uicontrol"> Lijsten met de rechtermuisknop aan </span> en de klik <span class="uicontrol"> voegt nieuw </span> &gt; <span class="uicontrol"> XMLDecoderTable toe </span>. </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Gebieden </td> 
   <td colname="col2"> <p>De uitgebreide gebieden (bijvoorbeeld, x-trackingidentiteitskaart, x-e-mail) waarin het gegeven wordt opgeslagen. De gegevens die in het veld moeten worden opgeslagen, worden bepaald door de subvelden Pad en/of Verrichting. </p> <p> De weg is het niveau van het gebied binnen het gestructureerde dossier van XML. De weg van een gebied is met betrekking tot de weg van de lijst waarin het wordt bepaald. Voorbeelden zijn <span class="filepath"> tag.tag.tag </span> of <span class="filepath"> tag.tag.tag.tag.@attribuut </span>. Merk op dat de wegen case-sensitive zijn. </p> <p> Een verrichting wordt toegepast op elke lijn in de gespecificeerde weg om een output te veroorzaken. De volgende activiteiten zijn beschikbaar: 
     <ul id="ul_B264A411D7E3446288E7E69D62150B8B"> 
      <li id="li_5936E81C0EEF46AFB780E451A04A88E4"><b>LAATST:</b> Het gebied neemt de waarde van het laatste voorkomen van de weg in het dossier van XML. </li> 
      <li id="li_7BC4F24F2CA84C2EB64B06FE09B4CAF6"><b>RANDOM:</b> Wijst een willekeurige waarde aan het gebied toe. Deze verrichting is nuttig als u een unieke identiteitskaart, zoals voor het x-trackingïdgebied moet produceren. </li> 
      <li id="li_C1D34EA11BFB4859A25A275A9B63FB56"><b>INHERIT:</b> Het bepaalde gebied erft zijn waarde van het overeenkomstige gebied van de ouderlijst. </li> 
      <li id="li_F62FB8CD962E4E1495D9A2D5B7A78E2A"><b>"<i>constante </i>":</b> De constante moet in aanhalingstekens worden ingesloten. U kunt een constante verrichting gebruiken om het bestaan van een bepaalde weg te controleren; als de weg bestaat, dan wordt het gebied toegewezen de waarde van de constante. </li> 
     </ul> </p> <p> <b>Om een gebied aan een decoderlijst toe te voegen</b> </p> <p> 
     <ul id="ul_91D104D927424DEA9E788E43B2F6FEA9"> 
      <li id="li_5448B01EE82349569BBFC99C9604D7B8"> Klik <span class="uicontrol"> Gebieden met de rechtermuisknop aan </span>, dan klik <span class="uicontrol"> toevoegen nieuw </span> &gt; <span class="uicontrol"> XMLDecoderField </span>. Bepaal Gebied, Verrichting en Weg zoals aangewezen. </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Pad </td> 
   <td colname="col2"> <p>Het niveau binnen het gestructureerde dossier van XML waarvoor de decoderlijst informatie bevat. Voor een de decoderlijst van kindXML, is de weg met betrekking tot de weg van de ouderlijst. Merk op dat de wegen case-sensitive zijn. </p> <p> Bijvoorbeeld, als uw dossier van XML de structuur bevat: </p> 

    &amp;lt;bezoeker&amp;gt;
    
    &amp;nbsp;
    
    ...
    
    &amp;nbsp;
    
    &amp;lt;/bezoeker&amp;gt;
    
    &amp;lt;/logdata&amp;gt;&amp;nbsp; &lt;/code> &lt;p> dan zou het pad &lt;span class=&quot;filepath&quot;> logdata zijn.bezoeker &lt;/span>. &lt;/p> &lt;/td>
</tr> 
  <tr> 
   <td colname="col1"> Tabel </td> 
   <td colname="col2"> <p>De waarde van deze parameter zou altijd "Ingang van het Logboek moeten zijn." </p> <p> <p>Opmerking:  Verander deze waarde niet zonder Adobe te raadplegen. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Kinderen </td> 
   <td colname="col2"> <p>Optioneel. Één of meerdere ingebedde decoderlijsten. Elk kind omvat de Gebieden, de Weg, en de hierboven beschreven parameters van de Lijst. </p> <p> <b>Om een kind aan een decoderlijst toe te voegen</b> </p> <p> 
     <ul id="ul_902AC6CA5D66457D84CBA3194FF49BBE"> 
      <li id="li_07B4D60E7E2E4630B4878691E575936A"> Klik <span class="uicontrol"> Kinderen met de rechtermuisknop aan </span> en de klik <span class="uicontrol"> voegt nieuw toe </span> &gt; <span class="uicontrol"> XMLDecoderTable </span>. Bepaal Gebied, Verrichting en Weg zoals aangewezen. </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

Om een dossier van XML als logboekbron voor een dataset te gebruiken, moeten de de decodergroepen en lijsten van XML worden bepaald om de informatie te halen die in de dataset moet worden verwerkt. In dit voorbeeld, kunt u zien hoe te om decodergroepen en lijsten voor een het logboekbron van steekproefXML voor een Webdataset te bepalen.

Het volgende dossier van XML bevat informatie over een websitebezoeker, met inbegrip van een identiteitskaart van de Wolk van de Ervaring, e-mailadres, fysiek adres, en informatie over de de paginameningen van de bezoeker.

![](assets/xmlFile_LogSource.png)

Aangezien wij één enkel dossier van XML hebben, hebben wij slechts één decodergroep nodig, die wij &quot;het Formaat van XML van de Steekproef noemen.&quot; Deze decodergroep is op een andere dossiers van XML van het zelfde formaat van toepassing zoals dit dossier. Om te beginnen construerend de decoderlijsten van XML binnen deze decodergroep, moeten wij eerst bepalen welke informatie wij willen halen en de gebieden waarin de gegevens zullen worden opgeslagen.

In dit voorbeeld, halen wij informatie over de bezoeker en de paginameningen verbonden aan die bezoeker. Om dit te doen, creëren wij een top-level (ouder) de decoderlijst van XML met informatie over de bezoeker en een ingebedde (kind) de decoderlijst van XML met informatie over de paginameningen van die bezoeker.

**De informatie voor de ouder (bezoeker) lijst is als volgt**

* Een gegevenstype herkenningsteken voor elke rij van gegevens in het dossier van XML. Wij gebruiken VISITOR als onze identificator zodat wij rijen van gegevens met betrekking tot de bezoeker en niet tot de paginameningen snel kunnen identificeren. We kunnen deze waarde opslaan in het x-rowtype veld.
* De bezoekersidentiteitskaart, die we opslaan in het x-trackingid veld.
* Het e-mailadres van de bezoeker (contact.email), dat we in het veld x-email opslaan.
* De inschrijvingsstatus van de bezoeker. Als de bezoeker een geregistreerde gebruiker is, dan kunnen wij waarde &quot;1&quot;op het x-is-geregistreerde gebied opslaan.
* De waarde van de Weg is, [!DNL logdata.visitor]en de waarde van de Lijst is [!DNL Log Entry]. Voor informatie over deze parameters, zie de lijst XMLDecoderGroup hierboven.

**De informatie voor de kind (paginameningen) lijst is als volgt:**

* Een gegevenstype herkenningsteken voor elke rij van gegevens in het dossier van XML. We gebruiken &quot;PAGEVIEW&quot; als onze identificator, zodat we snel rijen gegevens kunnen identificeren die betrekking hebben op de weergave van de bezoekerspagina en niet alleen op de bezoeker. We slaan deze waarde op in het x-rowtype veld.
* De bezoekersidentiteitskaart Deze waarde wordt geërft van de ouderlijst en op het x-trackingidentiteitskaart- gebied opgeslagen.
* De timestamp van elke paginamening, die op het x-gebeurtenis-tijd gebied wordt opgeslagen.
* URI van elke paginamening, die op het cs-uri-stengebied wordt opgeslagen.
* De waarde van de Weg is paginaleving, en de waarde van de Lijst is &quot;de Ingang van het Logboek.&quot; Voor informatie over deze parameters, zie de lijst XMLDecoderGroup hierboven.

De volgende het schermvangst toont een gedeelte van [!DNL Log Processing Dataset Include] dossier met de resulterende de decodergroep van XML voor het dossier van steekproefXML dat op de besproken structuur van de ouder en de decoderlijsten van kindXML wordt gebaseerd.

![](assets/cft_LogProc_xmldecodergroup_top.png)

![](assets/cfg_LogProcessingInclude_XMLDecoderGroup_bottom.png)

Een lijst die de output van deze decoder voor ons dossier van steekproefXML toont kijkt iets als het volgende:

| x-rowtype | cs—uri-stengel | x-e-mail | x-is-geregistreerd | x-gebeurtenis-tijd | x-tracking-id |
|---|---|---|---|---|---|
| BEZOEKER |  | foo@bar.com | 1 |  | 1 |
| PAGEVIEW | /index.html |  |  | 2006-01-01 08:00:00 | 1 |
| PAGEVIEW | / |  |  | 2006-01-01 08:00:30 | 1 |

U kunt een lijst zoals hierboven in gegevenswerkbank tot stand brengen door een interface van de gebiedskijker te gebruiken. Voor informatie over de interface van de gebiedskijker, zie de Hulpmiddelen [van de Configuratie van de](../../../../../home/c-dataset-const-proc/c-dataset-config-tools/c-dataset-config-tools.md#concept-6e058b7691834cf79dcfd1573f78d4f5)Dataset.

## Het gebruiken van #waarde op het element van XML om zijn attributenwaarde te lezen {#section-88758428afb94f0baa5a986604d53bc1}

U kunt de **[!DNL #value]** markering in de wegen van XML nu gebruiken om de waarde van een element van XML te trekken.

Bijvoorbeeld, eerder specificerend een weg van **`<Hit><Page name="Home Page" index="20">home.html</Page></Hit>`** verlaten u niet de waarde van de `<Page>` markering kunt lezen. Om de waarde van een `<Page>` markering en zijn attributen te lezen, kunt u [!DNL Hit.Page.@name] en [!DNL Hit.Page.@index] respectievelijk gebruiken. U kunt de waarde van de markering ook trekken gebruikend **`Hit.Page.#value`** uitdrukking.

Bijvoorbeeld, kunt u de waarde van markering lezen `<varValue>` door het volgende gebied in decoder toe te voegen:

```
7 = XMLDecoderField: 
Field = string: x-varvalue-name-added 
Operation = string: LAST 
Path = string:  
<b>#value</b> 
Path = string: varValue 
Table = string: Log Entry
```

Op dezelfde manier kunt u de waarde van markering lezen `<Rep>` door het volgende gebied in decoder toe te voegen:

```
7 = XMLDecoderField: 
Field = string: x-rep-name-added 
Operation = string: LAST 
Path = string: Rep.# 
<b>value</b> 
Path = string: Reps 
Table = string: Log Entry
```

In tegenstelling, om de waarde van elementenmarkering zonder attributen te lezen, kan een `<text>` markering onder een `<line>` markering en zijn waarde direct worden gelezen door &quot; [!DNL text]&quot;in een weg te geven of te gebruiken [!DNL line.text], afhankelijk van hoe u de decoder hebt gebouwd.

```
2 = XMLDecoderField: 
Field = string: x-chat-text 
Operation = string: LAST 
Path = string:  
<b>text</b> 
Path = string:  
<b>line</b> 
Table = string: Log Entry
```

