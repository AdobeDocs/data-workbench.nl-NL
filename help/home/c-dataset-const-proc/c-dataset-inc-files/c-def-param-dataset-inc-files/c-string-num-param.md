---
description: Tekenreeks en numerieke parameters nemen als hun waarden tekenreeksen en getallen.
title: Tekenreeks en numerieke parameters
uuid: 2840967e-dd9e-40b2-91e4-3fdfa38f88e7
exl-id: 37d004da-cde7-4b67-b0cb-0acbb6d8ad68
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 0%

---

# Tekenreeks en numerieke parameters{#string-and-numeric-parameters}

Tekenreeks en numerieke parameters nemen als hun waarden tekenreeksen en getallen.

U kunt ze onderling gebruiken, maar numerieke parameters moeten worden gedefinieerd om een numerieke waarde te hebben. U kunt naar tekenreeks en numerieke parameters verwijzen wanneer u transformaties, voorwaarden en uitgebreide afmetingen definieert en u kunt naar meerdere parameters op dezelfde regel verwijzen.

U kunt niet naar tekenreeks en numerieke parameters verwijzen in [!DNL Input]- of [!DNL Output]-velden, maar u kunt een tekenreeksparameter gebruiken om een constant invoerveld te definiëren. Bovendien kunt u niet naar tekenreeks en numerieke parameters in decoders of decoderingsgroepen verwijzen.

In dit voorbeeld wordt een [!DNL Log Processing Dataset Include]-bestand getoond dat een tekenreeksparameter en een numerieke parameter definieert. De tekenreeksparameter, genaamd &quot;Value Lookups&quot;, definieert een bestandslocatie (Lookups\Values) ten opzichte van de installatiemap van de gegevenswerkbankserver.

![](assets/cfg_Parameters_StringNumeric.png)
