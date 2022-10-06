---
description: Instructies over het installeren en configureren van Sensor voor Lotus Sametime voor Windows 3.1 of hoger onder Microsoft Windows Server 2000 of hoger.
title: Lotus Sametime op Windows Server 2000 of hoger
uuid: 5e24da54-7ef6-42cf-b693-cc4fd267af93
exl-id: 9292bfca-ad3b-436d-9d22-be67a61b8c05
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '1023'
ht-degree: 0%

---

# Lotus Sametime op Windows Server 2000 of hoger{#lotus-sametime-on-windows-server-or-later}

{{eol}}

Instructies over het installeren en configureren van Sensor voor Lotus Sametime voor Windows 3.1 of hoger onder Microsoft Windows Server 2000 of hoger.

De programmabestanden voor Sensor worden verpakt in een installatiebestand dat u van de downloadsite van de Adobe ontvangt. Als u nog geen Sensor-installatiebestand voor uw specifieke webserver hebt, downloadt u het bestand (of vraagt u het op bij uw Adobe-vertegenwoordiger) voordat u de volgende procedures start.

Voor het installeren en configureren van Sensor moet u de volgende stappen op hoog niveau uitvoeren:

## De programmabestanden installeren {#section-2f3e85083b4f4aa989a85997330e86ae}

Als Sensor wordt uitgevoerd op Sametime, moeten de programmabestanden en het bestand met de schijfwachtrij zich in dezelfde map bevinden.

Voordat u de programmabestanden installeert, moet u dus bepalen waar u de schijfwachtrij wilt behouden, omdat dat ook de locatie is waar u de programmabestanden moet installeren.

Gebruik de volgende procedure om de programmabestanden voor Sensor te extraheren en te installeren.

1. Stop de Lotus Domino Server en de Sametime Chat Logging Service.
1. Verwijder of maak een back-up van het bestand StChatLog.dll op uw Windows-computer in de Lotus Domino-map.
1. Pak de inhoud van het installatiebestand uit in de Lotus Domino-map. Tijdens deze stap installeert Sensor de volgende bestanden:

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
   <td colname="col2"> Gebeurtenisviewerberichten </td> 
  </tr> 
  <tr> 
   <td colname="col1"> stchatlog.dll </td> 
   <td colname="col2"> De verzamelaarmodule </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>TestExperiment.xls </p> </td> 
   <td colname="col2"> <p>Een Excel-spreadsheetbestand dat architecten kunnen gebruiken om een gecontroleerd experiment te configureren </p> <p>Sensor gebruikt dit bestand niet. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> trust_ca_cert.pem </td> 
   <td colname="col2"> Het certificaat dat wordt gebruikt om het digitale certificaat te bevestigen dat de Server van het Inzicht tijdens het verbindingsproces presenteert </td> 
  </tr> 
  <tr> 
   <td colname="col1"> TXLog.exe </td> 
   <td colname="col2"> Het uitzendprogramma </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>txlogd.conf </p> </td> 
   <td colname="col2"> Het Sensor-configuratiebestand </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Het installatiepakket bevat een spreadsheetbestand met de naam TestExperiment.xls. Dit spreadsheet is een hulpmiddel dat de architecten gebruiken om een gecontroleerd experiment te vormen. Sensor zelf gebruikt dit bestand niet. U hoeft het bestand dus niet te installeren op de computer waarop de Sensor wordt uitgevoerd (maar u kunt dit desgewenst doen). In plaats daarvan kunt u het bestand kopiëren naar een locatie waar uw architecten het kunnen openen of het bestand gewoon uit het installatiepakket extraheren. Zie de Gids met gecontroleerde experimenten voor meer informatie over gecontroleerde experimenten.

## Aanmelding inschakelen op de Sametime-server {#section-2e2f1875a5304cdfa2cbcd0680683cfd}

Stappen die u toestaan om aan de Server van Sametime aan te melden.

1. Gebruik de Lotus Domino Administrator-client om verbinding te maken met de Lotus Domino-server waarop Sametime wordt uitgevoerd.
1. Klik in Lotus Domino Administrator op het tabblad Bestanden en dubbelklik vervolgens op Sametime-configuratie - stconfig.nsf om het Sametime-configuratiebestand te openen.
1. Open in het Sametime-configuratiebestand het formulier Community Services en dubbelklik ergens op het formulier om de bewerkingsmodus te activeren.
1. Stel Chatlogingvlag in op &quot;strikt&quot; en stel Servicetype vastleggen in op &quot;0x1000&quot;.
1. Sla het formulier Community Services op en sluit het. Sluit vervolgens het Sametime-configuratiebestand.
1. Start de Sametime-server opnieuw.

## Het configuratiebestand van de sensor bewerken {#section-de0eb4a646394b61abb6cd5a2b706de0}

Het bestand txlogd.conf bevat de configuratieparameters voor Sensor.

U moet dit dossier uitgeven om, onder andere, de grootte en de plaats van het dossier van de schijfrij, het adres van de Server van het Inzicht, en identiteitskaart te specificeren die aan de gebeurtenisgegevens zal worden vastgemaakt die door deze sensor worden geproduceerd.

Het configuratiebestand bevat vereiste parameters en optionele parameters.

* **Vereiste parameters** Dit zijn instellingen die u moet opgeven wanneer u Sensor installeert. Zonder deze instellingen wordt Sensor niet uitgevoerd.
* **Optionele parameters** Dit zijn instellingen die standaard op vooraf gedefinieerde waarden (die u kunt wijzigen) of die optionele functies inschakelen.

**Het Sensor-configuratiebestand bewerken**

* Open de `<Sensor directory>/txlogd.conf` in een teksteditor en stel de vereiste parameters en eventueel gewenste optionele parameters in.
* Sla het bestand op en sluit het.

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

   >[!NOTE]
   >
   >Deze bevelopeenvolging zou kunnen variëren afhankelijk van welke versie van Vensters u gebruikt.

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

1. Start de Lotus Domino Server en de Sametime Chat Logging Service opnieuw.
