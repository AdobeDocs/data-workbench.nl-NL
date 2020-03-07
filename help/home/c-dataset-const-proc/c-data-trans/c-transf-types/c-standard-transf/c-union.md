---
description: De transformatie van de Unie neemt een reeks input en leidt tot een vector van koorden als output.
solution: Analytics
title: Unie
topic: Data workbench
uuid: 2f8bd332-727e-4a4e-a3e7-a52ea2b0a33a
translation-type: tm+mt
source-git-commit: 27600561841db3705f4eee6ff0aeb8890444bbc9

---


# Unie{#union}

De transformatie van de Unie neemt een reeks input en leidt tot een vector van koorden als output.

Als één van de input zelf een vector is, wordt elk element in de inputvector geassocieerd met één element in de outputvector (d.w.z., leidt de transformatie tot geen vector van vectoren).

| Parameter | Beschrijving | Standaard |
|---|---|---|
| Naam | Beschrijvende naam van de transformatie. U kunt om het even welke naam hier ingaan. |  |
| Opmerkingen | Optioneel. Opmerkingen over de transformatie. |  |
| Toestand | De omstandigheden waaronder deze transformatie wordt toegepast. |  |
| Standaard | De standaardwaarde om te gebruiken als aan de voorwaarde wordt voldaan en de inputwaarde niet beschikbaar is. |  |
| Ingangen | Één of meerdere inputwaarden. |  |
| Uitvoer | De naam van het outputgebied. |  |

Dit voorbeeld gebruikt gebieden van gegevens van websiteverkeer om een lijst van de postcodes tot stand te brengen verbonden aan de bezoekers van de website (namelijk, binnen elke logboekingang). De gegevens verstrekken twee mogelijke bronnen voor deze informatie: één in cs-uri-vraag en andere op een [!DNL zipcode] gebied van het koekje. Als geen van beide gebieden een postcode bevat, wordt de standaardwaarde van 00000 gebruikt.

![](assets/cfg_TransformationType_Union.png)

Terwijl het voor beide waarden mogelijk is om in één enkele logboekingang beschikbaar te zijn, kunt u selecteren welke waarde aan gebruik wanneer u een afmeting creeert die op de output van de transformatie wordt gebaseerd. In een typisch gebruiksgeval, zou u een eenvoudige afmeting tot stand brengen die of eerste of laatste van de ondervonden waarden neemt. Voor informatie over het creëren van eenvoudige afmetingen, zie [Uitgebreide Afmetingen](../../../../../home/c-dataset-const-proc/c-ex-dim/c-abt-ex-dim.md).
