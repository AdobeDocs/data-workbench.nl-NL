---
description: Informatie over de vereiste parameters voor Sensor txlogd.conf.
title: Vereiste parameters
uuid: 187f4199-ec7f-4d5a-93eb-64a62d51ec7b
exl-id: 782e11e9-b11b-4003-9669-f31187208ec3
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '538'
ht-degree: 0%

---

# Vereiste parameters{#required-parameters}

{{eol}}

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
   <td colname="col2"> <p>Een tekenreeks die dit uniek identificeert <span class="wintitle"> Sensor</span>. </p> <p> <span class="wintitle"> Sensor</span> heft SensorID aan elk gebeurtenisverslag toe het naar verzendt <span class="keyword"> gegevenswerkbankserver</span>. Met de SensorID kunnen de gebeurtenisgegevens van deze webserver worden onderscheiden van de gebeurtenisgegevens die worden vastgelegd door andere <span class="wintitle"> Sensoren</span>. </p> <p>Hoewel een SensorID uit om het even welke koord van karakters kan bestaan, door overeenkomst, de naam van de Webserver waarvan gebeurtenissen de <span class="wintitle"> Sensor</span> wordt vastgelegd. Door de servernaam als SensorID te gebruiken, kunt u gemakkelijk de bron van een gebeurtenis bepalen tijdens het analysestadium. Het zorgt ook dat SensorID binnen de implementatie uniek is. </p> <p>Voorbeeld: <span class="filepath"> SensorID web001a</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> ServerAddress </td> 
   <td colname="col2"> <p>Het adres van de <span class="keyword"> gegevenswerkbankserver</span> waarbij <span class="wintitle"> Sensor</span> verzendt gebeurtenisgegevens. </p> <p>Opmerking:  <p>Wanneer het werken in een gegroepeerde milieu, <span class="wintitle"> Sensor</span> moet worden geconfigureerd om toegang te krijgen tot de master <span class="keyword"> gegevenswerkbankserver</span> om synchronisatieproblemen te voorkomen. In Data Workbench kunt u informatie over de verwerking bekijken <span class="keyword"> gegevenswerkbankservers</span> in uw cluster met de menuoptie Verwante servers in de <span class="wintitle"> Serverbeheer</span>. Voor meer informatie over de <span class="wintitle"> Serverbeheer</span>, zie de <i><span class="keyword"> Data Workbench</span><span class="wintitle"> Sensor</span> Hulplijn</i>. </p> <p>Als uw webserver servernamen kan omzetten via DNS, kunt u het adres van de server op naam opgeven. Als dat niet het geval is, moet u het numerieke IP-adres van de server opgeven. </p> <p>Voorbeeld: <span class="filepath"> ServerAddress 10.1.0.7</span> of </p> <p> <span class="filepath"> ServerAddress vserver01.mijnbedrijf.nl</span> </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> SSL </td> 
   <td colname="col2"> <p>Of <span class="wintitle"> Sensor</span> communiceert met <span class="keyword"> gegevenswerkbankserver</span> met HTTP of HTTPS. Ingesteld op "on" voor HTTPS of "off" voor HTTP. </p> <p>Voorbeeld: <span class="filepath"> SSL ingeschakeld</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> ServerPort </td> 
   <td colname="col2"> <p>De poort waarop de <span class="keyword"> gegevenswerkbankserver</span> luistert naar gebeurtenisgegevens. </p> <p>Voorbeeld: <span class="filepath"> ServerPort 443</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> CertName </td> 
   <td colname="col2"> <p>Alleen vereist als de SSL-parameter is ingesteld op "on." </p> <p>De algemene naam van de <span class="keyword"> gegevenswerkbankserver</span> waarbij <span class="wintitle"> Sensor</span> verzendt gebeurtenisgegevens. </p> <p>De waarde die u opgeeft, moet exact overeenkomen met de algemene naam die wordt weergegeven op het tabblad <span class="keyword"> gegevenswerkbankserver</span> certificaat. </p> <p>Voorbeeld: <span class="filepath"> CertName vserver01.mijnbedrijf.com</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> CertPath </td> 
   <td colname="col2"> <p>Alleen vereist als de SSL-parameter is ingesteld op "on." </p> <p>De directory waarin de certificeringsinstantie (<span class="filepath"> trust_ca_cert.pem</span>) bestand bevindt zich </p> <p>Voorbeelden: </p> <p> <span class="filepath"> CertPath /usr/local/visualsensor</span> </p> <p> <span class="filepath"> CertPath C:\VisualSensor</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> QueueFile </td> 
   <td colname="col2"> <p>Niet nodig voor <span class="wintitle"> Sensor</span> installaties op Microsoft Windows 2000- of 2003 Server-computers met IIS-versies (Internet Information Service) 5.x of 6.x. </p> <p>De volledig gekwalificeerde naam van het bestand met de schijfwachtrij. </p> <p>Hoewel u elke naam aan dit bestand kunt toewijzen, wordt het bestand in de wachtrij standaard benoemd <span class="filepath"> VisualSensor.dat</span>. </p> <p>Voor <span class="wintitle"> Sensor</span> In Unix kunt u dit bestand overal plaatsen. In Windows met een Java-webserver moet u dit bestand in dezelfde map plaatsen als de verzender. Voor alle andere webservers moet dit bestand zich in de map /var/queue bevinden. </p> <p>Voorbeeld: <span class="filepath"> QueueFile /var/queue/VisualSensor.dat</span> </p> <p> <p>Opmerking: Zorg ervoor dat het apparaat waaraan u dit bestand toewijst, voldoende vrije ruimte heeft voor een wachtrij met de gewenste grootte. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> QueueSize </td> 
   <td colname="col2"> <p>Een geheel getal dat de grootte van het schijfrijbestand in MB vertegenwoordigt. </p> <p>Voor <span class="wintitle"> Sensor</span> installaties in Microsoft Windows wordt het bestand met de wachtrij zelf gemaakt in dezelfde map als de verzender en krijgt de naam <span class="filepath"> Diskq2000.log</span>. </p> <p>In het volgende voorbeeld wordt de wachtrijgrootte ingesteld op 200 MB: </p> <p>QueueSize 200 </p> <p>In het volgende voorbeeld wordt de wachtrijgrootte ingesteld op 2 GB: </p> <p>QueueSize 2000 </p> </td> 
  </tr> 
 </tbody> 
</table>
