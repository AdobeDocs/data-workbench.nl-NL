---
description: Gedetailleerde instructies voor het installeren en configureren van Sensor voor een Apache Server 1.3.x op RedHat Linux 7.x of hoger, SUSE Linux 9.x of hoger, Sun Solaris SPARC 2.6 of hoger, Sun Solaris x86 9 of hoger, FreeBSD 4 of hoger of Mac OS X PowerPC.
title: Apache Server 1.3.x op Linux, Sun Solaris, FreeBSD of Mac OS X
uuid: bd46dd0f-fe36-4f8b-a87c-8ca7b64da609
translation-type: tm+mt
source-git-commit: 98452ba81d71db65c75e3d07712eefa18c003f53
workflow-type: tm+mt
source-wordcount: '1345'
ht-degree: 0%

---


# Apache Server 1.3.x op Linux, Sun Solaris, FreeBSD of Mac OS X{#apache-server-x-on-linux-sun-solaris-freebsd-or-mac-os-x}

Gedetailleerde instructies voor het installeren en configureren van Sensor voor een Apache Server 1.3.x op RedHat Linux 7.x of hoger, SUSE Linux 9.x of hoger, Sun Solaris SPARC 2.6 of hoger, Sun Solaris x86 9 of hoger, FreeBSD 4 of hoger of Mac OS X PowerPC.

De programmabestanden voor Sensor worden verpakt in een installatiebestand dat u van de downloadsite van de Adobe ontvangt. Als u nog geen Sensor-installatiebestand voor uw specifieke webserver hebt, downloadt u het bestand (of vraagt u het op bij uw Adobe-vertegenwoordiger) voordat u de volgende procedures start.

U moet de volgende stappen op hoog niveau uitvoeren om Sensor te installeren en te configureren:

## De programmabestanden installeren {#section-aae323e252394212bf4096d65fdd280c}

Instructies voor het uitpakken en installeren van de programmabestanden voor Sensor op de servercomputer.

1. Meld u aan als de hoofdgebruiker of als een gebruiker met basisbevoegdheid.
1. Decomprimeer en pak het installatiebestand uit met de volgende opdracht:

   * In Linux:

      ```
      tar -zxf installationFilename.tar.gz
      ```

   * Op Solaris:

      ```
      unzip -d installationFilename.tar.gz 
       tar -xf installationFilename.tar
      ```

1. Kopieer de onverpakte programmabestanden naar de mappen in de volgende tabel:

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
   <td colname="col2"> De module voor het laden van verzamelingen </td> 
   <td colname="col3"> apachePath/libexec </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>txlogd </p> </td> 
   <td colname="col2"> Het uitzendprogramma </td> 
   <td colname="col3"> <p>/usr/local/bin </p> <p>—OF— </p> <p>/usr/local/sbin </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> txlogd.conf </td> 
   <td colname="col2"> Het Sensor-configuratiebestand </td> 
   <td colname="col3"> /etc </td> 
  </tr> 
  <tr> 
   <td colname="col1"> trust_ca_cert.pem </td> 
   <td colname="col2"> Het certificaat dat wordt gebruikt om het digitale certificaat te bevestigen dat de Server van het Inzicht tijdens het verbindingsproces presenteert </td> 
   <td colname="col3"> /usr/local/visual_sciences </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Het installatiepakket bevat een spreadsheetbestand met de naam TestExperiment.xls. Dit spreadsheet is een hulpmiddel dat de architecten gebruiken om een gecontroleerd experiment te vormen. Sensor zelf gebruikt dit bestand niet. U hoeft het bestand dus niet te installeren op de computer waarop Sensor wordt uitgevoerd (hoewel u dit kunt doen). In plaats daarvan kunt u het bestand kopiëren naar een locatie waar uw architecten het kunnen openen of het bestand gewoon uit het installatiepakket extraheren. Zie de Gids met gecontroleerde experimenten voor meer informatie over gecontroleerde experimenten.

**Machtigingen voor de programmabestanden**

Onjuiste machtigingen voor de programmabestanden veroorzaken de meeste problemen die worden aangetroffen bij de installatie van de sensor.

Controleer of u de machtigingen precies instelt zoals in deze sectie wordt vermeld.

Standaard hebben de programmabestanden in het teerbestand de volgende machtigingen. Afhankelijk van hoe uw systeem wordt gevormd, zouden deze montages (unmasked) kunnen worden veranderd wanneer u de dossiers haalt. Als u de machtigingen wilt terugzetten op de aanbevolen standaardinstellingen, gebruikt u de onderstaande opdrachten voor onderliggende items. Controleer of de mappen waarin u de bestanden hebt geïnstalleerd, ten minste dit toegangsniveau toestaan.

| Bestand | Standaardmachtigingen | chmod, opdracht |
|---|---|---|
| mod_visual_sciences.so | rwx r-x r-x | chmod 755 |
| txlogd | rwx —x —x | chmod 711 |
| txlogd.conf | rw- rw- r— | chmod 664 |
| trust_ca_cert.pem | rw- rw- r— | chmod 664 |

## Het Sensor-configuratiebestand bewerken {#section-3f22a1c91d7d43b6b4c30f1b7448b17f}

Het [!DNL txlogd.conf] bestand bevat de configuratieparameters voor Sensor.

U moet het dossier uitgeven om, onder andere, de grootte van de schijfrij, het adres van de Server van het Inzicht, en identiteitskaart te specificeren die aan de gegevens zal worden vastgemaakt die door deze sensor worden geproduceerd.

Het configuratiebestand bevat vereiste parameters en optionele parameters.

* Vereiste parameters zijn instellingen die u moet opgeven wanneer u Sensor installeert. Zonder deze instellingen wordt Sensor niet uitgevoerd.
* Optionele parameters zijn instellingen die standaard op vooraf gedefinieerde waarden (die u kunt wijzigen) of optionele functies inschakelen.

Het Sensor-configuratiebestand bewerken

1. Open het bestand /etc/txlogd.conf in een teksteditor en stel de vereiste parameters en eventueel gewenste optionele parameters in.
1. Sla het bestand op en sluit het.

## De zender starten en de schijfwachtrij maken {#section-a453d912ec3d47aa8e40ccacf527119d}

Instructies om de schijfrij te creëren nadat u het txlogd.conf- dossier vormt.

1. Als de map waarin de schijfwachtrij zich bevindt, nog niet bestaat, maakt u deze. Zorg ervoor dat de map zowel de verzamelaarmodule als het verzendprogramma lees- en schrijftoegang tot het bestand biedt.
1. Voer op de computer waarop Sensor is geïnstalleerd de volgende opdracht uit om de zender te starten:

   ```
   /usr/local/bin/txlogd -ic -f /etc/txlogd.conf
   ```

   * Met de optie &quot;i&quot; in deze opdracht start u de zender in de interactieve modus. In deze modus worden verzendberichten op het scherm weergegeven en kunt u met behulp van toetsenbordopdrachten communiceren met de zender.
   * De optie &quot;c&quot; geeft de zender de opdracht de schijfwachtrij te maken.
   * Met de optie &quot;f&quot; geeft u de locatie van het configuratiebestand op.

1. Verifieer dat de zender de schijfrij in de plaats heeft gecreeerd die in de parameter QueueFile en van de grootte in de parameter QueueSize wordt gespecificeerd.
1. Als de rij niet correct is gecreeerd, type Ctrl+C om de zender te eindigen, dan doe het volgende:

   1. Onderzoek het txtlogd.conf- dossier en verifieer dat de parameters QueueFile en QueueSize correct worden geplaatst.
   1. Controleer of het apparaat waaraan de schijfrij wordt toegewezen operationeel is en voldoende ruimte beschikbaar heeft om een dossier van de grootte te houden die in de parameter QueueSize wordt gespecificeerd.
   1. Breng de nodige correcties aan en herhaal deze procedure.

## Voeg de Collector aan de Server van het Web toe {#section-a7fb6425956f4f518ae3a7db091b33d2}

Voor Apache-servers is de verzamelaar een dynamisch, gezamenlijk object dat u in uw webserverproces laadt.

Als u de verzamelaar aan uw webserver wilt toevoegen, moet u het bestand httpd.conf bewerken zoals hieronder wordt beschreven en de webserver opnieuw starten.

Als Sensor gegevens vastlegt voor meerdere webservers op de servercomputer, moet u de volgende procedure voor elke webserver uitvoeren.

1. Open met een teksteditor het [!DNL httpd.conf] bestand voor de webserver waarvan de gebeurtenissen worden vastgelegd door Sensor.
1. Voeg de volgende regels toe aan het einde van het bestand:

   ```
   LoadModule  visual_sciences_module  libexec/mod_visual_sciences.so 
   VisualSciencesConfig  /etc/txlogd.conf 
   AddModule mod_visual_sciences.c
   ```

   >[!NOTE]
   >
   >Deze regels zijn hoofdlettergevoelig. Typ deze precies zoals ze hierboven worden weergegeven.

1. Start de webserver opnieuw. De verzamelaar wordt met de webserver geladen en zal gebeurtenisgegevens verzamelen en naar de schijfwachtrij schrijven.

## De sensor testen {#section-83d9f60b39a6474f9c76bee3e19b2575}

Begin de zender en verifieer dat het met succes met de Server van het Inzicht kan verbinden en gebeurtenisgegevens naar het overbrengen.

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
   * De parameters [!DNL ServerAddress] en [!DNL ServerPort] worden correct ingesteld in [!DNL txtlogd.conf].

   * Als u een servernaam hebt opgegeven, probeert u in plaats daarvan het numerieke IP-adres te gebruiken. [!DNL ServerAddress] De waarde van de [!DNL CertName] parameter komt precies overeen met de algemene naam die op het digitale certificaat van de doelserver van het Inzicht wordt weergegeven.

## De zender toevoegen aan het opstartscript van het systeem {#section-4e1ffa6e043941ab91411d91d596477a}

Informatie om ervoor te zorgen dat de zender automatisch wordt geladen wanneer de webservercomputer opnieuw wordt opgestart.

Voeg het volgende bevel (dat de zender) aan uw systeem startscript toe.

```
/usr/local/bin/txlogd -f /etc/txlogd.conf
```

Met deze opdracht start u de zender als een daemon. De werkende en foutenmeldingen die de zender produceert worden geschreven aan syslog.

>[!NOTE]
>
>Sommige Solaris-gebruikers kunnen een fout &quot;kunnen mutex niet verkrijgen&quot; tegenkomen. Voor een correcte werking van de Sensor op deze systemen, moet de volgende lijn of worden toegevoegd aan of in het dossier /etc/system uitgeven:
>
>
```
>semsys:seminfo_semmnu=1024
>```
>
>De standaardinstelling Solaris is 60. Op basis van tests die zijn uitgevoerd met Sensor, waarbij voor elke instantie drie semafoons worden gebruikt, raadt Adobe u aan 1024 te gebruiken als de instelling. Dit aantal is hoog genoeg voor Sensor om samen met andere toepassingen op de server te functioneren die semafoons kunnen vereisen, maar beïnvloedt prestaties niet. Ter ondersteuning van deze aanbeveling merkt Adrian Cockcroft het volgende op in zijn boek Sun Performance and Tuning (Prentice Hall, oktober 1994): &quot;Databases gebruiken doorgaans veel gedeelde geheugen- en semafoore-instellingen. Deze zijn niet van invloed op de prestaties; zolang ze groot genoeg zijn , zullen de programma &#39; s lopen . &quot;

