---
description: Informatie over de facultatieve het dossierparameters van de Sensor txlogd.conf.
solution: Insight
title: Optionele parameters
uuid: 8515a571-93ce-49cd-9ded-c9273259d0ee
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Optionele parameters{#optional-parameters}

Informatie over de facultatieve het dossierparameters van de Sensor txlogd.conf.

<table id="table_5FF491A7A6C24E43A06A5C344BF05430"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Parameter </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> AddressFilter </td> 
   <td colname="col2"> <p>Laat u toe om gespecificeerde IP adressen te filtreren. </p> <p>Wanneer u een bepaald adres filtert, wordt een "pakket"niet geregistreerd. Deze eigenschap elimineert interne of gecontroleerde agenten vóór logboekverwerking, daardoor verhogend de snelheid van logboekverwerking en verminderend gegevensopslagvereisten. U kunt vervangingen gebruiken wanneer het specificeren van adressen. </p> <p>Voorbeeld: <span class="filepath"> Adresfilter 10.0.000</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>ContentFilterInclusief </p> <p>ContentFilterExclude </p> </td> 
   <td colname="col2"> <p>Specificeer of om bepaalde soorten inhoud van registreren te omvatten of uit te sluiten. </p> <p>De parameterwaarden worden prefix-aangepast tegen het inhoudstype van het antwoord. </p> <p>Bijvoorbeeld, "beeld/"past alle types van beeldinhoud aan terwijl "beeld/gif"slechts dat type precies aanpast. Wanneer de veelvoudige gelijken voor een bepaald tevreden-type voorkomen, wordt de meest specifieke gelijke gebruikt. Daarom kon u "beeld/gif"in de parameter ContentFilterInclude en "beeld/"in de parameter ContentFilterExclude zetten en de "beeld/gif"antwoorden worden toegestaan maar alle andere beeldtypes worden gefiltreerd. </p> <p>Voorbeeld: <span class="filepath"> ContentFilterInclusief *</span> </p> <p>Voorbeeld: <span class="filepath"> ContentFilterAfbeelding/, tekst/css, toepassing/x-javascript uitsluiten</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> DebugLogPath </td> 
   <td colname="col2"> <p>Plaats deze parameter slechts wanneer het werken met de Raadplegende Diensten van Adobe. </p> <p>Laat toe zuiveren registreren voor de Webmodule en zender. </p> <p>U gebruikt deze parameter wanneer de <span class="wintitle"> Sensor</span> niet correct werkt. Nadat deze parameter wordt geplaatst, moet u een leeg dossier bij de gespecificeerde wegplaats creëren en "schrijf"rechten aan het voor alle gebruikers geven. Bijvoorbeeld (binnen unix shell op de Webserver): 
     <ul id="ul_7A067014A78048BF9D2F23DC66FF9E24"> 
      <li id="li_11C51EB9B9CC431585ECE9E8648F6122"><span class="filepath"> % cd/var/log</span> </li> 
      <li id="li_C56B2B5D49A543DBB258C5DE099B4AE5"><span class="filepath"> % touch vslog.txt</span> </li> 
      <li id="li_DA914383F813453AB6EF4F89279FD786"><span class="filepath"> % chmod a+w vslog.txt</span> </li> 
     </ul> </p> <p>U zou moeten toelaten zuivert registreren voor slechts een korte periode, waarna zou het logboekdossier moeten worden verzonden naar de Raadplegende Diensten van Adobe om worden geanalyseerd. </p> <p>Voorbeeld: <span class="filepath"> DebugLogPath /var/log/vslog.txt</span> </p> <p>Adobe adviseert dat deze parameter eerst in een testmilieu wordt geplaatst om het effect op uw systeem te bepalen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> DisableField </td> 
   <td colname="col2"> <p>Maakt het gespecificeerde gebied onbruikbaar </p> <p>De gebruikers kunnen gebieden elimineren die zij niet gebruiken of willen niet opslaan. Als het gebied koordwaarden neemt, die het onbruikbaar maakt gaat een leeg koord over. Als het gebied numerieke waarden neemt, overgaat het onbruikbaar makend het aantal nul (0). U kunt de volgende gebieden onbruikbaar maken: 
     <ul id="ul_4537B345EFAE449A9946DA0B52EA5C43"> 
      <li id="li_D674BC1982344C49B25A73EFF095C34A">SC-status </li> 
      <li id="li_6D647C845EB54B1B84C756DCDD7DD4CC">x-nieuwe bezoeker </li> 
      <li id="li_65EB695B223040BCB9888375354B6E8B">x-trackingid </li> 
      <li id="li_41197A9CB961496B9CD26AA8457233FD">sc-bytes </li> 
      <li id="li_DCD45D7E21964B959299494FA719F453">c-ip </li> 
      <li id="li_7650796C6246484C8267ED9923596AFB">cs-methode </li> 
      <li id="li_8941FCBBAA5E42EA9F04DA06EB91CAC5">cs-uri-stengel </li> 
      <li id="li_A10438D2DEBB4ADFB574BF7094F9F0C4">cs-uri-query </li> 
      <li id="li_1D83BA59AC8543319D1966BB8ED1D931">s-dns </li> 
      <li id="li_34A23CE1944F4AEFBE7D74E8D6D5BEE6">cs (referentie) </li> 
      <li id="li_B85D93C381BD440F82C711C9A6D56CE9">cs (cookie) </li> 
      <li id="li_18D9C084450149D6A8713EBDA0C02E5B">cs (gebruikersagent) </li> 
      <li id="li_A175CAF03E51473E990BE4F31F198B42">cs (gebruikersagent) </li> 
      <li id="li_ED38ED31B2644F2FA1C86FF93ADB9CEF">SC(inhoudstype) </li> 
      <li id="li_1173C0027C8A4638BDF35E9719CD9D4C">x-experiment </li> 
     </ul> </p> <p>Voorbeeld: <span class="filepath"> UitschakelenVeld x-trackingid</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> ExpFile </td> 
   <td colname="col2"> <p>Weg aan het Gecontroleerde de configuratiedossier van het Experiment. </p> <p>Voorbeeld: <span class="filepath"> ExpFile C:\VisualSensor\experiment.txt</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> ExpCookieURL </td> 
   <td colname="col2"> <p>Middel dat, wanneer gevraagd, veroorzaakt dat een nieuwe het volgen identiteitskaart wordt geproduceerd en de gebruiker om in een experimentele groep wordt geplaatst. </p> <p> <p>Opmerking:  Dit middel moet niet fysisch op de Webserver bestaan. </p> </p> <p>Voorbeeld: <span class="filepath"> ExpCookieURL /setcookie.htm</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> ExpPartialMatch </td> 
   <td colname="col2"> <p>Als u uw gecontroleerde experimenten wilt toelaten om uw volledige plaats of volledige subdirectory van uw plaats aan een andere plaats opnieuw in kaart te brengen, plaats deze parameter aan "op." Het gebrek is "weg." </p> <p>Voorbeeld: <span class="filepath"> ExpPartialMatch uit</span> </p> <p> <p>Opmerking:  Wees zeer voorzichtig wanneer het plaatsen van deze parameter aan "op." </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> LogAllNewUsers </td> 
   <td colname="col2"> <p>Bepaalt of de eerste klik van elke nieuwe gebruiker wordt geregistreerd zelfs als de gebruiker om een documenttype verzoekt dat door de parameter ContentFilterExclude wordt gefiltreerd. </p> <p>Het gebrek is "nee." </p> <p>Typisch worden de beelddossiers gefiltreerd uit door de parameter ContentFilterExclude. Als LogAllNewUsers aan "ja"wordt geplaatst en het allereerste document een nieuwe gebruiker krijgt van de server is een beeld, wordt dat verzoek geregistreerd. Als de parameter LogAllUsers of niet aan "nee"of plaats helemaal is geplaatst (en veronderstellend dat de beelden door de parameter ContentFilterExclude) worden gefiltreerd en het allereerste document een nieuwe gebruiker krijgt van de server is een beeld, wordt dat verzoek niet geregistreerd. </p> <p>Voorbeeld: <span class="filepath"> LogAllNewUsers</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> MaxPageLoadTime </td> 
   <td colname="col2"> <p>De hoeveelheid tijd in seconden dat de zender wacht om de volgende partij pakketten te verzenden. </p> <p>Het gebrek is 15. </p> <p>Voorbeeld: <span class="filepath"> MaxPageLoadTime 15</span> </p> <p> <p>Opmerking:  Verander deze parameterwaarde niet zonder eerst het contacteren van de Raadplegende Diensten van Adobe te contacteren. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> PrivacyID </td> 
   <td colname="col2"> <p>Laat u toe om bezoekersvolgen onbruikbaar te maken, die kan worden gebruikt om aan opt-out beleid te voldoen. </p> <p>Wanneer toegelaten, registreert de <span class="wintitle"> Sensor</span> geen "pakket"voor om het even welke bezoeker het waarvan V1st koekje aan gespecificeerde PrivacyID wordt geplaatst. Omdat geen informatie voor die bezoekers wordt geregistreerd, wordt geen informatie over die bezoekers verzonden naar de server <span class="keyword"> van de</span> gegevenswerkbank voor verwerking. </p> <p>Om deze eigenschap toe te laten, moet u de volgende stappen voltooien: 
     <ol id="ol_5D658C5E4AB14F419029E0FFC52F1310"> 
      <li id="li_BF056439F92148169BF592731264C3CD"> PrivacyID moet met een waarde van 0 (nul) in het <span class="filepath"> txlogd.conf</span> - dossier voor de <span class="wintitle"> Sensor</span>worden bepaald. <p>Voorbeeld: <span class="filepath"> Privacy-ID 0</span> </p> </li> 
      <li id="li_3E20F068C2F94512A92F284C80273B1C">De eigenaars van de website moeten code schrijven om bezoekers (V1st) koekjes te plaatsen dusdanig dat de waarde van koekje identiteitskaart de waarde aanpast PrivacyID die "<span class="filepath"> txlogd.conf</span>wordt bepaald." </li> 
     </ol> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> SiteTest </td> 
   <td colname="col2"> <p>Plaats waaraan de zender (txlogd) periodiek verzoeken verzendt om te zien of werkt de website correct. </p> <p>Merk op dat de plaats in het volgende formaat, niet als URL wordt gespecificeerd: </p> <p>http,<i>serverAddress,port,/resource</i> </p> <p>waar <i>serverAddress</i> servernaam of IP adres is, is de <i>haven</i> HTTP van de server het luisteren haven, en het <i>middel</i> is het specifieke middel om te verzoeken (kan een vraagkoord omvatten). </p> <p>U kunt veelvoudige lijnen specificeren SiteTest. </p> <p>Voorbeeld: <span class="filepath"> SiteTest http,localhost,80,/test.html</span> </p> <p> <p>Opmerking:  Alleen http wordt op dit moment ondersteund. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> TrackingCookie </td> 
   <td colname="col2"> <p>De naam van het koekje dat op browser van de bezoeker wordt geplaatst. </p> <p>Het gebrek is "v1st." </p> <p>Voorbeeld: <span class="filepath"> TrackingCookie v1st</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> VerifiërenCertName </td> 
   <td colname="col2"> <p>Wijst erop of om de server tegen parameter te bevestigen CertName </p> <p>Het gebrek is "op." </p> <p>Voorbeeld: <span class="filepath"> VerifiërenCertName op</span> </p> </td> 
  </tr> 
 </tbody> 
</table>

<table id="table_598C3CDA5AA440228AF88C3BE4A8F77C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Parameter </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> IISCaptureBytesSent </td> 
   <td colname="col2"> <p>Plaats deze parameter slechts wanneer het werken met de Raadplegende Diensten van Adobe. </p> <p>Vertelt de Sensor <span class="wintitle"></span> IIS die van twee mogelijke het registreren "haken"zou moeten worden gebruikt om een pakket te registreren </p> <p>Gebruik deze parameter wanneer de <span class="wintitle"> Sensor</span> IIS niet correct pakketten registreert. Deze parameter zou aan "van"worden geplaatst als de standaardregistrerenhaak niet correct werkte. Het gebrek is "op." </p> <p>Voorbeeld: <span class="filepath"> IISCaptureBytesVerzonden op</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> IISUseAlternateHandler </td> 
   <td colname="col2"> <p>Plaats deze parameter slechts wanneer het werken met de Raadplegende Diensten van Adobe. </p> <p>Vertelt de <span class="wintitle"> Sensor</span> welke van twee mogelijke "haken"zou moeten worden gebruikt om het v1st koekje te plaatsen. </p> <p>U gebruikt deze parameter wanneer de <span class="wintitle"> Sensor</span> IIS niet correct het v1st koekje plaatst. Deze parameter zou aan "ja"worden geplaatst als de standaardhaak niet correct plaatsend het v1st koekje. Het gebrek is "nee." </p> <p>Voorbeeld: <span class="filepath"> IISUseAlternateHandler</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>NewUserCacheControl </p> <p>CacheControl </p> </td> 
   <td colname="col2"> <p>Door gebrek, verzendt de <span class="wintitle"> Sensor</span> de reactiekopballen van de geheim voorgeheugencontrole op elk verzoek. Wanneer de eigenschap van de geheim voorgeheugencontrole wordt toegelaten <span class="wintitle"> Sensor</span> verzendt een kopbal van Verloopt met een waarde van Thu, 01 dec 1994 16:00:00 GMT naar browser. </p> <p>U kunt de antwoordkoorden wijzigen zoals gewenst door de volgende twee lijnen in het <span class="filepath"> txlogd.conf</span> - dossier uit te geven: </p> <p> <span class="filepath"> NewUserCacheControl</span> <i>&lt;<span class="filepath"> string1</span>&gt;</i> </p> <p> <span class="filepath"> CacheControl</span> <i>&lt;<span class="filepath"> string2</span>&gt;</i> </p> <p>Voorbeeld: </p> <p> <span class="filepath"> NewUserCacheControl no-cache=Set-Cookie</span> </p> <p> <span class="filepath"> CacheControl private, max-age=0,must-revalidate</span> </p> <p>Om het verzenden van de de reactiekopballen van de geheim voorgeheugencontrole onbruikbaar te maken, typ een koppelteken voor elke lijn zoals hieronder getoond: </p> <p> <span class="filepath"> NewUserCacheControl -</span> </p> <p> <span class="filepath"> CacheControl -</span> </p> </td> 
  </tr> 
 </tbody> 
</table>

<table id="table_88696CCA93874BB683538BD614E07890"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> In deze parameter... </th> 
   <th colname="col2" class="entry"> Specificeren... </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> ApacheUseAlternateHandler </td> 
   <td colname="col2"> <p>Plaats deze parameter slechts wanneer het werken met de Raadplegende Diensten van Adobe. </p> <p>Vertelt de <span class="wintitle"> Sensor</span> welke van twee mogelijke "haken"zou moeten worden gebruikt om het v1st koekje te plaatsen. </p> <p>U gebruikt deze parameter wanneer de Apache- <span class="wintitle"> sensor</span> het v1st-cookie niet correct instelt. Deze parameter zou aan "ja"worden geplaatst als de standaardhaak niet correct plaatsend het v1st koekje. Het gebrek is "nee." </p> <p>Voorbeeld: <span class="filepath"> ApacheUseAlternateHandler</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> ApacheUseBeideHandlers </td> 
   <td colname="col2"> <p>Plaats deze parameter slechts wanneer het werken met de Raadplegende Diensten van Adobe. </p> <p>Draagt de <span class="wintitle"> Sensor</span> op om te proberen het v1st koekje in beide haken te plaatsen. </p> <p>U gebruikt deze parameter wanneer de Apache- <span class="wintitle"> sensor</span> het v1st-cookie niet correct instelt. Het gebrek is "ja." </p> <p>Als de set op "ja" staat en het v1st cookie niet goed is ingesteld op de eerste haak, wordt de tweede haak gebruikt. Als de reeks aan "nee,"u de parameter ApacheUseAlternateHandler zou plaatsen om op welke haak te wijzen om het v1st koekje te gebruiken te plaatsen. </p> <p>Voorbeeld: <span class="filepath"> ApacheUseBeideHandlers ja</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>NewUserCacheControl </p> <p>CacheControl </p> </td> 
   <td colname="col2"> <p>Door gebrek, verzendt de <span class="wintitle"> Sensor</span> de reactiekopballen van de geheim voorgeheugencontrole op elk verzoek. Wanneer de eigenschap van de geheim voorgeheugencontrole wordt toegelaten <span class="wintitle"> Sensor</span> verzendt een kopbal van Verloopt met een waarde van Thu, 01 dec 1994 16:00:00 GMT naar browser. </p> <p>U kunt de antwoordkoorden wijzigen zoals gewenst door de volgende twee lijnen in het <span class="filepath"> txlogd.conf</span> - dossier uit te geven: </p> <p> <span class="filepath"> NewUserCacheControl</span> <i>&lt;<span class="filepath"> string1</span>&gt;</i> </p> <p> <span class="filepath"> CacheControl</span> <i>&lt;<span class="filepath"> string2</span>&gt;</i> </p> <p>Voorbeeld: </p> <p> <span class="filepath"> NewUserCacheControl no-cache=Set-Cookie</span> </p> <p> <span class="filepath"> CacheControl private, max-age=0,must-revalidate</span> </p> <p>Om het verzenden van de de reactiekopballen van de geheim voorgeheugencontrole onbruikbaar te maken, typ een koppelteken voor elke lijn zoals hieronder getoond: </p> <p> <span class="filepath"> NewUserCacheControl -</span> </p> <p> <span class="filepath"> CacheControl -</span> </p> <p> <p>Opmerking:  Adobe adviseert dat u niet deze eigenschap onbruikbaar maakt. </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

<table id="table_BF01F6265B8544DA9D9AD2C80A64C0F3"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> In deze parameter... </th> 
   <th colname="col2" class="entry"> Specificeren... </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> ApacheUseAlternateHandler </td> 
   <td colname="col2"> <p>Plaats deze parameter slechts wanneer het werken met de Raadplegende Diensten van Adobe. </p> <p>Vertelt de <span class="wintitle"> Sensor</span> welke van twee mogelijke "haken"zou moeten worden gebruikt om het v1st koekje te plaatsen. </p> <p>U gebruikt deze parameter wanneer de Apache- <span class="wintitle"> sensor</span> het v1st-cookie niet correct instelt. Deze parameter zou aan "ja"worden geplaatst als de standaardhaak niet correct plaatsend het v1st koekje. Het gebrek is "nee." </p> <p>Voorbeeld: <span class="filepath"> ApacheUseAlternateHandler</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> ApacheUseBeideHandlers </td> 
   <td colname="col2"> <p>Plaats deze parameter slechts wanneer het werken met de Raadplegende Diensten van Adobe. </p> <p>Draagt de <span class="wintitle"> Sensor</span> op om te proberen het v1st koekje in beide haken te plaatsen. </p> <p>U gebruikt deze parameter wanneer de Apache- <span class="wintitle"> sensor</span> het v1st-cookie niet correct instelt. Het gebrek is "ja." </p> <p>Als de set op "ja" staat en het v1st cookie niet goed is ingesteld op de eerste haak, wordt de tweede haak gebruikt. Als de reeks aan "nee,"u de parameter ApacheUseAlternateHandler zou plaatsen om op welke haak te wijzen om het v1st koekje te gebruiken te plaatsen. </p> <p>Voorbeeld: <span class="filepath"> ApacheUseBeideHandlers ja</span> </p> </td> 
  </tr> 
 </tbody> 
</table>

