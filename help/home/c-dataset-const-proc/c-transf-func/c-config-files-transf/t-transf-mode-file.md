---
description: De transformatie Mode.cfg van het configuratiedossier laat u toe om verwerking van gegevens in een dataset te pauzeren, off-line bronnen te specificeren, of de frequentie te specificeren waarbij de server die van de gegevenswerkbank transformatiefunctionaliteit in werking stelt zijn staatsdossiers bewaart.
solution: Analytics
title: Het dossier van de Transformatie Mode.cfg
topic: Data workbench
uuid: 6e875d02-341a-414c-90e5-aa7fa910ab81
translation-type: tm+mt
source-git-commit: 27600561841db3705f4eee6ff0aeb8890444bbc9

---


# Het dossier van de Transformatie Mode.cfg{#the-transform-mode-cfg-file}

De transformatie Mode.cfg van het configuratiedossier laat u toe om verwerking van gegevens in een dataset te pauzeren, off-line bronnen te specificeren, of de frequentie te specificeren waarbij de server die van de gegevenswerkbank transformatiefunctionaliteit in werking stelt zijn staatsdossiers bewaart.

Het aanbrengen van veranderingen in het [!DNL Transform Mode.cfg] dossier, met inbegrip van het toevoegen van of het verwijderen van bronnen, veroorzaakt geen opwerking van de gegevens.

**Om het dossier van de Transformatie Mode.cfg voor een datasetprofiel uit te geven**

1. Terwijl het werken in het profiel de waarvan gegevens u wilt uitvoeren, opent [!DNL Profile Manager] en klikt om de inhoud van de folder **[!UICONTROL Dataset]** te tonen.
1. Klik het vinkje naast met de rechtermuisknop aan [!DNL Transform Mode.cfg] en klik **[!UICONTROL Make Local]**. Een vinkje voor dit dossier verschijnt in de [!DNL User] kolom.
1. Klik het pas gecreëerde vinkje met de rechtermuisknop aan en klik **[!UICONTROL Open]** > **[!UICONTROL from the workbench]**. Het [!DNL Transform Mode.cfg] venster wordt weergegeven.
1. Geef de parameters in het configuratiedossier uit gebruikend de volgende lijst als gids:

   <table id="table_9FC00BD54FD8439DA17AEF61AC2ACD50"> 
    <thead> 
    <tr> 
    <th colname="col1" class="entry"> Parameter </th> 
    <th colname="col2" class="entry"> Beschrijving </th> 
    </tr> 
    </thead>
    <tbody> 
    <tr> 
    <td colname="col1"> Offline bronnen </td> 
    <td colname="col2"> <p>Masker van de off-line logboekbron. </p> <p> Om een off-line bron te specificeren: </p> 
    <ul id="ul_B93F945A697C4882ADE420438712B0B0"> 
     <li id="li_617C04FE9F1C4E998394F224CFEA21F3"> Klik <span class="uicontrol"> Off-line Bronnen</span> met de rechtermuisknop aan en de klik <span class="uicontrol"> voegt nieuw</span> &gt; <span class="uicontrol"> Bron</span>toe. </li> 
    <li id="li_B263A294D1F14D62BBAA5DBF3B388C38"> In de parameter voor de nieuwe bron, ga het masker van de logboekopeenvolging in. Voor het logboekbronnen van de Sensor met dossiernamen van het formaat <span class="filepath"> JJJJMMDD-SENSORID.vsl</span>, is het masker <i>SENSORID.SENSORID</i> case-sensitive. Voor de bronnen van het logboekdossier, is het masker het koord dat door het Patroon <span class="wintitle"> van het</span> Masker wordt gehaald (zie de Dossiers <a href="../../../../home/c-dataset-const-proc/c-log-proc-config-file/c-log-sources.md#concept-3d4fb817c057447d90f166b1183b461e"> van het</a>Logboek). </li> 
    </ul> <p> Het toevoegen van of het verwijderen van bronnen uit <span class="wintitle"> Off-line Bronnen</span> veroorzaakt geen opwerking van de dataset. </p> <p> Metingen in de tijd worden gehandhaafd voor de verwerking van de online bronnen van het profiel. Wanneer de off-line bron opnieuw online is, hervat de verwerking van inkomende logboekdossiers voor die bron. </p> <p> <p>Opmerking: Wanneer een bron online terugkomt, zou u het uit <span class="wintitle"> Offline Bronnen</span>moeten verwijderen. Als u dit niet doet, behandelt de server van de gegevenswerkbank de bron als online bron en werkt van tijd bij zolang de bron gegevens verzendt. Als de bron opnieuw off-line gaat, einde van tijdmetingen. </p> </p> </td> 
    </tr> 
    <tr> 
    <td colname="col1"> Gepauzeerd </td> 
    <td colname="col2"> Waar of vals. Als waar, wordt het nieuwe gegeven niet verwerkt in de dataset. De standaardwaarde is vals. </td> 
    </tr> 
    <tr> 
    <td colname="col1"> Interval opslaan (sec) </td> 
    <td colname="col2"> <p>De frequentie waarbij de server van de gegevenswerkbank waarop de transformatiefunctionaliteit loopt bewaart zijn staatsdossiers. De standaardwaarde is 3600. </p> <p> <p>Opmerking:  U zou deze waarde niet moeten veranderen zonder Adobe te raadplegen. </p> </p> </td> 
    </tr> 
    </tbody> 
   </table>

   Wanneer u het [!DNL Transform Mode.cfg] bestand bewerkt in een venster van een gegevensbank, kunt u sneltoetsen gebruiken voor elementaire bewerkingsfuncties, zoals snijden (Ctrl+x), kopiëren (Ctrl+c), plakken (Ctrl+v), ongedaan maken (Ctrl+z), opnieuw uitvoeren (Ctrl+Shift+z), sectie selecteren (klikken+slepen) en alles selecteren (Ctrl+a). Bovendien kunt u de kortere weg gebruiken om tekst van één configuratiedossier () aan een andere te kopiëren en te kleven. [!DNL .cfg]

1. Klik **[!UICONTROL (modified)]** bij de bovenkant van het venster met de rechtermuisknop aan en klik **[!UICONTROL Save]**.
1. Om de plaatselijk aangebrachte veranderingen van kracht te maken, in [!DNL Profile Manager], klik het vinkje voor de gegevenswerkbank [!DNL Transform Mode.cfg] in de [!DNL User] kolom met de rechtermuisknop aan, dan klik **[!UICONTROL Save to]** > **[!UICONTROL profile name]**, waar de profielnaam de naam van het profiel is waarvoor u gegevens uitvoert. De opwerking van de gegevens begint na synchronisatie van het profiel.

   Voor informatie over het opnieuw verwerken van uw gegevens voor de uitvoer, zie [Opwerking en Herschikking](../../../../home/c-dataset-const-proc/c-reproc-retrans/c-unst-reproc-retrans.md).
