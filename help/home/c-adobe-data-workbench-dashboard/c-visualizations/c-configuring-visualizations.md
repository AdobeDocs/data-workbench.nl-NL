---
description: Toont hoe te om Titel, Profiel, Dimensie, Metrisch, Filter, de Hoogste van de Vertoning, Soort door, en Periode te vormen.
solution: Analytics
title: Visualisaties configureren
topic: Data workbench
uuid: aca77188-8f28-4554-8913-412b252f688c
translation-type: tm+mt
source-git-commit: 25366087936dfa5e31c5921aac400535ec259f2e

---


# Visualisaties configureren{#configuring-visualizations}

Toont hoe te om Titel, Profiel, Dimensie, Metrisch, Filter, de Hoogste van de Vertoning, Soort door, en Periode te vormen.

Elke visualisatie op het dashboardcanvas heeft zijn eigen configuratie. Wanneer een visualisatie eerst aan het dashboardcanvas wordt toegevoegd, zal zijn configuratievenster automatisch verschijnen. Als de configuratie eenmaal is geconfigureerd, kan de visualisatie op elk gewenst moment worden gewijzigd door te klikken op het versnellingspictogram in het rechterbovengedeelte van het visualisatievenster.

>[!NOTE]
>
>De opties van de configuratie variëren lichtjes afhankelijk van het type van visualisatie die wordt getoond.

## Visualisatietitel {#section-0414844283d745ae912e85f8ea14a51d}

Dit gebied staat u toe om de titel aan te passen die bij de bovenkant van de visualisatie wordt getoond. Door gebrek wordt de titel geplaatst aan **[!UICONTROL Automatic Title]**, die automatisch een titel voor het visualiseringsvenster zal produceren. Door de **[!UICONTROL Automatic Title]** knoop te ontruimen, kunt u om het even welke titel op dit gebied plaatsen. (Dit gebied is op alle visualisaties van toepassing.)

![](assets/title.png)

## Profiel {#section-16eb0def0a2d4eb289f5bb9200d14754}

In dit veld kunt u selecteren uit welk profiel u gegevens wilt visualiseren. Het klikken op het dropdown menu zal u van een lijst van profielen voorzien waarvoor u toegang hebt. (Dit gebied is niet toepasselijk voor de Rijke visualisaties van de Tekst.)

De profielen zijn gegevensreeksen die binnen de werkbank van Gegevens worden bepaald die gegevens over een bepaald domein, samen met de afmetingen, de metriek, en de filters bevatten die de gegevens begeleiden. Een profiel wordt vaak ontworpen om een specifiek doel (zoals marketing of websiteverkeer) te vervullen.

>[!NOTE]
>
>U kunt slechts de profielen zien waarvoor u toegang hebt gekregen. Voor meer informatie zie de Controles van de Toegang.

![](assets/profile.png)

## Afmetingen {#section-4ebb8c4308a146c3a35c7ac7ab6b579f}

Laat de dimensie selecteren u zou willen visualiseren. De lijst is ingevuld in de lijst met afmetingen die beschikbaar is in het profiel dat is geselecteerd in het veld Profiel. Klik op de gewenste afmeting en klik dan de Uitgezochte knoop. (Dit gebied is niet toepasselijk voor de Metrische Legende en Rijke visualisaties van de Tekst.)

De afmetingen zijn categorieën van gelijkaardige gegevenstypes. Bijvoorbeeld, zijn de Dagen van Week dimensie samengesteld uit de volgende gegevenselementen: Zondag, Maandag, Dinsdag, Woensdag, Donderdag, Vrijdag, en Zaterdag. De afmetingen tonen wat wordt gemeten.

![](assets/dimension.png)

## Metrisch(e) {#section-7d46f2f1b9fe4e539b5eb0a0dc6e5ad3}

Laat u de metriek selecteren om te visualiseren. De metriek zijn kwantitatieve voorwerpen en door één of andere kwantificeerbare uitdrukking bepaald. Bijvoorbeeld, worden de Meningen van de Pagina per Zitting afgeleid uit de uitdrukking van de telling van de Meningen van de Pagina die door de telling van Zittingen worden verdeeld. De metriek beantwoorden de vraag van &quot;hoeveel?&quot;

De enig-metrische visualisaties hebben een enig-metrisch selectievenster:

![](assets/metrics2.png)

De multimetrische visualisaties hebben een multi-metrisch selectievenster:

![](assets/metrics.png)

De lijst is bevolkt van de lijst van metriek beschikbaar bij het profiel dat op het gebied van het Profiel wordt geselecteerd.

Klik op de gewenste metriek en klik dan **[!UICONTROL Select]**. (Dit gebied is niet toepasselijk voor de Rijke visualisaties van de Tekst.)

## Filters {#section-f8619ae2f8e54735a2c1b0fbb8bb1281}

Selecteer de filters u op uw visualisatie zou willen toepassen. Het venster van de filterselectie staat u toe om veelvoudige filters van de filterlijst te selecteren. De lijst is bevolkt van de lijst van filters beschikbaar bij het profiel dat op het gebied van het Profiel wordt geselecteerd. Klik op de gewenste filter en klik dan **[!UICONTROL Select]**.

>[!NOTE]
>
>De filters die hier worden toegepast worden slechts toegepast op hun overeenkomstige visualisatie, niet het volledige dashboard. Dit is nuttig om de resultaten van twee verschillende visualisaties met verschillende toegepaste filters te vergelijken.

![](assets/filter.png)

## Tops weergeven {#section-7ce71cb0fa6446998b710b427e68b133}

De visualisaties in het dashboard worden niet ontworpen om de volledige gegevens te tonen. Eerder, staan zij u toe om het aantal afmetingsverslagen te specificeren u op de visualisatie zou willen tonen. Dit toont het hoogste aantal afmetingen afhankelijk van de hieronder vermelde soort-door waarde. (Dit gebied is niet toepasselijk voor Lijsten, de Metrische Legende, en de Rijke visualisaties van de Tekst.)

![](assets/display_top.png)

## Sorteren op {#section-f686249e20444359bff87c00cc2ba29f}

Dit staat u toe om te specificeren hoe de gegevens zouden moeten worden gesorteerd wanneer het binnen de visualisatie wordt getoond. (Dit gebied is niet toepasselijk voor Lijsten, de Metrische Legende, en de Rijke visualisaties van de Tekst.) Er zijn veelvoudige sorteeropties:

* **[!UICONTROL Default]** - Terugkeer de gegevens ongesorteerd die op de soortorde worden gebaseerd die in gegevenswerkbank wordt opgeslagen. Dit is de optie voor op tijd-gebaseerde gegevens zoals uur, dag, week, of maand te gebruiken.
* **[!UICONTROL Dimension]** - Sorteer de gegevens die op de alfanumerieke afmetingswaarde worden gebaseerd.
* **[!UICONTROL Metric]** - Sorteer de gegevens die op de metrische waarde worden gebaseerd en is goed voor snel het visualiseren van de hoogste afmetingen.
* **[!UICONTROL Descending]** - Sorteer de gegevens in dalende orde.
* **[!UICONTROL Ascending]** - Sorteer de gegevens in oplopende volgorde.

![](assets/sort_by.png)

## Tijdsperiode {#section-6220368e9e524b46ac735add6ab9edb0}

Deze visualisatie staat u toe om de gewenste begin en/of einddatum van de gegevens te specificeren om binnen de visualisatie te tonen.

Het selecteren **[!UICONTROL All Dates]**toont de volledige datumwaaier beschikbaar in het profiel.

Het selecteren **[!UICONTROL Range]** toont slechts de gegevens die binnen een gespecificeerde waaier vallen. Om de datumwaaier in te gaan, kunt u in de begin en/of einddatum typen, of een kalenderinput gebruiken door het kalenderpictogram te selecteren.

(Dit gebied is niet toepasselijk voor de Rijke visualisaties van de Tekst.)

>[!NOTE]
>
>De waaiers van de datum die hier worden toegepast worden slechts toegepast op hun overeenkomstige visualisatie, niet het volledige dashboard. Dit is nuttig om de resultaten van twee verschillende visualisaties met verschillende toegepaste datumwaaiers te vergelijken.

![](assets/time_period.png)

