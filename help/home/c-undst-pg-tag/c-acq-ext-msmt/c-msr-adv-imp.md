---
description: Als u uw website op de markt brengt, moet u mogelijk advertenties plaatsen in de vorm van afbeeldings- of andere rich media-bestanden (die via uw webserver worden aangeboden) op websites van derden.
title: Meting van Advertisement Impression
uuid: ca2bd6bf-4f49-406c-b47a-18d6abfb48a4
exl-id: 77cd816e-63a4-4080-ac65-0661e1de4ec0
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '245'
ht-degree: 0%

---

# Meting van Advertisement Impression{#measuring-advertisement-impression}

{{eol}}

Als u uw website op de markt brengt, moet u mogelijk advertenties plaatsen in de vorm van afbeeldings- of andere rich media-bestanden (die via uw webserver worden aangeboden) op websites van derden.

In dergelijke gevallen kunt u zowel de indruk van de advertentie op een browser als de daaropvolgende doorklik, als die zich voordoet, op de doel-URL van de advertentie op uw website meten.

Voor advertenties in de vorm van afbeeldingen: toevoegen [!DNL Log=1] naar de queryreeks wordt de afbeelding aangevraagd, en dus de advertentie-indruk, vastgelegd door [!DNL Sensor] voor analysedoeleinden.

```
<!—REFERENCE IMPRESSION TAG->
<IMG SRC="https://www.mysite.com/images/zag.gif?Log=1&v_ic=CAMPAIGN 1&v_ica=72890ab&v_icr=https://money.cnn.com/markets/"/>
<!--END REFERENCE IMPRESSION TAG-->
```

| Gegevens verzameld | Toelichting | Voorbeeld |
|---|---|---|
| v_ic= | Waarde die de campagne voor onderdrukking aanduidt | v_ic=&quot;CAMPAIGN1&quot; |
| v_ica= | Waarde die de middelen van de campagne voor onderdrukking aanduidt | v_ica=&quot;72890ab&quot; |
| v_icr= | Waarde die de impressiecampagnegerder aangeeft | v_icr=&quot;https://money.cnn.com/markets/ |

Naast toevoegen [!DNL Log=1] aan de afbeeldingsaanvraag moet een id worden toegevoegd aan de URL die van de advertentie naar de doelpagina in uw website leidt, om de advertentie te volgen die tot de doorklikactie heeft geleid en om de doorklikprocedure weer bij te houden naar de specifieke campagne voor die advertentie.

```
<a href=”www.mysite.com/path/to/landingpage?Log=1&v_c=CAMPAIGN&v_ca=72890ab&v_cr=https://money.cnn.com/markets/”>
Click Here
</a>
```

<table id="table_B87134C522EF4AC9BD2AFA6F4A0CF574">
 <thead>
  <tr>
   <th colname="col1" class="entry"> Gegevens verzameld </th>
   <th colname="col2" class="entry"> Toelichting </th>
   <th colname="col3" class="entry"> Voorbeeld </th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td colname="col1"> v_c= </td>
   <td colname="col2"> Waarde die de Klikken-door Campagne duidt </td>
   <td colname="col3"> v_c="CAMPAIGN1" </td>
  </tr>
  <tr>
   <td colname="col1"> v_ca= </td>
   <td colname="col2"> Waarde die de Middel van de Campagne van het Doorklikken-door aanduidt </td>
   <td colname="col3"> v_ca="72890ab" </td>
  </tr>
  <tr>
   <td colname="col1"> v_cr= </td>
   <td colname="col2"> Waarde die de Click-through Referrer van de Campagne aanduidt </td>
   <td colname="col3"> <p> <span class="filepath"> v_cr="https://money.cnn.com/</span> </p> <p>markten/ </p> </td>
  </tr>
 </tbody>
</table>
