---
description: De server van het Inzicht laat u toe om telbare, eenvoudige, veel-aan-velen, numerieke, denormale, en tijddimensies voor opneming in uw gegevensreeks te bepalen.
solution: Analytics
title: Typen uitgebreide afmetingen
topic: Data workbench
uuid: 68f42903-0599-43f2-8b5b-da9e171d77b1
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Typen uitgebreide afmetingen{#types-of-extended-dimensions}

De server van het Inzicht laat u toe om telbare, eenvoudige, veel-aan-velen, numerieke, denormale, en tijddimensies voor opneming in uw gegevensreeks te bepalen.

Elk afmetingstype heeft een reeks parameters de waarvan waarden u uitgeeft om specifieke instructies voor de Server van het Inzicht te verstrekken om de afmetingen tijdens de transformatiefase van de bouw van de gegevensreeks tot stand te brengen.

Terwijl sommige van de parameters tussen de afmetingstypes verschillen, vereisen allen de specificatie van een ouderafmeting (de parameter van de Ouder). De ouderdimensie bepaalt welke logboekingangen van de logboekbronnen als input aan de nieuwe dimensie worden verstrekt. Met andere woorden, zijn de logboekingangen die met de elementen van de ouderafmeting worden geassocieerd degenen die met de nieuwe afmeting worden geassocieerd alvorens om het even welk filtreren wordt toegepast. De ouderdimensie bepaalt ook de positie van de nieuwe dimensie binnen de hiërarchie van de gegevensreeks, die als het schema van de gegevensreeks wordt bedoeld. Voor informatie over de interface die het schema van de gegevensreeks toont, zie de Hulpmiddelen [van de Configuratie van de](../../../../home/c-dataset-const-proc/c-dataset-config-tools/c-dataset-config-tools.md#concept-6e058b7691834cf79dcfd1573f78d4f5)Dataset.

Nadat de server van het Inzicht de ouderafmeting gebruikt om te bepalen welke logboekingangen in de verwezenlijking van de afmeting zouden moeten worden overwogen, past het de gespecificeerde voorwaarde(n) (de parameter van de Voorwaarde) op leeg de logboekingangen toe die niet aan de voorwaarde voldoen. De server identificeert dan de waarde van het gespecificeerde inputgebied (de parameter van de Input) voor elke logboekingang en past de gespecificeerde verrichting (de parameter van de Verrichting) toe, indien toepasselijk.

>[!NOTE]
>
>Als een logboekingang niet aan de Voorwaarde van een uitgebreide dimensie voldoet, substitueert de Server van het Inzicht lege waarden voor alle gebieden in de logboekingang. De daadwerkelijke logboekingang bestaat nog, en de gespecificeerde Verrichting bepaalt of de lege waarde van het [!DNL Input] gebied wordt gebruikt.

