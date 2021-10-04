---
description: Servercomponenten bijwerken voor Data Workbench 6.3.
title: DWB Server upgrade 6.2 tot 6.3
uuid: e12b6cc1-070e-4bc7-bc64-203d11cfeae9
exl-id: 5106d9a3-179a-49f1-915a-c03b36ed5257
source-git-commit: b21da6d12175fa8570b1b366049baa9c8e8ea862
workflow-type: tm+mt
source-wordcount: '380'
ht-degree: 0%

---

# Upgrade van DWB-server: 6.2 t/m 6.3{#dwb-server-upgrade-to}

Servercomponenten bijwerken voor Data Workbench 6.3.

**Upgradeserver**

Als u aangepaste profielen hebt die voorrang hebben op de standaardbestanden in het [!DNL Base]-pakket, moet u deze aangepaste bestanden bijwerken:

* **Werk het Meta.cfg- dossier**  (  [!DNL E:\..\Profiles\<your custom profile>\Context\meta.cfg)]om bijgewerkte wachtwoordencryptie voor de Eenheid van het Systeem van het Dossier (server FSU) te plaatsen, en ingangen voor de transformaties van het Paar van de Waarde van de Naam toe te voegen om uit de groeperingen [ van het Koord van de ](../../../../home/c-inst-svr/c-upgrd-uninst-sftwr/c-upgrd-sftwr/c-6-2-to-6-3-upgrade.md#concept-42f74911b5714219a359b719badac8e0)Vraag voordeel te halen.

   1. Open het [!DNL meta.cfg] dossier op FSU.
   1. Wijzig het gegevenstype voor **[!UICONTROL Proxy Password]** van &quot; [!DNL string"] in &quot; [!DNL EncryptedString]&quot; in de sectie *Werkstationconfiguratie*.

      ```
        Proxy User Name = string:
        Proxy Password = EncryptedString:   (
        from Proxy Password = String)
        Use Address File = bool: true
      ```

   1. Voeg nieuwe ingangen toe om de nieuwe transformaties van het Paar van de Waarde van de Naam toe te laten: *BuildNameValuePair* en *ExtractNameValueParen*.

      Open een werkruimte en klik met de rechtermuisknop **Admin** > **Profielbeheer**.

      Klik onder **Context** op het bestand **meta.cfg** in de kolom **Base** en klik vervolgens op **Lokaal maken**. Klik in de tabelkolom Gebruiker met de rechtermuisknop en selecteer **Open** > **in Workstation**.

      ![](assets/meta_cfg.png)

      * Klik in het nieuwe venster op **metadata** en voeg acceptabele onderliggende sjablonen toe.

         ![](assets/meta_cfg_child.png)

      * Open **transformatie** en voeg nieuwe malplaatjes toe.

         ![](assets/meta_cfg_template.png)

* **Update voor snelle verbeteringen** in de samenvoeging. Voeg parameters toe of verander waarden aan de volgende configuratiedossiers om uit snelheidsverbeteringen in Data Workbench tijdens een transformatie voordeel te halen.

   * **Communications.cfg** (  [!DNL E:\Server\Components\Communications.cfg])

      ```
      18 = SourceListServer:
          URI = string: /SourceListServer/
          Listing Interval = int: 10 (
      <new>)
      ```

   * **Disk Files.cfg** (at  [!DNL E:\Server\Components] en  [!DNL E:\Server\Components for Processing Servers])

      ```
      Disk Cache Size (MB) = double: 1024
      <(from double: 256)>
      Disk Cache Read Limit (MB) = double: 768
      <(new)>
      ```

   * **Log Processing Mode.cfg** (  [!DNL E:\Server\Profiles\<your profile>\Dataset\Log Processing Mode.cfg])

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

* **Adobe Target met DWB-integratieupdate**. Een nieuw exportbestand, [!DNL ExportIntegration.exe], vervangt het bestaande [!DNL TnTSend.exe]-bestand op de Insight Server (`E:\Server\Scripts\TnTSend.exe`). Dit nieuwe exportbestand biedt ondersteuning voor integratie en coördinatie met het nieuwe Master marketingprofiel (MMP) en [Adobe Audience Manager](https://www.adobe.com/analytics/audience-manager.html).[](https://www.adobe.com/marketing/target.html)

   U moet de volgende opdrachten voor Adobe Target-exportbewerkingen bijwerken.

   `Command = string: TnTSend.exe`

   tot

   ```
   <filepath>
   Command = string: ExportIntegration.exe
   </filepath>
   ```

   >[!NOTE]
   >
   >Dit is alleen van invloed op exportbewerkingen die vóór versie 6.3 zijn gemaakt.

   U kunt ook het volgende proberen om het oude exportproces te gebruiken:

   * Maak een nieuwe test- en doelexport in het werkstation.
   * Wijzig de oude test en de uitvoer van het Doel die in [!DNL Server/Profiles/`<your profile>`/de Uitvoer wordt gevonden.]

* **Werk het profiel Adobe SC bij.** Voor wijzigingen in het  [!DNL Exclude Hit.cfg] bestand moet een veld worden gedeclareerd in het bijbehorende  [!DNL Decoding Instructions.cfg] bestand.

   >[!NOTE]
   >
   >Als uw Adobe SC-profiel een aangepast [!DNL Decoding Instructions.cfg]-bestand bevat, moet u een [!DNL DelimitedDecoder]-parameter aan uw aangepaste bestand toevoegen.

   ```
   0 = DelimitedDecoder:
      Delimiter = string: \t
      Fields = vector: x items
      …
         5 = string:
   Changed to:
   
   5 = string: x-hit_source
   ```

   Door het veld [!DNL DelimitedDecoder] toe te voegen, kunt u gebruikmaken van functies-updates en kunt u mogelijke problemen met de logverwerking als gevolg van deze updates voorkomen.
