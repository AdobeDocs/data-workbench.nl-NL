---
description: Stappen om het dossier van het Logboek te uitgeven Processing.cfg voor een datasetprofiel.
title: Het configuratiebestand voor logbestanden verwerken bewerken
uuid: 2ffae53a-ef2f-4933-821d-13f29dcdb68d
exl-id: 294063ef-6771-4310-8198-df57fab1e2b4
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '1288'
ht-degree: 0%

---

# Het dossier van de Configuratie van de Verwerking van het Logboek{#editing-the-log-processing-configuration-file} uitgeven

Stappen om het dossier van het Logboek te uitgeven Processing.cfg voor een datasetprofiel.

1. Terwijl het werken in uw datasetprofiel, open [!DNL Profile Manager] en klik **[!UICONTROL Dataset]** om zijn inhoud te tonen.

   Voor informatie over het openen en het werken met [!DNL Profile Manager], zie *de Gids van de Gebruiker van de Data Workbench*.

   >[!NOTE]
   >
   >Er kan een submap voor logverwerking bestaan in de map Dataset. Deze submap bevat de [!DNL Log Processing Dataset Include] bestanden die zijn gemaakt voor een of meer overgeërfde profielen. Zie [Gegevensset met include-bestanden](../../../home/c-dataset-const-proc/c-dataset-inc-files/c-abt-dataset-inc-files.md).

1. Klik met de rechtermuisknop op het vinkje naast [!DNL Log Processing.cfg] en klik **[!UICONTROL Make Local]**. Er wordt een vinkje voor dit bestand weergegeven in de kolom [!DNL User].
1. Klik met de rechtermuisknop op het nieuwe vinkje en klik op **[!UICONTROL Open]** > **[!UICONTROL in Workstation]**. Het venster [!DNL Log Processing.cfg] verschijnt.

   U kunt het [!DNL Log Processing.cfg] dossier van [!DNL Transformation Dependency Map] ook openen. Voor informatie over de kaarten van de transformatiegebiedsafhankelijkheid, zie [Hulpmiddelen van de Configuratie van de Dataset](../../../home/c-dataset-const-proc/c-dataset-config-tools/c-dataset-config-tools.md#concept-6e058b7691834cf79dcfd1573f78d4f5).

1. Bewerk de parameters in het configuratiebestand met de volgende tabel als richtlijn.

   Wanneer u het [!DNL Log Processing.cfg]-bestand bewerkt in een werkbankvenster, kunt u sneltoetsen gebruiken voor elementaire bewerkingsfuncties, zoals cut ( Ctrl+x ), copy ( Ctrl+c), paste ( Ctrl+v ), ongedaan maken ( Ctrl+z ), opnieuw uitvoeren ( Ctrl+Shift+z ), sectie selecteren (klikken+slepen) en alles selecteren ( Ctrl+a ). U kunt de kortere weg ook gebruiken om tekst van één configuratiedossier ( [!DNL .cfg]) aan een ander te kopiëren en te kleven.

   >[!NOTE]
   >
   >Een [!DNL Log Processing Dataset Include]-bestand voor een overgeërfd profiel bevat een subset van de parameters die in de volgende tabel worden beschreven en enkele aanvullende parameters. Zie [Gegevensset met include-bestanden](../../../home/c-dataset-const-proc/c-dataset-inc-files/c-abt-dataset-inc-files.md).

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
      <td colname="col2"> <p>Optioneel. Gegevens filteren om logitems met tijdstempels tot en met deze tijd op te nemen. Adobe raadt u aan een van de volgende notaties te gebruiken: </p> 
      <ul id="ul_42613B1D2F3A4A6C9563BC9B54BE895E"> 
      <li id="li_BC6E5FC5CA204D89936845BE05DFE6E6">1 januari 2013 HH:MM:SS EDT </li> 
      <li id="li_18FE1B0417AF4207B02497664F47D23F">1 januari 2013 UU:MM:SS GMT </li> 
      </ul> <p>Als u bijvoorbeeld 29 juli 2013 00:00:00 EDT opgeeft als eindtijd, worden gegevens opgenomen tot en met 28 juli 2013, om 21:59:59 uur EDT. Zie <a href="../../../home/c-dataset-const-proc/c-log-proc-config-file/c-info-log-proc-param.md#concept-41bd49bf6b64442d91c232ec67529a3d"> Gegevensfilters </a>. </p> <p>U moet een tijdzone opgeven. De tijdzone is niet standaard ingesteld op GMT als deze niet is opgegeven. Zie <a href="../../../home/c-dataset-const-proc/c-time-zone.md#concept-9b540ec3e770490d94e9d5a985765477"> Tijdzonecodes </a> voor een lijst met afkortingen voor tijdzones die worden ondersteund door de gegevensworkbench-server. </p> <p> <p>Opmerking:  De parameter Start/End Times gebruiken voor <span class="wintitle"> Sensor </span>, logbestand en XML-bronnen is gerelateerd aan deze parameter. Zie de secties van <a href="../../../home/c-dataset-const-proc/c-log-proc-config-file/c-log-sources.md#concept-6714c720fac044cbb9af003bf401b2ea"> de Bronnen van het Logboek </a> die deze brontypes bespreken. </p> </p> </td> 
   </tr> 
   <tr> 
      <td colname="col1"> Velden </td> 
      <td colname="col2"> Optioneel. Adobe raadt aan <span class="wintitle"> velden </span> te definiëren in een of meer <span class="wintitle"> Gegevensset voor logverwerking Inclusief </span> bestanden. Zie <a href="../../../home/c-dataset-const-proc/c-dataset-inc-files/c-types-dataset-inc-files/c-log-proc-dataset-inc-files/c-log-proc-dataset-inc-files.md#concept-999475a22519432e98844622ca95b6ab"> Gegevensset logverwerking bevat bestanden </a>. </td> 
   </tr> 
   <tr> 
      <td colname="col1"> Maximaal aantal sleutelbytes groeperen </td> 
      <td colname="col2"> <p>Maximale hoeveelheid gebeurtenisgegevens die de server kan verwerken voor één enkele volgende-id. Gegevens die deze limiet overschrijden, worden gefilterd uit het constructieproces van de gegevensset. Deze waarde moet op 2e6 worden ingesteld wanneer de sleutelsplitsing actief is en op 1e6 wanneer de sleutelsplitsing niet actief is. Zie <a href="../../../home/c-dataset-const-proc/c-log-proc-config-file/c-info-log-proc-param.md#concept-64b416bbe42f4d689f90df246f7f7caf"> Sleutelsplitsing </a>. </p> <p> <p>Opmerking:  Wijzig deze waarde niet zonder Adobe te raadplegen. </p> </p> </td> 
   </tr> 
   <tr> 
      <td colname="col1"> Hash-drempel </td> 
      <td colname="col2"> <p>Optioneel. Een bemonsteringsfactor voor willekeurige subsampling van rijen. Als geplaatst aan een aantal n, dan slechts één van elke n het volgen IDs de dataset ingaat, die het totale aantal rijen in de dataset met een factor van n vermindert. </p> <p>Om een dataset tot stand te brengen die 100 percentennauwkeurigheid (namelijk om alle rijen te omvatten) vereist, zou u de Drempel van de Hash aan 1 plaatsen. </p> <p>Waarden: </p> <span class="filepath"> Hash-drempel = 1  </span> (100 procent van de gegevens inclusief alle rijen.) <p> <span class="filepath"> Hash Threshold = 2  </span> (1/2 van gegevens en bevat de helft van de rijen.) </p> <p> <span class="filepath"> Hash Threshold = 3  </span>(1/3 van gegevens en omvat één van drie rijen, maar aan 34% in de Voltooiing van de Vraag) </p> <p> <span class="filepath"> Hash Threshold = 4  </span>(1/4e van gegevens en bevat één op de vier rijen.) </p> <p> </p> <p> <p>Opmerking:  Het gebruiken van een <span class="filepath"> Drempel van de Hash = 8 </span> verstrekt 1/8e van de gegevens, die 12.5% is. De <span class="uicontrol">-waarde voor Voltooiing query </span> in de ronden is echter 13% voor deze waarde. De extra voorbeelden omvatten een <span class="filepath"> Drempel van de Hash = 6 </span> die in 17% vraagresolutie resulteert. Een <span class="filepath"> Hashdrempel = 13 </span>resulteert in 8% queryresolutie. </p> </p> <p>Als <span class="wintitle"> Hash Threshold </span> is opgegeven in zowel de <span class="filepath"> Log Processing.cfg </span>- als <span class="filepath"> Transformation.cfg </span>-bestanden, wordt deze niet achtereenvolgens toegepast. de maximumwaarde die in een van beide configuratiebestanden is ingesteld, is van toepassing. Zie <a href="../../../home/c-dataset-const-proc/c-log-proc-config-file/c-info-log-proc-param.md#concept-41bd49bf6b64442d91c232ec67529a3d"> Gegevensfilters </a>. </p> </td> 
   </tr> 
   <tr> 
      <td colname="col1"> Voorwaarde logbestandvermelding </td> 
      <td colname="col2"> Optioneel. Bepaalt de regels waardoor de logboekingangen voor opneming in de dataset worden overwogen. Zie <a href="../../../home/c-dataset-const-proc/c-log-proc-config-file/c-info-log-proc-param.md#concept-ecaff95cee4e40bc90f81e099c5fc934"> Log Entry Condition </a>. </td> 
   </tr> 
   <tr> 
      <td colname="col1"> Opnieuw verwerken </td> 
      <td colname="col2"> <p>Optioneel. Elk teken of elke combinatie van tekens kan hier worden ingevoerd. Als u deze parameter wijzigt en het bestand opslaat op de computer van de gegevenswerkbank, worden de gegevens opnieuw verwerkt. </p> <p>Zie <a href="../../../home/c-dataset-const-proc/c-reproc-retrans/c-unst-reproc-retrans.md"> Reprocessing and Retransformation </a>. </p> </td> 
   </tr> 
   <tr> 
      <td colname="col1"> Emmertje splitsen </td> 
      <td colname="col2"> <p>Parameter betrokken bij sleutelsplitsing. De waarde hiervan moet 6e6 zijn wanneer de sleutelsplitsing actief is. Zie <a href="/help/home/c-dataset-const-proc/c-log-proc-config-file/c-info-log-proc-param.md#key-split"> Sleutelsplitsing </a>. </p> <p> <p>Opmerking:  Wijzig deze waarde niet zonder Adobe te raadplegen. </p> </p> </td> 
   </tr> 
   <tr> 
      <td colname="col1"> Sleutelbytes splitsen </td> 
      <td colname="col2"> <p>Parameter betrokken bij sleutelsplitsing. De waarde hiervan moet 1e6 zijn wanneer de sleutelsplitsing actief is en 0 wanneer de sleutelsplitsing niet actief is. Zie <a href="../../../home/c-dataset-const-proc/c-log-proc-config-file/c-info-log-proc-param.md#concept-64b416bbe42f4d689f90df246f7f7caf"> Sleutelsplitsing </a>. </p> <p> <p>Opmerking:  Wijzig deze waarde niet zonder Adobe te raadplegen. </p> </p> </td> 
   </tr> 
   <tr> 
      <td colname="col1"> Splitsen van keyspatie </td> 
      <td colname="col2"> <p>Parameter betrokken bij sleutelsplitsing. De waarde hiervan moet 10 zijn wanneer de sleutelsplitsing actief is. Zie <a href="../../../home/c-dataset-const-proc/c-log-proc-config-file/c-info-log-proc-param.md#concept-64b416bbe42f4d689f90df246f7f7caf"> Sleutelsplitsing </a>. </p> <p> <p>Opmerking:  Wijzig deze waarde niet zonder Adobe te raadplegen. </p> </p> </td> 
   </tr> 
   <tr> 
      <td colname="col1"> Staven </td> 
      <td colname="col2"> <p>Optioneel. De namen van de verwerkingsstadia die in <span class="wintitle"> Dataset van de Dataset van de Verwerking van het Logboek kunnen worden gebruikt omvatten </span> dossiers. Met verwerkingsstadia kunt u de transformaties ordenen die zijn gedefinieerd in <span class="wintitle"> Gegevensset voor logverwerking Inclusief </span>-bestanden. Deze parameter is zeer nuttig als u een of meer transformaties binnen veelvoudige <span class="wintitle"> Dataset van de Dataset van de Verwerking van het Logboek omvat </span> dossiers en u specifieke transformaties op specifieke punten tijdens logboekverwerking wilt uitvoeren. </p> <p>De volgorde waarin u de stappen hier weergeeft, bepaalt de volgorde waarin de transformaties in de <span class="wintitle"> Gegevensset van logverwerking Inclusief </span>-bestanden worden uitgevoerd tijdens de logverwerking. Voorbewerking en nabewerking zijn ingebouwde stappen. Voorbewerken is altijd de eerste fase en nabewerking is altijd de laatste fase. Standaard wordt een werkgebied met de naam Standaard gebruikt. </p> <p> <b>Een nieuw verwerkingsstadium toevoegen</b> 
      <ul id="ul_3A49BEAD1C134344999FED379B8CE7A3"> 
         <li id="li_AFC9B2529EC64642AFF98E9D5BA88C71">Klik in het venster <span class="filepath"> Log Processing.cfg </span> met de rechtermuisknop <span class="uicontrol"> Stage </span> en klik <span class="uicontrol"> Add New </span> &gt; <span class="uicontrol"> Stage </span>. </li> 
         <li id="li_5731B836658D4E1DB721C57C6275369A">Voer een naam in voor het nieuwe werkgebied. </li> 
      </ul> </p> <p> <b>Een bestaand verwerkingsstadium verwijderen</b> 
      <ul id="ul_BBF4F710A5624C578F1F2A38FE18E9AD"> 
         <li id="li_CF6982C752DE41FFA97759C30CDE6AA0">Klik met de rechtermuisknop op het nummer dat overeenkomt met het werkgebied dat u wilt verwijderen en klik op <span class="uicontrol"> </span><i>&lt; <span class="uicontrol"> #stage_number </span></i>. </li> 
      </ul> </p> <p> <p>Opmerking:  Wanneer u een <span class="wintitle"> werkgebied </span> opgeeft in een <span class="wintitle"> Gegevensset voor logverwerking Inclusief </span> bestanden, moet de naam van het werkgebied exact overeenkomen met de naam die u hier invoert. Zie <a href="../../../home/c-dataset-const-proc/c-dataset-inc-files/c-abt-dataset-inc-files.md"> Gegevensset Inclusief bestanden </a>. </p> </p> </td> 
   </tr> 
   <tr> 
      <td colname="col1"> Begintijd </td> 
      <td colname="col2"> <p>Optioneel. Gegevens filteren om logitems met tijdstempels op of na dit tijdstip op te nemen. Adobe raadt u aan een van de volgende notaties te gebruiken: </p> <p> 
      <ul id="ul_0774889E22C24A6592809D289D1CBEC5"> 
         <li id="li_CE23541D8B584EA1AC432C5098564E46"> 1 januari 2013 HH:MM:SS EDT </li> 
         <li id="li_2EB0CF60CF12444BB744E52E9C919152"> 1 januari 2013 UU:MM:SS GMT </li> 
      </ul> </p> <p> Als u bijvoorbeeld "29 juli 2013 00:00:00 EDT" opgeeft als begintijd, worden vanaf 29 juli 2013 om 12:00:00 EDT gegevens opgenomen. Zie <a href="../../../home/c-dataset-const-proc/c-log-proc-config-file/c-info-log-proc-param.md#concept-41bd49bf6b64442d91c232ec67529a3d"> Gegevensfilters </a>. </p> <p> U moet een tijdzone opgeven. De tijdzone is niet standaard ingesteld op GMT als deze niet is opgegeven. Zie <a href="../../../home/c-dataset-const-proc/c-time-zone.md#concept-9b540ec3e770490d94e9d5a985765477"> Tijdzonecodes </a> voor een lijst met afkortingen voor tijdzones die worden ondersteund door de gegevensworkbench-server. </p> <p> <p>Opmerking:  De parameter Start/End Times gebruiken voor <span class="wintitle"> Sensor </span>, logbestand en XML-bronnen is gerelateerd aan deze parameter. Zie de secties van <a href="../../../home/c-dataset-const-proc/c-log-proc-config-file/c-log-sources.md#concept-6714c720fac044cbb9af003bf401b2ea"> de Bronnen van het Logboek </a> die deze brontypes bespreken. </p> </p> </td> 
   </tr> 
   <tr> 
      <td colname="col1"> Tijdzone </td> 
      <td colname="col2"> <p>Optioneel. Tijdzone van de server van de gegevenswerkbank die voor tijdomzettingen (zoals de omzetting die door het x-lokaal-timekoordgebied wordt vertegenwoordigd) tijdens logboekverwerking wordt gebruikt. </p> <p> <p>Opmerking:  U moet de Zone van de Tijd specificeren als u tot het omgezette tijdgebied tijdens de fase van de logboekverwerking van datasetconstructie wilt toegang hebben. Anders registreert de server van de gegevenswerkbank een fout in de gebeurtenislogboeken. </p> </p> <p>Zie <a href="../../../home/c-dataset-const-proc/c-trans-config-file/c-spec-trans-param/c-time-zones.md#concept-9cf16b1cb4874f7d85e1dd950fdb4956"> Tijdzones </a>. </p> </td> 
   </tr> 
   <tr> 
      <td colname="col1"> Transformaties </td> 
      <td colname="col2"> Optioneel. Adobe raadt aan transformaties te definiëren voor logverwerking in een of meer <span class="wintitle"> Gegevensset voor logverwerking Inclusief </span> bestanden. Zie <a href="../../../home/c-dataset-const-proc/c-dataset-inc-files/c-types-dataset-inc-files/c-log-proc-dataset-inc-files/c-log-proc-dataset-inc-files.md#concept-999475a22519432e98844622ca95b6ab"> Gegevensset logverwerking bevat bestanden </a>. </td> 
   </tr> 
   </tbody> 
   </table>

1. Klik met de rechtermuisknop **[!UICONTROL (modified)]** boven in het venster en klik **[!UICONTROL Save]**.
1. Klik in [!DNL Profile Manager] met de rechtermuisknop op het vinkje voor [!DNL Log Processing.cfg]in de kolom [!DNL User] en klik vervolgens op **[!UICONTROL Save to]** > *&lt;**[!UICONTROL dataset profile name]**>* om de lokaal aangebrachte wijzigingen van kracht te laten worden. Het opnieuw verwerken van de gegevens begint na synchronisatie van het gegevenssetprofiel.

   >[!NOTE]
   >
   >Sla het gewijzigde configuratiebestand niet op in een van de interne profielen die door Adobe worden geleverd, omdat de wijzigingen worden overschreven wanneer u updates voor deze profielen installeert.

   Zie [Opwerking en hertransformatie](../../../home/c-dataset-const-proc/c-reproc-retrans/c-unst-reproc-retrans.md) voor meer informatie over het opnieuw verwerken van uw gegevens.
