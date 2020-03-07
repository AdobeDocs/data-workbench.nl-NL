---
description: U kunt aantekenvellen gebruiken om erop te wijzen dat metrisch een bepaalde drempel heeft bereikt.
solution: Analytics
title: Creeer een metrische indicator
topic: Data workbench
uuid: da304004-ef45-4c89-8c91-dd5158172dd6
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Creeer een metrische indicator{#create-a-metric-indicator}

U kunt aantekenvellen gebruiken om erop te wijzen dat metrisch een bepaalde drempel heeft bereikt.

Bovendien kunt u gebruiken [!DNL Report] om een rapport automatisch te produceren en te verdelen wanneer metrisch een bepaalde drempel binnen een gespecificeerd tijdkader bereikt.

Voor meer informatie over [!DNL Report], zie de Gids *van het Rapport van het Rapport van de* Werkbank van Gegevens.

* [Indicator omhoog of omlaag](../../../../home/c-get-started/c-analysis-vis/c-wksts/c-metric-ind.md#section-40d7a2c3df0d40d4a7bb1a7e856abcba)
* [Controle-indicator](../../../../home/c-get-started/c-analysis-vis/c-wksts/c-metric-ind.md#section-98c5298a74f34dcbaaf151549fcc7090)

**Om een metrische indicator te creëren die een aantekenvel gebruikt**

1. Bepaal de inhoud van de cellen van het aantekenvel.

   1. In Kolom A, ga de naam van gewenste metrisch (bijvoorbeeld, [!DNL Visitors]) in.
   1. In Kolom B, ga de waarde van gewenste metrisch (bijvoorbeeld, [!DNL =Visitors]) in.
   1. In Kolom C, ga de lage drempel van metrisch in.
   1. In Kolom D, ga de hoge drempel van metrisch in.
   1. In kolom E, ga een aangewezen formule in. Bijvoorbeeld, zie [omhoog of onderaan Indicator](../../../../home/c-get-started/c-analysis-vis/c-wksts/c-metric-ind.md#section-40d7a2c3df0d40d4a7bb1a7e856abcba) of de Indicator [van de](../../../../home/c-get-started/c-analysis-vis/c-wksts/c-metric-ind.md#section-98c5298a74f34dcbaaf151549fcc7090)Controle.
   1. In de formulecel (Kolom E), klik met de rechtermuisknop aan en klik **[!UICONTROL Format]** > **[!UICONTROL Indicator]**, dan klik één van het volgende:

      * **[!UICONTROL None]**: Maakt een lijst van de nauwkeurige berekening in plaats van een indicator.
      * **[!UICONTROL Check]**: Gebruikt een vinkje of een X om erop te wijzen dat de waarde of boven of onder de drempel is u, afhankelijk van uw formule plaatst. Zie Indicator [controleren](../../../../home/c-get-started/c-analysis-vis/c-wksts/c-metric-ind.md#section-98c5298a74f34dcbaaf151549fcc7090).
      * **[!UICONTROL Up or Down]**: Gebruikt een naar boven of naar onder pijl om erop te wijzen of de waarde onder de lage drempel (benedenpijl), boven de hoge drempel (omhoog pijl), of tussen de lage en hoge drempels (leeg) is. Zie Indicator [omhoog of omlaag](../../../../home/c-get-started/c-analysis-vis/c-wksts/c-metric-ind.md#section-40d7a2c3df0d40d4a7bb1a7e856abcba).

1. Herhaal Stap 1 voor andere metriek waarvoor u indicatoren wilt tot stand brengen.

Het resulterende aantekenvel zou iets als het volgende voorbeeld kijken:

![](assets/vis_Worksheet_Alerts.png)

## Indicator omhoog of omlaag {#section-40d7a2c3df0d40d4a7bb1a7e856abcba}

Voor de [!DNL Up] of [!DNL Down indicator]de volgende formule gebruiken:

[!DNL (metric value - low threshold)/(high threshold - low threshold)*2 - 1]

Bijvoorbeeld: [!DNL =(b2-c2)/(d2-c2)*2-1]

Drie resultaten zijn mogelijk voor elke metrisch wanneer het gebruiken van deze formule met [!DNL Up] of [!DNL Down indicator]:

* Als de metrische waarde tussen de lage en hoge drempels is, evalueert de formule aan een aantal tussen -1 en 1 (uitsluitend). De naar boven of naar onder pijl tonen niet in het aantekenvel.
* Als de metrische waarde minder dan of gelijk aan de lage drempel is, evalueert de formule aan een waarde minder dan of gelijk aan -1. De metrische indicator verandert in een benedenpijl.
* Als de metrische waarde groter dan of gelijk aan de hoge drempel is, evalueert de formule aan een aantal groter dan of gelijk aan 1. De metrische indicator verandert in een omhooggaande pijl.

Het volgende aantekenvel illustreert wat de voorbeeldformule [!DNL =(b2-c2)/(d2-c2)*2-1] zou tonen:

![](assets/vis_Worksheet_Alerts_UpDown.png)

## Controle-indicator {#section-98c5298a74f34dcbaaf151549fcc7090}

Voor [!DNL Check indicator], gebruikt u een formule die erop wijst of u wilt worden op de hoogte gebracht wanneer de metrische waarde boven of onder de drempel is u specificeert. Bijvoorbeeld:

* Als u op de hoogte wilt worden gebracht wanneer de waarde onder de drempel is u plaatst, kon u het volgende formaat gebruiken:

   * [!DNL threshold - metric]

      Bijvoorbeeld: [!DNL =(c2-b2)]

* Als u wilt worden op de hoogte gebracht wanneer de waarde boven de drempel is u plaatst, kon u de volgende formule gebruiken:

   * [!DNL metric - threshold]

      Bijvoorbeeld: [!DNL =(b3-c3)]

Wanneer een vinkje toont, evalueerde de formule aan een positief aantal. Wanneer X toont, evalueerde de formule aan een negatief aantal.

Er zijn twee mogelijke resultaten voor elke metrisch wanneer het gebruiken van [!DNL Check indicator]:

* Als de formule erop wijst dat het houden van de metrische waarde boven de drempel wenselijk is, toont een vinkje wanneer de metrische waarde groter dan of gelijk aan de drempel is, en de vertoningen van X wanneer de waarde minder dan de drempel is.
* Als de formule erop wijst dat het houden van de metrische waarde onder de drempel wenselijk is, toont een vinkje wanneer de metrische waarde minder dan of gelijk aan de drempel is, en de vertoningen van X wanneer de waarde groter is dan de drempel.

Het volgende aantekenvel illustreert wat de voorbeeldformules [!DNL =(c2-b2)] en [!DNL =(b3-c3)] zou tonen:

![](assets/vis_Worksheet_Alerts_Check.png)

