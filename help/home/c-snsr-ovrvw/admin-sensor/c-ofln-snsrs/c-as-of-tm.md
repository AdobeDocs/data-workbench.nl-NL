---
description: Een server van de gegevenswerkbank krijgt zich van een bron van gegevens, zoals een Sensor, bewust wanneer het gegevens van die bron ontvangt.
title: '''Vanaf''-tijd begrijpen'
uuid: a1853573-e77c-41f7-8b99-2843e38cc82d
exl-id: 58ea5c6f-de6b-48d2-b573-f265857026da
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '275'
ht-degree: 0%

---

# &#39;Vanaf&#39;-tijd begrijpen{#understanding-as-of-time}

{{eol}}

Een server van de gegevenswerkbank krijgt zich van een bron van gegevens, zoals een Sensor, bewust wanneer het gegevens van die bron ontvangt.

De termijn is een garantie dat de [!DNL data workbench server] beschikt over gegevens voor alle gegevensbronnen waarvan zij op de hoogte is.

Laten we zeggen dat we een set van drie hebben [!DNL Sensors] die gegevens naar een [!DNL data workbench server]: WEB1, WEB2, en WEB3. Als de [!DNL data workbench server] ontvangt en verwerkt de gegevens van deze [!DNL Sensors]Het komt er automatisch op aan gegevens van elk van deze bronnen te verwachten. Met Als van tijd geeft u de laatste keer aan dat de [!DNL data workbench server] zij hebben gegevens van deze drie bronnen ontvangen.

In de praktijk [!DNL data workbench server] geeft slechts om aangezien van tijd en niet wat &quot;wandtijd,&quot;of de tijd van een klok op de muur zou kunnen worden bedoeld. De [!DNL data workbench server] weet de tijd slechts als van tijd. Dit is met name van belang voor rapportagedoeleinden, aangezien het garandeert dat rapporten altijd worden uitgevoerd op basis van het tijdstip waarop, dat ervoor zorgt dat rapporten met slechts gedeeltelijke gegevens nooit naar eindgebruikers van het systeem kunnen worden verzonden.

De [!DNL data workbench server] gebruikt gegevens die van de zender worden verzonden om het op tijd te verstrekken, of het om daadwerkelijke gegevens die van de website of periodieke hartslagen worden verzameld die door uw worden verzonden zijn [!DNL Sensors]. Deze hartslagen hebben twee doelen:

1. Om een blijvende verbinding van HTTP/1.1 tussen open te houden [!DNL Sensor] en de [!DNL data workbench server].

1. Zo blijft de periode &#39;Op tijd&#39; actueel als het websiteverkeer niet wordt verzameld en naar de [!DNL data workbench server].
