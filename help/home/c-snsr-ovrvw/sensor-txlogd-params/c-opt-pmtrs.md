---
description: Informatie over optionele parameters voor het bestand Sensor txlogd.conf.
solution: Analytics
title: Optionele parameters
uuid: 8515a571-93ce-49cd-9ded-c9273259d0ee
translation-type: tm+mt
source-git-commit: 34cdcfc83ae6bb620706db37228e200cff43ab2c
workflow-type: tm+mt
source-wordcount: '1484'
ht-degree: 0%

---


# Optionele parameters{#optional-parameters}

Informatie over optionele parameters voor het bestand Sensor txlogd.conf.

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
   <td colname="col2"> <p>Hiermee kunt u opgegeven IP-adressen filteren. </p> <p>Wanneer u een bepaald adres filtert, wordt een "pakket"niet geregistreerd. Deze eigenschap elimineert interne of gecontroleerde agenten alvorens logboekverwerking, daardoor verhogend de snelheid van logboekverwerking en verminderend gegevensopslagvereisten. U kunt jokertekens gebruiken wanneer u adressen opgeeft. </p> <p>Voorbeeld: <span class="filepath"> AddressFilter 10.0.0.000</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>ContentFilterInclude </p> <p>ContentFilterExclude </p> </td> 
   <td colname="col2"> <p>Geef op of bepaalde typen inhoud moeten worden opgenomen in of uitgesloten van registratie. </p> <p>De parameterwaarden komen overeen met het inhoudstype van de reactie. </p> <p>'image/' komt bijvoorbeeld overeen met alle typen afbeeldingsinhoud, terwijl 'image/gif' alleen met dat type overeenkomt. Wanneer er meerdere overeenkomsten voorkomen voor een bepaald inhoudstype, wordt de meest specifieke overeenkomst gebruikt. Daarom kunt u "image/gif" in de parameter ContentFilterInclude en "image/" in de parameter ContentFilterExclude plaatsen en zijn "image/gif"-antwoorden toegestaan, maar alle andere afbeeldingstypen worden uitgefilterd. </p> <p>Voorbeeld: <span class="filepath"> ContentFilterInclude *</span> </p> <p>Voorbeeld: <span class="filepath"> ContentFilterExclude image/,text/css,application/x-javascript</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> DebugLogPath </td> 
   <td colname="col2"> <p>Stel deze parameter alleen in wanneer u werkt met Adobe Consulting Services. </p> <p>Laat zuivert registreren voor de Webmodule en zender toe. </p> <p>U gebruikt deze parameter wanneer de <span class="wintitle"> sensor</span> niet correct werkt. Nadat deze parameter is ingesteld, moet u een leeg bestand op de opgegeven padlocatie maken en alle gebruikers schrijfrechten geven. Bijvoorbeeld (in een unix-shell op de webserver): 
     <ul id="ul_7A067014A78048BF9D2F23DC66FF9E24"> 
      <li id="li_11C51EB9B9CC431585ECE9E8648F6122"><span class="filepath"> % cd /var/log</span> </li> 
      <li id="li_C56B2B5D49A543DBB258C5DE099B4AE5"><span class="filepath"> % touch vslog.txt</span> </li> 
      <li id="li_DA914383F813453AB6EF4F89279FD786"><span class="filepath"> % chmod a+w vslog.txt</span> </li> 
     </ul> </p> <p>U zou moeten toelaten zuivert registreren voor slechts een korte periode, waarna het logboekdossier zou moeten worden verzonden naar de Raadgevende Diensten van Adobe worden geanalyseerd. </p> <p>Voorbeeld: <span class="filepath"> DebugLogPath /var/log/vslog.txt</span> </p> <p>Adobe raadt aan dat deze parameter eerst in een testomgeving wordt ingesteld om het effect op uw systeem te bepalen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> DisableField </td> 
   <td colname="col2"> <p>Hiermee wordt het opgegeven veld uitgeschakeld </p> <p>Gebruikers kunnen velden verwijderen die ze niet gebruiken of niet willen opslaan. Als het veld tekenreekswaarden gebruikt, wordt een lege tekenreeks doorgegeven als dit wordt uitgeschakeld. Als voor het veld numerieke waarden worden gebruikt, wordt het getal nul (0) overgeslagen wanneer het veld wordt uitgeschakeld. U kunt de volgende velden uitschakelen: 
     <ul id="ul_4537B345EFAE449A9946DA0B52EA5C43"> 
      <li id="li_D674BC1982344C49B25A73EFF095C34A">sc-status </li> 
      <li id="li_6D647C845EB54B1B84C756DCDD7DD4CC">x-new-bezoeker </li> 
      <li id="li_65EB695B223040BCB9888375354B6E8B">x-trackingid </li> 
      <li id="li_41197A9CB961496B9CD26AA8457233FD">sc-bytes </li> 
      <li id="li_DCD45D7E21964B959299494FA719F453">c-ip </li> 
      <li id="li_7650796C6246484C8267ED9923596AFB">cs-method </li> 
      <li id="li_8941FCBBAA5E42EA9F04DA06EB91CAC5">cs-uri-stem </li> 
      <li id="li_A10438D2DEBB4ADFB574BF7094F9F0C4">cs-uri-query </li> 
      <li id="li_1D83BA59AC8543319D1966BB8ED1D931">s-dns </li> 
      <li id="li_34A23CE1944F4AEFBE7D74E8D6D5BEE6">cs(referentie) </li> 
      <li id="li_B85D93C381BD440F82C711C9A6D56CE9">cs(cookie) </li> 
      <li id="li_18D9C084450149D6A8713EBDA0C02E5B">cs (user-agent) </li> 
      <li id="li_A175CAF03E51473E990BE4F31F198B42">cs(userAgent) </li> 
      <li id="li_ED38ED31B2644F2FA1C86FF93ADB9CEF">sc (inhoudstype) </li> 
      <li id="li_1173C0027C8A4638BDF35E9719CD9D4C">x-experiment </li> 
     </ul> </p> <p>Voorbeeld: <span class="filepath"> x-trackingid voor veld uitschakelen</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> ExpFile </td> 
   <td colname="col2"> <p>Pad naar het configuratiebestand voor gecontroleerde experimenten. </p> <p>Voorbeeld: <span class="filepath"> ExpFile C:\VisualSensor\experiment.txt</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> ExpCookieURL </td> 
   <td colname="col2"> <p>Bron die, wanneer gevraagd, een nieuwe het volgen identiteitskaart om veroorzaakt worden geproduceerd en de gebruiker om in een proefgroep worden geplaatst. </p> <p> <p>Opmerking:  Deze bron hoeft niet fysiek op de webserver te bestaan. </p> </p> <p>Voorbeeld: <span class="filepath"> ExpCookieURL /setcookie.htm</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> ExpPartialMatch </td> 
   <td colname="col2"> <p>Als u gecontroleerde experimenten wilt toelaten om uw volledige plaats of een volledige subdirectory van uw plaats aan een andere plaats opnieuw in kaart te brengen, plaats deze parameter aan "op." De standaardwaarde is "uit". </p> <p>Voorbeeld: <span class="filepath"> ExpPartialMatch uitgeschakeld</span> </p> <p> <p>Opmerking:  Wees zeer voorzichtig wanneer u deze parameter instelt op "on." </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> LogAllNewUsers </td> 
   <td colname="col2"> <p>Bepaalt of de eerste klik van elke nieuwe gebruiker het programma wordt geopend zelfs als de gebruiker om een documenttype verzoekt dat door de parameter ContentFilterExclude wordt gefiltreerd. </p> <p>De standaardwaarde is "nee". </p> <p>Afbeeldingsbestanden worden doorgaans uitgefilterd door de parameter ContentFilterExclude. Als LogAllNewUsers wordt geplaatst aan "ja"en het zeer eerste document een nieuwe gebruiker van de server krijgt is een beeld, dat verzoek wordt geregistreerd. Als de parameter LogAllNewUsers is ingesteld op "no" of helemaal niet is ingesteld (en als wordt aangenomen dat afbeeldingen zijn uitgefilterd door de parameter ContentFilterExclude) en het allereerste document dat een nieuwe gebruiker van de server krijgt, is een afbeelding, wordt dat verzoek niet geregistreerd. </p> <p>Voorbeeld: <span class="filepath"> LogAllNewUsers niet</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> MaxPageLoadTime </td> 
   <td colname="col2"> <p>De hoeveelheid tijd in seconden dat de zender wacht om de volgende partij pakketten te verzenden. </p> <p>De standaardwaarde is 15. </p> <p>Voorbeeld: <span class="filepath"> MaxPageLoadTime 15</span> </p> <p> <p>Opmerking:  Wijzig deze parameterwaarde niet zonder eerst contact op te nemen met Adobe Consulting Services. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> PrivacyID </td> 
   <td colname="col2"> <p>Hiermee kunt u het bijhouden van bezoekers uitschakelen. Deze functie kan worden gebruikt om te voldoen aan de regels voor het weigeren van toegang. </p> <p>Wanneer toegelaten, registreert de <span class="wintitle"> Sensor</span> geen "pakket"voor om het even welke bezoeker van wie V1st koekje aan gespecificeerde PrivacyID wordt geplaatst. Omdat voor deze bezoekers geen informatie wordt geregistreerd, wordt geen informatie over die bezoekers verzonden naar de server <span class="keyword"> van de</span> gegevenswerkbank voor verwerking. </p> <p>Als u deze functie wilt inschakelen, moet u de volgende stappen uitvoeren: 
     <ol id="ol_5D658C5E4AB14F419029E0FFC52F1310"> 
      <li id="li_BF056439F92148169BF592731264C3CD"> PrivacyID moet worden gedefinieerd met de waarde 0 (nul) in het bestand <span class="filepath"> txlogd.conf</span> voor de <span class="wintitle"> Sensor</span>. <p>Voorbeeld: <span class="filepath"> PrivacyID 0</span> </p> </li> 
      <li id="li_3E20F068C2F94512A92F284C80273B1C">Eigenaars van websites moeten code schrijven om cookies van bezoekers (V1st) zo in te stellen dat de waarde van de cookie-id overeenkomt met de waarde voor PrivacyID die is gedefinieerd als '<span class="filepath"> txlogd.conf</span>'. </li> 
     </ol> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> SiteTest </td> 
   <td colname="col2"> <p>Locatie waarnaar de verzender (txlogd) periodiek verzoeken verzendt om te controleren of de website correct werkt. </p> <p>De locatie wordt opgegeven in de volgende indeling, niet als een URL: </p> <p>http,<i>serverAddress,poort/resource</i> </p> <p>waarbij <i>serverAddress</i> servernaam of IP-adres is, is de <i>poort</i> de HTTP-luisterpoort van de server en is de <i>resource</i> de specifieke bron die moet worden aangevraagd (kan een querytekenreeks bevatten). </p> <p>U kunt meerdere SiteTest-regels opgeven. </p> <p>Voorbeeld: <span class="filepath"> SiteTest http,localhost,80,/test.html</span> </p> <p> <p>Opmerking:  Momenteel wordt alleen http ondersteund. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> TrackingCookie </td> 
   <td colname="col2"> <p>De naam van de cookie die is ingesteld in de browser van de bezoeker. </p> <p>De standaardwaarde is "v1st." </p> <p>Voorbeeld: <span class="filepath"> TrackingCookie v1st</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> VerifyCertName </td> 
   <td colname="col2"> <p>Geeft aan of de server moet worden gevalideerd met de CertName-parameter </p> <p>De standaardwaarde is "on." </p> <p>Voorbeeld: <span class="filepath"> VerifyCertName op</span> </p> </td> 
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
   <td colname="col2"> <p>Stel deze parameter alleen in wanneer u werkt met Adobe Consulting Services. </p> <p>Vertelt de <span class="wintitle"> Sensor</span> IIS die van twee mogelijke het registreren "haken"zou moeten worden gebruikt om een pakket te registreren </p> <p>Gebruik deze parameter wanneer de <span class="wintitle"> Sensor</span> IIS pakketten niet correct registreert. Deze parameter zou aan "weg"worden geplaatst als de standaardregistrerenhaak niet correct werkte. De standaardwaarde is "on." </p> <p>Voorbeeld: <span class="filepath"> IISCaptureBytesVerzonden op</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> IISUseAlternateHandler </td> 
   <td colname="col2"> <p>Stel deze parameter alleen in wanneer u werkt met Adobe Consulting Services. </p> <p>Geeft aan met welke <span class="wintitle"> sensor</span> van twee mogelijke "haken" het v1st-cookie moet worden ingesteld. </p> <p>U gebruikt deze parameter wanneer de IIS- <span class="wintitle"> sensor</span> het v1st-cookie niet correct instelt. Deze parameter zou op "ja"worden geplaatst als de standaardhaak niet correct het v1st koekje plaatste. De standaardwaarde is "nee". </p> <p>Voorbeeld: <span class="filepath"> IISUseAlternateHandler n</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>NewUserCacheControl </p> <p>CacheControl </p> </td> 
   <td colname="col2"> <p>Door gebrek, verzendt de <span class="wintitle"> Sensor</span> de reactiekopballen van de geheim voorgeheugencontrole op elk verzoek. Wanneer de eigenschap van de geheim voorgeheugencontrole wordt toegelaten <span class="wintitle"> Sensor</span> verzendt een kopbal van Verloopt met een waarde van Du, 01 Dec 1994 16:00:00 GMT naar browser. </p> <p>U kunt de antwoordtekenreeksen naar wens wijzigen door de volgende twee regels in het bestand <span class="filepath"> txlogd.conf</span> te bewerken: </p> <p> <span class="filepath"> NewUserCacheControl</span> <i>&lt;<span class="filepath"> string1</span>&gt;</i> </p> <p> <span class="filepath"> CacheControl</span> <i>&lt;<span class="filepath"> string2</span>&gt;</i> </p> <p>Voorbeeld: </p> <p> <span class="filepath"> NewUserCacheControl no-cache=Set-Cookie</span> </p> <p> <span class="filepath"> CacheControl private,max-age=0,moet-revalidate</span> </p> <p>Om het verzenden van de kopballen van de de reactie van de geheim voorgeheugencontrole onbruikbaar te maken, typ een koppelteken voor elke lijn zoals hieronder getoond: </p> <p> <span class="filepath"> NewUserCacheControl -</span> </p> <p> <span class="filepath"> CacheControl -</span> </p> </td> 
  </tr> 
 </tbody> 
</table>

<table id="table_88696CCA93874BB683538BD614E07890"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> In deze parameter... </th> 
   <th colname="col2" class="entry"> Opgeven... </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> ApacheUseAlternateHandler </td> 
   <td colname="col2"> <p>Stel deze parameter alleen in wanneer u werkt met Adobe Consulting Services. </p> <p>Geeft aan met welke <span class="wintitle"> sensor</span> van twee mogelijke "haken" het v1st-cookie moet worden ingesteld. </p> <p>U gebruikt deze parameter wanneer de Apache <span class="wintitle"> Sensor</span> het v1st-cookie niet correct instelt. Deze parameter zou op "ja"worden geplaatst als de standaardhaak niet correct het v1st koekje plaatste. De standaardwaarde is "nee". </p> <p>Voorbeeld: <span class="filepath"> ApacheUseAlternateHandler n</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> ApacheUsebothHandlers </td> 
   <td colname="col2"> <p>Stel deze parameter alleen in wanneer u werkt met Adobe Consulting Services. </p> <p>Geeft de <span class="wintitle"> Sensor</span> de opdracht om het v1st-cookie in beide haken in te stellen. </p> <p>U gebruikt deze parameter wanneer de Apache <span class="wintitle"> Sensor</span> het v1st-cookie niet correct instelt. De standaardwaarde is "ja". </p> <p>Als de waarde "yes" is ingesteld en het v1st-cookie niet correct is ingesteld in de eerste haak, wordt de tweede haak gebruikt. Indien ingesteld op "nee", stelt u de parameter ApacheUseAlternateHandler zo in dat deze aangeeft welke haak moet worden gebruikt om het v1st-cookie in te stellen. </p> <p>Voorbeeld: <span class="filepath"> ApacheUsebothHandlers yes</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>NewUserCacheControl </p> <p>CacheControl </p> </td> 
   <td colname="col2"> <p>Door gebrek, verzendt de <span class="wintitle"> Sensor</span> de reactiekopballen van de geheim voorgeheugencontrole op elk verzoek. Wanneer de eigenschap van de geheim voorgeheugencontrole wordt toegelaten <span class="wintitle"> Sensor</span> verzendt een kopbal van Verloopt met een waarde van Du, 01 Dec 1994 16:00:00 GMT naar browser. </p> <p>U kunt de antwoordtekenreeksen naar wens wijzigen door de volgende twee regels in het bestand <span class="filepath"> txlogd.conf</span> te bewerken: </p> <p> <span class="filepath"> NewUserCacheControl</span> <i>&lt;<span class="filepath"> string1</span>&gt;</i> </p> <p> <span class="filepath"> CacheControl</span> <i>&lt;<span class="filepath"> string2</span>&gt;</i> </p> <p>Voorbeeld: </p> <p> <span class="filepath"> NewUserCacheControl no-cache=Set-Cookie</span> </p> <p> <span class="filepath"> CacheControl private,max-age=0,moet-revalidate</span> </p> <p>Om het verzenden van de kopballen van de de reactie van de geheim voorgeheugencontrole onbruikbaar te maken, typ een koppelteken voor elke lijn zoals hieronder getoond: </p> <p> <span class="filepath"> NewUserCacheControl -</span> </p> <p> <span class="filepath"> CacheControl -</span> </p> <p> <p>Opmerking:  Adobe raadt u aan deze functie niet uit te schakelen. </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

<table id="table_BF01F6265B8544DA9D9AD2C80A64C0F3"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> In deze parameter... </th> 
   <th colname="col2" class="entry"> Opgeven... </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> ApacheUseAlternateHandler </td> 
   <td colname="col2"> <p>Stel deze parameter alleen in wanneer u werkt met Adobe Consulting Services. </p> <p>Geeft aan met welke <span class="wintitle"> sensor</span> van twee mogelijke "haken" het v1st-cookie moet worden ingesteld. </p> <p>U gebruikt deze parameter wanneer de Apache <span class="wintitle"> Sensor</span> het v1st-cookie niet correct instelt. Deze parameter zou op "ja"worden geplaatst als de standaardhaak niet correct het v1st koekje plaatste. De standaardwaarde is "nee". </p> <p>Voorbeeld: <span class="filepath"> ApacheUseAlternateHandler n</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> ApacheUsebothHandlers </td> 
   <td colname="col2"> <p>Stel deze parameter alleen in wanneer u werkt met Adobe Consulting Services. </p> <p>Geeft de <span class="wintitle"> Sensor</span> de opdracht om het v1st-cookie in beide haken in te stellen. </p> <p>U gebruikt deze parameter wanneer de Apache <span class="wintitle"> Sensor</span> het v1st-cookie niet correct instelt. De standaardwaarde is "ja". </p> <p>Als de waarde "yes" is ingesteld en het v1st-cookie niet correct is ingesteld in de eerste haak, wordt de tweede haak gebruikt. Indien ingesteld op "nee", stelt u de parameter ApacheUseAlternateHandler zo in dat deze aangeeft welke haak moet worden gebruikt om het v1st-cookie in te stellen. </p> <p>Voorbeeld: <span class="filepath"> ApacheUsebothHandlers yes</span> </p> </td> 
  </tr> 
 </tbody> 
</table>

