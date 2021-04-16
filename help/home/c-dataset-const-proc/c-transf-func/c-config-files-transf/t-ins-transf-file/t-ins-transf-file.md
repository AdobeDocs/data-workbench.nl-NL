---
description: Het bestand data workbenchTransform.cfg bevat de parameters die de logbronnen, gegevenstransformaties en exportfuncties definiëren.
title: Het bestand Transform.cfg
uuid: eab5bb70-6de7-4f08-85db-a6cb00abd3ed
exl-id: e84f2536-cb22-4c47-a7a8-270b3c37ece6
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '1336'
ht-degree: 0%

---

# Het bestand Transform.cfg{#the-transform-cfg-file}

Het bestand data workbenchTransform.cfg bevat de parameters die de logbronnen, gegevenstransformaties en exportfuncties definiëren.

De transformaties die u definieert, manipuleren onbewerkte gegevens die zijn verzameld door sensoren ( [!DNL .vsl] bestanden) of die zich bevinden in tekstbestanden, XML-bestanden of ODBC-compatibele databases en voeren deze uit in bestaande velden, overschrijven de huidige gegevens of in nieuw gedefinieerde velden.

Als u transformatiefunctionaliteit wilt configureren, bewerkt u het bestand data workbench [!DNL Transform.cfg] in de map Dataset voor het profiel waarvoor u gebeurtenisgegevens wilt exporteren. Dit profiel is doorgaans toegewezen aan transformatiefunctionaliteit (u voert dus geen andere gegevensverwerking uit dan wat is gedefinieerd in de gegevenswerkbank [!DNL Transform.cfg]-bestand). Het is belangrijk om op te merken dat alle verwerkingsinstructies die in de [!DNL Log Processing Dataset Include]-bestanden voor overerfde profielen zijn opgegeven, worden toegepast naast de instructies in het bestand [!DNL Transform.cfg] op de werkbank.

Voor informatie over dataset omvat dossiers, zie [Dataset omvat Dossiers](../../../../../home/c-dataset-const-proc/c-dataset-inc-files/c-abt-dataset-inc-files.md).

Als de gegevens die u wilt exporteren door een servercluster van een gegevenswerkbank worden verwerkt, verwerkt elk van de verwerkingsservers (DPU&#39;s) in de cluster de gegevens, maar alleen de eerste DPU (verwerkingsserver nr. 0 in het bestand [!DNL profile.cfg]) schrijft de uitvoergegevens naar het lokale bestandssysteem.

**Het bestand Transform.cfg op de werkbank Gegevens bewerken**

1. Wanneer u werkt in het profiel waarvoor u gegevens wilt exporteren, opent u [!DNL Profile Manager] en klikt u **[!UICONTROL Dataset]** om de inhoud van de map weer te geven.
1. Klik met de rechtermuisknop op het vinkje naast de gegevenswerkbank [!DNL Transform.cfg] en klik vervolgens op **[!UICONTROL Make Local]**. Er wordt een vinkje voor dit bestand weergegeven in de kolom [!DNL User].
1. Klik met de rechtermuisknop op het nieuwe vinkje en klik op **[!UICONTROL Open]** > **[!UICONTROL from the workbench]**. Het venster Data Workbench [!DNL Transform.cfg] wordt weergegeven.
1. Bewerk de parameters in het configuratiebestand met de onderstaande tabel als richtlijn:

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
    <td colname="col2"> <p>Optioneel. Gegevens filteren om logitems met tijdstempels tot aan, maar niet inclusief, deze keer op te nemen. Adobe raadt u aan een van de volgende notaties te gebruiken: 
      <ul id="ul_C8C7F0F631594F7095CB83EF54E7CD0E"> 
       <li id="li_77AB6EEE8EEC4698AA886DE8BB0E2783"> 1 januari 2013HH:MM:SS EDT </li> 
       <li id="li_33806070F991476BB986906876CAF7F1"> 1 januari 2013 UU:MM:SS GMT </li> 
      </ul> </p> <p> Als u bijvoorbeeld 29 juli 2013 00:00:00 EDT opgeeft als <span class="wintitle"> Eindtijd </span> bevat dit gegevens tot 28 juli 2013, om 21:59:59 PM EDT. </p> <p> U moet een tijdzone opgeven. De tijdzone is niet standaard ingesteld op GMT als deze niet is opgegeven. Zie <a href="../../../../../home/c-dataset-const-proc/c-time-zone.md#concept-9b540ec3e770490d94e9d5a985765477"> Tijdzonecodes </a> voor een lijst met afkortingen voor tijdzones die worden ondersteund door de gegevensworkbench-server. </p> <p> De parameter Start/End Times gebruiken voor Sensor- en logbestandsbronnen is gerelateerd aan deze parameter. </p> </td> 
    </tr> 
    <tr> 
    <td colname="col1"> Exporteurs </td> 
    <td colname="col2"> <p>De subvelden van een exporter geven aan hoe de uitvoergegevens worden verwerkt en/of opgemaakt. U kunt meerdere exportfuncties definiëren voor een set logbronnen. Elk type exporter maakt uitvoer onafhankelijk van elkaar. </p> <p> Er zijn drie soorten exporteurs: 
      <ul id="ul_C3C39F6DF3DC4F4CA2161EDB69599642"> 
       <li id="li_635FB271D0544D52B1C31740442D2E08"> ExportTextFile </li> 
       <li id="li_D496194848B44823A58890E03FFDD18E"> ExportDelimitedTextFile </li> 
       <li id="li_AEE9AA87076141FC91330D3FCFAB2101"> ExportVSLFile </li> 
      </ul> </p> <p> Zie <a href="../../../../../home/c-dataset-const-proc/c-transf-func/c-config-files-transf/t-ins-transf-file/t-def-exp.md#task-900c40d1914347f288587bf0ca394ff2"> Exporters definiëren </a> voor meer informatie over exporttypen. </p> </td> 
    </tr> 
    <tr> 
    <td colname="col1"> Hash-drempel </td> 
    <td colname="col2"> Optioneel. Een bemonsteringsfactor voor willekeurige subsampling van rijen. Als deze op een getal n is ingesteld, wordt slechts één van elke n-id geselecteerd voor exporteren, waardoor het totale aantal rijen dat met een factor n wordt geëxporteerd, wordt verminderd. Als u alle rijen wilt exporteren, stelt u Hash-drempel in op 1. </td> 
    </tr> 
    <tr> 
    <td colname="col1"> Voorwaarde logbestandvermelding </td> 
    <td colname="col2"> Optioneel. Bepaalt de regels waardoor de logboekingangen voor de uitvoer worden overwogen. Voor meer informatie over <span class="wintitle"> de Voorwaarde van de Ingang van het Logboek </span>, zie <a href="../../../../../home/c-dataset-const-proc/c-log-proc-config-file/c-abt-log-proc-config-file.md"> het Dossier van de Configuratie van de Verwerking van het Logboek </a>. </td> 
    </tr> 
    <tr> 
    <td colname="col1"> Logbronnen </td> 
    <td colname="col2"> <p>De gegevensbronnen. <span class="wintitle"> Logbronnen  </span> kunnen  <span class="filepath"> .vsl- </span> bestanden, logbestanden of XML-bestanden zijn of gegevens uit databases die compatibel zijn met ODBC. Voor informatie over <span class="wintitle"> logbronnen </span>, zie <a href="../../../../../home/c-dataset-const-proc/c-log-proc-config-file/c-abt-log-proc-config-file.md"> Logverwerkingsconfiguratiebestand </a>. </p> <p> <span class="wintitle"> Transform  </span> verwacht dat alle brongegevens in chronologische volgorde staan binnen lexicografisch geordende invoerbestanden. Als niet aan deze eis wordt voldaan, zijn de berekeningen Van onjuist, en de extra inputgegevens kunnen worden verwerkt nadat de outputdossiers worden gesloten. </p> </td> 
    </tr> 
    <tr> 
    <td colname="col1"> Offlinemodus </td> 
    <td colname="col2"> <p>Optioneel. Waar of onwaar. Indien waar (true), wordt bij het transformeren <span class="wintitle"> ervan uitgegaan dat alle invoerbestanden aanwezig zijn wanneer de gegevensverwerking wordt gestart. </span> Wanneer alle inputgegevens zijn gelezen, <span class="wintitle"> sluit de Transformatie </span> alle outputdossiers zonder het wachten op extra gegevens om worden ontvangen. De standaardwaarde is false. </p> <p> <p>Opmerking:  Als <span class="wintitle"> Offlinemodus </span> is ingesteld op true, verwacht <span class="wintitle"> Transformatie </span> dat alle brongegevens aanwezig zijn voordat de verwerking wordt gestart. Er wordt een waarschuwingsbericht gegenereerd in het <span class="filepath"> bestand VisualServer.log </span> als er aanvullende gegevens worden ontvangen nadat de uitvoerbestanden zijn gesloten. </p> </p> </td> 
    </tr> 
    <tr> 
    <td colname="col1"> Opnieuw verwerken </td> 
    <td colname="col2"> <p>Optioneel. Elk teken of elke combinatie van tekens kan hier worden ingevoerd. Als u deze parameter wijzigt en het bestand opslaat op de computer <span class="wintitle"> Transformeren </span>, worden de gegevens opnieuw verwerkt. </p> <p> Zie <a href="../../../../../home/c-dataset-const-proc/c-reproc-retrans/c-unst-reproc-retrans.md"> Opwerking en hertransformatie </a> voor informatie over het opnieuw verwerken van uw gegevens. </p> </td> 
    </tr> 
    <tr> 
    <td colname="col1"> Staven </td> 
    <td colname="col2"> <p>Optioneel. De namen van de verwerkingsstadia die in <span class="wintitle"> Dataset van de Verwerking van het Logboek kunnen worden gebruikt omvatten </span> dossiers die naast de gegevens werkbank <span class="filepath"> Transform.cfg </span> dossier worden uitgevoerd. Met verwerkingsstadia kunt u de transformaties ordenen die zijn gedefinieerd in <span class="wintitle"> Gegevensset voor logverwerking Inclusief </span>-bestanden. Deze parameter is zeer nuttig als u een of meer transformaties binnen veelvoudige <span class="wintitle"> Gegevensset van de Verwerking van het Logboek omvat </span> dossiers en u specifieke transformaties op specifieke punten tijdens het uitvoerproces wilt worden uitgevoerd. </p> <p> De volgorde waarin u de stappen hier weergeeft, bepaalt de volgorde waarin de transformaties in de <span class="wintitle"> Gegevensset van logverwerking Inclusief </span> bestanden worden uitgevoerd tijdens het exporteren van gegevens. <span class="wintitle"> Voorbewerking  </span> en  <span class="wintitle"> nabewerking  </span> zijn ingebouwde stappen;  <span class="wintitle"> Voorbewerken  </span> is altijd de eerste fase en  <span class="wintitle"> nabewerking  </span> is altijd de laatste fase. Standaard wordt een werkgebied met de naam <span class="wintitle"> Standaard </span> genoemd. </p> <p> <b>Een nieuw verwerkingsstadium toevoegen</b> </p> 
      <ul id="ul_869C52DD30E443A496DC6363C3FC62B5"> 
       <li id="li_6493B2A335A8497C9A1BC6292C88CA81"> Klik in het venster Transform.cfg </span> op de werkbank voor gegevens met de rechtermuisknop <span class="uicontrol"> Stage </span> en klik vervolgens op <span class="uicontrol"> Nieuwe </span> &gt; <span class="uicontrol"> Stage </span>.<span class="filepath"> </span></li> 
       <li id="li_EE25E50CEB53450EA6465B08B0AE5442"> Voer een naam in voor het nieuwe werkgebied. </li> 
      </ul> <p> <b>Een bestaand verwerkingsstadium verwijderen</b> </p> 
      <ul id="ul_4950BC26E0CD4837A4CB377605A52D3C"> 
      <li id="li_A61E2C17966E4F96A1256B8390623B0F"> Klik met de rechtermuisknop op het nummer dat overeenkomt met het werkgebied dat u wilt verwijderen en klik op <span class="uicontrol"> </span><i>&lt; <span class="uicontrol"> #stage_number </span></i>. </li> 
      </ul> <p> <p>Opmerking:  Wanneer u een werkgebied opgeeft in een <span class="wintitle"> Gegevensset voor logverwerking Inclusief </span>-bestand, moet de naam van het werkgebied exact overeenkomen met de naam die u hier invoert. Voor meer informatie over dataset omvat dossiers, zie <a href="../../../../../home/c-dataset-const-proc/c-dataset-inc-files/c-abt-dataset-inc-files.md"> Dataset omvat Dossiers </a>. </p> </p> </td> 
    </tr> 
    <tr> 
    <td colname="col1"> Begintijd </td> 
    <td colname="col2"> <p>Optioneel. Gegevens filteren om logitems met tijdstempels op of na dit tijdstip op te nemen. Adobe raadt u aan een van de volgende notaties te gebruiken: </p> 
      <ul id="ul_8F9B82A8AE7F45BE8C7949D2E96C7BEC"> 
       <li id="li_8F7BCFF251CB4F1B87DDA1A259FA9C7B"> 1 januari 2013 HH:MM:SS EDT </li> 
       <li id="li_4BCE317EE1914074B3642687CFED5FC2"> 1 januari 2013 UU:MM:SS GMT </li> 
      </ul> <p> Als u bijvoorbeeld 29 juli 2013 00:00:00 EDT opgeeft als begintijd, worden vanaf 29 juli 2013 om 12:00:00 EDT gegevens opgenomen. </p> <p> U moet een tijdzone opgeven. De tijdzone is niet standaard ingesteld op GMT als deze niet is opgegeven. Zie <a href="../../../../../home/c-dataset-const-proc/c-time-zone.md#concept-9b540ec3e770490d94e9d5a985765477"> Tijdzonecodes </a> voor een lijst met afkortingen voor tijdzones die worden ondersteund door de gegevensworkbench-server. </p> <p> <p>Opmerking:  De parameter Start/End Times gebruiken voor Sensor- en logbestandsbronnen is gerelateerd aan deze parameter. </p> </p> </td> 
    </tr> 
    <tr> 
    <td colname="col1"> Transformaties </td> 
    <td colname="col2"> <p>Optioneel. Definieert de transformaties die op de gegevens moeten worden toegepast. Zie <a href="../../../../../home/c-dataset-const-proc/c-data-trans/c-abt-transf.md"> Gegevenstransformaties </a> voor informatie over de beschikbare transformatietypen. </p> <p> <p>Opmerking:  De volgende transformatietypen werken niet wanneer deze worden gedefinieerd in de gegevenswerkbank <span class="filepath"> Transform.cfg </span>-bestand: </p> </p> 
      <ul id="ul_B091DFBD1C33471BBC01AEC7E92FC8CC"> 
       <li id="li_660EBECFC407488199CCCC886326806D"> AppendURI </li> 
       <li id="li_56BCEBE4A2D044AE87F5B747C6501817"> CrossRows </li> 
       <li id="li_B23B4E81B37942DCA55FEC1A6239C5FA"> ODBCLookup </li> 
       <li id="li_EF0AFF13C40D4AB49EAB4EF1691F8FA4"> Sessioneren </li> 
      </ul> </td> 
    </tr> 
  </tbody> 
  </table>

>[!NOTE]
>
>Als er aanvullende gegevens worden ontvangen nadat de uitvoerbestanden zijn gesloten (zie [!DNL Log Sources] en [!DNL Offline Mode] in de voorgaande tabel), maakt [!DNL Transform] nieuwe uitvoerbestanden met de aanvullende gegevens. De namen van de nieuwe uitvoerbestanden worden gegenereerd op basis van de naam van het oorspronkelijke uitvoerbestand, met toevoeging van een versienummer ter grootte van een haakje vlak voor de extensie. Als het oorspronkelijke uitvoerbestand bijvoorbeeld [!DNL 20070701-ABC.vsl] is, krijgen volgende versies van dit bestand de naam [!DNL 20070701-ABC(1).vsl], [!DNL 20070701-ABC(2).vsl] enzovoort. Houd er rekening mee dat het gebruik van de versiebestanden als invoer voor de gegevenswerkbankserver tot verwerkingsfouten kan leiden.
>
>
>Adobe raadt aan het maken van geversierde uitvoerbestanden te voorkomen door ervoor te zorgen dat alle brongegevens in chronologische volgorde staan binnen lexicografisch geordende invoerbestanden en dat, als [!DNL Offline Mode] op true is ingesteld, alle brongegevens aanwezig zijn voordat de verwerking wordt gestart. Zie de [!DNL Log Sources]- en [!DNL Offline Mode]-items in de voorgaande tabel voor meer informatie.

1. Voeg transformaties toe door met de rechtermuisknop **[!UICONTROL Transformations]** te klikken en **[!UICONTROL Add new]** > **[!UICONTROL Transformation type]** te klikken. Voltooi de transformatievelden.

   Zie [Gegevenstransformaties](../../../../../home/c-dataset-const-proc/c-data-trans/c-abt-transf.md) voor beschrijvingen en voorbeelden van de transformaties die u kunt gebruiken met transformatiefunctionaliteit.

1. Klik met de rechtermuisknop **[!UICONTROL (modified)]** boven in het venster en klik vervolgens op **[!UICONTROL Save]**.
1. Als u wilt dat de lokaal aangebrachte wijzigingen van kracht worden, klikt u in [!DNL Profile Manager] met de rechtermuisknop op het vinkje voor de gegevenswerkbank [!DNL Transform.cfg] in de kolom [!DNL User] en vervolgens op **[!UICONTROL Save to]** > **[!UICONTROL profile name]**, waarbij de profielnaam de naam is van het profiel waarvoor u gegevens exporteert. De gegevens worden opnieuw verwerkt nadat het profiel is gesynchroniseerd.

   >[!NOTE]
   >
   >Zie [Opwerking en wederomzetting](../../../../../home/c-dataset-const-proc/c-reproc-retrans/c-unst-reproc-retrans.md) voor informatie over het opnieuw verwerken van uw gegevens voor export.
