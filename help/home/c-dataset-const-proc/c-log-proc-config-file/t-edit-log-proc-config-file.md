---
description: Stappen om het dossier van het Logboek Processing.cfg voor een datasetprofiel uit te geven.
solution: Analytics
title: Het logbestand bewerken
topic: Data workbench
uuid: 2ffae53a-ef2f-4933-821d-13f29dcdb68d
translation-type: tm+mt
source-git-commit: 27600561841db3705f4eee6ff0aeb8890444bbc9

---


# Het logbestand bewerken{#editing-the-log-processing-configuration-file}

Stappen om het dossier van het Logboek Processing.cfg voor een datasetprofiel uit te geven.

1. Terwijl het werken in uw datasetprofiel, open [!DNL Profile Manager] en klik **[!UICONTROL Dataset]** om zijn inhoud te tonen.

   Voor informatie over het openen van en het werken met [!DNL Profile Manager], zie de Gids van de Gebruiker van de Werkbank van *Gegevens*.

   >[!NOTE]
   >
   >Een subdirectory Logboek verwerken kan bestaan binnen de directory Dataset. Deze subdirectory bevat de [!DNL Log Processing Dataset Include] dossiers die voor één of meerdere geërfte profielen zijn gecreeerd. Zie [Dataset Bestanden](../../../home/c-dataset-const-proc/c-dataset-inc-files/c-abt-dataset-inc-files.md)opnemen.

1. Klik het vinkje naast met de rechtermuisknop aan [!DNL Log Processing.cfg] en klik **[!UICONTROL Make Local]**. Een vinkje voor dit dossier verschijnt in de [!DNL User] kolom.
1. Klik het pas gecreëerde vinkje met de rechtermuisknop aan en klik **[!UICONTROL Open]** > **[!UICONTROL in Workstation]**. Het [!DNL Log Processing.cfg] venster wordt weergegeven.

   U kunt het [!DNL Log Processing.cfg] dossier van ook openen [!DNL Transformation Dependency Map]. Voor informatie over de kaarten van het transformatiegebiedsdeel, zie de Hulpmiddelen [van de Configuratie van de](../../../home/c-dataset-const-proc/c-dataset-config-tools/c-dataset-config-tools.md#concept-6e058b7691834cf79dcfd1573f78d4f5)Dataset.

1. Geef de parameters in het configuratiedossier uit gebruikend de volgende lijst als gids.

   Wanneer u het [!DNL Log Processing.cfg] bestand bewerkt in een venster op een gegevensbank, kunt u sneltoetsen gebruiken voor de basisbewerkingsfuncties, zoals cut ( Ctrl+x ), copy ( Ctrl+c), pasta ( Ctrl+v ), ongedaan maken ( Ctrl+z ), opnieuw uitvoeren ( Ctrl+Shift+z ), sectie selecteren (klik+drag) en alles selecteren ( Ctrl+a ). U kunt de kortere weg aan exemplaar ook gebruiken en tekst van één configuratiedossier ( [!DNL .cfg]) kleven aan een andere.

   >[!NOTE]
   >
   >Een [!DNL Log Processing Dataset Include] dossier voor een geërft profiel bevat een ondergroep van de parameters die in de volgende lijst evenals sommige extra parameters worden beschreven. Zie [Dataset Bestanden](../../../home/c-dataset-const-proc/c-dataset-inc-files/c-abt-dataset-inc-files.md)opnemen.

   <table id="table_BC7D3635C94049A9B608463AC1DBFA69">
   <thead> 
   <tr> 
      <th colname="col1" class="entry"> Parameter </th> 
      <th colname="col2" class="entry"> Beschrijving </th> 
   </tr> 
   </thead>
   <tbody> 
   <tr> 
      <td colname="col1"> Logbronnen </td> 
      <td colname="col2"> De gegevensbronnen. Zie <a href="../../../home/c-dataset-const-proc/c-log-proc-config-file/c-log-sources.md#concept-6714c720fac044cbb9af003bf401b2ea"> Logbronnen </a>. </td> 
   </tr> 
   <tr> 
      <td colname="col1"> Eindtijd </td> 
      <td colname="col2"> <p>Optioneel. De gegevens van de filter om logboekingangen met timestamps tot maar niet met inbegrip van deze tijd te omvatten. Adobe adviseert gebruikend één van de volgende formaten voor de tijd: </p> 
      <ul id="ul_42613B1D2F3A4A6C9563BC9B54BE895E"> 
      <li id="li_BC6E5FC5CA204D89936845BE05DFE6E6">1 januari 2013 UUR:MM.:SS EDT </li> 
      <li id="li_18FE1B0417AF4207B02497664F47D23F">1 januari 2013 UUR:MM:SS GMT </li> 
      </ul> <p>Bijvoorbeeld, specificerend 29 Juli 2013 00:00:00 EDT aangezien de Eind - tijd gegevens door 28 Juli, 2013, om 11:59:59 EDT omvat. Zie <a href="../../../home/c-dataset-const-proc/c-log-proc-config-file/c-info-log-proc-param.md#concept-41bd49bf6b64442d91c232ec67529a3d"> Gegevensfilters </a>. </p> <p>U moet een tijdzone specificeren. De tijdzone is niet standaard op GMT indien niet opgegeven. Voor een lijst van de afkortingen van de tijdzone die door de server van de gegevenswerkbank worden gesteund, zie de Codes van de Streek van de <a href="../../../home/c-dataset-const-proc/c-time-zone.md#concept-9b540ec3e770490d94e9d5a985765477"> Tijd </a>. </p> <p> <p>Opmerking:  De parameter van de Tijden van het Begin van het Gebruik/van het Eind voor <span class="wintitle"> Sensor </span>, logboekdossier, en de bronnen van XML is verwant met deze parameter. Zie de secties van de Bronnen van het <a href="../../../home/c-dataset-const-proc/c-log-proc-config-file/c-log-sources.md#concept-6714c720fac044cbb9af003bf401b2ea"> Logboek </a> die deze brontypes bespreken. </p> </p> </td> 
   </tr> 
   <tr> 
      <td colname="col1"> Gebieden </td> 
      <td colname="col2"> Optioneel. Adobe adviseert bepalend <span class="wintitle"> Gebieden </span> in één of meerdere Dataset van de Verwerking van het <span class="wintitle"> Logboek omvat </span> dossiers. Zie Gegevensset voor <a href="../../../home/c-dataset-const-proc/c-dataset-inc-files/c-types-dataset-inc-files/c-log-proc-dataset-inc-files/c-log-proc-dataset-inc-files.md#concept-999475a22519432e98844622ca95b6ab"> logverwerking Bestanden opnemen </a>. </td> 
   </tr> 
   <tr> 
      <td colname="col1"> Maximum aantal sleutelbytes groeperen </td> 
      <td colname="col2"> <p>Maximum hoeveelheid gebeurtenisgegevens die de Server voor één enkele volgende identiteitskaart kan verwerken Gegevens die deze grens overschrijden, worden gefilterd uit het proces voor de samenstelling van de dataset. Deze waarde moet aan 2e6 worden geplaatst wanneer de zeer belangrijke splitsing actief is en 1e6 wanneer de zeer belangrijke splitsing niet actief is. Zie <a href="../../../home/c-dataset-const-proc/c-log-proc-config-file/c-info-log-proc-param.md#concept-64b416bbe42f4d689f90df246f7f7caf"> Key Splitting </a>. </p> <p> <p>Opmerking:  Verander deze waarde niet zonder Adobe te raadplegen. </p> </p> </td> 
   </tr> 
   <tr> 
      <td colname="col1"> Hash Drempel </td> 
      <td colname="col2"> <p>Optioneel. Een bemonsteringsfactor voor willekeurige subbemonstering van rijen. Als de reeks aan een aantal n, dan slechts één van elke n het volgen IDs de dataset ingaat, verminderend het totale aantal rijen in de dataset door een factor van n. </p> <p>Om een dataset tot stand te brengen die 100 percentennauwkeurigheid (namelijk om alle rijen te omvatten) vereist, zou u de Drempel van de Hash aan 1 plaatsen. </p> <p>Waarden: </p> <span class="filepath"> De Drempel van de knoeiboel = 1 </span> (100 percent van gegevens met inbegrip van alle rijen.) <p> <span class="filepath"> De Drempel van de knoeiboel = 2 </span> (1/2 van gegevens en omvat de helft van de rijen.) </p> <p> <span class="filepath"> De Drempel van de knoeiboel = 3 </span>(1/3 van gegevens en omvat één van drie rijen, maar ronden aan 34% in de Voltooiing van de Vraag) </p> <p> <span class="filepath"> De Drempel van de knoeiboel = 4 </span>(1/4th van gegevens en omvat één van vier rijen.) </p> <p> </p> <p> <p>Opmerking:  Het gebruiken van een het Gebruiken van een Drempel van de <span class="filepath"> Hash = 8 </span> verstrekt 1/8e van de gegevens, die 12.5% is. Nochtans de <span class="uicontrol"> </span> waarde van de Voltooiing van de Vraag in de ronden aan 13% voor deze waarde. De extra voorbeelden omvatten een Drempel van de <span class="filepath"> Hash = 6 </span> die in 17% vraagresolutie resulteert. Een drempel van de <span class="filepath"> Hash = 13 </span>resulteert in 8% vraagresolutie. </p> </p> <p>Als de Drempel van de <span class="wintitle"> Hash </span> in zowel de <span class="filepath"> dossiers van de Verwerking van het Logboek als van de </span> <span class="filepath"> </span> Transformation.cfg wordt gespecificeerd, wordt het niet toegepast opeenvolgend; de maximumwaarde die in één van beide configuratiedossier wordt geplaatst is van toepassing. Zie <a href="../../../home/c-dataset-const-proc/c-log-proc-config-file/c-info-log-proc-param.md#concept-41bd49bf6b64442d91c232ec67529a3d"> Gegevensfilters </a>. </p> </td> 
   </tr> 
   <tr> 
      <td colname="col1"> Status voor logboekinvoer </td> 
      <td colname="col2"> Optioneel. Bepaalt de regels waardoor de logboekingangen voor opneming in de dataset worden overwogen. Zie <a href="../../../home/c-dataset-const-proc/c-log-proc-config-file/c-info-log-proc-param.md#concept-ecaff95cee4e40bc90f81e099c5fc934"> de Voorwaarde van de Ingang van het Logboek </a>. </td> 
   </tr> 
   <tr> 
      <td colname="col1"> Opnieuw verwerken </td> 
      <td colname="col2"> <p>Optioneel. Om het even welk karakter of combinatie karakters kunnen hier zijn ingegaan. Het veranderen van deze parameter en het opslaan van het dossier in de machine van de Server van de gegevenswerkbank stelt gegevensverwerking in werking. </p> <p>Zie <a href="../../../home/c-dataset-const-proc/c-reproc-retrans/c-unst-reproc-retrans.md"> Reprocessing and Retransformation </a>. </p> </td> 
   </tr> 
   <tr> 
      <td colname="col1"> Splitsen Key Bucket-ruimte </td> 
      <td colname="col2"> <p>Parameter betrokken bij sleutelsplitsing. Zijn waarde zou 6e6 moeten zijn wanneer de zeer belangrijke splitsing actief is. Zie <a href="/help/home/c-dataset-const-proc/c-log-proc-config-file/c-info-log-proc-param.md#key-split"> Key Splitting </a>. </p> <p> <p>Opmerking:  Verander deze waarde niet zonder Adobe te raadplegen. </p> </p> </td> 
   </tr> 
   <tr> 
      <td colname="col1"> Sleutelbytes splitsen </td> 
      <td colname="col2"> <p>Parameter betrokken bij sleutelsplitsing. Zijn waarde zou 1e6 moeten zijn wanneer de zeer belangrijke splitsing actief is en 0 wanneer de zeer belangrijke splitsing niet actief is. Zie <a href="../../../home/c-dataset-const-proc/c-log-proc-config-file/c-info-log-proc-param.md#concept-64b416bbe42f4d689f90df246f7f7caf"> Key Splitting </a>. </p> <p> <p>Opmerking:  Verander deze waarde niet zonder Adobe te raadplegen. </p> </p> </td> 
   </tr> 
   <tr> 
      <td colname="col1"> Splitsing van de belangrijkste ruimteverhouding </td> 
      <td colname="col2"> <p>Parameter betrokken bij sleutelsplitsing. Zijn waarde zou 10 moeten zijn wanneer de zeer belangrijke splitsing actief is. Zie <a href="../../../home/c-dataset-const-proc/c-log-proc-config-file/c-info-log-proc-param.md#concept-64b416bbe42f4d689f90df246f7f7caf"> Key Splitting </a>. </p> <p> <p>Opmerking:  Verander deze waarde niet zonder Adobe te raadplegen. </p> </p> </td> 
   </tr> 
   <tr> 
      <td colname="col1"> Fase </td> 
      <td colname="col2"> <p>Optioneel. De namen van de verwerkingsstadia die in de Dataset van de Verwerking van het <span class="wintitle"> Logboek kunnen worden gebruikt omvatten </span> dossiers. De stadia van de verwerking verstrekken een manier om tot de transformaties opdracht te geven die in de Dataset van de Verwerking van het <span class="wintitle"> Logboek worden bepaald omvatten </span> dossiers. Deze parameter is zeer nuttig als u één of meerdere transformaties binnen de veelvoudige Dataset van de Verwerking van het <span class="wintitle"> Logboek hebt bepaald omvat </span> dossiers en u wilt dat de specifieke transformaties op specifieke punten tijdens logboekverwerking worden uitgevoerd. </p> <p>De orde waarin u van de stadia hier een lijst maakt bepaalt de orde waarin de transformaties in de Dataset van de Verwerking van het <span class="wintitle"> Logboek omvatten </span> dossiers tijdens logboekverwerking worden uitgevoerd. De verwerking en de Postverwerking zijn ingebouwde stadia. Voorbewerking is altijd de eerste stap, en Postverwerking is altijd de laatste stap. Door gebrek, is er één genoemd stadium genoemd Gebrek. </p> <p> <b>Om een nieuwe verwerkingsfase toe te voegen</b> 
      <ul id="ul_3A49BEAD1C134344999FED379B8CE7A3"> 
         <li id="li_AFC9B2529EC64642AFF98E9D5BA88C71">Klik in het <span class="filepath"> venster </span> Log Processing.cfg met de rechtermuisknop op <span class="uicontrol"> Fases </span> en klik op <span class="uicontrol"> Add New </span> &gt; <span class="uicontrol"> Stage </span>. </li> 
         <li id="li_5731B836658D4E1DB721C57C6275369A">Ga een naam voor het nieuwe stadium in. </li> 
      </ul> </p> <p> <b>Om een bestaand verwerkingsstadium te schrappen</b> 
      <ul id="ul_BBF4F710A5624C578F1F2A38FE18E9AD"> 
         <li id="li_CF6982C752DE41FFA97759C30CDE6AA0">Klik met de rechtermuisknop op het nummer dat overeenkomt met het stadium dat u wilt verwijderen en klik op <span class="uicontrol"> Verwijderen </span><i>&lt; <span class="uicontrol"> #stage_number </span>&gt;</i>. </li> 
      </ul> </p> <p> <p>Opmerking:  Wanneer u een <span class="wintitle"> Stadium </span> in een Dataset van de Verwerking van het <span class="wintitle"> Logboek specificeert omvat </span> dossiers, moet de naam van het stadium precies de naam aanpassen die u hier ingaat. Zie <a href="../../../home/c-dataset-const-proc/c-dataset-inc-files/c-abt-dataset-inc-files.md"> Dataset Bestanden opnemen </a>. </p> </p> </td> 
   </tr> 
   <tr> 
      <td colname="col1"> Begintijd </td> 
      <td colname="col2"> <p>Optioneel. De gegevens van de filter om logboekingangen met timestamps te omvatten bij of na deze tijd. Adobe adviseert gebruikend één van de volgende formaten voor de tijd: </p> <p> 
      <ul id="ul_0774889E22C24A6592809D289D1CBEC5"> 
         <li id="li_CE23541D8B584EA1AC432C5098564E46"> 1 januari 2013 UUR:MM.:SS EDT </li> 
         <li id="li_2EB0CF60CF12444BB744E52E9C919152"> 1 januari 2013 UUR:MM:SS GMT </li> 
      </ul> </p> <p> Bijvoorbeeld, specificerend "29 Juli 2013 00:00:00 EDT"aangezien de Tijd van het Begin gegevens omvat die vanaf 29 Juli, 2013, om 12:00:00 EDT beginnen. Zie <a href="../../../home/c-dataset-const-proc/c-log-proc-config-file/c-info-log-proc-param.md#concept-41bd49bf6b64442d91c232ec67529a3d"> Gegevensfilters </a>. </p> <p> U moet een tijdzone specificeren. De tijdzone is niet standaard op GMT indien niet opgegeven. Voor een lijst van de afkortingen van de tijdzone die door de server van de gegevenswerkbank worden gesteund, zie de Codes van de Streek van de <a href="../../../home/c-dataset-const-proc/c-time-zone.md#concept-9b540ec3e770490d94e9d5a985765477"> Tijd </a>. </p> <p> <p>Opmerking:  De parameter van de Tijden van het Begin van het Gebruik/van het Eind voor <span class="wintitle"> Sensor </span>, logboekdossier, en de bronnen van XML is verwant met deze parameter. Zie de secties van de Bronnen van het <a href="../../../home/c-dataset-const-proc/c-log-proc-config-file/c-log-sources.md#concept-6714c720fac044cbb9af003bf401b2ea"> Logboek </a> die deze brontypes bespreken. </p> </p> </td> 
   </tr> 
   <tr> 
      <td colname="col1"> Tijdzone </td> 
      <td colname="col2"> <p>Optioneel. De streek van de tijd van de server van de gegevenswerkbank die voor tijdomzettingen (zoals de omzetting die door het x-lokaal-timekoordgebied wordt vertegenwoordigd) tijdens logboekverwerking wordt gebruikt. </p> <p> <p>Opmerking:  U moet de Streek van de Tijd specificeren als u tot het omgezette tijdgebied tijdens de fase van de logboekverwerking van datasetconstructie wilt toegang hebben. Anders, registreert de server van de gegevenswerkbank een fout in de gebeurtenislogboeken. </p> </p> <p>Zie <a href="../../../home/c-dataset-const-proc/c-trans-config-file/c-spec-trans-param/c-time-zones.md#concept-9cf16b1cb4874f7d85e1dd950fdb4956"> Tijdzones </a>. </p> </td> 
   </tr> 
   <tr> 
      <td colname="col1"> Transformaties </td> 
      <td colname="col2"> Optioneel. Adobe adviseert bepalend transformaties voor logboekverwerking in één of meerdere Dataset van de Verwerking van het <span class="wintitle"> Logboek omvat </span> dossiers. Zie Gegevensset voor <a href="../../../home/c-dataset-const-proc/c-dataset-inc-files/c-types-dataset-inc-files/c-log-proc-dataset-inc-files/c-log-proc-dataset-inc-files.md#concept-999475a22519432e98844622ca95b6ab"> logverwerking Bestanden opnemen </a>. </td> 
   </tr> 
   </tbody> 
   </table>

1. Klik **[!UICONTROL (modified)]** bij de bovenkant van het venster met de rechtermuisknop aan en klik **[!UICONTROL Save]**.
1. Klik in de [!DNL Profile Manager], klik met de rechtermuisknop op het vinkje voor [!DNL Log Processing.cfg]in de [!DNL User] kolom en klik vervolgens op **[!UICONTROL Save to]** > *&lt;**[!UICONTROL dataset profile name]**>* om de lokaal aangebrachte wijzigingen van kracht te laten worden. De verwerking van de gegevens begint na synchronisatie van het datasetprofiel.

   >[!NOTE]
   >
   >Sla het gewijzigde configuratiebestand niet op in een van de interne profielen die door Adobe worden geleverd, omdat uw wijzigingen worden overschreven wanneer u updates voor deze profielen installeert.

   Voor meer informatie over het opnieuw verwerken van uw gegevens, zie [Verwerking en Herschikking](../../../home/c-dataset-const-proc/c-reproc-retrans/c-unst-reproc-retrans.md).
