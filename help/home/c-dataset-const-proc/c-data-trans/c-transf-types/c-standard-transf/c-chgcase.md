---
description: Met de ChangeCase-transformatie wordt het hoofdlettergebruik van de tekenreeks in de invoerparameter gewijzigd, zoals opgegeven door de parameter Action.
title: ChangeCase
uuid: 676e79e6-324e-43d1-8982-b44596d0eeac
exl-id: 2002fe22-d31c-4286-9f73-59ef205f1384
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 2%

---

# ChangeCase{#changecase}

{{eol}}

Met de ChangeCase-transformatie wordt het hoofdlettergebruik van de tekenreeks in de invoerparameter gewijzigd, zoals opgegeven door de parameter Action.

| Parameter | Beschrijving | Standaard |
|---|---|---|
| Naam | Beschrijvende naam van de transformatie. U kunt hier elke naam invoeren. |  |
| Handeling | Hoger of lager. Hiermee wordt opgegeven of het hoofdlettergebruik moet worden gewijzigd in een hogere of lagere waarde. | lager |
| Opmerkingen | Optioneel. Opmerkingen over de transformatie. |  |
| Voorwaarde | De omstandigheden waaronder deze transformatie wordt toegepast. |  |
| Invoer | De naam van het veld in het logbestand dat als invoer moet worden gebruikt. |  |
| Uitvoer | De naam van het uitvoerveld. |  |

In dit voorbeeld, dat velden gebruikt met gegevens die zijn verzameld uit websiteverkeer, wordt het hoofdlettergebruik van de tekenreeks in het veld s-dns gewijzigd in kleine letters en wordt de nieuwe waarde uitgevoerd in het nieuwe veld, x-kleine letters-dns.

![](assets/cfg_TransformationType_ChangeCase.png)
