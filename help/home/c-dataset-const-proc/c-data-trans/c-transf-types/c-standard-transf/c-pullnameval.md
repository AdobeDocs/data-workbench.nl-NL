---
description: De transformatie PullNameValues is een speciale verrichting die de waarden op cs-uri-vraag gebied neemt en elk van de naam-waarde paren in een afzonderlijk koord scheidt.
solution: Analytics
title: PullNameValues
topic: Data workbench
uuid: b24db987-78e8-4afc-9113-89aedc0170b2
translation-type: tm+mt
source-git-commit: 27600561841db3705f4eee6ff0aeb8890444bbc9

---


# PullNameValues{#pullnamevalues}

De transformatie PullNameValues is een speciale verrichting die de waarden op cs-uri-vraag gebied neemt en elk van de naam-waarde paren in een afzonderlijk koord scheidt.

De volledige inzameling van naam-waarde paarkoorden is output op het gespecificeerde outputgebied als vector van koorden.

| Parameter | Beschrijving | Standaard |
|---|---|---|
| Naam | Beschrijvende naam van de transformatie. U kunt om het even welke naam hier ingaan. |  |
| Opmerkingen | Optioneel. Opmerkingen over de transformatie. |  |
| Toestand | De omstandigheden waaronder deze transformatie wordt toegepast. |  |
| Standaard | De standaardwaarde aan gebruik als de voorwaarde wordt voldaan aan en de inputwaarde is niet beschikbaar in de bepaalde logboekingang. |  |
| Uitvoer | De naam van het outputkoord. |  |

De [!DNL PullNameValues] transformatie wordt gebruikt in dit voorbeeld om het gebruik van bezoekers van het onderzoeksformulier te vangen: welke knopen werden geselecteerd, welke waarden in de vorm werden getypt, etc. Het voorbeeld gebruikt een [!DNL String Match] voorwaarde (zie [Voorwaarden](../../../../../home/c-dataset-const-proc/c-conditions/c-abt-cond.md)) om het gebruik van deze transformatie aan slechts de pagina te isoleren [!DNL /search.php]. De vector van naam-waarde paren is output in het gebied x-onderzoek-names.

![](assets/cfg_TransformationType_PullNameValues.png)

Gebruikend de transformatie zoals hierboven bepaald, als het cs-uri-stengebied de pagina [!DNL /search.php] en cs-uri-vraag aanpast bevatte het volgende:

* Searchfor=Bob&amp;State=Virginia&amp;isMale=true

dan zou x-onderzoek-noemt een vector bevatten die de volgende drie koorden bevat:

* Searchfor=Bob
* State=Virginia
* isMale=true

