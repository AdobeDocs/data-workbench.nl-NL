---
description: De toegang tot en de toestemmingen binnen uw Portaal van het Rapport worden gecontroleerd gebruikend individuele gebruiker en groepsrekeningen.
title: Het bestand Email.asp bewerken
uuid: 18251170-0317-4a32-b9e1-4ebf2d7ad123
exl-id: e984f12f-362a-4dee-9af3-6d7a38a178a4
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '469'
ht-degree: 0%

---

# Het bestand Email.asp bewerken{#edit-the-email-asp-file}

{{eol}}

De toegang tot en de toestemmingen binnen uw Portaal van het Rapport worden gecontroleerd gebruikend individuele gebruiker en groepsrekeningen.

Elke keer dat u een nieuwe account toevoegt of een bestaande account bewerkt, kan een bevestigingsbericht worden verzonden naar het e-mailadres dat u voor die account hebt opgegeven (zie [Werken met accounts](../../../home/c-rpt-oview/c-admin-rpt/c-work-accts/c-work-accts.md#concept-c933a1940bda4a3489d61d8af315e45d)) en gekopieerd naar de e-mailadressen die u in het dialoogvenster [!DNL email.asp] bestand.

>[!NOTE]
>
>E-mailberichten over meldingen worden alleen naar gebruikers van een account verzonden wanneer u een e-mailadres voor de account hebt opgegeven en de configuratie van de [!DNL email.asp] bestand. Laat het veld E-mail van de account leeg als je geen e-mailberichten voor een account wilt verzenden.

Dit bestand bevindt zich in het dialoogvenster `\*PortalName*\PortalASP` map.

1. Open op de computer waarop IIS wordt uitgevoerd de [!DNL email.asp] bestand in een teksteditor, zoals Kladblok.
1. Stel de volgende variabelen in:

<table id="table_44F52DA266364DF993C40678A28E0F0D">
 <thead>
  <tr>
   <th colname="col1" class="entry"> Voor deze variabele. . . </th>
   <th colname="col2" class="entry"> Geef deze informatie op. . . </th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td colname="col1"> smtpserver </td>
   <td colname="col2"> <p>DNS naam of IP adres van de server SMTP waardoor de berichten worden verzonden. </p> <p>Bijvoorbeeld: <span class="filepath"> mail.hq.omniture.com</span></p> </td>
  </tr>
  <tr>
   <td colname="col1"> smtpserverport </td>
   <td colname="col2"> De poort waarop de SMTP-server luistert naar verbindingen. Dit is doorgaans poort 25. </td>
  </tr>
  <tr>
   <td colname="col1"> versturen </td>
   <td colname="col2"> <p>Geeft aan hoe het bericht moet worden verzonden. Waarden zijn: </p> <p>1 - Verzend berichten gebruikend de plaatselijk geïnstalleerde dienst SMTP. Gebruik deze waarde als de dienst SMTP op de computer geïnstalleerd is waar het manuscript loopt. </p> <p>2 - Verzend berichten gebruikend de dienst SMTP op het netwerk. Gebruik deze waarde als de SMTP-service niet is geïnstalleerd op de computer waarop het script wordt uitgevoerd. </p> </td>
  </tr>
  <tr>
   <td colname="col1"> smtpconnectionTimeout </td>
   <td colname="col2">De hoeveelheid tijd die <span class="wintitle"> Rapport</span> moet wachten op een reactie van de SMTP-server voordat de verbinding wordt verbroken. </td>
  </tr>
 </tbody>
</table>

1. Voor de [!DNL NewUserEmail()] en [!DNL UpdateUserEmail()] functies, stelt u de volgende variabelen in:

   <table id="table_91C5E36B84A94C4097EE5993592BE587">
   <thead>
   <tr>
      <th colname="col1" class="entry"> Voor deze variabele. . . </th>
      <th colname="col2" class="entry"> Geef deze informatie op. . . </th>
   </tr>
   </thead>
   <tbody>
   <tr>
      <td colname="col1"> Van </td>
      <td colname="col2">De tekst die u wilt weergeven in de koptekstregel Van in uw bevestigingse-mails. Deze waarde kan gelijk zijn aan <span class="wintitle"> CC</span> waarde. </td>
   </tr>
   <tr>
      <td colname="col1"> CC </td>
      <td colname="col2"> <p>Optioneel. Het geldige e-mailadres van de persoon of alias die een kopie van alle berichten met betrekking tot nieuwe en gewijzigde gebruikersaccounts moet ontvangen. U kunt meerdere e-mailadressen opgeven door de adressen te scheiden met komma's (geen spaties). </p> <p>Bijvoorbeeld: <span class="filepath"> admin@company.com,joemanager@company.com</span></p> <p> <p>Opmerking: De ontvangers ontvangen kopieën van e-mailberichten die gebruikerswachtwoorden bevatten. </p> </p> </td>
   </tr>
   <tr>
      <td colname="col1"> Onderwerp </td>
      <td colname="col2"> De tekst die u in de onderwerpregel in uw bevestigingse-mails wilt weergeven. </td>
   </tr>
   <tr>
      <td colname="col1"> WebPath </td>
      <td colname="col2"> <p>Het daadwerkelijke pad naar uw portaal. </p> <p>Bijvoorbeeld: <span class="filepath"> https://portal.omniture.com/Example</span></p> </td>
   </tr>
   <tr>
      <td colname="col1"> Lichaam </td>
      <td colname="col2"> <p>De tekst in de automatisch gegenereerde e-mails. </p> <p>Hieronder ziet u bijvoorbeeld de standaardtekst die is opgenomen in de e-mails die worden verzonden om aanmeldingsgegevens op te geven:
      <ul id="ul_7FF2E7399AB64D279EC5794AB02C9749">
      <li id="li_7CBCC5CFF9E04776BBC893278785AEE7">Hieronder vindt u uw aanmeldingsgegevens voor uw webportal: </li>
      <li id="li_5346F0AB3568444B88117C295D8E99C5"><p>Gebruikersnaam: gebruikersnaam </p><p>Nieuw wachtwoord: password </p></li>
      <li id="li_B0D1FAE818BA42CF8546796800A1AA08"><p>U kunt het portaal openen met de volgende URL: </p><p><span class="filepath"> https://WebPath</span></p></li>
      <li id="li_7CD71EBDFA1D418F960040569CD511EB">Nadat u zich bij de portal hebt aangemeld, kunt u uw wachtwoord wijzigen in het dialoogvenster <span class="wintitle"> Beheer</span> tab. </li>
      </ul></p> </td>
   </tr>
   </tbody>
   </table>

1. Sla het bestand op en sluit het.
