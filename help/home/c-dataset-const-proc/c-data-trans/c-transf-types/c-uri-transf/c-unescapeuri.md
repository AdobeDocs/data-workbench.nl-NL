---
description: De transformatie van URI Unescape maakt om het even welke karakters in een koord vrij die zijn ontsnapt.
solution: Analytics
title: UnescapeURI
topic: Data workbench
uuid: 25e87cc7-812d-4d77-be94-16093e8955fe
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# UnescapeURI{#unescapeuri}

De transformatie van URI Unescape maakt om het even welke karakters in een koord vrij die zijn ontsnapt.

>[!NOTE]
>
>De geëscaleerde karakters vervangen de onveilige karakters in een koord van URI. Zij worden vertegenwoordigd door een triplet die uit een percententeken bestaat dat door twee hexadecimale cijfers wordt gevolgd (bijvoorbeeld, %20).

| Parameter | Beschrijving | Standaard |
|---|---|---|
| Naam | Beschrijvende naam van de transformatie. U kunt om het even welke naam hier ingaan. |  |
| Opmerkingen | Optioneel. Opmerkingen over de transformatie. |  |
| Toestand | De omstandigheden waaronder deze transformatie wordt toegepast. |  |
| Standaard | De standaardwaarde om te gebruiken als aan de voorwaarde wordt voldaan en de inputwaarde niet beschikbaar is. |  |
| Invoer | Het koord van URI dat moet zijn unescaped. |  |
| Uitvoer | De naam van het gebied waarin het unescaped koord moet worden opgeslagen. |  |

De volgende transformatie ontspant de docname waarde op een HTTP- kopbalgebied en slaat de output op het gebied x-docname-unescaped op:

![](assets/cfg_TransformationType_UnescapeURI.png)

Als de docname-waarde

* [!DNL mysite.net/lending%20and%20leasing%20forms/document%20library/credit%20application.doc]

dan zou de waarde van x-docname-unescape zijn

* [!DNL mysite.net/lending and leasing forms/document library/credit application.doc]

