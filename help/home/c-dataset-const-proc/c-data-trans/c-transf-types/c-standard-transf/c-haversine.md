---
description: In wiskunde, is de haversine formule een vergelijking die cirkelafstanden tussen twee punten op een gebied geeft dat van hun lengten en breedtegraden wordt geïdentificeerd.
solution: Analytics
title: Haversine
topic: Data workbench
uuid: 835fa9dd-db70-4498-a03e-59595bc041fe
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Haversine{#haversine}

In wiskunde, is de haversine formule een vergelijking die cirkelafstanden tussen twee punten op een gebied geeft dat van hun lengten en breedtegraden wordt geïdentificeerd.

Zoals de formule, vereist de [!DNL Haversine] transformatie twee reeksen [!DNL Latitude] en [!DNL Longitude] montages, gebruikend deze vier input om de ware afstand over de Aarde tussen twee plaatsen te berekenen.

Deze afstand kan worden weergegeven als kilometers of kilometers door de vlag &quot;In Kilometers&quot; te wijzigen van false naar true.

![](assets/cfg_TransformationType_Haversine.png)

| Parameter | Beschrijving | Standaard |
|---|---|---|
| Naam | Beschrijvende naam van de transformatie. U kunt om het even welke naam hier ingaan. |  |
| Opmerkingen | Optioneel. Opmerkingen over de transformatie. |  |
| Toestand | De omstandigheden waaronder deze transformatie wordt toegepast. |  |
| Latitude 1-veld | De breedtegraad van punt 1. |  |
| Latitude 2-veld | De breedtegraad van punt 2. |  |
| Lengtegraad 1 veld | De lengte van punt 1. |  |
| Lengtegraad 2 veld | De lengte van punt 2. |  |
| Uitvoer | Zodra berekend, bevat het [!DNL Output] gebied afstanden tussen de punten die als elementen in een Dimensie worden aangewezen. |  |

Als voorbeeld, als u in een breedte en een lengtegraad van hun opslag als Lat1 codeert, kan Lon1 en een IP raadpleging lang en lang voor hun klanten gebruikt, dan de afstanden aan een opslag de meeste klanten van kopen of van komen worden bepaald.

>[!NOTE]
>
>Als u afstanden voor andere plaatsen wilt identificeren, dan moet elke individuele plaats zijn eigen reeks van lat en lon gebieden hebben.

