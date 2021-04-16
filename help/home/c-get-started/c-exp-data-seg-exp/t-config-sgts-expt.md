---
description: U kunt een segment van de elementen van om het even welke telbare dimensie tot stand brengen, dan outputgegevens voor dat segment op een partij of aan de gang zijnde basis in real time in een lusje-afgebakend dossier.
title: Segmenten voor exporteren configureren
uuid: 651be834-ee41-4487-8c5a-30d94580f6a0
exl-id: 4f53e02c-3f00-44b3-9f6d-a2f23903b3fa
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '865'
ht-degree: 0%

---

# Segmenten voor exporteren configureren{#configure-segments-for-export}

U kunt een segment van de elementen van om het even welke telbare dimensie tot stand brengen, dan outputgegevens voor dat segment op een partij of aan de gang zijnde basis in real time in een lusje-afgebakend dossier.

Telkens wanneer u een segment exporteert, voert u metrische of dimensiegegevens uit voor alle afmetingselementen die in dat segment zijn opgenomen. U kunt bepalen hoe de uitvoergegevens worden opgemaakt, zodat andere systemen de gegevens gemakkelijk kunnen laden.

>[!NOTE]
>
>U kunt rapportafmetingen niet exporteren, omdat deze een [!DNL report time.metric]-bestand ter referentie gebruiken. Als tussenoplossing kunt u een hard-gecodeerde [!DNL report time.metric] in het profiel plaatsen, de segmentuitvoer het als referentiepunt voor het melden van dimensies gebruiken. De [!DNL report time.metric] wordt echter niet automatisch bijgewerkt op basis van het profiel &#39;s vanaf tijd. Als u de verwijzing naar de rapportdimensie wilt wijzigen, moet u het bestand met de harde code [!DNL report time.metric] wijzigen.

Als u een segment wilt configureren voor export, moet u een [!DNL .export]-bestand openen en bewerken.

1. Klik in [!DNL Profile Manager] op de map **[!UICONTROL Export]** in de kolom [!DNL File] om de inhoud ervan weer te geven.

       Als de map Export niet bestaat, maakt u deze als volgt:
   
   1. Navigeer naar de installatiemap van uw Data Workbench.
   1. Open de map voor het profiel waarmee u werkt.
   1. Maak in de map Profiel een nieuwe map met de naam &quot;Exporteren&quot;.

1. Klik in [!DNL Profile Manager] met de rechtermuisknop op de lege cel in de kolom [!DNL User] voor de map Export en klik vervolgens op **[!UICONTROL Create]** > **[!UICONTROL New Segment Export]**.

   Een dossier genoemd [!DNL New Segment Export.export] verschijnt in [!DNL File] kolom voor de Uitvoer.

1. Wijzig de naam van het nieuwe bestand door met de rechtermuisknop in de kolom [!DNL User] voor het bestand te klikken en de nieuwe naam in de parameter File te typen.
1. Open het nieuwe bestand door met de rechtermuisknop te klikken in de kolom [!DNL User] voor het bestand en te klikken op **[!UICONTROL Open]** > **[!UICONTROL from the workbench]**.

   Het configuratievenster voor het [!DNL .export] dossier verschijnt.

1. Klik **[!UICONTROL Query]**, dan wijzig de gebieden van het [!DNL .export] dossier zoals die in de volgende lijst worden beschreven:

<table id="table_C2EC8FCD3FA04DE78D2CADFA3F7FD8E3"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Voor deze parameter... </th> 
   <th colname="col2" class="entry"> Deze informatie opgeven... </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Opdracht </td> 
   <td colname="col2"> <p>Optioneel. Een programma dat wordt uitgevoerd nadat het uitvoerbestand is gemaakt. Dit gebied moet uitvoerbaar (een <span class="filepath"> .exe </span> dossier), niet shell bevel van verwijzingen voorzien. </p> <p>Opmerking:  De segmentexport zal mislukken als er een spatie in de bevelparameter is. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Filter </td> 
   <td colname="col2"> <p>Optioneel. Een benoemd filter of een filterexpressie. U kunt een benoemd filter maken met een filtereditor en vervolgens hier de naam van dat filter typen of u kunt een filterexpressie zelf typen. </p> <p>Zie <a href="../../../home/c-get-started/c-analysis-vis/c-filter-editors/c-filter-editors.md#concept-2f343ecbed8240f18b0c1f1eccef11e3"> Filtereditors </a> voor meer informatie over filtereditors. Zie <a href="../../../home/c-get-started/c-qry-lang-syntx/c-syntx-fltr-exp.md#concept-72f2563f809747a2a3cff7ec72462a15"> Syntaxis voor filterexpressies </a> voor meer informatie over syntaxis van filterexpressies. </p> <p>Elementen van Niveau die overeenkomen met het filter worden geëxporteerd, terwijl andere elementen dat niet doen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Niveau </td> 
   <td colname="col2"> <p>De aftelbare dimensie waarvan de elementen moeten worden geëxporteerd. </p> <p>Voorbeeld: Een niveau van Bezoeker voert één rij gegevens voor elke bezoeker uit. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Uitvoerbestand </td> 
   <td colname="col2"> <p>Pad en bestandsnaam van de geëxporteerde gegevens. Als het profiel op een servercluster van de Data Workbench loopt, schrijft elke server van de Data Workbench een Dossier van de Output dat een gedeelte van de gegevens bevat. </p> <p>De installatiemap van de server van de Data Workbench bevat een directory Exporteren waar u het uitvoerbestand kunt opslaan. U kunt bijvoorbeeld <span class="filepath"> Exports\Visitor Segment.txt </span> invoeren, waarbij <span class="filepath"> Visitor Segment.txt </span> de naam is van het bestand dat de geëxporteerde gegevens bevat. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Uitvoerindeling </td> 
   <td colname="col2"> De metrische of afmetingsgegevens die voor elk element van het Niveau moeten worden uitgevoerd. Als de uitvoer een door tabs gescheiden bestand is, moeten de velden worden gescheiden door tabtekens en moet de opmaak eindigen met de juiste tekens voor nieuwe regels. Zie <a href="../../../home/c-get-started/c-exp-data-seg-exp/c-abt-otpt-frmt.md#concept-ac7e24d1374a4b418365db7cc98c361e"> Informatie over Uitvoerindeling </a> voor meer informatie. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Eindtijd planning </td> 
   <td colname="col2"> <p>Optioneel. De einddatum en -tijd voor het programma, inclusief de tijdzone. </p> <p>Indeling: YYYY-MM-DD hh:mm tijdzone </p> <p>Voorbeeld: 2013-08-01 12:01 EDT </p> <p>De geplande uitvoer stopt op dat moment; het uitvoerbestand wordt echter nog steeds opnieuw gegenereerd wanneer de definitie ervan wordt gewijzigd. Dit veld heeft geen betekenis zonder planning op elke te definiëren. Voor meer informatie over de montages van de tijdzone, zie <i>de Gids van de Configuratie van de Dataset</i>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Plan elke </td> 
   <td colname="col2"> Optioneel. De frequentie waarmee het uitvoerbestand opnieuw moet worden gegenereerd. Ondersteunde waarden zijn uur, dag, week en maand. Het uitvoerbestand wordt nog steeds opnieuw gegenereerd wanneer de definitie ervan wordt gewijzigd. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Begintijd plannen </td> 
   <td colname="col2"> <p>Optioneel. De begindatum en -tijd voor het programma, inclusief de tijdzone. </p> <p>Indeling: YYYY-MM-DD hh:mm tijdzone </p> <p>Voorbeeld: 2013-08-01 12:01 EDT </p> <p>De geplande uitvoer begint op dit ogenblik, en het programma is met betrekking tot deze tijd. Dit veld heeft geen betekenis zonder <span class="wintitle"> Planning om </span> te definiëren. Voor meer informatie over de montages van de tijdzone, zie <i>de Gids van de Configuratie van de Dataset</i>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Tijdslimiet (sec) </td> 
   <td colname="col2"> Optioneel. De maximumtijd die wordt toegestaan om te verstrijken terwijl een segmentuitvoer wordt geproduceerd. Als het opgegeven interval wordt overschreden, wordt het exporteren opnieuw gestart. Als u deze waarde instelt op 0 (nul), wordt de limiet verwijderd. De standaardwaarde is 600 seconden. </td> 
  </tr> 
 </tbody> 
</table>

1. Klik met de rechtermuisknop **[!UICONTROL (New)]** boven in het venster en klik vervolgens op **[!UICONTROL Save]**.
1. Als u dit bestand beschikbaar wilt maken voor alle gebruikers van het werkprofiel, klikt u met de rechtermuisknop op het vinkje voor het gemaakte [!DNL .export]-bestand in de kolom [!DNL User] en klikt u op **[!UICONTROL Save to]** > *&lt;**[!UICONTROL working profile name]**>*.

   >[!NOTE]
   >
   >Wanneer u het [!DNL .export]-bestand opslaat op de Data Workbench-server, wordt het exporteren één keer direct uitgevoerd, zelfs als de Begintijd van het schema is ingesteld op een datum en tijd in de toekomst.

   Hier volgt een voorbeeld van een [!DNL .export]-bestand.

   ![](assets/vis_Segment_Export_File.png)

   >[!NOTE]
   >
   >Het [!DNL Visitor Segment.export]-bestand in het voorbeeld verwijst naar het filter Bezoekerssegment. Als u de definitie van dit filter wijzigt, verandert de definitie van de exportbewerking.
