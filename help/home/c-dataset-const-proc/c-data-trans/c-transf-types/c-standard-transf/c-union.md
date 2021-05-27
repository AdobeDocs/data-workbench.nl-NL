---
description: De Unietransformatie neemt een reeks invoer en maakt een vector van tekenreeksen als uitvoer.
title: Unie
uuid: 2f8bd332-727e-4a4e-a3e7-a52ea2b0a33a
exl-id: 841b5133-d587-409c-b39e-47169beb2ddf
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '262'
ht-degree: 1%

---

# Unie{#union}

De Unietransformatie neemt een reeks invoer en maakt een vector van tekenreeksen als uitvoer.

Als een van de invoeren zelf een vector is, wordt elk element in de invoervector gekoppeld aan één element in de uitvoervector (met andere woorden, de transformatie maakt geen vector van vectoren).

| Parameter | Beschrijving | Standaard |
|---|---|---|
| Naam | Beschrijvende naam van de transformatie. U kunt hier elke naam invoeren. |  |
| Opmerkingen | Optioneel. Opmerkingen over de transformatie. |  |
| Voorwaarde | De omstandigheden waaronder deze transformatie wordt toegepast. |  |
| Standaard | De standaardwaarde die moet worden gebruikt als aan de voorwaarde is voldaan en de invoerwaarde niet beschikbaar is. |  |
| Invoer | Een of meer invoerwaarden. |  |
| Uitvoer | De naam van het uitvoerveld. |  |

In dit voorbeeld worden gegevensvelden van websiteverkeer gebruikt om een lijst te maken met de postcodes die aan de bezoekers van de website zijn gekoppeld (dat wil zeggen, binnen elk logbestandvermelding). De gegevens bieden twee mogelijke bronnen voor deze informatie: één in cs-uri-query en andere op een [!DNL zipcode] gebied van het koekje. Als geen van deze velden een postcode bevat, wordt de standaardwaarde 00000 gebruikt.

![](assets/cfg_TransformationType_Union.png)

Hoewel het mogelijk is dat beide waarden beschikbaar zijn in één logbestandvermelding, kunt u selecteren welke waarde moet worden gebruikt wanneer u een dimensie maakt op basis van de uitvoer van de transformatie. Doorgaans maakt u een eenvoudige afmeting waarbij de eerste of laatste van de ondervonden waarden wordt gebruikt. Zie [Uitgebreide Dimension](../../../../../home/c-dataset-const-proc/c-ex-dim/c-abt-ex-dim.md) voor informatie over het maken van eenvoudige afmetingen.
