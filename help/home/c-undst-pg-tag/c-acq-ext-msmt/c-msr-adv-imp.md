---
description: Het op de markt brengen van uw website kan de plaatsing van reclame in de vorm van beeld of andere rijke media dossiers (die van uw Webserver worden gediend) op derdewebsites impliceren.
solution: Analytics
title: Meten van reclame-uitingen
topic: Data workbench
uuid: ca2bd6bf-4f49-406c-b47a-18d6abfb48a4
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Meten van reclame-uitingen{#measuring-advertisement-impression}

Het op de markt brengen van uw website kan de plaatsing van reclame in de vorm van beeld of andere rijke media dossiers (die van uw Webserver worden gediend) op derdewebsites impliceren.

In dergelijke gevallen, zou u zowel de indruk van de reclame op browser als de verdere klik-door, als één voorkomt, aan het doel URL van de reclame op uw website kunnen willen meten.

Voor advertenties in de vorm van beelden, resulteert het toevoegen [!DNL Log=1] aan het vraagkoord in het beeldverzoek, en zo de reclame-indruk, die door [!DNL Sensor] voor analysedoeleinden wordt gevangen.

```
<!—REFERENCE IMPRESSION TAG-> 
<IMG SRC="http://www.mysite.com/images/zag.gif?Log=1&v_ic=CAMPAIGN 1&v_ica=72890ab&v_icr=http://money.cnn.com/markets/"/>
<!--END REFERENCE IMPRESSION TAG-->
```

| Verzamelde gegevens | Toelichting | Voorbeeld |
|---|---|---|
| v_ic= | Waarde die de Campagne van de Impressie aanduidt | v_ic=&quot;CAMPAIGN1&quot; |
| v_ica= | Waarde die de Activa van de Campagne van de Impressie aanduidt | v_ica=&quot;72890ab&quot; |
| v_icr= | Waarde die de Referrer van de Campagne van de Impressie aanduidt | v_icr=&quot;http://money.cnn.com/markets/ |

Naast het toevoegen [!DNL Log=1] aan het beeldverzoek, zou een herkenningsteken aan URL moeten worden toegevoegd die van de reclame aan de doelpagina binnen uw website leidt om de reclame te volgen die tot de klik-door leidde en de klik-door terug naar de bepaalde campagne voor die reclame te volgen.

```
<a href=”www.mysite.com/path/to/landingpage?Log=1&v_c=CAMPAIGN&v_ca=72890ab&v_cr=http://money.cnn.com/markets/”>
Click Here
</a>
```

<table id="table_B87134C522EF4AC9BD2AFA6F4A0CF574"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Verzamelde gegevens </th> 
   <th colname="col2" class="entry"> Toelichting </th> 
   <th colname="col3" class="entry"> Voorbeeld </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> v_c= </td> 
   <td colname="col2"> Waarde die de klik-door Campagne aanduiden </td> 
   <td colname="col3"> v_c="CAMPAIGN1" </td> 
  </tr> 
  <tr> 
   <td colname="col1"> v_ca= </td> 
   <td colname="col2"> Waarde die de Click-through Activa van de Campagne aanduidt </td> 
   <td colname="col3"> v_ca="72890ab" </td> 
  </tr> 
  <tr> 
   <td colname="col1"> v_cr= </td> 
   <td colname="col2"> Waarde die de Click-through Referrer van de Campagne aanduidt </td> 
   <td colname="col3"> <p> <span class="filepath"> v_cr="http://money.cnn.com/</span> </p> <p>markten/ </p> </td> 
  </tr> 
 </tbody> 
</table>

