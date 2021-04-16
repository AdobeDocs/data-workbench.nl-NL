---
description: Met het configuratiebestand Log Processing Mode.cfg kunt u de verwerking van gegevens in een gegevensset onderbreken, offline bronnen opgeven of de frequentie opgeven waarmee de gegevenswerkbankserver de statusbestanden opslaat.
title: Modus Logverwerking.cfg
uuid: 1f1e5d8b-80e7-4423-bb03-56e706a1b7b4
exl-id: e252b815-e691-490d-9ac9-88bb1fd2c64d
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '956'
ht-degree: 0%

---

# Modus voor logboekverwerking.cfg{#log-processing-mode-cfg}

Met het configuratiebestand Log Processing Mode.cfg kunt u de verwerking van gegevens in een gegevensset onderbreken, offline bronnen opgeven of de frequentie opgeven waarmee de gegevenswerkbankserver de statusbestanden opslaat.

Het aanbrengen van wijzigingen in het [!DNL Log Processing Mode.cfg]-bestand, inclusief het toevoegen of verwijderen van bronnen, leidt niet tot het opnieuw verwerken van de gegevens.

**Het bestand Log Processing Mode.cfg voor een gegevenssetprofiel bewerken**

1. Terwijl het werken in uw datasetprofiel, open [!DNL Profile Manager] en klik **[!UICONTROL Dataset]** om zijn inhoud te tonen.

   >[!NOTE]
   >
   >Als het [!DNL Log Processing Mode.cfg] dossier niet in de folder voor het gewenste profiel wordt gevestigd, moet u dit dossier van de folder van de Basis op de machine van de gegevenswerkbankserver in de folder van het profiel kopiëren.

   Voor informatie over het openen en het werken met [!DNL Profile Manager,] zie *de Gids van de Gebruiker van de Data Workbench*.

1. Klik met de rechtermuisknop op het vinkje naast de naam van het configuratiebestand en klik op **[!UICONTROL Make Local]**. Er wordt een vinkje voor dit bestand weergegeven in de kolom [!DNL User].
1. Klik met de rechtermuisknop op het nieuwe vinkje en klik op **[!UICONTROL Open]** > **[!UICONTROL from the workbench]**. Het configuratievenster wordt weergegeven.
1. Bewerk de parameters in het configuratiebestand met de volgende tabel als richtlijn.

   >[!NOTE]
   >
   >Sommige parameters in het [!DNL Log Processing Mode.cfg] dossier hebben namen die [!DNL Fast Input] of [!DNL Fast Merge] omvatten. [!DNL Fast Input]verwijst naar de verwerkingsfase van het logboek van gegevenssetconstructie en is verantwoordelijk voor ongeveer de helft van de totale tijd van de gegevenssetverwerking. [!DNL Fast Merge] heeft alleen betrekking op de transformatiefase van de constructie van gegevenssets wanneer deze wordt voorafgegaan door de verwerking van het logboek. [!DNL Fast Merge] vindt niet plaats tijdens retransformatie die het resultaat is van het wijzigen van een  [!DNL Transformation Dataset Configuration] bestand. Net als [!DNL Fast Input] is [!DNL Fast Merge] ook verantwoordelijk voor ongeveer de helft van de verwerkingstijd van de gegevensset.

   <table id="table_1BF356E21C0E4119A277F40CEC5D7A21"> 
   <thead> 
   <tr> 
      <th colname="col1" class="entry"> Parameter </th> 
      <th colname="col2" class="entry"> Beschrijving </th> 
   </tr> 
   </thead>
   <tbody> 
   <tr> 
      <td colname="col1"> Cloud-bytes </td> 
      <td colname="col2"> <p>Een afstemmingsparameter die de efficiëntie van de gegevenstransformatie beïnvloedt. De standaardwaarde is 128000000. </p> <p> <p>Opmerking:  Wijzig deze waarde niet zonder Adobe te raadplegen. </p> </p> </td> 
   </tr> 
   <tr> 
      <td colname="col1"> Snelle beslissingsverhouding invoer </td> 
      <td colname="col2"> <p>Een afstemmingsparameter die de verhouding van totaal aan ongelezen logboekbytes specificeert waarbij het systeem <span class="wintitle"> Snelle Input</span> wijze (en later <span class="wintitle"> Snelle Fusie</span>) in plaats van verwerkingsgegevens in echt - tijd ingaat. </p> <p> De standaardwaarde is 200. Dit betekent dat het systeem de modus <span class="wintitle"> Fast Input</span> in real-time activeert wanneer de ongelezen loggegevens op 1/200th van de totale gegevens staan. Een hogere beslissingsverhouding zorgt ervoor dat het systeem sneller de modus <span class="wintitle"> Snelle invoer</span> betreedt, terwijl een lagere verhouding het minder waarschijnlijk maakt dat de modus <span class="wintitle"> Snelle invoer</span> wordt geactiveerd. </p> <p> <p>Opmerking: Als de parameter op 0 wordt ingesteld, kan het systeem de modus <span class="wintitle"> Fast Input</span> helemaal niet activeren, zelfs niet bij eerste verwerking. Door de parameter in te stellen op 1.1 kan het systeem <span class="wintitle"> Fast Input</span> invoeren tijdens de eerste verwerking, maar niet voor volgende verwerking. Adobe raadt u niet aan waarden tussen 0 en 1.1 te gebruiken. Neem contact op met Adobe voor meer informatie over het instellen van deze parameter. </p> </p> </td> 
   </tr> 
   <tr> 
      <td colname="col1"> FIFO-bytes voor snelle invoer </td> 
      <td colname="col2"> <p>Een tuningparameter die het geheugengebruik en de systeemprestaties tijdens gegevensverwerking in evenwicht brengt. De standaardwaarde is 120000000. </p> <p> <p>Opmerking:  Wijzig deze waarde niet zonder Adobe te raadplegen. </p> </p> </td> 
   </tr> 
   <tr> 
      <td colname="col1"> Bufferbytes voor snelle samenvoeging </td> 
      <td colname="col2"> <p>Een tuningparameter die het geheugengebruik en de systeemprestaties tijdens gegevensverwerking in evenwicht brengt. De standaardwaarde is 128000000. </p> <p> <p>Opmerking:  Wijzig deze waarde niet zonder Adobe te raadplegen. </p> </p> </td> 
   </tr> 
   <tr> 
      <td colname="col1"> Offline bronnen </td> 
      <td colname="col2"> <p>Masker van de bron van het off-line logboek. </p> <p> <b> Een offlinebron opgeven</b> 
      <ul id="ul_569B90E9A85246F88906FA5444F8A93E"> 
       <li id="li_3EF182CEF4A44106B5267175EC62B9AB"> Klik met de rechtermuisknop <span class="uicontrol"> Offlinebronnen</span> en klik vervolgens op <span class="uicontrol"> Nieuwe </span> &gt; <span class="uicontrol"> Bron</span> toevoegen. </li> 
       <li id="li_E8FBA212F4784B1A830745A90BB3AF90"> In de parameter voor de nieuwe bron, ga het masker van de logboekopeenvolging in. Voor Sensor-logbronnen met bestandsnamen in de indeling YYYMMDD-<i>SENSORID</i>.vsl is het masker <i>SENSORID.SENSORID</i> hoofdlettergevoelig. Voor logbestandlogbronnen is het masker de tekenreeks die wordt geëxtraheerd door het maskerpatroon <span class="wintitle">. </span> Zie <a href="../../../home/c-dataset-const-proc/c-log-proc-config-file/c-log-sources.md#concept-3d4fb817c057447d90f166b1183b461e"> Logbestanden</a>. </li> 
      </ul> </p> <p> Het toevoegen van of het verwijderen van bronnen uit Offlinebronnen veroorzaakt geen herverwerking van de dataset. </p> <p> Met ingang van de tijd worden metingen bijgehouden voor de verwerking van de onlinebronnen van het profiel. Wanneer de offline bron weer online is, wordt de verwerking van binnenkomende logbestanden voor die bron hervat. </p> <p> Wanneer een bron online terugkomt, zou u het uit Offline Bronnen moeten verwijderen. Als u dit niet doet, behandelt de server van de gegevenswerkbank de bron als online bron en werkt het van tijd bij zolang de bron gegevens verzendt. Als de bron weer offline gaat, worden de metingen bij Aan stopgezet. </p> </td> 
   </tr> 
   <tr> 
      <td colname="col1"> Gepauzeerd </td> 
      <td colname="col2"> Waar of onwaar. Indien waar (true), worden nieuwe gegevens niet naar de dataset verwerkt. De standaardwaarde is false. </td> 
   </tr> 
   <tr> 
      <td colname="col1"> Realtime vertraging </td> 
      <td colname="col2"> De hoeveelheid tijd in seconden dat de Server van de gegevenswerkbank tussen intervallen van verwerkingsgegevens in de dataset wacht. Wanneer deze waarde op nul wordt ingesteld, probeert het systeem inkomende gegevens in real time bij te houden. De standaardwaarde is nul (0), maar u kunt deze waarde verhogen om de CPU-belasting te verminderen. </td> 
   </tr> 
   <tr> 
      <td colname="col1"> Real-time FIFO-bytes </td> 
      <td colname="col2"> <p>De hoeveelheid geheugen in bytes die wordt gebruikt om gegevens op te slaan die wachten om in de dataset te worden verwerkt. U moet deze waarde mogelijk wijzigen op basis van het aantal seconden dat u opgeeft voor Real Time Delay. De standaardwaarde is 16000000. </p> <p> <p>Opmerking:  Wijzig deze waarde niet zonder Adobe te raadplegen. </p> </p> </td> 
   </tr> 
   <tr> 
      <td colname="col1"> Interval opslaan (sec) </td> 
      <td colname="col2"> <p>Frequentie waarop de gegevenswerkbankserver de statusbestanden opslaat. De standaardwaarde is 3600. </p> <p> <p>Opmerking:  Wijzig deze waarde niet zonder Adobe te raadplegen. </p> </p> </td> 
   </tr> 
   </tbody> 
   </table>

   Wanneer u het [!DNL Log Processing Mode.cfg]-bestand bewerkt in een werkbankvenster, kunt u sneltoetsen gebruiken voor elementaire bewerkingsfuncties, zoals cut (Ctrl+x), copy (Ctrl+c), paste (Ctrl+v), ongedaan maken (Ctrl+z), opnieuw uitvoeren (Ctrl+Shift+z), sectie selecteren (klikken+slepen) en alles selecteren (Ctrl+a). Bovendien kunt u de kortere weg gebruiken om tekst van één configuratiedossier ( [!DNL .cfg]) aan een ander te kopiëren en te kleven.

1. Klik met de rechtermuisknop **[!UICONTROL (modified)]** boven in het venster en klik **[!UICONTROL Save]**.
1. Klik in [!DNL Profile Manager] met de rechtermuisknop op het vinkje voor het bestand in de kolom [!DNL User] en klik vervolgens op **[!UICONTROL Save to]** > **[!UICONTROL datasetprofile name]**.

   >[!NOTE]
   >
   >Sla het gewijzigde configuratiebestand niet op in een van de interne profielen die door Adobe worden geleverd, omdat de wijzigingen worden overschreven wanneer u updates voor deze profielen installeert.
