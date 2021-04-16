---
description: Sensor kan bij gebruik op een server velden met gebeurtenisgegevens verzamelen van elke geldige HTTP-aanvraag- of antwoordheader of variabele die beschikbaar is via de API van de server.
title: Uitbreidbare velden
uuid: 91b9857e-44a4-497f-b157-51afd30306fe
exl-id: e783d073-cf06-4415-80e1-567b55fdee12
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '334'
ht-degree: 0%

---

# Uitbreidbare velden{#extensible-fields}

Sensor kan bij gebruik op een server velden met gebeurtenisgegevens verzamelen van elke geldige HTTP-aanvraag- of antwoordheader of variabele die beschikbaar is via de API van de server.

Als u dergelijke gegevensvelden wilt verzamelen, moet u de gewenste headervelden of variabelen opgeven in het configuratiebestand [!DNL txlogd.conf] voor [!DNL Sensor].

* [Aanvraagkoppen](../../../home/c-snsr-ovrvw/c-evnt-data-rcd-flds/c-ex-flds.md#section-22766692b45546d8bfc93dbe3bc9368f)
* [Servervariabelen](../../../home/c-snsr-ovrvw/c-evnt-data-rcd-flds/c-ex-flds.md#section-74b258bc3e8a4a93a0ee9fb01c067e4b)

## Aanvraagkoppen {#section-22766692b45546d8bfc93dbe3bc9368f}

Hier volgt de syntaxis voor het opgeven van een aanvraagheaderveld dat moet worden verzameld (bijvoorbeeld Host, Accept-Encoding, Keep-Alive, enzovoort) in [!DNL txlogd.conf]:

```
LogHeader RequestHeaderName
```

De verzamelde gegevens worden geregistreerd door [!DNL Sensor] aan een gebied genoemd &quot;cs (RequestHeaderName)&quot;in de [!DNL .vsl] dossiers die door [!DNL data workbench server] worden gecreeerd. Bijvoorbeeld, om de specifieke waarde van de verzoekkopbal van de verzoekkopbal &quot;Gastheer te verzamelen,&quot;zou u &quot;Gastheer LogHeader&quot;in [!DNL txlogd.conf] typen. De gegevens worden opgenomen in het veld &quot;cs(Host)&quot; in de record met gebeurtenisgegevens.

## Servervariabelen {#section-74b258bc3e8a4a93a0ee9fb01c067e4b}

[!DNL Sensor] U kunt gegevensvelden verzamelen van responsheaders of API-toegankelijke servervariabelen met SpecialLogField-items die u in het  [!DNL txlogd.conf] bestand opneemt. U kunt ook &#39;SpecialLogField&#39;-items gebruiken naast of in plaats van &#39;LogHeader&#39;-items om aanvraagheaders te verzamelen. Zie [Kopteksten aanvragen](../../../home/c-snsr-ovrvw/c-evnt-data-rcd-flds/c-ex-flds.md#section-22766692b45546d8bfc93dbe3bc9368f). De optie voor aanvraagheaders blijft beschikbaar voor achterwaartse compatibiliteit.

Hier volgt de syntaxis voor het opgeven van een &quot;SpecialLogField&quot; in [!DNL txlogd.conf]:

```
SpecialLogField cs(log field) = serverVariable stage
```

De volgende tabel bevat beschrijvingen van de componenten van een item &quot;SpecialLogField&quot;.

<table id="table_053D5F34D56E4B15A85CA3B4FAD6E1B1"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Component </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> cs (logveld) </td> 
   <td colname="col2"> De naam van het veld waarin de verzamelde gegevens worden opgenomen in de record met gebeurtenisgegevens en de <span class="filepath"> .vsl </span>-bestanden die zijn gemaakt door de <span class="keyword">-werkbankserver </span>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> serverVariable </td> 
   <td colname="col2"> <p>Elke servervariabele die via de API van de server beschikbaar is voor <span class="wintitle"> Sensor </span> </p> <p>Voorbeeld: response.p3p </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> stadium </td> 
   <td colname="col2"> <p>Vys_log of vys_cookie </p> <p>Wanneer u het werkgebied opgeeft, moet u weten welke servervariabelen beschikbaar zijn voor vys_log en vys_cookie. </p> <p>Voorbeeld: Voor serverVariable response.p3p, zou u vys_log ingaan. </p> </td> 
  </tr> 
 </tbody> 
</table>

Neem contact op met de Adobe Consulting Services voor hulp bij het configureren van [!DNL Sensor] voor het verzamelen van uitbreidbare velden voor het opnemen van gebeurtenisgegevens.
