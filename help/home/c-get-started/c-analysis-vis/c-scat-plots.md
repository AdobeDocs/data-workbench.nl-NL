---
description: Verstrooiingspunten geven de elementen van een gegevensdimensie (zoals Pagina of Stad) weer op een raster waarin de x- en y-as verschillende meetwaarden vertegenwoordigen.
title: 2D-spreidingspunten
uuid: 73c23d22-3c3a-4535-b66b-0e3508bd904c
exl-id: 340f8c18-ce47-4f3a-aba4-3d6124505313
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '366'
ht-degree: 0%

---

# 2D-spreidingspunten{#d-scatter-plots}

{{eol}}

Verstrooiingspunten geven de elementen van een gegevensdimensie (zoals Pagina of Stad) weer op een raster waarin de x- en y-as verschillende meetwaarden vertegenwoordigen.

Verstrooiingspunten kunnen nuttig zijn wanneer u de relatie probeert te begrijpen tussen grote aantallen ongelijksoortige items, door twee verschillende meeteenheden. In het volgende voorbeeld toont het spreidingsperceel elke stad aan de hand van het aantal bezoekers en de respectieve retentiepercentages.

![](assets/vis_ScatterPlot_City.png)

Met het spreidingsperceel kunt u de uitschieters snel zien. Zout Lake City heeft bijvoorbeeld een hogere retentieresnelheid dan gemiddeld per bezoeker.

U kunt ook spreidingspercelen gebruiken om de consistentie van gegevens aan te tonen. In het volgende voorbeeld wordt in het spreidingsperceel het aantal bezoekers met sessies van een bepaalde lengte weergegeven.

![](assets/vis_ScatterPlot_SessionDuration.png)

De grootte van elk punt op het verstrooiingsperceel wordt bepaald door de meetstraal. De standaardstraalmetrisch verschilt voor elke toepassing van Adobe. Bijvoorbeeld in [!DNL Site], metrische straal is gebaseerd op zittingen door gebrek. U kunt de metrische straal wijzigen zodat de punten in de spreidingsgebieden elke beschikbare metrische waarde vertegenwoordigen. Ga voor meer informatie naar [Straalmetriek wijzigen](../../../home/c-get-started/c-analysis-vis/c-scat-plots.md#section-fd80576d583c430cb469daf12e39aa2a) De kleur van de punten is gebaseerd op de kleurlegenda die binnen de werkruimte is geopend. Zie voor meer informatie over legenda [Kleurlegenda](../../../home/c-get-started/c-analysis-vis/c-legends/c-color-leg.md#concept-f84d51dc0d6547f981d0642fc2d01358).

## Punten selecteren {#section-4b4d45f39b884d54bb7407b3b2f4ea50}

**Eén punt selecteren**

* Klik op het punt.

**Een ander punt of een groep punten toevoegen aan de selectie**

* Houd Ctrl ingedrukt en klik op een punt of houd Ctrl ingedrukt en sleep over meerdere punten.

**Een punt of groep punten uit de selectie verwijderen**

* Houd Shift ingedrukt en klik op een punt of houd Shift ingedrukt en sleep over verschillende punten.

## Afmetingen wijzigen {#section-796cd962ef3f476caa89d99083782ed1}

* Klik met de rechtermuisknop op het label van de dimensie boven aan de grafiek en klik op **[!UICONTROL Change Dimension]** > *&lt;**[!UICONTROL dimension name]**>*.

## Metriek wijzigen {#section-44b8be9215cd4039b1eeb98ae1b31445}

**De metrische waarde wijzigen die wordt weergegeven op de x- of y-as van een spreidingsperceel**

* Klik met de rechtermuisknop op het label van de metrische waarde die u wilt wijzigen en klik op **[!UICONTROL Change Metric]** > *&lt;**[!UICONTROL metric name]**>*.

## Metrische gegevens van straal wijzigen {#section-fd80576d583c430cb469daf12e39aa2a}

**De straal van een spreidingsperceel wijzigen**

Klik met de rechtermuisknop op het label van de dimensie boven aan de grafiek en klik op **[!UICONTROL Change Radius Metric]** > *&lt;**[!UICONTROL metric name]**>*.

![](assets/mnu_ScatterPlot_Change.png)
