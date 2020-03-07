---
description: Het dossier van de gegevenswerkbankTransform.cfg bevat de parameters die de logboekbronnen, de gegevenstransformaties, en de exporteurs bepalen.
solution: Analytics
title: Het bestand Transform.cfg
topic: Data workbench
uuid: eab5bb70-6de7-4f08-85db-a6cb00abd3ed
translation-type: tm+mt
source-git-commit: 27600561841db3705f4eee6ff0aeb8890444bbc9

---


# Het bestand Transform.cfg{#the-transform-cfg-file}

Het dossier van de gegevenswerkbankTransform.cfg bevat de parameters die de logboekbronnen, de gegevenstransformaties, en de exporteurs bepalen.

De transformaties die u bepaalt manipuleren ruwe gegevens die door Sensors ( [!DNL .vsl] dossiers) worden verzameld of in tekstdossiers, de dossiers van XML, of ODBC-Volgzame gegevensbestanden en output hen of in bestaande gebieden, die de huidige gegevens beschrijven, of in nieuw bepaalde gebieden.

Om transformatiefunctionaliteit te vormen, geeft u het [!DNL Transform.cfg] dossier van de gegevenswerkbank binnen de omslag van de Dataset voor het profiel uit waarvoor u gebeurtenisgegevens wilt uitvoeren. Typisch, wordt dit profiel gewijd aan transformatiefunctionaliteit (d.w.z., voert u geen andere gegevensverwerking uit dan wat in het [!DNL Transform.cfg] dossier van de gegevenswerkbank wordt bepaald). Het is belangrijk om op te merken dat om het even welke verwerkingsinstructies die in de [!DNL Log Processing Dataset Include] dossiers voor om het even welke geërfte profielen worden gespecificeerd naast die worden toegepast die in het [!DNL Transform.cfg] dossier van de gegevenswerkbank worden gespecificeerd.

Voor informatie over dataset omvat dossiers, zie de [Dataset Dossiers](../../../../../home/c-dataset-const-proc/c-dataset-inc-files/c-abt-dataset-inc-files.md)omvat.

Als de gegevens die u wilt uitvoeren door een de servercluster van de gegevenswerkbank worden verwerkt, elk van de verwerkingsservers (DPUs) in de cluster verwerkt de gegevens, maar slechts zal eerste DPU (verwerkingsserver #0 in het [!DNL profile.cfg] dossier) de outputgegevens aan zijn lokaal dossiersysteem schrijven.

**Om het dossier van Transform.cfg van de gegevenswerkbank uit te geven**

1. Terwijl het werken in het profiel waarvoor u gegevens wilt uitvoeren, open [!DNL Profile Manager] en klik **[!UICONTROL Dataset]** om de inhoud van de folder te tonen.
1. Klik het vinkje naast gegevenswerkbank met de rechtermuisknop aan [!DNL Transform.cfg], dan klik **[!UICONTROL Make Local]**. Een vinkje voor dit dossier verschijnt in de [!DNL User] kolom.
1. Klik het pas gecreëerde vinkje met de rechtermuisknop aan en klik **[!UICONTROL Open]** > **[!UICONTROL from the workbench]**. Het [!DNL Transform.cfg] venster van de gegevenswerkbank verschijnt.
1. Geef de parameters in het configuratiedossier uit gebruikend de lijst hieronder als gids:

<table id="table_91D9C4C1BE2E43158D9D06C6284EE3C7"> 
  <thead> 
    <tr> 
    <th colname="col1" class="entry"> Parameter </th> 
    <th colname="col2" class="entry"> Beschrijving </th> 
    </tr> 
  </thead>
  <tbody> 
    <tr> 
    <td colname="col1"> Eindtijd </td> 
    <td colname="col2"> <p>Optioneel. De gegevens van de filter om logboekingangen met timestamps te omvatten tot, maar zonder, dit keer te omvatten. Adobe adviseert gebruikend één van de volgende formaten voor de tijd: 
      <ul id="ul_C8C7F0F631594F7095CB83EF54E7CD0E"> 
       <li id="li_77AB6EEE8EEC4698AA886DE8BB0E2783"> 1 januari 2013 UUR:MM.:SS EDT </li> 
       <li id="li_33806070F991476BB986906876CAF7F1"> 1 januari 2013 UUR:MM:SS GMT </li> 
      </ul> </p> <p> Bijvoorbeeld, specificerend 29 Juli 2013 00:00:00 EDT aangezien de <span class="wintitle"> Eind - tijd gegevens door 28 Juli, 2013, om 11:59:59 EDT </span> omvat. </p> <p> U moet een tijdzone specificeren. De tijdzone is niet standaard op GMT indien niet opgegeven. Voor een lijst van de afkortingen van de tijdzone die door de server van de gegevenswerkbank worden gesteund, zie de Codes van de Streek van de <a href="../../../../../home/c-dataset-const-proc/c-time-zone.md#concept-9b540ec3e770490d94e9d5a985765477"> Tijd </a>. </p> <p> De parameter van de Tijden van het Begin van het Gebruik/van het Eind voor Sensor en de bronnen van het logboekdossier is verwant met deze parameter. </p> </td> 
    </tr> 
    <tr> 
    <td colname="col1"> Exporteurs </td> 
    <td colname="col2"> <p>De subvelden van een exporteur specificeren hoe de outputgegevens worden verwerkt en/of geformatteerd. U kunt veelvoudige exporteurs voor een reeks logboekbronnen bepalen. Elk type exporteur leidt tot output onafhankelijk. </p> <p> Er zijn drie soorten exporteurs: 
      <ul id="ul_C3C39F6DF3DC4F4CA2161EDB69599642"> 
       <li id="li_635FB271D0544D52B1C31740442D2E08"> ExportTextFile </li> 
       <li id="li_D496194848B44823A58890E03FFDD18E"> ExportDelimitedTextFile </li> 
       <li id="li_AEE9AA87076141FC91330D3FCFAB2101"> ExportVSLFile </li> 
      </ul> </p> <p> Voor meer informatie over de types van exporteur, zie het <a href="../../../../../home/c-dataset-const-proc/c-transf-func/c-config-files-transf/t-ins-transf-file/t-def-exp.md#task-900c40d1914347f288587bf0ca394ff2"> Bepalen van Exporteurs </a>. </p> </td> 
    </tr> 
    <tr> 
    <td colname="col1"> Hash Drempel </td> 
    <td colname="col2"> Optioneel. Een bemonsteringsfactor voor willekeurige subbemonstering van rijen. Als de reeks aan een aantal n, dan slechts één van elke n volgende IDs voor het uitvoeren wordt geselecteerd, verminderend het totale aantal rijen die door een factor van n worden uitgevoerd. Om alle rijen uit te voeren, zou u de Drempel van de knoeiboel aan 1 plaatsen. </td> 
    </tr> 
    <tr> 
    <td colname="col1"> Status voor logboekinvoer </td> 
    <td colname="col2"> Optioneel. Bepaalt de regels waardoor de logboekingangen voor de uitvoer worden overwogen. Voor meer informatie over de Voorwaarde van de Ingang van het <span class="wintitle"> Logboek </span>, zie het Dossier van de Configuratie van de Verwerking van het <a href="../../../../../home/c-dataset-const-proc/c-log-proc-config-file/c-abt-log-proc-config-file.md"> Logboek </a>. </td> 
    </tr> 
    <tr> 
    <td colname="col1"> Logbronnen </td> 
    <td colname="col2"> <p>De gegevensbronnen. <span class="wintitle"> De bronnen van het logboek </span> kunnen <span class="filepath"> .vsl </span> - dossiers, logboekdossiers, of de dossiers of gegevens van XML van ODBC-Volgzame gegevensbestanden zijn. Voor informatie over <span class="wintitle"> logboekbronnen </span>, zie het Dossier van de Configuratie van de Verwerking van het <a href="../../../../../home/c-dataset-const-proc/c-log-proc-config-file/c-abt-log-proc-config-file.md"> Logboek </a>. </p> <p> <span class="wintitle"> De transformatie </span> verwacht dat alle brongegevens in chronologische orde binnen lexicografisch bevolen inputdossiers zullen zijn. Als niet aan deze eis wordt voldaan, aangezien van berekeningen onjuist zijn, en de extra inputgegevens kunnen worden verwerkt nadat de outputdossiers worden gesloten. </p> </td> 
    </tr> 
    <tr> 
    <td colname="col1"> Offline modus </td> 
    <td colname="col2"> <p>Optioneel. Waar of vals. Als waar, <span class="wintitle"> veronderstelt de Transformatie </span> dat alle inputdossiers aanwezig zijn wanneer het begint de gegevens te verwerken. Wanneer alle inputgegevens zijn gelezen, sluit de <span class="wintitle"> Transformatie alle outputdossiers </span> zonder het wachten op extra te ontvangen gegevens. De standaardwaarde is vals. </p> <p> <p>Opmerking:  Als de <span class="wintitle"> Off-line Wijze aan waar </span> wordt geplaatst, <span class="wintitle"> verwacht de Transformatie dat alle brongegevens aanwezig </span> zijn alvorens de verwerking begint. Een waarschuwingsbericht wordt geproduceerd in het <span class="filepath"> dossier van VisualServer.log </span> als de extra gegevens worden ontvangen nadat de outputdossiers worden gesloten. </p> </p> </td> 
    </tr> 
    <tr> 
    <td colname="col1"> Opnieuw verwerken </td> 
    <td colname="col2"> <p>Optioneel. Om het even welk karakter of combinatie karakters kunnen hier zijn ingegaan. Het veranderen van deze parameter en het opslaan van het dossier in het <span class="wintitle"> systeem van de Transformatie </span> stelt gegevensopwerking in werking. </p> <p> Voor informatie over het opnieuw verwerken van uw gegevens, zie <a href="../../../../../home/c-dataset-const-proc/c-reproc-retrans/c-unst-reproc-retrans.md"> Opwerking en Herschikking </a>. </p> </td> 
    </tr> 
    <tr> 
    <td colname="col1"> Fase </td> 
    <td colname="col2"> <p>Optioneel. De namen van de verwerkingsstadia die in de Dataset van de Verwerking van het <span class="wintitle"> Logboek kunnen worden gebruikt omvatten </span> dossiers die naast het dossier van Transform.cfg van de gegevenswerkbank worden uitgevoerd <span class="filepath"> </span> . De stadia van de verwerking verstrekken een manier om tot de transformaties opdracht te geven die in de Dataset van de Verwerking van het <span class="wintitle"> Logboek worden bepaald omvatten </span> dossiers. Deze parameter is zeer nuttig als u één of meerdere transformaties binnen de veelvoudige Dataset van de Verwerking van het <span class="wintitle"> Logboek hebt bepaald omvat </span> dossiers en u wilt dat de specifieke transformaties op specifieke punten tijdens het de uitvoerproces worden uitgevoerd. </p> <p> De orde waarin u van de stadia hier een lijst maakt bepaalt de orde waarin de transformaties in de Dataset van de Verwerking van het <span class="wintitle"> Logboek omvatten </span> dossiers tijdens gegevensuitvoer worden uitgevoerd. <span class="wintitle"> Voorbewerking </span> en <span class="wintitle"> Postverwerking </span> zijn ingebouwd; <span class="wintitle"> Voorbewerking </span> is altijd de eerste stap en <span class="wintitle"> Postverwerking </span> is altijd de laatste stap. Door gebrek, is er één genoemd stadium genoemd <span class="wintitle"> Gebrek </span>. </p> <p> <b>Om een nieuwe verwerkingsfase toe te voegen</b> </p> 
      <ul id="ul_869C52DD30E443A496DC6363C3FC62B5"> 
       <li id="li_6493B2A335A8497C9A1BC6292C88CA81"> In het venster van de <span class="filepath"> Transform.cfg van de gegevenswerkbank, klik </span> Staven met de rechtermuisknop aan <span class="uicontrol"> , dan klik </span>toevoegen Nieuw <span class="uicontrol"> &gt; </span> Stadium <span class="uicontrol"> </span>. </li> 
       <li id="li_EE25E50CEB53450EA6465B08B0AE5442"> Ga een naam voor het nieuwe stadium in. </li> 
      </ul> <p> <b>Om een bestaand verwerkingsstadium te schrappen</b> </p> 
      <ul id="ul_4950BC26E0CD4837A4CB377605A52D3C"> 
      <li id="li_A61E2C17966E4F96A1256B8390623B0F"> Klik met de rechtermuisknop op het nummer dat overeenkomt met het stadium dat u wilt verwijderen en klik op <span class="uicontrol"> Verwijderen </span><i>&lt; <span class="uicontrol"> #stage_number </span>&gt;</i>. </li> 
      </ul> <p> <p>Opmerking:  Wanneer u een Stadium in een Dataset van de Verwerking van het <span class="wintitle"> Logboek specificeert omvat </span> dossier moet de naam van het stadium precies de naam aanpassen die u hier ingaat. Voor meer informatie over dataset omvat dossiers, zie de <a href="../../../../../home/c-dataset-const-proc/c-dataset-inc-files/c-abt-dataset-inc-files.md"> Dataset Dossiers omvatten </a>. </p> </p> </td> 
    </tr> 
    <tr> 
    <td colname="col1"> Begintijd </td> 
    <td colname="col2"> <p>Optioneel. De gegevens van de filter om logboekingangen met timestamps te omvatten bij of na deze tijd. Adobe adviseert gebruikend één van de volgende formaten voor de tijd: </p> 
      <ul id="ul_8F9B82A8AE7F45BE8C7949D2E96C7BEC"> 
       <li id="li_8F7BCFF251CB4F1B87DDA1A259FA9C7B"> 1 januari 2013 UUR:MM.:SS EDT </li> 
       <li id="li_4BCE317EE1914074B3642687CFED5FC2"> 1 januari 2013 UUR:MM:SS GMT </li> 
      </ul> <p> Bijvoorbeeld, specificerend 29 Juli 2013 00:00:00 EDT aangezien de Tijd van het Begin gegevens omvat die vanaf 29 Juli, 2013, om 12:00:00 EDT beginnen. </p> <p> U moet een tijdzone specificeren. De tijdzone is niet standaard op GMT indien niet opgegeven. Voor een lijst van de afkortingen van de tijdzone die door de server van de gegevenswerkbank worden gesteund, zie de Codes van de Streek van de <a href="../../../../../home/c-dataset-const-proc/c-time-zone.md#concept-9b540ec3e770490d94e9d5a985765477"> Tijd </a>. </p> <p> <p>Opmerking:  De parameter van de Tijden van het Begin van het Gebruik/van het Eind voor Sensor en de bronnen van het logboekdossier is verwant met deze parameter. </p> </p> </td> 
    </tr> 
    <tr> 
    <td colname="col1"> Transformaties </td> 
    <td colname="col2"> <p>Optioneel. Bepaalt de transformaties die op de gegevens moeten worden toegepast. Voor informatie over de beschikbare transformatietypen, zie de Transformaties van <a href="../../../../../home/c-dataset-const-proc/c-data-trans/c-abt-transf.md"> Gegevens </a>. </p> <p> <p>Opmerking:  De volgende transformatietypes werken niet wanneer bepaald in het dossier van Transform.cfg van de gegevenswerkbank <span class="filepath"> </span> dossier: </p> </p> 
      <ul id="ul_B091DFBD1C33471BBC01AEC7E92FC8CC"> 
       <li id="li_660EBECFC407488199CCCC886326806D"> ToevoegenURI </li> 
       <li id="li_56BCEBE4A2D044AE87F5B747C6501817"> Kruisrijen </li> 
       <li id="li_B23B4E81B37942DCA55FEC1A6239C5FA"> ODBCLookup </li> 
       <li id="li_EF0AFF13C40D4AB49EAB4EF1691F8FA4"> Sessionize </li> 
      </ul> </td> 
    </tr> 
  </tbody> 
  </table>

>[!NOTE]
>
>Als de extra gegevens worden ontvangen nadat de outputdossiers worden gesloten (zie [!DNL Log Sources] en [!DNL Offline Mode] in de voorafgaande lijst), [!DNL Transform] leidt tot nieuwe outputdossiers met de extra gegevens. De namen van de nieuwe outputdossiers worden geproduceerd van de naam van het originele outputdossier met de toevoeging van een parenthesized versieaantal vlak vóór de uitbreiding. Bijvoorbeeld, als het originele outputdossier is [!DNL 20070701-ABC.vsl], zullen de verdere versies van dit dossier worden genoemd [!DNL 20070701-ABC(1).vsl], [!DNL 20070701-ABC(2).vsl], etc. Merk op dat het gebruiken van de versioned dossiers als input aan de server van de gegevenswerkbank in verwerkingsfouten kan resulteren.
>
>
>Adobe adviseert vermijdend de verwezenlijking van versioned outputdossiers door ervoor te zorgen dat alle brongegevens in chronologische orde binnen lexicografisch bevolen inputdossiers zijn en, als aan waar [!DNL Offline Mode] wordt geplaatst, dat alle brongegevens aanwezig alvorens verwerkingsbegin zijn. Voor meer informatie, zie de [!DNL Log Sources] en de [!DNL Offline Mode] ingangen in de voorafgaande lijst.

1. Voeg transformaties toe door met de rechtermuisknop te klikken **[!UICONTROL Transformations]** en te klikken **[!UICONTROL Add new]** > **[!UICONTROL Transformation type]**. Voltooi de transformatievelden.

   Zie de Transformaties [van](../../../../../home/c-dataset-const-proc/c-data-trans/c-abt-transf.md) Gegevens voor beschrijvingen en voorbeelden van de transformaties die u met transformatiefunctionaliteit kunt gebruiken.

1. Klik **[!UICONTROL (modified)]** bij de bovenkant van het venster met de rechtermuisknop aan, dan klik **[!UICONTROL Save]**.
1. Om de plaatselijk aangebrachte veranderingen van kracht te maken, in [!DNL Profile Manager], klik het vinkje voor gegevenswerkbank [!DNL Transform.cfg] in de [!DNL User] kolom met de rechtermuisknop aan, dan klik **[!UICONTROL Save to]** > **[!UICONTROL profile name]**, waar de profielnaam de naam van het profiel is waarvoor u gegevens uitvoert. De opwerking van de gegevens begint na synchronisatie van het profiel.

   >[!NOTE]
   >
   >Voor informatie over het opnieuw verwerken van uw gegevens voor de uitvoer, zie [Opwerking en Herschikking](../../../../../home/c-dataset-const-proc/c-reproc-retrans/c-unst-reproc-retrans.md).
