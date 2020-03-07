---
description: Plaats de parameters in het dossier Insight.cfg om uw de configuratiemontages van de netwerkverbinding en van de Werkbank van Gegevens te specificeren.
solution: Analytics
title: Configuratieparameters
topic: Data workbench
uuid: 6e1248c1-3eae-44a3-8b19-f595d79e8d0d
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Configuratieparameters{#configuration-parameters}

Plaats de parameters in het dossier Insight.cfg om uw de configuratiemontages van de netwerkverbinding en van de Werkbank van Gegevens te specificeren.

Het volgende voorbeeld bevat slechts de parameters inbegrepen in het [!DNL Insight.cfg] dossier door gebrek.

**Nieuwe layoutweergave**

![](assets/config_tree_new_layout.png)

**Originele layoutweergave**

![](assets/cfg_Workstation_AddServer.png)

Sommige parameters beschikbaar in het nieuwe [!DNL Insight.cfg] dossier kunnen niet beschikbaar in uw versie van het [!DNL Insight.cfg] dossier zijn. Als één van deze parameters nodig is, moet u het aan het [!DNL Insight.cfg] dossier toevoegen gebruikend [!DNL Add Custom Key], door op een parameter met de rechtermuisknop te klikken, dan specificerend de naam en het type. U kunt parameters ook toevoegen door het [!DNL .cfg] dossier (dat in de de installatiefolder van de Werkbank van Gegevens wordt gevestigd) te openen gebruikend een tekstredacteur.

Na is een voorbeeld van alle parameters beschikbaar voor het [!DNL Insight.cfg] dossier dat u als model kunt gebruiken om parameteringangen toe te voegen:

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

De volgende lijst verstrekt beschrijvingen van de beschikbare [!DNL Insight.cfg] dossierparameters in alfabetische orde.

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
   <td colname="col2"> <p>De gastheernaam of het numerieke IP adres van uw de servercomputer van de Werkbank van Gegevens. </p> <p>Voorbeeld: <span class="filepath"> vs. Server.mycompany.com of 192.168.1.90</span> </p> <p>Als het <span class="wintitle"> Adres</span> niet wordt gespecificeerd, gebruikt <span class="keyword"> de cliënt</span> de gemeenschappelijke naam die in de SSL Server wordt gespecificeerd gemeenschappelijke parameter van de Naam wanneer het Dossier van het Adres van het Gebruik aan vals wordt geplaatst. </p> <p> <p>Opmerking: Als de parameter van het Dossier van het Adres van het Gebruik aan waar wordt geplaatst, kan de tekst ingegaan in de parameter van het Adres worden verwijderd nadat het eerste profiel op <span class="keyword"> de cliënt</span>wordt geopend. Dan bepaalt het plaatsen voor de Parameter van de Plaats van het Netwerk welke adressen van het dossier van het Adres voor de cluster voor het verbinden met de hoofdserver worden gebruikt. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Kleurenreeks </p> </td> 
   <td colname="col2"> <p>Specificeert de achtergrondkleur van uw <span class="keyword"> cliënttoepassing</span>. De opties zijn als volgt: </p> <p>0 = zwart </p> <p>1 = wit </p> <p>2 = monochroom </p> <p>De standaardwaarde is 0, zwart. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Standaard online niveau </p> </td> 
   <td colname="col2"> <p>Optioneel. Laat u toe om uw geval van het werk van de Werkbank van Gegevens door gebrek te maken zoals het stromen, offline of online telkens als het opent. De opties zijn Streaming, Online, of Offline. De standaardconfiguratie voor de Werkbank van Gegevens moet Offline werken. </p> <p> <p>Opmerking: Alvorens te besluiten om online door gebrek te werken, zorg ervoor om de voordelen en de gevolgen te wegen die in het Werk Offline en Online <a href="../../home/c-get-started/c-off-on.md#concept-cef8758ede044b18b3558376c5eb9f54"></a>worden geschetst. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Lettertypen </p> </td> 
   <td colname="col2"> <p>Optioneel. Vector die van de doopvonten een lijst maakt die <span class="keyword"> de cliënt</span> zou moeten gebruiken om op UTF8-Gebaseerde unicode speciale karakters terug te geven. Het aantal doopvonten in de lijst is onbeperkt. </p> <p>De eerste doopvont zou altijd de Console van Lucida Sans moeten zijn. Als deze parameter niet inbegrepen in het <span class="filepath"> Insight.cfg</span> - dossier is, gebruikt de Werkbank van Gegevens slechts de console van Lucida Sans om tekst te tonen. </p> <p> De Werkbank van gegevens gebruikt de eerste doopvont in de lijst om alle karakters terug te geven tot het een karakter ontmoet dat het niet kan teruggeven. Het gebruikt de tweede doopvont in de lijst om dat karakter terug te geven. Als die doopvont niet het karakter teruggeeft, gebruikt de Werkbank van Gegevens de derde doopvont in de lijst om dat karakter terug te geven, etc., tot het het eind van de doopvontlijst bereikt. Als de correcte doopvont niet vermeld in de vector is, toont de Werkbank van Gegevens de hexadecimale waarde voor het karakter. </p> <p> <p>Opmerking:  Verander deze parameter niet terwijl de Werkbank van Gegevens loopt. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Gamma </p> </td> 
   <td colname="col2"> Gammainstelling voor het beeldscherm van de Data Workbench. De standaardwaarde is 1.6. Adobe adviseert niet veranderend deze waarde. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Licenties </p> </td> 
   <td colname="col2"> <p>Optioneel. U moet de parameters in de het Verlenen van vergunningen vector wijzigen slechts als u de vergunningsserver van Adobe door een volmachtsserver contacteert. </p> <p>Het herkenningsteken van de sectie voor parameters die uw <span class="keyword"> cliënt</span> toelaten om de Server van de Vergunning van Adobe door een volmachtsserver te contacteren. Breid de knoop van het Verlenen van vergunningen uit en voltooi de volgende parameters. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Proxyadres </p> </td> 
   <td colname="col2"> <p>Optioneel. Het adres van de volmachtsserver die de <span class="keyword"> cliënt</span> moet gebruiken om tot de Server van de Vergunning van Adobe toegang te hebben. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Proxypoort </p> </td> 
   <td colname="col2"> <p>Optioneel. De haven van de volmachtsserver. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Gebruikersnaam proxy </p> </td> 
   <td colname="col2"> <p>Optioneel. De gebruikersnaam voor de volmachtsserver. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Wachtwoord voor proxy </p> </td> 
   <td colname="col2"> <p>Optioneel. Het wachtwoord verbonden aan de Naam van de Gebruiker van de Volmacht. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Maximale steekproefgrootte (MB) </p> </td> 
   <td colname="col2"> <p>Specificeert de maximumgrootte toegestaan in het gegevensgeheime voorgeheugen dat door <span class="keyword"> de cliënt</span> wordt gebruikt die op één enkele computer loopt. </p> <p>Terwijl de parameter van de Bytes van de Steekproef in het <span class="filepath"> Server.cfg</span> - dossier de grootte van het gegevensgeheime voorgeheugen voor alle cliënten <span class="keyword"></span> specificeert die met een server van de Werkbank van Gegevens verbinden (250e6 bytes door gebrek), laat de Maximum parameter van de Grootte van de Steekproef u toe om de grootte van het gegevensgeheime voorgeheugen voor een bepaalde computer verder te beperken. Dit is nuttig wanneer de cliënt op een computer met beperkte opslag of gegevensverwerkingsmacht wordt geïnstalleerd. </p> <p> <p>Opmerking: Deze parameter beperkt de grootte van een lokale gegevenssteekproef die plaatselijk door het cliëntprogramma wordt gevraagd. In tegenstelling, bevat het <span class="filepath"> cache.db</span> - dossier gegevens voor elk profiel de cliënt met verbindt, plus de elementennamen en hun afmetingen. Deze elementennamen en afmetingen in de <span class="filepath"> cache.db</span> - dossiers worden vereist om lokale vragen in werking te stellen. Bijgevolg is er geen andere manier om de omvang ervan te beperken dan het verminderen van het aantal elementen in de gegevensverzameling. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Naam </p> </td> 
   <td colname="col2">Optioneel. De naam die <span class="keyword"> de cliënt</span> gebruikt om de <span class="keyword"> server</span>te identificeren. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Netwerklocatie </p> </td> 
   <td colname="col2"> <p>Optioneel. De netwerkplaats die de <span class="keyword"> cliënt</span> gebruikt om de server van de Werkbank van Gegevens gemeenschappelijke naam aan een IP adres op te lossen. De beschikbare netwerkplaatsen worden bepaald in het adresdossier op de server. Voor meer informatie, zie de Gids <i>van de Installatie en van het Beleid van de Producten van de</i>Server. </p> <p>Als u geen netwerkplaats specificeert, lost de <span class="keyword"> cliënt</span> gemeenschappelijke namen op gebruikend de standaardnetwerkplaats, "Inzicht." </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Poort </p> </td> 
   <td colname="col2"> <p>De haven waaraan <span class="keyword"> de cliënt</span> verzoeken verzendt. Dit havenaantal moet de haven aanpassen waarop de server van de Werkbank van Gegevens op verzoeken luistert. Dit is gewoonlijk 443 voor veilige verbindingen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Proxyadres </p> </td> 
   <td colname="col2"> <p>Als een volmachtsserver wordt vereist om met uw de servercomputers van de Werkbank van Gegevens te verbinden, moet u minstens deze parameter en de parameter van de Haven van de Volmacht voltooien. U kunt de de Naam van de Gebruiker van de Volmacht en parameters van het Wachtwoord van de Gebruiker van de Volmacht naar keuze voltooien. </p> <p>Het adres van de volmachtsserver die <span class="keyword"> de cliënt</span> moet gebruiken om tot de server van de Werkbank van Gegevens toegang te hebben. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Wachtwoord voor proxy </p> </td> 
   <td colname="col2"> <p>Optioneel. Het wachtwoord aan de volmachtsserver. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Proxypoort </p> </td> 
   <td colname="col2"> <p>De haven van de volmachtsserver. De standaardwaarde is 8080. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Gebruikersnaam proxy </p> </td> 
   <td colname="col2"> <p>Optioneel. De gebruikersnaam voor de volmachtsserver. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Zoeken </p> </td> 
   <td colname="col2"> <p>In <span class="filepath"> Insight.cfg</span> (of om het even welk <span class="filepath"> .cfg</span> dossier), kunt u door zeer belangrijke naam, zeer belangrijk type, of waarde zoeken om van een ingang snel de plaats te bepalen, om de behoefte te verwijderen om door uitgebreide, grote dossiers voor genestelde informatie te scrollen. U kunt van afmetingsnamen, servernamen, etc. de plaats bepalen. </p> <p>Typ een onderzoeksuitdrukking in dit gebied om van de gegevens de plaats te bepalen. Afhankelijk van het succes van een gelijke, verandert de kleur van het gebied. De gelijken worden getoond benadrukte en de niet-gelijken worden verduisterd. Als er geen gelijken zijn, wordt de achtergrond van het onderzoeksgebied rood. Wanneer u drukt ga binnen, breidt de config boom elke plaats uit waar er een gelijke is en doet ineenstorten waar er geen gelijke is. </p> <p>U kunt regelmatige uitdrukkingen op het gebied van het <span class="wintitle"> Onderzoek</span> ook gebruiken. Bijvoorbeeld, kunt u gebruiken re: * <span class="filepath"> *zip.*</span> voor elke rubriek met het woord "zip". </p> <p>Om een onderzoek te ontruimen, druk <span class="uicontrol"> Vlucht</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Servers </p> </td> 
   <td colname="col2"> <p>Vector rubriek voor <span class="keyword"> cliënt</span> aan <span class="keyword"> serververbindingen</span> . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>SSL-clientcertificaat </p> </td> 
   <td colname="col2"> <p>Facultatief tenzij u meer dan één certificaat hebt. De naam van het dossier dat het digitale certificaat voor dit exemplaar van de Werkbank van Gegevens bevat. Dit is het dossier dat u in het Downloaden van en het Installeren van het Digitale Certificaat downloadde. </p> <p>Voorbeeld: <span class="filepath"> Samantha Smith.pem</span> </p> <p>Als u deze parameterspatie verlaat, gebruikt <span class="keyword"> de cliënt</span> welk certificaat aanwezig is. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Algemene naam van SSL-server </p> </td> 
   <td colname="col2"> <p>De gemeenschappelijke naam van de server van de Werkbank van Gegevens (zoals die op zijn digitaal certificaat wordt toegewezen). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Werkbalkpictogrammen </p> </td> 
   <td colname="col2"> <p>De valse draaien van de pictogrammen in het werkstationgebruikersinterface en vertoningentekst in de toolbar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Adresbestand gebruiken </p> </td> 
   <td colname="col2"> <p>Specificeert of om het even welke montages in het adresdossier de parameter die van het Adres met voeten treden plaatsen. De opties zijn waar of vals. Als de reeks aan waar, de montages in het adresdossier, als heden, de parameter die van het Adres met voeten treedt plaatsen plaatst. De standaardwaarde is waar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>SSL gebruiken </p> </td> 
   <td colname="col2">Specificeert of SSL voor veilige communicatie tussen de server van de Werkbank van Gegevens en <span class="keyword"> de cliënt</span>wordt gebruikt. De opties zijn waar of vals. De standaardwaarde is waar. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Alles verwijderen </p> </td> 
   <td colname="col2"> <p>Optioneel. Laat u toe om alle metriek, afmetingen, en filters tijdelijk los te maken die gebruikend om het even welke volgende functionaliteit verborgen zijn geweest: 
     <ul id="ul_B40E28D9FDC0418BBFA9B0A37F4F6913"> 
      <li id="li_E51BAC99AAE949E5886F19557366453A">[Exclusief] instelling in <span class="filepath"> order.txt</span> -bestanden </li> 
      <li id="li_E3D8222BC55D4CEB90BCCAE606711306">Optie verbergen in <span class="filepath"> order.txt</span> -bestanden </li> 
      <li id="li_2ADE4EFC1F964D0A90B40CFB3D2766E8">Toon parameter in <span class="filepath"> .metric</span>, <span class="filepath"> .dim</span>, en. <span class="filepath"> .filter</span> dossiers. </li> 
      <li id="li_BBCD248A8F33440092B52E407E300FCC">Verborgen parameter in het <span class="filepath"> Transformation.cfg</span> - dossier. </li> 
     </ul> </p> <p>Voor meer informatie over deze methodes, zie <a href="../../home/c-get-started/c-intf-anlys-ftrs/c-ctm-menus/t-cstm-menus-ordr-files.md#task-a391800a8dd444deb3e1516d5189f999"> Huid een menupunt</a>. </p> <p>De opties zijn waar of vals. Standaard het plaatsen is vals. Verander deze parameter in waar om verborgen metriek, afmetingen, en filters tijdelijk los te maken. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Ontgrendelen </p> </td> 
   <td colname="col2"> <p>Optioneel. Specificeert of u wordt toegestaan om gesloten werkruimten te openen. De opties zijn waar en vals. Waar laat u toe om het even welke gesloten werkruimte te openen, terwijl vals niet. De standaardwaarde is vals. Voor meer informatie over gesloten werkruimten, zie het <a href="../../home/c-get-started/c-work-worksp/c-unlock-wksp.md#concept-18ada952aecf45c79a806b31b294023e"> Ontgrendelen van een Werkruimte</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Software bijwerken </p> </td> 
   <td colname="col2"> <p>Optioneel. Specificeert of om dit toe te staan <span class="keyword"> de </span>cliëntsoftware om door de server van de Werkbank van Gegevens worden bijgewerkt. De opties zijn waar of vals. De standaardwaarde is waar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Gebruikersmap </p> </td> 
   <td colname="col2"> <p>Optioneel. Specificeert de naam en de plaats van de omslag die de lokale exemplaren van om het even welke werkruimten, metriek, afmetingen, of configuratiedossiers voor elk profiel bevat. De standaardinstelling is Gebruiker\\\, die de omslag van de Gebruiker binnen de de installatiefolder van de Werkbank van Gegevens specificeert. </p> <p>Het veranderen van dit het plaatsen is nuttig wanneer twee gebruikers de zelfde computer delen. Om beide gebruikers aan te passen, kunt u een gedeelde omslag specificeren waartoe beide gebruikers toegang hebben. </p> </td> 
  </tr> 
 </tbody> 
</table>

