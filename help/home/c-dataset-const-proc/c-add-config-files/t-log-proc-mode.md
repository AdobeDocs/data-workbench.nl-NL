---
description: De verwerking Mode.cfg van het Logboek van het configuratiedossier laat u toe om verwerking van gegevens in een dataset te pauzeren, off-line bronnen te specificeren, of de frequentie te specificeren waarbij de server van de gegevenswerkbank zijn staatsdossiers bewaart.
solution: Analytics
title: Logverwerkingsmodus.cfg
topic: Data workbench
uuid: 1f1e5d8b-80e7-4423-bb03-56e706a1b7b4
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Logverwerkingsmodus.cfg{#log-processing-mode-cfg}

De verwerking Mode.cfg van het Logboek van het configuratiedossier laat u toe om verwerking van gegevens in een dataset te pauzeren, off-line bronnen te specificeren, of de frequentie te specificeren waarbij de server van de gegevenswerkbank zijn staatsdossiers bewaart.

Het aanbrengen van veranderingen in het [!DNL Log Processing Mode.cfg] dossier, met inbegrip van het toevoegen van of het verwijderen van bronnen, veroorzaakt geen opwerking van de gegevens.

**Om het dossier van de Verwerking van het Logboek Mode.cfg voor een datasetprofiel uit te geven**

1. Terwijl het werken in uw datasetprofiel, open [!DNL Profile Manager] en klik **[!UICONTROL Dataset]** om zijn inhoud te tonen.

   >[!NOTE]
   >
   >Als het [!DNL Log Processing Mode.cfg] dossier niet in de folder voor het gewenste profiel wordt gevestigd, moet u dit dossier van de folder van de Basis op de de servermachine van de gegevenswerkbank in de folder van het profiel kopiëren.

   Voor informatie over het openen van en het werken met [!DNL Profile Manager,] zie de Gids van de Gebruiker van de Werkbank van *Gegevens*.

1. Klik het vinkje naast de naam van het configuratiedossier met de rechtermuisknop aan en klik **[!UICONTROL Make Local]**. Een vinkje voor dit dossier verschijnt in de [!DNL User] kolom.
1. Klik het pas gecreëerde vinkje met de rechtermuisknop aan en klik **[!UICONTROL Open]** > **[!UICONTROL from the workbench]**. Het configuratievenster verschijnt.
1. Geef de parameters in het configuratiedossier uit gebruikend de volgende lijst als gids.

   >[!NOTE]
   >
   >Sommige parameters in het [!DNL Log Processing Mode.cfg] dossier hebben namen die omvatten [!DNL Fast Input] of [!DNL Fast Merge]. [!DNL Fast Input]heeft betrekking op de verwerkingsfase van de gegevensset voor de logboekgegevens en is verantwoordelijk voor ongeveer de helft van de totale verwerkingstijd van de gegevensset. [!DNL Fast Merge] verwijst naar de transformatiefase van de gegevensset, alleen wanneer deze wordt voorafgegaan door de verwerking van stamhout. [!DNL Fast Merge] komt niet tijdens retransformation voor die het gevolg is van het wijzigen van een [!DNL Transformation Dataset Configuration] bestand. Zoals [!DNL Fast Input], [!DNL Fast Merge] is ook de oorzaak van ongeveer de helft van de tijd van de datasetverwerking.

   <table id="table_1BF356E21C0E4119A277F40CEC5D7A21"> 
   <thead> 
   <tr> 
      <th colname="col1" class="entry"> Parameter </th> 
      <th colname="col2" class="entry"> Beschrijving </th> 
   </tr> 
   </thead>
   <tbody> 
   <tr> 
      <td colname="col1"> Cloud Bytes </td> 
      <td colname="col2"> <p>Een het stemmen parameter die de efficiency van gegevenstransformatie beïnvloedt. De standaardwaarde is 12800000. </p> <p> <p>Opmerking:  U zou deze waarde niet moeten veranderen zonder Adobe te raadplegen. </p> </p> </td> 
   </tr> 
   <tr> 
      <td colname="col1"> Snelle invoerbeslissingsverhouding </td> 
      <td colname="col2"> <p>Een het stemmen parameter die de verhouding van totaal aan ongelezen logboekbytes specificeert waarbij het systeem de Snelle wijze van de Input <span class="wintitle"> (en later</span> Snelle Fusie <span class="wintitle"></span>) in plaats van het verwerken van gegevens in echt ingaat - tijd. </p> <p> De standaardwaarde is 200, betekenend dat het systeem de Snelle wijze van de Input <span class="wintitle"></span> van wijze in real time ingaat wanneer de ongelezen logboekgegevens bij 1/200th van de totale gegevens zijn. Een hogere beslissingsverhouding maakt het systeem gemakkelijker om de <span class="wintitle"> Snelle wijze van de Input</span> in te gaan, terwijl een lagere verhouding het minder waarschijnlijk maakt om de <span class="wintitle"> Snelle wijze van de Input</span> in te gaan. </p> <p> <p>Opmerking: Het plaatsen van de parameter aan 0 verhindert het systeem de Snelle wijze van de Input <span class="wintitle"></span> bij allen, zelfs voor aanvankelijke verwerking in te gaan. Het plaatsen van de parameter aan 1.1 laat het systeem toe om Snelle Input <span class="wintitle"></span> tijdens aanvankelijke verwerking maar niet voor verdere verwerking in te gaan. Adobe adviseert niet gebruikend waarden tussen 0 en 1.1. Voor meer informatie over het plaatsen van deze parameter, contacteer Adobe. </p> </p> </td> 
   </tr> 
   <tr> 
      <td colname="col1"> Snelle invoer FIFO-bytes </td> 
      <td colname="col2"> <p>Een afstemmende parameter die geheugengebruik en systeemprestaties tijdens gegevensverwerking in evenwicht brengt. De standaardwaarde is 12000000. </p> <p> <p>Opmerking:  U zou deze waarde niet moeten veranderen zonder Adobe te raadplegen. </p> </p> </td> 
   </tr> 
   <tr> 
      <td colname="col1"> Snelle bufferbytes samenvoegen </td> 
      <td colname="col2"> <p>Een afstemmende parameter die geheugengebruik en systeemprestaties tijdens gegevensverwerking in evenwicht brengt. De standaardwaarde is 12800000. </p> <p> <p>Opmerking:  U zou deze waarde niet moeten veranderen zonder Adobe te raadplegen. </p> </p> </td> 
   </tr> 
   <tr> 
      <td colname="col1"> Offline bronnen </td> 
      <td colname="col2"> <p>Masker van de off-line logboekbron. </p> <p> <b> Om een off-line bron te specificeren</b> 
      <ul id="ul_569B90E9A85246F88906FA5444F8A93E"> 
       <li id="li_3EF182CEF4A44106B5267175EC62B9AB"> Klik <span class="uicontrol"> Off-line Bronnen</span>met de rechtermuisknop aan, dan klik <span class="uicontrol"> toevoegen nieuw</span> &gt; <span class="uicontrol"> Bron</span>. </li> 
       <li id="li_E8FBA212F4784B1A830745A90BB3AF90"> In de parameter voor de nieuwe bron, ga het masker van de logboekopeenvolging in. Voor het logboekbronnen van de Sensor met dossiernamen van het formaat YYYJMMDD-<i>SENSORID</i>.vsl, is het masker <i>SENSORID.SENSORID</i> case-sensitive. Voor de bronnen van het logboekdossier, is het masker het koord dat door het Patroon van het <span class="wintitle"> Masker</span>wordt gehaald. Zie <a href="../../../home/c-dataset-const-proc/c-log-proc-config-file/c-log-sources.md#concept-3d4fb817c057447d90f166b1183b461e"> Logbestanden</a>. </li> 
      </ul> </p> <p> Het toevoegen van of het verwijderen van bronnen uit Off-line Bronnen veroorzaken geen opwerking van de dataset. </p> <p> Metingen in de tijd worden gehandhaafd voor de verwerking van de online bronnen van het profiel. Wanneer de off-line bron opnieuw online is, hervat de verwerking van inkomende logboekdossiers voor die bron. </p> <p> Wanneer een bron online terugkomt, zou u het uit Off-line Bronnen moeten verwijderen. Als u dit niet doet, behandelt de server van de gegevenswerkbank de bron als online bron en werkt van tijd bij zolang de bron gegevens verzendt. Als de bron opnieuw off-line gaat, einde van tijdmetingen. </p> </td> 
   </tr> 
   <tr> 
      <td colname="col1"> Gepauzeerd </td> 
      <td colname="col2"> Waar of vals. Als waar, wordt het nieuwe gegeven niet verwerkt in de dataset. De standaardwaarde is vals. </td> 
   </tr> 
   <tr> 
      <td colname="col1"> Real-time vertraging </td> 
      <td colname="col2"> De hoeveelheid tijd in seconden dat de Server van de gegevenswerkbank tussen intervallen van verwerkingsgegevens in de dataset wacht. Wanneer deze waarde aan nul wordt geplaatst, probeert het systeem om omhoog met inkomende gegevens in echt te houden - tijd. De standaardwaarde is nul (0), maar u kunt deze waarde verhogen om de lading van cpu te verminderen. </td> 
   </tr> 
   <tr> 
      <td colname="col1"> Real-time FIFO-bytes </td> 
      <td colname="col2"> <p>De hoeveelheid geheugen in bytes die worden gebruikt om gegevens op te slaan die wachten om in de dataset worden verwerkt. U kunt deze waarde moeten veranderen die op het aantal seconden wordt gebaseerd dat u voor Echte Vertraging van de Tijd specificeert. De standaardwaarde is 1600000. </p> <p> <p>Opmerking:  U zou deze waarde niet moeten veranderen zonder Adobe te raadplegen. </p> </p> </td> 
   </tr> 
   <tr> 
      <td colname="col1"> Interval opslaan (sec) </td> 
      <td colname="col2"> <p>Frequentie waarop de server van de gegevenswerkbank zijn staatsdossiers bewaart. De standaardwaarde is 3600. </p> <p> <p>Opmerking:  U zou deze waarde niet moeten veranderen zonder Adobe te raadplegen. </p> </p> </td> 
   </tr> 
   </tbody> 
   </table>

   Wanneer u het [!DNL Log Processing Mode.cfg] bestand bewerkt in een venster van een gegevensbank, kunt u sneltoetsen gebruiken voor elementaire bewerkingsfuncties, zoals snijden (Ctrl+x), kopiëren (Ctrl+c), plakken (Ctrl+v), ongedaan maken (Ctrl+z), opnieuw uitvoeren (Ctrl+Shift+z), sectie selecteren (klikken+slepen) en alles selecteren (Ctrl+a). Bovendien kunt u de kortere weg gebruiken om tekst van één configuratiedossier () aan een andere te kopiëren en te kleven. [!DNL .cfg]

1. Klik **[!UICONTROL (modified)]** bij de bovenkant van het venster met de rechtermuisknop aan en klik **[!UICONTROL Save]**.
1. Klik in het [!DNL Profile Manager]dialoogvenster met de rechtermuisknop op het vinkje voor het bestand in de [!DNL User] kolom en klik vervolgens op **[!UICONTROL Save to]** > **[!UICONTROL datasetprofile name]**.

   >[!NOTE]
   >
   >Sla het gewijzigde configuratiebestand niet op in een van de interne profielen die door Adobe worden geleverd, omdat uw wijzigingen worden overschreven wanneer u updates voor deze profielen installeert.
