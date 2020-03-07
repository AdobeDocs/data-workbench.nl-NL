---
description: Informatie over het werken met filtervoorwaarden met inbegrip van het creëren van een nieuwe filter en het toevoegen van een voorwaarde aan een nieuwe filter.
solution: Analytics
title: Werken met filteromstandigheden
topic: Data workbench
uuid: a75fcb21-be5c-452a-8632-86cd78db15cb
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Werken met filteromstandigheden{#working-with-filter-conditions}

Informatie over het werken met filtervoorwaarden met inbegrip van het creëren van een nieuwe filter en het toevoegen van een voorwaarde aan een nieuwe filter.

## Een filter maken {#section-70ba51ae625e493fa3ca70b93ffba406}

* Open een filterredacteur in uw werkruimte door met de rechtermuisknop aan te klikken **[!UICONTROL Add Visualization]** > **[!UICONTROL Filter Editor]**.

   -of-

* Als u reeds een open filterredacteur en een geladen filter hebt, klik de naam van de huidige filter met de rechtermuisknop aan en klik **[!UICONTROL New Blank Filter]**.

## Voeg een voorwaarde aan een nieuwe filter toe {#section-50986db80f1148c489630a8a63fe9f28}

1. Creeer een nieuwe filter. Zorg ervoor dat de Filter van het Ontwerp (in tegenstelling tot Toepassen van Filter) wordt benadrukt, erop wijzend dat u op de wijze van de Filter van het Ontwerp werkt.
1. Klik binnen het gebied met de rechtermuisknop aan duidelijk **[!UICONTROL Right-click to build filter]** en selecteer één van de volgende opties:

   * Om een inclusiefilter tot stand te brengen, klik **[!UICONTROL Include group with]**.
   * Om een uitsluitingsfilter tot stand te brengen, klik **[!UICONTROL Exclude group with]**.

1. Selecteer het type van voorwaarde om aan de filter toe te voegen.

   De volgende lijst verstrekt beschrijvingen van de beschikbare types van filtervoorwaarde:

<table id="table_3B35B57FF32349F09E91E8256FF1672A"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Type toestand </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>werkruimteselectie </p> </td> 
   <td colname="col2"> <p>Bepaalt een filtervoorwaarde die op de selecties in de werkruimte wordt gebaseerd. Deze optie is beschikbaar slechts als één of meerdere selecties binnen de werkruimte bestaan. </p> <p>Om meer informatie over de selectie te bekijken, klik de voorwaarde met de rechtermuisknop aan en klik de Details <span class="uicontrol"></span>van de Mening. Een callout verschijnt voor de voorwaarde. </p> <p>Als u een andere selectie in de werkruimte maakt, kunt u de selectie als subvoorwaarde van de eerste selectie toevoegen. De selecties worden gegroepeerd als logisch ANDs. Daarom moeten de gegevens die door de voorwaarde inbegrepen of uitgesloten zijn aan alle werkruimteselecties voldoen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>ten minste één </p> </td> 
   <td colname="col2">Bepaalt een filtervoorwaarde die op het bestaan van minstens één (om het even welk) element van een afmeting wordt gebaseerd die u kiest. Om de voorwaarde uit te geven, klik de voorwaarde met de rechtermuisknop aan en klik de voorwaarde van de <span class="uicontrol"> Verandering</span> aan. Klik op een van de beschikbare afmetingen. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>formule </p> </td> 
   <td colname="col2"> <p>Bepaalt een filtervoorwaarde die op de formule wordt gebaseerd die u ingaat. U moet de aangewezen syntaxis voor de filter gebruiken om te werken. </p> <p> <p>Opmerking: Voor informatie over de syntaxis voor het bepalen van filters, zie <a href="../../../../home/c-get-started/c-qry-lang-syntx/c-syntx-fltr-exp.md#concept-72f2563f809747a2a3cff7ec72462a15"> Syntaxis voor de Uitdrukkingen</a>van de Filter. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>metrische waarde </p> </td> 
   <td colname="col2"> <p>Bepaalt een filtervoorwaarde die op een metrische waarde wordt gebaseerd die u specificeert. </p> <p>Om de voorwaarde te bepalen, volg deze stappen: 
     <ul id="ul_B69D31258A36460E94535709239CD165"> 
      <li id="li_51317A681E654DD7A9D997DF9F2F22BA">Klik <span class="uicontrol"> [kies niveau]</span> &gt; <span class="uicontrol"> het niveau</span> van de Verandering met de rechtermuisknop aan om het niveau en metrisch van een lijst van afmetingen in uw dataset te selecteren. </li> 
      <li id="li_975E56C335824FDCB988344952DE2E9F">Klik met de rechtermuisknop <span class="uicontrol"> [kies metrisch]</span> &gt; <span class="uicontrol"> Verandering metrisch</span> om metrisch van een lijst van metriek in uw dataset te selecteren. </li> 
      <li id="li_D00B3AF3D8DE472C9D0E9EABBBCAAF61">Klik minder dan met de rechtermuisknop aan en klik de vergelijking <span class="uicontrol"> van de</span> Verandering om één van de beschikbare vergelijkingsvoorwaarden (minder dan, meer dan, precies, minstens, of hoogstens) te selecteren. </li> 
      <li id="li_3334CE0A0950448590E5442AB243F46B">Typ de gewenste waarde voor metrisch. </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>eerste/laatste </p> </td> 
   <td colname="col2"> <p>Bepaalt een filter die u een niveau met een gespecificeerde afmeting laat omvatten of uitsluiten. Bijvoorbeeld, zou u een eerste/laatste filter kunnen specificeren om te omvatten (of uit te sluiten): </p> <p>Zittingen waarvan de laatste paginaweergave een pagina van <span class="filepath"> /hme/rts/Onze tarieven</span>heeft. </p> <p>Om een eerste/laatste voorwaarde te bepalen: 
     <ul id="ul_5AD916DA093844B8AC70127B1EB9BFC8"> 
      <li id="li_AB9FF22ADC8843A79856FED60B9478FA">Kies <span class="uicontrol"> omvatten groep met</span> of <span class="uicontrol"> sluit groep met</span> &gt; <span class="uicontrol"> uit eerst/laatste</span> als nieuwe voorwaarde in de Redacteur van de Filter. </li> 
      <li id="li_92F536FCC2A74DDE97F66C6C45ACC3DC">Klik met de rechtermuisknop <span class="uicontrol"> [kies container]</span> &gt; <span class="uicontrol"> De container</span> van de Verandering om de container te selecteren. </li> 
      <li id="li_1E5DBE04ABC74D84B7C0EF6886CDB5DC">Klik <span class="uicontrol"> eerst</span> of <span class="uicontrol"> het laatst</span> met de rechtermuisknop aan om het niveau te specificeren. </li> 
      <li id="li_8B73EBF5D06E4513B5F0376EB2805D1C">Klik met de rechtermuisknop om een dimensie op te geven en typ vervolgens een waarde in het beschikbare veld. </li> 
      <li id="li_A9E02EF6C6004DDF9B00EB853B6E54EE">Klik <span class="uicontrol"> van toepassing zijn</span>. </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

De filter in dit voorbeeld bepaalt een eerste/laatste filter voor gebruikers de waarvan laatste paginamening was [!DNL /hme/rts/Our Rates]:

![](assets/client-fil2.png)

1. (Facultatief) om meer voorwaarden aan uw filter toe te voegen, klik binnen het gebied van het venster met de rechtermuisknop aan waar u uw filter bouwt en het type van filter (zie Stap 2) en de voorwaardenregel (zie Stap 3) selecteert.

   >[!NOTE]
   >
   >De veelvoudige integratievoorwaarden worden gegroepeerd als logische OFs. De door het filter opgenomen gegevens moeten daarom aan ten minste een van de vastgestelde insluitingsvoorwaarden voldoen. De veelvoudige uitsluitingsvoorwaarden worden ook gegroepeerd als logische OFs. Om te worden uitgesloten, moeten de gegevens aan ten minste één van de uitsluitingsvoorwaarden voldoen.

De filter in dit voorbeeld bepaalt een ondergroep van gegevens die uit filmkijkers (gebruikers) bestaan die veel films schatten maar geen één film een hoge score (4 of 5) gaven. Deze filter (met de juiste naam Zeer moeilijk om te verzoeken) bestaat uit twee omstandigheden:

* **Een metrische waardevoorwaarde:** De voorwaarde omvat gebruikers die minstens 500 films hebben geschat.
* **Een voorwaarde van de werkruimteselectie:** De voorwaarde sluit gebruikers uit die om het even welke film een score van 4 of 5 gaven. De callout vertelt u dat 4 en 5 de elementen waren die uit de dimensie van de Score werden geselecteerd.

![](assets/vis_FilterEditor_ExampleMovies.png)

## Een filtervoorwaarde verwijderen {#section-3092e0d7ac624885b8fe24616279de13}

>[!NOTE]
>
>U kunt voorwaarden schrappen slechts wanneer u op de wijze van de Filter van het Ontwerp werkt. Als u een filter op uw werkruimte hebt toegepast, moet u de Filter van het Ontwerp klikken om op de wijze van de Filter van het Ontwerp terug te komen alvorens u één of meer van de voorwaarden van de filter kunt schrappen.

* Klik **x** links van de voorwaarde om het te schrappen.

## Een voorwaardenbeschrijving bewerken {#section-5015fd2c88ed4b6a95be7f0d53be2db0}

U kunt beschrijvingen aan elk van de voorwaarden toevoegen die u aan een filter toevoegt. U kunt de beschrijvingen desgewenst bewerken of verwijderen.

>[!NOTE]
>
>De beschrijvingen van voorwaarden verschijnen slechts wanneer u op de wijze van de Filter van het Ontwerp werkt.

* Klik de voorwaarde met de rechtermuisknop aan en klik **[!UICONTROL Edit description]**.

   * Om een beschrijving toe te voegen of uit te geven, typ de beschrijving op het [!DNL Edit condition description] gebied. De beschrijving verschijnt in aanhalingstekens boven de voorwaarde in het venster van de filterredacteur.

      ![](assets/vis_FilterEditor_ConditionDescription.png)

* Om een beschrijving te verwijderen, klik **[!UICONTROL Remove description]**. De voorwaarde blijft in het venster van de filterredacteur.

