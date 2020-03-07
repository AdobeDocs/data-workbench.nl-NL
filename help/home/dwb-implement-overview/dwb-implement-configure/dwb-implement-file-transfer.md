---
description: Een snelle gids voor verschillende methodes van de dossieroverdracht in DWB.
title: Bestandsoverdrachtsbeheer
uuid: a3e19f8a-1cc4-437c-9661-408f675109c0
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Bestandsoverdrachtsbeheer{#file-transfer-governance}

Een snelle gids voor verschillende methodes van de dossieroverdracht in DWB.

De Overdracht van het dossier Governance is een standaardproces om dossiers van een interne folder naar een andere server of interne dossierbeweging over te brengen.

## Verschillende methoden voor bestandsoverdracht {#section-972bb39ba1954c6ebd35f6d042593efe}

1. AWS (Amazon Web Services)

   1. Verhoog een Ticket om de interface van de bevellijn van AWS op server te installeren als niet reeds geïnstalleerd (zie [http://docs.aws.amazon.com/cli/latest/userguide/installing.html](http://docs.aws.amazon.com/cli/latest/userguide/installing.html)).
   1. Hoe te controleren? Probeer om AWS te vormen gebruikend bevelherinnering (zie [http://docs.aws.amazon.com/cli/latest/userguide/cli-chap-getting-started.html](http://docs.aws.amazon.com/cli/latest/userguide/cli-chap-getting-started.html)).

1. De dossiers van de overdracht van de server van FTP aan folder NAS.

   1. FTP offlinevoer van FTP server aan folder NAS. Voor FTP zijn de onderstaande gegevens vereist.

      ftp_gebruikersnaam

      ftp_password

      ftp_port

      ftp_adres

      ftp_directory

      delete_ftp_files

      ftp_file_extensie

      local_directory

      (De Details van FTP zullen in project checklist beschikbaar zijn. Externe FTP-gebruiker gebruiken voor het overbrengen van de bestanden)

   1. Het manuscript van ftp_winscp_get.pl van het gebruik hieronder en programma dat op vereiste wordt gebaseerd wordt vastgemaakt.

      ftp_winscp_get.pl

      Dit manuscript zou op E:\scripts\Scripository\Library\Perl moeten worden geplaatst

      >[!NOTE]
      >
      >Als de omslag van de Bewaarplaats niet beschikbaar is zie [Wekelijks opnieuw verwerken](../../../home/dwb-implement-overview/dwb-implement-configure/dwb-implement-reprocess-scripting.md#concept-60529e12d6d94386a02c1c6fdedf0295) om de omslag te downloaden.

   1. Plan het manuscript dat op dossierbeschikbaarheid bij ftp_address wordt gebaseerd.
   1. De noemende overeenkomst van dossier zou JJJJMMDD-&lt;offline_feed_name>-00 moeten zijn.*

1. De dossiers van de overdracht van folder NAS aan de server van FTP.

   1. Gebruik ftp_winscp_put.pl manuscript en programma dat op vereiste wordt gebaseerd.

      Dit manuscript zou op E:\scripts\Scripository\Library\Perl moeten worden geplaatst

      De details hieronder worden vereist om het manuscript in werking te stellen.

      ftp_gebruikersnaam

      ftp_password

      ftp_port

      ftp_adres

      ftp_directory

      delete_ftp_files

      ftp_file_extensie

      local_directory

      ```
      ####################################################################################################################### 
      # PLUGIN NAME HERE 
      my $pluginname = "FTP WinSCP"; 
      # 20140421 Script tp put files on the FTP 
      ####################################################################################################################### 
      # INCLUDE SCRIPOSITORY CORE 
      use FindBin;                 # locate this script 
      BEGIN {push @INC, $FindBin::Bin} 
      require 'core.pl'; 
      
         # check for the required parameters 
       GetOptions('local_directory:s'     => \$local_directory, 
                     'source_file_pattern:s' => \$source_file_pattern, 
                     'ftp_file_extension:s' => \$ftp_file_extension, 
                     'ftp_address=s'  => \$ftp_address, 
                     'ftp_username=s'  => \$ftp_username, 
                     'ftp_password:s'  => \$ftp_password, 
                     'ftp_port:s'   => \$ftp_port, 
                     'ftp_directory:s'     => \$ftp_directory, 
           'log_directory:s'  => \$log_directory, 
                     'error_directory:s'  => \$error_directory, 
                     'mail_from:s'  => \$mail_from, 
                     'mail_to:s'   => \$mail_to, 
                     'host:s'   => \$host, 
                     'trigger_directory:s' => \$trigger_directory, 
                     'trigger_file_extension:s' => \$trigger_file_extension, 
                     'delete_ftp_files:s'  => \$delete_ftp_files,); 
      
       # FOR LEFT OVER PARAMS, WE CAN CHECK GLOBAL PARAMS 
       check_parameters(@argv); 
      
       my $ftp_winscp_script = "winscpscript.txt"; 
       if (index($trigger_file_extension, '.') != -1) { 
        my @trigger_file_extension1=split(/\./,$trigger_file_extension,2); 
        $trigger_file_extension =  $trigger_file_extension1[1]; 
       } 
       if (index($ftp_file_extension, '.') != -1) { 
        my @ftp_file_extension1=split(/\./,$ftp_file_extension,2); 
        $ftp_file_extension =  $ftp_file_extension1[1]; 
       } 
       if ($trigger_file_extension ne "_empty_" && $trigger_directory ne "_empty_") { 
         print $trigger_file_extension; 
        my $ftp_winscp_trigger_script = "winscpscript_trigger.txt"; 
        create_winscp_script($ftp_winscp_trigger_script,$ftp_port,$ftp_username,$ftp_password,$ftp_address,$trigger_directory,$ftp_directory,$delete_ftp_files,"*",$trigger_file_extension); 
        sleep(10); 
        system("\"E:\\Scripts\\Scripository\\Library\\WinSCP\\WinSCP.exe\" /console /script=$ftp_winscp_trigger_script /log=$logfile"); 
        $files = getFiles($trigger_directory,$trigger_file_extension,$days_ago,$months_ago); 
        my $ftp_file_pattern=""; 
        my $numberoffiles = @$files; 
        my $i=0; 
        foreach my $trigger_file(@$files) { 
         $i++; 
         my $file_string=substr($trigger_file,length($trigger_directory), length($trigger_file)-length($trigger_directory)); 
         my @file_string1=split(/\./, $file_string, 2); 
         if ($i == $numberoffiles) { 
          $ftp_file_pattern.=$file_string1[0].".".$ftp_file_extension; 
         } 
         else { 
          $ftp_file_pattern.=$file_string1[0].".".$ftp_file_extension.", "; 
         }
      
        } 
      
        #unlink($ftp_winscp_trigger_script); 
        print $local_directory; 
        print $trigger_directory; 
        create_winscp_script($ftp_winscp_script,$ftp_port,$ftp_username,$ftp_password,$ftp_address,$local_directory,$ftp_directory,$delete_ftp_files,$ftp_file_pattern, ""); 
        runLogger("$pluginname: Sleeping for 10 sec to give enough time for the temp script to be available"); 
        sleep(10); 
        runLogger("$pluginname: FTP started"); 
        system("\"E:\\Scripts\\Scripository\\Library\\WinSCP\\WinSCP.exe\" /console /script=$ftp_winscp_script /log=$logfile"); 
        runLogger("$pluginname: FTP ended"); 
      
       } 
       else { 
        if ($source_file_pattern eq "_empty_") { 
         $source_file_pattern="*"; 
        } 
        else { 
         if (index($source_file_pattern, '.') != -1) { 
          my @source_file=split(/\./,$source_file_pattern,2); 
          $source_file_pattern =  $source_file[0]; 
         } 
        } 
        $ftp_file_extension=".".$ftp_file_extension; 
      print $local_directory; 
        create_winscp_script($ftp_winscp_script,$ftp_port,$ftp_username,$ftp_password,$ftp_address,$local_directory,$ftp_directory,$delete_ftp_files,$source_file_pattern,$ftp_file_extension); 
        runLogger("$pluginname: Sleeping for 10 sec to give enough time for the temp script to be available"); 
        sleep(10); 
        runLogger("$pluginname: FTP started"); 
        system("\"E:\\Scripts\\Scripository\\Library\\WinSCP\\WinSCP.exe\" /console /script=$ftp_winscp_script /log=$logfile"); 
        runLogger("$pluginname: FTP ended"); 
       } 
       unlink($ftp_winscp_script);
      
      sub create_winscp_script() { 
       my ($ftp_script,$ftp_port,$ftp_username,$ftp_password,$ftp_address,$local_directory,$ftp_directory,$delete_ftp_files,$file_pattern, $file_extension) = @_; 
       open (FTP, "> $ftp_script") or die "Can't open log: $!"; 
       print FTP "\# Automatically answer all prompts negatively not to stall\n"; 
       print FTP "option batch on\n\n"; 
       print FTP "\# Disable overwrite confirmations that conflict with the previous\n"; 
       print FTP "option confirm off\n\n"; 
       print FTP "\# Connect using a password\n"; 
       if ($ftp_port eq "22") { 
        print FTP "open sftp://$ftp_username:$ftp_password\@$ftp_address\n\n"; 
       } 
       else { 
        print FTP "open ftp://$ftp_username:$ftp_password\@$ftp_address\n\n"; 
       } 
       print FTP "\# Change local directory\n"; 
       print FTP "lcd \"$local_directory\"\n\n"; 
       print FTP "\# Change remote directory\n"; 
       if ($ftp_directory eq "_empty_") { 
       } 
       else { 
        print FTP "cd \"$ftp_directory\"\n\n"; 
       } 
       print FTP "\# Force binary mode transfer\n"; 
       print FTP "option transfer binary\n\n"; 
       print FTP "\# Download the file to specified directory\n"; 
       my @get_files=split(/,/,$file_pattern); 
       foreach my $file (@get_files){ 
        if ($delete_ftp_files eq "Y" || $delete_ftp_files eq "Yes") { 
         print FTP "put -nopreservetime -nopermissions -delete $file$file_extension\n"; 
      
        } 
        else { 
         print FTP "put -nopreservetime -nopermissions $file$file_extension\n"; 
      
        } 
      
       } 
      
       print FTP "\n\n"; 
       print FTP "\# Disconnect\n"; 
       print FTP "close\n\n"; 
       print FTP "\# Exit WinSCP\n"; 
       print FTP "exit\n\n"; 
       close(FTP); 
       runLogger("$pluginname: creating temporary winscp file"); 
      
      }
      ```

   1. Plan het manuscript dat op dossierbeschikbaarheid bij ftp_address wordt gebaseerd.
   1. De noemende overeenkomst van dossier zou JJJJMMDD-&lt;offline_feed_name>-00 moeten zijn.*

1. De Dossiers van de overdracht van één folder NAS aan andere folder NAS.

   1. Het dossier van het exemplaar en van het deeg direct verbindend met één NAS folder van andere. Volg hieronder proces:)

      aanmelden bij server -> Ga naar Uitvoeren -> \\server_name\E$ [nieuwe map wordt geopend en kopieert of verplaatst de bestanden rechtstreeks]

   1. Gebruik het &quot;copy_files.pl&quot;manuscript aan exemplaardossiers van één server aan andere of &quot;move_files.pl&quot;om dossiers van één server aan andere te verplaatsen. (Deze dossiers zijn beschikbaar in E:\scripts\Scripository)

