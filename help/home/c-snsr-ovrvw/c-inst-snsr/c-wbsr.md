---
description: Gedetailleerde instructies voor het installeren van en het vormen van Sensor voor WebSphere 5.x die op AIX 5.1 of later lopen.
solution: Insight
title: WebSphere op AIX
uuid: a5a3fd79-a7f0-4861-adca-8da3a185d0df
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# WebSphere op AIX{#websphere-on-aix}

Gedetailleerde instructies voor het installeren van en het vormen van Sensor voor WebSphere 5.x die op AIX 5.1 of later lopen.

De programmadossiers voor [!DNL Sensor] worden verpakt in een installatiedossier dat u van de de downloadplaats van Adobe verkrijgt. Als u niet reeds het [!DNL Sensor] installatiedossier voor uw bepaalde Webserver hebt, download het (of verkrijg het van uw vertegenwoordiger van Adobe) alvorens u met de volgende procedures begint.

>[!NOTE]
>
>De [!DNL Sensor] voor servers WebSphere steunen gecontroleerde experimenteren niet. Voor informatie over gecontroleerde experimentatie, zie de Gids van de Experimenten van de Werkbank van *Gegevens Gecontroleerde.*

## De programmabestanden installeren {#section-86f69127278c41bc90b97b68bb40bc6e}

Procedure voor het ophalen en installeren van de programmabestanden voor Sensorto op het serversysteem.

1. Opening van een sessie als wortelgebruiker of als gebruiker met wortelgezag.
1. Decompress en unpack het installatiedossier gebruikend het volgende bevel:

   ```
   gunzip installationFilename.tar.gz 
   tar -xf installationFilename.tar
   ```

1. Kopieer de onverpakte programmadossiers aan de folders die in de volgende lijst worden geïdentificeerd:

<table id="table_0E3B403071EF44AFBF0DD673EFEBBFE5"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Bestand </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
   <th colname="col3" class="entry"> Doelmap </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> libvisual_sciences.so </td> 
   <td colname="col2"> De module van de inzamelingenlading </td> 
   <td colname="col3"> /usr/local/visual_sciences </td> 
  </tr> 
  <tr> 
   <td colname="col1"> J2EECollector.jar </td> 
   <td colname="col2"> De de modulebibliotheken van de collectorlading </td> 
   <td colname="col3"> WebSphere/lib-directory </td> 
  </tr> 
  <tr> 
   <td colname="col1"> txlogge </td> 
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

Door gebrek, hebben de programmadossiers in het teerdossier de volgende toestemmingen. Afhankelijk van hoe uw systeem wordt gevormd, zouden deze montages (unmaskated) kunnen worden veranderd wanneer u de dossiers haalt.

Om de toestemmingen aan de geadviseerde standaardmontages terug te stellen, gebruik hieronder de bevelen van de wortelmethode.

>[!NOTE]
>
>Controle dat de folders waarin u de dossiers hebt geïnstalleerd minstens dit niveau van toegang toelaten.

| Bestand | Standaardrechten | chmod, opdracht |
|---|---|---|
| libvisual_sciences.so | rwx —x —x | chmod 711 |
| J2EECollector.jar | rw- rw- r— | chmod 664 |
| txlogge | rwx —x —x | chmod 711 |
| txlogd.conf | rw- rw- r— | chmod 664 |
| trust_ca_cert.pem | rw- rw- r— | chmod 664 |

Als u toestemmingen buiten de geadviseerde gebreken wilt gebruiken, herzie de informatie in de Toestemmingen van het Dossier van UNIX van de Sensor, om zeker te zijn u begrijpt hoe deze dossiers worden gebruikt.

## Geef het dossier van de Configuratie van de Sensor uit {#section-283c8a92fa8841c1b6034e5f834ef4e7}

Het txlogd.conf- dossier bevat de configuratieparameters voor Sensor.

U moet het dossier uitgeven om, onder andere, de grootte van de schijfrij, het adres van de Server van het Inzicht, en identiteitskaart te specificeren die aan de gegevens zal worden vastgemaakt die door deze sensor worden geproduceerd.

Het configuratiedossier bevat vereiste parameters en facultatieve parameters.

* De vereiste parameters zijn montages die u moet specificeren wanneer u Sensor installeert. Zonder deze montages, loopt de Sensor niet met succes.
* De facultatieve parameters zijn montages die aan vooraf bepaalde waarden (die u kunt wijzigen) in gebreke blijven of facultatieve eigenschappen toelaten.

**Om het configuratiedossier uit te geven**

1. Open het /etc/txlogd.conf dossier in een tekstredacteur en plaats de vereiste parameters evenals om het even welke gewenste facultatieve parameters.
1. Sparen en sluit het dossier.

## Start de zender en maak de schijfwachtrij {#section-63285a2328604f20a2cb31b3d5cb80e6}

Procedure om de schijfrij tot stand te brengen, nadat u het txlogd.conf- dossier vormt.

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

## Voeg de Collector aan de Toepassing van het Web toe {#section-d17297b1193f4e3cb150fb41f754ef12}

Voor servers WebSphere, werkt de inzamelaar als filter in de servletcontainer.

Om de collector aan de Webtoepassing toe te voegen, voeg de filter aan de de plaatsingsbeschrijver van Web.xml van de Webtoepassing toe en begin de Webtoepassing opnieuw.

1. Gebruikend een tekstredacteur, open het web.xml- dossier voor de Webserver de waarvan gebeurtenissenSensor vangt.
1. Voeg de volgende `<filter>` en `<filter-mapping>` elementen aan het beschrijvingsdossier toe. Als u txlogd.conf in de /etc folder niet installeerde, moet u de correcte weg aan dit dossier in het `<param-value>` element ingaan.

   ```
   <filter>
     <filter-name>VSCollectorFilter</filter-name> 
     <description></description> 
     <filter-class> 
         com.visualsciences.collector.VSCollectorFilter 
       </filter-class> 
     <init-param> 
       <param-name>configPath</param-name> 
       <param-value>C:/VisualSensor/txlogd.conf</param-value> 
     <description></description> 
     </init-param> 
   </filter> 
   
   <filter-mapping>
     <filter-name>VSCollectorFilter</filter-name> 
     <url-pattern>/*</url-pattern> 
   </filter-mapping>
   ```

   >[!NOTE]
   >
   >Deze lijnen zijn hoofdlettergevoelig. Typ hen precies zoals zij hierboven verschijnen.

1. Start de webtoepassing opnieuw. De inzamelaar wordt geladen met de toepassing en zal beginnen inzamelend gebeurtenisgegevens en schrijvend het aan de schijfrij.

## Verklaar de Plaats van de Collector en de Gedeelde Dossiers van Objecten {#section-e641f08999d34a648aaee2111b69ca25}

Procedure om het Websfeer startmanuscript uit te geven om de plaats van de dossiers te verklaren J2EECollector.jar en libvisual_sciences.so.

1. Open het setupCmdLine.sh- dossier in de folder Websphere /bin.
1. Na de lijn die de variabele $WAS_CLASSPATH bepaalt, voeg de volgende lijn toe:

   ```
   WAS_CLASSPATH="$WAS_CLASSPATH":"$WAS_HOME"/lib/J2EECollector.jar
   ```

1. Na het gevalblok dat de variabele $WAS_LIBPATH bepaalt, voeg de volgende lijn toe:

   ```
   WAS_LIBPATH="$WAS_LIBPATH":/usr/local/visual_sciences
   ```

1. Sla het [!DNL setupCmdLine.sh] bestand op.

## Test de sensor {#section-07f2da5c4caa46bf9dd1cb4ae4b61af5}

Procedure om de zender te beginnen en te verifiëren dat het met succes met de Server van het Inzicht kan verbinden en gebeurtenisgegevens overbrengen aan het.

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

## Voeg de Transmitter aan Uw Manuscript van de Opstarten van het Systeem toe {#section-23bb905100d04f018af93873dd4d5f68}

Informatie om te verzekeren dat de zender automatisch laadt wanneer de machine van de Webserver opnieuw is begonnen.

Voeg het volgende bevel (dat de zender) aan uw systeem startmanuscript lanceert toe.

```
/usr/local/bin/txlogd -f /etc/txlogd.conf
```

Dit bevel begint de zender als daemon. De werkende en foutenmeldingen die de zender produceert worden geschreven aan syslog.

## Bijkomende gegevens vastleggen {#section-d5ccf8ee50914a87938e0c17480757e6}

De sensoren voor alle platforms kunnen om het even welke gegevens verzamelen beschikbaar in de HTTP- verzoek en reactiekopballen.

De sensoren voor het J2EE-platform bieden een mechanisme voor het verzamelen van gegevens die niet beschikbaar zijn op andere platforms. De verzamelaar voor het J2EE-platform (J2EE-verzamelaar) bevindt zich op de toepassingslaag, waarmee het in staat is gevoelige gegevens te verzamelen die alleen beschikbaar zijn voor de toepassing en die niet door paginagabags of in de headers worden weergegeven.

>[!NOTE]
>
>Terwijl de paginarabels en de kopbalwijziging de gegevens kunnen verbergen, is het nog beschikbaar aan hen die de broncode van een pagina onderzoeken of de kopballen bekijken gebruikend browser stop - in hulpmiddelen.

Bijvoorbeeld, kan de J2EE inzamelaar worden gebruikt om kosten per klik (CPC) gegevens voor verbindingen te vangen die op een pagina worden getoond, gevoelige partnerinformatie over een pagina, en vele andere gegevenspunten. Het milieu J2EE maakt het voor u gemakkelijk om uw WEBAPP te wijzigen om deze douanegegevens te vangen gebruikend onze collectorklasse.

Wanneer een sensor voor het J2EE Platform een verzoek ontvangt, haalt het een collectorklasse aan die de functie appendToLog invoert. De functie appendToLog voegt aan het aanvankelijke verzoek de parameters van het vraagkoord toe die in de functie appendToLog worden gespecificeerd. Dit resulteert in URI van het aanvankelijke verzoek dat extra naam-waarde van het vraagkoord bevat paren die aan de namen en de waarden van de gegevens beantwoorden die worden gevangen. Bijvoorbeeld, zou CPC=20 aan het aanvankelijke verzoek worden toegevoegd wanneer de waarde van een bepaalde advertentie of een klik-door verbinding 20 cent is. De Server van het inzicht verwerkt deze waarden in de dataset voor analyse. Één extra voordeel aan deze inzamelingsmethodologie is dat het de inzameling van extra gegevens toestaat zonder extra logboekingangen tot stand te brengen, zoals zou kunnen worden gecreeerd gebruikend pagina het etiketteren methodologieën.

Voor meer informatie over verwerking, zie de Gids *van de Configuratie van de* Dataset.

1. Voeg de volgende code aan de bovenkant van de .jsp pagina toe waarvan u gegevens wilt vangen:

   ```
   <%@ page import="com.visualsciences.collector.VSCollector" %>
   ```

1. Gebruik de methode appendToLog() van het verzamelaarobject om de gewenste naam-waarde paren toe te voegen aan de query string van de gevraagde .jsp pagina. Het volgende voorbeeld voegt &quot;A=1&quot;en &quot;B=2&quot;aan het gevraagde .jsp de vraagkoord van de pagina voor de /index.jsp pagina toe:

   ```
   <html> 
   <body> 
     <h1>Hello World</h1> 
     <% 
       VSCollector collector = new VSCollector(request, response); 
       collector.appendToLog("A", "1"); 
       collector.appendToLog("B", "2"); 
     %> 
   </body> 
   </html>
   ```

   Het resulterende verzoek URI is /index.jsp?A=1&amp;B=2.

1. Herhaal deze procedure voor elke .jsp pagina waarvan u extra gegevens wilt vangen.

