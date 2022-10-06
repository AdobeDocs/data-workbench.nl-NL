---
description: Instructies voor het installeren en configureren van Sensor voor Apache Server 1.3, Apache Server 2.0.42 of hoger, of Apache Server 2.2 die wordt uitgevoerd onder Microsoft Windows Server 2000 of hoger.
title: Apache Server 1.3, 2, 2.2 of 2.4 op Windows Server 2000 of hoger
uuid: e159ed83-6004-4f65-a3b7-502cac1d0862
exl-id: d1bd0fc1-da5b-4183-8270-73c46195f724
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '971'
ht-degree: 0%

---

# Apache Server 1.3, 2, 2.2 of 2.4 op Windows Server 2000 of hoger{#apache-server-or-on-windows-server-or-later}

{{eol}}

Instructies voor het installeren en configureren van Sensor voor Apache Server 1.3, Apache Server 2.0.42 of hoger, of Apache Server 2.2 die wordt uitgevoerd onder Microsoft Windows Server 2000 of hoger.

De programmabestanden voor Sensor worden verpakt in een installatiebestand dat u van de downloadsite van de Adobe ontvangt. Als u nog geen Sensor-installatiebestand voor uw specifieke webserver hebt, downloadt u het bestand (of vraagt u het op bij uw Adobe-vertegenwoordiger) voordat u de volgende procedures start.

* Apache Server 1.3
* Apache Server 2.0.42 of hoger
* Apache Server 2.2 die onder Microsoft Windows Server 2000 of hoger wordt uitgevoerd

## De programmabestanden installeren {#section-2f3e85083b4f4aa989a85997330e86ae}

Voordat u de programmabestanden kunt installeren, moet u bepalen waar u de schijfwachtrij wilt behouden. Dat is namelijk ook de plaats waar u de programmabestanden moet installeren. Procedure voor het uitpakken en installeren van de programmabestanden voor Sensor.

Als u Sensor wilt installeren en configureren, moet u de volgende stappen uitvoeren:

1. Maak op uw Windows-computer een directory waarin u de Sensor-programmabestanden wilt installeren. Onthoud dat de schijfwachtrij zich ook in deze map bevindt. Zorg er dus voor dat het apparaat dat u kiest, voldoende ruimte heeft om een wachtrij met de gewenste grootte vast te houden.

   ```
   C:\VisualSensor
   ```

1. Pak de inhoud van het installatiebestand uit in de map die u net hebt gemaakt. Tijdens deze stap installeert Sensor de volgende bestanden:

<table id="table_ABFF5F92271B4F3CB0AC68DAB6A5709F"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Bestand </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> EventMessages.dll </td> 
   <td colname="col2"> Gebeurtenisviewerberichten. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> mod_visual_sciences.dll </td> 
   <td colname="col2"> De verzamelaarmodule. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>TestExperiment.xls </p> </td> 
   <td colname="col2"> <p>Een Excel-spreadsheetbestand dat architecten kunnen gebruiken om een gecontroleerd experiment te configureren. Sensor gebruikt dit bestand niet. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> trust_ca_cert.pem </td> 
   <td colname="col2"> Het certificaat dat wordt gebruikt om het digitale certificaat te bevestigen dat de Server van het Inzicht tijdens het verbindingsproces presenteert. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> TXLog.exe </td> 
   <td colname="col2"> Het uitzendprogramma </td> 
  </tr> 
  <tr> 
   <td colname="col1"> txlogd.conf </td> 
   <td colname="col2"> Het Sensor-configuratiebestand </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Het installatiepakket bevat een spreadsheetbestand met de naam TestExperiment.xls. Dit spreadsheet is een hulpmiddel dat de architecten gebruiken om een gecontroleerd experiment te vormen. Sensor zelf gebruikt dit bestand niet. U hoeft het bestand dus niet te installeren op de computer waarop de Sensor wordt uitgevoerd (maar u kunt dit desgewenst doen). In plaats daarvan kunt u het bestand kopiëren naar een locatie waar uw architecten het kunnen openen of het bestand gewoon uit het installatiepakket extraheren. Zie de Gids met gecontroleerde experimenten voor meer informatie over gecontroleerde experimenten.

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

Voor Apache-servers is de verzamelaar een dynamisch, gezamenlijk object dat u in uw webserverproces laadt.

Als u de verzamelaar aan uw webserver wilt toevoegen, moet u de opdracht [!DNL httpd.conf] en start de webserver opnieuw op.

>[!NOTE]
>
>Als Sensor gegevens vastlegt voor meerdere webservers op de servercomputer, moet u de volgende procedure voor elke webserver uitvoeren.

1. Open met een teksteditor de [!DNL httpd.conf]bestand voor de webserver waarvan de gebeurtenissen worden vastgelegd door Sensor.
1. Voeg de volgende twee regels toe aan het einde van het bestand:

   ```
   LoadModule visual_sciences_module modules/mod_visual_sciences.so 
   VisualSciencesConfig /etc/txlogd.conf
   ```

   >[!NOTE]
   >
   >Deze regels zijn hoofdlettergevoelig. Typ deze precies zoals ze hierboven worden weergegeven.

1. Start het webserverproces opnieuw (u hoeft niet de gehele servercomputer opnieuw op te starten, start gewoon het webserverproces opnieuw). De verzamelaar wordt met de webserver geladen en begint gebeurtenisgegevens te verzamelen en naar de schijfwachtrij te schrijven.
