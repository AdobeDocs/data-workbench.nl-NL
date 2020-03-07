---
description: Gedetailleerde instructies voor het installeren en het vormen van Sensor voor Apache Jakarta Tomcat 4.1 of later lopend onder de Server 2000 van Vensters of later.
title: Tomcat Server op de Server 2000 van Vensters of later
uuid: 58feec67-ffbb-4f25-8f22-3d109d464e9a
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Tomcat Server op de Server 2000 van Vensters of later{#tomcat-server-on-windows-server-or-later}

Gedetailleerde instructies voor het installeren en het vormen van Sensor voor Apache Jakarta Tomcat 4.1 of later lopend onder de Server 2000 van Vensters of later.

De programmadossiers voor Sensor worden verpakt in een installatiedossier dat u van de de downloadplaats van Adobe verkrijgt. Als u niet reeds het de installatiedossier van de Sensor voor uw bepaalde Webserver hebt, download het (of verkrijg het van uw vertegenwoordiger van Adobe) alvorens u met de volgende procedures begint.

De ondersteunde J2EE-implementaties omvatten:

* JBoss Server 4.0.5 of later lopend op de Server 2000 van Microsoft Windows of later.

Om Sensor te installeren en te vormen, moet u de volgende stappen uitvoeren:

## De programmabestanden installeren {#section-2f3e85083b4f4aa989a85997330e86ae}

Procedure om de programmadossiers voor Sensor te halen en te installeren.

1. Voor uw Server van de Tomcat, creeer een folder waarin om de het programmadossiers van de Sensor te installeren. Houd in mening dat uw schijfrij in deze folder verblijft, zodat ben zeker het apparaat u kiest voldoende ruimte heeft om een rij van de grootte te houden u wenst.

   ```
   C:\VisualSensor
   ```

1. Haal de inhoud van het installatiedossier in de folder uit u enkel creeerde. Tijdens deze stap installeert de sensor de volgende bestanden:

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
   <td colname="col1"> visual_sciences.dll </td> 
   <td colname="col2"> De module van de inzamelaarbelasting. </td> 
   <td colname="col3"> In elke directory. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> J2EECollector.jar </td> 
   <td colname="col2"> De de modulebibliotheken van de collectorlading </td> 
   <td colname="col3"> WEB-INF/lib </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>txlogd.exe </p> </td> 
   <td colname="col2"> Het uitzendprogramma. </td> 
   <td colname="col3"> In elke directory </td> 
  </tr> 
  <tr> 
   <td colname="col1"> txlogd.conf </td> 
   <td colname="col2"> Het de configuratiedossier van de Sensor. </td> 
   <td colname="col3"> In elke directory </td> 
  </tr> 
  <tr> 
   <td colname="col1"> trust_ca_cert.pem </td> 
   <td colname="col2"> Het certificaat dat wordt gebruikt om het digitale certificaat te bevestigen dat de Server van het Inzicht tijdens het verbindingsproces voorstelt </td> 
   <td colname="col3"> In elke directory </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Het installatiepakket bevat een spreadsheetdossier genoemd [!DNL TestExperiment.xls]. Deze spreadsheet is een hulpmiddel dat de architecten gebruiken om een gecontroleerd experiment te vormen. De sensor zelf gebruikt dit dossier niet, zodat is het niet noodzakelijk om het dossier op de machine te installeren waar de Sensor loopt (hoewel u kunt verkiezen om dit te doen). U zou, in plaats daarvan, het dossier aan een plaats kunnen willen kopiëren waar uw architecten tot het kunnen toegang hebben of eenvoudig het dossier uit het installatiepakket halen zoals nodig. Voor meer informatie over gecontroleerde experimentatie, zie de Gids van de Experimenten van het Inzicht de Gecontroleerde.

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

1. Van het menu van het Begin in Vensters, uitgezochte Toebehoren > de Herinnering van het Bevel.
1. In het bevel snelle venster, navigeer aan de folder waarin u Sensor installeerde en voer het volgende bevel uit:

   ```
   txlog /regserver
   ```

   Dit bevel begint de zender, leidt tot de schijfrij, en registreert Sensor als dienst van Vensters.

1. Om te bevestigen dat de zender correct loopt, klik Begin > Controlebord > Administratieve Hulpmiddelen > de Diensten.

   >[!NOTE]
   >
   >Deze bevelopeenvolging zou kunnen variëren afhankelijk van welke versie van Vensters u gebruikt.

   1. In de de dienstlijst, bepaal de plaats van de ingang voor Sensor en bevestig dat zijn status Begonnen is en zijn starttype Automatisch is.
   1. Sluit het de controlepaneel van de Diensten.

1. Om te controleren of de zender tijdens het opstarten fouten ondervond, klik Begin > Controlebord > Administratieve Hulpmiddelen > de Kijker van de Gebeurtenis om de Kijker van de Gebeurtenis te openen.

   1. In de linkerruit van het venster van de Kijker van de Gebeurtenis, selecteer het logboek van Toepassingen.
   1. In de juiste ruit, zoek gebeurtenissen met &quot;Adobe&quot;in de Bronkolom.
   1. Als u een fout van &quot;Adobe vindt,&quot;klik de fout tweemaal om het venster van de Eigenschappen van de Gebeurtenis te tonen. Dit venster verstrekt gedetailleerde informatie over de fout.

1. Wanneer u klaar bent met het onderzoeken van het logboek van Toepassingen, sluit de Kijker van de Gebeurtenis.
1. Verifieer dat de zender de schijfrij (Diskq2000.log) in de folder heeft gecreeerd waar u de het programmadossiers van de Sensor installeerde en dat het de grootte is die u in de parameter QueueSize in het txlogd.conf- dossier specificeerde.

   Als de rij niet correct is gecreeerd:

   1. Onderzoek het txtlogd.conf- dossier en verifieer dat de parameter QueueSize correct wordt geplaatst.
   1. Controle dat het apparaat waarop u Sensor installeerde voldoende ruimte beschikbaar heeft om een dossier van de grootte te houden die in de parameter QueueSize wordt gespecificeerd.
   1. Gebruikend het de controlepaneel van de Diensten in Vensters, houd de zender tegen.
   1. Schrap het rijdossier.
   1. Sensor opnieuw registreren als Windows-service: van het menu van het Begin in Vensters, uitgezochte Toebehoren > de Herinnering van het Bevel. In het bevel snelle venster, navigeer aan de folder waarin u Sensor installeerde en voer het volgende bevel uit:

      ```
      txlog /regserver
      ```

De zender is ontworpen om continu te werken. Als u de machine opnieuw start, wordt de zender automatisch opnieuw opgestart. Als u de zender moet beginnen en tegenhouden manueel, kunt u dit doen gebruikend het de controlepaneel van de Diensten in Vensters.

## Voeg de Collector aan de Server van het Web toe {#section-c5b83ae4ebce430aa764f951e849b333}

Voor servers JBoss, werkt de inzamelaar als filter in de servletcontainer.

Om de inzamelaar aan uw Webserver toe te voegen, moet u het [!DNL web.xml] dossier uitgeven zoals hieronder beschreven en uw Webtoepassing opnieuw beginnen.

1. Gebruikend een tekstredacteur, open het [!DNL web.xml] dossier voor de Webserver de waarvan gebeurtenissenSensor vangt.
1. Voeg de volgende `<filter>` en `<filter-mapping>` elementen aan het beschrijvingsdossier toe. Als u txlogd.conf in de /etc folder niet installeerde, moet u de correcte weg aan dit dossier in het `<param-value>` element ingaan:

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

1. Start het webserverproces opnieuw op (u hoeft de volledige servercomputer niet opnieuw op te starten, start het webserverproces gewoon opnieuw op). De inzamelaar wordt geladen met de Webserver en begint inzamelend gebeurtenisgegevens en schrijvend het aan de schijfrij.

## Het bibliotheekpad van Java wijzigen {#section-0dae181ef8884f10a57f6cfda8500969}

Instructies voor het toevoegen van visual_sciences.dll aan de de bibliotheekweg van Tomcat.

1. Voor uw server van Vensters, navigeer aan de installatiefolder van Tomcat. (Tomcat > bin)
1. Onder bakomslag, looppas Tomcat9w.exe (gemeenschappelijke de dienstmanager van daemon).

   In het lusje van Java, onder de opties van Java, voeg een nieuwe lijn toe:

   ```
   -Djava.library.path=C:\Sensor directory
   ```

   Waar de [!DNL C:\Sensor] folder de folder is die het [!DNL visual_sciences.dll] dossier bevat.

## Bijkomende gegevens vastleggen {#section-9483b663cbd0432daaca50c1089c7fca}

U kunt extra meetgegevens van op J2EE gebaseerde webtoepassingen vastleggen met de functie appendToLog().

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

