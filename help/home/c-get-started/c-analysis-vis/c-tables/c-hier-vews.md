---
description: De meningen van de hiërarchie zijn beschikbaar slechts wanneer het gebruiken van de Plaats of de toepassing HBX.
solution: Analytics
title: hiërarchieweergaven toepassen
topic: Data workbench
uuid: 859a92af-4f7e-4bb5-9a98-917006894301
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# hiërarchieweergaven toepassen{#apply-hierarchy-views}

De meningen van de hiërarchie zijn beschikbaar slechts wanneer het gebruiken van de Plaats of de toepassing HBX.

De hiërarchische die hiërarchisch door dossier wordt georganiseerd - noem en gesorteerd alfabetisch de hiërarchische vertoningen van de hiërarchiemening de pagina&#39;s in een website. Terwijl nuttig voor analyse zelf, kan de hiërarchiemening ook aan opstelling worden gebruikt dergelijke geavanceerde visualisaties zoals proceskaarten. Voor meer informatie over proceskaarten, zie de Kaarten van het [Proces](../../../../home/c-get-started/c-analysis-vis/c-proc-maps/c-proc-maps.md#concept-880aee224404429785b733a4e80d275e).

>[!NOTE]
>
>Als uw dataset is gevormd om op veelvoudige servers in een cluster te lopen, voor deze eigenschap om behoorlijk te werken, moet uw systeembeheerder aanwijzen welke machinefuncties als uw Centrale Server van de Normalisatie. Voor stappen om dit te doen, zie het hoofdstuk van het Dossier van de Configuratie van de Verwerking van het Logboek van de Gids *van de Configuratie van de* Dataset.

![](assets/vis_Table_CompareHierarchy.png)

**Om de hiërarchiemening toe te laten of onbruikbaar te maken**

* Van om het even welke pagina of de visualisatie van URI, klik een element of het etiket van de paginadimensie met de rechtermuisknop aan en klik **[!UICONTROL Hierarchy View]**.

   ![](assets/mnu_Table_HierarchyView.png)

   X wordt getoond naast de optie wanneer actief [!DNL hierarchy view] is.

   De hiërarchie wordt georganiseerd in websitesecties en pagina&#39;s gebruikend een boomstructuur. De secties (knopen) kunnen worden uitgebreid of worden gecondenseerd gebruikend + of - symbool naast de sectienaam. De individuele pagina&#39;s hebben geen + of - symbool naast hen.

   ![](assets/vis_Table_HierarchyView_Expanded.png)

## Het maskeren van de Elementen van de Dimensie in een Mening van de Hiërarchie {#section-e477c469934846da8d807f92fc2f3ed1}

Het maskeren verwijst naar het selecteren van een ondergroep van uw gegevens of een ondergroep van de elementen in een afmeting. U maskeert of verbergt die elementen die u niet inbegrepen in de analyse wilt. Gebruikend de [!DNL Mask] menuopties voor hiërarchiemeningen, selecteert u het minimumpercentage van metrisch dat een element in de visualisatie moet worden getoond.

**Om gegevens te maskeren die de[!DNL Mask]menuoptie gebruiken**

1. Klik een element of het etiket van de afmeting met de rechtermuisknop aan en klik **[!UICONTROL Mask]**.

   ![](assets/mnu_Table_HierarchyView_Masking.png)

1. Onder Meer dan, klik het aangewezen percentage, dan klik metrisch die u wilt maskeren.

Bijvoorbeeld, als u 0.1% klikt, en dan de Meningen van de Pagina klikt, maskeert u (het verbergen) om het even welk element dat minder dan 0.1% van het totale aantal paginameningen heeft en toont om het even welk element dat meer dan 0.1% van het totale aantal paginameningen heeft. Als u 0% klikt, maskeert u alle elementen met een waarde van 0 (nul) voor geselecteerde metrisch.
