---
description: De transformatie van het Exemplaar kopieert eenvoudig de waarde in het inputgebied aan het bepaalde outputgebied. Als het invoerveld een vector met tekenreeksen kan zijn, moet het uitvoerveld beginnen met "x-".
title: Kopiëren
uuid: 073f53bf-befb-4fba-a8f8-260ffcdd007c
exl-id: 04e97006-1e8e-4123-bbbc-b90a5231170f
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '176'
ht-degree: 2%

---

# Kopiëren{#copy}

{{eol}}

De transformatie van het Exemplaar kopieert eenvoudig de waarde in het inputgebied aan het bepaalde outputgebied. Als het invoerveld een vector met tekenreeksen kan zijn, moet het uitvoerveld beginnen met &quot;x-&quot;.

| Parameter | Beschrijving | Standaard |
|---|---|---|
| Naam | Beschrijvende naam van de transformatie. U kunt hier elke naam invoeren. |  |
| Opmerkingen | Optioneel. Opmerkingen over de transformatie. |  |
| Voorwaarde | De omstandigheden waaronder deze transformatie wordt toegepast. |  |
| Standaard | Wordt gebruikt als de voorwaarde true is en de invoerwaarde niet beschikbaar is in het opgegeven logbestand. |  |
| Invoer | De naam van het veld waaruit moet worden gekopieerd. |  |
| Uitvoer | De naam van het uitvoerveld. |  |

In dit voorbeeld, dat velden gebruikt die zijn verzameld van websiteverkeer, krijgt het uitvoerveld, x-purchase-success, de letterlijke waarde &quot;1&quot; telkens wanneer cs-uri-stem overeenkomt [!DNL /checkout/confirmed.php]. Als de [!DNL Condition] niet tevreden is (dat wil zeggen dat cs-uri-stem niet overeenkomt [!DNL /checkout/confirmed.php]), wordt het succes van de x-aankoop niet gewijzigd.

![](assets/cfg_TransformationType_Copy.png)
