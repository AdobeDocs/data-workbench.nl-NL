---
description: Instructies voor het installeren van en het vormen van Sensor voor de StandaardUitgave 7 die van de Server van de Toepassing van het Systeem van Zon Java onder de Server 2000 lopen van Vensters of later.
title: De Server van Java van de zon op de Server 2000 van Vensters of later
uuid: 43f3eee0-2633-4bda-af6c-6c15433dd539
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# De Server van Java van de zon op de Server 2000 van Vensters of later{#sun-java-server-on-windows-server-or-later}

Instructies voor het installeren van en het vormen van Sensor voor de StandaardUitgave 7 die van de Server van de Toepassing van het Systeem van Zon Java onder de Server 2000 lopen van Vensters of later.

De programmadossiers voor Sensor worden verpakt in een installatiedossier dat u van de de downloadplaats van Adobe verkrijgt. Als u niet reeds het de installatiedossier van de Sensor voor uw bepaalde Webserver hebt, download het (of verkrijg het van uw vertegenwoordiger van Adobe) alvorens u met de volgende procedures begint.

De sensor steunt de volgende servers die onder RedHat Linux 7.x of later of Sun Solaris SPARC 2.6 of later lopen:

Om Sensor te installeren en te vormen, moet u de volgende stappen uitvoeren:

## De programmabestanden installeren {#section-2f3e85083b4f4aa989a85997330e86ae}

Procedure om de programmadossiers voor Sensor aan de server te halen en te installeren.

1. Voor uw Onderneming van Netscape, creëren iPlanet, Zon ÉÉN, of de Server van het Systeem van Java van de Zon, een folder waarin om de het programmadossiers van de Sensor te installeren. Houd in mening dat uw schijfrij in deze folder verblijft, zodat ben zeker het apparaat u kiest voldoende ruimte heeft om een rij van de grootte te houden u wenst.

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
   <td colname="col1"> saf_visual_sciences.dll </td> 
   <td colname="col2"> De module van de inzamelaarbelasting. </td> 
   <td colname="col3"> <i>/usr/local/aolserver/visual_sciences</i> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>txlogge </p> </td> 
   <td colname="col2"> Het uitzendprogramma. </td> 
   <td colname="col3"> <p><i>/usr/local/bin</i> </p> <p><i>—OF—</i> </p> <p><i>/usr/local/sbin</i> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> txlogd.conf </td> 
   <td colname="col2"> Het de configuratiedossier van de Sensor. </td> 
   <td colname="col3"> <i>/etc</i> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> trust_ca_cert.pem </td> 
   <td colname="col2"> Het certificaat dat wordt gebruikt om het digitale certificaat te bevestigen dat de Server van het Inzicht tijdens het verbindingsproces voorstelt </td> 
   <td colname="col3"> <i>/usr/local/visual_sciences</i> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Het installatiepakket bevat een spreadsheetdossier genoemd TestExperiment.xls. Deze spreadsheet is een hulpmiddel dat de architecten gebruiken om een gecontroleerd experiment te vormen. De sensor zelf gebruikt dit dossier niet, zodat is het niet noodzakelijk om het dossier op de machine te installeren waar de Sensor loopt (hoewel u kunt verkiezen om dit te doen). U zou, in plaats daarvan, het dossier aan een plaats kunnen willen kopiëren waar uw architecten tot het kunnen toegang hebben of eenvoudig het dossier uit het installatiepakket halen zoals nodig. Voor meer informatie over gecontroleerde experimentatie, zie de Gids van de Experimenten van het Inzicht de Gecontroleerde.

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

1. Om te bevestigen dat de zender correct loopt, klik Begin > Controlebord > Administratieve Hulpmiddelen > de Diensten. In de de dienstlijst, bepaal de plaats van de ingang voor Sensor en bevestig dat zijn status Begonnen is en zijn starttype Automatisch is. Dan sluit het de controlepaneel van de Diensten.
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

## Het opstartscript wijzigen {#section-19a38f27c9f44adf88f8910f5ed483a3}

In het init.conf- dossier (bijvoorbeeld, C:\Sun\AppServer7\domains\domain1\server1\config\ init.conf), voeg de volgende lijnen aan het eind van het dossier toe:

```
Init fn="load-modules" shlib="C:/VisualSciences/saf_visual_sciences.dll" 
funcs="vys-cookie,vys-log,vys-init,vys-content-type" 
Init fn="vys-init" config-file="C:/VisualSciences/txlogd.conf"
```

In het obj.conf- dossier (bijvoorbeeld, C:\Sun\AppServer7\domains\domain1\server1\config\ server1-obj.conf), voeg direct de volgende lijnen onder de bestaande &quot;<Object name="default">&quot;lijn toe:

```
NameTrans fn="vys-cookie" 
ObjectType fn="vys-content-type" 
AddLog fn="vys-log"
```

