---
description: De sensor, wanneer gebruikt op een server, kan gebieden van gebeurtenisgegevens van om het even welke geldige HTTP- verzoek of reactiekopbal of variabele verzamelen beschikbaar aan het door API van de server.
solution: Insight
title: Uitbreidbare velden
uuid: 91b9857e-44a4-497f-b157-51afd30306fe
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Uitbreidbare velden{#extensible-fields}

De sensor, wanneer gebruikt op een server, kan gebieden van gebeurtenisgegevens van om het even welke geldige HTTP- verzoek of reactiekopbal of variabele verzamelen beschikbaar aan het door API van de server.

Om dergelijke gebieden van gegevens te verzamelen, moet u de gewenste kopbalgebieden of de variabelen in het [!DNL txlogd.conf] configuratiedossier voor specificeren [!DNL Sensor].

* [De Kopballen van het verzoek](../../../home/c-snsr-ovrvw/c-evnt-data-rcd-flds/c-ex-flds.md#section-22766692b45546d8bfc93dbe3bc9368f)
* [Servervariabelen](../../../home/c-snsr-ovrvw/c-evnt-data-rcd-flds/c-ex-flds.md#section-74b258bc3e8a4a93a0ee9fb01c067e4b)

## De Kopballen van het verzoek {#section-22766692b45546d8bfc93dbe3bc9368f}

Na is de syntaxis voor het specificeren van een te verzamelen gebied van de verzoekkopbal (bijvoorbeeld, Gastheer, Accept-Coderend, Levensonderhoud, etc.) in [!DNL txlogd.conf]:

```
LogHeader RequestHeaderName
```

De verzamelde gegevens worden geregistreerd door [!DNL Sensor] aan een gebied genoemd &quot;cs (RequestHeaderName)&quot;in de [!DNL .vsl] dossiers die door worden gecreeerd [!DNL data workbench server]. Bijvoorbeeld, om de specifieke waarde van de verzoekkopbal van de verzoekkopbal &quot;Gastheer te verzamelen,&quot;zou u &quot;Gastheer LogHeader&quot;in typen [!DNL txlogd.conf]. De gegevens worden geregistreerd aan het gebied &quot;cs (Gastheer)&quot;in het verslag van gebeurtenisgegevens.

## Servervariabelen {#section-74b258bc3e8a4a93a0ee9fb01c067e4b}

[!DNL Sensor] kan gebieden van gegevens van reactiekopballen of API-Toegankelijke servervariabelen verzamelen gebruikend de ingangen SpecialLogField die u in het [!DNL txlogd.conf] dossier omvat. U kunt de ingangen &quot;SpecialLogField&quot;naast of in plaats van de ingangen &quot;LogHeader&quot;ook gebruiken om verzoekkopballen te verzamelen. Zie [de Kopballen](../../../home/c-snsr-ovrvw/c-evnt-data-rcd-flds/c-ex-flds.md#section-22766692b45546d8bfc93dbe3bc9368f)van het Verzoek. De optie van verzoekkopballen blijft beschikbaar voor achterwaartse verenigbaarheid.

Na is de syntaxis voor het specificeren van een &quot;SpecialLogField&quot;in [!DNL txlogd.conf]:

```
SpecialLogField cs(log field) = serverVariable stage
```

De volgende lijst omvat beschrijvingen van de componenten van een ingang &quot;SpecialLogField&quot;.

<table id="table_053D5F34D56E4B15A85CA3B4FAD6E1B1"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Onderdeel </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> cs (logboekgebied) </td> 
   <td colname="col2"> De naam van het gebied waaraan de verzamelde gegevens in het verslag van gebeurtenisgegevens en de <span class="filepath"> .vsl </span> - dossiers worden geregistreerd die door de server van de <span class="keyword"> gegevenswerkbank worden gecreeerd </span>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> serverVariable </td> 
   <td colname="col2"> <p>Om het even welke servervariabele die aan <span class="wintitle"> Sensor </span> door API van de server beschikbaar is </p> <p>Voorbeeld: respons.p3p </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> stadium </td> 
   <td colname="col2"> <p>Of vys_log of vys_cookie </p> <p>Het specificeren van het stadium vereist dat u weet welke servervariabelen voor vys_log en vys_cookie beschikbaar zijn. </p> <p>Voorbeeld: Voor serverVariable response.p3p, zou u vys_log ingaan. </p> </td> 
  </tr> 
 </tbody> 
</table>

Voor hulp die het vormen [!DNL Sensor] om de verlengbare gebieden van het verslag van gebeurtenisgegevens te verzamelen, contacteer de Raadplegende Diensten van Adobe.
