---
description: Een server van de gegevenswerkbank krijgt zich van een bron van gegevens, zoals een Sensor, bewust wanneer het gegevens van die bron ontvangt.
title: '''Vanaf''-tijd begrijpen'
uuid: a1853573-e77c-41f7-8b99-2843e38cc82d
exl-id: 58ea5c6f-de6b-48d2-b573-f265857026da
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '275'
ht-degree: 0%

---

# Begrijpen &quot;vanaf&quot; tijd{#understanding-as-of-time}

Een server van de gegevenswerkbank krijgt zich van een bron van gegevens, zoals een Sensor, bewust wanneer het gegevens van die bron ontvangt.

De &#39;Op tijd&#39; is een garantie dat de [!DNL data workbench server] gegevens heeft voor alle gegevensbronnen waarvan het op de hoogte is.

Laten we zeggen dat we een set van drie [!DNL Sensors] hebben die gegevens naar een [!DNL data workbench server] verzenden: WEB1, WEB2, en WEB3. Aangezien [!DNL data workbench server] de gegevens van deze [!DNL Sensors] ontvangt en verwerkt, komt het automatisch om gegevens van elk van deze bronnen te verwachten. Met Als van tijd geeft u de laatste keer aan dat de [!DNL data workbench server] gegevens van deze drie bronnen heeft ontvangen.

In praktische termen, [!DNL data workbench server] geeft slechts om aangezien van tijd en niet wat &quot;wandtijd,&quot;of de tijd van een klok op de muur zou kunnen worden bedoeld. De [!DNL data workbench server] kent de tijd slechts als van tijd. Dit is met name van belang voor rapportagedoeleinden, aangezien het garandeert dat rapporten altijd op basis van het tijdstip worden uitgevoerd, hetgeen ervoor zorgt dat rapporten met alleen gedeeltelijke gegevens nooit naar eindgebruikers van het systeem kunnen worden verzonden.

[!DNL data workbench server] gebruikt gegevens die van de zender worden verzonden om het per tijd te verstrekken, of het om daadwerkelijke gegevens die van de website of periodieke hartslagen worden verzameld die door uw [!DNL Sensors] worden verzonden zijn. Deze hartslagen hebben twee doelen:

1. Om een blijvende verbinding van HTTP/1.1 open tussen [!DNL Sensor] en [!DNL data workbench server] te houden.

1. Als u wilt dat de functie &#39;Op tijd&#39; actueel blijft wanneer het websiteverkeer niet wordt verzameld en naar [!DNL data workbench server] wordt verzonden.
