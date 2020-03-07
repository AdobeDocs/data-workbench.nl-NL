---
description: Stappen voor het uitgeven van het dossier Transformation.cfg voor een datasetprofiel.
solution: Analytics
title: Het bewerken van het configuratiebestand voor transformatie
topic: Data workbench
uuid: 77b9e566-4a9a-4ea1-b5ab-63a4574c0fdb
translation-type: tm+mt
source-git-commit: 27600561841db3705f4eee6ff0aeb8890444bbc9

---


# Het bewerken van het configuratiebestand voor transformatie{#editing-the-transformation-configuration-file}

Stappen voor het uitgeven van het dossier Transformation.cfg voor een datasetprofiel.

1. Terwijl het werken in uw datasetprofiel, open [!DNL Profile Manager] en klik **[!UICONTROL Dataset]** om zijn inhoud te tonen.

   Voor informatie over het openen van en het werken met [!DNL Profile Manager], zie de Gids van de Gebruiker van de Werkbank van *Gegevens*.

   >[!NOTE]
   >
   >Een subdirectory van de Transformatie kan binnen de folder van de Dataset bestaan. Deze subdirectory bevat de [!DNL Transformation Dataset Include] dossiers die voor één of meerdere geërfte profielen zijn gecreeerd. Voor informatie over [!DNL Transformation Dataset Include] dossiers, zie [Dataset omvatten Dossiers](../../../home/c-dataset-const-proc/c-dataset-inc-files/c-abt-dataset-inc-files.md).

1. Klik het vinkje naast met de rechtermuisknop aan [!DNL Transformation.cfg] en klik **[!UICONTROL Make Local]**. Een vinkje voor dit dossier verschijnt in de [!DNL User] kolom.
1. Klik het pas gecreëerde vinkje met de rechtermuisknop aan en klik **[!UICONTROL Open]** > **[!UICONTROL in Workstation]**. Het [!DNL Transformation.cfg] venster wordt weergegeven.

   U kunt het [!DNL Transformation.cfg] dossier van ook openen [!DNL Transformation Dependency Map]. Voor informatie over [!DNL transformation dependency maps], zie de Hulpmiddelen van de Configuratie van de [Dataset](../../../home/c-dataset-const-proc/c-dataset-config-tools/c-dataset-config-tools.md#concept-6e058b7691834cf79dcfd1573f78d4f5).

1. Geef de parameters in het configuratiedossier uit gebruikend de volgende lijst als gids.

   Wanneer u het [!DNL Transformation.cfg] bestand bewerkt in een venster van een gegevensbank, kunt u sneltoetsen gebruiken voor elementaire bewerkingsfuncties, zoals snijden (Ctrl+x), kopiëren (Ctrl+c), plakken (Ctrl+v), ongedaan maken (Ctrl+z), opnieuw uitvoeren (Ctrl+Shift+z), sectie selecteren (klikken+slepen) en alles selecteren (Ctrl+a). Bovendien kunt u de kortere weg gebruiken om tekst van één configuratiedossier () aan een andere te kopiëren en te kleven. [!DNL .cfg]

   >[!NOTE]
   >
   >Een [!DNL Transformation Dataset Include] dossiers voor een geërft profiel bevat een ondergroep van de parameters die in de volgende lijst evenals sommige extra parameters worden beschreven. Voor informatie over [!DNL Transformation Dataset Include] dossiers, zie [Dataset omvatten Dossiers](../../../home/c-dataset-const-proc/c-dataset-inc-files/c-abt-dataset-inc-files.md)

   <table id="table_5E184F67CCEC4421B2BBD4261711A6FE"> 
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
      <ul id="ul_1EC55DA4936946C98E447E1476E8280F"> 
       <li id="li_F2D862833F4B451C965E1ED6C05DCE1B"> 1 januari 2013 UUR:MM.:SS EDT </li> 
       <li id="li_EB7FFEB2E2C24EAFB8E4B14F2479DA3D"> 1 januari 2013 UUR:MM:SS GMT </li> 
      </ul> </p> <p> Bijvoorbeeld, specificerend "29 Juli 2013 00:00:00 EDT"aangezien de Eind - tijd gegevens door 28 Juli, 2013, om 21:59:59 EDT omvat. </p> <p> U moet een tijdzone specificeren. De tijdzone is niet standaard op GMT indien niet opgegeven. Voor een lijst van de afkortingen van de tijdzone die door de server van de gegevenswerkbank worden gesteund, zie de Codes van de Streek van de <a href="../../../home/c-dataset-const-proc/c-time-zone.md#concept-9b540ec3e770490d94e9d5a985765477"> Tijd </a>. </p> <p> <p>Opmerking:  Als u een waarde voor de Tijd van het Eind specificeert, wordt een parameter genoemd Tijd van het Eind geplaatst en toegepast door de transformatiefase van datasetconstructie. Voor informatie over parameters, zie het <a href="../../../home/c-dataset-const-proc/c-dataset-inc-files/c-def-param-dataset-inc-files/c-def-param-dataset-inc-files.md#concept-5ad06acc8dc44bf2a99643fafdd56b50"> Bepalen van Parameters in Dataset Dossiers omvatten </a>. </p> </p> </td> 
   </tr> 
   <tr> 
      <td colname="col1"> Uitgebreide afmetingen </td> 
      <td colname="col2"> Optioneel. Adobe adviseert bepalend uitgebreide afmetingen in één of meerdere Dataset van de <span class="wintitle"> Transformatie omvat </span> dossiers. Voor informatie, zie de Dataset van de <a href="../../../home/c-dataset-const-proc/c-dataset-inc-files/c-types-dataset-inc-files/c-trans-dataset-inc-files.md#concept-c64aa78ed9ce40b8a0f4932c82ff5ace"> Transformatie omvatten Dossiers </a>. </td> 
   </tr> 
   <tr> 
      <td colname="col1"> Hash Drempel </td> 
      <td colname="col2"> <p>Optioneel. Een bemonsteringsfactor voor willekeurige subbemonstering van rijen. Als de reeks aan een aantal n, dan slechts één van elke n het volgen IDs de dataset ingaat, verminderend het totale aantal rijen in de dataset door een factor van n. Om een dataset tot stand te brengen die 100 percentennauwkeurigheid (namelijk om alle rijen te omvatten) vereist, zou u de Drempel van de Hash aan 1 plaatsen. </p> <p> Als de Drempel van de Hash in zowel de dossiers van het <span class="filepath"> Logboek Processing.cfg </span> als van de <span class="filepath"> </span> Transformation.cfg wordt gespecificeerd, wordt het niet toegepast opeenvolgend; het maximum van de waarden die in één van beide configuratiedossier worden geplaatst is van toepassing. </p> </td> 
   </tr> 
   <tr> 
      <td colname="col1"> Status voor logboekinvoer </td> 
      <td colname="col2"> Optioneel. Bepaalt de regels waardoor de output van logboekingangen van logboekverwerking voor opneming in het datasetprofiel wordt overwogen. Zie <a href="../../../home/c-dataset-const-proc/c-log-proc-config-file/c-info-log-proc-param.md#concept-ecaff95cee4e40bc90f81e099c5fc934"> de Voorwaarde van de Ingang van het Logboek </a>. </td> 
   </tr> 
   <tr> 
      <td colname="col1"> Nieuwe bezoekersvoorwaarde </td> 
      <td colname="col2"> Optioneel. Voor gebruik met Webgegevens. Bepaalt de regels waardoor de bezoekers voor opneming in de gegevens worden overwogen. De <span class="wintitle"> Nieuwe Voorwaarde van de Bezoeker </span> bepaalt de eerste logboekingang voor een bezoeker (die door tijd wordt bevolen) die in de dataset moet worden gebruikt. Alle verdere logboekingangen voor deze bezoeker zijn inbegrepen in de dataset ongeacht of zij aan deze voorwaarde voldoen. Zie <a href="../../../home/c-dataset-const-proc/c-trans-config-file/c-spec-trans-param/c-new-vstr-con.md#concept-1d0d8e26718447ad9d235e00b33a36f3"> Nieuwe bezoekersvoorwaarde </a>. </td> 
   </tr> 
   <tr> 
      <td colname="col1"> Opnieuw verwerken </td> 
      <td colname="col2"> <p>Optioneel. Om het even welk karakter of combinatie karakters kunnen hier zijn ingegaan. Het veranderen van deze parameter en het bewaren van het dossier stelt gegevensretransformatie in werking. </p> <p> Voor informatie over het opnieuw verwerken van uw gegevens, zie <a href="../../../home/c-dataset-const-proc/c-reproc-retrans/c-unst-reproc-retrans.md"> Opwerking en Herschikking </a>. </p> </td> 
   </tr> 
   <tr> 
      <td colname="col1"> Schema-controle </td> 
      <td colname="col2"> Waar of vals. Als waar, dan identificeert de server van de gegevenswerkbank de problemen van de gegevensstroom en registreert informatie over de problemen in logboekdossiers in de folder van het Spoor van de server van het Spoor van de gegevenswerkbank. De standaardwaarde is waar. Adobe adviseert verlatend deze parameter die aan waar op elk ogenblik wordt geplaatst. </td> 
   </tr> 
   <tr> 
      <td colname="col1"> Fase </td> 
      <td colname="col2"> <p>Optioneel. De namen van de verwerkingsstadia die in de Dataset van de <span class="wintitle"> Transformatie kunnen worden gebruikt omvatten </span> dossiers. De stadia van de verwerking verstrekken een manier om tot de transformaties opdracht te geven die in de Dataset van de <span class="wintitle"> Transformatie omvatten </span> dossiers worden bepaald. Deze parameter is zeer nuttig als u één of meerdere transformaties binnen veelvoudige Dataset van de <span class="wintitle"> Transformatie hebt bepaald omvat </span> dossiers en u wilt dat de specifieke transformaties op specifieke punten tijdens transformatie worden uitgevoerd. </p> <p> De orde waarin u van de stadia hier een lijst maakt bepaalt de orde waarin de transformaties in de Dataset van de <span class="wintitle"> Transformatie omvatten </span> dossiers tijdens transformatie worden uitgevoerd. <span class="wintitle"> Voorbewerking </span> en <span class="wintitle"> Postverwerking </span> zijn ingebouwd; <span class="wintitle"> Voorbewerking </span> is altijd de eerste stap en <span class="wintitle"> Postverwerking </span> is altijd de laatste stap. Door gebrek, is er één genoemd stadium genoemd <span class="wintitle"> Gebrek </span>. </p> <p> <b>Om een nieuwe verwerkingsfase toe te voegen</b> </p> <p> 
      <ul id="ul_6AF2EF72CEE34FA88575C46FA333BDA1"> 
       <li id="li_80627E7A89CE4E57A4228C4F5496533F"> Klik in het <span class="filepath"> venster </span> Transformation.cfg met de rechtermuisknop op <span class="uicontrol"> Fases </span> en klik op <span class="uicontrol"> Add New </span> &gt; <span class="uicontrol"> Stage </span>. </li> 
       <li id="li_321BEDB1E95F4AA4B282EED32A4CA196"> Ga een naam voor het nieuwe stadium in. </li> 
      </ul> </p> <p> <b>Om een bestaand verwerkingsstadium te schrappen</b> </p> <p> 
      <ul id="ul_2EFA5A40982A48919E9946BF1955110A"> 
       <li id="li_3B3829DA34FD4774B3F9F94074099794"> Klik met de rechtermuisknop op het nummer dat overeenkomt met het stadium dat u wilt verwijderen en klik op <span class="uicontrol"> Verwijderen </span><i>&lt; <span class="uicontrol"> #stage_number </span>&gt;</i>. </li> 
      </ul> </p> <p> <p>Opmerking:  Wanneer u een Stadium in een Dataset van de <span class="wintitle"> Transformatie specificeert omvat </span> dossiers moet de naam van het stadium precies de naam aanpassen die u hier ingaat. Voor meer informatie over dataset omvat dossiers, zie de <a href="../../../home/c-dataset-const-proc/c-dataset-inc-files/c-abt-dataset-inc-files.md"> Dataset Dossiers omvatten </a>. </p> </p> </td> 
   </tr> 
   <tr> 
      <td colname="col1"> Begintijd </td> 
      <td colname="col2"> <p>Optioneel. De gegevens van de filter om logboekingangen met timestamps te omvatten bij of na deze tijd. Adobe adviseert gebruikend één van de volgende formaten voor de tijd: 
      <ul id="ul_6BC86CCB1FC447ACAC4045E08C8EF8F8"> 
       <li id="li_2151B3F7FAD54F38B6C33E25CDCACBBE"> 1 januari 2013 UUR:MM.:SS EDT </li> 
       <li id="li_CA1BB675C1244104915FB9ED96A3013D"> 1 januari 2013 UUR:MM:SS GMT </li> 
      </ul> </p> <p> Bijvoorbeeld, specificerend 29 Juli 2013 00:00:00 EDT aangezien de Tijd van het <span class="wintitle"> Begin gegevens </span> omvat die vanaf 29 Juli, 2013, om 12:00:00 EDT beginnen. </p> <p> U moet een tijdzone specificeren. De tijdzone is niet standaard op GMT indien niet opgegeven. Voor een lijst van de afkortingen van de tijdzone die door de Server van de gegevenswerkbank worden gesteund, zie de Codes van de Streek van de <a href="../../../home/c-dataset-const-proc/c-time-zone.md#concept-9b540ec3e770490d94e9d5a985765477"> Tijd </a>. </p> <p> <p>Opmerking:  Als u een waarde voor de Tijd van het Begin specificeert, wordt een parameter genoemd de Tijd van het Begin geplaatst en toegepast door de transformatiefase van datasetconstructie. Voor informatie over parameters, zie het <a href="../../../home/c-dataset-const-proc/c-dataset-inc-files/c-def-param-dataset-inc-files/c-def-param-dataset-inc-files.md#concept-5ad06acc8dc44bf2a99643fafdd56b50"> Bepalen van Parameters in Dataset Dossiers omvatten </a>. </p> </p> </td> 
   </tr> 
   <tr> 
      <td colname="col1"> Transformaties </td> 
      <td colname="col2"> Optioneel. Adobe adviseert bepalend transformaties voor de transformatiefase van datasetconstructie in één of meerdere Dataset van de <span class="wintitle"> Transformatie omvat </span> dossiers. Voor informatie, zie de Dataset van de <a href="../../../home/c-dataset-const-proc/c-dataset-inc-files/c-types-dataset-inc-files/c-trans-dataset-inc-files.md#concept-c64aa78ed9ce40b8a0f4932c82ff5ace"> Transformatie omvatten Dossiers </a>. </td> 
   </tr> 
   <tr> 
      <td colname="col1"> Tijdzone </td> 
      <td colname="col2"> <p>Tijdzone van het datasetprofiel. De streken van de tijd worden gebruikt voor tijdomzettingen en voor het creëren van tijddimensies. Zie <a href="../../../home/c-dataset-const-proc/c-trans-config-file/c-spec-trans-param/c-time-zones.md#concept-9cf16b1cb4874f7d85e1dd950fdb4956"> Tijdzones </a>. </p> <p> <p>Opmerking:  Wanneer bepaald in het <span class="filepath"> Logboek Processing.cfg- </span> dossier, wordt de parameter van de Streek van de Tijd gebruikt voor slechts tijdomzettingen. </p> </p> </td> 
   </tr> 
   </tbody> 
   </table>

1. Klik **[!UICONTROL (modified)]** bij de bovenkant van het venster met de rechtermuisknop aan en klik **[!UICONTROL Save]**.
1. In [!DNL Profile Manager], klik het vinkje voor [!DNL Transformation.cfg]in de [!DNL User] kolom met de rechtermuisknop aan, dan klik **[!UICONTROL Save to]** > * **[!UICONTROL dataset profile name]** om de plaatselijk aangebrachte veranderingen van kracht te maken. De hertransformatie van de gegevens begint na synchronisatie van het datasetprofiel.

   >[!NOTE]
   >
   >Sla het gewijzigde configuratiebestand niet op in een van de interne profielen die door Adobe worden geleverd, omdat uw wijzigingen worden overschreven wanneer u updates voor deze profielen installeert.

   Zie [Reprocessing and Retransformation](../../../home/c-dataset-const-proc/c-reproc-retrans/c-unst-reproc-retrans.md)voor meer informatie over het opnieuw verwerken of transformeren van uw gegevens.
