---
description: De kaarten van het gebiedsdeel laten u toe om de configuratie van de componenten van uw profiel te visualiseren en te beheren.
solution: Analytics
title: Dependentiekaarten
topic: Data workbench
uuid: c869267c-5fa9-43b8-b4d4-06c7a36bfa8e
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Dependentiekaarten{#dependency-maps}

De kaarten van het gebiedsdeel laten u toe om de configuratie van de componenten van uw profiel te visualiseren en te beheren.

* **Componenten van gegevensset:** De bronnen, de filters, de gebieden, de transformaties, en de uitgebreide afmetingen van het logboek die in de dataset worden bepaald [!DNL Log Processing.cfg], [!DNL Transformation.cfg], en [!DNL dataset include] dossiers.

* **Modelonderdelen van zoekopdracht:** De metriek, de afmetingen, en de filters die in de Afmetingen, de Metriek, en de omslagen van Filters worden bepaald.
* **Werkruimten en visualisaties:** Werkruimten, rapporten, menuopties, en globe lagen.

Voor meer informatie over het werken met vraag modelcomponenten, werkruimten, en visualisaties in gebiedsdeelkaarten, zie de Gids van de Gebruiker van de Werkbank van *Gegevens*.

De componenten van het profiel worden vertegenwoordigd door gekleurde punten (knopen) in de kaart. De lijnen die de knopen verbinden schilderen gebiedsdelen, namelijk hoe de componenten met elkaar betrekking hebben. Een lijn tussen twee knopen betekent dat een output van de knoop op de linkerzijde een input van de knoop op het recht is, d.w.z., de juiste knoop van de linkerknoop afhangt.

## Gegevensset-componenten weergeven {#section-3e51c09c23cc40aeade2e6ad0fa7c8d2}

1. Klik binnen de gebiedsdeelkaart met de rechtermuisknop aan en klik **[!UICONTROL Display]**.
1. Kies **[!UICONTROL Dataset]**. Een X verschijnt links van [!DNL Dataset].

Voor meer informatie over de andere vertoningsopties zie de Gids *van de Gebruiker van de Werkbank van* Gegevens.

Het volgende cijfer toont een gebiedsdeelkaart de waarvan knopen de logboekbronnen, gebieden, transformaties, en uitgebreide afmetingen van een dataset vertegenwoordigen.

![](assets/vis_DependencyMap.png)

* Een geel-groene knoop vertegenwoordigt één of meerdere logboekbronnen of een filter die in de dataset wordt bepaald. Een knoop voor een logboekbron verschijnt altijd het verst aan de linkerzijde in de kaart.
* Een grijze knoop vertegenwoordigt een gebied dat in de parameter van Gebieden in een [!DNL Log Processing.cfg] of [!DNL Log Processing Include]dossier vermeld is.

* Een blauwe knoop vertegenwoordigt een transformatie.
* Een groene knoop vertegenwoordigt een uitgebreide dimensie.

>[!NOTE]
>
>Als uw dataset één enkele logboekbron heeft, de Bron van het Logboek van kaartvertoningen: Naam *logbron*. Als uw dataset veelvoudige logboekbronnen heeft, de bronnen van het *aantal* van kaartvertoningenLogboek, waar het aantal de telling van logboekbronnen is. Bijvoorbeeld, als u drie logboekbronnen in uw dataset hebt, uw kaartvertoningen 3 Bronnen van het Logboek.

Als u niet alle knopen op de kaart kunt zien, kunt u de kaart of het gezoem binnen bewegen of uit zoemen om de volledige kaart te tonen of zich op een bepaalde sectie te concentreren. Voor meer informatie over het zoemen, zie het Werken met het hoofdstuk van Visualisaties van de Gids van de Gebruiker van de Werkbank van *Gegevens*.

Wanneer u een knoop klikt, worden alle knopen die van die knoop en alle knopen afhangen waarvan die knoop afhangt benadrukt en hun namen tonen.

![](assets/vis_DependencyMap_HighlightedPath.png)

>[!NOTE]
>
>Een benadrukte weg in een gebiedsdeelkaart vormt geen selectie.

Wanneer u een knoop met de rechtermuisknop aanklikt, kunt u het identificeren van informatie over elke component zien die op de kaart wordt getoond en menuopties kiezen die u toelaten om meer detail over de component te bekijken of de component uit te geven. Bovendien kunt u tekstonderzoeken en vertoningsprestatiesinformatie voor transformaties en uitgebreide afmetingen uitvoeren.

Voor informatie over deze functies voor gebiedsdeelkaarten, zie het Administratieve hoofdstuk van Interfaces van de Gids *van de Gebruiker van de Werkbank van* Gegevens.
