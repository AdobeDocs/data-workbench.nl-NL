---
description: Het bestand data workbenchTransform.cfg bevat de parameters die de logbronnen, gegevenstransformaties en exportfuncties definiëren.
title: Het bestand Transform.cfg
uuid: eab5bb70-6de7-4f08-85db-a6cb00abd3ed
exl-id: e84f2536-cb22-4c47-a7a8-270b3c37ece6
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '1332'
ht-degree: 0%

---

# Het bestand Transform.cfg{#the-transform-cfg-file}

{{eol}}

Het bestand data workbenchTransform.cfg bevat de parameters die de logbronnen, gegevenstransformaties en exportfuncties definiëren.

De transformaties die u definieert, bewerken de onbewerkte gegevens die door sensoren worden verzameld ( [!DNL .vsl] bestanden) of opgenomen in tekstbestanden, XML-bestanden of ODBC-compatibele databases en uitgevoerd in bestaande velden, waarbij de huidige gegevens worden overschreven of in nieuw gedefinieerde velden.

Om transformatiefunctionaliteit te configureren, bewerkt u de gegevenswerkbank [!DNL Transform.cfg] in de map Dataset voor het profiel waarvoor u gebeurtenisgegevens wilt exporteren. Dit profiel is doorgaans toegewezen aan transformatiefunctionaliteit (u voert dus geen andere gegevensverwerking uit dan wat is gedefinieerd in de gegevenswerkbank) [!DNL Transform.cfg] bestand). Het is belangrijk op te merken dat alle in de [!DNL Log Processing Dataset Include] bestanden voor overerfde profielen worden toegepast naast de profielen die zijn opgegeven in de werkbank voor gegevens [!DNL Transform.cfg] bestand.

Voor informatie over dataset omvat dossiers, zie [Gegevensset met bestanden](../../../../../home/c-dataset-const-proc/c-dataset-inc-files/c-abt-dataset-inc-files.md).

Als de gegevens die u wilt uitvoeren door een servercluster van de gegevenswerkbank worden verwerkt, verwerkt elk van de verwerkingsservers (DPUs) in de cluster de gegevens, maar slechts eerste DPU (verwerkingsserver #0 in [!DNL profile.cfg] bestand) de uitvoergegevens naar het lokale bestandssysteem schrijven.

**Het bestand Transform.cfg op de werkbank Gegevens bewerken**

1. Als u werkt in het profiel waarvoor u gegevens wilt exporteren, opent u het dialoogvenster [!DNL Profile Manager] en klik op **[!UICONTROL Dataset]** om de inhoud van de map weer te geven.
1. Klik met de rechtermuisknop op het vinkje naast de gegevenswerkbank [!DNL Transform.cfg]en klik vervolgens op **[!UICONTROL Make Local]**. Er wordt een vinkje voor dit bestand weergegeven in het dialoogvenster [!DNL User] kolom.
1. Klik met de rechtermuisknop op het nieuwe vinkje en klik op **[!UICONTROL Open]** > **[!UICONTROL from the workbench]**. De gegevenswerkbank [!DNL Transform.cfg] wordt weergegeven.
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
       <li id="li_33806070F991476BB986906876CAF7F1"> 1 jan. 2013 HH:MM:SS GMT </li> 
      </ul> </p> <p> Bijvoorbeeld: 29 juli 2013 00 opgeven:00:00 EDT als de <span class="wintitle"> Eindtijd </span> inclusief gegevens tot en met 28 juli 2013, op 11:59:17:00 </p> <p> U moet een tijdzone opgeven. De tijdzone is niet standaard ingesteld op GMT als deze niet is opgegeven. Voor een lijst van de afkortingen van de tijdzone die door de server van de gegevenswerkbank worden gesteund, zie <a href="../../../../../home/c-dataset-const-proc/c-time-zone.md#concept-9b540ec3e770490d94e9d5a985765477"> Tijdzonecodes </a>. </p> <p> De parameter Start/End Times gebruiken voor Sensor- en logbestandsbronnen is gerelateerd aan deze parameter. </p> </td> 
    </tr> 
    <tr> 
    <td colname="col1"> Exporteurs </td> 
    <td colname="col2"> <p>De subvelden van een exporter geven aan hoe de uitvoergegevens worden verwerkt en/of opgemaakt. U kunt meerdere exportfuncties definiëren voor een set logbronnen. Elk type exporter maakt uitvoer onafhankelijk van elkaar. </p> <p> Er zijn drie soorten exporteurs: 
      <ul id="ul_C3C39F6DF3DC4F4CA2161EDB69599642"> 
       <li id="li_635FB271D0544D52B1C31740442D2E08"> ExportTextFile </li> 
       <li id="li_D496194848B44823A58890E03FFDD18E"> ExportDelimitedTextFile </li> 
       <li id="li_AEE9AA87076141FC91330D3FCFAB2101"> ExportVSLFile </li> 
      </ul> </p> <p> Zie voor meer informatie over exporttypen <a href="../../../../../home/c-dataset-const-proc/c-transf-func/c-config-files-transf/t-ins-transf-file/t-def-exp.md#task-900c40d1914347f288587bf0ca394ff2"> Exporters definiëren </a>. </p> </td> 
    </tr> 
    <tr> 
    <td colname="col1"> Hash-drempel </td> 
    <td colname="col2"> Optioneel. Een bemonsteringsfactor voor willekeurige subsampling van rijen. Als deze op een getal n is ingesteld, wordt slechts één van elke n-id geselecteerd voor exporteren, waardoor het totale aantal rijen dat met een factor n wordt geëxporteerd, wordt verminderd. Als u alle rijen wilt exporteren, stelt u Hash-drempel in op 1. </td> 
    </tr> 
    <tr> 
    <td colname="col1"> Voorwaarde logbestandvermelding </td> 
    <td colname="col2"> Optioneel. Bepaalt de regels waardoor de logboekingangen voor de uitvoer worden overwogen. Voor meer informatie over de <span class="wintitle"> Voorwaarde logbestandvermelding </span>, zie <a href="../../../../../home/c-dataset-const-proc/c-log-proc-config-file/c-abt-log-proc-config-file.md"> Logboekverwerkingsconfiguratiebestand </a>. </td> 
    </tr> 
    <tr> 
    <td colname="col1"> Logbronnen </td> 
    <td colname="col2"> <p>De gegevensbronnen. <span class="wintitle"> Logbronnen </span> kan <span class="filepath"> .vsl </span> bestanden, logbestanden of XML-bestanden of gegevens uit databases die compatibel zijn met ODBC. Voor informatie over <span class="wintitle"> logbronnen </span>, zie <a href="../../../../../home/c-dataset-const-proc/c-log-proc-config-file/c-abt-log-proc-config-file.md"> Logboekverwerkingsconfiguratiebestand </a>. </p> <p> <span class="wintitle"> Transformeren </span> verwacht dat alle brongegevens in chronologische volgorde staan binnen lexicografisch geordende invoerbestanden. Als niet aan deze eis wordt voldaan, zijn de berekeningen Van onjuist, en de extra inputgegevens kunnen worden verwerkt nadat de outputdossiers worden gesloten. </p> </td> 
    </tr> 
    <tr> 
    <td colname="col1"> Offlinemodus </td> 
    <td colname="col2"> <p>Optioneel. Waar of onwaar. Indien waar (true) <span class="wintitle"> Transformeren </span> Hierbij wordt ervan uitgegaan dat alle invoerbestanden aanwezig zijn wanneer de gegevens worden verwerkt. Wanneer alle invoergegevens zijn gelezen, <span class="wintitle"> Transformeren </span> Sluit alle outputdossiers zonder het wachten op extra te ontvangen gegevens. De standaardwaarde is false. </p> <p> <p>Opmerking: Indien <span class="wintitle"> Offlinemodus </span> is ingesteld op true, <span class="wintitle"> Transformeren </span> verwacht dat alle brongegevens aanwezig zijn alvorens de verwerking begint. Er wordt een waarschuwingsbericht gegenereerd in het dialoogvenster <span class="filepath"> VisualServer.log </span> als er aanvullende gegevens worden ontvangen nadat de uitvoerbestanden zijn gesloten. </p> </p> </td> 
    </tr> 
    <tr> 
    <td colname="col1"> Opnieuw verwerken </td> 
    <td colname="col2"> <p>Optioneel. Elk teken of elke combinatie van tekens kan hier worden ingevoerd. Deze parameter wijzigen en het bestand opslaan in de <span class="wintitle"> Transformeren </span> computer start gegevensopwerking. </p> <p> Voor informatie over het opnieuw verwerken van uw gegevens raadpleegt u <a href="../../../../../home/c-dataset-const-proc/c-reproc-retrans/c-unst-reproc-retrans.md"> Opwerking en heromzetting </a>. </p> </td> 
    </tr> 
    <tr> 
    <td colname="col1"> Staven </td> 
    <td colname="col2"> <p>Optioneel. De namen van de verwerkingsstadia die kunnen worden gebruikt in <span class="wintitle"> Gegevensset logbestandsverwerking opnemen </span> bestanden die worden uitgevoerd naast de gegevenswerkbank <span class="filepath"> Transform.cfg </span> bestand. Met verwerkingsstadia kunt u de transformaties die zijn gedefinieerd in <span class="wintitle"> Gegevensset logbestandsverwerking opnemen </span> bestanden. Deze parameter is erg handig als u een of meer transformaties binnen meerdere transformaties hebt gedefinieerd <span class="wintitle"> Gegevensset logbestandsverwerking opnemen </span> en u wilt dat specifieke transformaties op specifieke punten tijdens het exportproces worden uitgevoerd. </p> <p> De volgorde waarin u de stappen hier opsomt, bepaalt de volgorde waarin de transformaties in de <span class="wintitle"> Gegevensset logbestandsverwerking opnemen </span> bestanden worden uitgevoerd tijdens het exporteren van gegevens. <span class="wintitle"> Voorbewerken </span> en <span class="wintitle"> Postverwerking </span> ingebouwde fasen hebben; <span class="wintitle"> Voorbewerken </span> altijd de eerste fase is, en <span class="wintitle"> Postverwerking </span> is altijd de laatste fase. Standaard wordt een fase met de naam <span class="wintitle"> Standaard </span>. </p> <p> <b>Een nieuw verwerkingsstadium toevoegen</b> </p> 
      <ul id="ul_869C52DD30E443A496DC6363C3FC62B5"> 
       <li id="li_6493B2A335A8497C9A1BC6292C88CA81"> In de gegevenswerkbank <span class="filepath"> Transform.cfg </span> venster, klik met de rechtermuisknop <span class="uicontrol"> Staven </span>en klik vervolgens op <span class="uicontrol"> Nieuwe toevoegen </span> &gt; <span class="uicontrol"> Werkgebied </span>. </li> 
       <li id="li_EE25E50CEB53450EA6465B08B0AE5442"> Voer een naam in voor het nieuwe werkgebied. </li> 
      </ul> <p> <b>Een bestaand verwerkingsstadium verwijderen</b> </p> 
      <ul id="ul_4950BC26E0CD4837A4CB377605A52D3C"> 
      <li id="li_A61E2C17966E4F96A1256B8390623B0F"> Klik met de rechtermuisknop op het nummer dat overeenkomt met het werkgebied dat u wilt verwijderen en klik op <span class="uicontrol"> Verwijderen </span><i>&lt; <span class="uicontrol"> #stage_number </span>&gt;</i>. </li> 
      </ul> <p> <p>Opmerking: Wanneer u een werkgebied opgeeft in een <span class="wintitle"> Gegevensset logbestandsverwerking opnemen </span> moet de naam van het werkgebied exact overeenkomen met de naam die u hier invoert. Voor meer informatie over dataset omvat dossiers, zie <a href="../../../../../home/c-dataset-const-proc/c-dataset-inc-files/c-abt-dataset-inc-files.md"> Gegevensset met bestanden </a>. </p> </p> </td> 
    </tr> 
    <tr> 
    <td colname="col1"> Begintijd </td> 
    <td colname="col2"> <p>Optioneel. Gegevens filteren om logitems met tijdstempels op of na dit tijdstip op te nemen. Adobe raadt u aan een van de volgende notaties te gebruiken: </p> 
      <ul id="ul_8F9B82A8AE7F45BE8C7949D2E96C7BEC"> 
       <li id="li_8F7BCFF251CB4F1B87DDA1A259FA9C7B"> 1 januari 2013 HH:MM:SS EDT </li> 
       <li id="li_4BCE317EE1914074B3642687CFED5FC2"> 1 jan. 2013 HH:MM:SS GMT </li> 
      </ul> <p> Bijvoorbeeld: 29 juli 2013 00 opgeven:00:00 EDT als begintijd inclusief gegevens vanaf 29 juli 2013, op 12:00:00:00 </p> <p> U moet een tijdzone opgeven. De tijdzone is niet standaard ingesteld op GMT als deze niet is opgegeven. Voor een lijst van de afkortingen van de tijdzone die door de server van de gegevenswerkbank worden gesteund, zie <a href="../../../../../home/c-dataset-const-proc/c-time-zone.md#concept-9b540ec3e770490d94e9d5a985765477"> Tijdzonecodes </a>. </p> <p> <p>Opmerking: De parameter Start/End Times gebruiken voor Sensor- en logbestandsbronnen is gerelateerd aan deze parameter. </p> </p> </td> 
    </tr> 
    <tr> 
    <td colname="col1"> Transformaties </td> 
    <td colname="col2"> <p>Optioneel. Definieert de transformaties die op de gegevens moeten worden toegepast. Voor informatie over de beschikbare transformatietypen raadpleegt u <a href="../../../../../home/c-dataset-const-proc/c-data-trans/c-abt-transf.md"> Gegevenstransformaties </a>. </p> <p> <p>Opmerking: De volgende transformatietypen werken niet wanneer deze worden gedefinieerd in de gegevenswerkbank <span class="filepath"> Transform.cfg </span> bestand: </p> </p> 
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
>Als er aanvullende gegevens worden ontvangen nadat de uitvoerbestanden zijn gesloten (zie [!DNL Log Sources] en [!DNL Offline Mode] in de voorgaande tabel), [!DNL Transform] Hiermee maakt u nieuwe uitvoerbestanden met de aanvullende gegevens. De namen van de nieuwe uitvoerbestanden worden gegenereerd op basis van de naam van het oorspronkelijke uitvoerbestand, met toevoeging van een versienummer ter grootte van een haakje vlak voor de extensie. Als het oorspronkelijke uitvoerbestand bijvoorbeeld [!DNL 20070701-ABC.vsl]krijgen volgende versies van dit bestand de naam [!DNL 20070701-ABC(1).vsl], [!DNL 20070701-ABC(2).vsl], enzovoort. Houd er rekening mee dat het gebruik van de versiebestanden als invoer voor de gegevenswerkbankserver tot verwerkingsfouten kan leiden.
>
>
>Adobe raadt aan het maken van uitvoerbestanden met versienummer te vermijden door ervoor te zorgen dat alle brongegevens in chronologische volgorde staan binnen lexicografisch geordende invoerbestanden en, als [!DNL Offline Mode] is ingesteld op true, dat alle brongegevens aanwezig zijn voordat de verwerking wordt gestart. Zie voor meer informatie de [!DNL Log Sources] en [!DNL Offline Mode] in de voorgaande tabel.

1. Transformaties toevoegen door met de rechtermuisknop te klikken **[!UICONTROL Transformations]** en klikken **[!UICONTROL Add new]** > **[!UICONTROL Transformation type]**. Voltooi de transformatievelden.

   Zie [Gegevenstransformaties](../../../../../home/c-dataset-const-proc/c-data-trans/c-abt-transf.md) voor beschrijvingen en voorbeelden van de transformaties die u kunt gebruiken met transformatiefunctionaliteit.

1. Klikken met rechtermuisknop **[!UICONTROL (modified)]** boven aan het venster klikt u op **[!UICONTROL Save]**.
1. Om de plaatselijk aangebrachte veranderingen van kracht te maken, in [!DNL Profile Manager], klikt u met de rechtermuisknop op het vinkje voor de gegevenswerkbank [!DNL Transform.cfg] in de [!DNL User] kolom, klik vervolgens op **[!UICONTROL Save to]** >  **[!UICONTROL profile name]**, waarbij de profielnaam de naam is van het profiel waarvoor u gegevens exporteert. De gegevens worden opnieuw verwerkt nadat het profiel is gesynchroniseerd.

   >[!NOTE]
   >
   >Voor informatie over het opnieuw verwerken van uw gegevens voor export raadpleegt u [Opwerking en heromzetting](../../../../../home/c-dataset-const-proc/c-reproc-retrans/c-unst-reproc-retrans.md).
