---
description: U kunt selecties aanbrengen in procesafbeeldingen om filters te maken die gegevens bevatten of uitsluiten die aan een bepaald knooppunt zijn gekoppeld.
title: Een selectie maken op basis van een proceskaart
uuid: 7fd00090-c9ab-4bb6-8584-7de7b6f4b68c
exl-id: 8ede395f-906a-49e0-8ff8-b43a326275e5
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '393'
ht-degree: 0%

---

# Een selectie maken op basis van een proceskaart{#make-a-selection-from-a-process-map}

{{eol}}

U kunt selecties aanbrengen in procesafbeeldingen om filters te maken die gegevens bevatten of uitsluiten die aan een bepaald knooppunt zijn gekoppeld.

Het maken van een selectie binnen een proceskaart impliceert de de groepsdimensie van de kaart, die bepaalt hoe de elementen van de basisdimensie (namelijk de knopen in uw kaart) worden gegroepeerd om de verbindingen tussen knopen te vormen.

>[!NOTE]
>
>U kunt de standaardgroepsdimensie voor een proceskaart veranderen. Zie [Proceskaarten configureren](../../../../home/c-get-started/c-intf-anlys-ftrs/t-config-proc-maps.md#task-4a95730b18a14bc790a77c013832b2d6).

Wanneer u een selectie maakt die op een knoop binnen een proceskaart wordt gebaseerd, selecteert u alle elementen van de groepsdimensie die dat knoop impliceert. Neem de volgende voorbeelden om de rol van de groepsdimensie beter te begrijpen:

* Films kunnen worden gegroepeerd door de viewers die ze hebben beoordeeld. Elke kijker is een element van de dimensie van de Gebruiker, zodat zou de dimensie van de Gebruiker de groepsdimensie voor de proceskaart zijn. Wanneer u een selectie maakt van een knooppunt voor een bepaalde film, maakt u een filter dat gegevens weergeeft voor de gebruikers die de film wel of niet hebben beoordeeld.
* Websitepagina&#39;s kunnen worden gegroepeerd door de sessies waarin ze zijn weergegeven. Elke zitting is een element van de dimensie van de Zitting, zodat zou de dimensie van de Zitting de groepsdimensie voor de proceskaart zijn. Wanneer u een selectie maakt van een knooppunt voor een bepaalde pagina, maakt u een filter dat gegevens weergeeft voor de sessies waarin die pagina al dan niet is weergegeven.

**Een selectie maken**

1. Klik met de rechtermuisknop op een knooppunt in een proceskaart.
1. Klik op een van de volgende opties om een selectie te maken op basis van het knooppunt:

   * **[!UICONTROL Select]*** **[!UICONTROL group dimension name +s]*** **[!UICONTROL through node name]**: Filters de gegevens om alle elementen van de groepsdimensie te omvatten die door de knoop door het filtreren uit alle zittingen overgegaan die niet door de knoop hebben overgegaan.

   * **[!UICONTROL Select]*** **[!UICONTROL group dimension name +s]*** **[!UICONTROL NOT through node name]**: Filtert de gegevens om alle elementen van de groepsdimensie te omvatten die niet door de knoop door te filtreren uit alle zittingen die door de knoop overgaan.

![](assets/vis_2DProcessMap_Selections_Movie.png)

![](assets/vis_2DProcessMap_Selections_Page.png)

Wanneer u een selectie maakt in een 3D-procesafbeelding, wordt het knooppunt omcirkeld waarvoor de selectie is gemaakt. Met behulp van benchmarks rond elke balk kunt u metrische waarden met en zonder selectie vergelijken. Zie [Benchmarks begrijpen](../../../../home/c-get-started/c-vis/c-ustd-benchmks.md#concept-c7b0f4102e92458096f8c4765cbe2914).

![](assets/vis_3DProcessMap_Selection.png)
