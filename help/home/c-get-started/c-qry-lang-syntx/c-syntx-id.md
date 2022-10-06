---
description: Metrische expressies, afmetingen en filterexpressies kunnen id's gebruiken om te verwijzen naar benoemde metriek, afmetingen en filters.
title: Syntaxis voor id's
uuid: 9cfa188a-05ca-4163-a268-e33fce9a1929
exl-id: 79bc5585-7b21-4a9d-b044-28ff4bc5a885
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '168'
ht-degree: 0%

---

# Syntaxis voor id&#39;s{#syntax-for-identifiers}

{{eol}}

Metrische expressies, afmetingen en filterexpressies kunnen id&#39;s gebruiken om te verwijzen naar benoemde metriek, afmetingen en filters.

Deze id&#39;s zijn hoofdlettergevoelig en moeten exact worden getypt zoals ze zijn gedefinieerd.

Een geldige id kan een of meer van de volgende elementen bevatten:

* Onderstrepingstekens (_). Onderstrepingstekens in een id vertegenwoordigen spaties in de metrische naam, dimensie of filternaam. De dimensie Sessieverwijzing wordt bijvoorbeeld aangeduid als [!DNL Session_Referrer] in een expressie.
* Percentage tekens (%)
* Hoofdletters (A-Z)
* Kleine letters (a-z)
* Dollar-tekens ($)
* Getallen (0-9), behalve als het eerste teken in een id.
* Niet-ASCII-tekens

Alle andere tekens in een id zijn ongeldig.

Dezelfde regels gelden voor de namen van metriek, afmetingen en filters wanneer deze buiten expressies worden gebruikt, behalve dat namen spaties kunnen bevatten maar geen onderstrepingstekens. U kunt bijvoorbeeld de dimensie Sessieverwijzing definiëren in het dialoogvenster [!DNL Transformation.cfg] bestand als sessieverwijzer, maar niet [!DNL Session_Referrer].
