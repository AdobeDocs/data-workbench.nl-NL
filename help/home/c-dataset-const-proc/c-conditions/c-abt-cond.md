---
description: Transformaties en dimensies gebruiken voorwaarden om te bepalen wanneer bepaalde instructies of handelingen van toepassing zijn op logvelden.
title: Informatie over voorwaarden
uuid: 882fe761-895c-4226-a019-270c50ae6da2
exl-id: 0d44282f-1327-4f11-90fc-7e6a2ef8dc76
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '149'
ht-degree: 0%

---

# Info Voorwaarden{#about-conditions}

Transformaties en dimensies gebruiken voorwaarden om te bepalen wanneer bepaalde instructies of handelingen van toepassing zijn op logvelden.

De parameter van de Voorwaarde van de Ingang van het Logboek gebruikt voorwaarden om te bepalen welke logboekingangen in het proces van de gegevenssetconstructie zouden moeten worden omvat. In deze bijlage worden de verschillende typen voorwaarden beschreven die beschikbaar zijn binnen de gegevensworkbench-server.

Een voorwaarde valt in één van twee categorieën:

* **[!DNL Test Operations]:** [!DNL Compare],  [!DNL Not Empty],  [!DNL Range],  [!DNL Regular Expression], en de  [!DNL String Match] voorwaarden worden gebruikt om op verschillende staten in de beschikbare logboekgebieden te testen.

* **[!DNL Boolean Operations]:** De  [!DNL And],  [!DNL Or]en  [!DNL Neither] omstandigheden worden gebruikt om de hierboven beschreven testhandelingen te combineren. Als u bijvoorbeeld een voorwaarde [!DNL Range] en een voorwaarde [!DNL String Match] hebt die beide false moeten zijn om de juiste actie uit te voeren, maakt u deze twee bewerkingen onderliggende items van de voorwaarde [!DNL Neither]. De voorwaarde [!DNL And] wordt gebruikt als de basis voor alle voorwaarde-tests in het systeem.
