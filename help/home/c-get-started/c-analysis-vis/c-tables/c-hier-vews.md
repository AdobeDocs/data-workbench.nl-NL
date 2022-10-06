---
description: Hiërarchieweergaven zijn alleen beschikbaar wanneer u de site of HBX toepassing gebruikt.
title: Hiërarchieweergaven toepassen
uuid: 859a92af-4f7e-4bb5-9a98-917006894301
exl-id: 27a69404-40d3-44ab-bf5c-b2a5d8d836c2
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '363'
ht-degree: 0%

---

# Hiërarchieweergaven toepassen{#apply-hierarchy-views}

{{eol}}

Hiërarchieweergaven zijn alleen beschikbaar wanneer u de site of HBX toepassing gebruikt.

In de hiërarchische weergave worden de pagina&#39;s in een website weergegeven die hiërarchisch op bestandsnaam zijn geordend en alfabetisch zijn gesorteerd. Hoewel nuttig voor analyse zelf, kan de hiërarchiemening ook worden gebruikt aan opstelling dergelijke geavanceerde visualisaties zoals proceskaarten. Voor meer informatie over proceskaarten raadpleegt u [Proceskaarten](../../../../home/c-get-started/c-analysis-vis/c-proc-maps/c-proc-maps.md#concept-880aee224404429785b733a4e80d275e).

>[!NOTE]
>
>Als uw dataset is gevormd om op veelvoudige servers in een cluster in werking te stellen, voor deze eigenschap om behoorlijk te werken, moet uw systeembeheerder aanwijzen welke machinefuncties als uw Centrale Server van de Normalisatie. Voor stappen om dit te doen, zie het hoofdstuk van het Dossier van de Configuratie van de Configuratie van de Verwerking van het Logboek van *Configuratie-handleiding voor gegevensset*.

![](assets/vis_Table_CompareHierarchy.png)

**De hiërarchieweergave in- of uitschakelen**

* Klik vanuit een willekeurige pagina- of URI-visualisatie met de rechtermuisknop op een element of het label van de pagina-dimensie en klik op **[!UICONTROL Hierarchy View]**.

   ![](assets/mnu_Table_HierarchyView.png)

   Er wordt een X weergegeven naast de optie wanneer de optie [!DNL hierarchy view] is actief.

   De hiërarchie wordt ingedeeld in websitesecties en -pagina&#39;s met behulp van een boomstructuur. Secties (knooppunten) kunnen worden uitgebreid of gecondenseerd met het plus- of minteken naast de sectienaam. Afzonderlijke pagina&#39;s hebben geen plus- of minteken.

   ![](assets/vis_Table_HierarchyView_Expanded.png)

## Dimension-elementen maskeren in een hiërarchische weergave {#section-e477c469934846da8d807f92fc2f3ed1}

Maskeren verwijst naar het selecteren van een subset van uw gegevens of een subset van de elementen in een dimensie. U maskeert of verbergt de elementen die u niet in de analyse wilt opnemen. Met de [!DNL Mask] menuopties voor hiërarchische weergaven, selecteert u het minimumpercentage van een metrische waarde dat een element moet worden weergegeven in de visualisatie.

**Gegevens maskeren met de opdracht [!DNL Mask] menuoptie**

1. Klik met de rechtermuisknop op een element of het label van de dimensie en klik op **[!UICONTROL Mask]**.

   ![](assets/mnu_Table_HierarchyView_Masking.png)

1. Klik onder Meer dan op het juiste percentage en klik vervolgens op de metrische waarde die u wilt maskeren.

Als u bijvoorbeeld op 0,1% klikt en vervolgens op Paginaweergaven klikt, maskeert (verbergt) u een element dat minder dan 0,1% van het totale aantal pagina&#39;s weergaven heeft en geeft u een element weer dat meer dan 0,1% van het totale aantal pagina&#39;s weergaven heeft. Als u op 0% klikt, maskeert u alle elementen met een waarde van 0 (nul) voor de geselecteerde metrische waarde.
