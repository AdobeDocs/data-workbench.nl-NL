---
description: Gedetailleerde instructies voor het installeren en configureren van Sensor voor WebSphere 5.x die op AIX 5.1 of hoger wordt uitgevoerd.
title: WebSphere op AIX
uuid: a5a3fd79-a7f0-4861-adca-8da3a185d0df
exl-id: e560d265-dc84-4ff2-ac86-7a2ac5261451
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '1645'
ht-degree: 0%

---

# WebSphere op AIX{#websphere-on-aix}

Gedetailleerde instructies voor het installeren en configureren van Sensor voor WebSphere 5.x die op AIX 5.1 of hoger wordt uitgevoerd.

De programmabestanden voor [!DNL Sensor] worden verpakt in een installatiebestand dat u ontvangt van de downloadsite van Adobe. Als u nog niet over het [!DNL Sensor]-installatiebestand voor uw specifieke webserver beschikt, downloadt u het bestand (of vraagt u het op bij uw Adobe-vertegenwoordiger) voordat u de volgende procedures start.

>[!NOTE]
>
>De [!DNL Sensor] for WebSphere-servers bieden geen ondersteuning voor gecontroleerde experimenten. Zie de *Gids met gecontroleerde experimenten voor Data Workbench voor informatie over gecontroleerde experimenten.*

## Program Files {#section-86f69127278c41bc90b97b68bb40bc6e} installeren

Procedure voor het uitpakken en installeren van de programmabestanden voor Sensorto op de servercomputer.

1. Meld u aan als de hoofdgebruiker of als een gebruiker met basisbevoegdheid.
1. Decomprimeer en pak het installatiebestand uit met de volgende opdracht:

   ```
   gunzip installationFilename.tar.gz 
   tar -xf installationFilename.tar
   ```

1. Kopieer de onverpakte programmabestanden naar de mappen in de volgende tabel:

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
   <td colname="col2"> De module voor het laden van verzamelingen </td> 
   <td colname="col3"> /usr/local/visual_sciences </td> 
  </tr> 
  <tr> 
   <td colname="col1"> J2EECollector.jar </td> 
   <td colname="col2"> De bibliotheken van de module voor het laden van verzamelingen </td> 
   <td colname="col3"> WebSphere /lib directory </td> 
  </tr> 
  <tr> 
   <td colname="col1"> txlogd </td> 
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

Standaard hebben de programmabestanden in het teerbestand de volgende machtigingen. Afhankelijk van hoe uw systeem wordt gevormd, zouden deze montages (unmasked) kunnen worden veranderd wanneer u de dossiers haalt.

Als u de machtigingen wilt terugzetten op de aanbevolen standaardinstellingen, gebruikt u de onderstaande opdrachten voor onderliggende items.

>[!NOTE]
>
>Controleer of de mappen waarin u de bestanden hebt geïnstalleerd, ten minste dit toegangsniveau toestaan.

| Bestand | Standaardmachtigingen | chmod, opdracht |
|---|---|---|
| libvisual_sciences.so | rwx —x —x | chmod 711 |
| J2EECollector.jar | rw- rw- r— | chmod 664 |
| txlogd | rwx —x —x | chmod 711 |
| txlogd.conf | rw- rw- r— | chmod 664 |
| trust_ca_cert.pem | rw- rw- r— | chmod 664 |

Als u toestemmingen buiten de geadviseerde gebreken wilt gebruiken, herzie de informatie in de Toestemmingen van het Dossier van UNIX van de Sensor, om zeker te zijn u begrijpt hoe deze dossiers worden gebruikt.

## Het Sensor Configuration-bestand {#section-283c8a92fa8841c1b6034e5f834ef4e7} bewerken

Het bestand txlogd.conf bevat de configuratieparameters voor Sensor.

U moet het dossier uitgeven om, onder andere, de grootte van de schijfrij, het adres van de Server van het Inzicht, en identiteitskaart te specificeren die aan de gegevens zal worden vastgemaakt die door deze sensor worden geproduceerd.

Het configuratiebestand bevat vereiste parameters en optionele parameters.

* Vereiste parameters zijn instellingen die u moet opgeven wanneer u Sensor installeert. Zonder deze instellingen wordt Sensor niet uitgevoerd.
* Optionele parameters zijn instellingen die standaard op vooraf gedefinieerde waarden (die u kunt wijzigen) of optionele functies inschakelen.

**Het configuratiebestand bewerken**

1. Open het bestand /etc/txlogd.conf in een teksteditor en stel de vereiste parameters en eventueel gewenste optionele parameters in.
1. Sla het bestand op en sluit het.

## De zender starten en de schijfwachtrij maken {#section-63285a2328604f20a2cb31b3d5cb80e6}

Procedure om de schijfrij tot stand te brengen, nadat u het txlogd.conf- dossier vormt.

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

## Voeg de Collector aan de Toepassing van het Web {#section-d17297b1193f4e3cb150fb41f754ef12} toe

Voor servers WebSphere, werkt de inzamelaar als filter in de servlet container.

Als u de verzamelaar aan de webtoepassing wilt toevoegen, voegt u het filter toe aan de web.xml-implementatiebeschrijving van de webtoepassing en start u de webtoepassing opnieuw.

1. Open met behulp van een teksteditor het bestand web.xml voor de webserver waarvan de gebeurtenissen worden vastgelegd door Sensor.
1. Voeg de volgende `<filter>` en `<filter-mapping>` elementen aan het beschrijvingsdossier toe. Als u txlogd.conf niet in de /etc folder installeerde, moet u de correcte weg aan dit dossier in het `<param-value>` element ingaan.

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
   >Deze regels zijn hoofdlettergevoelig. Typ deze precies zoals ze hierboven worden weergegeven.

1. Start de webtoepassing opnieuw. De verzamelaar wordt met de toepassing geladen en begint gebeurtenisgegevens te verzamelen en naar de schijfwachtrij te schrijven.

## Declareer de Plaats van de Dossiers van de Collector en van het Gedeelde Voorwerp {#section-e641f08999d34a648aaee2111b69ca25}

Procedure voor het bewerken van het opstartscript van Websphere om de locatie van de bestanden J2EECollector.jar en libvisual_sciences.so te declareren.

1. Open het bestand setupCmdLine.sh in de map Websphere /bin.
1. Na de lijn die de variabele $WAS_CLASSPATH bepaalt, voeg de volgende lijn toe:

   ```
   WAS_CLASSPATH="$WAS_CLASSPATH":"$WAS_HOME"/lib/J2EECollector.jar
   ```

1. Na het gevalblok dat de variabele $WAS_LIBPATH bepaalt, voeg de volgende lijn toe:

   ```
   WAS_LIBPATH="$WAS_LIBPATH":/usr/local/visual_sciences
   ```

1. Sla het [!DNL setupCmdLine.sh]-bestand op.

## De sensor {#section-07f2da5c4caa46bf9dd1cb4ae4b61af5} testen

Procedure om de zender te beginnen en te verifiëren dat het met succes met de Server van het Inzicht kan verbinden en gebeurtenisgegevens naar het over te brengen.

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

## De zender toevoegen aan het opstartscript van het systeem {#section-23bb905100d04f018af93873dd4d5f68}

Informatie om ervoor te zorgen dat de zender automatisch wordt geladen wanneer de webservercomputer opnieuw wordt opgestart.

Voeg het volgende bevel (dat de zender) aan uw systeem startscript toe.

```
/usr/local/bin/txlogd -f /etc/txlogd.conf
```

Met deze opdracht start u de zender als een daemon. De werkende en foutenmeldingen die de zender produceert worden geschreven aan syslog.

## Aanvullende gegevens {#section-d5ccf8ee50914a87938e0c17480757e6} vastleggen

De sensoren voor alle platforms kunnen om het even welke gegevens verzamelen beschikbaar in de HTTP- verzoek en antwoordkopballen.

De sensoren voor het J2EE-Platform bieden een mechanisme voor het verzamelen van gegevens die niet beschikbaar zijn op andere platforms. De verzamelaar voor het J2EE-platform (J2EE-collector) bevindt zich op de toepassingslaag, zodat gevoelige gegevens kunnen worden verzameld die alleen beschikbaar zijn voor de toepassing en die niet mogen worden weergegeven via paginagarabeling of in de kopteksten.

>[!NOTE]
>
>Hoewel de gegevens kunnen worden verborgen door paginatags en headerwijzigingen, is deze nog steeds beschikbaar voor diegenen die de broncode van een pagina controleren of de koppen met plug-ins voor de browser bekijken.

Bijvoorbeeld, kan de inzamelaar J2EE worden gebruikt om kosten per klikgegevens (CPC) voor verbindingen te vangen die op een pagina worden getoond, gevoelige partnerinformatie op een pagina, en vele andere gegevenspunten. De J2EE-omgeving maakt het voor u gemakkelijk om uw WEBAPP te wijzigen om deze aangepaste gegevens vast te leggen met onze verzamelaarsklasse.

Wanneer een sensor voor het Platform J2EE een verzoek ontvangt, roept het een inzamelaarklasse aan die de appendToLog functie invoert. De functie appendToLog voegt aan de eerste aanvraag de parameters van de queryreeks toe die in de functie appendToLog zijn opgegeven. Dit resulteert in URI van het aanvankelijke verzoek die extra naam-waardeparen van het vraagkoord bevatten die aan de namen en de waarden van de gegevens beantwoorden die worden gevangen. Bijvoorbeeld, zou CPC=20 aan het aanvankelijke verzoek worden toegevoegd wanneer de waarde van een bepaalde advertentie plaatsing of klik-door verbinding 20 cent is. De Server van het inzicht verwerkt deze waarden in de dataset voor analyse. Een extra voordeel van deze verzamelingsmethode is dat extra gegevens kunnen worden verzameld zonder dat extra logbestandvermeldingen worden gemaakt, zoals mogelijk wordt gemaakt met methoden voor het coderen van pagina&#39;s.

Voor meer informatie over verwerking, zie *de Gids van de Configuratie van de Dataset*.

1. Voeg de volgende code aan de bovenkant van de .jsp pagina toe waarvan u gegevens wilt vangen:

   ```
   <%@ page import="com.visualsciences.collector.VSCollector" %>
   ```

1. Gebruik de methode appendToLog() van het verzamelaarobject om de gewenste naam-waardeparen toe te voegen aan de queryreeks van de opgevraagde .jsp-pagina. In het volgende voorbeeld worden &quot;A=1&quot; en &quot;B=2&quot; toegevoegd aan de queryreeks van de opgevraagde .jsp-pagina voor de pagina /index.jsp:

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

   De resulterende aanvraag-URI is /index.jsp?A=1&amp;B=2.

1. Herhaal deze procedure voor elke .jsp pagina waarvan u extra gegevens wilt vangen.
