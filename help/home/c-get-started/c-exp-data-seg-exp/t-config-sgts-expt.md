---
description: U kunt een segment van de elementen van om het even welke telbare afmeting, dan outputgegevens voor dat segment op een partij of aan de gang zijnde basis in real time in een lusje-afgebakend dossier tot stand brengen.
solution: Analytics
title: Vorm segmenten voor de uitvoer
topic: Data workbench
uuid: 651be834-ee41-4487-8c5a-30d94580f6a0
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Vorm segmenten voor de uitvoer{#configure-segments-for-export}

U kunt een segment van de elementen van om het even welke telbare afmeting, dan outputgegevens voor dat segment op een partij of aan de gang zijnde basis in real time in een lusje-afgebakend dossier tot stand brengen.

Telkens als u een segment uitvoert, output metrische of afmetingsgegevens voor alle afmetingselementen inbegrepen in dat segment. U kunt controleren hoe de outputgegevens geformatteerd zijn zodat andere systemen de gegevens kunnen gemakkelijk laden.

>[!NOTE]
>
>U kunt rapporteringsafmetingen niet uitvoeren, omdat zij een [!DNL report time.metric] dossier voor verwijzing gebruiken. Als alternerende actie, als u hard-gecodeerd [!DNL report time.metric] in het profiel plaatst, kan de segmentuitvoer het als verwijzingspunt gebruiken voor het melden van afmetingen. Nochtans, werkt [!DNL report time.metric] niet automatisch bij gebaseerd op het profiel van Tijd, zodat wanneer u de rapporteringsafmetingsverwijzing wilt veranderen, moet u het hard-gecodeerde [!DNL report time.metric] dossier veranderen.

Om een segment voor de uitvoer te vormen, moet u een [!DNL .export] dossier openen en uitgeven.

1. In [!DNL Profile Manager], klik de **[!UICONTROL Export]** folder in de [!DNL File] kolom om zijn inhoud te tonen.

       Als de folder van de Uitvoer niet bestaat, creeer het als volgt:
   
   1. Navigeer aan uw de installatiefolder van de Werkbank van Gegevens.
   1. Open de folder voor het profiel waarmee u werkt.
   1. Binnen de folder van het Profiel, creeer een nieuwe folder genoemd &quot;de Uitvoer.&quot;

1. In [!DNL Profile Manager], klik de lege cel in de [!DNL User] kolom voor de folder van de Uitvoer met de rechtermuisknop aan, dan klik **[!UICONTROL Create]** > **[!UICONTROL New Segment Export]**.

   Een dossier genoemd [!DNL New Segment Export.export] verschijnt in de [!DNL File] kolom voor de Uitvoer.

1. Noem het nieuwe dossier anders door in de kolom voor het dossier met de rechtermuisknop aan te klikken en de nieuwe naam in de parameter van het Dossier te typen. [!DNL User]
1. Open het nieuwe dossier door in de [!DNL User] kolom voor het dossier met de rechtermuisknop te klikken en **[!UICONTROL Open]** > te klikken **[!UICONTROL from the workbench]**.

   Het configuratievenster voor het [!DNL .export] dossier verschijnt.

1. Klik **[!UICONTROL Query]**, dan wijzig de gebieden van het [!DNL .export] dossier zoals die in de volgende lijst worden beschreven:

<table id="table_C2EC8FCD3FA04DE78D2CADFA3F7FD8E3"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Voor deze parameter... </th> 
   <th colname="col2" class="entry"> Verstrek deze informatie... </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Opdracht </td> 
   <td colname="col2"> <p>Optioneel. Een programma dat moet worden uitgevoerd nadat het Dossier van de Output wordt gecreeerd. Dit gebied moet uitvoerbaar (een <span class="filepath"> .exe- </span> dossier) van verwijzingen voorzien, niet shell bevel. </p> <p>Opmerking:  De segmentuitvoer zal ontbreken als er een ruimte in de bevelparameter is. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Filteren </td> 
   <td colname="col2"> <p>Optioneel. Een genoemde filter of een filteruitdrukking. U kunt of een genoemde filter tot stand brengen gebruikend een filterredacteur, dan typ hier de naam van die filter, of u kunt een filteruitdrukking zelf typen. </p> <p>Voor meer informatie over filterredacteurs, zie de Redacteurs van de <a href="../../../home/c-get-started/c-analysis-vis/c-filter-editors/c-filter-editors.md#concept-2f343ecbed8240f18b0c1f1eccef11e3"> Filter </a>. Voor meer informatie over de syntaxis van de filteruitdrukking, zie <a href="../../../home/c-get-started/c-qry-lang-syntx/c-syntx-fltr-exp.md#concept-72f2563f809747a2a3cff7ec72462a15"> Syntaxis voor de Uitdrukkingen van de Filter </a>. </p> <p>De elementen van Niveau die de filter aanpassen worden uitgevoerd, terwijl alle andere elementen niet zijn. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Niveau </td> 
   <td colname="col2"> <p>De telbare dimensie de waarvan elementen moeten worden uitgevoerd. </p> <p>Voorbeeld: Een bezoekersniveau exporteert één rij gegevens voor elke bezoeker. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Uitvoerbestand </td> 
   <td colname="col2"> <p>Pad en bestandsnaam van de geëxporteerde gegevens. Als het profiel op een de servercluster van de Werkbank van Gegevens loopt, schrijft elke server van de Werkbank van Gegevens een Dossier die van de Output een gedeelte van de gegevens bevat. </p> <p>De de serverinstallatiefolder van de Werkbank van Gegevens bevat een folder van Uitvoer waar u het outputdossier kunt bewaren. Bijvoorbeeld, kon u het Segment van de Bezoeker van de <span class="filepath"> Uitvoer ingaan \.txt </span>, waar het Segment van de <span class="filepath"> Bezoeker.txt de naam van het dossier </span> is dat de uitgevoerde gegevens bevat. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Uitvoerindeling </td> 
   <td colname="col2"> De metrische of afmetingsgegevens die voor elk element van het Niveau moeten worden uitgevoerd. Als de output een lusje-afgebakend dossier is, zouden de gebieden door de karakters van het Lusje moeten worden gescheiden, en het formaat zou met de aangewezen nieuw-lijn karakters moeten beëindigen. Voor meer informatie, zie <a href="../../../home/c-get-started/c-exp-data-seg-exp/c-abt-otpt-frmt.md#concept-ac7e24d1374a4b418365db7cc98c361e"> over het Formaat van de Output </a>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Eindtijd planning </td> 
   <td colname="col2"> <p>Optioneel. De einddatum en de tijd voor het programma, met inbegrip van de tijdzone. </p> <p>Formaat: JJJJ-MM-DD u:mm tijdzone </p> <p>Voorbeeld: 2013-08-01 12:01 EDT </p> <p>de geplande uitvoer stopt op dit moment; nochtans, wordt het Dossier van de Output nog geregenereerd wanneer zijn definitie wordt veranderd. Dit gebied is betekenisloos zonder Programma te bepalen elk. Voor meer informatie over de montages van de tijdzone, zie de Gids <i>van de Configuratie van de</i>Dataset. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Elk programma plannen </td> 
   <td colname="col2"> Optioneel. De frequentie waarbij om het Dossier van de Output te regenereren. De gesteunde waarden zijn uur, dag, week, en maand. Het dossier van de Output wordt nog geregenereerd wanneer zijn definitie wordt veranderd. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Begintijd plannen </td> 
   <td colname="col2"> <p>Optioneel. De begindatum en de tijd voor het programma, met inbegrip van de tijdzone. </p> <p>Formaat: JJJJ-MM-DD u:mm tijdzone </p> <p>Voorbeeld: 2013-08-01 12:01 EDT </p> <p>De geplande uitvoer begint op dit ogenblik, en het programma is met betrekking tot deze tijd. Dit gebied is betekenisloos zonder het bepalen van <span class="wintitle"> Programma elk </span>. Voor meer informatie over de montages van de tijdzone, zie de Gids <i>van de Configuratie van de</i>Dataset. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Termijn (sec) </td> 
   <td colname="col2"> Optioneel. De maximumtijd die wordt toegestaan om te verstrijken terwijl de segmentuitvoer wordt geproduceerd. Als het gespecificeerde interval wordt overschreden, dan begint de uitvoer over. Het plaatsen van deze waarde aan 0 (nul) verwijdert de grens. De standaardwaarde is 600 seconden. </td> 
  </tr> 
 </tbody> 
</table>

1. Klik **[!UICONTROL (New)]** bij de bovenkant van het venster met de rechtermuisknop aan, dan klik **[!UICONTROL Save]**.
1. Als u dit bestand beschikbaar wilt maken voor alle gebruikers van het werkprofiel, klikt u met de rechtermuisknop op het vinkje voor het gemaakte [!DNL .export] bestand in de [!DNL User] kolom en klikt u op **[!UICONTROL Save to]** > *&lt;**[!UICONTROL working profile name]**>*.

   >[!NOTE]
   >
   >Het opslaan van het [!DNL .export] dossier aan de server van de Werkbank van Gegevens veroorzaakt de uitvoer om één keer onmiddellijk te lopen, zelfs als de Tijd van het Begin van het Programma aan een toekomstige datum en een tijd wordt geplaatst.

   Het volgende is een steekproef [!DNL .export] dossier.

   ![](assets/vis_Segment_Export_File.png)

   >[!NOTE]
   >
   >Het [!DNL Visitor Segment.export] dossier dat in de steekproef wordt getoond verwijst naar de filter van het Segment van de Bezoeker. Het wijzigen van de definitie van deze filter verandert de definitie van de uitvoer.

