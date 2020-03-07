---
description: Informatie over de recordvelden van de basisgebeurtenis, zoals geregistreerd door de sensor.
solution: Insight
title: Gegevensrecordvelden voor basisgebeurtenissen
uuid: aa36d332-089c-4ae2-98e2-a93d2fa023b7
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Gegevensrecordvelden voor basisgebeurtenissen{#baseline-event-data-record-fields}

Informatie over de recordvelden van de basisgebeurtenis, zoals geregistreerd door de sensor.

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
   <td colname="col2"> <p>Het IP adres van de cliënt zoals inbegrepen in het verzoek dat aan de server wordt gemaakt. </p> <p>Voorbeeld: 207 68 146 68 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> cs (cookie) </td> 
   <td colname="col2"> <p>De koekjes die door de cliënt met het verzoek worden verzonden. </p> <p>Voorbeeld: v1st=42FDF66DE610CF36; ASPSESSIONIDQCATDAQC=GPIBKEIBFIPLOJMKCAAEPM; </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> cs (referentie) </td> 
   <td colname="col2"> <p>Het de verwijzingskoord van HTTP dat door de cliënt naar de server met het verzoek wordt verzonden. </p> <p>Voorbeeld: http://www.mysite.net/cgi-bin/websearch?qry </p> <p>Als u paginabags gebruikt, is cs (referrer) de volledige URL van het document met de tagafbeelding, inclusief HTTP of HTTP's. </p> <p>Ook, kunt u Apache (1.3, 2.0, en 2.2) en sensoren vormen IIS om de haven te vangen die voor het verzoek wordt gebruikt, die HTTP vs. HTTPS- verzoeken kan identificeren. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> cs (gebruikersagent) </td> 
   <td colname="col2"> <p>Het koord dat door de cliënt met zijn verzoek wordt verzonden naar de server die op welk type van gebruikersagent wijst de cliënt is. </p> <p>Voorbeeld: Mozilla/5.0 (Windows; U; Windows NT 5.1; en-VS; Rv.1.7) Gecko/20040707 Firefox/0.9.2 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> cs-methode </td> 
   <td colname="col2"> <p>Het methodetype van het HTTP- verzoek </p> <p>Voorbeeld: KRIJGEN </p> <p>Referentie: http://www.w3.org/TR/2000/NOTE-shoplogfileformat-20001115/#field_method </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> cs-uri-query </td> 
   <td colname="col2"> <p>Het gedeelte van het vraagkoord van URI (stem + vraagkoord = URI) </p> <p>Dit wordt voorafgegaan door een vraagteken (?) en kan één of meerdere naam-waarde paren bevatten die door ampersands (&amp;) worden gescheiden. </p> <p>Voorbeeld: page=homepage </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> cs-uri-stengel </td> 
   <td colname="col2"> <p>Het stamgedeelte van URI (stam + vraagkoord = URI) </p> <p>De stam is de daadwerkelijke of logische weg aan het gevraagde middel op de server. </p> <p>Voorbeeld: /index.asp </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> SC(inhoudstype) </td> 
   <td colname="col2"> <p>Het inhoudstype van het middel dat door de cliënt wordt gevraagd zoals die door de server wordt gemeld. </p> <p>Voorbeelden: tekst/html, beeld/png, beeld/gif, video/mpeg </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> sc-bytes </td> 
   <td colname="col2"> <p>Het aantal bytes van gegevens die van de server naar de cliënt in antwoord op het verzoek worden verzonden. </p> <p>Voorbeeld: 4996 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> SC-status </td> 
   <td colname="col2"> <p>De statuscode die door de server aan de cliënt is teruggekeerd. </p> <p>Voorbeeld: 200 </p> <p>Referentie: http://www.w3.org/Protocols/rfc2616/rfc2616-sec10.html </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> s-dns </td> 
   <td colname="col2"> <p>Volledig - gekwalificeerde domeinnaam of IP adres van de gastheer van het gevraagde middel. </p> <p>Voorbeeld: www.omniture.com </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> x-experiment </td> 
   <td colname="col2"> <p>De lijst van alle gecontroleerde experimentele namen en groepen waarvan de cliënt een lid op het tijdstip van het verzoek is. </p> <p>Voorbeeld: Home_Exp.Group_1,Registration_Exp.Group_2 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> x-timestamp </td> 
   <td colname="col2"> <p>De datum en de tijd (GMT) waarop het verzoek door de server werd ontvangen. </p> <p>De tijd wordt uitgedrukt als het aantal van 100 nanoseconden sinds 1 januari 1600. </p> <p>Voorbeeld: 12771098932000000 zou de x-timestamp waarde zijn voor 11:28:52.00000 op dinsdag 13 september 2005. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> x-trackingid </td> 
   <td colname="col2"> <p>De hexadecimale waarde met 64 bits van het unieke browser herkenningsteken dat in een blijvend koekje wordt gevonden zoals die door een <span class="wintitle"> Sensor wordt geplaatst </span> en door de cliënt met een verzoek aan een server wordt verstrekt. </p> <p>Voorbeeld: 42FDF66DE610CF36 </p> </td> 
  </tr> 
 </tbody> 
</table>

Het [!DNL data workbench server] kan een aantal variabelen uit de het gegevensverslaggebieden van de basislijngebeurtenis afleiden. Voor meer informatie, zie de Gids *van de Configuratie van de* Dataset.
