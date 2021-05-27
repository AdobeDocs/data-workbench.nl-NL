---
description: Informatie over de verschillende typen proceskaarten.
title: Typen procesafbeeldingen
uuid: 19473b77-13c1-4829-b018-d3316e434ba4
exl-id: 8bac7036-c7fe-4566-8e59-08e1ddc7ddb7
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '748'
ht-degree: 0%

---

# Typen procesafbeeldingen{#types-of-process-maps}

Informatie over de verschillende typen proceskaarten.

## 2D-procesmaps {#section-ea7fbdb80b1b44aebcd9e4090b6540bf}

Tweedimensionale proceskaarten bieden een tweedimensionale weergave van de activiteit tussen dimensie-elementen. De grootte van een knoop in een 2D proceskaart is evenredig aan de waarde metrisch verbonden aan die knoop. Bovendien zijn zowel de dikte als de intensiteit van een pijl tussen twee knooppunten evenredig met het gemiddelde van de waarden van de meting voor die knooppunten.

Binnen een 2D proceskaart, kunt u om het even welke volgende taken doen:

* Knooppunten selecteren, verplaatsen, verwijderen en labelen
* Selecties maken
* Afmetingen opslaan
* Andere visualisaties maken
* Kleurkoppelingen activeren
* Metrische hoeveelheden weergeven
* Bijschriften toevoegen

De 2D proceskaart in het volgende voorbeeld toont knopen die aan de namen van films beantwoorden. Elke filmnaam is een element van de afmetingen van de Film, die in een dataset wordt bepaald die uit filmgegevens bestaat. De dimensie van de Film is de basisdimensie voor dit procesoverzicht.

![](assets/vis_2DProcessMap_MovieNodes.png)

In het voorbeeld zijn de grootte van elk knooppunt en de dikte en intensiteit van elke pijl proportioneel ten opzichte van de maateenheid voor beoordelingen. Dit is een telling van classificaties die een film heeft ontvangen. Daarom heeft een film met een grote knoop, zoals *Onafhankelijkheidsdag*, meer classificaties dan een film met een kleine knoop, zoals *Event Horizon*. U kunt ook zien dat meer filmviewers *Onafhankelijkheidsdag* voor *Koude berg* hebben beoordeeld dan dezelfde films in de tegenovergestelde volgorde. De pijlen geven niet aan dat viewers *Onafhankelijkheidsdag* hebben beoordeeld en vervolgens *Koude berg* direct daarna hebben geclassificeerd, of andersom. Viewers hebben mogelijk andere films beoordeeld, maar deze films worden niet weergegeven op deze kaart.

## 2D metrische kaarten {#section-a9b846fc71224058918fbc378315effe}

Tweedimensionale metrische kaarten zijn een type van 2D proceskaart die knooppunten plaatsen die op de waarde van bepaalde metrisch worden gebaseerd. In veel gevallen, metrisch die met de 2D metrische kaart wordt gebruikt is of Omzetting of Behoud. De kaarten van de omzetting en van het behoud helpen u begrijpen welke stappen in de processen van uw klant-onder ogen ziet kanalen klantenomzetting en behoud beïnvloeden.

>[!NOTE]
>
>Metrisch die u met een 2D metrische kaart gebruikt moet als percentage worden uitgedrukt.

In een metrische kaart van de omzetting, worden de knopen met 0 percenten omzetting in kaart gebracht links van de grafiek, en de pagina&#39;s met 100 percenten omzetting worden getekend bij het recht. De activiteit tussen knopen wordt getoond, die het gemakkelijk maken om te zien welke stappen in een proces tot verhoogde of verminderde omzetting leiden en welke stappen aandrijven verlaten. Een proces-omzettingsanalyse is een efficiënte manier om processen te vergelijken of verschillende implementaties van het zelfde proces te vergelijken.

![](assets/vis_2DMetricMap_Conversion.png)

Op dezelfde manier tonen retentiekaarten elementen met 0 procent retentie aan de linkerkant van de grafiek en elementen met 100 procent retentie aan de rechterkant. U kunt het behoudtarief voor elke knoop op de kaart zien, die u helpt bepalen welke elementen klanten beïnvloeden om terug te keren.

![](assets/vis_2DMetricMap_Retention.png)

>[!NOTE]
>
>U kunt knooppunten op 2D-metrische toewijzingen niet horizontaal verplaatsen. De metrische kaarten worden ontworpen om knopen links aan recht te plaatsen die op hun metrische waarden worden gebaseerd.

## 3D-processtructuren {#section-80acb63ea0994af1af7faef3c6264e51}

Driedimensionale proceskaarten bieden een driedimensionale weergave van de activiteit tussen dimensie-elementen. De hoogte van een bar in een 3D proceskaart is proportioneel aan de waarde metrisch verbonden aan die knoop. Net als bij 2D-proceskaarten zijn zowel de dikte als de intensiteit van de connectoren tussen twee knooppunten evenredig aan het gemiddelde van de waarden van de metrische waarde voor die knooppunten. In een 3D-proceskaart kunt u de volgende taken uitvoeren:

* Knooppunten selecteren, verplaatsen, verwijderen en labelen
* Selecties maken
* Afmetingen opslaan
* Andere visualisaties maken
* Kleurkoppelingen activeren

De 3D-procesafbeelding in het volgende voorbeeld toont knooppunten die overeenkomen met de pagina&#39;s van een website. Elke pagina is een element van de dimensie van de Pagina, die in een dataset wordt bepaald die uit Webverkeersgegevens bestaat. De dimensie Pagina is de basisdimensie voor dit procesoverzicht.

![](assets/vis_3DProcessMap_PageNodes.png)

In het voorbeeld zijn de hoogte van elke balk en de dikte en intensiteit van elke connector proportioneel ten opzichte van de sessiemetrisch, een aantal sessies waarin de pagina&#39;s werden weergegeven. Daarom werd een pagina met lange bar, zoals /faq/all/FAQs, bekeken tijdens meer zittingen dan een pagina met een korte bar, zoals /vs/demo. De verbindingen tussen twee pagina&#39;s geven niet aan dat de ene pagina direct voor of na een andere tijdens een bepaalde sessie is weergegeven. Andere pagina&#39;s zijn mogelijk tijdens dezelfde sessie weergegeven, maar deze pagina&#39;s worden niet op deze kaart weergegeven.
