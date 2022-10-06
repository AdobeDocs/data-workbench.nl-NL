---
description: U kunt CSV, TSV, de Uitvoer van het Segment, en de Uitvoer van het Segment met Kopbal nu gebruiken gebruikend FTP en protocollen SFTP om segmentdossiers van de cliënt (werkstation) naar de server uit te voeren.
title: Een segment exporteren met S/FTP-levering
uuid: 4d654368-cbf7-4e7f-8ab9-82f4e0261ac6
exl-id: 0f1dc0a1-f376-47fb-887c-612a654ed0f0
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '543'
ht-degree: 0%

---

# Een segment exporteren met S/FTP-levering{#export-a-segment-using-s-ftp-delivery}

{{eol}}

U kunt CSV, TSV, de Uitvoer van het Segment, en de Uitvoer van het Segment met Kopbal nu gebruiken gebruikend FTP en protocollen SFTP om segmentdossiers van de cliënt (werkstation) naar de server uit te voeren.

**Configuratiebestanden voor S/FTP-export instellen**

Om de exportconfiguratie in te stellen, zijn twee nieuwe exportconfiguratiebestanden toegevoegd aan een FTP- of SFTP-verbinding, zodat de serverdetails kunnen worden gekozen uit de *FTPServerInfo.cfg* en de referenties worden gekozen uit *FTPUserCredentials* map (die overeenkomt met de servernaam die is opgegeven in de opdrachtargumenten).

* Stel de **FTPServerInfo.cfg** bestand.

   Voer de FTP-servergegevens in en stel verbindingspogingen in die vanaf het werkstation zijn toegestaan. Bewerken vanaf het werkstation of de server op  [!DNL Server\Addresses\Export\] **[!DNL FTPServerInfo.cfg]**bestand.

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

* Stel de **FTPUserCredentials.cfg** bestand.

   Geef gebruikersgegevens op om verbinding te maken met servers via de  [!DNL Server\Admin\Export\] **[!DNL FTPUserCredentials.cfg]**bestand. Dit bestand bevat gebruikersgegevens die nodig zijn om verbinding te maken met servers en kan alleen worden bewerkt vanaf de server en niet vanaf het werkstation (client).

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
   >Zorg ervoor dat SSH-sleutels die u voor verificatie genereert, dezelfde indeling hebben als de sleutels die worden gegenereerd wanneer u de opdracht SSH Keygen gebruikt.
   >
   >Voorbeeld voor het genereren van SSH-sleutels met behulp van sleutelgen:
   >
   >
   ```
   >ssh-keygen -t rsa -b 4096 -C "<label>"
   >```

   Er zijn zes parameters in de **FTPUserCredentials.cfg** bestand vereist voor verschillende FTP- of SFTP-overdrachten.

   1. *Gebruikersnaam*
   1. *Wachtwoord gebruiker*
   1. *Servernaam*
   1. *Pad naar openbare sleutel*
   1. *Pad naar persoonlijke sleutel*
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
      <td colname="col2"> <p>Stel de parameters 1, 2 en 3 in. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>SFTP met wachtwoordverificatie </p> </td> 
      <td colname="col2"> <p>Stel parameters 1, 2 en 3 in wanneer voor de overdracht wachtwoordverificatie wordt gebruikt (-p in de opdrachtargumenten). </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>SFTP met behulp van sleutelverificatie </p> </td> 
      <td colname="col2"> <p>Stel parameters 1, 2, 3, 4, 5 en 6 in wanneer voor de overdracht sleutelverificatie wordt gebruikt (-k in de opdrachtargumenten). </p> </td> 
      </tr> 
    </tbody> 
    </table>

**FTP- en SFTP-exportopdrachten instellen**

1. Open een exporttabel.

   Klik in het werkstation met de rechtermuisknop op een *Detailtabel* en kies een van de exporttypen: CSV, TSV, Segment Export of Segment Exporteren met koptekst. Of open de [!DNL .export] bestand van een opdrachtprompt en bewerken (zie [Segmenten voor export configureren](../../../home/c-get-started/c-exp-data-seg-exp/t-config-sgts-expt.md#task-8857f221fa66463990ec9b60db6db372)).

1. In de *Opdracht* -veld instellen zodat deze naar het uitvoerbare bestand verwijst:

   ```
   ExportIntegration.exe
   ```

1. Stel de *Opdrachtargumenten* velden zoals hieronder weergegeven voor het vereiste protocol en de vereiste verificatie:

   **FTP**

   ```
   <Command Arguments> set to  
   <ftp "%file%" ServerName ServerDestinationPath>
   ```

   ![](assets/FTP_Command_arguments.png)

   **SFTP** (als wachtwoord voor verificatie wordt gebruikt)

   ```
   <Command Arguments> set to  
   <sftp "%file%" ServerName ServerDestinationPath -p>
   ```

   **SFTP** (als u verificatietoetsen gebruikt)

   ```
   <Command Arguments> set to  
   <sftp "%file%" ServerName ServerDestinationPath -k>
   ```

   ![](assets/SFTP_command_arguments.png)

Alle argumenten van het Bevel zijn verplicht en moeten worden ingegaan zoals getoond.

## S/FTP-export met persoonlijke/openbare sleutels {#section-0534424d79a54a47b82594cfa7b3c17f}

Als u de FTP- en SFTP-export wilt implementeren met persoonlijke en openbare sleutels, plaatst u de configuratiebestanden in de volgende mappen:

* Plaatsen **FTPServerInfo.cfg** in de [!DNL Server/Addresses/Export/] map.
* Plaatsen **FTPUserCredentials.cfg** in de [!DNL Server/Admin/Export/] map.

Er zijn zes parameters opgenomen in de **FTPServerInfo.cfg** bestand:

1. *Gebruikersnaam*
1. *Wachtwoord gebruiker*
1. *Servernaam*
1. *Pad naar openbare sleutel*
1. *Pad naar persoonlijke sleutel —* Plaats het pad naar de persoonlijke sleutel in het configuratiebestand zonder de extensie, bijvoorbeeld:

[!DNL Private Key Path = string: E:\\Server\\campaign\\campaignprivatekey]

1. *Passphrase*

FTP gebruikt de parameters 1, 2 en 3.

SFTP gebruikt parameters 1, 2, en 3 wanneer de overdracht wachtwoordauthentificatie gebruikt.

SFTP gebruikt alle zes parameters wanneer de overdracht gebruikend zeer belangrijke authentificatie wordt gedaan. Als u bijvoorbeeld sleutels voor verificatie gebruikt:

[!DNL 'Command Arguments' = sftp "%file%" ServerName ServerDestinationPath -k]

De configuratiedossiers moeten in de correcte plaats zijn.

>[!NOTE]
>
>De openbare sleutels moeten aan een **.pem** en niet naar een maplocatie. U kunt toetsen maken met behulp van een SSH-sleutelgeneratiefunctie van toepassingen zoals Cygwin. (Met Putty worden toetsen in de indeling .ppk gegenereerd die niet wordt ondersteund.)
