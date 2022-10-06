---
description: Als u Sensorfouten zo snel mogelijk wilt detecteren en deze wilt herstellen voordat ze grote problemen of storingen veroorzaken, moet u regelmatig uw gebeurtenissenlogboeken controleren.
title: Bewaking van administratieve gebeurtenissen (sensor)
uuid: c43d6509-6950-4436-8d6c-be7b00664f05
exl-id: 70894074-b8aa-4f6c-87d1-d0403f4c3319
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '1093'
ht-degree: 0%

---

# Bewaking van administratieve gebeurtenissen{#monitoring-administrative-events}

{{eol}}

Als u Sensorfouten zo snel mogelijk wilt detecteren en deze wilt herstellen voordat ze grote problemen of storingen veroorzaken, moet u regelmatig uw gebeurtenissenlogboeken controleren.

**Aanbevolen frequentie:** Ten minste één uur

U kunt deze gebeurtenissen controleren met het Windows Event Viewer- of Unix Syslog-bestand en het [!DNL *.sensor-log] bestanden die standaard in het dialoogvenster [!DNL Logs] in de [!DNL Sensor] installatiemap. Deze bestanden geven aan dat er fouten optreden tijdens het verzamelen van gegevens, met name als een [!DNL Sensor] kan geen verbinding maken met het doel [!DNL data workbench server] en begint gegevens een wachtrij te maken.

## Gebeurtenissen controleren in Windows {#section-7c0443a356af4381bf22259654f5cd17}

Sensor registreert fouten aan het Logboek van de Toepassing van de Kijker van de Gebeurtenis van Vensters met een bron van &quot;Adobe.&quot;

Berichten worden, afhankelijk van hun ernst, als &quot;Informatie&quot;, &quot;Waarschuwing&quot; of &quot;Fout&quot; geregistreerd.

**De Windows Event Viewer openen**:

* Klikken **Start > Configuratiescherm > Systeembeheer > Gebeurtenisviewer**.

## Gebeurtenissen controleren op Unix {#section-5de3947891fb47ac88b7c855e545d54a}

Sensor registreert fouten aan de [!DNL syslog] daemon.

De syslog daemon schrijft foutenmeldingen aan logboekdossiers die op de regels worden gebaseerd u in uw syslog.conf- dossier specificeerde. Fouten worden geregistreerd met de markeringen &quot;LOG_DAEMON&quot; en &quot;LOG_NOTICE&quot; of &quot;LOG_ERR&quot;, afhankelijk van de ernst.

**Unix syslog openen**

Unix syslog wordt typisch gevestigd in [!DNL /var/adm/messages] of [!DNL /var/log/messages].

Blader naar de juiste locatie en open de syslog.

## Berichtindelingen {#section-a0899add30fd4b2da58a23b9e3324693}

Alle berichten van de Sensor bevatten het koord &quot;Sensor&quot;en genummerd om op het belang van het bericht te wijzen dat wordt getoond.

| Berichtnummer | Betekenis van bericht | Berichttekenreeks |
|---|---|---|
| 1 xxx | Informatief | Sensorinfo nr. |
| 2 xxx | Waarschuwing | Sensorwaarschuwing nr. |
| 3 xxx | Configuratiefout | Sensorfout nummer |
| 4xxx | Operationele fout | Sensorfout nummer |
| 5 xxx | Interne fout | Sensorfout nummer |

>[!NOTE]
>
>Waarschuwingen (2xxx) zijn momenteel niet in gebruik. Deze nummers zijn gereserveerd voor toekomstig gebruik.

Uw hulpmiddel van het netwerkbeheer kan worden geplaatst om uw berichten om de 5-10 minuten voor fouten met de &quot;Sensor&quot;bron te controleren en aangewezen personeel over kwesties te waarschuwen die interventie kunnen vereisen. U kunt ervoor kiezen het systeem alleen te controleren voor bepaalde typen gebeurtenisberichten, zoals de tekenreeks &quot;Sensor Error&quot;. U kunt ook verschillende regels toepassen op gebeurtenissen die worden voorafgegaan door de tekenreeksen &quot;Sensor Info&quot;, &quot;Sensorwaarschuwing&quot; en &quot;Sensorfout&quot;.

## Belangrijke berichten identificeren {#section-5a20f5dc18ca4012931d194db855e54e}

In uw gebeurtenislogboeken, zou u speciale aandacht aan moeten besteden en onmiddellijk om het even welke berichten betreffende rijgrootte richten.

Berichten zoals &quot; [!DNL Sensor Info 1012: Adobe disk queue is #% full]&quot; aandacht nodig.

## Reageren op Sensor-gebeurtenisberichten {#section-0004c4a169dc4a8882d9bd87dd326ad4}

Tabellen die Sensor-gebeurtenissen beschrijven en acties voorstellen voor de ondersteunde webserverplatforms.

**Alle Platforms**

<table id="table_F8835AC0AD8F43E2B4494D8D35EBC0FD"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Gebeurtenisbericht </th> 
   <th colname="col2" class="entry"> Voorgestelde actie </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Sensorinfo 1010: Sensor geïnitialiseerd. </td> 
   <td colname="col2"> Geen actie vereist. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Sensorinfo 1011: Sensor beëindigd. Totaal aantal klikken in de wachtrij ## </td> 
   <td colname="col2"> Geen actie vereist. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Sensorinfo 1012: Adobe schijfwachtrij is #% vol </td> 
   <td colname="col2"> Dit bericht wordt geregistreerd telkens als het gebruik van de schijfrij een drempel van 10% kruist. Als dit percentage blijft groeien, zou de actie moeten worden ondernomen alvorens de rij volledig is en de gegevens worden verloren. Het meest waarschijnlijke probleem is dat de Sensor gestopt is met het communiceren met de Server van het Inzicht. Neem contact op met de Adobe ClientCare. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Sensorinfo 1013: Sensorconfiguratie gewijzigd </td> 
   <td colname="col2"> Geen actie vereist. De sensor heeft een wijziging in een van de configuratiebestanden gedetecteerd en zal deze opnieuw laden. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Sensorinfo 1014: Probleem met het zaaien van een willekeurige-getalgenerator </td> 
   <td colname="col2"> Neem contact op met de Adobe ClientCare. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Sensorinfo 1016: Naam van configuratiebestand geladen </td> 
   <td colname="col2"> Geen actie vereist. De sensor heeft het vermelde configuratiebestand geladen. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Sensorinfo 1017: Naam van experimenteel bestand is geladen </td> 
   <td colname="col2"> Geen actie vereist. De sensor heeft het vermelde experimentele bestand geladen. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Sensorfout 3016: Kan configuratiebestand /mypath/mijnbestand niet laden </td> 
   <td colname="col2"> Bevestig dat het Sensor-configuratiebestand dat is opgegeven in de configuratie van de webserver, bestaat en over de vereiste machtigingen beschikt om door het webserverproces te worden gelezen. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Sensor 3017: Kan het gecontroleerde configuratiebestand voor experimenten /mypath/myfile niet laden </p> </td> 
   <td colname="col2"> <p>Bevestig dat het gecontroleerde experimentele bestand dat in txlogd.conf is opgegeven, bestaat en dat het tekstproces de benodigde machtigingen heeft om het bestand te lezen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Sensorfout 3018: Kan lijsten met inhoudsfilters niet parseren. Configuratiebestand van tekstveld controleren </td> 
   <td colname="col2"> Controleer de syntaxis van de vermeldingen ContentFilterInclude en ContentFilterExclude in txlogd.conf. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Sensorfout 3023: Failed to create lock (g_lockThrottle) </td> 
   <td colname="col2"> Neem contact op met de Adobe ClientCare. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Sensorfout 3024: Failed to create lock (g_lockConfigCheck) </td> 
   <td colname="col2"> Neem contact op met de Adobe ClientCare. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Sensorfout 4014: Kan de schijfwachtrij niet openen. </td> 
   <td colname="col2"> Controleer de bestandsnaam van het bestand QueueFile in txlogd.conf en neem contact op met Adobe ClientCare als dit correct wordt geacht. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Sensorfout 4020: Geen wachtrij-bestand </td> 
   <td colname="col2"> Controleer de bestandsnaam van het bestand QueueFile in txlogd.conf en neem contact op met Adobe ClientCare als dit correct wordt geacht. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Sensorfout 4021: Wachtrij is vol </td> 
   <td colname="col2"> Neem contact op met de Adobe ClientCare. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Sensorfout 4022: Kan geheugenblok met lengte niet toewijzen &lt;x&gt; bij offset &lt;y&gt; </td> 
   <td colname="col2"> Neem contact op met de Adobe ClientCare. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Sensorfout 5012: Kan mutex niet maken. </td> 
   <td colname="col2"> Neem contact op met de Adobe ClientCare. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Sensorfout 5013: Kan mutex niet ophalen. </td> 
   <td colname="col2"> Neem contact op met de Adobe ClientCare. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Sensorfout 5030: Forkfout met spinnervork. </td> 
   <td colname="col2"> Neem contact op met de Adobe ClientCare. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Sensorfout 5031: set failed. </td> 
   <td colname="col2"> Neem contact op met de Adobe ClientCare. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Sensorfout 5032: Forkfout met spinnervork. </td> 
   <td colname="col2"> Neem contact op met de Adobe ClientCare. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Sensorfout 5033: chdir failed. </td> 
   <td colname="col2"> Neem contact op met de Adobe ClientCare. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Sensorfout 5034: Signaal ontvangen </td> 
   <td colname="col2"> Het programma werd waarschijnlijk geëindigd door een extern signaal. Als de bron van dit signaal niet kan worden bepaald, contacteer Adobe ClientCare. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Sensorfout 5035: Afsluiten aangeroepen vanuit externe hoofdmap </td> 
   <td colname="col2"> Neem contact op met de Adobe ClientCare. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Sensorfout 5036: txlogd is al gestart </td> 
   <td colname="col2"> Er is al een andere instantie van de sxlogd daemon actief. Stop eerst de andere instantie als u een nieuwe wilt uitvoeren. </td> 
  </tr> 
 </tbody> 
</table>

**Apache/IBM HTTP Server**

| Gebeurtenisbericht | Voorgestelde actie |
|---|---|
| Sensorfout 3015: De VisualSciencesConfig richtlijn mist van httpd.conf. | Dit is een configuratiefout. De richtlijn VisualSciencesConfig moet in httpd.conf met een parameter zijn die de plaats van txlogd.conf is. |
| Sensorfout 3019: vys-cookie is niet aangeroepen vóór vys-log. Neem contact op met de technische ondersteuning. | Neem contact op met de Adobe ClientCare. |
| Sensorfout 3025: Subaanvraag verwijst terug naar zichzelf | Neem contact op met de Adobe ClientCare. |

**AOL-server**

| Gebeurtenisbericht | Voorgestelde actie |
|---|---|
| Sensorfout 3015: ns/server/[server]/module/[module] ontbreekt in het configuratiebestand van AOLServer. | Dit is een configuratiefout. Correct zoals aangegeven in fout. |
| Sensorfout 3019: vys-cookie is niet aangeroepen vóór vys-log. Neem contact op met de technische ondersteuning. Neem contact op met de Adobe ClientCare. | Neem contact op met de technische ondersteuning. Neem contact op met de Adobe ClientCare. |
| Sensorfout 3020: VisualSciencesConfig ontbreekt als eerste item in [sectie] in het configuratiebestand van AOLServer. | Dit is een configuratiefout. Correct zoals aangegeven in fout. |
| Sensorfout 3021: VisualSciencesConfig mist een waarde in [sectie] in het configuratiebestand van AOLServer. | Dit is een configuratiefout. Correct zoals aangegeven in fout. |

**iPlanet- en Java System Web Servers**

| Gebeurtenisbericht | Voorgestelde actie |
|---|---|
| Sensorfout 3011: Init-instructie vereist. Bijvoorbeeld Init fn=vys-init config-file=&quot;/mypath/myfile&quot; | Dit is een configuratiefout. De iPlanet init-richtlijn ontbreekt. |
| Sensorfout 3015: config-file is niet gespecificeerd in de richtlijn van de Inzet van iPlanet | Dit is een configuratiefout. Het pad naar het configuratiebestand is niet opgegeven in de iPlanet Init-instructie. |
| Sensorfout 3019: vys-cookie is niet aangeroepen vóór vys-log. Controleer het configuratiebestand | vys-koekje moet als eerste NameTrans richtlijn voor elke software virtuele server worden gespecificeerd. |
