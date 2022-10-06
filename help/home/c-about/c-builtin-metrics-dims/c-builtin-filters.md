---
description: Profielfilters beperken het bereik van de gegevens die beschikbaar zijn in een gegevensset.
title: Ingebouwde profielfilters
uuid: d6854d2c-4643-476e-8a44-f188e18cb115
exl-id: bb167487-415d-44a8-9a0a-9a76d90ba5c0
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '484'
ht-degree: 0%

---

# Ingebouwde profielfilters{#built-in-profile-filters}

{{eol}}

Profielfilters beperken het bereik van de gegevens die beschikbaar zijn in een gegevensset.

Naast de filters van de logboekverwerking en van de transformatie die vóór of tijdens de verwezenlijking van een dataset kunnen worden toegepast, zijn andere profielfilters beschikbaar die het werkingsgebied van de gegevens beïnvloeden beschikbaar voor selectie uit een dataset. In deze sectie wordt alleen het laatste type speciale filters beschreven.

De volgende profielfilters zijn beschikbaar aan de gebruiker nadat een dataset is gecreeerd:

* Filter gegevenssubset
* Filter verbroken sessie

>[!NOTE]
>
>Extra filters kunnen worden gemaakt en toegepast door hun aanwezigheid in de map Filters van een profiel.

## Gegevenssubset {#section-0defb44315d94254ab6e629ec3d6f420}

Een gegevenssubset fungeert als een gegevensfilter doordat u alleen de dimensie-elementen van gegevens kunt selecteren die voor u van belang zijn.

Het creëren van gegevensondergroepen vermindert de hoeveelheid tijd die wordt vereist om nauwkeurige antwoorden aan uw vragen te berekenen. Als de gegevensondergroep die u specificeert klein genoeg is, kan de Data Workbench alle vereiste gegevens van de Server van het Inzicht terugwinnen en vragen over de ondergroep snel en nauwkeurig beantwoorden. Dit is vooral handig als u weet dat bijvoorbeeld het analyseren van een dag met gegevens of sessies van een bepaalde referentie enkele uren zal vergen.

Gebruikers kunnen zelf gegevenssubsets maken of ze kunnen toegang krijgen tot gegevenssubsets die zijn gedefinieerd in een overgeërfd of werkprofiel. Wanneer een gebruiker een subset van de dataset (door de gewenste gegevens in Inzicht te selecteren en dan in de werkruimte met de rechtermuisknop te klikken en Gegevens > Subset te klikken) creeert een Subset.filter van Gegevens dossier wordt gecreeerd in de omslag van Filters binnen de folder van het Gebruikersprofiel. Dit filter definieert de gegevenssubset die u hebt geselecteerd en slaat de subset op voor toekomstig gebruik.

>[!NOTE]
>
>U kunt meerdere gegevenssubsets maken en deze schakelen om verschillende delen van de gegevens weer te geven. Vergeet niet om Subset van gegevens uit te schakelen wanneer u alle gegevens wilt weergeven. Anders, zullen uw metrische waarden niet representatief voor alle gegevens in de dataset zijn.

## Filter verbroken sessie {#section-1608e97da6464b11aea27cbb7f3160e4}

Het filter Gebroken Zitting is een metrische formule die gemakkelijk kan worden gewijzigd om het even welke het filtreren vereisten te ontmoeten. In de standaardsiteprofielen is het filter Gebroken sessie zo geconfigureerd dat het alle bezoekers bevat met een visitorized vlag die is ingesteld op 1. De waarde 1 geeft de aanwezigheid van een trackingcookie voor die bezoeker aan.

Hieronder volgt de tekst van het standaardbestand Broken Session Filter.filter dat door Adobe is opgegeven in het releasepakket voor de siteprofielen.

```
entity = derived_filter:
   formula = string: Visitorized_Flag="1"
   model = ref: wdata/model
```

Standaard wordt in werkruimten het filter Verbroken sessie toegepast op zowel de selectie als de bijbehorende benchmarks. U kunt schakelen door met de rechtermuisknop in de werkruimte te klikken en vervolgens te klikken op Gegevens > Verbroken sessiefilter.

In filterexpressies kan naar het filter Verbroken sessie worden verwezen als Broken_Session_Filter, zelfs als dit filter niet is ingeschakeld voor de huidige werkruimte. Zie [filterexpressies](https://experienceleague.adobe.com/docs/data-workbench/using/client/t-open-ins.html#Syntax_for_Identifiers) voor aanvullende informatie.
