---
description: Stel de parameters in het bestand Insight.cfg in om de configuratie-instellingen voor de netwerkverbinding en de Data Workbench op te geven.
title: Configuratieparameters
uuid: 6e1248c1-3eae-44a3-8b19-f595d79e8d0d
exl-id: c92fc79f-452d-4839-840a-a3ea9e8754c4
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '1519'
ht-degree: 1%

---

# Configuratieparameters{#configuration-parameters}

Stel de parameters in het bestand Insight.cfg in om de configuratie-instellingen voor de netwerkverbinding en de Data Workbench op te geven.

Het volgende voorbeeld bevat standaard alleen de parameters die in het [!DNL Insight.cfg]-bestand zijn opgenomen.

**Nieuwe layoutweergave**

![](assets/config_tree_new_layout.png)

**Oorspronkelijke layoutweergave**

![](assets/cfg_Workstation_AddServer.png)

Sommige parameters die beschikbaar zijn in het nieuwe [!DNL Insight.cfg]-bestand zijn mogelijk niet beschikbaar in uw versie van het [!DNL Insight.cfg]-bestand. Als één van deze parameters nodig is, moet u het aan [!DNL Insight.cfg] dossier toevoegen gebruikend [!DNL Add Custom Key], door op een parameter met de rechtermuisknop te klikken, dan specificerend de naam en het type. U kunt ook parameters toevoegen door het [!DNL .cfg]-bestand te openen (in de installatiemap van de Data Workbench) met een teksteditor.

Hieronder ziet u een voorbeeld van alle parameters die beschikbaar zijn voor het bestand [!DNL Insight.cfg] dat u kunt gebruiken als model voor het toevoegen van parameteritems:

```
Licensing = serverInfo:
  Proxy Address = string: 
  Proxy Port = int: 8080
  Proxy User Name = string: 
  Proxy Password = string: 
Servers = vector: 1 items
  0 = serverInfo: 
    Address = string: VS02
    Name = string: Insight Server
    Port = int: 443
    Proxy Address = string: 
    Proxy Password = string: 
    Proxy Port = int: 8080
    Proxy User Name = string: 
    SSL Client Certificate = string: Named User.pem
    SSL Server Common Name = string: VS02
    Use Address File = bool: false
    Use SSL = bool: true
Color Set = int: 0
Default to Online = bool: false
Fonts = vector: 0 items
Gamma = float: 1.6
Maximum Sample Size (MB) = double: 0
Network Location = string: 
Unhide All = bool: false
Unlock = bool: false
Update Software = bool: true
User Folder = string: User\\
Toolbar Icons = bool: false
```

De volgende tabel bevat een beschrijving van de beschikbare [!DNL Insight.cfg]-bestandsparameters in alfabetische volgorde.

<table id="table_4465713A08B649E280A3B4840E829518"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Parameter </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Adres </p> </td> 
   <td colname="col2"> <p>De hostnaam of het numerieke IP-adres van uw Data Workbench-servercomputer. </p> <p>Voorbeeld: <span class="filepath"> vsServer.mijnbedrijf.com of 192.168.1.90</span> </p> <p>Als <span class="wintitle"> Adres </span> niet wordt gespecificeerd, <span class="keyword"> gebruikt de cliënt </span> de gemeenschappelijke naam die in de SSL parameter van de Naam van de Server wordt gespecificeerd Common wanneer het Dossier van het Adres van het Gebruik aan vals wordt geplaatst. </p> <p> <p>Opmerking: Als de parameter van het Dossier van het Adres van het Gebruik aan waar wordt geplaatst, kan de tekst ingegaan in de parameter van het Adres worden verwijderd nadat het eerste profiel op <span class="keyword"> cliënt </span> wordt geopend. Dan bepaalt het plaatsen voor de Parameter van de Plaats van het Netwerk welke adressen van het dossier van het Adres voor de cluster voor het verbinden met de master server worden gebruikt. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Kleurenset </p> </td> 
   <td colname="col2"> <p>Hiermee geeft u de achtergrondkleur op van de <span class="keyword">-clienttoepassing</span>. De opties zijn als volgt: </p> <p>0 = zwart </p> <p>1 = wit </p> <p>2 = monochroom </p> <p>De standaardwaarde is 0, zwart. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Standaardniveau online </p> </td> 
   <td colname="col2"> <p>Optioneel. Hiermee kunt u uw instantie van Data Workbench standaard als streaming, offline of online laten werken wanneer deze wordt geopend. De opties zijn Streaming, Online of Offline. De standaardconfiguratie voor Data Workbench moet Offline werken. </p> <p> <p>Opmerking: Voordat u besluit om standaard online te werken, moet u de voordelen en gevolgen afwegen die worden beschreven in <a href="../../home/c-get-started/c-off-on.md#concept-cef8758ede044b18b3558376c5eb9f54"> Offline werken en Online</a>. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Lettertypen </p> </td> 
   <td colname="col2"> <p>Optioneel. Vector die een lijst maakt van de doopvonten die <span class="keyword"> de cliënt </span> zou moeten gebruiken om op UTF8-Gebaseerde unicode speciale karakters terug te geven. Het aantal lettertypen in de lijst is onbeperkt. </p> <p>Het eerste font moet altijd Lucida Sans Console zijn. Als deze parameter niet inbegrepen in <span class="filepath"> Insight.cfg</span> dossier is, gebruikt de Data Workbench slechts de console van Lucida Sans om tekst te tonen. </p> <p> Data Workbench gebruikt het eerste lettertype in de lijst om alle tekens te renderen totdat het een teken tegenkomt dat het niet kan renderen. Het tweede lettertype in de lijst wordt gebruikt om dat teken te renderen. Als dat lettertype het teken niet rendert, gebruikt Data Workbench het derde lettertype in de lijst om dat teken weer te geven, enzovoort, totdat het einde van de lettertypenlijst is bereikt. Als het juiste lettertype niet in de vector wordt vermeld, geeft Data Workbench de hexadecimale waarde voor het teken weer. </p> <p> <p>Opmerking:  Wijzig deze parameter niet terwijl de Data Workbench wordt uitgevoerd. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Gamma </p> </td> 
   <td colname="col2"> Gamma-instelling voor weergave van Data Workbench. De standaardwaarde is 1,6. Adobe raadt u niet aan deze waarde te wijzigen. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Licentie </p> </td> 
   <td colname="col2"> <p>Optioneel. U hoeft de parameters in de licentievector alleen te wijzigen als u via een proxyserver contact opneemt met de licentieserver van Adobe. </p> <p>Sectie-id voor parameters waarmee uw <span class="keyword">-client</span> via een proxyserver contact kan opnemen met de Adobe-licentieserver. Vouw het knooppunt Licensing uit en vul de volgende parameters in. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Proxyadres </p> </td> 
   <td colname="col2"> <p>Optioneel. Het adres van de proxyserver die <span class="keyword"> client</span> moet gebruiken om toegang te krijgen tot de Adobe-licentieserver. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Proxypoort </p> </td> 
   <td colname="col2"> <p>Optioneel. De poort van de proxyserver. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Gebruikersnaam proxy </p> </td> 
   <td colname="col2"> <p>Optioneel. De gebruikersnaam voor de proxyserver. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Proxywachtwoord </p> </td> 
   <td colname="col2"> <p>Optioneel. Het wachtwoord dat aan de Naam van de Gebruiker van de Volmacht wordt geassocieerd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Maximale monstergrootte (MB) </p> </td> 
   <td colname="col2"> <p>Geeft de maximale grootte aan die is toegestaan in de gegevenscache die wordt gebruikt door <span class="keyword"> de client</span> die op één computer wordt uitgevoerd. </p> <p>Terwijl de parameter van de Bytes van de Steekproef in <span class="filepath"> Server.cfg</span> dossier de grootte van het gegevensgeheime voorgeheugen voor alle <span class="keyword"> cliënten </span> het verbinden met een server van de Data Workbench (250e6 bytes door gebrek) specificeert, laat de Maximum parameter van de Grootte van de Steekproef u toe om de grootte van het gegevensgeheime voorgeheugen voor een bepaalde computer verder te beperken. Dit is handig wanneer de client is geïnstalleerd op een computer met beperkte opslag- of verwerkingscapaciteit. </p> <p> <p>Opmerking: Deze parameter beperkt de grootte van een lokaal gegevensvoorbeeld dat lokaal door het cliëntprogramma wordt gevraagd. Het bestand <span class="filepath"> cache.db</span> bevat daarentegen gegevens voor elk profiel waarmee de client verbinding maakt, plus de elementnamen en de afmetingen. Deze elementnamen en -afmetingen in de bestanden <span class="filepath"> cache.db</span> zijn vereist om lokale query's uit te voeren. Daarom is er geen andere manier om de grootte ervan te beperken dan het aantal elementen in de gegevensset te verminderen. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Naam </p> </td> 
   <td colname="col2">Optioneel. De naam die <span class="keyword"> de client</span> gebruikt om de <span class="keyword"> server</span> te identificeren. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Netwerklocatie </p> </td> 
   <td colname="col2"> <p>Optioneel. De netwerklocatie die <span class="keyword"> client</span> gebruikt om de algemene naam van de server van de Data Workbench op te lossen op een IP-adres. De beschikbare netwerklocaties worden gedefinieerd in het adresbestand op de server. Voor meer informatie, zie <i>de Gids van de Installatie en van het Beleid van de Producten van de Server</i>. </p> <p>Als u geen netwerklocatie opgeeft, wordt <span class="keyword"> client</span> omgezet in algemene namen met de standaardnetwerklocatie "Insight". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Poort </p> </td> 
   <td colname="col2"> <p>De poort waarnaar <span class="keyword"> de client</span> aanvragen verzendt. Dit havenaantal moet de haven aanpassen waarop de server van de Data Workbench op verzoeken luistert. Dit is gewoonlijk 443 voor veilige verbindingen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Proxyadres </p> </td> 
   <td colname="col2"> <p>Als een volmachtsserver wordt vereist om met uw de servercomputers van de Data Workbench te verbinden, moet u minstens deze parameter en de parameter van de Haven van de Volmacht voltooien. U kunt naar keuze de parameters van de Naam van de Gebruiker van de Volmacht en van het Wachtwoord van de Gebruiker van de Volmacht voltooien. </p> <p>Het adres van de proxyserver die <span class="keyword"> de client</span> moet gebruiken om toegang te krijgen tot de Data Workbench-server. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Proxywachtwoord </p> </td> 
   <td colname="col2"> <p>Optioneel. Het wachtwoord voor de proxyserver. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Proxypoort </p> </td> 
   <td colname="col2"> <p>De poort van de proxyserver. De standaardwaarde is 8080. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Gebruikersnaam proxy </p> </td> 
   <td colname="col2"> <p>Optioneel. De gebruikersnaam voor de proxyserver. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Zoeken </p> </td> 
   <td colname="col2"> <p>In <span class="filepath"> Insight.cfg</span> (of om het even welk <span class="filepath"> .cfg</span> dossier), kunt u op zeer belangrijke naam, zeer belangrijk type, of waarde zoeken om van een ingang snel de plaats te bepalen, om de behoefte te verwijderen om door uitgebreide, grote dossiers voor genestelde informatie te scrollen. U kunt afmetingsnamen, servernamen, enzovoort opzoeken. </p> <p>Typ een zoekterm in dit veld om de gegevens te zoeken. Afhankelijk van het succes van een overeenkomst, verandert de kleur van het gebied. Overeenkomsten worden gemarkeerd weergegeven en niet-overeenkomende items worden grijs weergegeven. Als er geen overeenkomsten zijn, wordt de achtergrond van het zoekveld rood. Wanneer u binnengaan drukt, breidt de config boom elke plaats uit waar er een gelijke is en doet ineenstorten waar er geen gelijke is. </p> <p>U kunt reguliere expressies ook gebruiken in het veld <span class="wintitle"> Zoeken</span>. U kunt bijvoorbeeld het volgende gebruiken: <span class="filepath"> *zip.*</span> voor elke vermelding die het woord "zip" bevat. </p> <p>Druk op <span class="uicontrol"> Escape</span> om een zoekopdracht te wissen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Servers </p> </td> 
   <td colname="col2"> <p>Vectorkop voor <span class="keyword"> client</span> naar <span class="keyword"> server</span> verbindingen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>SSL-clientcertificaat </p> </td> 
   <td colname="col2"> <p>Optioneel, tenzij u meer dan één certificaat hebt. De naam van het bestand dat het digitale certificaat voor deze kopie van de Data Workbench bevat. Dit is het bestand dat u hebt gedownload bij het downloaden en installeren van het digitale certificaat. </p> <p>Voorbeeld: <span class="filepath"> Samantha Smith.pem</span> </p> <p>Als u deze parameter leeg laat, <span class="keyword"> gebruikt de client</span> welk certificaat er ook aanwezig is. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Algemene naam SSL-server </p> </td> 
   <td colname="col2"> <p>De algemene naam van de server van de Data Workbench (zoals toegewezen op zijn digitaal certificaat). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Werkbalkpictogrammen </p> </td> 
   <td colname="col2"> <p>Met Onwaar worden de pictogrammen in de gebruikersinterface van het werkstation uitgeschakeld en wordt tekst in de werkbalk weergegeven. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Adresbestand gebruiken </p> </td> 
   <td colname="col2"> <p>Geeft aan of instellingen in het adresbestand de parameterinstelling Adres overschrijven. De opties zijn waar of onwaar. Indien ingesteld op true, overschrijven de instellingen in het adresbestand, indien aanwezig, de instelling voor de parameter Address. De standaardwaarde is true. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>SSL gebruiken </p> </td> 
   <td colname="col2">Geeft aan of SSL wordt gebruikt voor beveiligde communicatie tussen de server van de Data Workbench en <span class="keyword"> de client</span>. De opties zijn waar of onwaar. De standaardwaarde is true. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Alles zichtbaar maken </p> </td> 
   <td colname="col2"> <p>Optioneel. Hiermee kunt u tijdelijk alle verborgen metriek, afmetingen en filters zichtbaar maken met een van de volgende functies: 
     <ul id="ul_B40E28D9FDC0418BBFA9B0A37F4F6913"> 
      <li id="li_E51BAC99AAE949E5886F19557366453A">[Exclusief] het plaatsen in <span class="filepath"> orde.txt</span> dossiers </li> 
      <li id="li_E3D8222BC55D4CEB90BCCAE606711306">Optie verbergen in bestanden <span class="filepath"> order.txt</span> </li> 
      <li id="li_2ADE4EFC1F964D0A90B40CFB3D2766E8">Toon parameter in <span class="filepath"> .metrisch</span>, <span class="filepath"> .dim</span>, en <span class="filepath"> .filter</span> dossiers. </li> 
      <li id="li_BBCD248A8F33440092B52E407E300FCC">Verborgen parameter in het <span class="filepath"> bestand Transformation.cfg</span>. </li> 
     </ul> </p> <p>Zie <a href="../../home/c-get-started/c-intf-anlys-ftrs/c-ctm-menus/t-cstm-menus-ordr-files.md#task-a391800a8dd444deb3e1516d5189f999"> Een menu-item verbergen</a> voor meer informatie over deze methoden. </p> <p>De opties zijn waar of onwaar. De standaardinstelling is false. Wijzig deze parameter in true om verborgen metriek, afmetingen en filters tijdelijk weer te geven. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Ontgrendelen </p> </td> 
   <td colname="col2"> <p>Optioneel. Hiermee geeft u aan of vergrendelde werkruimten mogen worden ontgrendeld. De opties zijn waar en onwaar. Met True kunt u elke vergrendelde werkruimte ontgrendelen, maar met false. De standaardwaarde is false. Zie <a href="../../home/c-get-started/c-work-worksp/c-unlock-wksp.md#concept-18ada952aecf45c79a806b31b294023e"> Een werkruimte ontgrendelen</a> voor meer informatie over vergrendelde werkruimten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Software bijwerken </p> </td> 
   <td colname="col2"> <p>Optioneel. Geeft aan of dit <span class="keyword"> de </span>clientsoftware mag worden bijgewerkt door de Data Workbench-server. De opties zijn waar of onwaar. De standaardwaarde is true. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Gebruikersmap </p> </td> 
   <td colname="col2"> <p>Optioneel. Hier geeft u de naam en locatie op van de map die de lokale kopieën bevat van werkruimten, maateenheden, afmetingen of configuratiebestanden voor elk profiel. De standaardinstelling is Gebruiker\\. Hiermee wordt de map Gebruiker in de installatiemap van de Data Workbench opgegeven. </p> <p>Het is handig deze instelling te wijzigen wanneer twee gebruikers dezelfde computer delen. Als u beide gebruikers wilt plaatsen, kunt u een gedeelde map opgeven waartoe beide gebruikers toegang hebben. </p> </td> 
  </tr> 
 </tbody> 
</table>
