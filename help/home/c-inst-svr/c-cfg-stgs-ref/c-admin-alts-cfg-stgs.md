---
description: Instructies om administratief alarm voor de Server van het Inzicht, de Repeater, of de Transformatie te vormen.
solution: Insight
title: Instellingen voor configuratie van beheerberichten
uuid: c2be2d1e-d81d-4d9f-ac94-4b642dad90b9
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Instellingen voor configuratie van beheerberichten{#administrative-alerts-configuration-settings}

Instructies om administratief alarm voor de Server van het Inzicht, de Repeater, of de Transformatie te vormen.

Voltooi de parameters in het volgende dossier:

[!DNL Product Name installation directory\Components\Administrative Alerts.cfg]

<table id="table_5A2298906D5F4215B8FAC42CACBC0002"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Parameter </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Categorie </td> 
   <td colname="col2"> De naam van de categorie. Een categorie van Gebrek wordt vereist. Zie Foutrubrieken in deze tabel. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Foutcategorieën </td> 
   <td colname="col2"> Laat u fouten samen met het Dossier van de Indeling van de Fout categoriseren. Elke categorie van de Fout kan zijn eigen reeks Ontvangers en zijn eigen Vertraging van de Bedrading hebben. Bijvoorbeeld, zou u een Kritieke categorie met een throttle vertraging van 0 kunnen tot stand brengen, zodat elke kritieke fout onmiddellijk aan de ontvangers wordt gemaild die in de lijst van Ontvangers worden gespecificeerd. De fouten die geen substring in het Dossier van de Indeling van de Fout aanpassen worden toegewezen aan de Standaard categorie. Om een nieuwe categorie toe te voegen, klik op een aantal met de rechtermuisknop aan en de klik <span class="uicontrol"> voegt Nieuw </span> &gt; <span class="uicontrol"> de Categorie van de Fout toe </span>. U kunt hen ook kopiëren of verwijderen gebruikend de met de rechtermuisknop aangeklikte actie. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Foutcategorisatiebestand </td> 
   <td colname="col2"> <p>De naam van het dossier u wilt gebruiken om elk alarm te categoriseren. U creeert dit dossier gebruikend Blocnote. Dit dossier zou drie kolommen op elke lijn moeten hebben, die door lusjes wordt gescheiden. De eerste kolom is een koord in fouten aan te passen. Een ^ teken past het begin aan en een $ past het eind van het koord aan; alle andere karakters worden letterlijk aangepast. De tweede kolom is een categorie voor fouten die aanpassen, die in de Categorieën van de Fout is. Het derde is een afwisselend bericht, dat aan de daadwerkelijke foutenmelding in e-mails wordt voorbereid die worden verzonden. Als geen dossier wordt gespecificeerd, categoriseren alle fouten als Gebrek. </p> <p>Om een voorbeeld van dit dossier te zien, zie het <span class="filepath"> </span> dossier van de Categories.txt van de Fout in de folder van Raadplegingen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Van </td> 
   <td colname="col2"> <p>Adres dat in de "van"parameter van het e-mailbericht verschijnt. </p> <p>Voorbeeld: <span class="filepath"> server_errors@mycompany.com </span></p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Minimale schijfruimte (MB) </td> 
   <td colname="col2"> De server genereert een waarschuwing per e-mail wanneer er schijfopslag beschikbaar is in een directory die door de server wordt gebruikt en die onder deze waarde daalt. De standaardwaarde is 1000. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Sensor Alert Time-out (min) </td> 
   <td colname="col2"> <p>De server genereert een e-mailwaarschuwing wanneer deze geen gegevens van een geconfigureerde en eerder verbonden <span class="wintitle"> sensor </span> binnen dit tijdvenster heeft ontvangen. De standaardwaarde is 15. </p> <p> <p>Opmerking:  <span class="wintitle"> De </span> Waakzame Onderbreking van de sensor werkt slechts als een bestaande verbinding aan een <span class="wintitle"> Sensor </span> wordt gelaten vallen. Als de dienst van de server wordt tegengehouden en opnieuw begonnen en de <span class="wintitle"> Sensors </span> verbinden niet, produceert de server geen e-mailalarm. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Serveradres </td> 
   <td colname="col2"> <p>Het adres van de server SMTP voor uitgaande e-mail. </p> <p>Voorbeeld: <span class="filepath"> mail.mycompany.com </span></p> <p>Een server SMTP wordt vereist voor gebruik van de beschreven mogelijkheden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Serverwachtwoord </td> 
   <td colname="col2"> <p>Het wachtwoord voor het programma openen aan de server SMTP. Deze parameter is facultatief tenzij login wordt vereist om post te verzenden. </p> <p>Een server SMTP wordt vereist voor gebruik van de beschreven mogelijkheden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Servergebruiker </td> 
   <td colname="col2"> <p>De gebruiker - identiteitskaart/naam voor het programma openen aan de server SMTP. Deze parameter is facultatief tenzij login wordt vereist om post te verzenden. </p> <p>Een server SMTP wordt vereist voor gebruik van de beschreven mogelijkheden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Dronkelvertraging (sec.) </td> 
   <td colname="col2"> Het minimumaantal seconden dat tussen twee fouten in die categorie moet verlopen voor het verzenden van een e-mail. Een waarde van 0 verzendt onmiddellijk de e-mail. </td> 
  </tr> 
 </tbody> 
</table>

