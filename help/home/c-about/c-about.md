---
description: De metriek, de afmetingen, en de filters verstrekken een kader waarbinnen de berekeningen over de gegevens worden gemaakt die in een gegevenswerkbankdataset worden verwerkt.
solution: Analytics
title: Metriek van de Werkbank van gegevens, Afmetingen, en Filters
topic: Data workbench
uuid: 3c0300a0-ae19-4817-aab8-7294e0eabdd9
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Metriek van de Werkbank van gegevens, Afmetingen, en Filters{#data-workbench-metrics-dimensions-and-filters}

De metriek, de afmetingen, en de filters verstrekken een kader waarbinnen de berekeningen over de gegevens worden gemaakt die in een gegevenswerkbankdataset worden verwerkt.

De resultaten van de berekeningen die gebruikend dit kader worden bepaald worden getoond in werkruimten, dashboards, rapporten, of andere output. In het kort, om het even welk aantal dat u in of van een toepassing ziet is het resultaat van een vraag van een dataset die metrisch, een afmeting, en een filter impliceert.

Op het meest basisniveau, beschrijft metrisch wat van en over de dataset wordt berekend, breekt een afmeting de gegevens in de dataset in categorieën af, en een filter beschrijft een geselecteerd gedeelte of een ondergroep van de gegevens in de dataset.

Wanneer de Server van de Werkbank van Gegevens gegevens verwerkt om tot een dataset te leiden, worden de afmetingen van de gegevens gecreeerd en dan bijgewerkt op een aan de gang zijnde basis aangezien het nieuwe gegeven door de server wordt gelezen en verwerkt. De metriek en de filters worden berekend uit deze afmetingen van gegevens.

>[!CAUTION]
>
>Als u interne metrisch opnieuw definieert, zal het systeem zich onverwacht wegens de verkeerde waarde gedragen. Uw rapporten zullen niet produceren tenzij metrisch 100% leest. Men adviseert dat u metrische definities niet verandert.

## Een voorbeeld {#section-ecc465d1a5e34d559c1983e96fa409ec}

Stel je een dataset voor die informatie bevat over alle mensen in de wereld. Deze dataset bevat ten minste alle mensen in de wereld en hun leeftijd. Een nuttige metrisch om van deze dataset te berekenen zou Gemiddelde Leeftijd zijn. Het evalueren van dit metrisch zou in één aantal resulteren: de gemiddelde leeftijd van de wereldbevolking.

Het toevoegen van een afmeting aan de dataset maakt deze informatie nuttiger en handelbaarder. Als de gegevensset ook het land van verblijf van elke persoon bevat, zou het definiëren van een landdimensie een manier zijn om de mensen voor elk land in de wereld in groepen te verdelen. De evaluatie van de gemiddelde leeftijd over de landsdimensie zou resulteren in een lijst van getallen, één voor elk land, die elk de gemiddelde leeftijd van de mensen in dat land vertegenwoordigen.

De toepassing van een filter (of selectiefilter) in een metrische formule kan meer gedetailleerde informatie geven of de definitie van nieuwe metrisch toestaan die op bestaande metriek en afmetingen wordt gebaseerd. De evaluatie van de meting van de gemiddelde leeftijd met een filter van &quot;waar land Zweden gelijkstelt&quot; resulteert in één getal: de gemiddelde leeftijd van de mensen in Zweden. Een metrisch gebaseerd op deze filter zou de Gemiddelde Leeftijd van Zweden kunnen zijn.

Bijvoorbeeld:

```
Swedish_Average_Age=Average_Age[country = ‘Sweden’]
```

## Hoe de Metriek, de Afmetingen, en de Filters betrekking hebben {#section-28622596124140b280e6b993b174ef84}

In het algemeen, resulteert de evaluatie van metrisch over een afmeting in dat metrisch die voor elk afmetingselement (of element) wordt geëvalueerd. In het voorbeeld hierboven, heeft de dimensie van het Land een element voor elk land van de wereld. De evaluatie van de gemiddelde leeftijd boven het land zou de gemiddelde leeftijd opleveren voor elk van de elementen (landen), met inbegrip van het element Zweden.

Het is belangrijk om op te merken dat wanneer u metrisch over een afmeting evalueert, u het zelfde numerieke resultaat voor een specifiek afmetingselement ongeacht zult ontvangen of u die metrisch voor de gehele afmeting evalueert of u een filter bepaalt die aan dat specifieke afmetingselement beantwoordt. Bij het zoeken naar de gemiddelde leeftijd van de Zweedse bevolking zou een van de volgende methoden dezelfde resultaten opleveren:

* Evalueer de Gemiddelde Leeftijd metrisch over de afmeting van het Land en bekijk dan het aantal voor het afmetingselement Zweden.
* Evalueer de gemiddelde leeftijd met een filter van &quot;mensen in Zweden&quot; (uitgedrukt als [!DNL Average_[AgeCountry=&#39;Sweden&#39;]]).

De filters zijn syntactische uitdrukkingen die één of meerdere afmetingen en afmetingselementen van verwijzingen voorzien. Zoals u in het bovengenoemde voorbeeld zag, is het gebruiken van de uitdrukking [!DNL [dimensie=element]] een gemakkelijke manier om een filter te specificeren.

Het is enkel zo gemakkelijk om zulk een filter toe te passen om nieuwe metrisch te bepalen gebruikend een uitdrukking zoals [!DNL New_Metric=[MetricFilter]]. Zulk een filter kan worden gebruikt om nieuwe metrisch te bepalen die op een specifiek afmetingselement wordt gebaseerd. Om het bovengenoemde voorbeeld te gebruiken, [!DNL Average_[AgeCountry=&#39;Sweden&#39;]]specificeert metrisch voor de gemiddelde leeftijd van mensen in Zweden. Als we dit metrisch een naam zouden geven, zoals Swedish_Average_Age, konden we het in andere berekeningen als metrisch gebruiken. Bijvoorbeeld, [!DNL Swedish_Average_Age/Average_Age] zou de evaluatie in één enkel aantal resulteren: de verhouding tussen de gemiddelde leeftijd van de Zweedse bevolking en die van de rest van de wereld.

Als de dataset met informatie over alle mensen in de wereld ook een afmetingOogkleur omvat, zou de uitdrukking [!DNL Swedish_Average_[AgeEye_Color=&#39;green&quot;]] in de gemiddelde leeftijd van Zweden met groene ogen resulteren. U zou dit zelfde resultaat ook kunnen verkrijgen zonder een middenmetrische definitie te gebruiken door een verschillende filter toe te passen: [!DNL Average_[AgeCountry=&#39;Sweden&#39; AND Eye_Color=&#39;green&#39;]]. In dit geval, specificeert de [!DNL AND] exploitant een filteruitdrukking gebruikend twee andere basisfilteruitdrukkingen.
