---
description: Installeer en vorm Sensor voor Microsoft IIS 7.x of 8.x die onder de Server 2008 of later van Microsoft Windows lopen.
title: Microsoft IIS op de Server 2008 van Vensters of later
uuid: 7fd8da68-1553-4395-b13e-b08a6ee1948e
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Microsoft IIS op de Server 2008 van Vensters of later{#microsoft-iis-on-windows-server-or-later}

Installeer en vorm Sensor voor Microsoft IIS 7.x of 8.x die onder de Server 2008 of later van Microsoft Windows lopen.

De programmadossiers voor Sensor worden verpakt in een installatiedossier dat u van de de downloadplaats van Adobe verkrijgt. Als u niet reeds het de installatiedossier van de Sensor voor uw bepaalde Webserver hebt, download het (of verkrijg het van uw vertegenwoordiger van Adobe) alvorens u met de volgende procedures begint.

Om Sensor te installeren en te vormen, moet u de volgende stappen op hoog niveau uitvoeren:

1. [De programmabestanden installeren](../../../home/c-snsr-ovrvw/c-inst-snsr/c-install-iis-win8.md#section-cb51e5932a6d40c5b00758a7a51b7578)
1. [Geef het de configuratiedossier van de Sensor uit](../../../home/c-snsr-ovrvw/c-inst-snsr/c-install-iis-win8.md#section-1e1590a92222430e92066292512ae0df)
1. [Start de zender en maak de schijfwachtrij](../../../home/c-snsr-ovrvw/c-inst-snsr/c-install-iis-win8.md#section-2b8dfd06996d4ab49998eeb99bd9f5f0)
1. [Voeg de inzamelaar aan de Webserver toe](../../../home/c-snsr-ovrvw/c-inst-snsr/c-install-iis-win8.md#section-088960c986cf449cb712152298b3518d)
1. [Bijkomende gegevens vastleggen](../../../home/c-snsr-ovrvw/c-inst-snsr/c-install-iis-win8.md#section-98db9625efdc4b60bfd76f7adf4af74d)

## De programmabestanden installeren {#section-cb51e5932a6d40c5b00758a7a51b7578}

Wanneer het lopen van Sensor op Vensters IIS, moeten de programmadossiers en het dossier van de schijfrij in de zelfde folder verblijven.

Alvorens de programmadossiers te installeren, bepaal eerst waar u de schijfrij wilt handhaven omdat dat is waar u de programmadossiers moet installeren.

Gebruik de volgende procedure om de programmadossiers voor Sensor te halen en te installeren.

1. Voor uw machine van Vensters, creeer een folder waarin om de het programmadossiers van de Sensor te installeren. Houd in mening dat uw schijfrij ook in deze folder verblijft, zodat ben zeker het apparaat u kiest voldoende ruimte heeft om een rij van de grootte te houden u wenst.

   Bijvoorbeeld: C:\VisualSensor

1. Haal de inhoud van het installatiedossier in de folder uit u enkel creeerde. Tijdens deze stap installeert de sensor de volgende bestanden:

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
   <td colname="col2"> De berichten van de Kijker van de gebeurtenis. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> qlog.dll </td> 
   <td colname="col2"> De collectormodule (een filter ISAPI). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> TestExperiment.xls </td> 
   <td colname="col2"> <p>Een de spreadsheetdossier van Excel dat de architecten kunnen gebruiken om een gecontroleerd experiment te vormen. </p> <p>De sensor gebruikt dit dossier niet. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> trust_ca_cert.pem </td> 
   <td colname="col2"> Het certificaat dat wordt gebruikt om het digitale certificaat te bevestigen dat de Server van het Inzicht tijdens het verbindingsproces voorstelt. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> TXLog.exe </td> 
   <td colname="col2"> Het uitzendprogramma. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> txlogd.conf </td> 
   <td colname="col2"> Het de configuratiedossier van de Sensor. </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Het installatiepakket bevat een spreadsheetdossier genoemd TestExperiment.xls. Deze spreadsheet is een hulpmiddel dat de architecten gebruiken om een gecontroleerd experiment te vormen. De sensor zelf gebruikt dit dossier niet, zodat is het niet noodzakelijk om het dossier op de machine te installeren waar de Sensor loopt (hoewel u kunt verkiezen om dit te doen). U zou, in plaats daarvan, het dossier aan een plaats kunnen willen kopiëren waar uw architecten tot het kunnen toegang hebben of eenvoudig het dossier uit het installatiepakket halen zoals nodig. Voor meer informatie over gecontroleerde experimentatie, zie de Gids van de Experimenten van het Inzicht de Gecontroleerde.

## Geef het de configuratiedossier van de Sensor uit {#section-1e1590a92222430e92066292512ae0df}

Het txlogd.conf- dossier bevat de configuratieparameters voor Sensor.

U moet het dossier uitgeven om, onder andere, de grootte van de schijfrij, het adres van de Server van het Inzicht, en identiteitskaart te specificeren die aan de gegevens zal worden vastgemaakt die door deze sensor worden geproduceerd. Het configuratiedossier bevat vereiste parameters en facultatieve parameters.

* **De vereiste parameters** zijn montages die u moet specificeren wanneer u Sensor installeert. Zonder deze montages, loopt de Sensor niet met succes.
* **De facultatieve parameters** zijn montages die aan vooraf bepaalde waarden (die u kunt wijzigen) in gebreke blijven of facultatieve eigenschappen toelaten.

**Om het de configuratiedossier van de Sensor uit te geven**

1. Open het `<SensorDirectory>/txlogd.conf` dossier in een tekstredacteur en plaats de vereiste parameters evenals om het even welke gewenste facultatieve parameters.

   Voor beschrijvingen van [!DNL txlogd.conf] parameters, zie de Parameters [van het Dossier van de](../../../home/c-snsr-ovrvw/sensor-txlogd-params/sensor-txlogd-params.md#concept-4bb629f058894b4abc65a31eb02eebed)Sensor Txlogd.conf.

1. Sparen en sluit het dossier.

## Start de zender en maak de schijfwachtrij {#section-2b8dfd06996d4ab49998eeb99bd9f5f0}

Nadat u het [!DNL txlogd.conf]dossier vormt, kunt u het uitzendingsprogramma beginnen, het registreren als dienst van Vensters, en de schijfrij creëren.

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
1. Verifieer dat de zender de schijfrij (Diskq2008.log) in de folder heeft gecreeerd waar u de het programmadossiers van de Sensor installeerde en dat het de grootte is die u in de parameter QueueSize in het txlogd.conf- dossier specificeerde.

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

## Voeg de inzamelaar aan de Webserver toe {#section-088960c986cf449cb712152298b3518d}

Voor IIS, is de inzamelaar een filter ISAPI die u aan uw Webserver in IIS toevoegt.

1. Open de Manager IIS gebruikend **Begin > Administratieve Hulpmiddelen > de Manager** van de Informatie van Internet van de Diensten (IIS).
1. Breid de **Lokale knopen van de Computer** en van de **Plaatsen** uit.
1. Selecteer de website, en in de juiste ruit, klik **Filters** ISAPI tweemaal.
1. Klik in het deelvenster **Acties** op **Toevoegen**.

1. Op het gebied van de Naam **van de** Filter, ga een vertoningsnaam voor de filter in. De voorgestelde filternaam is &quot;Sensor.&quot;
1. Klik **doorbladeren**, selecteren het qlog.dll- dossier (dat in de folder wordt gevestigd waar u Sensor) installeerde, en klikken **O.K.**.

1. Klik op **OK** om het filter toe te voegen.

   Nadat u de filter toevoegt, is de inzamelaar onmiddellijk operationeel en klaar om gegevens te verzamelen.

Als de groene pijl niet na verkeersstromen aan de inzamelaar verschijnt, voltooi de volgende stappen:

1. Klik op Start > Administrative Tools > Event Viewer om de Event Viewer te controleren op fouten.

   >[!NOTE]
   >
   >Deze bevelopeenvolging zou kunnen variëren afhankelijk van welke versie van Vensters u gebruikt.

1. In de linkerruit van het venster van de Kijker van de Gebeurtenis, selecteer het logboek van de **Toepassing** .
1. In de juiste ruit, zoek gebeurtenissen met &quot;Adobe&quot;in de kolom **Bron** .
1. Als u een fout vindt, klik de fout tweemaal om het venster van de Eigenschappen van de **Gebeurtenis** te tonen.

## Bijkomende gegevens vastleggen {#section-98db9625efdc4b60bfd76f7adf4af74d}

De Web-pagina&#39;s zijn vaak gestructureerd gebruikend de programmeertaal van het ASPIS (de Actieve Pagina&#39;s van de Server).

ASP is een technologie van Microsoft die binnen IIS loopt. Wanneer browser om een dossier van het ASPIS verzoekt, gaat IIS het verzoek tot de motor van het ASPIS over. De motor van het ASPIS leest het dossier van het ASPIS, lijn door lijn, en voert de manuscripten in het dossier uit. Tot slot is het dossier van het ASPIS teruggekeerd aan browser als duidelijk HTML. Het ASPIS verstrekt RESPOND of VRAAGT voorwerpen die, naast andere gebruiken, de reactie of het verzoek van gebruikersvragen of gegevens toestaan die van de vormen van HTML worden voorgelegd.

In bepaalde gevallen, kunt u niet de waarden willen toevoegen ingegaan in vormen aan URL die binnen de bar van het Adres van browser van een gebruiker wordt getoond of die binnen de code van HTML zelf viewable is. Het eenvoudige server-zij Manuscript van het ASPIS laat u de namen van het vormgebied en hun respectieve waarden aan het logboekdossier toevoegen zonder hen beschikbaar te maken binnen browser van de gebruiker of hen in het HTML- dossier in te bedden. Om de daadwerkelijke vormwaarden te vangen ingegaan in bepaalde vormen binnen uw website, moeten een paar lijnen van code worden toegevoegd om de vormwaarden aan het logboekverzoek toe te voegen.

Binnen de verwerkingspagina van een formulier de volgende code opnemen om de ingevoerde formulierwaarden aan de aanvraaggegevens toe te voegen (naast het schrijven van de ingediende formulierwaarden aan een externe database of een andere locatie):

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

Dit proces zou de vormwaarden zoals die aan de verzoekgegevens voor de pagina van de Verwerking van de Vorm worden bepaald toevoegen. Binnen de logboekgegevens, zouden de toegevoegde waarden als vraagkoorden van de pagina van de Verwerking van de Vorm beschikbaar zijn zoals hieronder geïllustreerd. Bijvoorbeeld, v_1, v_2, v_3 en v_4 zou nu vraagkoorden zijn die de gegevens bevatten ingegaan in de aangewezen vormgebieden. De syntaxis die in het vorige voorbeeld wordt beschreven kan voor om het even welke extra vormgebieden en waarden worden gedupliceerd die u wilt vangen:

```
http://www.myserver.com/path/to/formprocessingpage.asp?v_1=John+Smith&v_2=Los+Angeles&v_3=California&v_4=90210
```

Als u wilt dat elk formulierveld en elke waarde worden vastgelegd en beschikbaar zijn voor analyse, kunt u de volgende syntaxis gebruiken:

```
var formvalues = Response.Form; 
Response.AppendToLog(formvalues);
```

Dit voorbeeld zou alle vormgebieden aanwezig binnen HTML samen met hun respectieve waarden nemen en hen toevoegen als vraagkoorden aan de logboekingang voor de pagina van de Verwerking van de Vorm. Houd er rekening mee dat dit alle verborgen velden in het formulier omvat.

De logboekgegevens zouden worden verhoogd zoals die in de volgende lijst worden gedetailleerd:

| Verzamelde gegevens | Toelichting | Voorbeeld |
|---|---|---|
| v_1 | Waarde verbonden aan het de vraagkoord van de NAAM | v_1=John Smith |
| v_2 | Waarde verbonden aan het de vraagkoord van de CITY | v_2=Los Angeles |
| v_3 | Waarde verbonden aan het STATE vraagkoord | v_3=Californië |
| v_4 | Waarde verbonden aan het het vraagkoord van het PIT | v_4=90210 |

<!-- <a id="section_55C623AC973246DC9EBECD48DA1EE0F7"></a> -->
