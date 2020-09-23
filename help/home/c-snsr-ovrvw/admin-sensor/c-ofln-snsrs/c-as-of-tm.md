---
description: Een server van de gegevenswerkbank krijgt zich van een bron van gegevens, zoals een Sensor, bewust wanneer het gegevens van die bron ontvangt.
solution: Analytics
title: '''Vanaf''-tijd begrijpen'
uuid: a1853573-e77c-41f7-8b99-2843e38cc82d
translation-type: tm+mt
source-git-commit: 34cdcfc83ae6bb620706db37228e200cff43ab2c
workflow-type: tm+mt
source-wordcount: '275'
ht-degree: 0%

---


# &#39;Vanaf&#39;-tijd begrijpen{#understanding-as-of-time}

Een server van de gegevenswerkbank krijgt zich van een bron van gegevens, zoals een Sensor, bewust wanneer het gegevens van die bron ontvangt.

De termijn is een garantie dat de gegevens [!DNL data workbench server] beschikbaar zijn voor alle gegevensbronnen waarvan zij op de hoogte is.

Laten we zeggen dat we een reeks van drie hebben [!DNL Sensors] die gegevens naar een [!DNL data workbench server]: WEB1, WEB2, en WEB3. Aangezien [!DNL data workbench server] ontvangt en de gegevens van deze verwerkt [!DNL Sensors], komt het automatisch om gegevens van elk van deze bronnen te verwachten. Met Als van tijd wijst op de laatste tijd dat de [!DNL data workbench server] ontvangen gegevens van alle drie van deze bronnen.

In praktische termen, geeft de [!DNL data workbench server] enige bekommernis over Eind van tijd en niet wat als &quot;muur tijd,&quot;of de tijd van een klok op de muur zou kunnen worden bedoeld. De [!DNL data workbench server] persoon kent de tijd alleen als &#39;Eind&#39;. Dit is met name van belang voor rapportagedoeleinden, aangezien het garandeert dat rapporten altijd op basis van het tijdstip worden uitgevoerd, hetgeen ervoor zorgt dat rapporten met alleen gedeeltelijke gegevens nooit naar eindgebruikers van het systeem kunnen worden verzonden.

De [!DNL data workbench server] gegevens die door de zender zijn verzonden, worden gebruikt om de gegevens op tijd te leveren, ongeacht of het gaat om feitelijke gegevens die van de website zijn verzameld of om periodieke hartslagen die door uw [!DNL Sensors]afzender zijn verzonden. Deze hartslagen hebben twee doelen:

1. Om een blijvende verbinding van HTTP/1.1 open tussen [!DNL Sensor] en [!DNL data workbench server]te houden.

1. Zo zorgt u ervoor dat de functie Na-tijd actueel blijft voor het geval dat websiteverkeer niet wordt verzameld en naar de [!DNL data workbench server]website wordt verzonden.

