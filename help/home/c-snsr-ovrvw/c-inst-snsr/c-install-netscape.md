---
description: Instructies voor het installeren en het vormen Sensor op de familie van Webservers die van de originele Server van het Web van de Onderneming van Netscape die op Linux of machines van Solaris loopt evolueerden. Bevat Netscape Enterprise, iPlanet, Sun ONE en Sun Java System Servers op Linux of Solaris.
title: Netscape Enterprise op Linux of Solaris
uuid: 47ea614c-d45c-4ab4-a8fe-ed9227da4582
exl-id: bd2e50b9-94fe-4f05-b227-11e83eb0a665
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '1494'
ht-degree: 0%

---

# Netscape Enterprise op Linux of Solaris{#netscape-enteprise-on-linux-or-solaris}

{{eol}}

Instructies voor het installeren en het vormen Sensor op de familie van Webservers die van de originele Server van het Web van de Onderneming van Netscape die op Linux of machines van Solaris loopt evolueerden. Bevat Netscape Enterprise, iPlanet, Sun ONE en Sun Java System Servers op Linux of Solaris.

De programmabestanden voor Sensor worden verpakt in een installatiebestand dat u van de downloadsite van de Adobe ontvangt. Als u nog geen Sensor-installatiebestand voor uw specifieke webserver hebt, downloadt u het bestand (of vraagt u het op bij uw Adobe-vertegenwoordiger) voordat u de volgende procedures start.

Sensor ondersteunt de volgende servers die worden uitgevoerd onder RedHat Linux 7.x of hoger of Sun Solaris SPARC 2.6 of hoger:

* Netscape Enterprise Server 3.6 of hoger
* iPlanet Web Server 4.0 of hoger

Sensor ondersteunt deze servers die worden uitgevoerd onder RedHat Linux 7.x of hoger of Sun Solaris 8.x of hoger:

* Sun ONE Web Server 6.0 of hoger
* Sun Java System Web Server 6.1 of hoger

De sensor steunt deze servers die onder Zon Solaris x86 9 of later lopen:

* Sun Java System Web Server 6.1 of hoger

>[!NOTE]
>
>Het installatiebestand voor deze reeks webservers wordt weergegeven als &quot;Netscape Solaris Sensor&quot; of &quot;Netscape LINUX Sensor&quot; op de downloadsite van Adobe.

Als u Sensor wilt installeren en configureren, moet u de volgende stappen uitvoeren:

## De programmabestanden installeren {#section-2f3e85083b4f4aa989a85997330e86ae}

Procedure voor het uitpakken en installeren van de programmabestanden voor Sensor.

1. Meld u aan als de hoofdgebruiker of als een gebruiker met basisbevoegdheid.
1. Decomprimeer en pak het installatiebestand uit met de volgende opdracht:

   ```
   gunzip installationFilename.tar.gz 
   
       tar -xf installationFilename.tar
   ```

1. Kopieer de onverpakte programmabestanden naar de mappen in de volgende tabel:

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
   <td colname="col2"> De module voor het laden van verzamelingen. </td> 
   <td colname="col3"> <i>/usr/local/aolserver/visual_sciences</i> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>txlogd </p> </td> 
   <td colname="col2"> Het verzendprogramma. </td> 
   <td colname="col3"> <p><i>/usr/local/bin</i> </p> <p><i>—OF—</i> </p> <p><i>/usr/local/sbin</i> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> txlogd.conf </td> 
   <td colname="col2"> Het Sensor-configuratiebestand. </td> 
   <td colname="col3"> <i>/etc</i> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> trust_ca_cert.pem </td> 
   <td colname="col2"> Het certificaat dat wordt gebruikt om het digitale certificaat te bevestigen dat de Server van het Inzicht tijdens het verbindingsproces presenteert </td> 
   <td colname="col3"> <i>/usr/local/visual_sciences</i> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Het installatiepakket bevat een spreadsheetbestand met de naam TestExperiment.xls. Dit spreadsheet is een hulpmiddel dat de architecten gebruiken om een gecontroleerd experiment te vormen. Sensor zelf gebruikt dit bestand niet. U hoeft het bestand dus niet te installeren op de computer waarop de Sensor wordt uitgevoerd (maar u kunt dit desgewenst doen). In plaats daarvan kunt u het bestand kopiëren naar een locatie waar uw architecten het kunnen openen of het bestand gewoon uit het installatiepakket extraheren. Zie de Gids met gecontroleerde experimenten voor meer informatie over gecontroleerde experimenten.

**Machtigingen voor de programmabestanden**

>[!NOTE]
>
>Onjuiste machtigingen voor de programmabestanden veroorzaken de meeste problemen die worden aangetroffen bij de installatie van de sensor. Controleer of u de machtigingen precies instelt zoals in deze sectie wordt vermeld.
>
>Standaard hebben de programmabestanden in het teerbestand de volgende machtigingen. Afhankelijk van hoe uw systeem wordt gevormd, zouden deze montages (unmasked) kunnen worden veranderd wanneer u de dossiers haalt. Als u de machtigingen wilt terugzetten op de aanbevolen standaardinstellingen, gebruikt u de onderstaande opdrachten voor onderliggende items. Controleer of de mappen waarin u de bestanden hebt geïnstalleerd, ten minste dit toegangsniveau toestaan.

| Bestand | Standaardmachtigingen | chmod, opdracht |
|---|---|---|
| mod_visual_sciences.so | rwx r-x r-x | chmod 775 |
| txlogd | rwx —x —x | chmod 711 |
| txlogd.conf | rw- r— r— | chmod 664 |
| trust_ca_cert.pem | rw- r— r— | chmod 664 |

## Het configuratiebestand van de sensor bewerken {#section-2e2f1875a5304cdfa2cbcd0680683cfd}

De [!DNL txlogd.conf] bevat de configuratieparameters voor Sensor.

U moet dit dossier uitgeven om, onder andere, de grootte en de plaats van het dossier van de schijfrij, het adres van de Server van het Inzicht, en identiteitskaart te specificeren die aan de gebeurtenisgegevens zal worden vastgemaakt die door deze sensor worden geproduceerd.

Het configuratiebestand bevat vereiste parameters en optionele parameters.

* **Vereiste parameters** Dit zijn instellingen die u moet opgeven wanneer u Sensor installeert. Zonder deze instellingen wordt Sensor niet uitgevoerd.
* **Optionele parameters** Dit zijn instellingen die standaard op vooraf gedefinieerde waarden (die u kunt wijzigen) of die optionele functies inschakelen.

**Het Sensor-configuratiebestand bewerken**

* Open de [!DNL /etc/txlogd.conf] in een teksteditor en stel de vereiste parameters en eventueel gewenste optionele parameters in.
* Sla het bestand op en sluit het.

**Het Sensor-configuratiebestand bewerken**

1. Open de [!DNL /etc/txlogd.conf] in een teksteditor en stel de vereiste parameters en eventueel gewenste optionele parameters in.
1. Sla het bestand op en sluit het.

## De zender starten en de schijfwachtrij maken {#section-55630de65f264274aefd771da2002852}

Nadat u het bestand txlogd.conf hebt geconfigureerd, kunt u het verzendprogramma starten, het registreren als Windows-service en de schijfwachtrij maken.

1. Als de map waarin de schijfwachtrij zich bevindt, nog niet bestaat, maakt u deze. Zorg ervoor dat de map zowel de verzamelaarmodule als het verzendprogramma lees- en schrijftoegang tot het bestand biedt.

   Voor meer informatie over de toestemmingen die door de dossiers van de schijfrij worden vereist, zie de Toestemmingen van het Dossier van UNIX van de Sensor.
1. Voer op de computer waarop Sensor is geïnstalleerd de volgende opdracht uit om de zender te starten:

   ```
   /usr/local/bin/txlogd -ic -f /etc/txlogd.conf
   ```

   * Met de optie &quot;i&quot; in deze opdracht start u de zender in de interactieve modus. In deze modus worden verzendberichten op het scherm weergegeven en kunt u met behulp van toetsenbordopdrachten communiceren met de zender.
   * De optie &quot;c&quot; geeft de zender de opdracht de schijfwachtrij te maken.
   * Met de optie &quot;f&quot; geeft u de locatie van het configuratiebestand op.

   Voor extra informatie over de opties u kunt gebruiken wanneer het beginnen van de zender, zie de Opdracht-Lijnopties van de Zender.

1. Verifieer dat de zender de schijfrij in de plaats heeft gecreeerd die in de parameter QueueFile en van de grootte in de parameter QueueSize wordt gespecificeerd.
1. Als de rij niet correct is gecreeerd, type Ctrl+C om de zender te eindigen, dan doe het volgende:

   1. Onderzoek het txtlogd.conf- dossier en verifieer dat de parameters QueueFile en QueueSize correct worden geplaatst.
   1. Controleer of het apparaat waaraan de schijfrij wordt toegewezen operationeel is en voldoende ruimte beschikbaar heeft om een dossier van de grootte te houden die in de parameter QueueSize wordt gespecificeerd.
   1. Breng de nodige correcties aan en herhaal deze procedure.

## De Collector toevoegen aan de AOL-server {#section-c5b83ae4ebce430aa764f951e849b333}

Voor AOLServer, is de inzamelaar een dynamisch gedeeld voorwerp dat u in uw proces van de Webserver laadt.

Als u de verzamelaar wilt toevoegen aan uw AOL-server, moet u het configuratiebestand voor uw server bewerken zoals hieronder beschreven en de AOL-server opnieuw starten. Gewoonlijk heeft het configuratiebestand van de server de naam nsd.tcl en bevindt het zich in de map waarin AOL Server is geïnstalleerd.

1. Open het configuratiebestand in een teksteditor en zoek de volgende sectie:

   ```
   ns_section "ns/server/${servername}/modules" 
   ```

1. Voeg de volgende regel toe. (Toevoegen als één instructie. Tekstomloop negeren zoals hieronder wordt weergegeven.)

   ```
   ns_param aol_visual_sciences /usr/local/aolserver/visual_sciences/aol_visual_sciences.so 
   ```

1. Maak als volgt een nieuwe sectie.

   ```
   ns_section "ns/server/${servername}/module/aol_visual_sciences"
   ```

1. Aan deze nieuwe sectie, voeg de lijn toe:

   ```
   ns_param    VisualSciencesConfig    /etc/txlogd.conf
   ```

   >[!NOTE]
   >
   >Deze regels zijn hoofdlettergevoelig. Typ deze precies zoals ze hierboven worden weergegeven.

1. Start de AOL-server opnieuw. De verzamelaar wordt geladen en begint gebeurtenisgegevens te verzamelen en naar de schijfwachtrij te schrijven.

## De sensor testen {#section-0dae181ef8884f10a57f6cfda8500969}

Verifieer dat de inzamelaar gebeurtenisgegevens verzamelt en de zender het naar de Server van het doelInzicht overbrengt.

>[!NOTE]
>
>Om te verifiëren dat de zender gebeurtenisgegevens naar de Server van het Inzicht kan met succes verzenden, zorg ervoor dat de Server van het DoelInzicht geïnstalleerd en lopend is alvorens u met de volgende test begint.

1. Als de zender nog niet actief is, start u deze opnieuw met de volgende opdracht:

   ```
   /usr/local/bin/txlogd -i -f /etc/txlogd.conf 
   ```

1. Open een browser (op een willekeurige computer) en vraag een pagina aan bij de webserver waarop Sensor wordt uitgevoerd (selecteer een pagina die wordt gecontroleerd door Sensor).
1. Nadat u het verzoek uitgeeft, controleer de console van de zender berichten erop wijzen die dat het gebeurtenisgegevens naar de Server van het doelInzicht verzendt.
1. Als Sensor gegevens niet verzendt, controleert u of:

   * De doelserver van het Inzicht loopt.
   * De parameters ServerAddress en ServerPort worden correct geplaatst in txtlogd.conf. Als u ServerAddress hebt opgegeven met een servernaam, probeert u in plaats daarvan het numerieke IP-adres te gebruiken.
   * De waarde van de parameter CertName past precies de gemeenschappelijke naam aan die op het digitale certificaat van de server van het doelInzicht verschijnt.

## De zender toevoegen aan het opstartscript van het systeem {#section-19a38f27c9f44adf88f8910f5ed483a3}

Informatie over het automatisch laden van de zender aan uw systeem startmanuscript.

Om ervoor te zorgen dat de zender automatisch wordt geladen wanneer de machine van de Webserver opnieuw wordt begonnen, voeg het volgende bevel (dat de zender) aan uw systeem startmanuscript toe:

```
/usr/local/bin/txlogd -f /etc/txlogd.conf
```

Met deze opdracht start u de zender als een daemon. De werking en de foutenmeldingen die de zender produceert worden geschreven aan [!DNL syslog].

De standaardinstelling Solaris is 60. Op basis van tests die zijn uitgevoerd met Sensor, waarbij voor elke instantie drie semafoons worden gebruikt, raadt Adobe u aan 1024 te gebruiken als de instelling. Dit aantal is hoog genoeg voor Sensor om samen met andere toepassingen op de server te functioneren die semafoons kunnen vereisen, maar beïnvloedt prestaties niet. Ter ondersteuning van deze aanbeveling merkt Adrian Cockcroft het volgende op in zijn boek Sun Performance and Tuning (Prentice Hall, oktober 1994): &quot;Databases gebruiken doorgaans veel gedeelde geheugen- en semafoore-instellingen. Deze zijn niet van invloed op de prestaties; zolang ze groot genoeg zijn , zullen de programma &#39; s lopen . &quot;
