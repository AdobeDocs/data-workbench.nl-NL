---
description: U kunt een segment van de elementen van om het even welke telbare dimensie tot stand brengen, dan outputgegevens voor dat segment op een partij of aan de gang zijnde basis in real time in een lusje-afgebakend dossier.
title: Segmenten voor exporteren configureren
uuid: 651be834-ee41-4487-8c5a-30d94580f6a0
exl-id: 4f53e02c-3f00-44b3-9f6d-a2f23903b3fa
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '865'
ht-degree: 0%

---

# Segmenten voor exporteren configureren{#configure-segments-for-export}

{{eol}}

U kunt een segment van de elementen van om het even welke telbare dimensie tot stand brengen, dan outputgegevens voor dat segment op een partij of aan de gang zijnde basis in real time in een lusje-afgebakend dossier.

Telkens wanneer u een segment exporteert, voert u metrische of dimensiegegevens uit voor alle afmetingselementen die in dat segment zijn opgenomen. U kunt bepalen hoe de uitvoergegevens worden opgemaakt, zodat andere systemen de gegevens gemakkelijk kunnen laden.

>[!NOTE]
>
>U kunt de rapportafmetingen niet exporteren, omdat deze een [!DNL report time.metric] bestand ter referentie. Als oplossing kunt u een harde code plaatsen [!DNL report time.metric] in het profiel, kan de segmentuitvoer het als verwijzingspunt voor het melden van dimensies gebruiken. De [!DNL report time.metric] wordt niet automatisch bijgewerkt op basis van het profiel &#39;s vanaf tijd&#39;. Als u de verwijzing naar de rapportdimensie wilt wijzigen, moet u de code wijzigen [!DNL report time.metric] bestand.

Om een segment voor de uitvoer te vormen, moet u openen en uitgeven [!DNL .export] bestand.

1. In de [!DNL Profile Manager]klikt u op de knop **[!UICONTROL Export]** in de [!DNL File] om de inhoud weer te geven.

       Als de map Export niet bestaat, maakt u deze als volgt:
   
   1. Navigeer naar de installatiemap van uw Data Workbench.
   1. Open de map voor het profiel waarmee u werkt.
   1. Maak in de map Profiel een nieuwe map met de naam &quot;Exporteren&quot;.

1. In de [!DNL Profile Manager]klikt u met de rechtermuisknop op de lege cel in het dialoogvenster [!DNL User] kolom voor de map Export en klik vervolgens op **[!UICONTROL Create]** > **[!UICONTROL New Segment Export]**.

   Een bestand met de naam [!DNL New Segment Export.export] in het dialoogvenster [!DNL File] kolom voor Exporteren.

1. Wijzig de naam van het nieuwe bestand door met de rechtermuisknop in het dialoogvenster [!DNL User] en typt u de nieuwe naam in de parameter File.
1. Open het nieuwe bestand door met de rechtermuisknop in het dialoogvenster [!DNL User] kolom voor het bestand en klikken op **[!UICONTROL Open]** > **[!UICONTROL from the workbench]**.

   Het configuratievenster voor de [!DNL .export] wordt weergegeven.

1. Klikken **[!UICONTROL Query]** wijzigt u vervolgens de velden van het dialoogvenster [!DNL .export] bestand zoals beschreven in de volgende tabel:

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
   <td colname="col2"> <p>Optioneel. Een programma dat wordt uitgevoerd nadat het uitvoerbestand is gemaakt. Dit veld moet verwijzen naar een uitvoerbaar bestand (en <span class="filepath"> .exe </span> bestand), niet een shell-opdracht. </p> <p>Opmerking: De segmentexport zal mislukken als er een spatie in de bevelparameter is. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Filter </td> 
   <td colname="col2"> <p>Optioneel. Een benoemd filter of een filterexpressie. U kunt een benoemd filter maken met een filtereditor en vervolgens hier de naam van dat filter typen of u kunt een filterexpressie zelf typen. </p> <p>Zie voor meer informatie over filtereditors <a href="../../../home/c-get-started/c-analysis-vis/c-filter-editors/c-filter-editors.md#concept-2f343ecbed8240f18b0c1f1eccef11e3"> Filtereditors </a>. Zie voor meer informatie over syntaxis van filterexpressies <a href="../../../home/c-get-started/c-qry-lang-syntx/c-syntx-fltr-exp.md#concept-72f2563f809747a2a3cff7ec72462a15"> Syntaxis voor filterexpressies </a>. </p> <p>Elementen van Niveau die overeenkomen met het filter worden geëxporteerd, terwijl andere elementen dat niet doen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Niveau </td> 
   <td colname="col2"> <p>De aftelbare dimensie waarvan de elementen moeten worden geëxporteerd. </p> <p>Voorbeeld: Een niveau van Bezoeker voert één rij gegevens voor elke bezoeker uit. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Uitvoerbestand </td> 
   <td colname="col2"> <p>Pad en bestandsnaam van de geëxporteerde gegevens. Als het profiel op een servercluster van de Data Workbench loopt, schrijft elke server van de Data Workbench een Dossier van de Output dat een gedeelte van de gegevens bevat. </p> <p>De installatiemap van de server van de Data Workbench bevat een directory Exporteren waar u het uitvoerbestand kunt opslaan. U kunt bijvoorbeeld <span class="filepath"> Exporteren\Visitor Segment.txt </span>, waarbij <span class="filepath"> Bezoekerssegment.txt </span> is de naam van het bestand dat de geëxporteerde gegevens bevat. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Uitvoerindeling </td> 
   <td colname="col2"> De metrische of afmetingsgegevens die voor elk element van het Niveau moeten worden uitgevoerd. Als de uitvoer een door tabs gescheiden bestand is, moeten de velden worden gescheiden door tabtekens en moet de opmaak eindigen met de juiste tekens voor nieuwe regels. Zie voor meer informatie <a href="../../../home/c-get-started/c-exp-data-seg-exp/c-abt-otpt-frmt.md#concept-ac7e24d1374a4b418365db7cc98c361e"> De uitvoerindeling </a>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Eindtijd planning </td> 
   <td colname="col2"> <p>Optioneel. De einddatum en -tijd voor het programma, inclusief de tijdzone. </p> <p>Indeling: YYYY-MM-DD hh:mm tijdzone </p> <p>Voorbeeld: 2013-08-01 12:01 EDT </p> <p>De geplande uitvoer stopt op dat moment; het uitvoerbestand wordt echter nog steeds opnieuw gegenereerd wanneer de definitie ervan wordt gewijzigd. Dit veld heeft geen betekenis zonder planning op elke te definiëren. Voor meer informatie over de montages van de tijdzone, zie <i>Configuratie-handleiding voor gegevensset</i>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Plan elke </td> 
   <td colname="col2"> Optioneel. De frequentie waarmee het uitvoerbestand opnieuw moet worden gegenereerd. Ondersteunde waarden zijn uur, dag, week en maand. Het uitvoerbestand wordt nog steeds opnieuw gegenereerd wanneer de definitie ervan wordt gewijzigd. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Begintijd plannen </td> 
   <td colname="col2"> <p>Optioneel. De begindatum en -tijd voor het programma, inclusief de tijdzone. </p> <p>Indeling: YYYY-MM-DD hh:mm tijdzone </p> <p>Voorbeeld: 2013-08-01 12:01 EDT </p> <p>De geplande uitvoer begint op dit ogenblik, en het programma is met betrekking tot deze tijd. Dit veld heeft geen betekenis zonder definitie <span class="wintitle"> Plan elke </span>. Voor meer informatie over de montages van de tijdzone, zie <i>Configuratie-handleiding voor gegevensset</i>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Tijdslimiet (sec) </td> 
   <td colname="col2"> Optioneel. De maximumtijd die wordt toegestaan om te verstrijken terwijl een segmentuitvoer wordt geproduceerd. Als het opgegeven interval wordt overschreden, wordt het exporteren opnieuw gestart. Als u deze waarde instelt op 0 (nul), wordt de limiet verwijderd. De standaardwaarde is 600 seconden. </td> 
  </tr> 
 </tbody> 
</table>

1. Klikken met rechtermuisknop **[!UICONTROL (New)]** boven aan het venster klikt u op **[!UICONTROL Save]**.
1. Als u dit bestand beschikbaar wilt maken voor alle gebruikers van het werkprofiel, klikt u met de rechtermuisknop op het vinkje voor het gemaakte [!DNL .export] in het [!DNL User] kolom, klik vervolgens op **[!UICONTROL Save to]** > *&lt;**[!UICONTROL working profile name]**>*.

   >[!NOTE]
   >
   >De [!DNL .export] het bestand naar de server van de Data Workbench zorgt ervoor dat het exporteren één keer direct wordt uitgevoerd, zelfs als de Begintijd van het schema is ingesteld op een datum en tijd in de toekomst.

   Hier volgt een voorbeeld [!DNL .export] bestand.

   ![](assets/vis_Segment_Export_File.png)

   >[!NOTE]
   >
   >De [!DNL Visitor Segment.export] Het bestand in het voorbeeld verwijst naar het filter Bezoekerssegment. Als u de definitie van dit filter wijzigt, verandert de definitie van de exportbewerking.
