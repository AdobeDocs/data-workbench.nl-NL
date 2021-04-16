---
description: Stappen voor het bewerken van het bestand Transformation.cfg voor een gegevenssetprofiel.
title: Het configuratiebestand voor transformatie bewerken
uuid: 77b9e566-4a9a-4ea1-b5ab-63a4574c0fdb
exl-id: 3fab17a4-d356-4548-b977-f5d409870753
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '1135'
ht-degree: 0%

---

# Het dossier van de Configuratie van de Transformatie{#editing-the-transformation-configuration-file} uitgeven

Stappen voor het bewerken van het bestand Transformation.cfg voor een gegevenssetprofiel.

1. Terwijl het werken in uw datasetprofiel, open [!DNL Profile Manager] en klik **[!UICONTROL Dataset]** om zijn inhoud te tonen.

   Voor informatie over het openen en het werken met [!DNL Profile Manager], zie *de Gids van de Gebruiker van de Data Workbench*.

   >[!NOTE]
   >
   >Er kan een submap Transformation bestaan in de map Dataset. Deze submap bevat de [!DNL Transformation Dataset Include] bestanden die zijn gemaakt voor een of meer overgeërfde profielen. Voor informatie over [!DNL Transformation Dataset Include] dossiers, zie [Dataset omvat Dossiers](../../../home/c-dataset-const-proc/c-dataset-inc-files/c-abt-dataset-inc-files.md).

1. Klik met de rechtermuisknop op het vinkje naast [!DNL Transformation.cfg] en klik **[!UICONTROL Make Local]**. Er wordt een vinkje voor dit bestand weergegeven in de kolom [!DNL User].
1. Klik met de rechtermuisknop op het nieuwe vinkje en klik op **[!UICONTROL Open]** > **[!UICONTROL in Workstation]**. Het venster [!DNL Transformation.cfg] verschijnt.

   U kunt het [!DNL Transformation.cfg] dossier van [!DNL Transformation Dependency Map] ook openen. Voor informatie over [!DNL transformation dependency maps], zie [Hulpmiddelen van de Configuratie van de Dataset](../../../home/c-dataset-const-proc/c-dataset-config-tools/c-dataset-config-tools.md#concept-6e058b7691834cf79dcfd1573f78d4f5).

1. Bewerk de parameters in het configuratiebestand met de volgende tabel als richtlijn.

   Wanneer u het [!DNL Transformation.cfg]-bestand bewerkt in een werkbankvenster, kunt u sneltoetsen gebruiken voor elementaire bewerkingsfuncties, zoals cut (Ctrl+x), copy (Ctrl+c), paste (Ctrl+v), ongedaan maken (Ctrl+z), opnieuw uitvoeren (Ctrl+Shift+z), sectie selecteren (klikken+slepen) en alles selecteren (Ctrl+a). Bovendien kunt u de kortere weg gebruiken om tekst van één configuratiedossier ( [!DNL .cfg]) aan een ander te kopiëren en te kleven.

   >[!NOTE]
   >
   >Een [!DNL Transformation Dataset Include]-bestand voor een overgeërfd profiel bevat een subset van de parameters die in de volgende tabel worden beschreven en enkele aanvullende parameters. Voor informatie over [!DNL Transformation Dataset Include] dossiers, zie [Dataset omvat Dossiers](../../../home/c-dataset-const-proc/c-dataset-inc-files/c-abt-dataset-inc-files.md)

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
      <td colname="col2"> <p>Optioneel. Gegevens filteren om logitems met tijdstempels tot aan, maar niet inclusief, deze keer op te nemen. Adobe raadt u aan een van de volgende notaties te gebruiken: 
      <ul id="ul_1EC55DA4936946C98E447E1476E8280F"> 
       <li id="li_F2D862833F4B451C965E1ED6C05DCE1B"> 1 januari 2013 HH:MM:SS EDT </li> 
       <li id="li_EB7FFEB2E2C24EAFB8E4B14F2479DA3D"> 1 januari 2013 UU:MM:SS GMT </li> 
      </ul> </p> <p> Als u bijvoorbeeld "29 juli 2013 00:00:00 EDT" opgeeft als eindtijd, worden gegevens opgenomen tot en met 28 juli 2013, om 21:59:59 uur EDT. </p> <p> U moet een tijdzone opgeven. De tijdzone is niet standaard ingesteld op GMT als deze niet is opgegeven. Zie <a href="../../../home/c-dataset-const-proc/c-time-zone.md#concept-9b540ec3e770490d94e9d5a985765477"> Tijdzonecodes </a> voor een lijst met afkortingen voor tijdzones die worden ondersteund door de gegevensworkbench-server. </p> <p> <p>Opmerking:  Als u een waarde voor EindTijd specificeert, wordt een parameter genoemd EindTijd geplaatst en toegepast door de transformatiefase van datasetconstructie. Zie <a href="../../../home/c-dataset-const-proc/c-dataset-inc-files/c-def-param-dataset-inc-files/c-def-param-dataset-inc-files.md#concept-5ad06acc8dc44bf2a99643fafdd56b50"> Parameters definiëren in Dataset Inclusief bestanden </a> voor informatie over parameters. </p> </p> </td> 
   </tr> 
   <tr> 
      <td colname="col1"> Uitgebreide Dimension </td> 
      <td colname="col2"> Optioneel. Adobe raadt aan uitgebreide afmetingen te definiëren in een of meer <span class="wintitle">-gegevensset voor transformatie. Neem </span>-bestanden op. Zie <a href="../../../home/c-dataset-const-proc/c-dataset-inc-files/c-types-dataset-inc-files/c-trans-dataset-inc-files.md#concept-c64aa78ed9ce40b8a0f4932c82ff5ace"> Gegevensset transformatie Inclusief bestanden </a> voor meer informatie. </td> 
   </tr> 
   <tr> 
      <td colname="col1"> Hash-drempel </td> 
      <td colname="col2"> <p>Optioneel. Een bemonsteringsfactor voor willekeurige subsampling van rijen. Als geplaatst aan een aantal n, dan slechts één van elke n het volgen IDs de dataset ingaat, die het totale aantal rijen in de dataset met een factor van n vermindert. Om een dataset tot stand te brengen die 100 percentennauwkeurigheid (namelijk om alle rijen te omvatten) vereist, zou u de Drempel van de Hash aan 1 plaatsen. </p> <p> Als de Drempel van de Hash in zowel <span class="filepath"> Logverwerking.cfg </span> als <span class="filepath"> Transformation.cfg </span> dossiers wordt gespecificeerd, wordt het niet opeenvolgend toegepast; het maximum van de waarden die in één van beide configuratiedossier worden geplaatst is van toepassing. </p> </td> 
   </tr> 
   <tr> 
      <td colname="col1"> Voorwaarde logbestandvermelding </td> 
      <td colname="col2"> Optioneel. Bepaalt de regels waardoor de logboekingangen output van logboekverwerking voor opneming in het datasetprofiel worden overwogen. Zie <a href="../../../home/c-dataset-const-proc/c-log-proc-config-file/c-info-log-proc-param.md#concept-ecaff95cee4e40bc90f81e099c5fc934"> Log Entry Condition </a>. </td> 
   </tr> 
   <tr> 
      <td colname="col1"> Nieuwe voorwaarde bezoeker </td> 
      <td colname="col2"> Optioneel. Voor gebruik met webgegevens. Definieert de regels volgens welke bezoekers worden overwogen om in de gegevens op te nemen. De <span class="wintitle"> Nieuwe voorwaarde van de Bezoeker </span> bepaalt de eerste logboekingang voor een bezoeker (die door tijd wordt bevolen) die in de dataset moet worden gebruikt. Alle volgende logingangen voor deze bezoeker zijn inbegrepen in de dataset ongeacht of zij aan deze voorwaarde voldoen. Zie <a href="../../../home/c-dataset-const-proc/c-trans-config-file/c-spec-trans-param/c-new-vstr-con.md#concept-1d0d8e26718447ad9d235e00b33a36f3"> Nieuwe bezoekersvoorwaarde </a>. </td> 
   </tr> 
   <tr> 
      <td colname="col1"> Opnieuw verwerken </td> 
      <td colname="col2"> <p>Optioneel. Elk teken of elke combinatie van tekens kan hier worden ingevoerd. Als u deze parameter wijzigt en het bestand opslaat, worden de gegevens opnieuw getransformeerd. </p> <p> Zie <a href="../../../home/c-dataset-const-proc/c-reproc-retrans/c-unst-reproc-retrans.md"> Opwerking en hertransformatie </a> voor informatie over het opnieuw verwerken van uw gegevens. </p> </td> 
   </tr> 
   <tr> 
      <td colname="col1"> Schemacontrole </td> 
      <td colname="col2"> Waar of onwaar. Als waar, dan identificeert de server van de gegevenswerkbank de problemen van de gegevenssetcorruptie en registreert informatie over de problemen in logboekdossiers in de folder van het Spoor van de server van de server van de werkbank van gegevens. De standaardwaarde is true. Adobe raadt u aan deze parameter altijd op true in te stellen. </td> 
   </tr> 
   <tr> 
      <td colname="col1"> Staven </td> 
      <td colname="col2"> <p>Optioneel. De namen van de verwerkingsstadia die in <span class="wintitle"> Dataset van de Transformatie kunnen worden gebruikt omvatten </span> dossiers. Met verwerkingsstadia kunt u de transformaties die zijn gedefinieerd in <span class="wintitle"> Gegevensset transformatie Inclusief </span>-bestanden, ordenen. Deze parameter is zeer nuttig als u een of meer transformaties binnen veelvoudige <span class="wintitle"> Dataset van de Transformatie omvat </span> dossiers en u specifieke transformaties op specifieke punten tijdens transformatie wilt worden uitgevoerd. </p> <p> De volgorde waarin u de fasen hier opsomt, bepaalt de volgorde waarin de transformaties in de Dataset <span class="wintitle"> Transformatie Inclusief </span>-bestanden worden uitgevoerd tijdens de transformatie. <span class="wintitle"> Voorbewerking  </span> en  <span class="wintitle"> nabewerking  </span> zijn ingebouwde stappen;  <span class="wintitle"> Voorbewerken  </span> is altijd de eerste fase en  <span class="wintitle"> nabewerking  </span> is altijd de laatste fase. Standaard wordt een werkgebied met de naam <span class="wintitle"> Standaard </span> genoemd. </p> <p> <b>Een nieuw verwerkingsstadium toevoegen</b> </p> <p> 
      <ul id="ul_6AF2EF72CEE34FA88575C46FA333BDA1"> 
       <li id="li_80627E7A89CE4E57A4228C4F5496533F"> Klik in het venster <span class="filepath"> Transformation.cfg </span> met de rechtermuisknop <span class="uicontrol"> Stage </span> en klik <span class="uicontrol"> Add New </span> &gt; <span class="uicontrol"> Stage </span>. </li> 
       <li id="li_321BEDB1E95F4AA4B282EED32A4CA196"> Voer een naam in voor het nieuwe werkgebied. </li> 
      </ul> </p> <p> <b>Een bestaand verwerkingsstadium verwijderen</b> </p> <p> 
      <ul id="ul_2EFA5A40982A48919E9946BF1955110A"> 
       <li id="li_3B3829DA34FD4774B3F9F94074099794"> Klik met de rechtermuisknop op het nummer dat overeenkomt met het werkgebied dat u wilt verwijderen en klik op <span class="uicontrol"> </span><i>&lt; <span class="uicontrol"> #stage_number </span></i>. </li> 
      </ul> </p> <p> <p>Opmerking:  Wanneer u een werkgebied opgeeft in een <span class="wintitle"> Dataset voor transformatie Inclusief </span>-bestanden, moet de naam van het werkgebied exact overeenkomen met de naam die u hier invoert. Voor meer informatie over dataset omvat dossiers, zie <a href="../../../home/c-dataset-const-proc/c-dataset-inc-files/c-abt-dataset-inc-files.md"> Dataset omvat Dossiers </a>. </p> </p> </td> 
   </tr> 
   <tr> 
      <td colname="col1"> Begintijd </td> 
      <td colname="col2"> <p>Optioneel. Gegevens filteren om logitems met tijdstempels op of na dit tijdstip op te nemen. Adobe raadt u aan een van de volgende notaties te gebruiken: 
      <ul id="ul_6BC86CCB1FC447ACAC4045E08C8EF8F8"> 
       <li id="li_2151B3F7FAD54F38B6C33E25CDCACBBE"> 1 januari 2013 HH:MM:SS EDT </li> 
       <li id="li_CA1BB675C1244104915FB9ED96A3013D"> 1 januari 2013 UU:MM:SS GMT </li> 
      </ul> </p> <p> Als u bijvoorbeeld 29 juli 2013 00:00:00 EDT opgeeft als <span class="wintitle"> Begintijd </span>, worden gegevens opgenomen die op 29 juli 2013 om 12:00:00 uur EDT beginnen. </p> <p> U moet een tijdzone opgeven. De tijdzone is niet standaard ingesteld op GMT als deze niet is opgegeven. Zie <a href="../../../home/c-dataset-const-proc/c-time-zone.md#concept-9b540ec3e770490d94e9d5a985765477"> Tijdzonecodes </a> voor een lijst met afkortingen voor tijdzones die worden ondersteund door Data Workbench Server. </p> <p> <p>Opmerking:  Als u een waarde voor de Tijd van het Begin specificeert, wordt een parameter genoemd de Tijd van het Begin geplaatst en toegepast door de transformatiefase van datasetconstructie. Zie <a href="../../../home/c-dataset-const-proc/c-dataset-inc-files/c-def-param-dataset-inc-files/c-def-param-dataset-inc-files.md#concept-5ad06acc8dc44bf2a99643fafdd56b50"> Parameters definiëren in Dataset Inclusief bestanden </a> voor informatie over parameters. </p> </p> </td> 
   </tr> 
   <tr> 
      <td colname="col1"> Transformaties </td> 
      <td colname="col2"> Optioneel. Adobe raadt aan transformaties te definiëren voor de transformatiefase van de constructie van gegevenssets in een of meer <span class="wintitle">-gegevensset voor transformatie Inclusief </span> bestanden. Zie <a href="../../../home/c-dataset-const-proc/c-dataset-inc-files/c-types-dataset-inc-files/c-trans-dataset-inc-files.md#concept-c64aa78ed9ce40b8a0f4932c82ff5ace"> Gegevensset transformatie Inclusief bestanden </a> voor meer informatie. </td> 
   </tr> 
   <tr> 
      <td colname="col1"> Tijdzone </td> 
      <td colname="col2"> <p>Tijdzone van het gegevenssetprofiel. Tijdzones worden gebruikt voor tijdconversies en voor het maken van tijddimensies. Zie <a href="../../../home/c-dataset-const-proc/c-trans-config-file/c-spec-trans-param/c-time-zones.md#concept-9cf16b1cb4874f7d85e1dd950fdb4956"> Tijdzones </a>. </p> <p> <p>Opmerking:  Wanneer gedefinieerd in het <span class="filepath"> Logbestand Processing.cfg </span>, wordt de parameter Tijdzone alleen gebruikt voor tijdconversies. </p> </p> </td> 
   </tr> 
   </tbody> 
   </table>

1. Klik met de rechtermuisknop **[!UICONTROL (modified)]** boven in het venster en klik **[!UICONTROL Save]**.
1. Klik in [!DNL Profile Manager] met de rechtermuisknop op het vinkje voor [!DNL Transformation.cfg]in de kolom [!DNL User] en klik vervolgens op **[!UICONTROL Save to]** > * **[!UICONTROL dataset profile name]** om de lokaal aangebrachte wijzigingen van kracht te laten worden. De gegevens worden opnieuw getransformeerd nadat het gegevenssetprofiel is gesynchroniseerd.

   >[!NOTE]
   >
   >Sla het gewijzigde configuratiebestand niet op in een van de interne profielen die door Adobe worden geleverd, omdat de wijzigingen worden overschreven wanneer u updates voor deze profielen installeert.

   Zie [Opwerking en hertransformatie](../../../home/c-dataset-const-proc/c-reproc-retrans/c-unst-reproc-retrans.md) voor informatie over het opnieuw verwerken of opnieuw transformeren van uw gegevens.
