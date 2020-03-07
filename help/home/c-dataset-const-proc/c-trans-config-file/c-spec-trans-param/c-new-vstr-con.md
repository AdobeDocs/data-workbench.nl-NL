---
description: De nieuwe voorwaarde van de Bezoeker is een Verrichting van de Voorwaarde die met websitegegevens wordt gebruikt om te bepalen welke bezoekers voor opneming in de dataset worden overwogen.
solution: Analytics
title: Nieuwe bezoekersvoorwaarde
topic: Data workbench
uuid: e9733109-5bf3-47ce-974c-d68264291f19
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Nieuwe bezoekersvoorwaarde{#new-visitor-condition}

De nieuwe voorwaarde van de Bezoeker is een Verrichting van de Voorwaarde die met websitegegevens wordt gebruikt om te bepalen welke bezoekers voor opneming in de dataset worden overwogen.

Het [!DNL New Visitor Condition] bepaalt de eerste logboekingang (die door tijd wordt bevolen) voor een bezoeker die in de dataset moet worden gebruikt, en alle verdere logboekingangen voor deze bezoeker zijn inbegrepen in de dataset ongeacht of zij aan deze voorwaarde voldoen. Omdat het [!DNL New Visitor Condition] vereist dat het gegeven door bezoeker en tijd wordt bevolen, wordt het toegepast slechts tijdens de transformatiefase van datasetconstructie.

De [!DNL New Visitor Condition] getoonde in dit voorbeeld leidt tot een dataset die slechts die logboekingangen voor bezoekers omvat die aan e-mailcampagnes antwoorden. Dit wordt verwezenlijkt door de [!DNL NotEmptyCondition] test (zie [niet Leeg](../../../../home/c-dataset-const-proc/c-conditions/c-test-ops/c-test-op-con.md#section-1decb9d887894073a1b6b3d985729ac8)) en het [!DNL x-campaign-email] gebied als input aan de regelmatige uitdrukking te gebruiken. Nadat de nieuwe bezoekers die aan de voorwaarde voldoen worden geïdentificeerd, worden alle logboekingangen voor die bezoekers gevangen.

![](assets/cfg_Transformation_NewVisitorCondition.png)

