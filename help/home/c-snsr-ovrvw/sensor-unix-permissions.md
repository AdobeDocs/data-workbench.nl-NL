---
description: Informatie over de het dossiertoestemmingen van de UNIX van de Sensor zoals de inzamelaarmodule, het transmissieproces, het configuratiedossier, en meer.
title: UNIX-bestandsmachtigingen instellen
uuid: 04d159b5-6569-48b6-a2db-9a0b40118ffe
exl-id: 07cbc7df-c628-437d-9ca1-b006da8de242
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '401'
ht-degree: 1%

---

# UNIX-bestandsmachtigingen instellen{#sensor-unix-file-permissions}

{{eol}}

Informatie over de het dossiertoestemmingen van de UNIX van de Sensor zoals de inzamelaarmodule, het transmissieproces, het configuratiedossier, en meer.

## De module Verzameling {#section-49c855baece24c4695184bfcbeeddebf}

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
   <td colname="col2"> <p>mod_visual_sciences.so (op Apache-webservers en IBM HTTP-servers) </p> <p>libvisual_sciences.so en J2EECollector.jar (op J2EE-toepassingsservers) </p> <p>aol_visual_sciences.so (op AOL-webservers) </p> <p>saf_visual_sciences.so (op Sun Java-webservers) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Standaardmachtigingen </p> </td> 
   <td colname="col2"> <p>rwx r-x r-x (IBM HTTP en Apache 1.3.x) </p> <p>rwx rwx r-x (Apache 2.0.x) </p> <p>rwx —x —x (J2EE-, AOL- en Sun Java-webservers) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Lezen op </p> </td> 
   <td colname="col2"> <p>De webserver, die soms als hoofdgebruiker wordt uitgevoerd, maar vaker onder een specifieke gebruikersaccount wordt uitgevoerd </p> <p>Als de webserver wordt uitgevoerd onder een niet-hoofdaccount, moeten de machtigingen voor dit bestand toestaan dat de account deze kan lezen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Wordt uitgevoerd als </p> </td> 
   <td colname="col2"> <p>Een onderliggend proces in de webserver </p> <p>Onderliggende processen worden uitgevoerd onder een gebruikersaccount die in uw webserverconfiguratie is opgegeven. Op veel servers is dit een speciaal account met zeer beperkte rechten, 'niemand' genoemd. Niet alle webservers gebruiken dit account. Controleer het configuratiebestand van uw webserver om te bepalen welke gebruikersaccount is ingesteld. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Lezen van </p> </td> 
   <td colname="col2"> <p>txlogd.conf </p> <p>Het bestand diskQueue </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Schrijft naar </td> 
   <td colname="col2"> Het bestand diskQueue </td> 
  </tr> 
 </tbody> 
</table>

## Verzendproces {#section-8af432472e9d4bd9a42270bf27adf33a}

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
   <td colname="col1"> <p>Standaardmachtigingen </p> </td> 
   <td colname="col2"> <p>rw- r— r— (IBM HTTP-, AOL- en Sun Java-webservers) </p> <p>rw- rw- r— (Apache-webservers en J2EE-toepassingsservers) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Lezen op </td> 
   <td colname="col2"> Het uitzendprogramma </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Geschreven door </td> 
   <td colname="col2"> — </td> 
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
   <td colname="col1"> <p>Standaardmachtigingen </p> </td> 
   <td colname="col2"> <p>rw- r— r— (IBM HTTP-, AOL- en Sun Java-webservers) </p> <p>rw- rw- r— (Apache-webservers en J2EE-toepassingsservers) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Lezen op </td> 
   <td colname="col2"> <p>De verzamelaarmodule </p> <p>Het uitzendprogramma </p> <p>De beheerder die verantwoordelijk is voor het installeren, configureren en onderhouden van de Sensor </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Geschreven door </td> 
   <td colname="col2"> De beheerder die verantwoordelijk is voor het installeren, configureren en onderhouden van de Sensor </td> 
  </tr> 
 </tbody> 
</table>

## Het bestand van de certificeringsinstantie {#section-2818dff887b8456992bdc589fd8510f3}

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
   <td colname="col1"> <p>Standaardmachtigingen </p> </td> 
   <td colname="col2"> <p>rw- r— r— (IBM HTTP-, AOL- en Sun Java-webservers) </p> <p>rw- rw- r— (Apache-webservers en J2EE-toepassingsservers) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Lezen op </td> 
   <td colname="col2"> Het uitzendprogramma </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Geschreven door </td> 
   <td colname="col2"> — </td> 
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
   <td colname="col1"> Standaardmachtigingen </td> 
   <td colname="col2"> rw- rw- rw- (Alle servertypen) </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Lezen op </p> </td> 
   <td colname="col2"> <p>De verzamelaarmodule </p> <p>Het uitzendprogramma </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Geschreven door </p> </td> 
   <td colname="col2"> <p>De verzamelaarmodule </p> <p>Het uitzendprogramma </p> </td> 
  </tr> 
 </tbody> 
</table>
