---
description: De manager van de Dossiers van de Server laat u toe om de servercomputers van de Werkbank van Gegevens van om het even welke erkende Werkbank van Gegevens ver te beheren en te beheren door toegang tot alle folders en dossiers in de de installatiefolder van het product, met inbegrip van configuratie en opkijk-up dossiers te verlenen.
solution: Analytics
title: Serverbestandsbeheer
topic: Data workbench
uuid: 62625b9d-587f-4a78-8328-2270869909f8
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Serverbestandsbeheer{#server-files-manager}

De manager van de Dossiers van de Server laat u toe om de servercomputers van de Werkbank van Gegevens van om het even welke erkende Werkbank van Gegevens ver te beheren en te beheren door toegang tot alle folders en dossiers in de de installatiefolder van het product, met inbegrip van configuratie en opkijk-up dossiers te verlenen.

U kunt tot het [!DNL Server Files Manager] gebruiken van het [!DNL Admin] menu toegang hebben evenals door de knoop van de de servercomputer van de Werkbank van Gegevens in met de rechtermuisknop aan te klikken [!DNL Servers Manager] en te klikken **[!UICONTROL Server Files]**.

![](assets/vis_FileManager.png)

>[!NOTE]
>
>U kunt nieuwe managers van serverdossiers tot stand brengen die geselecteerde folders tonen. Zie Nieuwe [serverbestandsbeheerders maken](../../../home/c-get-started/c-intf-anlys-ftrs/c-cstm-prof-files-mgrs/c-new-svr-files-mgrs.md#concept-6e8f63273109443699a8f61b1a2ea816).

De linkerkolom van [!DNL Server Files Manager] lijstdossier en omslagnamen. De controletekens in het centrum en de juiste kolommen wijzen op waar in de dossierstructuur deze folders en dossiers verblijven.

Als een dossier in de de installatiefolder van het product verblijft, bevat de kolom van de *servernaam* (bijvoorbeeld, de server van de Werkbank van Gegevens) een vinkje. Als een dossier op de computer van de gebruiker van de Werkbank van Gegevens in de folder van de de installatiefolder *\ Temp van de Werkbank van* Gegevens verblijft \, bevat de [!DNL Temp] kolom een vinkje. De kleur van de controletekens wijst erop of de dossiers die in verschillende plaatsen verblijven tezelfdertijd werden gewijzigd.

* Een rood vinkje in de kolom van de servernaam wijst erop dat de omslag of het dossier op de de servercomputer van de Werkbank van Gegevens verblijven.
* Een rood vinkje in de [!DNL Temp] kolom wijst erop dat het lokale exemplaar van het dossier of de omslag de zelfde Gewijzigde datum en de tijd zoals het dossier of de omslag op de de servercomputer van de Werkbank van Gegevens hebben.
* Een wit vinkje in de [!DNL Temp] kolom wijst erop dat het dossier of de omslag in de de installatiefolder *\ Temp van de Werkbank van* Gegevens de folder een verschillende Gewijzigde datum en tijd dan het dossier of de omslag op de de servercomputer van de Werkbank van Gegevens hebben.

De volgende grafische shows [!DNL Server Files Manager] met zowel rode als witte vinkjes:

![](assets/vis_FileManager_RedWhiteChecks.png)

**Om folders en dossiers te beheren die gebruiken[!DNL Server Files Manager]**

U kunt gebruiken [!DNL Server Files Manager] om folders en dossiers op een de servercomputer van de Werkbank van Gegevens te manipuleren.

De volgende lijst maakt een lijst van de taken die kunnen worden voltooid gebruikend [!DNL Server Files Manager]:

<table id="table_D217AE5A878542EC8B604812A61819C3"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Om deze taak uit te voeren... </th> 
   <th colname="col2" class="entry"> Doe dit... </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Om de dossiers binnen om het even welke folder te zien </p> </td> 
   <td colname="col2"> <p>Klik de foldernaam om zijn inhoud te bekijken. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Om de inhoud van een folder te verbergen </p> </td> 
   <td colname="col2"> <p>Klik de foldernaam. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Om details over een folder te zien </p> </td> 
   <td colname="col2"> <p>Klik de cel naast de folder in of de de servernaam of kolom van <span class="wintitle"> Temperaturen</span> met de rechtermuisknop aan. U ziet de volgende informatie: </p> 
    <ul id="ul_2DA5C8D0E95F4BCC8F7E25D05F00EB02"> 
     <li id="li_3FDECC14D62543B183C3509C338DF432">Pad. De weg van de folder. </li> 
     <li id="li_9CF3989FD9E2427995F070E043FAD02C">Dir. De naam van de folder. </li> 
     <li id="li_68AAA11907404D0BBF407ECD7CA2E467">Vanaf. De plaats van de folder, Verre of Temp. </li> 
     <li id="li_CB4AEEC89E424868B758465EC0B701B5">Datum (alleen kolom Temperaturen). Aanmaakdatum of de datum van de laatste revisie op de lokale kopie. </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Om details over een dossier te zien </p> </td> 
   <td colname="col2"> <p>Klik het vinkje naast het dossier in of de servernaam of kolom van <span class="wintitle"> Temperatuur met de rechtermuisknop aan</span> . U ziet de volgende informatie: </p> <p> 
     <ul id="ul_C4E6CB86D1774D739B5ECF48AF8DB628"> 
      <li id="li_7A6D39CF8C064FDDAB87F8D4E50FA832">Pad. Het pad van het bestand. </li> 
      <li id="li_9C735B6F0A2541F1992B845359C3685A">Bestand. De naam van het dossier. </li> 
      <li id="li_3EB903E4F4C44A6093732C588F0125EF">Vanaf. De plaats van de folder, Verre of Temp. </li> 
      <li id="li_C1FED4F98F854D5892DBAD9F9E1D47B8">Datum. Datum van de laatste herziening van het dossier. </li> 
      <li id="li_7477C727C62F4406BB2026063E41F2AE">Grootte. De grootte van het dossier. </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Om een folder aan uw lokale computer te downloaden </p> </td> 
   <td colname="col2"> <p>Klik het vinkje in de kolom van de <i>servernaam</i> voor deze folder met de rechtermuisknop aan en klik <span class="uicontrol"> maken Lokale</span>Folder. Een vinkje voor de folder verschijnt in de kolom van <span class="wintitle"> Temperaturen</span> . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Om een dossier aan uw lokale computer te downloaden </p> </td> 
   <td colname="col2"> <p>Klik het vinkje in de kolom van de <i>servernaam</i> voor dit dossier met de rechtermuisknop aan en klik <span class="uicontrol"> maken Lokaal</span>. Een vinkje voor het dossier verschijnt in de kolom van <span class="wintitle"> Temperaturen</span> . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Om het laatste gedeelte van een logboekdossier aan uw lokale computer te downloaden </p> </td> 
   <td colname="col2"> <p>Vermijden hebbend om een volledig logboekdossier (vooral te downloaden wanneer u weet dat de foutenmelding aan het eind van het dossier) dicht is, klik het vinkje in de kolom van de servernaam voor het dossier met de rechtermuisknop aan, klik <span class="uicontrol"> Lusje</span>, en selecteer de grootte van het gedeelte u wilt downloaden. Een vinkje voor het dossier verschijnt in de kolom van <span class="wintitle"> Temperaturen</span> . Het lokale dossier bevat slechts de hoeveelheid gegevens die u, beginnend bij het eind van het dossier specificeerde. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Om een folder te openen </p> </td> 
   <td colname="col2"> <p>Klik het vinkje voor de folder in de kolom van <span class="wintitle"> Temperaturen</span> met de rechtermuisknop aan en klik <span class="uicontrol"> Open</span> &gt; <span class="uicontrol"> omslag</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Om een dossier te openen </p> </td> 
   <td colname="col2"> <p>Klik het vinkje voor het dossier in de kolom van <span class="wintitle"> Temperaturen</span> met de rechtermuisknop aan, klik <span class="uicontrol"> Open</span>, dan klik in de Werkbank <span class="uicontrol"> van</span>Gegevens, <span class="uicontrol"> in Blocnote</span>, of <span class="uicontrol"> omslag</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Sparen een lokaal exemplaar van een folder aan de server van de Werkbank van Gegevens </p> </td> 
   <td colname="col2"> <p>Klik het vinkje voor de folder in de kolom van <span class="wintitle"> Temperaturen</span> met de rechtermuisknop aan en klik <span class="uicontrol"> sparen Folder aan</span> &gt; <i>&lt;<span class="uicontrol"> profielnaam</span>&gt;</i>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Sparen een lokaal exemplaar van een dossier aan de server van de Werkbank van Gegevens </p> </td> 
   <td colname="col2"> <p>Klik met de rechtermuisknop op het vinkje voor het bestand in de kolom <span class="wintitle"> Temperatuur</span> en klik op <span class="uicontrol"> Opslaan naar</span> &gt; <i>&lt;<span class="uicontrol"> profielnaam</span>&gt;</i>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Verwijder een lokaal exemplaar van een folder of een dossier </p> </td> 
   <td colname="col2"> <p>Klik het vinkje voor de folder of het dossier in de kolom van <span class="wintitle"> Temperaturen</span> met de rechtermuisknop aan en de klik <span class="uicontrol"> verwijdert</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Kopieer en plak een dossier als e-mailgehechtheid in Microsoft Outlook </p> </td> 
   <td colname="col2"> <p>Klik het vinkje voor het dossier in de kolom van <span class="wintitle"> Temperaturen</span> met de rechtermuisknop aan en klik <span class="uicontrol"> Exemplaar</span>. In het lichaam van uw e-mail, druk Ctrl+v om het dossier vast te maken. </p> </td> 
  </tr> 
 </tbody> 
</table>

