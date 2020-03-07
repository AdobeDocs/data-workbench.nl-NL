---
description: Instructies voor het installeren van en het vormen van Sensor op de familie van Webservers die van de originele Server evolueerden van het Web van de Onderneming van Netscape die op de machines van Linux of van Solaris loopt. Omvat de Onderneming van Netscape, iPlanet, Zon ONE, en de Servers van het Systeem van Java van de Zon op Linux of Solaris.
title: Netscape Enterprise op Linux of Solaris
uuid: 47ea614c-d45c-4ab4-a8fe-ed9227da4582
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Netscape Enterprise op Linux of Solaris{#netscape-enteprise-on-linux-or-solaris}

Instructies voor het installeren van en het vormen van Sensor op de familie van Webservers die van de originele Server evolueerden van het Web van de Onderneming van Netscape die op de machines van Linux of van Solaris loopt. Omvat de Onderneming van Netscape, iPlanet, Zon ONE, en de Servers van het Systeem van Java van de Zon op Linux of Solaris.

De programmadossiers voor Sensor worden verpakt in een installatiedossier dat u van de de downloadplaats van Adobe verkrijgt. Als u niet reeds het de installatiedossier van de Sensor voor uw bepaalde Webserver hebt, download het (of verkrijg het van uw vertegenwoordiger van Adobe) alvorens u met de volgende procedures begint.

De sensor steunt de volgende servers die onder RedHat Linux 7.x of later of Sun Solaris SPARC 2.6 of later lopen:

* Netscape Enterprise Server 3.6 of hoger
* iPlanet Web Server 4.0 of hoger

De sensor steunt deze servers die onder RedHat Linux 7.x of later of Zon Solaris 8.x of later lopen:

* Sun ONE Web Server 6.0 of hoger
* Sun Java System Web Server 6.1 of hoger

De sensor steunt deze servers die onder Zon Solaris x86 9 lopen of later:

* Sun Java System Web Server 6.1 of hoger

>[!NOTE]
>
>Het installatiedossier voor deze familie van Webservers is vermeld als &quot;Sensor van Solaris van Netscape&quot;of &quot;Sensor van LINUX van Netscape&quot;op de de downloadplaats van Adobe.

Om Sensor te installeren en te vormen, moet u de volgende stappen uitvoeren:

## De programmabestanden installeren {#section-2f3e85083b4f4aa989a85997330e86ae}

Procedure om de programmadossiers voor Sensor te halen en te installeren.

1. Opening van een sessie als wortelgebruiker of als gebruiker met wortelgezag.
1. Decompress en unpack het installatiedossier gebruikend het volgende bevel:

   ```
   gunzip installationFilename.tar.gz 
   
       tar -xf installationFilename.tar
   ```

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
   <td colname="col1"> aol_visual_sciences.so </td> 
   <td colname="col2"> De module van de inzamelaarbelasting. </td> 
   <td colname="col3"> <i>/usr/local/aolserver/visual_sciences</i> </td> 
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

## Geef het Dossier van de Configuratie van de Sensor uit {#section-2e2f1875a5304cdfa2cbcd0680683cfd}

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

## Voeg de Collector aan de Server van AOL toe {#section-c5b83ae4ebce430aa764f951e849b333}

Voor AOLServer, is de inzamelaar een dynamisch gedeeld voorwerp dat u in uw proces van de Webserver laadt.

Om de collector aan uw AOL-server toe te voegen, moet u het configuratiebestand voor uw server bewerken zoals hieronder wordt beschreven en uw AOL-server opnieuw starten. Gewoonlijk wordt het de configuratiedossier van de server genoemd nsd.tcl en in de folder gevestigd waar de Server van AOL geïnstalleerd is.

1. Open het configuratiedossier in een tekstredacteur en bepaal de plaats van de volgende sectie:

   ```
   ns_section "ns/server/${servername}/modules" 
   ```

1. Voeg de volgende lijn toe. (Voeg als één enkele verklaring toe. Negeer woordomslag hieronder getoond.)

   ```
   ns_param aol_visual_sciences /usr/local/aolserver/visual_sciences/aol_visual_sciences.so 
   ```

1. Creeer als volgt een nieuwe sectie.

   ```
   ns_section "ns/server/${servername}/module/aol_visual_sciences"
   ```

1. Aan deze nieuwe sectie, voeg de lijn toe:

   ```
   ns_param    VisualSciencesConfig    /etc/txlogd.conf
   ```

   >[!NOTE]
   >
   >Deze lijnen zijn hoofdlettergevoelig. Typ hen precies zoals zij hierboven verschijnen.

1. Start de AOL-server opnieuw op. De collector wordt geladen en zal beginnen met het verzamelen van gebeurtenisgegevens en het schrijven van het aan de schijfrij.

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

Dit bevel begint de zender als daemon. De werkende en foutenmeldingen die de zender produceert worden geschreven aan [!DNL syslog].

Standaard het plaatsen van Solaris is 60. Gebaseerd op tests die met Sensor worden uitgevoerd, die drie semafoons voor elke instantie gebruikt, adviseert Adobe dat u 1024 als uw het plaatsen gebruikt. Dit aantal is hoog genoeg voor Sensor om samen met een andere toepassingen op de server te functioneren die semafoons kunnen vereisen, maar beïnvloedt prestaties niet. Ter ondersteuning van deze aanbeveling merk ik op dat Adrian Cockcroft in zijn boek Sun Performance and Tuning (Prentice Hall, oktober 1994) het volgende verklaarde: &quot;De gegevensbestanden neigen om veel gedeeld geheugen en semafoermontages te gebruiken. Deze hebben geen invloed op de prestaties; zolang ze groot genoeg zijn , zullen de programma &#39; s lopen . &quot;
