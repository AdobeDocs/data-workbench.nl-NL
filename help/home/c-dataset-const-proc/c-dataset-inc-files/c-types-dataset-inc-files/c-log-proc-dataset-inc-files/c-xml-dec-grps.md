---
description: De verwerking van XML-bestanden als logbronnen om decoders te definiëren voor het extraheren van gegevens uit het XML-bestand.
title: XML-decoderingsgroepen
uuid: 8fc9ab80-9a71-4fe2-a646-e830ffeb67b9
exl-id: 0b0534b7-8596-4528-a643-8a9b41dcaa33
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '1295'
ht-degree: 0%

---

# XML-decoderingsgroepen{#xml-decoder-groups}

{{eol}}

De verwerking van XML-bestanden als logbronnen om decoders te definiëren voor het extraheren van gegevens uit het XML-bestand.

>[!NOTE]
>
>Voor het definiëren van XML-decoderingsgroepen voor XML-logbronnen is kennis vereist van de structuur en inhoud van het XML-bestand, de gegevens die moeten worden geëxtraheerd en de velden waarin die gegevens worden opgeslagen. Deze sectie bevat basisbeschrijvingen van de parameters die u kunt opgeven voor decoders. De manier waarop u een decoder gebruikt, is afhankelijk van het XML-bestand dat de brongegevens bevat.

Voor informatie over formaatvereisten voor het logboekbronnen van XML, zie [Logbronnen](../../../../../home/c-dataset-const-proc/c-log-proc-config-file/c-log-sources.md#concept-6714c720fac044cbb9af003bf401b2ea). Neem contact op met Adobe voor hulp bij het definiëren van XML-decoders.

Het hoogste niveau van een decoder van XML is een decoderingsgroep (XMLDecoderGroup), die een reeks decoderingstabellen is die u gebruikt om gegevens uit een dossier van XML van een bepaald formaat te halen. Als u XML-bestanden met verschillende indelingen hebt, moet u voor elke indeling een decoderingsgroep definiëren. Elke decoderingsgroep bestaat uit een of meer decoderingstabellen.

In de volgende tabel worden de parameter Tabellen en alle subparameters beschreven die u moet opgeven om een XML-decoderingsgroep te definiëren.

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
   <td colname="col2"> <p>Elke tabel in een decoderingsgroep vertegenwoordigt één gegevensniveau dat uit het XML-bestand moet worden geëxtraheerd. Als u bijvoorbeeld gegevens over bezoekers wilt extraheren, maakt u een decoderingstabel die bestaat uit de gegevens die u voor elke bezoeker wilt extraheren. U kunt ook decoderingstabellen maken in decoderingstabellen (zie Onderliggende niveaus). </p> <p> <b>Een tabel toevoegen aan een decoderingsgroep</b> 
     <ul id="ul_C73CAD77440B4465B9FCE08BF4FA0749"> 
      <li id="li_C4B8CC5A85D942898F1EB76778105818"> Klikken met rechtermuisknop <span class="uicontrol"> Tabellen </span> en klik op <span class="uicontrol"> Nieuw toevoegen </span> &gt; <span class="uicontrol"> XMLDecoderTable </span>. </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Velden </td> 
   <td colname="col2"> <p>De uitgebreide velden (bijvoorbeeld x-trackingid, x-email) waarin de gegevens worden opgeslagen. De gegevens die in het veld moeten worden opgeslagen, worden bepaald door de subvelden Pad en/of Bewerking. </p> <p> Het pad is het niveau van het veld in het gestructureerde XML-bestand. Het pad van een veld is relatief ten opzichte van het pad van de tabel waarin het is gedefinieerd. Voorbeelden zijn <span class="filepath"> tag.tag.tag </span> of <span class="filepath"> tag.tag.tag.@attribute </span>. Paden zijn hoofdlettergevoelig. </p> <p> Een bewerking wordt toegepast op elke regel in het opgegeven pad om een uitvoerbewerking te maken. De volgende bewerkingen zijn beschikbaar: 
     <ul id="ul_B264A411D7E3446288E7E69D62150B8B"> 
      <li id="li_5936E81C0EEF46AFB780E451A04A88E4"><b>LAATSTE:</b> Het veld krijgt de waarde van de laatste instantie van het pad in het XML-bestand. </li> 
      <li id="li_7BC4F24F2CA84C2EB64B06FE09B4CAF6"><b>RANDOM:</b> Hiermee wijst u een willekeurige waarde toe aan het veld. Deze bewerking is handig als u een unieke id wilt genereren, bijvoorbeeld voor het veld x-trackingid. </li> 
      <li id="li_C1D34EA11BFB4859A25A275A9B63FB56"><b>OVERNEMEN:</b> Het gedefinieerde veld neemt de waarde over van het corresponderende veld van de bovenliggende tabel. </li> 
      <li id="li_F62FB8CD962E4E1495D9A2D5B7A78E2A"><b>"<i>constante </i>":</b> De constante moet tussen aanhalingstekens staan. U kunt een constante bewerking gebruiken om te controleren of een bepaald pad bestaat. Als het pad bestaat, wordt aan het veld de waarde van de constante toegewezen. </li> 
     </ul> </p> <p> <b>Een veld toevoegen aan een decoderingstabel</b> </p> <p> 
     <ul id="ul_91D104D927424DEA9E788E43B2F6FEA9"> 
      <li id="li_5448B01EE82349569BBFC99C9604D7B8"> Klikken met rechtermuisknop <span class="uicontrol"> Velden </span>en klik vervolgens op <span class="uicontrol"> Nieuw toevoegen </span> &gt; <span class="uicontrol"> XMLDecoderField </span>. Definieer het veld, de bewerking en het pad naar wens. </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Pad </td> 
   <td colname="col2"> <p>Het niveau binnen het gestructureerde dossier van XML waarvoor de decoderingstabel informatie bevat. Voor een onderliggende XML-decoderingstabel is het pad relatief ten opzichte van het pad van de bovenliggende tabel. Paden zijn hoofdlettergevoelig. </p> <p> Als uw XML-bestand bijvoorbeeld de structuur bevat: </p> 

    &amp;lt;bezoeker&amp;gt;
    
    &amp;nbsp;
    
    ...
    
    &amp;nbsp;
    
    &amp;lt;/bezoeker&amp;gt;
    
    &amp;lt;/logdata&amp;gt;&amp;nbsp; &lt;/code> &lt;p> dan zou het pad &lt;span class=&quot;filepath&quot;>logdata.bezoeker&lt;/span> zijn. &lt;/p> &lt;/td>
</tr> 
  <tr> 
   <td colname="col1"> Tabel </td> 
   <td colname="col2"> <p>De waarde van deze parameter moet altijd 'Logbestandvermelding' zijn. </p> <p> <p>Opmerking: Wijzig deze waarde niet zonder Adobe te raadplegen. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Kinderen </td> 
   <td colname="col2"> <p>Optioneel. Een of meer ingesloten decoderingstabellen. Elk onderliggend element bevat de hierboven beschreven parameters Velden, Pad en Tabel. </p> <p> <b>Een onderliggend element toevoegen aan een decoderingstabel</b> </p> <p> 
     <ul id="ul_902AC6CA5D66457D84CBA3194FF49BBE"> 
      <li id="li_07B4D60E7E2E4630B4878691E575936A"> Klikken met rechtermuisknop <span class="uicontrol"> Kinderen </span> en klik op <span class="uicontrol"> Nieuw toevoegen </span> &gt; <span class="uicontrol"> XMLDecoderTable </span>. Definieer het veld, de bewerking en het pad naar wens. </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

Om een dossier van XML als logboekbron voor een dataset te gebruiken, moeten de decoderingsgroepen en de lijsten van XML worden bepaald om de informatie te halen die in de dataset moet worden verwerkt. In dit voorbeeld, kunt u zien hoe te om decoderingsgroepen en lijsten voor een bron van het steekproeflogboek van XML voor een Webdataset te bepalen.

Het volgende XML-bestand bevat informatie over een websitebezoeker, zoals een Experience Cloud-id, e-mailadres, fysiek adres en informatie over de paginaweergaven van de bezoeker.

![](assets/xmlFile_LogSource.png)

Omdat we één XML-bestand hebben, hebben we maar één decoderingsgroep nodig, die we &#39;Voorbeeld-XML-indeling&#39; noemen. Deze decoderingsgroep is van toepassing op alle andere XML-bestanden met dezelfde indeling als dit bestand. Als u XML-decoderingstabellen wilt samenstellen binnen deze decoderingsgroep, moet u eerst bepalen welke gegevens u wilt extraheren en in welke velden de gegevens worden opgeslagen.

In dit voorbeeld extraheren we informatie over de bezoeker en de paginaweergaven die aan die bezoeker zijn gekoppeld. Hiertoe maken we een XML-decoderingstabel op hoofdniveau (bovenliggend) met informatie over de bezoeker en een ingesloten (onderliggende) XML-decoderingstabel met informatie over de paginaweergaven van die bezoeker.

**De informatie voor de bovenliggende tabel (bezoeker) ziet er als volgt uit**

* Een id voor het gegevenstype van elke rij gegevens in het XML-bestand. Wij gebruiken VISITOR als onze identificatie zodat wij rijen van gegevens met betrekking tot de bezoeker en niet tot de paginameningen snel kunnen identificeren. Deze waarde kan worden opgeslagen in het veld x-rowtype.
* De id van de bezoeker, die we opslaan in het veld x-trackingid.
* Het e-mailadres van de bezoeker (contact.email), dat we in het veld x-email opslaan.
* De registratiestatus van de bezoeker. Als de bezoeker een geregistreerde gebruiker is, dan kunnen wij de waarde &quot;1&quot;op het x-is-geregistreerde gebied opslaan.
* De waarde van het pad is [!DNL logdata.visitor]en de tabelwaarde is [!DNL Log Entry]. Zie de tabel XMLDecoderGroup hierboven voor informatie over deze parameters.

**De informatie voor de onderliggende tabel (paginaweergaven) ziet er als volgt uit:**

* Een id voor het gegevenstype van elke rij gegevens in het XML-bestand. We gebruiken &#39;PAGEVIEW&#39; als onze id, zodat we snel rijen met gegevens kunnen identificeren die betrekking hebben op de paginaweergaven van de bezoeker en niet alleen op de bezoeker. Deze waarde wordt opgeslagen in het veld x-rowtype.
* De ID van de bezoeker. Deze waarde wordt overgenomen van de bovenliggende tabel en wordt opgeslagen in het veld x-trackingid.
* De tijdstempel van elke paginaweergave, die wordt opgeslagen in het veld x-event-time.
* De URI van elke paginaweergave, die wordt opgeslagen in het veld cs-uri-stem.
* De waarde Pad is PadView en de waarde in Tabel is Logbestandvermelding. Zie de tabel XMLDecoderGroup hierboven voor informatie over deze parameters.

De volgende schermopname toont een deel van [!DNL Log Processing Dataset Include] bestand met de resulterende XML-decoderingsgroep voor het XML-voorbeeldbestand op basis van de besproken structuur van de bovenliggende en onderliggende XML-decoderingstabellen.

![](assets/cft_LogProc_xmldecodergroup_top.png)

![](assets/cfg_LogProcessingInclude_XMLDecoderGroup_bottom.png)

Een tabel met de uitvoer van deze decoder voor ons XML-voorbeeldbestand ziet er ongeveer als volgt uit:

| x-rowtype | cs—uri-stem | x-email | x-is-geregistreerd | x-event-time | x-tracking-id |
|---|---|---|---|---|---|
| VISITOR |  | foo@bar.com | 1 |  | 1 |
| PAGEVIEW | /index.html |  |  | 2006-01-01 08:00:00 | 1 |
| PAGEVIEW | / |  |  | 2006-01-01 08:00:30 | 1 |

U kunt een tabel als de bovenstaande tabel maken in een werkbank voor gegevens met behulp van een interface voor veldviewers. Voor informatie over de interface van de veldviewer raadpleegt u [Hulpprogramma&#39;s voor gegevensverzameling](../../../../../home/c-dataset-const-proc/c-dataset-config-tools/c-dataset-config-tools.md#concept-6e058b7691834cf79dcfd1573f78d4f5).

## De kenmerkwaarde van het XML-element lezen met #value {#section-88758428afb94f0baa5a986604d53bc1}

U kunt nu de opdracht **[!DNL #value]** in XML-paden om de waarde van een XML-element te trekken.

Als u bijvoorbeeld eerder een pad opgeeft van **`<Hit><Page name="Home Page" index="20">home.html</Page></Hit>`** u de waarde van de optie `<Page>` tag. De waarde van een `<Page>` -tags en de bijbehorende kenmerken kunt u gebruiken [!DNL Hit.Page.@name] en [!DNL Hit.Page.@index] respectievelijk. U kunt de waarde van de tag ook ophalen met **`Hit.Page.#value`** expressie.

U kunt bijvoorbeeld de waarde van de tag lezen `<varValue>` door het volgende veld in de decoder toe te voegen:

```
7 = XMLDecoderField: 
Field = string: x-varvalue-name-added 
Operation = string: LAST 
Path = string:  
<b>#value</b> 
Path = string: varValue 
Table = string: Log Entry
```

U kunt ook de waarde van de tag lezen `<Rep>` door het volgende veld in de decoder toe te voegen:

```
7 = XMLDecoderField: 
Field = string: x-rep-name-added 
Operation = string: LAST 
Path = string: Rep.# 
<b>value</b> 
Path = string: Reps 
Table = string: Log Entry
```

Als u daarentegen de waarde van een elementtag zonder kenmerk wilt lezen, kunt u `<text>` tag onder een `<line>` -tag en de bijbehorende waarde kunnen rechtstreeks worden gelezen door &quot; [!DNL text]&quot; in een pad of met [!DNL line.text], afhankelijk van de manier waarop u de decoder hebt gemaakt.

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
