---
description: De metriek, de afmetingen, en de filters verstrekken een kader waarbinnen de berekeningen over de gegevens worden gemaakt die in een gegevenswerkbankdataset worden verwerkt.
title: Metriek, Dimension en filters van de Data Workbench
uuid: 3c0300a0-ae19-4817-aab8-7294e0eabdd9
exl-id: 687d9695-e70c-49ff-ac11-1537e6309e16
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '827'
ht-degree: 0%

---

# Metriek, Dimension en filters{#data-workbench-metrics-dimensions-and-filters} van de Data Workbench

De metriek, de afmetingen, en de filters verstrekken een kader waarbinnen de berekeningen over de gegevens worden gemaakt die in een gegevenswerkbankdataset worden verwerkt.

De resultaten van de berekeningen die met dit framework zijn gedefinieerd, worden weergegeven in werkruimten, dashboards, rapporten of andere uitvoerbestanden. Kortom, om het even welk aantal dat u in of van een toepassing ziet is het resultaat van een vraag van een dataset die metrisch, een afmeting, en een filter impliceert.

Op het meest basisniveau, beschrijft metrisch wat van en over de dataset wordt berekend, onderbreekt een dimensie de gegevens in de dataset in categorieën, en een filter beschrijft een geselecteerd gedeelte of een ondergroep van de gegevens in de dataset.

Wanneer de Server van de Data Workbench gegevens verwerkt om een dataset tot stand te brengen, worden de afmetingen van de gegevens gecreeerd en dan bijgewerkt op een lopende basis aangezien de nieuwe gegevens door de server worden gelezen en verwerkt. Metriek en filters worden berekend op basis van deze afmetingen van gegevens.

>[!CAUTION]
>
>Als u een interne metrisch herdefinieert, zal het systeem onverwacht wegens de verkeerde waarde gedragen. Uw rapporten zullen niet produceren tenzij metrisch 100% leest. Het wordt aanbevolen geen metrische definities te wijzigen.

## Een voorbeeld {#section-ecc465d1a5e34d559c1983e96fa409ec}

Stel je een dataset voor die informatie bevat over alle mensen in de wereld. Deze dataset bevat ten minste alle mensen in de wereld en hun leeftijd. Een nuttige metrische waarde om uit deze dataset te berekenen zou Gemiddelde Leeftijd zijn. Het evalueren van dit metrisch zou in één aantal resulteren: de gemiddelde leeftijd van de wereldbevolking.

Het toevoegen van een dimensie aan de dataset maakt deze informatie nuttiger en handelbaar. Als de gegevensset ook het land van verblijf van elke persoon bevat, zou het definiëren van een landdimensie een manier zijn om de mensen in groepen te verdelen voor elk land in de wereld. De evaluatie van de gemiddelde leeftijd over de landdimensie zou resulteren in een lijst van getallen, één voor elk land, elk voor de gemiddelde leeftijd van de mensen in dat land.

De toepassing van een filter (of selectiefilter) in een metrische formule kan gedetailleerdere informatie geven of de definitie van nieuwe metrisch toestaan die op bestaande metriek en afmetingen wordt gebaseerd. De evaluatie van de gemiddelde leeftijd met een filter &quot;waarbij het land gelijk is aan Zweden&quot; resulteert in één getal: de gemiddelde leeftijd van de Zweedse bevolking. Op basis van dit filter kan de gemiddelde leeftijd in Zweden worden bepaald.

Bijvoorbeeld:

```
Swedish_Average_Age=Average_Age[country = ‘Sweden’]
```

## Hoe de Metriek, de Dimension, en de Filters {#section-28622596124140b280e6b993b174ef84} met elkaar in verband brengen

In het algemeen, leidt het evalueren van metrisch over een afmeting tot dat metrisch die voor elk afmetingselement (of element) wordt geëvalueerd. In het bovenstaande voorbeeld heeft de landdimensie een element voor elk land van de wereld. De evaluatie van de gemiddelde leeftijd boven het land zou de gemiddelde leeftijd opleveren voor elk element (land), inclusief het element Zweden.

Het is belangrijk om op te merken dat wanneer u metrisch over een afmeting evalueert, u het zelfde numerieke resultaat voor een specifiek afmetingselement zult ontvangen ongeacht of u dat metrisch voor de volledige afmeting evalueert of u een filter bepaalt die aan dat specifieke afmetingselement beantwoordt. Wanneer in het vorige voorbeeld naar de gemiddelde leeftijd van de Zweedse bevolking wordt gezocht, zouden de volgende methoden identieke resultaten opleveren:

* Evalueer de maatstaf voor de gemiddelde leeftijd over de landdimensie en bekijk dan het getal voor het dimensie-element Zweden.
* Evalueer de metrische waarde van de gemiddelde leeftijd met een filter &quot;mensen in Zweden&quot; (uitgedrukt als [!DNL Gemiddelde_Leeftijd[Land=&#39;Zweden&#39;]]).

Filters zijn syntactische expressies die verwijzen naar een of meer dimensies en dimensie-elementen. Zoals u in het bovenstaande voorbeeld hebt gezien, is het gebruik van de expressie [!DNL [afmetingen=element]] een eenvoudige manier om een filter op te geven.

Het is net zo gemakkelijk om zulk een filter toe te passen om nieuwe metrisch te bepalen gebruikend een uitdrukking zoals [!DNL New_Metric=Metric[Filter]]. Een dergelijk filter kan worden gebruikt om een nieuwe metrische waarde te definiëren op basis van een specifiek afmetingselement. Om het bovenstaande voorbeeld te gebruiken, [!DNL Gemiddelde_Leeftijd[Land=&#39;Zweden&#39;]]specificeert metrisch voor de gemiddelde leeftijd van mensen in Zweden. Als we deze metrische waarde een naam zouden geven, zoals Swedish_Gemiddelde_Age, zouden we het in andere berekeningen als metrisch kunnen gebruiken. Als u bijvoorbeeld [!DNL Swedish_Average_Age/Average_Age] evalueert, resulteert dit in één getal: de verhouding tussen de gemiddelde leeftijd van de Zweedse bevolking en die van de rest van de wereld.

Als de dataset met informatie over alle mensen in de wereld ook een afmeting Oogkleur omvat, zou de uitdrukking [!DNL Swedish_Average_Age[Eye_Color=&#39;green&#39;]] in de gemiddelde leeftijd van Zweden met groene ogen resulteren. U zou dit zelfde resultaat ook kunnen verkrijgen zonder een tussenmetrische definitie te gebruiken door een verschillend filter toe te passen: [!DNL average_age[Country=&#39;Sweden&#39; AND Eye_Color=&#39;green&#39;]]. In dit geval geeft de operator [!DNL AND] een filterexpressie op met behulp van twee andere basisfilterexpressies.
