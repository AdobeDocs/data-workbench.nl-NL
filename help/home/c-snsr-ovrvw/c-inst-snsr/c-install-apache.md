---
description: Instructies over om Server 2.0.40, 2.0.42 of later Apache te installeren en te vormen, Server 2.2 van Apache, of Server 2.4 Apache op Linux, Zon Solaris, of FreeBSD.
title: Apache Server 2.0.40, 2.0.42 of later, en Apache Server 2.2 of 2.4 op Linux, Solaris, of FreeBSD
uuid: 3703e2c1-5b8d-4def-b146-49e59d78a669
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Apache Server 2.0.40, 2.0.42 of later, en Apache Server 2.2 of 2.4 op Linux, Solaris, of FreeBSD{#apache-server-or-later-and-apache-server-or-on-linux-solaris-or-freebsd}

Instructies over om Server 2.0.40, 2.0.42 of later Apache te installeren en te vormen, Server 2.2 van Apache, of Server 2.4 Apache op Linux, Zon Solaris, of FreeBSD.

De programmadossiers voor Sensor worden verpakt in een installatiedossier dat u van de de downloadplaats van Adobe verkrijgt. Als u niet reeds het de installatiedossier van de Sensor voor uw bepaalde Webserver hebt, download het (of verkrijg het van uw vertegenwoordiger van Adobe) alvorens u met de volgende procedures begint.

Om Sensor te installeren en te vormen, moet u de volgende stappen op hoog niveau uitvoeren:

De volgende Apache-servers worden ondersteund:

* Apache Server 2.0.40 die onder RedHat Linux 7.x of later, of Zon Solaris SPARC 2.6 of later loopt.
* Apache Server 2.0.40, 2.0.42 of later, Apache Server 2.2, of Apache Server 2.4 op Linux, Sun Solaris, of FreeBSD
* Apache Server 2.0.42 of later die onder RedHat Linux 7.x of later, Zon Solaris SPARC 2.6 of later, SUSE Linux 9.x of later, of FreeBSD 5.3 loopt.
* Apache Server 2.0.42 of later die onder versies met 64 bits van RedHat Linux ES 4 en ES 5 loopt.
* Apache Server 2.2 die onder RedHat Linux 7.x of later of Sun Solaris SPARC 2.6 of later loopt.
* Apache Server 2.4 die onder RedHat Linux 7.x of later, of Sun Solaris x86_64, of FreeBSD loopt

>[!NOTE]
>
>Hoewel de instructies om Sensors op Webservers te installeren die versies 2.0.40 in werking stellen van de Server van Apache, 2.0.42 of later (met 32 bits en met 64 bits), of 2.2 het zelfde (behalve waar genoteerd in de volgende procedures) zijn, verschillen de installatiedossiers voor elke versie. Alvorens de sensor te installeren, zorg ervoor dat u de correcte installatiedossiers voor de Server van Apache en werkend systeemversies hebt ontvangen die u in werking stelt.

## De programmabestanden installeren {#section-2f3e85083b4f4aa989a85997330e86ae}

Procedure om de programmadossiers voor Sensor te halen en te installeren.

1. Opening van een sessie als wortelgebruiker of als gebruiker met wortelgezag.
1. Decompress en unpack het installatiedossier gebruikend het volgende bevel:

   * Op Linux:

      ```
      tar -zxf installationFilename
      ```

      ```
      unzip -d installationFilename.tar.gz 
       tar -xf installationFilename.tar
      ```

   * Op Solaris:

1. Kopieer de onverpakte programmadossiers aan de folders die in de volgende lijst worden geïdentificeerd:

<table id="table_ABFF5F92271B4F3CB0AC68DAB6A5709F"> 
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
   <td colname="col2"> De module van de inzamelaarbelasting. </td> 
   <td colname="col3"> <i> IBMHttpServer/modules</i> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>txlogge </p> </td> 
   <td colname="col2"> Het uitzendprogramma. </td> 
   <td colname="col3"> <p><i>/usr/local/bin</i> </p> <p><i>—OF—</i> </p> <p><i>/usr/local/sbin</i> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> txlogd.conf </td> 
   <td colname="col2"> Het de configuratiedossier van de Sensor. </td> 
   <td colname="col3"> <i>/etc</i> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> trust_ca_cert.pem </td> 
   <td colname="col2"> Het certificaat dat wordt gebruikt om het digitale certificaat te bevestigen dat de Server van het Inzicht tijdens het verbindingsproces voorstelt </td> 
   <td colname="col3"> <i>/usr/local/visual_sciences</i> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Het installatiepakket bevat een spreadsheetdossier genoemd TestExperiment.xls. Deze spreadsheet is een hulpmiddel dat de architecten gebruiken om een gecontroleerd experiment te vormen. De sensor zelf gebruikt dit dossier niet, zodat is het niet noodzakelijk om het dossier op de machine te installeren waar de Sensor loopt (hoewel u kunt verkiezen om dit te doen). U zou, in plaats daarvan, het dossier aan een plaats kunnen willen kopiëren waar uw architecten tot het kunnen toegang hebben of eenvoudig het dossier uit het installatiepakket halen zoals nodig. Voor meer informatie over gecontroleerde experimentatie, zie de Gids van de Experimenten van het Inzicht de Gecontroleerde.

**Toestemmingen op de programmabestanden**

>[!NOTE]
>
>De onjuiste toestemmingen op de programmadossiers veroorzaken de meerderheid van problemen die bij het installeren van Sensor worden ontmoet. Gelieve te zorgen ervoor dat u de toestemmingen precies zoals die in deze sectie wordt verklaard plaatst.
>
>Door gebrek, hebben de programmadossiers in het teerdossier de volgende toestemmingen. Afhankelijk van hoe uw systeem wordt gevormd, zouden deze montages (unmaskated) kunnen worden veranderd wanneer u de dossiers haalt. Om de toestemmingen aan de geadviseerde standaardmontages terug te stellen, gebruik hieronder de bevelen van de wortelmethode. Controle dat de folders waarin u de dossiers hebt geïnstalleerd minstens dit niveau van toegang toelaten.

| Bestand | Standaardrechten | chmod, opdracht |
|---|---|---|
| mod_visual_sciences.so | rwx r-x r-x | chmod 775 |
| txlogge | rwx —x —x | chmod 711 |
| txlogd.conf | rw- r— r— r— | chmod 664 |
| trust_ca_cert.pem | rw- r— r— r— | chmod 664 |

## Aanmelden inschakelen op Sametime Server {#section-2e2f1875a5304cdfa2cbcd0680683cfd}

Stappen die u toestaan om aan de Server te registreren Sametime.

1. Gebruik de Lotus Domino Administrator-client om verbinding te maken met de Lotus Domino-server waarop Sametime wordt uitgevoerd.
1. In de Beheerder van de Domino van Lotus, klik het lusje van Dossiers, dan tweemaal klik Configuratie Sametime - stconfig.nsf om het dossier van de Configuratie te openen Sametime.
1. In het dossier van de Configuratie Sametime, open het formulier van de Diensten van de Gemeenschap en klik overal op het formulier tweemaal om binnen te gaan uitgeven wijze.
1. De vastgestelde Vlag van de Registratie van het Praatje aan &quot;streng&quot;en vangt het Type van Dienst aan &quot;0x1000.&quot;
1. Sparen en sluit de vorm van de Diensten Communautaire, dan sluit het dossier van de Configuratie Sametime.
1. Start de Sametime-server opnieuw.

## Geef het Dossier van de Configuratie van de Sensor uit {#section-de0eb4a646394b61abb6cd5a2b706de0}

Het [!DNL txlogd.conf] dossier bevat de configuratieparameters voor Sensor.

U moet dit dossier uitgeven om, onder andere, de grootte en de plaats van het dossier van de schijfrij, het adres van de Server van het Inzicht, en identiteitskaart te specificeren die aan de gebeurtenisgegevens zal worden vastgemaakt die door deze sensor worden geproduceerd.

Het configuratiedossier bevat vereiste parameters en facultatieve parameters.

* **De vereiste parameters** zijn montages die u moet specificeren wanneer u Sensor installeert. Zonder deze montages, loopt de Sensor niet met succes.
* **De facultatieve parameters** zijn montages die aan vooraf bepaalde waarden (die u kunt wijzigen) in gebreke blijven of facultatieve eigenschappen toelaten.

**Om het de configuratiedossier van de Sensor uit te geven**

* Open het [!DNL /etc/txlogd.conf] dossier in een tekstredacteur en plaats de vereiste parameters evenals om het even welke gewenste facultatieve parameters.
* Sparen en sluit het dossier.

**Om het de configuratiedossier van de Sensor uit te geven**

1. Open het [!DNL /etc/txlogd.conf] dossier in een tekstredacteur en plaats de vereiste parameters evenals om het even welke gewenste facultatieve parameters.
1. Sparen en sluit het dossier.

## Start de zender en maak de schijfwachtrij {#section-55630de65f264274aefd771da2002852}

Nadat u het txlogd.conf- dossier vormt, kunt u het transmissieprogramma beginnen, het registreren als dienst van Vensters, en de schijfrij creëren.

1. Als de folder waarin de schijfrij verblijft niet reeds bestaat, creeer het. Zorg ervoor dat de folder zowel de inzamelaarmodule als het uitzendingsprogramma van lees-schrijftoegang tot het dossier voorziet.

   Voor meer informatie over de toestemmingen die door de dossiers van de schijfrij worden vereist, zie de Toestemmingen van het Dossier van UNIX van de Sensor.
1. Op de computer waar de Sensor geïnstalleerd is, voer het volgende bevel uit om de zender te beginnen:

   ```
   /usr/local/bin/txlogd -ic -f /etc/txlogd.conf
   ```

   * De &quot;i&quot;optie in dit bevel begint de zender op &quot;interactieve wijze.&quot; Deze wijze toont zenderberichten op het scherm en laat u ook toe om met de zender in wisselwerking te staan gebruikend toetsenbordbevelen.
   * De &quot;c&quot;optie leidt de zender om de schijfrij tot stand te brengen.
   * De &quot;f&quot;optie specificeert de plaats van het configuratiedossier.
   Voor extra informatie over de opties kunt u gebruiken wanneer het beginnen van de zender, zie de Zender bevel-Lijn Opties van de Zender overbrengt.

1. Verifieer dat de zender de schijfrij in de plaats gecreeerd heeft die in de parameter QueueFile en van de grootte in de parameter QueueSize wordt gespecificeerd.
1. Als de rij niet correct is gecreeerd, type Ctrl+C om de zender te eindigen, dan doe het volgende:

   1. Onderzoek het txtlogd.conf- dossier en verifieer dat de parameters QueueFile en QueueSize correct worden geplaatst.
   1. Controle dat het apparaat waaraan de schijfrij wordt toegewezen operationeel is en voldoende ruimte beschikbaar heeft om een dossier van de grootte te houden die in de parameter QueueSize wordt gespecificeerd.
   1. Breng de nodige correcties aan en herhaal deze procedure.

## Voeg de Collector aan de Server van het Web toe {#section-c5b83ae4ebce430aa764f951e849b333}

Voor de servers van HTTP van IBM, is de inzamelaar een dynamisch gedeeld voorwerp dat u in uw proces van de Webserver laadt.

Om de inzamelaar aan uw Webserver toe te voegen, moet u het httpd.conf- dossier uitgeven zoals hieronder beschreven en uw Webserver opnieuw beginnen.

Als de Sensor gegevens voor veelvoudige Webservers op de servercomputer vangt, moet u de volgende procedure voor elke Webserver uitvoeren.

1. Gebruikend een tekstredacteur, open het httpd.conf- dossier voor de Webserver de waarvan gebeurtenissenSensor vangt.
1. Voeg de volgende twee lijnen aan het eind van het dossier toe:

   ```
   LoadModule visual_sciences_module modules/mod_visual_sciences.so 
   VisualSciencesConfig /etc/txlogd.conf
   ```

   >[!NOTE]
   >
   >Deze lijnen zijn hoofdlettergevoelig. Typ hen precies zoals zij hierboven verschijnen.

1. Start het webserverproces opnieuw op (u hoeft de volledige servercomputer niet opnieuw op te starten, start het webserverproces gewoon opnieuw op). De inzamelaar wordt geladen met de Webserver en begint inzamelend gebeurtenisgegevens en schrijvend het aan de schijfrij.

## Test de sensor {#section-0dae181ef8884f10a57f6cfda8500969}

Verifieer dat de inzamelaar gebeurtenisgegevens verzamelt en de zender het naar de Server van het doelInzicht overbrengt.

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
   * De parameters ServerAddress en ServerPort worden correct geplaatst in txtlogd.conf. Als u ServerAddress gebruikend een servernaam specificeerde, probeer in plaats daarvan gebruikend zijn numeriek IP adres.
   * De waarde van de parameter CertName past de gemeenschappelijke naam aan die op het digitale certificaat van de Server van het doelInzicht precies verschijnt.

## Voeg de Transmitter aan het Opstartmanuscript van het Systeem toe {#section-19a38f27c9f44adf88f8910f5ed483a3}

Informatie over het automatisch laden van de zender aan uw systeem startmanuscript.

Om ervoor te zorgen dat de zenderladingen automatisch wanneer de machine van de Webserver opnieuw is begonnen, voeg het volgende bevel (dat de zender) aan uw systeem startmanuscript lanceert toe:

```
/usr/local/bin/txlogd -f /etc/txlogd.conf
```

Dit bevel begint de zender als daemon. De werkende en foutenmeldingen die de zender produceert worden geschreven aan syslog.
