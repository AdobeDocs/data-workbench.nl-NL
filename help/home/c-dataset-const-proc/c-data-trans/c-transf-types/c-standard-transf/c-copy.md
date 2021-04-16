---
description: De transformatie van het Exemplaar kopieert eenvoudig de waarde in het inputgebied aan het bepaalde outputgebied. Als het invoerveld een vector met tekenreeksen kan zijn, moet het uitvoerveld beginnen met "x-".
title: Kopiëren
uuid: 073f53bf-befb-4fba-a8f8-260ffcdd007c
exl-id: 04e97006-1e8e-4123-bbbc-b90a5231170f
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '176'
ht-degree: 2%

---

# Kopiëren{#copy}

De transformatie van het Exemplaar kopieert eenvoudig de waarde in het inputgebied aan het bepaalde outputgebied. Als het invoerveld een vector met tekenreeksen kan zijn, moet het uitvoerveld beginnen met &quot;x-&quot;.

| Parameter | Beschrijving | Standaard |
|---|---|---|
| Naam | Beschrijvende naam van de transformatie. U kunt hier elke naam invoeren. |  |
| Opmerkingen | Optioneel. Opmerkingen over de transformatie. |  |
| Voorwaarde | De omstandigheden waaronder deze transformatie wordt toegepast. |  |
| Standaard | Wordt gebruikt als de voorwaarde true is en de invoerwaarde niet beschikbaar is in het opgegeven logbestand. |  |
| Invoer | De naam van het veld waaruit moet worden gekopieerd. |  |
| Uitvoer | De naam van het uitvoerveld. |  |

In dit voorbeeld, dat velden gebruikt van gegevens die zijn verzameld uit websiteverkeer, krijgt het uitvoerveld, x-purchase-success, de letterlijke waarde &quot;1&quot; telkens wanneer cs-uri-stem overeenkomt met [!DNL /checkout/confirmed.php]. Als [!DNL Condition] niet tevreden is (dat wil zeggen, cs-uri-stem niet [!DNL /checkout/confirmed.php]), wordt x-purchase-success niet veranderd.

![](assets/cfg_TransformationType_Copy.png)
