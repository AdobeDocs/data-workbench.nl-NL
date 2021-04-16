---
description: Bij de transformatie Afvlakken wordt een vector met tekenreeksen gebruikt en wordt elke waarde toegewezen aan een eigen veld.
title: Afvlakken
uuid: 00b06a5c-506b-45fe-9773-44d65b8ec233
exl-id: 63f3e4bc-238f-4e15-8ae5-2f805bd080d3
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '223'
ht-degree: 1%

---

# Afvlakken{#flatten}

Bij de transformatie Afvlakken wordt een vector met tekenreeksen gebruikt en wordt elke waarde toegewezen aan een eigen veld.

| Parameter | Beschrijving | Standaard |
|---|---|---|
| Naam | Beschrijvende naam van de transformatie. U kunt hier elke naam invoeren. |  |
| Opmerkingen | Optioneel. Opmerkingen over de transformatie. |  |
| Voorwaarde | De omstandigheden waaronder deze transformatie wordt toegepast. |  |
| Standaard | De standaardwaarde die moet worden gebruikt als aan de voorwaarde is voldaan en de invoerwaarde niet beschikbaar is voor de logbestandvermelding. |  |
| Invoer | Een vector met tekenreekswaarden die worden toegewezen aan de namen van uitvoervelden. |  |
| Uitvoer | Een set namen van uitvoervelden. |  |

Overwegingen voor [!DNL Flatten]

* Als de invoervector meer waarden bevat dan er gedefinieerde uitvoervelden zijn, gaan de extra invoerwaarden gewoon verloren.
* Als de invoervector minder waarden bevat dan er gedefinieerde uitvoervelden zijn, krijgen de extra uitvoervelden de standaardwaarde (indien gedefinieerd) of een lege tekenreeks als er geen standaardwaarde is gedefinieerd.

Hier wordt de [!DNL Flatten]-transformatie gebruikt om een vector met producten (x-producten) te nemen en deze in vier velden te scheiden (x-product1, ..., x-product4).

![](assets/cfg_TransformationType_Flatten.png)

Als de invoerwaarde de tekenreeksen B57481, C46355 en Z97123 bevatte, zouden de uitvoervelden de hier getoonde waarden hebben:

* x-product1 = B57481
* x-product2 = C46355
* x-product3 = Z97123
* x-product4 = Leeg (Er zijn meer invoeren dan uitvoer en er is geen standaardwaarde opgegeven.)
