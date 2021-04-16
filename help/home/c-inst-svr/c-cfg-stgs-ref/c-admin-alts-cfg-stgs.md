---
description: Instructies om administratieve alarm voor de Server, de Repeater van het Inzicht, of Transformatie te vormen.
title: Configuratie-instellingen voor administratieve waarschuwingen
uuid: c2be2d1e-d81d-4d9f-ac94-4b642dad90b9
exl-id: c75e442e-33e6-4fc8-8368-29482f09e1cc
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '514'
ht-degree: 0%

---

# Systeeminstellingen voor waarschuwingen{#administrative-alerts-configuration-settings}

Instructies om administratieve alarm voor de Server, de Repeater van het Inzicht, of Transformatie te vormen.

Voltooi de parameters in het volgende bestand:

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
   <td colname="col2"> De naam van de categorie. Een categorie Standaard is vereist. Zie Foutcategorieën in deze tabel. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Foutcategorieën </td> 
   <td colname="col2"> Hiermee kunt u fouten categoriseren in combinatie met het Error Categorization-bestand. Elke categorie van de Fout kan zijn eigen reeks Ontvangers en zijn eigen Vertraging Throttle hebben. U kunt bijvoorbeeld een categorie Kritiek maken met een vertragingstijd van 0, zodat elke kritieke fout direct naar de ontvangers wordt gemaild die in de lijst met ontvangers zijn opgegeven. Fouten die niet overeenkomen met een subtekenreeks in het bestand met foutcategorisering worden toegewezen aan de categorie Standaard. Als u een nieuwe categorie wilt toevoegen, klikt u met de rechtermuisknop op een nummer en klikt u op Nieuwe </span> &gt; <span class="uicontrol"> Foutcategorie </span> toevoegen. <span class="uicontrol"> U kunt de clips ook kopiëren of verwijderen met de rechtermuisknop. </span></td> 
  </tr> 
  <tr> 
   <td colname="col1"> Fout bij categoriseren van bestand </td> 
   <td colname="col2"> <p>De naam van het bestand dat u wilt gebruiken om elke waarschuwing te categoriseren. U maakt dit bestand met Kladblok. Dit bestand moet drie kolommen bevatten op elke regel, gescheiden door tabs. De eerste kolom is een tekenreeks die moet overeenkomen met fouten. Een ^-teken komt overeen met het begin en een $ komt overeen met het einde van de tekenreeks. alle andere tekens komen letterlijk overeen. De tweede kolom is een categorie voor fouten die overeenkomen. Deze categorie bevindt zich in Foutcategorieën. Het derde is een alternatief bericht, dat aan het daadwerkelijke foutenbericht in e-mails wordt toegevoegd die worden verzonden. Als er geen bestand is opgegeven, worden alle fouten gecategoriseerd als standaard. </p> <p>Als u een voorbeeld van dit bestand wilt zien, raadpleegt u het bestand <span class="filepath"> Error Categories.txt </span> in de map Lookups. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Van </td> 
   <td colname="col2"> <p>Adres dat in de parameter "van"van het e-mailbericht verschijnt. </p> <p>Voorbeeld: <span class="filepath"> server_errors@mycompany.com </span></p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Minimale schijfruimte (MB) </td> 
   <td colname="col2"> De server genereert een e-mailwaarschuwing wanneer beschikbare schijfopslag in een map die door de server wordt gebruikt, onder deze waarde daalt. De standaardwaarde is 1000. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Tijdslimiet voor sensorwaarschuwing (min) </td> 
   <td colname="col2"> <p>De server genereert een e-mailwaarschuwing wanneer deze binnen dit tijdvenster geen gegevens heeft ontvangen van een geconfigureerde en eerder verbonden <span class="wintitle">-sensor </span>. De standaardwaarde is 15. </p> <p> <p>Opmerking:  <span class="wintitle"> Sensor </span> Alert Timeout werkt slechts als een bestaande verbinding aan een <span class="wintitle"> Sensor </span> wordt gelaten vallen. Als de service van de server wordt gestopt en opnieuw wordt gestart en de <span class="wintitle">-sensoren </span> geen verbinding maken, genereert de server geen e-mailwaarschuwingen. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Serveradres </td> 
   <td colname="col2"> <p>Het adres van de SMTP-server voor uitgaande e-mail. </p> <p>Voorbeeld: <span class="filepath"> mail.mijnbedrijf.nl </span></p> <p>Een server SMTP wordt vereist voor gebruik van de beschreven mogelijkheden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Serverwachtwoord </td> 
   <td colname="col2"> <p>Het wachtwoord voor het aanmelden bij de SMTP-server. Deze parameter is optioneel, tenzij aanmelding vereist is om e-mail te verzenden. </p> <p>Een server SMTP wordt vereist voor gebruik van de beschreven mogelijkheden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Servergebruiker </td> 
   <td colname="col2"> <p>De gebruikersnaam/naam voor het aanmelden bij de SMTP-server. Deze parameter is optioneel, tenzij aanmelding vereist is om e-mail te verzenden. </p> <p>Een server SMTP wordt vereist voor gebruik van de beschreven mogelijkheden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Vertraging door Throttle (sec) </td> 
   <td colname="col2"> Het minimale aantal seconden dat moet verstrijken tussen twee fouten in die categorie voor een e-mailbericht dat moet worden verzonden. Met de waarde 0 wordt het e-mailbericht direct verzonden. </td> 
  </tr> 
 </tbody> 
</table>
