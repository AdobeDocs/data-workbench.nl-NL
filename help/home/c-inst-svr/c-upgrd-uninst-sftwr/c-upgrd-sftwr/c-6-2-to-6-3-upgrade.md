---
description: Servercomponenten voor Data Workbench 6.3 upgraden.
title: DWB-serverupgrade 6.2 naar 6.3
uuid: e12b6cc1-070e-4bc7-bc64-203d11cfeae9
translation-type: tm+mt
source-git-commit: 25366087936dfa5e31c5921aac400535ec259f2e

---


# DWB-serverupgrade: 6.2 t/m 6.3{#dwb-server-upgrade-to}

Servercomponenten voor Data Workbench 6.3 upgraden.

**Upgrademeserver**

Als u profielen hebt aangepast die belangrijkheid over de standaarddossiers nemen die in het [!DNL Base] pakket worden verstrekt, dan zult u deze aangepaste dossiers moeten bijwerken:

* **Werk het Meta.cfg- dossier** bij ( [!DNL E:\..\Profiles\<your custom profile>\Context\meta.cfg)]om bijgewerkte wachtwoordencryptie voor de Eenheid van het Systeem van het Dossier (server FSU) te plaatsen, en om ingangen voor de transformaties van het Paar van de Waarde van de Naam toe te voegen om uit de groeperingen [van het Koord van de](../../../../home/c-inst-svr/c-upgrd-uninst-sftwr/c-upgrd-sftwr/c-6-2-to-6-3-upgrade.md#concept-42f74911b5714219a359b719badac8e0)Vraag voordeel te halen.

   1. Open het [!DNL meta.cfg] bestand op de FSU.
   1. Verander het gegevenstype voor **[!UICONTROL Proxy Password]** van &quot; [!DNL string"] in &quot; [!DNL EncryptedString]&quot;in de sectie van de Configuratie van het *Werkstation* .

      ```
      Proxy User Name = string: 
      Proxy Password = EncryptedString:   ( 
      
<i>van het Wachtwoord van de Volmacht = Koord</i>) het Dossier van het Adres van het gebruik = bool: waar&quot;

    1. Voeg nieuwe ingangen toe om de nieuwe transformaties van het Paar van de Waarde van de Naam toe te laten: *BuildNameValuePair* en *ExtractNameValuePairs*.
    
    Open een werkruimte en klik met de rechtermuisknop op **Admin** > **Profielbeheer**.
    
    Klik onder **Context** op het **meta.cfg** bestand in de kolom **Base** en klik op **Make Local**. Klik in de kolom Gebruikerslijst met de rechtermuisknop op en selecteer **Open** > **in Werkstation**.
    
    ![](assets/meta_cfg.png)
    
    * In het nieuwe venster, klik **meta-gegevens*** en voeg aanvaardbare kindmalplaatjes toe.
    
    ![](assets/meta_cfg_child.png)
    
    * Open **transformation** en voeg nieuwe sjablonen toe.
    
    ![assets/meta_cfg_template.png]

* **Update voor de Snelle verbeteringen** van de Fusie. Voeg parameters of veranderingswaarden aan de volgende configuratiedossiers toe om uit snelheidsverbeteringen in de Werkbank van Gegevens tijdens een transformatie voordeel te halen.

   * **Communications.cfg** ( [!DNL E:\Server\Components\Communications.cfg])

      ```
      18 = SourceListServer:  
          URI = string: /SourceListServer/ 
          Listing Interval = int: 10 ( 
      <new>)
      ```

   * **Disk Files.cfg** (bij [!DNL E:\Server\Components] en [!DNL E:\Server\Components for Processing Servers])

      ```
      Disk Cache Size (MB) = double: 1024  
      <(from double: 256)> 
      Disk Cache Read Limit (MB) = double: 768  
      <(new)>
      ```

   * **Logverwerkingsmodus.cfg** ( [!DNL E:\Server\Profiles\<your profile>\Dataset\Log Processing Mode.cfg])

      ```
      <(changed) 
      Batch Bytes = int: 268435456 
      Cloud Bytes = int: 268435456 
      Real Time FIFO Bytes = int: 268435456
      ```

      ```
      ( 
      <new>) 
      Cache Bytes = int: 32000000 
      Fast Input Decision Ratio = double: 200 
      Fast Input FIFO Bytes = int: 268435456 
      FIFO Hash Mask = int: 16383 
      Fast Merge Buffer Bytes = int: 536870912 
      Slow Merge Buffer Bytes = int: 268435456 
      Fast Merge Fan In = int: 64 
      Key Cache Size Logarithm = int: 21 
      Max Seeks = int: 512 
      Output Old Buffer Bytes = int: 536870912 
      Overflow FIFO Bytes = int: 67108864 
      Paused = bool: false
      ```
   >[!NOTE]
   >
   >Om uit de Snelle verbeteringen van de Fusie voordeel te halen, zorg ervoor u minstens 8 GBs van RAM per DPU hebt.

* **Het Doel van Adobe met DWB integratieupdate**. Een nieuw de uitvoerdossier, [!DNL ExportIntegration.exe], vervangt het bestaande [!DNL TnTSend.exe] dossier op de Server van het Inzicht (`E:\Server\Scripts\TnTSend.exe`). Dit nieuwe de uitvoerdossier steunt zowel de integratie van het Doel [van](https://www.adobe.com/marketing/target.html) Adobe als de coördinatie met het nieuwe HoofdProfiel van de Marketing (MMP) en de Manager [van het Publiek van](https://www.adobe.com/analytics/audience-manager.html)Adobe.

   U zult de volgende bevelen voor de uitvoer van het Doel van Adobe moeten bijwerken.

   `Command = string: TnTSend.exe`

   tot

   ```
   <filepath>
   Command = string: ExportIntegration.exe 
   </filepath>
   ```

   >[!NOTE]
   >
   >Dit zal slechts de uitvoer beïnvloeden die vóór versie 6.3 wordt gecreeerd.

   U kunt het volgende ook proberen om het oude de uitvoerproces aan te wenden:

   * Creeer een nieuwe Test en de Uitvoer van het Doel in het werkstation.
   * Wijzig de oude die Test en de uitvoer van het Doel in wordt gevonden [!DNL Server/Profiles/`<your profile>`/uitvoert.]

* **Werk het profiel van Adobe SC bij.** De veranderingen in het [!DNL Exclude Hit.cfg] dossier vereisen dat een gebied in het bijbehorende [!DNL Decoding Instructions.cfg] dossier wordt verklaard.

   >[!NOTE]
   >
   >Als uw profiel van Adobe SC een aangepast [!DNL Decoding Instructions.cfg] dossier omvat, zult u een [!DNL DelimitedDecoder] parameter aan uw aangepast dossier moeten omvatten.

   ```
   0 = DelimitedDecoder: 
      Delimiter = string: \t 
      Fields = vector: x items 
      …  
         5 = string: 
   Changed to: 
   
   5 = string: x-hit_source
   ```

   Het toevoegen van het [!DNL DelimitedDecoder] gebied staat u toe om uit eigenschapupdates voordeel te halen en mogelijke problemen van de Verwerking van het Logboek te vermijden die uit deze updates voortvloeien.
