---
description: U kunt selecties binnen proceskaarten maken om filters tot stand te brengen die omvatten of gegevens uitsluiten verbonden aan een bepaalde knoop.
solution: Analytics
title: Maak een selectie van een proceskaart
topic: Data workbench
uuid: 7fd00090-c9ab-4bb6-8584-7de7b6f4b68c
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Maak een selectie van een proceskaart{#make-a-selection-from-a-process-map}

U kunt selecties binnen proceskaarten maken om filters tot stand te brengen die omvatten of gegevens uitsluiten verbonden aan een bepaalde knoop.

Het maken van een selectie binnen een proceskaart impliceert de de groepsdimensie van de kaart, die bepaalt hoe de elementen van de basisdimensie (namelijk de knopen in uw kaart) worden gegroepeerd om de verbindingen tussen knopen te vormen.

>[!NOTE]
>
>U kunt de standaardgroepsdimensie voor een proceskaart veranderen. Zie [het Vormen de Kaarten](../../../../home/c-get-started/c-intf-anlys-ftrs/t-config-proc-maps.md#task-4a95730b18a14bc790a77c013832b2d6)van het Proces.

Wanneer u een selectie maakt die op een knoop binnen een proceskaart wordt gebaseerd, selecteert u alle elementen van de groepsdimensie die die knoop impliceerde. Om de rol van de groepsdimensie beter te begrijpen, overweeg de volgende voorbeelden:

* De films kunnen door de kijkers worden gegroepeerd die hen schatten. Elke kijker is een element van de dimensie van de Gebruiker, zodat zou de dimensie van de Gebruiker de groepsdimensie voor de proceskaart zijn. Wanneer u een selectie van een knoop voor een bepaalde film maakt, creeert u een filter die gegevens voor de gebruikers toont die of niet die film geloofden.
* De pagina&#39;s van de website kunnen door de zittingen worden gegroepeerd waarin zij werden bekeken. Elke zitting is een element van de dimensie van de Zitting, zodat zou de dimensie van de Zitting de groepsdimensie voor de proceskaart zijn. Wanneer u een selectie van een knoop voor een bepaalde pagina maakt, creeert u een filter die gegevens voor de zittingen toont waarin die pagina was of niet werd bekeken.

**Om een selectie te maken**

1. Klik om het even welke knoop in een proceskaart met de rechtermuisknop aan.
1. Klik één van de volgende opties om een selectie te maken die op de knoop wordt gebaseerd:

   * **[!UICONTROL Select]*** **[!UICONTROL group dimension name +s]*** **[!UICONTROL through node name]**: Filtert de gegevens om alle elementen van de groepsdimensie te omvatten die door de knoop door alle zittingen overging te filtreren die niet door de knoop overgingen.

   * **[!UICONTROL Select]*** **[!UICONTROL group dimension name +s]*** **[!UICONTROL NOT through node name]**: Filters de gegevens om alle elementen van de groepsdimensie te omvatten die niet door de knoop door uit te filtreren alle zittingen overgingen die door de knoop overgingen.

![](assets/vis_2DProcessMap_Selections_Movie.png)

![](assets/vis_2DProcessMap_Selections_Page.png)

Wanneer u een selectie in een 3D proceskaart maakt, wordt de knoop waarvoor de selectie wordt gemaakt omcirkeld. De benchmarks verschijnen rond elke bar hulp u metrische waarden met en zonder de selectie vergelijkt. Zie Benchmarks [begrijpen](../../../../home/c-get-started/c-vis/c-ustd-benchmks.md#concept-c7b0f4102e92458096f8c4765cbe2914).

![](assets/vis_3DProcessMap_Selection.png)

