---
description: Informatie over de parameters van Server.cfg van het Rapport.
title: Server.cfg-parameters rapporteren
uuid: 506f30f7-c8c6-4580-8423-7da8d00b0d57
exl-id: 339e4219-ff4d-4df6-b45a-7144927a843b
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '1683'
ht-degree: 0%

---

# Server.cfg-parameters rapporteren{#report-server-cfg-parameters}

{{eol}}

Informatie over de parameters van Server.cfg van het Rapport.

Het voorbeeld [!DNL Report Server.cfg] getoond in [De verbinding met Insight Server configureren](../../../home/c-rpt-oview/c-inst-rpt/t-config-conn-ins-svr.md#task-a3ca949c43244782b658fb4437fd724c) bevat alleen de parameters die zijn opgenomen in de [!DNL Report Server.cfg] bestand standaard.

Als u via een proxyserver contact opneemt met de Adobe-licentieserver, moet u de licentievector en de bijbehorende parameters toevoegen aan de [!DNL Report Server.cfg]. Hieronder ziet u een voorbeeld van deze vector en de bijbehorende parameters die u kunt gebruiken als model voor uw licentievector:

```
Licensing = serverInfo:  
Proxy Address = string: ProxyIPAddress 
Proxy Password = string: ProxyPassword 
Proxy Port = int: ProxyPort 
Proxy User Name = string: ProxyUserName 
```

In de volgende tabel vindt u een beschrijving van de [!DNL Report Server.cfg] bestandsparameters:

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
   <td colname="col2"> <p>Tot de ondersteunde Excel-extensies behoren: </p> <p>Excel Extension = string: <span class="filepath"> .xlsx </span> </p> <p>Excel Extension = string: <span class="filepath"> .xls </span> (dit is standaard) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Lettertypen </td> 
   <td colname="col2"> <p>Optioneel. Vector met vermelding van de lettertypen die <span class="keyword"> Rapportserver </span> moet worden gebruikt om op UTF8 gebaseerde unicode speciale karakters terug te geven. Het aantal lettertypen in de lijst is onbeperkt. </p> <p>Het eerste font moet altijd Lucida Sans Console zijn. Als deze parameter niet in de <span class="filepath"> Server.cfg rapporteren </span> bestand, <span class="keyword"> Rapportserver </span> gebruikt alleen de Lucida Sans-console om tekst weer te geven. </p> <p> <span class="keyword"> Rapportserver </span> gebruikt het eerste lettertype in de lijst om alle tekens te renderen totdat een teken wordt aangetroffen dat niet kan worden gerenderd. Vervolgens wordt het tweede lettertype in de lijst gebruikt om dat teken te renderen. Als dat lettertype het teken niet rendert, <span class="keyword"> Rapportserver </span> gebruikt het derde lettertype in de lijst om dat teken te renderen, enzovoort, totdat het einde van de lettertypenlijst is bereikt. Als het juiste lettertype niet in de vector wordt vermeld, <span class="keyword"> Rapportserver </span> geeft de hexadecimale waarde voor het teken weer. </p> <p> <p>Opmerking: Breng geen wijzigingen aan in deze parameter terwijl <span class="keyword"> Rapportserver </span> wordt uitgevoerd. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Gamma </td> 
   <td colname="col2"> <p> <span class="wintitle"> Gamma </span> instellen voor <span class="filepath"> .png </span> bestandsuitvoer. De standaardwaarde is 1,6. </p> <p> <p>Opmerking: Adobe raadt u niet aan deze waarde te wijzigen. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Licentie </td> 
   <td colname="col2"> <p>Optioneel. U moet de parameters in deze vector slechts wijzigen als u Adobe licentieserver door een volmachtsserver contacteert. </p> <p>Sectie-id voor parameters die u instelt op de Adobe-licentieserver via een proxyserver. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Proxyadres </td> 
   <td colname="col2"> Het adres van een proxyserver die <span class="keyword"> Rapportserver </span> moet worden gebruikt om toegang te krijgen tot Adobe-licentieserver. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Proxywachtwoord </td> 
   <td colname="col2"> Optioneel. Het wachtwoord dat aan de <span class="wintitle"> Gebruikersnaam proxy </span>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Proxypoort </td> 
   <td colname="col2"> De poort van de proxyserver. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Gebruikersnaam proxy </td> 
   <td colname="col2"> Optioneel. De gebruikersnaam die wordt gebruikt om toegang te krijgen tot de proxyserver. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Netwerklocatie </td> 
   <td colname="col2"> De netwerklocatie die <span class="keyword"> Rapportserver </span> gebruikt om de gemeenschappelijke naam van de server aan een IP adres op te lossen. De plaatsen van het netwerk worden bepaald in het adresdossier in de folder van Adressen op de machine van de gegevenswerkbankserver wordt gevestigd. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Servers </td> 
   <td colname="col2"> <p>Sectie-id voor parameters die u instelt om te configureren welke gegevenswerkbankservercomputers <span class="keyword"> Rapportserver </span> moet verbinding maken om rapporten te genereren. Dit omvat een getal dat aangeeft hoeveel items in deze vector worden vermeld. </p> <p>Voor elke server, voeg een serverInfo ingang toe en voltooi zonodig de parameters. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Adres </td> 
   <td colname="col2"> IP-adres van de gegevenswerkbankserver waarop <span class="keyword"> Rapportserver </span> moet verbinding maken om rapporten te genereren. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Naam </td> 
   <td colname="col2"> De naam die <span class="keyword"> Rapportserver </span> intern gebruik om de server van de gegevenswerkbank te identificeren. Dit is gewoon een intern label, dus u kunt elke gewenste naam gebruiken. Ter wille van de consistentie raden we u aan de algemene naam te gebruiken die wordt vermeld op het digitale certificaat van de server. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Poort </td> 
   <td colname="col2"> Poort waardoor <span class="keyword"> Rapportserver </span> communiceert met de server van de gegevenswerkbank. Voor veilige verbindingen, is deze waarde gewoonlijk 443. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Proxyadres </td> 
   <td colname="col2"> Het adres van een proxyserver die <span class="keyword"> Rapportserver </span> moet worden gebruikt om toegang te krijgen tot de gegevenswerkbankserver. Deze parameter is alleen nodig wanneer een proxyserver is vereist om verbinding te maken met uw servercomputers. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Proxywachtwoord </td> 
   <td colname="col2"> Het wachtwoord voor de proxyserver. Deze parameter is alleen nodig wanneer een proxyserver is vereist om verbinding te maken met uw gegevensworkbench-servercomputers. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Proxypoort </td> 
   <td colname="col2"> De poort van de proxyserver. De standaardwaarde is 8080. Deze parameter is alleen nodig wanneer een proxyserver is vereist om verbinding te maken met uw gegevensworkbench-servercomputers. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Gebruikersnaam proxy </td> 
   <td colname="col2"> De gebruikersnaam voor de proxyserver. Deze parameter is alleen nodig wanneer een proxyserver is vereist om verbinding te maken met uw gegevensworkbench-servercomputers. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> SSL-clientcertificaat </td> 
   <td colname="col2"> Naam van het SSL-certificaatbestand voor het <span class="keyword"> Rapportserver </span> machine. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Algemene naam SSL-server </td> 
   <td colname="col2"> <span class="wintitle"> Algemene naam server </span> vermeld op het digitale certificaat van de werkbankserver van gegevens. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> SSL gebruiken </td> 
   <td colname="col2"> Geeft aan of SSL wordt gebruikt voor veilige communicatie tussen de gegevenswerkbankserver en <span class="keyword"> Rapportserver </span>. De opties zijn waar of onwaar. De standaardwaarde is true. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Limiet voor resultaatgeheugen (kB) </td> 
   <td colname="col2"> <p>De hoeveelheid geheugen (in kB) die u beschikbaar wilt maken voor rapporten en waarschuwingen. De standaardwaarde is 50000. </p> <p>Wanneer rapporten worden uitgevoerd, <span class="keyword"> Rapportserver </span> Hiermee wordt eerst deze waarde gecontroleerd en vervolgens de waarde in de parameter Maximale segmentgrootte. Als u deze parameter bijvoorbeeld instelt op 50.000 en Maximale segmentgrootte op 50, <span class="keyword"> Rapportserver </span> Er worden slechts 50 werkruimten tegelijk uitgevoerd, zelfs als er ruimte beschikbaar is om meer werkruimten uit te voeren. </p> <p> <p>Opmerking: Deze grens zou nooit de waarde moeten overschrijden die in de parameter van de Limiet van het Geheugen van de Vraag van de server van de werkbank van gegevens wordt geplaatst, en, idealiter zou, iets lager dan moeten worden geplaatst <span class="wintitle"> Limiet voor vraaggeheugen </span> om enige ruimte te bieden aan andere gebruikers die rapporten tegelijk kunnen uitvoeren. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Maximale segmentgrootte </td> 
   <td colname="col2"> Het maximumaantal rapportwerkruimten dat <span class="keyword"> Rapportserver </span> kan tegelijk worden uitgevoerd. De standaardwaarde is 50. Voor meer informatie over hoe <span class="keyword"> Rapportserver </span> gebruikt deze instelling, raadpleegt u de <span class="wintitle"> Limiet voor resultaatgeheugen (kB) </span> parameterbeschrijving. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Software bijwerken </td> 
   <td colname="col2"> <p>Geeft aan of dit is toegestaan <span class="keyword"> Rapportserver </span> software die door de gegevenswerkbankserver moet worden bijgewerkt. De opties zijn waar of onwaar. De standaardwaarde is true. </p> <p>Hieronder ziet u een voorbeeld van deze parameter waarmee u een model kunt gebruiken: </p> <p> <code> Update&amp;nbsp;Software&amp;nbsp;=&amp;nbsp;bool:&amp;nbsp;false </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> OpenGL-hardwarerendering gebruiken </td> 
   <td colname="col2"> <p>Bepaalt of <span class="keyword"> Rapportserver </span> gebruikt hardwarerendering (zoals de grafische kaart van de computer) om rapportuitvoer te produceren. De opties zijn waar of onwaar. De standaardwaarde is true. </p> <p>Deze parameter moet alleen op false worden ingesteld als er problemen optreden met de grafische kaart. Wanneer ingesteld op false, <span class="keyword"> Rapportserver </span> probeert geen hardwarerendering te gebruiken en maakt standaard gebruik van softwarerendering. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Rapportage </td> 
   <td colname="col2"> Sectie-id voor parameters die u instelt om rapportage te configureren. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Interval voor voltooiingsbericht </td> 
   <td colname="col2"> <p>De frequentie (in seconden) waarmee <span class="keyword"> Rapportserver </span> drukt de berichten van de voltooiingsstatus wanneer de vragen tijdens rapport of waakzame generatie worden in werking gesteld. De standaardwaarde is 120 seconden. </p> <p>Voorbeeld: De vragen van de werkruimte zijn 62.145672% volledig. </p> <p>Voltooiingsberichten worden naar de <span class="filepath"> reportserver.log </span> en worden gesynchroniseerd met de server. Deze instelling bepaalt de <span class="filepath"> status.txt </span> bestanden die voor elke rapportset heen en weer worden verzonden, zodat het volledige percentage met miniaturen kan worden weergegeven. De berichten worden verzonden wanneer een rapportreeks voltooit of wanneer het interval wordt bereikt, welke eerst komt. Het plaatsen van dit hoger beïnvloedt niet het tarief waaraan u rapport dat in de cliëntinterface door de duimnagels wordt geproduceerd ziet, maar beïnvloedt hoeveel tussentijdse berichten u ziet. Door een lage waarde op te geven, kan het systeem veel tijd besteden aan het synchroniseren van gegevens, omdat gegevens worden gesynchroniseerd van <span class="keyword"> Rapportserver </span> server aan het profiel, over alle DPUs en aan alle verbonden cliënten telkens als <span class="filepath"> status.txt </span> berichtwijzigingen. </p> <p>Het systeem verzendt altijd een <span class="filepath"> status.txt </span> dossier wanneer een rapportreeks, ongeacht het plaatsen van deze configuratieparameter voltooit. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Profielen </td> 
   <td colname="col2"> <p>Getal dat aangeeft hoeveel items in deze vector worden vermeld. Voor elk profiel waarvoor rapporten moeten worden gemaakt, voegt u een <span class="wintitle"> ReportProfile </span> in de vector Profielen en voer de parameters Server en Profiel in. </p> <p> <span class="wintitle"> Server </span> - De naam die <span class="keyword"> Rapportserver </span> intern gebruik om de server van de gegevenswerkbank te identificeren. Deze naam moet de algemene servernaam zijn die wordt vermeld op het SSL-certificaat van de gegevenswerkbankserver. </p> <p> <span class="wintitle"> Profiel </span> - Naam van het profiel waarvoor rapporten moeten worden gemaakt. Deze naam moet overeenkomen met het benoemde profiel op de computer met de gegevenswerkbankserver. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> SMTP-server voor fouten </td> 
   <td colname="col2"> <p>Het adres van de server SMTP waarvan u wilt verzenden <span class="wintitle"> Rapportserver </span> fouten via e-mail. </p> <p>Voorbeeld: <span class="filepath"> mail.mijnbedrijf.com </span> </p> <p>Een server SMTP wordt vereist voor gebruik van de beschreven mogelijkheden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> SMTP-server voor foutwachtwoord </td> 
   <td colname="col2"> <p>Het wachtwoord voor het aanmelden bij de SMTP-server. Deze parameter is optioneel, tenzij aanmelding vereist is om e-mail te verzenden. </p> <p>Een server SMTP wordt vereist voor gebruik van de beschreven mogelijkheden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> SMTP-server voor fouten die worden verzonden vanaf </td> 
   <td colname="col2"> Het e-mailadres waaruit u wilt verzenden <span class="wintitle"> Rapportserver </span> fouten. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> SMTP-server voor fouten die worden verzonden naar </td> 
   <td colname="col2"> <p>Het e-mailadres of de e-mailadressen waarnaar waarschuwingen worden verzonden. </p> <p>Voorbeeld: <span class="filepath"> adm1@company.com,adm2@company.com </span> </p> <p>Een server SMTP wordt vereist voor gebruik van de beschreven mogelijkheden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> SMTP-server voor gebruikersnaam fouten </td> 
   <td colname="col2"> <p>De gebruikersnaam voor het aanmelden bij de SMTP-server. Deze parameter is optioneel, tenzij aanmelding vereist is om e-mail te verzenden. </p> <p>Een server SMTP wordt vereist voor gebruik van de beschreven mogelijkheden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Statusinterval </td> 
   <td colname="col2"> <p>De frequentie (in seconden) waarmee <span class="wintitle"> Rapportserver </span> genereert en verzendt statusinformatie naar de gegevenswerkbankserver die wordt weergegeven in <span class="wintitle"> Gedetailleerde status </span>. </p> <p>De standaardwaarde is 120 seconden. Het wordt afgeraden dit op een kleine waarde in te stellen, bijvoorbeeld op twee minuten, omdat een rapportwachtrij uren kan duren. In dat geval kunt u een instelling van 600 tot 1200 seconden overwegen. </p> <p>Meer informatie over <span class="wintitle"> Gedetailleerde status </span>, zie het hoofdstuk Administratieve Interfaces van <a href="https://experienceleague.adobe.com/docs/data-workbench/using/client/admin-ui/c-admin-intrf.html" format="http" scope="external"> Gebruikershandleiding voor Inzicht </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Interval bijwerken </td> 
   <td colname="col2"> <p>De frequentie (in minuten) waarmee <span class="keyword"> Rapportserver </span> Hiermee controleert u alle profielen die worden vermeld in de profielvector op nieuwe rapporten en waarschuwingen. De standaardwaarde is 10 minuten. </p> <p>De tijd die u opgeeft, wordt verdeeld over alle vermelde profielen. Als uw interval bijvoorbeeld is ingesteld op 10 minuten en u twee profielen controleert, wordt elk profiel vijf minuten bewaakt. Als een profiel wordt gecontroleerd wanneer een nieuw of gewijzigd rapport of een alarm aan het profiel wordt opgeslagen, is het rapport of de alarm onmiddellijk beschikbaar voor generatie. </p> <p>Als de <span class="wintitle"> Interval bijwerken </span> is geconfigureerd om meerdere profielen te controleren, is het belangrijk dat deze instelling hoog genoeg is om alle profielen binnen de geconfigureerde tijd te laden. In systemen met vele grote gevormde dimensies, bijvoorbeeld, waar het verscheidene notulen zou kunnen vergen om de aanvankelijke gegevensverbinding met alle elementennamen terug te winnen, moet dit het plaatsen lang genoeg zijn voor die volledige synchronisatie om voor te komen. Anders geeft het systeem een profielsynchronisatiefout weer. </p> </td> 
  </tr> 
 </tbody> 
</table>
