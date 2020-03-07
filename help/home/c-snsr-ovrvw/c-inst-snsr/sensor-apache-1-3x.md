---
description: Gedetailleerde instructies voor het installeren en het vormen van Sensor voor een Server 1.3.x van Apache op RedHat Linux 7.x of later, SUSE Linux 9.x of later, Zon Solaris SPARC 2.6 of later, Zon Solaris x86 9 of later, FreeBSD 4 of later, of MAC OS X PowerPC.
title: Apache Server 1.3.x op Linux, Sun Solaris, FreeBSD, of MAC OS X
uuid: bd46dd0f-fe36-4f8b-a87c-8ca7b64da609
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Apache Server 1.3.x op Linux, Sun Solaris, FreeBSD, of MAC OS X{#apache-server-x-on-linux-sun-solaris-freebsd-or-mac-os-x}

Gedetailleerde instructies voor het installeren en het vormen van Sensor voor een Server 1.3.x van Apache op RedHat Linux 7.x of later, SUSE Linux 9.x of later, Zon Solaris SPARC 2.6 of later, Zon Solaris x86 9 of later, FreeBSD 4 of later, of MAC OS X PowerPC.

De programmadossiers voor Sensor worden verpakt in een installatiedossier dat u van de de downloadplaats van Adobe verkrijgt. Als u niet reeds het de installatiedossier van de Sensor voor uw bepaalde Webserver hebt, download het (of verkrijg het van uw vertegenwoordiger van Adobe) alvorens u met de volgende procedures begint.

Om Sensor te installeren en te vormen, moet u de volgende stappen op hoog niveau uitvoeren:

## De programmabestanden installeren {#section-aae323e252394212bf4096d65fdd280c}

Instructies voor het ophalen en installeren van de programmabestanden voor Sensor op het serversysteem.

1. Opening van een sessie als wortelgebruiker of als gebruiker met wortelgezag.
1. Decompress en unpack het installatiedossier gebruikend het volgende bevel:

   * Op Linux:

      ```
      tar -zxf installationFilename.tar.gz
      ```

   * Op Solaris:

      ```
      unzip -d installationFilename.tar.gz 
       tar -xf installationFilename.tar
      ```

1. Kopieer de onverpakte programmadossiers aan de folders die in de volgende lijst worden geïdentificeerd:

<table id="table_A97CF630633C4543A742D96C302D1138"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Bestand </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
   <th colname="col3" class="entry"> Doelmap </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> mod_visual_sciences.so </td> 
   <td colname="col2"> De module van de inzamelingenlading </td> 
   <td colname="col3"> apachePath/libexec </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>txlogge </p> </td> 
   <td colname="col2"> Het uitzendprogramma </td> 
   <td colname="col3"> <p>/usr/local/bin </p> <p>—OF— </p> <p>/usr/local/sbin </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> txlogd.conf </td> 
   <td colname="col2"> Het de configuratiedossier van de Sensor </td> 
   <td colname="col3"> /etc </td> 
  </tr> 
  <tr> 
   <td colname="col1"> trust_ca_cert.pem </td> 
   <td colname="col2"> Het certificaat dat wordt gebruikt om het digitale certificaat te bevestigen dat de Server van het Inzicht tijdens het verbindingsproces voorstelt </td> 
   <td colname="col3"> /usr/local/visual_sciences </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Het installatiepakket bevat een spreadsheetdossier genoemd TestExperiment.xls. Deze spreadsheet is een hulpmiddel dat de architecten gebruiken om een gecontroleerd experiment te vormen. De sensor zelf gebruikt dit dossier niet, zodat is het niet noodzakelijk om het dossier op de machine te installeren waar de Sensor loopt (hoewel u kunt verkiezen om dit te doen). U zou, in plaats daarvan, het dossier aan een plaats kunnen willen kopiëren waar uw architecten tot het kunnen toegang hebben of eenvoudig het dossier uit het installatiepakket halen zoals nodig. Voor meer informatie over gecontroleerde experimentatie, zie de Gids van de Experimenten van het Inzicht de Gecontroleerde.

**Toestemmingen op de programmabestanden**

De onjuiste toestemmingen op de programmadossiers veroorzaken de meerderheid van problemen die bij het installeren van Sensor worden ontmoet.

Gelieve te zorgen ervoor dat u de toestemmingen precies zoals die in deze sectie wordt verklaard plaatst.

Door gebrek, hebben de programmadossiers in het teerdossier de volgende toestemmingen. Afhankelijk van hoe uw systeem wordt gevormd, zouden deze montages (unmaskated) kunnen worden veranderd wanneer u de dossiers haalt. Om de toestemmingen aan de geadviseerde standaardmontages terug te stellen, gebruik hieronder de bevelen van de wortelmethode. Controle dat de folders waarin u de dossiers hebt geïnstalleerd minstens dit niveau van toegang toelaten.

| Bestand | Standaardrechten | chmod, opdracht |
|---|---|---|
| mod_visual_sciences.so | rwx r-x r-x | chmod 755 |
| txlogge | rwx —x —x | chmod 711 |
| txlogd.conf | rw- rw- r— | chmod 664 |
| trust_ca_cert.pem | rw- rw- r— | chmod 664 |

## Geef het de configuratiedossier van de Sensor uit {#section-3f22a1c91d7d43b6b4c30f1b7448b17f}

Het [!DNL txlogd.conf] dossier bevat de configuratieparameters voor Sensor.

U moet het dossier uitgeven om, onder andere, de grootte van de schijfrij, het adres van de Server van het Inzicht, en identiteitskaart te specificeren die aan de gegevens zal worden vastgemaakt die door deze sensor worden geproduceerd.

Het configuratiedossier bevat vereiste parameters en facultatieve parameters.

* De vereiste parameters zijn montages die u moet specificeren wanneer u Sensor installeert. Zonder deze montages, loopt de Sensor niet met succes.
* De facultatieve parameters zijn montages die aan vooraf bepaalde waarden (die u kunt wijzigen) in gebreke blijven of facultatieve eigenschappen toelaten.

Om het de configuratiedossier van de Sensor uit te geven

1. Open het /etc/txlogd.conf dossier in een tekstredacteur en plaats de vereiste parameters evenals om het even welke gewenste facultatieve parameters.
1. Sparen en sluit het dossier.

## Start de zender en maak de schijfwachtrij {#section-a453d912ec3d47aa8e40ccacf527119d}

Instructies om de schijfrij tot stand te brengen nadat u het txlogd.conf- dossier vormt.

1. Als de folder waarin de schijfrij verblijft niet reeds bestaat, creeer het. Zorg ervoor dat de folder zowel de inzamelaarmodule als het uitzendingsprogramma van lees-schrijftoegang tot het dossier voorziet.
1. Op de computer waar de Sensor geïnstalleerd is, voer het volgende bevel uit om de zender te beginnen:

   ```
   /usr/local/bin/txlogd -ic -f /etc/txlogd.conf
   ```

   * De &quot;i&quot;optie in dit bevel begint de zender op interactieve wijze. Deze wijze toont zenderberichten op het scherm en laat u ook toe om met de zender in wisselwerking te staan gebruikend toetsenbordbevelen.
   * De &quot;c&quot;optie leidt de zender om de schijfrij tot stand te brengen.
   * De &quot;f&quot;optie specificeert de plaats van het configuratiedossier.

1. Verifieer dat de zender de schijfrij in de plaats gecreeerd heeft die in de parameter QueueFile en van de grootte in de parameter QueueSize wordt gespecificeerd.
1. Als de rij niet correct is gecreeerd, typ Ctrl+C om de zender te eindigen, dan doe het volgende:

   1. Onderzoek het txtlogd.conf- dossier en verifieer dat de parameters QueueFile en QueueSize correct worden geplaatst.
   1. Controle dat het apparaat waaraan de schijfrij wordt toegewezen operationeel is en voldoende ruimte beschikbaar heeft om een dossier van de grootte te houden die in de parameter QueueSize wordt gespecificeerd.
   1. Breng de nodige correcties aan en herhaal deze procedure.

## Voeg de Collector aan de Server van het Web toe {#section-a7fb6425956f4f518ae3a7db091b33d2}

Voor servers Apache, is de inzamelaar een dynamisch gedeeld voorwerp dat u in uw proces van de Webserver laadt.

Om de inzamelaar aan uw Webserver toe te voegen, moet u het httpd.conf- dossier uitgeven zoals hieronder beschreven en uw Webserver opnieuw beginnen.

Als de Sensor gegevens voor veelvoudige Webservers op de servercomputer vangt, moet u de volgende procedure voor elke Webserver uitvoeren.

1. Gebruikend een tekstredacteur, open het [!DNL httpd.conf] dossier voor de Webserver de waarvan gebeurtenissenSensor vangt.
1. Voeg de volgende lijnen aan het eind van het dossier toe:

   ```
   LoadModule  visual_sciences_module  libexec/mod_visual_sciences.so 
   VisualSciencesConfig  /etc/txlogd.conf 
   AddModule mod_visual_sciences.c
   ```

   >[!NOTE]
   >
   >Deze lijnen zijn hoofdlettergevoelig. Typ hen precies zoals zij hierboven verschijnen.

1. Start de webserver opnieuw op. De inzamelaar wordt geladen met de Webserver en zal beginnen inzamelend gebeurtenisgegevens en schrijvend het aan de schijfrij.

## Test de sensor {#section-83d9f60b39a6474f9c76bee3e19b2575}

Begin de zender en verifieer dat het met succes met de Server van het Inzicht kan verbinden en gebeurtenisgegevens overbrengen aan het.

>[!NOTE]
>
>Om te verifiëren dat de zender gebeurtenisgegevens naar de Server van het Inzicht kan met succes verzenden, zorg ervoor dat de Server van het doelInzicht geïnstalleerd en lopend is alvorens u met de volgende test begint.

1. Als de zender niet reeds loopt, begin het opnieuw gebruikend het volgende bevel:

   ```
   /usr/local/bin/txlogd -i -f /etc/txlogd.conf 
   ```

1. Open browser (op om het even welk systeem) en verzoek om een pagina van de Webserver waarop de Sensor loopt (ben zeker om een pagina te selecteren die de Sensor controleert).
1. Nadat u het verzoek uitgeeft, controleer de console van de zender berichten erop wijzend dat het gebeurtenisgegevens naar de Server van het doelInzicht verzendt.
1. Als de Sensor geen gegevens met succes overbrengt, verifieer dat:

   * De doelserver van het Inzicht loopt.
   * De [!DNL ServerAddress] en [!DNL ServerPort] parameters worden correct geplaatst in [!DNL txtlogd.conf].

   * Als u het [!DNL ServerAddress] gebruiken van een servernaam specificeerde, probeer in plaats daarvan gebruikend zijn numeriek IP adres. De waarde van de [!DNL CertName] parameter past de gemeenschappelijke naam aan die op het digitale certificaat van de Server van het doelInzicht precies verschijnt.

## Voeg de Transmitter aan Uw Manuscript van de Opstarten van het Systeem toe {#section-4e1ffa6e043941ab91411d91d596477a}

Informatie om te verzekeren dat de zender automatisch laadt wanneer de machine van de Webserver opnieuw is begonnen.

Voeg het volgende bevel (dat de zender) aan uw systeem startmanuscript lanceert toe.

```
/usr/local/bin/txlogd -f /etc/txlogd.conf
```

Dit bevel begint de zender als daemon. De werkende en foutenmeldingen die de zender produceert worden geschreven aan syslog.

>[!NOTE]
>
>Sommige gebruikers van Solaris zouden een &quot;niet kunnen&quot;fout ontmoeten om mutex&quot;te verwerven. Voor Sensor om behoorlijk op deze systemen te functioneren, moet de volgende lijn of aan of in het dossier/etc/systeem worden toegevoegd of worden uitgegeven: >
>
```>
>semsys:seminfo_semmnu=1024
>```>
>The default Solaris setting is 60. Based on tests conducted with Sensor, which uses three semaphores for each instance, Adobe recommends that you use 1024 as your setting. This number is high enough for Sensor to function along with any other applications on the server that may require semaphores, but does not affect performance. To support this recommendation, please note that Adrian Cockcroft stated the following in his book Sun Performance and Tuning (Prentice Hall, October 1994): “Databases tend to use lots of shared memory and semaphore settings. These do not affect performance; as long as they are big enough, the programs will run.”



