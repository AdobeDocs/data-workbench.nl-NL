---
description: Informatie over recordvelden voor basislijngebeurtenissen, zoals vastgelegd door de sensor.
title: Gegevensrecordvelden basislijngebeurtenis
uuid: aa36d332-089c-4ae2-98e2-a93d2fa023b7
exl-id: ad3d8806-863a-4871-a35b-6680163f00ac
source-git-commit: 79981e92dd1c2e552f958716626a632ead940973
workflow-type: tm+mt
source-wordcount: '461'
ht-degree: 0%

---

# Gegevensrecordvelden basislijngebeurtenis{#baseline-event-data-record-fields}

Informatie over recordvelden voor basislijngebeurtenissen, zoals vastgelegd door de sensor.

<table id="table_E29606BB010E4DB48C463979B7BEC769">
 <thead>
  <tr>
   <th colname="col1" class="entry"> Veld </th>
   <th colname="col2" class="entry"> Beschrijving </th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td colname="col1"> c-ip </td>
   <td colname="col2"> <p>Het IP-adres van de client, zoals opgenomen in het verzoek aan de server. </p> <p>Voorbeeld: 207 68 146,68 </p> </td>
  </tr>
  <tr>
   <td colname="col1"> cs(cookie) </td>
   <td colname="col2"> <p>De cookies die door de client met de aanvraag worden verzonden. </p> <p>Voorbeeld: v1st=42FDF66DE610CF36; ASPSESSIONIDQCATDAQC=GPIBKEIBFIPLOJMKCAAEPM; </p> </td>
  </tr>
  <tr>
   <td colname="col1"> cs(referentie) </td>
   <td colname="col2"> <p>De tekenreeks van de HTTP-referentie die door de client bij de aanvraag naar de server is verzonden. </p> <p>Voorbeeld: https://www.mysite.net/cgi-bin/websearch?qry </p> <p>Als u paginatags gebruikt, is cs(reference) de volledige URL van het document met de tagafbeelding, inclusief HTTP of HTTP. </p> <p>Ook, kunt u Apache (1.3, 2.0, en 2.2) en sensoren vormen IIS om de haven te vangen die voor het verzoek wordt gebruikt, die HTTP tegenover HTTPS verzoeken kan identificeren. </p> </td>
  </tr>
  <tr>
   <td colname="col1"> cs (user-agent) </td>
   <td colname="col2"> <p>De tekenreeks die door de client met zijn verzoek naar de server wordt verzonden en die aangeeft welk type gebruikersagent de client is. </p> <p>Voorbeeld: Mozilla/5.0 (Windows; U; Windows NT 5.1; en-US; rv:1.7) Gecko/20040707 Firefox/0.9.2 </p> </td>
  </tr>
  <tr>
   <td colname="col1"> cs-method </td>
   <td colname="col2"> <p>Het methodetype van het HTTP- verzoek </p> <p>Voorbeeld: GET </p> <p>Referentie: https://www.w3.org/TR/2000/NOTE-shoplogfileformat-20001115/#field_method </p> </td>
  </tr>
  <tr>
   <td colname="col1"> cs-uri-query </td>
   <td colname="col2"> <p>Het gedeelte van de querytekenreeks van URI (stem + querytekenreeks = URI) </p> <p>Dit wordt voorafgegaan door een vraagteken (?) en kan een of meer naam-waardeparen bevatten die door ampersands (&amp;) worden gescheiden. </p> <p>Voorbeeld: page=homepage </p> </td>
  </tr>
  <tr>
   <td colname="col1"> cs-uri-stem </td>
   <td colname="col2"> <p>Het stamgedeelte van URI (stem + query string = URI) </p> <p>De stam is de daadwerkelijke of logische weg aan het gevraagde middel op de server. </p> <p>Voorbeeld: /index.asp </p> </td>
  </tr>
  <tr>
   <td colname="col1"> sc (inhoudstype) </td>
   <td colname="col2"> <p>Het inhoudstype van het middel dat door de cliënt wordt gevraagd zoals die door de server wordt gemeld. </p> <p>Voorbeelden: text/html, image/png, image/gif, video/mpeg </p> </td>
  </tr>
  <tr>
   <td colname="col1"> sc-bytes </td>
   <td colname="col2"> <p>Het aantal bytes aan gegevens dat door de server naar de client is verzonden als reactie op de aanvraag. </p> <p>Voorbeeld: 4996 </p> </td>
  </tr>
  <tr>
   <td colname="col1"> sc-status </td>
   <td colname="col2"> <p>De statuscode die door de server aan de client wordt geretourneerd. </p> <p>Voorbeeld: 200 </p> <p>Referentie: https://www.w3.org/Protocols/rfc2616/rfc2616-sec10.html </p> </td>
  </tr>
  <tr>
   <td colname="col1"> s-dns </td>
   <td colname="col2"> <p>Het volledig - gekwalificeerde domeinnaam of IP adres van de gastheer van het gevraagde middel. </p> <p>Voorbeeld: www.omniture.com </p> </td>
  </tr>
  <tr>
   <td colname="col1"> x-experiment </td>
   <td colname="col2"> <p>De lijst met alle gecontroleerde experimentele namen en groepen waarvan de client lid is op het moment van de aanvraag. </p> <p>Voorbeeld: Home_Exp.Group_1,registration_exp.group_2 </p> </td>
  </tr>
  <tr>
   <td colname="col1"> x-timestamp </td>
   <td colname="col2"> <p>De datum en tijd (GMT) waarop het verzoek door de server is ontvangen. </p> <p>De tijd wordt uitgedrukt als het aantal 100 nanoseconden sinds 1 januari 1600. </p> <p>Voorbeeld: 127710989320000000 zou de x-timestamp waarde voor 11:28:52.0000000 zijn op dinsdag 13 september 2005. </p> </td>
  </tr>
  <tr>
   <td colname="col1"> x-trackingid </td>
   <td colname="col2"> <p>De hexadecimale 64-bits waarde van de unieke browser-id die wordt gevonden in een permanente cookie, zoals ingesteld door een <span class="wintitle">-sensor </span> en verstrekt door de client met een aanvraag aan een server. </p> <p>Voorbeeld: 42FDF66DE610CF36 </p> </td>
  </tr>
 </tbody>
</table>

De [!DNL data workbench server] kan een aantal variabelen van de gebieden van het de verslagverslag van de basislijngebeurtenis afleiden. Voor meer informatie, zie *de Gids van de Configuratie van de Dataset*.
