---
description: De exporteurs verstrekken de instructies voor het zetten van de gebeurtenisgegevens.
solution: Analytics
title: Exporteurs definiëren
topic: Data workbench
uuid: 565d4482-6c25-407c-bda7-0d116180902a
translation-type: tm+mt
source-git-commit: 27600561841db3705f4eee6ff0aeb8890444bbc9

---


# Exporteurs definiëren{#defining-exporters}

De exporteurs verstrekken de instructies voor het zetten van de gebeurtenisgegevens.

De functionaliteit van de transformatie verstrekt drie types van exporteurs voor het uitvoeren van [!DNL .vsl] dossiers, logboekdossiers, de dossiers van XML, en gegevens ODBC als [!DNL .vsl] dossiers, tekstdossiers, of afgebakende tekstdossiers die door de het laden van DataWarehouse routines, controlebureaus, of andere doelstellingen kunnen worden gebruikt.

>[!NOTE]
>
>Voor een exporteur om behoorlijk te werken, moet de logboekbron aan de aangewezen vereisten voldoen die in de sectie van de Bronnen [van het](../../../../../home/c-dataset-const-proc/c-log-proc-config-file/c-log-sources.md#concept-6714c720fac044cbb9af003bf401b2ea) Logboek van het Dossier [van de Configuratie van de Verwerking van het](../../../../../home/c-dataset-const-proc/c-log-proc-config-file/c-abt-log-proc-config-file.md)Logboek worden besproken.

**Om een exporteur te definiëren**

1. Open [!DNL Transform.cfg] in gegevenswerkbank. Zie [om het dossier](../../../../../home/c-dataset-const-proc/c-transf-func/c-config-files-transf/t-ins-transf-file/t-ins-transf-file.md#task-857fc535ccdb4c39b763179efa4b0f13)van Transform.cfg van het Inzicht uit te geven.
1. Klik **[!UICONTROL Exporters]** met de rechtermuisknop en klik op **[!UICONTROL Add New]**.
1. Selecteer een van de volgende opties:

   * **[!UICONTROL ExportTextFile]**
   * **[!UICONTROL ExportDelimitedTextFile]**
   * **[!UICONTROL ExportVSLFile]**
   >[!NOTE]
   >
   >Voor de [!DNL ExportVSLFile] optie, worden alle uitgebreide gebieden in het inputdossier en alle user-defined gebieden van de vorm cs (*kopbal*) altijd geschreven aan het VSL- outputdossier. Als u een bestaand uitgebreid gebied beschrijft, wordt de nieuwe waarde geschreven aan het outputdossier, zelfs als het gebied leeg is.

1. Geef de parameters van Exporteurs in het configuratiedossier uit gebruikend de volgende lijst als gids:

   <table id="table_35C380DB6E4F42448C149D5EC185213C"> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> Parameter </th> 
      <th colname="col2" class="entry"> Beschrijving </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> Gegevensformaat </td> 
      <td colname="col2"> <p>Alleen voor <span class="wintitle"> ExporterenTextFile</span> . Het formaat van elke outputlijn, die uit gebiedsnaam bestaat ontsnapt (uitgedrukt als %<i>veldnaam</i>%) en een andere gewenste vaste tekst. Het formaat zou een lijnseparator moeten omvatten, typisch [CR] [LF]. </p> <p> Een letterlijk percententeken (%) kan in het formaatkoord worden ingebed door het karakter te ontsnappen zoals hier getoond: %% </p> <p> Een voorbeeld van een ingang voor de parameter van het Formaat van Gegevens is <span class="filepath"> %x-timestring% %x-trackingid%[CR][LF]</span>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> Gebieden </td> 
      <td colname="col2">Alleen voor <span class="wintitle"> ExporterenDelimitedTextFile</span> . Namen van de gebieden die output moeten zijn. </td> 
      </tr> 
      <tr> 
      <td colname="col1"> Afbakening </td> 
      <td colname="col2"> <p>Optioneel. Alleen voor <span class="wintitle"> ExporterenDelimitedTextFile</span> . Karakter dat wordt gebruikt om de gebieden in het outputdossier te scheiden. </p> <p> De software kan geen grenzen aan afbakeningen die in de waarden van de gegevens inbegrepen zijn. Dientengevolge, adviseert Adobe niet gebruikend komma's als afbakeningen. </p> <p> Als u de sleutel van CTRL onderdrukt en binnen de parameter van de Afbakening met de rechtermuisknop aanklikt, verschijnt een menu van het <span class="wintitle"> Tussenvoegsel</span> . Dit menu bevat een lijst van speciale karakters die vaak als afbakeningen worden gebruikt. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> Lijnscheider </td> 
      <td colname="col2">Optioneel. Alleen voor <span class="wintitle"> ExporterenDelimitedTextFile</span> . De tekens die worden gebruikt om lijnen in de uitvoerbestanden te scheiden. De standaardwaarde is [CR] [LF]. </td> 
      </tr> 
      <tr> 
      <td colname="col1"> Naam </td> 
      <td colname="col2"> <p>Optioneel. Identificatiecode van de exporteur. Deze naam verschijnt in de <span class="wintitle"> Gedetailleerde interface van de Status</span> . </p> <p> Voor informatie over de <span class="wintitle"> Gedetailleerde interface van de Status</span> , zie de Gids <i>van de Gebruiker van de Werkbank van</i>Gegevens. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> Opmerkingen </td> 
      <td colname="col2"> Optioneel. Opmerkingen over de exporteur. </td> 
      </tr> 
      <tr> 
      <td colname="col1"> Uitvoerpad </td> 
      <td colname="col2"> <p>Weg waar de outputdossiers moeten worden opgeslagen. De weg is met betrekking tot de omslag van de de serverinstallatie van de gegevenswerkbank. </p> <p> <p>Opmerking: De server van de gegevenswerkbank die outputgegevens opslaat verwerkt server #0 in het <span class="filepath"> profile.cfg</span> - dossier. </p> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> Bestandsrotatieperiode </td> 
      <td colname="col2"> <p>Optioneel. De frequentie waarbij het gegeven naar het outputdossier wordt uitgevoerd. Elk outputdossier bevat gegevens met betrekking tot een specifieke tijdspanne genoemd de omwentelingsperiode. Alle tijdberekeningen zijn in GMT: Één dag begint bij middernacht GMT en beëindigt de volgende dag bij middernacht GMT, zelfs als de gegevens die aan het dossier worden geschreven een gebied omvatten dat aan lokale tijd is omgezet. </p> <p> De beschikbare waarden zijn als volgt: </p> 
      <ul id="ul_64F56D093E2E4D07ACB7D7921F4E6FA1"> 
       <li id="li_E4985C7F56E443049AFF57B0270032D6"> JAAR. Elk bestand bevat gegevens voor één kalenderjaar. </li> 
       <li id="li_42E59BB7A5704C85A6079ED9715C44BC"> MAAND. Elk bestand bevat gegevens voor een kalendermaand. De maanden worden genummerd 1 (Januari) door 12 (December). </li> 
       <li id="li_91831283616C48DA8C8086776D181751"> WEEK. Elk dossier bevat gegevens voor één week. Een week begint op maandag. De week die begint op een van de eerste zeven dagen van het jaar is week 1, en de voorafgaande (gedeeltelijke) week, indien van toepassing, is week 0. </li> 
       <li id="li_BDB7B4D779434B98935261B8B5C0AABB"> DAG. Elke dossiers bevat gegevens voor één kalenderdag. </li> 
       <li id="li_018F4133E03C42F29073FED1DB082ED5"> UUR. Elk dossier bevat gegevens voor één uur. </li> 
       <li id="li_EE8CF71BA12149F49D4B7F7108262CD0"> NIETS. Er wordt geen rotatie uitgevoerd. Alle gegevens worden geschreven aan het zelfde dossier (of een reeks dossiers zoals die door andere parametermontages wordt bepaald). Zie de parameter van het Formaat <span class="wintitle"></span> van het Dossier - noem in deze lijst. </li> 
      </ul> <p>De standaardperiode van de dossieromwenteling is DAG. </p> 
      <ul id="ul_0F3BC98275634F759E5022FF2C19715E"> 
       <li id="li_24DC4D144DA94ED0B7B50E8BB39DB8E3"> Plaats de dossieromwenteling aan GEEN slechts wanneer het werken op <span class="wintitle"> Off-line Wijze</span>. Zie de <a href="../../../../../home/c-dataset-const-proc/c-transf-func/c-config-files-transf/t-ins-transf-file/t-ins-transf-file.md#task-857fc535ccdb4c39b763179efa4b0f13"> Off-line de parameterbeschrijving van de Wijze</a> . </li> 
      </ul> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> Bestandsnaam formatteren </td> 
      <td colname="col2"> <p>Optioneel. Het formaat van het outputdossier - noem. </p> <p> Elke logboekingang kan in een dossier worden opgeslagen de waarvan naam van de begintijd van de omwentelingsperiode, en naar keuze, van waarden van gebieden in de rijen wordt afgeleid die het bevat. De gebieden in het dossier worden te gebruiken - de naam wordt ingebed aangezien de gebiedsnaam ontsnapt (die als %<i>veldnaam</i>% wordt uitgedrukt). </p> <p>Het dossier - noem componenten met betrekking tot de omwentelingsperiode worden ingebed in het formaatkoord gebruikend de volgende vluchtopeenvolgingen: 
      <ul id="ul_3C5C8C5DC9104070ABCFDD85F49BE596"> 
       <li id="li_B100AE13FEA84AB6A1138CF58440E29E"> %yyyy% (jaar met vier cijfers) </li> 
       <li id="li_0583970798494A1795B03866DC717FB9"> %yy% (jaar met twee cijfers) </li> 
       <li id="li_10AA96200F294364A5CE9DC3F22C789A"> %mm% (maand met twee cijfers, 01 - 12) </li> 
       <li id="li_E112E367F62147C49751D6894E47607C"> %ww% (tweecijferige week, 01 - 52) </li> 
       <li id="li_C4B30E38C05942BB8CAA92F3C9B98A3C"> %dd% (tweecijferige dag, 01-31) </li> 
       <li id="li_0318CA8C4DC441B48C16B29A615F3293"> %HH% (2-cijferig uur, 00 - 23) </li> 
      </ul> </p> <p> De standaardbestandsnaam is <span class="filepath"> %yyyy%%mm%%dd%-%x-masker%.txt</span> </p> 
      <ul id="ul_07AE3624E7D74632AD5E5F164048196F"> 
       <li id="li_BA5C2BFBA73D4AAD8D729B30FF812759"> De vluchtsequenties zijn case-sensitive. </li> 
       <li id="li_32CB9C98190D4B17B4DA84732CFB9E2F"> Wanneer de Periode van de Omwenteling van het Dossier aan GEEN wordt geplaatst, wordt een leeg koord vervangen voor elk van de vluchtopeenvolgingen, als heden. </li> 
       <li id="li_C64731961ED6402FB92210A42854BA72"> Een fout wordt geproduceerd als het Formaat <span class="wintitle"> van de Naam van het</span> Dossier niet in een uniek dossier resulteert - noem voor elke omwentelingsperiode (zie de parameter van de Periode van de Omwenteling van het Dossier in deze lijst). Bijvoorbeeld, wanneer het gebruiken van de de omwentelingsperiode van de DAG, moeten de %dd%, %mm%, en %yy% of %yyyy% vluchtopeenvolgingen in het patroon aanwezig zijn om gegevensverlies te vermijden. </li> 
       <li id="li_15CDA2ABE450418FA8D9C4BC581C4ADD"> Als u de de vluchtopeenvolgingen van de gebiedsnaam binnen het patroon gebruikt en het bepaalde gebied vele verschillende waarden heeft, worden vele outputdossiers geschreven voor elke omwentelingsperiode. Merk op dat dit scenario in slechte prestaties kan resulteren, zodat zou u deze eigenschap met voorzichtigheid moeten gebruiken. </li> 
       <li id="li_D0F75E4FFAFF47C4AA8A8D14A6E1C18A"> Alle berekeningen zijn in GMT. </li> 
      </ul> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> Uitvoeren bij omvergooien </td> 
      <td colname="col2"> <p>Optioneel. Wanneer elk dossier wordt voltooid, kan een extern (Vensters) bevel worden uitgevoerd. De bevellijn wordt afgeleid uit het definitieve dossier - noem door de volgende vluchtopeenvolgingen in deze parameter te substitueren: </p> 
      <ul id="ul_5E16832BDBEA4757A2C02DE4B019A122"> 
       <li id="li_6A74D069353E4FE781657BF492675220"> %dir%. Het folderdeel van het definitieve dossier - noem, met inbegrip van het slepen backslash. </li> 
       <li id="li_2CF7232553C348089B1395BBB0BBD6AE"> %bestand%. Het dossier - noem (exclusief de folder en de uitbreiding) van het definitieve dossier. </li> 
       <li id="li_901BAB90E5EA434F9EE37A60477F4591"> %ext%. De uitbreiding (met inbegrip van het leiden ".") van het definitieve dossier - noem. </li> 
       <li id="li_AD7269A67A0041438A6951FD1898D458"> %pad%. De volledige wegnaam van het dossier, gelijkwaardig aan %dir%%file%%ext%. </li> 
      </ul> <p> Door gebrek, is deze parameter leeg (geen bevel wordt uitgevoerd). </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> Geheugenlimiet </td> 
      <td colname="col2"> <p>Optioneel. De hoeveelheid geheugen in bytes die voor het als buffer optreden voor van de output van de exporteur worden gebruikt. De standaardwaarde is 10.000.000 bytes. </p> <p> <p>Opmerking:  Als u vele outputdossiers hebt die tezelfdertijd open zijn, kunt u deze waarde willen verhogen, maar u kunt de hoeveelheid geheugen verminderen beschikbaar voor gebruik door andere componenten van het systeem. Het verminderen van deze waarde, echter, kan het uitvoerproces vertragen. Voor hulp, contacteer Adobe. </p> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> Bestanden limiet openen </td> 
      <td colname="col2"> <p>Optioneel. Het maximumaantal dossiers dat tezelfdertijd voor output van de exporteur kan open zijn. Als dit aantal wordt overschreden, wordt een fout geregistreerd in het gebeurtenislogboek en de server van de gegevenswerkbank houdt op lopend. De standaardwaarde is 1000. </p> </td> 
      </tr> 
    </tbody> 
   </table>

1. Nadat u uw exporteur (en veranderingen in andere parameters) in het [!DNL Transform.cfg] dossier hebt bepaald, sla plaatselijk het dossier op en sla het in het aangewezen profiel op de de servermachine van de gegevenswerkbank op.
