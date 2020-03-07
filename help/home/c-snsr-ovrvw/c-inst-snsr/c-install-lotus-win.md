---
description: Instructies over het installeren en configureren van Sensor voor Lotus Sametime voor Windows 3.1 of hoger onder Microsoft Windows Server 2000 of hoger.
title: Lotus Sametime op de Server 2000 van Vensters of later
uuid: 5e24da54-7ef6-42cf-b693-cc4fd267af93
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Lotus Sametime op de Server 2000 van Vensters of later{#lotus-sametime-on-windows-server-or-later}

Instructies over het installeren en configureren van Sensor voor Lotus Sametime voor Windows 3.1 of hoger onder Microsoft Windows Server 2000 of hoger.

De programmadossiers voor Sensor worden verpakt in een installatiedossier dat u van de de downloadplaats van Adobe verkrijgt. Als u niet reeds het de installatiedossier van de Sensor voor uw bepaalde Webserver hebt, download het (of verkrijg het van uw vertegenwoordiger van Adobe) alvorens u met de volgende procedures begint.

Om Sensor te installeren en te vormen, moet u de volgende stappen op hoog niveau uitvoeren:

## De programmabestanden installeren {#section-2f3e85083b4f4aa989a85997330e86ae}

Wanneer het lopen van Sensor op Sametime, moeten de programmadossiers en het dossier van de schijfrij in de zelfde folder verblijven.

Daarom alvorens de programmadossiers te installeren, moet u bepalen waar u de schijfrij wilt handhaven, omdat dat ook is waar u de programmadossiers moet installeren.

Gebruik de volgende procedure om de programmadossiers voor Sensor te halen en te installeren.

1. Stop de Lotus Domino Server en de dienst van het Registreren van het Praatje Sametime.
1. Op uw machine van Vensters, in de folder van de Domino van Lotus, schrap of steun het dossier genoemd StChatLog.dll.
1. Haal de inhoud van het installatiebestand uit de directory Lotus Domino. Tijdens deze stap installeert de sensor de volgende bestanden:

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
   <td colname="col2"> Event Viewer-berichten </td> 
  </tr> 
  <tr> 
   <td colname="col1"> stchatlog.dll </td> 
   <td colname="col2"> De collectormodule </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>TestExperiment.xls </p> </td> 
   <td colname="col2"> <p>Een de spreadsheetdossier van Excel dat de architecten kunnen gebruiken om een gecontroleerd experiment te vormen </p> <p>De sensor gebruikt dit dossier niet. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> trust_ca_cert.pem </td> 
   <td colname="col2"> Het certificaat dat wordt gebruikt om het digitale certificaat te bevestigen dat de Server van het Inzicht tijdens het verbindingsproces voorstelt </td> 
  </tr> 
  <tr> 
   <td colname="col1"> TXLog.exe </td> 
   <td colname="col2"> Het uitzendprogramma </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>txlogd.conf </p> </td> 
   <td colname="col2"> Het de configuratiedossier van de Sensor </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Het installatiepakket bevat een spreadsheetdossier genoemd TestExperiment.xls. Deze spreadsheet is een hulpmiddel dat de architecten gebruiken om een gecontroleerd experiment te vormen. De sensor zelf gebruikt dit dossier niet, zodat is het niet noodzakelijk om het dossier op de machine te installeren waar de Sensor loopt (hoewel u kunt verkiezen om dit te doen). U zou, in plaats daarvan, het dossier aan een plaats kunnen willen kopiëren waar uw architecten tot het kunnen toegang hebben of eenvoudig het dossier uit het installatiepakket halen zoals nodig. Voor meer informatie over gecontroleerde experimentatie, zie de Gids van de Experimenten van het Inzicht de Gecontroleerde.

## Aanmelden inschakelen op Sametime Server {#section-2e2f1875a5304cdfa2cbcd0680683cfd}

Stappen die u toestaan om aan de Server te registreren Sametime.

1. Gebruik de Lotus Domino Administrator-client om verbinding te maken met de Lotus Domino-server waarop Sametime wordt uitgevoerd.
1. In de Beheerder van de Domino van Lotus, klik het lusje van Dossiers, dan tweemaal klik Configuratie Sametime - stconfig.nsf om het dossier van de Configuratie te openen Sametime.
1. In het dossier van de Configuratie Sametime, open het formulier van de Diensten van de Gemeenschap en klik overal op het formulier tweemaal om binnen te gaan uitgeven wijze.
1. De vastgestelde Vlag van de Registratie van het Praatje aan &quot;streng&quot;en vangt het Type van Dienst aan &quot;0x1000.&quot;
1. Sparen en sluit de vorm van de Diensten Communautaire, dan sluit het dossier van de Configuratie Sametime.
1. Start de Sametime-server opnieuw.

## Geef het Dossier van de Configuratie van de Sensor uit {#section-de0eb4a646394b61abb6cd5a2b706de0}

Het txlogd.conf- dossier bevat de configuratieparameters voor Sensor.

U moet dit dossier uitgeven om, onder andere, de grootte en de plaats van het dossier van de schijfrij, het adres van de Server van het Inzicht, en identiteitskaart te specificeren die aan de gebeurtenisgegevens zal worden vastgemaakt die door deze sensor worden geproduceerd.

Het configuratiedossier bevat vereiste parameters en facultatieve parameters.

* **De vereiste parameters** zijn montages die u moet specificeren wanneer u Sensor installeert. Zonder deze montages, loopt de Sensor niet met succes.
* **De facultatieve parameters** zijn montages die aan vooraf bepaalde waarden (die u kunt wijzigen) in gebreke blijven of facultatieve eigenschappen toelaten.

**Om het de configuratiedossier van de Sensor uit te geven**

* Open het `<Sensor directory>/txlogd.conf` dossier in een tekstredacteur en plaats de vereiste parameters evenals om het even welke gewenste facultatieve parameters.
* Sparen en sluit het dossier.

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

   >[!NOTE]
   >
   >Deze bevelopeenvolging zou kunnen variëren afhankelijk van welke versie van Vensters u gebruikt.

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

1. Start de Lotus Domino Server en de Sametime Chat Logging Service opnieuw.

