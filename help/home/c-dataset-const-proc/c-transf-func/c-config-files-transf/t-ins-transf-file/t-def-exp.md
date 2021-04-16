---
description: Exporters geven de instructies voor het uitvoeren van de gebeurtenisgegevens.
title: Exporters definiëren
uuid: 565d4482-6c25-407c-bda7-0d116180902a
exl-id: 5de6266a-e959-414c-9512-5e9f4011881b
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '1120'
ht-degree: 1%

---

# Exporters definiëren{#defining-exporters}

Exporters geven de instructies voor het uitvoeren van de gebeurtenisgegevens.

De functionaliteit van de transformatie verstrekt drie soorten exporteurs voor het uitvoeren van [!DNL .vsl] dossiers, logboekdossiers, de dossiers van XML, en ODBC- gegevens als [!DNL .vsl] dossiers, tekstdossiers, of afgebakende tekstdossiers die door DataWarehouse ladingsroutines, controlebureaus, of andere doelstellingen kunnen worden gebruikt.

>[!NOTE]
>
>Een exportfunctie werkt alleen correct als de logbron voldoet aan de vereisten die worden beschreven in de sectie [Logbronnen](../../../../../home/c-dataset-const-proc/c-log-proc-config-file/c-log-sources.md#concept-6714c720fac044cbb9af003bf401b2ea) van [Logverwerkingsconfiguratiebestand](../../../../../home/c-dataset-const-proc/c-log-proc-config-file/c-abt-log-proc-config-file.md).

**Een exporteur definiëren**

1. Open [!DNL Transform.cfg] in gegevenswerkbank. Zie [Het bestand Insight Transform.cfg](../../../../../home/c-dataset-const-proc/c-transf-func/c-config-files-transf/t-ins-transf-file/t-ins-transf-file.md#task-857fc535ccdb4c39b763179efa4b0f13) bewerken.
1. Klik met de rechtermuisknop **[!UICONTROL Exporters]** en klik vervolgens op **[!UICONTROL Add New]**.
1. Selecteer een van de volgende opties:

   * **[!UICONTROL ExportTextFile]**
   * **[!UICONTROL ExportDelimitedTextFile]**
   * **[!UICONTROL ExportVSLFile]**

   >[!NOTE]
   >
   >Voor de optie [!DNL ExportVSLFile] worden alle uitgebreide velden in het invoerbestand en alle door de gebruiker gedefinieerde velden van het formulier cs(*header*) altijd naar het VSL uitvoerbestand geschreven. Als u een bestaand uitgebreid veld overschrijft, wordt de nieuwe waarde naar het uitvoerbestand geschreven, zelfs als het veld leeg is.

1. Bewerk de parameters Exporters in het configuratiebestand met de volgende tabel als richtlijn:

   <table id="table_35C380DB6E4F42448C149D5EC185213C"> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> Parameter </th> 
      <th colname="col2" class="entry"> Beschrijving </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> Gegevensindeling </td> 
      <td colname="col2"> <p>Alleen voor <span class="wintitle"> ExportTextFile</span>. De indeling van elke uitvoerregel, bestaande uit veldnaamescape-tekens (uitgedrukt als %<i>veldnaam</i>%) en andere gewenste vaste tekst. De notatie moet een regelscheidingsteken bevatten, doorgaans [CR] [LF]. </p> <p> Een letterlijk percentageteken (%) kan in het formaat worden ingebed koord door het karakter te ontsnappen zoals hier getoond: %% </p> <p> Een voorbeeld van een vermelding voor de parameter Gegevensindeling is <span class="filepath"> %x-timestring% %x-trackingid%[CR][LF]</span>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> Velden </td> 
      <td colname="col2">Alleen voor <span class="wintitle"> ExportDelimitedTextFile</span>. Namen van de velden die moeten worden uitgevoerd. </td> 
      </tr> 
      <tr> 
      <td colname="col1"> Scheidingsteken </td> 
      <td colname="col2"> <p>Optioneel. Alleen voor <span class="wintitle"> ExportDelimitedTextFile</span>. Teken dat wordt gebruikt om de velden in het uitvoerbestand van elkaar te scheiden. </p> <p> De software kan geen scheidingstekens ontsnappen die in de waarden van de gegevens zijn opgenomen. Als gevolg hiervan wordt het gebruik van komma's als scheidingstekens afgeraden door Adobe. </p> <p> Als u de sleutel van CTRL onderdrukt en binnen de parameter van Scheidingsteken met de rechtermuisknop klikt, <span class="wintitle"> Tussenvoegsel</span> verschijnt een menu. Dit menu bevat een lijst met speciale tekens die vaak als scheidingstekens worden gebruikt. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> Lijnscheidingsteken </td> 
      <td colname="col2">Optioneel. Alleen voor <span class="wintitle"> ExportDelimitedTextFile</span>. Het teken of de tekens waarmee regels in de uitvoerbestanden worden gescheiden. De standaardwaarde is [CR] [LF]. </td> 
      </tr> 
      <tr> 
      <td colname="col1"> Naam </td> 
      <td colname="col2"> <p>Optioneel. Identificatiecode voor de exporteur. Deze naam verschijnt in <span class="wintitle"> Gedetailleerde Status</span> interface. </p> <p> Voor informatie over <span class="wintitle"> Gedetailleerde Status</span> interface, zie <i>de Gids van de Gebruiker van de Data Workbench</i>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> Opmerkingen </td> 
      <td colname="col2"> Optioneel. Opmerkingen over de exportfunctie. </td> 
      </tr> 
      <tr> 
      <td colname="col1"> Uitvoerpad </td> 
      <td colname="col2"> <p>Pad waar uitvoerbestanden moeten worden opgeslagen. Het pad is relatief ten opzichte van de installatiemap van de gegevenswerkbankserver. </p> <p> <p>Opmerking: De gegevenswerkbankserver die uitvoergegevens opslaat verwerkt server nr. 0 in het bestand <span class="filepath"> profile.cfg</span>. </p> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> Rotatieperiode bestand </td> 
      <td colname="col2"> <p>Optioneel. De frequentie waarmee gegevens naar het uitvoerbestand worden geëxporteerd. Elk uitvoerbestand bevat gegevens die betrekking hebben op een specifieke periode die de rotatieperiode wordt genoemd. Alle tijdberekeningen zijn in GMT: Een dag begint om middernacht GMT en eindigt de volgende dag om middernacht GMT, zelfs als de gegevens die naar het dossier worden geschreven een gebied omvatten dat aan lokale tijd is omgezet. </p> <p> De beschikbare waarden zijn als volgt: </p> 
      <ul id="ul_64F56D093E2E4D07ACB7D7921F4E6FA1"> 
       <li id="li_E4985C7F56E443049AFF57B0270032D6"> JAAR. Elk bestand bevat gegevens voor één kalenderjaar. </li> 
       <li id="li_42E59BB7A5704C85A6079ED9715C44BC"> MAAND. Elk bestand bevat gegevens voor één kalendermaand. De maanden worden genummerd 1 (januari) tot en met 12 (december). </li> 
       <li id="li_91831283616C48DA8C8086776D181751"> WEEK. Elk bestand bevat gegevens voor een week. Een week begint op maandag. De week die begint op een van de eerste zeven dagen van het jaar is week 1 en de voorafgaande (gedeeltelijke) week, als die er is, is week 0. </li> 
       <li id="li_BDB7B4D779434B98935261B8B5C0AABB"> DAG. Elk bestand bevat gegevens voor één kalenderdag. </li> 
       <li id="li_018F4133E03C42F29073FED1DB082ED5"> UUR. Elk bestand bevat gegevens voor een uur. </li> 
       <li id="li_EE8CF71BA12149F49D4B7F7108262CD0"> GEEN. Er wordt geen rotatie uitgevoerd. Alle gegevens worden naar hetzelfde bestand geschreven (of een set bestanden zoals bepaald door andere parameterinstellingen). Zie de <span class="wintitle"> parameter van het Formaat van de Naam van het Dossier </span> in deze lijst. </li> 
      </ul> <p>De standaardperiode voor het roteren van bestanden is DAG. </p> 
      <ul id="ul_0F3BC98275634F759E5022FF2C19715E"> 
       <li id="li_24DC4D144DA94ED0B7B50E8BB39DB8E3"> Stel de rotatie van het bestand alleen in op NONE wanneer u werkt in <span class="wintitle"> Offlinemodus</span>. Zie de beschrijving van de parameter <a href="../../../../../home/c-dataset-const-proc/c-transf-func/c-config-files-transf/t-ins-transf-file/t-ins-transf-file.md#task-857fc535ccdb4c39b763179efa4b0f13"> Offlinemodus</a>. </li> 
      </ul> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> Bestandsnaamindeling </td> 
      <td colname="col2"> <p>Optioneel. De indeling van de naam van het uitvoerbestand. </p> <p> Elk logbestandvermelding kan worden opgeslagen in een bestand waarvan de naam wordt afgeleid van de begintijd van de rotatieperiode en eventueel van waarden van velden in de rijen die het bevat. De velden die in de bestandsnaam moeten worden gebruikt, worden ingesloten als veldnaamescape-tekens (uitgedrukt als %<i>veldnaam</i>%). </p> <p>De bestandsnaamcomponenten met betrekking tot de rotatieperiode worden in de indelingstekenreeks ingesloten met de volgende escape-reeksen: 
      <ul id="ul_3C5C8C5DC9104070ABCFDD85F49BE596"> 
       <li id="li_B100AE13FEA84AB6A1138CF58440E29E"> %yyyy% (jaar met vier cijfers) </li> 
       <li id="li_0583970798494A1795B03866DC717FB9"> %yy% (jaar van twee cijfers) </li> 
       <li id="li_10AA96200F294364A5CE9DC3F22C789A"> %mm% (maand met twee cijfers, 01 - 12) </li> 
       <li id="li_E112E367F62147C49751D6894E47607C"> %ww% (tweecijferige week, 01 - 52) </li> 
       <li id="li_C4B30E38C05942BB8CAA92F3C9B98A3C"> %dd% (dag van twee cijfers, 01 - 31) </li> 
       <li id="li_0318CA8C4DC441B48C16B29A615F3293"> %HH% (2-cijferig uur, 00 - 23) </li> 
      </ul> </p> <p> De standaardbestandsnaamindeling is <span class="filepath"> %yyyy%%dd%-%x-mask%.txt</span> </p> 
      <ul id="ul_07AE3624E7D74632AD5E5F164048196F"> 
       <li id="li_BA5C2BFBA73D4AAD8D729B30FF812759"> De escapereeksen zijn hoofdlettergevoelig. </li> 
       <li id="li_32CB9C98190D4B17B4DA84732CFB9E2F"> Wanneer de Periode van de Omwenteling van het Dossier aan NONE wordt geplaatst, wordt een lege koord vervangen voor elk van de escape opeenvolgingen, als heden. </li> 
       <li id="li_C64731961ED6402FB92210A42854BA72"> Er wordt een fout gegenereerd als <span class="wintitle"> File Name Format</span> niet resulteert in een unieke bestandsnaam voor elke rotatieperiode (zie de parameter File Rotation Period in deze tabel). Als u bijvoorbeeld de rotatieperiode DAG gebruikt, moeten de escape-reeksen %dd%, %mm% en %yy% of %yyyy% aanwezig zijn in het patroon om gegevensverlies te voorkomen. </li> 
       <li id="li_15CDA2ABE450418FA8D9C4BC581C4ADD"> Als u escapereeksen voor veldnamen gebruikt binnen het patroon en het opgegeven veld vele verschillende waarden heeft, worden veel uitvoerbestanden geschreven voor elke rotatieperiode. Merk op dat dit scenario in slechte prestaties kan resulteren, zodat zou u deze eigenschap met voorzichtigheid moeten gebruiken. </li> 
       <li id="li_D0F75E4FFAFF47C4AA8A8D14A6E1C18A"> Berekeningen worden altijd in GMT uitgevoerd. </li> 
      </ul> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> Uitvoeren bij rollover </td> 
      <td colname="col2"> <p>Optioneel. Wanneer elk bestand is voltooid, kan een externe opdracht (Windows) worden uitgevoerd. De opdrachtregel wordt afgeleid van de uiteindelijke bestandsnaam door de volgende escapereeksen in deze parameter te vervangen: </p> 
      <ul id="ul_5E16832BDBEA4757A2C02DE4B019A122"> 
       <li id="li_6A74D069353E4FE781657BF492675220"> %dir%. Het directorygedeelte van de uiteindelijke bestandsnaam, inclusief de achterliggende backslash. </li> 
       <li id="li_2CF7232553C348089B1395BBB0BBD6AE"> %file%. De bestandsnaam (exclusief de map en extensie) van het uiteindelijke bestand. </li> 
       <li id="li_901BAB90E5EA434F9EE37A60477F4591"> %ext%. De extensie (inclusief de regelafstand ".") van de uiteindelijke bestandsnaam. </li> 
       <li id="li_AD7269A67A0041438A6951FD1898D458"> %path%. De volledige padnaam van het bestand, gelijk aan %dir%%file%%ext%. </li> 
      </ul> <p> Deze parameter is standaard leeg (er wordt geen opdracht uitgevoerd). </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> Geheugenlimiet </td> 
      <td colname="col2"> <p>Optioneel. De hoeveelheid geheugen in bytes die wordt gebruikt voor het bufferen van de uitvoer van de exportfunctie. De standaardwaarde is 10.000.000 bytes. </p> <p> <p>Opmerking:  Als u veel uitvoerbestanden hebt die tegelijkertijd geopend zijn, kunt u deze waarde verhogen, maar u kunt de hoeveelheid geheugen die beschikbaar is voor gebruik door andere componenten van het systeem verminderen. Als u deze waarde verlaagt, kan dit het exportproces vertragen. Neem voor hulp contact op met Adobe. </p> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> Limiet voor geopende bestanden </td> 
      <td colname="col2"> <p>Optioneel. Het maximumaantal bestanden dat tegelijkertijd kan worden geopend voor uitvoer door de exportfunctie. Als dit aantal wordt overschreden, wordt een fout geregistreerd in het gebeurtenislogboek en de server van de gegevenswerkbank houdt op lopend. De standaardwaarde is 1000. </p> </td> 
      </tr> 
    </tbody> 
   </table>

1. Nadat u de exportfunctie hebt gedefinieerd (en wijzigingen hebt aangebracht in andere parameters) in het [!DNL Transform.cfg]-bestand, slaat u het bestand lokaal op en slaat u het op in het juiste profiel op de server op de werkbank.
