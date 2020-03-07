---
description: De sensor verwerft alle meetgegevens die op de paginaverzoeken (GET verzoeken) worden gedragen die aan de Webservers worden gemaakt waarop het is geïnstalleerd.
solution: Analytics
title: Gegevens voor het aanvragen van pagina's ophalen
topic: Data workbench
uuid: 06cf2b14-8d2c-483e-8a75-ce772798978f
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Gegevens voor het aanvragen van pagina&#39;s ophalen{#acquiring-page-request-data}

De sensor verwerft alle meetgegevens die op de paginaverzoeken (GET verzoeken) worden gedragen die aan de Webservers worden gemaakt waarop het is geïnstalleerd.

[!DNL Sensor] verwerft deze meetgegevens door de toepassing van de Webserver programmeringsinterface, direct van de instantie of de instanties van de software die van de Webserver op uw Webserver loopt. [!DNL Sensor] heeft geen toegang tot de Webserver geproduceerde logboekdossiers. In feite, nadat [!DNL Sensor] en de server van de gegevenswerkbank is geïnstalleerd en getest, kan de inheemse registrereneigenschap van de Webserver worden onbruikbaar gemaakt zonder gegevensinzameling te beïnvloeden. In veel gevallen, verbetert het onbruikbaar maken van het registreren van dossiers aan de lokale schijven van de machines van de Webserver zelf de pagina dienend capaciteit van die Webservers wegens de vrij grote hoeveelheid vaste schijf I/O die wordt vereist om deze informatie aan de lokale schijf van de machine van de Webserver te registreren.

[!DNL Sensor] verzamelt direct gegevens voor meting en webverzoeken van elk webserverproces en virtuele webserverprocessen (indien van toepassing) en schrijft de gegevens tijdelijk naar een wachtrijbestand, een fouttolerante geheugenwachtrij met vaste schijfback-ups, op de webservermachine. De dienst van de Transmitter van de Sensor (of daemon afhankelijk van het platform) wint gegevens van het Dossier van de Rij terug en comprimeert en codeert het dan alvorens het aan de server van de gegevenswerkbank voor opslag op lange termijn over te brengen. Met [!DNL Sensor], wordt het gegeven geaccumuleerd op uw machines van de Webserver in het Dossier van de Rij slechts als u een netwerk of ander probleem hebt dat zijn transmissie verhindert. Het dossier van de Rij staat voor de efficiënte lokale opslag van uren tot dagen van de gegevens van het Webverzoek toe om de gegevens te beschermen als een netwerk of systeemfout niet de gegevens om aan de server van de gegevenswerkbank in echt - tijd toelaat worden overgebracht.

[!DNL Sensor] verzamelt meetgegevens van elk fysiek en logisch proces van de Webserver, filters het door inhoudstype, perst het samen, codeert het, en stromen het aan de server van de gegevenswerkbank.

De volgende lijst bevat de gebieden van logboekinformatie die door [!DNL Sensor] voor elk GET verzoek worden verworven dat niet wordt gefiltreerd uit gebaseerd op [!DNL Sensor’s] configuratiedossier:

<table id="table_5F65474150EC41648B35D0B031FB9B15"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> W3C-naam </th> 
   <th colname="col2" class="entry"> Verzamelde gegevens </th> 
   <th colname="col3" class="entry"> Toelichting </th> 
   <th colname="col4" class="entry"> Toelichting </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> x-trackingid </td> 
   <td colname="col2"> Tracking Identifier (unieke bezoeker) </td> 
   <td colname="col3"> Herkenningsteken dat van een koekje wordt gelezen dat in browser van de gebruiker door <span class="wintitle"> </span> Sensor op het aanvankelijke verzoek van de Bezoeker wordt geplaatst </td> 
   <td colname="col4"> V1st=3C94007B4E01F9C2 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Datum </p> <p>Tijd </p> </td> 
   <td colname="col2"> Tijdstempel </td> 
   <td colname="col3"> Tijdstip waarop het verzoek door server (bij precisie 100ns werd verwerkt; nauwkeurigheid hangt van servermilieu en NTP af) </td> 
   <td colname="col4"> 2002-11-21 17:21:45.123 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> SC (inhoudstype) </td> 
   <td colname="col2"> Content type </td> 
   <td colname="col3"> Type voorwerp dat van server is teruggekeerd </td> 
   <td colname="col4"> tekst/html </td> 
  </tr> 
  <tr> 
   <td colname="col1"> SC-status </td> 
   <td colname="col2"> HTTP-responsstatuscode </td> 
   <td colname="col3"> Numerieke code die door de server wordt geproduceerd die nota neemt van het statuut van de reactie van de server van HTTP </td> 
   <td colname="col4"> 404 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> cs-uri-stengel </td> 
   <td colname="col2"> URI Stem </td> 
   <td colname="col3"> Het stamgedeelte van URI dat door de cliënt wordt gevraagd </td> 
   <td colname="col4"> <span class="filepath"> pagedir/page.asp </span> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> c-ip </td> 
   <td colname="col2"> IP client </td> 
   <td colname="col3"> IP-adres van de verzoekende client </td> 
   <td colname="col4"> 127.0.0.1 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> s-dns </td> 
   <td colname="col2"> Serverdomeinnaam </td> 
   <td colname="col3"> De naam van het domein van de Webserver die het verzoek verwerkt </td> 
   <td colname="col4"> <span class="filepath"> www.domain.com </span> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> cs (referentie) </td> 
   <td colname="col2"> URL verwijzen </td> 
   <td colname="col3"> Inhoud van het de verwijzingsgebied van HTTP dat door de cliënt wordt verzonden </td> 
   <td colname="col4"> <span class="filepath"> http://www.referringsite.com </span> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> cs (gebruikersagent) </td> 
   <td colname="col2"> Gebruikersagent </td> 
   <td colname="col3"> Apparaat dat wordt gebruikt om een verzoek aan de server van HTTP in te dienen </td> 
   <td colname="col4"> Mozilla/4.0+(compatibel;+MSIE+6.0; +Windows+NT+5.1) </td> 
  </tr> 
  <tr> 
   <td colname="col1"> cs (cookie) </td> 
   <td colname="col2"> Clientcookies van domein </td> 
   <td colname="col3"> Inhoud van alle koekjes van de gebruiker voor de plaats </td> 
   <td colname="col4"> <p>KL_TC1 1038058778312 </p> <p>KL972x1038058778312282052 </p> <p>KL_PVKL972 0 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> cs-uri-query </td> 
   <td colname="col2"> Query-tekenreeks </td> 
   <td colname="col3"> Het gedeelte van het vraagkoord, als om het even welk, van URI gevraagd door de cliënt </td> 
   <td colname="col4"> PAGENAME=dynamic1&amp;link=3001 </td> 
  </tr> 
 </tbody> 
</table>

