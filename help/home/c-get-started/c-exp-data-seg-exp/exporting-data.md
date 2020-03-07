---
description: U kunt CSV, TSV, de Uitvoer van het Segment, en de Uitvoer van het Segment met Kopbal nu gebruiken gebruikend de protocollen van FTP en van SFTP om segmentdossiers van de cliënt (werkstation) naar de server uit te voeren.
title: Voer een segment uit gebruikend levering S/FTP
uuid: 4d654368-cbf7-4e7f-8ab9-82f4e0261ac6
translation-type: tm+mt
source-git-commit: 72761a57e4bb9f230581b2cd37bff04ba7be8e37

---


# Voer een segment uit gebruikend levering S/FTP{#export-a-segment-using-s-ftp-delivery}

U kunt CSV, TSV, de Uitvoer van het Segment, en de Uitvoer van het Segment met Kopbal nu gebruiken gebruikend de protocollen van FTP en van SFTP om segmentdossiers van de cliënt (werkstation) naar de server uit te voeren.

**De configuratiedossiers van de Uitvoer van de vestiging S/FTP**

Om de de uitvoerconfiguratie te plaatsen, werden twee nieuwe dossiers van de de uitvoerconfiguratie toegevoegd aan opstelling een verbinding van FTP of van SFTP, die de details van de Server om van het dossier van *FTPServerInfo.cfg* toelaat worden geselecteerd en de geloofsbrieven zullen van *omslag FTPUserCredentials* (die aan de Naam van de Server beantwoordt die in de bevelargumenten wordt gegeven) worden geselecteerd.

* Stel het **FTPServerInfo.cfg** -bestand in.

   Ga de de serverinformatie van FTP in en vastgestelde verbinding opnieuw probeert toegestaan van het werkstation. Geef uit van het werkstation of de server bij [!DNL Server\Addresses\Export\] **[!DNL FTPServerInfo.cfg]** - dossier uit.

   ```
   FTP Servers = vector: 1 items 
     0 = ftpServerInfo:  
       Address = string:  
       Name = string:  
       Port = int: 21 
   Connect Retries = vector: 1 items 
     0 = connectServerRetries:  
       Retries = int: 0 
       Server Name = string:
   ```

* Plaats het **FTPUserCredentials.cfg** - dossier.

   Ga gebruikersgeloofsbrieven in om met servers te verbinden gebruikend het [!DNL Server\Admin\Export\] **[!DNL FTPUserCredentials.cfg]** - dossier. Dit dossier bevat gebruikersgeloofsbrieven nodig om met servers te verbinden en kan slechts van server en niet van werkstation (cliënt) worden uitgegeven.

   ```
   FTP User Credentials = vector: 1 items 
     0 = ftpUserCredInfo: 
       User Name = string:  
       User Password = EncryptedString:  
       Server Name = string:  
       Public Key Path = string:  
       Private Key Path = string:  
       Passphrase = EncryptedString:
   ```

   >[!NOTE]
   >
   >Zorg ervoor dat de sleutels van SSH u voor authentificatie produceert in het formaat identiek aan die zijn die worden geproduceerd wanneer u het bevel van het Sleutelgen van SSH gebruikt.
   >
   >Voorbeeld voor het genereren van SSH-sleutels met behulp van keygen:
   >
   >
   ```
   >ssh-keygen -t rsa -b 4096 -C "<label>"
   >```

   Er zijn zes parameters in het **FTPUserCredentials.cfg** - dossier dat voor diverse FTP of overdrachten SFTP wordt vereist.

   1. *Gebruikersnaam*
   1. *Gebruikerswachtwoord*
   1. *Servernaam*
   1. *Pad openbare sleutel*
   1. *Pad voor privésleutel*
   1. *Passphrase*
   <table id="table_4EB416DC770D4D1AA4FAD9676C0D680C"> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> Protocol </th> 
      <th colname="col2" class="entry"> Parameters </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>FTP </p> </td> 
      <td colname="col2"> <p>Vastgestelde parameters 1, 2, 3. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>SFTP die wachtwoordauthentificatie gebruiken </p> </td> 
      <td colname="col2"> <p>Vastgestelde parameters 1, 2, 3 wanneer de overdracht wachtwoordauthentificatie (-p in de bevelargumenten) gebruikt. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>SFTP die zeer belangrijke authentificatie gebruiken </p> </td> 
      <td colname="col2"> <p>Vastgestelde parameters 1, 2, 3, 4, 5, 6 wanneer de overdracht zeer belangrijke authentificatie (-k in de bevelargumenten) gebruikt. </p> </td> 
      </tr> 
    </tbody> 
    </table>

**Het plaatsen van de Bevelen van de Uitvoer van FTP en van SFTP**

1. Open een de uitvoerlijst.

   Van het Werkstation, klik een Lijst *van het* Detail met de rechtermuisknop aan en kies één van de uitvoer type-CSV, TSV, de Uitvoer van het Segment, of de Uitvoer van het Segment met Kopbal. Of open het [!DNL .export] dossier van een bevel-herinnering en geef uit (zie het [Vormen Segmenten voor de Uitvoer](../../../home/c-get-started/c-exp-data-seg-exp/t-config-sgts-expt.md#task-8857f221fa66463990ec9b60db6db372)).

1. Op het gebied van het *Bevel* , plaats het aan punt aan uitvoerbaar de uitvoer:

   ```
   ExportIntegration.exe
   ```

1. Plaats de gebieden van de Argumenten *van het* Bevel zoals hieronder getoond voor het vereiste protocol en de authentificatie:

   **FTP**

   ```
   <Command Arguments> set to  
   <ftp "%file%" ServerName ServerDestinationPath>
   ```

   ![](assets/FTP_Command_arguments.png)

   **SFTP** (als het gebruiken van wachtwoord voor authentificatie)

   ```
   <Command Arguments> set to  
   <sftp "%file%" ServerName ServerDestinationPath -p>
   ```

   **SFTP** (als het gebruiken van sleutels voor authentificatie)

   ```
   <Command Arguments> set to  
   <sftp "%file%" ServerName ServerDestinationPath -k>
   ```

   ![](assets/SFTP_command_arguments.png)

Alle Argumenten van het Bevel zijn verplicht en moeten zijn ingegaan zoals getoond.

## S/FTP-export met particuliere/openbare sleutels {#section-0534424d79a54a47b82594cfa7b3c17f}

Om de Uitvoer van FTP en van SFTP uit te voeren gebruikend privé en openbare sleutels, plaats de configuratiedossiers in deze omslagen:

* Plaats **FTPServerInfo.cfg** in de [!DNL Server/Addresses/Export/] omslag.
* Plaats **FTPUserCredentials.cfg** in de [!DNL Server/Admin/Export/] omslag.

Zes parameters zijn inbegrepen in het dossier **FTPServerInfo.cfg** :

1. *Gebruikersnaam*
1. *Gebruikerswachtwoord*
1. *Servernaam*
1. *Pad openbare sleutel*
1. *Privé Zeer belangrijke Weg —* Plaats de privé belangrijkste weg in het configuratiedossier zonder de uitbreiding, bijvoorbeeld:

[!DNL Private Key Path = string: E:\\Server\\campaign\\campaignprivatekey]

1. *Passphrase*

FTP gebruikt parameters 1, 2, en 3.

SFTP gebruikt parameters 1, 2, en 3 wanneer de overdracht wachtwoordauthentificatie gebruikt.

SFTP gebruikt alle zes parameters wanneer de overdracht gebruikend zeer belangrijke authentificatie wordt gedaan. Bijvoorbeeld, als u sleutels voor authentificatie gebruikt:

[!DNL 'Command Arguments' = sftp "%file%" ServerName ServerDestinationPath -k]

De configuratiedossiers moeten in de correcte plaats zijn.

>[!NOTE]
>
>De openbare sleutels moeten aan een **.pem** - dossier en niet aan een omslagplaats richten. U kunt sleutels tot stand brengen gebruikend een de zeer belangrijke generatiefunctie van SSH van toepassingen zoals Cygwin. (Het Putty produceert sleutels in een .ppk formaat dat niet wordt gesteund.)
