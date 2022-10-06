---
description: Installeer en configureer de sensor voor Microsoft IIS 7.x of 8.x die wordt uitgevoerd onder Microsoft Windows Server 2008 of hoger.
title: Microsoft IIS op Windows Server 2008 of hoger
uuid: 7fd8da68-1553-4395-b13e-b08a6ee1948e
exl-id: cc909daa-60c0-4188-8e90-035c41bf3105
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '1589'
ht-degree: 0%

---

# Microsoft IIS op Windows Server 2008 of hoger{#microsoft-iis-on-windows-server-or-later}

{{eol}}

Installeer en configureer de sensor voor Microsoft IIS 7.x of 8.x die wordt uitgevoerd onder Microsoft Windows Server 2008 of hoger.

De programmabestanden voor Sensor worden verpakt in een installatiebestand dat u van de downloadsite van de Adobe ontvangt. Als u nog geen Sensor-installatiebestand voor uw specifieke webserver hebt, downloadt u het bestand (of vraagt u het op bij uw Adobe-vertegenwoordiger) voordat u de volgende procedures start.

Voor het installeren en configureren van Sensor moet u de volgende stappen op hoog niveau uitvoeren:

1. [De programmabestanden installeren](../../../home/c-snsr-ovrvw/c-inst-snsr/c-install-iis-win8.md#section-cb51e5932a6d40c5b00758a7a51b7578)
1. [Het Sensor-configuratiebestand bewerken](../../../home/c-snsr-ovrvw/c-inst-snsr/c-install-iis-win8.md#section-1e1590a92222430e92066292512ae0df)
1. [De zender starten en de schijfwachtrij maken](../../../home/c-snsr-ovrvw/c-inst-snsr/c-install-iis-win8.md#section-2b8dfd06996d4ab49998eeb99bd9f5f0)
1. [De verzamelaar toevoegen aan de webserver](../../../home/c-snsr-ovrvw/c-inst-snsr/c-install-iis-win8.md#section-088960c986cf449cb712152298b3518d)
1. [Extra gegevens vastleggen](../../../home/c-snsr-ovrvw/c-inst-snsr/c-install-iis-win8.md#section-98db9625efdc4b60bfd76f7adf4af74d)

## De programmabestanden installeren {#section-cb51e5932a6d40c5b00758a7a51b7578}

Wanneer Sensor wordt uitgevoerd op Windows IIS, moeten de programmabestanden en het bestand met de schijfwachtrij zich in dezelfde map bevinden.

Voordat u de programmabestanden installeert, moet u eerst bepalen waar u de schijfwachtrij wilt behouden, omdat u de programmabestanden dan moet installeren.

Gebruik de volgende procedure om de programmabestanden voor Sensor te extraheren en te installeren.

1. Maak op uw Windows-computer een directory waarin u de Sensor-programmabestanden wilt installeren. Onthoud dat de schijfwachtrij zich ook in deze map bevindt. Zorg er dus voor dat het apparaat dat u kiest, voldoende ruimte heeft om een wachtrij met de gewenste grootte vast te houden.

   Bijvoorbeeld: C:\VisualSensor

1. Pak de inhoud van het installatiebestand uit in de map die u net hebt gemaakt. Tijdens deze stap installeert Sensor de volgende bestanden:

<table id="table_C9E8803E51D046FD8FCCA38F8DAC04D1">
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
   <td colname="col1"> qlog.dll </td>
   <td colname="col2"> De verzamelaarmodule (een ISAPI-filter). </td>
  </tr>
  <tr>
   <td colname="col1"> TestExperiment.xls </td>
   <td colname="col2"> <p>Een Excel-spreadsheetbestand dat architecten kunnen gebruiken om een gecontroleerd experiment te configureren. </p> <p>Sensor gebruikt dit bestand niet. </p> </td>
  </tr>
  <tr>
   <td colname="col1"> trust_ca_cert.pem </td>
   <td colname="col2"> Het certificaat dat wordt gebruikt om het digitale certificaat te bevestigen dat de Server van het Inzicht tijdens het verbindingsproces presenteert. </td>
  </tr>
  <tr>
   <td colname="col1"> TXLog.exe </td>
   <td colname="col2"> Het verzendprogramma. </td>
  </tr>
  <tr>
   <td colname="col1"> txlogd.conf </td>
   <td colname="col2"> Het Sensor-configuratiebestand. </td>
  </tr>
 </tbody>
</table>

>[!NOTE]
>
>Het installatiepakket bevat een spreadsheetbestand met de naam TestExperiment.xls. Dit spreadsheet is een hulpmiddel dat de architecten gebruiken om een gecontroleerd experiment te vormen. Sensor zelf gebruikt dit bestand niet. U hoeft het bestand dus niet te installeren op de computer waarop de Sensor wordt uitgevoerd (maar u kunt dit desgewenst doen). In plaats daarvan kunt u het bestand kopiëren naar een locatie waar uw architecten het kunnen openen of het bestand gewoon uit het installatiepakket extraheren. Zie de Gids met gecontroleerde experimenten voor meer informatie over gecontroleerde experimenten.

## Het Sensor-configuratiebestand bewerken {#section-1e1590a92222430e92066292512ae0df}

Het bestand txlogd.conf bevat de configuratieparameters voor Sensor.

U moet het dossier uitgeven om, onder andere, de grootte van de schijfrij, het adres van de Server van het Inzicht, en identiteitskaart te specificeren die aan de gegevens zal worden vastgemaakt die door deze sensor worden geproduceerd. Het configuratiebestand bevat vereiste parameters en optionele parameters.

* **Vereiste parameters** Dit zijn instellingen die u moet opgeven wanneer u Sensor installeert. Zonder deze instellingen wordt Sensor niet uitgevoerd.
* **Optionele parameters** Dit zijn instellingen die standaard op vooraf gedefinieerde waarden (die u kunt wijzigen) of die optionele functies inschakelen.

**Het Sensor-configuratiebestand bewerken**

1. Open de `<SensorDirectory>/txlogd.conf` in een teksteditor en stel de vereiste parameters en eventueel gewenste optionele parameters in.

   Voor beschrijvingen van [!DNL txlogd.conf] parameters, zie [Sensor Txlogd.conf, bestandsparameters](../../../home/c-snsr-ovrvw/sensor-txlogd-params/sensor-txlogd-params.md#concept-4bb629f058894b4abc65a31eb02eebed).

1. Sla het bestand op en sluit het.

## De zender starten en de schijfwachtrij maken {#section-2b8dfd06996d4ab49998eeb99bd9f5f0}

Nadat u vormt [!DNL txlogd.conf]kunt u het verzendprogramma starten, het registreren als Windows-service en de schijfwachtrij maken.

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
1. Verifieer dat de zender de schijfrij (Diskq2008.log) in de folder heeft gecreeerd waar u de het programmadossiers van de Sensor installeerde en dat het de grootte is die u in de parameter QueueSize in het txlogd.conf- dossier specificeerde.

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

## De verzamelaar toevoegen aan de webserver {#section-088960c986cf449cb712152298b3518d}

Voor IIS, is de inzamelaar een filter ISAPI dat u aan uw Webserver in IIS toevoegt.

1. IIS Manager openen met **Start > Systeembeheer > Internet Information Services (IIS) Manager**.
1. Breid uit **Lokale computer** en **Sites** knooppunten.
1. Selecteer de website en dubbelklik in het rechterdeelvenster **ISAPI-filters**.
1. Onder de **Handelingen** deelvenster, klikt u op **Toevoegen**.

1. In de **Filternaam** voert u een weergavenaam voor het filter in. De voorgestelde filternaam is &quot;Sensor&quot;.
1. Klikken **Bladeren**, selecteert u het bestand qlog.dll (in de map waarin u Sensor hebt geïnstalleerd) en klikt u op **OK**.

1. Klikken **OK** om het filter toe te voegen.

   Nadat u het filter hebt toegevoegd, is de verzamelaar direct operationeel en klaar om gegevens te verzamelen.

Voer de volgende stappen uit als de groene pijl niet wordt weergegeven nadat het verkeer naar de verzamelaar is gegaan:

1. Klik op Start > Systeembeheer > Gebeurtenisviewer om te controleren of er fouten optreden in de Event Viewer.

   >[!NOTE]
   >
   >Deze bevelopeenvolging zou kunnen variëren afhankelijk van welke versie van Vensters u gebruikt.

1. Selecteer in het linkerdeelvenster van het venster van de Event Viewer de optie **Toepassing** log.
1. Zoek in het rechterdeelvenster naar gebeurtenissen met &quot;Adobe&quot; in het dialoogvenster **Bron** kolom.
1. Als u een fout vindt, dubbelklikt u op de fout om de fout weer te geven **Gebeurteniseigenschappen** venster.

## Extra gegevens vastleggen {#section-98db9625efdc4b60bfd76f7adf4af74d}

Webpagina&#39;s zijn vaak gestructureerd met de programmeertaal ASP (Active Server Pages).

ASP is een technologie van Microsoft die binnen IIS loopt. Wanneer browser om een dossier van het ASPIS verzoekt, gaat IIS het verzoek tot de motor van het ASPIS over. De ASP-engine leest het ASP-bestand regel voor regel en voert de scripts in het bestand uit. Ten slotte wordt het ASP-bestand als normale HTML aan de browser geretourneerd. ASP biedt RESPOND- of REQUEST-objecten die, naast andere toepassingen, het antwoord of de aanvraag van gebruikersquery&#39;s of gegevens die vanuit HTML-formulieren worden verzonden mogelijk maken.

In bepaalde gevallen wilt u de waarden die in formulieren zijn ingevoerd, mogelijk niet toevoegen aan de URL die wordt weergegeven in de adresbalk van de browser van de gebruiker of die kan worden weergegeven in de HTML-code zelf. Met ASP-script aan de serverzijde kunt u namen van formuliervelden en hun respectieve waarden aan het logbestand toevoegen zonder deze beschikbaar te maken in de browser van de gebruiker of in het HTML-bestand in te sluiten. Als u de werkelijke formulierwaarden wilt vastleggen die in bepaalde formulieren op uw website zijn ingevoerd, moet u enkele coderegels toevoegen om de formulierwaarden aan de logaanvraag toe te voegen.

Neem op de pagina voor de verwerking van een formulier de volgende code op om de ingevoerde formulierwaarden aan de aanvraaggegevens toe te voegen (en schrijf de ingediende formulierwaarden niet alleen naar een externe database of een andere locatie):

```
var sName= Request.Form("Name");
var sCity= Request.Form("City");
var sState= Request.Form("State");
var sZip= Request.Form("Zip");

Response.AppendToLog("&v_1=" +  sName);
Response.AppendToLog("&v_2=" +  sCity);
Response.AppendToLog("&v_3=" +  sState);
Response.AppendToLog("&v_4=" +  sZip);
```

Hiermee voegt u de formulierwaarden zoals gedefinieerd toe aan de aanvraaggegevens voor de pagina Formulierverwerking. In de loggegevens zijn de toegevoegde waarden beschikbaar als queryreeksen van de pagina Formulierverwerking, zoals hieronder wordt weergegeven. v_1, v_2, v_3 en v_4 zijn nu bijvoorbeeld queryreeksen die de gegevens bevatten die in de desbetreffende formuliervelden zijn ingevoerd. De syntaxis die in het vorige voorbeeld wordt beschreven, kan worden gedupliceerd voor extra formuliervelden en waarden die u wilt vastleggen:

```
https://www.myserver.com/path/to/formprocessingpage.asp?v_1=John+Smith&v_2=Los+Angeles&v_3=California&v_4=90210
```

Als u wilt dat elk formulierveld en elke waarde worden vastgelegd en beschikbaar zijn voor analyse, kunt u de volgende syntaxis gebruiken:

```
var formvalues = Response.Form;
Response.AppendToLog(formvalues);
```

In dit voorbeeld worden alle formuliervelden in de HTML samen met de bijbehorende waarden gebruikt en worden deze als queryreeksen toegevoegd aan de logbestandvermelding voor de pagina Formulierverwerking. Houd er rekening mee dat dit alle verborgen velden in het formulier omvat.

De loggegevens worden aangevuld zoals in de volgende tabel wordt beschreven:

| Gegevens verzameld | Toelichting | Voorbeeld |
|---|---|---|
| v_1 | Waarde die is gekoppeld aan de queryreeks NAME | v_1=John Smith |
| v_2 | Waarde die is gekoppeld aan de CITY-queryreeks | v_2=Los Angeles |
| v_3 | Waarde verbonden aan het de vraagkoord van de STAAT | v_3=California |
| v_4 | Waarde die is gekoppeld aan de ZIP-queryreeks | v_4=90210 |

<!-- <a id="section_55C623AC973246DC9EBECD48DA1EE0F7"></a> -->
