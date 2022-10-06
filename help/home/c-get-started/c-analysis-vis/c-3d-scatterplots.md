---
description: Een 3D-spreidingsgrafiek geeft de elementen van een gegevensdimensie (zoals dagen of Referral-site) weer op een driedimensionaal raster waar de x-, y- en z-as verschillende metriek vertegenwoordigen.
title: 3D-verstrooiingspunten
uuid: 5e23547c-dbb4-490c-94bc-0731deee612e
exl-id: 18f18cab-a31b-4ffe-89c5-412a5645af2e
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '500'
ht-degree: 0%

---

# 3D-verstrooiingspunten{#d-scatter-plots}

{{eol}}

Een 3D-spreidingsgrafiek geeft de elementen van een gegevensdimensie (zoals dagen of Referral-site) weer op een driedimensionaal raster waar de x-, y- en z-as verschillende metriek vertegenwoordigen.

Zoals de [Spreidingspad 2D](https://experienceleague.adobe.com/docs/data-workbench/using/client/t-open-ins.html#Scatter_Plots)Deze visualisatie is nuttig wanneer u probeert de relatie te begrijpen tussen grote aantallen ongelijke items die verschillende maatstaven gebruiken.

**U kunt als volgt de visualisatie voor 3D-spreidingspunten gebruiken:**

1. Open een nieuwe werkruimte.

   Nadat u een nieuwe werkruimte hebt geopend, moet u mogelijk op **Toevoegen** > **Tijdelijk ontgrendelen**.
1. Klik met de rechtermuisknop en selecteer **Visualisatie** > **3D-spreidingspad**.

   Een menulijst **[!UICONTROL Dimensions]** wordt geopend.

1. Selecteer een dimensie voor de vraag.

   Met het 3D-spotje worden de standaardmeetgegevens voor die dimensie geopend.

   ![](assets/3D_main.png)

   Het selecteren van **[!UICONTROL Days]** geeft het volgende 3D-diagram met deze standaardmeetwaarden weer op de volgende assen: **[!UICONTROL x=Visits]**, **[!UICONTROL y=Retention]**, en **[!UICONTROL z=Visits]**.

1. Metriek wijzigen. Klik met de rechtermuisknop op het metrische label in de x-, y- of z-as en selecteer **[!UICONTROL Change Metric]**. Selecteer vervolgens een andere metrische waarde voor de geselecteerde as.

   ![](assets/3D_change.png)

   >[!IMPORTANT]
   >
   >
   >    
   >    
   >    * Sleep metrisch aan één van de drie asetiketten en laat vallen het om de geselecteerde as in gelaten vallen metrisch te veranderen.
   >    * Sleep metrisch overal anders op visualisatie en laat vallen het om straal metrisch voor die as te veranderen.
   >    * Sleep een dimensie naar een willekeurige locatie op de visualisatie en zet deze neer om de dimensie voor de visualisatie te wijzigen.


1. Wijzig de Straal. Klik met de rechtermuisknop op de titel boven aan de pagina (na de geselecteerde dimensie) en selecteer **[!UICONTROL Change Radius Metric]**.

   De straalmetrische waarde bepaalt de grootte van het geplot punt dat op de metrische selectie wordt gebaseerd. De relatieve positie van punten verandert niet in het verstrooiingsperceel, maar de uitgezette puntgrootten binnen de visualisatie nemen toe op basis van de metrische waarde.

   ![](assets/3D_change_radius.png)

1. De **[!UICONTROL Orthographic Camera]**. Met deze optie kunt u de uitgezette punten identificeren in verhouding tot hun werkelijke perspectief op basis van de meetstraal om driedimensionale vervorming te voorkomen.

   Wanneer het 3D-spreidingspad voor het eerst wordt weergegeven, wordt het weergegeven in een driedimensionale draaiende projectie, die enige vervorming veroorzaakt voor punten die dichter bij het perspectief worden geplaatst, of in een virtuele &quot;camera&quot;. (De plots die zich dichter bij de camera bevinden, worden veel groter weergegeven dan de punten die verder van de camera worden geroteerd.)

   Als u deze perspectiefvervorming wilt voorkomen, selecteert u de optie **[!UICONTROL Orthographic Camera]** door met de rechtermuisknop op de titel te klikken en in het menu te selecteren. Hierdoor kunt u de driedimensionale objecten in tweedimensionale dimensies weergeven. Hierdoor worden de uitgezette punten als vlak weergegeven en worden de punten ten opzichte van de straal weergegeven, waarbij de driedimensionale verschuivingen worden verminderd.

1. Selecteer punten in het spreidingsperceel.

   * **Een punt of groep punten verwijderen**: Klik op het punt.
   * **Een ander punt of een groep punten toevoegen aan de selectie**: **Ctrl** + **klikken** een punt of **Ctrl** + **slepen** over meerdere punten.

   * **Een punt of groep punten uit de selectie verwijderen**: **Shift** + **klikken** een punt of **Shift** **+** **slepen** op verschillende punten.

<!-- <a id="section_9C30F9799F1440F09278327002E6B47A"></a> -->
