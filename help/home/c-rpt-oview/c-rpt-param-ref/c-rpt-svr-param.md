---
description: Informatie over de parameters van Server.cfg van het Rapport.
solution: Analytics
title: Server.cfg van het rapport Parameters
topic: Data workbench
uuid: 506f30f7-c8c6-4580-8423-7da8d00b0d57
translation-type: tm+mt
source-git-commit: 6443bdf8856ba51252685fa0c1ed65f831142956

---


# Server.cfg van het rapport Parameters{#report-server-cfg-parameters}

Informatie over de parameters van Server.cfg van het Rapport.

De steekproef [!DNL Report Server.cfg] die in het [Vormen van de Verbinding aan de Server](../../../home/c-rpt-oview/c-inst-rpt/t-config-conn-ins-svr.md#task-a3ca949c43244782b658fb4437fd724c) van het Inzicht wordt getoond bevat slechts de parameters inbegrepen in het [!DNL Report Server.cfg] dossier door gebrek.

Als u de Server van de Vergunning van Adobe door een volmachtsserver contacteert, moet u de het Verlenen van vergunningen vector en zijn parameters aan toevoegen [!DNL Report Server.cfg]. Na is een voorbeeld van deze vector en zijn parameters dat u een model voor uw vector van het Verlenen van vergunningen kunt gebruiken:

```
Licensing = serverInfo:  
Proxy Address = string: ProxyIPAddress 
Proxy Password = string: ProxyPassword 
Proxy Port = int: ProxyPort 
Proxy User Name = string: ProxyUserName 
```

De volgende lijst verstrekt beschrijvingen van de [!DNL Report Server.cfg] dossierparameters:

<table id="table_9DA4A3124A9D444CBB4CBFF6FA279A42"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Parameter </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Excel-extensie </td> 
   <td colname="col2"> <p>De gesteunde uitbreidingen van Excel omvatten: </p> <p>Excel Extension = string: <span class="filepath"> .xlsx </span> </p> <p>Excel Extension = string: <span class="filepath"> .xls </span> (dit is gebrek) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Lettertypen </td> 
   <td colname="col2"> <p>Optioneel. Vector die van de doopvonten een lijst maakt die de Server van het Rapport <span class="keyword"> </span> zou moeten gebruiken om op UTF8-Gebaseerde unicode speciale karakters terug te geven. Het aantal doopvonten in de lijst is onbeperkt. </p> <p>De eerste doopvont zou altijd de Console van Lucida Sans moeten zijn. Als deze parameter niet inbegrepen in het <span class="filepath"> dossier van Server.cfg van het Rapport is, gebruikt de Server van het </span> Rapport slechts de console van de Sans van Lucida <span class="keyword"> </span> om tekst te tonen. </p> <p> <span class="keyword"> De Server van het rapport </span> gebruikt de eerste doopvont in de lijst om alle karakters terug te geven tot het een karakter ontmoet dat het niet kan teruggeven. Het gebruikt dan de tweede doopvont in de lijst om dat karakter terug te geven. Als die doopvont niet het karakter teruggeeft, <span class="keyword"> </span> gebruikt de Server van het Rapport de derde doopvont in de lijst om dat karakter terug te geven, etc., tot het het eind van de doopvontlijst bereikt. Als de correcte doopvont niet vermeld in de vector is, <span class="keyword"> toont de Server van het Rapport de hexidecimale waarde voor het karakter </span> . </p> <p> <p>Opmerking:  Breng geen veranderingen in deze parameter aan terwijl de Server van het <span class="keyword"> Rapport </span> loopt. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Gamma </td> 
   <td colname="col2"> <p> <span class="wintitle"> Gamma-instelling </span> voor <span class="filepath"> .png </span> bestandsuitvoer. De standaardwaarde is 1.6. </p> <p> <p>Opmerking:  Adobe adviseert niet veranderend deze waarde. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Licenties </td> 
   <td colname="col2"> <p>Optioneel. U moet de parameters in deze vector wijzigen slechts als u de vergunningsserver van Adobe door een volmachtsserver contacteert. </p> <p>Het herkenningsteken van de sectie voor parameters u plaatste om de vergunningsserver van Adobe door een volmachtsserver te contacteren. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Proxyadres </td> 
   <td colname="col2"> Het adres van een volmachtsserver die de Server van het Rapport <span class="keyword"> </span> moet gebruiken om tot de vergunningsserver van Adobe toegang te hebben. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Wachtwoord voor proxy </td> 
   <td colname="col2"> Optioneel. Het wachtwoord verbonden aan de Naam van de Gebruiker van de <span class="wintitle"> Volmacht </span>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Proxypoort </td> 
   <td colname="col2"> De haven van de volmachtsserver. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Gebruikersnaam proxy </td> 
   <td colname="col2"> Optioneel. De gebruikersnaam die wordt gebruikt om tot de volmachtsserver toegang te hebben. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Netwerklocatie </td> 
   <td colname="col2"> De netwerkplaats die de Server van het Rapport <span class="keyword"> </span> gebruikt om de gemeenschappelijke naam van de server aan een IP adres op te lossen. De plaatsen van het netwerk worden bepaald in het adresdossier dat in de folder van Adressen op de de servermachine van de gegevenswerkbank wordt gevestigd. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Servers </td> 
   <td colname="col2"> <p>Het herkenningsteken van de sectie voor parameters u plaatste om te vormen welke server van het <span class="keyword"> Rapport van de werkbankserver Server </span> moet verbinden om rapporten te produceren. Dit omvat een aantal erop wijst dat hoeveel punten in deze vector vermeld zijn. </p> <p>Voor elke server, voeg een serverInfo ingang toe en voltooi zonodig de parameters. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Adres </td> 
   <td colname="col2"> IP adres van de de servermachine van de gegevenswerkbank waaraan de Server van het <span class="keyword"> Rapport </span> moet verbinden om rapporten te produceren. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Naam </td> 
   <td colname="col2"> De naam die de Server van het Rapport intern <span class="keyword"> </span> gebruikt om de server van de gegevenswerkbank te identificeren. Dit is eenvoudig een intern etiket, zodat kunt u om het even welke naam gebruiken u houdt van. Voor consistentie, stellen wij voor dat u de gemeenschappelijke naam gebruikt zoals die op het digitale certificaat van de server wordt vermeld. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Poort </td> 
   <td colname="col2"> Haven waardoor de Server van het <span class="keyword"> Rapport met de server van de gegevenswerkbank </span> communiceert. Voor veilige verbindingen, is deze waarde gewoonlijk 443. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Proxyadres </td> 
   <td colname="col2"> Het adres van een volmachtsserver die de Server van het <span class="keyword"> Rapport </span> moet gebruiken om tot de server van de gegevenswerkbank toegang te hebben. Deze parameter is nodig slechts wanneer een volmachtsserver wordt vereist om met uw servermachines te verbinden. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Wachtwoord voor proxy </td> 
   <td colname="col2"> Het wachtwoord aan de volmachtsserver. Deze parameter is nodig slechts wanneer een volmachtsserver wordt vereist om met uw de servermachines van de gegevenswerkbank te verbinden. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Proxypoort </td> 
   <td colname="col2"> De haven van de volmachtsserver. De standaardwaarde is 8080. Deze parameter is nodig slechts wanneer een volmachtsserver wordt vereist om met uw de servermachines van de gegevenswerkbank te verbinden. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Gebruikersnaam proxy </td> 
   <td colname="col2"> De gebruikersnaam aan de volmachtsserver. Deze parameter is nodig slechts wanneer een volmachtsserver wordt vereist om met uw de servermachines van de gegevenswerkbank te verbinden. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> SSL-clientcertificaat </td> 
   <td colname="col2"> Naam van het SSL certificaatdossier voor het <span class="keyword"> systeem van de Server van het Rapport </span> . </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Algemene naam van SSL-server </td> 
   <td colname="col2"> <span class="wintitle"> De Gemeenschappelijke Naam van de server </span> die op het digitale certificaat van de server van de gegevenswerkbank wordt vermeld. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> SSL gebruiken </td> 
   <td colname="col2"> Wijst erop of SSL voor veilige communicatie tussen de server van de gegevenswerkbank en de Server van het <span class="keyword"> Rapport wordt gebruikt </span>. De opties zijn waar of vals. De standaardwaarde is waar. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Geheugenlimiet resultaat (KB) </td> 
   <td colname="col2"> <p>De hoeveelheid geheugen (in KB) die u voor rapporten en alarm beschikbaar wilt stellen. De standaardwaarde is 50000. </p> <p>Wanneer het runnen van rapporten, controleert de Server van het <span class="keyword"> </span> Rapport eerst deze waarde, dan controleert de waarde in de Maximum parameter van de Grootte van de Plak. Bijvoorbeeld, als u deze parameter aan 50.000 en de MaximumGrootte van de Plak aan 50 plaatst, <span class="keyword"> </span> stelt de Server van het Rapport slechts 50 werkruimten tegelijkertijd in werking zelfs als de ruimte beschikbaar is om meer werkruimten in werking te stellen. </p> <p> <p>Opmerking:  Deze grens zou nooit de waarde moeten overschrijden die in de parameter van de Limiet van het Geheugen van de Vraag van de server van de gegevenswerkbank wordt geplaatst, en, idealiter, zou een weinig lager dan de Grens van het Geheugen van de <span class="wintitle"> Vraag moeten worden geplaatst </span> om wat ruimte aan andere gebruikers te verstrekken die rapporten kunnen tezelfdertijd in werking stellen. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Maximale schuifgrootte </td> 
   <td colname="col2"> Het maximumaantal rapportwerkruimten dat de Server van het <span class="keyword"> Rapport in één keer </span> kan lopen. De standaardwaarde is 50. Voor meer informatie over hoe de Server van het <span class="keyword"> Rapport dit het plaatsen </span> gebruikt, zie de de parameterbeschrijving van het Geheugen van het <span class="wintitle"> Resultaat (KB) </span> . </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Software bijwerken </td> 
   <td colname="col2"> <p>Wijst erop of om de software van deze <span class="keyword"> </span> Server van Rapport toe te staan om door de server van de gegevenswerkbank worden bijgewerkt. De opties zijn waar of vals. De standaardwaarde is waar. </p> <p>Na is een voorbeeld van deze parameter dat u een model kunt gebruiken: </p> <p> <code> Update&amp;nbsp;Software&amp;nbsp;=&amp;nbsp;bool:&amp;nbsp;false </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> OpenGL Hardware Rendering gebruiken </td> 
   <td colname="col2"> <p>Controleert of de Server van het <span class="keyword"> Rapport hardware </span> gebruikt teruggevend (zoals de de grafiekkaart van de machine) om rapportoutput te veroorzaken. De opties zijn waar of vals. De standaardwaarde is waar. </p> <p>Deze parameter zou aan vals moeten worden geplaatst slechts wanneer u problemen met uw grafiekkaart ervaart. Wanneer de reeks aan vals, <span class="keyword"> probeert de Server van het Rapport </span> niet om hardware terug te geven te gebruiken en software gebruikt die door gebrek teruggeeft. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Rapportage </td> 
   <td colname="col2"> Het herkenningsteken van de sectie voor parameters u plaatst om het melden te vormen. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Interval van het Bericht van de voltooiing </td> 
   <td colname="col2"> <p>De frequentie (in seconden) waarmee de <span class="keyword"> Server van het Rapport de berichten van de </span> voltooiingsstatus drukt wanneer de vragen tijdens rapport of waakzame generatie in werking worden gesteld. De standaardwaarde is 120 seconden. </p> <p>Voorbeeld: De vragen van de werkruimte zijn 62.145672% volledig. </p> <p>De berichten van de voltooiing worden geschreven aan <span class="filepath"> reportserver.log </span> en zijn synched aan de server. Dit het plaatsen controleert de <span class="filepath"> status.txt </span> - dossiers die heen en weer voor elke rapportreeks worden verzonden, zodat de percenten volledig met duimnagels kunnen worden getoond. De berichten worden verzonden wanneer een rapportreeks voltooit of wanneer het interval wordt bereikt, welke eerst komt. Het plaatsen van dit hoger beïnvloedt niet het tarief waaraan u rapport ziet dat in de cliëntinterface door de duimnagels wordt geproduceerd, maar beïnvloedt hoeveel tussentijdse berichten u ziet. Het specificeren van een lage waarde kan het systeem veroorzaken om een grote hoeveelheid tijd door te brengen die gegevens synchroniseert, omdat het gegeven van de server van de Server van het <span class="keyword"> Rapport aan het profiel, over alle DPUs en aan alle verbonden cliënten synchroon is telkens als een </span> status.txt <span class="filepath"> </span> - bericht verandert. </p> <p>Het systeem verzendt altijd een <span class="filepath"> status.txt </span> - dossier wanneer een rapportreeks, ongeacht het plaatsen van deze configuratieparameter voltooit. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Profielen </td> 
   <td colname="col2"> <p>Aantal erop wijst dat hoeveel punten in deze vector vermeld zijn. Voor elk profiel waarvoor rapporten moeten worden gemaakt, voegt u een item <span class="wintitle"> ReportProfile </span> toe aan de vector Profielen en vult u de parameters Server en Profiel in. </p> <p> <span class="wintitle"> Server </span> - de naam die de Server van het <span class="keyword"> Rapport intern </span> gebruikt om de server van de gegevenswerkbank te identificeren. Deze naam moet de server gemeenschappelijke naam zijn die op SSL certificaat van de server van de gegevenswerkbank wordt vermeld. </p> <p> <span class="wintitle"> Profiel </span> - Naam van het profiel waarvoor rapporten moeten worden gemaakt. Deze naam moet het genoemde profiel op het de serversysteem van de gegevenswerkbank aanpassen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> SMTP-server voor fouten </td> 
   <td colname="col2"> <p>Het adres van de server SMTP waarvan u de fouten van de Server van het <span class="wintitle"> </span> Rapport via e-mail wilt verzenden. </p> <p>Voorbeeld: <span class="filepath"> mail.mycompany.com </span> </p> <p>Een server SMTP wordt vereist voor gebruik van de beschreven mogelijkheden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> SMTP-server voor foutwachtwoord </td> 
   <td colname="col2"> <p>Het wachtwoord voor het programma openen aan server SMTP. Deze parameter is facultatief tenzij login wordt vereist om post te verzenden. </p> <p>Een server SMTP wordt vereist voor gebruik van de beschreven mogelijkheden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> SMTP-server voor fouten die worden verzonden van </td> 
   <td colname="col2"> Het e-mailadres waarvan u de fouten van de Server van het <span class="wintitle"> Rapport wilt verzenden </span> . </td> 
  </tr> 
  <tr> 
   <td colname="col1"> SMTP-server voor fouten die worden verzonden naar </td> 
   <td colname="col2"> <p>Het (de) e-mailadres(sen) waarnaar waarschuwingen worden verzonden. </p> <p>Voorbeeld: <span class="filepath"> adm1@company.com,adm2@company.com </span> </p> <p>Een server SMTP wordt vereist voor gebruik van de beschreven mogelijkheden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> SMTP-server voor Foutengebruikersnaam </td> 
   <td colname="col2"> <p>De gebruikersnaam voor het programma openen aan de server SMTP. Deze parameter is facultatief tenzij login wordt vereist om post te verzenden. </p> <p>Een server SMTP wordt vereist voor gebruik van de beschreven mogelijkheden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Statusinterval </td> 
   <td colname="col2"> <p>De frequentie (in seconden) waarmee de Server van het <span class="wintitle"> Rapport </span> produceert en statusinformatie naar de server van de gegevenswerkbank verzendt die in Gedetailleerde Status moet worden getoond <span class="wintitle"> </span>. </p> <p>De standaardwaarde is 120 seconden. Het wordt niet geadviseerd om dit aan een kleine waarde, zoals twee minuten te plaatsen, omdat een rapporteringsrij uren kan vergen te lopen. In dat geval, zou u het plaatsen van 600 tot 1200 seconden kunnen overwegen. </p> <p>Voor meer informatie over <span class="wintitle"> Gedetailleerde Status </span>, zie het Administratieve hoofdstuk van Interfaces van de Gids van de Gebruiker van het <a href="https://docs.adobe.com/content/help/en/data-workbench/using/client/admin-ui/c-admin-intrf.html" format="http" scope="external"> Inzicht </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Interval bijwerken </td> 
   <td colname="col2"> <p>De frequentie (in notulen) waarmee de Server van het <span class="keyword"> Rapport alle profielen </span> controleert die in de vector van Profielen voor nieuwe rapporten en alarm worden vermeld. De standaardwaarde is 10 minuten. </p> <p>De tijd die u specificeert is verdeeld onder alle vermelde profielen. Bijvoorbeeld, als uw interval aan 10 minuten wordt geplaatst en u twee profielen controleert, wordt elk profiel gecontroleerd 5 minuten. Als een profiel wordt gecontroleerd wanneer een nieuw of gewijzigd rapport of een alarm aan het profiel wordt bewaard, is het rapport of het alarm onmiddellijk beschikbaar voor generatie. </p> <p>Als het Interval van de <span class="wintitle"> Update </span> wordt gevormd om meer dan één profiel te controleren, is het belangrijk dat dit het plaatsen hoog genoeg is om alle profielen binnen de gevormde tijd te laden. In systemen met vele grote gevormde afmetingen, bijvoorbeeld, waar het verscheidene notulen zou kunnen vergen om de aanvankelijke gegevensverbinding met alle elementennamen terug te winnen, moet dit het plaatsen lang genoeg zijn voor die volledige synchronisatie om voor te komen. Anders, geeft het systeem een fout van de profielsynch uit. </p> </td> 
  </tr> 
 </tbody> 
</table>

