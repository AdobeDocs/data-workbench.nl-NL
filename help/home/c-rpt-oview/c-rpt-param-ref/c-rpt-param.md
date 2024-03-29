---
description: Informatie over parameters Report.cfg.
title: Report.cfg-parameters
uuid: 7a20f4f6-99e6-401a-ba3c-c508881c0f0d
exl-id: 31e4de5f-f7e8-4a35-b5c6-6ad8ef79a259
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '2348'
ht-degree: 1%

---

# Report.cfg-parameters{#report-cfg-parameters}

{{eol}}

Informatie over parameters Report.cfg.

Het voorbeeld [!DNL Report.cfg] getoond in [De rapportset configureren](../../../home/c-rpt-oview/c-work-rpt-sets/t-create-rpt-set/t-config-rpt-set/t-config-rpt-set.md#task-cfb2fd0c28bc48c2acdd582fe0d670d0) bevat alleen de parameters die zijn opgenomen in de [!DNL Report.cfg] bestand standaard. In de volgende tabel vindt u een beschrijving van alle beschikbare [!DNL Report.cfg] bestandsparameters.

Als u aanvullende parameters aan een [!DNL Report.cfg] , moet u dit doen met een teksteditor. Voor stappen om dit te doen, met voorbeelden van hoe te om elke parameteringang te bepalen, zie [Bestaand Report.cfg-bestanden bewerken](../../../home/c-rpt-oview/c-work-rpt-sets/c-edit-ex-rpt-files/c-edit-ex-rpt-files.md#concept-96fd57159f454defa09bd18655a12887).

>[!NOTE]
>
>De parameters in deze tabel worden in alfabetische volgorde weergegeven. Wanneer u het dialoogvenster [!DNL Report.cfg] in Data Workbench worden vectoren in alfabetische volgorde weergegeven, gevolgd door afzonderlijke parameters in alfabetische volgorde.

<table id="table_F55E925EA34F43B6832788BB6878BB4A">
 <thead>
  <tr>
   <th colname="col1" class="entry"> Parameter </th>
   <th colname="col2" class="entry"> Beschrijving </th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td colname="col1"> Drempel voor waarschuwing </td>
   <td colname="col2"> <p><i>Optioneel</i>. Deze parameter is slechts op rapporten met metrische indicatoren van toepassing. Aantal metrische indicatoren die in het aantekenvel moeten verschijnen alvorens een alarmerend rapport wordt verzonden. </p> <p>Als slechts één metrisch in het metrische indicatoraantekenvel wordt gecontroleerd, plaats de drempel aan 1. Het rapport wordt geproduceerd wanneer metrisch in het blad aan omhoog/omlaag pijl of X evalueert. Als meer dan één metrisch in het rapport wordt gecontroleerd, kunt u het aantal metrische indicatoren selecteren die aan omhoog/onderaan pijl of X moeten evalueren alvorens het rapport wordt geproduceerd. Bijvoorbeeld, als twee metriek worden gecontroleerd:
     <ul id="ul_A64E8A2306B14371A233D372B956F64D">
      <li id="li_2A3020ED350644A3954C36D3EB0B86D4">Als de drempel aan 1 wordt geplaatst, wordt het rapport geproduceerd als één van beiden van de metriek in het blad aan een naar boven/naar pijl of X evalueert. </li>
      <li id="li_DA4EF4984880483DA48322D9D57B9240">Als de drempel aan 2 wordt geplaatst, moeten beide metriek aan omhoog/omlaag pijl of X evalueren alvorens het rapport wordt geproduceerd. </li>
     </ul> </p> <p>Voor meer informatie over metrische indicatoren, zie <i>Gebruikershandleiding voor Data Workbench</i>. </p> </td>
  </tr>
  <tr>
   <td colname="col1"> Rapportregeneratie toestaan </td>
   <td colname="col2"> <p>Geeft aan of <span class="keyword"> Rapportserver </span> Hiermee genereert of genereert u automatisch bepaalde rapporten wanneer u deze rapporten maakt of wijzigt. De opties zijn waar of onwaar. Indien ingesteld op true, veroorzaakt het maken of wijzigen van een rapportwerkruimte <span class="keyword"> Rapportserver </span> om dat rapport voor de meest recente looppas te regenereren. </p> <p> <p>Opmerking: Het wijzigen van <span class="filepath"> Report.cfg </span> bestandsoorzaken <span class="keyword"> Rapportserver </span> om alle rapporten te regenereren die door dat worden gecontroleerd <span class="filepath"> Report.cfg </span> bestand. </p> </p> </td>
  </tr>
  <tr>
   <td colname="col1"> Bijlagen </td>
   <td colname="col2"> <p><i>Optioneel</i>. Sectie-id voor de naam en het inhoudstype van alle bijlagen die gaan met rapporten die via e-mail worden verspreid, inclusief het aantal bijlagen. </p> <p>Een nieuwe bijlage toevoegen:
     <ol id="ol_CBDC1E95D34A4D08A862680127438433">
      <li id="li_784C48C540534F4CBB35BBDA6BC5F48E">Open de <span class="filepath"> Report.cfg </span> bestand in Data Workbench. </li>
      <li id="li_0709ADDDDF2E469FAB10761B46173136">Klikken met rechtermuisknop <span class="uicontrol"> Bijlagen </span> en klik op <span class="uicontrol"> Nieuw onderliggend element toevoegen </span> &gt; <span class="uicontrol"> Bijlage </span>. </li>
     </ol> </p> </td>
  </tr>
  <tr>
   <td colname="col1"> Inhoudstype </td>
   <td colname="col2"> <p>Inhoudstype van het bestand dat moet worden gekoppeld. </p> <p>Voorbeeld: image/jpeg </p> </td>
  </tr>
  <tr>
   <td colname="col1"> FileName </td>
   <td colname="col2"> <p>Locatie en naam van het bestand dat u wilt bijvoegen. </p> <p>Voorbeeld: <span class="filepath"> c:\myimage.jpg </span> </p> </td>
  </tr>
  <tr>
   <td colname="col1"> Kleurenset </td>
   <td colname="col2"> Hiermee wordt het kleurschema aangegeven dat moet worden gebruikt voor <span class="filepath"> .png </span> bestanden. 0 voor een zwarte achtergrond; 1 voor een witte achtergrond; en 2 voor een grijswaardenafbeelding. </td>
  </tr>
  <tr>
   <td colname="col1"> Uit te voeren opdracht </td>
   <td colname="col2"> <i>Optioneel</i>. Een partijbevel of uitvoerbaar die lopen nadat de rapportreeks wordt geproduceerd. Als het bevel shell interpreter wordt vereist lanceren, ga het bevel met cmd /c vooraf. </td>
  </tr>
  <tr>
   <td colname="col1"> Standaard Excel-sjabloon </td>
   <td colname="col2"> <p><i>Optioneel</i>. Bestandsnaam van het algemene Excel-sjabloonbestand ( <span class="filepath"> .xls </span> of <span class="filepath"> .xlsx </span>) die u wilt gebruiken wanneer het produceren van rapporten als dossiers van Excel. Deze parameter ondersteunt volledige bestandspaden, zoals <span class="filepath"> c:\templates\mytemplate.xls </span>. </p> <p>Dit dossier wordt gebruikt voor alle rapporten van Excel tenzij een malplaatje specifiek voor een bepaald rapport is bepaald. Zie <a href="../../../home/c-rpt-oview/c-work-rpt-sets/t-create-rpt-set/t-config-rpt-set/c-gen-rpts-ex-files.md#section-40ab11916f464b1a88214ab969da6751"> Een sjabloonbestand gebruiken </a>. </p> </td>
  </tr>
  <tr>
   <td colname="col1"> Naam dimensie </td>
   <td colname="col2"> <i>Optioneel</i>. Naam van de afmeting waarvoor u een rapport dynamisch wilt produceren. Als u een dimensienaam in deze parameter ingaat, moet u een waarde in of de parameter van het Dossier van de Opzoeker of Bovenste Metrische N en Hoogste parameters van de Waarde van N ingaan. De dimensie die in deze parameter wordt genoemd moet in de dataset bestaan waarvoor de rapporten worden gecreeerd. </td>
  </tr>
  <tr>
   <td colname="col1"> Alleen e-mail als perfect </td>
   <td colname="col2"> <i>Optioneel</i>. Laat de gebruiker specificeren dat een rapportreeks slechts zou moeten worden verzonden wanneer geen fouten tijdens de looppas voorkwamen. De opties zijn waar en onwaar. De standaardwaarde is false. </td>
  </tr>
  <tr>
   <td colname="col1"> Einddatum </td>
   <td colname="col2"> <p><i>Optioneel</i>. De laatste datum en tijd dat u het rapport wilt lopen dat wordt geplaatst. Deze tijd is gebaseerd op het begin van tijd van de dataset. </p> <p>Indeling: DD-MM-JJJJ UU:mm-tijdzone, met de syntaxis van 24 uur voor tijd </p> <p>Voorbeeld: 08/01/2007 12:01 EDT </p> <p>Voor meer informatie over de montages van de tijdzone, zie <i>Configuratie-handleiding voor gegevensset</i>. </p> </td>
  </tr>
  <tr>
   <td colname="col1"> Elke </td>
   <td colname="col2"> Frequentie van het genereren van de rapportset: dag, week of maand. </td>
  </tr>
  <tr>
   <td colname="col1"> Time-out Excel-controlehond (seconden) </td>
   <td colname="col2"> <p><i>Optioneel</i>. Het aantal seconden dat u wilt <span class="keyword"> Rapportserver </span> om op Microsoft Excel te wachten antwoorden wanneer het produceren van een rapport als dossier van Excel alvorens <span class="keyword"> Rapportserver </span> besluit dat Excel niet antwoordt en het proces beëindigt. Met deze parameter schakelt u <span class="keyword"> Rapportserver </span> om Excel te eindigen wanneer het niet antwoordt en uw niet-Excel- rapporten blijft verwerken. De standaardwaarde is 300,0. Als u deze functionaliteit wilt uitschakelen, stelt u deze parameter in op 0,0. </p> <p>Zorg ervoor dat de waarde u bepaalt lang genoeg is om het rapport toe te laten om naar Excel worden uitgevoerd. Anders, <span class="keyword"> Rapportserver </span> kan Excel voortijdig beëindigen en uw rapport zal niet produceren. </p> </td>
  </tr>
  <tr>
   <td colname="col1"> Filterformule </td>
   <td colname="col2"> <p><i>Optioneel</i>. Filter dat op elke werkruimte in de rapportreeks wordt toegepast. </p> <p>Zie voor meer informatie de <a href="https://experienceleague.adobe.com/docs/data-workbench/using/client/t-open-ins.html#Syntax_for_Filter_Expressions" format="http" scope="external"> syntaxis voor het maken van filters </a>. </p> </td>
  </tr>
  <tr>
   <td colname="col1"> Gammacorrectie </td>
   <td colname="col2"> <p>Gamma-instelling voor <span class="filepath"> .png </span> bestandsuitvoer. De standaardwaarde is 1.6. </p> <p> <p>Opmerking: Adobe raadt u aan deze waarde niet te wijzigen. </p> </p> </td>
  </tr>
  <tr>
   <td colname="col1"> Logo's verbergen </td>
   <td colname="col2"> Wijst erop of de Server van het Rapport de logo's verbergt wanneer het produceren van uw rapporten. De opties zijn <span class="filepath"> true </span> of <span class="filepath"> false </span>. Indien ingesteld op <span class="filepath"> false </span>, wordt uw rapport gegenereerd met het rapportlogo. De standaardwaarde is <span class="filepath"> false </span>. </td>
  </tr>
  <tr>
   <td colname="col1"> Bestand opzoeken </td>
   <td colname="col2"> <p><i>Optioneel</i>. Wanneer deze parameter wordt bevolkt, loopt de looppas van de Server van het Rapport op dynamische wijze en produceert rapporten voor elk element van de afmeting die in de parameter van de Naam van de Dimension wordt gespecificeerd. Dit bestand moet twee tabgescheiden kolommen bevatten, zonder koptekstrij. </p> <p>
     <ul id="ul_378D4104BB5141C4A013EFE881BFFC6A">
      <li id="li_6F2C89A286B24FFE8EE8C82D278D0633">Kolom 1 bevat een lijst met dimensie-elementen. </li>
      <li id="li_4BD1CAA77FEC43268B40489BC5E5E6F7">Kolom 2 bevat de e-mailadressen van de rapportontvangers. Een rapport voor een bepaald element in kolom 1 wordt verzonden naar het e-mailadres op dezelfde rij in kolom 2. U kunt meerdere e-mailadressen invoeren door deze te scheiden met komma's (geen spaties). Als rapporten niet moeten worden gemaild, kan deze kolom leeg zijn maar moet bestaan. </li>
     </ul> </p> <p> <p>Opmerking: Als u een waarde in deze parameter ingaat, moet u een waarde in de parameter van de Naam van de Dimension ingaan. </p> </p> </td>
  </tr>
  <tr>
   <td colname="col1"> Alleen kennisgeving </td>
   <td colname="col2"> Dit <span class="wintitle"> Rapportserver </span> het plaatsen staat u toe om gegevenswerkbank te vormen om een e-mail te verzenden wanneer een rapport wordt geproduceerd. Deze waarde instellen op <span class="filepath"> true </span> verzendt niet het rapport, maar verzendt eerder een e-mail op de hoogte brengend de ingetekende gebruiker dat het rapport is geproduceerd. </td>
  </tr>
  <tr>
   <td colname="col1"> E-mailrapport </td>
   <td colname="col2"> <p>Sectie-id voor het distribueren van rapporten via e-mail. Als u rapporten via e-mail wilt verspreiden, voert u de volgende parameters in voor de <span class="wintitle"> E-mailrapport </span> vermelding. Alle rapporten in de rapportset worden in één bericht naar de e-mailadressen gemaild die in de parameter Ontvangers zijn opgegeven. </p> <p> <p>Opmerking: De Server van het rapport verzendt een e-mail slechts wanneer het minstens één rapport heeft geproduceerd. </p> </p> <p>Als u de e-mail van rapporten wilt mogelijk maken, moet u ten minste de volgende parameters voor deze vermelding invullen:
     <ul id="ul_539D64D61A8B4F1E95D889C6610EE3B8">
      <li id="li_D2EDBEE57BFE4FD4BB66F63AE561F1E2">SMTP-server </li>
      <li id="li_4EEFE6CDA3384FE38149CE8DCBEFF847">Ontvangers </li>
      <li id="li_CF9F0CF7ECFC4D88A7F4F11BAC4938D6">Adres van afzender </li>
      <li id="li_40BFDCDC9640488EBB450CF8579DA250">Alleen kennisgeving </li>
     </ul> </p> <p> <p>Opmerking: Als u rapporten per e-mail wilt verzenden nadat u een rapportset opnieuw hebt gegenereerd, raadpleegt u <a href="../../../home/c-rpt-oview/c-work-rpt-sets/c-edit-ex-rpt-files/c-edit-ex-rpt-files.md#concept-96fd57159f454defa09bd18655a12887"> Bestaand Report.cfg-bestanden bewerken </a>. </p> </p> <p>De waarde Alleen kennisgeving is beschikbaar in 5,4x en 5,5x releases. </p> <p>Als u een groot aantal ontvangers op de hoogte wilt stellen (meer dan 20), kunt u het beste e-maildistributielijsten gebruiken. </p> </td>
  </tr>
  <tr>
   <td colname="col1"> Body XSL-sjabloon </td>
   <td colname="col2"> <p><i>Optioneel</i>. Pad van het XSL-sjabloonbestand dat moet worden toegepast op het <span class="filepath"> reports.xml </span> bestand. Het gebruiken van deze parameter laat de Server van het Rapport toe om uw rapporten binnen verdeelde e-mail in plaats van als gehechtheid te verzenden. De resulterende tekst wordt gebruikt als de hoofdtekst van het e-mailbericht. </p> <p>Zie <a href="../../../home/c-rpt-oview/c-rpt-sample-files/c-rpt-sample-files.md#concept-a06b93f21c5d4888be335fa2281b2a87"> Voorbeeldbestanden rapporteren </a> voor een voorbeeldbestand. </p> <p>Voor informatie over Extensible Stylesheet Language (XSLT) raadpleegt u <a href="https://www.w3.org/Style/XSL/" format="http" scope="external"> De uitbreidbare stijlbladtaalfamilie </a>. </p> </td>
  </tr>
  <tr>
   <td colname="col1"> Ontvangers </td>
   <td colname="col2"> E-mailadressen van de personen aan wie u het rapport wilt verzenden. </td>
  </tr>
  <tr>
   <td colname="col1"> Adres van afzender </td>
   <td colname="col2"> E-mailadres van de afzender. </td>
  </tr>
  <tr>
   <td colname="col1"> Naam afzender </td>
   <td colname="col2"> Optioneel. Naam van de afzender. </td>
  </tr>
  <tr>
   <td colname="col1"> SMTP-server </td>
   <td colname="col2"> Adres van de SMTP servermachine en het wachtwoord en de gebruikersnaam die voor authentificatie wordt vereist. </td>
  </tr>
  <tr>
   <td colname="col1"> Onderwerp </td>
   <td colname="col2"> <i>Optioneel</i>. Onderwerpregel die de te verzenden e-mail beschrijft. </td>
  </tr>
  <tr>
   <td colname="col1"> Alleen kennisgeving </td>
   <td colname="col2"> Hiermee kunt u de werkbank voor gegevens configureren om een e-mail te verzenden wanneer een achtergrondrapport wordt gegenereerd. Het plaatsen van deze waarde aan Waar verzendt niet het rapport, maar verzendt eerder een e-mail die de geabonneerde gebruiker aan de rapportplaats verbindt. </td>
  </tr>
  <tr>
   <td colname="col1"> Uitvoer hoofdmap </td>
   <td colname="col2"> <p><i>Optioneel</i>. Uitvoerlocatie van de gegenereerde rapportsets. De standaardwaarde is <i>&lt;profile name=""&gt;</i>\Reports folder within the Report Server installation directory. </p> <p>Om te vormen <span class="keyword"> Rapportserver </span> om rapporten aan een portaal uit te voeren, plaats <span class="wintitle"> Uitvoer hoofdmap </span> naar de documenthoofdmap van de webserver die voor de portal wordt gebruikt. </p> </td>
  </tr>
  <tr>
   <td colname="col1"> Query-filter vooraf laden </td>
   <td colname="col2"> <p><i>Optioneel</i>. Deze parameter is alleen van toepassing op <span class="wintitle"> Element Dimension boven </span> rapporttype. </p> <p>De naam van de filter die u op de vraag wilt toepassen die moet worden in werking gesteld om de hoogste de afmetingselementen van N te bepalen alvorens het rapport kan worden geproduceerd. De standaardwaarde is <span class="wintitle"> Gebroken_sessie_filter </span>. Voor meer informatie over de <span class="wintitle"> Filter verbroken sessie </span>, zie de <i>Gebruikershandleiding voor Data Workbench</i>. </p> </td>
  </tr>
  <tr>
   <td colname="col1"> <span class="wintitle"> Rapporttypen </span> </td>
   <td colname="col2"> <p>Indeling(en) waarin u de uitvoer wilt genereren. U kunt om het even welke of alle volgende opties gebruiken om het rapport uit te voeren dat in veelvoudige formaten tegelijkertijd wordt geplaatst:
     <ul id="ul_FAF024F73F6B4F2C9D6760441E8F0CF9">
      <li id="li_04A3E0C7812B43E7BBFCDA8C3EA21CFC">Excel leidt tot een werkboek van Excel met één visualisatie per aantekenvel. Gebruik in het algemeen Excel-bestanden voor e-maildistributie. Zie <a href="../../../home/c-rpt-oview/c-work-rpt-sets/t-create-rpt-set/t-config-rpt-set/c-gen-rpts-ex-files.md#concept-0b0fdb938805422d95c5f6fe706f09ee"> Rapporten genereren als Microsoft Excel-bestanden </a>. Voor informatie over het gebruik van een sjabloonbestand raadpleegt u <a href="../../../home/c-rpt-oview/c-work-rpt-sets/t-create-rpt-set/t-config-rpt-set/c-gen-rpts-ex-files.md#section-40ab11916f464b1a88214ab969da6751"> Een sjabloonbestand gebruiken </a>. </li>
      <li id="li_CD1BDDEDE85349CE8C736887BB5E4726">png maakt grafische bestanden voor Portable Network. Als algemene regel geldt dat <span class="filepath"> .png </span> bestanden die kunnen worden weergegeven in een webbrowser (portal). </li>
      <li id="li_869DA266E6A041A5BD343537743FAC79">Met Miniatuur wordt een miniatuur gemaakt ( <span class="filepath"> .jpg </span> bestand) van de werkruimte. De standaardgrootte is 240 x 180. Als u de standaardgrootte wilt wijzigen, bewerkt u de parameters X en Y van miniatuur. </li>
     </ul> </p> <p>Een nieuw rapporttype toevoegen tijdens het bewerken <span class="filepath"> Report.cfg </span> in gegevenswerkbank, klik met de rechtermuisknop <span class="uicontrol"> Rapporttypen </span>, klikt u op <span class="uicontrol"> Nieuw onderliggend element toevoegen </span>en selecteert u het gewenste rapporttype. </p> </td>
  </tr>
  <tr>
   <td colname="col1"> Begindatum </td>
   <td colname="col2"> <p>De eerste datum en tijd dat u het rapport wilt lopen wordt geplaatst. Deze tijd is gebaseerd op het begin van tijd van de dataset. </p> <p>Indeling: DD-MM-JJJJ UU:mm-tijdzone, met de syntaxis van 24 uur voor tijd. </p> <p>Voor meer informatie over de montages van de tijdzone, zie <i>Configuratie-handleiding voor gegevensset</i>. </p> <p> <p>Opmerking: De rapporten worden uitgevoerd wanneer de tijdstempels van de gegevens in het profiel overeenkomen met de opgegeven datum en tijd. </p> </p> <p>Voorbeeld: </p> <p>Als de begindatum 08/08/2006 12:00 EST is, worden rapporten uitgevoerd voor gegevens met een tijdstempel van 08/08/2006 12:00 EST en hoger.
     <ul id="ul_EEF6F61B55E440DFB3348A9B10DFA5F1">
      <li id="li_133374F1287D4631BCAE7691E3FC93B6">Dagelijkse rapporten zullen voor 08/08/2006 en elke dag daarna voor gegevens met hh:mm = 12:00 EST lopen. </li>
      <li id="li_89514719C5F94D789E4A1049D2CD5F93">De wekelijkse verslagen zullen voor 08/08/2006 en voor elke 7e dag daarna voor gegevens met uu:mm = 12:00 EST lopen. </li>
      <li id="li_EB986D04FA664DB89C66B0FC1CE4D36B">Maandelijkse rapporten zullen worden opgesteld voor 08/08/2006 en voor de achtste dag van elke daaropvolgende maand voor gegevens met h:mm = 12:00 EST. </li>
     </ul> </p> <p>De <span class="wintitle"> Rapporttijd </span> De metrische waarde beïnvloedt de rapportdimensies "Laatste N", zoals "Laatste 7 dagen," "Gisteren," en "3 weken geleden". Voor vragen in de Server van het Rapport, <span class="wintitle"> Rapporttijd </span> metrisch ( <span class="filepath"> Report Time.metrisch </span>) geeft de datum en het tijdstip aan waarop de rapporten worden uitgevoerd. Dit is aanvankelijk de datum en tijd die in de parameter van de Datum van het Begin worden gespecificeerd, die dan met de periode door de Elke parameter wordt gespecificeerd. Voor vragen in de werkbank van gegevens, <span class="wintitle"> Rapporttijd </span> metrisch is gebaseerd op middernacht van metrisch ( <span class="filepath"> Vanaf.metrisch </span>). Wegens het verschil in de definities van metrische de Tijd van het Rapport, als u een werkruimte vraagt die een Laatste dimensie N gebruikt, kunt u verschillende resultaten in gegevenswerkbank ontvangen en <span class="keyword"> Rapportserver </span> voor dezelfde werkruimte. </p> </td>
  </tr>
  <tr>
   <td colname="col1"> Miniatuur X </td>
   <td colname="col2"> <i>Optioneel</i>. Geheel getal dat de grootte (in pixels) van de X-as bepaalt van miniaturen die als uitvoer worden gegenereerd. </td>
  </tr>
  <tr>
   <td colname="col1"> Miniatuur Y </td>
   <td colname="col2"> <i>Optioneel</i>. Geheel getal dat de grootte (in pixels) van de Y-as bepaalt van miniaturen die als uitvoer worden gegenereerd. </td>
  </tr>
  <tr>
   <td colname="col1"> Bovenste N metrisch </td>
   <td colname="col2"> <p><i>Optioneel</i>. Zie de beschrijving voor de bovenste parameter voor N-waarden. </p> <p> <p>Opmerking: Als u een waarde in deze parameter ingaat, moet u een waarde in de parameter van de Naam van de Dimension en de Bovenste parameter van de Waarde N ingaan. </p> </p> </td>
  </tr>
  <tr>
   <td colname="col1"> Bovenste N-waarde </td>
   <td colname="col2"> <p><i>Optioneel</i>. Wanneer deze parameter wordt gevuld, <span class="keyword"> Rapportserver </span> wordt uitgevoerd in de dynamische modus en genereert rapporten voor het bovenste nummer (opgegeven in deze parameter) van de elementen voor de dimensie die is opgegeven in de parameter Dimension Name, geteld met de waarde die is opgegeven in de parameter N-metrisch boven. </p> <p>Voorbeeld: Als u Pagina in de parameter van de Naam van de Dimension, Zittingen in de Bovenste Metrische parameter N, en 5 in deze parameter ingaat, maakt het geproduceerde rapport een lijst van de vijf hoogste pagina's met het hoogste aantal zittingen. </p> <p> <p>Opmerking: Als u een waarde in deze parameter ingaat, moet u een waarde in de parameter van de Naam van de Dimension en de Bovenste metrische parameter van N ingaan. </p> </p> </td>
  </tr>
  <tr>
   <td colname="col1"> Alleen lokaal voorbeeld gebruiken </td>
   <td colname="col2"> <i>Optioneel</i>. Geeft aan of u <span class="keyword"> Rapportserver </span> om rapporten te produceren gebruikend slechts de lokale steekproef van de dataset. Het plaatsen van deze parameter aan waar laat u toe om een steekproef van de rapportreeks (zonder een lading op een server van de gegevenswerkbank te plaatsen) te bekijken om te zien hoe de output kijkt zonder alle tijd te nemen nodig om de gegevens volledig te verwerken. Dit werkt als een testfunctie. De opties zijn waar of onwaar. De standaardwaarde is false. </td>
  </tr>
  <tr>
   <td colname="col1"> Pad naar werkruimte </td>
   <td colname="col2"> <p><i>Optioneel</i>. Plaats van een inzameling van werkruimten voor een bepaalde rapportreeks. Dit is nuttig om één enkel exemplaar van werkruimten te handhaven die moeten worden geproduceerd en verdeeld veelvoudige manieren, gebruikend <span class="filepath"> Report.cfg </span> bestanden voor meerdere rapportsets. De hoofdmap voor dit pad kan elke profielmap zijn. Voer geen schuine streep (\) in aan het begin van de padtekenreeks. </p> <p>Voorbeeld: U kunt de algemene werkruimten voor Set A en Set B opslaan in het dialoogvenster <span class="filepath"> Rapporten\Algemeen </span> map, definieert vervolgens de <span class="filepath"> Report.cfg </span> dossiers voor twee verschillende rapportreeksen, elk met verschillende generatie en distributiemontages. In beide <span class="filepath"> Report.cfg </span> bestanden, stelt u de parameter Workspace Path in op <i>profielnaam</i>\Reports\Common. </p> </td>
  </tr>
  <tr>
   <td colname="col1"> XSL-uitvoerbestand </td>
   <td colname="col2"> <i>Optioneel</i>. Het pad van het uitvoerbestand dat is gemaakt bij het <span class="wintitle"> XSL-sjabloon </span> wordt toegepast op de rapportindex. </td>
  </tr>
  <tr>
   <td colname="col1"> XSL-sjabloon </td>
   <td colname="col2"> <p><i>Optioneel</i>. Pad van het XSL-sjabloonbestand dat op de rapportindex moet worden toegepast. De resulterende transformatie <span class="filepath"> .xml </span> wordt geschreven naar de opgegeven <span class="wintitle"> XSL-uitvoerbestand </span>. Zie <a href="../../../home/c-rpt-oview/c-rpt-sample-files/c-rpt-sample-files.md#concept-a06b93f21c5d4888be335fa2281b2a87"> Voorbeeldbestanden rapporteren </a> voor een voorbeeldbestand. </p> <p> <p>Opmerking: Tenzij u een <span class="filepath"> .xsl </span> alle rapporten worden tijdens het genereren van uw rapporten per e-mail als bijlagen gedistribueerd. </p> </p> </td>
  </tr>
 </tbody>
</table>
