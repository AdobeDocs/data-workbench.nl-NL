---
description: De informatie over het dossiertoestemmingen van UNIX van de Sensor zoals de inzamelaarmodule, het transmissieproces, het configuratiedossier, en meer.
title: Sensor UNIX-bestandsrechten
uuid: 04d159b5-6569-48b6-a2db-9a0b40118ffe
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Sensor UNIX-bestandsrechten{#sensor-unix-file-permissions}

De informatie over het dossiertoestemmingen van UNIX van de Sensor zoals de inzamelaarmodule, het transmissieproces, het configuratiedossier, en meer.

## De collectormodule {#section-49c855baece24c4695184bfcbeeddebf}

<table id="table_0B972ABD2A5342CA8A6FE80EB666298A"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Kwaliteit </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Bestandsnaam </p> </td> 
   <td colname="col2"> <p>mod_visual_sciences.so (op Apache-webservers en IBM HTTP-servers) </p> <p>libvisual_sciences.so en J2EECollector.jar (op J2EE toepassingsservers) </p> <p>aol_visual_sciences.so (op AOL-webservers) </p> <p>saf_visual_sciences.so (op het Webservers van Java van de Zon) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Standaardrechten </p> </td> 
   <td colname="col2"> <p>rwx r-x r-x (IBM HTTP en Apache 1.3.x) </p> <p>rwx rwx r-x (Apache 2.0.x) </p> <p>rwx —x —x (J2EE, AOL, en de Webservers van Java van de Zon) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Lees door </p> </td> 
   <td colname="col2"> <p>De Webserver, die soms als wortelgebruiker loopt, maar vaak looppas onder een specifieke gebruikersrekening </p> <p>Als de looppas van de Webserver onder een niet-wortelrekening, de toestemmingen op dit dossier die rekening moeten toestaan om het te lezen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Looppas zoals </p> </td> 
   <td colname="col2"> <p>Een kindproces in de Webserver </p> <p>De processen van het kind lopen onder een gebruikersrekening die in uw configuratie van de Webserver wordt gespecificeerd. Op veel servers is dit een speciale account met zeer beperkte privileges die "niemand" wordt genoemd — maar niet alle Webservers gebruiken deze rekening. Controleer het de configuratiedossier van uw Webserver om te bepalen welke gebruikersrekening wordt geplaatst. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Leest van </p> </td> 
   <td colname="col2"> <p>txlogd.conf </p> <p>Het diskQueue-bestand </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Schrijft naar </td> 
   <td colname="col2"> Het diskQueue-bestand </td> 
  </tr> 
 </tbody> 
</table>

## Het verzendingsproces {#section-8af432472e9d4bd9a42270bf27adf33a}

<table id="table_3028CC9640D54016BD8CA7F9CAA34280"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Kwaliteit </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Bestandsnaam </td> 
   <td colname="col2"> trust_ca_cert.pem </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Standaardrechten </p> </td> 
   <td colname="col2"> <p>rw- r— r— (IBM HTTP, AOL, en de Webservers van Java van de Zon) </p> <p>rw- rw- r— (Apache-webservers en J2EE-toepassingsservers) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Lees door </td> 
   <td colname="col2"> Het uitzendprogramma </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Geschreven door </td> 
   <td colname="col2"> -- </td> 
  </tr> 
 </tbody> 
</table>

## Het configuratiebestand {#section-341d85f2abf34a69970a0ff91b7e9123}

<table id="table_79AC614F5435443CB3CFB457B8375704"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Kwaliteit </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Bestandsnaam </td> 
   <td colname="col2"> txlogd.conf </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Standaardrechten </p> </td> 
   <td colname="col2"> <p>rw- r— r— (IBM HTTP, AOL, en de Webservers van Java van de Zon) </p> <p>rw- rw- r— (Apache-webservers en J2EE-toepassingsservers) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Lees door </td> 
   <td colname="col2"> <p>De collectormodule </p> <p>Het uitzendprogramma </p> <p>De beheerder verantwoordelijk voor het installeren, het vormen, en het handhaven van Sensor </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Geschreven door </td> 
   <td colname="col2"> De beheerder verantwoordelijk voor het installeren, het vormen, en het handhaven van Sensor </td> 
  </tr> 
 </tbody> 
</table>

## Het dossier van de certificeringsinstantie {#section-2818dff887b8456992bdc589fd8510f3}

<table id="table_ED8BEEEFA91245C3A6645D27B148A5A7"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Kwaliteit </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Bestandsnaam </td> 
   <td colname="col2"> trust_ca_cert.pem </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Standaardrechten </p> </td> 
   <td colname="col2"> <p>rw- r— r— (IBM HTTP, AOL, en de Webservers van Java van de Zon) </p> <p>rw- rw- r— (Apache-webservers en J2EE-toepassingsservers) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Lees door </td> 
   <td colname="col2"> Het uitzendprogramma </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Geschreven door </td> 
   <td colname="col2"> -- </td> 
  </tr> 
 </tbody> 
</table>

## De schijfwachtrij {#section-0407c52744de41af867d0b7933a69256}

<table id="table_35DB32228E7443FF90BE24AB14CBE54B"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Kwaliteit </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Bestandsnaam </td> 
   <td colname="col2"> Door gebruiker gedefinieerd </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Standaardrechten </td> 
   <td colname="col2"> rw- rw- rw- (Alle servertypes) </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Lees door </p> </td> 
   <td colname="col2"> <p>De collectormodule </p> <p>Het uitzendprogramma </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Geschreven door </p> </td> 
   <td colname="col2"> <p>De collectormodule </p> <p>Het uitzendprogramma </p> </td> 
  </tr> 
 </tbody> 
</table>

