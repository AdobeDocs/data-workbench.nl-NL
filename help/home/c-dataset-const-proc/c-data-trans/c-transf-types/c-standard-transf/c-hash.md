---
description: De transformatie van de Hash leidt tot een bijna uniek koord dat een aantal met 64 bits van de inputwaarden vertegenwoordigt.
solution: Analytics
title: Hash
topic: Data workbench
uuid: 13bc14e6-75e2-4711-8f98-50fd18802be5
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Hash{#hash}

De transformatie van de Hash leidt tot een bijna uniek koord dat een aantal met 64 bits van de inputwaarden vertegenwoordigt.

Deze transformatie verstrekt de zelfde knoeiboelwaarde wanneer gegeven de zelfde input.

>[!NOTE]
>
>De resulterende waarde is bijna uniek omdat de transformatie een aantal met 64 bits als ruimte van mogelijke knoeiboelwaarden gebruikt. Voor één miljoen unieke inputs voor de [!DNL hash] transformatie is er een kans van 1 op de 38.000.000 om een dubbele knoeiboelwaarde te krijgen.

| Parameter | Beschrijving | Standaard |
|---|---|---|
| Naam | Beschrijvende naam van de transformatie. U kunt om het even welke naam hier ingaan. |  |
| Opmerkingen | Optioneel. Opmerkingen over de transformatie. |  |
| Toestand | De omstandigheden waaronder deze transformatie wordt toegepast. |  |
| Standaard | De standaardwaarde om te gebruiken als de inputwaarde niet beschikbaar is. |  |
| Ingangen | De reeks input aan gebruik om de knoeiboelwaarde tot stand te brengen. |  |
| Uitvoer | De naam van het gebied voor output. |  |

In dit voorbeeld, worden de waarden van c-ip en cs (gebruiker-agent) gebieden gebruikt om een volgende identiteitskaart tot stand te brengen, die op het x-trackingid gebied wordt opgeslagen.

![](assets/cfg_TransformationType_Hash.png)

>[!NOTE]
>
>Dit voorbeeld vertegenwoordigt geen ideale oplossing voor het creëren van unieke volgende IDs. Nochtans, in situaties waarin de informatie van het archieflogboek wordt gebruikt, kan het de beste methode zijn.

