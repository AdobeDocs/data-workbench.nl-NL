---
description: Instructies voor het installeren en configureren van Apache Server 2.0.40, 2.0.42 of hoger, Apache Server 2.2 of Apache Server 2.4 op Linux, Sun Solaris of FreeBSD.
title: Apache Server 2.0.40, 2.0.42 of hoger en Apache Server 2.2 of 2.4 op Linux, Solaris of FreeBSD
uuid: 3703e2c1-5b8d-4def-b146-49e59d78a669
exl-id: d5b943be-e9ca-4601-88c7-bb2bfdc0d080
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '1546'
ht-degree: 0%

---

# Apache Server 2.0.40, 2.0.42 of hoger en Apache Server 2.2 of 2.4 op Linux, Solaris of FreeBSD{#apache-server-or-later-and-apache-server-or-on-linux-solaris-or-freebsd}

{{eol}}

Instructies voor het installeren en configureren van Apache Server 2.0.40, 2.0.42 of hoger, Apache Server 2.2 of Apache Server 2.4 op Linux, Sun Solaris of FreeBSD.

De programmabestanden voor Sensor worden verpakt in een installatiebestand dat u van de downloadsite van de Adobe ontvangt. Als u nog geen Sensor-installatiebestand voor uw specifieke webserver hebt, downloadt u het bestand (of vraagt u het op bij uw Adobe-vertegenwoordiger) voordat u de volgende procedures start.

Voor het installeren en configureren van Sensor moet u de volgende stappen op hoog niveau uitvoeren:

De volgende Apache-servers worden ondersteund:

* Apache Server 2.0.40 die onder RedHat Linux 7.x of later, of de SPARC 2.6 van Zon Solaris of later loopt.
* Apache Server 2.0.40, 2.0.42 of hoger, Apache Server 2.2 of Apache Server 2.4 op Linux, Sun Solaris of FreeBSD
* Apache Server 2.0.42 of hoger, uitgevoerd onder RedHat Linux 7.x of hoger, Sun Solaris SPARC 2.6 of hoger, SUSE Linux 9.x of hoger, of FreeBSD 5.3.
* Apache Server 2.0.42 of hoger met 64-bits versies van RedHat Linux ES 4 en ES 5.
* Apache Server 2.2 die onder RedHat Linux 7.x of recenter of Sun Solaris SPARC 2.6 of recenter loopt.
* Apache Server 2.4 die onder RedHat Linux 7.x of recenter, of Sun Solaris x86_64, of FreeBSD loopt

>[!NOTE]
>
>Hoewel de instructies voor het installeren van sensoren op webservers waarop Apache Server 2.0.40, 2.0.42 of hoger (32-bits en 64-bits) of 2.2 wordt uitgevoerd hetzelfde zijn (behalve wanneer dit in de volgende procedures wordt vermeld), verschillen de installatiebestanden voor elke versie. Voordat u de Sensor installeert, moet u controleren of u de juiste installatiebestanden hebt ontvangen voor de Apache Server en de versies van het besturingssysteem die u uitvoert.

## De programmabestanden installeren {#section-2f3e85083b4f4aa989a85997330e86ae}

Procedure voor het uitpakken en installeren van de programmabestanden voor Sensor.

1. Meld u aan als de hoofdgebruiker of als een gebruiker met basisbevoegdheid.
1. Decomprimeer en pak het installatiebestand uit met de volgende opdracht:

   * In Linux:

      ```
      tar -zxf installationFilename
      ```

      ```
      unzip -d installationFilename.tar.gz 
       tar -xf installationFilename.tar
      ```

   * Op Solaris:

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
   <td colname="col1"> mod_visual_sciences.so </td> 
   <td colname="col2"> De module voor het laden van verzamelingen. </td> 
   <td colname="col3"> <i> IBMHttpServer/modules</i> </td> 
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

## Aanmelding inschakelen op de Sametime-server {#section-2e2f1875a5304cdfa2cbcd0680683cfd}

Stappen die u toestaan om aan de Server van Sametime aan te melden.

1. Gebruik de Lotus Domino Administrator-client om verbinding te maken met de Lotus Domino-server waarop Sametime wordt uitgevoerd.
1. Klik in Lotus Domino Administrator op het tabblad Bestanden en dubbelklik vervolgens op Sametime-configuratie - stconfig.nsf om het Sametime-configuratiebestand te openen.
1. Open in het Sametime-configuratiebestand het formulier Community Services en dubbelklik ergens op het formulier om de bewerkingsmodus te activeren.
1. Stel Chatlogingvlag in op &quot;strikt&quot; en stel Servicetype vastleggen in op &quot;0x1000&quot;.
1. Sla het formulier Community Services op en sluit het. Sluit vervolgens het Sametime-configuratiebestand.
1. Start de Sametime-server opnieuw.

## Het configuratiebestand van de sensor bewerken {#section-de0eb4a646394b61abb6cd5a2b706de0}

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

## Voeg de Collector aan de Server van het Web toe {#section-c5b83ae4ebce430aa764f951e849b333}

Voor IBM HTTP-servers is de verzamelaar een dynamisch gezamenlijk object dat u in uw webserverproces laadt.

Als u de verzamelaar aan uw webserver wilt toevoegen, moet u het bestand httpd.conf bewerken zoals hieronder wordt beschreven en de webserver opnieuw starten.

Als Sensor gegevens vastlegt voor meerdere webservers op de servercomputer, moet u de volgende procedure voor elke webserver uitvoeren.

1. Open met een teksteditor het bestand httpd.conf voor de webserver waarvan de gebeurtenissen worden vastgelegd door Sensor.
1. Voeg de volgende twee regels toe aan het einde van het bestand:

   ```
   LoadModule visual_sciences_module modules/mod_visual_sciences.so 
   VisualSciencesConfig /etc/txlogd.conf
   ```

   >[!NOTE]
   >
   >Deze regels zijn hoofdlettergevoelig. Typ deze precies zoals ze hierboven worden weergegeven.

1. Start het webserverproces opnieuw (u hoeft niet de gehele servercomputer opnieuw op te starten, start gewoon het webserverproces opnieuw). De verzamelaar wordt met de webserver geladen en begint gebeurtenisgegevens te verzamelen en naar de schijfwachtrij te schrijven.

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

Met deze opdracht start u de zender als een daemon. De werkende en foutenmeldingen die de zender produceert worden geschreven aan syslog.
