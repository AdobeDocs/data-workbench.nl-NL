---
description: Met de Server Files Manager kunt u vanaf elke geoorloofde Data Workbench op afstand de servercomputers van de Data Workbench beheren en beheren door toegang te verlenen tot alle mappen en bestanden in de installatiemap van het product, inclusief configuratie- en opzoekbestanden.
title: Serverbestandsbeheer
uuid: 62625b9d-587f-4a78-8328-2270869909f8
exl-id: 9ac7e95d-47e5-4862-a16e-bee0df1d3d15
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '856'
ht-degree: 0%

---

# Serverbestandsbeheer{#server-files-manager}

{{eol}}

Met de Server Files Manager kunt u vanaf elke geoorloofde Data Workbench op afstand de servercomputers van de Data Workbench beheren en beheren door toegang te verlenen tot alle mappen en bestanden in de installatiemap van het product, inclusief configuratie- en opzoekbestanden.

U hebt toegang tot de [!DNL Server Files Manager] met de [!DNL Admin] en door met de rechtermuisknop op het knooppunt van de Data Workbench-servercomputer in het deelvenster [!DNL Servers Manager] en klikken **[!UICONTROL Server Files]**.

![](assets/vis_FileManager.png)

>[!NOTE]
>
>U kunt nieuwe serverbestandsbeheerders maken die geselecteerde mappen weergeven. Zie [Nieuwe beheerders voor serverbestanden maken](../../../home/c-get-started/c-intf-anlys-ftrs/c-cstm-prof-files-mgrs/c-new-svr-files-mgrs.md#concept-6e8f63273109443699a8f61b1a2ea816).

De linkerkolom van [!DNL Server Files Manager] bevat een lijst met bestands- en mapnamen. De vinkjes in het midden en in de rechterkolom geven aan waar in de bestandsstructuur deze mappen en bestanden zich bevinden.

Als een bestand zich in de installatiemap van het product bevindt, gaat u naar *servernaam* (bijvoorbeeld Data Workbench server) bevat een vinkje. Als een bestand zich op de computer van de gebruiker van de Data Workbench in de *Installatiemap Data Workbench*\Temp, de map [!DNL Temp] bevat een vinkje. De kleur van de vinkjes geeft aan of de bestanden die zich op verschillende locaties bevinden, tegelijkertijd zijn gewijzigd.

* Een rood vinkje in de kolom van de servernaam wijst erop dat de omslag of het dossier op de de servercomputer van de Data Workbench verblijft.
* Een rood vinkje in de [!DNL Temp] geeft aan dat de lokale kopie van het bestand of de map dezelfde datum en tijd heeft als het bestand of de map op de servercomputer van de Data Workbench.
* Een wit vinkje in de [!DNL Temp] geeft aan dat het bestand of de map in de *Installatiemap Data Workbench*\Temp-map heeft een andere datum en tijd met een wijziging dan het bestand of de map op de servercomputer van de Data Workbench.

De volgende afbeelding toont de [!DNL Server Files Manager] met zowel rode als witte vinkjes:

![](assets/vis_FileManager_RedWhiteChecks.png)

**Mappen en bestanden beheren met de opdracht[!DNL Server Files Manager]**

U kunt de [!DNL Server Files Manager] om mappen en bestanden op een Data Workbench-servercomputer te bewerken.

In de volgende tabel worden de taken weergegeven die u kunt voltooien met de opdracht [!DNL Server Files Manager]:

<table id="table_D217AE5A878542EC8B604812A61819C3"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Deze taak uitvoeren... </th> 
   <th colname="col2" class="entry"> Doe dit... </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>De bestanden in een map weergeven </p> </td> 
   <td colname="col2"> <p>Klik op de mapnaam om de inhoud ervan weer te geven. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>De inhoud van een map verbergen </p> </td> 
   <td colname="col2"> <p>Klik op de mapnaam. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Details over een map weergeven </p> </td> 
   <td colname="col2"> <p>Klik met de rechtermuisknop op de cel naast de map in de servernaam of <span class="wintitle"> Temperatuur</span> kolom. U ziet de volgende informatie: </p> 
    <ul id="ul_2DA5C8D0E95F4BCC8F7E25D05F00EB02"> 
     <li id="li_3FDECC14D62543B183C3509C338DF432">Pad. Het pad van de map. </li> 
     <li id="li_9CF3989FD9E2427995F070E043FAD02C">Dir. De naam van de map. </li> 
     <li id="li_68AAA11907404D0BBF407ECD7CA2E467">Van. De locatie van de directory, Extern of Temperatuur. </li> 
     <li id="li_CB4AEEC89E424868B758465EC0B701B5">Datum (alleen kolom Temperatuur). Aanmaakdatum of de datum van de laatste revisie van de lokale kopie. </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Details over een bestand weergeven </p> </td> 
   <td colname="col2"> <p>Klik met de rechtermuisknop op het vinkje naast het bestand in de servernaam of <span class="wintitle"> Temperatuur</span> kolom. U ziet de volgende informatie: </p> <p> 
     <ul id="ul_C4E6CB86D1774D739B5ECF48AF8DB628"> 
      <li id="li_7A6D39CF8C064FDDAB87F8D4E50FA832">Pad. Het pad van het bestand. </li> 
      <li id="li_9C735B6F0A2541F1992B845359C3685A">Bestand. De naam van het bestand. </li> 
      <li id="li_3EB903E4F4C44A6093732C588F0125EF">Van. De locatie van de directory, Extern of Temperatuur. </li> 
      <li id="li_C1FED4F98F854D5892DBAD9F9E1D47B8">Datum. Datum van de laatste revisie van het bestand. </li> 
      <li id="li_7477C727C62F4406BB2026063E41F2AE">Grootte. De grootte van het bestand. </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Een map downloaden naar uw lokale computer </p> </td> 
   <td colname="col2"> <p>Klik met de rechtermuisknop op het vinkje in het dialoogvenster <i>servernaam</i> kolom voor deze map en klik op <span class="uicontrol"> Directory lokaal maken</span>. Er verschijnt een vinkje voor de map in het dialoogvenster <span class="wintitle"> Temperatuur</span> kolom. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Een bestand downloaden naar uw lokale computer </p> </td> 
   <td colname="col2"> <p>Klik met de rechtermuisknop op het vinkje in het dialoogvenster <i>servernaam</i> kolom voor dit bestand en klik op <span class="uicontrol"> Lokaal maken</span>. Er verschijnt een vinkje voor het bestand in het dialoogvenster <span class="wintitle"> Temperatuur</span> kolom. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Het laatste gedeelte van een logbestand downloaden naar uw lokale computer </p> </td> 
   <td colname="col2"> <p>Als u wilt voorkomen dat u een volledig logbestand moet downloaden (met name wanneer u weet dat het foutbericht zich bijna aan het einde van het bestand bevindt), klikt u met de rechtermuisknop op het vinkje in de kolom met de servernaam voor het bestand en klikt u op <span class="uicontrol"> Staart</span>en selecteert u de grootte van het gedeelte dat u wilt downloaden. Er verschijnt een vinkje voor het bestand in het dialoogvenster <span class="wintitle"> Temperatuur</span> kolom. Het lokale bestand bevat alleen de hoeveelheid gegevens die u hebt opgegeven, vanaf het einde van het bestand. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Een directory openen </p> </td> 
   <td colname="col2"> <p>Klik met de rechtermuisknop op het vinkje voor de map in het dialoogvenster <span class="wintitle"> Temperatuur</span> kolom en klik op <span class="uicontrol"> Openen</span> &gt; <span class="uicontrol"> map</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Een bestand openen </p> </td> 
   <td colname="col2"> <p>Klik met de rechtermuisknop op het vinkje voor het bestand in het dialoogvenster <span class="wintitle"> Temperatuur</span> kolom, klikt u op <span class="uicontrol"> Openen</span>en klik vervolgens op <span class="uicontrol"> Data Workbench</span>, <span class="uicontrol"> in Kladblok</span>, of <span class="uicontrol"> map</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Een lokale kopie van een map opslaan op de Data Workbench-server </p> </td> 
   <td colname="col2"> <p>Klik met de rechtermuisknop op het vinkje voor de map in het dialoogvenster <span class="wintitle"> Temperatuur</span> kolom en klik op <span class="uicontrol"> Map opslaan naar</span> &gt; <i>&lt;<span class="uicontrol"> profielnaam</span>&gt;</i>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Een lokale kopie van een bestand opslaan op de Data Workbench-server </p> </td> 
   <td colname="col2"> <p>Klik met de rechtermuisknop op het vinkje voor het bestand in het dialoogvenster <span class="wintitle"> Temperatuur</span> kolom en klik op <span class="uicontrol"> Opslaan naar</span> &gt; <i>&lt;<span class="uicontrol"> profielnaam</span>&gt;</i>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Een lokale kopie van een map of bestand verwijderen </p> </td> 
   <td colname="col2"> <p>Klik met de rechtermuisknop op het vinkje voor de map of het bestand in het dialoogvenster <span class="wintitle"> Temperatuur</span> kolom en klik op <span class="uicontrol"> Verwijderen</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Een bestand kopiëren en plakken als e-mailbijlage in Microsoft Outlook </p> </td> 
   <td colname="col2"> <p>Klik met de rechtermuisknop op het vinkje voor het bestand in het dialoogvenster <span class="wintitle"> Temperatuur</span> kolom en klik op <span class="uicontrol"> Kopiëren</span>. Druk in de tekst van de e-mail op Ctrl+v om het bestand bij te voegen. </p> </td> 
  </tr> 
 </tbody> 
</table>
