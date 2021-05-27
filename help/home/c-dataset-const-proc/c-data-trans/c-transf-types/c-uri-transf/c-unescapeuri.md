---
description: Met de URI-transformatie Unescape worden alle tekens in een tekenreeks die zijn beschermd, verwijderd.
title: UnescapeURI
uuid: 25e87cc7-812d-4d77-be94-16093e8955fe
exl-id: abf20906-5052-4bbe-9ffb-522b850669a6
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 2%

---

# UnescapeURI{#unescapeuri}

Met de URI-transformatie Unescape worden alle tekens in een tekenreeks die zijn beschermd, verwijderd.

>[!NOTE]
>
>Onveilige tekens in een URI-tekenreeks worden vervangen door geneste tekens. Ze worden vertegenwoordigd door een drievoud dat bestaat uit een procentteken gevolgd door twee hexadecimale cijfers (bijvoorbeeld %20).

| Parameter | Beschrijving | Standaard |
|---|---|---|
| Naam | Beschrijvende naam van de transformatie. U kunt hier elke naam invoeren. |  |
| Opmerkingen | Optioneel. Opmerkingen over de transformatie. |  |
| Voorwaarde | De omstandigheden waaronder deze transformatie wordt toegepast. |  |
| Standaard | De standaardwaarde die moet worden gebruikt als aan de voorwaarde is voldaan en de invoerwaarde niet beschikbaar is. |  |
| Invoer | De URI-tekenreeks die moet worden vrijgemaakt. |  |
| Uitvoer | De naam van het veld waarin de niet-beschermde tekenreeks moet worden opgeslagen. |  |

Met de volgende transformatie wordt de waarde van de docname in een HTTP-headerveld vrijgemaakt en wordt de uitvoer opgeslagen in het veld x-docname-unescaped:

![](assets/cfg_TransformationType_UnescapeURI.png)

Als de waarde van de documentnaam

* [!DNL mysite.net/lending%20and%20leasing%20forms/document%20library/credit%20application.doc]

dan zou de waarde x-docname-unescape

* [!DNL mysite.net/lending and leasing forms/document library/credit application.doc]
