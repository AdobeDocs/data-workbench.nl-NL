---
description: Met het configuratiebestand Transform Mode.cfg kunt u de verwerking van gegevens in een gegevensset onderbreken, offline bronnen opgeven of de frequentie opgeven waarmee de gegevenswerkbankserver met transformatiefunctionaliteit de statusbestanden opslaat.
title: Het bestand Transform Mode.cfg
uuid: 6e875d02-341a-414c-90e5-aa7fa910ab81
exl-id: 4faca063-3ca9-4c7c-9f04-ba2dfb647a77
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '528'
ht-degree: 0%

---

# Het bestand Transform Mode.cfg{#the-transform-mode-cfg-file}

Met het configuratiebestand Transform Mode.cfg kunt u de verwerking van gegevens in een gegevensset onderbreken, offline bronnen opgeven of de frequentie opgeven waarmee de gegevenswerkbankserver met transformatiefunctionaliteit de statusbestanden opslaat.

Het aanbrengen van wijzigingen in het [!DNL Transform Mode.cfg]-bestand, inclusief het toevoegen of verwijderen van bronnen, leidt niet tot het opnieuw verwerken van de gegevens.

**Het bestand Transform Mode.cfg voor een gegevenssetprofiel bewerken**

1. Wanneer u werkt in het profiel waarvan u de gegevens wilt exporteren, opent u [!DNL Profile Manager] en klikt u **[!UICONTROL Dataset]** om de inhoud van de map weer te geven.
1. Klik met de rechtermuisknop op het vinkje naast [!DNL Transform Mode.cfg] en klik **[!UICONTROL Make Local]**. Er wordt een vinkje voor dit bestand weergegeven in de kolom [!DNL User].
1. Klik met de rechtermuisknop op het nieuwe vinkje en klik op **[!UICONTROL Open]** > **[!UICONTROL from the workbench]**. Het venster [!DNL Transform Mode.cfg] verschijnt.
1. Bewerk de parameters in het configuratiebestand met de volgende tabel als richtlijn:

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
    <td colname="col2"> <p>Masker van de bron van het off-line logboek. </p> <p> Een offline bron opgeven: </p> 
    <ul id="ul_B93F945A697C4882ADE420438712B0B0"> 
     <li id="li_617C04FE9F1C4E998394F224CFEA21F3"> Klik met de rechtermuisknop <span class="uicontrol"> Offlinebronnen</span> en klik <span class="uicontrol"> Nieuwe </span> &gt; <span class="uicontrol"> Bron</span> toevoegen. </li> 
    <li id="li_B263A294D1F14D62BBAA5DBF3B388C38"> In de parameter voor de nieuwe bron, ga het masker van de logboekopeenvolging in. Voor Sensor-logbronnen met bestandsnamen in de notatie <span class="filepath"> YYYYMMDD-SENSORID.vsl</span> is het masker <i>SENSORID.SENSORID</i> hoofdlettergevoelig. Voor logbestandlogbronnen is het masker de tekenreeks die wordt geëxtraheerd door het maskerpatroon <span class="wintitle"> (zie <a href="../../../../home/c-dataset-const-proc/c-log-proc-config-file/c-log-sources.md#concept-3d4fb817c057447d90f166b1183b461e"> Logbestanden</a>).</span> </li> 
    </ul> <p> Het toevoegen of verwijderen van bronnen uit <span class="wintitle"> Offlinebronnen</span> veroorzaakt geen opwerking van de dataset. </p> <p> Met ingang van de tijd worden metingen bijgehouden voor de verwerking van de onlinebronnen van het profiel. Wanneer de offline bron weer online is, wordt de verwerking van binnenkomende logbestanden voor die bron hervat. </p> <p> <p>Opmerking: Wanneer een bron online terugkomt, zou u het uit <span class="wintitle"> Offlinebronnen</span> moeten verwijderen. Als u dit niet doet, behandelt de server van de gegevenswerkbank de bron als online bron en werkt het van tijd bij zolang de bron gegevens verzendt. Als de bron weer offline gaat, worden de metingen bij Aan stopgezet. </p> </p> </td> 
    </tr> 
    <tr> 
    <td colname="col1"> Gepauzeerd </td> 
    <td colname="col2"> Waar of onwaar. Indien waar (true), worden nieuwe gegevens niet naar de dataset verwerkt. De standaardwaarde is false. </td> 
    </tr> 
    <tr> 
    <td colname="col1"> Interval opslaan (sec) </td> 
    <td colname="col2"> <p>De frequentie waarmee de gegevenswerkbankserver waarop de transformatiefunctionaliteit wordt uitgevoerd zijn staatsdossiers bewaart. De standaardwaarde is 3600. </p> <p> <p>Opmerking:  Wijzig deze waarde niet zonder Adobe te raadplegen. </p> </p> </td> 
    </tr> 
    </tbody> 
   </table>

   Wanneer u het [!DNL Transform Mode.cfg]-bestand bewerkt in een werkbankvenster, kunt u sneltoetsen gebruiken voor elementaire bewerkingsfuncties, zoals cut (Ctrl+x), copy (Ctrl+c), paste (Ctrl+v), ongedaan maken (Ctrl+z), opnieuw uitvoeren (Ctrl+Shift+z), sectie selecteren (klikken+slepen) en alles selecteren (Ctrl+a). Bovendien kunt u de kortere weg gebruiken om tekst van één configuratiedossier ( [!DNL .cfg]) aan een ander te kopiëren en te kleven.

1. Klik met de rechtermuisknop **[!UICONTROL (modified)]** boven in het venster en klik **[!UICONTROL Save]**.
1. Als u wilt dat de lokaal aangebrachte wijzigingen van kracht worden, klikt u in [!DNL Profile Manager] met de rechtermuisknop op het vinkje voor de gegevenswerkbank [!DNL Transform Mode.cfg] in de kolom [!DNL User] en vervolgens op **[!UICONTROL Save to]** > **[!UICONTROL profile name]**, waarbij de profielnaam de naam is van het profiel waarvoor u gegevens exporteert. De gegevens worden opnieuw verwerkt nadat het profiel is gesynchroniseerd.

   Zie [Opwerking en wederomzetting](../../../../home/c-dataset-const-proc/c-reproc-retrans/c-unst-reproc-retrans.md) voor informatie over het opnieuw verwerken van uw gegevens voor export.
