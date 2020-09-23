---
description: Informatie over de vereiste parameters voor Sensor txlogd.conf.
solution: Analytics
title: Vereiste parameters
uuid: 187f4199-ec7f-4d5a-93eb-64a62d51ec7b
translation-type: tm+mt
source-git-commit: 34cdcfc83ae6bb620706db37228e200cff43ab2c
workflow-type: tm+mt
source-wordcount: '538'
ht-degree: 0%

---


# Vereiste parameters{#required-parameters}

Informatie over de vereiste parameters voor Sensor txlogd.conf.

<table id="table_69CFE10A3707403F9793137B128E706A"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> In deze parameter... </th> 
   <th colname="col2" class="entry"> Opgeven... </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> SensorID </td> 
   <td colname="col2"> <p>Een tekenreeks die deze <span class="wintitle"> sensor</span>op unieke wijze identificeert. </p> <p> <span class="wintitle"> Sensor</span> koppelt de SensorID aan elke gebeurtenisrecord die het naar de <span class="keyword"> gegevenswerkbankserver</span>verzendt. Met de SensorID kunnen de gebeurtenisgegevens van deze webserver worden onderscheiden van de gebeurtenisgegevens die door andere <span class="wintitle"> sensoren</span>zijn vastgelegd. </p> <p>Hoewel een SensorID uit om het even welke koord van karakters kan bestaan, door overeenkomst, wordt de naam van de Webserver waarvan de gebeurtenissen <span class="wintitle"> Sensor</span> vangt gebruikt. Door de servernaam als SensorID te gebruiken, kunt u gemakkelijk de bron van een gebeurtenis bepalen tijdens het analysestadium. Het zorgt ook dat SensorID binnen de implementatie uniek is. </p> <p>Voorbeeld: <span class="filepath"> SensorID web001a</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> ServerAddress </td> 
   <td colname="col2"> <p>Het adres van de <span class="keyword"> gegevenswerkbankserver</span> waarnaar deze <span class="wintitle"> Sensor</span> gebeurtenisgegevens verzendt. </p> <p>Opmerking:  <p>Wanneer het werken in een gegroepeerd milieu, zou de <span class="wintitle"> Sensor</span> moeten worden gevormd om tot de master server <span class="keyword"> van de</span> gegevenswerkbank toegang te hebben om synchronisatiekwesties te vermijden. In Data Workbench kunt u informatie over de werkbankservers <span class="keyword"> van verwerkingsgegevens in uw cluster bekijken gebruikend het Verwante het menupunt van Servers in de Manager</span> van <span class="wintitle"></span>Servers. Raadpleeg de <span class="wintitle"> Data Workbench</span>Sensor <i><span class="keyword"> Guide</span><span class="wintitle"> voor meer informatie over de Servers Manager</span></i>. </p> <p>Als uw webserver servernamen kan omzetten via DNS, kunt u het adres van de server op naam opgeven. Als dat niet het geval is, moet u het numerieke IP-adres van de server opgeven. </p> <p>Voorbeeld: <span class="filepath"> ServerAddress 10.1.0.7</span> of </p> <p> <span class="filepath"> ServerAddress vserver01.mijnbedrijf.nl</span> </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> SSL </td> 
   <td colname="col2"> <p>Of <span class="wintitle"> Sensor</span> communiceert met <span class="keyword"> gegevenswerkbankserver</span> via HTTP of HTTPS. Ingesteld op "on" voor HTTPS of "off" voor HTTP. </p> <p>Voorbeeld: <span class="filepath"> SSL ingeschakeld</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> ServerPort </td> 
   <td colname="col2"> <p>De poort waarop de <span class="keyword"> gegevenswerkbankserver</span> luistert naar gebeurtenisgegevens. </p> <p>Voorbeeld: <span class="filepath"> ServerPort 443</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> CertName </td> 
   <td colname="col2"> <p>Alleen vereist als de SSL-parameter is ingesteld op "on." </p> <p>De algemene naam van de <span class="keyword"> gegevenswerkbankserver</span> waarnaar deze <span class="wintitle"> sensor</span> gebeurtenisgegevens verzendt. </p> <p>De waarde die u opgeeft, moet exact overeenkomen met de algemene naam die wordt weergegeven in het <span class="keyword"> gegevenswerkbankcertificaat voor serverlicenties</span> . </p> <p>Voorbeeld: <span class="filepath"> CertName vserver01.mijnbedrijf.com</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> CertPath </td> 
   <td colname="col2"> <p>Alleen vereist als de SSL-parameter is ingesteld op "on." </p> <p>De map waarin het bestand Trust_ca_cert.pem<span class="filepath"></span>(Certificate Authority) zich bevindt </p> <p>Voorbeelden: </p> <p> <span class="filepath"> CertPath /usr/local/visualsensor</span> </p> <p> <span class="filepath"> CertPath C:\VisualSensor</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> QueueFile </td> 
   <td colname="col2"> <p>Niet nodig voor <span class="wintitle"> Sensor</span> -installaties op Microsoft Windows 2000- of 2003 Server-computers met IIS-versies 5.x of 6.x. </p> <p>De volledig gekwalificeerde naam van het bestand met de schijfwachtrij. </p> <p>Hoewel u om het even welke naam aan dit dossier kunt toewijzen, door overeenkomst, wordt het rijdossier genoemd <span class="filepath"> VisualSensor.dat</span>. </p> <p>Voor <span class="wintitle"> Sensor</span> -installaties op Unix kunt u dit bestand overal plaatsen. In Windows met een Java-webserver moet u dit bestand in dezelfde map plaatsen als de verzender. Voor alle andere webservers moet dit bestand zich in de map /var/queue bevinden. </p> <p>Voorbeeld: <span class="filepath"> QueueFile /var/queue/VisualSensor.dat</span> </p> <p> <p>Opmerking:  Zorg ervoor dat het apparaat waaraan u dit bestand toewijst, voldoende vrije ruimte heeft voor een wachtrij met de gewenste grootte. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> QueueSize </td> 
   <td colname="col2"> <p>Een geheel getal dat de grootte van het schijfrijbestand in MB vertegenwoordigt. </p> <p>Voor de installaties van de <span class="wintitle"> Sensor</span> op Microsoft Windows, wordt het rijdossier zelf gecreeerd in de zelfde folder zoals de zender en genoemd <span class="filepath"> Diskq2000.log</span>. </p> <p>In het volgende voorbeeld wordt de wachtrijgrootte ingesteld op 200 MB: </p> <p>QueueSize 200 </p> <p>In het volgende voorbeeld wordt de wachtrijgrootte ingesteld op 2 GB: </p> <p>QueueSize 2000 </p> </td> 
  </tr> 
 </tbody> 
</table>

