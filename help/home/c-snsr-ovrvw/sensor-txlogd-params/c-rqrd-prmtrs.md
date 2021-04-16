---
description: Informatie over de vereiste parameters voor Sensor txlogd.conf.
title: Vereiste parameters
uuid: 187f4199-ec7f-4d5a-93eb-64a62d51ec7b
exl-id: 782e11e9-b11b-4003-9669-f31187208ec3
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
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
   <td colname="col2"> <p>Een tekenreeks die deze <span class="wintitle"> Sensor</span> uniek identificeert. </p> <p> <span class="wintitle"> </span> Sensorattaches de SensorID aan elke gebeurtenisrecord die het verzendt naar de  <span class="keyword"> gegevenswerkbench-server</span>. Met de SensorID kunnen de gebeurtenisgegevens van deze webserver worden onderscheiden van de gebeurtenisgegevens die worden vastgelegd door andere <span class="wintitle"> Sensors</span>. </p> <p>Hoewel een SensorID uit om het even welke koord van karakters kan bestaan, door overeenkomst, wordt de naam van de Webserver waarvan de gebeurtenissen <span class="wintitle"> Sensor</span> vangt gebruikt. Door de servernaam als SensorID te gebruiken, kunt u gemakkelijk de bron van een gebeurtenis bepalen tijdens het analysestadium. Het zorgt ook dat SensorID binnen de implementatie uniek is. </p> <p>Voorbeeld: <span class="filepath"> SensorID web001a</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> ServerAddress </td> 
   <td colname="col2"> <p>Het adres van de <span class="keyword"> gegevenswerkbankserver</span> waarnaar deze <span class="wintitle"> Sensor</span> gebeurtenisgegevens verzendt. </p> <p>Opmerking:  <p>Als u in een geclusterde omgeving werkt, moet <span class="wintitle"> Sensor</span> worden geconfigureerd om toegang te krijgen tot de master <span class="keyword"> gegevenswerkbankserver</span> om synchronisatieproblemen te voorkomen. In Data Workbench kunt u informatie over de verwerking <span class="keyword"> gegevens werkbench servers</span> in uw cluster bekijken gebruikend het Verwante het menupunt van Servers in <span class="wintitle"> de Manager van Servers </span>. Voor meer informatie over <span class="wintitle"> de Manager van Servers </span>, zie <i><span class="keyword"> Data Workbench</span><span class="wintitle"> Sensor</span> Gids</i>. </p> <p>Als uw webserver servernamen kan omzetten via DNS, kunt u het adres van de server op naam opgeven. Als dat niet het geval is, moet u het numerieke IP-adres van de server opgeven. </p> <p>Voorbeeld: <span class="filepath"> ServerAddress 10.1.0.7</span> of </p> <p> <span class="filepath"> ServerAddress vserver01.mijnbedrijf.nl</span> </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> SSL </td> 
   <td colname="col2"> <p>Geeft aan of <span class="wintitle"> Sensor</span> communiceert met <span class="keyword"> gegevenswerkbench server</span> via HTTP of HTTPS. Ingesteld op "on" voor HTTPS of "off" voor HTTP. </p> <p>Voorbeeld: <span class="filepath"> SSL op</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> ServerPort </td> 
   <td colname="col2"> <p>De poort waarop de <span class="keyword"> gegevenswerkbankserver</span> luistert naar gebeurtenisgegevens. </p> <p>Voorbeeld: <span class="filepath"> ServerPort 443</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> CertName </td> 
   <td colname="col2"> <p>Alleen vereist als de SSL-parameter is ingesteld op "on." </p> <p>De algemene naam van de <span class="keyword"> gegevenswerkbankserver</span> waarnaar deze <span class="wintitle"> Sensor</span> gebeurtenisgegevens verzendt. </p> <p>De waarde die u opgeeft, moet exact overeenkomen met de algemene naam die wordt weergegeven op het <span class="keyword"> gegevenswerkbench-servercertificaat</span>. </p> <p>Voorbeeld: <span class="filepath"> CertName vserver01.mycompany.com</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> CertPath </td> 
   <td colname="col2"> <p>Alleen vereist als de SSL-parameter is ingesteld op "on." </p> <p>De map waarin het bestand van de certificeringsinstantie (<span class="filepath"> trust_ca_cert.pem</span>) zich bevindt </p> <p>Voorbeelden: </p> <p> <span class="filepath"> CertPath /usr/local/visualsensor</span> </p> <p> <span class="filepath"> CertPath C:\VisualSensor</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> QueueFile </td> 
   <td colname="col2"> <p>Niet nodig voor <span class="wintitle"> Sensor</span> installaties op de machines van de Server van Microsoft Windows 2000 of 2003 die versies van de Dienst van de Informatie van Internet (IIS) 5.x of 6.x in werking stellen. </p> <p>De volledig gekwalificeerde naam van het bestand met de schijfwachtrij. </p> <p>Hoewel u om het even welke naam aan dit dossier kunt toewijzen, door overeenkomst, wordt het rijdossier genoemd <span class="filepath"> VisualSensor.dat</span>. </p> <p>Voor <span class="wintitle"> Sensor</span> installaties op Unix, kunt u dit dossier overal plaatsen. In Windows met een Java-webserver moet u dit bestand in dezelfde map plaatsen als de verzender. Voor alle andere webservers moet dit bestand zich in de map /var/queue bevinden. </p> <p>Voorbeeld: <span class="filepath"> QueueFile /var/queue/VisualSensor.dat</span> </p> <p> <p>Opmerking:  Zorg ervoor dat het apparaat waaraan u dit bestand toewijst, voldoende vrije ruimte heeft voor een wachtrij met de gewenste grootte. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> QueueSize </td> 
   <td colname="col2"> <p>Een geheel getal dat de grootte van het schijfrijbestand in MB vertegenwoordigt. </p> <p>Voor <span class="wintitle"> Sensor</span> installaties op Microsoft Windows, wordt het rijdossier zelf gecreeerd in de zelfde folder zoals de zender en genoemd <span class="filepath"> Diskq2000.log</span>. </p> <p>In het volgende voorbeeld wordt de wachtrijgrootte ingesteld op 200 MB: </p> <p>QueueSize 200 </p> <p>In het volgende voorbeeld wordt de wachtrijgrootte ingesteld op 2 GB: </p> <p>QueueSize 2000 </p> </td> 
  </tr> 
 </tbody> 
</table>
