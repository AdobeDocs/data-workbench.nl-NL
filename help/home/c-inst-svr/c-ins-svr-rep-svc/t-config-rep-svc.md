---
description: U moet de doelServer(s) van het Inzicht vormen om gegevens van de Repeater terug te winnen waarop de originele gebeurtenisgegevens worden opgeslagen.
title: De replicatieservice configureren
uuid: 93931b1d-d1fd-4e98-aa88-f7962eea92a2
exl-id: ae189089-fd5d-41cb-ad10-2b8c2032dafc
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '1005'
ht-degree: 0%

---

# De replicatieservice configureren{#configuring-the-replication-service}

U moet de doelServer(s) van het Inzicht vormen om gegevens van de Repeater terug te winnen waarop de originele gebeurtenisgegevens worden opgeslagen.

Als u het ophalen van gegevens van een [!DNL Repeater] naar een doel [!DNL Insight Server] wilt configureren, moet u het [!DNL Replicate.cfg]-bestand in de map [!DNL Components] op het doel [!DNL Insight Server(s)] bewerken, zoals in de volgende procedure wordt beschreven:

**Om het  [!DNL Replication Service] op de doelmachine te vormen**

1. Klik in [!DNL Insight] op het tabblad [!DNL Admin] > [!DNL Dataset and Profile] op de miniatuur **[!UICONTROL Servers Manager]** om de werkruimte Servers Manager te openen.
1. Klik met de rechtermuisknop op het pictogram van het doel [!DNL Insight Server] dat u wilt configureren en klik op **[!UICONTROL Server Files]**.
1. Klik in [!DNL Server Files Manager] op **[!UICONTROL Components]** om de inhoud ervan weer te geven. Het [!DNL Replicate.cfg]-bestand bevindt zich in deze map.
1. Klik met de rechtermuisknop op het vinkje in de kolom *servernaam* voor [!DNL Replicate.cfg] en klik op **[!UICONTROL Make Local]**. In de kolom [!DNL Temp] wordt een vinkje weergegeven voor [!DNL Replicate.cfg].
1. Klik met de rechtermuisknop op het nieuwe vinkje in de kolom [!DNL Temp] en klik op **[!UICONTROL Open]** > **[!UICONTROL in Insight]**. Het venster [!DNL Replicate.cfg] wordt geopend.
1. Klik in het venster [!DNL Replicate.cfg] op **[!UICONTROL Replicate.cfg]** en **[!UICONTROL component]** om de inhoud ervan weer te geven.
1. Bewerk de parameters met behulp van het volgende voorbeeld en de tabel als hulplijnen:

   ![Stapinfo](assets/cfg_ReplicateFile.png)

   <table id="table_F32D4BFA2D834BBB81DF8F84417CA969"> 
   <thead> 
   <tr> 
      <th colname="col1" class="entry"> Voor deze parameter... </th> 
      <th colname="col2" class="entry"> Opgeven... </th> 
   </tr> 
   </thead>
   <tbody> 
   <tr> 
      <td colname="col1"> Mappen </td> 
      <td colname="col2"> <p>De directory's op de <span class="wintitle"> Repeater</span> die moeten worden gekopieerd (gerepliceerd) naar het doel <span class="keyword"> Insight Server</span>. Met de <span class="wintitle"> Replication Service</span> kunt u meerdere mappen repliceren van één <span class="wintitle"> Repeater</span>. </p> <p>Als u een nieuwe map wilt toevoegen, klikt u met de rechtermuisknop op <span class="uicontrol"> Directories</span> en klikt u op <span class="uicontrol"> Nieuwe map toevoegen</span> &gt; <span class="uicontrol"> Directory</span>. </p> </td> 
   </tr> 
   <tr> 
      <td colname="col1"> Paden samenvoegen </td> 
      <td colname="col2"> <p>Waar of onwaar. De actie die door het plaatsen van deze parameter wordt bepaald hangt van het plaatsen van de parameter Recursive in dit dossier af: 
      <ul id="ul_D4BF3C22FBEF41C290ED938EB57E0F27">
      <li id="li_CB85E5AF9E1B4441AA38C2DB8D4F1800">Als Recursief onwaar is, heeft het afvlakken van paden geen effect. Alleen de bestanden op het hoofdniveau van de map die door de parameter Remote URI wordt opgegeven, worden gerepliceerd. </li>
      <li id="li_8FDB351102344E3995035557445354BB">Als Recursief waar is en Paden afvlakken onwaar is, wordt de mapstructuur van de externe map (<span class="wintitle"> Repeater</span>) exact gedupliceerd in het lokale pad op de doelserver <span class="keyword"> Insight Server</span>. </li>
      <li id="li_3114B191C73744658799E112C61AB004">Als zowel Paden recursief als Afvlakken waar zijn, worden geen submappen gemaakt in het lokale pad. In plaats daarvan worden alle bestanden uit de externe mapstructuur op het hoofdniveau van de lokale map geplaatst. </li>
      </ul></p> <p> <p>Opmerking: Als zowel Paden afvlakken als Recursief zijn ingesteld op true en bestanden in de verschillende submappen op de externe computer dezelfde naam of namen hebben, kan <span class="wintitle"> Replication Service</span> stoppen of kan ander ongedefinieerd gedrag optreden. </p> </p> </td> 
   </tr> 
   <tr> 
      <td colname="col1"> Lokaal pad </td> 
      <td colname="col2">De opslagplaats voor de dossiers die van <span class="wintitle"> Repeater</span> worden teruggewonnen. Het pad is relatief ten opzichte van de installatiemap <span class="keyword"> Insight Server</span>. </td> 
   </tr> 
   <tr> 
      <td colname="col1"> Recursief </td> 
      <td colname="col2"> Waar of onwaar. Indien onwaar worden alleen de bestanden op het hoofdniveau van de map gerepliceerd die door de parameter Remote URI wordt opgegeven. Zie Paden samenvoegen in deze tabel. </td> 
   </tr> 
   <tr> 
      <td colname="col1"> Externe URI </td> 
      <td colname="col2">De URI, met inbegrip van een dossiermasker, om tot <span class="wintitle"> de dossieropslag van de Repeater </span> toegang te hebben. Het <span class="filepath"> Communications.cfg</span> dossier op <span class="wintitle"> Repeater</span> zou moeten worden gevormd zodat de gebeurtenisgegevens kunnen worden betreden gebruikend dit URI. Zie <a href="../../../home/c-inst-svr/c-admin-inst-svr/c-mntr-disk-spc/t-mntr-evt-data-spc.md#task-a54d4bd16b96437f943cd09e5d848440"> Gegevensruimte van gebeurtenissen controleren</a>. </td> 
   </tr> 
   <tr> 
      <td colname="col1"> Server </td> 
      <td colname="col2">Parameters voor de <span class="wintitle"> Repeater</span> waarvan het doel <span class="keyword"> Insight Server</span> de dossiers van gebeurtenisgegevens terugwint. </td> 
   </tr> 
   <tr> 
      <td colname="col1"> Naam </td> 
      <td colname="col2">Optioneel. De naam om <span class="wintitle"> Repeater</span> te identificeren. </td> 
   </tr> 
   <tr> 
      <td colname="col1"> Algemene naam SSL-server </td> 
      <td colname="col2">Alleen vereist als Use SSL is ingesteld op true. Algemene naam van de <span class="wintitle"> Repeater</span> waarop de gebeurtenisgegevens worden opgeslagen. Deze naam moet overeenkomen met de algemene naam die wordt vermeld in het communicatiecertificaat voor de computer. </td> 
   </tr> 
   <tr> 
      <td colname="col1"> Adres </td> 
      <td colname="col2">Hostnaam of numeriek IP-adres van de <span class="wintitle"> Repeater</span> waarop de gebeurtenisgegevens worden opgeslagen. De algemene naam van de server is geen geldige invoer. </td> 
   </tr> 
   <tr> 
      <td colname="col1"> Poort </td> 
      <td colname="col2"> Poort die wordt gebruikt voor gegevensoverdracht. De standaardpoort is 80. </td> 
   </tr> 
   <tr> 
      <td colname="col1"> SSL-clientcertificaat </td> 
      <td colname="col2">Alleen vereist als Use SSL is ingesteld op true. Naam van het licentiecertificaat dat wordt gebruikt om verbinding te maken met de <span class="wintitle"> Repeater</span>. </td> 
   </tr> 
   <tr> 
      <td colname="col1"> SSL gebruiken </td> 
      <td colname="col2"> <p>Bepaalt of SSL voor de gegevenstransmissie wordt gebruikt. De opties zijn true of false en de standaardwaarde is false. </p> <p> <p>Opmerking: Het gebruik van SSL wordt afgeraden omdat dit negatieve gevolgen kan hebben voor de prestaties. Merk op dat SSL niet wordt vereist tenzij het netwerk dat <span class="wintitle"> Repeater</span> aan de doelmachines verbindt onveilig is. </p> </p> </td> 
   </tr> 
   <tr> 
      <td colname="col1"> Eindtijd, Begintijd </td> 
      <td colname="col2"> <p>(Optioneel) Beperkt de set bestanden met gebeurtenisgegevens die naar het doel <span class="keyword"> Insight Server</span> worden gekopieerd tot bestanden die gegevens bevatten die binnen het bereik vallen dat wordt gedefinieerd door Begintijd en Eindtijd. Als Begintijd is ingesteld, worden de bestanden met gebeurtenisgegevens waarin alle logitems van vóór de opgegeven begintijd afkomstig zijn, niet gekopieerd. Als Eindtijd is ingesteld, worden de bestanden met gebeurtenisgegevens waarin alle logitems van de opgegeven of latere tijd niet worden gekopieerd. Als slechts een deel van de gegevens in een bestand binnen het opgegeven bereik valt, wordt het gehele bestand naar de doelcomputer gekopieerd. </p> <p>Adobe raadt u aan een van de volgende notaties te gebruiken: 
      <ul id="ul_AE15A159A4C043398B37AD56FDFD9DCA">
      <li id="li_4DEF0F13D13E43E39CBD1A0F32765F32">1 januari 2013 HH:MM:SS EDT </li>
      <li id="li_E3275312E93D4C1FAA028543DC21B51A">1 januari 2013 UU:MM:SS GMT </li>
      </ul></p> <p> <p>Opmerking: U moet een tijdzone opgeven. De tijdzone wordt niet standaard ingesteld op de systeemtijd als deze niet is opgegeven. Als u wenst om de Tijd van de Besparing van het Daglicht of een gelijkaardig klok-veranderende beleid uit te voeren, moet u <span class="filepath"> .dst</span> dossier opslaan die de aangewezen regels in Base\Dataset\Timezone directory on the <span class="keyword"> de machine van de Server van het Inzicht</span> bevatten. Voor een lijst van gesteunde tijdzoneafkortingen en informatie over het uitvoeren van de Tijd van de Besparing van het Daglicht, zie <a href="../../../home/c-inst-svr/c-time-zn-cds.md#concept-eed5ba32d5d347cf94b76db83b29f211"> Codes van de Tijdzone</a>. </p> </p> <p> <p>Opmerking:  Als u deze instellingen wilt gebruiken, moeten de namen van de bestanden met gebeurtenisgegevens beginnen met een ISO-datum (JJJMMDD) en moet elk bestand gegevens bevatten voor de periode van 24 uur die op die datum om 12.00 uur begint. </p> </p> </td> 
   </tr> 
   </tbody> 
   </table>

1. Sla de wijzigingen op de server op door het volgende te doen:

   1. Klik met de rechtermuisknop **[!UICONTROL (modified)]** boven in het venster en klik **[!UICONTROL Save]**.
   1. Klik in [!DNL Server Files Manager] met de rechtermuisknop op het vinkje voor het bestand in de kolom [!DNL Temp] en selecteer **[!UICONTROL Save to]** > *&lt;**[!UICONTROL server name]**>*.

<!-- <a id="example_A60DE2383CA341DCB512E52DE76ADA89"></a> -->

In dit voorbeeld ziet u hoe bestanden worden gekopieerd als zowel de parameters Paden afvlakken als Recursief zijn ingesteld op true.

Stel dat de externe URI [!DNL /RemoteRoot/] is en het lokale pad  [!DNL E:\LocalRoot\]. Op de computer op afstand ( [!DNL Repeater]) worden de bestanden als volgt geordend:

* [!DNL /RemoteRoot/fileA.txt]
* [!DNL /RemoteRoot/Dir1/fileB.txt]
* [!DNL /RemoteRoot/Dir2/Subdir3/fileC.txt]

Wanneer de replicatie is voltooid, heeft de lokale folder de volgende dossiers:

* [!DNL E:\LocalRoot\fileA.txt]
* [!DNL E:\LocalRoot\fileB.txt]
* [!DNL E:\LocalRoot\fileC.txt]

In de lokale map worden geen submappen gemaakt en worden alle bestanden van de externe mapstructuur op het hoofdniveau van de lokale map geplaatst.

>[!NOTE]
>
>Als bestanden in de verschillende submappen op de externe computer dezelfde naam hebben, kan [!DNL Replication Service] stoppen of kan ander ongedefinieerd gedrag optreden.
