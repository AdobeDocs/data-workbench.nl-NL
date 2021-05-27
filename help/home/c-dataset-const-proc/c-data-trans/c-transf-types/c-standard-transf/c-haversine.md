---
description: In wiskunde, is de haversine formule een vergelijking die cirkelafstanden tussen twee punten op een bol geeft die van hun lengte en breedtegraad worden geïdentificeerd.
title: Haversine
uuid: 835fa9dd-db70-4498-a03e-59595bc041fe
exl-id: e700c0a0-1a1a-4c56-bb4f-1deb1b39b059
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '235'
ht-degree: 1%

---

# Haversine{#haversine}

In wiskunde, is de haversine formule een vergelijking die cirkelafstanden tussen twee punten op een bol geeft die van hun lengte en breedtegraad worden geïdentificeerd.

Net als de formule vereist de [!DNL Haversine]-transformatie twee sets [!DNL Latitude]- en [!DNL Longitude]-instellingen, waarbij deze vier ingangen worden gebruikt om de werkelijke afstand over de aarde tussen twee locaties te berekenen.

Deze afstand kan worden weergegeven als kilometers of als kilometers door de markering &quot;In kilometer&quot; te wijzigen van false in true.

![](assets/cfg_TransformationType_Haversine.png)

| Parameter | Beschrijving | Standaard |
|---|---|---|
| Naam | Beschrijvende naam van de transformatie. U kunt hier elke naam invoeren. |  |
| Opmerkingen | Optioneel. Opmerkingen over de transformatie. |  |
| Voorwaarde | De omstandigheden waaronder deze transformatie wordt toegepast. |  |
| Veld Latitude 1 | De breedtegraad van punt 1. |  |
| Latitude 2-veld | De breedtegraad van punt 2. |  |
| Lengtegraad 1 veld | De lengtegraad van punt 1. |  |
| Veld Lengtegraad 2 | De lengtegraad van punt 2. |  |
| Uitvoer | Na berekening bevat het veld [!DNL Output] afstanden tussen de punten die als elementen in een Dimension zijn opgegeven. |  |

Als voorbeeld, als u in een breedtegraad en lengtegraad van hun opslag als Lat1 codeert, Lon1 en een IP raadpleging lang en lang voor hun klanten gebruikt, dan kunnen de afstanden aan een opslag die de meeste klanten kopen van of komen van worden bepaald.

>[!NOTE]
>
>Als u afstanden voor andere locaties wilt identificeren, moet elke afzonderlijke locatie een eigen set latente en lange velden hebben.
