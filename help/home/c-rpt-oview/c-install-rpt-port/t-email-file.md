---
description: De toegang tot en de toestemmingen binnen uw Portaal van het Rapport worden gecontroleerd gebruikend individuele gebruiker en groepsrekeningen.
solution: Analytics
title: Het bestand Email.asp bewerken
topic: Data workbench
uuid: 18251170-0317-4a32-b9e1-4ebf2d7ad123
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Het bestand Email.asp bewerken{#edit-the-email-asp-file}

De toegang tot en de toestemmingen binnen uw Portaal van het Rapport worden gecontroleerd gebruikend individuele gebruiker en groepsrekeningen.

Telkens wanneer u een nieuwe account toevoegt of een bestaande account bewerkt, kunt u een bevestigingsbericht verzenden naar het e-mailadres dat u voor die account opgeeft (zie [Werken met accounts](../../../home/c-rpt-oview/c-admin-rpt/c-work-accts/c-work-accts.md#concept-c933a1940bda4a3489d61d8af315e45d)) en naar de e-mailadressen die u in het [!DNL email.asp] bestand opgeeft, kopiëren.

>[!NOTE]
>
>E-mails met berichten worden alleen naar rekeninggebruikers gestuurd als u een e-mailadres voor de account hebt opgegeven en het [!DNL email.asp] bestand correct hebt geconfigureerd. Als je geen e-mailberichten voor een account wilt verzenden, moet je het e-mailveld van de account leeg laten.

Dit dossier verblijft in de `\*PortalName*\PortalASP` omslag.

1. Voor de machine waar IIS loopt, open het [!DNL email.asp] dossier in een tekstredacteur zoals Blocnote.
1. Stel de volgende variabelen in:

<table id="table_44F52DA266364DF993C40678A28E0F0D"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Voor deze variabele. . . </th> 
   <th colname="col2" class="entry"> Verstrek deze informatie. . . </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> smpserver </td> 
   <td colname="col2"> <p>DNS naam of IP adres van de server SMTP waardoor de berichten worden verzonden. </p> <p>Bijvoorbeeld: <span class="filepath"> mail.hq.omniture.com</span></p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> smtpserverpoort </td> 
   <td colname="col2"> De haven waarop de server SMTP op verbindingen let. Dit is typisch haven 25. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> slingerend </td> 
   <td colname="col2"> <p>Wijst op hoe het bericht moet worden verzonden. De waarden zijn: </p> <p>1 - verzend berichten gebruikend de plaatselijk geïnstalleerde dienst SMTP. Gebruik deze waarde als de dienst SMTP op de computer geïnstalleerd is waar het manuscript loopt. </p> <p>2 - verzend berichten gebruikend de dienst SMTP op het netwerk. Gebruik deze waarde als de dienst SMTP niet geïnstalleerd op de computer is waar het manuscript loopt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> time-out voor verbinding </td> 
   <td colname="col2">De hoeveelheid tijd dat het <span class="wintitle"> Rapport</span> op een reactie van de server zou moeten wachten SMTP alvorens het uit de verbinding tijden. </td> 
  </tr> 
 </tbody> 
</table>

1. Voor de [!DNL NewUserEmail()] en [!DNL UpdateUserEmail()] functies, plaats de volgende variabelen:

   <table id="table_91C5E36B84A94C4097EE5993592BE587"> 
   <thead> 
   <tr> 
      <th colname="col1" class="entry"> Voor deze variabele. . . </th> 
      <th colname="col2" class="entry"> Verstrek deze informatie. . . </th> 
   </tr> 
   </thead>
   <tbody> 
   <tr> 
      <td colname="col1"> Van </td> 
      <td colname="col2">De tekst die u in van kopballijn in uw bevestigingse-mails wilt verschijnen. Deze waarde zou het zelfde als de waarde van <span class="wintitle"> CC</span> kunnen zijn. </td> 
   </tr> 
   <tr> 
      <td colname="col1"> CC </td> 
      <td colname="col2"> <p>Optioneel. Het geldige e-mailadres van de persoon of het alias die een exemplaar van alle berichten betreffende nieuwe en veranderde gebruikersrekeningen zou moeten ontvangen. U kunt veelvoudige e-mailadressen specificeren door de adressen met komma's (geen ruimten) te scheiden. </p> <p>Bijvoorbeeld: <span class="filepath"> admin@company.com,joemanager@company.com</span></p> <p> <p>Opmerking:  De ontvangers ontvangen exemplaren van e-mails die gebruikerswachtwoorden bevatten. </p> </p> </td> 
   </tr> 
   <tr> 
      <td colname="col1"> Onderwerp </td> 
      <td colname="col2"> De tekst die u in de Onderworpen kopballijn in uw bevestigingse-mail wilt verschijnen. </td> 
   </tr> 
   <tr> 
      <td colname="col1"> WebPath </td> 
      <td colname="col2"> <p>Het daadwerkelijke pad naar uw portaal. </p> <p>Bijvoorbeeld: <span class="filepath"> http://portal.omniture.com/Example</span></p> </td> 
   </tr> 
   <tr> 
      <td colname="col1"> Lichaamslichaam </td> 
      <td colname="col2"> <p>De tekst in de automatisch gegenereerde e-mails. </p> <p>Bijvoorbeeld, is het volgende de standaardtekst inbegrepen in e-mails die worden verzonden om login informatie te verstrekken: 
      <ul id="ul_7FF2E7399AB64D279EC5794AB02C9749">
      <li id="li_7CBCC5CFF9E04776BBC893278785AEE7">De aanmeldgegevens van uw webportaal worden hieronder weergegeven: </li>
      <li id="li_5346F0AB3568444B88117C295D8E99C5"><p>Gebruikersnaam: gebruikersnaam </p><p>Nieuw wachtwoord: wachtwoord </p></li>
      <li id="li_B0D1FAE818BA42CF8546796800A1AA08"><p>U kunt tot het portaal toegang hebben gebruikend volgende URL: </p><p><span class="filepath"> http://WebPath</span></p></li>
      <li id="li_7CD71EBDFA1D418F960040569CD511EB">Nadat u in het portaal registreert, kunt u uw wachtwoord op <span class="wintitle"> Admin</span> tabel veranderen. </li>
      </ul></p> </td> 
   </tr> 
   </tbody> 
   </table>

1. Sparen en sluit het dossier.
