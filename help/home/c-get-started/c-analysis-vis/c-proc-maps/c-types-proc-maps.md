---
description: Informatie over de verschillende soorten proceskaarten.
solution: Analytics
title: Typen proceskaarten
topic: Data workbench
uuid: 19473b77-13c1-4829-b018-d3316e434ba4
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Typen proceskaarten{#types-of-process-maps}

Informatie over de verschillende soorten proceskaarten.

## 2D-proceskaarten {#section-ea7fbdb80b1b44aebcd9e4090b6540bf}

Tweedimensionale proceskaarten verstrekken een tweedimensionale mening van de activiteit tussen afmetingselementen. De grootte van een knoop in een 2D proceskaart is proportioneel aan de waarde van metrisch verbonden aan die knoop. Bovendien zijn zowel de dikte als de intensiteit van een pijl tussen twee knopen proportioneel aan het gemiddelde van de metrische waarden voor die knopen.

Binnen een 2D proceskaart, kunt u om het even welke volgende taken doen:

* Selecteer, beweeg, verwijder, en etiketknopen
* Selecties maken
* Afmetingen opslaan
* Andere visualisaties maken
* Kleurkoppelingen activeren
* Metrische hoeveelheden weergeven
* callouts toevoegen

De 2D proceskaart in het volgende voorbeeld toont knopen die aan de namen van films beantwoorden. Elke filmnaam is een element van de afmeting van de Film, die in een dataset wordt bepaald die uit filmgegevens bestaat. De dimensie van de Film is de basisdimensie voor deze proceskaart.

![](assets/vis_2DProcessMap_MovieNodes.png)

In het voorbeeld, zijn de grootte van elke knoop en de dikte en de intensiteit van elke pijl proportioneel aan metrisch Ratings, die een telling van classificaties is die een film ontving. Daarom heeft een film met een grote knoop, zoals Dag *van de* Onafhankelijkheid, meer classificaties dan een film met een kleine knoop, zoals de Horizon *van de* Gebeurtenis. U kunt ook zien dat meer filmkijkers *Onafhankelijkheidsdag* voor de *Koude Berg* beoordeelden dan de zelfde films in de tegenovergestelde orde schatten. Merk op dat de pijlen niet erop wijzen dat de kijkers de Dag *van de* Onafhankelijkheid en toen de *Koude Berg* onmiddellijk daarna, of vice versa schatten. De kijkers zouden andere films tussen kunnen beoordeeld hebben, maar deze films worden niet getoond op deze kaart.

## 2D metrische kaarten {#section-a9b846fc71224058918fbc378315effe}

Tweedimensionale metrische kaarten zijn een type van 2D proceskaart die de positieknopen die op de waarde van bepaalde metrisch worden gebaseerd. In veel gevallen, is metrisch gebruikt met de 2D metrische kaart of Omzetting of Behoud. De omzetting en de retentiekaarten helpen u begrijpen welke stappen in de processen van uw klant-onder ogen ziende kanalen klantenomzetting en behoud beïnvloeden.

>[!NOTE]
>
>Metrisch die u met een 2D metrische kaart gebruikt moet als percentage worden uitgedrukt.

In een conversie-metrische kaart, worden de knopen met 0 percenten omzetting uitgezet links van de grafiek, en de pagina&#39;s met 100 percenten omzetting worden uitgezet bij het recht. De activiteit tussen knopen wordt getoond, makend het gemakkelijk om te zien welke stappen in een proces tot verhoogde of verminderde omzetting leiden en welke stappen aandrijvingsbeëindiging. Een proces-omzetting analyse is een efficiënte manier om processen te vergelijken of verschillende implementaties van het zelfde proces te vergelijken.

![](assets/vis_2DMetricMap_Conversion.png)

Op dezelfde manier tonen de retentiekaarten elementen met 0 percentenbehoud links van de grafiek en elementen met 100 percenten behoud bij het recht. U kunt het behoudstarief voor elke knoop op de kaart zien, die u helpt bepalen welke elementen klanten beïnvloeden om terug te keren.

![](assets/vis_2DMetricMap_Retention.png)

>[!NOTE]
>
>U kunt geen knopen op 2D metrische kaarten horizontaal bewegen. De metrische kaarten worden ontworpen om knopen te plaatsen links aan recht gebaseerd op hun metrische waarden.

## 3D-proceskaarten {#section-80acb63ea0994af1af7faef3c6264e51}

De driedimensionale proceskaarten verstrekken een driedimensionele mening van de activiteit tussen afmetingselementen. De hoogte van een bar in een 3D proceskaart is proportioneel aan de waarde van metrisch verbonden aan die knoop. Zoals met 2D proceskaarten, zowel zijn de dikte als de intensiteit van de schakelaars tussen twee knopen proportioneel aan het gemiddelde van de waarden van metrisch voor die knopen. Binnen een 3D proceskaart, kunt u om het even welke volgende taken doen:

* Selecteer, beweeg, verwijder, en etiketknopen
* Selecties maken
* Afmetingen opslaan
* Andere visualisaties maken
* Kleurkoppelingen activeren

De 3D proceskaart in het volgende voorbeeld toont knopen die aan de pagina&#39;s van een website beantwoorden. Elke pagina is een element van de dimensie van de Pagina, die in een dataset wordt bepaald die uit de gegevens van het Webverkeer bestaat. De dimensie van de Pagina is de basisdimensie voor deze proceskaart.

![](assets/vis_3DProcessMap_PageNodes.png)

In het voorbeeld, zijn de hoogte van elke bar en de dikte en de intensiteit van elke schakelaar proportioneel aan metrische Zittingen, een telling van zittingen waarin de pagina&#39;s werden bekeken. Daarom werd een pagina met lange bar, zoals /faq/all/FAQs, bekeken tijdens meer zittingen dan een pagina met een korte bar, zoals /vs/demo. Merk op dat de verbindingen tussen twee pagina&#39;s niet erop wijzen dat één pagina onmiddellijk vóór of na een andere tijdens een bepaalde zitting werd bekeken. Andere pagina&#39;s zouden tijdens de zelfde zitting kunnen zijn bekeken, maar deze pagina&#39;s worden niet getoond op deze kaart.
