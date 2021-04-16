---
description: De gedetailleerde interface van de Status is nuttig voor het oplossen van problemenfouten of andere kwesties met de servercomputers van de Data Workbench.
title: Gedetailleerde statusinterface
uuid: c4d375d9-431f-4b0a-ba15-b7a10501b2e2
exl-id: 6a460ebd-fb8f-4486-9849-dad2ff745cb5
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '1223'
ht-degree: 0%

---

# Gedetailleerde statusinterface{#detailed-status-interface}

De gedetailleerde interface van de Status is nuttig voor het oplossen van problemenfouten of andere kwesties met de servercomputers van de Data Workbench.

Dit omvat om het even welke [!DNL Transform] profielen die op die computers lopen, of [!DNL Report] computers die cliënten van de server van de Data Workbench zijn. U kunt tot [!DNL Master Server] en [!DNL Query Server Detailed Status] interfaces door [!DNL Admin] menu toegang hebben. Als u toegang wilt krijgen tot de [!DNL Detailed Status]-interface voor andere computers, klikt u in [!DNL Servers Manager] met de rechtermuisknop op het knooppunt van de server waarvan u de status wilt weergeven en klikt u op **[!UICONTROL Detailed Status]**. Zie [De Servers Manager](../../../home/c-get-started/c-admin-intrf/c-svrs-mgr.md#concept-2dfff1ca5bce470a8ee854ed57cbe5ba).

Voor meer informatie over de server van de Data Workbench, zie *de Gids van de Installatie en van het Beleid van de Producten van de Server*.

![](assets/vis_DetailedStatus.png)

>[!NOTE]
>
>Als u de informatie in een [!DNL Detailed Status]-interface wilt bijwerken, klikt u met de rechtermuisknop op de kop **[!UICONTROL Detailed Status]** en klikt u op **[!UICONTROL Refresh]**.

De volgende lijst maakt een lijst van de taken die kunnen worden voltooid gebruikend de [!DNL Detailed Status] interface.

<table id="table_E685F31DCDB343F49FFA1019F2E8DA85"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Deze taak uitvoeren... </th> 
   <th colname="col2" class="entry"> Doe dit... </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Om elke computercomponent en zijn huidige status te tonen </p> </td> 
   <td colname="col2"> <p>Klik <span class="uicontrol"> Component Status</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Om te tonen hoeveel geheugen op de computer wordt gebruikt </p> </td> 
   <td colname="col2"> <p>Klik <span class="uicontrol"> Geheugenstatus</span> &gt; <span class="uicontrol"> Adresruimtelading</span>. </p> <p>Voor meer informatie over het controleren van de lading van de adresruimte, zie <i>de Gids van de Installatie en van het Beleid van de Producten van de Server</i>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Om te bepalen of de computer wordt gevormd om de /3GB Schakelaar te gebruiken </p> </td> 
   <td colname="col2"> <p>Klik op <span class="uicontrol"> Geheugenstatus</span> &gt; <span class="uicontrol"> Procesadresruimte</span>. </p> <p>Als <span class="wintitle"> Totaal</span> meer toont dat 3000000 KB, wordt uw computer gevormd om de /3GB Schakelaar te gebruiken. </p> <p>Voor meer informatie over de /3GB Schakelaar, zie <i>de Gids van de Installatie en van het Beleid van de Producten van de Server</i>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Om de hoeveelheid schijfruimte en geheugen te controleren die wordt gebruikt om elke dimensie evenals die op te slaan die wordt gebruikt om de namen van zijn elementen op te slaan </p> </td> 
   <td colname="col2"> <p>Klik op <span class="uicontrol"> Prestaties</span> &gt; <span class="uicontrol"> Dimension</span> &gt; <span class="uicontrol"> Schijfgebruik</span> &gt; <i>&lt;<span class="uicontrol"> profielnaam</span> </i>of <span class="uicontrol"> Prestaties</span> &gt; <span class="uicontrol"> Dimension</span> &gt; <span class="uicontrol"> Geheugengebruik</span> &gt; <i>&lt;<span class="uicontrol"> profielnaam</span></i>. </p> <p>In de velden <span class="wintitle"> Schijfgebruik</span> staan de naam en hoeveelheid schijfruimte (in MB) die vereist is om elke dimensie op te slaan. De aantallen van het grote schijfgebruik kunnen vraagtijden negatief beïnvloeden omdat de server van de Data Workbench door alle gegevens moet lezen om verwante vragen te voltooien. Het verminderen van het schijfgebruik voor een afmeting kan de tijd verminderen het neemt om verwante vragen te voltooien. </p> <p>In de velden <span class="wintitle"> Geheugenverbruik</span> wordt het aantal elementen in elke dimensie aangegeven, evenals de hoeveelheid geheugen die nodig is om de lijst met elementnamen op te slaan. Grote aantallen elementen kunnen de hoeveelheid geheugen die tijdens een vraag wordt gebruikt negatief beïnvloeden omdat de server van de Data Workbench door elk element moet lezen. Het verminderen van het aantal elementen in een dimensie kan de tijd verminderen het neemt om verwante vragen te voltooien. </p> <p>Voorbeeld: <code>+&nbsp;Performance
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;-&nbsp;Dimensions&nbsp;
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;-&nbsp;Disk&nbsp;Usage
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;-&nbsp;ProfileName
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;-&nbsp;DimensionName&nbsp;1.386&nbsp;MB
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;.&nbsp;.&nbsp;.
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;-&nbsp;Memory&nbsp;Usage
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;-&nbsp;ProfileName
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;-&nbsp;DimensionName&nbsp;21&nbsp;elements,&nbsp;0.001&nbsp;MB
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;.&nbsp;.&nbsp;.</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Om het CPU-gebruik voor de fasen binnen de verwerking en transformatie van logbestanden te controleren </p> </td> 
   <td colname="col2"> <p>Klik op <span class="uicontrol"> Prestaties</span> &gt; <span class="uicontrol"> CPU-verbruik</span> &gt; <span class="uicontrol"> Logverwerking</span> &gt; <i>&lt;<span class="uicontrol"> profielnaam</span></i> of <span class="uicontrol"> Prestaties</span> &gt; <span class="uicontrol"> CPU-gebruik</span> &gt; <span class="uicontrol"> Transformatie</span> &gt; &lt;<span class="uicontrol"> profielnaam</span>&gt;. </p> <p>Elk van deze reeksen gebieden voorziet u van het Gebruik van cpu (in seconden) voor elk van de stadia binnen de Verwerking en de Transformatie van het Logboek. </p> <p>Voorbeeld: <code>+&nbsp;Performance
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;-&nbsp;CPU&nbsp;Usage&nbsp;
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;-&nbsp;Log&nbsp;Processing
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;-&nbsp;ProfileName&nbsp;158.9&nbsp;sec
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;-&nbsp;Built-in&nbsp;158.1&nbsp;sec
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;-&nbsp;StageName&nbsp;13.0&nbsp;sec
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;.&nbsp;.&nbsp;.
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;-&nbsp;Log&nbsp;Processing\ProfileName&nbsp;0.8&nbsp;sec
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;-&nbsp;StageName&nbsp;0.8&nbsp;sec</code> </p> <p>De tijd die het neemt om een vraag te voltooien is gewoonlijk evenredig aan de totale grootte van al uw dimensies. Na het herzien van de grootte van elke afmeting, kunt u beoordelen of een bepaalde afmeting nuttig genoeg is en vaak genoeg gebruikt om de prestatieskosten van de afmeting te rechtvaardigen. Als het niet is, kunt u de afmeting in <span class="wintitle"> de Manager van het Profiel</span> schrappen.<p>Een afmeting de waarvan lijst van elementnamen te groot (namelijk meer dan 128 MB) is kan "uit geheugen"fouten veroorzaken zelfs als het totale gebruik van de adresruimte niet dichtbij de grens is. </p> <p>Ook, als u een de servercluster van de Data Workbench maar gebruikt geen gecentraliseerde normalisatie gebruikt, heeft een afmeting de waarvan lijst van elementennamen groot is een significante invloed op verzendt geheugenbegrotingen. Voor meer informatie over gecentraliseerde normalisatie, zie <i>de Gids van de Configuratie van de Dataset</i>. Als de hoeveelheid geheugen die wordt vereist om alle lijsten van samengevoegde elementennamen op te slaan meer dan 100 MB over alle servers in de cluster is, zou u "Send geheugenbegroting kunnen ontvangen overschrijden"fouten zelfs wanneer de vraagactiviteit licht is. Bijvoorbeeld, als u een vier-server cluster met meer dan 25 MB op elke server hebt die wordt gebruikt om de lijsten van elementennamen op te slaan, zou u fouten kunnen ontvangen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Om de tijd te controleren die in de Verwerking en de Transformatie van het Logboek wordt doorgebracht </p> </td> 
   <td colname="col2"> <p>Klik op <span class="uicontrol"> Prestaties</span> &gt; <span class="uicontrol"> CPU-verbruik</span> &gt; <span class="uicontrol"> Logverwerking</span> &gt; <i>&lt;<span class="uicontrol"> profielnaam</span></i> of <span class="uicontrol"> Prestaties</span> &gt; <span class="uicontrol"> CPU-gebruik</span> &gt; <span class="uicontrol"> Transformation</span> &gt; <i>&lt;<span class="uicontrol"> profielnaam</span></i>. </p> <p>Door de velden in deze secties te bekijken, kunt u filters en transformaties identificeren die een negatief effect kunnen hebben op de hoeveelheid tijd die nodig is voor logverwerking en -transformatie. Vervolgens kunt u ontwerpbeslissingen nemen over afzonderlijke filters en transformaties met lange verwerkingstijd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Om schijfruimtegebruik te controleren en vraagsnelheid te verhogen </p> </td> 
   <td colname="col2"> <p>Klik <span class="uicontrol"> Prestaties</span> &gt; <span class="uicontrol"> Logverwerkingsvelden</span> &gt; <i>&lt;<span class="uicontrol"> profielnaam</span></i>. </p> <p>Elk regelitem in deze sectie komt overeen met een parameter in het bestand <span class="filepath"> Log Processing.cfg</span>. Door deze velden te bekijken, kunt u zien hoeveel geheugen elke parameter gebruikt. Vervolgens kunt u ontwerpbeslissingen nemen met betrekking tot afzonderlijke items die vrij groot zijn. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>De verstreken tijd van vorige opwerking of transformatie bepalen </p> </td> 
   <td colname="col2"> <p>Klik <span class="uicontrol"> Verwerkingsstatus</span> &gt; <i>&lt;<span class="uicontrol"> profielnaam</span></i> &gt; <span class="uicontrol"> Verwerkingsmodusgeschiedenis</span>. </p> <p> 
     <ul id="ul_B7CC0DF54E004C72B220F928CF223F8E"> 
      <li id="li_2707D8C0D52A44C8BADA4D9AFB5EB2BC">Echt - tijd dat de server van de Data Workbench voor het maken van vragen beschikbaar was. </li> 
      <li id="li_3A3B490D70864A259780FC9FFC9AC15E">Snelle Invoer - deze tijd plus de Snelle tijd van de Fusie is de totale tijd nodig voor de verwerking van de dataset. </li> 
      <li id="li_B754C6DECD924170A15721EA4C942E3D">Snel samenvoegen - totale tijd die nodig is voor het transformeren van de gegevensset. </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Problemen met 's middags diagnosticeren </p> </td> 
   <td colname="col2"> <p>Klik <span class="uicontrol"> Verwerkingsstatus</span> &gt; <i>&lt;<span class="uicontrol"> profielnaam</span></i> &gt; <span class="uicontrol"> Vanaf tijd</span> &gt; <span class="uicontrol"> Bronnen as-of</span>. </p> <p>Door de tijden voor elke bron te controleren, kunt u bepalen welke bron(nen) de algemene evaluatie negatief kan beïnvloeden. Vervolgens kunt u de problemen met die specifieke bronnen aanpakken. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Om te schatten hoe lang een lopende vraag duurt te voltooien </p> </td> 
   <td colname="col2"> <p>Klik <span class="uicontrol"> de Motor van de Uitvoering</span>. </p> <p>Als u het veld <span class="wintitle"> Tijd van gegevenswissing</span> controleert, krijgt u een schatting van hoe lang het duurt voordat een query is voltooid. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Alle profielen weergeven die op deze computer beschikbaar zijn en gegevens over de status weergeven </p> </td> 
   <td colname="col2"> <p>Klik <span class="uicontrol"> Profielen</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>De replicatiestatus weergeven </p> </td> 
   <td colname="col2"> <p>Klik <span class="uicontrol"> Component Status</span>. </p> <p>Controleer de status van de component Replicate. Als de Replicatie loopt, O.K. toont. Als de component Replicate is mislukt, wordt een foutbericht weergegeven. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Als u de status <span class="wintitle"> Rapportserver</span> wilt weergeven voor een <span class="keyword"> Report</span>-computer die verbinding maakt met de Data Workbench-server </p> </td> 
   <td colname="col2"> <p>Klik <span class="uicontrol"> de Status van de Server van het Rapport</span>. </p> <p>Deze sectie van de <span class="wintitle"> Gedetailleerde Status</span> interface omvat een exemplaar van het <span class="filepath"> dossier van het Rapport Server.cfg</span>, informatie over het aantal rapporten die (Huidige Segment) lopen, en informatie over de recentste fout (Laatste Fout). </p> <p>Voor stappen om het <span class="filepath"> dossier van het Rapport Server.cfg</span> uit te geven, zie <i>Gids van het Rapport van de Data Workbench</i>. </p> <p> <p>Opmerking: Als de <span class="wintitle"> sectie van de Status van de Server van het Rapport </span> niet in <span class="wintitle"> Gedetailleerde Status</span> interface verschijnt, kunt u de server van de Data Workbench moeten vormen om <span class="wintitle"> de Status van de Server van het Rapport </span> te tonen. Voor stappen, zie <i>Gids van het Rapport van de Data Workbench</i>. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Informatie over geheugengebruik voor Transformatie weergeven </p> </td> 
   <td colname="col2"> <p>Klik op <span class="uicontrol"> Verwerkingsstatus</span> &gt; <span class="uicontrol"> Transformatie</span>. </p> <p>Voor meer informatie over Transformatie, zie <i>de Gids van de Installatie en van het Beleid van de Producten van de Server</i> en <i>Gids van de Configuratie van de Dataset</i>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Om <span class="wintitle"> Gedetailleerde Status</span> interface als <span class="filepath"> *.cfg</span> dossier te bewaren dat in een tekstredacteur zoals Kladblok kan worden geopend of aan anderen worden verdeeld </p> </td> 
   <td colname="col2"> <p>Klik met de rechtermuisknop op de kop <span class="uicontrol"> Gedetailleerde status</span> en klik op <span class="uicontrol"> Kopie opslaan als</span>. </p> <p>Opmerking:  <p>Klik met de rechtermuisknop op de kop <span class="uicontrol"> Gedetailleerde status</span> en klik op <span class="uicontrol"> Opslaan</span> naar <i>servernaam</i>/Status/ werkt niet in de interface <span class="wintitle"> Gedetailleerde status</span>. Het volgende foutbericht wordt weergegeven: </p> <p>Kan /Status/ niet opslaan. 403 Verboden </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Als u <span class="uicontrol"> rijen per logbron</span> metrisch wilt weergeven </p> </td> 
   <td colname="col2"> <p>Als Rijen per bron van het Logboek metrisch in Gedetailleerde Status moet worden gemeld, dan zou de beheerder van de Data Workbench "Van het Bron Logboek identiteitskaart"moeten bepalen en een unieke naam in het Logboek van het Profiel van de Douane Verwerking.cfg verstrekken. </p> </td> 
  </tr> 
 </tbody> 
</table>
