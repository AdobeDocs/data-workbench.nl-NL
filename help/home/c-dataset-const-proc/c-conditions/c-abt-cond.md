---
description: Transformaties en dimensies gebruiken voorwaarden om te bepalen wanneer bepaalde instructies of handelingen van toepassing zijn op logvelden.
title: Informatie over voorwaarden
uuid: 882fe761-895c-4226-a019-270c50ae6da2
exl-id: 0d44282f-1327-4f11-90fc-7e6a2ef8dc76
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '149'
ht-degree: 0%

---

# Informatie over voorwaarden{#about-conditions}

{{eol}}

Transformaties en dimensies gebruiken voorwaarden om te bepalen wanneer bepaalde instructies of handelingen van toepassing zijn op logvelden.

De parameter van de Voorwaarde van de Ingang van het Logboek gebruikt voorwaarden om te bepalen welke logboekingangen in het proces van de gegevenssetconstructie zouden moeten worden omvat. In deze bijlage worden de verschillende typen voorwaarden beschreven die beschikbaar zijn binnen de gegevensworkbench-server.

Een voorwaarde valt in één van twee categorieën:

* **[!DNL Test Operations]:** [!DNL Compare], [!DNL Not Empty], [!DNL Range], [!DNL Regular Expression], en [!DNL String Match] de voorwaarden worden gebruikt om op verschillende staten in de beschikbare logboekgebieden te testen.

* **[!DNL Boolean Operations]:** De [!DNL And], [!DNL Or], en [!DNL Neither] er worden voorwaarden gebruikt om de hierboven beschreven testbewerkingen te combineren. Als u bijvoorbeeld een [!DNL Range] voorwaarde en [!DNL String Match] voorwaarde die zowel vals moet zijn om de aangewezen actie te nemen, zou u deze twee verrichtingenkinderen van [!DNL Neither] voorwaarde. De [!DNL And] De voorwaarde wordt gebruikt als basis voor alle voorwaarde het testen in het systeem.
