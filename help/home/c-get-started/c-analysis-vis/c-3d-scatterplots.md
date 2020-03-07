---
description: Een 3D Plot van de Drager grafieken de elementen van een gegevensdimensie (zoals Dagen of de Plaats van de Verwijzing) op een driedimensionaal net waar de x, y, en z assen diverse metriek vertegenwoordigen.
solution: Analytics
title: 3D-sccatterpercelen
topic: Data workbench
uuid: 5e23547c-dbb4-490c-94bc-0731deee612e
translation-type: tm+mt
source-git-commit: 2e4991206394ca0c463210990ea44dfb700341a5

---


# 3D-sccatterpercelen{#d-scatter-plots}

Een 3D Plot van de Drager grafieken de elementen van een gegevensdimensie (zoals Dagen of de Plaats van de Verwijzing) op een driedimensionaal net waar de x, y, en z assen diverse metriek vertegenwoordigen.

Net als het [Scatter Plot 2D](https://docs.adobe.com/content/help/en/data-workbench/using/client/t-open-ins.html#Scatter_Plots), is deze visualisatie handig wanneer je probeert de relatie te begrijpen tussen grote aantallen ongelijksoortige items die verschillende maatstaven gebruiken.

**Om de visualisatie van het 3D Scatter Plot aan te wenden:**

1. Open een nieuwe werkruimte.

   Na het openen van een nieuwe werkruimte, kunt u moeten klikken **toevoegt** > **tijdelijk opent**.
1. Klik met de rechtermuisknop en selecteer **Visualisatie** > **3D Scatter Plot**.

   Een menulijst **[!UICONTROL Dimensions]** wordt geopend.

1. Selecteer een dimensie voor de vraag.

   Het 3D Plot van de Scatter zal de standaardmetriek voor die dimensie openen.

   ![](assets/3D_main.png)

   Het selecteren van het **[!UICONTROL Days]** menu toont het volgende 3D Plot van de Scatter met deze standaardmetriek op de volgende assen: **[!UICONTROL x=Visits]**, **[!UICONTROL y=Retention]**, en **[!UICONTROL z=Visits]**.

1. De metriek van de verandering. Klik op het metrische etiket in de x, y, of zas met de rechtermuisknop aan en selecteer **[!UICONTROL Change Metric]**. Dan selecteer verschillende metrisch voor de geselecteerde as.

   ![](assets/3D_change.png)

   >[!IMPORTANT]
   >
   >
   >    
   >    
   >    * Sleep metrisch aan één van de drie asetiketten en laat vallen het om de geselecteerde as in gelaten vallen metrisch te veranderen.
   >    * Sleep overal metrisch anders op de visualisatie en laat vallen het om de straal metrisch voor die as te veranderen.
   >    * Sleep een afmeting aan overal op de visualisatie en laat vallen het om de afmeting voor de visualisatie te veranderen.


1. Verander de metrische Straal. Klik de titel bij de bovenkant van de pagina met de rechtermuisknop aan (titel na de geselecteerde afmeting) en selecteer **[!UICONTROL Change Radius Metric]**.

   De metrische straal bepaalt de grootte van het plotselinge punt dat op de metrische selectie wordt gebaseerd. De relatieve positie van de punten verandert niet in het verspreidingsperceel, maar de uitgezette puntgrootte binnen de visualisatieverhoging op basis van de metrische waarde.

   ![](assets/3D_change_radius.png)

1. Gebruik de **[!UICONTROL Orthographic Camera]**. Deze optie laat u de plotselinge punten met betrekking tot hun ware perspectief identificeren dat op de metrische straal wordt gebaseerd om driedimensionale vervorming te vermijden.

   Wanneer het 3D-scatterdiagram voor het eerst wordt weergegeven, wordt het weergegeven in een driedimensionale roterende projectie, die enige vervorming veroorzaakt voor punten die dichter bij het perspectief worden uitgezet, of een virtuele &quot;camera&quot;. (De percelen dichtbij de camera verschijnen veel groter dan de punten die verder van de camera roteren.)

   Om deze perspectiefvervorming te vermijden, kunt u de **[!UICONTROL Orthographic Camera]** optie selecteren door op de titel met de rechtermuisknop te klikken en van het menu te selecteren. Dit staat u toe om de driedimensionale voorwerpen in twee-afmetingen te vertegenwoordigen. Dit geeft de plotselinge punten als vlak terug en toont de punten met betrekking tot metrische straal, verminderend de driedimensionale compensatie.

1. Selecteer punten van het verspreidingsplot.

   * **Om een punt of een groep punten** te verwijderen: Klik op het punt.
   * **Om een ander punt of een groep punten aan uw selectie** toe te voegen: **CTRL** + **klik** een punt of **CTRL** + **belemmering** over veelvoudige punten.

   * **Om een punt of een groep punten uit uw selectie** te verwijderen: **Verschuiving** + **klik** een punt of **Verschuiving** **+** **belemmering** over verscheidene punten.

<!-- <a id="section_9C30F9799F1440F09278327002E6B47A"></a> -->

