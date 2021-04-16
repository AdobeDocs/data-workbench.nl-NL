---
description: De Server van het Inzicht laat u toe om telbare, eenvoudige, veel-aan-vele, numerieke, ontvormende, en tijddimensies voor opneming in uw gegevensreeks te bepalen.
title: Typen uitgebreide Dimension
uuid: 68f42903-0599-43f2-8b5b-da9e171d77b1
exl-id: 13a52ece-b68b-45bc-ac2d-d68c91742c9d
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '305'
ht-degree: 0%

---

# Typen uitgebreide Dimension{#types-of-extended-dimensions}

De Server van het Inzicht laat u toe om telbare, eenvoudige, veel-aan-vele, numerieke, ontvormende, en tijddimensies voor opneming in uw gegevensreeks te bepalen.

Elk dimensietype heeft een reeks parameters waarvan waarden u uitgeeft om specifieke instructies voor de Server van het Inzicht te verstrekken om de afmetingen tijdens de transformatiefase van de bouw van gegevensreeks tot stand te brengen.

Hoewel sommige parameters verschillen tussen de dimensietypen, vereisen allen de specificatie van een ouderafmeting (de parameter van de Ouder). De ouderafmeting bepaalt welke logboekingangen van de logboekbronnen als input aan de nieuwe afmeting worden verstrekt. Met andere woorden, de logboekingangen die met de elementen van de ouderafmeting worden geassocieerd zijn degenen die met de nieuwe afmeting worden geassocieerd alvorens om het even welk filtreren wordt toegepast. De ouderafmeting bepaalt ook de positie van de nieuwe afmeting binnen de hiërarchie van de gegevensreeks, die als het schema van de gegevensreeks wordt bedoeld. Voor informatie over de interface die het schema van de gegevensreeks toont, zie [Hulpmiddelen van de Configuratie van de Dataset](../../../../home/c-dataset-const-proc/c-dataset-config-tools/c-dataset-config-tools.md#concept-6e058b7691834cf79dcfd1573f78d4f5).

Nadat de Server van het Inzicht de ouderafmeting gebruikt om te bepalen welke logboekingangen in de verwezenlijking van de afmeting zouden moeten worden overwogen, past het de gespecificeerde voorwaarde(n) (de parameter van de Voorwaarde) op leeg de logboekingangen toe die niet aan de voorwaarde voldoen. De server identificeert vervolgens de waarde van het opgegeven invoerveld (de invoerparameter) voor elke logbestandvermelding en past de opgegeven bewerking (de bewerkingsparameter) toe, indien van toepassing.

>[!NOTE]
>
>Als een logboekingang niet aan de Uitgebreide Voorwaarde van een afmeting voldoet, vervangt de Server van het Inzicht lege waarden voor alle gebieden in de logboekingang. De daadwerkelijke logboekingang bestaat nog, en de gespecificeerde Verrichting bepaalt of de lege waarde van het [!DNL Input] gebied wordt gebruikt.
