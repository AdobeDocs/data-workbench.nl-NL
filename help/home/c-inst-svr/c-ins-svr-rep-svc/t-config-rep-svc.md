---
description: U moet de doelServer(s) van het Inzicht vormen om gegevens van de Repeater terug te winnen waarop de originele gebeurtenisgegevens worden opgeslagen.
title: De replicatieservice configureren
uuid: 93931b1d-d1fd-4e98-aa88-f7962eea92a2
exl-id: ae189089-fd5d-41cb-ad10-2b8c2032dafc
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '1006'
ht-degree: 0%

---

# De replicatieservice configureren{#configuring-the-replication-service}

{{eol}}

U moet de doelServer(s) van het Inzicht vormen om gegevens van de Repeater terug te winnen waarop de originele gebeurtenisgegevens worden opgeslagen.

Om de terugwinning van gegevens van a te vormen [!DNL Repeater] naar een doel [!DNL Insight Server], moet u de [!DNL Replicate.cfg] in het [!DNL Components] map op het doel [!DNL Insight Server(s)] zoals beschreven in de volgende procedure:

**Om het [!DNL Replication Service] op de doelcomputer**

1. In [!DNL Insight]over de [!DNL Admin] > [!DNL Dataset and Profile] klikt u op de knop **[!UICONTROL Servers Manager]** om de werkruimte van Servers Manager te openen.
1. Klik met de rechtermuisknop op het pictogram van het doel [!DNL Insight Server] u wilt vormen en klikken **[!UICONTROL Server Files]**.
1. In de [!DNL Server Files Manager], klikt u op **[!UICONTROL Components]** om de inhoud te bekijken. De [!DNL Replicate.cfg] bestand bevindt zich in deze map.
1. Klik met de rechtermuisknop op het vinkje in het dialoogvenster *servernaam* kolom voor [!DNL Replicate.cfg] en klik op **[!UICONTROL Make Local]**. Er verschijnt een vinkje in het dialoogvenster [!DNL Temp] kolom voor [!DNL Replicate.cfg].
1. Klik met de rechtermuisknop op het nieuwe vinkje in het dialoogvenster [!DNL Temp] kolom en klik op **[!UICONTROL Open]** > **[!UICONTROL in Insight]**. De [!DNL Replicate.cfg] wordt geopend.
1. In de [!DNL Replicate.cfg] venster, klikt u op **[!UICONTROL Replicate.cfg]** vervolgens **[!UICONTROL component]** om de inhoud te bekijken.
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
      <td colname="col2"> <p>De directory's op de <span class="wintitle"> Repeater</span> die naar het doel moeten worden gekopieerd (gerepliceerd) <span class="keyword"> Insight Server</span>. De <span class="wintitle"> Replicatieservice</span> staat de replicatie van veelvoudige folders van één toe <span class="wintitle"> Repeater</span>. </p> <p>Als u een nieuwe map wilt toevoegen, klikt u met de rechtermuisknop <span class="uicontrol"> Mappen</span> en klik op <span class="uicontrol"> Nieuw toevoegen</span> &gt; <span class="uicontrol"> Map</span>. </p> </td> 
   </tr> 
   <tr> 
      <td colname="col1"> Paden samenvoegen </td> 
      <td colname="col2"> <p>Waar of onwaar. De actie die door het plaatsen van deze parameter wordt bepaald hangt van het plaatsen van de parameter Recursive in dit dossier af: 
      <ul id="ul_D4BF3C22FBEF41C290ED938EB57E0F27">
      <li id="li_CB85E5AF9E1B4441AA38C2DB8D4F1800">Als Recursief onwaar is, heeft het afvlakken van paden geen effect. Alleen de bestanden op het hoofdniveau van de map die door de parameter Remote URI wordt opgegeven, worden gerepliceerd. </li>
      <li id="li_8FDB351102344E3995035557445354BB">Als Recursief waar is en Paden samenvoegen onwaar is, wordt de mapstructuur van het externe (<span class="wintitle"> Repeater</span>) wordt precies gedupliceerd in het lokale pad op het doel <span class="keyword"> Insight Server</span>. </li>
      <li id="li_3114B191C73744658799E112C61AB004">Als zowel Paden recursief als Afvlakken waar zijn, worden geen submappen gemaakt in het lokale pad. In plaats daarvan worden alle bestanden uit de externe mapstructuur op het hoofdniveau van de lokale map geplaatst. </li>
      </ul></p> <p> <p>Opmerking: Als zowel Paden afvlakken als Recursief zijn ingesteld op true en de bestanden in de verschillende submappen op de externe computer dezelfde naam hebben, worden de <span class="wintitle"> Replicatieservice</span> kan stoppen of er kan ander ongedefinieerd gedrag optreden. </p> </p> </td> 
   </tr> 
   <tr> 
      <td colname="col1"> Lokaal pad </td> 
      <td colname="col2">De opslaglocatie voor de bestanden die worden opgehaald van <span class="wintitle"> Repeater</span>. Het pad is relatief ten opzichte van de <span class="keyword"> Insight Server</span> installatiemap. </td> 
   </tr> 
   <tr> 
      <td colname="col1"> Recursief </td> 
      <td colname="col2"> Waar of onwaar. Indien onwaar worden alleen de bestanden op het hoofdniveau van de map gerepliceerd die door de parameter Remote URI wordt opgegeven. Zie Paden samenvoegen in deze tabel. </td> 
   </tr> 
   <tr> 
      <td colname="col1"> Externe URI </td> 
      <td colname="col2">De URI, inclusief een bestandsmasker, voor toegang tot de <span class="wintitle"> Repeater's</span> opslaan. De <span class="filepath"> Communications.cfg</span> bestand op de <span class="wintitle"> Repeater</span> moet zo worden geconfigureerd dat de gebeurtenisgegevens kunnen worden benaderd met deze URI. Zie <a href="../../../home/c-inst-svr/c-admin-inst-svr/c-mntr-disk-spc/t-mntr-evt-data-spc.md#task-a54d4bd16b96437f943cd09e5d848440"> Gegevensruimte van gebeurtenissen controleren</a>. </td> 
   </tr> 
   <tr> 
      <td colname="col1"> Server </td> 
      <td colname="col2">Parameters voor de <span class="wintitle"> Repeater</span> waarvan het doel <span class="keyword"> Insight Server</span> Hiermee worden bestanden met gebeurtenisgegevens opgehaald. </td> 
   </tr> 
   <tr> 
      <td colname="col1"> Naam </td> 
      <td colname="col2">Optioneel. De naam waarmee de <span class="wintitle"> Repeater</span>. </td> 
   </tr> 
   <tr> 
      <td colname="col1"> Algemene naam SSL-server </td> 
      <td colname="col2">Alleen vereist als Use SSL is ingesteld op true. Algemene naam van de <span class="wintitle"> Repeater</span> waarop de gebeurtenisgegevens worden opgeslagen. Deze naam moet overeenkomen met de algemene naam die wordt vermeld in het communicatiecertificaat voor de computer. </td> 
   </tr> 
   <tr> 
      <td colname="col1"> Adres </td> 
      <td colname="col2">De naam van de gastheer of numeriek IP adres van het <span class="wintitle"> Repeater</span> waarop de gebeurtenisgegevens worden opgeslagen. De algemene naam van de server is geen geldige invoer. </td> 
   </tr> 
   <tr> 
      <td colname="col1"> Poort </td> 
      <td colname="col2"> Poort die wordt gebruikt voor gegevensoverdracht. De standaardpoort is 80. </td> 
   </tr> 
   <tr> 
      <td colname="col1"> SSL-clientcertificaat </td> 
      <td colname="col2">Alleen vereist als Use SSL is ingesteld op true. Naam van het licentiecertificaat dat wordt gebruikt om verbinding te maken met het <span class="wintitle"> Repeater</span>. </td> 
   </tr> 
   <tr> 
      <td colname="col1"> SSL gebruiken </td> 
      <td colname="col2"> <p>Bepaalt of SSL voor de gegevenstransmissie wordt gebruikt. De opties zijn true of false en de standaardwaarde is false. </p> <p> <p>Opmerking: Het gebruik van SSL wordt afgeraden omdat dit negatieve gevolgen kan hebben voor de prestaties. SSL is alleen vereist als het netwerk dat de <span class="wintitle"> Repeater</span> aan de doelmachines onzeker is. </p> </p> </td> 
   </tr> 
   <tr> 
      <td colname="col1"> Eindtijd, Begintijd </td> 
      <td colname="col2"> <p>(Optioneel) Beperkt de set bestanden met gebeurtenisgegevens die naar het doel worden gekopieerd <span class="keyword"> Insight Server</span> aan die die gegevens bevatten in de waaier die door de Tijd van het Begin en de Tijd van het Eind wordt bepaald. Als Begintijd is ingesteld, worden de bestanden met gebeurtenisgegevens waarin alle logitems van vóór de opgegeven begintijd afkomstig zijn, niet gekopieerd. Als Eindtijd is ingesteld, worden de bestanden met gebeurtenisgegevens waarin alle logitems van de opgegeven of latere tijd niet worden gekopieerd. Als slechts een deel van de gegevens in een bestand binnen het opgegeven bereik valt, wordt het gehele bestand naar de doelcomputer gekopieerd. </p> <p>Adobe raadt u aan een van de volgende notaties te gebruiken: 
      <ul id="ul_AE15A159A4C043398B37AD56FDFD9DCA">
      <li id="li_4DEF0F13D13E43E39CBD1A0F32765F32">1 januari 2013 HH:MM:SS EDT </li>
      <li id="li_E3275312E93D4C1FAA028543DC21B51A">1 jan. 2013 HH:MM:SS GMT </li>
      </ul></p> <p> <p>Opmerking: U moet een tijdzone opgeven. De tijdzone wordt niet standaard ingesteld op de systeemtijd als deze niet is opgegeven. Als u de Tijd van de Besparing van het Daglicht of een gelijkaardig klok-veranderende beleid wilt uitvoeren, moet u sparen <span class="filepath"> .dst</span> bestand met de desbetreffende regels in de map Base\Dataset\Timezone in het dialoogvenster <span class="keyword"> Insight Server</span> machine. Voor een lijst van gesteunde tijdzoneafkortingen en informatie over het uitvoeren van de Tijd van de Besparing van het Daglicht, zie <a href="../../../home/c-inst-svr/c-time-zn-cds.md#concept-eed5ba32d5d347cf94b76db83b29f211"> Tijdzonecodes</a>. </p> </p> <p> <p>Opmerking: Als u deze instellingen wilt gebruiken, moeten de namen van de bestanden met gebeurtenisgegevens beginnen met een ISO-datum (JJJMMDD) en moet elk bestand gegevens bevatten voor de periode van 24 uur die op die datum om 12.00 uur begint. </p> </p> </td> 
   </tr> 
   </tbody> 
   </table>

1. Sla de wijzigingen op de server op door het volgende te doen:

   1. Klikken met rechtermuisknop **[!UICONTROL (modified)]** boven aan het venster en klik op **[!UICONTROL Save]**.
   1. In de [!DNL Server Files Manager]klikt u met de rechtermuisknop op het vinkje voor het bestand in het dialoogvenster [!DNL Temp] kolom en selecteer **[!UICONTROL Save to]** > *&lt;**[!UICONTROL server name]**>*.

<!-- <a id="example_A60DE2383CA341DCB512E52DE76ADA89"></a> -->

In dit voorbeeld ziet u hoe bestanden worden gekopieerd als zowel de parameters Paden afvlakken als Recursief zijn ingesteld op true.

Stel dat de externe URI [!DNL /RemoteRoot/] en Lokaal pad is [!DNL E:\LocalRoot\]. Op de afstandsbediening ( [!DNL Repeater]), worden de bestanden als volgt geordend:

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
>Als bestanden in de verschillende submappen op de externe computer dezelfde naam of namen hebben, worden de [!DNL Replication Service] kan stoppen of er kan ander ongedefinieerd gedrag optreden.
