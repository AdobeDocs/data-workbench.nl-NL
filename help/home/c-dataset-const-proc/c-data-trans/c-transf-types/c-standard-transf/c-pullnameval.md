---
description: De transformatie PullNameValues is een speciale verrichting die de waarden op cs-uri-vraag gebied neemt en elk van de naam-waarde paren in een afzonderlijke koord scheidt.
title: PullNameValues
uuid: b24db987-78e8-4afc-9113-89aedc0170b2
exl-id: 3660ff6e-87dc-42cf-a897-0e2e0e021c07
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '232'
ht-degree: 1%

---

# PullNameValues{#pullnamevalues}

De transformatie PullNameValues is een speciale verrichting die de waarden op cs-uri-vraag gebied neemt en elk van de naam-waarde paren in een afzonderlijke koord scheidt.

De gehele verzameling van naam-waardepaartekenreeksen wordt als een vector met tekenreeksen uitgevoerd in het opgegeven uitvoerveld.

| Parameter | Beschrijving | Standaard |
|---|---|---|
| Naam | Beschrijvende naam van de transformatie. U kunt hier elke naam invoeren. |  |
| Opmerkingen | Optioneel. Opmerkingen over de transformatie. |  |
| Voorwaarde | De omstandigheden waaronder deze transformatie wordt toegepast. |  |
| Standaard | De standaardwaarde die moet worden gebruikt als aan de voorwaarde is voldaan en de invoerwaarde niet beschikbaar is in het opgegeven logbestand. |  |
| Uitvoer | De naam van de uitvoertekenreeks. |  |

De transformatie [!DNL PullNameValues] wordt in dit voorbeeld gebruikt om het gebruik van het zoekformulier door bezoekers vast te leggen: welke knoppen zijn geselecteerd, welke waarden in het formulier zijn getypt, enzovoort. In het voorbeeld wordt een voorwaarde [!DNL String Match] gebruikt (zie [Voorwaarden](../../../../../home/c-dataset-const-proc/c-conditions/c-abt-cond.md)) om het gebruik van deze transformatie te isoleren tot alleen de pagina [!DNL /search.php]. De vector van naam-waardeparen wordt uitgevoerd in het veld x-search-names.

![](assets/cfg_TransformationType_PullNameValues.png)

Met behulp van de transformatie zoals hierboven gedefinieerd, als het veld cs-uri-stem overeenkomt met de pagina [!DNL /search.php] en cs-uri-query het volgende bevatte:

* Zoekopdracht=Bob&amp;State=Virginia&amp;isMale=true

vervolgens bevatten x-search-names een vector met de volgende drie tekenreeksen:

* Searchfor=Bob
* State=Virginia
* isMale=true
