---
description: De Hash-transformatie maakt een bijna unieke tekenreeks die een 64-bits getal uit de invoerwaarden vertegenwoordigt.
title: Hash
uuid: 13bc14e6-75e2-4711-8f98-50fd18802be5
exl-id: 6912a1d2-9ae8-42ba-94bd-a7a28cbdfae6
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '203'
ht-degree: 1%

---

# Hash{#hash}

De Hash-transformatie maakt een bijna unieke tekenreeks die een 64-bits getal uit de invoerwaarden vertegenwoordigt.

Deze transformatie levert dezelfde hash-waarde op bij dezelfde invoer.

>[!NOTE]
>
>De resulterende waarde is bijna uniek omdat bij de transformatie een 64-bits getal wordt gebruikt als de ruimte van mogelijke hashwaarden. Voor één miljoen unieke input aan de [!DNL hash] transformatie, is er 1 op 38.000.000 kans om een dubbele knoeiboelwaarde te krijgen.

| Parameter | Beschrijving | Standaard |
|---|---|---|
| Naam | Beschrijvende naam van de transformatie. U kunt hier elke naam invoeren. |  |
| Opmerkingen | Optioneel. Opmerkingen over de transformatie. |  |
| Voorwaarde | De omstandigheden waaronder deze transformatie wordt toegepast. |  |
| Standaard | De standaardwaarde die moet worden gebruikt als de invoerwaarde niet beschikbaar is. |  |
| Invoer | De set invoer die moet worden gebruikt om de hashwaarde te maken. |  |
| Uitvoer | De naam van het veld voor uitvoer. |  |

In dit voorbeeld worden de waarden van de velden c-ip en cs (user-agent) gebruikt om een tracking-id te maken. Deze id wordt opgeslagen in het veld x-trackingid.

![](assets/cfg_TransformationType_Hash.png)

>[!NOTE]
>
>Dit voorbeeld is geen ideale oplossing voor het maken van unieke id&#39;s voor bijhouden. In situaties waarin archieflogboekinformatie wordt gebruikt, kan dit echter de beste methode zijn.
