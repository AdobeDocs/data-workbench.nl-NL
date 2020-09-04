---
description: Instructies voor het installeren en het vormen Sensor voor de StandaardUitgave 7 van de Server van de Toepassing van het Systeem van Zon Java die onder de Server 2000 van Vensters of later loopt.
title: Sun Java Server op Windows Server 2000 of hoger
uuid: 43f3eee0-2633-4bda-af6c-6c15433dd539
translation-type: tm+mt
source-git-commit: 8f5c69541bdd97aefbad3840f75f06846615f222
workflow-type: tm+mt
source-wordcount: '956'
ht-degree: 0%

---


# Sun Java Server op Windows Server 2000 of hoger{#sun-java-server-on-windows-server-or-later}

Instructies voor het installeren en het vormen Sensor voor de StandaardUitgave 7 van de Server van de Toepassing van het Systeem van Zon Java die onder de Server 2000 van Vensters of later loopt.

De programmabestanden voor Sensor worden verpakt in een installatiebestand dat u van de downloadsite van de Adobe ontvangt. Als u nog geen Sensor-installatiebestand voor uw specifieke webserver hebt, downloadt u het bestand (of vraagt u het op bij uw Adobe-vertegenwoordiger) voordat u de volgende procedures start.

Sensor ondersteunt de volgende servers die worden uitgevoerd onder RedHat Linux 7.x of hoger of Sun Solaris SPARC 2.6 of hoger:

Als u Sensor wilt installeren en configureren, moet u de volgende stappen uitvoeren:

## De programmabestanden installeren {#section-2f3e85083b4f4aa989a85997330e86ae}

Procedure voor het uitpakken en installeren van de programmabestanden voor Sensor op de server.

1. Voor uw Onderneming Netscape, iPlanet, Zon ONE, of de Server van het Systeem van Zon Java, creeer een folder waarin om de het programmadossiers van de Sensor te installeren. Onthoud dat de schijfwachtrij zich in deze map bevindt. Zorg er dus voor dat het apparaat dat u kiest, voldoende ruimte heeft om een wachtrij met de gewenste grootte vast te houden.

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
   <td colname="col1"> saf_visual_sciences.dll </td> 
   <td colname="col2"> De module voor het laden van verzamelingen. </td> 
   <td colname="col3"> <i>/usr/local/aolserver/visual_sciences</i> </td> 
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

## Het configuratiebestand van de sensor bewerken {#section-2e2f1875a5304cdfa2cbcd0680683cfd}

Het [!DNL txlogd.conf] bestand bevat de configuratieparameters voor Sensor.

U moet dit dossier uitgeven om, onder andere, de grootte en de plaats van het dossier van de schijfrij, het adres van de Server van het Inzicht, en identiteitskaart te specificeren die aan de gebeurtenisgegevens zal worden vastgemaakt die door deze sensor worden geproduceerd.

Het configuratiebestand bevat vereiste parameters en optionele parameters.

* **Vereiste parameters** zijn instellingen die u moet opgeven wanneer u Sensor installeert. Zonder deze instellingen wordt Sensor niet uitgevoerd.
* **Optionele parameters** zijn instellingen die standaard op vooraf gedefinieerde waarden (die u kunt wijzigen) of optionele functies inschakelen.

**Het Sensor-configuratiebestand bewerken**

* Open het [!DNL /etc/txlogd.conf] bestand in een teksteditor en stel de vereiste parameters en eventueel gewenste optionele parameters in.
* Sla het bestand op en sluit het.

**Het Sensor-configuratiebestand bewerken**

1. Open het [!DNL /etc/txlogd.conf] bestand in een teksteditor en stel de vereiste parameters en eventueel gewenste optionele parameters in.
1. Sla het bestand op en sluit het.

## De zender starten en de schijfwachtrij maken {#section-55630de65f264274aefd771da2002852}

Nadat u het bestand txlogd.conf hebt geconfigureerd, kunt u het verzendprogramma starten, het registreren als Windows-service en de schijfwachtrij maken.

1. Selecteer in het menu Start in Windows Accessoires > Opdrachtprompt.
1. Navigeer in het opdrachtpromptvenster naar de map waarin u Sensor hebt geïnstalleerd en voer de volgende opdracht uit:

   ```
   txlog /regserver
   ```

   Dit bevel begint de zender, leidt tot de schijfrij, en registreert Sensor als dienst van Vensters.

1. Klik op Start > Configuratiescherm > Systeembeheer > Services om te bevestigen dat de zender correct wordt uitgevoerd. In de de dienstlijst, bepaal de plaats van de ingang voor Sensor en bevestig dat zijn status Begonnen is en zijn starttype Automatisch is. Sluit vervolgens het configuratiescherm Services.
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

## Het opstartscript wijzigen {#section-19a38f27c9f44adf88f8910f5ed483a3}

Voeg in het bestand init.conf (bijvoorbeeld C:\Sun\AppServer7\domains\domain1\server1\config\ init.conf) de volgende regels toe aan het einde van het bestand:

```
Init fn="load-modules" shlib="C:/VisualSciences/saf_visual_sciences.dll" 
funcs="vys-cookie,vys-log,vys-init,vys-content-type" 
Init fn="vys-init" config-file="C:/VisualSciences/txlogd.conf"
```

Voeg in het bestand obj.conf (bijvoorbeeld C:\Sun\AppServer7\domains\domain1\server1\config\ server1-obj.conf) de volgende regels direct onder de bestaande `<Object name="default">` regel toe:

```
NameTrans fn="vys-cookie" 
ObjectType fn="vys-content-type" 
AddLog fn="vys-log"
```

