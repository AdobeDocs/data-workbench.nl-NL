---
description: Instructies over het installeren en configureren van Sensor voor Lotus Domino Server 6 voor Windows 3.1 of hoger en het uitvoeren van Sensor voor Microsoft Windows Server 2000 of hoger.
title: Lotus Domino Server op Windows Server 2000 of hoger
uuid: e3fb1478-92d1-4488-a4b8-244d258cc00a
exl-id: b736c8e6-0642-419c-8715-6586c21f2182
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '924'
ht-degree: 0%

---

# Lotus Domino Server op Windows Server 2000 of hoger{#lotus-domino-server-on-windows-server-or-later}

{{eol}}

Instructies over het installeren en configureren van Sensor voor Lotus Domino Server 6 voor Windows 3.1 of hoger en het uitvoeren van Sensor voor Microsoft Windows Server 2000 of hoger.

De programmabestanden voor Sensor worden verpakt in een installatiebestand dat u van de downloadsite van de Adobe ontvangt. Als u nog geen Sensor-installatiebestand voor uw specifieke webserver hebt, downloadt u het bestand (of vraagt u het op bij uw Adobe-vertegenwoordiger) voordat u de volgende procedures start.

Als u Sensor wilt installeren en configureren, moet u de volgende stappen uitvoeren:

## De programmabestanden installeren {#section-2f3e85083b4f4aa989a85997330e86ae}

1. Maak op uw Lotus Domino-computer een directory om de Sensor-programmabestanden te installeren. Onthoud dat de schijfwachtrij zich ook in deze map bevindt. Zorg er dus voor dat het apparaat dat u kiest, voldoende ruimte heeft om een wachtrij met de gewenste grootte vast te houden.

   ```
   C:\VisualSensor
   ```

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

## De Lotus Domino-server configureren {#section-2e2f1875a5304cdfa2cbcd0680683cfd}

Stappen om de Lotus Domino-server te configureren.

1. Meld u aan bij de beheerder van Lotus Domino en klik op **[!UICONTROL Domain]**.

   ![](assets/dom_svr1.png)

1. Klik in Lotus Domino Administrator op **[!UICONTROL Configuration]**.

   ![](assets/dom_svr2.png)

1. Vouw het knooppunt Server uit en klik op **[!UICONTROL Current Server Document]**.

   ![](assets/dom_svr3.png)

1. Klikken **[!UICONTROL Current Server Document]** en klik vervolgens op **[!UICONTROL Internet Protocols]**.

   ![](assets/dom_svr4.png)

1. Dubbelklik op het tabblad HTTP onder de sectie DSAPI op het woord [!DNL ndolextn].

   ![](assets/dom_svr5.png)

1. Druk **[!UICONTROL Enter]** en typ in het pad naar het [!DNL dominosensor.dll] bestand.

   ![](assets/dom_svr6.png)

1. Klik op **[!UICONTROL Save & Close]**.

   ![](assets/dom_svr7.png)

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

1. Selecteer in het menu Start in Windows de optie **Accessoires** > **Opdrachtprompt**.

1. Navigeer in het opdrachtpromptvenster naar de map waarin u Sensor hebt geïnstalleerd en voer de volgende opdracht uit:

   ```
   txlog /regserver
   ```

   Dit bevel begint de zender, leidt tot de schijfrij, en registreert Sensor als dienst van Vensters.

1. Om te bevestigen dat de zender correct loopt, klik **Start > Configuratiescherm > Systeembeheer > Services**.

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
1. Controleer of de zender de schijfwachtrij heeft gemaakt ( [!DNL Diskq2000.log]) in de map waarin u de Sensor-programmabestanden hebt geïnstalleerd en dat dit de grootte is die u hebt opgegeven in het dialoogvenster [!DNL QueueSize] in de [!DNL txlogd.conf] bestand.

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
