---
description: De gedetailleerde interface van de Status is nuttig voor het oplossen van problemenfouten of andere kwesties met de servercomputers van de Werkbank van Gegevens.
solution: Analytics
title: Gedetailleerde statusinterface
topic: Data workbench
uuid: c4d375d9-431f-4b0a-ba15-b7a10501b2e2
translation-type: tm+mt
source-git-commit: 27600561841db3705f4eee6ff0aeb8890444bbc9

---


# Gedetailleerde statusinterface{#detailed-status-interface}

De gedetailleerde interface van de Status is nuttig voor het oplossen van problemenfouten of andere kwesties met de servercomputers van de Werkbank van Gegevens.

Dit omvat om het even welke [!DNL Transform] profielen die op die computers lopen, of [!DNL Report] computers die cliënten van de server van de Werkbank van Gegevens zijn. U kunt tot [!DNL Master Server] en tot [!DNL Query Server Detailed Status] interfaces door het [!DNL Admin] menu toegang hebben. Om tot de [!DNL Detailed Status] interface voor andere computers, in [!DNL Servers Manager]toegang te hebben, klik de knoop van de server met de rechtermuisknop aan waarvoor u status wilt bekijken en klikken **[!UICONTROL Detailed Status]**. Zie [de Servers Manager](../../../home/c-get-started/c-admin-intrf/c-svrs-mgr.md#concept-2dfff1ca5bce470a8ee854ed57cbe5ba).

Voor meer informatie over de server van de Werkbank van Gegevens, zie de Gids *van de Installatie en van het Beleid van de Producten van de* Server.

![](assets/vis_DetailedStatus.png)

>[!NOTE]
>
>Om de informatie in een [!DNL Detailed Status] interface bij te werken, klik de **[!UICONTROL Detailed Status]** rubriek met de rechtermuisknop aan en klik **[!UICONTROL Refresh]**.

De volgende lijst maakt een lijst van de taken die kunnen worden voltooid gebruikend de [!DNL Detailed Status] interface.

<table id="table_E685F31DCDB343F49FFA1019F2E8DA85"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Om deze taak uit te voeren... </th> 
   <th colname="col2" class="entry"> Doe dit... </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Om elke computercomponent en zijn huidige status weer te geven </p> </td> 
   <td colname="col2"> <p>Klik op <span class="uicontrol"> Component Status</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Om te tonen hoeveel geheugen op de computer wordt gebruikt </p> </td> 
   <td colname="col2"> <p>Klik de Status <span class="uicontrol"> van het</span> Geheugen &gt; <span class="uicontrol"> de Ruimtelading</span>van het Adres. </p> <p>Voor meer informatie over de lading van de controleadresruimte, zie de Gids <i>van de Installatie en van het Beleid van de Producten van de</i>Server. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Om te bepalen of de computer wordt gevormd om de /3GB Schakelaar te gebruiken </p> </td> 
   <td colname="col2"> <p>Klik op <span class="uicontrol"> Geheugenstatus</span> &gt; <span class="uicontrol"> Procesadresruimte</span>. </p> <p>Als het <span class="wintitle"> Totale</span> gebied meer dan 300000 KB toont, wordt uw computer gevormd om de /3GB Schakelaar te gebruiken. </p> <p>Voor meer informatie over de /3GB Schakelaar, zie de Gids <i>van de Installatie en van het Beleid van de Producten van de</i>Server. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Om de hoeveelheid schijfruimte en geheugen te controleren die wordt gebruikt om elke afmeting evenals die op te slaan die wordt gebruikt om de namen van zijn elementen op te slaan </p> </td> 
   <td colname="col2"> <p>Klik op <span class="uicontrol"> Prestaties</span> &gt; <span class="uicontrol"> Afmetingen</span> &gt; <span class="uicontrol"> Schijfgebruik</span> &gt; <i>&lt;<span class="uicontrol"> profielnaam</span>&gt; </i><span class="uicontrol"></span> <span class="uicontrol"></span> <span class="uicontrol"></span> <i><span class="uicontrol"></span></i>of Prestaties &gt; &gt; Afmetingen &gt; Gebruik geheugen&gt; &gt; &gt; Gebruik van geheugen&gt; &lt;naam vanprofiel&gt;. </p> <p>De gebieden van het Gebruik <span class="wintitle"> van de</span> Schijf verstrekken de naam en de hoeveelheid schijfruimte (in MB) wordt vereist om elke afmeting op te slaan die. De grote aantallen van het schijfgebruik kunnen vraagtijden ongunstig beïnvloeden omdat de server van de Werkbank van Gegevens door alle gegevens moet lezen om verwante vragen te voltooien. Het verminderen van het schijfgebruik voor een afmeting kan de tijd verminderen het neemt om verwante vragen te voltooien. </p> <p>De gebieden van het Gebruik <span class="wintitle"> van het</span> Geheugen verstrekken het aantal elementen in elke afmeting en de hoeveelheid geheugen die wordt vereist om de lijst van elementennamen op te slaan. De grote aantallen elementen kunnen de hoeveelheid geheugen ongunstig beïnvloeden dat tijdens een vraag wordt gebruikt omdat de server van de Werkbank van Gegevens door elk element moet lezen. Het verminderen van het aantal elementen in een afmeting kan de tijd verminderen het neemt om verwante vragen te voltooien. </p> <p>Voorbeeld: <code>+&nbsp;Performance
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
   <td colname="col1"> <p>Om het gebruik van cpu voor de stadia binnen de Verwerking en de Transformatie van het Logboek te controleren </p> </td> 
   <td colname="col2"> <p>Klik op <span class="uicontrol"> Prestaties</span> &gt; <span class="uicontrol"> CPU-gebruik</span> &gt; <span class="uicontrol"> Logboekverwerking</span> &gt; <i>&lt;<span class="uicontrol"> profielnaam</span>&gt;</i> <span class="uicontrol"></span> <span class="uicontrol"></span> <span class="uicontrol"></span><span class="uicontrol"></span>of Prestaties &gt; CPU-gebruik &gt; Transformatie &gt; &lt;naam van profiel&gt;. </p> <p>Elk van deze reeksen gebieden voorziet u van het Gebruik van cpu (in seconden) voor elk van de stadia binnen de Verwerking en de Transformatie van het Logboek. </p> <p>Voorbeeld: <code>+&nbsp;Performance
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;-&nbsp;CPU&nbsp;Usage&nbsp;
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;-&nbsp;Log&nbsp;Processing
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;-&nbsp;ProfileName&nbsp;158.9&nbsp;sec
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;-&nbsp;Built-in&nbsp;158.1&nbsp;sec
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;-&nbsp;StageName&nbsp;13.0&nbsp;sec
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;.&nbsp;.&nbsp;.
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;-&nbsp;Log&nbsp;Processing\ProfileName&nbsp;0.8&nbsp;sec
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;-&nbsp;StageName&nbsp;0.8&nbsp;sec</code> </p> <p>De tijd dat het neemt om een vraag te voltooien is gewoonlijk proportioneel aan de totale grootte van elk van uw afmetingen. Na het herzien van de grootte van elke afmeting, kunt u evalueren of een bepaalde afmeting nuttig genoeg is en vaak genoeg gebruikt om de prestatieskosten van de afmeting te rechtvaardigen. Als het niet is, kunt u de dimensie in de Manager <span class="wintitle"> van het</span>Profiel schrappen. Zie<a href="../../../home/c-get-started/c-admin-intrf/c-prof-mgr/c-prof-mgr.md"> Profielbeheer</a>. </p> <p>Een afmeting de waarvan lijst van elementennamen buitensporig groot is (namelijk meer dan 128 MB) kan "uit geheugen"fouten veroorzaken zelfs als het totale gebruik van de adresruimte niet dichtbij de grens is. </p> <p>Ook, als u een de servercluster van de Werkbank van Gegevens gebruikt maar geen gecentraliseerde normalisatie gebruikt, heeft een afmeting de waarvan lijst van elementennamen groot is een significante invloed op het verzenden van geheugenbegrotingen. Voor meer informatie over gecentraliseerde normalisatie, zie de Gids <i>van de Configuratie van de</i>Dataset. Als de hoeveelheid geheugen die wordt vereist om alle lijsten van samengevoegde elementennamen op te slaan meer dan 100 MB over alle servers in de cluster is, zou u "kunnen ontvangen overschrijdt het geheugenbudget"fouten verzenden zelfs wanneer de vraagactiviteit licht is. Bijvoorbeeld, als u een four-server cluster met meer dan 25 MB op elke server hebt die wordt gebruikt om de lijsten van elementennamen op te slaan, zou u fouten kunnen ontvangen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Om de tijd te controleren die in de Verwerking en de Transformatie van het Logboek wordt doorgebracht </p> </td> 
   <td colname="col2"> <p>Klik op <span class="uicontrol"> Prestaties</span> &gt; <span class="uicontrol"> CPU-gebruik</span> &gt; <span class="uicontrol"> Logboekverwerking</span> &gt; <i>&lt;<span class="uicontrol"> profielnaam</span>&gt;</i> <span class="uicontrol"></span> <span class="uicontrol"></span> <span class="uicontrol"></span> <i><span class="uicontrol"></span></i>of Prestaties &gt; CPU-gebruik &gt; Transformatie &gt; &lt; profiel&gt;. </p> <p>Het herzien van de gebieden in deze secties laat u toe om filters en transformaties te identificeren die negatief de hoeveelheid tijd kunnen beïnvloeden nodig voor de Verwerking van het Logboek en de Transformatie. U kunt dan ontwerpbesluiten betreffende individuele filters en transformaties met lange verwerkingstijden maken. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Om het gebruik van de schijfruimte te controleren en vraagsnelheid te verhogen </p> </td> 
   <td colname="col2"> <p>Klik op <span class="uicontrol"> Prestaties</span> &gt; <span class="uicontrol"> Logboekverwerkingsvelden</span> &gt; <i>&lt;<span class="uicontrol"> profielnaam</span>&gt;</i>. </p> <p>Elk lijnpunt in deze sectie beantwoordt aan een parameter in het dossier van het <span class="filepath"> Logboek Processing.cfg</span> . Het herzien van deze gebieden laat u toe om te zien hoeveel geheugen elke parameter gebruikt. U kunt dan ontwerpbesluiten betreffende individuele punten maken die vrij groot zijn. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Om de verstreken tijd van vorige opwerking of transformatie te bepalen </p> </td> 
   <td colname="col2"> <p>Klik <span class="uicontrol"> de Status</span> van de Verwerking &gt; <i>&lt;<span class="uicontrol"> profielnaam</span>&gt;</i> &gt; de Geschiedenis <span class="uicontrol"></span>van de Wijze van de Verwerking. </p> <p> 
     <ul id="ul_B7CC0DF54E004C72B220F928CF223F8E"> 
      <li id="li_2707D8C0D52A44C8BADA4D9AFB5EB2BC">Echt - tijd dat de server van de Werkbank van Gegevens beschikbaar was voor het maken van vragen. </li> 
      <li id="li_3A3B490D70864A259780FC9FFC9AC15E">Snelle Input - deze keer plus de Snelle tijd van de Fusie is de totale tijd nodig voor de verwerking van de dataset. </li> 
      <li id="li_B754C6DECD924170A15721EA4C942E3D">Snelle Fusie - totale tijd nodig voor het omzetten van de dataset. </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Om "van tijd"kwesties te diagnostiseren </p> </td> 
   <td colname="col2"> <p>Klik <span class="uicontrol"> de Status</span> van de Verwerking &gt; <i>&lt;<span class="uicontrol"> profielnaam</span>&gt;</i> &gt; <span class="uicontrol"> vanaf Tijd</span> &gt; <span class="uicontrol"> Bronnen zoals-van</span>. </p> <p>Het herzien van de tijden voor elke bron kan u helpen bepalen welke bron(nen) de algemene as-van-waarde negatief kan beïnvloeden. U kunt dan de problemen met die specifieke bronnen aanpakken. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Om te schatten hoe lang een lopende vraag duurt te voltooien </p> </td> 
   <td colname="col2"> <p>Klik op <span class="uicontrol"> Uitvoeringsengine</span>. </p> <p>Het herzien van het gebied van de Tijd <span class="wintitle"> van de Zeep van</span> Gegevens verstrekt u van een schatting van hoe lang het voor een te voltooien vraag vergt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Om alle profielen weer te geven die op deze computer beschikbaar zijn en details over hun status </p> </td> 
   <td colname="col2"> <p>Klik op <span class="uicontrol"> Profielen</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Om de status van de Replicatie te bekijken </p> </td> 
   <td colname="col2"> <p>Klik op <span class="uicontrol"> Component Status</span>. </p> <p>Controleer de status van de replicaatcomponent. Als de Replicatie loopt, O.K. vertoningen. Als de Replicate-component is mislukt, wordt een foutmelding weergegeven. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Om de status van de Server <span class="wintitle"> van het Rapport voor een computer van het</span> Rapport <span class="keyword"></span> te bekijken die met de server van de Werkbank van Gegevens verbindt </p> </td> 
   <td colname="col2"> <p>Klik de Status <span class="uicontrol"> van de Server van het Rapport</span>. </p> <p>Deze sectie van de <span class="wintitle"> Gedetailleerde interface van de Status</span> omvat een exemplaar van het dossier van het <span class="filepath"> Rapport Server.cfg</span> , informatie over het aantal rapporten die (Huidige Plak) lopen, en informatie over de meest recente fout (Laatste Fout). </p> <p>Voor stappen om het <span class="filepath"> dossier van het Rapport uit te geven Server.cfg</span> , zie de Gids <i>van het Rapport van de Werkbank van</i>Gegevens. </p> <p> <p>Opmerking: Als de sectie van de Status <span class="wintitle"> van de Server van het</span> Rapport niet in de <span class="wintitle"> Gedetailleerde interface van de Status</span> verschijnt, kunt u de server van de Werkbank van Gegevens moeten vormen om de Status <span class="wintitle"> van de Server van het</span>Rapport te tonen. Voor stappen, zie de Gids <i>van het Rapport van de Werkbank van</i>Gegevens. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Om de informatie van het geheugengebruik voor Transformatie te bekijken </p> </td> 
   <td colname="col2"> <p>Klik <span class="uicontrol"> de Status</span> van de Verwerking &gt; <span class="uicontrol"> Transformatie</span>. </p> <p>Voor meer informatie over Transformatie, zie de Gids <i>van de Installatie en van het Beleid van de Producten van de</i> Server en de Gids <i>van de Configuratie van de</i>Dataset. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Om de <span class="wintitle"> Gedetailleerde interface van de Status</span> als <span class="filepath"> *.cfg</span> - dossier te bewaren dat in een tekstredacteur zoals Blocnote kan worden geopend of aan anderen worden verdeeld </p> </td> 
   <td colname="col2"> <p>Klik de <span class="uicontrol"> Gedetailleerde rubriek van de Status</span> met de rechtermuisknop aan en klik <span class="uicontrol"> sparen Exemplaar als</span>. </p> <p>Opmerking:  <p>Klik de <span class="uicontrol"> Gedetailleerde rubriek van de Status</span> met de rechtermuisknop aan en het klikken <span class="uicontrol"> sparen</span> aan <i>servernaam</i>/Status/ werkt niet in de <span class="wintitle"> Gedetailleerde interface van de Status</span> . De volgende foutmelding wordt weergegeven: </p> <p>Kan /Status/ niet opslaan. 403 Verboden </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Om <span class="uicontrol"> Rijen per metrisch Bron</span> van het Logboek te bekijken </p> </td> 
   <td colname="col2"> <p>Als Rijen per Logbron metrisch in Gedetailleerde Status moet worden gemeld, dan zou de Beheerder van de Werkbank van Gegevens "identiteitskaart van de Bron van het Logboek"moeten bepalen en een unieke naam in Logprocessing.cfg van het Profiel van de Douane verstrekken. </p> </td> 
  </tr> 
 </tbody> 
</table>

