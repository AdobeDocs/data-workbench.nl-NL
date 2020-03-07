---
description: Informatie over de vereiste parameters van de Sensor txlogd.conf.
solution: Insight
title: Vereiste parameters
uuid: 187f4199-ec7f-4d5a-93eb-64a62d51ec7b
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Vereiste parameters{#required-parameters}

Informatie over de vereiste parameters van de Sensor txlogd.conf.

<table id="table_69CFE10A3707403F9793137B128E706A"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> In deze parameter... </th> 
   <th colname="col2" class="entry"> Specificeren... </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> SensorID </td> 
   <td colname="col2"> <p>Een karakterkoord dat uniek deze <span class="wintitle"> Sensor</span>identificeert. </p> <p> <span class="wintitle"> De sensor</span> maakt SensorID aan elke gebeurtenisverslag vast het naar de server <span class="keyword"> van de</span>gegevenswerkbank verzendt. SensorID laat dat de gebeurtenisgegevens van deze Webserver toe om van de gebeurtenisgegevens worden onderscheiden die door andere <span class="wintitle"> Sensoren</span>worden gevangen. </p> <p>Hoewel een SensorID uit om het even welk koord van karakters kan bestaan, door overeenkomst, wordt de naam van de Webserver de waarvan gebeurtenissen de <span class="wintitle"> Sensor</span> vangt gebruikt. Het gebruiken van de servernaam als SensorID maakt het gemakkelijk om de bron van een gebeurtenis tijdens het analysestadium te bepalen. Het zorgt ook ervoor dat SensorID binnen de implementatie uniek is. </p> <p>Voorbeeld: <span class="filepath"> SensorID web001a</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> ServerAddress </td> 
   <td colname="col2"> <p>Het adres van de server <span class="keyword"> van de</span> gegevenswerkbank waaraan deze <span class="wintitle"> Sensor</span> gebeurtenisgegevens verzendt. </p> <p>Opmerking:  <p>Wanneer het werken in een gegroepeerd milieu, zou de <span class="wintitle"> Sensor</span> moeten worden gevormd om tot de hoofdserver <span class="keyword"> van de</span> gegevenswerkbank toegang te hebben om synchronisatiekwesties te vermijden. In de Werkbank van Gegevens kunt u informatie over de servers <span class="keyword"> van de</span> gegevenswerkbank van de verwerking in uw cluster bekijken gebruikend het Verwante het menupunt van Servers in de Manager <span class="wintitle"> van</span>Servers. Voor meer informatie over de Manager <span class="wintitle"> van</span>Servers, zie de Gids van de Sensor <i><span class="keyword"> van de</span><span class="wintitle"> Werkbank</span> van Gegevens</i>. </p> <p>Als uw Webserver servernamen door DNS kan oplossen, kunt u het adres van de server door naam specificeren. Als niet, moet u het numerieke IP van de server adres specificeren. </p> <p>Voorbeeld: <span class="filepath"> Serveradres 10.1.0.7</span> of </p> <p> <span class="filepath"> ServerAddress vserver01.mycompany.com</span> </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> SSL </td> 
   <td colname="col2"> <p>Of de <span class="wintitle"> Sensor</span> met de server <span class="keyword"> van de</span> gegevenswerkbank communiceert gebruikend HTTP of HTTPS. Reeks aan "op"voor HTTPS of "weg"voor HTTP. </p> <p>Voorbeeld: <span class="filepath"> SSL op</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> ServerPort </td> 
   <td colname="col2"> <p>De haven waarop de server <span class="keyword"> van de</span> gegevenswerkbank op gebeurtenisgegevens let. </p> <p>Voorbeeld: <span class="filepath"> ServerPort 443</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> CertName </td> 
   <td colname="col2"> <p>Vereist slechts als de SSL parameter aan "aan wordt geplaatst." </p> <p>De gemeenschappelijke naam van de server <span class="keyword"> van de</span> gegevenswerkbank waaraan deze <span class="wintitle"> Sensor</span> gebeurtenisgegevens verzendt. </p> <p>De waarde u specificeert moet de gemeenschappelijke naam precies aanpassen die op het de vergunningscertificaat van de de <span class="keyword"> gegevenswerkbankserver</span> verschijnt. </p> <p>Voorbeeld: <span class="filepath"> CertName vserver01.mycompany.com</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> CertPath </td> 
   <td colname="col2"> <p>Vereist slechts als de SSL parameter aan "aan wordt geplaatst." </p> <p>De folder waarin het dossier van de certificaatautoriteit (<span class="filepath"> trust_ca_cert.pem</span>) wordt gevestigd </p> <p>Voorbeelden: </p> <p> <span class="filepath"> CertPath /usr/local/visualsensor</span> </p> <p> <span class="filepath"> CertPath C:\VisualSensor</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> QueueFile </td> 
   <td colname="col2"> <p>Niet nodig voor de installaties van de <span class="wintitle"> Sensor</span> op de machines van de Server van Microsoft Windows 2000 of van 2003 die de versies van de Informatie van Internet van de Dienst (IIS) 5.x of 6.x in werking stellen. </p> <p>Volledig - gekwalificeerde naam van het dossier van de schijfrij. </p> <p>Hoewel u om het even welke naam aan dit dossier kunt toewijzen, door overeenkomst, wordt het rijdossier genoemd <span class="filepath"> VisualSensor.dat</span>. </p> <p>Voor de installaties van de <span class="wintitle"> Sensor</span> op Unix, kunt u dit dossier overal plaatsen. Op Vensters die een het Webserver van Java in werking stellen, moet u dit dossier in de zelfde folder plaatsen zoals de zender. Voor alle andere Webservers, zou dit dossier in de /var/rijfolder moeten verblijven. </p> <p>Voorbeeld: <span class="filepath"> QueueFile /var/queue/VisualSensor.dat</span> </p> <p> <p>Opmerking:  Zorg ervoor dat het apparaat waaraan u dit dossier toewijst genoeg vrije ruimte heeft om een rij van de grootte aan te passen u wenst. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> QueueSize </td> 
   <td colname="col2"> <p>Een geheel dat de grootte van het dossier van de schijfrij in MB vertegenwoordigt. </p> <p>Voor de installaties van de <span class="wintitle"> Sensor</span> op Microsoft Windows, wordt het rijdossier zelf gecreeerd in de zelfde folder zoals de zender en genoemd <span class="filepath"> Diskq2000.log</span>. </p> <p>Het volgende voorbeeld plaatst de rijgrootte aan 200 MB: </p> <p>QueueSize 200 </p> <p>Het volgende voorbeeld plaatst de rijgrootte aan 2 GB: </p> <p>QueueSize 2000 </p> </td> 
  </tr> 
 </tbody> 
</table>

