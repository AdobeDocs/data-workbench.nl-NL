---
description: De sensor verwerft alle meetgegevens die worden gedragen op de paginaverzoeken (verzoeken van de GET) die aan de Webservers worden gemaakt waarop het is geïnstalleerd.
title: Aanvraaggegevens van pagina ophalen
uuid: 06cf2b14-8d2c-483e-8a75-ce772798978f
exl-id: e42566a3-d5b4-4f1a-b8cd-1ea646041101
source-git-commit: 79981e92dd1c2e552f958716626a632ead940973
workflow-type: tm+mt
source-wordcount: '575'
ht-degree: 1%

---

# Aanvraaggegevens van pagina ophalen{#acquiring-page-request-data}

De sensor verwerft alle meetgegevens die worden gedragen op de paginaverzoeken (verzoeken van de GET) die aan de Webservers worden gemaakt waarop het is geïnstalleerd.

[!DNL Sensor] Verkrijgt deze meetgegevens via de programmeerinterface van de webserver, rechtstreeks van de instantie of instanties van de webserversoftware die op uw webserver wordt uitgevoerd. [!DNL Sensor] heeft geen toegang tot de door de webserver gegenereerde logbestanden. Nadat [!DNL Sensor] en de gegevenswerkbankserver zijn geïnstalleerd en getest, kan de native logboekfunctie van de webserver worden uitgeschakeld zonder dat dit van invloed is op de gegevensverzameling. In veel gevallen, verbetert het onbruikbaar maken van het registreren van dossiers aan de lokale schijven van de machines van de Webserver zelf de pagina dienend capaciteit van die Webservers wegens de vrij grote hoeveelheid vaste schijf I/O die wordt vereist om deze informatie aan de lokale schijf van de machine van de Webserver te registreren.

[!DNL Sensor] verzamelt meet- en webaanvraaggegevens rechtstreeks van elk webserverproces en van elk virtueel webserverproces (indien van toepassing) en schrijft de gegevens tijdelijk naar een bestand in de wachtrij, een fouttolerante geheugenwachtrij met vaste schijfback-ups, op de webservercomputer. De dienst van de Transmitter van de Sensor (of daemon afhankelijk van het platform) wint gegevens van het Dossier van de Rij terug en comprimeert en codeert het dan alvorens het aan de server van de gegevenswerkbank voor langetermijnopslag over te brengen. Met [!DNL Sensor] worden gegevens alleen verzameld op uw webservercomputers in het bestand Wachtrij als u een netwerk hebt of een ander probleem dat de overdracht ervan verhindert. Het dossier van de Rij staat voor de efficiënte lokale opslag van uren aan dagen van Webverzoekgegevens toe om de gegevens te beschermen als een netwerk of systeemfout niet de gegevens toelaat om aan de server van de gegevenswerkbank in echt - tijd worden overgebracht.

[!DNL Sensor] verzamelt meetgegevens van elk fysiek en logisch proces van de Webserver, filtert het door inhoudstype, comprimeert het, codeert het, en stromen het aan de server van de gegevenswerkbank.

De volgende lijst bevat de gebieden van logboekinformatie die door [!DNL Sensor] voor elk verzoek van de GET worden verworven dat niet uit gebaseerd op [!DNL Sensor’s] configuratiedossier wordt gefilterd:

<table id="table_5F65474150EC41648B35D0B031FB9B15">
 <thead>
  <tr>
   <th colname="col1" class="entry"> W3C-naam </th>
   <th colname="col2" class="entry"> Gegevens verzameld </th>
   <th colname="col3" class="entry"> Toelichting </th>
   <th colname="col4" class="entry"> Toelichting </th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td colname="col1"> x-trackingid </td>
   <td colname="col2"> Tracking-id (unieke bezoeker) </td>
   <td colname="col3"> Identifier gelezen van een cookie die door <span class="wintitle"> Sensor </span> op eerste verzoek van bezoeker in de browser van de gebruiker is geplaatst. </td>
   <td colname="col4"> V1st=3C94007B4E01F9C2 </td>
  </tr>
  <tr>
   <td colname="col1"> <p>Datum </p> <p>Tijd </p> </td>
   <td colname="col2"> Tijdstempel </td>
   <td colname="col3"> Tijdstip waarop het verzoek door de server werd verwerkt (bij precisie 100 ns; nauwkeurigheid is afhankelijk van serveromgeving en NTP) </td>
   <td colname="col4"> 2002-11-21 17:21: </td>
  </tr>
  <tr>
   <td colname="col1"> sc (inhoudstype) </td>
   <td colname="col2"> Inhoudstype </td>
   <td colname="col3"> Type object dat door server wordt geretourneerd </td>
   <td colname="col4"> text/html </td>
  </tr>
  <tr>
   <td colname="col1"> sc-status </td>
   <td colname="col2"> HTTP Response Status Code </td>
   <td colname="col3"> Numerieke code die is gegenereerd door de server die de status van de reactie van de HTTP-server aangeeft </td>
   <td colname="col4"> 404 </td>
  </tr>
  <tr>
   <td colname="col1"> cs-uri-stem </td>
   <td colname="col2"> URI Stem </td>
   <td colname="col3"> Het stamgedeelte van de URI die door de client wordt aangevraagd </td>
   <td colname="col4"> <span class="filepath"> pagedir/page.asp  </span> </td>
  </tr>
  <tr>
   <td colname="col1"> c-ip </td>
   <td colname="col2"> Client IP </td>
   <td colname="col3"> IP-adres van de verzoekende client </td>
   <td colname="col4"> 127.0.0.1 </td>
  </tr>
  <tr>
   <td colname="col1"> s-dns </td>
   <td colname="col2"> Domeinnaam server </td>
   <td colname="col3"> Domeinnaam van de webserver die de aanvraag verwerkt </td>
   <td colname="col4"> <span class="filepath"> www.domain.com  </span> </td>
  </tr>
  <tr>
   <td colname="col1"> cs(referentie) </td>
   <td colname="col2"> URL verwijzen </td>
   <td colname="col3"> Inhoud van het veld HTTP-referentie die door de client is verzonden </td>
   <td colname="col4"> <span class="filepath"> https://www.referringsite.com  </span> </td>
  </tr>
  <tr>
   <td colname="col1"> cs (user-agent) </td>
   <td colname="col2"> User Agent </td>
   <td colname="col3"> Apparaat dat wordt gebruikt om een aanvraag bij de HTTP-server in te dienen </td>
   <td colname="col4"> Mozilla/4.0+(compatibel;+MSIE+6.0; +Windows+NT+5.1) </td>
  </tr>
  <tr>
   <td colname="col1"> cs(cookie) </td>
   <td colname="col2"> Clientcookies van domein </td>
   <td colname="col3"> Inhoud van alle cookies van de gebruiker voor de site </td>
   <td colname="col4"> <p>KL_TC1 1038058778312 </p> <p>KL972x1038058778312282052 </p> <p>KL_PVKL972 0 </p> </td>
  </tr>
  <tr>
   <td colname="col1"> cs-uri-query </td>
   <td colname="col2"> Tekenreeks query </td>
   <td colname="col3"> Het gedeelte van de querytekenreeks, indien aanwezig, van de URI die door de client wordt aangevraagd </td>
   <td colname="col4"> PAGENAME=dynamic1&amp;link=3001 </td>
  </tr>
 </tbody>
</table>
