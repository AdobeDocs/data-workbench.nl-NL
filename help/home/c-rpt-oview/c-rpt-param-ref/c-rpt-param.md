---
description: Informatie over parameters Report.cfg.
solution: Analytics
title: Report.cfg-parameters
topic: Data workbench
uuid: 7a20f4f6-99e6-401a-ba3c-c508881c0f0d
translation-type: tm+mt
source-git-commit: 2e4991206394ca0c463210990ea44dfb700341a5

---


# Report.cfg-parameters{#report-cfg-parameters}

Informatie over parameters Report.cfg.

De steekproef [!DNL Report.cfg] die in [vormt de Reeks](../../../home/c-rpt-oview/c-work-rpt-sets/t-create-rpt-set/t-config-rpt-set/t-config-rpt-set.md#task-cfb2fd0c28bc48c2acdd582fe0d670d0) van het Rapport wordt getoond bevat slechts de parameters inbegrepen in het [!DNL Report.cfg] dossier door gebrek. De volgende lijst verstrekt beschrijvingen van alle beschikbare [!DNL Report.cfg] dossierparameters.

Als u extra parameters aan een [!DNL Report.cfg] dossier moet toevoegen, moet u dit doen gebruikend een tekstredacteur. Voor stappen om dit te doen, met inbegrip van voorbeelden van hoe te om elke parameteringang te bepalen, zie het [Uitgeven van Bestaande Dossiers](../../../home/c-rpt-oview/c-work-rpt-sets/c-edit-ex-rpt-files/c-edit-ex-rpt-files.md#concept-96fd57159f454defa09bd18655a12887)Report.cfg.

>[!NOTE]
>
>De parameters in deze lijst zijn vermeld in alfabetische orde. Wanneer u het [!DNL Report.cfg] dossier in de Werkbank van Gegevens opent, zijn de vectoren vermeld in alfabetische orde, gevolgd door individuele parameters die in alfabetische orde worden vermeld.

<table id="table_F55E925EA34F43B6832788BB6878BB4A"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Parameter </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Drempelwaarde voor waarschuwingen </td> 
   <td colname="col2"> <p><i>Optioneel</i>. Deze parameter is slechts op rapporten met metrische indicatoren van toepassing. Aantal metrische indicatoren dat in het aantekenvel moet verschijnen alvorens een alarmerend rapport wordt verzonden. </p> <p>Als slechts één metrisch in het metrische indicatoraantekenvel wordt gecontroleerd, plaats de drempel aan 1. Het rapport wordt geproduceerd wanneer metrisch in het blad aan een omhoog/benedenpijl of X evalueert. Als meer dan metrisch in het rapport wordt gecontroleerd, kunt u het aantal metrische indicatoren selecteren die aan een naar boven/naar beneden pijl of X moeten evalueren alvorens het rapport wordt geproduceerd. Bijvoorbeeld, als twee metriek worden gecontroleerd: 
     <ul id="ul_A64E8A2306B14371A233D372B956F64D"> 
      <li id="li_2A3020ED350644A3954C36D3EB0B86D4">Als de drempel aan 1 wordt geplaatst, wordt het rapport geproduceerd als één van beiden van de metriek in het blad aan een omhoog/benedenpijl of X evalueert. </li> 
      <li id="li_DA4EF4984880483DA48322D9D57B9240">Als de drempel aan 2 wordt geplaatst, moeten allebei van de metriek aan een omhoog/benedenpijl of X evalueren alvorens het rapport wordt geproduceerd. </li> 
     </ul> </p> <p>Voor meer informatie over metrische indicatoren, zie de Gids <i>van de Gebruiker van de Werkbank van</i>Gegevens. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Sta het Herstel van het Rapport toe </td> 
   <td colname="col2"> <p>Wijst erop of de Server van het <span class="keyword"> Rapport </span> automatisch produceert of regenereert bepaalde rapporten wanneer u creeert of die rapporten wijzigt. De opties zijn waar of vals. Als de reeks aan waar, het creëren van of het wijzigen van een rapportwerkruimte de Server van het <span class="keyword"> Rapport veroorzaakt </span> om dat rapport voor de meest recente looppas te regenereren. </p> <p> <p>Opmerking:  Het veranderen van het <span class="filepath"> Report.cfg- </span> - dossier veroorzaakt de Server van het <span class="keyword"> Rapport </span> om alle rapporten te regenereren die door dat <span class="filepath"> Report.cfg- </span> dossier worden gecontroleerd. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Bijlagen </td> 
   <td colname="col2"> <p><i>Optioneel</i>. Sectidentificatiecode voor de naam en het inhoudstype van eventuele bijlagen die uitgaan van rapporten die via e-mail worden verspreid, inclusief het aantal bijlagen. </p> <p>Om een nieuwe gehechtheid toe te voegen: 
     <ol id="ol_CBDC1E95D34A4D08A862680127438433"> 
      <li id="li_784C48C540534F4CBB35BBDA6BC5F48E">Open het <span class="filepath"> Report.cfg- </span> dossier in de Werkbank van Gegevens. </li> 
      <li id="li_0709ADDDDF2E469FAB10761B46173136">Klik <span class="uicontrol"> Gehechtheid met de rechtermuisknop aan </span> en de klik <span class="uicontrol"> voegt nieuw kind </span> &gt; <span class="uicontrol"> Gehechtheid toe </span>. </li> 
     </ol> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Content type </td> 
   <td colname="col2"> <p>Inhoudstype van het bestand dat moet worden bijgevoegd. </p> <p>Voorbeeld: afbeelding/jpeg </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> FileName </td> 
   <td colname="col2"> <p>Plaats en naam van het bestand dat moet worden bijgevoegd. </p> <p>Voorbeeld: <span class="filepath"> c:\myimage.jpg </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Kleurenreeks </td> 
   <td colname="col2"> Identificeert het kleurenschema dat voor <span class="filepath"> .png </span> dossiers moet worden gebruikt. 0 is voor een zwarte achtergrond; 1 is voor een witte achtergrond; en 2 is voor een grayscalebeeld. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Opdracht om uit te voeren </td> 
   <td colname="col2"> <i>Optioneel</i>. Een partijbevel of uitvoerbaar dat loopt nadat de rapportreeks wordt geproduceerd. Als de lancering van de bevelshell tolk wordt vereist, ga het bevel met cmd /c vooraf. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Standaard Excel-sjabloon </td> 
   <td colname="col2"> <p><i>Optioneel</i>. De naam van het dossier van het generische het malplaatjedossier van Excel ( <span class="filepath"> .xls </span> of <span class="filepath"> .xlsx </span>) dat u wilt gebruiken wanneer het produceren van rapporten als dossiers van Excel. Deze parameter steunt volledige dossierwegen, zoals <span class="filepath"> c:\templates\mytemplate.xls </span>. </p> <p>Dit dossier wordt gebruikt voor alle rapporten van Excel tenzij een malplaatje specifiek voor een bepaald rapport is bepaald. Zie Een sjabloonbestand <a href="../../../home/c-rpt-oview/c-work-rpt-sets/t-create-rpt-set/t-config-rpt-set/c-gen-rpts-ex-files.md#section-40ab11916f464b1a88214ab969da6751"> gebruiken </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Naam dimensie </td> 
   <td colname="col2"> <i>Optioneel</i>. Naam van de afmeting waarvoor u een rapport wilt dynamisch produceren. Als u een afmetingsnaam in deze parameter ingaat, moet u een waarde in of de parameter van het Dossier van de Raadpleging of de Hoogste Metrische en Hoogste parameters van de Waarde van N ingaan. De dimensie die in deze parameter wordt genoemd moet in de dataset bestaan waarvoor de rapporten worden gecreeerd. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Alleen e-mail als perfect </td> 
   <td colname="col2"> <i>Optioneel</i>. Laat de gebruiker specificeren dat een rapportreeks zou moeten worden verzonden slechts wanneer geen fouten tijdens de looppas voorkwamen. De opties zijn waar en vals. De standaardwaarde is vals. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Einddatum </td> 
   <td colname="col2"> <p><i>Optioneel</i>. De laatste datum en de tijd dat u het rapport wilt dat wordt geplaatst om te lopen. Deze tijd is gebaseerd op het Eind van tijd van de dataset. </p> <p>Formaat: MM/DD/JJJJ u:mm tijdzone, gebruikend de syntaxis van 24 uur voor tijd </p> <p>Voorbeeld: 01-08-2007 12:01 EDT </p> <p>Voor meer informatie over de montages van de tijdzone, zie de Gids <i>van de Configuratie van de</i>Dataset. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Elke </td> 
   <td colname="col2"> Frequentie van de rapportreeks: dag, week of maand. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Time-out van Excel-doorwachter (seconden) </td> 
   <td colname="col2"> <p><i>Optioneel</i>. Het aantal seconden dat u de Server van het <span class="keyword"> Rapport </span> op Microsoft Excel wilt wachten te antwoorden wanneer het produceren van een rapport als dossier van Excel alvorens de Server van het <span class="keyword"> Rapport </span> beslist dat Excel niet antwoordt en het proces beëindigt. Het gebruiken van deze parameter laat de Server van het <span class="keyword"> Rapport toe om Excel te eindigen </span> wanneer het onontvankelijk wordt en verwerkingsend uw niet-Excel- rapporten voortzet. Het gebrek is 300.0. Om deze functionaliteit onbruikbaar te maken, plaats deze parameter aan 0.0. </p> <p>Zorg ervoor dat de waarde u bepaalt lang genoeg is om het rapport toe te laten om naar Excel worden uitgevoerd. Anders, <span class="keyword"> kan de Server van het Rapport Excel </span> voortijdig eindigen en uw rapport zal niet produceren. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Filterformule </td> 
   <td colname="col2"> <p><i>Optioneel</i>. Filter die wordt toegepast op elke werkruimte in de rapportreeks. </p> <p>Voor meer informatie, zie de <a href="https://docs.adobe.com/content/help/en/data-workbench/using/client/t-open-ins.html#Syntax_for_Filter_Expressions" format="http" scope="external"> syntaxis voor het creëren van filters </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Gammacorrectie </td> 
   <td colname="col2"> <p>Gamma-instelling voor <span class="filepath"> .png </span> bestandsuitvoer. Het gebrek is 1.6. </p> <p> <p>Opmerking:  Adobe adviseert dat u deze waarde niet verandert. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Logo's verbergen </td> 
   <td colname="col2"> Wijst erop of de Server van het Rapport de logo's verbergt wanneer het produceren van uw rapporten. De opties zijn <span class="filepath"> waar </span> of <span class="filepath"> vals </span>. Als de reeks aan <span class="filepath"> vals </span>, uw rapport met het embleem van het Rapport wordt geproduceerd. Het gebrek is <span class="filepath"> vals </span>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Opzoeken in bestand </td> 
   <td colname="col2"> <p><i>Optioneel</i>. Wanneer deze parameter wordt bevolkt, loopt de looppas van de Server van het Rapport op dynamische wijze en produceert rapporten voor elk element van de afmeting die in de parameter van de Naam van de Dimensie wordt gespecificeerd. Dit dossier moet twee lusje-afgebakende kolommen, zonder een kopbalrij bevatten. </p> <p> 
     <ul id="ul_378D4104BB5141C4A013EFE881BFFC6A"> 
      <li id="li_6F2C89A286B24FFE8EE8C82D278D0633">Kolom 1 bevat een lijst van afmetingselementen. </li> 
      <li id="li_4BD1CAA77FEC43268B40489BC5E5E6F7">Kolom 2 bevat de e-mailadressen van de rapportontvangers. Een rapport voor een bepaald element in kolom 1 wordt verzonden naar het e-mailadres op de zelfde rij in kolom 2. U kunt veelvoudige e-mailadressen ingaan door hen met komma's (geen ruimten) te scheiden. Als de rapporten niet per e-mail moeten worden verstuurd, kan deze kolom leeg zijn maar moet bestaan. </li> 
     </ul> </p> <p> <p>Opmerking:  Als u een waarde in deze parameter ingaat, moet u een waarde in de parameter van de Naam van de Dimensie ingaan. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Alleen kennisgeving </td> 
   <td colname="col2"> Dit <span class="wintitle"> </span> plaatsen van de Server van het Rapport staat u toe om gegevenswerkbank te vormen om een e-mail te verzenden wanneer een rapport wordt geproduceerd. Het plaatsen van deze waarde aan <span class="filepath"> waar verzendt </span> niet het rapport, maar verzendt eerder een e-mail die de ingetekende gebruiker op de hoogte brengt dat het rapport is geproduceerd. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Mail Report </td> 
   <td colname="col2"> <p>Sectidentificatiecode voor het verspreiden van rapporten via e-mail. Om rapporten via e-mail te verdelen, voltooi de volgende parameters voor de <span class="wintitle"> ingang van het Rapport van de Post </span> . Alle rapporten in de rapportreeks worden per e-mail verzonden in één bericht aan de e-mailadressen die in de parameter van Ontvangers worden gespecificeerd. </p> <p> <p>Opmerking:  De Server van het rapport verzendt een e-mail slechts wanneer het minstens één rapport heeft geproduceerd. </p> </p> <p>Om het e-mailen van rapporten toe te laten, moet u minstens de volgende parameters voor deze ingang voltooien: 
     <ul id="ul_539D64D61A8B4F1E95D889C6610EE3B8"> 
      <li id="li_D2EDBEE57BFE4FD4BB66F63AE561F1E2">SMTP-server </li> 
      <li id="li_4EEFE6CDA3384FE38149CE8DCBEFF847">Ontvangers </li> 
      <li id="li_CF9F0CF7ECFC4D88A7F4F11BAC4938D6">Adres afzender </li> 
      <li id="li_40BFDCDC9640488EBB450CF8579DA250">Alleen kennisgeving </li> 
     </ul> </p> <p> <p>Opmerking:  Om rapporten per e-mail te verzenden na het re-produceren van een rapportreeks, zie het <a href="../../../home/c-rpt-oview/c-work-rpt-sets/c-edit-ex-rpt-files/c-edit-ex-rpt-files.md#concept-96fd57159f454defa09bd18655a12887"> Uitgeven van Bestaande Dossiers Report.cfg </a>. </p> </p> <p>De waarde van het Bericht slechts is beschikbaar in 5.4x en 5.5x versies. </p> <p>Voor een grote reeks ontvangers die (meer dan 20) moeten worden meegedeeld, adviseert men hoogst dat u de lijsten van de e-maildistributie gebruikt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Body XSL-sjabloon </td> 
   <td colname="col2"> <p><i>Optioneel</i>. Weg van het het malplaatjedossier van XSL dat op het <span class="filepath"> reports.xml- </span> dossier moet worden toegepast. Het gebruiken van deze parameter laat de Server van het Rapport toe om uw rapporten binnen verdeelde e-mail in plaats van als gehechtheid te verzenden. De resulterende tekst wordt gebruikt als het lichaam van het e-mailbericht. </p> <p>Zie de Dossiers van de Steekproef van het <a href="../../../home/c-rpt-oview/c-rpt-sample-files/c-rpt-sample-files.md#concept-a06b93f21c5d4888be335fa2281b2a87"> Rapport </a> voor een steekproefdossier. </p> <p>Voor informatie over de Verlengbare Taal Stylesheet (XSLT), zie de Verlengbare Familie van de Taal Stylesheet <a href="http://www.w3.org/Style/XSL/" format="http" scope="external"> </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Ontvangers </td> 
   <td colname="col2"> E-mailadressen van de mensen aan wie u het rapport wilt verzenden. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Adres afzender </td> 
   <td colname="col2"> E-mailadres van de afzender. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Naam afzender </td> 
   <td colname="col2"> Optioneel. Naam van de afzender. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> SMTP-server </td> 
   <td colname="col2"> Adres van de SMTP servermachine en het wachtwoord en de gebruikersnaam die voor authentificatie worden vereist. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Onderwerp </td> 
   <td colname="col2"> <i>Optioneel</i>. Onderworpen lijn die de te verzenden e-mail beschrijft. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Alleen kennisgeving </td> 
   <td colname="col2"> Laat u gegevenswerkbank vormen om een e-mail te verzenden wanneer een achtergrondrapport wordt geproduceerd. Het plaatsen van deze waarde aan Waar verzendt niet het rapport, maar verzendt eerder een e-mail die de ingetekende gebruiker met de rapportplaats verbindt. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Uitgangswortelen </td> 
   <td colname="col2"> <p><i>Optioneel</i>. De plaats van de output van de geproduceerde rapportreeksen. Het gebrek is de <i>&lt;profielnaam&gt;</i>\ omslag van Rapporten \ binnen de de installatiefolder van de Server van het Rapport. </p> <p>Om de Server van het <span class="keyword"> Rapport aan outputrapporten </span> aan een portaal te vormen, plaats de Wortel van de <span class="wintitle"> Output </span> aan de documentwortel van de Webserver die voor het portaal wordt gebruikt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Query-filter voorladen </td> 
   <td colname="col2"> <p><i>Optioneel</i>. Deze parameter is slechts op het <span class="wintitle"> Hoogste het rapporttype van het Element van de Dimensie van toepassing </span> . </p> <p>De naam van de filter die u op de vraag wilt toepassen die moet worden in werking gesteld om de hoogste de afmetingselementen van N te bepalen alvorens het rapport kan worden geproduceerd. Het gebrek is <span class="wintitle"> Broken_Session_Filter </span>. Voor meer informatie over het <span class="wintitle"> Gebroken Filter van de Zitting </span>, zie de Gids van de Gebruiker van de Werkbank van <i>Gegevens</i>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> Rapporttypen </span> </td> 
   <td colname="col2"> <p>Opmaak(en) waarin u de uitvoer wilt genereren. U kunt om het even welke of alle volgende opties gebruiken om het rapport uit te voeren dat in veelvoudige formaten in één keer wordt geplaatst: 
     <ul id="ul_FAF024F73F6B4F2C9D6760441E8F0CF9"> 
      <li id="li_04A3E0C7812B43E7BBFCDA8C3EA21CFC">Excel leidt tot een werkboek van Excel met één visualisatie per aantekenvel. Als algemene regel, gebruik de dossiers van Excel voor e-maildistributie. Zie Rapporten <a href="../../../home/c-rpt-oview/c-work-rpt-sets/t-create-rpt-set/t-config-rpt-set/c-gen-rpts-ex-files.md#concept-0b0fdb938805422d95c5f6fe706f09ee"> genereren als Microsoft Excel-bestanden </a>. Voor informatie over het gebruiken van een malplaatjedossier, zie het <a href="../../../home/c-rpt-oview/c-work-rpt-sets/t-create-rpt-set/t-config-rpt-set/c-gen-rpts-ex-files.md#section-40ab11916f464b1a88214ab969da6751"> Gebruiken van een Dossier van het Malplaatje </a>. </li> 
      <li id="li_CD1BDDEDE85349CE8C736887BB5E4726">png leidt tot Draagbare Grafische dossiers van het Netwerk. Als algemene regel, gebruik <span class="filepath"> .png </span> - dossiers voor vertoning in Webbrowser (portaal). </li> 
      <li id="li_869DA266E6A041A5BD343537743FAC79">De duimnagel leidt tot een duimnagel ( <span class="filepath"> .jpg </span> dossier) van de werkruimte. De standaardgrootte is 240x180. Om de standaardgrootte te veranderen, geef de parameters van de Duimnagel X en van de Duimnagel Y uit. </li> 
     </ul> </p> <p>Om een nieuw rapporttype toe te voegen wanneer het uitgeven van <span class="filepath"> Report.cfg </span> in gegevenswerkbank, klik de Types van <span class="uicontrol"> Rapport met de rechtermuisknop aan </span>, voegt de klik nieuw kind toe <span class="uicontrol"> </span>, en selecteert het gewenste rapporttype. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Begindatum </td> 
   <td colname="col2"> <p>De eerste datum en de tijd dat u het rapport wilt dat wordt geplaatst om te lopen. Deze tijd is gebaseerd op het Eind van tijd van de dataset. </p> <p>Formaat: MM/DD/JJJJ hh:mm tijdzone, gebruikend de syntaxis van 24 uur voor tijd. </p> <p>Voor meer informatie over de montages van de tijdzone, zie de Gids <i>van de Configuratie van de</i>Dataset. </p> <p> <p>Opmerking:  De rapporten beginnen te lopen wanneer timestamps van de gegevens in het profiel de gespecificeerde datum en tijd aanpassen. </p> </p> <p>Voorbeeld: </p> <p>Als de begindatum 08/08/2006 12:00 EST is, lopen de rapporten voor gegevens met een timestamp van 08/08/2006 12:00 EST en later. 
     <ul id="ul_EEF6F61B55E440DFB3348A9B10DFA5F1"> 
      <li id="li_133374F1287D4631BCAE7691E3FC93B6">Dagelijkse rapporten lopen voor 08/08/2006 en elke dag daarna voor gegevens met h:mm = 12:00 EST. </li> 
      <li id="li_89514719C5F94D789E4A1049D2CD5F93">De wekelijkse verslagen lopen voor 08/08/2006 en voor elke zevende dag daarna voor gegevens met h:mm = 12:00 EST. </li> 
      <li id="li_EB986D04FA664DB89C66B0FC1CE4D36B">Maandelijkse verslagen lopen voor 08/08/2006 en voor de 8e dag van elke maand daarna voor gegevens met h:mm = 12:00 EST. </li> 
     </ul> </p> <p>De metrische <span class="wintitle"> Tijd van het Rapport </span> beïnvloedt "Laatste N"rapporteringsdimensies, zoals "Afgelopen 7 Dagen,"Gisteren,"en "3 weken geleden." Voor vragen in de Server van het Rapport, identificeert de <span class="wintitle"> metrische Tijd van het Rapport </span> ( <span class="filepath"> Rapport Time.metric </span>) de datum en de tijd waarvoor de rapporten in werking worden gesteld. Dit is aanvankelijk de datum en de tijd die in de parameter van de Datum van het Begin wordt gespecificeerd, die dan toename door de periode die door de Elke parameter wordt gespecificeerd. Voor vragen in gegevenswerkbank, is de metrische <span class="wintitle"> Tijd van het Rapport </span> gebaseerd op middernacht van metrisch ( <span class="filepath"> vanaf.metric </span>). Wegens het verschil in de definities van de metrische Tijd van het Rapport, als u een werkruimte vraagt die een Laatste dimensie van N gebruikt, kunt u verschillende resultaten in gegevenswerkbank en de Server van het <span class="keyword"> Rapport </span> voor de zelfde werkruimte ontvangen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Miniatuur X </td> 
   <td colname="col2"> <i>Optioneel</i>. Geheel dat de grootte (in pixel) controleert van de as van X van duimnagels die als output worden geproduceerd. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Miniatuur Y </td> 
   <td colname="col2"> <i>Optioneel</i>. Geheel dat de grootte (in pixel) controleert van de as van Y van duimnagels die als output worden geproduceerd. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Bovenste N metrisch </td> 
   <td colname="col2"> <p><i>Optioneel</i>. Zie de beschrijving voor de TopN parameter van de Waarde. </p> <p> <p>Opmerking:  Als u een waarde in deze parameter ingaat, moet u een waarde in de parameter van de Naam van de Dimensie en de Hoogste parameter van de Waarde ingaan N. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Beste N-waarde </td> 
   <td colname="col2"> <p><i>Optioneel</i>. Wanneer deze parameter wordt bevolkt, <span class="keyword"> </span> loopt de Server van het Rapport op dynamische wijze en produceert rapporten voor het hoogste aantal (dat in deze parameter wordt gespecificeerd) van elementen voor de afmeting die in de parameter van de Naam van de Dimensie wordt gespecificeerd, tellend door metrisch die in de Hoogste Metrische parameter van N wordt gespecificeerd. </p> <p>Voorbeeld: Als u Pagina in de parameter van de Naam van de Dimensie ingaat, Zittingen in de Hoogste Metrische parameter van N, en 5 in deze parameter, maakt een lijst van het geproduceerde rapport de vijf hoogste pagina's met het hoogste aantal zittingen. </p> <p> <p>Opmerking:  Als u een waarde in deze parameter ingaat, moet u een waarde in de parameter van de Naam van de Dimensie en de Hoogste Metrische parameter van N ingaan. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Alleen lokale steekproef gebruiken </td> 
   <td colname="col2"> <i>Optioneel</i>. Wijst erop of u de Server van het <span class="keyword"> Rapport </span> wilt produceren gebruikend slechts de lokale steekproef van de dataset. Het plaatsen van deze parameter aan waar laat u toe om een steekproef van de rapportreeks (zonder een lading op een server van de gegevenswerkbank te plaatsen) te bekijken om te zien hoe de output kijkt zonder alle tijd te nemen nodig om de gegevens volledig te verwerken. Dit werkt als testfunctie. De opties zijn waar of vals. Het gebrek is vals. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Werkruimte pad </td> 
   <td colname="col2"> <p><i>Optioneel</i>. Plaats van een inzameling van werkruimten voor een bepaalde rapportreeks. Dit is nuttig om één enkel exemplaar van werkruimten te handhaven die moeten worden geproduceerd en verdeeld veelvoudige manieren, gebruikend <span class="filepath"> Report.cfg- </span> dossiers voor veelvoudige rapportreeksen. De wortelfolder voor deze weg kan om het even welke profielomslag zijn. Voer geen schuine streep (\) in aan het begin van de tekenreeks pad. </p> <p>Voorbeeld: U kunt de gemeenschappelijke werkruimten voor Reeks A en Reeks B in de Gemeenschappelijke <span class="filepath"> omslag van Rapporten bewaren \, dan de </span> Report.cfg- <span class="filepath"> </span> dossiers voor twee verschillende rapportreeksen, elk met verschillende generatie en distributiemontages bepalen. In beide <span class="filepath"> dossiers Report.cfg, zou u de parameter van de Weg van de Werkruimte aan </span> profielnaam <i></i>\Reports\Common plaatsen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> XSL-uitvoerbestand </td> 
   <td colname="col2"> <i>Optioneel</i>. Weg van het outputdossier dat wordt gecreeerd wanneer het Malplaatje van <span class="wintitle"> XSL op de rapportindex </span> wordt toegepast. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> XSL-sjabloon </td> 
   <td colname="col2"> <p><i>Optioneel</i>. Weg van het het malplaatjedossier van XSL dat op de rapportindex moet worden toegepast. Het resulterende getransformeerde <span class="filepath"> .xml </span> wordt geschreven aan het gespecificeerde <span class="wintitle"> Dossier van de Output van XSL </span>. Zie de Dossiers van de Steekproef van het <a href="../../../home/c-rpt-oview/c-rpt-sample-files/c-rpt-sample-files.md#concept-a06b93f21c5d4888be335fa2281b2a87"> Rapport </a> voor een steekproefdossier. </p> <p> <p>Opmerking:  Tenzij u een <span class="filepath"> .xsl </span> malplaatje wanneer het produceren van uw rapporten gebruikt, worden alle rapporten verdeeld per e-mail als gehechtheid. </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

