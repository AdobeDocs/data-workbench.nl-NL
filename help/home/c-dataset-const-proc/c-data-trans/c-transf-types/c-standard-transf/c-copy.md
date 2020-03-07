---
description: De transformatie van het Exemplaar kopieert eenvoudig de waarde op het inputgebied aan het bepaalde outputgebied. Als het inputgebied een vector van koorden zou kunnen zijn, moet het outputgebied met "x- beginnen."
solution: Analytics
title: Kopiëren
topic: Data workbench
uuid: 073f53bf-befb-4fba-a8f8-260ffcdd007c
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Kopiëren{#copy}

De transformatie van het Exemplaar kopieert eenvoudig de waarde op het inputgebied aan het bepaalde outputgebied. Als het inputgebied een vector van koorden zou kunnen zijn, moet het outputgebied met &quot;x- beginnen.&quot;

| Parameter | Beschrijving | Standaard |
|---|---|---|
| Naam | Beschrijvende naam van de transformatie. U kunt om het even welke naam hier ingaan. |  |
| Opmerkingen | Optioneel. Opmerkingen over de transformatie. |  |
| Toestand | De omstandigheden waaronder deze transformatie wordt toegepast. |  |
| Standaard | Gebruikt als de voorwaardentest waar is en de inputwaarde niet beschikbaar in de bepaalde logboekingang is. |  |
| Invoer | De naam van het gebied waarvan om te kopiëren. |  |
| Uitvoer | De naam van het outputgebied. |  |

In dit voorbeeld, dat gebieden van gegevens gebruikt die van websiteverkeer worden verzameld, wordt het outputgebied, x-aankoop-succes, gegeven de letterlijke waarde van &quot;1&quot;telkens als cs-uri-stengelijken [!DNL /checkout/confirmed.php]. Als de [!DNL Condition] niet tevreden is (dat wil zeggen dat de cs-uri-stengel niet overeenkomt [!DNL /checkout/confirmed.php]), wordt het x-aankoop-succes niet gewijzigd.

![](assets/cfg_TransformationType_Copy.png)

