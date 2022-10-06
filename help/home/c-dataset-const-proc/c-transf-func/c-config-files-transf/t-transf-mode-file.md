---
description: Met het configuratiebestand Transform Mode.cfg kunt u de verwerking van gegevens in een gegevensset onderbreken, offline bronnen opgeven of de frequentie opgeven waarmee de gegevenswerkbankserver met transformatiefunctionaliteit de statusbestanden opslaat.
title: Het bestand Transform Mode.cfg
uuid: 6e875d02-341a-414c-90e5-aa7fa910ab81
exl-id: 4faca063-3ca9-4c7c-9f04-ba2dfb647a77
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '528'
ht-degree: 0%

---

# Het bestand Transform Mode.cfg{#the-transform-mode-cfg-file}

{{eol}}

Met het configuratiebestand Transform Mode.cfg kunt u de verwerking van gegevens in een gegevensset onderbreken, offline bronnen opgeven of de frequentie opgeven waarmee de gegevenswerkbankserver met transformatiefunctionaliteit de statusbestanden opslaat.

Wijzigingen aanbrengen in de [!DNL Transform Mode.cfg] De gegevens worden niet opnieuw verwerkt, inclusief het toevoegen of verwijderen van bronnen.

**Het bestand Transform Mode.cfg voor een gegevenssetprofiel bewerken**

1. Als u werkt in het profiel waarvan u de gegevens wilt exporteren, opent u het dialoogvenster [!DNL Profile Manager] en klik op **[!UICONTROL Dataset]** om de inhoud van de map weer te geven.
1. Klik met de rechtermuisknop op het vinkje naast [!DNL Transform Mode.cfg] en klik op **[!UICONTROL Make Local]**. Er wordt een vinkje voor dit bestand weergegeven in het dialoogvenster [!DNL User] kolom.
1. Klik met de rechtermuisknop op het nieuwe vinkje en klik op **[!UICONTROL Open]** > **[!UICONTROL from the workbench]**. De [!DNL Transform Mode.cfg] wordt weergegeven.
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
     <li id="li_617C04FE9F1C4E998394F224CFEA21F3"> Klikken met rechtermuisknop <span class="uicontrol"> Offline bronnen</span> en klik op <span class="uicontrol"> Nieuw toevoegen</span> &gt; <span class="uicontrol"> Bron</span>. </li> 
    <li id="li_B263A294D1F14D62BBAA5DBF3B388C38"> In de parameter voor de nieuwe bron, ga het masker van de logboekopeenvolging in. Voor Sensor-logbronnen met bestandsnamen van de indeling <span class="filepath"> JJJMMDD-SENSORID.vsl</span>, het masker is <i>SENSORID.SENSORID</i> is hoofdlettergevoelig. Voor logbestandlogbronnen is het masker de tekenreeks die door de <span class="wintitle"> Maskerpatroon</span> (zie <a href="../../../../home/c-dataset-const-proc/c-log-proc-config-file/c-log-sources.md#concept-3d4fb817c057447d90f166b1183b461e"> Logbestanden</a>). </li> 
    </ul> <p> Bronnen toevoegen aan of verwijderen uit <span class="wintitle"> Offline bronnen</span> de gegevensset niet opnieuw verwerkt. </p> <p> Met ingang van de tijd worden metingen bijgehouden voor de verwerking van de onlinebronnen van het profiel. Wanneer de offline bron weer online is, wordt de verwerking van binnenkomende logbestanden voor die bron hervat. </p> <p> <p>Opmerking: Wanneer een bron weer online komt, moet u deze verwijderen uit <span class="wintitle"> Offline bronnen</span>. Als u dit niet doet, behandelt de server van de gegevenswerkbank de bron als online bron en werkt het van tijd bij zolang de bron gegevens verzendt. Als de bron weer offline gaat, worden de metingen bij Aan stopgezet. </p> </p> </td> 
    </tr> 
    <tr> 
    <td colname="col1"> Gepauzeerd </td> 
    <td colname="col2"> Waar of onwaar. Indien waar (true), worden nieuwe gegevens niet naar de dataset verwerkt. De standaardwaarde is false. </td> 
    </tr> 
    <tr> 
    <td colname="col1"> Interval opslaan (sec) </td> 
    <td colname="col2"> <p>De frequentie waarmee de gegevenswerkbankserver waarop de transformatiefunctionaliteit wordt uitgevoerd zijn staatsdossiers bewaart. De standaardwaarde is 3600. </p> <p> <p>Opmerking: Wijzig deze waarde niet zonder Adobe te raadplegen. </p> </p> </td> 
    </tr> 
    </tbody> 
   </table>

   Bij het bewerken van de [!DNL Transform Mode.cfg] in een werkbankvenster voor gegevens kunt u sneltoetsen gebruiken voor elementaire bewerkingsfuncties, zoals knippen (Ctrl+x), kopiëren (Ctrl+c), plakken (Ctrl+v), Ongedaan maken (Ctrl+z), Opnieuw uitvoeren (Ctrl+Shift+z), Sectie selecteren (klikken+slepen) en Alles selecteren (Ctrl+a). Daarnaast kunt u de sneltoetsen gebruiken om tekst uit één configuratiebestand te kopiëren en te plakken ( [!DNL .cfg]) aan een andere.

1. Klikken met rechtermuisknop **[!UICONTROL (modified)]** boven aan het venster en klik op **[!UICONTROL Save]**.
1. Om de plaatselijk aangebrachte veranderingen van kracht te maken, in [!DNL Profile Manager], klikt u met de rechtermuisknop op het vinkje voor de gegevenswerkbank [!DNL Transform Mode.cfg] in de [!DNL User] kolom, klik vervolgens op **[!UICONTROL Save to]** > **[!UICONTROL profile name]**, waarbij de profielnaam de naam is van het profiel waarvoor u gegevens exporteert. De gegevens worden opnieuw verwerkt nadat het profiel is gesynchroniseerd.

   Voor informatie over het opnieuw verwerken van uw gegevens voor export raadpleegt u [Opwerking en heromzetting](../../../../home/c-dataset-const-proc/c-reproc-retrans/c-unst-reproc-retrans.md).
