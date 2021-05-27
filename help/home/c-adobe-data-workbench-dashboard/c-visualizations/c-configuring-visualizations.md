---
description: Toont hoe te om Titel, Profiel, Dimension, Metrisch, Filter, de Boven van de Vertoning, Soort door, en Periode te vormen.
title: Visualisaties configureren
uuid: aca77188-8f28-4554-8913-412b252f688c
exl-id: 153adf94-5689-4917-9d71-625caef49903
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '795'
ht-degree: 0%

---

# Visualisaties configureren{#configuring-visualizations}

Toont hoe te om Titel, Profiel, Dimension, Metrisch, Filter, de Boven van de Vertoning, Soort door, en Periode te vormen.

Elke visualisatie op het dashboardcanvas heeft zijn eigen configuratie. Wanneer een visualisatie voor het eerst aan het dashboardcanvas wordt toegevoegd, wordt het bijbehorende configuratievenster automatisch weergegeven. Zodra gevormd, kan de visualisatie op elk ogenblik worden gewijzigd door het tandwielpictogram in het hogere juiste gedeelte van het visualisatievenster te klikken.

>[!NOTE]
>
>De configuratieopties variëren enigszins afhankelijk van het type visualisatie dat wordt weergegeven.

## Visualisatietitel {#section-0414844283d745ae912e85f8ea14a51d}

In dit veld kunt u de titel aanpassen die boven aan de visualisatie wordt weergegeven. De titel wordt standaard ingesteld op **[!UICONTROL Automatic Title]**, waardoor automatisch een titel voor het visualisatievenster wordt gegenereerd. Door de **[!UICONTROL Automatic Title]** knoop te ontruimen, kunt u om het even welke titel op dit gebied plaatsen. (Dit veld is van toepassing op alle visualisaties.)

![](assets/title.png)

## Profiel {#section-16eb0def0a2d4eb289f5bb9200d14754}

In dit veld kunt u selecteren uit welk profiel u de gegevens wilt visualiseren. Als u op het vervolgkeuzemenu klikt, krijgt u een lijst met profielen waartoe u toegang hebt. (Dit veld is niet van toepassing op RTF-visualisaties.)

Profielen zijn gegevenssets die zijn gedefinieerd in de Data Workbench en die gegevens bevatten over een bepaald domein, samen met de afmetingen, metriek en filters die bij de gegevens horen. Een profiel wordt vaak ontworpen om een specifiek doel (zoals marketing of websiteverkeer) te vervullen.

>[!NOTE]
>
>U kunt alleen de profielen zien waarvoor u toegang hebt gekregen. Voor meer informatie zie de Controles van de Toegang.

![](assets/profile.png)

## Dimension {#section-4ebb8c4308a146c3a35c7ac7ab6b579f}

Hiermee selecteert u de dimensie die u wilt visualiseren. De lijst wordt gevuld vanuit de lijst met afmetingen die beschikbaar is via het profiel dat is geselecteerd in het veld Profiel. Klik op de gewenste dimensie en klik vervolgens op de knop Selecteren. (Dit veld is niet van toepassing op weergaven van metrische legenda en RTF.)

Dimension zijn categorieën van soortgelijke gegevenstypen. De dimensie Dagen van week bestaat bijvoorbeeld uit de volgende gegevenselementen: Zondag, maandag, dinsdag, woensdag, donderdag, vrijdag, en zaterdag. Dimension laten zien wat er wordt gemeten.

![](assets/dimension.png)

## Metrisch(e) {#section-7d46f2f1b9fe4e539b5eb0a0dc6e5ad3}

Hiermee kunt u de meetgegevens selecteren die u wilt visualiseren. Metrische waarden zijn kwantitatieve objecten die worden gedefinieerd door een kwantificeerbare expressie. Paginaweergaven per sessie worden bijvoorbeeld afgeleid van de expressie van het aantal paginaweergaven gedeeld door het aantal sessies. Metrics beantwoorden de vraag &quot;hoeveel?&quot;

Single-Metrische visualisaties hebben een enig-metrisch selectievenster:

![](assets/metrics2.png)

Multimetrische visualisaties hebben een multi-metrisch selectievenster:

![](assets/metrics.png)

De lijst wordt gevuld vanuit de lijst met beschikbare metriek van het profiel dat is geselecteerd in het veld Profiel.

Klik op de gewenste metriek en klik dan **[!UICONTROL Select]**. (Dit veld is niet van toepassing op RTF-visualisaties.)

## Filters {#section-f8619ae2f8e54735a2c1b0fbb8bb1281}

Selecteer de filters die u op uw visualisatie wilt toepassen. In het venster met filterselectie kunt u meerdere filters in de filterlijst selecteren. De lijst wordt gevuld met de lijst met filters die beschikbaar zijn via het profiel dat is geselecteerd in het veld Profiel. Klik op het gewenste filter en klik vervolgens op **[!UICONTROL Select]**.

>[!NOTE]
>
>Filters die u hier toepast, worden alleen toegepast op de bijbehorende visualisatie, niet op het hele dashboard. Dit is handig als u de resultaten van twee verschillende visualisaties wilt vergelijken met verschillende toegepaste filters.

![](assets/filter.png)

## Tops {#section-7ce71cb0fa6446998b710b427e68b133} weergeven

Visualisaties in het dashboard zijn niet ontworpen om alle gegevens weer te geven. In plaats daarvan kunt u hiermee het aantal dimensie-records opgeven dat u wilt weergeven op de visualisatie. Hierdoor wordt het bovenste aantal dimensies weergegeven, afhankelijk van de onderstaande sorteerwaarde. (Dit veld is niet van toepassing op tabellen, metrische legenda en RTF-visualisaties.)

![](assets/display_top.png)

## Sorteren op {#section-f686249e20444359bff87c00cc2ba29f}

Op deze manier kunt u opgeven hoe de gegevens moeten worden gesorteerd wanneer deze worden weergegeven in de visualisatie. (Dit veld is niet van toepassing op tabellen, metrische legenda en RTF-visualisaties.) Er zijn meerdere sorteeropties:

* **[!UICONTROL Default]** - Retourneer de gegevens ongesorteerd op basis van de sorteervolgorde die is opgeslagen in de gegevenswerkbank. Dit is de optie die u kunt gebruiken voor op tijd gebaseerde gegevens zoals uur, dag, week of maand.
* **[!UICONTROL Dimension]** - Sorteer de gegevens op basis van de waarde van de alfanumerieke dimensie.
* **[!UICONTROL Metric]** - Sorteer de gegevens op basis van de metrische waarde en is goed voor het snel visualiseren van de bovenste afmetingen.
* **[!UICONTROL Descending]** - Sorteer de gegevens in aflopende volgorde.
* **[!UICONTROL Ascending]** - Sorteer de gegevens in oplopende volgorde.

![](assets/sort_by.png)

## Tijdsperiode {#section-6220368e9e524b46ac735add6ab9edb0}

Met deze visualisatie kunt u de gewenste begin- en/of einddatum opgeven voor de gegevens die binnen de visualisatie worden weergegeven.

Als u **[!UICONTROL All Dates]**selecteert, wordt het volledige datumbereik weergegeven dat beschikbaar is in het profiel.

Als u **[!UICONTROL Range]** selecteert, worden alleen de gegevens weergegeven die binnen een opgegeven bereik vallen. Als u het datumbereik wilt invoeren, typt u de begin- en/of einddatum of gebruikt u een kalenderinvoer door het kalenderpictogram te selecteren.

(Dit veld is niet van toepassing op RTF-visualisaties.)

>[!NOTE]
>
>De hier toegepaste datumbereiken worden alleen toegepast op de bijbehorende visualisatie, niet op het hele dashboard. Dit is handig als u de resultaten van twee verschillende visualisaties wilt vergelijken met verschillende toegepaste datumbereiken.

![](assets/time_period.png)
