---
description: Gedetailleerde instructies voor het installeren en configureren van Sensor voor JBoss Server 4.0.5 of hoger die wordt uitgevoerd onder Microsoft Windows Server 2000 of hoger.
title: JBoss Server op de Server 2000 van Vensters of later
uuid: b0501749-9479-484b-8876-fe3001825f8d
exl-id: d9001bc4-f3ef-4d26-9190-807194d20ada
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '1190'
ht-degree: 0%

---

# JBoss Server op de Server 2000 van Vensters of later{#jboss-server-on-windows-server-or-later}

{{eol}}

Gedetailleerde instructies voor het installeren en configureren van Sensor voor JBoss Server 4.0.5 of hoger die wordt uitgevoerd onder Microsoft Windows Server 2000 of hoger.

De programmabestanden voor Sensor worden verpakt in een installatiebestand dat u van de downloadsite van de Adobe ontvangt. Als u nog geen Sensor-installatiebestand voor uw specifieke webserver hebt, downloadt u het bestand (of vraagt u het op bij uw Adobe-vertegenwoordiger) voordat u de volgende procedures start.

Tot de ondersteunde J2EE-implementaties behoren:

* JBoss Server 4.0.5 of later die op de Server 2000 van Microsoft Windows of later loopt.

Als u Sensor wilt installeren en configureren, moet u de volgende stappen uitvoeren:

## De programmabestanden installeren {#section-2f3e85083b4f4aa989a85997330e86ae}

Procedure voor het uitpakken en installeren van de programmabestanden voor Sensor.

1. Maak op uw JBoss-server een map waarin u de Sensor-programmabestanden wilt installeren. Onthoud dat de schijfwachtrij zich in deze map bevindt. Zorg er dus voor dat het apparaat dat u kiest, voldoende ruimte heeft om een wachtrij met de gewenste grootte vast te houden.

   ```
   C:\VisualSensor
   ```

1. Pak de inhoud van het installatiebestand uit in de map die u net hebt gemaakt. Tijdens deze stap installeert Sensor de volgende bestanden:

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
>Het installatiepakket bevat een spreadsheetbestand met de naam [!DNL TestExperiment.xls]. Dit spreadsheet is een hulpmiddel dat de architecten gebruiken om een gecontroleerd experiment te vormen. Sensor zelf gebruikt dit bestand niet. U hoeft het bestand dus niet te installeren op de computer waarop de Sensor wordt uitgevoerd (maar u kunt dit desgewenst doen). In plaats daarvan kunt u het bestand kopiëren naar een locatie waar uw architecten het kunnen openen of het bestand gewoon uit het installatiepakket extraheren. Zie de Gids met gecontroleerde experimenten voor meer informatie over gecontroleerde experimenten.

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

1. Selecteer in het menu Start in Windows Accessoires > Opdrachtprompt.
1. Navigeer in het opdrachtpromptvenster naar de map waarin u Sensor hebt geïnstalleerd en voer de volgende opdracht uit:

   ```
   txlog /regserver
   ```

   Dit bevel begint de zender, leidt tot de schijfrij, en registreert Sensor als dienst van Vensters.

1. Klik op Start > Configuratiescherm > Systeembeheer > Services om te bevestigen dat de zender correct wordt uitgevoerd.

   >[!NOTE]
   >
   >Deze bevelopeenvolging zou kunnen variëren afhankelijk van welke versie van Vensters u gebruikt.

   1. In de de dienstlijst, bepaal de plaats van de ingang voor Sensor en bevestig dat zijn status Begonnen is en zijn starttype Automatisch is.
   1. Sluit het configuratiescherm Services.

1. Als u wilt controleren of er bij het opstarten fouten zijn opgetreden in de zender, klikt u op Start > Configuratiescherm > Systeembeheer > Gebeurtenisviewer om de Event Viewer te openen.

   1. Selecteer in het linkerdeelvenster van het venster van de Event Viewer het logboek Toepassingen.
   1. Zoek in het rechterdeelvenster naar gebeurtenissen met &quot;Adobe&quot; in de kolom Bron.
   1. Als er een fout optreedt bij &quot;Adobe&quot;, dubbelklikt u op de fout om het venster Eigenschappen van gebeurtenis weer te geven. Dit venster bevat gedetailleerde informatie over de fout.

1. Wanneer u klaar bent met het controleren van het logboek Toepassingen, sluit u de Event Viewer.
1. Verifieer dat de zender de schijfrij (Diskq2000.log) in de folder heeft gecreeerd waar u de het programmadossiers van de Sensor installeerde en dat het de grootte is die u in de parameter QueueSize in het txlogd.conf- dossier specificeerde.

   Als de wachtrij niet correct is gemaakt:

   1. Onderzoek het txtlogd.conf- dossier en verifieer dat de parameter QueueSize correct wordt geplaatst.
   1. Controleer of het apparaat waarop u Sensor hebt geïnstalleerd voldoende ruimte heeft om een bestand van de grootte op te slaan die in de parameter QueueSize is opgegeven.
   1. Stop de zender met behulp van het configuratiescherm Services in Windows.
   1. Verwijder het bestand in de wachtrij.
   1. Registreer Sensor opnieuw als Windows-service: Selecteer in het menu Start in Windows Accessoires > Opdrachtprompt. Navigeer in het opdrachtpromptvenster naar de map waarin u Sensor hebt geïnstalleerd en voer de volgende opdracht uit:

      ```
      txlog /regserver
      ```

De zender is ontworpen om continu te werken. Als u de computer opnieuw opstart, wordt de zender automatisch opnieuw opgestart. Als u de zender handmatig moet starten en stoppen, kunt u dit doen met het configuratiescherm Services in Windows.

## Voeg de Collector aan de Server van het Web toe {#section-c5b83ae4ebce430aa764f951e849b333}

Voor JBoss servers, werkt de inzamelaar als filter in de servlet container.

Als u de verzamelaar aan uw webserver wilt toevoegen, moet u de opdracht [!DNL web.xml] en start de webtoepassing opnieuw op.

1. Open met een teksteditor de [!DNL web.xml] bestand voor de webserver waarvan de gebeurtenissen worden vastgelegd door Sensor.
1. Voeg het volgende toe `<filter>` en `<filter-mapping>` elementen naar het descriptorbestand. Als u txlogd.conf niet hebt geïnstalleerd in de map /etc, moet u het juiste pad naar dit bestand invoeren in de map `<param-value>` element:

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

1. Start het webserverproces opnieuw (u hoeft niet de gehele servercomputer opnieuw op te starten, start gewoon het webserverproces opnieuw). De verzamelaar wordt met de webserver geladen en begint gebeurtenisgegevens te verzamelen en naar de schijfwachtrij te schrijven.

## Het opstartscript wijzigen {#section-0dae181ef8884f10a57f6cfda8500969}

Alvorens het startmanuscript te wijzigen, zorg ervoor dat de variabele JAVA_HOME in het milieu van Vensters wordt bepaald.

In de [!DNL run.bat] bestand (bijvoorbeeld C:\jboss-4.0.5.GA\bin\run.bat), voeg de volgende regels toe vlak voor het einde van het bestand &quot;echo&quot;-regels die voorafgaan aan de opstartopdracht van de JBoss-server:

```
set JBOSS_CLASSPATH=%JBOSS_CLASSPATH%;C:\jboss-4.0.5.GA\server\default\lib\javax.servlet.jar;C:\VisualSciences\J2EECollector.jar 
set JAVA_OPTS=%JAVA_OPTS% -Djava.library.path=C:\VisualSciences
```

## Aanvullende gegevens vastleggen {#section-9483b663cbd0432daaca50c1089c7fca}

U kunt aanvullende meetgegevens vastleggen uit J2EE-webtoepassingen met behulp van de appendToLog()-functionaliteit.

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
