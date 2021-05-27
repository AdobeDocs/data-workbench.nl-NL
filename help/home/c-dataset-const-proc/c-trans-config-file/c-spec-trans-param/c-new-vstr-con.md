---
description: De nieuwe voorwaarde van de Bezoeker is een Bewerking van de Voorwaarde die met websitegegevens wordt gebruikt om te bepalen welke bezoekers voor opneming in de dataset worden overwogen.
title: Nieuwe voorwaarde bezoeker
uuid: e9733109-5bf3-47ce-974c-d68264291f19
exl-id: a0520edd-bde3-4f55-858c-8974d4224435
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '175'
ht-degree: 0%

---

# Nieuwe bezoekervoorwaarde{#new-visitor-condition}

De nieuwe voorwaarde van de Bezoeker is een Bewerking van de Voorwaarde die met websitegegevens wordt gebruikt om te bepalen welke bezoekers voor opneming in de dataset worden overwogen.

[!DNL New Visitor Condition] bepaalt de eerste logboekingang (die door tijd wordt bevolen) voor een bezoeker die in de dataset moet worden gebruikt, en alle verdere logboekingangen voor deze bezoeker zijn inbegrepen in de dataset ongeacht of zij aan deze voorwaarde voldoen. Omdat [!DNL New Visitor Condition] vereist dat de gegevens door bezoeker en tijd worden bevolen, wordt het toegepast slechts tijdens de transformatiefase van datasetconstructie.

In het voorbeeld [!DNL New Visitor Condition] wordt een gegevensset gemaakt die alleen die logbestandvermeldingen bevat voor bezoekers die reageren op e-mailcampagnes. Dit wordt verwezenlijkt door [!DNL NotEmptyCondition] test (zie [Niet Leeg](../../../../home/c-dataset-const-proc/c-conditions/c-test-ops/c-test-op-con.md#section-1decb9d887894073a1b6b3d985729ac8)) en het [!DNL x-campaign-email] gebied als input aan de regelmatige uitdrukking te gebruiken. Nadat de nieuwe bezoekers die aan de voorwaarde voldoen, zijn geïdentificeerd, worden alle logboekingangen voor die bezoekers gevangen.

![](assets/cfg_Transformation_NewVisitorCondition.png)
