---
description: U moet de doelserver(s) van het Inzicht configureren om gegevens op te halen uit de Repeater waarop de oorspronkelijke gebeurtenisgegevens zijn opgeslagen.
solution: Insight
title: De replicatieservice configureren
uuid: 93931b1d-d1fd-4e98-aa88-f7962eea92a2
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# De replicatieservice configureren{#configuring-the-replication-service}

U moet de doelserver(s) van het Inzicht configureren om gegevens op te halen uit de Repeater waarop de oorspronkelijke gebeurtenisgegevens zijn opgeslagen.

Om de herwinning van gegevens van een [!DNL Repeater] aan een doel te vormen [!DNL Insight Server], moet u het [!DNL Replicate.cfg] dossier uitgeven dat in de [!DNL Components] omslag op het doel wordt verstrekt [!DNL Insight Server(s)] zoals die in de volgende procedure wordt beschreven:

**Om het[!DNL Replication Service]op de doelmachine te vormen**

1. In [!DNL Insight], op het [!DNL Admin] > [!DNL Dataset and Profile] lusje, klik de **[!UICONTROL Servers Manager]** duimnagel om de werkruimte van de Manager van Servers te openen.
1. Klik het pictogram van het doel met de rechtermuisknop aan [!DNL Insight Server] u wilt vormen en klikken **[!UICONTROL Server Files]**.
1. In [!DNL Server Files Manager], klik **[!UICONTROL Components]** om zijn inhoud te bekijken. Het [!DNL Replicate.cfg] dossier wordt gevestigd binnen deze folder.
1. Klik het vinkje in de kolom van de *servernaam* voor met de rechtermuisknop aan [!DNL Replicate.cfg] en klik **[!UICONTROL Make Local]**. Een vinkje verschijnt in de [!DNL Temp] kolom voor [!DNL Replicate.cfg].
1. Klik het pas gecreëerde vinkje in de [!DNL Temp] kolom met de rechtermuisknop aan en klik **[!UICONTROL Open]** > **[!UICONTROL in Insight]**. Het [!DNL Replicate.cfg] venster wordt geopend.
1. In het [!DNL Replicate.cfg] venster, klik **[!UICONTROL Replicate.cfg]**, dan **[!UICONTROL component]** om zijn inhoud te bekijken.
1. Geef de parameters uit gebruikend het volgende voorbeeld en de lijst als gidsen:

   ![Stapgegevens](assets/cfg_ReplicateFile.png)

   <table id="table_F32D4BFA2D834BBB81DF8F84417CA969"> 
   <thead> 
   <tr> 
      <th colname="col1" class="entry"> Voor deze parameter... </th> 
      <th colname="col2" class="entry"> Specificeren... </th> 
   </tr> 
   </thead>
   <tbody> 
   <tr> 
      <td colname="col1"> Directoraten </td> 
      <td colname="col2"> <p>De folders op de <span class="wintitle"> Repeater</span> die (herhaald) aan de Server <span class="keyword"> van het doel</span>van het Inzicht moeten worden gekopieerd. De <span class="wintitle"> Dienst</span> van de Replicatie staat de replicatie van veelvoudige folders van één enkele <span class="wintitle"> Repeater</span>toe. </p> <p>Om een nieuwe folder toe te voegen, klik <span class="uicontrol"> Folders</span> met de rechtermuisknop aan en klik <span class="uicontrol"> toevoegen nieuw</span> &gt; <span class="uicontrol"> Folder</span>. </p> </td> 
   </tr> 
   <tr> 
      <td colname="col1"> Flatten paden </td> 
      <td colname="col2"> <p>Waar of vals. De actie die door het plaatsen van deze parameter wordt bepaald hangt van het plaatsen van de Recursieve parameter in dit dossier af: 
      <ul id="ul_D4BF3C22FBEF41C290ED938EB57E0F27">
      <li id="li_CB85E5AF9E1B4441AA38C2DB8D4F1800">Als Recursief vals is, hebben de Afvlakte Wegen geen effect. Slechts worden de dossiers op het hoogste niveau van de folder die door de Verre parameter van URI wordt gespecificeerd herhaald. </li>
      <li id="li_8FDB351102344E3995035557445354BB">Als Recursief waar is en de Afvlakkende Wegen vals is, wordt de folderstructuur van de verre (<span class="wintitle"> Repeater</span>) folder gedupliceerd precies in de lokale weg op de Server <span class="keyword"> van het doel</span>van het Inzicht. </li>
      <li id="li_3114B191C73744658799E112C61AB004">Als zowel de Recursieve als de Afvlakte Wegen waar zijn, worden geen subdirectories gecreeerd in de lokale weg. In plaats daarvan, worden alle dossiers van de verre folderboom geplaatst op het hoogste niveau van de lokale folder. </li>
      </ul></p> <p> <p>Opmerking: Als zowel Flatten Paths als Recursive true zijn en bestanden in de verschillende subdirectories op de externe machine dezelfde naam of namen delen, kan de <span class="wintitle"> Replicatieservice</span> stoppen of kan er een ander ongedefinieerd gedrag optreden. </p> </p> </td> 
   </tr> 
   <tr> 
      <td colname="col1"> Lokaal pad </td> 
      <td colname="col2">De opslagplaats voor de dossiers die van <span class="wintitle"> Repeater</span>worden teruggewonnen. De weg is met betrekking tot de de installatiefolder van de Server <span class="keyword"> van het</span> Inzicht. </td> 
   </tr> 
   <tr> 
      <td colname="col1"> Recursief </td> 
      <td colname="col2"> Waar of vals. Als vals, slechts worden de dossiers op het hoogste niveau van de folder die door de Verre parameter van URI wordt gespecificeerd herhaald. Zie Afvlakken afvlakken in deze tabel. </td> 
   </tr> 
   <tr> 
      <td colname="col1"> Extern URI </td> 
      <td colname="col2">URI, met inbegrip van een dossiermasker, om tot de het dossieropslag van de <span class="wintitle"> Repeater</span> toegang te hebben. Het <span class="filepath"> Communications.cfg</span> - dossier op de <span class="wintitle"> Repeater</span> zou moeten worden gevormd zodat de gebeurtenisgegevens kunnen worden betreden gebruikend dit URI. Zie <a href="../../../home/c-inst-svr/c-admin-inst-svr/c-mntr-disk-spc/t-mntr-evt-data-spc.md#task-a54d4bd16b96437f943cd09e5d848440"> de Ruimte</a>van de Gegevens van de Gebeurtenis van de Controle. </td> 
   </tr> 
   <tr> 
      <td colname="col1"> Server </td> 
      <td colname="col2">De parameters voor de <span class="wintitle"> Repeater</span> waarvan de Server <span class="keyword"> van het doel</span> van het Inzicht de dossiers van gebeurtenisgegevens terugwint. </td> 
   </tr> 
   <tr> 
      <td colname="col1"> Naam </td> 
      <td colname="col2">Optioneel. De naam om de <span class="wintitle"> Repeater</span>te identificeren. </td> 
   </tr> 
   <tr> 
      <td colname="col1"> Algemene naam van SSL-server </td> 
      <td colname="col2">Vereist slechts als SSL van het Gebruik aan waar wordt geplaatst. De gemeenschappelijke naam van de <span class="wintitle"> Repeater</span> waarop het gebeurtenisgegeven wordt opgeslagen. Deze naam moet de gemeenschappelijke naam aanpassen die in het communicatie certificaat voor de machine wordt vermeld. </td> 
   </tr> 
   <tr> 
      <td colname="col1"> Adres </td> 
      <td colname="col2">De naam van de gastheer of numeriek IP adres van de <span class="wintitle"> Repeater</span> waarop het gebeurtenisgegeven wordt opgeslagen. De gemeenschappelijke naam van de server is geen geldige ingang. </td> 
   </tr> 
   <tr> 
      <td colname="col1"> Poort </td> 
      <td colname="col2"> Haven die voor gegevenstransmissie wordt gebruikt. De standaardhaven is 80. </td> 
   </tr> 
   <tr> 
      <td colname="col1"> SSL-clientcertificaat </td> 
      <td colname="col2">Vereist slechts als SSL van het Gebruik aan waar wordt geplaatst. Naam van het vergunningscertificaat dat wordt gebruikt om met de <span class="wintitle"> Repeater</span>te verbinden. </td> 
   </tr> 
   <tr> 
      <td colname="col1"> SSL gebruiken </td> 
      <td colname="col2"> <p>Bepaalt of SSL voor de gegevenstransmissie wordt gebruikt. De opties zijn waar of vals, en de standaardwaarde is vals. </p> <p> <p>Opmerking: Het gebruiken van SSL wordt niet geadviseerd omdat het prestaties negatief kan beïnvloeden. Merk op dat SSL niet wordt vereist tenzij het netwerk dat de Repeater <span class="wintitle"></span> met de doelmachines verbindt onzeker is. </p> </p> </td> 
   </tr> 
   <tr> 
      <td colname="col1"> Eindtijd, Begintijd </td> 
      <td colname="col2"> <p>(Facultatief) beperkt de reeks dossiers van gebeurtenisgegevens die aan de Server <span class="keyword"> van het</span> Inzicht van het doel worden gekopieerd aan die die gegevens in de waaier bevatten die door de Tijd van het Begin en de Tijd van het Eind wordt bepaald. Als de Tijd van het Begin wordt geplaatst, worden de dossiers van gebeurtenisgegevens waarin alle logboekingangen van vroeger dan de gespecificeerde begintijd zijn niet gekopieerd. Als de Tijd van het Eind wordt geplaatst, de dossiers van gebeurtenisgegevens waarin alle logboekingangen van de gespecificeerde tijd of later niet worden gekopieerd. Als slechts een deel van de gegevens in een dossier in de gespecificeerde waaier is, dan wordt het volledige dossier gekopieerd aan de doelmachine. </p> <p>Adobe adviseert gebruikend één van de volgende formaten voor de tijd: 
      <ul id="ul_AE15A159A4C043398B37AD56FDFD9DCA">
      <li id="li_4DEF0F13D13E43E39CBD1A0F32765F32">1 januari 2013 UUR:MM.:SS EDT </li>
      <li id="li_E3275312E93D4C1FAA028543DC21B51A">1 januari 2013 UUR:MM:SS GMT </li>
      </ul></p> <p> <p>Opmerking: U moet een tijdzone specificeren. De tijdzone blijft niet in gebreke aan systeemtijd indien niet gespecificeerd. Als u wenst om de Tijd van de Besparing van het Daglicht of een gelijkaardig klok-verschuivend beleid uit te voeren, moet u het <span class="filepath"> .dst</span> dossier bewaren dat de aangewezen regels in de machine van de Server <span class="keyword"> van het Inzicht van Base\Dataset\Timezone directory on the</span> bevat. Voor een lijst van gesteunde afkortingen van de tijdzone en informatie over het uitvoeren van de Tijd van de Besparing van het Daglicht, zie de Codes <a href="../../../home/c-inst-svr/c-time-zn-cds.md#concept-eed5ba32d5d347cf94b76db83b29f211"> van de</a>Tijdzone. </p> </p> <p> <p>Opmerking:  Om deze montages te gebruiken, moeten de namen van de dossiers van gebeurtenisgegevens met een datum van ISO (JJJJMMDD) beginnen, en elk dossier moet gegevens voor de periode bevatten van 24 uur die bij 12 AM GMT op die datum begint. </p> </p> </td> 
   </tr> 
   </tbody> 
   </table>

1. Sparen uw veranderingen in de server door het volgende te doen:

   1. Klik **[!UICONTROL (modified)]** bij de bovenkant van het venster met de rechtermuisknop aan en klik **[!UICONTROL Save]**.
   1. Klik in het [!DNL Server Files Manager]dialoogvenster met de rechtermuisknop op het vinkje voor het bestand in de [!DNL Temp] kolom en selecteer **[!UICONTROL Save to]** > *&lt;**[!UICONTROL server name]**>*.

<!-- <a id="example_A60DE2383CA341DCB512E52DE76ADA89"></a> -->

Dit voorbeeld illustreert hoe de dossiers worden gekopieerd als zowel de Afvlakkende Wegen als de Recursieve parameters aan waar worden geplaatst.

Veronderstel Verre URI is [!DNL /RemoteRoot/] en de Lokale Weg is [!DNL E:\LocalRoot\]. Op het verre ( [!DNL Repeater]) systeem, worden de dossiers georganiseerd als volgt:

* [!DNL /RemoteRoot/fileA.txt]
* [!DNL /RemoteRoot/Dir1/fileB.txt]
* [!DNL /RemoteRoot/Dir2/Subdir3/fileC.txt]

Wanneer de replicatie volledig is, heeft de lokale folder de volgende dossiers:

* [!DNL E:\LocalRoot\fileA.txt]
* [!DNL E:\LocalRoot\fileB.txt]
* [!DNL E:\LocalRoot\fileC.txt]

In de lokale folder, worden geen subdirectories gecreeerd, en alle dossiers van de verre folderboom worden geplaatst op het hoogste niveau van de lokale folder.

>[!NOTE]
>
>Als bestanden in de verschillende subdirectories op de externe machine dezelfde naam (namen) hebben, [!DNL Replication Service] kan het stoppen of kan er een ander ongedefinieerd gedrag optreden.
