---
description: Om de fouten van de Sensor zo snel mogelijk te ontdekken en hen te herstellen alvorens zij belangrijke problemen of stroomonderbrekingen veroorzaken, zou u uw logboeken van de Gebeurtenis regelmatig moeten controleren.
solution: Insight
title: Toezicht op administratieve gebeurtenissen
uuid: c43d6509-6950-4436-8d6c-be7b00664f05
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Toezicht op administratieve gebeurtenissen{#monitoring-administrative-events}

Om de fouten van de Sensor zo snel mogelijk te ontdekken en hen te herstellen alvorens zij belangrijke problemen of stroomonderbrekingen veroorzaken, zou u uw logboeken van de Gebeurtenis regelmatig moeten controleren.

**Aanbevolen frequentie:** Minstens uur

U kunt deze gebeurtenissen controleren gebruikend de Kijker van de Gebeurtenis van Vensters of het dossier van Unix Syslog en de [!DNL *.sensor-log] dossiers die door gebrek in de [!DNL Logs] omslag binnen de [!DNL Sensor] installatiefolder worden gevestigd. Deze dossiers wijzen op de aanwezigheid van fouten tijdens gegevensinzameling, vooral als a [!DNL Sensor] niet met het doel kan verbinden [!DNL data workbench server] en begint een rij vormend gegevens.

## De Gebeurtenissen van de controle op Vensters {#section-7c0443a356af4381bf22259654f5cd17}

De sensor registreert fouten aan het Logboek van de Toepassing van de Kijker van de Gebeurtenis van Vensters met een bron van &quot;Adobe.&quot;

De berichten worden geregistreerd als &quot;Informatie,&quot;Waarschuwing,&quot;of &quot;Fout&quot;afhankelijk van hun strengheid.

**De Windows Event Viewer** openen:

* Klik op **Start > Configuratiescherm > Systeembeheer > Event Viewer**.

## Monitoring van gebeurtenissen op Unix {#section-5de3947891fb47ac88b7c855e545d54a}

De sensor registreert fouten aan de [!DNL syslog] daemon.

syslog daemon schrijft foutenmeldingen aan logboekdossiers die op de regels worden gebaseerd u in uw syslog.conf- dossier specificeerde. De fouten worden geregistreerd met de vlaggen &quot;LOG_DAEMON&quot;en of &quot;LOG_NOTICE&quot;of &quot;LOG_ERR,&quot;afhankelijk van strengheid.

**Om de Unix syslog te openen**

Unix syslog wordt typisch gevestigd in [!DNL /var/adm/messages] of [!DNL /var/log/messages].

Doorblader aan de aangewezen plaats en open syslog.

## Het begrip van de Formaten van het Bericht {#section-a0899add30fd4b2da58a23b9e3324693}

Alle berichten van de Sensor bevatten het koord &quot;Sensor&quot;en genummerd om op het belang van het bericht te wijzen dat wordt getoond.

| Berichtnummer | Betekenis bericht | Message String |
|---|---|---|
| 1xxx | Voorlichting | Sensorinfo # |
| 2xxx | Waarschuwing | Sensorwaarschuwing # |
| 3xxx | Configuratiefout | Sensor-fout # |
| 4xxx | Operationele fout | Sensor-fout # |
| 5xxx | Interne fout | Sensor-fout # |

>[!NOTE]
>
>De waarschuwingen (2xxx) zijn momenteel niet in gebruik. Deze aantallen zijn gereserveerd voor toekomstig gebruik.

Uw hulpmiddel van het netwerkbeheer kan worden geplaatst om uw berichten om de 5-10 minuten voor fouten met de bron van de &quot;Sensor&quot;te controleren en aangewezen personeel over kwesties te alarmeren die interventie kunnen vereisen. U kunt verkiezen om het systeem voor slechts bepaalde types van de berichten van de Gebeurtenis, zoals het koord van de Fout van de &quot;Sensor&quot;te controleren. Alternatief, kunt u verschillende regels op gebeurtenissen toepassen die met &quot;Info van de Sensor,&quot;&quot;de Waarschuwing van de Sensor,&quot;en de koorden van de Fout van de &quot;Sensor&quot;worden voorgevuld.

## Belangrijke berichten identificeren {#section-5a20f5dc18ca4012931d194db855e54e}

Binnen uw gebeurtenislogboeken, zou u speciale aandacht aan moeten besteden en onmiddellijk om het even welke berichten betreffende rijgrootte richten.

Bijvoorbeeld, hebben de berichten zoals &quot; [!DNL Sensor Info 1012: Adobe disk queue is #% full]&quot;aandacht nodig.

## Reageren op berichten van de Gebeurtenis van de Sensor {#section-0004c4a169dc4a8882d9bd87dd326ad4}

Lijsten die de gebeurtenissen van de Sensor beschrijven en acties voor de gesteunde platforms van de Webserver voorstellen.

**Alle platforms**

<table id="table_F8835AC0AD8F43E2B4494D8D35EBC0FD"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Gebeurtenisbericht </th> 
   <th colname="col2" class="entry"> Voorgestelde actie </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Sensor Info 1010: Sensor geïnitialiseerd. </td> 
   <td colname="col2"> Geen actie vereist. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Sensor Info 1011: Sensor beëindigd. Totale geijkte kliks ## </td> 
   <td colname="col2"> Geen actie vereist. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Sensor Info 1012: De schijfrij van Adobe is #% volledig </td> 
   <td colname="col2"> Dit bericht wordt geregistreerd telkens als het gebruik van de schijfrij een 10% drempel kruist. Als dit percentage blijft groeien, zou de actie moeten worden genomen alvorens de rij volledig is en het gegeven wordt verloren. Het waarschijnlijkste probleem is dat de Sensor met het communiceren met de Server van het Inzicht heeft tegengehouden. Contact opnemen met Adobe ClientCare. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Sensor Info 1013: De configuratie van de sensor veranderde </td> 
   <td colname="col2"> Geen actie vereist. De sensor ontdekte een verandering in één van zijn configuratiedossiers en zal herladen. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Sensor Info 1014: Probleem met het zaaien van een willekeurige-aantalgenerator </td> 
   <td colname="col2"> Contact opnemen met Adobe ClientCare. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Sensor Info 1016: Bestandsnaam van configuratiebestand geladen </td> 
   <td colname="col2"> Geen actie vereist. De sensor laadde met succes het vermelde configuratiedossier. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Sensor Info 1017: Experimentele bestandsnaam geladen </td> 
   <td colname="col2"> Geen actie vereist. De sensor laadde met succes het vermelde experimentele dossier. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Sensorfout 3016: Kan configuratiebestand /mypath/myfile niet laden </td> 
   <td colname="col2"> Bevestig dat het de configuratiedossier van de Sensor in de configuratie van de Webserver wordt gespecificeerd bestaat en de vereiste toestemmingen heeft die door het proces van de Webserver moeten worden gelezen. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Sensor 3017: Onbekwaam om gecontroleerd dossier van de experimentconfiguratie /mypath/myfile te laden </p> </td> 
   <td colname="col2"> <p>Bevestig dat het gecontroleerde experimentdossier dat in txlogd.conf wordt gespecificeerd bestaat en dat het tekstproces de noodzakelijke toestemmingen heeft om het dossier te lezen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Sensorfout 3018: Kan lijsten met inhoudsfilters niet ontleden. Het dossier van de de configuratievorm van de controle </td> 
   <td colname="col2"> Verifieer de syntaxis van de ingangen ContentFilterInclude en ContentFilterExclude in txlogd.conf. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Sensorfout 3023: Slot kan niet worden gemaakt (g_lockThrottle) </td> 
   <td colname="col2"> Contact opnemen met Adobe ClientCare. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Sensorfout 3024: Slot kan niet worden gemaakt (g_lockConfigCheck) </td> 
   <td colname="col2"> Contact opnemen met Adobe ClientCare. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Sensorfout 4014: Kon geen schijfrij openen. </td> 
   <td colname="col2"> Verifieer het dossier van QueueFile - noem in txlogd.conf en indien verondersteld om correct te zijn, contacteer Adobe ClientCare. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Sensorfout 4020: Geen wachtrijbestand </td> 
   <td colname="col2"> Verifieer het dossier van QueueFile - noem in txlogd.conf en indien verondersteld om correct te zijn, contacteer Adobe ClientCare. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Sensorfout 4021: De rij is volledig </td> 
   <td colname="col2"> Contact opnemen met Adobe ClientCare. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Sensorfout 4022: Onbekwaam om geheugenblok van lengte &lt;x&gt; bij compensatie &lt;y&gt; in kaart te brengen </td> 
   <td colname="col2"> Contact opnemen met Adobe ClientCare. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Sensorfout 5012: Kan geen mutex maken. </td> 
   <td colname="col2"> Contact opnemen met Adobe ClientCare. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Sensorfout 5013: Kan geen mutex krijgen. </td> 
   <td colname="col2"> Contact opnemen met Adobe ClientCare. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Sensorfout 5030: Fork-fout in de zonsopgang. </td> 
   <td colname="col2"> Contact opnemen met Adobe ClientCare. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Sensorfout 5031: ingesteld is mislukt. </td> 
   <td colname="col2"> Contact opnemen met Adobe ClientCare. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Sensorfout 5032: Fork-fout in de zonsopgang. </td> 
   <td colname="col2"> Contact opnemen met Adobe ClientCare. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Sensorfout 5033: chdir is mislukt. </td> 
   <td colname="col2"> Contact opnemen met Adobe ClientCare. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Sensorfout 5034: Ontvangen signaal </td> 
   <td colname="col2"> Het programma werd waarschijnlijk beëindigd door een extern signaal. Als de bron van dit signaal niet kan worden bepaald, contacteer Adobe ClientCare. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Sensorfout 5035: Uitgang geroepen van buitenhoofd </td> 
   <td colname="col2"> Contact opnemen met Adobe ClientCare. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Sensorfout 5036: txlogd loopt al </td> 
   <td colname="col2"> Een ander geval van de txlogd daemon loopt reeds. Stop eerst de andere instantie als u een nieuwe wilt in werking stellen. </td> 
  </tr> 
 </tbody> 
</table>

**Apache/IBM HTTP Server**

| Gebeurtenisbericht | Voorgestelde actie |
|---|---|
| Sensorfout 3015: De richtlijn VisualSciencesConfig mist van httpd.conf. | Dit is een configuratiefout. De richtlijn VisualSciencesConfig moet in httpd.conf met een parameter zijn die de plaats van txlogd.conf is. |
| Sensorfout 3019: vys-cookie werd niet opgeroepen voor vys-log. Neem contact op met ondersteuning. | Contact opnemen met Adobe ClientCare. |
| Sensorfout 3025: Subverzoek wijst terug naar zich | Contact opnemen met Adobe ClientCare. |

**AOL-server**

| Gebeurtenisbericht | Voorgestelde actie |
|---|---|
| Sensorfout 3015: ns/server/[server]/module/[module] de sectie mist in AOLServer config- dossier. | Dit is een configuratiefout. Correct zoals bij vergissing vermeld. |
| Sensorfout 3019: vys-cookie werd niet opgeroepen voor vys-log. Neem contact op met ondersteuning. Contact opnemen met Adobe ClientCare. | Neem contact op met ondersteuning. Contact opnemen met Adobe ClientCare. |
| Sensorfout 3020: VisualSciencesConfig mist als eerste ingang in [sectie] sectie in AOLServer config- dossier. | Dit is een configuratiefout. Correct zoals bij vergissing vermeld. |
| Sensorfout 3021: VisualSciencesConfig mist een waarde in [sectiesectie] in AOLServer config- dossier. | Dit is een configuratiefout. Correct zoals bij vergissing vermeld. |

**iPlanet en Java System Web Servers**

| Gebeurtenisbericht | Voorgestelde actie |
|---|---|
| Sensorfout 3011: Init-richtlijn vereist. Zoals Init fn=vys-init config-file=&quot;/mypath/myfile&quot; | Dit is een configuratiefout. De iPlanet-richtlijn ontbreekt. |
| Sensorfout 3015: config-dossier wordt niet gespecificeerd in de richtlijn van het Punt van de iPlanet | Dit is een configuratiefout. De weg aan het configuratiedossier werd niet geleverd in de iPlanet richtlijn van het Punt. |
| Sensorfout 3019: vys-cookie werd niet opgeroepen voor vys-log. Controleer het configuratiebestand | vys-cookie moet worden opgegeven als de first NameTrans-richtlijn voor elke virtuele softwareserver. |

