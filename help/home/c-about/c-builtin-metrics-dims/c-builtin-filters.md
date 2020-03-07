---
description: De filters van het profiel beperken het werkingsgebied van de gegevens beschikbaar bij een dataset.
solution: Analytics
title: Ingebouwde profielfilters
topic: Data workbench
uuid: d6854d2c-4643-476e-8a44-f188e18cb115
translation-type: tm+mt
source-git-commit: 2e4991206394ca0c463210990ea44dfb700341a5

---


# Ingebouwde profielfilters{#built-in-profile-filters}

De filters van het profiel beperken het werkingsgebied van de gegevens beschikbaar bij een dataset.

Naast de filters van de logboekverwerking en transformatie die vóór of tijdens de verwezenlijking van een dataset kunnen worden toegepast, zijn andere profielfilters beschikbaar die het werkingsgebied van de gegevens beschikbaar voor selectie uit een dataset beïnvloeden. In deze sectie wordt alleen het laatste type speciale filters beschreven.

De volgende profielfilters zijn beschikbaar aan de gebruiker nadat een dataset is gecreeerd:

* Filter voor gegevenssubsetting
* Broken sessiefilter

>[!NOTE]
>
>De extra filters kunnen door hun aanwezigheid in de folder van de Filters van een profiel worden gecreeerd en worden toegepast.

## Subsetting van gegevens {#section-0defb44315d94254ab6e629ec3d6f420}

Een gegevensondergroep doet dienst als gegevensfilter door u toe te staan om slechts de afmetingselementen van gegevens te selecteren die voor u van belang zijn.

Het creëren van gegevensondergroepen vermindert de hoeveelheid tijd die wordt vereist om nauwkeurige antwoorden aan uw vragen te berekenen. Als de gegevensondergroep die u specificeert klein genoeg is, kan de Werkbank van Gegevens alle noodzakelijke gegevens van de Server van het Inzicht terugwinnen en vragen over de ondergroep snel en nauwkeurig beantwoorden. Dit is vooral nuttig als u weet dat, bijvoorbeeld, het analyseren van een dag van gegevens of zittingen van een bepaalde verwijzer verscheidene uren zal vereisen.

De gebruikers kunnen gegevensondergroepen tot stand brengen zelf, of zij kunnen tot gegevensondergroepen toegang hebben die in een geërft of werkend profiel worden bepaald. Wanneer een gebruiker tot een ondergroep van de dataset (door de gewenste gegevens in Inzicht te selecteren en dan in de werkruimte met de rechtermuisknop te klikken en Gegevens > Subset te klikken) leidt, wordt een dossier van Subset.filter van Gegevens gecreeerd in de omslag van Filters binnen de folder van het Profiel van de Gebruiker. Deze filter bepaalt de gegevensondergroep die u hebt geselecteerd en bewaart de ondergroep voor toekomstig gebruik.

>[!NOTE]
>
>U kunt veelvoudige gegevensondergroepen tot stand brengen en kunt hen van een knevel voorzien om verschillende gedeelten van de gegevens te bekijken. Herinner me om Subsetting van Gegevens uit te zetten wanneer u alle gegevens wilt bekijken. Anders, zullen uw metrische waarden niet representatief van alle gegevens in de dataset zijn.

## Broken sessiefilter {#section-1608e97da6464b11aea27cbb7f3160e4}

De gebroken Filter van de Zitting is een metrische formule die gemakkelijk kan worden gewijzigd om het even welke het filtreren vereisten te ontmoeten. In de standaardprofielen van de Plaats, wordt de Gebroken Filter van de Zitting gevormd om alle bezoekers te omvatten die een Bezochte Vlag hebben die aan 1 wordt geplaatst. Waarde 1 wijst op de aanwezigheid van een volgend koekje voor die bezoeker.

Hierna volgt de tekst van het standaard Broken Session Filter.filter-bestand dat door Adobe wordt geleverd in het releasepakket voor de siteprofielen.

```
entity = derived_filter:
   formula = string: Visitorized_Flag="1"
   model = ref: wdata/model
```

Door gebrek, hebben de werkruimten de Broken filter van de Zitting die op zowel hun selectie als hun benchmarks wordt toegepast, en het kan worden van een knevel voorzien door in de werkruimte met de rechtermuisknop te klikken en Gegevens te klikken > de Broken Filter van de Zitting.

De gebroken Filter van de Zitting kan in filteruitdrukkingen als Broken_Session_Filter worden van verwijzingen voorzien, zelfs als het niet voor de huidige werkruimte wordt toegelaten. Zie [filteruitdrukkingen](https://docs.adobe.com/content/help/en/data-workbench/using/client/t-open-ins.html#Syntax_for_Identifiers) voor extra informatie.
